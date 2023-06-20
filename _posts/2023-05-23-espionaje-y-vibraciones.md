---
layout: post
title: "Conozco tu PIN: sobre altavoces, acelerómetros y formas creativas de espiar"
date: "2023-05-23 15:00:00 +0000"
category: seguridad
tags:
- seguridad
- teléfono
- acelerómetro
- espionaje
- ataques
imagefeature: 'https://live.staticflickr.com/4802/40040528114_3d9092657f.jpg'
---
<a href="https://www.flickr.com/photos/fernand0/40040528114/" title="Teléfono "><img src="https://live.staticflickr.com/4802/40040528114_3d9092657f.jpg" alt="Teléfono " class="img-responsive img-centered"></a>

Otra forma curiosa de espionaje: [EarSpy: Spying on Phone Calls via Ear Speaker Vibrations Captured by Accelerometer](https://www.securityweek.com/earspy-spying-phone-calls-ear-speaker-vibrations-captured-accelerometer/). 

Investigadores de Texas A&M University, Temple University, New Jersey Institute of Technology, Rutgers University, y la University of Dayton han publiado un artículo ([[PDF] EarSpy: Spying Caller Speech and Identity through Tiny Vibrations of Smartphone Ear Speakers](https://arxiv.org/pdf/2212.12151.pdf)) donde proponen observar el altavoz que se pone en el oído y el acelerómetro del terminal para capturar las vibraciones y espiarnos.

> EarSpy relies on the phone’s ear speaker — the speaker at the top of the device that is used when the phone is held to the ear — and the device’s built-in accelerometer for capturing the tiny vibrations generated by the speaker. 

Ya había propuestas basadas en los altavoces del teléfono, pero la novedad aquí parece ser que no es necesario recurrir a elementos externos para realizar el espionaje. Sin olvidar que cada vez es más complicado en Android obtener los permisos necesarios para realizar otros ataques, para otros ataques más obvios (grabar la conversación del teléfono directamente).

Porque parece que obtener los datos de los sensores de movimiento del teléfono no necesita ningún permiso especial.

> On the other hand, accessing raw data from the motion sensors in a smartphone does not require any special permissions. Android developers have started placing some restrictions on sensor data collection, but the EarSpy attack is still possible, the researchers said.

Sí que haría falta, claro, algún tipo de programa (*malware*) que hiciese este trabajo.

Todo se basa en que estos altavoces para escuchar las llamadas son cada vez mejores (incluso los hay que son estéreo).

Entre los resultados, se puede distinguir el género con un 98% de precisión, y la identidad con hasta un 92%.

> In the gender recognition test, whose goal is to determine whether the target is male or female, the EarSpy attack had a 98% accuracy. The accuracy was nearly as high, at 92%, for detecting the speaker’s identity. 

En cuanto a la posibilidad de escuchar la conversación la precisión se reduce  a un 52% para reconocer dígitos en una conversación.

> When it comes to actual speech, the accuracy was up to 56% for capturing digits spoken in a phone call. 

Puede parecer poco, pero multiplica por 5 la prueba de valores de modo aleatorio.

Curioso.

> 