# Detect-Adblock
Check If Ad Block Working JavaScript Code

```javascript
var ___adBlockEnabled = false;
var ___testAd = document.createElement('div');
___testAd.innerHTML = '&nbsp;';
___testAd.className = 'adsbox';
document.body.appendChild(___testAd);
function ___checkadblock(){
	var __checkadblock = window.setTimeout(function(){
		if(___testAd.offsetHeight === 0){
			___adBlockEnabled = true;
		}
		___testAd.remove();
		console.log('AdBlock Enable :', ___adBlockEnabled);
		clearTimeout(__checkadblock);
	},10);
	___detectadblock();
}
function ___detectadblock(){
	var __detectadblock = window.setTimeout(function(){
		if(___adBlockEnabled){
		clearTimeout(__detectadblock);
		// do something
		}
	},10);
}
___checkadblock();
```
