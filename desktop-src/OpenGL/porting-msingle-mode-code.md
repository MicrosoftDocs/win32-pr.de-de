---
title: Portieren von Code im msingle-Modus
description: OpenGL hat keine Entsprechung für den msingle-, Single Matrix-Modus.
ms.assetid: 7de933b8-150c-432d-89ee-5f5799ad8443
keywords:
- IRIS GL Porting, msingle Mode
- Portieren von IRIS GL, msingle Mode
- Portieren auf OpenGL von IRIS GL, msingle Mode
- OpenGL-Portierung von IRIS GL, msingle Mode
- Msingle-Modus
- IRIS GL portieren, Einzel Matrix Modus
- Portieren von IRIS GL, Einzel Matrix Modus
- Portieren auf OpenGL von IRIS GL, Single Matrix Mode
- OpenGL-Portierung von IRIS GL, Einzel Matrix Modus
- Einzel Matrix Modus
- Double-Matrix-Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b8c62f93fa8e027dd1c91ca0bd40bc8e6ffaf9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388486"
---
# <a name="porting-msingle-mode-code"></a>Portieren von Code im msingle-Modus

OpenGL hat keine Entsprechung für den **msingle**-, Single Matrix-Modus. Obwohl die Verwendung dieses Modus davon abgeraten hat, ist dies der Standardwert für Iris GL. Wenn Ihr IRIS GL-Programm den Einzel Matrix Modus verwendet, müssen Sie es so umschreiben, dass nur der Double-Matrix-Modus verwendet wird. OpenGL befindet sich immer im Double-Matrix-Modus und ist anfänglich im GL \_ Modelview-Modus.

Der größte IRIS GL-Code im msingle-Modus sieht wie folgt aus:

``` syntax
projectionmatrix();
```

Dabei ist *ProjectionMatrix* einer der folgenden **: Ortho**, **ortho2**, **Perspective** oder **Window**. Um auf OpenGL zu portieren, ersetzen Sie die " **msingle** -Mode *ProjectionMatrix* "-Funktion durch:


```C++
glMatrixMode( GL_PROJECTION ); 
glLoadMatrix( identity matrix ); 
 
/* call one of these functions here: */ 
/* glFrustrum(), glOrtho(), glOrtho2(), gluPerspective()}; */ 
 
glMatrixMode( GL_MODELVIEW ); 
glLoadMatrix( identity matrix );
```



 

 




