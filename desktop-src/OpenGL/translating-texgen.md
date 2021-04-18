---
title: Übersetzen von TEXGEN
description: Die Iris GL-Funktion TEXGEN wird in gltexgen für OpenGL übersetzt.
ms.assetid: ddf398ed-37d4-4fb6-97be-20fe0564cb77
keywords:
- IRIS GL portieren, Textur
- Portieren von IRIS GL, Textur
- Portieren auf OpenGL von IRIS GL, Texture
- OpenGL-Portierung von IRIS GL, Textur
- Struktur
- IRIS GL portieren, TEXGEN
- Portieren von IRIS GL, TEXGEN
- Portieren auf OpenGL von IRIS GL, TEXGEN
- OpenGL-Portierung von IRIS GL, TEXGEN
- TEXGEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07654fc35e20096ed71c3fe74ff9279214eb45c8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337612"
---
# <a name="translating-texgen"></a>Übersetzen von TEXGEN

Die Iris GL-Funktion **TEXGEN** wird in [gltexgen](gltexgen-functions.md) für OpenGL übersetzt.

Bei Iris GL wird **TEXGEN** zweimal aufgerufen: einmal, um den Modus und die ebenengleichung gleichzeitig festzulegen, und einmal, um die Generierung der Textur Koordinate zu aktivieren. Beispiel:


```C++
texgen(TX_S, TG_LINEAR, planeParams); 
texgen(TX_S, TG_ON, NULL);
```



Mit OpenGL führen Sie drei Aufrufe aus: zwei bis zu **gltexgen** (einmal, um den Modus festzulegen, und einmal, um die Ebene der Ebene festzulegen) und einen zu [**glEnable**](glenable.md). Beispielsweise ist der OpenGL-Code, der dem obigen IRIS GL-Code entspricht,:


```C++
glTexGen(GL_S, GLTEXTURE_GEN_MODE, modeName); 
glTextGen(GL_S, GL_OBJECT_PLANE, planeParameters); 
glEnable(GL_TEXTURE_GEN_S);
```



In der folgenden Tabelle werden die Namen der Iris GL-Texturkoordinaten und deren OpenGL-Entsprechungen aufgelistet.



| IRIS GL-Textur Koordinate | OpenGL-Textur Koordinate | glEnable-Argument   |
|----------------------------|---------------------------|---------------------|
| TX \_ S                      | GL \_ S                     | GL- \_ Textur \_ gen \_ S |
| TX \_ T                      | GL \_ T                     | GL \_ Textur \_ gen \_ T |
| TX \_ R                      | GL \_ .                     | GL \_ Textur \_ gen \_ R |
| TX \_ Q                      | GL. \_ f                     | GL \_ Textur \_ gen, \_ Q |



 

In der folgenden Tabelle sind die Formen der Iris GL-Textur Generierung und ihre entsprechenden OpenGL-Textur Modi und-Namen aufgelistet.



| IRIS GL-Textur Modus | OpenGL-Textur Modus | OpenGL-Ebenenname |
|----------------------|---------------------|-------------------|
| TG \_ linear           | GL- \_ Objekt \_ linear  | GL- \_ Objekt \_ Ebene |
| TG- \_ Kontur          | GL- \_ Eye \_ linear     | GL- \_ Augen \_ Ebene    |
| \_spheremap von TG        | GL- \_ Kugel \_ Karte     |                   |



 

 

 




