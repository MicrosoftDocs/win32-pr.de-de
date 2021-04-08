---
description: Nachdem Sie den logischen Ereignisconsumer und den Ereignis Filter erstellt haben, müssen Sie diese verknüpfen, wodurch der logische Consumer registriert wird, um Benachrichtigungen zu den vom Filter angegebenen Ereignissen zu erhalten.
ms.assetid: 2fc3d781-2b93-4e9e-90a1-1b975ab40a01
ms.tgt_platform: multiple
title: Binden eines Ereignis Filters mit einem logischen Consumer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f44c4b64b98877231b73543d8753c765c3219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867788"
---
# <a name="binding-an-event-filter-with-a-logical-consumer"></a><span data-ttu-id="f536f-103">Binden eines Ereignis Filters mit einem logischen Consumer</span><span class="sxs-lookup"><span data-stu-id="f536f-103">Binding an Event Filter with a Logical Consumer</span></span>

<span data-ttu-id="f536f-104">Nachdem Sie den logischen Ereignisconsumer und den Ereignis Filter erstellt haben, müssen Sie diese verknüpfen, wodurch der logische Consumer registriert wird, um Benachrichtigungen zu den vom Filter angegebenen Ereignissen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f536f-104">After you create the logical event consumer and the event filter you must link them, which registers the logical consumer to receive notification about the events specified by the filter.</span></span>

<span data-ttu-id="f536f-105">Im folgenden Verfahren wird beschrieben, wie ein Ereignis Filter an einen logischen Consumer gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="f536f-105">The following procedure describes how to bind an event filter with a logical consumer.</span></span>

<span data-ttu-id="f536f-106">**So binden Sie einen Ereignis Filter mit einem logischen Consumer**</span><span class="sxs-lookup"><span data-stu-id="f536f-106">**To bind an event filter with a logical consumer**</span></span>

1.  <span data-ttu-id="f536f-107">Erstellen Sie eine Instanz der [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) -System Klasse im WMI-Repository.</span><span class="sxs-lookup"><span data-stu-id="f536f-107">Create an instance of the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) system class in the WMI repository.</span></span>

    <span data-ttu-id="f536f-108">Die [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) -Klasse ist eine Association-Klasse, die die Ereignis Filter Instanz und die logische consumerinstanz über  die Filter **-und** consumerverweiseigenschaften verknüpft.</span><span class="sxs-lookup"><span data-stu-id="f536f-108">The [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) class is an association class that links the event filter instance and the logical consumer instance together through the **Filter** and **Consumer** reference properties.</span></span> <span data-ttu-id="f536f-109">Weitere Informationen finden Sie unter [Deklarieren einer Association-Klasse](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="f536f-109">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

2.  <span data-ttu-id="f536f-110">Legen Sie die **Filter** -Eigenschaft auf die Instanz des Filters fest.</span><span class="sxs-lookup"><span data-stu-id="f536f-110">Set the **Filter** property to the instance of your filter.</span></span>
3.  <span data-ttu-id="f536f-111">Legen Sie die Eigenschaft **Consumer** auf die Instanz des logischen Consumers fest.</span><span class="sxs-lookup"><span data-stu-id="f536f-111">Set the **Consumer** property to the instance of your logical consumer.</span></span>
4.  <span data-ttu-id="f536f-112">Legen Sie die Eigenschaft **deliversynchron** fest, um den gewünschten Typ der Übermittlung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f536f-112">Set the **DeliverSynchronously** property to determine the type of delivery you want.</span></span>

    <span data-ttu-id="f536f-113">Die **deliversynchron** -Eigenschaft bestimmt, wann WMI Ereignis Benachrichtigungen synchron oder asynchron bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f536f-113">The **DeliverSynchronously** property determines when WMI delivers event notifications synchronously or asynchronously.</span></span> <span data-ttu-id="f536f-114">Wenn Sie diese Eigenschaft auf **true** festlegen, wird eine synchrone Übermittlung angefordert.</span><span class="sxs-lookup"><span data-stu-id="f536f-114">Setting this property to **TRUE** requests a synchronous delivery.</span></span> <span data-ttu-id="f536f-115">Verwenden Sie die synchrone Übermittlung nur dann, wenn der permanente Consumer Ereignisse innerhalb von ungefähr 100 Mikrosekunden verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="f536f-115">Use synchronous delivery only when the permanent consumer can process events within approximately 100 microseconds.</span></span>

    > [!Note]  
    > <span data-ttu-id="f536f-116">Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f536f-116">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="f536f-117">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f536f-117">For more information, see [Calling a Method](calling-a-method.md).</span></span>

     

5.  <span data-ttu-id="f536f-118">Stellen Sie beim Aufheben der Registrierung des logischen Ereignisconsumers sicher, dass Sie die [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) -Instanz löschen.</span><span class="sxs-lookup"><span data-stu-id="f536f-118">When unregistering your logical event consumer, ensure you delete the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance.</span></span>

    <span data-ttu-id="f536f-119">Jede [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) -Instanz stellt eine Registrierung für eine bestimmte Ereignis Benachrichtigung dar.</span><span class="sxs-lookup"><span data-stu-id="f536f-119">Each [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance represents a registration for a specific event notification.</span></span> <span data-ttu-id="f536f-120">Wenn Sie eine Bindung löschen, deaktiviert WMI die Registrierung.</span><span class="sxs-lookup"><span data-stu-id="f536f-120">When you delete a binding, WMI deactivates the registration.</span></span> <span data-ttu-id="f536f-121">Möglicherweise müssen Sie die Instanzen des logischen Consumers und des Ereignis Filters löschen, um die Registrierung abhängig von der Implementierung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="f536f-121">You might have to delete the logical consumer and event filter instances to deactivate registration, depending on the implementation.</span></span>

<span data-ttu-id="f536f-122">Im folgenden Codebeispiel wird eine [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) -Instanz veranschaulicht, die eine Instanz einer [**activescripteventconsumer**](activescripteventconsumer.md) -Klasse mit einem bestimmten Ereignis Filter verknüpft (die Instanz des Ereignisconsumers wurde im Thema [Erstellen eines logischen](creating-a-logical-consumer.md) Consumers erstellt, und der Ereignis Filter wurde im Thema [Erstellen eines Ereignis Filters](creating-an-event-filter.md) erstellt).</span><span class="sxs-lookup"><span data-stu-id="f536f-122">The following code example shows you a [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance that associates an instance of an [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class with a specific event filter (the instance of the event consumer was created in the [Creating a Logical Consumer](creating-a-logical-consumer.md) topic, and the event filter was created in the [Creating an Event Filter](creating-an-event-filter.md) topic).</span></span>

``` syntax
instance of __FilterToConsumerBinding
{
    Filter = $FILTER;
    Consumer = $CONSUMER;
    DeliverSynchronously=FALSE;

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="f536f-123">Zwei Consumer, [**activescripteventconsumer**](activescripteventconsumer.md) und [**commandlineeventconsumer**](commandlineeventconsumer.md), funktionieren nur, wenn Ihr Ersteller Mitglied der lokalen Administratoren Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="f536f-123">Two consumers, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) and [**CommandLineEventConsumer**](commandlineeventconsumer.md), will not work unless their creator is a member of the local Administrators group.</span></span>

<span data-ttu-id="f536f-124">**:** Wenn ein Administrator ein Abonnement erstellt, wird seine SID nicht für die Eigenschaft " **kreatorsid** " verwendet, sondern stattdessen die SID der lokalen Gruppe "Administratoren".</span><span class="sxs-lookup"><span data-stu-id="f536f-124">**:** When an administrator creates a subscription, his SID is not used for the **CreatorSID** property, but the SID of the local Administrators group is used instead.</span></span> <span data-ttu-id="f536f-125">Daher können Instanzen von verschiedenen Administratoren erstellt werden, und das Abonnement funktioniert weiterhin.</span><span class="sxs-lookup"><span data-stu-id="f536f-125">Therefore, instances can be created by different administrators and the subscription will still work.</span></span> <span data-ttu-id="f536f-126">Weitere Informationen finden Sie unter [sicheres empfangen von Ereignissen](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="f536f-126">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="f536f-127">Wenn ein Filter an einen logischen Consumer gebunden ist, wird das Ereignis von der [Ereignis Ablauf Verfolgung](/windows/desktop/ETW/event-tracing-portal) für Windows (ETW) aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f536f-127">When a filter is bound to a logical consumer the event is recorded by [Event Tracing](/windows/desktop/ETW/event-tracing-portal) for Windows (ETW).</span></span> <span data-ttu-id="f536f-128">Weitere Informationen finden Sie unter Ablauf [Verfolgung von WMI-Aktivitäten](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="f536f-128">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f536f-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f536f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f536f-130">Empfangen von Ereignissen zu allen Zeitpunkten</span><span class="sxs-lookup"><span data-stu-id="f536f-130">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

 
