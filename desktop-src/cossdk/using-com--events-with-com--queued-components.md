---
description: Der com+-Ereignis Dienst wird verwendet, um die Übermittlung von Ereignissen von Verlegern an Abonnenten zu verwalten.
ms.assetid: 0945163b-1276-47f6-ae7f-9d932a1b586d
title: Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be31dd1088b720902295738c23173c28145cef2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346862"
---
# <a name="using-com-events-with-com-queued-components"></a>Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange

Der com+-Ereignis Dienst wird verwendet, um die Übermittlung von Ereignissen von Verlegern an Abonnenten zu verwalten. Der Dienst "com+-Warteschlangen Komponenten" kann verwendet werden, um die Verarbeitungszeit des Verlegers und des Abonnenten unabhängig voneinander zu machen, indem die Verleger Nachricht in die Warteschlange eingereiht wird Ob Sie den Dienst für die Warteschlangen Dienste verwenden müssen, hängt von der zugrunde liegenden Geschäftslogik Ihrer Anwendung ab. Wenn Sie Ereignisse haben müssen, die Zeit unabhängig sind, können Sie diese mithilfe des com+-Ereignis Dienstanbieter mit den COM+-Diensten in der Warteschlange erstellen.

> [!Note]  
> Weitere Informationen zur Verwendung des-Dienstanbieter für die com+-Warteschlange finden Sie unter [com+-Komponenten in der Warteschlange](com--queued-components.md).

 

Der Dienst für in der Warteschlange befindliche Komponenten verwaltet den Aufruf der Aufruf Reihenfolge in einer einzelnen Nachricht. Der Recorder fasst alle Methodenaufrufe in eine Nachricht um. Anschließend ruft der Player diese Methoden in der Reihenfolge auf, in der die Nachricht verarbeitet wird.

Eine in der Warteschlange befindliche Komponenten Aufzeichnung und ein Player können an einem der beiden folgenden Stellen positioniert werden:

-   Zwischen dem Verleger und dem Ereignis Objekt
-   Zwischen dem Ereignis Objekt und dem Abonnenten

Wenn Sie die Aufzeichnung und den Player zwischen dem Verleger und dem Ereignis Objekt positionieren, stellen Sie die [Ereignis Klassen](the-com--event-class-object.md) Komponente in die Warteschlange. Die Ereignis Klassen Komponente muss für die Warteschlange markiert und vom Player in einem Prozess aktiviert werden, der vom Verleger getrennt ist.

Um Ereignisse asynchron zu übermitteln, verfassen Sie den Recorder und den Player zwischen dem Ereignis Objekt und dem Abonnenten, und legen Sie das Attribut in der Warteschlange des Abonnement Objekts fest. Hierdurch wird der Abonnement Name wie folgt festgelegt: "Queue:/New:/ {12345678-1234-1234-1234-123456789012} ".

Bei der Verwendung von in der Warteschlange befindlichen Komponenten in einer Ereignis Situation ist eine Reihenfolge der Übermittlungs Implikation zu beachten. Da die in der Warteschlange befindlichen Komponenten alle Aufrufe innerhalb der Lebensdauer eines einzelnen Objekts in einer Nachricht aufzeichnet und wieder gibt, werden alle Aufrufe in der Reihenfolge wiedergegeben, in der Sie erstellt wurden. Wenn jedoch mehr als eine Sitzung mit mehreren Objekten vorhanden ist, kann die Reihenfolge nicht garantiert werden. Wenn die Reihenfolge wichtig ist, stellen Sie sicher, dass Aufrufe, die in der Reihenfolge wiedergegeben werden müssen, sich in derselben Objektinstanz befinden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Filtern von Ereignissen in com+](filtering-events-in-com-.md)
</dt> <dt>

[Veröffentlichen und Bereitstellung von Ereignissen in com+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Abonnements](subscriptions.md)
</dt> <dt>

[Das com+-Ereignis Klassenobjekt](the-com--event-class-object.md)
</dt> </dl>

 

 



