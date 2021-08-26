---
description: Die Layoutanalyse arbeitet mit einer Strokes-Auflistung und klassifiziert die Striche in Handschrift- und Zeichnungselemente. Das Divider-Objekt bietet Zugriff auf die Layoutanalysefeatures des Tablet-PCs.
ms.assetid: ac30d5c2-13a1-4f9e-a519-2bf428e21c75
title: Layoutanalyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8131859dd7e4c7bd6927db42bd605541001ac0f1222bfbf27b0e59809d4b7bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934820"
---
# <a name="layout-analysis"></a>Layoutanalyse

Die Layoutanalyse arbeitet mit einer [**Strokes-Auflistung**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) und klassifiziert die Striche in Handschrift- und Zeichnungselemente. Das [**Divider-Objekt**](inkdivider-class.md) bietet Zugriff auf die Layoutanalysefeatures des Tablet-PCs.

In der folgenden Tabelle werden die strukturellen Elementtypen der [**InkDivisionType-Enumeration**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) beschrieben, in die das [**Divider-Objekt**](inkdivider-class.md) Striche klassifiziert.



| type          | BESCHREIBUNG                                                                      |
|---------------|----------------------------------------------------------------------------------|
| **Segment**   | Ein Erkennungssegment.<br/>                                                |
| **Linie**      | Eine Handschriftzeile, die ein oder mehrere Erkennungssegmente enthält.<br/> |
| **Paragraph** | Ein Strichblock, der eine oder mehrere Handschriftzeilen enthält.<br/>    |
| **Zeichnung**   | Ink, die keine Handschrift ist.<br/>                                          |



 

Das [**Divider-Objekt**](inkdivider-class.md) verfügt über eine [**Strokes-Auflistung,**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) die das **Divider-Objekt** jedes Mal dynamisch analysiert, wenn Sie der Auflistung hinzufügen oder daraus löschen. Das **Divider-Objekt** ist nicht serialisierbar, und Sie können seinen Analysezustand nicht speichern. Daher ist **das Divider-Objekt** für Anwendungen konzipiert, die zwischen gemischter Handschrift und Zeicheneingabe unterscheiden müssen, aber keine großen Mengen von Ink zwischen Sitzungen neuanalysieren müssen.

Sie können eine statische Momentaufnahme des aktuellen Analyseergebnisses abrufen, die in einem [**DivisionResult-Objekt zurückgegeben**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) wird. Sie können [**DivisionUnit-Objekte**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) abrufen, die jeweils ein einzelnes strukturelles Element eines **DivisionResult-Objekts** darstellt. Die **Objekte DivisionResult** und **DivisionUnit** sind nicht serialisierbar. Es sind jedoch Zustandsinformationen aus diesen Objekten verfügbar.

Das [**Divider-Objekt**](inkdivider-class.md) funktioniert nur mit der Handschrift von links nach rechts. Damit das **Divider-Objekt** vertikale Sprachen wie Chinesisch richtig analysieren kann, müssen die Zeichen von links nach rechts anstatt von oben nach unten gezeichnet werden.

 

