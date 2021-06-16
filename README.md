# DiscordExperiments
Enable Discord Experiments

<h2><a href="https://github.com/ABD0U-DZB/Discord_Experiments" rel="nofollow">Main Repositori</a></h2>

<h2><a href="https://gist.github.com/MPThLee/3ccb554b9d882abc6313330e38e5dfaa" rel="nofollow">Original Repositori</a></h2>


<td class="d-block comment-body markdown-body  js-comment-body user-select-contain">
          <h2>This script works on any environment except mobile app. also works on Web version with Chrome and Firefox.</h2>
<h1>How to enable experiments menu</h1>
<ol>
<li>Copy whole script.</li>
<li>Press <code>Ctrl + Shift + I</code>(Mac: <code>⌥+⌘+I</code>) Normally, It opens Devloper Console. also on Web Browser. <a href="https://support.discordapp.com/hc/en-us/articles/115001239472-Troubleshooting-Console-Log-Errors" rel="nofollow">Described on Discord Support</a></li>
<li>You will see a warning. Paste this script.</li>
<li>Go to setting menu. You can see the experiments menu now.</li>
</ol>
<h1>Is this scam?</h1>

<img style="-webkit-user-select: none;margin: auto;background-color: hsl(0, 0%, 90%);transition: background-color 300ms;" src="https://raw.githubusercontent.com/HappyRogelio7/DiscordExperiments/main/Wiki/Console-Discord-IMG-1.png">
          
<p>Nope. but as you can see on the warning on console, if you don't know what script does. You can close console menu.<br>
Please do not paste any scripts on console menu. <strong>Before paste script(s), Please trying to review a code.</strong></p>
<h1>License Information</h1>
<p>I don't have any copyrights on this script.</p>
<p><code>samogot</code>'s LibDiscordInternals:</p>
<pre><code>MIT License

Copyright (c) 2017 samogot

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
</code></pre>
<p><code>Inve1951</code>'s BetterDiscordStuff:</p>
<pre><code>©2017-2018 square
</code></pre>
      </td>
      
# Code_DZB JavaScript

```js
(() => {
    // Extracted from Samogot's LibDiscordInternals for BetterDiscord.
    const req = typeof(webpackJsonp) === "function" ? webpackJsonp([], {
        '__extra_id__': (module, exports, req) => exports.default = req
    }, ['__extra_id__']).default : webpackJsonp.push([[], {
        '__extra_id__': (module, exports, req) => module.exports = req
    }, [['__extra_id__']]]);
    delete req.m['__extra_id__'];
    delete req.c['__extra_id__'];
    const find = (filter, options = {}) => {
        const {cacheOnly = true} = options;
        for (let i in req.c) {
            if (req.c.hasOwnProperty(i)) {
                let m = req.c[i].exports;
                if (m && m.__esModule && m.default && filter(m.default))
                    return m.default;
                if (m && filter(m))
                    return m;
            }
        }
        if (cacheOnly) {
            console.warn('Cannot find loaded module in cache');
            return null;
        }
        console.warn('Cannot find loaded module in cache. Loading all modules may have unexpected side effects');
        for (let i = 0; i < req.m.length; ++i) {
            try {
                let m = req(i);
                if (m && m.__esModule && m.default && filter(m.default))
                    return m.default;
                if (m && filter(m))
                    return m;
            }
            catch (e) {
            }
        }
        console.warn('Cannot find module');
        return null;
    };
    const findByUniqueProperties = (propNames, options) => find(module => propNames.every(prop => module[prop] !== undefined), options);
    // https://github.com/Inve1951/BetterDiscordStuff/blob/master/plugins/discordexperiments.plugin.js
    Object.defineProperty(findByUniqueProperties(["isDeveloper"]),"isDeveloper",{get:_=>1,set:_=>_,configurable:true});
})();
```
