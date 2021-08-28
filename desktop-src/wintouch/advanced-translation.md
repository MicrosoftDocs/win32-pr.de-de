---
title: Erweiterte Übersetzung
description: Erweiterte Übersetzung
ms.assetid: 48a1bdd5-8b7b-4460-9b7b-1ab8969a28f8
keywords:
- Windows Toucheingabe, Übersetzung
- Windows Toucheingabe, erweiterte Übersetzung
- Windows Toucheingabe, Bearbeitungen
- Manipulationen, Übersetzung
- Manipulationen, erweiterte Übersetzung
- Verschiebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4712375c12420e076bb93c1240d18dc8e3c1d58006eb24ced7a62a7485e01c5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810345"
---
# <a name="advanced-translation"></a>Erweiterte Übersetzung

Die folgende Abbildung zeigt zwei Übersetzungsinterpretationen.

![Abbildung, die zuerst die einfache Übersetzung zeigt, in der ein Objekt ohne Drehung verschoben wird, und dann die erweiterte Übersetzung, die das Verschieben mit Drehung umfasst](images/translation.png)

In Beispiel A, dem einfachen Übersetzungsbeispiel, wird das Objekt ohne Drehung verschoben. In Beispiel B wird das Objekt während der Übersetzung gedreht, je nachdem, wo sich der Objektkontaktpunkt befindet. Wenn Sie die Drehung mit einem Finger aktivieren, wie unter [Einfingerrotation](single-finger-rotation.md)beschrieben, können Sie die komplexe Übersetzung aktivieren. Das folgende Diagramm zeigt die verschiedenen Komponenten der Drehung mit einem Finger, wenn Sie die Übersetzung durchführen.

![Abbildung, die die Komponenten der Single-Finger-Drehung zeigt: pivotpointx, pivotpointy und pivotradius](images/translation-complex-components.png)

Wenn das Objekt verschoben wird, wird der Radius neu berechnet, und der Pivotpunkt wird verschoben.

Der folgende Code zeigt eine Möglichkeit, dies in einer Implementierung von [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) zu erreichen, die eine komplexe Übersetzung ermöglicht.


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
> Objekttransformationen treten auf, bevor die Pivotpunkte und der Radius berechnet werden. Auf diese Weise wird das Objekt ordnungsgemäß verschoben, wenn der Benutzer während des Verschiebens eine Erweiterung des Objekts ausführt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Manipulationen](getting-started-with-manipulations.md)
</dt> </dl>

 

 




