---
description: Ein Ereignisconsumeranbieter ist eine Komponente der permanenten consumerarchitektur, die bestimmt, welcher permanente Ereignisconsumer ein bestimmtes Ereignis behandelt.
ms.assetid: c5a0d0ec-99af-4815-9ad2-e59db70e04ce
ms.tgt_platform: multiple
title: Schreiben eines Ereignisconsumeranbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c7aeeb9b44b37d887df49cf5049d5a9e59ad72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347435"
---
# <a name="writing-an-event-consumer-provider"></a><span data-ttu-id="1fb49-103">Schreiben eines Ereignisconsumeranbieters</span><span class="sxs-lookup"><span data-stu-id="1fb49-103">Writing an Event Consumer Provider</span></span>

<span data-ttu-id="1fb49-104">Ein Ereignisconsumeranbieter ist eine Komponente der permanenten consumerarchitektur, die bestimmt, welcher permanente Ereignisconsumer ein bestimmtes Ereignis behandelt.</span><span class="sxs-lookup"><span data-stu-id="1fb49-104">An event consumer provider is a component of the permanent consumer architecture that determines which permanent event consumer handles a given event.</span></span> <span data-ttu-id="1fb49-105">Sie sollten einen Ereignisconsumeranbieter zusammen mit ihren permanenten Ereignisconsumer erstellen, um Ereignisse ordnungsgemäß aus WMI zu leiten.</span><span class="sxs-lookup"><span data-stu-id="1fb49-105">You should create an event consumer provider along with your permanent event consumers to route events properly from WMI.</span></span>

<span data-ttu-id="1fb49-106">Ein Ereignisconsumeranbieter verknüpft einen Ereignis Anbieter mit einer Liste von Consumerklassen.</span><span class="sxs-lookup"><span data-stu-id="1fb49-106">An event consumer provider links an event provider with a list of consumer classes.</span></span> <span data-ttu-id="1fb49-107">Instanzen dieser Consumerklassen empfangen dann Ereignisse von diesem Anbieter.</span><span class="sxs-lookup"><span data-stu-id="1fb49-107">Instances of these consumer classes then receive events from that provider.</span></span> <span data-ttu-id="1fb49-108">WMI identifiziert den Consumeranbieter, an den die Ereignisse übermittelt werden, basierend auf der [**\_ \_ eventconsumerproviderregistration**](--eventconsumerproviderregistration.md) -Instanz, die die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz des consumeranbieters einer logischen Consumerklasse zuordnet.</span><span class="sxs-lookup"><span data-stu-id="1fb49-108">WMI identifies which consumer provider the events are delivered to, based on the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) instance, which associates the consumer provider [**\_\_Win32Provider**](--win32provider.md) instance with a logical consumer class.</span></span> <span data-ttu-id="1fb49-109">Benutzer erstellen Instanzen der Consumer-Klasse als Teil eines permanenten Abonnements.</span><span class="sxs-lookup"><span data-stu-id="1fb49-109">Users create instances of the consumer class as part of a permanent subscription.</span></span> <span data-ttu-id="1fb49-110">Wenn der Ereignis Anbieter nicht ausgeführt wird, wenn ein Ereignis auftritt, startet WMI den Anbieter, wenn er Ereignisse übermitteln muss.</span><span class="sxs-lookup"><span data-stu-id="1fb49-110">If the event provider is not running when an event occurs, then WMI starts the provider when it needs to deliver events.</span></span>

<span data-ttu-id="1fb49-111">Im folgenden Verfahren wird beschrieben, wie ein Ereignisconsumeranbieter implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="1fb49-111">The following procedure describes how to implement an event consumer provider.</span></span>

<span data-ttu-id="1fb49-112">**So implementieren Sie einen Ereignisconsumeranbieter**</span><span class="sxs-lookup"><span data-stu-id="1fb49-112">**To implement an event consumer provider**</span></span>

1.  <span data-ttu-id="1fb49-113">Entwerfen Sie Consumerklassen in Managed Object Format (MOF), und registrieren Sie Sie bei WMI.</span><span class="sxs-lookup"><span data-stu-id="1fb49-113">Design consumer classes in Managed Object Format (MOF) and register them with WMI.</span></span> <span data-ttu-id="1fb49-114">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="1fb49-114">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

    <span data-ttu-id="1fb49-115">Klassen Anbieter registrieren sich bei WMI durch Erstellen einer [**\_ \_ Win32Provider**](--win32provider.md) -Instanz und einer [**\_ \_ eventconsumerproviderregistration**](--eventconsumerproviderregistration.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="1fb49-115">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and an [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) class.</span></span> <span data-ttu-id="1fb49-116">Weitere Informationen finden Sie unter [Registrieren eines Ereignisconsumeranbieters](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1fb49-116">For more information, see [Registering an Event Consumer Provider](registering-an-event-consumer-provider.md).</span></span>

2.  <span data-ttu-id="1fb49-117">Implementieren Sie die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle für Ihren Anbieter.</span><span class="sxs-lookup"><span data-stu-id="1fb49-117">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="1fb49-118">WMI verwendet [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) , um einen Anbieter zu laden und zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="1fb49-118">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="1fb49-119">Weitere Informationen finden Sie unter [Initialisieren eines Anbieters](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1fb49-119">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="1fb49-120">Ereignisconsumeranbietern wird dringend empfohlen, das Multithreading Modell "both" zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1fb49-120">Event consumer providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="1fb49-121">Implementieren Sie die [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) -Schnittstelle für Ihren Anbieter.</span><span class="sxs-lookup"><span data-stu-id="1fb49-121">Implement the [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface for your provider.</span></span>

    <span data-ttu-id="1fb49-122">Die [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) -Schnittstelle ist die primäre Schnittstelle für einen Ereignisconsumeranbieter.</span><span class="sxs-lookup"><span data-stu-id="1fb49-122">The [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface is the primary interface for an event consumer provider.</span></span>

4.  <span data-ttu-id="1fb49-123">Stellen Sie einen oder mehrere physische Consumer bereit, um die Ereignis Nachrichten von WMI zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="1fb49-123">Supply one or more physical consumers to receive the event messages from WMI.</span></span>

    <span data-ttu-id="1fb49-124">Ein physischer Consumer ist ein COM-Objekt, das einen permanenten Ereignisconsumer darstellt.</span><span class="sxs-lookup"><span data-stu-id="1fb49-124">A physical consumer is a COM object that represents a permanent event consumer.</span></span> <span data-ttu-id="1fb49-125">Alle physischen Consumer müssen die [**iwbemunboundobjectsink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="1fb49-125">All physical consumers must implement the [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) interface.</span></span> <span data-ttu-id="1fb49-126">Weitere Informationen finden Sie unter [Implementieren eines physischen](implementing-a-physical-consumer.md)Consumers.</span><span class="sxs-lookup"><span data-stu-id="1fb49-126">For more information, see [Implementing a Physical Consumer](implementing-a-physical-consumer.md).</span></span>

 

 



