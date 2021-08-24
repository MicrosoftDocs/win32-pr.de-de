---
title: Single-Finger Rotation
description: In diesem Abschnitt wird erläutert, wie Sie ein Objekt mithilfe eines Pivotpunkts drehen.
ms.assetid: b9c19009-8ac0-4168-bf26-393280fc589f
keywords:
- Windows Touch,Drehung
- Windows Touch,Manipulationen
- Windows Touch, Drehung mit einem Finger
- Windows Touch,Pivotpunktrotation
- Manipulationen, Drehung
- Drehung, Pivotpunkte
- Drehung, einzelfinger
- Gesten, Drehung mit einem Finger
- Drehung mit einem Finger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36fe7e92f6d68515e1d13b39c32ee4af5b6b03e675479242210fe302b84e6395
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110650"
---
# <a name="single-finger-rotation"></a>Single-Finger Rotation

In diesem Abschnitt wird erläutert, wie Sie ein Objekt mithilfe eines Pivotpunkts drehen.

Die folgende Abbildung veranschaulicht die Drehung mit einem Finger.

![Abbildung, die zwei Arten der Drehung mit einem Finger zeigt: um die Mitte oder um den Rand](images/sfrotation.png)

In Beispiel A wird das -Objekt mithilfe der Drehbewegung um den Mittelpunkt des Objekts gedreht. In Beispiel B wird das Objekt gedreht, indem ein einzelner Finger um den Rand des Objekts bewegt wird. Der Manipulationsprozessor ermöglicht diese Drehung mithilfe von Pivotpunkt- und Pivotradiuswerten. Die folgende Abbildung veranschaulicht die Komponenten der Drehung mit einem Finger.

![Abbildung der Komponenten der Drehung mit einem Finger: pivotpointx, pivotpointy und pivotradius](images/sfrotation-components.png)

Nachdem Sie die [**Werte PivotPointX,**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)und [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) festgelegt haben, enthalten nachfolgende Übersetzungsmeldungen die Drehung. Je größer der Pivotradius, desto größer muss die Änderung in x und y sein, um das Objekt zu drehen. Der folgende Code zeigt, wie diese Werte im Bearbeitungsprozessor festgelegt werden können.


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;

    // Set the pivot point to the object's center and then set the radius 
    // to the distance from the center to the edge of the object.
    m_pManip->put_PivotPointX(m_objectRef->xPos);
    m_pManip->put_PivotPointY(m_objectRef->yPos);
    
    float fPivotRadius = (FLOAT)(sqrt(pow(m_dObj->get_Width()/2, 2) + pow(m_dObj->get_Height()/2, 2)))*0.4f;
    
    m_pManip->put_PivotRadius(fPivotRadius);
  

    return S_OK;
}    
     
```



Im vorherigen Beispiel wird der Abstand zum Rand des Objekts (auf 40 Prozent skaliert) als Pivotradius verwendet. Da die Objektgröße berücksichtigt wird, ist diese Berechnung für jedes Objektdelta gültig. Wenn das Objekt skaliert wird, wächst der Pivotradius. Dieser Wert und die x- und y-Werte in der Mitte des Objekts werden an den Bearbeitungsprozessor übergeben, um das Objekt um den Pivotpunkt zu drehen.

> [!Note]  
> Der [**PivotRadius-Wert**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) sollte nie zwischen 0,0 und 1,0 liegen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Manipulationen](getting-started-with-manipulations.md)
</dt> <dt>

[**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius)
</dt> <dt>

[**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx)
</dt> <dt>

[**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)
</dt> </dl>

 

 




