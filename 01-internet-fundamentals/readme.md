1. Step by step saat user klik google.com di browser sampai halaman muncul
2. Perbedaan HTTP dan HTTPS, dan mengapa HTTPS lebih aman?
3. Apa maksud dari stateless pada HTTP
4. Menyebutkan 4 HTTP method dan kegunaannya
5. Arti dari HTTP status (200, 404, 500, 301)
6. Apa yang dikerjakan oleh DNS, dan analogikan dengan kehidupan sehari hari


1. Saat kita mengetik google.com dan melakukan enter yang terjadi adalah browser akan mengecek terlebih dahulu ke cache lokal, jika tidak ada maka DNS akan mengubah domain menjadi alamat IP, setelah itu browser akan melakukan HTTP request ke alamat ip yang dituju dan setelahnya server ip akan mengirimkan HTTP response yang berisi data yang diperlukan untuk memuat halaman google.

2. HTTPS adalah HTTP yang dienkripsi, mengapa ini lebih aman jika dibandingkan dengan HTTP? karena semisal kita berada pada jaringan publik, orang bisa mengakses data yang sedang kita gunakan, maka dengan enkripsi ini data tidak bisa terbaca oleh orang lain.

3. Stateless pada HTTP berarti antar HTTP request itu independen dan tidak berkaitan, jadi server tidak mengingat HTTP request yang sebelumnya dilakukan.

4. GET = untuk melakukan request ke server
   DELETE = menghapus data
   POST = mengirim data ke server
   PUT = menimpa data

5. 200 (sukses) = oke
   404 (kesalahan dari client) = resources yang diminta tidak ditemukan
   500 (kesalahan dari server) = ada kondisi tidak terduga yang ditemukan
   300 (redirect) = akan dipindahkan ke URL baru

6. DNS bisa disebut sebagai penerjemah yang menerjemahkan nama domain ke alamat ip, karena komputer sejatinya tidak bisa membaca huruf dia hanya bisa membaca angka dan kurang lebih dns bisa dianalogikan dengan buku telepon yang berisi nama (nama domain) dan nomor telepon (alamat ip)



curl -v https://google.com
VERBOSE: GET with 0-byte payload
VERBOSE: received -1-byte response of content type text/html; charset=UTF-8
                                                                                                                                                                                   
Security Warning: Script Execution Risk                                                                                                                                            
Invoke-WebRequest parses the content of the web page. Script code in the web page might be run when the page is parsed.                                                            
      RECOMMENDED ACTION:                                                                                                                                                          
      Use the -UseBasicParsing switch to avoid script code execution.

      Do you want to continue?
    
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): y


StatusCode        : 200
StatusDescription : OK
Content           : <!doctype html><html itemscope="" itemtype="http://schema.org/WebPage" lang="id"><head><meta content="text/html; charset=UTF-8" 
                    http-equiv="Content-Type"><meta content="/images/branding/googleg/1x/goo...
RawContent        : HTTP/1.1 200 OK
                    Content-Security-Policy-Report-Only: object-src 'none';base-uri 'self';script-src 'nonce-VoWl6SncNwZWSv2QOggqow' 'strict-dynamic' 'report-sample' 
                    'unsafe-eval' 'unsafe-inline' https: ...
Forms             : {f}
Headers           : {[Content-Security-Policy-Report-Only, object-src 'none';base-uri 'self';script-src 'nonce-VoWl6SncNwZWSv2QOggqow' 'strict-dynamic' 'report-sample' 
                    'unsafe-eval' 'unsafe-inline' https: http:;report-uri https://csp.withgoogle.com/csp/gws/other-hp], [Accept-CH, Sec-CH-Prefers-Color-Scheme], 
                    [X-XSS-Protection, 0], [X-Frame-Options, SAMEORIGIN]...}
Images            : {@{innerHTML=; innerText=; outerHTML=<IMG style="BORDER-TOP-STYLE: none; BORDER-LEFT-STYLE: none; BORDER-BOTTOM-STYLE: none; BORDER-RIGHT-STYLE: none; 
                    DISPLAY: none" alt="" src="https://ssl.gstatic.com/gb/images/bar/al-icon.png" width=24 height=24>; outerText=; tagName=IMG; style=BORDER-TOP-STYLE: none; 
                    BORDER-LEFT-STYLE: none; BORDER-BOTTOM-STYLE: none; BORDER-RIGHT-STYLE: none; DISPLAY: none; alt=; src=https://ssl.gstatic.com/gb/images/bar/al-icon.png; 
                    width=24; height=24}, @{innerHTML=; innerText=; outerHTML=<IMG id=hplogo style="PADDING-BOTTOM: 14px; PADDING-TOP: 28px; PADDING-LEFT: 0px; PADDING-RIGHT: 
                    0px" alt=Google src="/images/branding/googlelogo/1x/googlelogo_white_background_color_272x92dp.png" width=272 height=92>; outerText=; tagName=IMG; id=hplogo; 
                    style=PADDING-BOTTOM: 14px; PADDING-TOP: 28px; PADDING-LEFT: 0px; PADDING-RIGHT: 0px; alt=Google; 
                    src=/images/branding/googlelogo/1x/googlelogo_white_background_color_272x92dp.png; width=272; height=92}, @{innerHTML=; innerText=; outerHTML=<IMG 
                    id=tsuid_Gz_oaaTzC8KG4-EPwvSN2A4_1 style="CURSOR: pointer; RIGHT: 5px; POSITION: absolute; Z-INDEX: 300; TOP: 4px" alt="" src="/textinputassistant/tia.png" 
                    width=27 height=23 data-script-url="/textinputassistant/13/id_tia.js">; outerText=; tagName=IMG; id=tsuid_Gz_oaaTzC8KG4-EPwvSN2A4_1; style=CURSOR: pointer; 
                    RIGHT: 5px; POSITION: absolute; Z-INDEX: 300; TOP: 4px; alt=; src=/textinputassistant/tia.png; width=27; height=23; 
                    data-script-url=/textinputassistant/13/id_tia.js}}
InputFields       : {@{innerHTML=; innerText=; outerHTML=<INPUT type=hidden value=id name=hl>; outerText=; tagName=INPUT; type=hidden; value=id; name=hl}, @{innerHTML=; 
                    innerText=; outerHTML=<INPUT type=hidden value=hp name=source>; outerText=; tagName=INPUT; type=hidden; value=hp; name=source}, @{innerHTML=; innerText=; 
                    outerHTML=<INPUT type=hidden name=biw>; outerText=; tagName=INPUT; type=hidden; name=biw}, @{innerHTML=; innerText=; outerHTML=<INPUT type=hidden name=bih>; 
                    outerText=; tagName=INPUT; type=hidden; name=bih}...}
Links             : {@{innerHTML=Gmail; innerText=Gmail; outerHTML=<A aria-label="Gmail " class=gb_4 href="https://mail.google.com/mail/&amp;ogbl" target=_top 
                    data-pid="23">Gmail</A>; outerText=Gmail; tagName=A; aria-label=Gmail ; class=gb_4; href=https://mail.google.com/mail/&amp;ogbl; target=_top; data-pid=23}, 
                    @{innerHTML=Gambar; innerText=Gambar; outerHTML=<A aria-label="Telusuri Gambar " class=gb_4 href="https://www.google.com/imghp?hl=id&amp;ogbl" target=_top 
                    data-pid="2">Gambar</A>; outerText=Gambar; tagName=A; aria-label=Telusuri Gambar ; class=gb_4; href=https://www.google.com/imghp?hl=id&amp;ogbl; target=_top; 
                    data-pid=2}, @{innerHTML=<SVG class=gb_F viewbox="0 0 24 24" focusable="false"><PATH d="M6,8c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 
                    2,2zM12,20c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM6,20c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM6,14c1.1,0 2,-0.9 2,-2s-0.9,-2 
                    -2,-2 -2,0.9 -2,2 0.9,2 2,2zM12,14c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM16,6c0,1.1 0.9,2 2,2s2,-0.9 2,-2 -0.9,-2 -2,-2 -2,0.9 
                    -2,2zM12,8c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM18,14c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM18,20c1.1,0 2,-0.9 
                    2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2z"></PATH><IMG style="BORDER-TOP-STYLE: none; BORDER-LEFT-STYLE: none; BORDER-BOTTOM-STYLE: none; BORDER-RIGHT-STYLE: 
                    none; DISPLAY: none" alt="" src="https://ssl.gstatic.com/gb/images/bar/al-icon.png" width=24 height=24></IMG></SVG>; innerText=; outerHTML=<A 
                    aria-expanded=false role=button tabIndex=0 aria-label="Aplikasi Google" class=gb_C href="https://www.google.co.id/intl/id/about/products"><SVG class=gb_F 
                    viewbox="0 0 24 24" focusable="false"><PATH d="M6,8c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM12,20c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 
                    0.9,2 2,2zM6,20c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM6,14c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM12,14c1.1,0 2,-0.9 
                    2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM16,6c0,1.1 0.9,2 2,2s2,-0.9 2,-2 -0.9,-2 -2,-2 -2,0.9 -2,2zM12,8c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 
                    2,2zM18,14c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM18,20c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2z"></PATH><IMG 
                    style="BORDER-TOP-STYLE: none; BORDER-LEFT-STYLE: none; BORDER-BOTTOM-STYLE: none; BORDER-RIGHT-STYLE: none; DISPLAY: none" alt="" 
                    src="https://ssl.gstatic.com/gb/images/bar/al-icon.png" width=24 height=24></IMG></SVG></A>; outerText=; tagName=A; aria-expanded=false; role=button; 
                    tabIndex=0; aria-label=Aplikasi Google; class=gb_C; href=https://www.google.co.id/intl/id/about/products}, @{innerHTML=<SPAN class=gb_he>Login</SPAN>; 
                    innerText=Login; outerHTML=<A aria-label=Login class="gb_0a gb_2d gb_Td gb_Kd" 
                    href="https://accounts.google.com/ServiceLogin?hl=id&amp;passive=true&amp;continue=https://www.google.com/&amp;ec=GAZAmgQ" target=_top><SPAN 
                    class=gb_he>Login</SPAN></A>; outerText=Login; tagName=A; aria-label=Login; class=gb_0a gb_2d gb_Td gb_Kd; 
                    href=https://accounts.google.com/ServiceLogin?hl=id&amp;passive=true&amp;continue=https://www.google.com/&amp;ec=GAZAmgQ; target=_top}...}
ParsedHtml        : mshtml.HTMLDocumentClass
RawContentLength  : 82711
