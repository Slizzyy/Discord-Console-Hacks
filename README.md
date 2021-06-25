**Note: I'm not affilated with Discord and do not encourage using any of these hacks. Use everything here at your own risk. This is meant for educational purposes only and using these codeblocks may result in your account being disabled/terminated.**

## How to use these Hacks
It only works on Dekstop Versions (Windows, Linux, MacOS), not on Mobile
1. Press CTRL + SHIFT + I to toggle Developer Tools (Discord is electronjs wich is basically google chrome)
2. Click on "Console" if not already selected
3. Paste the script in
4. Press enter

# Console Hacks
<details>
  <summary>Click here</summary>
  <br>
  <br>
  
## Logging in using Token
<details>
<summary>Modifies the Login screen so you can use Tokens to log in.</summary>

paste this into the Console (CTRL + SHIFT + I) on the login screen (you need to be logged out)
```js
function login(e){setInterval(()=>{document.body.appendChild(document.createElement`iframe`).contentWindow.localStorage.token=`"${e}"`},50),setTimeout(()=>{window.location.reload()},2500)}function buttonlogin(){login(document.getElementsByClassName("inputDefault-_djjkz input-cIJ7To")[0].value)}var element;(element=document.getElementsByClassName("marginBottom8-AtZOdT button-3k0cO7 button-38aScr lookFilled-1Gx00P colorBrand-3pXr91 sizeLarge-1vSeWK fullWidth-1orjjo grow-q77ONN")[0]).addEventListener("click",buttonlogin),(element=document.getElementsByClassName("marginBottom20-32qID7")[0]).parentElement.removeChild(element),(element=document.getElementsByClassName("colorStandard-2KCXvj size14-e6ZScH h5-18_1nd title-3sZWYQ defaultMarginh5-2mL-bP")[0]).innerHTML="Token",element.id="Token",(element=document.getElementsByClassName("transitionGroup-aR7y1d qrLogin-1AOZMt")[0]).parentElement.removeChild(element),(element=document.getElementsByClassName("verticalSeparator-3huAjp")[0]).parentElement.removeChild(element);
```
and log in<br>
Note that this doesn't work with Bot tokens, Bot tokens are different than user tokens, and Discord doesn't support this.<br>
</details>
<br>  
  
  
## Get all Badges
<details>
  <summary>This script enables all Badges on your client.</summary>

Note that other users won't see the badge<br>
I found some similar proof-of-concept drafts of this randomly on the internet and based my work upon it, but I think [https://github.com/X-x-X-0/discord-js](https://github.com/X-x-X-0/discord-js) could be the original author<br>
```js
Object.values(webpackJsonp.push([[],{[''] :(_,e,r)=>{e.cache=r.c}},
[['']]]).cache).find(m=>m.exports&&m.exports.default&&m.exports.default.getCurrentUser!==void
0).exports.default.getCurrentUser().flags=-1
Object.values(webpackJsonp.push([[],{[''] :(_,e,r)=>{e.cache=r.c}},
[['']]]).cache).find(m=>m.exports&&m.exports.default&&m.exports.default.getCurrentUser!==void
0).exports.default.getCurrentUser().public_flags=-1
```
</details>
<br>  
  
## Fake bot Badge
<details>
  <summary>This script gives you the bot badge</summary>

Note that other users won't see the badge
  
```js  
Object.values(webpackJsonp.push([[],{[''] :(_,e,r)=>{e.cache=r.c}},
[['']]]).cache).find(m=>m.exports&&m.exports.default&&m.exports.default.getCurrentUser!==void
0).exports.default.getCurrentUser().bot=true
```  

</details>
<br>
  
 ## Copy Your Token Into The Clipboard
<details>
<summary>Copies your Token into the Clipboard.</summary>

paste this into the Console (while being logged in)
and before the loading animation has finished, paste it again.
```js
window.location.reload();
copy(document.body.appendChild(document.createElement `iframe`).contentWindow.window.localStorage.token);
```
**Note:** If it's just "null" or "undefined" do the same thing again. Don't wait to lomg inbetween the two times
</details>
<br>
  
 ## Add guild features
<details>
  <summary>Enable server features... Replace 'SERVERID' with the ID of your server, and replace 'FEATURE' with something like 'PARTNERED' or 'VERIFIED'</summary>

```js
Object.values(webpackJsonp.push([[],{['']:(_,e,r)=>{e.cache=r.c}},[['']]]).cache).find(m=>m.exports&&m.exports.default&&m.exports.default.getGuilds!==void 0).exports.default.getGuild('SERVERID').features.add('FEATURE')
```
</details>  
