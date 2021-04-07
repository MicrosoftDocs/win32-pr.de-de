---
description: Zum Veröffentlichen eines Ereignisses instanziieren Sie einfach ein Ereignis Klassenobjekt, und rufen Sie die gewünschte Methode auf. Ausführliche Anweisungen dazu, wie Sie dies in Code tun, finden Sie unter Veröffentlichen eines Ereignisses.
ms.assetid: 835c3753-fdcc-4afe-94c3-c954aaf1c832
title: Veröffentlichen und Bereitstellung von Ereignissen in com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a444b64501156191590c115d6000f4c0bda153
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748856"
---
# <a name="publishing-and-delivering-events-in-com"></a>Veröffentlichen und Bereitstellung von Ereignissen in com+

Zum Veröffentlichen eines Ereignisses instanziieren Sie einfach ein [Ereignis Klassen](the-com--event-class-object.md) Objekt, und rufen Sie die gewünschte Methode auf. Ausführliche Anweisungen dazu, wie Sie dies in Code tun, finden Sie unter [Veröffentlichen eines Ereignisses](publishing-an-event.md).

Wenn ein Verleger ein Ereignis auslöst, durchsucht der com+-Ereignis Dienst die Abonnement Datenbank, um alle Abonnenten zu suchen, die Abonnements für die instanziierte Ereignisklasse registriert haben. Sie stellt eine Verbindung mit diesen Abonnenten her (durch direkte Erstellung, Moniker oder in der Warteschlange befindliche Komponenten) und ruft die-Methode auf. Um mehr als eine Abonnenten Benachrichtigung für ein Ereignis zu unterstützen, können-Methoden nur in-Parameter enthalten und dürfen nur Erfolgs-oder Fehler- **HRESULT** -Werte zurückgeben.

> [!Note]  
> Diese Version von COM+-Ereignissen unterstützt keinen verteilten Ereignisspeicher. Ein Abonnent muss ein Ereignis auf jedem Computer abonnieren, von dem aus eine Benachrichtigung empfangen werden soll. Als Alternative können Sie das Ereignis Klassenobjekt und die Abonnements auf einem zentralen Computer registrieren und dieses Ereignis Klassenobjekt von den Remote Computern, auf denen Ereignisse veröffentlicht werden, instanziieren. Die Übermittlung von Ereignissen wird entweder durch DCOM oder durch den com+-Dienst in der Warteschlange bereitgestellt. Weitere Informationen zur Verwendung des-Dienstanbieter für die com+-Warteschlange finden Sie unter [Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange](using-com--events-with-com--queued-components.md)

 

Standardmäßig löst der com+-Ereignis Dienst Ereignisse nacheinander in einer nicht ermittelten oder wiederholbaren Reihenfolge auf. Herausgeber, die die Reihenfolge steuern müssen, in der Abonnenten ein Ereignis empfangen, können einen Herausgeber Filter implementieren. (Weitere Informationen finden Sie unter [Filtern von Ereignissen in com+](filtering-events-in-com-.md).)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Filtern von Ereignissen in com+](filtering-events-in-com-.md)
</dt> <dt>

[Abonnements](subscriptions.md)
</dt> <dt>

[Das com+-Ereignis Klassenobjekt](the-com--event-class-object.md)
</dt> <dt>

[Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



