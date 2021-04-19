---
description: Viele Anwendungen sind von der zeitlichen Beziehungs Beziehung zwischen Medien Ereignissen abhängig (z. b. empfangene DTMF-Ziffern), um die Art eines angeforderten Vorgangs zu bestimmen.
ms.assetid: 8d25a31f-de40-4c74-b8e7-a81fbfd47db2
title: Medienereignis Timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a584518c9c33e8991bd2388f01cb863bab1c7a3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106353625"
---
# <a name="media-event-timers"></a>Medienereignis Timer

Viele Anwendungen sind von der zeitlichen Beziehungs Beziehung zwischen Medien Ereignissen abhängig (z. b. empfangene DTMF-Ziffern), um die Art eines angeforderten Vorgangs zu bestimmen. In einer Voicemailanwendung können z. b. zwei aufeinander folgende DTMF-Ziffern "1" den Wert "zwei Segmente sichern" oder "Wiedergabe von Anfang der Nachricht" bedeuten, je nachdem, wie viel Zeit zwischen den beiden Ziffern verstrichen ist. Wenn die DTMF-Erkennung in einer Client/Server-Umgebung auf einem separaten Prozessor ausgeführt wird, auf dem die Anwendung ausgeführt wird, ist es sehr wahrscheinlich, dass die zeitliche Beziehung zwischen Medien Ereignissen verzerrt wird. das Ergebnis ist, dass diese zeitlichen Unterschiede verloren gehen oder unzuverlässig werden.

Um dieses Problem zu beheben, können mehrere TAPI-Nachrichten mit einem Zeitstempel versehen werden. Da es sich hierbei um die relative zeitliche Steuerung zwischen diesen Ereignissen handelt, ist die "Uhrzeitangabe" des Ereignisses nicht wichtig, und die Zeitüberschreitung bei der untergeordneten Sekunde ist betroffen. diese Zeitstempel verwenden die Millisekunden-Auflösungszeit seit Windows, die von der [**GetTickCount**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount) -Funktion zurückgegeben wurde. Anwendungen müssen beachten, dass es sich hierbei um die Takt Anzahl auf dem Server (oder auf dem Computer, auf dem der Dienstanbieter, der die Hardware direkt verwaltet) handelt und nicht unbedingt um denselben Computer handelt, auf dem die Anwendung ausgeführt wird. Daher können die Zeitstempel in diesen TAPI-Nachrichten nur miteinander verglichen werden, und nicht mit dem Wert, der von **GetTickCount** für den Prozessor zurückgegeben wird, auf dem die Anwendung ausgeführt wird.

Die TAPI-Nachrichten, die mit einem Zeitstempel versehen werden können, sind: [**line \_ gatherdigits**](line-gatherdigits.md), [**line \_ Generate**](line-generate.md), [**line \_ monitordigits**](line-monitordigits.md), [**line \_ monitormedia**](line-monitormedia.md)und [**line \_ monitortone**](line-monitortone.md). Der Tick-Zähler wird in *dwParam3* dieser Nachrichten eingefügt. Wenn das Zeitstempel vom Dienstanbieter nicht unterstützt wird (Dies wird durch die Dienstanbieter Einstellung *dwParam3* in diesen Nachrichten auf 0 angegeben), fügt TAPI den Tick-Zähler in den *dwParam3* aller dieser Nachrichten ein (er kann etwas verzerrt werden, aber kleiner als, wenn die Anwendung nach dem Durchlaufen eines prozessübergreifenden Kommunikations Schemas das gleiche getan hat).

 

 
