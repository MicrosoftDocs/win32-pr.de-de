---
title: Portieren von Mischungs Code
description: Wenn Sie in IRIS gl auf den vorderen und den Hintergrund Puffer zeichnen, wird der Mischungs Vorgang durch das Lesen eines der Puffer, das Kombination mit dieser Farbe und das anschließende Schreiben des Ergebnisses in beide Puffer erfolgt. In OpenGL wird jeder Puffer jedoch nacheinander gelesen, gemischt und dann geschrieben.
ms.assetid: 18334c6b-586d-44a3-aa95-d10589ba99f4
keywords:
- IRIS GL portieren, mischen
- Portieren von IRIS GL, Blending
- Portieren auf OpenGL von IRIS GL, Blending
- OpenGL-Portierung von IRIS GL, Blending
- Mischen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7956c675848f454b660126a7a17869295a827438
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338612"
---
# <a name="porting-blending-code"></a>Portieren von Mischungs Code

Wenn Sie in IRIS gl auf den vorderen und den Hintergrund Puffer zeichnen, wird der Mischungs Vorgang durch das Lesen eines der Puffer, das Kombination mit dieser Farbe und das anschließende Schreiben des Ergebnisses in beide Puffer erfolgt. In OpenGL wird jeder Puffer jedoch nacheinander gelesen, gemischt und dann geschrieben.

In der folgenden Tabelle werden die Mischungs Funktionen von IRIS GL und ihre entsprechenden OpenGL-Funktionen aufgelistet.



| IRIS GL-Funktion  | OpenGL-Funktion                            | Bedeutung                     |
|-------------------|--------------------------------------------|-----------------------------|
|                   | [**glEnable**](glenable.md) (GL \_ Blend) | Schaltet das Mischen ein.          |
| **BLENDFUNCTION** | [**glblendfunc**](glblendfunc.md)         | Gibt eine Blend-Funktion an. |



 

Die OpenGL-Funktion " **glblendfunc** " und die Iris GL **BLENDFUNCTION** -Funktion sind nahezu identisch. Die folgende Tabelle enthält die Iris GL-Faktoren und deren OpenGL-Entsprechungen.



| IRIS GL          | OpenGL                     | Notizen             |
|------------------|----------------------------|-------------------|
| BF \_ null         | GL \_ null                   |                   |
| BF- \_ 1          | GL \_ 1                    |                   |
| BF \_ sa           | GL \_ src \_ Alpha             |                   |
| BF- \_ MSA          | GL \_ One \_ minus \_ src \_ Alpha |                   |
| BF- \_ da           | GL- \_ DST- \_ Alpha             |                   |
| BF- \_ MDA          | GL \_ 1 \_ minus \_ DST- \_ Alpha |                   |
| BF \_ SC           | GL- \_ src- \_ Farbe             |                   |
| BF \_ MSC          | GL \_ 1 \_ minus \_ src- \_ Farbe | Nur Ziel. |
| BF- \_ DC           | GL- \_ DST- \_ Farbe             | Nur Quelle.      |
| BF- \_ MDC          | GL \_ 1 \_ minus \_ DST- \_ Farbe | Nur Quelle.      |
| BF \_ Min. \_ sa- \_ MDA | GL \_ src \_ alpha- \_ vollständig   |                   |



 

??

 

 




