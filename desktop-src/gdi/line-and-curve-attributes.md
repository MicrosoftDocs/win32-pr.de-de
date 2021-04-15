---
description: Ein Gerätekontext (DC) enthält Attribute, die sich auf die Zeilen-und Kurven Ausgabe auswirken. Die Attribute "Line" und "Curve" umfassen die aktuelle Position, den Pinsel Stil, die Pinsel Farbe, den Stift Stil, die Stift Farbe, die Transformation usw.
ms.assetid: 9529b389-85f6-421f-8429-9b61cee56ef1
title: Linien-und Kurven Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6ec13ea49a72447045c45ea2837ba40e64e6741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993950"
---
# <a name="line-and-curve-attributes"></a>Linien-und Kurven Attribute

Ein Gerätekontext (DC) enthält Attribute, die sich auf die Zeilen-und Kurven Ausgabe auswirken. Die *Attribute "Line" und "Curve* " umfassen die aktuelle Position, den Pinsel Stil, die Pinsel Farbe, den Stift Stil, die Stift Farbe, die Transformation usw.

Die aktuelle Standardposition für einen beliebigen Domänen Controller befindet sich am Punkt (0,0) im logischen (oder Welt-) Raum. Sie können diese Koordinaten auf eine neue Position festlegen, indem Sie die Funktion " [**muvetoex**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) " aufrufen und einen neuen Satz von Koordinaten übergeben.

> [!Note]  
> Es gibt zwei Sätze von Zeilen-und Kurven Zeichnungsfunktionen. Der erste Satz behält die aktuelle Position in einem DC bei, und der zweite Satz ändert die Position. Sie können die Funktionen identifizieren, die die aktuelle Position ändern, indem Sie den Funktionsnamen untersuchen. Wenn der Funktionsname mit der Vorposition "to" endet, legt die Funktion die aktuelle Position auf den Endpunkt der letzten gezogenen Zeile fest ([**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto), [**ArcTo**](/windows/desktop/api/Wingdi/nf-wingdi-arcto), [**PolylineTo**](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)oder [**PolyBezierTo**](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)). Wenn der Funktionsname nicht mit dieser Vorposition endet, wird die aktuelle Position intakt gelassen ([**Bogen**](/windows/desktop/api/Wingdi/nf-wingdi-arc), [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)oder [**polybezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)).

 

Der Standard Pinsel ist ein volltoner Pinsel. Eine Anwendung kann einen neuen Pinsel erstellen, indem Sie die [**createbrushindirekte**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect) -Funktion aufrufen. Nachdem Sie einen Pinsel erstellt haben, kann die Anwendung ihn durch Aufrufen der [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion in seinen DC auswählen. Windows stellt einen kompletten Satz von Funktionen zum Erstellen, auswählen und Ändern des Pinsels im DC einer Anwendung bereit. Weitere Informationen zu diesen Funktionen und zu Pinsel im Allgemeinen finden Sie unter [Pinsel](brushes.md).

Der Standard Stift ist ein kosmetischer, solider schwarzer Stift, der ein Pixel breit ist. Eine Anwendung kann einen Stift mithilfe der [**extkreatepen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) -Funktion erstellen. Nachdem Sie einen Stift erstellt haben, kann die Anwendung ihn durch Aufrufen der [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion in seinen DC auswählen. Windows stellt einen kompletten Satz von Funktionen zum Erstellen, auswählen und Ändern des Stifts im DC einer Anwendung bereit. Weitere Informationen zu diesen Funktionen und zu den-Stiften im Allgemeinen finden Sie unter [Stifte](pens.md).

Die Standard Transformation ist die Unity-Transformation (angegeben durch die Identitätsmatrix). Eine Anwendung kann eine neue Transformation angeben, indem Sie die [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -Funktion aufruft. Windows bietet einen vollständigen Satz von Funktionen zum Transformieren von Linien und Kurven durch Ändern der Breite, Position und des allgemeinen Erscheinungs Bilds. Weitere Informationen zu diesen Funktionen finden Sie unter [Koordinaten Bereiche und Transformationen](coordinate-spaces-and-transformations.md).

 

 



