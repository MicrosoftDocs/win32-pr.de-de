---
title: Verwenden von Antialiasingfunktionen
description: In der folgenden Tabelle sind iris gl antialiasing-Funktionen und die entsprechenden OpenGL-Funktionen aufgeführt.
ms.assetid: d54990b6-5645-4389-82ca-7d7f0a7fd7e9
keywords:
- IRIS GL-Portierung,Antialiasing
- Portieren von IRIS GL,Antialiasing
- Portieren von IRIS GL zu OpenGL, Antialiasing
- OpenGL-Portierung von IRIS GL,Antialiasing
- Antialiasing (antialiasing)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab36f41e3b639447b4f246d706e11c134d8f920528cde1e946d26af057a95951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117980346"
---
# <a name="using-antialiasing-functions"></a>Verwenden von Antialiasingfunktionen

In der folgenden Tabelle sind iris gl antialiasing-Funktionen und die entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion | OpenGL-Funktion                                      | Bedeutung                           |
|------------------|------------------------------------------------------|-----------------------------------|
| **pntsmooth**    | [**glEnable**](glenable.md) ( GL \_ POINT \_ SMOOTH )   | Aktiviert das Antialiasing von Punkten.   |
| **linesmooth**   | **glEnable**( GL \_ LINE \_ SMOOTH )                     | Aktiviert das Antialiasing von Zeilen.    |
| **polysmooth**   | [**glEnable**](glenable.md) ( GL \_ POLYGON \_ SMOOTH ) | Aktiviert Antialiasing von Polygonen. |



 

Verwenden Sie die entsprechenden [**glDisable-Aufrufe,**](gldisable.md) um Antialiasing zu deaktivieren.

In IRIS GL können Sie die Qualität des Antialiasings steuern, indem Sie Folgendes aufrufen:


```C++
linesmooth(SML_ON + SML_SMOOTHER);
```



OpenGL bietet ein ähnliches Steuerelement wie [**glHint:**](glhint.md)


```C++
glHint(GL_POINT_SMOOTH_HINT, hintMode); 
glHint(GL_LINE_SMOOTH_HINT, hintMode); 
glHint(GL_POLYGON_SMOOTH_HINT, hintMode);
```



dabei ist *hintMode* einer der folgenden:

-   GL \_ NICEST (Verwenden Sie die Glättung der höchsten Qualität.)
-   GL \_ FASTEST (Verwenden Sie die effizienteste Glättung.)
-   GL \_ DONT \_ CARE

IRIS GL ermöglicht auch die Endkorrektur durch Aufrufen von:


```C++
linesmooth(SML_ON +  SML_END_CORRECT);
```



OpenGL verfügt über keine Entsprechung für diese Funktion.

 

 




