---
description: Das Divider-Objekt stellt Layoutanalysefeatures zur Verfügung, die Striche in verschiedene Strukturelemente klassifizieren und gruppieren.
ms.assetid: 9e4ed24f-4451-431c-9f0f-2f1c4f5e5084
title: Ink-Analyse mit dem Divider-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d036428bbe32c42e6419c2218e6196a0b89a892137e55d141d5553d360c0a652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939555"
---
# <a name="ink-analysis-with-the-divider-object"></a>Ink-Analyse mit dem Divider-Objekt

Das [Divider-Objekt](/previous-versions/ms583616(v=vs.100)) stellt Layoutanalysefeatures zur Verfügung, die Striche in verschiedene Strukturelemente klassifizieren und gruppieren.

## <a name="divider-object"></a>Divider-Objekt

Das [Divider-Objekt](/previous-versions/ms583616(v=vs.100)) analysiert Striche, wenn Sie sie hinzufügen oder entfernen. Sie können die aktuelle Klassifizierung und Gruppierung der analysierten Striche in einem [DivisionResult-Objekt](/previous-versions/ms583620(v=vs.100)) abrufen, indem Sie die [Divide-Methode](/previous-versions/ms568936(v=vs.100)) des Divider-Objekts aufrufen.

Die vom [Divider-Objekt analysierten](/previous-versions/ms583616(v=vs.100)) Striche werden in der [Strokes-Eigenschaft](/previous-versions/ms582090(v=vs.100)) des Divider-Objekts beibehalten. Da eine [Strokes-Auflistung](/previous-versions/ms552701(v=vs.100)) ein Verweis auf Ink-Daten ist und nicht die tatsächlichen Daten selbst sind, können Änderungen im übergeordneten [Ink-Objekt](/previous-versions/ms583670(v=vs.100)) der Strokes-Auflistung die Strokes-Auflistung ungültig machen. Weitere Informationen zu Ink-Daten finden Sie unter [Ink Data](ink-data.md).

Das [Divider-Objekt](/previous-versions/ms583616(v=vs.100)) verwendet einen Erkennungskontext, um die Analyse von Erkennungssegmenten zu verbessern und Erkennungstext für Handschriftelemente zu generieren. Wenn der [RecognizerContext-Eigenschaft](/previous-versions/ms582089(v=vs.100)) des Divider-Objekts kein Erkennungskontext zugewiesen ist oder keine Erkennungen installiert sind, führt die Layoutanalysefunktion die Erkennungssegmentaufteilung aus, und dem [DivisionResult-Objekt](/previous-versions/ms583620(v=vs.100)) ist kein Text zugeordnet. Weitere Informationen zur Ink-Erkennung finden Sie unter [Ink Recognition](ink-recognition.md).

## <a name="divisionresult-object"></a>DivisionResult-Objekt

Jedes [DivisionResult-Objekt](/previous-versions/ms583620(v=vs.100)) zeichnet die Layoutanalyse der Striche auf, die zum Zeitpunkt des Aufrufens der Divide-Methode im [Divider-Objekt](/previous-versions/ms583616(v=vs.100)) enthalten sind. [](/previous-versions/ms568936(v=vs.100)) Das DivisionResult-Objekt speichert auch eine Kopie der Striche, die in der Analyse verwendet wurden.

Das [DivisionResult-Objekt](/previous-versions/ms583620(v=vs.100)) unterteilt die Analyseergebnisse nach strukturellem Elementtyp. Die [**ResultByType-Methode**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) des DivisionResult-Objekts gibt in einer [DivisionUnits-Auflistung](/previous-versions/ms583625(v=vs.100)) die Auflistung aller strukturellen Elemente eines bestimmten Typs zurück. Die [InkDivisionType-Enumeration](/previous-versions/ms552251(v=vs.100)) definiert die Elementtypen, die von der Layoutanalyse erkannt werden.

In der folgenden Tabelle werden die Elementtypen in der [InkDivisionType-Enumeration](/previous-versions/ms552251(v=vs.100)) beschrieben.



| Name                 | BESCHREIBUNG                                                                      |
|----------------------|----------------------------------------------------------------------------------|
| Segment<br/>   | Ein Erkennungssegment.<br/>                                                |
| Linie<br/>      | Eine Handschriftzeile, die ein oder mehrere Erkennungssegmente enthält.<br/> |
| Paragraph<br/> | Ein Strichblock, der eine oder mehrere Handschriftzeilen enthält.<br/>    |
| Zeichnung<br/>   | Ink, die kein Text ist.<br/>                                                 |



 

Die folgende Abbildung zeigt ein Beispiel für die verschiedenen Elementtypen, die das [DivisionResult-Objekt](/previous-versions/ms583620(v=vs.100)) erkennt.

![Abbildung der verschiedenen Elementtypen, die das divisionresult-Objekt erkennt](images/5f2ab955-1f74-4b71-b3ba-8d1ca23e0578.gif)

## <a name="divisionunits-collection-and-divisionunit-objects"></a>DivisionUnits-Auflistung und DivisionUnit-Objekte

Jede [DivisionUnits-Auflistung](/previous-versions/ms583625(v=vs.100)) ist eine Kopie des Layoutanalyseergebnis für einen einzelnen Typ von strukturellen Element. Das [DivisionUnit-Objekt](/previous-versions/ms583624(v=vs.100)) stellt ein einzelnes Element in der DivisionUnits-Auflistung dar. Jedes strukturelle Element verfügt über einen Verweis auf die Striche, die das Element enthalten. Wenn Erkennungen installiert sind, steht Handschriftelementen Erkennungstext zur Verfügung. Linien- und Erkennungssegmentelemente enthalten auch eine Drehungsmatrix, die die Striche eines Elements von vertikal zu horizontal drehen kann.

Im [Thema Ink Divider Sample wird](ink-divider-sample.md) veranschaulicht, wie ein [Divider-Objekt](/previous-versions/ms583616(v=vs.100)) mit Ink-Objekten verwendet wird, um eine [Ink-Layoutanalyse](/previous-versions/ms583670(v=vs.100)) durchzuführen.

Weitere Informationen zur Verwendung der Ink-Analyse finden Sie unter [The Divider Object](the-divider-object.md).

 

