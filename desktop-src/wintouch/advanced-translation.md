---
title: Erweiterte Übersetzung
description: Erweiterte Übersetzung
ms.assetid: 48a1bdd5-8b7b-4460-9b7b-1ab8969a28f8
keywords:
- Windows-Fingereingabe, Übersetzung
- Windows-Fingereingabe, erweiterte Übersetzung
- Windows-Fingereingabe, Manipulationen
- Manipulationen, Übersetzung
- Manipulationen, erweiterte Übersetzung
- Verschiebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc383c71e1f1417d30b64db18aa627039602b942
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855503"
---
# <a name="advanced-translation"></a>Erweiterte Übersetzung

Die folgende Abbildung zeigt zwei Interpretationen der Übersetzung.

![Abbildung, die zuerst die einfache Übersetzung anzeigt, bei der ein Objekt ohne Drehung verschoben wird, und dann die erweiterte Übersetzung anzeigt, die das Verschieben mit Drehung einschließt](images/translation.png)

In Beispiel A, dem Beispiel für die einfache Übersetzung, wird das Objekt ohne Drehung verschoben. In Beispiel B wird das Objekt während der Übersetzung gedreht, je nachdem, wo sich der Objekt Kontaktpunkt befindet. Wenn Sie die Drehung mit einem Finger wie in [Einzel Finger Drehung](single-finger-rotation.md)beschrieben aktivieren, können Sie die komplexe Übersetzung aktivieren. Das folgende Diagramm zeigt die verschiedenen Komponenten der Einzel Finger Drehung, wenn Sie die Übersetzung durchführen.

![die Abbildung zeigt die Komponenten der Einzel Finger Drehung: pivotpointx, pivotpointy und pivotradius.](images/translation-complex-components.png)

Beim Verschieben des Objekts wird der RADIUS neu berechnet, und der Pivotpunkt wird verschoben.

Der folgende Code zeigt eine Möglichkeit, wie Sie dies in einer Implementierung von [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) durchführen können, die eine komplexe Übersetzung ermöglicht.


```C++
    //Apply transformation based on rotationDelta (in radians)
    FLOAT rads = 180.0f / 3.14159f;
    m_dObj->Rotate(rotationDelta*rads, x, y);

    // Apply translation based on scaleDelta
    m_dObj->Scale(scaleDelta);

    // Apply translation based on translationDelta
    m_dObj->Translate(translationDeltaX, translationDeltaY);

    // Set values for one finger rotations
    FLOAT fPivotRadius = (FLOAT)(m_dObj->get_Width() + m_dObj->get_Height())/8.0f;
    FLOAT fPivotPtX = m_dObj->get_CenterX();
    FLOAT fPivotPtY = m_dObj->get_CenterY();
        
    m_manip->put_PivotPointX(fPivotPtX);
    m_manip->put_PivotPointY(fPivotPtY);
    m_manip->put_PivotRadius(fPivotRadius);       
   
```



> [!Note]  
> Objekt Transformationen treten auf, bevor die pivotpunkte und der Radius berechnet werden. Auf diese Weise wird das Objekt ordnungsgemäß verschoben, wenn der Benutzer während des Verschiebens eine Erweiterung des Objekts ausführt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Manipulationen](getting-started-with-manipulations.md)
</dt> </dl>

 

 




