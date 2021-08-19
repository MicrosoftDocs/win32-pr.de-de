---
description: Möglicherweise möchten Sie eine Anwendung schreiben, die jederzeit auf Ereignisse reagieren kann.
ms.assetid: 475dca47-b1e5-4362-ab00-9ab9383e92f9
ms.tgt_platform: multiple
title: Jederzeites Empfangen von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e049b7816e53439ede5edbc67c3bcdbaf6ed6e71accb8b3f994544cdd0efbd31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817446"
---
# <a name="receiving-events-at-all-times"></a>Jederzeites Empfangen von Ereignissen

Möglicherweise möchten Sie eine Anwendung schreiben, die jederzeit auf Ereignisse reagieren kann. Ein Administrator möchte beispielsweise eine E-Mail erhalten, wenn bestimmte Leistungsindikatoren auf Netzwerkservern abgelehnt werden. In diesem Fall sollte Ihre Anwendung jederzeit ausgeführt werden. Die kontinuierliche Ausführung einer Anwendung ist jedoch keine effiziente Verwendung von Systemressourcen. Stattdessen können Sie mit WMI einen permanenten Ereignisverbraucher erstellen. Permanente Ereignisverbraucher müssen besondere Sicherheitsanforderungen erfüllen. Weitere Informationen finden Sie unter [Sichern von WMI-Ereignissen.](securing-wmi-events.md)

Ein permanenter Ereignis-Consumer empfängt Ereignisse, bis seine Registrierung explizit abgebrochen wird.

Ein permanenter Ereignisverbraucher ist eine Kombination der folgenden WMI-Klassen, Filter und COM-Objekte, die sich in Ihrem System befinden:

-   Ein COM-Objekt, das als physischer Consumer bezeichnet wird. WMI bietet mehrere permanente Standardverbraucher. Beispielsweise führt der Consumer des Active Script-Ereignisses [ein Skript aus, wenn ein Ereignis auftritt.](running-a-script-based-on-an-event.md)
-   Eine neue permanente Consumerklasse.
-   Eine Instanz der permanenten Consumerklasse, die als logischer Consumer bezeichnet wird.
-   Ein Filter, der die Abfrage für Ereignisse enthält.
-   Eine Verknüpfung zwischen dem Consumer und dem Filter.

Die Eigenschaften eines logischen Ereignis-Consumers geben die Aktionen an, die bei einer Benachrichtigung über ein Ereignis durchgeführt werden sollen, definieren jedoch nicht die Ereignisabfragen, denen sie zugeordnet sind. Bei Signalisierung lädt WMI automatisch das COM-Objekt, das den permanenten Ereignisverbraucher darstellt, in den aktiven Arbeitsspeicher. In der Regel tritt dies während des Starts oder als Reaktion auf ein auslösende Ereignis auf. Nach der Aktivierung fungiert der permanente Ereignisverbraucher als normaler Ereignisverbraucher, bleibt aber bestehen, bis er vom Betriebssystem speziell entladen wird.

Sie können einen eigenen permanenten Ereignisconsumer schreiben oder die vorinstallierten [Standardconsumerklassen](standard-consumer-classes.md)von WMI verwenden, z. B. [**ActiveScriptEventConsumer**](activescripteventconsumer.md). Weitere Informationen finden Sie unter [Standard-Consumerklassen,](standard-consumer-classes.md)Überwachung und Reaktion auf Ereignisse [mit Standardverbrauchern](monitoring-and-responding-to-events-with-standard-consumers.md)und [Überwachen von Ereignissen.](monitoring-events.md)

Im folgenden Verfahren wird beschrieben, wie Sie Einen eigenen permanenten Ereignisverbraucher erstellen.

**So erstellen Sie einen eigenen permanenten Ereignisverbraucher**

1.  Bestimmen Sie, welche Art von Ereignissen Sie empfangen möchten.

    WMI unterstützt systeminterne und extrinsische Ereignisse. Ein systeminternes Ereignis ist ein von WMI vordefiniertes Ereignis, während ein extrinsisches Ereignis ein Ereignis ist, das von einem Drittanbieter definiert wird. Weitere Informationen finden Sie unter [Bestimmen des Ereignistyps, der empfangen werden soll.](determining-the-type-of-event-to-receive.md)

2.  [Implementieren Sie einen physischen Consumer.](implementing-a-physical-consumer.md)

    Der Hauptunterschied zwischen einer [](gloss-p.md) Verwaltungsanwendung und einem physischen Consumer ist, dass ein Benutzer eine Verwaltungsanwendung lädt und entlädt, während WMI einen physischen Consumer lädt und entlädt. Der großteil Ihrer Codierung sollte sich im physischen Consumer beziehen.

    > [!Note]  
    > Dieser Schritt ist der erste Schritt im Verfahren, um die Erläuterung zu erleichtern. Im Hinblick auf die Codierung sollten Sie tatsächlich den physischen Consumer zuletzt erstellen. Auf diese Weise können Sie Ihre Parameter und Logik für Ihren permanenten Ereignisanbieter festlegen, bevor Sie mit der langen Codierung beginnen. Es gibt jedoch keine Einschränkung, den physischen Consumer zuerst zu schreiben.

     

3.  [Erstellen Sie eine neue Consumerklasse, die den physischen Consumer beschreibt.](creating-a-new-permanent-event-consumer-class.md)

    Wie jede Klasse beschreibt die Consumerklasse die allgemeinen Parameter eines permanenten Ereignisverbraucher für WMI.

4.  [Erstellen Sie eine Instanz der Consumerklasse](creating-a-logical-consumer.md).

    Wie jede andere WMI-Klasse müssen Sie eine Instanz der Consumerklasse erstellen, wenn Sie die Klasse implementieren möchten. Eine Instanz einer Consumerklasse wird auch als [*logischer Consumer bezeichnet.*](gloss-l.md) Der logische Consumer stellt den physischen Consumer für WMI dar.

5.  [Erstellen Sie einen Ereignisfilter.](creating-an-event-filter.md)

    Die Ereignisabfragen, die permanente Ereignisverbraucher aktivieren, werden als [*Ereignisfilter bezeichnet.*](gloss-e.md) Ein einzelner Ereignisfilter kann mehreren logischen Ereignisverbrauchern zugeordnet werden. Darüber hinaus können einem einzelnen logischen Ereignis consumer mehrere Ereignisfilter zugeordnet werden. Der Filter ist eine Instanz von [**\_ \_ EventFilter.**](--eventfilter.md)

    Ein NT-Protokollereignis wird generiert, wenn die Abfrage eines permanenten Ereignisverbraucher fehlschlägt. Die Quelle des Ereignisses ist WinMgmt, die Ereignis-ID ist 10, und der Ereignistyp ist Error.

6.  [Verknüpfen Sie den Ereignisfilter mit dem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md).

    Durch Verknüpfen des Ereignisfilters mit dem logischen Consumer weisen Sie WMI an, welcher Ereignisfilter zu welchem logischen Consumer gehört. Logische Ereignisconsumer und Ereignisfilter werden von einer Zuordnungsklasseninstanz von [**\_ \_ FilterToConsumerBinding verknüpft.**](--filtertoconsumerbinding.md) Wenn ein Ereignis empfangen wird, das einer in einem Ereignisfilter beschriebenen Ereignisabfrage entspricht, sucht WMI den zugeordneten consumer für logische Ereignisse, indem die Zuordnungsklasseninstanz betrachtet wird. Nachdem die logische Ereignisconsumerinstanz gefunden wurde, verwendet WMI eine Instanz der [**\_ \_ EventConsumerProviderRegistration-Klasse,**](--eventconsumerproviderregistration.md) um den physischen Ereignisconsumer zu suchen und ausführen, der dieser Instanz zugeordnet ist.

7.  [Schreiben eines Ereignisverbraucheranbieters.](writing-an-event-consumer-provider.md)

    Der Ereignisverbraucheranbieter ist ein COM-Objekt, das den physischen Consumer für WMI sucht.

 

 



