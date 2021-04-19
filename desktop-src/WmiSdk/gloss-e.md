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
# <a name="e-wmi"></a><span data-ttu-id="0aacd-103">E (WMI)</span><span class="sxs-lookup"><span data-stu-id="0aacd-103">E (WMI)</span></span>

<span data-ttu-id="0aacd-104">[a](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="0aacd-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="0aacd-105"><span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**Ereignisklasse**</span><span class="sxs-lookup"><span data-stu-id="0aacd-105"><span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**event class**</span></span>
</dt> <dd>

<span data-ttu-id="0aacd-106">Eine WMI-Klasse, die *Ereignisconsumer* von einer *Ereignis Abfrage* abonnieren können.</span><span class="sxs-lookup"><span data-stu-id="0aacd-106">A WMI class that *event consumers* can subscribe to by an *event query*.</span></span> <span data-ttu-id="0aacd-107">Die-Klasse meldet einen bestimmten Typ von vorkommen.</span><span class="sxs-lookup"><span data-stu-id="0aacd-107">The class reports a specific type of occurrence.</span></span> <span data-ttu-id="0aacd-108">Beispielsweise meldet die [**Win32-Klasse \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) , dass ein bestimmter Prozess angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="0aacd-108">For example, the [**Win32\_ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) class reports that a specific process has stopped.</span></span>

</dd> <dt>

<span data-ttu-id="0aacd-109"><span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**Ereignisconsumer**</span><span class="sxs-lookup"><span data-stu-id="0aacd-109"><span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**event consumer**</span></span>
</dt> <dd>

<span data-ttu-id="0aacd-110">Ein Empfänger von Benachrichtigungen über das Eintreten eines Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="0aacd-110">A recipient of notifications that report an occurrence of an event.</span></span> <span data-ttu-id="0aacd-111">Ein Ereignisconsumer ist entweder [*temporär*](gloss-t.md) oder [*permanent*](gloss-p.md).</span><span class="sxs-lookup"><span data-stu-id="0aacd-111">An event consumer is either [*temporary*](gloss-t.md) or [*permanent*](gloss-p.md).</span></span>

</dd> <dt>

<span data-ttu-id="0aacd-112"><span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**Ereignisconsumeranbieter**</span><span class="sxs-lookup"><span data-stu-id="0aacd-112"><span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**event consumer provider**</span></span>
</dt> <dd>

<span data-ttu-id="0aacd-113">Ein Anbieter, der den permanenten Ereignisconsumer festlegt, der ein bestimmtes Ereignis behandelt.</span><span class="sxs-lookup"><span data-stu-id="0aacd-113">A provider that determines which permanent event consumer handles a given event.</span></span> <span data-ttu-id="0aacd-114">Ein Ereignisconsumeranbieter wird von einer Instanz von [**\_ \_ eventconsumerproviderregistration**](--eventconsumerproviderregistration.md)bei WMI registriert, die eine Liste der [*logischen*](gloss-l.md) Consumerklassen enthält, die der Ereignisconsumeranbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0aacd-114">An event consumer provider is registered with WMI by an instance of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md), which contains a list of the [*logical consumer*](gloss-l.md) classes that the event consumer provider supports.</span></span> <span data-ttu-id="0aacd-115">Ein Ereignisconsumeranbieter ist ein com-Server, der [*physische*](gloss-p.md) Consumer *logischen* Consumern zuordnet.</span><span class="sxs-lookup"><span data-stu-id="0aacd-115">An event consumer provider is a COM server that maps [*physical consumers*](gloss-p.md) to *logical consumers*.</span></span> <span data-ttu-id="0aacd-116">Ein Ereignisconsumeranbieter unterstützt die [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) -Schnittstelle und ist eine Komponente der permanenten consumerarchitektur.</span><span class="sxs-lookup"><span data-stu-id="0aacd-116">An event consumer provider supports the [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface and is a component of the permanent consumer architecture.</span></span>

</dd> <dt>

<span data-ttu-id="0aacd-117"><span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**Ereignis Filter**</span><span class="sxs-lookup"><span data-stu-id="0aacd-117"><span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**event filter**</span></span>
</dt> <dd>

<span data-ttu-id="0aacd-118">Eine Instanz der [**\_ \_ EventFilter**](--eventfilter.md) -System Klasse, die einen Ereignistyp und die Bedingungen für die Übermittlung einer Benachrichtigung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0aacd-118">An instance of the [**\_\_EventFilter**](--eventfilter.md) system class that describes an event type and the conditions for delivering a notification.</span></span> <span data-ttu-id="0aacd-119">Ein Consumer verwendet einen Ereignis Filter, um sich zu registrieren, um Benachrichtigungen zu einem bestimmten Ereignistyp zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0aacd-119">A consumer uses an event filter to register to receive notification of a specific type of event.</span></span>

</dd> <dt>

<span data-ttu-id="0aacd-120"><span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**Ereignis Anbieter**</span><span class="sxs-lookup"><span data-stu-id="0aacd-120"><span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**event provider**</span></span>
</dt> <dd>

<span data-ttu-id="0aacd-121">Ein WMI-Anbieter, der eine Quelle von Ereignissen überwacht und WMI benachrichtigt, wenn Ereignisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="0aacd-121">A WMI provider that monitors a source of events and notifies WMI when events occur.</span></span> <span data-ttu-id="0aacd-122">Ein Ereignis Anbieter implementiert die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -und [**iwbemeventprovider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) -Schnittstellen und manchmal [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).</span><span class="sxs-lookup"><span data-stu-id="0aacd-122">An event provider implements the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) interfaces, and sometimes [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).</span></span>

</dd> <dt>

<span data-ttu-id="0aacd-123"><span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**Ereignis Abfrage**</span><span class="sxs-lookup"><span data-stu-id="0aacd-123"><span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**event query**</span></span>
</dt> <dd>

<span data-ttu-id="0aacd-124">Eine [*WMI Query Language*](gloss-w.md) -Anweisung, die Ereignisconsumer zur Registrierung verwenden, um Benachrichtigungen über bestimmte Ereignisse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0aacd-124">A [*WMI Query Language*](gloss-w.md) statement that event consumers use to register to receive notification of specific events.</span></span> <span data-ttu-id="0aacd-125">Ein Ereignisanbieter wird mit einer Ereignisabfrage für das Generieren von Benachrichtigungen über bestimmte Ereignisse registriert.</span><span class="sxs-lookup"><span data-stu-id="0aacd-125">An event provider uses an event query to register to generate notifications of specific events.</span></span>

</dd> <dt>

<span data-ttu-id="0aacd-126"><span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**Erweiterungs Schema**</span><span class="sxs-lookup"><span data-stu-id="0aacd-126"><span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**extension schema**</span></span>
</dt> <dd>

<span data-ttu-id="0aacd-127">Die dritte Ebene des [*CIM-Schemas*](gloss-c.md), die plattformspezifische Erweiterungen des CIM-Schemas umfasst, z. b. Windows, UNIX und Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0aacd-127">The third layer of the [*CIM schema*](gloss-c.md), which includes platform-specific extensions of the CIM schema such as Windows, UNIX, and Exchange Server.</span></span> <span data-ttu-id="0aacd-128">Siehe auch [*gängiges Modell*](gloss-c.md) und Kernmodell.</span><span class="sxs-lookup"><span data-stu-id="0aacd-128">Also see [*common model*](gloss-c.md) and core model.</span></span>

</dd> <dt>

<span data-ttu-id="0aacd-129"><span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**System externe-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="0aacd-129"><span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**extrinsic event**</span></span>
</dt> <dd>

<span data-ttu-id="0aacd-130">Eine Ereignis Benachrichtigung von einem Anbieter.</span><span class="sxs-lookup"><span data-stu-id="0aacd-130">An event notification from a provider.</span></span> <span data-ttu-id="0aacd-131">Die meisten Anbieter erstellen eine Instanz einer Ereignisklasse, die in den MOF-Dateien des Anbieters definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0aacd-131">Most providers create an instance of an event class defined in the provider MOF files.</span></span> <span data-ttu-id="0aacd-132">Ein System externe-Ereignis erbt von [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md).</span><span class="sxs-lookup"><span data-stu-id="0aacd-132">An extrinsic event inherits from [**\_\_ExtrinsicEvent**](--extrinsicevent.md).</span></span> <span data-ttu-id="0aacd-133">Der [Ereignisprotokoll Anbieter](/previous-versions/windows/desktop/eventlogprov/event-log-provider) definiert z. b. die Ereignisklasse [**Win32 \_ ntlogevent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span><span class="sxs-lookup"><span data-stu-id="0aacd-133">For example, the [Event Log Provider](/previous-versions/windows/desktop/eventlogprov/event-log-provider) defines the event class [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span> <span data-ttu-id="0aacd-134">Siehe auch System internes [*Ereignis*](gloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="0aacd-134">Also see [*intrinsic event*](gloss-i.md).</span></span>

</dd> </dl>

 

 
