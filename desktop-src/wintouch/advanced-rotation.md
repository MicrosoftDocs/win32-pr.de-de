---
title: Erweiterte Drehung
description: In diesem Abschnitt wird erläutert, wie ein Objekt basierend auf dem Ort rotiert wird, an dem der Benutzer die Drehungsbearbeitung vor ort macht.
ms.assetid: 56b339b1-a062-4c0e-91c8-aec08a17bc65
keywords:
- Windows Touch,Drehung
- Windows Touch,erweiterte Drehung
- Windows Touch,Manipulationen
- Manipulationen, Drehung
- Manipulationen,erweiterte Drehung
- Rotation,erweitert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6dda17ae8076061f7b5b7b935afb2b7f8e5fb10cb270280f7edbb8c23aa896
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199516"
---
# <a name="advanced-rotation"></a>Erweiterte Drehung

In diesem Abschnitt wird erläutert, wie ein Objekt basierend auf dem Ort rotiert wird, an dem der Benutzer die Drehungsbearbeitung vor ort macht.

Die folgende Abbildung veranschaulicht zwei verschiedene Möglichkeiten, wie ein Objekt gedreht werden kann.

![Abbildung, die zwei Arten der Drehung mit einem Finger zeigt: um die Mitte oder um den Rand herum, mit dem Rand, der sowohl Drehung als auch Übersetzung einträgt](images/rotation.png)

In Beispiel A wird das -Objekt um den Mittelpunkt des Objekts herum bearbeitet. In Beispiel B wird das -Objekt um den Mittelpunkt der Bearbeitung gedreht. Um bearbeitungen um einen anderen Punkt als den Mittelpunkt des Objekts zu unterstützen, müssen Sie eine zusammengesetzte Bearbeitung durchführen, die sowohl Drehung als auch Übersetzung ausführt. Der folgende Code zeigt, wie diese Bearbeitung durchgeführt und berechnet wird.


```C++
RotateVector(FLOAT *vector, FLOAT *tVector, FLOAT fAngle) {
    FLOAT fAngleRads = fAngle / 180.0f * 3.14159f;
    FLOAT fSin = sin(fAngleRads);
    FLOAT fCos = cos(fAngleRads);

    FLOAT fNewX = (vector[0]*fCos) - (vector[1]*fSin);
    FLOAT fNewY = (vector[0]*fSin) + (vector[1]*fCos);

    tVector[0] = fNewX;
    tVector[1] = fNewY;
}
     
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Manipulationen](advanced-manipulations.md)
</dt> <dt>

[Manipulationen](getting-started-with-manipulations.md)
</dt> </dl>

 

 




