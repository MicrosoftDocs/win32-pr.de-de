---
title: Client seitige asynchrone Pipe-Verarbeitung
description: Vor dem Ausführen eines asynchronen Remote Aufrufes muss der Client zuerst das asynchrone handle initialisieren.
ms.assetid: 3d54b233-d8b0-45d1-b759-0d2d24c1e247
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ff503f80c77b2403d683c2b644d89836365956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856687"
---
# <a name="client-side-asynchronous-pipe-handling"></a>Client seitige asynchrone Pipe-Verarbeitung

Vor dem Ausführen eines asynchronen Remote Aufrufes muss der Client zuerst das asynchrone handle initialisieren. Wie bei nonpipe-Prozeduren ruft der Client eine asynchrone Funktion mit dem asynchronen Handle als ersten Parameter auf und verwendet das asynchrone handle, um pipedaten zu senden und zu empfangen, den Status des Aufrufs abzufragen und die Antwort zu empfangen.

Der Client führt den asynchronen Remote Prozedur Aufrufvorgang mit dem asynchronen Handle als ersten Parameter aus. Der Client kann dieses Handle verwenden, um den Status des Aufrufes abzufragen und die Antwort zu empfangen. Das asynchrone Pipe-Modell ist symmetrisch. Client-und Server Anwendungen senden und empfangen Pipe-Daten aktiv (im Gegensatz zu synchronem RPC, bei denen die pipedaten passiv gesendet und empfangen werden).

Der Client sendet asynchrone Pipe-Daten durch Aufrufen der **Push** -Funktion in der entsprechenden asynchronen Pipe, wobei die Status Variable der Pipe als erster Parameter angegeben wird. Wenn die **Push** -Funktion zurückgegeben wird, kann der Client den Sendepuffer ändern oder freigeben.

Wenn das \_ Flag zum Vervollständigen von RPC Async \_ \_ on \_ Send \_ im asynchronen handle festgelegt ist und APCs als Benachrichtigungs Mechanismus verwendet werden, wird ein APC in die Warteschlange eingereiht, wenn der Pipe-Sendevorgang tatsächlich ausgeführt wird. Sie können diesen Mechanismus nutzen, um die Fluss Steuerung zu implementieren. Beachten Sie jedoch Folgendes: Wenn der Client einen anderen Puffer überträgt, bevor der vorherige Push-Vorgang ausgeführt wird, kann der Client abhängig von der Geschwindigkeit des Übertragungs Vorgangs nur eine Benachrichtigung zum Senden von Benachrichtigungen empfangen, anstatt für jeden Puffer oder jeden **Pushvorgang** eine Benachrichtigung zu erhalten. Wenn der Client alle pipedaten gesendet hat, wird ein abschließender **Push** -Vorgang mit der Anzahl der Elemente auf 0 festgelegt.

Das Client Programm empfängt asynchrone Pipe-Daten durch Aufrufen der **Pull** -Funktion in der entsprechenden asynchronen Pipe, wobei die Status Variable der Pipe als erster Parameter angegeben wird. Wenn keine pipedaten verfügbar sind, gibt die **Pull** -Funktion einen asynchronen RPC \_ S- \_ \_ Aufruf \_ aus.

Wenn der Benachrichtigungs Mechanismus APC ist und der Server einen asynchronen RPC-Aufruf zurückgibt \_ \_ \_ \_ , muss der Client warten, bis er das APC **rpcreceivecomplete** von der Laufzeit empfängt  , bevor der Pullvorgang erneut aufgerufen wird.

 

 




