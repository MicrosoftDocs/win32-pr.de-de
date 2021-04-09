---
title: Single-Finger Drehung
description: In diesem Abschnitt wird erläutert, wie ein Objekt mithilfe eines pivotpunkts gedreht wird.
ms.assetid: b9c19009-8ac0-4168-bf26-393280fc589f
keywords:
- Windows-Fingereingabe, Drehung
- Windows-Fingereingabe, Manipulationen
- Windows Touch, Einzel Finger Drehung
- Windows-Fingereingabe, pivotpunktdrehung
- Manipulationen, Drehung
- Drehung, pivotpunkte
- Drehung, Einzel Finger
- Gesten, Einzel Finger Drehung
- Rotation mit einem Finger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d74263f502749e2aaf942c4bbec5aa0a284e76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855739"
---
# <a name="single-finger-rotation"></a>Single-Finger Drehung

In diesem Abschnitt wird erläutert, wie ein Objekt mithilfe eines pivotpunkts gedreht wird.

In der folgenden Abbildung wird die Rotation mit einem Finger veranschaulicht.

![Abbildung mit zwei Arten von Einzel fingerdrehung: um das Zentrum oder um den Rand herum](images/sfrotation.png)

In Beispiel A wird das Objekt um den Mittelpunkt des Objekts mit der Drehungs Bewegung gedreht. In Beispiel B wird das Objekt gedreht, indem ein einzelner Finger um den Rand des Objekts bewegt wird. Der Manipulations Prozessor ermöglicht diese Rotation mithilfe von Pivotpunkt-und Pivot-RADIUS-Werten. In der folgenden Abbildung werden die Komponenten der Einzel Finger Drehung veranschaulicht.

![die Abbildung zeigt die Komponenten der Einzel Finger Drehung: pivotpointx, pivotpointy und pivotradius.](images/sfrotation-components.png)

Nachdem Sie die Werte [**pivotpointx**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx), [**pivotpointy**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)und [**pivotradius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) festgelegt haben, enthalten nachfolgende Übersetzungs Meldungen die Drehung. Je größer der pivotradius ist, desto größer ist die Änderung in x und y, um das Objekt zu drehen. Der folgende Code zeigt, wie diese Werte im Bearbeitungs Prozessor festgelegt werden können.


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



Im vorherigen Beispiel wird der Abstand zum Rand des Objekts (auf 40 Prozent skaliert) als pivotradius verwendet. Da die Objektgröße berücksichtigt wird, ist diese Berechnung für jedes Objekt Delta gültig. Beim Skalieren des Objekts wächst der pivotradius. Dieser Wert und die x-und y-Werte des-Objekts werden an den Manipulations Prozessor übermittelt, um das Objekt um den Pivotpunkt zu drehen.

> [!Note]  
> Der [**pivotradius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) -Wert darf niemals zwischen 0,0 und 1,0 liegen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Manipulationen](getting-started-with-manipulations.md)
</dt> <dt>

[**Pivotradius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius)
</dt> <dt>

[**Pivotpointx**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx)
</dt> <dt>

[**Pivotpointy**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)
</dt> </dl>

 

 




