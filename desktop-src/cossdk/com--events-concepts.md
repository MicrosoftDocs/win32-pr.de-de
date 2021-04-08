---
description: Konzepte der com+-Ereignisse
ms.assetid: 6bfe4852-4029-4dd4-92ad-3061618b1b23
title: Konzepte der com+-Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811dbca17c4e90ba5e8c2bcb8c918ce6634487e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749088"
---
# <a name="com-events-concepts"></a>Konzepte der com+-Ereignisse

Der com+-Ereignis Dienst ist ein automatisiertes, *locker gekoppeltes Ereignis* System, das Ereignis Informationen von verschiedenen Verlegern im com+-Katalog speichert. Abonnenten können diesen Ereignisspeicher Abfragen und die Ereignisse auswählen, über die Sie hören möchten.

> [!Note]  
> Ein *Ereignis* wird durch eine Methode in einer COM+-Schnittstelle identifiziert, die als *Ereignismethode* bezeichnet wird und von einem Verleger stammt und über den com+-Ereignis Dienst an die richtigen Abonnenten oder Abonnenten gesendet wird. Ereignis Methoden müssen eindeutig benannt werden und dürfen nur Eingabeparameter (keine Ausgabe-oder Eingabe-/Ausgabeparameter) enthalten. Der Rückgabewert muss ein **HRESULT** sein.

 

Der com+-Ereignis Dienst verarbeitet den größten Teil der Ereignis Semantik für den Verleger und den Abonnenten. Herausgeber bieten die Veröffentlichung von Ereignis Typen, und Abonnenten fordern Ereignis Typen von Verlegern an. Anders als bei einem *eng verknüpften Ereignis* System, bei dem Herausgeber den mehr Aufwand für das direkte Aufrufen von Abonnenten behandeln müssen, verwaltet der com+-Ereignis Dienst Abonnement Daten im com+-Katalog unabhängig vom Verleger und dem Abonnenten. Dadurch wird das Programmiermodell für den Verleger und den Abonnenten vereinfacht, da die com+-Abonnenten Komponente nicht die Logik zum Aufbauen von Abonnements enthalten muss.

Da der Lebenszyklus der com+-Ereignis Abonnement Daten vom Verleger oder Abonnenten getrennt ist, können Abonnements erstellt werden, bevor entweder der Abonnent oder die Verleger Anwendungen aktiv werden. Dies bedeutet auch, dass Verleger und Abonnenten separat entwickelt und bereitgestellt werden können. Der Verleger kann ohne Kenntnis der Anzahl und des Speicher Orts der Abonnenten geschrieben werden. Die Abonnenten verwenden den com+-Ereignis Dienst, um nach dem Verleger zu suchen und seine Abonnements zu verwalten.

Die folgenden Themen in diesem Abschnitt enthalten ausführliche Informationen zu den Kernelementen des com+-Ereignis Dienstanbieter und deren Verwendung.

-   [Das com+-Ereignis Klassenobjekt](the-com--event-class-object.md)
-   [Abonnements](subscriptions.md)
-   [Veröffentlichen und Bereitstellung von Ereignissen in com+](publishing-and-delivering-events-in-com-.md)
-   [Filtern von Ereignissen in com+](filtering-events-in-com-.md)
-   [Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange](using-com--events-with-com--queued-components.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheitsüberlegungen für COM+-Ereignisse](com--events-security-considerations.md)
</dt> <dt>

[Aufgaben für COM+-Ereignisse](com--events-tasks.md)
</dt> </dl>

 

 



