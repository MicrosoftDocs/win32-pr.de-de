---
description: Die Layoutanalyse basiert auf einer Striche-Auflistung und klassifiziert die Striche in Handschrift-und Zeichnungs Elemente. Das Divider-Objekt ermöglicht den Zugriff auf die Features der Tablet PC-Layoutanalyse.
ms.assetid: ac30d5c2-13a1-4f9e-a519-2bf428e21c75
title: Layoutanalyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0901e7c7df96bec5ea3972f643469033fbb22ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351734"
---
# <a name="layout-analysis"></a>Layoutanalyse

Die Layoutanalyse basiert auf einer [**Striche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung und klassifiziert die Striche in Handschrift-und Zeichnungs Elemente. Das [**Divider**](inkdivider-class.md) -Objekt ermöglicht den Zugriff auf die Features der Tablet PC-Layoutanalyse.

In der folgenden Tabelle werden die strukturellen Elementtypen der [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) -Enumeration beschrieben, in die das unter [**Teiler**](inkdivider-class.md) -Objekt Striche klassifiziert.



| type          | BESCHREIBUNG                                                                      |
|---------------|----------------------------------------------------------------------------------|
| **Segment**   | Ein Erkennungs Segment.<br/>                                                |
| **Line**      | Eine Handschrift Zeile, die ein oder mehrere Erkennungs Segmente enthält.<br/> |
| **Paragraph** | Ein Block von Strichen, der eine oder mehrere Zeilen der Handschrift enthält.<br/>    |
| **Zeichnung**   | Frei Handschrift.<br/>                                          |



 

Das [**Divider**](inkdivider-class.md) -Objekt verfügt über eine [**Striche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, die das **Divider** -Objekt dynamisch analysiert, wenn Sie der Auflistung hinzufügen oder daraus löschen. Das **Divider** -Objekt ist nicht serialisierbar, und der Analyse Zustand kann nicht gespeichert werden. Folglich ist das **Divider** -Objekt für Anwendungen konzipiert, die zwischen gemischtem Handschrift und Zeichnungs Eingaben unterscheiden müssen, aber keine großen Mengen von frei Hand Eingaben zwischen den Sitzungen neu analysieren müssen.

Sie können eine statische Momentaufnahme des aktuellen Analyse Ergebnisses abrufen, die in einem [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) -Objekt zurückgegeben wird. Sie können [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) -Objekte abrufen, die jeweils ein einzelnes Strukturelement eines **DivisionResult** -Objekts darstellen. Die Objekte " **DivisionResult** " und " **DivisionUnit** " sind nicht serialisierbar. Zustandsinformationen aus diesen Objekten sind jedoch verfügbar.

Das [**Divider**](inkdivider-class.md) -Objekt funktioniert nur mit der Handschrift von links nach rechts. Damit das unter **Teiler** -Objekt vertikale Sprachen, wie z. b. Chinesisch, ordnungsgemäß analysieren kann, müssen die Zeichen von links nach rechts und nicht von oben nach unten gezeichnet werden.

 

