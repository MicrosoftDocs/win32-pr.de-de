---
description: Wird vom Microsoft Internet Explorer-System Ereignis Benachrichtigungsdienst (Sens) verwendet, um auf den Ereignisdaten Speicher zuzugreifen. Diese Schnittstelle erweitert die ieventsystem-Schnittstelle.
ms.assetid: ad3c38a6-fa2d-4fcd-8782-1fac7595e829
title: IEventSystem2-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a174c9457dc347257677e8111772ad14f0dc9fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483598"
---
# <a name="ieventsystem2-interface"></a><span data-ttu-id="db71d-104">IEventSystem2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="db71d-104">IEventSystem2 interface</span></span>

<span data-ttu-id="db71d-105">Wird vom Microsoft Internet Explorer-System Ereignis Benachrichtigungsdienst (Sens) verwendet, um auf den Ereignisdaten Speicher zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="db71d-105">Used by the Microsoft Internet Explorer System Event Notification Service (SENS) to access the event data store.</span></span> <span data-ttu-id="db71d-106">Diese Schnittstelle erweitert die [**ieventsystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="db71d-106">This interface extends the [**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="db71d-107">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="db71d-107">When to implement</span></span>

<span data-ttu-id="db71d-108">Sie müssen die **IEventSystem2** -Schnittstelle nicht implementieren.</span><span class="sxs-lookup"><span data-stu-id="db71d-108">You do not need to implement the **IEventSystem2** interface.</span></span> <span data-ttu-id="db71d-109">Ein vom System bereitgestelltes Ereignis Systemobjekt (CLSID \_ ceventsystem) implementiert **IEventSystem2**.</span><span class="sxs-lookup"><span data-stu-id="db71d-109">A system-supplied event system object (CLSID\_CEventSystem) implements **IEventSystem2**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="db71d-110">Verwendung</span><span class="sxs-lookup"><span data-stu-id="db71d-110">When to use</span></span>

<span data-ttu-id="db71d-111">Wenn Sie "Sens" verwenden, können Sie die **IEventSystem2** -Methoden zum Hinzufügen und Entfernen von Objekten aus dem Ereignisspeicher und zum Abrufen von Objekten aus dem Ereignisspeicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="db71d-111">If you use SENS, you can call the methods of **IEventSystem2** to add and remove objects to and from the event store and to obtain objects from the event store.</span></span>

<span data-ttu-id="db71d-112">Da [**ieventpublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) und das Verleger Objekt nicht mehr unterstützt werden, wird [**ieventobjectchange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) nicht in der [**changedpublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="db71d-112">Because [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) and the publisher object are no longer supported, [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) is not called on the [**ChangedPublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) method.</span></span>

## <a name="members"></a><span data-ttu-id="db71d-113">Member</span><span class="sxs-lookup"><span data-stu-id="db71d-113">Members</span></span>

<span data-ttu-id="db71d-114">Die **IEventSystem2** -Schnittstelle erbt von **ieventsystem**.</span><span class="sxs-lookup"><span data-stu-id="db71d-114">The **IEventSystem2** interface inherits from **IEventSystem**.</span></span> <span data-ttu-id="db71d-115">**IEventSystem2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="db71d-115">**IEventSystem2** also has these types of members:</span></span>

-   [<span data-ttu-id="db71d-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="db71d-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="db71d-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="db71d-117">Methods</span></span>

<span data-ttu-id="db71d-118">Die **IEventSystem2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="db71d-118">The **IEventSystem2** interface has these methods.</span></span>



| <span data-ttu-id="db71d-119">Methode</span><span class="sxs-lookup"><span data-stu-id="db71d-119">Method</span></span>                                                                         | <span data-ttu-id="db71d-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db71d-120">Description</span></span>                                                                       |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="db71d-121">**GetVersion**</span><span class="sxs-lookup"><span data-stu-id="db71d-121">**GetVersion**</span></span>](ieventsystem2-getversion.md)                                 | <span data-ttu-id="db71d-122">Ruft die Versionsnummer des Ereignis Systems ab.</span><span class="sxs-lookup"><span data-stu-id="db71d-122">Retrieves the version number of the event system.</span></span><br/>                      |
| [<span data-ttu-id="db71d-123">**Verifytransientabonnenten**</span><span class="sxs-lookup"><span data-stu-id="db71d-123">**VerifyTransientSubscribers**</span></span>](ieventsystem2-verifytransientsubscribers.md) | <span data-ttu-id="db71d-124">Überprüft, ob alle vorübergehenden Abonnenten im Datenspeicher vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="db71d-124">Verifies the existence of all transient subscribers in the data store.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="db71d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db71d-125">Requirements</span></span>



| <span data-ttu-id="db71d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db71d-126">Requirement</span></span> | <span data-ttu-id="db71d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="db71d-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="db71d-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db71d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="db71d-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db71d-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="db71d-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db71d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="db71d-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db71d-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="db71d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db71d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db71d-133">**Ieventsystem**</span><span class="sxs-lookup"><span data-stu-id="db71d-133">**IEventSystem**</span></span>](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)
</dt> </dl>

 

