---
description: Möglicherweise möchten Sie eine Anwendung schreiben, die jederzeit auf Ereignisse reagieren kann.
ms.assetid: 475dca47-b1e5-4362-ab00-9ab9383e92f9
ms.tgt_platform: multiple
title: Empfangen von Ereignissen zu allen Zeitpunkten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5559068e1e108c6f4185c31f8858a9e4169c50c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344729"
---
# <a name="receiving-events-at-all-times"></a>Empfangen von Ereignissen zu allen Zeitpunkten

Möglicherweise möchten Sie eine Anwendung schreiben, die jederzeit auf Ereignisse reagieren kann. Ein Administrator möchte z. b. eine e-Mail-Nachricht erhalten, wenn bestimmte leistungsmaßnahmen auf Netzwerkservern abgelehnt werden. In diesem Fall sollte die Anwendung jederzeit ausgeführt werden. Die kontinuierliche Ausführung einer Anwendung ist jedoch keine effiziente Verwendung von Systemressourcen. Stattdessen können Sie mit WMI einen permanenten Ereignisconsumer erstellen. Permanente Ereignisconsumer müssen besondere Sicherheitsanforderungen erfüllen. Weitere Informationen finden Sie unter [Sichern von WMI-Ereignissen](securing-wmi-events.md).

Ein dauerhafter Ereignisconsumer empfängt Ereignisse, bis die Registrierung explizit abgebrochen wird.

Bei einem permanenten Ereignisconsumer handelt es sich um eine Kombination der folgenden WMI-Klassen, Filter und COM-Objekte, die sich auf Ihrem System befinden:

-   Ein COM-Objekt, das als physischer Consumer bezeichnet wird. WMI bietet mehrere permanente Standard Consumer. Beispielsweise führt der Consumer des aktiven Skript Ereignisses [ein Skript aus, wenn ein Ereignis auftritt](running-a-script-based-on-an-event.md).
-   Eine neue permanente Consumerklasse.
-   Eine Instanz der permanenten Consumerklasse, die als logischer Consumer bezeichnet wird.
-   Ein Filter, der die Abfrage für Ereignisse enthält.
-   Eine Verknüpfung zwischen dem Consumer und dem Filter.

Die Eigenschaften eines logischen Ereignisconsumers geben die Aktionen an, die durchgeführt werden sollen, wenn ein Ereignis benachrichtigt wird, aber Sie definieren nicht die Ereignis Abfragen, denen Sie zugeordnet sind. Beim signalisieren lädt WMI das COM-Objekt, das den permanenten Ereignisconsumer darstellt, automatisch in den aktiven Arbeitsspeicher. Dies erfolgt in der Regel während des Starts oder als Reaktion auf ein auslösendes Ereignis. Nach der Aktivierung fungiert der Consumer des permanenten Ereignisses als normaler Ereignisconsumer, bleibt aber bestehen, bis er vom Betriebssystem explizit entladen wurde.

Sie können einen eigenen permanenten Ereignisconsumer schreiben oder die vorinstallierten [Standard Consumerklassen](standard-consumer-classes.md)von WMI verwenden, z. b. [**activescripteventconsumer**](activescripteventconsumer.md). Weitere Informationen finden Sie unter [Standard Consumer-Klassen](standard-consumer-classes.md), über [wachen und reagieren auf Ereignisse mit Standardconsumern](monitoring-and-responding-to-events-with-standard-consumers.md)und über [Wachen von Ereignissen](monitoring-events.md).

Im folgenden Verfahren wird beschrieben, wie Sie einen eigenen permanenten Ereignisconsumer erstellen.

**So erstellen Sie einen eigenen permanenten Ereignisconsumer**

1.  Bestimmen Sie, welche Art von Ereignissen Sie empfangen möchten.

    WMI unterstützt systeminterne und extrinsische Ereignisse. Ein System internes Ereignis ist ein von WMI vordefiniertes Ereignis, wohingegen ein extrinsisches Ereignis ein Ereignis ist, das von einem Drittanbieter definiert wird. Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).

2.  [Implementieren Sie einen physischen Consumer](implementing-a-physical-consumer.md).

    Der Hauptunterschied zwischen einer Verwaltungs Anwendung und einem [*physischen Consumer*](gloss-p.md) besteht darin, dass ein Benutzer eine Verwaltungs Anwendung lädt und entlädt, während WMI einen physischen Consumer lädt und entlädt. Der größte Teil ihrer Codierung sollte dem physischen Consumer unterliegen.

    > [!Note]  
    > Dieser Schritt ist das erste Verfahren, um die Erläuterung zu vereinfachen. Im Hinblick auf die Codierung sollten Sie tatsächlich den physischen Consumer zuletzt erstellen. Auf diese Weise können Sie Ihre Parameter und ihre Logik für ihren permanenten Ereignis Anbieter anordnen, bevor Sie lange codieren. Es gibt jedoch keine Einschränkung bei der ersten Erstellung des physischen Consumers.

     

3.  [Erstellen Sie eine neue Consumerklasse, in der der physische Consumer beschrieben](creating-a-new-permanent-event-consumer-class.md)wird.

    Wie jede beliebige Klasse beschreibt die Consumerklasse die allgemeinen Parameter eines permanenten Ereignisconsumers für WMI.

4.  [Erstellen Sie eine Instanz der Consumer-Klasse](creating-a-logical-consumer.md).

    Wie jede andere WMI-Klasse müssen Sie eine Instanz der Consumer-Klasse erstellen, wenn Sie die-Klasse implementieren möchten. Eine Instanz einer Consumerklasse wird auch als [*logischer Consumer*](gloss-l.md)bezeichnet. Der logische Consumer stellt den physischen Consumer von WMI dar.

5.  [Erstellen Sie einen Ereignis Filter](creating-an-event-filter.md).

    Die Ereignis Abfragen, die permanente Ereignisconsumer aktivieren, werden als [*Ereignis Filter*](gloss-e.md)bezeichnet. Einem einzelnen Ereignis Filter können mehrere logische Ereignisconsumer zugeordnet werden. Darüber hinaus können mehrere Ereignis Filter einem einzelnen logischen Ereignisconsumer zugeordnet werden. Der Filter ist eine Instanz von [**\_ \_ EventFilter**](--eventfilter.md).

    Ein NT-Protokoll Ereignis wird generiert, wenn die Abfrage eines permanenten Ereignis Consumers fehlschlägt. Die Quelle des Ereignisses ist WinMgmt, die Ereignis-ID ist 10, und der Ereignistyp ist Fehler.

6.  [Verknüpfen Sie den Ereignis Filter mit dem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md).

    Indem Sie den Ereignis Filter mit dem logischen Consumer verknüpfen, weisen Sie WMI an, welcher Ereignis Filter zu welchem logischen Consumer gehört. Logische Ereignisconsumer und Ereignis Filter werden durch eine Association-Klasseninstanz von [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md)verknüpft. Wenn ein Ereignis empfangen wird, das einer Ereignis Abfrage entspricht, die in einem Ereignis Filter beschrieben wird, sucht WMI den zugeordneten logischen Ereignisconsumer, indem er die Association-Klasseninstanz betrachtet. Nachdem die Consumer-Instanz des logischen Ereignisses gefunden wurde, verwendet WMI eine Instanz der [**\_ \_ eventconsumerproviderregistration**](--eventconsumerproviderregistration.md) -Klasse, um den physischen Ereignisconsumer zu suchen und auszuführen, der dieser Instanz zugeordnet ist.

7.  [Schreiben eines Ereignisconsumeranbieters](writing-an-event-consumer-provider.md).

    Der Ereignisconsumeranbieter ist ein COM-Objekt, das den physischen Consumer für WMI sucht.

 

 



