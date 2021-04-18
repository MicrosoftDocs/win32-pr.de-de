---
description: WMI unterstützt verschiedene Threading Modelle in Abhängigkeit davon, wie der Anbieter gehostet wird, und den Typ der Anbieter Funktionalität, z. b. Klasse oder Eigenschaft.
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: Auswählen der richtigen Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b66ec0266b5482dcff13a7de05a5bd1414312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357808"
---
# <a name="choosing-correct-registration"></a><span data-ttu-id="9390d-103">Auswählen der richtigen Registrierung</span><span class="sxs-lookup"><span data-stu-id="9390d-103">Choosing Correct Registration</span></span>

<span data-ttu-id="9390d-104">WMI unterstützt verschiedene Threading Modelle in Abhängigkeit davon, wie der Anbieter gehostet wird, und den Typ der Anbieter Funktionalität, z. b. [Klasse](writing-a-class-provider.md) oder [Eigenschaft](writing-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9390d-104">WMI supports different threading models depending on how the provider is hosted and the type of provider functionality, such as [Class](writing-a-class-provider.md) or [Property](writing-a-property-provider.md).</span></span> <span data-ttu-id="9390d-105">Beispielsweise unterstützen [*entkoppelte Anbieter*](gloss-d.md) nicht alle Typen von Anbieter Funktionen.</span><span class="sxs-lookup"><span data-stu-id="9390d-105">For example, [*decoupled providers*](gloss-d.md) do not support all the types of provider functionality.</span></span> <span data-ttu-id="9390d-106">Weitere Informationen zu unterschiedlichen Hostingmodellen und deren Konfiguration finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="9390d-106">For more information about different hosting models and how to configure them, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="in-process-providers"></a><span data-ttu-id="9390d-107">In-Process Anbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-107">In-Process Providers</span></span>

<span data-ttu-id="9390d-108">In-Process-Anbieter werden in einem freigegebenen Host Prozess ausgeführt, Wmiprvse.exe.</span><span class="sxs-lookup"><span data-stu-id="9390d-108">In-process providers run in a shared host process, Wmiprvse.exe.</span></span> <span data-ttu-id="9390d-109">Die meisten in-Process-Anbieter Typen verwenden das Multithread-Apartment-Modell (MTA).</span><span class="sxs-lookup"><span data-stu-id="9390d-109">Most in-process provider types use the multithreaded apartment (MTA) model.</span></span>

<span data-ttu-id="9390d-110">Das MTA-Modell wird für die folgenden Typen von Anbieter Funktionen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="9390d-110">The MTA model is supported for the following types of provider functionality:</span></span>

-   [<span data-ttu-id="9390d-111">Klassen Anbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-111">Class Provider</span></span>](writing-a-class-provider.md)
-   [<span data-ttu-id="9390d-112">Instanzanbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-112">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="9390d-113">Methoden Anbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-113">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="9390d-114">Eigenschaften Anbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-114">Property Provider</span></span>](writing-a-property-provider.md)
-   [<span data-ttu-id="9390d-115">Ereignis Anbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-115">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="9390d-116">Ereignisconsumeranbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-116">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

<span data-ttu-id="9390d-117">Das STA-Modell (Single Thread-Apartment) wird für einige Arten von Anbieter Funktionen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="9390d-117">The single-threaded apartment (STA) model is supported for some types of provider functionality:</span></span>

-   [<span data-ttu-id="9390d-118">Instanzanbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-118">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="9390d-119">Methoden Anbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-119">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="9390d-120">Ereignis Anbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-120">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="9390d-121">Ereignisconsumeranbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-121">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a><span data-ttu-id="9390d-122">Out-of-Process-Anbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-122">Out-of-Process Providers</span></span>

<span data-ttu-id="9390d-123">Anbieter, die auf einem anderen gemeinsamen Dienst Host gehostet werden, unterstützen die folgende Anbieter Funktionalität:</span><span class="sxs-lookup"><span data-stu-id="9390d-123">Providers that are hosted in a different shared service host support the following provider functionality:</span></span>

-   [<span data-ttu-id="9390d-124">Klassen Anbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-124">Class Provider</span></span>](writing-a-class-provider.md)
-   [<span data-ttu-id="9390d-125">Instanzanbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-125">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="9390d-126">Methoden Anbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-126">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="9390d-127">Eigenschaften Anbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-127">Property Provider</span></span>](writing-a-property-provider.md)
-   [<span data-ttu-id="9390d-128">Ereignis Anbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-128">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="9390d-129">Ereignisconsumeranbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-129">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

<span data-ttu-id="9390d-130">Weitere Informationen zu Hosts für gemeinsame Dienste finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="9390d-130">For more information about shared service hosts, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="decoupled-providers"></a><span data-ttu-id="9390d-131">Entkoppelte Anbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-131">Decoupled Providers</span></span>

<span data-ttu-id="9390d-132">Entkoppelte Anbieter werden in einer Anwendung gehostet.</span><span class="sxs-lookup"><span data-stu-id="9390d-132">Decoupled providers are hosted in an application.</span></span> <span data-ttu-id="9390d-133">Weitere Informationen finden Sie unter [Einbinden eines Anbieters in eine Anwendung](incorporating-a-provider-in-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="9390d-133">For more information, see [Incorporating a Provider in an Application](incorporating-a-provider-in-an-application.md).</span></span> <span data-ttu-id="9390d-134">Anbieter, die im .NET Framework mithilfe von WMI erstellt wurden, sind entkoppelt.</span><span class="sxs-lookup"><span data-stu-id="9390d-134">Providers created using WMI in the .NET Framework are decoupled.</span></span> <span data-ttu-id="9390d-135">Entkoppelte Anbieter unterstützen die folgende Anbieter Funktionalität:</span><span class="sxs-lookup"><span data-stu-id="9390d-135">Decoupled providers support the following provider functionality:</span></span>

-   [<span data-ttu-id="9390d-136">Instanzanbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-136">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="9390d-137">Methoden Anbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-137">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="9390d-138">Ereignis Anbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-138">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="9390d-139">Ereignisconsumeranbieter</span><span class="sxs-lookup"><span data-stu-id="9390d-139">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a><span data-ttu-id="9390d-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9390d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9390d-141">Entwickeln eines WMI-Anbieters</span><span class="sxs-lookup"><span data-stu-id="9390d-141">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="9390d-142">Anbieter Hosting und-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="9390d-142">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
</dt> </dl>

 

 



