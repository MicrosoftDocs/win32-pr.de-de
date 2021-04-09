---
title: Skalierbarkeit
description: Skalierbarkeit
ms.assetid: 39327621-b536-4494-9319-9e9d4f534123
keywords:
- Skalierbarkeit
- Remote Prozedur Aufruf RPC, bewährte Methoden, Skalierbarkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0728e35d9c9b27494014363c448be9965e39eea7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856736"
---
# <a name="scalability"></a>Skalierbarkeit

Der Begriff "Skalierbarkeit" wird häufig missbraucht. In diesem Abschnitt wird eine Dual Definition bereitgestellt:

-   Skalierbarkeit ist die Möglichkeit, die verfügbare Verarbeitungsleistung auf einem Multiprozessorsystem (2, 4, 8, 32 oder mehr Prozessoren) vollständig zu nutzen.
-   Skalierbarkeit ist die Fähigkeit, eine große Anzahl von Clients zu bedienen.

Diese beiden verknüpften Definitionen werden im Allgemeinen als zentrales *hochskalieren* bezeichnet. Am Ende dieses Themas finden Sie Tipps zum horizontalen hoch *skalieren*.

Diese Erörterung konzentriert sich ausschließlich auf das Schreiben skalierbarer Server, nicht auf skalierbare Clients, da skalierbare Server häufiger Anforderungen sind. In diesem Abschnitt wird auch die Skalierbarkeit nur im Kontext von RPC-und RPC-Servern behandelt. Bewährte Methoden für die Skalierbarkeit, wie z. b. das Reduzieren von Konflikten, das Vermeiden häufiger Cache Fehler an globalen Speicherorten oder die Vermeidung von falsch Freigaben, werden hier nicht erläutert.

## <a name="rpc-threading-model"></a>RPC-Threading Modell

Wenn ein RPC-Aufruf von einem Server empfangen wird, wird die Server Routine (Manager-Routine) in einem Thread aufgerufen, der von RPC bereitgestellt wird. RPC verwendet einen adaptiven Thread Pool, der zunimmt und abnimmt, wenn die Arbeitsauslastung zunimmt. Ab Windows 2000 ist der Kern des RPC-Thread Pools ein Abschlussport. Der Abschlussport und seine Verwendung durch RPC sind auf Server Routinen mit Null bis zu niedrigem Konflikt optimiert. Dies bedeutet, dass der RPC-Thread Pool die Anzahl der Arbeitsthreads aggressiv erhöht, wenn einige blockiert werden. Es wird auf die Annahme angewendet, dass die Blockierung selten vorkommt, und wenn ein Thread blockiert wird, ist dies eine vorübergehende Bedingung, die schnell aufgelöst werden kann. Dieser Ansatz ermöglicht die Effizienz für Server mit geringem Konflikt. Beispielsweise wird ein void-RPC-Server, der auf einem Server mit acht Prozessoren mit 550 MHz ausgeführt wird und auf den über eine hoch Geschwindigkeits System Area Network (San) zugegriffen wird, über 30.000 void-Aufrufe pro Sekunde von über 200 Remote Clients bedient. Dies entspricht mehr als 108 Millionen Aufrufen pro Stunde.

Das Ergebnis ist, dass der aggressive Thread Pool tatsächlich auf den Weg kommt, wenn die Konflikte auf dem Server hoch sind. Stellen Sie sich zur Veranschaulichung einen Hochleistungsserver vor, der für den Remote Zugriff auf Dateien verwendet wird. Angenommen der Server übernimmt den einfachsten Ansatz: die Datei wird einfach synchron in dem Thread gelesen/geschrieben, auf dem die Server Routine von RPC aufgerufen wird. Angenommen, wir verfügen über einen Server mit vier Prozessoren, der viele Clients bedient.

Der Server beginnt mit fünf Threads (Dies variiert tatsächlich, aber fünf Threads werden aus Gründen der Einfachheit verwendet). Nachdem RPC den ersten RPC-Aufruf übernommen hat, sendet er den Aufruf an die Server Routine, und die Server Routine gibt den e/a-Vorgang aus. In den meisten Fällen wird der Dateicache nicht ausgeführt, und das warten auf das Ergebnis wird blockiert. Sobald es blockiert wird, wird der fünfte Thread freigegeben, um eine Anforderung zu übernehmen, und ein sechster Thread wird als Hot Standby erstellt. Wenn bei jedem zehnten e/a-Vorgang der Cache fehlschlägt und für 100 Millisekunden (einen willkürlichen Uhrzeitwert) blockiert wird und vorausgesetzt wird, dass der Server mit vier Prozessoren ungefähr 20.000 Anrufe pro Sekunde bedient (5.000 Anrufe pro Prozessor), würde eine vereinfachte Modellierung Vorhersagen, dass jeder Prozessor ungefähr 50 Threads erzeugt. Dabei wird davon ausgegangen, dass ein-Vorgang blockiert wird, der alle 2 Millisekunden blockiert wird, und nach 100 Millisekunden wird der erste Thread erneut freigegeben, sodass sich der Pool bei ungefähr 200 Threads (50 pro Prozessor) stabilisiert.

Das tatsächliche Verhalten ist komplizierter, da die große Anzahl von Threads zusätzliche Kontextwechsel zur Verlangsamung des Servers verursacht und auch die Rate der Erstellung neuer Threads verlangsamt, aber die grundlegende Idee ist eindeutig. Die Anzahl der Threads wird schnell beschleunigt, wenn Threads auf dem Server blockieren und auf etwas (e/a-Vorgänge oder Zugriff auf eine Ressource) warten.

RPC und der Abschlussport, der eingehende Anforderungen Gates, wird versuchen, die Anzahl der verwendbaren RPC-Threads auf dem Server so zu verwalten, dass Sie mit der Anzahl der Prozessoren auf dem Computer identisch sind. Dies bedeutet, dass auf einem Server mit vier Prozessoren, sobald ein Thread zu RPC zurückkehrt, der fünfte Thread nicht in der Lage ist, eine neue Anforderung zu übernehmen, und sich stattdessen im aktiven Standbymodus befindet, wenn einer der aktuell verwendbaren Threads blockiert wird. Wenn der fünfte Thread lange genug als Hot Standby wartet, ohne dass die Anzahl der verwendbaren RPC-Threads unter der Anzahl der Prozessoren liegt, wird er freigegeben, d. h., der Thread Pool wird verringert.

Stellen Sie sich einen Server mit vielen Threads vor. Wie bereits erläutert, wird ein RPC-Server mit vielen Threads beendet, aber nur, wenn die Threads häufig blockiert werden. Auf einem Server, auf dem Threads oft blockieren, wird ein Thread, der zu RPC zurückkehrt, bald aus der Liste der aktiven standbyvorgänge entfernt, da alle gegenwärtig verwendbaren Threads blockiert werden und eine Anforderung zur Verarbeitung erhalten. Wenn ein Thread blockiert wird, wechselt der Thread Verteiler im Kernel in den Kontext zu einem anderen Thread. Dieser Kontextwechsel selbst beansprucht CPU-Zyklen. Der nächste Thread führt einen anderen Code aus, greift auf verschiedene Datenstrukturen zu und verfügt über einen anderen Stapel. Dies bedeutet, dass die Speicher Cache-Treffer Rate (L1-und L2-Caches) erheblich geringer ist, was zu einer langsameren Ausführung führt. Die zahlreichen Threads, die gleichzeitig ausgeführt werden, erhöhen Konflikte für vorhandene Ressourcen, z. b. Heap, kritische Abschnitte im Servercode usw. Dadurch erhöht sich der Konflikt als Konvois im Ressourcen Formular. Wenn nicht genügend Arbeitsspeicher verfügbar ist, verursacht der Arbeitsspeicher Mangel, der durch die große und wachsende Anzahl von Threads verursacht wird, Seiten Fehler, wodurch die Rate, mit der der Thread blockiert wird, weiter erhöht wird und noch mehr Threads erstellt werden. Je nachdem, wie oft es blockiert wird und wie viel physischer Arbeitsspeicher verfügbar ist, kann sich der Server entweder auf einer niedrigeren Leistungsstufe mit einer hohen Kontextwechsel Rate stabilisieren, oder es kann zu dem Punkt, an dem er nur wiederholt auf die Festplatte und den Kontextwechsel zugreift, ohne wirkliche Arbeitsschritte beeinträchtigt werden. Diese Situation wird natürlich nicht unter Licht Arbeitsauslastung angezeigt, aber eine hohe Arbeitsauslastung bringt das Problem schnell auf die Oberfläche.

Wie kann dies verhindert werden? Wenn die Blockierung von Threads zu erwarten ist, deklarieren Sie Aufrufe als asynchron, und sobald die Anforderung in die Server Routine eintritt, stellen Sie Sie in eine Warteschlange für einen Pool von Arbeitsthreads, die die asynchronen Funktionen des e/a-Systems und/oder RPC verwenden. Wenn der Server seinerseits RPC-Aufrufe durchführt, machen Sie diese asynchron, und stellen Sie sicher, dass die Warteschlange nicht zu groß wird. Wenn die Server Routine Datei-e/a-Vorgänge ausführt, verwenden Sie asynchrone Datei-e/a-Vorgänge, um mehrere Anforderungen an das e/a-System in die Warteschlange zu stellen und die Ergebnisse in die Warteschlange aufzunehmen. Wenn die Server Routine Netzwerk-e/a-Vorgänge durchführen, verwenden Sie die asynchronen Funktionen des Systems, um die Anforderungen auszugeben, und übernehmen Sie die Antworten asynchron, und verwenden Sie so wenige Threads wie möglich. Wenn die e/a-Vorgänge abgeschlossen sind oder der vom Server ausgeführte RPC-Aufruf abgeschlossen ist, vervollständigen Sie den asynchronen RPC-Aufruf, der die Anforderung übermittelt hat. Auf diese Weise kann der Server mit möglichst wenigen Threads ausgeführt werden, wodurch die Leistung und die Anzahl der Clients, die ein Server bedienen kann, erhöht werden.

## <a name="scale-out"></a>Aufskalieren

RPC kann so konfiguriert werden, dass er mit Netzwerk Lastenausgleich (NLB) funktioniert, wenn der Netzwerk Lastenausgleich so konfiguriert ist, dass alle Anforderungen von einer bestimmten Client Adresse an denselben Server weitergeleitet werden. Da jeder RPC-Client einen Verbindungspool öffnet (Weitere Informationen finden Sie unter [RPC und das Netzwerk](rpc-and-the-network.md)), ist es von entscheidender Bedeutung, dass alle Verbindungen aus dem Pool des angegebenen Clients auf demselben Server Computer enden. Solange diese Bedingung erfüllt ist, kann ein NLB-Cluster so konfiguriert werden, dass er als ein großer RPC-Server mit möglicherweise hervorragender Skalierbarkeit funktioniert.

 

 




