---
title: Übersetzen von tevdef
description: Das folgende Codebeispiel ist eine IRIS GL-Textur-Umgebungs Definition, die den \_ Parameter "TV Decal Texture-Environment" angibt.
ms.assetid: bb4c8231-8102-4ecb-a5d2-c41243c2682d
keywords:
- IRIS GL portieren, Textur
- Portieren von IRIS GL, Textur
- Portieren auf OpenGL von IRIS GL, Texture
- OpenGL-Portierung von IRIS GL, Textur
- Struktur
- IRIS GL Porting, tevdef
- Portieren von IRIS GL, tevdef
- Portieren auf OpenGL von IRIS GL, tevdef
- OpenGL-Portierung von IRIS GL, tevdef
- tevdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac2610d1467adb6faa1ea105fc8e8734bfb9c4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948032"
---
# <a name="translating-tevdef"></a>Übersetzen von tevdef

Das folgende Codebeispiel ist eine IRIS GL-Textur-Umgebungs Definition, die den \_ Parameter "TV-Decal Texture-Environment" angibt:


```C++
float tevprops[] = {TV_DECAL, TV_NULL}; 
 
tevdef(1, 0, tevprops);
```



und der gleiche Code, der in OpenGL übersetzt wurde:


```C++
glTexEnvfv(GL_TEXTURE_ENV, GL_TEXTURE_ENV_MODE, GL_DECAL);
```



In der folgenden Tabelle werden die Parameter der Iris GL-Textur Umgebung und ihre entsprechenden OpenGL-Parameter aufgelistet.



| IRIS GL-Parameter     | OpenGL-Parameter             |
|-----------------------|------------------------------|
| TV- \_ modulate          | GL \_ modulate                 |
| TV \_ -Debug             | GL \_ -Debug                    |
| TV- \_ Blend             | GL \_ Blend                    |
| TV- \_ Farbe             | GL- \_ Textur Gesamt \_ \_ Farbe      |
| TV- \_ Alpha             | Keine direkte OpenGL-Entsprechung. |
| TV- \_ Komponente \_ auswählen | Keine direkte OpenGL-Entsprechung. |



 

Weitere Informationen zu Textur Umgebungs Parametern finden Sie unter [**gltextev**](gltexenv-functions.md).

 

 




