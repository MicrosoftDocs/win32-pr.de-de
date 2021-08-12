---
description: 'Berücksichtigen Sie bei der Entscheidung, wann und wie das Divider-Objekt in einer Anwendung verwendet werden soll, Folgendes:'
ms.assetid: 17404789-7f08-4cf1-88f8-e1f70296c163
title: Überlegungen zu anderen Divisionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3328fd553a16aeee1e1dfa5459b78a45732a55494e0481950d730dab7ce0d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449360"
---
# <a name="other-divider-considerations"></a>Überlegungen zu anderen Divisionen

Berücksichtigen Sie bei der Entscheidung, wann und wie das [**Divider-Objekt**](inkdivider-class.md) in einer Anwendung verwendet werden soll, Folgendes:

-   Das [**Divider-Objekt**](inkdivider-class.md) dient zum Trennen von Zeichnungen und Handschriftblöcken, aber nicht zum Erkennen höherer Strukturebenen wie Tabellen oder Spalten.
-   Das [**Divider-Objekt**](inkdivider-class.md) stellt keine Schnittstellen bereit, die speziell für die Korrektur der Ergebnisse der Layoutanalyse vorgesehen sind.
-   Die Verwendung von Timeout und Anzahl von Strichhuristiken, um mehrere Striche gleichzeitig aus den Strichen im [**Divider-Objekt**](inkdivider-class.md) hinzuzufügen oder zu entfernen, kann die Leistung verbessern.

## <a name="reanalysis-considerations"></a>Überlegungen zur Neuanalyse

Wenn Sie erwägen, das [**Divider-Objekt**](inkdivider-class.md) in einer Anwendung zu verwenden, in der das **Divider-Objekt** möglicherweise große Mengen an Ink neu untersuchen muss, beachten Sie Folgendes.

### <a name="retaining-copies-of-ink-and-strokes"></a>Beibehalten von Kopien von Ink und Strichen

Eine Anwendung kann Kopien von [**Ink-**](inkdisp-class.md) und [**DivisionResult-Objekten**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) für Anwendungselemente speichern, die später in der Anwendungssitzung erneut verwendet werden können. Dadurch entfällt die Notwendigkeit, das **Ink-Objekt** neu zu prüfen, wenn der Benutzer zum -Element zurückkehrt. Dieser Ansatz tauscht Arbeitsspeicher aus, um eine bessere Leistung zu erzielen.

### <a name="data-reduction-heuristics"></a>Heuristik zur Datenverringerung

Möglicherweise können Sie die Analyseergebnisse als Anwendungsdaten aufzeichnen und Heuristik implementieren, um zu bestimmen, wann eine Reihe von Strichen neu analysiert werden soll. Diese Vorgehensweise würde die Notwendigkeit reduzieren, alle Ink-Dateien in der Anwendung zwischen Anwendungssitzungen neu zuanalysieren. Es muss jedoch darauf geachtet werden, strukturelle Elementgrenzen beizubehalten oder alle Striche für die betroffenen Elemente neu zu prüfen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**InkDivider-Klasse**](inkdivider-class.md)
</dt> <dt>

[Microsoft.Ink.Divider-Klasse](/previous-versions/ms583616(v=vs.100))
</dt> </dl>

 

 
