---
title: Verwenden von Antialiasing-Funktionen
description: In der folgenden Tabelle sind die Iris GL-Antialiasing-Funktionen und ihre entsprechenden OpenGL-Funktionen aufgelistet.
ms.assetid: d54990b6-5645-4389-82ca-7d7f0a7fd7e9
keywords:
- IRIS GL portieren, Antialiasing
- Portieren von IRIS GL, Antialiasing
- Portieren auf OpenGL von IRIS GL, Antialiasing
- OpenGL-Portierung von IRIS GL, Antialiasing
- Antialiasing (antialiasing)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896d02dec050c72e59762ff5ee139b0bd091d9a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206562"
---
# <a name="using-antialiasing-functions"></a>Verwenden von Antialiasing-Funktionen

In der folgenden Tabelle sind die Iris GL-Antialiasing-Funktionen und ihre entsprechenden OpenGL-Funktionen aufgelistet.



| IRIS GL-Funktion | OpenGL-Funktion                                      | Bedeutung                           |
|------------------|------------------------------------------------------|-----------------------------------|
| **PNP**    | [**glEnable**](glenable.md) (GL- \_ Punkt \_ glatt)   | Ermöglicht das Antialiasing von Punkten.   |
| **linesmuoth**   | **glEnable**(GL- \_ Linie \_ glatt)                     | Ermöglicht das Antialiasing von Zeilen.    |
| **polysmooth**   | [**glEnable**](glenable.md) (GL- \_ Polygon \_ glatt) | Ermöglicht das Antialiasing von Polygonen. |



 

Verwenden Sie die entsprechenden [**gldeaktiviert**](gldisable.md) -Aufrufe, um das Antialiasing zu deaktivieren.

In IRIS GL können Sie die Qualität des Antialiasing steuern, indem Sie Folgendes aufrufen:


```C++
linesmooth(SML_ON + SML_SMOOTHER);
```



OpenGL bietet einen ähnlichen controluse- [**glhint**](glhint.md):


```C++
glHint(GL_POINT_SMOOTH_HINT, hintMode); 
glHint(GL_LINE_SMOOTH_HINT, hintMode); 
glHint(GL_POLYGON_SMOOTH_HINT, hintMode);
```



Dabei ist *hintmode* einer der folgenden:

-   GL \_ am schönsten (verwenden Sie die höchste Qualität der Glättung)
-   GL \_ schnellste (verwenden Sie die effizienteste Glättung)
-   GL ist nicht \_ \_ wichtig

IRIS GL ermöglicht außerdem eine End-Korrektur durch Aufrufen von:


```C++
linesmooth(SML_ON +  SML_END_CORRECT);
```



OpenGL ist für diese Funktion nicht gleichwertig.

 

 




