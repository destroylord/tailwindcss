# Dokumentasi Tailwindcss

*Theme Name* : Tailwindcss 

*Created*    : 15/11/2020 

*Author*     : **Destroylord**

***
Terima kasih telah memberikan kesempatan untuk membagi pengalaman saya tentang konfigurasi larvel-mix + tailwindcss.
***

## Daftar isi

1. [Installasi laravel-mix](#1-installasi-laravel-mix)
2. [installasi tailwindcss](#2-installasi-tailwindcss)
3. [Browser Support](#3-browser-support)

##  1. Installasi laravel-mix

* Untuk installasi laravel mix bisa ikuti dokumentasi website resminya [di sini.](https://laravel-mix.com/docs/5.0/installation) 
* Setelah installasi selesai kita tahap installasi tailwindcss

##  2. Installasi Tailwindcss

* Buka terminal anda, pastikan posisi terminal berada di folder project yang baru anda install.

* Copy script dibawah ini dan paste di terminal anda.
  
  ```npm install tailwindcss@latest postcss@latest autoprefixer@latest```
  
* Lanjut ketahap berikutnya, kemudian install purgeCSS untuk laravel-mix
  
  ```npm install laravel-mix-purgecss --save-dev```

* Edit file webpack.mix.js, seperti dibawah ini : 
  ```let mix = require('laravel-mix');
    const tailwindcss = require('tailwindcss');
    require('laravel-mix-purgecss');

    mix.js('src/js/app.js', 'public/js')
        .sass('src/sass/app.scss', 'public/css')
        .sass('src/sass/style.scss', 'public/css')
    
        .options({
            processCssUrls: false,
            postCss: [ tailwindcss('./tailwind.config.js') ]
        })
        .purgeCss()
        .setPublicPath('public');
* Langkah selanjutnya buat konfigurasi Tailwindcss dengan perintah :

    ```npx tailwind init```

* Kemuduian taruh script ini di src/scss/style.scss :

    ```@import "tailwindcss/base";```

    ```@import "tailwindcss/components";```

    ```@import "tailwindcss/utilities";```
* Terakhir jalankan perintah ini diterminal anda :

    ```npx mix``` / ```npx mix watch```

##  3. Browser Support
Working ke semua browser : 
 
**IE 6-8**   
**IE 9+**   
**Chrome**   
**Firefox**   
**Safari**   
**Opera** 
***

#### Theme by Destroylord
Jika anda memiliki pertanyaan lain yang tidak mencangkup dalam dokumentasi, Silahkan kirim email ke <masapin68@gmail.com>.
<br>

###### Terima Kasih
