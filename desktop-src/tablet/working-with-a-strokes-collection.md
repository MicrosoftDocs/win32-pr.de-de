---
description: Die vom Divider-Objekt analysierte Strokes-Auflistung wird in der Strokes-Eigenschaft des Divider-Objekts beibehalten.
ms.assetid: c2def964-6f2d-4b79-bfbf-a6719baf3c13
title: Arbeiten mit einer Strichsammlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35673ef17882f246969e7c74869f47b09b604195c74bb1456c3624713a42045d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119221870"
---
# <a name="working-with-a-strokes-collection"></a>Arbeiten mit einer Strichsammlung

Die vom [**Divider-Objekt analysierte**](inkdivider-class.md) Strokes-Auflistung wird in der [**Strokes-Eigenschaft**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) des **Divider-Objekts** beibehalten. [](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) Da eine **Strokes-Auflistung** ein Verweis auf Ink-Daten ist und nicht die tatsächlichen Daten selbst sind, können Änderungen im übergeordneten [**Ink-Objekt**](inkdisp-class.md) der Strokes-Auflistung die **Strokes-Auflistung** ungültig machen.  Weitere Informationen zu Ink-Daten finden Sie unter [Ink Data](ink-data.md). Weitere Informationen zur Ink-Sammlung finden Sie unter [Ink Collection](ink-collection.md).

Um die [**Strokes-Eigenschaft**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) des [**Divider-Objekts**](inkdivider-class.md) mit einem [**Ink-Objekt**](inkdisp-class.md) synchronisiert zu halten, verwenden Sie die [**Ereignisse InkAdded**](inkdisp-inkadded.md) und [**InkDeleted des Ink-Objekts,**](inkdisp-inkdeleted.md) um auf Striche zu lauschen, die dem **Divider-Objekt** hinzugefügt oder daraus entfernt werden sollen.  Dies gilt für Fälle, in denen Striche innerhalb des Ink-Objekts hinzugefügt, daraus gelöscht, abgeschnitten oder **aufgeteilt** werden. Beim Verschieben, Skalieren oder anderen Transformationen für Striche im **Ink-Objekt** werden keine **InkAdded-** oder **InkDeleted-Ereignisse** generiert. Um eine solche Transformation in der **Strokes-Eigenschaft** des **Divider-Objekts** widerzubilden, führen Sie die gleiche Transformation für die Striche im **Divider-Objekt** aus.

Die [**Strokes-Eigenschaft**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) des [**DivisionResult-Objekts**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) enthält eine Kopie der Striche im [**Divider-Objekt**](inkdivider-class.md) zum Zeitpunkt der **DivisionResult-Objekt** erstellt wurde. Sie können die **Strokes-Eigenschaften** von zwei **DivisionResult-Objekten** vergleichen, um zu bestimmen, ob sich die Striche zwischen den beiden Aufrufen der [**Divide-Methode**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) geändert haben.

Die [**Strokes-Eigenschaft**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) des [**DivisionUnit-Objekts**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) enthält die Teilmenge der Striche im [**DivisionResult-Objekt,**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) die diesem Element entsprechen. Sie können diese Striche an einen separaten [**RecognizerContext**](inkrecognizercontext-class.md) übergeben, um ein Erkennungsergebnis für das Element zu erhalten. Da Handschriftelemente auf unterschiedlichen Detailebenen vorhanden sind, können sich die [**Strichsammlungen**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) für verschiedene Elemente überlappen. Die **Strokes-Auflistung** für ein Erkennungssegmentelement ist beispielsweise eine Teilmenge der Strokes-Auflistung für das Linienelement, dessen Teil das **Erkennungssegment** ist.

 

 
