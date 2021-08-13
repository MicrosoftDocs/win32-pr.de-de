---
description: Die Vom Divider-Objekt analysierte Strokes-Auflistung wird in der Strokes-Eigenschaft des Divider-Objekts beibehalten.
ms.assetid: c2def964-6f2d-4b79-bfbf-a6719baf3c13
title: Arbeiten mit einer Strokes-Auflistung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35673ef17882f246969e7c74869f47b09b604195c74bb1456c3624713a42045d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119221870"
---
# <a name="working-with-a-strokes-collection"></a>Arbeiten mit einer Strokes-Auflistung

Die Vom [**Divider-Objekt**](inkdivider-class.md) [**analysierte Strokes-Auflistung**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) wird in der [**Strokes-Eigenschaft**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) des **Divider-Objekts** beibehalten. Da eine **Strokes-Auflistung** ein Verweis auf Ink-Daten und nicht die eigentlichen Daten selbst ist, können Änderungen im übergeordneten [**Ink-Objekt**](inkdisp-class.md) der **Strokes-Auflistung** die **Strokes-Auflistung** ungültig machen. Weitere Informationen zu Ink-Daten finden Sie unter [Ink Data](ink-data.md). Weitere Informationen zur Ink-Sammlung finden Sie unter [Ink Collection](ink-collection.md).

Um die [**Strokes-Eigenschaft**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) des [**Divider-Objekts**](inkdivider-class.md) mit einem [**Ink-Objekt**](inkdisp-class.md) synchronisiert zu lassen, verwenden Sie die Ereignisse [**InkAdded**](inkdisp-inkadded.md) und [**InkDeleted**](inkdisp-inkdeleted.md) des **Ink-Objekts,** um auf Striche zu lauschen, die dem **Divider-Objekt** hinzugefügt oder daraus entfernt werden sollen. Dies deckt Fälle ab, in denen Striche innerhalb des **Freihandobjekts** hinzugefügt, daraus gelöscht, abgeschnitten oder geteilt werden. Beim Verschieben, Skalieren oder anderen Transformationen für Striche im **Ink-Objekt** werden keine **InkAdded-** oder **InkDeleted-Ereignisse** generiert. Um eine solche Transformation in der **Strokes-Eigenschaft** des **Divider-Objekts** widerzuspiegeln, führen Sie dieselbe Transformation für die Striche im **Divider-Objekt** aus.

Die [**Strokes-Eigenschaft**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) des [**DivisionResult-Objekts**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) enthält eine Kopie der Striche im [**Divider-Objekt**](inkdivider-class.md) zum Zeitpunkt der Erstellung des **DivisionResult-Objekts.** Sie können die **Strokes-Eigenschaften** von zwei **DivisionResult-Objekten** vergleichen, um zu bestimmen, ob sich die Striche zwischen dem zweimaligen Aufruf der [**Divide-Methode**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) geändert haben.

Die [**Strokes-Eigenschaft**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) des [**DivisionUnit-Objekts**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) enthält die Teilmenge der Striche im [**DivisionResult-Objekt,**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) die diesem Element entsprechen. Sie können diese Striche an einen separaten [**RecognizerContext**](inkrecognizercontext-class.md) übergeben, um ein Erkennungsergebnis für das Element zu erhalten. Da Handschriftelemente auf unterschiedlichen Detailebenen vorhanden sind, können sich die [**Strichauflistungen**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) für verschiedene Elemente überlappen. Beispielsweise ist die Strokes-Auflistung für ein **Erkennungssegmentelement** eine Teilmenge der **Strokes-Auflistung** für das Linienelement, dessen Teil das Erkennungssegment ist.

 

 
