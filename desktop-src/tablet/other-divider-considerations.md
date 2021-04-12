---
description: 'Berücksichtigen Sie Folgendes, wenn Sie entscheiden, wann und wie das Divider-Objekt in einer Anwendung verwendet werden soll:'
ms.assetid: 17404789-7f08-4cf1-88f8-e1f70296c163
title: Weitere Überlegungen zu Trenn Punkten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e00ebc926dd51efb592304f6015351bdc2790b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216974"
---
# <a name="other-divider-considerations"></a>Weitere Überlegungen zu Trenn Punkten

Berücksichtigen Sie Folgendes, wenn Sie entscheiden, wann und wie das [**Divider**](inkdivider-class.md) -Objekt in einer Anwendung verwendet werden soll:

-   Das [**Divider**](inkdivider-class.md) -Objekt ist so konzipiert, dass Zeichnungen und Handschrift Blöcke getrennt werden, aber keine höheren Ebenen der Struktur erkannt werden, z. b. Tabellen oder Spalten.
-   Das [**Divider**](inkdivider-class.md) -Objekt stellt keine Schnittstellen speziell für die Korrektur der Ergebnisse der Layoutanalyse bereit.
-   Die Verwendung des Timeouts und der Anzahl der hubheuristiken zum Hinzufügen oder Entfernen mehrerer Striche gleichzeitig aus den Strichen im [**Divider**](inkdivider-class.md) -Objekt kann die Leistung verbessern.

## <a name="reanalysis-considerations"></a>Überlegungen zur erneuten Analyse

Wenn Sie in Erwägung ziehen, das [**Divider**](inkdivider-class.md) -Objekt in einer Anwendung zu verwenden, **in der möglich** erweise große Mengen von frei Hand Eingaben erneut analysiert werden müssen, beachten Sie Folgendes:

### <a name="retaining-copies-of-ink-and-strokes"></a>Beibehalten von Kopien von frei Hand Eingaben und Strichen

Eine Anwendung kann Kopien von " [**Ink**](inkdisp-class.md) "-und " [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) "-Objekten für Anwendungs Elemente aufbewahren, die später in der Anwendungs Sitzung wieder besucht werden können. Dadurch entfällt die Notwendigkeit, das **Ink** -Objekt erneut zu analysieren, wenn der Benutzer zum-Element zurückkehrt. Bei diesem Ansatz wird der Arbeitsspeicher für eine bessere Leistung betrieben.

### <a name="data-reduction-heuristics"></a>Heuristik zur Daten Reduzierung

Möglicherweise sind Sie in der Lage, die Analyseergebnisse als Anwendungsdaten aufzuzeichnen und Heuristik zu implementieren, um zu bestimmen, wann ein Satz von Strichen erneut analysiert werden muss. Diese Vorgehensweise würde die Notwendigkeit verringern, alle frei Hand Eingaben in der Anwendung zwischen Anwendungs Sitzungen erneut zu analysieren. Sie müssen jedoch sorgfältig vorgehen, um strukturelle Elementgrenzen beizubehalten oder alle Striche für betroffene Elemente erneut zu analysieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**InkDivider-Klasse**](inkdivider-class.md)
</dt> <dt>

[Microsoft. Ink. Divider-Klasse](/previous-versions/ms583616(v=vs.100))
</dt> </dl>

 

 
