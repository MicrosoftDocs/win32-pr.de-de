---
title: Erweiterte Erweiterung
description: Erweiterte Erweiterung
ms.assetid: 29db15a1-fa56-441a-af99-9e858d143804
keywords:
- Windows-Fingereingabe, Erweiterung
- Windows-Fingereingabe, erweiterte Erweiterung
- Windows-Fingereingabe, Manipulationen
- Manipulationen, Erweiterung
- Manipulationen, erweiterte Erweiterung
- Erweiterung, erweitert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b81a3a395da053b7d0e8f79a115a2489f3e63190
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206325"
---
# <a name="advanced-expansion"></a>Erweiterte Erweiterung

Die folgende Abbildung zeigt zwei Möglichkeiten, wie ein Objekt erweitert werden kann.

![die Abbildung zeigt eine einfache Erweiterung um den Mittelpunkt eines Objekts und eine erweiterte Erweiterung um den Mittelpunkt der Bearbeitung.](images/expansion.png)

In Beispiel A, dem einfachen Erweiterungs Beispiel, wird das-Objekt um seinen Mittelpunkt erweitert. In Beispiel B wird das Objekt um den Mittelpunkt der Bearbeitung erweitert. Um dies zu ermöglichen, müssen Sie das Objekt übersetzen, während es erweitert wird. Die Menge, die Sie das Objekt übersetzen, entspricht der Entfernung vom Mittelpunkt des Objekts bis zum Mittelpunkt der Bewegung. Intuitiv ist es so, als ob Sie das Objekt vom Mittelpunkt der Erweiterungs Geste erweitern und es dann verschieben, damit es sich immer noch in der gleichen Mitte wie die anfängliche Position befindet. Der folgende Code zeigt eine Möglichkeit, wie dieses Konzept angewendet werden kann, um die Erweiterung um einen Mittelpunkt zu ermöglichen.


```C++
    if(m_fFactor != 1.0f)
    {
        // We represent our vectors as an array.
        // x: vx[0], y: vx[1]

        FLOAT v1[2];
        v1[0] = this->get_CenterX() - fOffset[0];
        v1[1] = this->get_CenterY() - fOffset[1];

        FLOAT v2[2];
        v2[0] = v1[0] * m_fFactor;
        v2[1] = v1[1] * m_fFactor;
        
        m_fdX += v2[0] - v1[0];
        m_fdY += v2[1] - v1[1];
    }
   
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Manipulationen](getting-started-with-manipulations.md)
</dt> </dl>

 

 




