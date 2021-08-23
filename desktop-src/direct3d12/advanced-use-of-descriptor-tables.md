---
title: Erweiterte Verwendung von Deskriptortabellen
description: Die folgenden Abschnitte enthalten Informationen zur erweiterten Verwendung von Deskriptortabellen.
ms.assetid: BB0CA29C-65CB-48B1-8351-EE13CC470B54
ms.date: 05/31/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: 044c02b87591f7ad53212ce37d7549ade68308a648092a260a67c97395959c98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632590"
---
# <a name="advanced-use-of-descriptor-tables"></a>Erweiterte Verwendung von Deskriptortabellen

Die folgenden Abschnitte enthalten Informationen zur erweiterten Verwendung von Deskriptortabellen.

-   [Ändern von Deskriptortabelleneinträgen zwischen Renderingaufrufen](#changing-descriptor-table-entries-between-rendering-calls)
-   [Out-of-Bounds-Indizierung](#out-of-bounds-indexing)
-   [Shader-Ableitungen und abweichende Indizierung](#shader-derivatives-and-divergent-indexing)
-   [Zugehörige Themen](#related-topics)

## <a name="changing-descriptor-table-entries-between-rendering-calls"></a>Ändern von Deskriptortabelleneinträgen zwischen Renderingaufrufen

Nachdem Befehlslisten, die Deskriptortabellen festlegen, zur Ausführung an eine Warteschlange übermittelt wurden, darf die Anwendung die Teile der Deskriptorheaps, auf die die GPU verweisen kann, nicht von der CPU bearbeiten, bis die Anwendung weiß, dass die GPU die Verweise verwendet hat.

Die Arbeitsvervollständigung kann mithilfe von API-Zäunen zur Nachverfolgung des GPU-Fortschritts oder mit weiteren groben Mechanismen wie dem Warten darauf, dass das Rendering zur Anzeige gesendet wurde, bestimmt werden – unabhängig davon, was für die Anwendung geeignet ist. Wenn eine Anwendung weiß, dass nur auf eine Teilmenge des Bereichs, auf den eine Deskriptortabelle verweist , zugegriffen wird (z. B. aufgrund der Flusssteuerung im Shader), können die anderen nicht zurückgestellten Deskriptoren weiterhin geändert werden. Wenn eine Anwendung zwischen verschiedenen Deskriptortabellen zwischen Renderingaufrufen wechseln muss, gibt es einige Ansätze, aus denen die Anwendung wählen kann:

-   Versionsangabe für Deskriptortabellen: Erstellen (oder wiederverwenden) Sie eine separate Deskriptortabelle für jede eindeutige Auflistung von Deskriptoren, auf die von einer Befehlsliste verwiesen werden soll. Beim Bearbeiten und Wiederverwenden zuvor aufgefüllter Bereiche auf Deskriptorheaps müssen Anwendungen zunächst sicherstellen, dass die GPU alle Teile eines Deskriptorheaps verwendet, der wiederverwendet wird.
-   Dynamische Indizierung: Anwendungen können Objekte anordnen, die sich über Draw/Dispatch (oder sogar innerhalb eines Draws) in einem Bereich eines Deskriptorheaps unterscheiden, eine Deskriptortabelle definieren, die sich über alle Bereiche erstreckt, und über den Shader die dynamische Indizierung der Tabelle während der Shaderausführung verwenden, um auszuwählen, welches Objekt verwendet werden soll.
-   Direktes Setzen von Deskriptoren in die Stammsignatur. Auf diese Weise kann nur eine sehr kleine Anzahl von Deskriptoren verwaltet werden, da der Stammsignaturbereich begrenzt ist.

Die Verwendung der Deskriptortabellenversionsierung impliziert, dass der Deskriptorspeicher eines Deskriptorheaps für jeden eindeutigen Satz von Deskriptoren, auf den von der Grafikpipeline verwiesen wird, für jede Befehlsliste, die entweder ausgeführt werden kann, zur Ausführung in die Warteschlange eingereiht oder zu einem beliebigen Zeitpunkt aufgezeichnet wird, durchlaufen werden muss.

D3D12 überlässt die Verwaltung der Versionsverwaltung der Anwendung für die Objekttypen, die über Deskriptorheaps und Deskriptortabellen verwaltet werden. Ein Vorteil besteht darin, dass Anwendungen deskriptortabelleninhalte so weit wie möglich wiederverwenden können, anstatt immer eine neue Deskriptortabellenversion für jede Befehlslistenübermittlung zu definieren. Die Stammsignatur ist ein Bereich, den der D3D12-Treiber automatisch erstellt.

Die Möglichkeit, mehrere Deskriptortabellen gleichzeitig an die Stammsignatur (und somit an die Pipeline) zu binden, ermöglicht Anwendungen das Gruppieren und Wechseln von Deskriptorverweisen in unterschiedlichen Häufigkeiten, falls gewünscht. Beispielsweise könnte eine Anwendung eine kleine Zahl (vielleicht nur eine) großer statischer Deskriptortabellen verwenden, die sich nur selten ändern, oder in welchen Bereichen im zugrunde liegenden Deskriptorheapspeicher nach Bedarf aufgefüllt wird, wobei die dynamische Indizierung vom Shader zum Auswählen von Texturen verwendet wird. Gleichzeitig könnte die Anwendung eine weitere Klasse von Ressourcen verwalten, bei der die Menge, auf die durch jeden Draw-Aufruf verwiesen wird, mithilfe der Deskriptortabellenversionsverwaltung von der CPU gewechselt wird.

## <a name="out-of-bounds-indexing"></a>Out-of-Bounds-Indizierung

Die Indizierung außerhalb der Grenzen einer Deskriptortabelle aus dem Shader führt zu einem größtenteils nicht definierten Speicherzugriff, einschließlich der Möglichkeit, beliebigen In-Process-Speicher zu lesen, als wäre es ein Hardwarezustandsdeskriptor, der mit dem Ergebnis der Hardwarearbeit arbeitet. Dies kann zu einer Geräterücksetzung führen, stürzt jedoch nicht Windows ab.

## <a name="shader-derivatives-and-divergent-indexing"></a>Shader-Ableitungen und abweichende Indizierung

Wenn Pixel-Shaderaufrufe, die in einem 2x2-Stempel ausgeführt werden (um abgeleitete Berechnungen zu unterstützen), verschiedene Texturindizes auswählen, die aus einer Deskriptortabelle entnommen werden sollen, und wenn die ausgewählte Samplerkonfiguration und -textur für ein bestimmtes Pixel eine LOD-Berechnung aus Texturkoordinatenableitungen erfordert, erfolgt die LOD-Berechnung und Textursampling unabhängig von der Hardware für jede Textursuche im 2x2-Stempel.  Dies wirkt sich auf die Leistung aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deskriptortabellen](descriptor-tables.md)
</dt> </dl>

 

 




