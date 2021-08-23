---
title: Entwurfsphilosophie von Befehlswarteschlangen und Befehlslisten
description: Die Ziele, die Wiederverwendung von Renderingarbeit und Multithreadskalierung zu ermöglichen, erforderten grundlegende Änderungen an der Art und Weise, wie Direct3D-Apps Renderingarbeit an die GPU übermitteln.
ms.assetid: C85C8C41-2306-4568-8FAE-F57EDA624298
keywords:
- Befehlsliste
- bundle
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08f996f3de54b63668d44122929feb4fdbef4380fb8b2f7bb1458f50fe274ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124218"
---
# <a name="design-philosophy-of-command-queues-and-command-lists"></a>Entwurfsphilosophie von Befehlswarteschlangen und Befehlslisten

Die Ziele, die Wiederverwendung von Renderingarbeit und Multithreadskalierung zu ermöglichen, erforderten grundlegende Änderungen an der Art und Weise, wie Direct3D-Apps Renderingarbeit an die GPU übermitteln. In Direct3D 12 unterscheidet sich der Prozess der Übermittlung von Renderingarbeiten von früheren Versionen auf drei wichtige Arten:

<dl> 1. Beseitigung des unmittelbaren Kontexts. Dies ermöglicht Multithreading.  
2. Apps besitzen jetzt, wie Renderingaufrufe in GPU-Arbeitselemente (Graphics Processing Unit) gruppiert werden. Dies ermöglicht die Wiederverwendung.  
3. Apps steuern jetzt explizit, wann Arbeit an die GPU übermittelt wird. Dadurch werden die Elemente 1 und 2 aktiviert.  
</dl>

-   [Entfernen des unmittelbaren Kontexts](#removal-of-the-immediate-context)
-   [Gruppieren von GPU-Arbeitselementen](#grouping-of-gpu-work-items)
-   [GPU-Arbeitsübermittlung](#gpu-work-submission)
-   [Zugehörige Themen](#related-topics)

## <a name="removal-of-the-immediate-context"></a>Entfernen des unmittelbaren Kontexts

Die größte Änderung von Microsoft Direct3D 11 zu Microsoft Direct3D 12 besteht darin, dass einem Gerät kein einzelner, direkter Kontext mehr zugeordnet ist. Stattdessen erstellen Apps zum Rendern Befehlslisten, in denen herkömmliche Rendering-APIs aufgerufen werden können. Eine Befehlsliste ähnelt der Rendermethode einer Direct3D 11-App, die den unmittelbaren Kontext verwendet hat, da sie Aufrufe enthält, die Primitive zeichnen oder den Renderingzustand ändern. Wie bei unmittelbaren Kontexten ist jede Befehlsliste nicht mit Freethreading; mehrere Befehlslisten können jedoch gleichzeitig aufgezeichnet werden, wodurch moderne Mehrkernprozessoren genutzt werden.

Befehlslisten werden in der Regel einmal ausgeführt. Eine Befehlsliste kann jedoch mehrmals ausgeführt werden, wenn die Anwendung sicherstellt, dass die vorherigen Ausführungen abgeschlossen sind, bevor neue Ausführungen übermittelt werden. Weitere Informationen zur Befehlslistensynchronisierung finden Sie unter [Ausführen und Synchronisieren von Befehlslisten.](executing-and-synchronizing-command-lists.md)

## <a name="grouping-of-gpu-work-items"></a>Gruppieren von GPU-Arbeitselementen

Zusätzlich zu Befehlslisten nutzt Direct3D 12 die Funktionen, die derzeit auf der gesamten Hardware vorhanden sind, indem eine zweite Ebene von *Befehlslisten* hinzugefügt wird, die als Bundles bezeichnet werden. Um diese beiden Typen zu unterscheiden, können die Befehlslisten der ersten Ebene als *direkte Befehlslisten* bezeichnet werden. Der Zweck von Paketen besteht darin, Apps das Gruppieren einer kleinen Anzahl von API-Befehlen für eine spätere, wiederholte Ausführung aus direkten Befehlslisten zu ermöglichen. Zum Zeitpunkt der Erstellung eines Pakets führt der Treiber so viel Vorverarbeitung wie möglich aus, um die spätere Ausführung effizient zu gestalten. Bundles können dann innerhalb mehrerer Befehlslisten und mehrmals innerhalb derselben Befehlsliste ausgeführt werden.

Die Wiederverwendung von Paketen ist ein großer Treiber für verbesserte Effizienz mit einzelnen CPU-Threads. Da Bundles vorab verarbeitet werden und mehrmals übermittelt werden können, gibt es bestimmte Einschränkungen hinsichtlich der Vorgänge, die innerhalb eines Pakets ausgeführt werden können. Weitere Informationen finden Sie unter [Erstellen und Aufzeichnen von Befehlslisten und Paketen.](recording-command-lists-and-bundles.md)

## <a name="gpu-work-submission"></a>GPU-Arbeitsübermittlung

Um Aufgaben auf der GPU auszuführen, muss eine App explizit eine Befehlsliste an eine Befehlswarteschlange übermitteln, die dem Direct3D-Gerät zugeordnet ist. Eine Liste mit direkten Befehlen kann mehrmals zur Ausführung übermittelt werden, aber die App ist dafür verantwortlich, sicherzustellen, dass die Ausführung der Direktbefehlsliste auf der GPU abgeschlossen ist, bevor sie erneut übermittelt wird. Bundles weisen keine Einschränkungen bei gleichzeitiger Verwendung auf und können mehrmals in mehreren Befehlslisten ausgeführt werden. Bundles können jedoch nicht direkt zur Ausführung an eine Befehlswarteschlange übermittelt werden.

Jeder Thread kann jederzeit eine Befehlsliste an eine beliebige Befehlswarteschlange übermitteln, und die Runtime serialisiert die Übermittlung der Befehlsliste in der Befehlswarteschlange automatisch, während die Übermittlungsreihenfolge beibehalten wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeitsübermittlung in Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

 




