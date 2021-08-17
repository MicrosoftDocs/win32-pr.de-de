---
title: Portieren von Schablonenebenenaufrufen
description: In OpenGL ordnen Sie Schablonenebenen zu, indem Sie das entsprechende Pixelformat mit OpenGL auxInitDisplayMode oder ChoosePixelFormat anfordern.
ms.assetid: faea8a10-860a-4495-80fb-e83303e397df
keywords:
- IRIS GL-Portierung, Schablonenebenen
- Portieren von IRIS GL,Schablonenebenen
- Portieren von IRIS GL,Schablonenebenen zu OpenGL
- OpenGL-Portierung von IRIS GL,Schablonenebenen
- Schablonenebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d2c9ea8a9c025c06f179b51cab1301f8ff871740576a6c9e28cdfc1f15ad3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485390"
---
# <a name="porting-stencil-plane-calls"></a>Portieren von Schablonenebenenaufrufen

In OpenGL ordnen Sie Schablonenebenen zu, indem Sie das entsprechende Pixelformat mit openGL **auxInitDisplayMode** oder [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)anfordern. Funktionen. In der folgenden Tabelle sind IRIS GL-Funktionen aufgeführt, die sich auf die Schablonenebenen und die entsprechenden OpenGL-Funktionen auswirken.



| IRIS GL-Funktion             | OpenGL-Funktion                                         | Bedeutung                                                |
|------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| **stensize**                 | **ChoosePixelFormat**                                   |                                                        |
| **Schablone**( **TRUE**, ... ) | [**glEnable**](glenable.md) ( GL \_ STENCIL \_ TEST )      | Aktiviert Schablonentests.                                 |
| **Schablone**                  | [**glStencilOp**](glstencilop.md)                      | Legt Schablonentestaktionen fest.                             |
| **Schablone**(... func, ... )  | [**glStencilFunc**](glstencilfunc.md)                  | Legt Funktionen- und Verweiswerte für Schablonentests fest. |
| **swritemask**               | [**glStencilMask**](glstencilmask.md)                  | Gibt an, welche Schablonenbits geschrieben werden können.           |
|                              | [**glClearStencil**](glclearstencil.md)                | Gibt den clear-Wert für den Schablonenpuffer an.      |
| **sclear**                   | [**glClear**](glclear.md) ( GL \_ STENCIL \_ BUFFER BIT \_ ) |                                                        |



 

Schablonenvergleichsfunktionen und Schablonendurchlauf-/Fehlervorgänge sind in OpenGL und IRIS GL nahezu gleichwertig. Den IRIS GL-Schablonenfunktionsflags wird SF vorangestellt. die OpenGL-Flags mit GL. IRIS GL-Flags für Pass-/Fail-Vorgänge wird ST vorangestellt. Die OpenGL-Flags mit GL.

 

 




