```html
<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<title>mushrooms-classifications</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
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
    color: #000 !important;
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
 *  Font Awesome 4.2.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.2.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.2.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.2.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.2.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.2.0#fontawesomeregular') format('svg');
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
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=1);
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2);
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=3);
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1);
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1);
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
.fa-gittip:before {
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
.fa-pied-piper:before {
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
@media (max-width: 991px) {
  #ipython_notebook {
    margin-left: 10px;
  }
}
[dir="rtl"] #ipython_notebook {
  float: right !important;
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
span#login_widget {
  float: right;
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
  text-align: center;
  vertical-align: middle;
  display: inline;
  opacity: 0;
  z-index: 2;
  width: 12ex;
  margin-right: -12ex;
}
.alternate_upload .btn-upload {
  height: 22px;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
[dir="rtl"] #tabs li {
  float: right;
}
ul#tabs {
  margin-bottom: 4px;
}
[dir="rtl"] ul#tabs {
  margin-right: 0px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
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
[dir="rtl"] .list_toolbar .tree-buttons {
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-right {
  padding-top: 1px;
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-left {
  float: right !important;
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
  vertical-align: baseline;
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
#tree-selector {
  padding-right: 0px;
}
[dir="rtl"] #tree-selector a {
  float: right;
}
#button-select-all {
  min-width: 50px;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
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
[dir="rtl"] #new-menu {
  text-align: right;
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
[dir="rtl"] #running .col-sm-8 {
  float: right !important;
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
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI colors. */
.ansibold {
  font-weight: bold;
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
  border-left-width: 1px;
  padding-left: 5px;
  background: linear-gradient(to right, transparent -40px, transparent 1px, transparent 1px, transparent 100%);
}
div.cell.jupyter-soft-selected {
  border-left-color: #90CAF9;
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
div.cell.selected {
  border-color: #ababab;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 5px, transparent 5px, transparent 100%);
}
@media print {
  div.cell.selected {
    border-color: transparent;
  }
}
div.cell.selected.jupyter-soft-selected {
  border-left-width: 0;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 7px, #E3F2FD 7px, #E3F2FD 100%);
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #66BB6A -40px, #66BB6A 5px, transparent 5px, transparent 100%);
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
  padding: 0.4em;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. We need the 0 value because of how we size */
  /* .CodeMirror-lines */
  padding: 0;
  border: 0;
  border-radius: 0;
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
  padding: 0;
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
.rendered_html ul {
  list-style: disc;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ul ul {
  list-style: square;
  margin: 0em 2em;
}
.rendered_html ul ul ul {
  list-style: circle;
  margin: 0em 2em;
}
.rendered_html ol {
  list-style: decimal;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
  margin: 0em 2em;
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
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  background-color: #fff;
  color: #000;
  font-size: 100%;
  padding: 0px;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: 1px solid black;
  border-collapse: collapse;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  border: 1px solid black;
  border-collapse: collapse;
  margin: 1em 2em;
}
.rendered_html td,
.rendered_html th {
  text-align: left;
  vertical-align: middle;
  padding: 4px;
}
.rendered_html th {
  font-weight: bold;
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
.text_cell.unrendered .text_cell_render {
  display: none;
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
#kernel_logo_widget {
  float: right !important;
  float: right;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
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
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
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
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
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
  margin-top: 6px;
}
span.save_widget span.filename {
  height: 1em;
  line-height: 1em;
  padding: 3px;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
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
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
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
  display: none;
}
.command-shortcut:before {
  content: "(command)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
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

/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }

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
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS_HTML"></script>
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

<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">os</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">warnings</span>
<span class="n">warnings</span><span class="o">.</span><span class="n">filterwarnings</span><span class="p">(</span><span class="s2">&quot;ignore&quot;</span><span class="p">)</span>

<span class="n">INPUT_FILE</span> <span class="o">=</span> <span class="s2">&quot;mushrooms.csv&quot;</span>

<span class="k">def</span> <span class="nf">load_data</span><span class="p">(</span><span class="n">file</span><span class="o">=</span><span class="n">INPUT_FILE</span><span class="p">,</span> <span class="n">header</span><span class="o">=</span><span class="kc">True</span><span class="p">):</span>
    <span class="n">csv_path</span> <span class="o">=</span> <span class="n">os</span><span class="o">.</span><span class="n">path</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="s2">&quot;&quot;</span><span class="p">,</span> <span class="n">file</span><span class="p">)</span>
    <span class="k">if</span> <span class="n">header</span><span class="p">:</span>
        <span class="k">return</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="n">csv_path</span><span class="p">)</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="k">return</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="n">csv_path</span><span class="p">,</span> <span class="n">header</span><span class="o">=</span><span class="kc">None</span><span class="p">)</span>


<span class="n">data</span> <span class="o">=</span> <span class="n">load_data</span><span class="p">(</span><span class="n">INPUT_FILE</span><span class="p">)</span>
<span class="n">data</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[1]:</div>



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
      <th>class</th>
      <th>cap-shape</th>
      <th>cap-surface</th>
      <th>cap-color</th>
      <th>bruises</th>
      <th>odor</th>
      <th>gill-attachment</th>
      <th>gill-spacing</th>
      <th>gill-size</th>
      <th>gill-color</th>
      <th>...</th>
      <th>stalk-surface-below-ring</th>
      <th>stalk-color-above-ring</th>
      <th>stalk-color-below-ring</th>
      <th>veil-type</th>
      <th>veil-color</th>
      <th>ring-number</th>
      <th>ring-type</th>
      <th>spore-print-color</th>
      <th>population</th>
      <th>habitat</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>p</td>
      <td>x</td>
      <td>s</td>
      <td>n</td>
      <td>t</td>
      <td>p</td>
      <td>f</td>
      <td>c</td>
      <td>n</td>
      <td>k</td>
      <td>...</td>
      <td>s</td>
      <td>w</td>
      <td>w</td>
      <td>p</td>
      <td>w</td>
      <td>o</td>
      <td>p</td>
      <td>k</td>
      <td>s</td>
      <td>u</td>
    </tr>
    <tr>
      <th>1</th>
      <td>e</td>
      <td>x</td>
      <td>s</td>
      <td>y</td>
      <td>t</td>
      <td>a</td>
      <td>f</td>
      <td>c</td>
      <td>b</td>
      <td>k</td>
      <td>...</td>
      <td>s</td>
      <td>w</td>
      <td>w</td>
      <td>p</td>
      <td>w</td>
      <td>o</td>
      <td>p</td>
      <td>n</td>
      <td>n</td>
      <td>g</td>
    </tr>
    <tr>
      <th>2</th>
      <td>e</td>
      <td>b</td>
      <td>s</td>
      <td>w</td>
      <td>t</td>
      <td>l</td>
      <td>f</td>
      <td>c</td>
      <td>b</td>
      <td>n</td>
      <td>...</td>
      <td>s</td>
      <td>w</td>
      <td>w</td>
      <td>p</td>
      <td>w</td>
      <td>o</td>
      <td>p</td>
      <td>n</td>
      <td>n</td>
      <td>m</td>
    </tr>
    <tr>
      <th>3</th>
      <td>p</td>
      <td>x</td>
      <td>y</td>
      <td>w</td>
      <td>t</td>
      <td>p</td>
      <td>f</td>
      <td>c</td>
      <td>n</td>
      <td>n</td>
      <td>...</td>
      <td>s</td>
      <td>w</td>
      <td>w</td>
      <td>p</td>
      <td>w</td>
      <td>o</td>
      <td>p</td>
      <td>k</td>
      <td>s</td>
      <td>u</td>
    </tr>
    <tr>
      <th>4</th>
      <td>e</td>
      <td>x</td>
      <td>s</td>
      <td>g</td>
      <td>f</td>
      <td>n</td>
      <td>f</td>
      <td>w</td>
      <td>b</td>
      <td>k</td>
      <td>...</td>
      <td>s</td>
      <td>w</td>
      <td>w</td>
      <td>p</td>
      <td>w</td>
      <td>o</td>
      <td>e</td>
      <td>n</td>
      <td>a</td>
      <td>g</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 23 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">data</span><span class="o">.</span><span class="n">info</span><span class="p">()</span>
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
RangeIndex: 8124 entries, 0 to 8123
Data columns (total 23 columns):
class                       8124 non-null object
cap-shape                   8124 non-null object
cap-surface                 8124 non-null object
cap-color                   8124 non-null object
bruises                     8124 non-null object
odor                        8124 non-null object
gill-attachment             8124 non-null object
gill-spacing                8124 non-null object
gill-size                   8124 non-null object
gill-color                  8124 non-null object
stalk-shape                 8124 non-null object
stalk-root                  8124 non-null object
stalk-surface-above-ring    8124 non-null object
stalk-surface-below-ring    8124 non-null object
stalk-color-above-ring      8124 non-null object
stalk-color-below-ring      8124 non-null object
veil-type                   8124 non-null object
veil-color                  8124 non-null object
ring-number                 8124 non-null object
ring-type                   8124 non-null object
spore-print-color           8124 non-null object
population                  8124 non-null object
habitat                     8124 non-null object
dtypes: object(23)
memory usage: 1.4+ MB
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">datacopy</span> <span class="o">=</span> <span class="n">data</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.preprocessing</span> <span class="k">import</span> <span class="n">LabelEncoder</span><span class="p">,</span> <span class="n">LabelBinarizer</span>

<span class="n">encoders</span> <span class="o">=</span> <span class="p">{}</span>
<span class="n">binarizers</span> <span class="o">=</span> <span class="p">{}</span>
<span class="k">for</span> <span class="n">column</span> <span class="ow">in</span> <span class="nb">list</span><span class="p">(</span><span class="n">data</span><span class="p">):</span>
    <span class="n">encoder</span> <span class="o">=</span> <span class="n">LabelEncoder</span><span class="p">()</span>
    <span class="n">encoder</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">data</span><span class="p">[</span><span class="n">column</span><span class="p">])</span>
    <span class="n">binarizer</span> <span class="o">=</span> <span class="n">LabelBinarizer</span><span class="p">()</span>
    <span class="n">binarizer</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">data</span><span class="p">[</span><span class="n">column</span><span class="p">])</span>
    <span class="n">data</span><span class="p">[</span><span class="n">column</span><span class="p">]</span> <span class="o">=</span> <span class="n">encoder</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">data</span><span class="p">[</span><span class="n">column</span><span class="p">])</span>
    <span class="n">encoders</span><span class="p">[</span><span class="n">column</span><span class="p">]</span> <span class="o">=</span> <span class="n">encoder</span>
    <span class="n">binarizers</span><span class="p">[</span><span class="n">column</span><span class="p">]</span> <span class="o">=</span> <span class="n">binarizer</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">data</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[5]:</div>



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
      <th>class</th>
      <th>cap-shape</th>
      <th>cap-surface</th>
      <th>cap-color</th>
      <th>bruises</th>
      <th>odor</th>
      <th>gill-attachment</th>
      <th>gill-spacing</th>
      <th>gill-size</th>
      <th>gill-color</th>
      <th>...</th>
      <th>stalk-surface-below-ring</th>
      <th>stalk-color-above-ring</th>
      <th>stalk-color-below-ring</th>
      <th>veil-type</th>
      <th>veil-color</th>
      <th>ring-number</th>
      <th>ring-type</th>
      <th>spore-print-color</th>
      <th>population</th>
      <th>habitat</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>5</td>
      <td>2</td>
      <td>4</td>
      <td>1</td>
      <td>6</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>4</td>
      <td>...</td>
      <td>2</td>
      <td>7</td>
      <td>7</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
      <td>4</td>
      <td>2</td>
      <td>3</td>
      <td>5</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0</td>
      <td>5</td>
      <td>2</td>
      <td>9</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>4</td>
      <td>...</td>
      <td>2</td>
      <td>7</td>
      <td>7</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
      <td>4</td>
      <td>3</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>8</td>
      <td>1</td>
      <td>3</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>5</td>
      <td>...</td>
      <td>2</td>
      <td>7</td>
      <td>7</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
      <td>4</td>
      <td>3</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>5</td>
      <td>3</td>
      <td>8</td>
      <td>1</td>
      <td>6</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>5</td>
      <td>...</td>
      <td>2</td>
      <td>7</td>
      <td>7</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
      <td>4</td>
      <td>2</td>
      <td>3</td>
      <td>5</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>5</td>
      <td>2</td>
      <td>3</td>
      <td>0</td>
      <td>5</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>4</td>
      <td>...</td>
      <td>2</td>
      <td>7</td>
      <td>7</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>0</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 23 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="o">%</span><span class="k">matplotlib</span> inline
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="n">data</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">bins</span><span class="o">=</span><span class="mi">50</span><span class="p">,</span> <span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">20</span><span class="p">,</span><span class="mi">15</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


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
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">corr_features</span> <span class="o">=</span> <span class="n">data</span><span class="o">.</span><span class="n">corr</span><span class="p">()</span>
<span class="n">corr_features</span><span class="p">[</span><span class="s2">&quot;class&quot;</span><span class="p">]</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[7]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>class                       1.000000
cap-shape                   0.052951
cap-surface                 0.178446
cap-color                  -0.031384
bruises                    -0.501530
odor                       -0.093552
gill-attachment             0.129200
gill-spacing               -0.348387
gill-size                   0.540024
gill-color                 -0.530566
stalk-shape                -0.102019
stalk-root                 -0.379361
stalk-surface-above-ring   -0.334593
stalk-surface-below-ring   -0.298801
stalk-color-above-ring     -0.154003
stalk-color-below-ring     -0.146730
veil-type                        NaN
veil-color                  0.145142
ring-number                -0.214366
ring-type                  -0.411771
spore-print-color           0.171961
population                  0.298686
habitat                     0.217179
Name: class, dtype: float64</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">columns_removed</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">columns_removed</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="s2">&quot;veil-type&quot;</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">data</span> <span class="o">=</span> <span class="n">datacopy</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn</span> <span class="o">.</span><span class="n">model_selection</span> <span class="kn">import</span> <span class="nn">StratifiedShuffleSplit</span>
<span class="n">split</span> <span class="o">=</span> <span class="n">StratifiedShuffleSplit</span><span class="p">(</span><span class="n">n_splits</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">test_size</span><span class="o">=</span><span class="mf">0.2</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">42</span><span class="p">)</span>
<span class="k">for</span> <span class="n">train_index</span><span class="p">,</span> <span class="n">test_index</span> <span class="ow">in</span> <span class="n">split</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">data</span><span class="p">[</span><span class="s2">&quot;class&quot;</span><span class="p">]):</span>
    <span class="n">train_features</span> <span class="o">=</span> <span class="n">data</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">train_index</span><span class="p">]</span>
    <span class="n">test_features</span> <span class="o">=</span> <span class="n">data</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">test_index</span><span class="p">]</span>

<span class="n">train_labels</span> <span class="o">=</span> <span class="n">train_features</span><span class="p">[</span><span class="s2">&quot;class&quot;</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span><span class="o">.</span><span class="n">values</span>
<span class="n">train_features</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s2">&quot;class&quot;</span><span class="p">,</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="n">test_labels</span> <span class="o">=</span> <span class="n">test_features</span><span class="p">[</span><span class="s2">&quot;class&quot;</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span><span class="o">.</span><span class="n">values</span>
<span class="n">test_features</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s2">&quot;class&quot;</span><span class="p">,</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="nb">set</span> <span class="ow">in</span> <span class="p">(</span><span class="n">train_features</span><span class="p">,</span> <span class="n">test_features</span><span class="p">):</span>
    <span class="k">for</span> <span class="n">column_removed</span> <span class="ow">in</span> <span class="n">columns_removed</span><span class="p">:</span>
        <span class="nb">set</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="n">column_removed</span><span class="p">],</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">train_features</span><span class="o">.</span><span class="n">info</span><span class="p">()</span>
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
Int64Index: 6499 entries, 5249 to 2411
Data columns (total 21 columns):
cap-shape                   6499 non-null object
cap-surface                 6499 non-null object
cap-color                   6499 non-null object
bruises                     6499 non-null object
odor                        6499 non-null object
gill-attachment             6499 non-null object
gill-spacing                6499 non-null object
gill-size                   6499 non-null object
gill-color                  6499 non-null object
stalk-shape                 6499 non-null object
stalk-root                  6499 non-null object
stalk-surface-above-ring    6499 non-null object
stalk-surface-below-ring    6499 non-null object
stalk-color-above-ring      6499 non-null object
stalk-color-below-ring      6499 non-null object
veil-color                  6499 non-null object
ring-number                 6499 non-null object
ring-type                   6499 non-null object
spore-print-color           6499 non-null object
population                  6499 non-null object
habitat                     6499 non-null object
dtypes: object(21)
memory usage: 1.1+ MB
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[13]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>

<span class="n">X</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">X_test</span> <span class="o">=</span> <span class="p">[]</span>
<span class="k">for</span> <span class="n">column</span> <span class="ow">in</span> <span class="nb">list</span><span class="p">(</span><span class="n">train_features</span><span class="p">):</span>
    <span class="k">if</span> <span class="nb">len</span><span class="p">(</span><span class="n">X</span><span class="p">)</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
        <span class="n">X</span> <span class="o">=</span> <span class="n">binarizers</span><span class="p">[</span><span class="n">column</span><span class="p">]</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">train_features</span><span class="p">[</span><span class="n">column</span><span class="p">])</span>
        <span class="n">X_test</span> <span class="o">=</span> <span class="n">binarizers</span><span class="p">[</span><span class="n">column</span><span class="p">]</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">test_features</span><span class="p">[</span><span class="n">column</span><span class="p">])</span>
        <span class="k">continue</span>

    <span class="n">X</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">X</span><span class="p">,</span> <span class="n">binarizers</span><span class="p">[</span><span class="n">column</span><span class="p">]</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">train_features</span><span class="p">[</span><span class="n">column</span><span class="p">])),</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
    <span class="n">X_test</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">X_test</span><span class="p">,</span> <span class="n">binarizers</span><span class="p">[</span><span class="n">column</span><span class="p">]</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">test_features</span><span class="p">[</span><span class="n">column</span><span class="p">])),</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>

<span class="n">Y</span> <span class="o">=</span> <span class="n">binarizers</span><span class="p">[</span><span class="s2">&quot;class&quot;</span><span class="p">]</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">train_labels</span><span class="p">)</span><span class="o">.</span><span class="n">flatten</span><span class="p">()</span>
<span class="n">Y_test</span> <span class="o">=</span> <span class="n">binarizers</span><span class="p">[</span><span class="s2">&quot;class&quot;</span><span class="p">]</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">test_labels</span><span class="p">)</span><span class="o">.</span><span class="n">flatten</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">shape</span><span class="p">(</span><span class="n">Y</span><span class="p">),</span> <span class="n">np</span><span class="o">.</span><span class="n">shape</span><span class="p">(</span><span class="n">Y_test</span><span class="p">),</span> <span class="n">np</span><span class="o">.</span><span class="n">shape</span><span class="p">(</span><span class="n">X</span><span class="p">),</span> <span class="n">np</span><span class="o">.</span><span class="n">shape</span><span class="p">(</span><span class="n">X_test</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>(6499,) (1625,) (6499, 111) (1625, 111)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[15]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.decomposition</span> <span class="k">import</span> <span class="n">PCA</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>

<span class="k">def</span> <span class="nf">get_dims_variances</span><span class="p">(</span><span class="n">min_dim</span><span class="p">,</span> <span class="n">max_dim</span><span class="p">,</span> <span class="n">threshold</span><span class="o">=</span><span class="mf">0.1</span><span class="p">,</span> <span class="n">capToThreshold</span><span class="o">=</span><span class="kc">False</span><span class="p">):</span>
    <span class="n">dims</span> <span class="o">=</span> <span class="p">[]</span>
    <span class="n">variances</span> <span class="o">=</span> <span class="p">[]</span>
    <span class="n">optimum_dim</span> <span class="o">=</span> <span class="n">min_dim</span>
    <span class="k">for</span> <span class="n">dim</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">min_dim</span><span class="p">,</span> <span class="n">max_dim</span><span class="p">):</span>
        <span class="n">pca</span> <span class="o">=</span> <span class="n">PCA</span><span class="p">(</span><span class="n">n_components</span><span class="o">=</span><span class="n">dim</span><span class="p">)</span>
        <span class="n">pca</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X</span><span class="p">)</span>
        <span class="n">variance</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span><span class="n">pca</span><span class="o">.</span><span class="n">explained_variance_ratio_</span><span class="p">)</span>
        <span class="n">variance</span> <span class="o">=</span> <span class="n">variance</span><span class="o">.</span><span class="n">min</span><span class="p">()</span>
        <span class="k">if</span> <span class="n">threshold</span> <span class="o">&lt;</span> <span class="n">variance</span><span class="p">:</span>
            <span class="n">optimum_dim</span> <span class="o">=</span> <span class="n">dim</span>
            <span class="n">dims</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">dim</span><span class="p">)</span>
            <span class="n">variances</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">variance</span><span class="p">)</span>
        <span class="k">else</span><span class="p">:</span>
            <span class="k">if</span> <span class="n">capToThreshold</span><span class="p">:</span>
                <span class="k">break</span>

    <span class="k">return</span> <span class="n">dims</span><span class="p">,</span> <span class="n">variances</span><span class="p">,</span> <span class="n">optimum_dim</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[16]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">dims</span><span class="p">,</span> <span class="n">variances</span><span class="p">,</span> <span class="n">optimum_dim</span> <span class="o">=</span> <span class="n">get_dims_variances</span><span class="p">(</span><span class="mi">2</span><span class="p">,</span>  <span class="n">np</span><span class="o">.</span><span class="n">shape</span><span class="p">(</span><span class="n">X</span><span class="p">)[</span><span class="mi">1</span><span class="p">],</span> <span class="mf">0.01</span><span class="p">,</span> <span class="n">capToThreshold</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">optimum_dim</span><span class="p">)</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">dims</span><span class="p">,</span> <span class="n">variances</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>23
</pre>
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
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[17]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="n">variances</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>[0.1383103486069508, 0.09191351304950753, 0.055092220882746575, 0.04059961237076332, 0.0382216251657648, 0.03322290740898192, 0.028425778227087733, 0.023507742490091438, 0.022422208875307967, 0.022018563506496596, 0.019523801628874463, 0.01930641110645749, 0.017141087632104625, 0.016341137031180127, 0.015957143794627166, 0.015517540411970001, 0.015184129960424411, 0.013283279622003125, 0.012218032513305927, 0.011549195653202483, 0.01113867128886284, 0.010249336164108499]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[18]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">pca</span> <span class="o">=</span> <span class="n">PCA</span><span class="p">(</span><span class="n">n_components</span><span class="o">=</span><span class="n">optimum_dim</span><span class="p">)</span>
<span class="n">pca</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">pca</span><span class="o">.</span><span class="n">explained_variance_ratio_</span><span class="p">)</span>
<span class="n">X</span> <span class="o">=</span> <span class="n">pca</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">X</span><span class="p">)</span>
<span class="n">X_test</span> <span class="o">=</span> <span class="n">pca</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>[0.16188491 0.13831035 0.09191351 0.05509222 0.04059962 0.03822164
 0.03322293 0.02842691 0.02350955 0.02242325 0.02201855 0.01952805
 0.01933961 0.01717538 0.0163586  0.0160183  0.01554436 0.01520302
 0.0132878  0.0122408  0.01154081 0.01117127 0.01026622]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[19]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.preprocessing</span> <span class="k">import</span> <span class="n">Imputer</span>
<span class="n">imputer</span> <span class="o">=</span> <span class="n">Imputer</span><span class="p">(</span><span class="n">strategy</span><span class="o">=</span><span class="s2">&quot;median&quot;</span><span class="p">)</span>
<span class="n">imputer</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X</span><span class="p">)</span>

<span class="n">X</span> <span class="o">=</span> <span class="n">imputer</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">X</span><span class="p">)</span>
<span class="n">X_test</span> <span class="o">=</span> <span class="n">imputer</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[20]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.preprocessing</span> <span class="k">import</span> <span class="n">StandardScaler</span>

<span class="n">scalar</span> <span class="o">=</span> <span class="n">StandardScaler</span><span class="p">()</span>
<span class="n">scalar</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X</span><span class="p">)</span>

<span class="n">X</span> <span class="o">=</span> <span class="n">scalar</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">X</span><span class="p">)</span>
<span class="n">X_test</span> <span class="o">=</span> <span class="n">scalar</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[21]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="n">Y</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">binarizers</span><span class="p">[</span><span class="s2">&quot;class&quot;</span><span class="p">]</span><span class="o">.</span><span class="n">classes_</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>[1 0 0 ... 0 0 0]
[&#39;e&#39; &#39;p&#39;]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[22]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="k">import</span> <span class="n">roc_curve</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="k">def</span> <span class="nf">plot_roc_curve</span><span class="p">(</span><span class="n">clf_sets</span><span class="p">):</span>
    <span class="k">for</span> <span class="n">clf_set</span> <span class="ow">in</span> <span class="n">clf_sets</span><span class="p">:</span>
        <span class="n">y</span> <span class="o">=</span> <span class="n">clf_set</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
        <span class="n">y_pred</span> <span class="o">=</span> <span class="n">clf_set</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span>
        <span class="n">label</span> <span class="o">=</span> <span class="n">clf_set</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span>
        <span class="n">fpr</span><span class="p">,</span> <span class="n">tpr</span><span class="p">,</span> <span class="n">thresholds</span> <span class="o">=</span> <span class="n">roc_curve</span><span class="p">(</span><span class="n">y</span><span class="p">,</span> <span class="n">y_pred</span><span class="p">)</span>
        <span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">fpr</span><span class="p">,</span> <span class="n">tpr</span><span class="p">,</span> <span class="n">linewidth</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="n">label</span><span class="p">)</span>

    <span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">],[</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">],</span><span class="s1">&#39;k--&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;False Positive Rate&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;True Positive Rate&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">loc</span><span class="o">=</span><span class="s2">&quot;bottom right&quot;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[23]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># SGD Classifier</span>
<span class="kn">from</span> <span class="nn">sklearn.linear_model</span> <span class="k">import</span> <span class="n">SGDClassifier</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="k">import</span> <span class="n">cross_val_score</span><span class="p">,</span> <span class="n">cross_val_predict</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="k">import</span> <span class="n">confusion_matrix</span><span class="p">,</span> <span class="n">f1_score</span><span class="p">,</span> <span class="n">precision_score</span><span class="p">,</span> <span class="n">recall_score</span>
<span class="kn">from</span> <span class="nn">sklearn.base</span> <span class="k">import</span> <span class="n">clone</span>

<span class="n">clf_sets</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">sgd_clf</span> <span class="o">=</span> <span class="n">SGDClassifier</span><span class="p">(</span><span class="n">random_state</span><span class="o">=</span><span class="mi">42</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Cross Val Scores on training set</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">cross_val_score</span><span class="p">(</span><span class="n">clone</span><span class="p">(</span><span class="n">sgd_clf</span><span class="p">),</span> <span class="n">X</span><span class="p">,</span> <span class="n">Y</span><span class="p">,</span> <span class="n">cv</span><span class="o">=</span><span class="mi">3</span><span class="p">,</span> <span class="n">scoring</span><span class="o">=</span><span class="s2">&quot;accuracy&quot;</span><span class="p">))</span>
<span class="n">Y_pred</span> <span class="o">=</span> <span class="n">cross_val_predict</span><span class="p">(</span><span class="n">clone</span><span class="p">(</span><span class="n">sgd_clf</span><span class="p">),</span> <span class="n">X</span><span class="p">,</span> <span class="n">Y</span><span class="p">,</span> <span class="n">cv</span><span class="o">=</span><span class="mi">3</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;confusion_matrix</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">confusion_matrix</span><span class="p">(</span><span class="n">Y</span><span class="p">,</span> <span class="n">Y_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;f1_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">f1_score</span><span class="p">(</span><span class="n">Y</span><span class="p">,</span> <span class="n">Y_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;precision_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">precision_score</span><span class="p">(</span><span class="n">Y</span><span class="p">,</span> <span class="n">Y_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;recall_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">recall_score</span><span class="p">(</span><span class="n">Y</span><span class="p">,</span> <span class="n">Y_pred</span><span class="p">))</span>
<span class="n">clf_sets</span><span class="o">.</span><span class="n">append</span><span class="p">((</span><span class="n">Y</span><span class="p">,</span> <span class="n">Y_pred</span><span class="p">,</span> <span class="s2">&quot;SGDClassifier-train&quot;</span><span class="p">))</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\n\n</span><span class="s2">Cross Val Scores on testing set</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">cross_val_score</span><span class="p">(</span><span class="n">clone</span><span class="p">(</span><span class="n">sgd_clf</span><span class="p">),</span> <span class="n">X_test</span><span class="p">,</span> <span class="n">Y_test</span><span class="p">,</span> <span class="n">cv</span><span class="o">=</span><span class="mi">3</span><span class="p">,</span> <span class="n">scoring</span><span class="o">=</span><span class="s2">&quot;accuracy&quot;</span><span class="p">))</span>
<span class="n">Y_test_pred</span> <span class="o">=</span> <span class="n">cross_val_predict</span><span class="p">(</span><span class="n">clone</span><span class="p">(</span><span class="n">sgd_clf</span><span class="p">),</span> <span class="n">X_test</span><span class="p">,</span> <span class="n">Y_test</span><span class="p">,</span> <span class="n">cv</span><span class="o">=</span><span class="mi">3</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;confusion_matrix</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">confusion_matrix</span><span class="p">(</span><span class="n">Y_test</span><span class="p">,</span> <span class="n">Y_test_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;f1_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">f1_score</span><span class="p">(</span><span class="n">Y_test</span><span class="p">,</span> <span class="n">Y_test_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;precision_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">precision_score</span><span class="p">(</span><span class="n">Y_test</span><span class="p">,</span> <span class="n">Y_test_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;recall_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">recall_score</span><span class="p">(</span><span class="n">Y_test</span><span class="p">,</span> <span class="n">Y_test_pred</span><span class="p">))</span>
<span class="n">clf_sets</span><span class="o">.</span><span class="n">append</span><span class="p">((</span><span class="n">Y_test</span><span class="p">,</span> <span class="n">Y_test_pred</span><span class="p">,</span> <span class="s2">&quot;SGDClassifier-test&quot;</span><span class="p">))</span>

<span class="n">sgd_clf</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X</span><span class="p">,</span> <span class="n">Y</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\n\n</span><span class="s2">Accuracy on testing data set</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="nb">sum</span><span class="p">(</span><span class="n">Y_test</span> <span class="o">==</span> <span class="n">sgd_clf</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">X_test</span><span class="p">))</span> <span class="o">/</span> <span class="nb">len</span><span class="p">(</span><span class="n">X_test</span><span class="p">))</span>

<span class="n">plot_roc_curve</span><span class="p">(</span><span class="n">clf_sets</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Cross Val Scores on training set
 [0.97784956 0.97968606 0.98014774]
confusion_matrix
 [[3293   73]
 [  62 3071]]
f1_score
 0.9784929106260952
precision_score
 0.9767811704834606
recall_score
 0.980210660708586


Cross Val Scores on testing set
 [0.96863469 0.95940959 0.96672828]
confusion_matrix
 [[794  48]
 [  9 774]]
f1_score
 0.9644859813084112
precision_score
 0.9416058394160584
recall_score
 0.9885057471264368


Accuracy on testing data set
 0.9661538461538461
</pre>
</div>
</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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RACSkpLo1asXhw8f5sknn+SPP/7g9ttvZ+bMmTRu3BiAjz76iCNHjhR6/HPmnLib/7XXXmPevHlZY4a33RbwEa+TuN3uU6YcnjFjBrVq1eKSSy45ZXuPx5PnLfBDhgxx/LnBErktigibtChzYqH58+czadIkSxImKv3+++9UrFiRUqVKAVCxYkXOPvtspkyZwquvvkpcXBwA5cuXZ+zYsbke44ILLmDy5MlMmDABVWXixIn07ds3K0kAdOvWjQsvvPCk/WbPnk2jRo2oV68erVq14o8//gBg4cKFWa2YevXqceTIEX7//XeaNWtGfHw8tWrV4vvvvwegWrVq7Nu3jyFDhrB9+3batWvHv/71r5NaLsnJyXTt2pUGDRrQoEEDlixZAsDYsWPp06cPTZo0oU+fPifF9tFHH7FixQp69+5NfHw8x44do1q1aowaNYr69evz4YcfMmXKFBo0aEDdunXp2rUrR48ezTruiy++CMBNN93EqFGjaNiwIVdffXVW3MEWcS0Kb/a7nsJ8MHv27Nls2rSJv/zlL7Ro0YKNGzee8l+GMcFS7dEvC/2Y/3u2Q8D1rVu35qmnnuLqq6+mVatWdO/enXPOOYcqVapQvnx5x59z+eWX4/F4SEpKYv369fTt2zfffW688UaWLl2KiDB16lSef/55xo0bx4svvsjEiRNp0qQJKSkpxMXFMXnyZNq0acPjjz+Ox+PJuihnmjRpEl9//TXz58+nYsWKzJgxI2vd/fffz4MPPsiNN97Izp07adOmDZs2bQJg48aNLF68mNKlS590vG7dujFhwgRefPFFEhISspafd955rFq1CoD9+/czaNAgAEaPHs20adO47777Tvk53W43y5cvZ86cOTz55JPMmzfP2Uk9AxF31dLMEh5hPJidnJzM/fffz3/+8x/i4+N54IEHKFmypCUJU6Tyu6gHQ7ly5Vi5ciXff/898+fPp3v37vz1r389aZs333yTV155hf379/PDDz8U2pzuu3fvpnv37vz+++8cP3486zmCJk2a8NBDD9G7d2+6dOlC5cqVadCgAQMGDCAjI4POnTsTHx/v+HPmzZvHxo0bs94fPnyYlJQUwNc9lTNJBNK9e/es1+vXr2f06NEcPHiQlJQU2rRpk+s+Xbp0AeC6667jf//7n+PPOhMR2PWkxMV4Ie0QlDkv1OGcRFV57733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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[24]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># KNeighbors Classifier</span>

<span class="kn">from</span> <span class="nn">sklearn.neighbors</span> <span class="k">import</span> <span class="n">KNeighborsClassifier</span>

<span class="n">knn_clf</span> <span class="o">=</span> <span class="n">KNeighborsClassifier</span><span class="p">()</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Cross Val Scores on training set</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">cross_val_score</span><span class="p">(</span><span class="n">clone</span><span class="p">(</span><span class="n">knn_clf</span><span class="p">),</span> <span class="n">X</span><span class="p">,</span> <span class="n">Y</span><span class="p">,</span> <span class="n">cv</span><span class="o">=</span><span class="mi">3</span><span class="p">,</span> <span class="n">scoring</span><span class="o">=</span><span class="s2">&quot;accuracy&quot;</span><span class="p">))</span>
<span class="n">Y_pred</span> <span class="o">=</span> <span class="n">cross_val_predict</span><span class="p">(</span><span class="n">clone</span><span class="p">(</span><span class="n">knn_clf</span><span class="p">),</span> <span class="n">X</span><span class="p">,</span> <span class="n">Y</span><span class="p">,</span> <span class="n">cv</span><span class="o">=</span><span class="mi">3</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;confusion_matrix</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">confusion_matrix</span><span class="p">(</span><span class="n">Y</span><span class="p">,</span> <span class="n">Y_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;f1_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">f1_score</span><span class="p">(</span><span class="n">Y</span><span class="p">,</span> <span class="n">Y_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;precision_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">precision_score</span><span class="p">(</span><span class="n">Y</span><span class="p">,</span> <span class="n">Y_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;recall_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">recall_score</span><span class="p">(</span><span class="n">Y</span><span class="p">,</span> <span class="n">Y_pred</span><span class="p">))</span>
<span class="n">clf_sets</span><span class="o">.</span><span class="n">append</span><span class="p">((</span><span class="n">Y</span><span class="p">,</span> <span class="n">Y_pred</span><span class="p">,</span> <span class="s2">&quot;KNN-train&quot;</span><span class="p">))</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\n\n</span><span class="s2">Cross Val Scores on testing set</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">cross_val_score</span><span class="p">(</span><span class="n">clone</span><span class="p">(</span><span class="n">knn_clf</span><span class="p">),</span> <span class="n">X_test</span><span class="p">,</span> <span class="n">Y_test</span><span class="p">,</span> <span class="n">cv</span><span class="o">=</span><span class="mi">3</span><span class="p">,</span> <span class="n">scoring</span><span class="o">=</span><span class="s2">&quot;accuracy&quot;</span><span class="p">))</span>
<span class="n">Y_test_pred</span> <span class="o">=</span> <span class="n">cross_val_predict</span><span class="p">(</span><span class="n">clone</span><span class="p">(</span><span class="n">knn_clf</span><span class="p">),</span> <span class="n">X_test</span><span class="p">,</span> <span class="n">Y_test</span><span class="p">,</span> <span class="n">cv</span><span class="o">=</span><span class="mi">3</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;confusion_matrix</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">confusion_matrix</span><span class="p">(</span><span class="n">Y_test</span><span class="p">,</span> <span class="n">Y_test_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;f1_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">f1_score</span><span class="p">(</span><span class="n">Y_test</span><span class="p">,</span> <span class="n">Y_test_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;precision_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">precision_score</span><span class="p">(</span><span class="n">Y_test</span><span class="p">,</span> <span class="n">Y_test_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;recall_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">recall_score</span><span class="p">(</span><span class="n">Y_test</span><span class="p">,</span> <span class="n">Y_test_pred</span><span class="p">))</span>
<span class="n">clf_sets</span><span class="o">.</span><span class="n">append</span><span class="p">((</span><span class="n">Y_test</span><span class="p">,</span> <span class="n">Y_test_pred</span><span class="p">,</span> <span class="s2">&quot;KNN-test&quot;</span><span class="p">))</span>

<span class="n">knn_clf</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X</span><span class="p">,</span> <span class="n">Y</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\n\n</span><span class="s2">Accuracy on testing data set</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="nb">sum</span><span class="p">(</span><span class="n">Y_test</span> <span class="o">==</span> <span class="n">knn_clf</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">X_test</span><span class="p">))</span> <span class="o">/</span> <span class="nb">len</span><span class="p">(</span><span class="n">X_test</span><span class="p">))</span>

<span class="n">plot_roc_curve</span><span class="p">(</span><span class="n">clf_sets</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Cross Val Scores on training set
 [0.99907707 1.         0.99815328]
confusion_matrix
 [[3362    4]
 [   2 3131]]
f1_score
 0.9990427568602426
precision_score
 0.9987240829346092
recall_score
 0.999361634216406


Cross Val Scores on testing set
 [1.         0.99630996 0.99445471]
confusion_matrix
 [[838   4]
 [  1 782]]
f1_score
 0.9968132568514977
precision_score
 0.9949109414758269
recall_score
 0.9987228607918263


Accuracy on testing data set
 1.0
</pre>
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
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[25]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Random Forest Classifier</span>

<span class="kn">from</span> <span class="nn">sklearn.ensemble</span> <span class="k">import</span> <span class="n">RandomForestClassifier</span>

<span class="n">forest_clf</span> <span class="o">=</span> <span class="n">RandomForestClassifier</span><span class="p">(</span><span class="n">random_state</span><span class="o">=</span><span class="mi">42</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Cross Val Scores on training set</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">cross_val_score</span><span class="p">(</span><span class="n">clone</span><span class="p">(</span><span class="n">forest_clf</span><span class="p">),</span> <span class="n">X</span><span class="p">,</span> <span class="n">Y</span><span class="p">,</span> <span class="n">cv</span><span class="o">=</span><span class="mi">3</span><span class="p">,</span> <span class="n">scoring</span><span class="o">=</span><span class="s2">&quot;accuracy&quot;</span><span class="p">))</span>
<span class="n">Y_pred</span> <span class="o">=</span> <span class="n">cross_val_predict</span><span class="p">(</span><span class="n">clone</span><span class="p">(</span><span class="n">forest_clf</span><span class="p">),</span> <span class="n">X</span><span class="p">,</span> <span class="n">Y</span><span class="p">,</span> <span class="n">cv</span><span class="o">=</span><span class="mi">3</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;confusion_matrix</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">confusion_matrix</span><span class="p">(</span><span class="n">Y</span><span class="p">,</span> <span class="n">Y_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;f1_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">f1_score</span><span class="p">(</span><span class="n">Y</span><span class="p">,</span> <span class="n">Y_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;precision_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">precision_score</span><span class="p">(</span><span class="n">Y</span><span class="p">,</span> <span class="n">Y_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;recall_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">recall_score</span><span class="p">(</span><span class="n">Y</span><span class="p">,</span> <span class="n">Y_pred</span><span class="p">))</span>
<span class="n">clf_sets</span><span class="o">.</span><span class="n">append</span><span class="p">((</span><span class="n">Y</span><span class="p">,</span> <span class="n">Y_pred</span><span class="p">,</span> <span class="s2">&quot;RandomForest-train&quot;</span><span class="p">))</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\n\n</span><span class="s2">Cross Val Scores on testing set</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">cross_val_score</span><span class="p">(</span><span class="n">clone</span><span class="p">(</span><span class="n">forest_clf</span><span class="p">),</span> <span class="n">X_test</span><span class="p">,</span> <span class="n">Y_test</span><span class="p">,</span> <span class="n">cv</span><span class="o">=</span><span class="mi">3</span><span class="p">,</span> <span class="n">scoring</span><span class="o">=</span><span class="s2">&quot;accuracy&quot;</span><span class="p">))</span>
<span class="n">Y_test_pred</span> <span class="o">=</span> <span class="n">cross_val_predict</span><span class="p">(</span><span class="n">clone</span><span class="p">(</span><span class="n">forest_clf</span><span class="p">),</span> <span class="n">X_test</span><span class="p">,</span> <span class="n">Y_test</span><span class="p">,</span> <span class="n">cv</span><span class="o">=</span><span class="mi">3</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;confusion_matrix</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">confusion_matrix</span><span class="p">(</span><span class="n">Y_test</span><span class="p">,</span> <span class="n">Y_test_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;f1_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">f1_score</span><span class="p">(</span><span class="n">Y_test</span><span class="p">,</span> <span class="n">Y_test_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;precision_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">precision_score</span><span class="p">(</span><span class="n">Y_test</span><span class="p">,</span> <span class="n">Y_test_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;recall_score</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">recall_score</span><span class="p">(</span><span class="n">Y_test</span><span class="p">,</span> <span class="n">Y_test_pred</span><span class="p">))</span>
<span class="n">clf_sets</span><span class="o">.</span><span class="n">append</span><span class="p">((</span><span class="n">Y_test</span><span class="p">,</span> <span class="n">Y_test_pred</span><span class="p">,</span> <span class="s2">&quot;RandomForest-test&quot;</span><span class="p">))</span>

<span class="n">forest_clf</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X</span><span class="p">,</span> <span class="n">Y</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\n\n</span><span class="s2">Accuracy on testing data set</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="nb">sum</span><span class="p">(</span><span class="n">Y_test</span> <span class="o">==</span> <span class="n">forest_clf</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">X_test</span><span class="p">))</span> <span class="o">/</span> <span class="nb">len</span><span class="p">(</span><span class="n">X_test</span><span class="p">))</span>

<span class="n">plot_roc_curve</span><span class="p">(</span><span class="n">clf_sets</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Cross Val Scores on training set
 [0.99815413 0.99815328 0.99861496]
confusion_matrix
 [[3361    5]
 [   6 3127]]
f1_score
 0.9982442138866721
precision_score
 0.9984035759897829
recall_score
 0.998084902649218


Cross Val Scores on testing set
 [0.99261993 0.99077491 0.98890943]
confusion_matrix
 [[840   2]
 [ 13 770]]
f1_score
 0.990353697749196
precision_score
 0.9974093264248705
recall_score
 0.9833971902937421


Accuracy on testing data set
 0.9987692307692307
</pre>
</div>
</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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3HvvvYwaNYpdu3ZRqlQpwsPD+e677+jUqRPx8fE0aNCAKVOmkJSURLNmzVixYgVly5ZlyZIljB49mnnz5jFx4kROnjxJ4cKF7bLmAwYMwN/fP0O13LSS6adOneLo0aMsXLiQhg0bAvDuu+9SunRpzGYzLVu2ZN++fdSuXTtVOfHx8TRs2JB3332X119/ndmzZzNmzBiX/6Y5xStrrfzemR0bG8vLL7/M119/TUhICMOHD6dQoULiJAS34WqlnpskvyGfP3+emjVr0qpVK8AaSnnzzTfZuHEjBoOB8+fP2998k/sLAOrVq8epU6e4evUqV69epWnTpoB1Kd+ffrKuOLBp0yaGDh0KQI0aNahcubLdUbRo0YLixYtTvHhxSpQoQYcOHQAICgpi3759djsnTZpEly5d7PsrVqygefPmlC1rrT969OjBxo0b6dSpE0ajkc6dOwNw+PBhoqOj7fdlNpu5//77Aez6U506daJTp045en6VK1e2OwmApUuXMmvWLEwmExcuXODgwYPpHEWhQoVo3769/fn9+uuvObp2dvHO0JPRAgnXoOi9njYlFVprvvrqK2rWrMmyZct455132L59u4j4CQWS5D6K06dPo7W2h4wWLVpEbGwsu3btIioqivLly5OQkABYl0FNxmg0Zqgq6yqOZRkMBvu+wWDIcbl+fn52JQStNQEBAfb+jf3797N69WoAfvzxRwYPHszu3bsJCwtLd72sJNMBihUrZt8+efIkkydPZu3atezbt4927drZn5kjvr6+9tGRd/r8soNXOoqS3LAKARryl7TFmTNn6NOnD4888gh79uzhrbfeEichFHiKFi3KtGnTmDJlCiaTiWvXrlGuXDl8fX1Zt24dp0+fdnp+yZIlKVmyJJs2bQKsjiaZJk2a2PePHDnCmTNnqF69+h3ZW79+fTZs2MClS5cwm818/fXXNGvWLF2+6tWrExsby9atWwFrP+OBAwewWCycPXuWFi1a8P7773Pt2jXi4uJSyZpnJZmeluvXr1OsWDFKlCjBxYsX7S2q/IJ3OgrL1XwzK9tisfDLL78A1qbk77//zubNmwkICPCwZYKQd9SpU4fatWvz9ddf06NHD3bu3ElQUBCff/55umVSM2L+/PkMHjyYkJAQHBWtBw0ahMViISgoiK5du7JgwYJULYmccP/99zNx4kRatGhBcHAw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
"
>
</div>

</div>

</div>
</div>

</div>
    </div>
  </div>
</body>




</html>
```
