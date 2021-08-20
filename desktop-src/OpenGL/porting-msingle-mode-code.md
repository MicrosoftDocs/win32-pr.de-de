---
title: Portieren von MSINGLE-Moduscode
description: OpenGL verfügt nicht über ein Äquivalent für den Einzelmatrixmodus MSINGLE.
ms.assetid: 7de933b8-150c-432d-89ee-5f5799ad8443
keywords:
- IRIS GL-Portierung, MSINGLE-Modus
- Portieren von IRIS GL, MSINGLE-Modus
- Portieren von IRIS GL im MSINGLE-Modus zu OpenGL
- OpenGL-Portierung über IRIS GL, MSINGLE-Modus
- MSINGLE-Modus
- IRIS GL-Portierung, Einzelmatrixmodus
- Portieren aus IRIS GL, Einzelmatrixmodus
- Portieren von IRIS GL im Einzelmatrixmodus zu OpenGL
- OpenGL-Portierung über IRIS GL, Einzelmatrixmodus
- Einzelmatrixmodus
- Double-Matrix-Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83716cead9134ba7823f4206fb6479d323bd35bddee480e9353a7ceb9aad38ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132389"
---
# <a name="porting-msingle-mode-code"></a>Portieren von MSINGLE-Moduscode

OpenGL verfügt über kein Äquivalent für **MSINGLE**, Einzelmatrixmodus. Obwohl von der Verwendung dieses Modus abgeraten wurde, ist dies die Standardeinstellung für IRIS GL. Wenn Ihr IRIS GL-Programm den Einzelmatrixmodus verwendet, müssen Sie ihn so umschreiben, dass nur der Modus mit doppelter Matrix verwendet wird. OpenGL befindet sich immer im Doppelmatrixmodus und befindet sich zunächst im GL \_ MODELVIEW-Modus.

Der großteil IRIS GL-Code im MSINGLE-Modus sieht wie hier aus:

``` syntax
projectionmatrix();
```

dabei *ist projectionmatrix* eines der: **ortho,** **ortho2,** **perspective** oder **window**. Ersetzen Sie zum Portieren zu OpenGL die **MSINGLE** -mode *projectionmatrix-Funktion* durch:


```C++
glMatrixMode( GL_PROJECTION ); 
glLoadMatrix( identity matrix ); 
 
/* call one of these functions here: */ 
/* glFrustrum(), glOrtho(), glOrtho2(), gluPerspective()}; */ 
 
glMatrixMode( GL_MODELVIEW ); 
glLoadMatrix( identity matrix );
```



 

 




