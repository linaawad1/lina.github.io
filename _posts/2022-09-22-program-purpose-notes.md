---
keywords: fastai
description: Learning to use JavaScript
title: JavaScript
toc: true 
layout: default
badges: true
categories: [week 5]
nb_path: _notebooks/2022-09-22-program-purpose-notes.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-09-22-program-purpose-notes.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-javascript"><pre><span></span><span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="s2">&quot;My name is Lina!&quot;</span><span class="p">);</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>My name is Lina!
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-javascript"><pre><span></span><span class="kd">var</span> <span class="nx">msg</span> <span class="o">=</span> <span class="s2">&quot;My name is Lina!&quot;</span><span class="p">;</span>
<span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="nx">msg</span><span class="p">);</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>My name is Lina!
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-javascript"><pre><span></span><span class="kd">function</span> <span class="nx">logIt</span><span class="p">(</span><span class="nx">output</span><span class="p">)</span> <span class="p">{</span>
    <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="nx">output</span><span class="p">);</span>
<span class="p">}</span>
<span class="nx">logIt</span><span class="p">(</span><span class="nx">msg</span><span class="p">);</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>My name is Lina!
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-javascript"><pre><span></span><span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="s2">&quot;Reuse of logIT&quot;</span><span class="p">)</span>
<span class="nx">logIt</span><span class="p">(</span><span class="s2">&quot;What&#39;s up yo&quot;</span><span class="p">);</span>
<span class="nx">logIt</span><span class="p">(</span><span class="mf">111</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Reuse of logIT
What&#39;s up yo
111
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-javascript"><pre><span></span><span class="kd">function</span> <span class="nx">logItType</span><span class="p">(</span><span class="nx">output</span><span class="p">)</span> <span class="p">{</span>
    <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="k">typeof</span> <span class="nx">output</span><span class="p">,</span> <span class="s2">&quot;;&quot;</span><span class="p">,</span> <span class="nx">output</span><span class="p">)</span>
<span class="p">}</span>
<span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="s2">&quot;Did you have a good weekend?&quot;</span><span class="p">)</span>
<span class="nx">logItType</span><span class="p">(</span><span class="s2">&quot;Birthday&quot;</span><span class="p">)</span> <span class="c1">// String</span>
<span class="nx">logItType</span><span class="p">(</span><span class="s2">&quot;10-28-2006&quot;</span><span class="p">)</span> <span class="c1">// Number</span>
<span class="nx">logItType</span><span class="p">([</span><span class="mf">1</span><span class="p">,</span> <span class="mf">2</span><span class="p">,</span> <span class="mf">3</span><span class="p">]);</span> <span class="c1">//object</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Did you have a good weekend?
string ; Birthday
string ; 10-28-2006
object ; [ 1, 2, 3 ]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-javascript"><pre><span></span><span class="c1">// define a function to hold data for a Person</span>
<span class="kd">function</span> <span class="nx">Person</span><span class="p">(</span><span class="nx">name</span><span class="p">,</span> <span class="nx">age</span><span class="p">,</span> <span class="nx">classOf</span><span class="p">)</span> <span class="p">{</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">name</span> <span class="o">=</span> <span class="nx">name</span><span class="p">;</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">age</span> <span class="o">=</span> <span class="nx">age</span><span class="p">;</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">classOf</span> <span class="o">=</span> <span class="nx">classOf</span><span class="p">;</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">role</span> <span class="o">=</span> <span class="s2">&quot;&quot;</span><span class="p">;</span>
<span class="p">}</span>

<span class="c1">// define a setter for role in Person data</span>
<span class="nx">Person</span><span class="p">.</span><span class="nx">prototype</span><span class="p">.</span><span class="nx">setRole</span> <span class="o">=</span> <span class="kd">function</span><span class="p">(</span><span class="nx">role</span><span class="p">)</span> <span class="p">{</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">role</span> <span class="o">=</span> <span class="nx">role</span><span class="p">;</span>
<span class="p">}</span>

<span class="c1">// define a JSON conversion &quot;method&quot; associated with Person</span>
<span class="nx">Person</span><span class="p">.</span><span class="nx">prototype</span><span class="p">.</span><span class="nx">toJSON</span> <span class="o">=</span> <span class="kd">function</span><span class="p">()</span> <span class="p">{</span>
    <span class="kr">const</span> <span class="nx">obj</span> <span class="o">=</span> <span class="p">{</span><span class="nx">name</span><span class="o">:</span> <span class="k">this</span><span class="p">.</span><span class="nx">name</span><span class="p">,</span> <span class="nx">age</span><span class="o">:</span> <span class="k">this</span><span class="p">.</span><span class="nx">age</span><span class="p">,</span> <span class="nx">classOf</span><span class="o">:</span> <span class="k">this</span><span class="p">.</span><span class="nx">classOf</span><span class="p">,</span> <span class="nx">role</span><span class="o">:</span> <span class="k">this</span><span class="p">.</span><span class="nx">role</span><span class="p">};</span>
    <span class="kr">const</span> <span class="nx">json</span> <span class="o">=</span> <span class="nx">JSON</span><span class="p">.</span><span class="nx">stringify</span><span class="p">(</span><span class="nx">obj</span><span class="p">);</span>
    <span class="k">return</span> <span class="nx">json</span><span class="p">;</span>
<span class="p">}</span>

<span class="c1">// make a new Person and assign to variable me</span>
<span class="kd">var</span> <span class="nx">me</span> <span class="o">=</span> <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Lina&quot;</span><span class="p">,</span> <span class="s2">&quot;15&quot;</span><span class="p">,</span> <span class="mf">2024</span><span class="p">);</span>  <span class="c1">// object type is easy to work with in JavaScript</span>
<span class="nx">logItType</span><span class="p">(</span><span class="nx">me</span><span class="p">);</span>  <span class="c1">// before role</span>
<span class="nx">logItType</span><span class="p">(</span><span class="nx">me</span><span class="p">.</span><span class="nx">toJSON</span><span class="p">());</span>  <span class="c1">// ok to do this even though role is not yet defined</span>

<span class="c1">// output of Object and JSON/string associated with Teacher</span>
<span class="nx">teacher</span><span class="p">.</span><span class="nx">setRole</span><span class="p">(</span><span class="s2">&quot;me&quot;</span><span class="p">);</span>   <span class="c1">// set the role</span>
<span class="nx">logItType</span><span class="p">(</span><span class="nx">me</span><span class="p">);</span> 
<span class="nx">logItType</span><span class="p">(</span><span class="nx">me</span><span class="p">.</span><span class="nx">toJSON</span><span class="p">());</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>object ; Person { name: &#39;Lina&#39;, age: &#39;15&#39;, classOf: 2024, role: &#39;&#39; }
string ; {&#34;name&#34;:&#34;Lina&#34;,&#34;age&#34;:&#34;15&#34;,&#34;classOf&#34;:2024,&#34;role&#34;:&#34;&#34;}
object ; Person { name: &#39;Lina&#39;, age: &#39;15&#39;, classOf: 2024, role: &#39;&#39; }
string ; {&#34;name&#34;:&#34;Lina&#34;,&#34;age&#34;:&#34;15&#34;,&#34;classOf&#34;:2024,&#34;role&#34;:&#34;&#34;}
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-javascript"><pre><span></span><span class="c1">// define an HTML conversion &quot;method&quot; associated with Classroom</span>
<span class="nx">Classroom</span><span class="p">.</span><span class="nx">prototype</span><span class="p">.</span><span class="nx">_toHtml</span> <span class="o">=</span> <span class="kd">function</span><span class="p">()</span> <span class="p">{</span>
  <span class="c1">// HTML Style is build using inline structure</span>
  <span class="kd">var</span> <span class="nx">style</span> <span class="o">=</span> <span class="p">(</span>
    <span class="s2">&quot;display:inline-block;&quot;</span> <span class="o">+</span>
    <span class="s2">&quot;border: 2px dashed pink;&quot;</span> <span class="o">+</span>
    <span class="s2">&quot;background-color: black;&quot;</span> <span class="o">+</span>
    <span class="s2">&quot;box-shadow: 0.5em 0.5em 0.5em purple;&quot;</span>
  <span class="p">);</span>

  <span class="c1">// HTML Body of Table is build as a series of concatenations (+=)</span>
  <span class="kd">var</span> <span class="nx">body</span> <span class="o">=</span> <span class="s2">&quot;&quot;</span><span class="p">;</span>
  <span class="c1">// Heading for Array Columns</span>
  <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;tr&gt;&quot;</span><span class="p">;</span>
  <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;th&gt;&lt;mark&gt;&quot;</span> <span class="o">+</span> <span class="s2">&quot;Name&quot;</span> <span class="o">+</span> <span class="s2">&quot;&lt;/mark&gt;&lt;/th&gt;&quot;</span><span class="p">;</span>
  <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;th&gt;&lt;mark&gt;&quot;</span> <span class="o">+</span> <span class="s2">&quot;Age&quot;</span> <span class="o">+</span> <span class="s2">&quot;&lt;/mark&gt;&lt;/th&gt;&quot;</span><span class="p">;</span>
  <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;th&gt;&lt;mark&gt;&quot;</span> <span class="o">+</span> <span class="s2">&quot;Class Of&quot;</span> <span class="o">+</span> <span class="s2">&quot;&lt;/mark&gt;&lt;/th&gt;&quot;</span><span class="p">;</span>
  <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;th&gt;&lt;mark&gt;&quot;</span> <span class="o">+</span> <span class="s2">&quot;Role&quot;</span> <span class="o">+</span> <span class="s2">&quot;&lt;/mark&gt;&lt;/th&gt;&quot;</span><span class="p">;</span>
  <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;/tr&gt;&quot;</span><span class="p">;</span>
  <span class="c1">// Data of Array, iterate through each row of compsci.classroom </span>
  <span class="k">for</span> <span class="p">(</span><span class="kd">var</span> <span class="nx">row</span> <span class="k">of</span> <span class="nx">compsci</span><span class="p">.</span><span class="nx">classroom</span><span class="p">)</span> <span class="p">{</span>
    <span class="c1">// tr for each row, a new line</span>
    <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;tr&gt;&quot;</span><span class="p">;</span>
    <span class="c1">// td for each column of data</span>
    <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;td&gt;&quot;</span> <span class="o">+</span> <span class="nx">row</span><span class="p">.</span><span class="nx">name</span> <span class="o">+</span> <span class="s2">&quot;&lt;/td&gt;&quot;</span><span class="p">;</span>
    <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;td&gt;&quot;</span> <span class="o">+</span> <span class="nx">row</span><span class="p">.</span><span class="nx">age</span> <span class="o">+</span> <span class="s2">&quot;&lt;/td&gt;&quot;</span><span class="p">;</span>
    <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;td&gt;&quot;</span> <span class="o">+</span> <span class="nx">row</span><span class="p">.</span><span class="nx">classOf</span> <span class="o">+</span> <span class="s2">&quot;&lt;/td&gt;&quot;</span><span class="p">;</span>
    <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;td&gt;&quot;</span> <span class="o">+</span> <span class="nx">row</span><span class="p">.</span><span class="nx">role</span> <span class="o">+</span> <span class="s2">&quot;&lt;/td&gt;&quot;</span><span class="p">;</span>
    <span class="c1">// tr to end line</span>
    <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;tr&gt;&quot;</span><span class="p">;</span>
  <span class="p">}</span>

   <span class="c1">// Build and HTML fragment of div, table, table body</span>
  <span class="k">return</span> <span class="p">(</span>
    <span class="s2">&quot;&lt;div style=&#39;&quot;</span> <span class="o">+</span> <span class="nx">style</span> <span class="o">+</span> <span class="s2">&quot;&#39;&gt;&quot;</span> <span class="o">+</span>
      <span class="s2">&quot;&lt;table&gt;&quot;</span> <span class="o">+</span>
        <span class="nx">body</span> <span class="o">+</span>
      <span class="s2">&quot;&lt;/table&gt;&quot;</span> <span class="o">+</span>
    <span class="s2">&quot;&lt;/div&gt;&quot;</span>
  <span class="p">);</span>

<span class="p">};</span>

<span class="c1">// IJavaScript HTML processor receive parameter of defined HTML fragment</span>
<span class="nx">$$</span><span class="p">.</span><span class="nx">html</span><span class="p">(</span><span class="nx">compsci</span><span class="p">.</span><span class="nx">_toHtml</span><span class="p">());</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">


<div class="output_html rendered_html output_subarea output_execute_result">
<div style='display:inline-block;border: 2px dashed pink;background-color: black;font-color: white;box-shadow: 0.5em 0.5em 0.5em purple;'><table><tr><th><mark>Name</mark></th><th><mark>Age</mark></th><th><mark>Class Of</mark></th><th><mark>Role</mark></th></tr><tr><td>Lina</td><td>15</td><td>2024</td><td>me</td><tr><tr><td>Lydia</td><td>16</td><td>2024</td><td>friends</td><tr><tr><td>Naja</td><td>15</td><td>2025</td><td>friends</td><tr><tr><td>Dylan</td><td>15</td><td>2025</td><td>friends</td><tr></table></div>
</div>

</div>

</div>
</div>

</div>
    {% endraw %}

</div>
 
