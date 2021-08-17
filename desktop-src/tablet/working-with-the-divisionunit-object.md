---
description: Das DivisionUnit-Objekt stellt ein einzelnes strukturelles Element eines DivisionResult-Objekts dar. Ein DivisionUnit-Objekt kann eine Zeichnung, ein einzelnes Erkennungssegment der Handschrift, eine Handschriftzeile oder einen Handschriftblock darstellen.
ms.assetid: 13f6121c-2b83-4788-9d06-460dc03094bf
title: Arbeiten mit dem DivisionUnit-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c2ce09bf2b67f5724bba523219d0555063c3f7215810d3b11c48596f979fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966509"
---
# <a name="working-with-the-divisionunit-object"></a>Arbeiten mit dem DivisionUnit-Objekt

Das **DivisionUnit-Objekt** stellt ein einzelnes strukturelles Element eines **DivisionResult-Objekts** dar. Ein **DivisionUnit-Objekt** kann eine Zeichnung, ein einzelnes Erkennungssegment der Handschrift, eine Handschriftzeile oder einen Handschriftblock darstellen.

Die [**InkDivisionType-Enumeration**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) definiert die strukturellen Elementtypen, die von der Layoutanalyse erkannt werden. In Automation heißt das **DivisionUnit-Objekt** [**IInkDivisionUnit.**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit)

Die [**DivisionType-Eigenschaft**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_divisiontype) des **DivisionUnit-Objekts** gibt den strukturellen Elementtyp zurück, der das **DivisionUnit-Objekt** ist. Die [**RecognitionString-Eigenschaft**](/previous-versions/windows/desktop/legacy/ms703283(v=vs.85)) des **DivisionUnit-Objekts** gibt den Erkennungstext für Handschriftelemente oder **NULL** für Zeichnungselemente zurück.

Die [**Strokes-Eigenschaft**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) des **DivisionUnit-Objekts** enthält die Teilmenge der Striche im **DivisionResult-Objekt,** die diesem Element entsprechen. Da Handschriftelemente für verschiedene Detailebenen vorhanden sind, können sich die **Strichauflistungen** für verschiedene Elemente überlappen. Insbesondere teilt sich ein Erkennungssegment Striche mit der Linie und dem Block, zu dem es gehört, und eine Linie teilt Striche mit dem Block, zu dem es gehört.

Die [**RotationTransform-Eigenschaft**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_rotationtransform) des **DivisionUnit-Objekts** gibt eine Matrix zum Drehen der Striche des Elements in horizontal zurück. Für Absatz- und Zeichnungselemente gibt die **RotationTransform-Eigenschaft** die Identitätsmatrix zurück. Eine Texterkennung funktioniert bei der horizontal ausgerichteten Handschrift viel besser als bei handschriftlichen Texten, die nicht horizontal ausgerichtet sind. In Automation wird dies als **RotationTransform-Eigenschaft** bezeichnet und gibt ein [**InkTransform-Objekt**](inktransform-class.md) zurück, das die Transformationsmatrix enthält. Die **RotationTransform-Eigenschaft** gibt **NULL** für Absatz- und Zeichnungselemente zurück.

Weitere Informationen zum **DivisionResult-Objekt** finden Sie unter [Arbeiten mit dem DivisionResult-Objekt.](working-with-the-divisionresult-object.md)

 

 
