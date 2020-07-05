<h1 class="code-line" data-line-start=0 data-line-end=1 ><a id="webpackconfig_by_Batyodie_0"></a>webpack-config by Batyodie</h1>
<p class="has-line-data" data-line-start="2" data-line-end="3"><a href="http://github.com/batyodie"><img src="https://travis-ci.org/joemccann/dillinger.svg?branch=master" alt="Build Status"></a></p>
<p class="has-line-data" data-line-start="4" data-line-end="5">An opinionated <a href="https://webpack.js.org/">webpack</a> config for GitHub apps.</p>
<h1 class="code-line" data-line-start=6 data-line-end=7 ><a id="Features_6"></a>Features!</h1>
<ul>
<li class="has-line-data" data-line-start="8" data-line-end="9">Single and multiple HTML entry points</li>
<li class="has-line-data" data-line-start="9" data-line-end="10">Common chunks bundle when using multiple entry points</li>
<li class="has-line-data" data-line-start="10" data-line-end="11">ES6 transpilation via Babel</li>
<li class="has-line-data" data-line-start="11" data-line-end="12">Source Maps</li>
<li class="has-line-data" data-line-start="12" data-line-end="13">PostCSS/scss(sass)/less</li>
<li class="has-line-data" data-line-start="13" data-line-end="14">Eslint/pritter/stylelint</li>
<li class="has-line-data" data-line-start="14" data-line-end="15">Pre-commit</li>
<li class="has-line-data" data-line-start="15" data-line-end="16">Image Optimization</li>
<li class="has-line-data" data-line-start="16" data-line-end="17">HTML, css and JS minification (in production)</li>
<li class="has-line-data" data-line-start="17" data-line-end="18">Static brotli compression (in production)</li>
</ul>
<h3 class="code-line" data-line-start=23 data-line-end=24 ><a id="Deployment_23"></a>Deployment</h3>
<p class="has-line-data" data-line-start="25" data-line-end="26">Currently intended for deployment on heroku, more on <a href="https://medium.com/devschacht/%D0%BA%D0%B0%D0%BA-%D1%80%D0%B0%D0%B7%D0%BC%D0%B5%D1%81%D1%82%D0%B8%D1%82%D1%8C-vue-app-%D0%BD%D0%B0-heroku-29a3102a9c2d">deployment</a>.</p>
<h3 class="code-line" data-line-start=27 data-line-end=28 ><a id="Basic_Setup_27"></a>Basic Setup</h3>
<p class="has-line-data" data-line-start="29" data-line-end="30">Dillinger requires <a href="https://nodejs.org/">Node.js</a> v4+ to run.</p>
<p class="has-line-data" data-line-start="31" data-line-end="32">Install the dependencies and devDependencies and start the server.</p>
<pre><code class="has-line-data" data-line-start="34" data-line-end="38" class="language-sh">$ <span class="hljs-built_in">cd</span> my-project
$ npm install 
$ npm run start
</code></pre>
<p class="has-line-data" data-line-start="39" data-line-end="40">For development environments…</p>
<pre><code class="has-line-data" data-line-start="42" data-line-end="44" class="language-sh">$ npm run dev
</code></pre>
<h3 class="code-line" data-line-start=45 data-line-end=46 ><a id="Directory_Structure_45"></a>Directory Structure</h3>
<p class="has-line-data" data-line-start="47" data-line-end="71">app<br>
├──  package.json<br>
├── src<br>
│     └──  index.js<br>
│     └──  index.html<br>
│     └──  styles.css<br>
│     └──  assets<br>
│       │      └──   fonts<br>
│       └──  common<br>
│       │      └──   button<br>
│       │       │      └──   button.css<br>
│       │       │      └──   button.js<br>
│       │       │      └──   button.png<br>
│       └──  desktop<br>
│       └──  touch<br>
│       └──  styles<br>
│       │        └──   vars.css<br>
│       │        └──   reset.css<br>
│       │        └──   break-points.css<br>
├──  webpack.config<br>
├──  node_modules<br>
├──  dist<br>
├──  .gitignore<br>
├──  README</p>
<h4 class="code-line" data-line-start=72 data-line-end=73 ><a id="Building_for_source_72"></a>Building for source</h4>
<p class="has-line-data" data-line-start="73" data-line-end="74">For production release:</p>
<pre><code class="has-line-data" data-line-start="75" data-line-end="77" class="language-sh">$ npm run build 
</code></pre>
<h5 class="code-line" data-line-start=77 data-line-end=78 ><a id="srcassets_77"></a>src/assets</h5>
<p class="has-line-data" data-line-start="78" data-line-end="79">The public/ directory contains static assets that will be exposed as is. This is useful for well known static assets that need to be served at a specific root path like favicon.ico and robots.txt fonts.</p>
<h5 class="code-line" data-line-start=80 data-line-end=81 ><a id="src_80"></a>src/</h5>
<p class="has-line-data" data-line-start="81" data-line-end="82">Contains source JavaScript, CSS and other assets that will be compiled via webpack.</p>
<h5 class="code-line" data-line-start=83 data-line-end=84 ><a id="srccommon_83"></a>src/common</h5>
<p class="has-line-data" data-line-start="84" data-line-end="85">General directory for storing blocks, components, elements and modifiers.</p>
<h5 class="code-line" data-line-start=86 data-line-end=87 ><a id="srcdesktop_86"></a>src/desktop</h5>
<p class="has-line-data" data-line-start="87" data-line-end="88">Directory for storing blocks, components, elements and modifiers designed for desktop devices.</p>
<h5 class="code-line" data-line-start=89 data-line-end=90 ><a id="srctouch_89"></a>src/touch</h5>
<p class="has-line-data" data-line-start="90" data-line-end="91">Directory for storing blocks, components, elements and modifiers intended for touch devices</p>
<h5 class="code-line" data-line-start=92 data-line-end=93 ><a id="srcstyles_92"></a>src/styles</h5>
<p class="has-line-data" data-line-start="93" data-line-end="95">A directory for storing static styles such as normalize reset css, vars,<br>
breakpoints, or styles for third-party libraries</p>
<h4 class="code-line" data-line-start=95 data-line-end=96 ><a id="srcindexjs_95"></a>src/index.js</h4>
<p class="has-line-data" data-line-start="96" data-line-end="97">Is the main entry point for bootstrapping the application.</p>
<p class="has-line-data" data-line-start="98" data-line-end="99">When using vue, this file should render the root application component.</p>
<p class="has-line-data" data-line-start="100" data-line-end="102">
  ```
import Vue from ‘vue’<br>
import App from ‘./App.vue’</p>

<p class="has-line-data" data-line-start="103" data-line-end="106">new Vue({<br>
render: h =&gt; h(App)<br>
}).$mount(’#app’)</p>
```
