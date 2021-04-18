---
description: Ein Ereignis Filter ist eine WMI-Klasse, die beschreibt, welche Ereignisse WMI an einen physischen Consumer übergibt.
ms.assetid: c0ce26a4-5ff2-44b4-8550-c7d8ad0ba0f0
ms.tgt_platform: multiple
title: Erstellen eines Ereignis Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693e4ef2eee5de14550b8efbf25a9b6720d6a8b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351137"
---
# <a name="creating-an-event-filter"></a><span data-ttu-id="6cc4a-103">Erstellen eines Ereignis Filters</span><span class="sxs-lookup"><span data-stu-id="6cc4a-103">Creating an Event Filter</span></span>

<span data-ttu-id="6cc4a-104">Ein Ereignis Filter ist eine WMI-Klasse, die beschreibt, welche Ereignisse WMI an einen physischen Consumer übergibt.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-104">An event filter is a WMI class that describes which events WMI delivers to a physical consumer.</span></span> <span data-ttu-id="6cc4a-105">Beispielsweise kann ein Ereignis Filter WMI anweisen, alle Energie Verwaltungs Ereignisse oder alle Systemneustart Ereignisse an einen Consumer zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-105">For example, an event filter can instruct WMI to deliver to a consumer all power management events, or all system reboot events.</span></span> <span data-ttu-id="6cc4a-106">Ein Ereignis Filter beschreibt auch die Bedingungen, unter denen WMI die Ereignisse übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-106">An event filter also describes the conditions under which WMI delivers the events.</span></span> <span data-ttu-id="6cc4a-107">Ein Ereignis Filter kann ein System internes oder ein extrinsisches Ereignis angeben. und der Filter kann auf Ereignisse verweisen, die aus dem-Namespace stammen, d. –. mit Ausnahme des Namespace des Filters.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-107">An event filter can specify an intrinsic or extrinsic event; and the filter can refer to events that originate in the namespace—that is, other than the namespace of the filter.</span></span> <span data-ttu-id="6cc4a-108">Der permanente Consumer muss in den Consumer-, Filter-und Binding-Instanzen die gleiche " [**kreatorsid**](--eventconsumer.md) " aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-108">The permanent consumer must have the same [**CreatorSID**](--eventconsumer.md) in the consumer, filter, and binding instances.</span></span> <span data-ttu-id="6cc4a-109">Weitere Informationen finden Sie unter [sicheres empfangen von Ereignissen](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="6cc4a-109">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="6cc4a-110">Im folgenden Verfahren wird beschrieben, wie ein Ereignis Filter erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-110">The following procedure describes how to create an event filter.</span></span>

<span data-ttu-id="6cc4a-111">**So erstellen Sie einen Ereignis Filter**</span><span class="sxs-lookup"><span data-stu-id="6cc4a-111">**To create an event filter**</span></span>

1.  <span data-ttu-id="6cc4a-112">Erstellen Sie eine Instanz der WMI- [**\_ \_ EventFilter**](--eventfilter.md) -System Klasse.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-112">Create an instance of the WMI [**\_\_EventFilter**](--eventfilter.md) system class.</span></span>
2.  <span data-ttu-id="6cc4a-113">Erstellen Sie einen eindeutigen Bezeichner für Ihren Filter mit der **Name** -Eigenschaft auf zwei Arten:</span><span class="sxs-lookup"><span data-stu-id="6cc4a-113">Create a unique identifier for your filter with the **Name** property, in one of two ways:</span></span>

    -   <span data-ttu-id="6cc4a-114">Verwenden Sie ein privates Schema.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-114">Use a private scheme.</span></span>

        <span data-ttu-id="6cc4a-115">Das willkürliche benennen ihrer Ereignis Filter funktioniert, solange Sie nicht mit anderen Filter Benennungs Schemas in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-115">Arbitrarily naming your event filters works as long as you do not conflict with other filter naming schemes.</span></span> <span data-ttu-id="6cc4a-116">Benennungs Konflikte müssen vermieden werden, da das Hinzufügen einer Instanz mit einem doppelten **namens** Wert die alte Instanz überschreibt.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-116">You must avoid naming conflicts because adding an instance with a duplicate **Name** value overwrites the old instance.</span></span>

    -   <span data-ttu-id="6cc4a-117">Verwenden Sie einen Globally Unique Identifier (GUID).</span><span class="sxs-lookup"><span data-stu-id="6cc4a-117">Use a globally unique identifier (GUID).</span></span>

        <span data-ttu-id="6cc4a-118">Wenn Sie den **Namen** leer lassen, füllt WMI den **Namen** mit einer GUID aus.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-118">If you leave **Name** empty, WMI fills **Name** with a GUID.</span></span>

3.  <span data-ttu-id="6cc4a-119">Beschreiben Sie den Ereignistyp, den Sie mit der **Query** -Eigenschaft filtern möchten.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-119">Describe the type of event you want filtered with the **Query** property.</span></span>

    <span data-ttu-id="6cc4a-120">Die **Query** -Eigenschaft enthält die WMI Query Language (WQL)-Abfrage, die den Typ des zu filternden Ereignisses beschreibt.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-120">The **Query** property contains the WMI Query Language (WQL) query that describes the type of event you want filtered.</span></span> <span data-ttu-id="6cc4a-121">Sie können mit einer Vielzahl von Operatoren und Erweiterungen von WQL eine exakte Filterung erzielen.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-121">You can achieve precise filtering using a variety of operators and extensions to WQL.</span></span>

    <span data-ttu-id="6cc4a-122">Ein NT-Protokoll Ereignis wird generiert, wenn eine Abfrage von einem permanenten Ereignisconsumer fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-122">An NT Log event is generated when a query from a permanent event consumer fails.</span></span> <span data-ttu-id="6cc4a-123">Die Quelle des Ereignisses ist WinMgmt, die Ereignis-ID ist 10, und der Ereignistyp ist Fehler.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-123">The event's source is WinMgmt, the event ID is 10, and the event type is Error.</span></span>

    <span data-ttu-id="6cc4a-124">WMI ist effizienter bei der Verarbeitung restriktiver, spezifischer Abfragen als bei umfangreichen Abfragen.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-124">WMI is more efficient at processing restrictive, specific queries than broad queries.</span></span> <span data-ttu-id="6cc4a-125">Indem Sie eine bestimmte Abfrage erstellen, können Sie unnötige prozessübergreifende Kommunikation und Netzwerk Datenverkehr vermeiden.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-125">By creating a specific query, you can avoid unnecessary inter-process communication and network traffic.</span></span> <span data-ttu-id="6cc4a-126">Bei Ereignissen, die von einem Anbieter generiert werden, führt WMI die Filterung im Prozess für den Anbieter durch. Dadurch wird sichergestellt, dass nur Ereignisse, die dem Filter entsprechen, die Kosten für die prozessübergreifende Kommunikation verursachen</span><span class="sxs-lookup"><span data-stu-id="6cc4a-126">In cases of events generated by a provider, WMI performs the filtering in process to the provider; this ensures that only events matching the filter incur the interprocess communication cost.</span></span> <span data-ttu-id="6cc4a-127">Weitere Informationen finden Sie unter [WMI-Abfrage](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6cc4a-127">For more information, see [Querying WMI](querying-wmi.md).</span></span>

4.  <span data-ttu-id="6cc4a-128">Legen Sie die **QueryLanguage** -Eigenschaft auf den Typ der Abfragesprache fest, den Sie in der **Query** -Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-128">Set the **QueryLanguage** property to the type of query language you use in the **Query** property.</span></span>

    <span data-ttu-id="6cc4a-129">Sie legen " **QueryLanguage** " fast immer auf "WQL" fest.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-129">You will almost always set **QueryLanguage** to "WQL".</span></span>

<span data-ttu-id="6cc4a-130">Im folgenden Codebeispiel wird ein Ereignis Filter beschrieben, der jedes Mal ein Ereignis signalisiert, wenn WMI eine Instanz der [**\_ \_ TimerEvent**](--timerevent.md) -Klasse im root \\ CIMV2-Namespace erstellt.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-130">The following code example describes an event filter that signals an event each time WMI creates an instance of the [**\_\_TimerEvent**](--timerevent.md) class in the root\\cimv2 namespace.</span></span>

``` syntax
instance of __EventFilter as $FILTER
{
    Name = "MyFilterName";
    Query = "select * from __TimerEvent where TimerID=\"MyTimer\"";
    QueryLanguage = "WQL";
    EventNamespace = "\root\cimv2";

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="6cc4a-131">Die **eventnamespace** -Eigenschaft gibt den Namespace an, von dem die Ereignisse stammen.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-131">The **EventNamespace** property specifies the namespace from which the events originate.</span></span> <span data-ttu-id="6cc4a-132">Sie müssen keine Instanz der Filter in dem Namespace erstellen, von dem die Ereignisse stammen.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-132">You do not have to create an instance of the filters in the namespace where the events originate.</span></span> <span data-ttu-id="6cc4a-133">Wenn Sie den Namespace nicht angeben, erstellt WMI den Filter im Standard Namespace.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-133">If you do not specify the namespace, then WMI creates the filter in the default namespace.</span></span> <span data-ttu-id="6cc4a-134">Die systeminternen Ereignis Klassen, z. b. [**\_ \_ instanceoperationevent**](--instanceoperationevent.md) , sind in jedem Namespace verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-134">The intrinsic events classes, such as [**\_\_InstanceOperationEvent**](--instanceoperationevent.md) are available in every namespace.</span></span>

<span data-ttu-id="6cc4a-135">Um den logischen Consumer für Ereignis Benachrichtigungen zu registrieren, müssen Sie die Ereignis Filter an einen logischen Consumer binden.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-135">To register your logical consumer for event notifications, you must bind the event filters to a logical consumer.</span></span> <span data-ttu-id="6cc4a-136">Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="6cc4a-136">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

 

 



