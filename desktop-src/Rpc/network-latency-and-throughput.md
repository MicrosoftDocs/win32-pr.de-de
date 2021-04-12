---
title: Netzwerk Latenz und Durchsatz
description: Netzwerk Latenz und Durchsatz mit Remote Prozedur Aufruf (RPC).
ms.assetid: 8285fd73-eb54-4c06-b01a-1bffafb7e675
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c51c4db75b904ac5feae8c4a1cc5965fc2b06e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207246"
---
# <a name="network-latency-and-throughput"></a>Netzwerk Latenz und Durchsatz

Drei Hauptprobleme beziehen sich auf die optimale Verwendung des Netzwerks:

-   Netzwerklatenz
-   Netzwerk Sättigung
-   Auswirkungen der Paketverarbeitung

In diesem Abschnitt wird eine Programmieraufgabe eingeführt, die die Verwendung von RPC erfordert, anschließend werden zwei Lösungen entworfen: eine schlecht geschriebene und eine gut geschriebene. Beide Lösungen werden dann überprüft, und die Auswirkungen auf die Netzwerkleistung werden erörtert.

Bevor Sie die beiden Lösungen erörtern, werden die netzwerkbezogenen Leistungsprobleme in den nächsten Abschnitten erläutert und verdeutlicht.

## <a name="network-latency"></a>Netzwerklatenz

Netzwerkbandbreite und Netzwerk Latenz sind separate Begriffe. Netzwerke mit hoher Bandbreite garantieren keine geringe Latenz. Beispielsweise weist ein Netzwerkpfad, der einen Satelliten Link durchläuft, häufig eine hohe Latenzzeit auf, obwohl der Durchsatz sehr hoch ist. Es ist nicht ungewöhnlich, dass ein Netzwerkroundtrip einen Satellitenlink durchläuft, der fünf oder mehr Sekunden Latenz hat. Eine solche Verzögerung besteht darin, dass eine Anwendung, die für das Senden einer Anforderung, das warten auf eine Antwort, das Senden einer anderen Anforderung, das warten auf eine andere Antwort usw. konzipiert ist, mindestens fünf Sekunden für jeden Paket Austausch wartet, unabhängig davon, wie schnell der Server ist. Trotz der zunehmenden Geschwindigkeit von Computern basieren Satellitenübertragungen und Netzwerk Medien auf der Geschwindigkeit des Lichts, das in der Regel konstant bleibt. Daher ist es unwahrscheinlich, dass die Latenz für vorhandene Satelliten Netzwerke verbessert wird.

## <a name="network-saturation"></a>Netzwerk Sättigung

In vielen Netzwerken kommt es zu einer gewissen Sättigung. Die einfachsten Netzwerke zum sätftigen sind langsame Modem Verknüpfungen, wie z. b. die analogen standardmäßigen 56K-Modems. Allerdings können Ethernet-Verbindungen mit vielen Computern eines einzelnen Segments auch ausgelastet werden. Dasselbe gilt für Wide Area Networks mit einer Verbindung mit geringer Bandbreite oder anderweitig überladener Verbindung, z. b. einem Router oder Switch, der eine begrenzte Menge an Datenverkehr verarbeiten kann. In solchen Fällen, wenn das Netzwerk mehr Pakete sendet, als der schwächste Link verarbeiten kann, werden Pakete gelöscht. Um Überlastung zu vermeiden, wird der Windows-TCP-Stapel zurückgezogen, wenn gelöschte Pakete erkannt werden, was zu erheblichen Verzögerungen führen kann.

## <a name="packet-processing-implications"></a>Auswirkungen der Paketverarbeitung

Wenn Programme für Umgebungen höherer Ebene wie RPC, com und sogar Windows Sockets entwickelt werden, neigen Entwickler dazu, zu vergessen, wie viel Arbeit im Hintergrund für jedes gesendete oder empfangene Paket stattfindet. Wenn ein Paket aus dem Netzwerk eingeht, wird vom Computer ein Interrupt von der Netzwerkkarte gewartet. Anschließend wird ein verzögerter Prozedur Rückruf (DPC) in die Warteschlange eingereiht und muss die Treiber durchlaufen. Wenn eine Art von Sicherheit verwendet wird, muss das Paket möglicherweise entschlüsselt oder der kryptografische Hash überprüft werden. Eine Reihe von Gültigkeits Prüfungen muss auch in jedem Zustand ausgeführt werden. Nur dann empfängt das Paket am endgültigen Ziel: dem Servercode. Das Senden vieler kleiner Datenblöcke führt zu einem Paket Verarbeitungsaufwand für jeden kleinen Datenblock. Das Senden eines großen Datenblocks beansprucht tendenziell erheblich weniger CPU-Zeit im gesamten System, obwohl die Ausführungskosten für viele kleine Blöcke im Vergleich zu einem großen Block für die Serveranwendung identisch sein können.

## <a name="example-1-a-poorly-designed-rpc-server"></a>Beispiel 1: ein schlecht gestalteter RPC-Server

Stellen Sie sich eine Anwendung vor, die auf Remote Dateien zugreifen muss, und die Aufgabe ist es, eine RPC-Schnittstelle zum Bearbeiten der Remote Datei zu entwerfen. Die einfachste Lösung ist die Spiegelung der Studio-Datei Routinen für lokale Dateien. Dies führt möglicherweise zu einer nicht ordnungsgemäß sauberen und vertrauten Schnittstelle. Im folgenden finden Sie eine abgekürzte IDL-Datei:

``` syntax
typedef [context_handle] void *remote_file;
... .
interface remote_file
{
    remote_file remote_fopen(file_name);
    void remote_fclose(remote_file ...);
    size_t remote_fread(void *, size_t, size_t, remote_file ...);
    size_t remote_fwrite(const void *, size_t, size_t, remote_file ...);
    size_t remote_fseek(remote_file ..., long, int);
}
```

Dies scheint elegant genug zu sein, aber das ist ein Zeit würdiges Rezept für einen Leistungs Notfall. Im Gegensatz zu gängigen Meinungen ist der Remote Prozedur Aufruf nicht einfach ein lokaler Prozedur Aufruf mit einer Verbindung zwischen dem Aufrufer und dem aufgerufenen.

Um zu sehen, wie die Leistung durch dieses Rezept beeinträchtigt wird, sollten Sie eine 2K-Datei in Erwägung gezogen werden, bei der 20 Bytes von Anfang an und 20 Bytes vom Ende gelesen werden. Auf der Clientseite werden die folgenden Aufrufe durchgeführt (viele Codepfade werden aus Gründen der Kürze ausgelassen):

``` syntax
rfp = remote_fopen("c:\\sample.txt");
remote_read(...);
remote_fseek(...);
remote_read(...);
remote_fclose(rfp);
```

Stellen Sie sich nun vor, dass der Server von einem Satelliten Link mit einer Roundtrip-Zeit von fünf Sekunden vom Client getrennt wird. Jeder dieser Aufrufe muss auf eine Antwort warten, bevor er fortfahren kann. Dies bedeutet ein absolutes Minimal Limit für die Ausführung dieser Sequenz von 25 Sekunden. Wenn wir nur 40 Bytes abrufen, ist dies eine unerhört langsame Leistung. Kunden dieser Anwendung sind wütend.

Stellen Sie sich nun vor, dass das Netzwerk ausgelastet ist, weil die Kapazität eines Routers an einer beliebigen Stelle im Netzwerkpfad überlastet ist. Dieser Entwurf zwingt den Router, mindestens 10 Pakete zu verarbeiten, wenn keine Sicherheit (eine für jede Anforderung und eine für jede Antwort) vorhanden ist. Auch das ist nicht gut geeignet.

Dieser Entwurf zwingt auch den Server, fünf Pakete zu empfangen und fünf Pakete zu senden. Auch hier keine sehr gute Implementierung.

## <a name="example-2-a-better-designed-rpc-server"></a>Beispiel 2: ein besser entworfener RPC-Server

Im folgenden wird die in Beispiel 1 erörterte Schnittstelle umgestaltet, um zu erfahren, ob wir Sie verbessern können. Es ist wichtig zu beachten, dass es für diesen Server wirklich sinnvoll ist, das Verwendungs Muster für die angegebenen Dateien zu kennen: solche Kenntnisse werden für dieses Beispiel nicht angenommen. Daher handelt es sich hierbei um einen besser entwickelten RPC-Server, aber nicht um einen optimal entworfenen RPC-Server.

Die Idee in diesem Beispiel besteht darin, so viele Remote Vorgänge wie möglich in einem Vorgang zu reduzieren. Der erste Versuch lautet wie folgt:

``` syntax
typedef [context_handle] void *remote_file;
typedef struct
{
    long position;
    int origin;
} remote_seek_instruction;
... .
interface remote_file
{
    remote_fread(file_name, void *, size_t, size_t, [in, out] remote_file ..., BOOL CloseWhenDone, remote_seek_instruction *...);
    size_t remote_fwrite(file_name, const void *, size_t, size_t, [in, out] remote_file ..., BOOL CloseWhenDone, remote_seek_instruction *...);
}
```

In diesem Beispiel werden alle Vorgänge auf einen Lese-und Schreibvorgang reduziert, wodurch ein optionales öffnen für denselben Vorgang sowie ein optionales schließen und suchen ermöglicht wird.

Dieselbe Abfolge von Vorgängen, die in abgekürzten Formularen geschrieben werden, sieht wie folgt aus:

``` syntax
remote_read("c:\\sample.txt", ..., &rfp, FALSE, NULL);
remote_read(NULL, ..., &rfp, TRUE, seek_to_20_bytes_before_end);
```

Wenn Sie den besser entworfenen RPC-Server in Erwägung ziehen, prüft der Server beim zweiten Aufruf, ob der *Dateiname \_* **null** ist, und verwendet die gespeicherte geöffnete Datei in RFP. Dann sehen Sie, dass Such Anweisungen vorhanden sind, und die Dateizeiger 20 Bytes vor dem Ende positionieren, bevor Sie gelesen werden. Wenn dies der Fall ist, erkennt er, dass das Flag **closewhendone** auf **true** festgelegt ist, schließt die Datei und schließt RFP.

Im Netzwerk mit hoher Latenzzeit dauert diese bessere Version 10 Sekunden (2,5-mal schneller) und erfordert die Verarbeitung von nur vier Paketen. zwei vom Server empfangene und zwei Sende Vorgänge vom Server. Das zusätzliche *IFS* und das ungemarshalling des Servers sind im Vergleich zu allen anderen vernachlässigbar.

Wenn die kausale Reihenfolge ordnungsgemäß angegeben ist, kann die Schnittstelle sogar asynchron gemacht werden, und die beiden Aufrufe können parallel gesendet werden. Wenn die kausale Reihenfolge verwendet wird, werden Aufrufe weiterhin in der richtigen Reihenfolge verteilt, was bedeutet, dass im Netzwerk mit hoher Latenz nur eine Verzögerung von fünf Sekunden durchlaufen wird, auch wenn die Anzahl der gesendeten und empfangenen Pakete gleich ist.

Wir können dies noch weiter reduzieren, indem wir eine Methode erstellen, die ein Array von Strukturen annimmt, wobei jeder Member des Arrays einen bestimmten Datei Vorgang beschreibt. eine Remote Variation von Scatter/Gather-e/a. Der Ansatz zahlt sich aus, solange das Ergebnis jedes Vorgangs keine weitere Verarbeitung auf dem Client erfordert. Anders ausgedrückt: die Anwendung liest die 20 Bytes am Ende, unabhängig davon, was die ersten 20 Bytes sind.

Wenn jedoch einige Verarbeitungsschritte für die ersten 20 Bytes ausgeführt werden müssen, nachdem Sie gelesen wurden, um den nächsten Vorgang zu bestimmen, funktioniert das Reduzieren von Elementen in einen Vorgang nicht (zumindest nicht in allen Fällen). Die Eleganz von RPC besteht darin, dass eine Anwendung beide Methoden in der Schnittstelle aufweisen kann und jede Methode je nach Bedarf aufruft.

Im Allgemeinen ist es am besten, wenn das Netzwerk beteiligt ist, möglichst viele Aufrufe eines einzelnen Aufrufs zu kombinieren. Wenn eine Anwendung über zwei unabhängige Aktivitäten verfügt, verwenden Sie asynchrone Vorgänge, und lassen Sie sie parallel ausführen. Halten Sie die Pipeline im wesentlichen vollständig.

 

 




