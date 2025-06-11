# help

A Whole list of code

### SAVE INPUT, TEXTAREA, [SAVE], SELECT

```HTML
<script>
(function _A_SVALL(){
const _G=()=>Array.from(document.querySelectorAll('input,textarea,select,[save]'));
const _ST=(k,v)=>{typeof chrome!='undefined'&&chrome.storage&&chrome.storage.local?chrome.storage.local.set({[k]:v}):localStorage.setItem(k,v)};
const _GT=(k,c)=>{if(typeof chrome!='undefined'&&chrome.storage&&chrome.storage.local){chrome.storage.local.get(k,r=>c(r[k]??null))}else{c(localStorage.getItem(k))}};
const _SV=()=>{_G().forEach((e,i)=>_ST(`_INID${i}`,'value'in e?e.value:(e.textContent||'')))};
const _RS=()=>{_G().forEach((e,i)=>_GT(`_INID${i}`,v=>{if(v!=null){'value'in e?e.value=v:e.textContent=v}}))};
const _LS=()=>{_G().forEach(e=>'value'in e?(e.oninput=_SV,e.onchange=_SV):e.hasAttribute('save')&&new MutationObserver(_SV).observe(e,{childList:1,subtree:1,characterData:1}))};
(_RS(),_LS());document.addEventListener('DOMContentLoaded',()=>{_RS();_LS()});
})();
</script>
```


> CSS default is use

```html

<style>
:root,*{--p:#3855d7;--b:#19191c;--f:#fafafa;--d:#202127;--font:sans-serif;--pad:1rem;--gap:10;--mar:0.3rem;--radius:8px;--maxw:100%;--midw:450px;--fz:1rem;--fz-lg:1.2rem;}
body{margin:0 auto auto;background:var(--b);color:var(--f);font-family:var(--font);display:flex;flex-direction:column;padding:5px;box-sizing:border-box;width:100vw;max-width:var(--midw);text-align:center;justify-content: center;place-content: center; align-content: center; min-height: 100svh;}
input,button,a,video{background:var(--d);color:var(--f);border:none;padding:var(--pad);border-radius:var(--radius);width:var(--maxw);max-width:var(--midw);font-size:var(--fz);box-sizing:border-box;}
video,embed[video],embed[vid],iframe[video],iframe[vid] {aspect-ratio:16/9;}
input,button,a {min-height: 0.12in;min-width: 0.3in;}
span {display: flex;flex-wrap: wrap;flex-direction: row;align-items: center;justify-content: center;gap: var(--gap);}
span > * {display: flex;flex: 1;margin: 0;}
body > *:not(:last-child) {margin-bottom: var(--mar);}
span > *:not(:last-child) {margin-right: var(--mar);}
[p=''],[p='hover']:hover,[p='active']:active {background:var(--p);color:var(--f);cursor:pointer;
}
input[type="date"]::-webkit-calendar-picker-indicator {opacity: 0;position: absolute;right: 0;width: 100%;height: 100%;cursor: pointer;}
input[type="date"] {position: relative;background: var(--d) url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='%23fafafa' viewBox='0 0 24 24'%3E%3Cpath d='M19 4h-1V2h-2v2H8V2H6v2H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 16H5V9h14v11z'/%3E%3C/svg%3E") no-repeat right 1rem center;background-size: 1rem;padding-right: 2.5rem;color: var(--f);border: none;border-radius: var(--radius);font-size: var(--fz);width: var(--maxw);max-width: var(--midw);box-sizing: border-box;appearance: none;-webkit-appearance: none;-moz-appearance: none;cursor: pointer;}
select, summary {background: var(--d);color: var(--f);border: none;padding: var(--pad);border-radius: var(--radius);width: var(--maxw);max-width: var(--midw);font-size: var(--fz);box-sizing: border-box;appearance: none;-webkit-appearance: none;-moz-appearance: none;}
select, summary {background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 10 6' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M0 0l5 6 5-6z' fill='%23fafafa'/%3E%3C/svg%3E");background-repeat: no-repeat;background-position: right 1rem center;background-size: 1em;padding-right: 2.5rem;cursor: pointer;}
details {padding: 0;max-width: var(--midw);border-radius: var(--radius);overflow: hidden;transition: all 0.3s ease-in-out;}
summary {list-style: none;user-select: none;font-weight: bold;}
summary::-webkit-details-marker {  display: none;}
</style>
```
