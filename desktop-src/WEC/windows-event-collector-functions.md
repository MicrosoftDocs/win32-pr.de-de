---
title: Funktionen der Windows-Ereignis Sammlung
description: In der folgenden Liste werden die Funktionen, die in der Windows-Ereignis Sammlung verwendet werden, kurz beschrieben.
ms.assetid: 48155df6-ba9c-4abe-ba84-6190cee95878
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c20e3bbee6226d385681c7471bb7fd3f337dfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309191"
---
# <a name="windows-event-collector-functions"></a><span data-ttu-id="51dd4-103">Funktionen der Windows-Ereignis Sammlung</span><span class="sxs-lookup"><span data-stu-id="51dd4-103">Windows Event Collector Functions</span></span>

<span data-ttu-id="51dd4-104">In der folgenden Liste werden die Funktionen, die in der Windows-Ereignis Sammlung verwendet werden, kurz beschrieben.</span><span class="sxs-lookup"><span data-stu-id="51dd4-104">The following list briefly describes the functions that are used in Windows Event Collector.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="51dd4-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="51dd4-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="51dd4-106">**Ecclose**</span><span class="sxs-lookup"><span data-stu-id="51dd4-106">**EcClose**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecclose)
</dt> <dd>

<span data-ttu-id="51dd4-107">Schließt ein Handle, das von anderen Ereignis Sammler Funktionen empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="51dd4-107">Closes a handle received from other Event Collector functions.</span></span>

</dd> <dt>

[<span data-ttu-id="51dd4-108">**Ecdelta etesub-Abonnement**</span><span class="sxs-lookup"><span data-stu-id="51dd4-108">**EcDeleteSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription)
</dt> <dd>

<span data-ttu-id="51dd4-109">Löscht ein vorhandenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="51dd4-109">Deletes an existing subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="51dd4-110">**Ecenumnextabonnement**</span><span class="sxs-lookup"><span data-stu-id="51dd4-110">**EcEnumNextSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecenumnextsubscription)
</dt> <dd>

<span data-ttu-id="51dd4-111">Setzt die Enumeration der auf dem lokalen Computer registrierten Abonnements fort.</span><span class="sxs-lookup"><span data-stu-id="51dd4-111">Continues the enumeration of the subscriptions registered on the local machine.</span></span>

</dd> <dt>

[<span data-ttu-id="51dd4-112">**Ecgetobjectarrayproperty**</span><span class="sxs-lookup"><span data-stu-id="51dd4-112">**EcGetObjectArrayProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty)
</dt> <dd>

<span data-ttu-id="51dd4-113">Ruft Eigenschaftswerte für die Ereignis Quellen eines Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="51dd4-113">Retrieves property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="51dd4-114">**Ecgetobjectarraysize**</span><span class="sxs-lookup"><span data-stu-id="51dd4-114">**EcGetObjectArraySize**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarraysize)
</dt> <dd>

<span data-ttu-id="51dd4-115">Ruft die Anzahl der Indizes des Arrays von Eigenschafts Werten für die Ereignis Quellen eines Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="51dd4-115">Retrieves the number of indexes of the array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="51dd4-116">**Ecgetsubscribe ptionproperty**</span><span class="sxs-lookup"><span data-stu-id="51dd4-116">**EcGetSubscriptionProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty)
</dt> <dd>

<span data-ttu-id="51dd4-117">Ruft einen Eigenschafts Wert aus einem Abonnement Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="51dd4-117">Retrieves a property value from a subscription object.</span></span>

</dd> <dt>

[<span data-ttu-id="51dd4-118">**Ecgetabonptionruntimestatus**</span><span class="sxs-lookup"><span data-stu-id="51dd4-118">**EcGetSubscriptionRunTimeStatus**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus)
</dt> <dd>

<span data-ttu-id="51dd4-119">Ruft die Lauf Zeit Statusinformationen für eine Ereignis Quelle eines Abonnements oder das Abonnement selbst ab.</span><span class="sxs-lookup"><span data-stu-id="51dd4-119">Retrieves the run time status information for an event source of a subscription or the subscription itself.</span></span>

</dd> <dt>

[<span data-ttu-id="51dd4-120">**Ecinsertobjectarrayelement**</span><span class="sxs-lookup"><span data-stu-id="51dd4-120">**EcInsertObjectArrayElement**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement)
</dt> <dd>

<span data-ttu-id="51dd4-121">Fügt ein leeres-Objekt in ein Array von Eigenschafts Werten für die Ereignis Quellen eines Abonnements ein.</span><span class="sxs-lookup"><span data-stu-id="51dd4-121">Inserts an empty object into an array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="51dd4-122">**Ecopenabonptionenum**</span><span class="sxs-lookup"><span data-stu-id="51dd4-122">**EcOpenSubscriptionEnum**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum)
</dt> <dd>

<span data-ttu-id="51dd4-123">Erstellt einen Abonnement Enumerator zum Auflisten aller registrierten Abonnements auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="51dd4-123">Creates a subscription enumerator to enumerate all registered subscriptions on the local machine.</span></span>

</dd> <dt>

[<span data-ttu-id="51dd4-124">**Ecopenabonnement**</span><span class="sxs-lookup"><span data-stu-id="51dd4-124">**EcOpenSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription)
</dt> <dd>

<span data-ttu-id="51dd4-125">Öffnet ein vorhandenes Abonnement oder erstellt ein neues Abonnement.</span><span class="sxs-lookup"><span data-stu-id="51dd4-125">Opens an existing subscription or creates a new subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="51dd4-126">**Ecsavesub-Abonnement**</span><span class="sxs-lookup"><span data-stu-id="51dd4-126">**EcSaveSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription)
</dt> <dd>

<span data-ttu-id="51dd4-127">Speichert die Konfigurationsinformationen für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="51dd4-127">Saves subscription configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="51dd4-128">**Ectartobjectarrayproperty**</span><span class="sxs-lookup"><span data-stu-id="51dd4-128">**EcSetObjectArrayProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty)
</dt> <dd>

<span data-ttu-id="51dd4-129">Legt einen Eigenschafts Wert in einem Array von Eigenschafts Werten für die Ereignis Quellen eines Abonnements fest.</span><span class="sxs-lookup"><span data-stu-id="51dd4-129">Sets a property value in an array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="51dd4-130">**Ecsetabonptionproperty**</span><span class="sxs-lookup"><span data-stu-id="51dd4-130">**EcSetSubscriptionProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty)
</dt> <dd>

<span data-ttu-id="51dd4-131">Legt neue Werte fest oder aktualisiert vorhandene Werte eines Abonnements.</span><span class="sxs-lookup"><span data-stu-id="51dd4-131">Sets new values or updates existing values of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="51dd4-132">**Ecremoveobjectarrayelement**</span><span class="sxs-lookup"><span data-stu-id="51dd4-132">**EcRemoveObjectArrayElement**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement)
</dt> <dd>

<span data-ttu-id="51dd4-133">Entfernt ein Element aus einem Array von-Objekten, die Eigenschaftswerte für die Ereignis Quellen eines Abonnements enthalten.</span><span class="sxs-lookup"><span data-stu-id="51dd4-133">Removes an element from an array of objects that contain property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="51dd4-134">**Ecretryabonnement**</span><span class="sxs-lookup"><span data-stu-id="51dd4-134">**EcRetrySubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecretrysubscription)
</dt> <dd>

<span data-ttu-id="51dd4-135">Versucht, eine Verbindung mit der Ereignis Quelle eines Abonnements herzustellen, das nicht verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="51dd4-135">Retries connecting to the event source of a subscription that is not connected.</span></span>

</dd> </dl>

 

 




