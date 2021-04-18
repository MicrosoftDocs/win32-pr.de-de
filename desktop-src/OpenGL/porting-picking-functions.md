---
title: Portieren von Pick-Funktionen
description: Alle IRIS GL-Pick-Funktionen verfügen über OpenGL-Entsprechungen, mit Ausnahme von clearhitcode. In der folgenden Tabelle werden die Funktionen von IRIS GL Picking und ihre entsprechenden OpenGL-Funktionen aufgelistet.
ms.assetid: f8fbd0c2-14bf-47bc-be7f-eeef346dbac1
keywords:
- IRIS GL Porting, Picking
- Portieren von IRIS GL, auswählen
- Portieren auf OpenGL von IRIS GL, auswählen
- OpenGL-Portierung von IRIS GL, Auswahl
- Pick
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4c0ea6011860f7d5010dd0bb7d5d23b671d99a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339003"
---
# <a name="porting-picking-functions"></a>Portieren von Pick-Funktionen

Alle IRIS GL-Pick-Funktionen verfügen über OpenGL-Entsprechungen, mit Ausnahme von **clearhitcode**. In der folgenden Tabelle werden die Funktionen von IRIS GL Picking und ihre entsprechenden OpenGL-Funktionen aufgelistet.



| IRIS GL-Funktion                | OpenGL-Funktion                                                                           | Bedeutung                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| **clearhitcode**                | Wird nicht unterstützt.                                                                            | Löscht die globale Variable und den hitcode.    |
| **pickselect**<br/>       | [**glrendermode**](glrendermode.md) (GL \_ Select)                                       | Wechselt zum Auswahl-oder Pick-Modus. |
| **endpickendselect**<br/> | [**glrendermode**](glrendermode.md) (GL- \_ Rendering)                                       | Wechselt in den Renderingmodus.            |
| **picksize**                    | [**glupickmatrix**](glupickmatrix.md)-[**glselectbuffer**](glselectbuffer.md)<br/> | Legt das Rückgabe Array fest.                 |
| **initnames**                   | [**glinitnames**](glinitnames.md)                                                        |                                        |
| **pushnamepopname**<br/>  | [**glpushname**](glpushname.md)([**glpopname** )](glpopname.md)<br/>                 |                                        |
| **loadname**                    | [**glloadname**](glloadname.md)                                                          |                                        |



 

Weitere Informationen zum Auswählen von finden Sie unter [**glupickmatrix**](glupickmatrix.md).

 

 





