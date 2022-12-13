---
layout: post
title: "Sobre inclusión más segura de contenidos con iframes"
date: "Fri Jan 08 10:45:01 +0100 2016"
category: seguridad
tags: [seguridad, sandbox, iframe, html5, inclusión, marcos, contenido]
---




<a href="https://plus.google.com/u/1/photos/photo/112862240851570159916/6237348164241243442" title="Enmarcado"><img src="https://lh3.googleusercontent.com/Ai47q5eskdaVA1b9na4nXbhDp7LzgN10AUE1pMuIanfkyeC4wDxCM5OH15jyuNDZcZrF=w1680-h1050-no" width="240"  alt="Enmarcado" style="float:left; margin:5px"></a>
La utilización de *frames* es vieja en la red: permite incluir contenido de otros sitios en nuestra página y es un mecanismo que algunos servicios ofrecen como el habitual para este cometido. 

> Nowadays, old-school (Netscape style) frames have fallen out of fashion, but iframes are more popular than ever. They’re used for advertising, social plugins (e.g. Facebook “like” buttons and “Share on Twitter” functionality), webpage widgets, and so on.

En [You've Been Framed!  A survey of iframes and the sandbox attribute](http://www.debug.is/2015/04/15/youve-been-framed/) se comenta sobre estas técnicas y su prevalencia, así como el atributo *sandbox*, que permite controlar políticas de seguridad sobre contenido incrustado en nuestra web:

> Just how popular are iframes? Not all websites have them but those that do tend to have quite a lot. To find out, I recently crawled the top ranking sites on the web and counted the iframes. Most iframes are dynamically generated by javascript, so you need to use a crawler which evaluates js. I wrote about the method I used in a follow-up post.

> 72% of the Alexa top 5000 sites have iframes on their landing pages. Of those, each has on average 7.1 iframes. Some sites have well over 50 frames.

> Of all these 25,849 iframes on the top 5000 sites, only 10 use the HTML5 sandbox security attribute. That’s a whopping 0.04%! We’ll learn more about this attribute in a bit.

> Examining the top 50 sites, there are a lot fewer iframes. But no one is using the aforementioned sandbox attribute. Of the top 1000, only two sites employ it.

Los riesgos son, esencialmente, que alguien saque partido de estar en nuestra página web al estar integrando contenido que está fuera de nuestro control:

>  However, external content is completely beyond your control. It can control the browser and the user experience to a degree. Unrestricted iframes can run javascript, Flash and other plugins, open pop-up windows, and even navigate from the containing page. If the site is just intended to display an ad or social button, does it really need to be able to do all (or even any) of these things?

En sitios de perfil alto esto no debería ser un problema (pero mejor no fiarse) pero nunca sabemos lo que puede pasar con otros sitios: esos botones tan chulos que proporcionaba alguien y que, en algún momento, no puede seguir con el servicio, abandona el dominio y es utilizado por otra persona.

En [Play safely in sandboxed IFrames](http://www.html5rocks.com/en/tutorials/security/sandboxed-iframes/) se habla  un poco más del marco general (principios básicos de seguridad, mínimo privilegio y compartimentalización) y se explica la forma de incluir *iframes* de forma más segura:

> The sandbox attribute of the iframe element gives us just what we need to tighten the restrictions on framed content. We can instruct the browser to load a specific frame’s content in a low-privilege environment, allowing only the subset of capabilities necessary to do whatever work needs doing.