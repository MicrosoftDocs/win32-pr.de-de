---
title: Portieren von Auswahlfunktionen
description: Alle IRIS GL-Auswahlfunktionen verfügen über OpenGL-Entsprechungen, mit Ausnahme von clearhitcode. In der folgenden Tabelle sind die IRIS GL-Auswahlfunktionen und die entsprechenden OpenGL-Funktionen aufgeführt.
ms.assetid: f8fbd0c2-14bf-47bc-be7f-eeef346dbac1
keywords:
- IRIS GL-Portierung, Auswählen
- Portieren von IRIS GL, Auswählen
- Portieren von IRIS GL zu OpenGL, Auswählen
- OpenGL-Portierung von IRIS GL,Auswählen
- Kommissionierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be2cbeed54a18e7f1d3f26ec01dca2ad352aa4e190fbdc667ed75a60badec29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034810"
---
# <a name="porting-picking-functions"></a>Portieren von Auswahlfunktionen

Alle IRIS GL-Auswahlfunktionen verfügen über OpenGL-Entsprechungen, mit Ausnahme von **clearhitcode**. In der folgenden Tabelle sind die IRIS GL-Auswahlfunktionen und die entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion                | OpenGL-Funktion                                                                           | Bedeutung                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| **clearhitcode**                | Wird nicht unterstützt.                                                                            | Löscht die globale Variable und den Hitcode.    |
| **pickselect**<br/>       | [**glRenderMode**](glrendermode.md) ( GL \_ SELECT )                                       | Wechselt zum Auswahl- oder Auswahlmodus. |
| **endpickendselect**<br/> | [**glRenderMode**](glrendermode.md) ( GL \_ RENDER )                                       | Wechselt in den Renderingmodus.            |
| **picksize**                    | [**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)<br/> | Legt das Rückgabearray fest.                 |
| **initnames**                   | [**glInitNames**](glinitnames.md)                                                        |                                        |
| **pushnamepopname**<br/>  | [**glPushName**](glpushname.md)[**glPopName**](glpopname.md)<br/>                 |                                        |
| **loadname**                    | [**glLoadName**](glloadname.md)                                                          |                                        |



 

Weitere Informationen zur Auswahl finden Sie unter [**gluPickMatrix**](glupickmatrix.md).

 

 





