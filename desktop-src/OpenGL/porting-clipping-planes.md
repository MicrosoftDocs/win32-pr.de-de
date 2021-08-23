---
title: Portieren von Clippingebenen
description: OpenGL implementiert Clippingebenen ähnlich wie IRIS GL. Darüber hinaus können Sie in OpenGL Clippingebenen abfragen. In der folgenden Tabelle sind die IRIS GL-Clippingebenenfunktionen und die entsprechenden OpenGL-Funktionen aufgeführt.
ms.assetid: bfca59c3-b7ef-4545-8b8d-022ea782569b
keywords:
- IRIS GL-Portierung, Clippingebenen
- Portieren von IRIS GL,Clippingebenen
- Portieren von IRIS GL zu OpenGL, Clippingebenen
- OpenGL-Portierung von IRIS GL,Clippingebenen
- Clippingebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f314b7c6453de3b0933970b7d520a8c161d6eef4a9bb98ea891c73665fba4933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777120"
---
# <a name="porting-clipping-planes"></a>Portieren von Clippingebenen

OpenGL implementiert Clippingebenen ähnlich wie IRIS GL. Darüber hinaus können Sie in OpenGL Clippingebenen abfragen. In der folgenden Tabelle sind die IRIS GL-Clippingebenenfunktionen und die entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion                          | OpenGL-Funktion                                                                               | Bedeutung                                  |
|-------------------------------------------|-----------------------------------------------------------------------------------------------|------------------------------------------|
| **clipplane** (i, **CP \_ ON,** params)     | [**glEnable**](glenable.md) ( GL \_ CLIP \_ PLANEi )                                             | Aktiviert clipping auf Ebene i.             |
| **clipplane**( i, **CP \_ DEFINE**, plane ) | [**glClipPlane**](glclipplane.md) ( GL \_ CLIP \_ PLANEi, plane )                                | Definiert die Clippingebene.                  |
|                                           | [**glGetClipPlane**](glgetclipplane.md)                                                      | Gibt die Gleichung der Clippingebene zurück.         |
|                                           | [**glIsEnabled**](glisenabled.md) ( GL \_ CLIP \_ PLANEi )                                       | Gibt TRUE zurück, wenn die Clipebene i aktiviert ist. |
| **scrmask**                               | [**glScissor**](glscissor.md)                                                                | Definiert das Scissor-Feld.                 |
| **getscrmask**                            | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ SCISSOR \_ BOX ) | Gibt das aktuelle Scissor-Feld zurück.         |



 

Rufen Sie **glEnable mithilfe** von GL SCISSOR BOX als Parameter auf, um den Scissor-Test \_ zu \_ aktivieren.

??

 

 




