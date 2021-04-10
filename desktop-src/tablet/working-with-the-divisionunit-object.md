---
description: Das DivisionUnit-Objekt stellt ein einzelnes Strukturelement eines DivisionResult-Objekts dar. Ein DivisionUnit-Objekt kann eine Zeichnung, ein einzelnes Erkennungs Segment von Handschrift, eine Handschrift Zeile oder einen Hand schriftblock darstellen.
ms.assetid: 13f6121c-2b83-4788-9d06-460dc03094bf
title: Arbeiten mit dem DivisionUnit-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade8b617ae8e64c2641ef53a628a44e72e4fc35f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862483"
---
# <a name="working-with-the-divisionunit-object"></a>Arbeiten mit dem DivisionUnit-Objekt

Das **DivisionUnit** -Objekt stellt ein einzelnes Strukturelement eines **DivisionResult** -Objekts dar. Ein **DivisionUnit** -Objekt kann eine Zeichnung, ein einzelnes Erkennungs Segment von Handschrift, eine Handschrift Zeile oder einen Hand schriftblock darstellen.

Die [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) -Enumeration definiert die Strukturelement Typen, die von der Layoutanalyse erkannt werden. In Automation wird das **DivisionUnit** -Objekt als [**iinkdivisionunit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit)bezeichnet.

Die [**DivisionType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_divisiontype) -Eigenschaft des **DivisionUnit** -Objekts gibt den strukturellen Elementtyp zurück, den das **DivisionUnit** -Objekt ist. Die [**erkenntionstring**](/previous-versions/windows/desktop/legacy/ms703283(v=vs.85)) -Eigenschaft des **DivisionUnit** -Objekts gibt den Erkennungs Text für Handschrift Elemente oder **null** für Zeichnungs Elemente zurück.

Die [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) -Eigenschaft des **DivisionUnit** -Objekts enthält die Teilmenge der Striche im **DivisionResult** -Objekt, die diesem Element entsprechen. Da Handschrift Elemente für verschiedene Detailebenen vorhanden sind, können sich die **Striche** -Auflistungen für unterschiedliche Elemente überlappen. Insbesondere gibt ein Erkennungs Segment Striche mit der Zeile frei und sperrt Sie als Teil von, und eine Zeile teilt Striche mit dem Block, zu dem Sie gehört.

Die [**RotationTransform**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_rotationtransform) -Eigenschaft des **DivisionUnit** -Objekts gibt eine Matrix zum Drehen der Striche des Elements auf Horizontal zurück. Für Absatz-und Zeichnungs Elemente gibt die **RotationTransform** -Eigenschaft die Identitätsmatrix zurück. Eine Texterkennung ist viel besser bei der Handschrift, die horizontal ausgerichtet ist als bei der Handschrift, die nicht ist. In Automation wird dies als **RotationTransform** -Eigenschaft bezeichnet und gibt ein [**inktransform**](inktransform-class.md) -Objekt zurück, das die Transformationsmatrix enthält. Die **RotationTransform** -Eigenschaft gibt **null** für Absatz-und Zeichnungs Elemente zurück.

Weitere Informationen zum **DivisionResult** -Objekt finden Sie unter [Arbeiten mit dem DivisionResult-Objekt](working-with-the-divisionresult-object.md).

 

 
