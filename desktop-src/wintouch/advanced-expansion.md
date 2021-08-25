---
title: Erweiterte Erweiterung
description: Erweiterte Erweiterung
ms.assetid: 29db15a1-fa56-441a-af99-9e858d143804
keywords:
- Windows Touch,Erweiterung
- Windows Touch,erweiterte Erweiterung
- Windows Touch,Manipulationen
- Manipulationen, Erweiterung
- Manipulationen,erweiterte Erweiterung
- Erweiterung,erweitert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27e176d91c08bd0d39383e2aba269bbdb5629cfe6b7c2d20eb1ac955786bef2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881500"
---
# <a name="advanced-expansion"></a>Erweiterte Erweiterung

Die folgende Abbildung zeigt zwei Möglichkeiten, wie ein Objekt erweitert werden kann.

![Abbildung: einfache Erweiterung um den Mittelpunkt eines Objekts und erweiterte Erweiterung um den Mittelpunkt der Manipulation](images/expansion.png)

In Beispiel A, dem einfachen Erweiterungsbeispiel, wird das -Objekt um seinen Mittelpunkt erweitert. In Beispiel B wird das -Objekt um den Mittelpunkt der Bearbeitung erweitert. Um dies zu aktivieren, müssen Sie das Objekt übersetzen, während es erweitert wird. Der Betrag, den Sie das Objekt übersetzen, entspricht dem Abstand zwischen der Mitte des Objekts und dem Mittelpunkt der Geste. Intuitiv ist es so, als ob Sie das Objekt vom Mittelpunkt ihrer Erweiterungsgeste aus erweitern und es dann verschieben, sodass es sich immer noch in der Mitte der ursprünglichen Position befindet. Der folgende Code zeigt eine Möglichkeit, dieses Konzept anzuwenden, um die Erweiterung um einen Mittelpunkt zu ermöglichen.


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

 

 




