<div align="center">

## Try/Catch Blues


</div>

### Description

Performance - It may seem like you are doing good putting try/catch blocks all throughout your code, but you are probably being redundant.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Sachin Mehra \(Delhi\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/sachin-mehra-delhi.md)
**Level**          |Advanced
**User Rating**    |4.6 (69 globes from 15 users)
**Compatibility**  |Java \(JDK 1\.1\), Java \(JDK 1\.2\)
**Category**       |[Coding Standards](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/coding-standards__2-87.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/sachin-mehra-delhi-try-catch-blues__2-2957/archive/master.zip)





### Source Code

```
<html xmlns:o="urn:schemas-microsoft-com:office:office"
xmlns:w="urn:schemas-microsoft-com:office:word"
xmlns="http://www.w3.org/TR/REC-html40">
<head>
<meta http-equiv=Content-Type content="text/html; charset=windows-1252">
<meta name=ProgId content=Word.Document>
<meta name=Generator content="Microsoft Word 10">
<meta name=Originator content="Microsoft Word 10">
<link rel=File-List href="Try_files/filelist.xml">
<title>Try/Catch Blues</title>
<!--[if gte mso 9]><xml>
 <o:DocumentProperties>
 <o:Author>Sachin</o:Author>
 <o:LastAuthor>default</o:LastAuthor>
 <o:Revision>1</o:Revision>
 <o:TotalTime>21</o:TotalTime>
 <o:Created>2002-06-07T04:20:00Z</o:Created>
 <o:LastSaved>2002-06-07T04:41:00Z</o:LastSaved>
 <o:Pages>1</o:Pages>
 <o:Words>914</o:Words>
 <o:Characters>5215</o:Characters>
 <o:Lines>43</o:Lines>
 <o:Paragraphs>12</o:Paragraphs>
 <o:CharactersWithSpaces>6117</o:CharactersWithSpaces>
 <o:Version>10.2625</o:Version>
 </o:DocumentProperties>
</xml><![endif]--><!--[if gte mso 9]><xml>
 <w:WordDocument>
 <w:SpellingState>Clean</w:SpellingState>
 <w:GrammarState>Clean</w:GrammarState>
 <w:Compatibility>
  <w:BreakWrappedTables/>
  <w:SnapToGridInCell/>
  <w:WrapTextWithPunct/>
  <w:UseAsianBreakRules/>
 </w:Compatibility>
 <w:BrowserLevel>MicrosoftInternetExplorer4</w:BrowserLevel>
 </w:WordDocument>
</xml><![endif]-->
<style>
<!--
 /* Style Definitions */
 p.MsoNormal, li.MsoNormal, div.MsoNormal
	{mso-style-parent:"";
	margin:0in;
	margin-bottom:.0001pt;
	mso-pagination:widow-orphan;
	font-size:12.0pt;
	font-family:"Times New Roman";
	mso-fareast-font-family:"Times New Roman";}
a:link, span.MsoHyperlink
	{color:blue;
	text-decoration:underline;
	text-underline:single;}
a:visited, span.MsoHyperlinkFollowed
	{color:purple;
	text-decoration:underline;
	text-underline:single;}
span.SpellE
	{mso-style-name:"";
	mso-spl-e:yes;}
span.GramE
	{mso-style-name:"";
	mso-gram-e:yes;}
@page Section1
	{size:8.5in 11.0in;
	margin:1.0in 1.25in 1.0in 1.25in;
	mso-header-margin:.5in;
	mso-footer-margin:.5in;
	mso-paper-source:0;}
div.Section1
	{page:Section1;}
-->
</style>
<!--[if gte mso 10]>
<style>
 /* Style Definitions */
 table.MsoNormalTable
	{mso-style-name:"Table Normal";
	mso-tstyle-rowband-size:0;
	mso-tstyle-colband-size:0;
	mso-style-noshow:yes;
	mso-style-parent:"";
	mso-padding-alt:0in 5.4pt 0in 5.4pt;
	mso-para-margin:0in;
	mso-para-margin-bottom:.0001pt;
	mso-pagination:widow-orphan;
	font-size:10.0pt;
	font-family:"Times New Roman";}
</style>
<![endif]-->
</head>
<body lang=EN-US link=blue vlink=purple style='tab-interval:.5in'>
<div class=Section1>
<p class=MsoNormal><span style='font-size:16.0pt;font-family:Arial'>Try/Catch
Blues</span><o:p></o:p></p>
<p class=MsoNormal><span class=GramE><span style='font-size:10.0pt;font-family:
Arial'>Error Checking Gone Horribly Wrong.</span></span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>Technical
Article by Sachin Mehra (<a href="mailto:mbrock@corebrix.com"><i><span
style='color:windowtext;text-decoration:none;text-underline:none'><span
style='mso-field-code:" HYPERLINK \0022mailto\:sachinweb\@hotmail\.com\0022 "'><u><span
style='color:blue'>sachinweb@hotmail.com</span></u></span></span></i></a>)</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>It may seem
like you are doing good putting try/catch blocks all throughout your code, but
you are probably being redundant.&nbsp; When you declare a try/catch block in
Java you cause the compiler to create “protected zones” of execution which
require the runtime to do boundary checks and create further processing for the
system.&nbsp; You are not making the program more stable by doing <span
class=GramE>this,</span> you are making it many times slower!</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>If you have
a try/catch block which has only one line of code inside the </span><span
style='font-size:10.0pt;font-family:"Courier New"'>try <span class=GramE>{ …</span>
}&nbsp; </span><span style='font-size:10.0pt;font-family:Arial'>you are
probably being inefficient.&nbsp; </span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>Here is an
example of a <b>bad</b> piece of code:</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><b><span style='font-size:8.0pt;font-family:Arial'>Example
1a</span></b><span style='font-size:10.0pt;font-family:Arial'>:</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span class=GramE><b><span
style='font-size:8.0pt;font-family:"Courier New"'>public</span></b></span><span
style='font-size:8.0pt;font-family:"Courier New"'> <span class=SpellE>HashTable</span>
<span class=SpellE>doEvent</span>(Event <span class=SpellE>event</span>) <b>throws</b>
<span class=SpellE>CBException</span> { </span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; Connection <span class=SpellE>conn</span> =
<b>null</b>;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; <span class=SpellE>EntityClass</span> <span
class=SpellE>entClass</span> = <b>null</b>;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; <span class=SpellE>ArrayList</span> list =
<b>null</b>;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><b><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; <span class=GramE>try</span></span></b><span
style='font-size:8.0pt;font-family:"Courier New"'> {</span><o:p></o:p></p>
<p class=MsoNormal style='text-indent:.5in;background:#E6E6E6'><span
class=GramE><b><span style='font-size:8.0pt;font-family:"Courier New"'>try</span></b></span><span
style='font-size:8.0pt;font-family:"Courier New"'> {</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=SpellE><span class=GramE>conn</span></span>
= <span class=SpellE>dataAdapter.getConnection</span>(<span
class=SpellE>DataSource.PRIMARY</span>);</span><o:p></o:p></p>
<p class=MsoNormal style='text-indent:.5in;background:#E6E6E6'><span
style='font-size:8.0pt;font-family:"Courier New"'>}</span><o:p></o:p></p>
<p class=MsoNormal style='text-indent:.5in;background:#E6E6E6'><span
class=GramE><b><span style='font-size:8.0pt;font-family:"Courier
New"'>catch</span></b></span><span
style='font-size:8.0pt;font-family:"Courier New"'> (Exception e) {</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=SpellE><span
class=GramE>System.out.println</span></span><span
class=GramE>(</span>“[<span class=SpellE>SomeClass</span>] An error occurred
obtaining connection: “ + <span class=SpellE>e.getMessage</span>());</span><o:p></o:p></p>
<p class=MsoNormal style='text-indent:.5in;background:#E6E6E6'><span
style='font-size:8.0pt;font-family:"Courier New"'>}</span><o:p></o:p></p>
<p class=MsoNormal style='text-indent:.5in;background:#E6E6E6'><span
class=GramE><b><span style='font-size:8.0pt;font-family:"Courier New"'>try</span></b></span><span
style='font-size:8.0pt;font-family:"Courier New"'> { </span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=SpellE><span class=GramE>entClass</span></span>
= new <span class=SpellE>EntityClass</span>();</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=GramE>list</span> = <span
class=SpellE>entClass.list</span>(<span class=SpellE>conn</span>);</span><o:p></o:p></p>
<p class=MsoNormal style='text-indent:.5in;background:#E6E6E6'><span
style='font-size:8.0pt;font-family:"Courier New"'>}</span><o:p></o:p></p>
<p class=MsoNormal style='text-indent:.5in;background:#E6E6E6'><span
class=GramE><b><span style='font-size:8.0pt;font-family:"Courier
New"'>catch</span></b></span><span
style='font-size:8.0pt;font-family:"Courier New"'> (Exception e)
{&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=SpellE><span
class=GramE>System.out.println</span></span><span
class=GramE>(</span>“[<span class=SpellE>SomeClass</span>] An error occurred
obtaining data from the Entity: “ + <span
class=SpellE>e.getMessage</span>());</span><o:p></o:p></p>
<p class=MsoNormal style='text-indent:.5in;background:#E6E6E6'><span
style='font-size:8.0pt;font-family:"Courier New"'>}</span><o:p></o:p></p>
<p class=MsoNormal style='text-indent:.5in;background:#E6E6E6'><span
class=GramE><b><span style='font-size:8.0pt;font-family:"Courier New"'>try</span></b></span><span
style='font-size:8.0pt;font-family:"Courier New"'> {</span><o:p></o:p></p>
<p class=MsoNormal style='text-indent:.5in;background:#E6E6E6'><span
style='font-size:8.0pt;font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<span class=SpellE><span class=GramE>result.put</span></span><span class=GramE>(</span>“stuff”,
list);</span><o:p></o:p></p>
<p class=MsoNormal style='text-indent:.5in;background:#E6E6E6'><span
style='font-size:8.0pt;font-family:"Courier New"'>}</span><o:p></o:p></p>
<p class=MsoNormal style='text-indent:.5in;background:#E6E6E6'><span
class=GramE><b><span style='font-size:8.0pt;font-family:"Courier
New"'>catch</span></b></span><span
style='font-size:8.0pt;font-family:"Courier New"'> (Exception e) {</span><o:p></o:p></p>
<p class=MsoNormal style='text-indent:.5in;background:#E6E6E6'><span
style='font-size:8.0pt;font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<span class=SpellE><span class=GramE>System.out.println</span></span><span
class=GramE>(</span>“[<span class=SpellE>SomeClass</span>] An error occurred
putting data into <span class=SpellE>HashTable</span>: ” + <span
class=SpellE>e.getMessage</span>());</span><o:p></o:p></p>
<p class=MsoNormal style='text-indent:.5in;background:#E6E6E6'><span
style='font-size:8.0pt;font-family:"Courier New"'>}</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; }</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; <span class=GramE><b>catch</b></span>
(Exception e {</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=SpellE><span class=GramE>System.out.println</span></span><span
class=GramE>(</span>“[<span class=SpellE>SomeClass</span>] An error occurred in
the method: “ + <span class=SpellE>e.getMessage</span>());</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; }</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; <span class=GramE><b>finally</b></span> {</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=SpellE><span class=GramE>dataAdapter.releaseConnection</span></span><span
class=GramE>(</span><span class=SpellE>conn</span>);</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; }</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>}&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>The above
example is a terrible piece of code.&nbsp; It is inherently inefficient,
represents poor error handling (despite the try/catch blocks) and is very ugly
to look at to say the least.&nbsp; For one, doing a boundary check on </span><span
class=SpellE><span class=GramE><span style='font-size:10.0pt;font-family:"Courier
New"'>dataAdapter.getConnection</span></span></span><span
class=GramE><span style='font-size:10.0pt;font-family:"Courier New"'>(</span></span><span
class=SpellE><span style='font-size:10.0pt;font-family:"Courier
New"'>DataSource.PRIMARY</span></span><span
style='font-size:10.0pt;font-family:"Courier New"'>)</span><span
style='font-size:10.0pt;font-family:Arial'> is pointless, why would you create
a unique boundary for this.&nbsp; This represents poor thinking.&nbsp; Consider
the following example of much more “cleaned up code”.</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><b><span style='font-size:8.0pt;font-family:Arial'>Example
1b:</span></b><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span class=GramE><b><span
style='font-size:8.0pt;font-family:"Courier New"'>public</span></b></span><span
style='font-size:8.0pt;font-family:"Courier New"'> <span class=SpellE>HashTable</span>
<span class=SpellE>doEvent</span>(Event <span class=SpellE>event</span>) { </span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; Connection <span class=SpellE>conn</span> =
<b>null</b>;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; <span class=SpellE>EntityClass</span> <span
class=SpellE>entClass</span> = <b>null</b>;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; <span class=SpellE>ArrayList</span> list =
<b>null</b>;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><b><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; <span class=GramE>try</span></span></b><span
style='font-size:8.0pt;font-family:"Courier New"'> {</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=SpellE><span class=GramE>conn</span></span> = <span
class=SpellE>dataAdapter.getConnection</span>(<span
class=SpellE>DataSource.PRIMARY</span>);</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=SpellE><span class=GramE>entClass</span></span> = new <span
class=SpellE>EntityClass</span>();</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=GramE>list</span> = <span class=SpellE>entClass.list</span>(<span
class=SpellE>conn</span>);</span><o:p></o:p></p>
<p class=MsoNormal style='text-indent:.5in;background:#E6E6E6'><span
class=SpellE><span class=GramE><span style='font-size:8.0pt;font-family:"Courier
New"'>result.put</span></span></span><span
class=GramE><span style='font-size:8.0pt;font-family:"Courier New"'>(</span></span><span
style='font-size:8.0pt;font-family:"Courier New"'>“stuff”, list);</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; }</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; <span class=GramE><b>catch</b></span>
(Exception e {</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=SpellE><span class=GramE>System.out.println</span></span><span
class=GramE>(</span>“[<span class=SpellE>SomeClass</span>] An error occurred in
the method: “ + <span class=SpellE>e.getMessage</span>());</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; }</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; <span class=GramE><b>finally</b></span> {</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=SpellE><span class=GramE>dataAdapter.releaseConnection</span></span><span
class=GramE>(</span><span class=SpellE>conn</span>);</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; }</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp; <span class=GramE><b>return</b></span>
result;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>}&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:8.0pt;
font-family:"Courier New"'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:"Courier
New"'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>The above
method in <i>Example 1b</i> is just as effective as <i>Example 1a</i> at
handling exceptions, and its execution time is much faster.&nbsp; Think
logically, if for example the </span><span class=SpellE><span class=GramE><span
style='font-size:10.0pt;font-family:"Courier
New"'>dataAdapter.getConnection</span></span></span><span
class=GramE><span style='font-size:10.0pt;font-family:"Courier New"'>(</span></span><span
style='font-size:10.0pt;font-family:"Courier New"'>)</span><span
style='font-size:10.0pt;font-family:Arial'> method fails, the </span><span
style='font-size:10.0pt;font-family:"Courier New"'>Exception</span><span
style='font-size:10.0pt;font-family:Arial'> will still be caught by the one
single catch block.&nbsp; Also, you can generally rely on the message coming
from the </span><span class=SpellE><span style='font-size:10.0pt;font-family:
"Courier New"'>ConnectionPoolManager</span></span><span style='font-size:10.0pt;
font-family:Arial'>, and </span><span class=SpellE><span style='font-size:10.0pt;
font-family:"Courier New"'>DataAdapter</span></span><span style='font-size:
10.0pt;font-family:Arial'> to pass an understandable failure message.&nbsp;
</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span class=GramE><span style='font-size:10.0pt;font-family:
Arial'>Lets</span></span><span style='font-size:10.0pt;font-family:Arial'> take
a look at another bad habit:</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><b><span style='font-size:8.0pt;font-family:Arial'>Example
2a:</span></b><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span class=GramE><b><span
style='font-size:10.0pt;font-family:"Courier New"'>try</span></b></span><span
style='font-size:10.0pt;font-family:"Courier New"'> {</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; <span class=GramE><b>try</b></span>
{</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=SpellE><span
class=GramE>compEntity.fetch</span></span><span class=GramE>(</span><span
class=SpellE>conn</span>, <span
class=SpellE>compToolEvent.getComponentId</span>());</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=SpellE>ArrayList</span>
roles = <span class=SpellE><span class=GramE>genRolesEntity.list</span></span><span
class=GramE>(</span><span class=SpellE>conn</span>);</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=SpellE><span
class=GramE>results.put</span></span><span class=GramE>(</span>&quot;roles&quot;,
roles);</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=SpellE><span
class=GramE>results.put</span></span><span class=GramE>(</span>&quot;component&quot;,
<span class=SpellE>compEntity</span>);</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; }</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; <span class=GramE><b>catch</b></span> (<span
class=SpellE>CBException</span> e) {</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=GramE><b>throw</b></span><b>
new</b> <span class=SpellE>CBException</span>(“Error: “ + <span
class=SpellE>e.toString</span>());
</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; }</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; <span class=GramE><b>catch</b></span>
(Exception e) {</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=GramE><b>throw</b></span><b>
new</b> <span class=SpellE>CBException</span>(“Error: “ + <span
class=SpellE>e.toString</span>());</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; }</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; … Hidden Code Here …</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>}</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span class=GramE><b><span
style='font-size:10.0pt;font-family:"Courier New"'>catch</span></b></span><span
style='font-size:10.0pt;font-family:"Courier New"'> (Exception e) { </span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=GramE><b>throw</b></span><b>
new</b> <span class=SpellE>CBException</span>(“Error: “ + <span
class=SpellE>e.toString</span>());</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>}&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>First of
all, if you don’t see a problem in the above block of code then you don’t
understand Exceptions.&nbsp;&nbsp;&nbsp; The above code shows massive
redundancy in the error handling.&nbsp;&nbsp; Let’s say for example that </span><span
class=SpellE><span class=GramE><span style='font-size:10.0pt;font-family:"Courier
New"'>compEntity.fetch</span></span></span><span
class=GramE><span style='font-size:10.0pt;font-family:"Courier New"'>(</span></span><span
style='font-size:10.0pt;font-family:"Courier New"'>) </span><span
style='font-size:10.0pt;font-family:Arial'>throws a </span><span class=SpellE><span
style='font-size:10.0pt;font-family:"Courier New"'>CBException</span></span><span
style='font-size:10.0pt;font-family:Arial'>, this is what happen at
runtime:</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>1.&nbsp; Line:
</span><span class=SpellE><span class=GramE><span style='font-size:10.0pt;
font-family:"Courier New"'>compEntity.fetch</span></span></span><span
class=GramE><span style='font-size:10.0pt;font-family:"Courier New"'>(</span></span><span
class=SpellE><span style='font-size:10.0pt;font-family:"Courier New"'>conn</span></span><span
style='font-size:10.0pt;font-family:"Courier New"'>, <span
class=SpellE>compToolEvent.getComponentId</span>())
</span><span style='font-size:10.0pt;font-family:Arial'>Throws a </span><span
class=SpellE><span style='font-size:10.0pt;font-family:"Courier
New"'>CBException</span></span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>2.&nbsp; </span><span
class=SpellE><span style='font-size:10.0pt;font-family:"Courier
New"'>CBException</span></span><span
style='font-size:10.0pt;font-family:Arial'> is CAUGHT by first catch block.</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>3.&nbsp; A
NEW </span><span class=SpellE><span style='font-size:10.0pt;font-family:"Courier
New"'>CBException</span></span><span
style='font-size:10.0pt;font-family:Arial'> is THROWN.</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>4.&nbsp; </span><span
class=SpellE><span style='font-size:10.0pt;font-family:"Courier
New"'>CBException</span></span><span
style='font-size:10.0pt;font-family:Arial'> is caught in the Exception catch
block at the bottom.</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>5.&nbsp; A
NEW </span><span class=SpellE><span style='font-size:10.0pt;font-family:"Courier
New"'>CBException</span></span><span
style='font-size:10.0pt;font-family:Arial'> is THROWN.</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>So what’s
the problem you ask?&nbsp; There are three big problems, and they are that:
Three <span class=SpellE>CBExceptions</span> are instantiated instead of
one!&nbsp; But what does it matter? A lot actually, this type of boundary
checking is expensive and foolish.&nbsp; Consider this revised code.</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><b><span style='font-size:8.0pt;font-family:Arial'>Example
2b:</span></b><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span class=GramE><b><span
style='font-size:10.0pt;font-family:"Courier New"'>try</span></b></span><span
style='font-size:10.0pt;font-family:"Courier New"'> {</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; <span class=GramE><b>try</b></span>
{</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=SpellE><span
class=GramE>compEntity.fetch</span></span><span class=GramE>(</span><span
class=SpellE>conn</span>, <span
class=SpellE>compToolEvent.getComponentId</span>());</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=SpellE>ArrayList</span>
roles = <span class=SpellE><span class=GramE>genRolesEntity.list</span></span><span
class=GramE>(</span><span class=SpellE>conn</span>);</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=SpellE><span
class=GramE>results.put</span></span><span class=GramE>(</span>&quot;roles&quot;,
roles);</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=SpellE><span
class=GramE>results.put</span></span><span class=GramE>(</span>&quot;component&quot;,
<span class=SpellE>compEntity</span>);</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=GramE>return</span>
results;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; }</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; <span class=GramE><b>catch</b></span> (<span
class=SpellE>CBException</span> e) {</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=GramE><b>throw</b></span><b>
e;</b></span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; }</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; <span class=GramE><b>catch</b></span>
(Exception e) {</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=GramE><b>throw</b></span><b>
e</b>;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; }</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; … Hidden Code Here …</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>}</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span class=GramE><b><span
style='font-size:10.0pt;font-family:"Courier New"'>catch</span></b></span><span
style='font-size:10.0pt;font-family:"Courier New"'> (<span class=SpellE>CBException</span>
e) {</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=GramE><b>throw</b></span>
e;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>}</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span class=GramE><b><span
style='font-size:10.0pt;font-family:"Courier New"'>catch</span></b></span><span
style='font-size:10.0pt;font-family:"Courier New"'> (Exception e) { </span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=GramE><b>throw</b></span><b>
new</b> <span class=SpellE>CBException</span>(“Error: “ + <span
class=SpellE>e.toString</span>());</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>}&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>The above
example makes much more sense.&nbsp; When we catch a </span><span class=SpellE><span
style='font-size:10.0pt;font-family:"Courier New"'>CBException</span></span><span
style='font-size:10.0pt;font-family:Arial'>, we just throw the existing </span><span
class=SpellE><span style='font-size:10.0pt;font-family:"Courier
New"'>CBException</span></span><span
style='font-size:10.0pt;font-family:Arial'> instance which is caught again and
thrown to the higher level.&nbsp; In this case we only create one </span><span
style='font-size:10.0pt;font-family:"Courier New"'>Exception</span><span
style='font-size:10.0pt;font-family:Arial'> object.&nbsp; &nbsp;The above
example is once again also inherently redundant anyways, and can be even
further compressed into the following example (remembering the discussion
earlier):</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><b><span style='font-size:8.0pt;font-family:Arial'>Example
2c:</span></b><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span class=GramE><b><span
style='font-size:10.0pt;font-family:"Courier New"'>try</span></b></span><span
style='font-size:10.0pt;font-family:"Courier New"'> {</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; <span class=SpellE><span
class=GramE>compEntity.fetch</span></span><span
class=GramE>(</span><span class=SpellE>conn</span>, <span
class=SpellE>compToolEvent.getComponentId</span>());</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; <span class=SpellE>ArrayList</span>
roles = <span class=SpellE><span class=GramE>genRolesEntity.list</span></span><span
class=GramE>(</span><span class=SpellE>conn</span>);</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; <span class=SpellE><span
class=GramE>results.put</span></span><span
class=GramE>(</span>&quot;roles&quot;, roles);</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; <span class=SpellE><span
class=GramE>results.put</span></span><span
class=GramE>(</span>&quot;component&quot;, <span
class=SpellE>compEntity</span>);</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; <span class=GramE>return</span>
results;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; … Hidden Code Here …</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>}</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span class=GramE><b><span
style='font-size:10.0pt;font-family:"Courier New"'>catch</span></b></span><span
style='font-size:10.0pt;font-family:"Courier New"'> (<span class=SpellE>CBException</span>
e) {</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; <span class=GramE><b>throw</b></span>
e;</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>}</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span class=GramE><b><span
style='font-size:10.0pt;font-family:"Courier New"'>catch</span></b></span><span
style='font-size:10.0pt;font-family:"Courier New"'> (Exception e) { </span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>&nbsp;&nbsp; <span class=GramE><b>throw</b></span><b>
new</b> <span class=SpellE>CBException</span>(“Error: “ + <span
class=SpellE>e.toString</span>());</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:"Courier New"'>}&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span><o:p></o:p></p>
<p class=MsoNormal style='background:#E6E6E6'><span style='font-size:10.0pt;
font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>That’s more
like it.&nbsp; But it could still be better, but that can wait until a later
article.</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:16.0pt;font-family:Arial'>Final
Words</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>&nbsp;</span><o:p></o:p></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Arial'>To
re-iterate, don’t use excessive try/catch blocks.&nbsp; Plan more carefully,
and also take advantage of stacked catches to encapsulate code rather than
creating many protected areas.&nbsp;&nbsp; Performance is a very important.</span><o:p></o:p></p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
</div>
</body>
</html>
```

