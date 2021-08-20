---
title: Portieren von Blendingcode
description: In IRIS GL wird beim Zeichnen in den Vorder- und Hintergrundpuffer eine Mischung durchgeführt, indem einer der Puffer gelesen, mit dieser Farbe gemischt und dann das Ergebnis in beide Puffer geschrieben wird. In OpenGL wird jeder Puffer jedoch nacheinander gelesen, gemischt und dann geschrieben.
ms.assetid: 18334c6b-586d-44a3-aa95-d10589ba99f4
keywords:
- IRIS GL-Portierung, Blending
- Portieren von IRIS GL,Blending
- Portieren von IRIS GL zu OpenGL,Blending
- OpenGL-Portierung von IRIS GL,Blending
- Mischen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13548a2f08821e4f80bf63230077f9a39540ba9b8a37763e7935d211ef0dcdc0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485910"
---
# <a name="porting-blending-code"></a>Portieren von Blendingcode

In IRIS GL wird beim Zeichnen in den Vorder- und Hintergrundpuffer eine Mischung durchgeführt, indem einer der Puffer gelesen, mit dieser Farbe gemischt und dann das Ergebnis in beide Puffer geschrieben wird. In OpenGL wird jeder Puffer jedoch nacheinander gelesen, gemischt und dann geschrieben.

In der folgenden Tabelle sind die IRIS GL-Mischungsfunktionen und die entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion  | OpenGL-Funktion                            | Bedeutung                     |
|-------------------|--------------------------------------------|-----------------------------|
|                   | [**glEnable**](glenable.md) ( GL \_ BLEND ) | Aktiviert das Mischen.          |
| **Blendfunction** | [**glBlendFunc**](glblendfunc.md)         | Gibt eine Blend-Funktion an. |



 

Die OpenGL **glBlendFunc-Funktion** und die **Blendfunction-Funktion** IRIS GL sind fast identisch. In der folgenden Tabelle sind iris gl blend-Faktoren und ihre OpenGL-Entsprechungen aufgeführt.



| IRIS GL          | Opengl                     | Hinweise             |
|------------------|----------------------------|-------------------|
| BF \_ ZERO         | GL \_ ZERO                   |                   |
| BF \_ ONE          | GL \_ ONE                    |                   |
| BF \_ SA           | GL \_ SRC \_ ALPHA             |                   |
| BF \_ MSA          | GL \_ 1 \_ MINUS \_ SRC \_ ALPHA |                   |
| BF \_ DA           | GL \_ DST \_ ALPHA             |                   |
| BF \_ MDA          | GL \_ 1 \_ MINUS \_ DST \_ ALPHA |                   |
| BF \_ SC           | GL \_ SRC \_ COLOR             |                   |
| BF \_ MSC          | GL \_ ONE \_ MINUS \_ SRC \_ COLOR | Nur Ziel. |
| BF \_ DC           | GL \_ DST \_ COLOR             | Nur Quelle.      |
| BF \_ MDC          | GL \_ ONE \_ MINUS \_ DST \_ COLOR | Nur Quelle.      |
| BF \_ MIN \_ SA \_ MDA | GL \_ SRC \_ ALPHA \_ SATURATE   |                   |



 

??

 

 




