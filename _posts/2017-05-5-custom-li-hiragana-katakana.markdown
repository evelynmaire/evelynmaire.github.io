---
layout: post
title:  "Custom li in Hiragana and Katakana"
date:   2017-04-24 23:32:51 +1200
categories: japanese
---
On a whole bunch of fansites, I kept seeing people being using hiragana and katakana on their ordered lists. I really wanted to try this! But I had no idea how. With some Google-fu, I found a page and I thought I’d share how it works here with some added cultural info.

Note: So far I’ve found this works in Safari, Chrome and Firefox, but not IE.

So you know how an ordered list works, right?
You add <code class="language-markup">&lt;ul&gt;</code> and then add <code class="language-markup">&lt;li&gt;</code> for each item on the list.

So for example, this:
<pre><code class="language-markup">&lt;ul&gt;
 &lt;li&gt;List item 1&lt;/li&gt;
 &lt;li&gt;List item 2&lt;/li&gt;
 &lt;li&gt;List item 3&lt;/li&gt;
&lt;/ul&gt;</code></pre>

Creates:
<ul>
<li>List item 1</li>
<li>List item 2</li>
<li>List item 3</li>
</ul>

What we want to do is have the japanese <ruby>あ<rp>(</rp><rt>a</rt><rp>)</rp>い<rp>(</rp><rt>i</rt><rp>)</rp>う<rp>(</rp><rt>u</rt><rp>)</rp>え<rp>(</rp><rt>e</rt><rp>)</rp>お<rp>(</rp><rt>o</rt><rp>)</rp></ruby>　or <ruby>ア<rp>(</rp><rt>a</rt><rp>)</rp>イ<rp>(</rp><rt>i</rt><rp>)</rp>ウ<rp>(</rp><rt>u</rt><rp>)</rp>エ<rp>(</rp><rt>e</rt><rp>)</rp>オ<rp>(</rp><rt>o</rt><rp>)</rp></ruby> replace those numbers. This modern ordering of the characters is called the <ruby>五<rp>(</rp><rt>go</rt><rp>)</rp>十<rp>(</rp><rt>jyuu</rt><rp>)</rp>音<rp>(</rp><rt>on</rt><rp>)</rp></ruby>, or <em>fifty sounds</em>

One way is to attach the style tag directly to the <code class="language-markup">&lt;ul&gt;</code> tag.
Simply write <code class="language-markup">&lt;ul style="list-style-type:hiragana;"&gt;</code> for the hiragana and <code class="language-markup">&lt;ul style="list-style-type:katakana;"&gt;</code> for katakana.

Hiragana:
<ul style="list-style-type:hiragana;">
<li>Usagi</li>
<li>Rei</li>
<li>Ami</li>
<li>Minako</li>
<li>Makoto</li>
</ul>

Katakana:
<ul style="list-style-type:katakana;">
<li>Chibi-Usa</li>
<li>Setsuna</li>
<li>Haruka</li>
<li>Michiru</li>
<li>Hotaru</li>
</ul>

But wait! There’s more!

Another cute trick I haven’t seen before, was using the <ruby>い<rp>(</rp><rt>i</rt><rp>)</rp>ろ<rp>(</rp><rt>ro</rt><rp>)</rp>は<rp>(</rp><rt>ha</rt><rp>)</rp></ruby> system instead.
For those of you who don’t know, iroha is an ancient poem used in Japan similar to the English <em>the quick brown fox jumped over the lazy dog</em>… it uses every character in the Japanese syllabary.

Because the poem is old (c.794-1179), some defunct hiragana are also represented, which has been changed for modern usage. However, the poem is still well-known and is used for functions like numbered seating in a theatre and notes of an octave.

To add the iroha version instead of the above gojyuuon, instead add <code class="language-markup">&lt;ul style="list-style-type:hiragana-iroha;"&gt;</code> for the hiragana and <code class="language-markup">&lt;ul style="list-style-type:katakana-iroha;"&gt;</code> for katakana.

<ul style="list-style-type:hiragana-iroha;">
<li>Usagi</li>
<li>Rei</li>
<li>Ami</li>
<li>Minako</li>
<li>Makoto</li>
</ul>

<ul style="list-style-type:katakana-iroha;">
<li>Chibi-Usa</li>
<li>Setsuna</li>
<li>Haruka</li>
<li>Michiru</li>
<li>Hotaru</li>
</ul>

See? Easy!

(bonus points if you noticed the katakana for “ho” ホ was right next to Hotaru)

But what if (like me) you’re lazy and don’t want that extra code cluttering up your page every time? You can add it to your CSS file.

<pre><code class="language-css">ol, ul {
 list-style: hiragana;
}</code></pre>

Just replace hiragana with whatever you want; <code class="language-markup">hiragana</code>, <code class="language-markup">katakana</code>, <code class="language-markup">hiragana-iroha</code> or <code class="language-markup">katakana-iroha</code>.
