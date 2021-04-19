---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 40d26ea1-3081-4afd-8b12-bc6521fad390
ms.tgt_platform: multiple
title: E (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd162feb3936712b396db016de036f78aea35a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366162"
---
# <a name="e-wmi"></a>E (WMI)

[a](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**Ereignisklasse**
</dt> <dd>

Eine WMI-Klasse, die *Ereignisconsumer* von einer *Ereignis Abfrage* abonnieren können. Die-Klasse meldet einen bestimmten Typ von vorkommen. Beispielsweise meldet die [**Win32-Klasse \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) , dass ein bestimmter Prozess angehalten wurde.

</dd> <dt>

<span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**Ereignisconsumer**
</dt> <dd>

Ein Empfänger von Benachrichtigungen über das Eintreten eines Ereignisses. Ein Ereignisconsumer ist entweder [*temporär*](gloss-t.md) oder [*permanent*](gloss-p.md).

</dd> <dt>

<span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**Ereignisconsumeranbieter**
</dt> <dd>

Ein Anbieter, der den permanenten Ereignisconsumer festlegt, der ein bestimmtes Ereignis behandelt. Ein Ereignisconsumeranbieter wird von einer Instanz von [**\_ \_ eventconsumerproviderregistration**](--eventconsumerproviderregistration.md)bei WMI registriert, die eine Liste der [*logischen*](gloss-l.md) Consumerklassen enthält, die der Ereignisconsumeranbieter unterstützt. Ein Ereignisconsumeranbieter ist ein com-Server, der [*physische*](gloss-p.md) Consumer *logischen* Consumern zuordnet. Ein Ereignisconsumeranbieter unterstützt die [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) -Schnittstelle und ist eine Komponente der permanenten consumerarchitektur.

</dd> <dt>

<span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**Ereignis Filter**
</dt> <dd>

Eine Instanz der [**\_ \_ EventFilter**](--eventfilter.md) -System Klasse, die einen Ereignistyp und die Bedingungen für die Übermittlung einer Benachrichtigung beschreibt. Ein Consumer verwendet einen Ereignis Filter, um sich zu registrieren, um Benachrichtigungen zu einem bestimmten Ereignistyp zu erhalten.

</dd> <dt>

<span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**Ereignis Anbieter**
</dt> <dd>

Ein WMI-Anbieter, der eine Quelle von Ereignissen überwacht und WMI benachrichtigt, wenn Ereignisse auftreten. Ein Ereignis Anbieter implementiert die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -und [**iwbemeventprovider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) -Schnittstellen und manchmal [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).

</dd> <dt>

<span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**Ereignis Abfrage**
</dt> <dd>

Eine [*WMI Query Language*](gloss-w.md) -Anweisung, die Ereignisconsumer zur Registrierung verwenden, um Benachrichtigungen über bestimmte Ereignisse zu erhalten. Ein Ereignisanbieter wird mit einer Ereignisabfrage für das Generieren von Benachrichtigungen über bestimmte Ereignisse registriert.

</dd> <dt>

<span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**Erweiterungs Schema**
</dt> <dd>

Die dritte Ebene des [*CIM-Schemas*](gloss-c.md), die plattformspezifische Erweiterungen des CIM-Schemas umfasst, z. b. Windows, UNIX und Exchange Server. Siehe auch [*gängiges Modell*](gloss-c.md) und Kernmodell.

</dd> <dt>

<span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**System externe-Ereignis**
</dt> <dd>

Eine Ereignis Benachrichtigung von einem Anbieter. Die meisten Anbieter erstellen eine Instanz einer Ereignisklasse, die in den MOF-Dateien des Anbieters definiert ist. Ein System externe-Ereignis erbt von [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md). Der [Ereignisprotokoll Anbieter](/previous-versions/windows/desktop/eventlogprov/event-log-provider) definiert z. b. die Ereignisklasse [**Win32 \_ ntlogevent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). Siehe auch System internes [*Ereignis*](gloss-i.md).

</dd> </dl>

 

 
