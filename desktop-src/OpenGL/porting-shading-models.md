---
title: Portieren von Schattierungsmodellen
description: Wie IRIS GL können Sie mit OpenGL zwischen smooth (Gouraud)-Schattierung und flacher Schattierung wechseln. In der folgenden Tabelle sind die IRIS GL-Schattierungs- und Ditheringfunktionen sowie die entsprechenden OpenGL-Funktionen aufgeführt.
ms.assetid: 93e8f437-381f-4620-ad6f-52ce830d99b6
keywords:
- IRIS GL-Portierung, Schattierung
- Portieren von IRIS GL,Schattierung
- Portieren von IRIS GL zu OpenGL, Schattierung
- OpenGL-Portierung über IRIS GL,Schattierung
- Smooth Shading
- Gouraud-Schattierung
- Flache Schattierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee4265341e17843dbe4752bb51e5728aa54914ec5670c08b6b7921537050a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012038"
---
# <a name="porting-shading-models"></a>Portieren von Schattierungsmodellen

Wie IRIS GL können Sie mit OpenGL zwischen smooth (Gouraud)-Schattierung und flacher Schattierung wechseln. In der folgenden Tabelle sind die IRIS GL-Schattierungs- und Ditheringfunktionen sowie die entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion                                   | OpenGL-Funktion                                                                                    | Bedeutung                      |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------|
| **shademodel**(FLAT)                               | [**glShadeModel**](glshademodel.md) ( GL \_ FLAT )                                                  | Führt flache Schattierung durch.           |
| **shademodel**(GOURAUD)                            | **glShadeModel**( GL \_ SMOOTH )                                                                     | Führt eine reibungslose Schattierung durch.         |
| **getsm**                                          | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ SHADE \_ MODEL )      | Gibt das aktuelle Schattierungsmodell zurück. |
| **dither**(DT \_ ON) **dither**(DT \_ OFF) <br/> | [**glEnable**](glenable.md) ( GL \_ DITHER )[**glDisable**](gldisable.md)( GL \_ DITHER )<br/> | Schaltet das Dithering ein/aus.      |



 

??

 

 





