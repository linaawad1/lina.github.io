---
keywords: fastai
description: An introduction to Data Abstraction using Python Lists [] and Python Dictionaries {}.
title: Lists, Dictionaries, Iteration
toc: true
categories: [collegeboard]
permalink: /collegeboard/python_lists
image: /images/python_lists.png
tags: [python]
nb_path: _notebooks/2022-08-29-TP120-python_lists.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-08-29-TP120-python_lists.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># variable of type string</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;What is the variable name/key?&quot;</span><span class="p">,</span> <span class="s2">&quot;value?&quot;</span><span class="p">,</span> <span class="s2">&quot;type?&quot;</span><span class="p">,</span> <span class="s2">&quot;primitive or collection, why?&quot;</span><span class="p">)</span>
<span class="n">name</span> <span class="o">=</span> <span class="s2">&quot;John Doe&quot;</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;name&quot;</span><span class="p">,</span> <span class="n">name</span><span class="p">,</span> <span class="nb">type</span><span class="p">(</span><span class="n">name</span><span class="p">))</span>

<span class="nb">print</span><span class="p">()</span>


<span class="c1"># variable of type integer</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;What is the variable name/key?&quot;</span><span class="p">,</span> <span class="s2">&quot;value?&quot;</span><span class="p">,</span> <span class="s2">&quot;type?&quot;</span><span class="p">,</span> <span class="s2">&quot;primitive or collection, why?&quot;</span><span class="p">)</span>
<span class="n">age</span> <span class="o">=</span> <span class="mi">18</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;age&quot;</span><span class="p">,</span> <span class="n">age</span><span class="p">,</span> <span class="nb">type</span><span class="p">(</span><span class="n">age</span><span class="p">))</span>

<span class="nb">print</span><span class="p">()</span>

<span class="c1"># variable of type float</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;What is the variable name/key?&quot;</span><span class="p">,</span> <span class="s2">&quot;value?&quot;</span><span class="p">,</span> <span class="s2">&quot;type?&quot;</span><span class="p">,</span> <span class="s2">&quot;primitive or collection, why?&quot;</span><span class="p">)</span>
<span class="n">score</span> <span class="o">=</span> <span class="mf">90.0</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;score&quot;</span><span class="p">,</span> <span class="n">score</span><span class="p">,</span> <span class="nb">type</span><span class="p">(</span><span class="n">score</span><span class="p">))</span>

<span class="nb">print</span><span class="p">()</span>

<span class="c1"># variable of type list (many values in one variable)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;What is variable name/key?&quot;</span><span class="p">,</span> <span class="s2">&quot;value?&quot;</span><span class="p">,</span> <span class="s2">&quot;type?&quot;</span><span class="p">,</span> <span class="s2">&quot;primitive or collection?&quot;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;What is different about the list output?&quot;</span><span class="p">)</span>
<span class="n">langs</span> <span class="o">=</span> <span class="p">[</span><span class="s2">&quot;Python&quot;</span><span class="p">,</span> <span class="s2">&quot;JavaScript&quot;</span><span class="p">,</span> <span class="s2">&quot;Java&quot;</span><span class="p">,</span> <span class="s2">&quot;Bash&quot;</span><span class="p">]</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;langs&quot;</span><span class="p">,</span> <span class="n">langs</span><span class="p">,</span> <span class="nb">type</span><span class="p">(</span><span class="n">langs</span><span class="p">),</span> <span class="s2">&quot;length&quot;</span><span class="p">,</span> <span class="nb">len</span><span class="p">(</span><span class="n">langs</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;- langs[3]&quot;</span><span class="p">,</span> <span class="n">langs</span><span class="p">[</span><span class="mi">3</span><span class="p">],</span> <span class="nb">type</span><span class="p">(</span><span class="n">langs</span><span class="p">[</span><span class="mi">3</span><span class="p">]))</span>

<span class="nb">print</span><span class="p">()</span>

<span class="c1"># variable of type dictionary (a group of keys and values)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;What is the variable name/key?&quot;</span><span class="p">,</span> <span class="s2">&quot;value?&quot;</span><span class="p">,</span> <span class="s2">&quot;type?&quot;</span><span class="p">,</span> <span class="s2">&quot;primitive or collection, why?&quot;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;What is different about the dictionary output?&quot;</span><span class="p">)</span>
<span class="n">person</span> <span class="o">=</span> <span class="p">{</span>
    <span class="s2">&quot;name&quot;</span><span class="p">:</span> <span class="n">name</span><span class="p">,</span>
    <span class="s2">&quot;age&quot;</span><span class="p">:</span> <span class="n">age</span><span class="p">,</span>
    <span class="s2">&quot;score&quot;</span><span class="p">:</span> <span class="n">score</span><span class="p">,</span>
    <span class="s2">&quot;langs&quot;</span><span class="p">:</span> <span class="n">langs</span>
<span class="p">}</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;person&quot;</span><span class="p">,</span> <span class="n">person</span><span class="p">,</span> <span class="nb">type</span><span class="p">(</span><span class="n">person</span><span class="p">),</span> <span class="s2">&quot;length&quot;</span><span class="p">,</span> <span class="nb">len</span><span class="p">(</span><span class="n">person</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;- person[&quot;name&quot;]&#39;</span><span class="p">,</span> <span class="n">person</span><span class="p">[</span><span class="s2">&quot;name&quot;</span><span class="p">],</span> <span class="nb">type</span><span class="p">(</span><span class="n">person</span><span class="p">[</span><span class="s2">&quot;name&quot;</span><span class="p">]))</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>What is the variable name/key? value? type? primitive or collection, why?
name John Doe &lt;class &#39;str&#39;&gt;

What is the variable name/key? value? type? primitive or collection, why?
age 18 &lt;class &#39;int&#39;&gt;

What is the variable name/key? value? type? primitive or collection, why?
score 90.0 &lt;class &#39;float&#39;&gt;

What is variable name/key? value? type? primitive or collection?
What is different about the list output?
langs [&#39;Python&#39;, &#39;JavaScript&#39;, &#39;Java&#39;, &#39;Bash&#39;] &lt;class &#39;list&#39;&gt; length 4
- langs[3] Bash &lt;class &#39;str&#39;&gt;

What is the variable name/key? value? type? primitive or collection, why?
What is different about the dictionary output?
person {&#39;name&#39;: &#39;John Doe&#39;, &#39;age&#39;: 18, &#39;score&#39;: 90.0, &#39;langs&#39;: [&#39;Python&#39;, &#39;JavaScript&#39;, &#39;Java&#39;, &#39;Bash&#39;]} &lt;class &#39;dict&#39;&gt; length 4
- person[&#34;name&#34;] John Doe &lt;class &#39;str&#39;&gt;
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="List-and-Dictionary-purpose">List and Dictionary purpose<a class="anchor-link" href="#List-and-Dictionary-purpose"> </a></h3><p>Our society is being built on information.  <mark>List and Dictionaries are used to collect information</mark>.  Mostly, when information is collected it is formed into patterns.  As that pattern is established you will be able collect many instances of that pattern.</p>
<ul>
<li>List is used to collect many instances of a pattern</li>
<li>Dictionary is used to define data patterns.</li>
<li>Iteration is often used to process through lists.</li>
</ul>
<p>To start exploring more deeply into List, Dictionary and Iteration this example will explore constructing a List of people and cars.</p>
<ul>
<li>As we learned above, a List is a data type: class 'list'</li>
<li>A <mark>'list' data type has the method '.append(expression)'</mark> that allows you to add to the list.  A class usually has extra method to support working with its objects/instances.</li>
<li>In the example below,  the expression is appended to the 'list' is the data type: class 'dict'</li>
<li>At the end, you see a fairly complicated data structure.  This is a <mark>list of dictionaries</mark>, or a collection of many similar data patterns.  The output looks similar to JavaScript Object Notation (JSON), Jekyll/GitHub pages yml files, FastPages Front Matter. As discussed we will see this key/value patter often, you will be required to understand this data structure and understand the parts.  Just believe it is peasy ;) and it will become so.</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">InfoDb</span> <span class="o">=</span> <span class="p">[]</span>

<span class="c1"># InfoDB is a data structure with expected Keys and Values</span>

<span class="c1"># Append to List a Dictionary of key/values related to a person and cars</span>
<span class="n">InfoDb</span><span class="o">.</span><span class="n">append</span><span class="p">({</span>
    <span class="s2">&quot;FirstName&quot;</span><span class="p">:</span> <span class="s2">&quot;John&quot;</span><span class="p">,</span>
    <span class="s2">&quot;LastName&quot;</span><span class="p">:</span> <span class="s2">&quot;Mortensen&quot;</span><span class="p">,</span>
    <span class="s2">&quot;DOB&quot;</span><span class="p">:</span> <span class="s2">&quot;October 21&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Residence&quot;</span><span class="p">:</span> <span class="s2">&quot;San Diego&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Email&quot;</span><span class="p">:</span> <span class="s2">&quot;jmortensen@powayusd.com&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Owns_Cars&quot;</span><span class="p">:</span> <span class="p">[</span><span class="s2">&quot;2015-Fusion&quot;</span><span class="p">,</span> <span class="s2">&quot;2011-Ranger&quot;</span><span class="p">,</span> <span class="s2">&quot;2003-Excursion&quot;</span><span class="p">,</span> <span class="s2">&quot;1997-F350&quot;</span><span class="p">,</span> <span class="s2">&quot;1969-Cadillac&quot;</span><span class="p">]</span>
<span class="p">})</span>

<span class="c1"># Append to List a 2nd Dictionary of key/values</span>
<span class="n">InfoDb</span><span class="o">.</span><span class="n">append</span><span class="p">({</span>
    <span class="s2">&quot;FirstName&quot;</span><span class="p">:</span> <span class="s2">&quot;Sunny&quot;</span><span class="p">,</span>
    <span class="s2">&quot;LastName&quot;</span><span class="p">:</span> <span class="s2">&quot;Naidu&quot;</span><span class="p">,</span>
    <span class="s2">&quot;DOB&quot;</span><span class="p">:</span> <span class="s2">&quot;August 2&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Residence&quot;</span><span class="p">:</span> <span class="s2">&quot;Temecula&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Email&quot;</span><span class="p">:</span> <span class="s2">&quot;snaidu@powayusd.com&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Owns_Cars&quot;</span><span class="p">:</span> <span class="p">[</span><span class="s2">&quot;4Runner&quot;</span><span class="p">]</span>
<span class="p">})</span>

<span class="n">InfoDb</span><span class="o">.</span><span class="n">append</span><span class="p">({</span>
    <span class="s2">&quot;FirstName&quot;</span><span class="p">:</span> <span class="s2">&quot;Lina&quot;</span><span class="p">,</span>
    <span class="s2">&quot;LastName&quot;</span><span class="p">:</span> <span class="s2">&quot;Awad&quot;</span><span class="p">,</span>
    <span class="s2">&quot;DOB&quot;</span><span class="p">:</span> <span class="s2">&quot;October 28&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Residence&quot;</span><span class="p">:</span> <span class="s2">&quot;San Diego&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Email&quot;</span><span class="p">:</span> <span class="s2">&quot;lina.eid28@gmail.com&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Own_Cars&quot;</span><span class="p">:</span> <span class="p">[</span><span class="s2">&quot;Honda&quot;</span><span class="p">,</span> <span class="s2">&quot;Infinity&quot;</span><span class="p">,</span> <span class="s2">&quot;Tesla&quot;</span><span class="p">]</span>
<span class="p">})</span>

<span class="c1"># Print the data structure</span>
<span class="nb">print</span><span class="p">(</span><span class="n">InfoDb</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[{&#39;FirstName&#39;: &#39;John&#39;, &#39;LastName&#39;: &#39;Mortensen&#39;, &#39;DOB&#39;: &#39;October 21&#39;, &#39;Residence&#39;: &#39;San Diego&#39;, &#39;Email&#39;: &#39;jmortensen@powayusd.com&#39;, &#39;Owns_Cars&#39;: [&#39;2015-Fusion&#39;, &#39;2011-Ranger&#39;, &#39;2003-Excursion&#39;, &#39;1997-F350&#39;, &#39;1969-Cadillac&#39;]}, {&#39;FirstName&#39;: &#39;Sunny&#39;, &#39;LastName&#39;: &#39;Naidu&#39;, &#39;DOB&#39;: &#39;August 2&#39;, &#39;Residence&#39;: &#39;Temecula&#39;, &#39;Email&#39;: &#39;snaidu@powayusd.com&#39;, &#39;Owns_Cars&#39;: [&#39;4Runner&#39;]}, {&#39;FirstName&#39;: &#39;Lina&#39;, &#39;LastName&#39;: &#39;Awad&#39;, &#39;DOB&#39;: &#39;October 28&#39;, &#39;Residence&#39;: &#39;San Diego&#39;, &#39;Email&#39;: &#39;lina.eid28@gmail.com&#39;, &#39;Own_Cars&#39;: [&#39;Honda&#39;, &#39;Infinity&#39;, &#39;Tesla&#39;]}]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Formatted-output-of-List/Dictionary---for-loop">Formatted output of List/Dictionary - for loop<a class="anchor-link" href="#Formatted-output-of-List/Dictionary---for-loop"> </a></h3><p>Managing data in Lists and Dictionaries is for the convenience of passing the data across the internet, to applications, or preparing it to be stored into a database.  It is a great way to exchange data between programs and programmers.  Exchange of data between programs includes the data type the method/function and the format of the data type.  These concepts are key to learning how to write functions, receive, and return data.  This process is often referred to as an <mark>Application Programming Interface (API)</mark>.</p>
<p>Next, we will take the stored data and output it within our notebook.  There are multiple steps to this process...</p>
<ul>
<li><mark>Preparing a function to format the data</mark>, the print_data() function receives a parameter called "d_rec" short for dictionary record.  It then references different keys within [] square brackets.   </li>
<li><mark>Preparing a function to iterate through the list</mark>, the for_loop() function uses an enhanced for loop that pull record by record out of InfoDb until the list is empty.  Each time through the loop it call print_data(record), which passes the dictionary record to that function.</li>
<li>Finally, you need to <mark>activate your function</mark> with the call to the defined function for_loop().  Functions are defined, not activated until they are called.  By placing for_loop() at the left margin the function is activated.</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># print function: given a dictionary of InfoDb content</span>
<span class="k">def</span> <span class="nf">print_data</span><span class="p">(</span><span class="n">d_rec</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">d_rec</span><span class="p">[</span><span class="s2">&quot;FirstName&quot;</span><span class="p">],</span> <span class="n">d_rec</span><span class="p">[</span><span class="s2">&quot;LastName&quot;</span><span class="p">])</span>  <span class="c1"># using comma puts space between values</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\t</span><span class="s2">&quot;</span><span class="p">,</span> <span class="s2">&quot;Residence:&quot;</span><span class="p">,</span> <span class="n">d_rec</span><span class="p">[</span><span class="s2">&quot;Residence&quot;</span><span class="p">])</span> <span class="c1"># \t is a tab indent</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\t</span><span class="s2">&quot;</span><span class="p">,</span> <span class="s2">&quot;Birth Day:&quot;</span><span class="p">,</span> <span class="n">d_rec</span><span class="p">[</span><span class="s2">&quot;DOB&quot;</span><span class="p">])</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\t</span><span class="s2">&quot;</span><span class="p">,</span> <span class="s2">&quot;Cars: &quot;</span><span class="p">,</span> <span class="n">end</span><span class="o">=</span><span class="s2">&quot;&quot;</span><span class="p">)</span>  <span class="c1"># end=&quot;&quot; make sure no return occurs</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">d_rec</span><span class="p">[</span><span class="s2">&quot;Owns_Cars&quot;</span><span class="p">]))</span>  <span class="c1"># join allows printing a string list with separator</span>
    <span class="nb">print</span><span class="p">()</span>

<span class="c1"># for loop algorithm iterates on length of InfoDb</span>
<span class="k">def</span> <span class="nf">for_loop</span><span class="p">():</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;For loop output</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>
    <span class="k">for</span> <span class="n">record</span> <span class="ow">in</span> <span class="n">InfoDb</span><span class="p">:</span>
        <span class="n">print_data</span><span class="p">(</span><span class="n">record</span><span class="p">)</span>

<span class="n">for_loop</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>For loop output

John Mortensen
	 Residence: San Diego
	 Birth Day: October 21
	 Cars: 2015-Fusion, 2011-Ranger, 2003-Excursion, 1997-F350, 1969-Cadillac

Sunny Naidu
	 Residence: Temecula
	 Birth Day: August 2
	 Cars: 4Runner

Lina Awad
	 Residence: San Diego
	 Birth Day: October 28
	 Cars: </pre>
</div>
</div>

<div class="output_area">

<div class="output_subarea output_text output_error">
<pre>
<span class="ansi-red-fg">---------------------------------------------------------------------------</span>
<span class="ansi-red-fg">KeyError</span>                                  Traceback (most recent call last)
<span class="ansi-green-intense-fg ansi-bold">/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb Cell 7</span> in <span class="ansi-cyan-fg">&lt;cell line: 18&gt;</span><span class="ansi-blue-fg">()</span>
<span class="ansi-green-intense-fg ansi-bold">     &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#W6sZmlsZQ%3D%3D?line=14&#39;&gt;15&lt;/a&gt;</span>     for record in InfoDb:
<span class="ansi-green-intense-fg ansi-bold">     &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#W6sZmlsZQ%3D%3D?line=15&#39;&gt;16&lt;/a&gt;</span>         print_data(record)
<span class="ansi-green-fg">---&gt; &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#W6sZmlsZQ%3D%3D?line=17&#39;&gt;18&lt;/a&gt;</span> for_loop()

<span class="ansi-green-intense-fg ansi-bold">/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb Cell 7</span> in <span class="ansi-cyan-fg">for_loop</span><span class="ansi-blue-fg">()</span>
<span class="ansi-green-intense-fg ansi-bold">     &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#W6sZmlsZQ%3D%3D?line=13&#39;&gt;14&lt;/a&gt;</span> print(&#34;For loop output\n&#34;)
<span class="ansi-green-intense-fg ansi-bold">     &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#W6sZmlsZQ%3D%3D?line=14&#39;&gt;15&lt;/a&gt;</span> for record in InfoDb:
<span class="ansi-green-fg">---&gt; &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#W6sZmlsZQ%3D%3D?line=15&#39;&gt;16&lt;/a&gt;</span>     print_data(record)

<span class="ansi-green-intense-fg ansi-bold">/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb Cell 7</span> in <span class="ansi-cyan-fg">print_data</span><span class="ansi-blue-fg">(d_rec)</span>
<span class="ansi-green-intense-fg ansi-bold">      &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#W6sZmlsZQ%3D%3D?line=6&#39;&gt;7&lt;/a&gt;</span> print(&#34;\t&#34;, &#34;Birth Day:&#34;, d_rec[&#34;DOB&#34;])
<span class="ansi-green-intense-fg ansi-bold">      &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#W6sZmlsZQ%3D%3D?line=7&#39;&gt;8&lt;/a&gt;</span> print(&#34;\t&#34;, &#34;Cars: &#34;, end=&#34;&#34;)  # end=&#34;&#34; make sure no return occurs
<span class="ansi-green-fg">----&gt; &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#W6sZmlsZQ%3D%3D?line=8&#39;&gt;9&lt;/a&gt;</span> print(&#34;, &#34;.join(d_rec[&#34;Owns_Cars&#34;]))  # join allows printing a string list with separator
<span class="ansi-green-intense-fg ansi-bold">     &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#W6sZmlsZQ%3D%3D?line=9&#39;&gt;10&lt;/a&gt;</span> print()

<span class="ansi-red-fg">KeyError</span>: &#39;Owns_Cars&#39;</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Alternate-methods-for-iteration---while-loop">Alternate methods for iteration - while loop<a class="anchor-link" href="#Alternate-methods-for-iteration---while-loop"> </a></h3><p>In coding, there are usually many ways to achieve the same result.  Defined are functions illustrating using index to reference records in a list, these methods are called a "while" loop and "recursion".</p>
<ul>
<li>The while_loop() function contains a while loop, "while i &lt; len(InfoDb):".  This counts through the elements in the list start at zero, and passes the record to print_data()</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># while loop algorithm contains an initial n and an index incrementing statement (n += 1)</span>
<span class="k">def</span> <span class="nf">while_loop</span><span class="p">():</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;While loop output</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>
    <span class="n">i</span> <span class="o">=</span> <span class="mi">0</span>
    <span class="k">while</span> <span class="n">i</span> <span class="o">&lt;</span> <span class="nb">len</span><span class="p">(</span><span class="n">InfoDb</span><span class="p">):</span>
        <span class="n">record</span> <span class="o">=</span> <span class="n">InfoDb</span><span class="p">[</span><span class="n">i</span><span class="p">]</span>
        <span class="n">print_data</span><span class="p">(</span><span class="n">record</span><span class="p">)</span>
        <span class="n">i</span> <span class="o">+=</span> <span class="mi">1</span>
    <span class="k">return</span>

<span class="n">while_loop</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>While loop output

John Mortensen
	 Residence: San Diego
	 Birth Day: October 21
	 Cars: 2015-Fusion, 2011-Ranger, 2003-Excursion, 1997-F350, 1969-Cadillac

Sunny Naidu
	 Residence: Temecula
	 Birth Day: August 2
	 Cars: 4Runner

</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Calling-a-function-repeatedly---recursion">Calling a function repeatedly - recursion<a class="anchor-link" href="#Calling-a-function-repeatedly---recursion"> </a></h3><p>This final technique achieves looping by calling itself repeatedly.</p>
<ul>
<li>recursive_loop(i) function is primed with the value 0 on its activation with "recursive_loop(0)"</li>
<li>the last statement indented inside the if statement "recursive_loop(i + 1)" activates another call to the recursive_loop(i) function, each time i is increasing</li>
<li>ultimately the "if i &lt; len(InfoDb):" will evaluate to false and the program ends</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># recursion algorithm loops incrementing on each call (n + 1) until exit condition is met</span>
<span class="k">def</span> <span class="nf">recursive_loop</span><span class="p">(</span><span class="n">i</span><span class="p">):</span>
    <span class="k">if</span> <span class="n">i</span> <span class="o">&lt;</span> <span class="nb">len</span><span class="p">(</span><span class="n">InfoDb</span><span class="p">):</span>
        <span class="n">record</span> <span class="o">=</span> <span class="n">InfoDb</span><span class="p">[</span><span class="n">i</span><span class="p">]</span>
        <span class="n">print_data</span><span class="p">(</span><span class="n">record</span><span class="p">)</span>
        <span class="n">recursive_loop</span><span class="p">(</span><span class="n">i</span> <span class="o">+</span> <span class="mi">1</span><span class="p">)</span>
    <span class="k">return</span>
    
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Recursive loop output</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>
<span class="n">recursive_loop</span><span class="p">(</span><span class="mi">0</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Recursive loop output

</pre>
</div>
</div>

<div class="output_area">

<div class="output_subarea output_text output_error">
<pre>
<span class="ansi-red-fg">---------------------------------------------------------------------------</span>
<span class="ansi-red-fg">NameError</span>                                 Traceback (most recent call last)
<span class="ansi-green-intense-fg ansi-bold">/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb Cell 11</span> in <span class="ansi-cyan-fg">&lt;cell line: 12&gt;</span><span class="ansi-blue-fg">()</span>
<span class="ansi-green-intense-fg ansi-bold">      &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#X13sZmlsZQ%3D%3D?line=8&#39;&gt;9&lt;/a&gt;</span>     return
<span class="ansi-green-intense-fg ansi-bold">     &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#X13sZmlsZQ%3D%3D?line=10&#39;&gt;11&lt;/a&gt;</span> print(&#34;Recursive loop output\n&#34;)
<span class="ansi-green-fg">---&gt; &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#X13sZmlsZQ%3D%3D?line=11&#39;&gt;12&lt;/a&gt;</span> recursive_loop(0)

<span class="ansi-green-intense-fg ansi-bold">/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb Cell 11</span> in <span class="ansi-cyan-fg">recursive_loop</span><span class="ansi-blue-fg">(i)</span>
<span class="ansi-green-intense-fg ansi-bold">      &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#X13sZmlsZQ%3D%3D?line=4&#39;&gt;5&lt;/a&gt;</span> if i &lt; len(InfoDb):
<span class="ansi-green-intense-fg ansi-bold">      &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#X13sZmlsZQ%3D%3D?line=5&#39;&gt;6&lt;/a&gt;</span>     record = InfoDb[i]
<span class="ansi-green-fg">----&gt; &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#X13sZmlsZQ%3D%3D?line=6&#39;&gt;7&lt;/a&gt;</span>     print_data(record)
<span class="ansi-green-intense-fg ansi-bold">      &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#X13sZmlsZQ%3D%3D?line=7&#39;&gt;8&lt;/a&gt;</span>     recursive_loop(i + 1)
<span class="ansi-green-intense-fg ansi-bold">      &lt;a href=&#39;vscode-notebook-cell:/Users/linaalsheikh-eid/APCSP/_notebooks/2022-08-29-TP120-python_lists.ipynb#X13sZmlsZQ%3D%3D?line=8&#39;&gt;9&lt;/a&gt;</span> return

<span class="ansi-red-fg">NameError</span>: name &#39;print_data&#39; is not defined</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">FirstName</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;What is your first name?&quot;</span><span class="p">)</span>

<span class="n">Age</span><span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;How old are you?&quot;</span><span class="p">)</span>

<span class="n">FavoriteDrink</span><span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;What is your favorite drink?&quot;</span><span class="p">)</span>

<span class="n">BestSeason</span><span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;What is the best season of the year?&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

</div>
 

