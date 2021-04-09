---
title: Übersetzen von texdef
description: Das folgende Codebeispiel ist eine IRIS GL-Textur Definition.
ms.assetid: bb2d257d-ee74-4a65-b364-c7a97bccaa78
keywords:
- IRIS GL portieren, Textur
- Portieren von IRIS GL, Textur
- Portieren auf OpenGL von IRIS GL, Texture
- OpenGL-Portierung von IRIS GL, Textur
- Struktur
- IRIS GL Porting, texdef
- Portieren von IRIS GL, texdef
- Portieren auf OpenGL von IRIS GL, texdef
- OpenGL-Portierung von IRIS GL, texdef
- texdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479af06bcfd3a50daf56fb0629e4c32f24750081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856811"
---
# <a name="translating-texdef"></a>Übersetzen von texdef

Das folgende Codebeispiel ist eine IRIS GL-Textur Definition:


```C++
float texprops[] = { TX_MINFILTER, TX_POINT, 
                         TX_MAGFILTER, TX_POINT, 
                         TX_WRAP_S, TX_REPEAT, 
                         TX_WRAP_T, TX_REPEAT, 
                         TX_NULL }; 
 
textdef2d(1, 1, 6, 6, granite_texture, 7, texprops);
```



Im vorherigen Beispiel gibt **texdef** den TX \_ -Punkt Filter sowohl als Vergrößerungs-als auch als Minimierungs Mechanismus an \_ . Außerdem wird das Textur Bild angegeben: **Granit \_ Textur**.

In OpenGL gibt [**glteximage**](glteximage1d.md) das Image an, und [gltexparameter](gltexparameter-functions.md) legt die-Eigenschaft fest. Um IRIS GL-Textur Definitionen zu übersetzen, ersetzen Sie die **textdef** -Funktion durch **glteximage** und einen oder mehrere Aufrufe von **gltexparameter**.

Der obige IRIS GL-Code sieht wie folgt aus, wenn er in OpenGL übersetzt wird:


```C++
GLfloat nearest[] = {GL_NEAREST}; 
GLfloat repeat = {GL_REPEAT}; 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MIN_FILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MAGILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_S, repeat); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_T, nearest); 
glTexImage1D( GL_TEXTURE_1D, 0, 1, 6, 0, GL_RGB, GL_UNSIGNED_SHORT, granite_texture);
```



In der folgenden Tabelle sind die Iris GL-Textur Parameter und ihre entsprechenden OpenGL-Parameter aufgelistet.



| IRIS GL-Textur Parameter | OpenGL-Textur Parameter                                  |
|---------------------------|-----------------------------------------------------------|
| TX \_ MinFilter             | GL- \_ Textur- \_ Min- \_ Filter                                  |
| TX- \_ MagFilter             | GL- \_ Textur- \_ mag- \_ Filter                                  |
| TX \_ Wrap, TX \_ Wrap \_ S     | GL- \_ Textur Umbruch \_ \_ S                                      |
| TX \_ Wrap, TX \_ Wrap \_ T     | Rahmenfarbe für GL- \_ Textur Umbruch \_ \_ TGL- \_ Textur \_ \_ Umbruch<br/> |



 

In der folgenden Tabelle sind die möglichen Werte der Iris GL-Textur Parameter und ihre entsprechenden OpenGL-Parameter aufgelistet.



| IRIS GL-Textur Parameter | OpenGL-Textur Parameter     |
|---------------------------|------------------------------|
| TX- \_ Punkt                 | GL am \_ nächsten                  |
| TX \_ Bilinear              | GL \_ linear                   |
| TX- \_ MipMap- \_ Punkt         | nächste \_ nächste \_ MipMap \_ am nächsten |
| TX \_ MipMap \_ Bilinear      | GL \_ lineare \_ MipMap am \_ nächsten  |
| TX \_ MipMap \_ linear        | \_nächste nächste \_ MipMap ( \_ linear)  |
| TX- \_ drei-linear             | GL \_ lineare \_ MipMap \_ linear   |



 

 

 





