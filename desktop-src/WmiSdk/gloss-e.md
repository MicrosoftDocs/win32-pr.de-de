---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 40d26ea1-3081-4afd-8b12-bc6521fad390
ms.tgt_platform: multiple
title: E (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbd1ce4685ee9901dfedca2a4b3a1b948d91c8f5b56def28494eb6c4c63e726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319219"
---
# <a name="e-wmi"></a>E (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F G](gloss-f.md) [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) T [U](gloss-t.md) V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**Event-Klasse**
</dt> <dd>

Eine WMI-Klasse, die *Ereignisverbraucher* von einer Ereignisabfrage *abonnieren können.* Die -Klasse meldet einen bestimmten Vorkommenstyp. Die [**Win32 \_ ProcessStopTrace-Klasse**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) meldet beispielsweise, dass ein bestimmter Prozess beendet wurde.

</dd> <dt>

<span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**Ereignisverbraucher**
</dt> <dd>

Ein Empfänger von Benachrichtigungen über das Eintreten eines Ereignisses. Ein Ereignis consumer ist entweder temporär [*oder*](gloss-t.md) [*permanent.*](gloss-p.md)

</dd> <dt>

<span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**Ereignisverbraucheranbieter**
</dt> <dd>

Ein Anbieter, der den permanenten Ereignisconsumer festlegt, der ein bestimmtes Ereignis behandelt. Ein Ereignisconsumeranbieter wird bei WMI von einer Instanz von [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)registriert, die eine Liste der logischen Consumerklassen enthält, die der Ereignisconsumeranbieter unterstützt. [](gloss-l.md) Ein Ereignisverbraucheranbieter ist ein COM-Server, der [*physische Consumer logischen*](gloss-p.md) *Consumern zu ordnet.* Ein Ereignisconsumeranbieter unterstützt die [**IWbemEventConsumerProvider-Schnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) und ist eine Komponente der permanenten Consumerarchitektur.

</dd> <dt>

<span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**Ereignisfilter**
</dt> <dd>

Eine Instanz der [**\_ \_ EventFilter-Systemklasse,**](--eventfilter.md) die einen Ereignistyp und die Bedingungen für die Bereitstellung einer Benachrichtigung beschreibt. Ein Consumer verwendet einen Ereignisfilter, um sich zu registrieren, um Benachrichtigungen über einen bestimmten Ereignistyp zu erhalten.

</dd> <dt>

<span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**Ereignisanbieter**
</dt> <dd>

Ein WMI-Anbieter, der eine Ereignisquelle überwacht und WMI benachrichtigt, wenn Ereignisse auftreten. Ein Ereignisanbieter implementiert die [**Schnittstellen IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) und [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) und [**manchmal IWbemEventProviderQuerySink.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)

</dd> <dt>

<span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**Ereignisabfrage**
</dt> <dd>

Eine [*WMI Query Language,*](gloss-w.md) die Ereignisverbraucher zum Registrieren verwenden, um Benachrichtigungen über bestimmte Ereignisse zu empfangen. Ein Ereignisanbieter wird mit einer Ereignisabfrage für das Generieren von Benachrichtigungen über bestimmte Ereignisse registriert.

</dd> <dt>

<span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**Erweiterungsschema**
</dt> <dd>

Die dritte Ebene des [*CIM-Schemas,*](gloss-c.md)die plattformspezifische Erweiterungen des CIM-Schemas wie Windows, UNIX und Exchange Server. Siehe auch [*allgemeines Modell*](gloss-c.md) und Kernmodell.

</dd> <dt>

<span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**Extrinsisches Ereignis**
</dt> <dd>

Eine Ereignisbenachrichtigung von einem Anbieter. Die meisten Anbieter erstellen eine Instanz einer Ereignisklasse, die in den MOF-Anbieterdateien definiert ist. Ein extrinsisches Ereignis erbt von [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md). Beispielsweise definiert der [Ereignisprotokollanbieter](/previous-versions/windows/desktop/eventlogprov/event-log-provider) die Ereignisklasse [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). Siehe auch [*systeminternes Ereignis*](gloss-i.md).

</dd> </dl>

 

 
