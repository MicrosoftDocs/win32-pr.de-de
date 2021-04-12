---
title: Portieren von Schattierungs Modellen
description: Wie IRIS GL ermöglicht OpenGL den Wechsel zwischen Smooth (Gouraud) Schattierung und flacher Schattierung. In der folgenden Tabelle werden die Funktionen zum Schattieren und Dithering von IRIS GL sowie die entsprechenden OpenGL-Funktionen aufgelistet.
ms.assetid: 93e8f437-381f-4620-ad6f-52ce830d99b6
keywords:
- IRIS GL portieren, Schattierung
- Portieren von IRIS GL, Schattierung
- Portieren auf OpenGL von IRIS GL, Schattierung
- OpenGL-Portierung von IRIS GL, Schattierung
- Smooth-Schattierung
- Gouraud-Schattierung
- flatschattierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124bb002f6f133b4d47dd40e1a0e8738c512ce99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310543"
---
# <a name="porting-shading-models"></a>Portieren von Schattierungs Modellen

Wie IRIS GL ermöglicht OpenGL den Wechsel zwischen Smooth (Gouraud) Schattierung und flacher Schattierung. In der folgenden Tabelle werden die Funktionen zum Schattieren und Dithering von IRIS GL sowie die entsprechenden OpenGL-Funktionen aufgelistet.



| IRIS GL-Funktion                                   | OpenGL-Funktion                                                                                    | Bedeutung                      |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------|
| **shademodel**(flach)                               | [**glshademodel**](glshademodel.md) (GL \_ Flat)                                                  | Führt eine flache Schattierung durch.           |
| **shademodel**(Gouraud)                            | **glshademodel**(GL \_ Smooth)                                                                     | Führt eine Smooth-Schattierung durch.         |
| **ge-m**                                          | [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL- \_ Schattierung- \_ Modell)      | Gibt das aktuelle Farbton Modell zurück. |
| **Dithering**(dt \_ on) **Dithering**(dt \_ Off) <br/> | [**glEnable**](glenable.md) (GL \_ Dither)[**gldeaktiviert**](gldisable.md)(GL \_ Dither)<br/> | Schaltet die Dithering ein/aus.      |



 

??

 

 





