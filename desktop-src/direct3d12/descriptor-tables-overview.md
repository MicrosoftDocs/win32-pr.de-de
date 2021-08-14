---
title: Übersicht über Deskriptortabellen
description: 'Jede Deskriptortabelle speichert Deskriptoren eines oder mehrerer Typen: SRVs, UAVe, CBVs und Samplers. Eine Deskriptortabelle ist keine Speicherbelegung. es ist einfach ein Offset und eine Länge in einem Deskriptorheap.'
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da614063f5584369009367c03d0b087b808a60eb0979f1bfad07af128280ee25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098100"
---
# <a name="descriptor-tables-overview"></a>Übersicht über Deskriptortabellen

Jede Deskriptortabelle speichert Deskriptoren eines oder mehrerer Typen &mdash; von SRVs, UAVe, CBVs und Samplern. Eine Deskriptortabelle ist keine Speicherbelegung. es ist einfach ein Offset und eine Länge in einem Deskriptorheap.

## <a name="referencing-descriptor-tables"></a>Verweisen auf Deskriptortabellen

Die Grafikpipeline erhält über die Stammsignatur Zugriff auf Ressourcen, indem sie nach Index in Deskriptortabellen verweist.

Eine Deskriptortabelle ist eigentlich nur ein Unterbereich eines Deskriptorheaps. Deskriptorheaps stellen die zugrunde liegende Speicherbelegung für eine Auflistung von Deskriptoren dar. Da die Speicherbelegung eine Eigenschaft eines Erstellens eines Deskriptorheaps ist, ist die Definition einer Deskriptortabelle aus einer Tabelle garantiert so kostengünstig wie die Identifizierung eines Bereichs im Heap für die Hardware. Deskriptortabellen müssen nicht auf API-Ebene erstellt oder zerstört werden. Sie werden den Treibern lediglich als Offset und Größe aus einem Heap identifiziert, wenn darauf verwiesen wird.

Es ist durchaus möglich, dass eine App sehr große Deskriptortabellen definiert, wenn ihre Shader die Auswahl aus einer großen Menge verfügbarer Deskriptoren (die häufig auf Texturen verweisen) während der Zeit (möglicherweise durch Materialdaten gesteuert) auswählen möchten.

Die Stammsignatur verweist auf den Deskriptortabelleneintrag mit einem Verweis auf den Heap, der Startposition der Tabelle (einem Offset vom Anfang des Heaps) und der Länge (in Einträgen) der Tabelle. Die folgende Abbildung zeigt diese Konzepte: die Deskriptortabellenzeiger aus der Stammsignatur und die Deskriptoren im Deskriptorheap, die auf die vollständige Textur oder die Pufferdaten in einem Heap verweisen (im Fall einer Textur der Standardheap).

![Deskriptortabellen](images/descriptor-table.png)

## <a name="related-topics"></a>Zugehörige Themen

* [Deskriptortabellen](descriptor-tables.md)
