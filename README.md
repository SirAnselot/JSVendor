# JSVendor
JavaScript-Vendor collection with script to compress a custom selection of frameworks in one .min.js to keep page-requests in projects under control. The collection should grow as other frameworks turn out as indispensable and new stable versions are released. Older Versions are kept to quickly turn back to, if incompatibilities in custom combinations of a project occure.

## Usage

Files you want to compress and add to the custom-collection file should be separated with spaces. The last filename is the build target. 

Run next command in terminal:

```bash
$ ./compressjs.sh [name]/[v]/[file-1].js [name]/[v]/[file-2].js [...] ../[dest]/[target].min.js
```
Courtesy of [dfsq/compressJS.sh](https://github.com/dfsq/compressJS.sh)

## TOC
```
vendor/
│
├── bootsrap/
│   │
│   └── 4.0.0/
│       ├── bootstrap.min.js
│       └── bootstrap.js
│
├── bootsrap.datepicker/ (https://bootstrap-datepicker.readthedocs.io/en/latest/)
│   │
│   ├── 1.7.0/  
│   │   ├── bootstrap-datepicker.min.js
│   │   └── bootstrap-datepicker.js
│   ├── css/
│   └── locales/
│
├── chartjs/ (www.chartjs.org/docs/)
│   │
│   └── 2.1.4/
│       ├── Chart.bundle.js
│       ├── Chart.bundle.min.js 
│       ├── Chart.js
│       └── Chart.min.js
│
├── enquire/2.1.0/enquire.js    
│
├── gsap/   
│   │
│   ├── 1.14.2/
│   ├── 1.17.0/
│   └── 1.18.4/ (CLUB-EDITION! with bonus plugins and tools – @see: https://greensock.com/club/)
│       ├── easing/
│       ├── plugins/ (plugins must be added separately as needed)
│       ├── utils/
│       ├── TimelineLite.js
│       ├── TimelineMax.js
│       ├── TweenLite.js
│       └── TweenMax.js
│
├── imagesloaded/   
│   │
│   ├── 3.1.4/imagesloaded.js
│   ├── 3.1.8/imagesloaded.js
│   └── 4.1.0/imagesloaded.js
│
├── jquery/
│   │   
│   ├── 1.11.1/
│   └── 1.12.4/
│       ├── jquery.js
│       └── jquery.min.js
│
├── jquery-ui/
│   │   
│   ├── 1.10.4/
│   ├── 1.11.0/
│   │   ├── jquery-ui.js
│   │   └── jquery-ui.min.js                
│   ├── 1.11.2/
│   └── 1.11.4/
│
├── modernizr/  
│   │
│   └── 2.6.2/
│       ├── modernizr.custom.min.js
│       └── modernizr.min.js
│
├── scrollmagic/    
│   │
│   ├── 1.2.0/
│   └── 2.0.5/
│       ├── plugins/
│       └── ScrollMagic.min.js
│
├── slick/
│   │
│   └── 1.5.9/
│       ├── fonts/
│       ├── slick.js
│       ├── slick.min.js
│       ├── slick.css
│       ├── slick.less
│       └── slick.scss
│
├── tether/ (don't know what this is but seems necessary to run 'bootstrap v4 alpha')
│   │
│   └── 1.3.0/
│       ├── css/
│       ├── tether.js
│       └── tether.min.js
│
└── waypoints/
    │
    ├── 1.6.2/
    └── 4.0.0/
        ├── shortcuts/  (shortcuts must be added separately as needed)
        │   ├── infinite.min.js
        │   ├── infinite.js
        │   ├── inview.min.js
        │   ├── inview.js
        │   ├── sticky.min.js
        │   └── sticky.js
        ├── jquery.waypoints.js     
        ├── jquery.waypoints.min.js 
        └── waypoints.debug.js  	
 		    
 		    
```
