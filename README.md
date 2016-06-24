# JSVendor
JavaScript-Vendor collection with script to compress a custom selection of frameworks in one .min.js to keep page-requests in projects under control. The collection should grow as other frameworks turn out as indispensable and new stable versions are released. Older Versions are kept to quickly turn back to, if incompatibilities in custom combinations of a project occure.

## Usage

### 1. "Pack & Go" (bash)    
Files you want to compress and add to the custom-collection file should be separated with spaces. The last filename is the build target.

Run next command in terminal:

```bash
$ ./compressjs.sh [name]/[v]/[file-1].js [name]/[v]/[file-2].js [...] ../[dest]/[target].min.js
```
Courtesy of [dfsq] (https://github.com/dfsq/compressJS.sh)

### 2. "Itegrated Service" (grunt) in [WS-Base](https://github.com/SirAnselot/WS-Base/) ...
Add script-paths to [**vendorBridge.json**](https://github.com/SirAnselot/WS-Base/blob/master/grunt/vendorBridge.json)  `(WS-Base/grunt/vendorBridge.json)` of your project.

#### Sample content of `vendorBridge.json` 
```json
{
    "paths": {
		"vendor": [
			"jquery/1.12.4/jquery.js",
			"tether/1.3.0/tether.js",
			"bootstrap/4.0.0/bootstrap.js",
			"gsap/1.18.4/TweenMax.js",
			"imagesloaded/3.1.4/imagesloaded.js",
			"modernizr/2.6.2/modernizr.min.js",
			"enquire/2.1.0/enquire.js"
		]
  	}
}
```


## TOC
```
vendor/
│
├── bootsrap/
│   │
│   ├── 3.3.6/
│   │   ├── bootstrap.min.js
│   │   ├── bootstrap.js
│   │   └── plugins/... (affix.js, alert.js, button.js, ...)
│   │
│   └── 4.0.0/
│       ├── bootstrap.min.js
│       └── bootstrap.js
│
├── bootsrap.datepicker/ (@see: https://bootstrap-datepicker.readthedocs.io/en/latest/)
│   │
│   ├── 1.7.0/  
│   │   ├── bootstrap-datepicker.min.js
│   │   └── bootstrap-datepicker.js
│   ├── css/
│   └── locales/
│
├── bootsrap.jasny/ (@see:	http://www.jasny.net/bootstrap/)
│   │
│   ├── 3.1.0/
│   └── 3.1.3/  
│		  ├── jasny-bootstrap.min.js
│       ├── jasny-bootstrap.min.css
│       └── jasny-bootstrap.js
│
├── chartjs/ (@see: http://www.chartjs.org/docs/)
│   │
│   └── 2.1.4/
│       ├── Chart.bundle.js
│       ├── Chart.bundle.min.js
│       ├── Chart.js
│       └── Chart.min.js
│
├── chosen/   
│   │
│   ├── 1.4.2/
│   └── 1.5.1/ (@see: https://harvesthq.github.io/chosen/)
│       ├── chosen.jquery.js
│       ├── chosen.jquery.min.js
│       ├── chosen.css
│       ├── chosen.min.css
│       ├── chosen-sprite.png
│       └── chosen-sprite@2x.png
│
├── enquire/  
│   │
│   └── 2.1.0/
│       └── enquire.js
│
├── foundation/  
│   │
│   └── 6.1.2/
│       └── foundation.min.js    
│
├── gsap/   
│   │
│   ├── 1.14.2/
│   ├── 1.17.0/
│   └── 1.18.4/ (CLUB-EDITION! with bonus plugins and tools – @see: https://greensock.com/club/)
│       ├── easing/
│       ├── plugins/
│       ├── utils/
│       ├── TimelineLite.js
│       ├── TimelineMax.js
│       ├── TweenLite.js
│       └── TweenMax.js
│
├── imagescroll/  
│   │
│   └── 0.2.3/
│       ├── imageScroll.min.js
│       └── imageScroll.js
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
├── js.cookie/  
│   │
│   └── 2.1.1/
│       └── js.cookie.js
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
├── slick/ (@see http://kenwheeler.github.io)
│   │
│   └── 1.5.9/
│       ├── fonts/
│       ├── slick.js
│       ├── slick.min.js
│       ├── slick.css
│       ├── slick.less
│       └── slick.scss
│
├── sticky-kit/  
│   │
│   └── 1.1.1/
│       ├── jquery.sticky-kit.js
│       └── jquery.sticky-kit.min.js
│
├── tablesorter/ (@see:	http://tablesorter.com/docs/)
│   │
│   └── 2.0.5/
│		  ├── jquery.metadata.js
│       ├── jquery.tablesorter.min.js
│       └── jquery.tablesorter.js
│
├── tether/ (required by 'bootstrap v4-alpha' tooltips @see http://v4-alpha.getbootstrap.com/components/tooltips/)
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
        ├── shortcuts/ (shortcuts must be added separately as needed)
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
