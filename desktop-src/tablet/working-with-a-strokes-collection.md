---
description: Die Striche-Auflistung, die das Divider-Objekt analysiert, wird in der Striche-Eigenschaft des Divider-Objekts beibehalten.
ms.assetid: c2def964-6f2d-4b79-bfbf-a6719baf3c13
title: Arbeiten mit einer Striche-Auflistung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdeb03ce8168cec489dfed954a091f50f8d846d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344434"
---
# <a name="working-with-a-strokes-collection"></a>Arbeiten mit einer Striche-Auflistung

Die [**Striche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, die das [**Divider**](inkdivider-class.md) -Objekt analysiert, wird in der [**Striche**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) -Eigenschaft des **Divider** -Objekts beibehalten. Da eine **Striche** -Auflistung ein Verweis auf frei Hand Daten ist und nicht die eigentlichen Daten selbst ist, können Änderungen im übergeordneten [**Ink**](inkdisp-class.md) -Objekt der **Striche** -Auflistung die **Striche** -Auflistung für ungültig erklären. Weitere Informationen zu frei Hand Daten finden Sie unter frei Hand [Daten](ink-data.md). Weitere Informationen zur Freihand Auflistung finden Sie unter [Ink Collection](ink-collection.md).

Um die [**Striche**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) -Eigenschaft des [**Divider**](inkdivider-class.md) -Objekts mit einem [**Ink**](inkdisp-class.md) -Objekt zu synchronisieren, verwenden Sie die [**InkAdded**](inkdisp-inkadded.md) -und [**InkDeleted**](inkdisp-inkdeleted.md) -Ereignisse des **Ink** -Objekts, um Striche zu überwachen, die dem **Divider** -Objekt hinzugefügt oder daraus entfernt werden sollen. Dies umfasst Fälle, in denen Striche hinzugefügt, gelöscht, abgeschnitten oder **innerhalb des frei** Hand Objekts aufgeteilt werden. Durch verschieben, skalieren oder andere Transformationen bei Strichen im **Ink** -Objekt werden keine **InkAdded** -oder **InkDeleted** -Ereignisse generiert. Um eine solche Transformation in der **Striche** -Eigenschaft des **Divider** -Objekts widerzuspiegeln, führen Sie die gleiche Transformation für die Striche im **Divider** -Objekt aus.

Die [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) -Eigenschaft des [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) -Objekts enthält eine Kopie der Striche im [**Divider**](inkdivider-class.md) -Objekt zum Zeitpunkt der Erstellung des **DivisionResult** -Objekts. Sie können die **Striche** -Eigenschaften zweier **DivisionResult** -Objekte vergleichen, um zu bestimmen, ob sich die Striche zwischen den zwei Wiederholungen der [**Divide**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) -Methode geändert haben.

Die [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) -Eigenschaft des [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) -Objekts enthält die Teilmenge der Striche im [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) -Objekt, die diesem Element entsprechen. Sie können diese Striche an einen separaten [**Erkennungs Kontext**](inkrecognizercontext-class.md) übergeben, um ein Erkennungs Ergebnis für das Element zu erhalten. Da Handschrift Elemente auf unterschiedlichen Detailebenen vorhanden sind, können sich die [**Striche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistungen für unterschiedliche Elemente überlappen. Beispielsweise ist die **Striche** -Auflistung für ein Erkennungs Segment Element eine Teilmenge der **Striche** -Auflistung für das Line-Element, in dem das Erkennungs Segment ein Teil ist.

 

 
