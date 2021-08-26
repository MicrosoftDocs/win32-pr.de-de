---
title: Übersetzen von tevdef
description: Das folgende Codebeispiel ist eine IRIS GL-Texturumgebungsdefinition, die den Texturumgebungsparameter \_ TV DECAL angibt.
ms.assetid: bb4c8231-8102-4ecb-a5d2-c41243c2682d
keywords:
- IRIS GL-Portierung, Textur
- Portieren von IRIS GL, Textur
- Portieren von IRIS GL zu OpenGL, Textur
- OpenGL-Portierung aus IRIS GL,Textur
- Struktur
- IRIS GL-Portierung, tevdef
- Portieren von IRIS GL,tevdef
- Portieren von IRIS GL,tevdef zu OpenGL
- OpenGL-Portierung von IRIS GL,tevdef
- tevdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7feef33c2aa725c6e5bb91782fe43fdc6a84d23db8aa412f02c07b6ec588f719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887880"
---
# <a name="translating-tevdef"></a>Übersetzen von tevdef

Das folgende Codebeispiel ist eine IRIS GL-Texturumgebungsdefinition, die den Texturumgebungsparameter \_ TV DECAL angibt:


```C++
float tevprops[] = {TV_DECAL, TV_NULL}; 
 
tevdef(1, 0, tevprops);
```



und den gleichen Code, der in OpenGL übersetzt wurde:


```C++
glTexEnvfv(GL_TEXTURE_ENV, GL_TEXTURE_ENV_MODE, GL_DECAL);
```



In der folgenden Tabelle sind die IRIS GL-Texturumgebungsparameter und die entsprechenden OpenGL-Parameter aufgeführt.



| IRIS GL-Parameter     | OpenGL-Parameter             |
|-----------------------|------------------------------|
| TV \_ MODULATE          | GL \_ MODULATE                 |
| TV \_ DECAL             | GL \_ DECAL                    |
| TV \_ BLEND             | GL \_ BLEND                    |
| \_TV-FARBE             | GL \_ TEXTURE \_ ENV \_ COLOR      |
| TV \_ ALPHA             | Keine direkte OpenGL-Entsprechung. |
| TV \_ COMPONENT \_ SELECT | Keine direkte OpenGL-Entsprechung. |



 

Weitere Informationen zu Texturumgebungsparametern finden Sie unter [**glTexEnv**](gltexenv-functions.md).

 

 




