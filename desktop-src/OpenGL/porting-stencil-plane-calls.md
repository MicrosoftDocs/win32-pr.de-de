---
title: Portieren von Schablonen der Schablone
description: In OpenGL weisen Sie Schablone-Ebenen zu, indem Sie das entsprechende Pixel Format mit dem OpenGL-Format "", "
ms.assetid: faea8a10-860a-4495-80fb-e83303e397df
keywords:
- IRIS GL portieren, Schablone-Ebenen
- Portieren von IRIS GL, Schablone-Ebenen
- Portieren auf OpenGL von IRIS GL, Schablone-Ebenen
- OpenGL-Portierung von IRIS GL, Schablone-Ebenen
- Schablone-Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829ea033a75cb1153a475496c3f33398640dbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310540"
---
# <a name="porting-stencil-plane-calls"></a>Portieren von Schablonen der Schablone

In OpenGL weisen Sie Schablone-Ebenen zu, indem Sie das entsprechende Pixel Format mit dem **OpenGL-** [**Format "**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)", " Funktionen. In der folgenden Tabelle sind die Funktionen von IRIS GL aufgeführt, die sich auf die Schablone-Ebenen und ihre entsprechenden OpenGL-Funktionen auswirken.



| IRIS GL-Funktion             | OpenGL-Funktion                                         | Bedeutung                                                |
|------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| **Schablone**                 | **Auswahl Pixel Format**                                   |                                                        |
| **Schablone**( **true**,...) | [**glEnable**](glenable.md) (GL- \_ Schablone- \_ Test)      | Aktiviert Schablonen Tests.                                 |
| **Schablone**                  | [**glstencilop**](glstencilop.md)                      | Legt Schablone-Test Aktionen fest.                             |
| **Schablone**(... Func,...)  | [**glstencilfunc**](glstencilfunc.md)                  | Legt die Funktion und den Verweis Wert für das Testen der Schablone fest. |
| **sschreibfrage**               | [**glstencilmask**](glstencilmask.md)                  | Gibt an, welche Schablonen Bits geschrieben werden können.           |
|                              | [**glclearstencil**](glclearstencil.md)                | Gibt den eindeutigen Wert für den Schablonen Puffer an.      |
| **sClear**                   | [**glClear**](glclear.md) (GL- \_ Schablone- \_ Puffer \_ Bit) |                                                        |



 

Schablone: Vergleichsfunktionen und Schablonen Durchlauf-/Fehlervorgänge sind fast Äquivalent in OpenGL und IRIS GL. Die Iris GL Stencil-funktionsflags werden mit SF vorangestellt. die OpenGL-Flags mit GL. Bei Iris GL Pass/Fail-Vorgangs Flags wird "St;" vorangestellt. die OpenGL-Flags mit GL.

 

 




