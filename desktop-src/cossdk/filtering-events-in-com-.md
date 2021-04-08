---
description: 'Com+-Ereignisse bieten zwei Möglichkeiten, um zu steuern, welche Ereignisse die folgenden Abonnenten erreichen: Herausgeber Filterung und Parameter Filterung.'
ms.assetid: dfc82a57-5587-462d-a43d-516b7d70e25e
title: Filtern von Ereignissen in com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a7d152813e4806a9cfb6a342255e0981ecf37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748864"
---
# <a name="filtering-events-in-com"></a>Filtern von Ereignissen in com+

Com+-Ereignisse bieten zwei Möglichkeiten, um zu steuern, welche Ereignisse die folgenden Abonnenten erreichen: *Herausgeber Filterung* und *Parameter Filterung*.

## <a name="publisher-filtering"></a>Herausgeber Filterung

Die Herausgeber Filterung steuert die Reihenfolge und das Auslösen einer Ereignismethode durch ein [Ereignis Klassen](the-com--event-class-object.md) Objekt. Die Herausgeber Filterung ermöglicht dem Verleger, zu bestimmen, welche Abonnenten ein bestimmtes Ereignis erhalten.

Ein Beispiel für die effektive Verwendung der Herausgeber Filterung ist die von einem Aktien Austausch. Die meisten Abonnenten möchten wissen, wann ein neuer bestand hinzugefügt wird. Viele dieser Abonnenten möchten jedoch möglicherweise nicht wissen, wann jeder Aktienkurs geändert wird. Die Herausgeber Filterung bietet die Granularität, die für die effektive Bereitstellung von Ereignissen an die Abonnenten erforderlich ist, die diese Informationen wünschen

Wenn eine Methode für das instanziierte Ereignis Klassenobjekt aufgerufen wird, sammelt Sie alle Verleger Filter für diese Methode. Der Filter erzwingt, dass das Ereignis Objekt die Ereignismethode für einen bestimmten Abonnenten auslöst. Der Filter bestimmt, welche Abonnements ausgelöst werden und in welcher Reihenfolge Sie ausgelöst werden. Beispielsweise könnte der Filter die Abonnementliste lesen und die Reihenfolge basierend auf einigen Anwendungskriterien erstellen und dann die Abonnenten in dieser Reihenfolge aufzurufen.

Ausführliche Anweisungen zum Erstellen eines Herausgeber Filters finden Sie unter [Erstellen eines Herausgeber Filters](creating-a-publisher-filter.md).

## <a name="parameter-filtering"></a>Parameterfilterung

Anders als bei der Herausgeber Filterung bietet der com+-Ereignis Dienst eine optionale Filterung von Abonnenten Parametern für jedes Abonnement und jeden Aufruf der Ereignismethode. Durch die Parameter Filterung wird die Eigenschaft "filterCriteria" des Abonnements mit den Parametern der Ereignismethode ausgewertet. Dieser Filtertyp wird pro Methode und pro Abonnement verwendet und bietet eine Ebene der Abonnenten Filterung an der Ereignis Quelle. Die Filter Kriterienzeichenfolge erkennt relationale Operatoren zum Überprüfen von Gleichheit (=, = =,!,! =, ~, ~ =,  <>), geschachtelten Klammern und logischen Schlüsselwörtern **und**, **or** oder **Not**.

Die Parameter Filterung erfolgt nach dem Filtern aller Verleger und beim Auslösen des Standard Ereignis Objekts für ein bestimmtes Abonnement. Wenn die Herausgeber Filterung verwendet wird, erfolgt die Parameter Filterung nur, wenn der Verleger Filter [**ifiringcontrol:: fireabonnement**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription)aufruft. Aus diesem Grund können Herausgeber Filterung und Parameter Filterung zusammen verfasst werden, aber die Herausgeber Filterung hat Vorrang.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Veröffentlichen und Bereitstellung von Ereignissen in com+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Abonnements](subscriptions.md)
</dt> <dt>

[Das com+-Ereignis Klassenobjekt](the-com--event-class-object.md)
</dt> <dt>

[Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



