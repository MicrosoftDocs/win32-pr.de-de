---
description: Obwohl dieser Mechanismus für einfache Anwendungen ausreichend ist, kann er die komplexen Anforderungen für die Nachrichten Verteilung erweiterter Anwendungen, wie z. b. solche mit dem MDI-Modell (Multiple Document Interface), nicht unterstützen.
ms.assetid: e4558e71-bbec-415a-a7c2-9025a4d6c474
title: Hook blockieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcd098692784a662456c990a238bd309db0c321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368079"
---
# <a name="blocking-hook"></a>Hook blockieren

Obwohl dieser Mechanismus für einfache Anwendungen ausreichend ist, kann er die komplexen Anforderungen für die Nachrichten Verteilung erweiterter Anwendungen, wie z. b. solche mit dem MDI-Modell (Multiple Document Interface), nicht unterstützen. Bei solchen Anwendungen kann ein Thread spezifischer blockierender Hook von der Anwendung installiert werden. Diese wird vom Dienstanbieter anstelle des standardmäßigen blockierenden Hooks aufgerufen, der im vorherigen beschrieben wird. Ein Dienstanbieter muss einen Zeiger auf den Thread für Thread übergreifende Blockierung aus dem Ws2-32.dll abrufen, \_ indem [**wpuqueryblockingcallback**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueryblockingcallback)aufgerufen wird. Wenn die Anwendung keinen eigenen blockierenden Hook installiert hat, wird ein Zeiger auf die standardmäßige blockierende Hook-Funktion zurückgegeben.

Ein Windows Sockets-Dienstanbieter kann nicht davon ausgehen, dass ein von der Anwendung bereitgestellter blockierter Hook das Fortsetzen der Nachrichtenverarbeitung zulässt Einige Anwendungen können die Möglichkeit der wieder eintretende Nachricht nicht tolerieren, wenn ein Blockierungs Vorgang aussteht. Die blockierende Hook-Funktion einer solchen Anwendung würde einfach **false** zurückgeben. Wenn ein Dienstanbieter von Nachrichten für den internen Vorgang abhängig ist, kann er **gekmessage**(hmywnd...) ausführen, bevor er den blockierenden Hook der Anwendung ausführt, sodass er seine eigenen Nachrichten abrufen kann, ohne dass sich dies auf den Rest des Systems auswirkt.

In präemptiven Multithread-Versionen von Windows ist kein standardmäßiger blockierter Hook installiert. Dies liegt daran, dass andere Prozesse nicht blockiert werden, wenn eine einzelne Anwendung auf den Abschluss eines Vorgangs wartet (und daher nicht " **Peer-Message** " oder " **GetMessage** " aufrufen, was dazu führt, dass die Anwendung den Prozessor in nicht präemptiven Fenstern liefert). Wenn der Dienstanbieter [**wpuqueryblockingcallback**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueryblockingcallback) aufruft, wird ein NULL-Zeiger zurückgegeben, der angibt, dass der Anbieter systemeigene Blockierungs Funktionen von Betriebssystemen verwenden soll. Um die Abwärtskompatibilität zu erhalten, kann jedoch ein von der Anwendung bereitgestellter blockierter Hook in Windows immer noch auf Thread Basis installiert werden.

Der Winsock-Dienstanbieter ruft den blockierenden Hook nur auf, wenn Folgendes zutrifft: die Routine ist eine, die so definiert ist, dass Sie blockiert werden kann, der angegebene Socket ist ein blockierender Socket, und die Anforderung kann nicht sofort abgeschlossen werden. Wenn nur nicht blockierende Sockets und [**wspasyncselect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) / [**wspeventselect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) anstelle von [**wspselect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) verwendet werden, wird der blockierende Hook nie aufgerufen.

> [!Note]  
> Wenn während der Zeit, in der pseudoblocking zum Blockieren eines Threads verwendet wird, eine Windows-Meldung für den Thread empfangen wird, besteht das Risiko, dass der Thread versucht, einen anderen Winsock-Aufruf auszugeben. Aufgrund der Schwierigkeit, diese Bedingung sicher zu verwalten, hat die Windows Sockets 1,1-Spezifikation dieses Verhalten nicht zugelassen. Es ist nicht zulässig, dass ein angegebener Thread mehrere, nicht aufgerufenen Winsock-Funktionsaufrufe durchführen kann. Nur ein ausstehender Funktions Aufrufwert ist für einen bestimmten Thread zulässig. Alle geschsasteten Winsock-Funktionsaufrufe schlagen mit dem Fehler "wsaerprogress" fehl. Es sollte hervorgehoben werden, dass diese Einschränkung sowohl für blockierende als auch für nicht blockierende Vorgänge gilt, aber nur in Windows Sockets 1,1-Umgebungen. Es gibt einige Ausnahmen zu dieser Regel, einschließlich zwei Funktionen, mit denen eine Anwendung ermitteln kann, ob ein Pseudo Blockierungs Vorgang tatsächlich ausgeführt wird, und um einen solchen Vorgang bei Bedarf abzubrechen. Diese werden im folgenden beschrieben.

 

 

 
