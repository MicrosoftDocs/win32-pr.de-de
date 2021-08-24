---
description: Ein Gerätekontext (DC) enthält Attribute, die sich auf die Zeilen- und Kurvenausgabe auswirken. Die Linien- und Kurvenattribute umfassen die aktuelle Position, den Pinselstil, die Pinselfarbe, den Stiftstil, die Stiftfarbe, die Transformation usw.
ms.assetid: 9529b389-85f6-421f-8429-9b61cee56ef1
title: Linien- und Kurvenattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d5ab8758cf6e77b28568cacafd8c57312c052d9e9415211f034e3d1a70b6c09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831610"
---
# <a name="line-and-curve-attributes"></a>Linien- und Kurvenattribute

Ein Gerätekontext (DC) enthält Attribute, die sich auf die Zeilen- und Kurvenausgabe auswirken. Die *Linien- und Kurvenattribute* umfassen die aktuelle Position, den Pinselstil, die Pinselfarbe, den Stiftstil, die Stiftfarbe, die Transformation usw.

Die aktuelle Standardposition für jeden DC befindet sich am Punkt (0,0) im logischen (oder welten) Raum. Sie können diese Koordinaten auf eine neue Position festlegen, indem Sie die [**MoveToEx-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) aufrufen und einen neuen Satz von Koordinaten übergeben.

> [!Note]  
> Es gibt zwei Sätze von Linien- und Kurvenzeichnungsfunktionen. Die erste Gruppe behält die aktuelle Position in einem Domänencontroller bei, und die zweite Gruppe ändert die Position. Sie können die Funktionen identifizieren, die die aktuelle Position ändern, indem Sie den Funktionsnamen untersuchen. Wenn der Funktionsname mit der Präposition "To" endet, legt die Funktion die aktuelle Position auf den Endpunkt der letzten gezeichneten Zeile fest ([**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto), [**ArcTo,**](/windows/desktop/api/Wingdi/nf-wingdi-arcto) [**PolylineTo**](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)oder [**PolyBezierTo**](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)). Wenn der Funktionsname nicht mit dieser Präposition endet, bleibt die aktuelle Position unverändert ([**Arc,**](/windows/desktop/api/Wingdi/nf-wingdi-arc) [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)oder [**PolyBezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)).

 

Der Standardpinsel ist ein weißer Volltextpinsel. Eine Anwendung kann einen neuen Pinsel erstellen, indem sie die [**CreateBrushIndirect-Funktion aufruft.**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect) Nach dem Erstellen eines Pinsels kann die Anwendung ihn in ihrem DC auswählen, indem sie die [**SelectObject-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) aufruft. Windows bietet einen vollständigen Satz von Funktionen zum Erstellen, Auswählen und Ändern des Pinsels im DC einer Anwendung. Weitere Informationen zu diesen Funktionen und zu Pinseln im Allgemeinen finden Sie unter [Pinsel.](brushes.md)

Der Standardstift ist ein farbiger, solider schwarzer Stift, der ein Pixel breit ist. Eine Anwendung kann mithilfe der [**ExtCreatePen-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) einen Stift erstellen. Nach dem Erstellen eines Stifts kann Ihre Anwendung ihn in ihrem DC auswählen, indem sie die [**SelectObject-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) aufruft. Windows bietet einen vollständigen Satz von Funktionen zum Erstellen, Auswählen und Ändern des Stifts im DC einer Anwendung. Weitere Informationen zu diesen Funktionen und zu Stiften im Allgemeinen finden Sie unter [Stifte.](pens.md)

Die Standardtransformation ist die Unity-Transformation (angegeben durch die Identitätsmatrix). Eine Anwendung kann eine neue Transformation angeben, indem sie die [**SetWorldTransform-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) aufruft. Windows bietet einen vollständigen Satz von Funktionen zum Transformieren von Linien und Kurven durch Ändern ihrer Breite, Position und allgemeinen Darstellung. Weitere Informationen zu diesen Funktionen finden Sie unter [Koordinatenräume und Transformationen.](coordinate-spaces-and-transformations.md)

 

 



