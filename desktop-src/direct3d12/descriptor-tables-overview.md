---
title: Übersicht über Deskriptortabellen
description: 'In jeder Deskriptortabelle werden Deskriptoren eines oder mehrere Typen gespeichert: SRVs, UAVe, CBVs und Sampler. Eine Deskriptortabelle ist keine Speicherzuweisung. es handelt sich lediglich um einen Offset und eine Länge in einem Deskriptorhap.'
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3edae00c37a451aa0fb71355a1dea5860de4398f
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813114"
---
# <a name="descriptor-tables-overview"></a>Übersicht über Deskriptortabellen

Jede Deskriptortabelle speichert Deskriptoren eines oder mehrere Typen &mdash; von SRVs, UAVe, CBVs und Samplern. Eine Deskriptortabelle ist keine Speicherzuweisung. es ist einfach ein Offset und eine Länge in einem Deskriptorhap.

## <a name="referencing-descriptor-tables"></a>Verweisen auf Deskriptortabellen

Die Grafikpipeline hat über die Stammsignatur Zugriff auf Ressourcen, indem sie nach Index in Deskriptortabellen referenziert.

Eine Deskriptortabelle ist eigentlich nur ein Unterbereich eines Deskriptor-Heaps. Deskriptor-Heaps stellen die zugrunde liegende Speicherzuordnung für eine Auflistung von Deskriptoren dar. Da die Speicherbelegung eine Eigenschaft eines ist, die einen Deskriptor-Heap erstellt, ist es garantiert so kostengünstig, eine Deskriptortabelle zu definieren, wie eine Region im Heap für die Hardware zu identifizieren. Deskriptortabellen müssen nicht auf API-Ebene erstellt oder zerstört werden. Sie werden treibern lediglich als Offset und Größe aus einem Heap identifiziert, wenn darauf verwiesen wird.

Es ist sicherlich möglich, dass eine App sehr große Deskriptortabellen definiert, wenn ihre Shader die Möglichkeit haben möchten, aus einer vielzahl verfügbaren Deskriptoren (häufig referenzierend auf Texturen) direkt auszuwählen (möglicherweise durch Materialdaten gesteuert).

Die Stammsignatur verweist auf den Deskriptortabelleneintrag mit einem Verweis auf den Heap, der Startposition der Tabelle (ein Offset vom Anfang des Heaps) und der Länge (in Einträgen) der Tabelle. Die folgende Abbildung zeigt diese Konzepte: die Deskriptortabellenzeder aus der Stammsignatur und die Deskriptoren innerhalb des Deskriptor-Heaps, die auf die vollständige Textur oder die Pufferdaten in einem Heap verweisen (im Fall einer Textur der Standardhap).

![Deskriptortabellen](images/descriptor-table.png)

## <a name="related-topics"></a>Zugehörige Themen

* [Deskriptortabellen](descriptor-tables.md)
