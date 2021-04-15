---
description: Das Divider-Objekt stellt layoutanalysefunktionen bereit, die Striche klassifizieren und in verschiedene Strukturelemente gruppieren.
ms.assetid: 9e4ed24f-4451-431c-9f0f-2f1c4f5e5084
title: Ink-Analyse mit dem Divider-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f1df175f8746e56cf6ebd1b222b3901fbef36e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525316"
---
# <a name="ink-analysis-with-the-divider-object"></a>Ink-Analyse mit dem Divider-Objekt

Das [Divider](/previous-versions/ms583616(v=vs.100)) -Objekt stellt layoutanalysefunktionen bereit, die Striche klassifizieren und in verschiedene Strukturelemente gruppieren.

## <a name="divider-object"></a>Divider-Objekt

Das [Divider](/previous-versions/ms583616(v=vs.100)) -Objekt analysiert Striche beim Hinzufügen oder entfernen. Sie können die aktuelle Klassifizierung und Gruppierung der analysierten Striche in einem [DivisionResult](/previous-versions/ms583620(v=vs.100)) -Objekt abrufen, indem Sie die [Divide](/previous-versions/ms568936(v=vs.100)) -Methode des Divider-Objekts aufrufen.

Die vom [Divider](/previous-versions/ms583616(v=vs.100)) -Objekt analysierten Striche werden in der [Striche](/previous-versions/ms582090(v=vs.100)) -Eigenschaft des Divider-Objekts beibehalten. Da eine [Striche](/previous-versions/ms552701(v=vs.100)) -Auflistung ein Verweis auf frei Hand Daten ist und nicht die eigentlichen Daten selbst ist, können Änderungen im übergeordneten [Ink](/previous-versions/ms583670(v=vs.100)) -Objekt der Striche-Auflistung die Striche-Auflistung für ungültig erklären. Weitere Informationen zu frei Hand Daten finden Sie unter frei Hand [Daten](ink-data.md).

Das [Divider](/previous-versions/ms583616(v=vs.100)) -Objekt verwendet einen Erkennungs Kontext, um die Analyse der Erkennungs Segmente zu verbessern und Erkennungs Text für Handschrift Elemente zu generieren. Wenn der Erkennungs [Kontext](/previous-versions/ms582089(v=vs.100)) -Eigenschaft des unter Teiler-Objekts kein Erkennungs Kontext zugewiesen ist oder die Erkennungs Tools nicht installiert sind, führt das layoutanalysefeature die Division des Erkennungs Segments aus, und dem [DivisionResult](/previous-versions/ms583620(v=vs.100)) -Objekt ist kein Text zugeordnet. Weitere Informationen zur frei Handerkennung finden Sie unter frei Hand [Erkennung](ink-recognition.md).

## <a name="divisionresult-object"></a>DivisionResult-Objekt

Jedes [DivisionResult](/previous-versions/ms583620(v=vs.100)) -Objekt zeichnet die Layoutanalyse der Striche auf, die zum Zeitpunkt des Aufrufs der [Divide](/previous-versions/ms568936(v=vs.100)) -Methode im [Divider](/previous-versions/ms583616(v=vs.100)) -Objekt enthalten sind. Das DivisionResult-Objekt speichert außerdem eine Kopie der Striche, die in der Analyse verwendet wurden.

Das [DivisionResult](/previous-versions/ms583620(v=vs.100)) -Objekt gruppiert die Analyseergebnisse nach Struktur Elementtyp. Die [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) -Methode des DivisionResult-Objekts gibt in einer [DivisionUnits](/previous-versions/ms583625(v=vs.100)) -Auflistung die Auflistung aller strukturellen Elemente eines bestimmten Typs zurück. Die [InkDivisionType](/previous-versions/ms552251(v=vs.100)) -Enumeration definiert die Elementtypen, die von der Layoutanalyse erkannt werden.

In der folgenden Tabelle werden die Elementtypen in der [InkDivisionType](/previous-versions/ms552251(v=vs.100)) -Enumeration beschrieben.



| Name                 | BESCHREIBUNG                                                                      |
|----------------------|----------------------------------------------------------------------------------|
| Segment<br/>   | Ein Erkennungs Segment.<br/>                                                |
| Zeile<br/>      | Eine Handschrift Zeile, die ein oder mehrere Erkennungs Segmente enthält.<br/> |
| Paragraph<br/> | Ein Block von Strichen, der eine oder mehrere Zeilen der Handschrift enthält.<br/>    |
| Zeichnung<br/>   | Freihand, die kein Text ist.<br/>                                                 |



 

Die folgende Abbildung zeigt ein Beispiel für die unterschiedlichen Elementtypen, die vom [DivisionResult](/previous-versions/ms583620(v=vs.100)) -Objekt erkannt werden.

![Abbildung der unterschiedlichen Elementtypen, die vom DivisionResult-Objekt erkannt werden](images/5f2ab955-1f74-4b71-b3ba-8d1ca23e0578.gif)

## <a name="divisionunits-collection-and-divisionunit-objects"></a>DivisionUnits Collection-und DivisionUnit-Objekte

Jede [DivisionUnits](/previous-versions/ms583625(v=vs.100)) -Auflistung ist eine Kopie des layoutanalyseergebnisses für einen einzelnen Typ von strukturiertem Element. Das [DivisionUnit](/previous-versions/ms583624(v=vs.100)) -Objekt stellt ein einzelnes Element in der DivisionUnits-Auflistung dar. Jedes Strukturelement verfügt über einen Verweis auf die Striche, die das-Element bilden. Wenn Erkennungs Tools installiert sind, ist der Erkennungs Text für Handschrift Elemente verfügbar. Zeilen-und Erkennungs Segment Elemente enthalten außerdem eine Rotations Matrix, mit der die Striche eines Elements von vertikal zu horizontal gedreht werden können.

Das " [Ink Divider](ink-divider-sample.md) "-Beispiel Thema veranschaulicht, wie ein [Divider](/previous-versions/ms583616(v=vs.100)) -Objekt mit [Ink](/previous-versions/ms583670(v=vs.100)) -Objekten verwendet wird, um eine frei Hand Layout-Analyse auszuführen

Weitere Informationen zur Verwendung der Ink-Analyse finden Sie [unter Divider-Objekt](the-divider-object.md).

 

