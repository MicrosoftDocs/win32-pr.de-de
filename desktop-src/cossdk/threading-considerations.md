---
description: Überlegungen zum Threading
ms.assetid: 4d27f0b3-3e30-4e88-b2b2-d57218da4ffa
title: Überlegungen zum Threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acde9a06802a867cb6a93e7c52be8066ad483c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041522"
---
# <a name="threading-considerations"></a>Überlegungen zum Threading

Die COM+-Komponenten Aufzeichnung in der Warteschlange kann im Multithread-Apartment (MTA) des Prozesses oder in einem Single Thread-Apartment (STA) ausgeführt werden. Wenn die Aufzeichnung im STA ausgeführt wird, erfordert com+, dass jedes Apartment, das Objekte enthält, über eine [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) Warteschlange verfügen muss, um Aufrufe von anderen Prozessen und Apartments innerhalb desselben Prozesses verarbeiten zu können. Dies bedeutet, dass die Arbeitsfunktion des Threads eine Nachrichten Schleife aufweisen muss. Wenn eine in der Warteschlange befindliche Komponente instanziiert wird, ist der zurückgegebene Schnittstellen Zeiger immer ein Proxy Schnittstellen Zeiger anstelle eines direkten Schnittstellen Zeigers. Der Zeiger ist tatsächlich ein Verweis auf eine Instanz der Aufzeichnung. Wenn dieser Aufzeichnungs Schnittstellen Verweis an einen anderen Thread weitergeleitet wird, muss der ursprüngliche Thread weiterhin die Windows-Nachrichten Schleife ausführen, damit der empfangende Thread die Mars Hall Ende Schnittstelle entsperren kann. Wenn dies nicht der Fall ist, hängt der empfangende Thread in einem [**callmarshalinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)-Befehl auf.

Wenn Sie die Threads mithilfe von primitiven synchronisieren, sollten Sie die Verwendung von [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) anstelle anderer Synchronisierungs Funktionen in Erwägung gezogen. Dies überprüft, ob Nachrichten in der Warteschlange sowie in den Status des Synchronisierungs Objekts angezeigt werden.

 

 
