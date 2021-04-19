---
description: Der System Ereignis Benachrichtigungsdienst funktioniert mit dem com+-Ereignis System.
ms.assetid: c51d1f61-6087-4480-b989-31241829781b
title: Sens-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32976a716ab0ba5651ce6605fe524d639820696
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355329"
---
# <a name="sens-architecture"></a><span data-ttu-id="fe916-103">Sens-Architektur</span><span class="sxs-lookup"><span data-stu-id="fe916-103">SENS Architecture</span></span>

<span data-ttu-id="fe916-104">Der System Ereignis Benachrichtigungsdienst funktioniert mit dem com+-Ereignis System.</span><span class="sxs-lookup"><span data-stu-id="fe916-104">The System Event Notification Service works with the COM+ Event System.</span></span> <span data-ttu-id="fe916-105">Sens ist ein Ereignis Herausgeber für die Klassen von Ereignissen, die er überwacht: Netzwerk-, Anmeldungs-und Strom-/Akku-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="fe916-105">SENS is an event publisher for the classes of events that it monitors: network, logon, and power/battery events.</span></span> <span data-ttu-id="fe916-106">Die Anwendung, die eine Benachrichtigung empfängt, wird als Ereignis Abonnent bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fe916-106">The application receiving a notification is called an event subscriber.</span></span>

<span data-ttu-id="fe916-107">Wenn eine Anwendung Benachrichtigungen empfängt, kann Sie auch Filter angeben, die den abonnierten Ereignissen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fe916-107">When an application subscribes to receive notifications, it can also specify filters associated with the subscribed events.</span></span> <span data-ttu-id="fe916-108">Die Ereignisse "Sens" und "com+" verwenden die Filter, um festzustellen, wann die Anwendung benachrichtigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe916-108">SENS and COM+ Events use the filters to further determine when the application should be notified.</span></span>

<span data-ttu-id="fe916-109">Benachrichtigungen sind asynchron, sodass die Anwendung, die die Benachrichtigung empfängt, nicht aktiv sein muss, wenn die Benachrichtigung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe916-109">Notifications are asynchronous, so the application receiving the notification does not have to be active when the notification is sent.</span></span> <span data-ttu-id="fe916-110">Wenn eine Anwendung Benachrichtigungen empfängt, kann Sie angeben, ob Sie bei Auftreten des Ereignisses aktiviert oder später benachrichtigt werden soll, wenn Sie aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="fe916-110">When an application subscribes to receive notifications, it can specify whether it should be activated when the event occurs or notified later when it is active.</span></span>

<span data-ttu-id="fe916-111">Das Abonnement kann vorübergehend und gültig sein, bis die Anwendung beendet wird, oder es kann persistent und gültig sein, bis die Anwendung aus dem System entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="fe916-111">The subscription can be transient and valid only until the application stops running, or it can be persistent and valid until the application is removed from the system.</span></span>

<span data-ttu-id="fe916-112">Ein com+-Ereignisdaten Speicher enthält Informationen über den Ereignis Herausgeber (Sens), Ereignis Abonnenten und Filter.</span><span class="sxs-lookup"><span data-stu-id="fe916-112">A COM+ Events data store contains information about the event publisher (SENS), event subscribers, and filters.</span></span> <span data-ttu-id="fe916-113">Sens definiert auch eine ausgehende Schnittstelle für jede Ereignisklasse in einer Typbibliothek.</span><span class="sxs-lookup"><span data-stu-id="fe916-113">SENS also predefines an outgoing interface for each event class in a type library.</span></span>



| <span data-ttu-id="fe916-114">Ereignisklasse</span><span class="sxs-lookup"><span data-stu-id="fe916-114">Event class</span></span>    | <span data-ttu-id="fe916-115">GUID</span><span class="sxs-lookup"><span data-stu-id="fe916-115">GUID</span></span>                          | <span data-ttu-id="fe916-116">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="fe916-116">Interface</span></span>    |
|----------------|-------------------------------|--------------|
| <span data-ttu-id="fe916-117">Netzwerkereignisse</span><span class="sxs-lookup"><span data-stu-id="fe916-117">Network events</span></span> | <span data-ttu-id="fe916-118">sensorguid \_ EventClass- \_ Netzwerk</span><span class="sxs-lookup"><span data-stu-id="fe916-118">SENSGUID\_EVENTCLASS\_NETWORK</span></span> | <span data-ttu-id="fe916-119">Isensnetwork</span><span class="sxs-lookup"><span data-stu-id="fe916-119">ISensNetwork</span></span> |
| <span data-ttu-id="fe916-120">Anmeldeereignisse</span><span class="sxs-lookup"><span data-stu-id="fe916-120">Logon events</span></span>   | <span data-ttu-id="fe916-121">sensorguid \_ EventClass- \_ Anmeldung</span><span class="sxs-lookup"><span data-stu-id="fe916-121">SENSGUID\_EVENTCLASS\_LOGON</span></span>   | <span data-ttu-id="fe916-122">Isenslogon</span><span class="sxs-lookup"><span data-stu-id="fe916-122">ISensLogon</span></span>   |
| <span data-ttu-id="fe916-123">Energie Ereignisse</span><span class="sxs-lookup"><span data-stu-id="fe916-123">Power events</span></span>   | <span data-ttu-id="fe916-124">sensguid \_ EventClass \_ OnNow</span><span class="sxs-lookup"><span data-stu-id="fe916-124">SENSGUID\_EVENTCLASS\_ONNOW</span></span>   | <span data-ttu-id="fe916-125">Isennow</span><span class="sxs-lookup"><span data-stu-id="fe916-125">ISensOnNow</span></span>   |



 

<span data-ttu-id="fe916-126">Um Benachrichtigungen für diese Ereignisse zu erhalten, muss Ihre Anwendung zwei Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="fe916-126">To receive notifications for any of these events, your application must do two things:</span></span>

-   <span data-ttu-id="fe916-127">Abonnieren Sie die für Sie interessanten Sens-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="fe916-127">Subscribe to the SENS events that interest you.</span></span> <span data-ttu-id="fe916-128">Um ein Ereignis zu abonnieren, verwenden Sie die Schnittstellen **ieventabonnement** und **ieventsystem** in COM+-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="fe916-128">To subscribe to an event, use the **IEventSubscription** and **IEventSystem** interfaces in COM+ Events.</span></span> <span data-ttu-id="fe916-129">Sie müssen einen Bezeichner für die Ereignis Klassen und den Sens-Verleger Bezeichner, sensorguid Publisher, angeben \_ .</span><span class="sxs-lookup"><span data-stu-id="fe916-129">You need to supply an identifier for the event classes and the SENS publisher identifier, SENSGUID\_PUBLISHER.</span></span> <span data-ttu-id="fe916-130">Abonnements sind auf der Ebene pro Ereignis festgelegt, sodass die abonnierende Anwendung auch angeben muss, welche Ereignisse in der Klasse von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="fe916-130">Subscriptions are on a per event level so the subscribing application must also specify which events within the class are of interest.</span></span> <span data-ttu-id="fe916-131">Jedes Ereignis entspricht einer Methode in der-Schnittstelle, die der-Ereignisklasse entspricht.</span><span class="sxs-lookup"><span data-stu-id="fe916-131">Each event corresponds to a method in the interface corresponding to its event class.</span></span>
-   <span data-ttu-id="fe916-132">Erstellen Sie ein Sink-Objekt mit einer Implementierung für jede Schnittstelle, die Sie verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="fe916-132">Create a sink object with an implementation for each interface that you handle.</span></span> <span data-ttu-id="fe916-133">Weitere Informationen zu diesen Schnittstellen und den jeweils unterstützten Ereignissen finden Sie unter [**isensnetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**isenslogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)und [**isensonnow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) .</span><span class="sxs-lookup"><span data-stu-id="fe916-133">See [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon), and [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) for more information about these interfaces and the events supported in each one.</span></span>

<span data-ttu-id="fe916-134">Wenn eines der überwachten Ereignisse auftritt, verarbeitet Sens jedes Abonnement mit zugeordneten Filtern und benachrichtigt die Abonnenten über das com+-Ereignis System.</span><span class="sxs-lookup"><span data-stu-id="fe916-134">When one of the monitored events occurs, SENS processes each subscription with any associated filters and notifies the subscribers through the COM+ Event system.</span></span>

 

 



