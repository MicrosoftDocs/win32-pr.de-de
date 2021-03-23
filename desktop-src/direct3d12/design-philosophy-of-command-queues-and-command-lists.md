---
title: Entwurfs Philosophie von Befehls Warteschlangen und Befehlslisten
description: Die Ziele der Aktivierung der Wiederverwendung von renderingarbeiten und der Multithread-Skalierung erforderten grundlegende Änderungen an der Art und Weise, wie Direct3D apps renderingarbeit an die GPU
ms.assetid: C85C8C41-2306-4568-8FAE-F57EDA624298
keywords:
- Befehlsliste
- bundle
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812275a630464dbe9137d587a672803f4d0c72f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103403"
---
# <a name="design-philosophy-of-command-queues-and-command-lists"></a>Entwurfs Philosophie von Befehls Warteschlangen und Befehlslisten

Die Ziele der Aktivierung der Wiederverwendung von renderingarbeiten und der Multithread-Skalierung erforderten grundlegende Änderungen an der Art und Weise, wie Direct3D apps renderingarbeit an die GPU In Direct3D 12 unterscheidet sich der Prozess der Übermittlung von renderingarbeiten von früheren Versionen auf drei wichtige Arten:

<dl> 1. Beseitigung des unmittelbaren Kontexts. Dies ermöglicht das Multithreading.  
2. Apps sind jetzt für die Gruppierung von renderingaufrufen in GPU-Arbeitsaufgaben (Graphics Processing Unit) geeignet. Dies ermöglicht die Wiederverwendung.  
3. Apps steuern nun explizit, wann die Arbeit an die GPU übermittelt wird. Dies ermöglicht die Elemente 1 und 2.  
</dl>

-   [Entfernen des unmittelbaren Kontexts](#removal-of-the-immediate-context)
-   [Gruppieren von GPU-Arbeits Elementen](#grouping-of-gpu-work-items)
-   [GPU-Arbeits Übermittlung](#gpu-work-submission)
-   [Verwandte Themen](#related-topics)

## <a name="removal-of-the-immediate-context"></a>Entfernen des unmittelbaren Kontexts

Die größte Änderung von Microsoft Direct3D 11 zu Microsoft Direct3D 12 besteht darin, dass ein einzelnes, unmittelbares Kontext mit einem Gerät nicht mehr vorhanden ist. Stattdessen erstellen Apps zum Rendern Befehlslisten, in denen herkömmliche Rendering-APIs aufgerufen werden können. Eine Befehlsliste ähnelt der Renderingmethode einer Direct3D 11-APP, die den unmittelbaren Kontext verwendet, in dem Sie Aufrufe enthält, die primitive zeichnen oder den renderingstatus ändern. Wie bei unmittelbaren Kontexten ist jede Befehlsliste nicht frei Thread. Es können jedoch mehrere Befehlslisten gleichzeitig aufgezeichnet werden, was die Vorteile moderner, Multikern-Prozessoren nutzt.

Befehlslisten werden in der Regel einmal ausgeführt. Eine Befehlsliste kann jedoch mehrmals ausgeführt werden, wenn die Anwendung sicherstellt, dass die vorherigen Ausführungen abgeschlossen sind, bevor neue Ausführungen übermittelt werden. Weitere Informationen zur Synchronisierung von Befehlslisten finden Sie unter [ausführen und Synchronisieren von Befehlslisten](executing-and-synchronizing-command-lists.md).

## <a name="grouping-of-gpu-work-items"></a>Gruppieren von GPU-Arbeits Elementen

Zusätzlich zu den Befehlslisten nutzt Direct3D 12 die Funktionen, die heute in der gesamten Hardware vorhanden sind, indem eine zweite Ebene von Befehlslisten hinzugefügt wird, die als *Bündel* bezeichnet werden. Um diese beiden Typen zu unterscheiden, können die Befehlslisten der ersten Ebene als *direkte Befehlslisten* bezeichnet werden. Der Zweck von Paketen besteht darin, dass apps eine kleine Anzahl von API-Befehlen zur späteren wiederholten Ausführung in direkten Befehlslisten gruppieren können. Zum Zeitpunkt der Erstellung eines Pakets führt der Treiber so viel Vorverarbeitung wie möglich aus, um eine spätere Ausführung zu ermöglichen. Pakete können dann in mehreren Befehlslisten und mehrmals innerhalb derselben Befehlsliste ausgeführt werden.

Die Wiederverwendung von Paketen ist ein großer Treiber für eine höhere Effizienz mit einzelnen CPU-Threads. Da Pakete vorab verarbeitet werden und mehrmals übermittelt werden können, gibt es bestimmte Einschränkungen hinsichtlich der Vorgänge, die innerhalb eines Pakets ausgeführt werden können. Weitere Informationen finden Sie unter [Erstellen und Aufzeichnen von Befehlslisten und Paketen](recording-command-lists-and-bundles.md).

## <a name="gpu-work-submission"></a>GPU-Arbeits Übermittlung

Um die Arbeit auf der GPU auszuführen, muss eine APP explizit eine Befehlsliste an eine Befehls Warteschlange senden, die dem Direct3D-Gerät zugeordnet ist. Eine direkte Befehlsliste kann mehrmals zur Ausführung übermittelt werden, aber die APP ist dafür verantwortlich, sicherzustellen, dass die Ausführung der direkten Befehlsliste auf der GPU abgeschlossen ist, bevor Sie erneut gesendet wird. Bündel haben keine Einschränkungen für die gleichzeitige Verwendung und können mehrmals in mehreren Befehlslisten ausgeführt werden, aber Pakete können nicht direkt zur Ausführung an eine Befehls Warteschlange übermittelt werden.

Jeder Thread kann jederzeit eine Befehlsliste an eine beliebige Befehls Warteschlange senden, und die Laufzeit serialisiert die Übermittlung der Befehlsliste automatisch in der Befehls Warteschlange, während die Übermittlungs Reihenfolge beibehalten wird.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Arbeits Übermittlung in Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

 




