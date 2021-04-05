---
title: Erweiterte Drehung
description: In diesem Abschnitt wird erläutert, wie ein Objekt basierend auf dem Ort, an dem der Benutzer die Drehung bearbeitet, gedreht wird.
ms.assetid: 56b339b1-a062-4c0e-91c8-aec08a17bc65
keywords:
- Windows-Fingereingabe, Drehung
- Windows-Fingereingabe, erweiterte Drehung
- Windows-Fingereingabe, Manipulationen
- Manipulationen, Drehung
- Manipulationen, erweiterte Drehung
- Rotation, erweitert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3a84679f4189d28941262cda2585887b0932c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947433"
---
# <a name="advanced-rotation"></a>Erweiterte Drehung

In diesem Abschnitt wird erläutert, wie ein Objekt basierend auf dem Ort, an dem der Benutzer die Drehung bearbeitet, gedreht wird.

In der folgenden Abbildung werden zwei verschiedene Möglichkeiten veranschaulicht, wie ein Objekt gedreht werden kann.

![die Abbildung zeigt zwei Arten von Einzel fingerdrehung: um den Mittelpunkt oder um den Rand, wobei der Rand sowohl Drehung als auch Übersetzung umfasst.](images/rotation.png)

In Beispiel A wird das Objekt um den Mittelpunkt des Objekts manipuliert. In Beispiel B wird das Objekt um den Mittelpunkt der Bearbeitung gedreht. Zur Unterstützung von Manipulationen um einen anderen Punkt als den Mittelpunkt des Objekts muss eine verbundbearbeitung durchgeführt werden, die sowohl Drehung als auch Übersetzung ausführt. Der folgende Code zeigt, wie diese Manipulation ausgeführt und berechnet wird.


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

 

 




