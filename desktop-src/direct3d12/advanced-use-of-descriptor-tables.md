---
title: Erweiterte Verwendung von deskriptortabellen
description: In den folgenden Abschnitten finden Sie Informationen zur erweiterten Verwendung von deskriptortabellen.
ms.assetid: BB0CA29C-65CB-48B1-8351-EE13CC470B54
ms.date: 05/31/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: 79dad6914cff07726c2d40ed2ee27cccb6a0cf1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104641"
---
# <a name="advanced-use-of-descriptor-tables"></a>Erweiterte Verwendung von deskriptortabellen

In den folgenden Abschnitten finden Sie Informationen zur erweiterten Verwendung von deskriptortabellen.

-   [Ändern von deskriptortabelleneinträgen zwischen renderingaufrufen](#changing-descriptor-table-entries-between-rendering-calls)
-   [Indizierung außerhalb der Grenzen](#out-of-bounds-indexing)
-   [Shader-Ableitungen und abweichende Indizierung](#shader-derivatives-and-divergent-indexing)
-   [Verwandte Themen](#related-topics)

## <a name="changing-descriptor-table-entries-between-rendering-calls"></a>Ändern von deskriptortabelleneinträgen zwischen renderingaufrufen

Nachdem in der Befehlsliste festgelegt wurde, dass die deskriptortabellen für die Ausführung an eine Warteschlange gesendet wurden, darf die Anwendung die Teile der deskriptorheaps, auf die die GPU verweisen könnte, nicht aus der CPU bearbeiten, bis die Anwendung weiß, dass die GPU die Verwendung der Verweise abgeschlossen hat.

Der Abschluss des Vorgangs kann an einer eng gebundenen Grenze mithilfe von API-Zäunen für die Nachverfolgung des GPU-Status oder durch mehr grobe Mechanismen (z. b. das warten darauf, dass das Rendering an die Anzeige gesendet wurde) festgelegt werden. Wenn eine Anwendung weiß, dass nur eine Teilmenge des Bereichs, auf den eine Deskriptortabelle zeigt, zugegriffen wird (z.b. aufgrund der Fluss Steuerung im Shader), können die anderen Deskriptoren, auf die nicht verwiesen wird, weiterhin geändert werden. Wenn eine Anwendung zwischen den verschiedenen deskriptortabellen zwischen renderingaufrufen wechseln muss, gibt es einige Ansätze, aus denen die Anwendung wählen kann:

-   Deskriptor Table Versioning: erstellt (oder verwendet) eine separate Deskriptortabelle für jede eindeutige Auflistung von Deskriptoren, auf die von einer Befehlsliste verwiesen werden soll. Beim Bearbeiten und erneuten verwenden zuvor aufgefüllter Bereiche auf deskriptorheaps müssen Anwendungen zuerst sicherstellen, dass die GPU die Verwendung eines beliebigen Teils eines deskriptorheaps abgeschlossen hat, der wieder verwendet werden soll.
-   Dynamische Indizierung: Anwendungen können Objekte anordnen, die überzeichnen/verteilen (oder sogar innerhalb eines zeichnen) in einem Bereich eines deskriptorheaps variieren, eine Deskriptortabelle definieren, die alle umfasst, und aus dem Shader die dynamische Indizierung der Tabelle während der shaderausführung verwenden, um das zu verwendende Objekt auszuwählen.
-   Direktes Platzieren von Deskriptoren in der Stamm Signatur. Nur eine sehr kleine Anzahl von Deskriptoren kann auf diese Weise verwaltet werden, da der Stamm Signatur Bereich beschränkt ist.

Die Verwendung der deskriptortabellenversionierung besteht darin, dass der deskriptorspeicher aus einem deskriptorheap für jeden eindeutigen Satz von Deskriptoren, auf die von der Grafik Pipeline für jede Befehlsliste verwiesen wird, die entweder ausgeführt werden kann, in die Warteschlange eingereiht oder zu einem bestimmten Zeitpunkt aufgezeichnet werden kann, durchgebrannt werden muss.

D3D12 übernimmt die Verwaltung der Versionsverwaltung für die Anwendung für die Objekttypen, die über deskriptorheaps und deskriptortabellen verwaltet werden. Ein Vorteil besteht darin, dass Anwendungen den deskriptortabelleninhalt so weit wie möglich wieder verwenden können, anstatt immer eine neue deskriptortabellenversion für jede Übermittlung von Befehlslisten zu definieren. Bei der Stamm Signatur handelt es sich um ein Leerzeichen, das der D3D12-Treiber automatisch Versionen

Die Möglichkeit, mehrere deskriptortabellen gleichzeitig an die Stamm Signatur (und somit an die Pipeline) zu binden, ermöglicht es Anwendungen, Gruppen von deskriptorverweisen bei Bedarf zu gruppieren und zu wechseln. Eine Anwendung kann z. b. eine kleine Zahl (z. b. nur eine) von großen statischen deskriptortabellen verwenden, die selten geändert werden, oder in der die Bereiche im zugrunde liegenden deskriptorheap-Speicher nach Bedarf aufgefüllt werden, wobei die dynamische Indizierung aus dem Shader verwendet wird, um Texturen auszuwählen. Gleichzeitig kann die Anwendung eine andere Klasse von Ressourcen verwalten, in der die Gruppe, auf die von jedem Zeichnen-Befehl verwiesen wird, mithilfe der deskriptortable-versionierungstechnik von der CPU gewechselt wird.

## <a name="out-of-bounds-indexing"></a>Indizierung außerhalb der Grenzen

Die Indizierung einer beliebigen Deskriptortabelle aus dem Shader führt zu einem größtenteils undefinierten Speicherzugriff, einschließlich der Möglichkeit, beliebigen Prozess internen Speicher zu lesen, als ob es sich um einen Hardware Zustands Deskriptor handelt, der mit der Folge der Auswirkungen der Hardware zu tun hat. Dies kann zum Zurücksetzen des Geräts führen, stürzt jedoch nicht auf Windows ab.

## <a name="shader-derivatives-and-divergent-indexing"></a>Shader-Ableitungen und abweichende Indizierung

Wenn Pixel-Shader-Aufrufe, die in einem 2 x 2-Stempel ausgeführt werden (zur Unterstützung von abgeleiteten Berechnungen), verschiedene Textur Indizes auswählen, um aus einer Deskriptortabelle Stichproben zu erhalten. wenn die ausgewählte samplingkonfiguration und Textur für ein bestimmtes Pixel eine Lod-Berechnung aus Texturkoordinaten Ableitungen erfordert, werden die Lod-Berechnung und der Textur samplingprozess von der Hardware unabhängig für jede Textur Suche im 2 x 2-Stempel durchgeführt. , was sich auf die Leistung auswirkt.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Deskriptortabellen](descriptor-tables.md)
</dt> </dl>

 

 




