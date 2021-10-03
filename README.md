# etalage.css
/*
 * Title: jQuery Etalage plugin CSS
 * Author: Berend de Jong, Frique
 * Author URI: http://www.frique.me/
 * Version: 1.3.1 (20120705.1)
 *
 * ------------------------------------ STYLE ------------------------------------
 * Edit this section to style your thumbnails, zoom area, magnifier etc.
 * If the id of your Etalage instance is different, do a find/replace on #etalage.
 * -------------------------------------------------------------------------------
 */

/* Etalage container (large thumb + small thumbs): */
#etalage{
	display: none;
	margin-bottom:18%;
}

/* Large thumbnail: */
#etalage .etalage_thumb{
	background:url(../images/loading.gif) center no-repeat;
	border: 1px solid #eee;
	padding: 6px;
}
/* Large thumbnail - image (in case you want to add a border around the image within the frame) */
#etalage .etalage_thumb_image{ }

/* Small thumbnails: */
#etalage .etalage_small_thumbs li{
	border: 1px solid #ddd;
	margin: 10px;
	padding: 3px;
}
/* The one on the left that makes them slide */
#etalage ul li.etalage_smallthumb_first{ }
/* The one on the right that makes them slide */
#etalage ul li.etalage_smallthumb_last{ }
/* The currently active one */
#etalage ul li.etalage_smallthumb_active{
}

/* Zoomed image area: */
#etalage .etalage_zoom_area,
.etalage_zoom_area{
	background: white url(../images/loading.gif) center no-repeat;
	border: 1px solid #EEE;
	padding: 6px;
}

/* Magnifier area (thumbnail hovering rectangle): */
#etalage .etalage_magnifier{
	background: white;
	border: 1px solid #eee;
}

/* Icon that will apear at the left bottom of the large thumbnail (optional): */
#etalage .etalage_icon{
	background: url(../images/zoom.png) no-repeat rgba(184, 183, 181, 0.32);
	width: 104px;
	height: 104px;
}

/* Hint that will apear at the top right of the large thumbnail (optional): */
#etalage .etalage_hint{
	background: url(../images/hint.gif) no-repeat;
	width: 130px;
	height: 57px;
}

/* Description area (optional) */
#etalage .etalage_description{
	background: white;
	font-style: italic;
	margin: 10px;
	padding: 6px 10px;
}

/*
 * ------------------------------------ FUNCTIONALITY --------------------------------------
 * The following CSS serves to make Etalage function properly. Don't edit or edit carefully.
 * -----------------------------------------------------------------------------------------
 */

.etalage, .etalage_thumb, .etalage_thumb_image, .etalage_source_image, .etalage_zoom_preview, .etalage_icon, .etalage_hint{ display:none }
.etalage, .etalage ul, .etalage li, .etalage img, .etalage_hint, .etalage_icon, .etalage_description{ margin:0; padding:0; border:0; list-style:none }
.etalage, .etalage_magnifier div, .etalage_magnifier div img, .etalage_small_thumbs ul, ul .etalage_small_thumbs li, .etalage_zoom_area div, .etalage_zoom_img{ position:relative }
.etalage img, .etalage li{ -webkit-user-select:none; -khtml-user-select:none; -moz-user-select:none; -o-user-select:none; user-select:none; -webkit-user-drag:none; -moz-user-drag:none; user-drag:none }
.etalage, .etalage_small_thumbs li{ float:left }
.etalage_right{ float:right }
.etalage li{ position:absolute }
.etalage img{ vertical-align:bottom; max-width:none }
.etalage_magnifier{ cursor:default }
.etalage_magnifier div, .etalage_small_thumbs{ overflow:hidden }
.etalage_magnifier div img{ display:none }
.etalage_icon, .etalage_hint{ cursor:default; width:0; height:0; overflow:hidden }
.etalage_small_thumbs li.vertical{ float:none }
.etalage_zoom_area{ z-index:996 }
.etalage_zoom_area div{ overflow:hidden; z-index:997 }
.etalage_zoom_preview{ position:absolute; z-index:998 }
.etalage_zoom_img, .etalage_hint{ z-index:999 }
.etalage{ direction:ltr }
div.etalage_description{ position:absolute; bottom:0; left:0; z-index:999 }
div.etalage_description.rtl{ direction:rtl; text-align:right }

@media (max-width:1024px){
#etalage .etalage_thumb_image {
		width: 240px !important;
		height: 340px !important;
	}
	#etalage .etalage_icon {
		background: url(../images/zoom.png) no-repeat rgba(184, 183, 181, 0.32) -13px -9px;
		width: 80px;
		height: 80px;
		top: 270px !important;
		left: 4px !important;
	}
	li.etalage_small_thumbs {
		width: 216px !important;
		top: 370px !important;
	}
}
@media (max-width:640px){
#etalage .etalage_thumb_image {
		width: 200px !important;
		height: 300px !important;
	}
	#etalage .etalage_icon {
		background: url(../images/zoom.png) no-repeat rgba(184, 183, 181, 0.32) -19px -20px;
		width: 60px;
		height: 60px;
		top: 249px !important;
		left: 4px !important;
	}
	li.etalage_small_thumbs {
		width: 216px !important;
		top: 350px !important;
	}
}
@media (max-width:480px){
	#etalage {
	margin-bottom:0%;
 }
 .single_right {
	width: 100%;
	float: none;
 }
}
