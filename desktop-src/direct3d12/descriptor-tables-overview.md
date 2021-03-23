---
title: Übersicht über deskriptortabellen
description: 'Jede Deskriptortabelle speichert Deskriptoren von einem oder mehreren Typen: Srvs, uave, cbvs und Samplers. Eine Deskriptortabelle ist keine Speicher Belegung. Es handelt sich einfach um einen Offset und eine Länge in einem deskriptorheap.'
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d446a0570cf813eacaa4d036781e8cd4b8def3c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105151"
---
# <a name="descriptor-tables-overview"></a>Übersicht über deskriptortabellen

Jede Deskriptortabelle speichert Deskriptoren von einem oder mehreren Typen: Srvs, uave, cbvs und Samplers. Eine Deskriptortabelle ist keine Speicher Belegung. Es handelt sich einfach um einen Offset und eine Länge in einem deskriptorheap.

-   [Verweisen auf deskriptortabellen](#referencing-descriptor-tables)
-   [Verwandte Themen](#related-topics)

## <a name="referencing-descriptor-tables"></a>Verweisen auf deskriptortabellen

Die Grafik Pipeline durch die Stamm Signatur erhält Zugriff auf Ressourcen, indem Sie über den Index auf deskriptortabellen verweist.

Eine Deskriptortabelle ist tatsächlich nur ein Unterbereich eines deskriptorheaps. Deskriptorheaps stellen die zugrunde liegende Speicher Belegung für eine Auflistung von Deskriptoren dar. Da die Speicher Belegung eine Eigenschaft eines-Objekts ist, das einen deskriptorheap erstellt, ist die Definition einer Deskriptortabelle aus einer Tabelle garantiert so kostengünstig wie die Identifizierung eines Bereichs im Heap für die Hardware. Deskriptortabellen müssen nicht auf API-Ebene erstellt oder zerstört werden – Sie werden nur für Treiber als Offset und Größe aus einem Heap identifiziert, wenn auf Sie verwiesen wird.

Es ist durchaus möglich, dass eine APP sehr große deskriptortabellen definiert, wenn deren Shader eine Vielzahl von verfügbaren Deskriptoren (häufig auf Texturen verweisen) im laufenden Betrieb (möglicherweise durch Materialdaten) auswählen möchten.

Die Stamm Signatur verweist auf den deskriptortabelleneintrag mit einem Verweis auf den Heap, die Startposition der Tabelle (ein Offset vom Beginn des Heaps) und die Länge (in Einträgen) der Tabelle. Die folgende Abbildung zeigt die folgenden Konzepte: die deskriptortabellenzeiger aus der Stamm Signatur und die Deskriptoren im deskriptorheap, die auf die vollständige Textur oder die Puffer Daten in einem uploadheap verweisen.

![deskriptortabellen](images/descriptor-table.png)

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Deskriptortabellen](descriptor-tables.md)
</dt> </dl>

 

 




