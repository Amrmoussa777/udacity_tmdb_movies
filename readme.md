<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />

<title>investigate-a-dataset-template</title>

<script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>



<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.7.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.7.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.7.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff2?v=4.7.0') format('woff2'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.7.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.7.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.7.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.fa-pull-left {
  float: left;
}
.fa-pull-right {
  float: right;
}
.fa.fa-pull-left {
  margin-right: .3em;
}
.fa.fa-pull-right {
  margin-left: .3em;
}
/* Deprecated as of 4.4.0 */
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
.fa-pulse {
  -webkit-animation: fa-spin 1s infinite steps(8);
  animation: fa-spin 1s infinite steps(8);
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=1)";
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2)";
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=3)";
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1)";
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1)";
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook-f:before,
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-feed:before,
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before,
.fa-gratipay:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper-pp:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-resistance:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-y-combinator-square:before,
.fa-yc-square:before,
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
.fa-buysellads:before {
  content: "\f20d";
}
.fa-connectdevelop:before {
  content: "\f20e";
}
.fa-dashcube:before {
  content: "\f210";
}
.fa-forumbee:before {
  content: "\f211";
}
.fa-leanpub:before {
  content: "\f212";
}
.fa-sellsy:before {
  content: "\f213";
}
.fa-shirtsinbulk:before {
  content: "\f214";
}
.fa-simplybuilt:before {
  content: "\f215";
}
.fa-skyatlas:before {
  content: "\f216";
}
.fa-cart-plus:before {
  content: "\f217";
}
.fa-cart-arrow-down:before {
  content: "\f218";
}
.fa-diamond:before {
  content: "\f219";
}
.fa-ship:before {
  content: "\f21a";
}
.fa-user-secret:before {
  content: "\f21b";
}
.fa-motorcycle:before {
  content: "\f21c";
}
.fa-street-view:before {
  content: "\f21d";
}
.fa-heartbeat:before {
  content: "\f21e";
}
.fa-venus:before {
  content: "\f221";
}
.fa-mars:before {
  content: "\f222";
}
.fa-mercury:before {
  content: "\f223";
}
.fa-intersex:before,
.fa-transgender:before {
  content: "\f224";
}
.fa-transgender-alt:before {
  content: "\f225";
}
.fa-venus-double:before {
  content: "\f226";
}
.fa-mars-double:before {
  content: "\f227";
}
.fa-venus-mars:before {
  content: "\f228";
}
.fa-mars-stroke:before {
  content: "\f229";
}
.fa-mars-stroke-v:before {
  content: "\f22a";
}
.fa-mars-stroke-h:before {
  content: "\f22b";
}
.fa-neuter:before {
  content: "\f22c";
}
.fa-genderless:before {
  content: "\f22d";
}
.fa-facebook-official:before {
  content: "\f230";
}
.fa-pinterest-p:before {
  content: "\f231";
}
.fa-whatsapp:before {
  content: "\f232";
}
.fa-server:before {
  content: "\f233";
}
.fa-user-plus:before {
  content: "\f234";
}
.fa-user-times:before {
  content: "\f235";
}
.fa-hotel:before,
.fa-bed:before {
  content: "\f236";
}
.fa-viacoin:before {
  content: "\f237";
}
.fa-train:before {
  content: "\f238";
}
.fa-subway:before {
  content: "\f239";
}
.fa-medium:before {
  content: "\f23a";
}
.fa-yc:before,
.fa-y-combinator:before {
  content: "\f23b";
}
.fa-optin-monster:before {
  content: "\f23c";
}
.fa-opencart:before {
  content: "\f23d";
}
.fa-expeditedssl:before {
  content: "\f23e";
}
.fa-battery-4:before,
.fa-battery:before,
.fa-battery-full:before {
  content: "\f240";
}
.fa-battery-3:before,
.fa-battery-three-quarters:before {
  content: "\f241";
}
.fa-battery-2:before,
.fa-battery-half:before {
  content: "\f242";
}
.fa-battery-1:before,
.fa-battery-quarter:before {
  content: "\f243";
}
.fa-battery-0:before,
.fa-battery-empty:before {
  content: "\f244";
}
.fa-mouse-pointer:before {
  content: "\f245";
}
.fa-i-cursor:before {
  content: "\f246";
}
.fa-object-group:before {
  content: "\f247";
}
.fa-object-ungroup:before {
  content: "\f248";
}
.fa-sticky-note:before {
  content: "\f249";
}
.fa-sticky-note-o:before {
  content: "\f24a";
}
.fa-cc-jcb:before {
  content: "\f24b";
}
.fa-cc-diners-club:before {
  content: "\f24c";
}
.fa-clone:before {
  content: "\f24d";
}
.fa-balance-scale:before {
  content: "\f24e";
}
.fa-hourglass-o:before {
  content: "\f250";
}
.fa-hourglass-1:before,
.fa-hourglass-start:before {
  content: "\f251";
}
.fa-hourglass-2:before,
.fa-hourglass-half:before {
  content: "\f252";
}
.fa-hourglass-3:before,
.fa-hourglass-end:before {
  content: "\f253";
}
.fa-hourglass:before {
  content: "\f254";
}
.fa-hand-grab-o:before,
.fa-hand-rock-o:before {
  content: "\f255";
}
.fa-hand-stop-o:before,
.fa-hand-paper-o:before {
  content: "\f256";
}
.fa-hand-scissors-o:before {
  content: "\f257";
}
.fa-hand-lizard-o:before {
  content: "\f258";
}
.fa-hand-spock-o:before {
  content: "\f259";
}
.fa-hand-pointer-o:before {
  content: "\f25a";
}
.fa-hand-peace-o:before {
  content: "\f25b";
}
.fa-trademark:before {
  content: "\f25c";
}
.fa-registered:before {
  content: "\f25d";
}
.fa-creative-commons:before {
  content: "\f25e";
}
.fa-gg:before {
  content: "\f260";
}
.fa-gg-circle:before {
  content: "\f261";
}
.fa-tripadvisor:before {
  content: "\f262";
}
.fa-odnoklassniki:before {
  content: "\f263";
}
.fa-odnoklassniki-square:before {
  content: "\f264";
}
.fa-get-pocket:before {
  content: "\f265";
}
.fa-wikipedia-w:before {
  content: "\f266";
}
.fa-safari:before {
  content: "\f267";
}
.fa-chrome:before {
  content: "\f268";
}
.fa-firefox:before {
  content: "\f269";
}
.fa-opera:before {
  content: "\f26a";
}
.fa-internet-explorer:before {
  content: "\f26b";
}
.fa-tv:before,
.fa-television:before {
  content: "\f26c";
}
.fa-contao:before {
  content: "\f26d";
}
.fa-500px:before {
  content: "\f26e";
}
.fa-amazon:before {
  content: "\f270";
}
.fa-calendar-plus-o:before {
  content: "\f271";
}
.fa-calendar-minus-o:before {
  content: "\f272";
}
.fa-calendar-times-o:before {
  content: "\f273";
}
.fa-calendar-check-o:before {
  content: "\f274";
}
.fa-industry:before {
  content: "\f275";
}
.fa-map-pin:before {
  content: "\f276";
}
.fa-map-signs:before {
  content: "\f277";
}
.fa-map-o:before {
  content: "\f278";
}
.fa-map:before {
  content: "\f279";
}
.fa-commenting:before {
  content: "\f27a";
}
.fa-commenting-o:before {
  content: "\f27b";
}
.fa-houzz:before {
  content: "\f27c";
}
.fa-vimeo:before {
  content: "\f27d";
}
.fa-black-tie:before {
  content: "\f27e";
}
.fa-fonticons:before {
  content: "\f280";
}
.fa-reddit-alien:before {
  content: "\f281";
}
.fa-edge:before {
  content: "\f282";
}
.fa-credit-card-alt:before {
  content: "\f283";
}
.fa-codiepie:before {
  content: "\f284";
}
.fa-modx:before {
  content: "\f285";
}
.fa-fort-awesome:before {
  content: "\f286";
}
.fa-usb:before {
  content: "\f287";
}
.fa-product-hunt:before {
  content: "\f288";
}
.fa-mixcloud:before {
  content: "\f289";
}
.fa-scribd:before {
  content: "\f28a";
}
.fa-pause-circle:before {
  content: "\f28b";
}
.fa-pause-circle-o:before {
  content: "\f28c";
}
.fa-stop-circle:before {
  content: "\f28d";
}
.fa-stop-circle-o:before {
  content: "\f28e";
}
.fa-shopping-bag:before {
  content: "\f290";
}
.fa-shopping-basket:before {
  content: "\f291";
}
.fa-hashtag:before {
  content: "\f292";
}
.fa-bluetooth:before {
  content: "\f293";
}
.fa-bluetooth-b:before {
  content: "\f294";
}
.fa-percent:before {
  content: "\f295";
}
.fa-gitlab:before {
  content: "\f296";
}
.fa-wpbeginner:before {
  content: "\f297";
}
.fa-wpforms:before {
  content: "\f298";
}
.fa-envira:before {
  content: "\f299";
}
.fa-universal-access:before {
  content: "\f29a";
}
.fa-wheelchair-alt:before {
  content: "\f29b";
}
.fa-question-circle-o:before {
  content: "\f29c";
}
.fa-blind:before {
  content: "\f29d";
}
.fa-audio-description:before {
  content: "\f29e";
}
.fa-volume-control-phone:before {
  content: "\f2a0";
}
.fa-braille:before {
  content: "\f2a1";
}
.fa-assistive-listening-systems:before {
  content: "\f2a2";
}
.fa-asl-interpreting:before,
.fa-american-sign-language-interpreting:before {
  content: "\f2a3";
}
.fa-deafness:before,
.fa-hard-of-hearing:before,
.fa-deaf:before {
  content: "\f2a4";
}
.fa-glide:before {
  content: "\f2a5";
}
.fa-glide-g:before {
  content: "\f2a6";
}
.fa-signing:before,
.fa-sign-language:before {
  content: "\f2a7";
}
.fa-low-vision:before {
  content: "\f2a8";
}
.fa-viadeo:before {
  content: "\f2a9";
}
.fa-viadeo-square:before {
  content: "\f2aa";
}
.fa-snapchat:before {
  content: "\f2ab";
}
.fa-snapchat-ghost:before {
  content: "\f2ac";
}
.fa-snapchat-square:before {
  content: "\f2ad";
}
.fa-pied-piper:before {
  content: "\f2ae";
}
.fa-first-order:before {
  content: "\f2b0";
}
.fa-yoast:before {
  content: "\f2b1";
}
.fa-themeisle:before {
  content: "\f2b2";
}
.fa-google-plus-circle:before,
.fa-google-plus-official:before {
  content: "\f2b3";
}
.fa-fa:before,
.fa-font-awesome:before {
  content: "\f2b4";
}
.fa-handshake-o:before {
  content: "\f2b5";
}
.fa-envelope-open:before {
  content: "\f2b6";
}
.fa-envelope-open-o:before {
  content: "\f2b7";
}
.fa-linode:before {
  content: "\f2b8";
}
.fa-address-book:before {
  content: "\f2b9";
}
.fa-address-book-o:before {
  content: "\f2ba";
}
.fa-vcard:before,
.fa-address-card:before {
  content: "\f2bb";
}
.fa-vcard-o:before,
.fa-address-card-o:before {
  content: "\f2bc";
}
.fa-user-circle:before {
  content: "\f2bd";
}
.fa-user-circle-o:before {
  content: "\f2be";
}
.fa-user-o:before {
  content: "\f2c0";
}
.fa-id-badge:before {
  content: "\f2c1";
}
.fa-drivers-license:before,
.fa-id-card:before {
  content: "\f2c2";
}
.fa-drivers-license-o:before,
.fa-id-card-o:before {
  content: "\f2c3";
}
.fa-quora:before {
  content: "\f2c4";
}
.fa-free-code-camp:before {
  content: "\f2c5";
}
.fa-telegram:before {
  content: "\f2c6";
}
.fa-thermometer-4:before,
.fa-thermometer:before,
.fa-thermometer-full:before {
  content: "\f2c7";
}
.fa-thermometer-3:before,
.fa-thermometer-three-quarters:before {
  content: "\f2c8";
}
.fa-thermometer-2:before,
.fa-thermometer-half:before {
  content: "\f2c9";
}
.fa-thermometer-1:before,
.fa-thermometer-quarter:before {
  content: "\f2ca";
}
.fa-thermometer-0:before,
.fa-thermometer-empty:before {
  content: "\f2cb";
}
.fa-shower:before {
  content: "\f2cc";
}
.fa-bathtub:before,
.fa-s15:before,
.fa-bath:before {
  content: "\f2cd";
}
.fa-podcast:before {
  content: "\f2ce";
}
.fa-window-maximize:before {
  content: "\f2d0";
}
.fa-window-minimize:before {
  content: "\f2d1";
}
.fa-window-restore:before {
  content: "\f2d2";
}
.fa-times-rectangle:before,
.fa-window-close:before {
  content: "\f2d3";
}
.fa-times-rectangle-o:before,
.fa-window-close-o:before {
  content: "\f2d4";
}
.fa-bandcamp:before {
  content: "\f2d5";
}
.fa-grav:before {
  content: "\f2d6";
}
.fa-etsy:before {
  content: "\f2d7";
}
.fa-imdb:before {
  content: "\f2d8";
}
.fa-ravelry:before {
  content: "\f2d9";
}
.fa-eercast:before {
  content: "\f2da";
}
.fa-microchip:before {
  content: "\f2db";
}
.fa-snowflake-o:before {
  content: "\f2dc";
}
.fa-superpowers:before {
  content: "\f2dd";
}
.fa-wpexplorer:before {
  content: "\f2de";
}
.fa-meetup:before {
  content: "\f2e0";
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
div.traceback-wrapper pre.traceback {
  max-height: 600px;
  overflow: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 5px;
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
[dir="rtl"] #ipython_notebook {
  margin-right: 10px;
  margin-left: 0;
}
[dir="rtl"] #ipython_notebook.pull-left {
  float: right !important;
  float: right;
}
.flex-spacer {
  flex: 1;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#kernel_logo_widget {
  margin: 0 10px;
}
span#login_widget {
  float: right;
}
[dir="rtl"] span#login_widget {
  float: left;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
.modal-header {
  cursor: move;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
[dir="rtl"] .center-nav form.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] .center-nav .navbar-text {
  float: right;
}
[dir="rtl"] .navbar-inner {
  text-align: right;
}
[dir="rtl"] div.text-left {
  text-align: right;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  overflow: hidden;
  cursor: pointer;
  opacity: 0;
  z-index: 2;
}
.alternate_upload .btn-xs > input.fileinput {
  margin: -1px -5px;
}
.alternate_upload .btn-upload {
  position: relative;
  height: 22px;
}
::-webkit-file-upload-button {
  cursor: pointer;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
ul#tabs {
  margin-bottom: 4px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
[dir="rtl"] ul#tabs.nav-tabs > li {
  float: right;
}
[dir="rtl"] ul#tabs.nav.nav-tabs {
  padding-right: 0;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons .pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .list_toolbar .col-sm-4,
[dir="rtl"] .list_toolbar .col-sm-8 {
  float: right;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: text-bottom;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
[dir="rtl"] .list_item > div input {
  margin-right: 0;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_modified {
  margin-right: 7px;
  margin-left: 7px;
}
[dir="rtl"] .item_modified.pull-right {
  float: left !important;
  float: left;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
[dir="rtl"] .item_buttons.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .item_buttons .kernel-name {
  margin-left: 7px;
  float: right;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
.sort_button {
  display: inline-block;
  padding-left: 7px;
}
[dir="rtl"] .sort_button.pull-right {
  float: left !important;
  float: left;
}
#tree-selector {
  padding-right: 0px;
}
#button-select-all {
  min-width: 50px;
}
[dir="rtl"] #button-select-all.btn {
  float: right ;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
  margin-top: 2px;
  height: 16px;
}
[dir="rtl"] #select-all.pull-left {
  float: right !important;
  float: right;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.fa-pull-left {
  margin-right: .3em;
}
.folder_icon:before.fa-pull-right {
  margin-left: .3em;
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.fa-pull-left {
  margin-right: .3em;
}
.file_icon:before.fa-pull-right {
  margin-left: .3em;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
#new-menu .dropdown-header {
  font-size: 10px;
  border-bottom: 1px solid #e5e5e5;
  padding: 0 0 3px;
  margin: -3px 20px 0;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.move-button {
  display: none;
}
.download-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
.CodeMirror-dialog {
  background-color: #fff;
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI escape sequences */
/* The color values are a mix of
   http://www.xcolors.net/dl/baskerville-ivorylight and
   http://www.xcolors.net/dl/euphrasia */
.ansi-black-fg {
  color: #3E424D;
}
.ansi-black-bg {
  background-color: #3E424D;
}
.ansi-black-intense-fg {
  color: #282C36;
}
.ansi-black-intense-bg {
  background-color: #282C36;
}
.ansi-red-fg {
  color: #E75C58;
}
.ansi-red-bg {
  background-color: #E75C58;
}
.ansi-red-intense-fg {
  color: #B22B31;
}
.ansi-red-intense-bg {
  background-color: #B22B31;
}
.ansi-green-fg {
  color: #00A250;
}
.ansi-green-bg {
  background-color: #00A250;
}
.ansi-green-intense-fg {
  color: #007427;
}
.ansi-green-intense-bg {
  background-color: #007427;
}
.ansi-yellow-fg {
  color: #DDB62B;
}
.ansi-yellow-bg {
  background-color: #DDB62B;
}
.ansi-yellow-intense-fg {
  color: #B27D12;
}
.ansi-yellow-intense-bg {
  background-color: #B27D12;
}
.ansi-blue-fg {
  color: #208FFB;
}
.ansi-blue-bg {
  background-color: #208FFB;
}
.ansi-blue-intense-fg {
  color: #0065CA;
}
.ansi-blue-intense-bg {
  background-color: #0065CA;
}
.ansi-magenta-fg {
  color: #D160C4;
}
.ansi-magenta-bg {
  background-color: #D160C4;
}
.ansi-magenta-intense-fg {
  color: #A03196;
}
.ansi-magenta-intense-bg {
  background-color: #A03196;
}
.ansi-cyan-fg {
  color: #60C6C8;
}
.ansi-cyan-bg {
  background-color: #60C6C8;
}
.ansi-cyan-intense-fg {
  color: #258F8F;
}
.ansi-cyan-intense-bg {
  background-color: #258F8F;
}
.ansi-white-fg {
  color: #C5C1B4;
}
.ansi-white-bg {
  background-color: #C5C1B4;
}
.ansi-white-intense-fg {
  color: #A1A6B2;
}
.ansi-white-intense-bg {
  background-color: #A1A6B2;
}
.ansi-default-inverse-fg {
  color: #FFFFFF;
}
.ansi-default-inverse-bg {
  background-color: #000000;
}
.ansi-bold {
  font-weight: bold;
}
.ansi-underline {
  text-decoration: underline;
}
/* The following styles are deprecated an will be removed in a future version */
.ansibold {
  font-weight: bold;
}
.ansi-inverse {
  outline: 0.5px dotted;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  position: relative;
  overflow: visible;
}
div.cell:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: transparent;
}
div.cell.jupyter-soft-selected {
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected,
div.cell.selected.jupyter-soft-selected {
  border-color: #ababab;
}
div.cell.selected:before,
div.cell.selected.jupyter-soft-selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #42A5F5;
}
@media print {
  div.cell.selected,
  div.cell.selected.jupyter-soft-selected {
    border-color: transparent;
  }
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
}
.edit_mode div.cell.selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #66BB6A;
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  /* Note that this should set vertical padding only, since CodeMirror assumes
       that horizontal padding will be set on CodeMirror pre */
  padding: 0.4em 0;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. This sets horizontal padding only,
    use .CodeMirror-lines for vertical */
  padding: 0 0.4em;
  border: 0;
  border-radius: 0;
}
.CodeMirror-cursor {
  border-left: 1.4px solid black;
}
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .CodeMirror-cursor {
    border-left: 2px solid black;
  }
}
@media screen and (min-width: 4320px) {
  .CodeMirror-cursor {
    border-left: 4px solid black;
  }
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
div.output_area .mglyph > img {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 1px 0 1px 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul:not(.list-inline),
.rendered_html ol:not(.list-inline) {
  padding-left: 2em;
}
.rendered_html ul {
  list-style: disc;
}
.rendered_html ul ul {
  list-style: square;
  margin-top: 0;
}
.rendered_html ul ul ul {
  list-style: circle;
}
.rendered_html ol {
  list-style: decimal;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin-top: 0;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
  padding: 0px;
  background-color: #fff;
}
.rendered_html code {
  background-color: #eff0f1;
}
.rendered_html p code {
  padding: 1px 5px;
}
.rendered_html pre code {
  background-color: #fff;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  color: #000;
  font-size: 100%;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: none;
  border-collapse: collapse;
  border-spacing: 0;
  color: black;
  font-size: 12px;
  table-layout: fixed;
}
.rendered_html thead {
  border-bottom: 1px solid black;
  vertical-align: bottom;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  text-align: right;
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html tbody tr:nth-child(odd) {
  background: #f5f5f5;
}
.rendered_html tbody tr:hover {
  background: rgba(66, 165, 245, 0.2);
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
.rendered_html .alert {
  margin-bottom: initial;
}
.rendered_html * + .alert {
  margin-top: 1em;
}
[dir="rtl"] .rendered_html p {
  text-align: right;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.rendered .rendered_html tr,
.text_cell.rendered .rendered_html th,
.text_cell.rendered .rendered_html td {
  max-width: none;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.text_cell .dropzone .input_area {
  border: 2px dashed #bababa;
  margin: -1px;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
.jupyter-keybindings {
  padding: 1px;
  line-height: 24px;
  border-bottom: 1px solid gray;
}
.jupyter-keybindings input {
  margin: 0;
  padding: 0;
  border: none;
}
.jupyter-keybindings i {
  padding: 6px;
}
.well code {
  background-color: #ffffff;
  border-color: #ababab;
  border-width: 1px;
  border-style: solid;
  padding: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.tags_button_container {
  width: 100%;
  display: flex;
}
.tag-container {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
  overflow: hidden;
  position: relative;
}
.tag-container > * {
  margin: 0 4px;
}
.remove-tag-btn {
  margin-left: 4px;
}
.tags-input {
  display: flex;
}
.cell-tag:last-child:after {
  content: "";
  position: absolute;
  right: 0;
  width: 40px;
  height: 100%;
  /* Fade to background color of cell toolbar */
  background: linear-gradient(to right, rgba(0, 0, 0, 0), #EEE);
}
.tags-input > * {
  margin-left: 4px;
}
.cell-tag,
.tags-input input,
.tags-input button {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  box-shadow: none;
  width: inherit;
  font-size: inherit;
  height: 22px;
  line-height: 22px;
  padding: 0px 4px;
  display: inline-block;
}
.cell-tag:focus,
.tags-input input:focus,
.tags-input button:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.cell-tag::-moz-placeholder,
.tags-input input::-moz-placeholder,
.tags-input button::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.cell-tag:-ms-input-placeholder,
.tags-input input:-ms-input-placeholder,
.tags-input button:-ms-input-placeholder {
  color: #999;
}
.cell-tag::-webkit-input-placeholder,
.tags-input input::-webkit-input-placeholder,
.tags-input button::-webkit-input-placeholder {
  color: #999;
}
.cell-tag::-ms-expand,
.tags-input input::-ms-expand,
.tags-input button::-ms-expand {
  border: 0;
  background-color: transparent;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
.cell-tag[readonly],
.tags-input input[readonly],
.tags-input button[readonly],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  background-color: #eeeeee;
  opacity: 1;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  cursor: not-allowed;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button {
  height: auto;
}
select.cell-tag,
select.tags-input input,
select.tags-input button {
  height: 30px;
  line-height: 30px;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button,
select[multiple].cell-tag,
select[multiple].tags-input input,
select[multiple].tags-input button {
  height: auto;
}
.cell-tag,
.tags-input button {
  padding: 0px 4px;
}
.cell-tag {
  background-color: #fff;
  white-space: nowrap;
}
.tags-input input[type=text]:focus {
  outline: none;
  box-shadow: none;
  border-color: #ccc;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
[dir="rtl"] #kernel_logo_widget {
  float: left !important;
  float: left;
}
.modal .modal-body .move-path {
  display: flex;
  flex-direction: row;
  justify-content: space;
  align-items: center;
}
.modal .modal-body .move-path .server-root {
  padding-right: 20px;
}
.modal .modal-body .move-path .path-input {
  flex: 1;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
[dir="rtl"] #menubar .navbar-toggle {
  float: right;
}
[dir="rtl"] #menubar .navbar-collapse {
  clear: right;
}
[dir="rtl"] #menubar .navbar-nav {
  float: right;
}
[dir="rtl"] #menubar .nav {
  padding-right: 0px;
}
[dir="rtl"] #menubar .navbar-nav > li {
  float: right;
}
[dir="rtl"] #menubar .navbar-right {
  float: left !important;
}
[dir="rtl"] ul.dropdown-menu {
  text-align: right;
  left: auto;
}
[dir="rtl"] ul#new-menu.dropdown-menu {
  right: auto;
  left: 0;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
[dir="rtl"] i.menu-icon.pull-right {
  float: left !important;
  float: left;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
[dir="rtl"] ul#help_menu li a {
  padding-left: 2.2em;
}
[dir="rtl"] ul#help_menu li a i {
  margin-right: 0;
  margin-left: -1.2em;
}
[dir="rtl"] ul#help_menu li a i.pull-right {
  float: left !important;
  float: left;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
[dir="rtl"] .dropdown-submenu > .dropdown-menu {
  right: 100%;
  margin-right: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.fa-pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.fa-pull-right {
  margin-left: .3em;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
[dir="rtl"] .dropdown-submenu > a:after {
  float: left;
  content: "\f0d9";
  margin-right: 0;
  margin-left: -10px;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
[dir="rtl"] #notification_area {
  float: left !important;
  float: left;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] .indicator_area {
  float: left !important;
  float: left;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
[dir="rtl"] #kernel_indicator {
  float: left !important;
  float: left;
  border-left: 0;
  border-right: 1px solid;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] #modal_indicator {
  float: left !important;
  float: left;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  height: 30px;
  margin-top: 4px;
  display: flex;
  justify-content: flex-start;
  align-items: baseline;
  width: 50%;
  flex: 1;
}
span.save_widget span.filename {
  height: 100%;
  line-height: 1em;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  text-overflow: ellipsis;
  overflow: hidden;
  white-space: nowrap;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
[dir="rtl"] span.save_widget.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] span.save_widget span.filename {
  margin-left: 0;
  margin-right: 16px;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
  white-space: nowrap;
  padding: 0 5px;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
    padding: 0 0 0 5px;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
.toolbar-btn-label {
  margin-left: 6px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
[dir="rtl"] .btn-group > .btn,
.btn-group-vertical > .btn {
  float: right;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
[dir="rtl"] ul.typeahead-list i {
  margin-left: 0;
  margin-right: -10px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
ul.typeahead-list  > li > a.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .typeahead-list {
  text-align: right;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  min-width: 20px;
  color: transparent;
}
[dir="rtl"] .no-shortcut.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .command-shortcut.pull-right {
  float: left !important;
  float: left;
}
.command-shortcut:before {
  content: "(command mode)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
[dir="rtl"] .edit-shortcut.pull-right {
  float: left !important;
  float: left;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
[dir="ltr"] #find-and-replace .input-group-btn + .form-control {
  border-left: none;
}
[dir="rtl"] #find-and-replace .input-group-btn + .form-control {
  border-right: none;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/latest.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Project:-Investigate-a-Dataset-(Investigate-a-Dataset-(TMDb))">Project: Investigate a Dataset (Investigate a Dataset (TMDb))<a class="anchor-link" href="#Project:-Investigate-a-Dataset-(Investigate-a-Dataset-(TMDb))">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='intro'></a></p>
<h2 id="Introduction">Introduction<a class="anchor-link" href="#Introduction">&#182;</a></h2><blockquote><p><strong>Tip</strong>: In this section of the report, provide a brief introduction to the dataset you've selected for analysis. At the end of this section, describe the questions that you plan on exploring over the course of the report. Try to build your report around the analysis of at least one dependent variable and three independent variables.</p>
<p>If you haven't yet selected and downloaded your data, make sure you do that first before coming back here. If you're not sure what questions to ask right now, then make sure you familiarize yourself with the variables and the dataset context for ideas of what to explore.</p>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[305]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Use this cell to set up import statements for all of the packages that you</span>
<span class="c1">#   plan to use.</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">import</span> <span class="nn">json</span>
<span class="o">%</span><span class="k">matplotlib</span> inline
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[306]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">ast</span> <span class="kn">import</span> <span class="n">literal_eval</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='wrangling'></a></p>
<h2 id="Data-Wrangling">Data Wrangling<a class="anchor-link" href="#Data-Wrangling">&#182;</a></h2><h3 id="General-Properties">General Properties<a class="anchor-link" href="#General-Properties">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[307]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Load your data and print out a few lines. Perform operations to inspect data</span>
<span class="c1">#   types and look for instances of missing or possibly errant data.</span>
<span class="n">mov_df</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;tmdb_5000_movies.csv&#39;</span><span class="p">)</span>
<span class="n">mov_df</span><span class="o">.</span><span class="n">info</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>&lt;class &#39;pandas.core.frame.DataFrame&#39;&gt;
RangeIndex: 4803 entries, 0 to 4802
Data columns (total 20 columns):
 #   Column                Non-Null Count  Dtype  
---  ------                --------------  -----  
 0   budget                4803 non-null   int64  
 1   genres                4803 non-null   object 
 2   homepage              1712 non-null   object 
 3   id                    4803 non-null   int64  
 4   keywords              4803 non-null   object 
 5   original_language     4803 non-null   object 
 6   original_title        4803 non-null   object 
 7   overview              4800 non-null   object 
 8   popularity            4803 non-null   float64
 9   production_companies  4803 non-null   object 
 10  production_countries  4803 non-null   object 
 11  release_date          4802 non-null   object 
 12  revenue               4803 non-null   int64  
 13  runtime               4801 non-null   float64
 14  spoken_languages      4803 non-null   object 
 15  status                4803 non-null   object 
 16  tagline               3959 non-null   object 
 17  title                 4803 non-null   object 
 18  vote_average          4803 non-null   float64
 19  vote_count            4803 non-null   int64  
dtypes: float64(3), int64(4), object(13)
memory usage: 750.6+ KB
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[308]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">mov_df</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
<span class="c1">#revenue column has 25% of its values equal to zero.</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[308]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>budget</th>
      <th>id</th>
      <th>popularity</th>
      <th>revenue</th>
      <th>runtime</th>
      <th>vote_average</th>
      <th>vote_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>4.803000e+03</td>
      <td>4803.000000</td>
      <td>4803.000000</td>
      <td>4.803000e+03</td>
      <td>4801.000000</td>
      <td>4803.000000</td>
      <td>4803.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>2.904504e+07</td>
      <td>57165.484281</td>
      <td>21.492301</td>
      <td>8.226064e+07</td>
      <td>106.875859</td>
      <td>6.092172</td>
      <td>690.217989</td>
    </tr>
    <tr>
      <th>std</th>
      <td>4.072239e+07</td>
      <td>88694.614033</td>
      <td>31.816650</td>
      <td>1.628571e+08</td>
      <td>22.611935</td>
      <td>1.194612</td>
      <td>1234.585891</td>
    </tr>
    <tr>
      <th>min</th>
      <td>0.000000e+00</td>
      <td>5.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>7.900000e+05</td>
      <td>9014.500000</td>
      <td>4.668070</td>
      <td>0.000000e+00</td>
      <td>94.000000</td>
      <td>5.600000</td>
      <td>54.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>1.500000e+07</td>
      <td>14629.000000</td>
      <td>12.921594</td>
      <td>1.917000e+07</td>
      <td>103.000000</td>
      <td>6.200000</td>
      <td>235.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>4.000000e+07</td>
      <td>58610.500000</td>
      <td>28.313505</td>
      <td>9.291719e+07</td>
      <td>118.000000</td>
      <td>6.800000</td>
      <td>737.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>3.800000e+08</td>
      <td>459488.000000</td>
      <td>875.581305</td>
      <td>2.787965e+09</td>
      <td>338.000000</td>
      <td>10.000000</td>
      <td>13752.000000</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="budget-and-revenue-has-a-lot-of-zero-values.">budget and revenue has a lot of zero values.<a class="anchor-link" href="#budget-and-revenue-has-a-lot-of-zero-values.">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[309]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">mov_df</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">12</span><span class="p">,</span><span class="mi">12</span><span class="p">))</span>

<span class="c1"># budget and revenue has alot of zeros .</span>
<span class="n">s</span> <span class="o">=</span> <span class="n">mov_df</span><span class="p">[</span><span class="n">mov_df</span><span class="o">.</span><span class="n">revenue</span> <span class="o">==</span> <span class="mi">0</span><span class="p">]</span>
<span class="n">s</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[309]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(1427, 20)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Data-cleaning">Data cleaning<a class="anchor-link" href="#Data-cleaning">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[310]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">mov_df</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">.</span><span class="n">any</span><span class="p">()</span>
<span class="c1"># homepage,overview,release_date and tagline has Null values.</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[310]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>budget                  False
genres                  False
homepage                 True
id                      False
keywords                False
original_language       False
original_title          False
overview                 True
popularity              False
production_companies    False
production_countries    False
release_date             True
revenue                 False
runtime                  True
spoken_languages        False
status                  False
tagline                  True
title                   False
vote_average            False
vote_count              False
dtype: bool</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="...-we-will-not-drop-null-values-until-selecting-our-prefered-columns.">... we will not drop null values until selecting our prefered columns.<a class="anchor-link" href="#...-we-will-not-drop-null-values-until-selecting-our-prefered-columns.">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[311]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">mov_df</span><span class="o">.</span><span class="n">columns</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[311]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Index([&#39;budget&#39;, &#39;genres&#39;, &#39;homepage&#39;, &#39;id&#39;, &#39;keywords&#39;, &#39;original_language&#39;,
       &#39;original_title&#39;, &#39;overview&#39;, &#39;popularity&#39;, &#39;production_companies&#39;,
       &#39;production_countries&#39;, &#39;release_date&#39;, &#39;revenue&#39;, &#39;runtime&#39;,
       &#39;spoken_languages&#39;, &#39;status&#39;, &#39;tagline&#39;, &#39;title&#39;, &#39;vote_average&#39;,
       &#39;vote_count&#39;],
      dtype=&#39;object&#39;)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[312]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># we will ignore columns that has no added value </span>
<span class="n">filtered_mov</span><span class="o">=</span><span class="n">mov_df</span><span class="p">[[</span><span class="s1">&#39;budget&#39;</span><span class="p">,</span> <span class="s1">&#39;genres&#39;</span><span class="p">,</span><span class="s1">&#39;original_language&#39;</span><span class="p">,</span> <span class="s1">&#39;popularity&#39;</span><span class="p">,</span> <span class="s1">&#39;production_companies&#39;</span><span class="p">,</span>
       <span class="s1">&#39;production_countries&#39;</span><span class="p">,</span> <span class="s1">&#39;release_date&#39;</span><span class="p">,</span> <span class="s1">&#39;revenue&#39;</span><span class="p">,</span> <span class="s1">&#39;runtime&#39;</span><span class="p">,</span> <span class="s1">&#39;title&#39;</span><span class="p">,</span> <span class="s1">&#39;vote_average&#39;</span><span class="p">,</span>
       <span class="s1">&#39;vote_count&#39;</span><span class="p">]]</span>
<span class="n">filtered_mov</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">.</span><span class="n">any</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[312]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>budget                  False
genres                  False
original_language       False
popularity              False
production_companies    False
production_countries    False
release_date             True
revenue                 False
runtime                  True
title                   False
vote_average            False
vote_count              False
dtype: bool</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[313]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#then we drop null values in selected df</span>
<span class="n">filtered_mov_1</span><span class="o">=</span><span class="n">filtered_mov</span><span class="o">.</span><span class="n">dropna</span><span class="p">()</span>
<span class="n">filtered_mov_1</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">.</span><span class="n">any</span><span class="p">()</span>
<span class="n">filtered_mov_1</span><span class="o">.</span><span class="n">head</span><span class="p">(</span><span class="mi">2</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[313]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>budget</th>
      <th>genres</th>
      <th>original_language</th>
      <th>popularity</th>
      <th>production_companies</th>
      <th>production_countries</th>
      <th>release_date</th>
      <th>revenue</th>
      <th>runtime</th>
      <th>title</th>
      <th>vote_average</th>
      <th>vote_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>237000000</td>
      <td>[{"id": 28, "name": "Action"}, {"id": 12, "nam...</td>
      <td>en</td>
      <td>150.437577</td>
      <td>[{"name": "Ingenious Film Partners", "id": 289...</td>
      <td>[{"iso_3166_1": "US", "name": "United States o...</td>
      <td>2009-12-10</td>
      <td>2787965087</td>
      <td>162.0</td>
      <td>Avatar</td>
      <td>7.2</td>
      <td>11800</td>
    </tr>
    <tr>
      <th>1</th>
      <td>300000000</td>
      <td>[{"id": 12, "name": "Adventure"}, {"id": 14, "...</td>
      <td>en</td>
      <td>139.082615</td>
      <td>[{"name": "Walt Disney Pictures", "id": 2}, {"...</td>
      <td>[{"iso_3166_1": "US", "name": "United States o...</td>
      <td>2007-05-19</td>
      <td>961000000</td>
      <td>169.0</td>
      <td>Pirates of the Caribbean: At World's End</td>
      <td>6.9</td>
      <td>4500</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[314]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#column release_date has a string value </span>
<span class="nb">type</span><span class="p">(</span><span class="n">filtered_mov_1</span><span class="p">[</span><span class="s1">&#39;release_date&#39;</span><span class="p">][</span><span class="mi">0</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[314]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>str</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[315]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#we have to change to date data type </span>
<span class="n">mov_copy</span> <span class="o">=</span> <span class="n">filtered_mov_1</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;release_date&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">to_datetime</span><span class="p">(</span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;release_date&#39;</span><span class="p">])</span>
<span class="c1">#chcek release_date data type</span>
<span class="n">mov_copy</span><span class="o">.</span><span class="n">dtypes</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[315]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>budget                           int64
genres                          object
original_language               object
popularity                     float64
production_companies            object
production_countries            object
release_date            datetime64[ns]
revenue                          int64
runtime                        float64
title                           object
vote_average                   float64
vote_count                       int64
dtype: object</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h5 id="&#9679;-genres-,-production_companies-,-production_countries-has-list-of-dicts.">&#9679; genres , production_companies , production_countries has list of dicts.<a class="anchor-link" href="#&#9679;-genres-,-production_companies-,-production_countries-has-list-of-dicts.">&#182;</a></h5><h4 id="&#9679;-we-can-extract-first-single-value">&#9679; we can extract first single value<a class="anchor-link" href="#&#9679;-we-can-extract-first-single-value">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[316]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># we need to transform dicts to single values</span>
<span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;genres&#39;</span><span class="p">][</span><span class="mi">0</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[316]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&#39;[{&#34;id&#34;: 28, &#34;name&#34;: &#34;Action&#34;}, {&#34;id&#34;: 12, &#34;name&#34;: &#34;Adventure&#34;}, {&#34;id&#34;: 14, &#34;name&#34;: &#34;Fantasy&#34;}, {&#34;id&#34;: 878, &#34;name&#34;: &#34;Science Fiction&#34;}]&#39;</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[317]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#extract dicts  to list items </span>
<span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;genres&#39;</span><span class="p">]</span> <span class="o">=</span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;genres&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="n">literal_eval</span><span class="p">)</span>
<span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;production_companies&#39;</span><span class="p">]</span> <span class="o">=</span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;production_companies&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="n">literal_eval</span><span class="p">)</span>
<span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;production_countries&#39;</span><span class="p">]</span> <span class="o">=</span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;production_countries&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="n">literal_eval</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[318]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#Now column type is list not str</span>
<span class="nb">type</span><span class="p">(</span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;genres&#39;</span><span class="p">][</span><span class="mi">0</span><span class="p">])</span>
<span class="nb">len</span><span class="p">(</span><span class="n">mov_copy</span><span class="p">)</span>
<span class="nb">len</span><span class="p">(</span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;genres&#39;</span><span class="p">][</span><span class="mi">34</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[318]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>2</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[319]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">getTopGeneres</span><span class="p">(</span><span class="n">column</span><span class="p">):</span>
        <span class="c1">#return first  genere ,country or language of a movie</span>
        <span class="n">names</span> <span class="o">=</span> <span class="p">[</span><span class="n">row</span><span class="p">[</span><span class="s1">&#39;name&#39;</span><span class="p">]</span> <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">column</span><span class="p">]</span>
        <span class="n">names</span> <span class="o">=</span> <span class="n">names</span><span class="p">[</span><span class="mi">0</span><span class="p">:</span><span class="mi">1</span><span class="p">]</span>
        <span class="k">return</span> <span class="n">names</span>

<span class="k">def</span> <span class="nf">listItemToString</span><span class="p">(</span><span class="n">st</span><span class="p">):</span>  
    <span class="c1">#return string of a list item .</span>
    <span class="n">string</span> <span class="o">=</span> <span class="s2">&quot; &quot;</span>  
    <span class="k">return</span> <span class="p">(</span><span class="n">string</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">st</span><span class="p">))</span>  



<span class="c1">#genres column</span>
<span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;genres&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;genres&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="n">getTopGeneres</span><span class="p">)</span>
<span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;genres&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;genres&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="n">listItemToString</span><span class="p">)</span>

<span class="c1">#production_companies</span>
<span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;production_companies&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;production_companies&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="n">getTopGeneres</span><span class="p">)</span>
<span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;production_companies&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;production_companies&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="n">listItemToString</span><span class="p">)</span>

<span class="c1">#production_countries</span>
<span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;production_countries&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;production_countries&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="n">getTopGeneres</span><span class="p">)</span>
<span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;production_countries&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;production_countries&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="n">listItemToString</span><span class="p">)</span>



<span class="n">mov_copy</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[319]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>budget</th>
      <th>genres</th>
      <th>original_language</th>
      <th>popularity</th>
      <th>production_companies</th>
      <th>production_countries</th>
      <th>release_date</th>
      <th>revenue</th>
      <th>runtime</th>
      <th>title</th>
      <th>vote_average</th>
      <th>vote_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>237000000</td>
      <td>Action</td>
      <td>en</td>
      <td>150.437577</td>
      <td>Ingenious Film Partners</td>
      <td>United States of America</td>
      <td>2009-12-10</td>
      <td>2787965087</td>
      <td>162.0</td>
      <td>Avatar</td>
      <td>7.2</td>
      <td>11800</td>
    </tr>
    <tr>
      <th>1</th>
      <td>300000000</td>
      <td>Adventure</td>
      <td>en</td>
      <td>139.082615</td>
      <td>Walt Disney Pictures</td>
      <td>United States of America</td>
      <td>2007-05-19</td>
      <td>961000000</td>
      <td>169.0</td>
      <td>Pirates of the Caribbean: At World's End</td>
      <td>6.9</td>
      <td>4500</td>
    </tr>
    <tr>
      <th>2</th>
      <td>245000000</td>
      <td>Action</td>
      <td>en</td>
      <td>107.376788</td>
      <td>Columbia Pictures</td>
      <td>United Kingdom</td>
      <td>2015-10-26</td>
      <td>880674609</td>
      <td>148.0</td>
      <td>Spectre</td>
      <td>6.3</td>
      <td>4466</td>
    </tr>
    <tr>
      <th>3</th>
      <td>250000000</td>
      <td>Action</td>
      <td>en</td>
      <td>112.312950</td>
      <td>Legendary Pictures</td>
      <td>United States of America</td>
      <td>2012-07-16</td>
      <td>1084939099</td>
      <td>165.0</td>
      <td>The Dark Knight Rises</td>
      <td>7.6</td>
      <td>9106</td>
    </tr>
    <tr>
      <th>4</th>
      <td>260000000</td>
      <td>Action</td>
      <td>en</td>
      <td>43.926995</td>
      <td>Walt Disney Pictures</td>
      <td>United States of America</td>
      <td>2012-03-07</td>
      <td>284139100</td>
      <td>132.0</td>
      <td>John Carter</td>
      <td>6.1</td>
      <td>2124</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[320]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;budget&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[320]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>29060068.024791665</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[321]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">len</span><span class="p">(</span><span class="n">mov_copy</span><span class="p">[</span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;budget&#39;</span><span class="p">]</span>  <span class="o">&lt;</span> <span class="mi">1000</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[321]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>1067</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[322]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">mov_copy</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[322]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>budget</th>
      <th>popularity</th>
      <th>revenue</th>
      <th>runtime</th>
      <th>vote_average</th>
      <th>vote_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>4.800000e+03</td>
      <td>4800.000000</td>
      <td>4.800000e+03</td>
      <td>4800.000000</td>
      <td>4800.000000</td>
      <td>4800.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>2.906007e+07</td>
      <td>21.505569</td>
      <td>8.231205e+07</td>
      <td>106.898125</td>
      <td>6.094458</td>
      <td>690.646875</td>
    </tr>
    <tr>
      <th>std</th>
      <td>4.073029e+07</td>
      <td>31.822163</td>
      <td>1.628950e+08</td>
      <td>22.561593</td>
      <td>1.188366</td>
      <td>1234.852449</td>
    </tr>
    <tr>
      <th>min</th>
      <td>0.000000e+00</td>
      <td>0.000372</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>8.000000e+05</td>
      <td>4.682212</td>
      <td>0.000000e+00</td>
      <td>94.000000</td>
      <td>5.600000</td>
      <td>54.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>1.500000e+07</td>
      <td>12.928897</td>
      <td>1.918199e+07</td>
      <td>103.000000</td>
      <td>6.200000</td>
      <td>236.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>4.000000e+07</td>
      <td>28.350628</td>
      <td>9.293886e+07</td>
      <td>118.000000</td>
      <td>6.800000</td>
      <td>737.250000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>3.800000e+08</td>
      <td>875.581305</td>
      <td>2.787965e+09</td>
      <td>338.000000</td>
      <td>10.000000</td>
      <td>13752.000000</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="mov_copy-has-outliers-in-budget-,-vote_count-and-revenue-so-we-have-to-deal-with">mov_copy has outliers in budget , vote_count and revenue so we have to deal with<a class="anchor-link" href="#mov_copy-has-outliers-in-budget-,-vote_count-and-revenue-so-we-have-to-deal-with">&#182;</a></h4><h4 id="we-detect-outliers-and-remove-.">we detect outliers and remove .<a class="anchor-link" href="#we-detect-outliers-and-remove-.">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[323]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">mov_copy</span><span class="o">=</span><span class="n">mov_copy</span><span class="p">[(</span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;budget&#39;</span><span class="p">]</span><span class="o">&gt;</span> <span class="mi">800000</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;vote_count&#39;</span><span class="p">]</span><span class="o">&gt;</span> <span class="mi">54</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;revenue&#39;</span><span class="p">]</span><span class="o">&gt;</span> <span class="mf">1.9</span><span class="p">)]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[324]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">mov_copy</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
<span class="n">mov_copy</span><span class="o">.</span><span class="n">info</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>&lt;class &#39;pandas.core.frame.DataFrame&#39;&gt;
Int64Index: 2867 entries, 0 to 4758
Data columns (total 12 columns):
 #   Column                Non-Null Count  Dtype         
---  ------                --------------  -----         
 0   budget                2867 non-null   int64         
 1   genres                2867 non-null   object        
 2   original_language     2867 non-null   object        
 3   popularity            2867 non-null   float64       
 4   production_companies  2867 non-null   object        
 5   production_countries  2867 non-null   object        
 6   release_date          2867 non-null   datetime64[ns]
 7   revenue               2867 non-null   int64         
 8   runtime               2867 non-null   float64       
 9   title                 2867 non-null   object        
 10  vote_average          2867 non-null   float64       
 11  vote_count            2867 non-null   int64         
dtypes: datetime64[ns](1), float64(3), int64(3), object(5)
memory usage: 291.2+ KB
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[329]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">mov_copy</span><span class="p">[</span><span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;revenue&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;revenue&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">max</span><span class="p">()]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[329]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>budget</th>
      <th>genres</th>
      <th>original_language</th>
      <th>popularity</th>
      <th>production_companies</th>
      <th>production_countries</th>
      <th>release_date</th>
      <th>revenue</th>
      <th>runtime</th>
      <th>title</th>
      <th>vote_average</th>
      <th>vote_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>237000000</td>
      <td>Action</td>
      <td>en</td>
      <td>150.437577</td>
      <td>Ingenious Film Partners</td>
      <td>United States of America</td>
      <td>2009-12-10</td>
      <td>2787965087</td>
      <td>162.0</td>
      <td>Avatar</td>
      <td>7.2</td>
      <td>11800</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='eda'></a></p>
<h2 id="Exploratory-Data-Analysis">Exploratory Data Analysis<a class="anchor-link" href="#Exploratory-Data-Analysis">&#182;</a></h2><h3 id="Research-Question-1:-Is-there-a-relation-between-the-budget-and-the-revenue-?">Research Question 1: Is there a relation between the budget and the revenue ?<a class="anchor-link" href="#Research-Question-1:-Is-there-a-relation-between-the-budget-and-the-revenue-?">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[332]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">mov_copy</span><span class="o">.</span><span class="n">revenue</span><span class="p">,</span> <span class="n">mov_copy</span><span class="o">.</span><span class="n">budget</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Revenue&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Budget&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Revnue &amp; Budget Relatioship&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">20</span><span class="p">,</span> <span class="mi">20</span><span class="p">))</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[332]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;Figure size 1440x1440 with 0 Axes&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_text output_subarea ">
<pre>&lt;Figure size 1440x1440 with 0 Axes&gt;</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="&#9679;-we-notice-there-is-a-positive-relation-between-budget-and-revenue">&#9679; we notice there is a positive relation between budget and revenue<a class="anchor-link" href="#&#9679;-we-notice-there-is-a-positive-relation-between-budget-and-revenue">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Research-Question-2:-which-genre-made-more-money-?">Research Question 2: which genre made more money ?<a class="anchor-link" href="#Research-Question-2:-which-genre-made-more-money-?">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[348]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#extract total revenue per genre.</span>
<span class="n">genres_sum</span> <span class="o">=</span><span class="n">mov_copy</span><span class="o">.</span><span class="n">groupby</span><span class="p">(</span><span class="s1">&#39;genres&#39;</span><span class="p">)</span><span class="o">.</span><span class="n">revenue</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
<span class="n">genres_sum</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">kind</span> <span class="o">=</span><span class="s1">&#39;bar&#39;</span><span class="p">,</span><span class="n">figsize</span> <span class="o">=</span><span class="p">(</span><span class="mi">8</span><span class="p">,</span><span class="mi">8</span><span class="p">))</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[348]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x7f856539e710&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="&#9679;-we-see-that-Action-and-Adventure-made-more-money-than-others.">&#9679; we see that Action and Adventure made more money than others.<a class="anchor-link" href="#&#9679;-we-see-that-Action-and-Adventure-made-more-money-than-others.">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Research-Question-3:-which-copmany-has-the-biggest-Market-share--in-each-year?">Research Question 3: which copmany has the biggest Market share  in each year?<a class="anchor-link" href="#Research-Question-3:-which-copmany-has-the-biggest-Market-share--in-each-year?">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[644]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">mov_copy</span><span class="o">.</span><span class="n">tail</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[644]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>budget</th>
      <th>genres</th>
      <th>original_language</th>
      <th>popularity</th>
      <th>production_companies</th>
      <th>production_countries</th>
      <th>release_date</th>
      <th>revenue</th>
      <th>runtime</th>
      <th>title</th>
      <th>vote_average</th>
      <th>vote_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4535</th>
      <td>2000000</td>
      <td>Action</td>
      <td>ja</td>
      <td>39.756748</td>
      <td>Toho Company</td>
      <td>Japan</td>
      <td>1954</td>
      <td>271841</td>
      <td>207.0</td>
      <td>Seven Samurai</td>
      <td>8.2</td>
      <td>878</td>
    </tr>
    <tr>
      <th>4586</th>
      <td>35000000</td>
      <td>Comedy</td>
      <td>da</td>
      <td>38.100488</td>
      <td>Twentieth Century Fox Film Corporation</td>
      <td>United States of America</td>
      <td>2008</td>
      <td>170000000</td>
      <td>99.0</td>
      <td>What Happens in Vegas</td>
      <td>5.8</td>
      <td>923</td>
    </tr>
    <tr>
      <th>4596</th>
      <td>6000000</td>
      <td>Horror</td>
      <td>en</td>
      <td>19.331884</td>
      <td>La Petite Reine</td>
      <td>France</td>
      <td>2012</td>
      <td>31081</td>
      <td>89.0</td>
      <td>Maniac</td>
      <td>6.0</td>
      <td>316</td>
    </tr>
    <tr>
      <th>4720</th>
      <td>8500000</td>
      <td>Drama</td>
      <td>en</td>
      <td>9.452808</td>
      <td>Phantom Four</td>
      <td>United States of America</td>
      <td>2016</td>
      <td>15861566</td>
      <td>120.0</td>
      <td>The Birth of a Nation</td>
      <td>6.5</td>
      <td>178</td>
    </tr>
    <tr>
      <th>4758</th>
      <td>4000000</td>
      <td>Thriller</td>
      <td>en</td>
      <td>27.662696</td>
      <td>Automatik Entertainment</td>
      <td>United States of America</td>
      <td>2014</td>
      <td>600896</td>
      <td>95.0</td>
      <td>The Signal</td>
      <td>5.8</td>
      <td>631</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[350]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#extract year from date time.</span>
<span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;release_date&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">mov_copy</span><span class="p">[</span><span class="s1">&#39;release_date&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">year</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[653]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#each year companies.</span>
<span class="n">each_year_companies</span> <span class="o">=</span> <span class="n">mov_copy</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">&#39;release_date&#39;</span> <span class="p">,</span><span class="s1">&#39;production_companies&#39;</span><span class="p">])[</span><span class="s1">&#39;revenue&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
<span class="c1">#create data frame .</span>
<span class="n">df</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">each_year_companies</span><span class="p">)</span><span class="o">.</span><span class="n">reset_index</span><span class="p">()</span>
<span class="n">df</span><span class="o">.</span><span class="n">columns</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">,</span> <span class="s1">&#39;production_company&#39;</span><span class="p">,</span><span class="s1">&#39;revenue&#39;</span><span class="p">]</span>
<span class="nb">type</span><span class="p">(</span><span class="n">df</span><span class="p">)</span>
<span class="c1">#get first 5 companies with high revenue in each year.</span>
<span class="n">df</span><span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;revenue&#39;</span><span class="p">],</span><span class="n">ascending</span><span class="o">=</span><span class="p">[</span><span class="kc">True</span><span class="p">,</span> <span class="kc">False</span><span class="p">])</span>
<span class="n">df1</span> <span class="o">=</span><span class="n">df</span><span class="o">.</span><span class="n">groupby</span><span class="p">(</span><span class="s1">&#39;year&#39;</span><span class="p">)</span><span class="o">.</span><span class="n">head</span><span class="p">(</span><span class="mi">5</span><span class="p">)</span>


<span class="c1">#plot year with revenue and the highest companies by revenue.</span>
<span class="n">ax</span> <span class="o">=</span> <span class="n">df1</span><span class="o">.</span><span class="n">tail</span><span class="p">(</span><span class="mi">40</span><span class="p">)</span><span class="o">.</span><span class="n">plot</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">&#39;revenue&#39;</span><span class="p">,</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">16</span><span class="p">,</span><span class="mi">16</span><span class="p">),</span><span class="n">width</span><span class="o">=</span><span class="mf">0.5</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;#5cb85c&#39;</span><span class="p">,</span><span class="s1">&#39;#5bc0de&#39;</span><span class="p">,</span><span class="s1">&#39;#CCCC00&#39;</span><span class="p">,</span><span class="s1">&#39;#FFC0CB&#39;</span><span class="p">,</span><span class="s1">&#39;#d9534f&#39;</span><span class="p">])</span>
<span class="n">a</span> <span class="o">=</span> <span class="n">ax</span><span class="o">.</span><span class="n">set_xticklabels</span><span class="p">(</span><span class="nb">list</span><span class="p">(</span><span class="n">df1</span><span class="o">.</span><span class="n">tail</span><span class="p">(</span><span class="mi">40</span><span class="p">)[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="nb">str</span><span class="p">)</span><span class="o">+</span> <span class="s2">&quot; __&quot;</span><span class="o">+</span> <span class="n">df1</span><span class="o">.</span><span class="n">tail</span><span class="p">(</span><span class="mi">40</span><span class="p">)[</span><span class="s1">&#39;production_company&#39;</span><span class="p">]))</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAA6IAAASECAYAAAB+qrIiAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4xLjMsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+AADFEAAAgAElEQVR4nOzdb2xd9X348c+NbxLHOKWJLbY4CahJQSUdFEikUCgZFJdkUNY9yIJAi6hK1VaZiqKtEKiq5cmY8oesNGsy1MHQhMoKottUTUMFj1+EphbWKCBlZSKmMNGSZMz5o4SUhDq+vwdoHsbX2Df2+fge5/V6FJ/79cff3MON/OYc+1ZqtVotAAAAIMm0yd4AAAAAZxchCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQKrqZH7xnTt3xp49e+Lcc8+Nbdu2feja//mf/4m//uu/jmPHjkV7e3t8/etfj46OjqSdAgAAMFEm9YrotddeG9/85jfHtPbRRx+NFStWxP333x+rV6+Oxx57rODdAQAAUIRJvSK6ZMmSeOutt4YcO3jwYDz88MNx7NixmDlzZnz1q1+N+fPnx69+9au4/fbbIyLik5/8ZGzdunUytgwAAMA4Nd3PiH7ve9+LL33pS7F58+ZYu3ZtPPTQQxERccEFF8QLL7wQERH//u//Hu+8804cP358MrcKAADAGZjUK6IfdPLkyXjllVfiL//yLweP9ff3R0TE2rVr42//9m9j165dcfHFF8fcuXOjpaVlsrYKAADAGWqqEB0YGIhzzjmn7m23c+fOjW984xsR8V6wvvDCC9HW1pa9RQAAAMapqW7NbWtri/POOy9++tOfRkRErVaL//qv/4qIiGPHjsXAwEBERPzjP/5jXHfddZO1TQAAAMahUqvVapP1xR944IF4+eWX4/jx43HuuefGmjVr4nd+53fib/7mb+Lo0aPR398fV199daxevTqef/75eOyxx6JSqcTFF18cd9xxR0yfPn2ytg4AAMAZmtQQBQAA4OzTVLfmAgAAMPUJUQAAAFJN6m/N3b9//5jWdXZ2Rl9fXyF7KGp22eYWObtsc4ucXba5Rc4u29wiZ5tb/OyyzS1ydtnmFjm7bHOLnF22uUXOLtvcImeXbW6Rs8s2t8jZjczt6uoa8TFXRAEAAEglRAEAAEglRAEAAEg1qT8jCgAA0GxqtVqcPHkyBgYGolKpxH//93/HqVOnJvzrFDW3yNkfnFur1WLatGnR2toalUplzHOEKAAAwPucPHkypk+fHtXqe7lUrVajpaVlwr9OUXOLnF1vbn9/f5w8eTJmzZo15jluzQUAAHifgYGBwQhldNVqNQYGBhr6HCEKAADwPo3cYsp7Gn3OhCgAAACpXG8GAAD4EH/64p9O6LzNl2ye0Hll5IooAABAE6vVag3/DGazE6IAAABN5pe//GX87u/+btx7772xcuXKePLJJ+Pmm2+OlStXxle+8pU4ceJEPPvss/HVr3518HN+8pOfxO233x4REbt27Rq2PiJi+fLlcf/998fKlSvj+uuvj1dffTUiIrZt2xYPPvjg4KzPfvaz8ctf/jIiIn74wx/GTTfdFJ/73OfiG9/4Rpw+fXrcfz8hCgAA0IR+8YtfxOrVq+MHP/hB/OAHP4jHH388fvzjH8enPvWp+N73vhcrVqyIPXv2xK9//euIiPjRj34Uv//7vx+HDx+Ob3/728PW/6+5c+fGj3/841i7du2Q+Kynt7c3fvSjH8U//dM/xTPPPBMtLS3xD//wD+P+u/kZUQAAgCa0YMGCWLp0aTzzzDOxb9+++MIXvhAREb/5zW9i6dKlUa1W47rrrotnnnkmbrrppvjXf/3X+Na3vhU//elP667/X7/3e78XERGXXnppPPXUUx+6h3/7t3+LvXv3xo033hgREadOnYq5c+eO++8mRAEAAJpQW1tbRLz3M6IrVqyInTt3Dltz8803x9/93d/FRz/60bjsssuivb19cP2OHTvqzp05c2ZERLS0tAzeZtvS0jLk51BPnTo1+LX/8A//MO69996IeO89Q/v7+8f9d3NrLgAAQBNbunRp/OxnP4vXX389IiLeeeed+MUvfhEREVdddVXs3bs3vv/978fNN9886vqRLFy4MPbu3RsREXv37o033ngjIiI+85nPxD//8z9HX19fREQcOXIkfvWrX4377+SKKAAAwIfYdvm2CbkKeKY6Ojri29/+dvzxH/9xvPvuuxERcffdd8fixYujpaUluru744knnojvfOc7g+u/853v1F0/khtvvDGefPLJ+NznPheXXXZZLFq0KCIiLrroorj77rvj1ltvjVqtFtOnT48///M/jwULFozr7yREAQAAmszChQvj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pBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApBKiAAAApKpO9gYA4Gy2Ye+GMa/dfMnmAncCAHlcEQUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACBVdbI3AEDzurv31PCDvW/WXbvlwpkF7wYAmCpcEQUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACCVEAUAACDVqO8j2tfXFzt27IijR49GpVKJ7u7uuPHGG4es+fnPfx5btmyJ8847LyIili9fHqtXry5mx2eo7nvhRdR9PzzvhQcAAFCcUUO0paUl1q5dG4sWLYp33nkn7rnnnrj00ktjwYIFQ9ZdfPHFcc899xS2UQAAAKaGUW/NnTNnTixatCgiImbNmhXz58+Pw4cPF74xAAAApqZRr4i+31tvvRWvv/56fPzjHx/22L59++Kuu+6KOXPmxNq1a2PhwoXD1vT09ERPT09ERGzatCk6OzvPcNvvaejz69yCOyFzR1CtVidkTtbcomfXM96vVcbnomxzR+I1Uo65I/FvZ/PPHcnZ+BwXOdv5K+/comfX4/uW5p9b5OyyzS1y9kTNHXOInjx5MrZt2xZf/OIXo62tbchjH/vYx2Lnzp3R2toae/bsia1bt8b27duHzeju7o7u7u7Bj/v6+sax9fF/fpFzOzs7C9lfUXOLnl3PeL9WGZ+Lss0diddIOeaOxL+dzT93JGfjc1zkbOevvHOLnl2P71uaf26Rs8s2t8jZjczt6uoa8bEx/dbc/v7+2LZtW1xzzTWxfPnyYY+3tbVFa2trRERcccUVcfr06Th27NiYNgcAAMDZZdQQrdVq8eCDD8b8+fPj85//fN01R48ejVqtFhERr776agwMDMTs2bMndqcAAABMCaPemvvKK6/Ec889F+eff37cddddERFx6623Dl6OveGGG+L555+Pp59+OlpaWmLGjBmxfv36qFQqxe4cAACAUho1RD/xiU/EE0888aFrVq1aFatWrZqwTQEAADB1jelnRAEAAGCiCFEAAABSCVEAAABSCVEAAABSCVEAAABSCVEAAABSCVEAAABSCVEAAABSCVEAAABSCVEAAABSCVEAAABSCVEAAABSCVEAAABSCVEAAABSCVEAAABSCVEAAABSVSd7AwBAMe7uPTX8YO+bddduuXBmwbsBgP/jiigAAACphCgAAACphCgAAACphCgAAACphCgAAACphCgAAACphCgAAACphCgAAACphCgAAACphCgAAACphCgAAACphCgAAACphCgAAACphCgAAACphCgAAACpqpO9AQDOPgcOzB/h+PBj8+a9WfBuAIBsrogCAACQSogCAACQSogCAACQSogCAACQSogCAACQSogCAACQSogCAACQSogCAACQSogCAACQSogCAACQSogCAACQSogCAACQSogCAACQSogCAACQqjrZGwAAYKi7e0/Vf6D3zWGHtlw4s+DdAEw8V0QBAABIJUQBAABIJUQBAABIJUQBAABI5ZcVAQAApbJh74Yxr918yeYCd8KZckUUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVEIUAACAVNXJ3gAwtd3de6r+A71vDju05cKZBe8GAIBm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QCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQCohCgAAQKrqWBa99NJL8cgjj8TAwEBcf/318Qd/8AdDHt+1a1c8+uijMXfu3IiIWLVqVVx//fUTv1sAAABKb9QQHRgYiIcffji+9a1vRUdHR9x7772xbNmyWLBgwZB1V111Vdxxxx2FbRQAAICpYdRbc1999dX47d/+7fit3/qtqFarcdVVV8XPfvazjL0BAAAwBY16RfTw4cPR0dEx+HFHR0f09vYOW/fCCy/Ef/7nf8a8efPi9ttvj87OzmFrenp6oqenJyIiNm3aVHdNIxr6/N43C5l74MDYt9Do7OjdX8jct8e+g3Gfowmb3QTnr6hz1+jsZjh/zXDuIprj/JXt3DU8u2yvvYgpff4afy5Kdv6a4Nw1OruwuU1w7hqd3Qznz7+dZzbX9y3v4/uWQUWfu1FDtFarDTtWqVSGfLx06dK4+uqrY/r06fH000/Hjh07YuPGjcM+r7u7O7q7uwc/7uvra3jD7zfez8+e2+jsroLmNqJZnouyzW3k3DU629ziZ3vtlXvuVD5/U/2/i2Y4d0XOLtvcRmc3w/lrlueibHN939Jccxud3cyvva6ukXc36q25HR0dcejQocGPDx06FHPmzBmyZvbs2TF9+vSIeC82X3vttTFtGAAAgLPPqCG6ePHiOHDgQLz11lvR398fP/nJT2LZsmVD1hw5cmTwz7t37x72i4wAAADgf416a25LS0t86Utfivvuuy8GBgbiuuuui4ULF8bjjz8e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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="&#9679;-we-conclude--that-Twentieth-Century-Fox-Film-Corporation-has-the-biggest--revenue-share-at-2016-and-universal-pictures-doing-very-well-in-2015-(bar-with-green-color)">&#9679; we conclude  that Twentieth Century Fox Film Corporation has the biggest  revenue share at 2016 and universal pictures doing very well in 2015 (bar with green color)<a class="anchor-link" href="#&#9679;-we-conclude--that-Twentieth-Century-Fox-Film-Corporation-has-the-biggest--revenue-share-at-2016-and-universal-pictures-doing-very-well-in-2015-(bar-with-green-color)">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='conclusions'></a></p>
<h2 id="Conclusions">Conclusions<a class="anchor-link" href="#Conclusions">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h6 id="*-Is-there-a-relation-between-the-budget-and-the-revenue-?">* Is there a relation between the budget and the revenue ?<a class="anchor-link" href="#*-Is-there-a-relation-between-the-budget-and-the-revenue-?">&#182;</a></h6>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h6 id="&#9679;__-&#9679;-there-is-a-positive-relation-between-budget-and-revenue">&#9679;<em>__</em> &#9679; there is a positive relation between budget and revenue<a class="anchor-link" href="#&#9679;__-&#9679;-there-is-a-positive-relation-between-budget-and-revenue">&#182;</a></h6>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h5 id="*-which-genre-made-more-money-?">* which genre made more money ?<a class="anchor-link" href="#*-which-genre-made-more-money-?">&#182;</a></h5>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h6 id="&#9679;__-&#9679;-we-see-that-Action-and-Adventure-made-more-money-than-others.">&#9679;<em>__</em> &#9679; we see that Action and Adventure made more money than others.<a class="anchor-link" href="#&#9679;__-&#9679;-we-see-that-Action-and-Adventure-made-more-money-than-others.">&#182;</a></h6>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h5 id="*which-copmany-has-the-biggest-Market-share-in-each-year?">*which copmany has the biggest Market share in each year?<a class="anchor-link" href="#*which-copmany-has-the-biggest-Market-share-in-each-year?">&#182;</a></h5>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h6 id="&#9679;__-&#9679;-we-conclude-that-Twentieth-Century-Fox-Film-Corporation-has-the-biggest-revenue-share-at-2016-and-universal-pictures-doing-very-well-in-2015-(bar-with-green-color)">&#9679;<em>__</em> &#9679; we conclude that Twentieth Century Fox Film Corporation has the biggest revenue share at 2016 and universal pictures doing very well in 2015 (bar with green color)<a class="anchor-link" href="#&#9679;__-&#9679;-we-conclude-that-Twentieth-Century-Fox-Film-Corporation-has-the-biggest-revenue-share-at-2016-and-universal-pictures-doing-very-well-in-2015-(bar-with-green-color)">&#182;</a></h6>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
    </div>
  </div>
</body>

 


</html>
