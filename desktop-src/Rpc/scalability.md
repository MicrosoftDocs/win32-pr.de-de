---
title: Skalierbarkeit
description: Skalierbarkeit
ms.assetid: 39327621-b536-4494-9319-9e9d4f534123
keywords:
- Skalierbarkeit
- Remoteprozeduraufruf-RPC, bewährte Methoden, Skalierbarkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2a004a5ce3adb0f27e2e31071cac69fc1c34bfc650c618dcf39b3c8ebc954f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018060"
---
# <a name="scalability"></a>Skalierbarkeit

Der Begriff Skalierbarkeit wird häufig missbraucht. Für diesen Abschnitt wird eine duale Definition bereitgestellt:

-   Skalierbarkeit ist die Fähigkeit, die verfügbare Verarbeitungsleistung auf einem Multiprozessorsystem (2, 4, 8, 32 oder mehr Prozessoren) vollständig zu nutzen.
-   Skalierbarkeit ist die Fähigkeit, eine große Anzahl von Clients zu unterstützen.

Diese beiden verwandten Definitionen werden häufig als *hochskalieren bezeichnet.* Am Ende dieses Themas finden Sie Tipps zum *horizontalen Hochskalieren* von .

Diese Diskussion konzentriert sich ausschließlich auf das Schreiben skalierbarer Server, nicht auf skalierbare Clients, da skalierbare Server häufigere Anforderungen sind. In diesem Abschnitt wird auch die Skalierbarkeit nur im Kontext von RPC- und RPC-Servern behandelt. Bewährte Methoden für die Skalierbarkeit, z. B. das Reduzieren von Konflikte, das Vermeiden häufiger Cache-Fehler an globalen Speicherorten oder das Vermeiden falscher Freigaben, werden hier nicht erläutert.

## <a name="rpc-threading-model"></a>RPC-Threadingmodell

Wenn ein RPC-Aufruf von einem Server empfangen wird, wird die Serverroutine (Managerroutine) für einen von RPC bereitgestellten Thread aufgerufen. RPC verwendet einen adaptiven Threadpool, der bei schwankender Workload erhöht und verringert wird. Ab Windows 2000 ist der Kern des RPC-Threadpools ein Abschlussport. Der Vervollständigungsport und seine Verwendung durch RPC sind für Serverroutinen mit null bis geringem Inhalt optimiert. Dies bedeutet, dass der RPC-Threadpool die Anzahl der Wartungsthreads aggressiv erhöht, wenn einige blockiert werden. Dies ist eine vorübergehende Bedingung, die schnell behoben werden kann, wenn ein Thread blockiert wird. Dieser Ansatz ermöglicht die Effizienz für Server mit geringem Inhalt. Ein void-Aufruf-RPC-Server, der auf einem 550 MHz-Server mit acht Prozessoren ausgeführt wird, auf den über ein San (High Speed System Area Network) zugegriffen wird, bedient beispielsweise über 30.000 void-Aufrufe pro Sekunde von über 200 Remoteclients. Dies stellt mehr als 108 Millionen Aufrufe pro Stunde dar.

Das Ergebnis ist, dass der aggressive Threadpool tatsächlich im Weg steht, wenn der Server einen hohen Inhalt hat. Stellen Sie sich zur Veranschaulichung einen Hochleistungsserver vor, der für den Remotezugriff auf Dateien verwendet wird. Angenommen, der Server verfolgt den unkompliziertesten Ansatz: Er liest/schreibt die Datei einfach synchron in dem Thread, in dem der RPC die Serverroutine aufruft. Nehmen wir außerdem an, dass wir über einen Server mit vier Prozessoren verfügen, der viele Clients bedient.

Der Server beginnt mit fünf Threads (dies variiert tatsächlich, aber der Einfachheit halber werden fünf Threads verwendet). Sobald RPC den ersten RPC-Aufruf abruft, wird der Aufruf an die Serverroutine gesendet, und die Serverroutine gibt die E/A aus. Selten wird der Dateicache übersehen, und das Warten auf das Ergebnis wird blockiert. Sobald er blockiert wird, wird der fünfte Thread freigegeben, um eine Anforderung zu erhalten, und ein sechster Thread wird als hot standby erstellt. Wenn bei jedem zehnten E/A-Vorgang der Cache fehlt und 100 Millisekunden (ein beliebiger Zeitwert) blockiert wird und der Server mit vier Prozessoren etwa 20.000 Aufrufe pro Sekunde (5.000 Aufrufe pro Prozessor) bedient, würde eine einfache Modellierung vorhersagen, dass jeder Prozessor ungefähr 50 Threads erstellt. Dabei wird von einem Aufruf ausgegangen, der alle 2 Millisekunden blockiert wird, und nach 100 Millisekunden wird der erste Thread wieder frei, sodass sich der Pool bei etwa 200 Threads (50 pro Prozessor) stabilisiert.

Das tatsächliche Verhalten ist komplizierter, da die hohe Anzahl von Threads zusätzliche Kontextwechsel verursacht, die den Server verlangsamen und auch die Rate der Erstellung neuer Threads verlangsamen, aber die Grundidee ist klar. Die Anzahl der Threads steigt schnell an, wenn Threads auf dem Server blockieren und auf etwas warten (sei es eine E/A oder der Zugriff auf eine Ressource).

RPC und der Abschlussport, der eingehende Anforderungen abfängt, versuchen, die Anzahl der nutzbaren RPC-Threads auf dem Server so zu halten, dass sie der Anzahl der Prozessoren auf dem Computer entspricht. Dies bedeutet, dass der fünfte Thread auf einem Server mit vier Prozessoren, sobald ein Thread zu RPC zurückkehrt, bei vier oder mehr nutzbaren RPC-Threads keine neue Anforderung empfangen darf und sich stattdessen im Zustand "Hot Standby" befindet, falls einer der derzeit nutzbaren Threads blockiert wird. Wenn der fünfte Thread lange genug als hot-Standby wartet, ohne dass die Anzahl der nutzbaren RPC-Threads unter die Anzahl der Prozessoren fällt, wird er freigegeben, d.&a; der Threadpool verringert sich.

Imagine einen Server mit vielen Threads. Wie bereits erläutert, hat ein RPC-Server viele Threads, aber nur, wenn die Threads häufig blockiert werden. Auf einem Server, auf dem Threads häufig blockiert werden, wird ein Thread, der zu RPC zurückkehrt, bald aus der Hot Standby-Liste genommen, da alle derzeit nutzbaren Threads blockiert werden und eine Anforderung zur Verarbeitung erhalten wird. Wenn ein Thread blockiert wird, wechselt der Thread dispatcher im Kernel den Kontext zu einem anderen Thread. Dieser Kontextwechsel allein verbraucht CPU-Zyklen. Der nächste Thread führt unterschiedlichen Code aus, greifen auf verschiedene Datenstrukturen zu und hat einen anderen Stapel, was bedeutet, dass die Trefferrate des Arbeitsspeichercaches (die L1- und L2-Caches) viel niedriger ist, was zu einer langsameren Ausführung führt. Die zahlreichen Threads, die gleichzeitig ausgeführt werden, erhöhen den Inhalt bestehender Ressourcen, z. B. Heap, kritische Abschnitte im Servercode und so weiter. Dies erhöht auch die Auswendigung von Konvois im Ressourcenformular. Wenn der Arbeitsspeicher gering ist, verursacht die hohe Arbeitsspeicherleistung, die durch die große und wachsende Anzahl von Threads entsteht, Seitenfehler, wodurch die Rate, mit der die Threads blockiert werden, weiter erhöht wird und noch mehr Threads erstellt werden. Je nachdem, wie oft blockiert wird und wie viel physischer Arbeitsspeicher verfügbar ist, kann sich der Server entweder auf einer niedrigeren Leistungsstufe mit einer hohen Kontextwechselrate stabilisiert oder zu dem Punkt führen, an dem er nur wiederholt auf die Festplatte und den Kontextwechsel zusteuert, ohne tatsächlich arbeiten zu müssen. Diese Situation zeigt sich natürlich nicht unter einer geringen Workload, aber eine hohe Workload bringt das Problem schnell ans Licht.

Wie kann dies verhindert werden? Wenn threads blockiert werden sollen, deklarieren Sie Aufrufe als asynchron, und sobald die Anforderung in die Serverroutine eintritt, stellen Sie sie in einen Pool von Arbeitsthreads ein, die die asynchronen Funktionen des E/A-Systems und/oder RPC verwenden. Wenn der Server wiederum RPC-Aufrufe sendet, werden diese asynchron, und stellen Sie sicher, dass die Warteschlange nicht zu groß wird. Wenn die Serverroutine Datei-E/A-Vorgänge vor sich hat, verwenden Sie asynchrone Datei-E/A, um mehrere Anforderungen an das E/A-System in die Warteschlange zu stellen und nur wenige Threads in die Warteschlange zu stellen und die Ergebnisse zu erhalten. Wenn die Serverroutine Netzwerk-E/A-Vorgänge vor sich hat, verwenden Sie erneut die asynchronen Funktionen des Systems, um die Anforderungen aus- und die Antworten asynchron zu erhalten und so wenige Threads wie möglich zu verwenden. Wenn die E/A abgeschlossen ist oder der VOM Server ausgeführte RPC-Aufruf abgeschlossen ist, schließen Sie den asynchronen RPC-Aufruf ab, der die Anforderung übermittelt hat. Dadurch kann der Server mit so wenigen Threads wie möglich ausgeführt werden, was die Leistung und die Anzahl der Clients erhöht, die von einem Server unterstützt werden können.

## <a name="scale-out"></a>Aufskalieren

RPC kann für die Verwendung des Netzwerklastenausgleichs (Network Load Balancing, NLB) konfiguriert werden, wenn NLB so konfiguriert ist, dass alle Anforderungen von einer bestimmten Clientadresse an denselben Server gesendet werden. Da jeder RPC-Client einen Verbindungspool öffnet (weitere Informationen finden Sie unter [RPC](rpc-and-the-network.md)und das Netzwerk), ist es wichtig, dass alle Verbindungen aus dem Pool des angegebenen Clients auf demselben Servercomputer enden. Solange diese Bedingung erfüllt ist, kann ein NLB-Cluster so konfiguriert werden, dass er als ein großer RPC-Server mit potenziell hervorragender Skalierbarkeit funktioniert.

 

 




