---
description: Enthält ein-Objekt für jedes Abonnement für die Auflistung der übergeordneten Komponenten.
ms.assetid: ec93d500-32bf-4e67-9eda-c1fe0349faa2
title: "\"Abonniert forcomponent\"-Sammlung"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriptionsForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: c8334aa54b56a9dccaa7aa0787d8c997baf0445e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342756"
---
# <a name="subscriptionsforcomponent-collection"></a><span data-ttu-id="129b6-103">"Abonniert forcomponent"-Sammlung</span><span class="sxs-lookup"><span data-stu-id="129b6-103">SubscriptionsForComponent collection</span></span>

<span data-ttu-id="129b6-104">Enthält ein-Objekt für jedes Abonnement für die Auflistung der übergeordneten [**Komponenten**](components.md) .</span><span class="sxs-lookup"><span data-stu-id="129b6-104">Contains an object for each subscription for the parent [**Components**](components.md) collection.</span></span>

<span data-ttu-id="129b6-105">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="129b6-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="129b6-106">Member</span><span class="sxs-lookup"><span data-stu-id="129b6-106">Members</span></span>

<span data-ttu-id="129b6-107">Die " **abonptionsforcomponent** "-Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="129b6-107">The **SubscriptionsForComponent** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="129b6-108">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="129b6-108">Related Collections</span></span>

<span data-ttu-id="129b6-109">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="129b6-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="129b6-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="129b6-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="129b6-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="129b6-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="129b6-112">**Publisherproperties**</span><span class="sxs-lookup"><span data-stu-id="129b6-112">**PublisherProperties**</span></span>](publisherproperties.md)
-   [<span data-ttu-id="129b6-113">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="129b6-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="129b6-114">**Abonnement Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="129b6-114">**SubscriberProperties**</span></span>](subscriberproperties.md)

<span data-ttu-id="129b6-115">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="129b6-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="129b6-116">**Komponenten**</span><span class="sxs-lookup"><span data-stu-id="129b6-116">**Components**</span></span>](components.md)

## <a name="properties"></a><span data-ttu-id="129b6-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="129b6-117">Properties</span></span>

<span data-ttu-id="129b6-118">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="129b6-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="129b6-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="129b6-119">Description</span></span>](#description)
-   [<span data-ttu-id="129b6-120">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="129b6-120">Enabled</span></span>](#enabled)
-   [<span data-ttu-id="129b6-121">Eventclasspartitionid</span><span class="sxs-lookup"><span data-stu-id="129b6-121">EventClassPartitionID</span></span>](#eventclasspartitionid)
-   [<span data-ttu-id="129b6-122">Eventclsid</span><span class="sxs-lookup"><span data-stu-id="129b6-122">EventCLSID</span></span>](#eventclsid)
-   [<span data-ttu-id="129b6-123">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="129b6-123">FilterCriteria</span></span>](#filtercriteria)
-   [<span data-ttu-id="129b6-124">ID</span><span class="sxs-lookup"><span data-stu-id="129b6-124">ID</span></span>](#subscriptionsforcomponent-collection)
-   [<span data-ttu-id="129b6-125">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="129b6-125">InterfaceID</span></span>](#interfaceid)
-   [<span data-ttu-id="129b6-126">MachineName</span><span class="sxs-lookup"><span data-stu-id="129b6-126">MachineName</span></span>](#machinename)
-   [<span data-ttu-id="129b6-127">MethodName</span><span class="sxs-lookup"><span data-stu-id="129b6-127">MethodName</span></span>](#methodname)
-   [<span data-ttu-id="129b6-128">Name</span><span class="sxs-lookup"><span data-stu-id="129b6-128">Name</span></span>](#machinename)
-   [<span data-ttu-id="129b6-129">Peruser</span><span class="sxs-lookup"><span data-stu-id="129b6-129">PerUser</span></span>](#peruser)
-   [<span data-ttu-id="129b6-130">PublisherID</span><span class="sxs-lookup"><span data-stu-id="129b6-130">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="129b6-131">In Warteschlange</span><span class="sxs-lookup"><span data-stu-id="129b6-131">Queued</span></span>](#queued)
-   [<span data-ttu-id="129b6-132">Abonniert</span><span class="sxs-lookup"><span data-stu-id="129b6-132">SubscriberMoniker</span></span>](#subscribermoniker)
-   [<span data-ttu-id="129b6-133">Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="129b6-133">SubscriberPartitionID</span></span>](#subscriberpartitionid)
-   [<span data-ttu-id="129b6-134">UserName</span><span class="sxs-lookup"><span data-stu-id="129b6-134">UserName</span></span>](#username)

### <a name="description"></a><span data-ttu-id="129b6-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="129b6-135">Description</span></span>



| <span data-ttu-id="129b6-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="129b6-136">Entry</span></span> | <span data-ttu-id="129b6-137">Wert</span><span class="sxs-lookup"><span data-stu-id="129b6-137">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="129b6-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="129b6-138">Description</span></span>    | <span data-ttu-id="129b6-139">Eine Beschreibung für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="129b6-139">A description for the subscription.</span></span> |
| <span data-ttu-id="129b6-140">Access</span><span class="sxs-lookup"><span data-stu-id="129b6-140">Access</span></span>         | <span data-ttu-id="129b6-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="129b6-141">ReadWrite</span></span>                           |
| <span data-ttu-id="129b6-142">type</span><span class="sxs-lookup"><span data-stu-id="129b6-142">Type</span></span>           | <span data-ttu-id="129b6-143">String</span><span class="sxs-lookup"><span data-stu-id="129b6-143">String</span></span>                              |
| <span data-ttu-id="129b6-144">Standard</span><span class="sxs-lookup"><span data-stu-id="129b6-144">Default</span></span>        | <span data-ttu-id="129b6-145">""</span><span class="sxs-lookup"><span data-stu-id="129b6-145">""</span></span>                                  |
| <span data-ttu-id="129b6-146">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="129b6-146">Minimum system</span></span> | <span data-ttu-id="129b6-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="129b6-147">Windows 2000</span></span>                        |



 

### <a name="enabled"></a><span data-ttu-id="129b6-148">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="129b6-148">Enabled</span></span>



| <span data-ttu-id="129b6-149">Eingabe</span><span class="sxs-lookup"><span data-stu-id="129b6-149">Entry</span></span> | <span data-ttu-id="129b6-150">Wert</span><span class="sxs-lookup"><span data-stu-id="129b6-150">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="129b6-151">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="129b6-151">Description</span></span>    | <span data-ttu-id="129b6-152">Gibt an, ob das Abonnement derzeit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="129b6-152">Indicates whether the subscription is presently enabled.</span></span> |
| <span data-ttu-id="129b6-153">Access</span><span class="sxs-lookup"><span data-stu-id="129b6-153">Access</span></span>         | <span data-ttu-id="129b6-154">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="129b6-154">ReadWrite</span></span>                                                |
| <span data-ttu-id="129b6-155">type</span><span class="sxs-lookup"><span data-stu-id="129b6-155">Type</span></span>           | <span data-ttu-id="129b6-156">Bool</span><span class="sxs-lookup"><span data-stu-id="129b6-156">Bool</span></span>                                                     |
| <span data-ttu-id="129b6-157">Standard</span><span class="sxs-lookup"><span data-stu-id="129b6-157">Default</span></span>        | <span data-ttu-id="129b6-158">Richtig</span><span class="sxs-lookup"><span data-stu-id="129b6-158">True</span></span>                                                     |
| <span data-ttu-id="129b6-159">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="129b6-159">Minimum system</span></span> | <span data-ttu-id="129b6-160">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="129b6-160">Windows 2000</span></span>                                             |



 

### <a name="eventclasspartitionid"></a><span data-ttu-id="129b6-161">Eventclasspartitionid</span><span class="sxs-lookup"><span data-stu-id="129b6-161">EventClassPartitionID</span></span>



| <span data-ttu-id="129b6-162">Eingabe</span><span class="sxs-lookup"><span data-stu-id="129b6-162">Entry</span></span> | <span data-ttu-id="129b6-163">Wert</span><span class="sxs-lookup"><span data-stu-id="129b6-163">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="129b6-164">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="129b6-164">Description</span></span>    | <span data-ttu-id="129b6-165">Beim Abonnieren einer Ereignisklasse wird verwendet, um die GUID der Partitions-ID darzustellen, die die Ereignisklasse enthält.</span><span class="sxs-lookup"><span data-stu-id="129b6-165">When subscribing to an event class, used to represent the GUID of the partition ID containing the event class.</span></span> <span data-ttu-id="129b6-166">Beim Abonnieren von Ereignis Klassen hat der Abonnent die Möglichkeit, eine Ereignisklasse in derselben oder in einer anderen Partition zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="129b6-166">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="129b6-167">Access</span><span class="sxs-lookup"><span data-stu-id="129b6-167">Access</span></span>         | <span data-ttu-id="129b6-168">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="129b6-168">ReadWrite</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="129b6-169">type</span><span class="sxs-lookup"><span data-stu-id="129b6-169">Type</span></span>           | <span data-ttu-id="129b6-170">String</span><span class="sxs-lookup"><span data-stu-id="129b6-170">String</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="129b6-171">Standard</span><span class="sxs-lookup"><span data-stu-id="129b6-171">Default</span></span>        | <span data-ttu-id="129b6-172">NULL</span><span class="sxs-lookup"><span data-stu-id="129b6-172">NULL</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="129b6-173">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="129b6-173">Minimum system</span></span> | <span data-ttu-id="129b6-174">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="129b6-174">Windows Server 2003</span></span>                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a><span data-ttu-id="129b6-175">Eventclsid</span><span class="sxs-lookup"><span data-stu-id="129b6-175">EventCLSID</span></span>



| <span data-ttu-id="129b6-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="129b6-176">Entry</span></span> | <span data-ttu-id="129b6-177">Wert</span><span class="sxs-lookup"><span data-stu-id="129b6-177">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="129b6-178">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="129b6-178">Description</span></span>    | <span data-ttu-id="129b6-179">Die CLSID für die Ereignisklasse.</span><span class="sxs-lookup"><span data-stu-id="129b6-179">The CLSID for the event class.</span></span> <span data-ttu-id="129b6-180">Sie können angeben, dass es sich um eine eventclsid oder eine PublisherID handelt, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="129b6-180">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="129b6-181">Access</span><span class="sxs-lookup"><span data-stu-id="129b6-181">Access</span></span>         | <span data-ttu-id="129b6-182">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="129b6-182">WriteOnce</span></span>                                                                                    |
| <span data-ttu-id="129b6-183">type</span><span class="sxs-lookup"><span data-stu-id="129b6-183">Type</span></span>           | <span data-ttu-id="129b6-184">String</span><span class="sxs-lookup"><span data-stu-id="129b6-184">String</span></span>                                                                                       |
| <span data-ttu-id="129b6-185">Standard</span><span class="sxs-lookup"><span data-stu-id="129b6-185">Default</span></span>        | <span data-ttu-id="129b6-186">–</span><span class="sxs-lookup"><span data-stu-id="129b6-186">N/A</span></span>                                                                                          |
| <span data-ttu-id="129b6-187">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="129b6-187">Minimum system</span></span> | <span data-ttu-id="129b6-188">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="129b6-188">Windows 2000</span></span>                                                                                 |



 

### <a name="filtercriteria"></a><span data-ttu-id="129b6-189">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="129b6-189">FilterCriteria</span></span>



| <span data-ttu-id="129b6-190">Eingabe</span><span class="sxs-lookup"><span data-stu-id="129b6-190">Entry</span></span> | <span data-ttu-id="129b6-191">Wert</span><span class="sxs-lookup"><span data-stu-id="129b6-191">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="129b6-192">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="129b6-192">Description</span></span>    | <span data-ttu-id="129b6-193">Eine Zeichenfolge, die die Filterkriterien angibt.</span><span class="sxs-lookup"><span data-stu-id="129b6-193">A string indicating the filter criteria.</span></span> <span data-ttu-id="129b6-194">Kann eine CLSID für eine [**publisherfilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) -Klasse sein.</span><span class="sxs-lookup"><span data-stu-id="129b6-194">Can be a CLSID for a [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) class.</span></span> |
| <span data-ttu-id="129b6-195">Access</span><span class="sxs-lookup"><span data-stu-id="129b6-195">Access</span></span>         | <span data-ttu-id="129b6-196">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="129b6-196">ReadWrite</span></span>                                                                                                        |
| <span data-ttu-id="129b6-197">type</span><span class="sxs-lookup"><span data-stu-id="129b6-197">Type</span></span>           | <span data-ttu-id="129b6-198">String</span><span class="sxs-lookup"><span data-stu-id="129b6-198">String</span></span>                                                                                                           |
| <span data-ttu-id="129b6-199">Standard</span><span class="sxs-lookup"><span data-stu-id="129b6-199">Default</span></span>        | <span data-ttu-id="129b6-200">–</span><span class="sxs-lookup"><span data-stu-id="129b6-200">N/A</span></span>                                                                                                              |
| <span data-ttu-id="129b6-201">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="129b6-201">Minimum system</span></span> | <span data-ttu-id="129b6-202">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="129b6-202">Windows 2000</span></span>                                                                                                     |



 

### <a name="id"></a><span data-ttu-id="129b6-203">id</span><span class="sxs-lookup"><span data-stu-id="129b6-203">ID</span></span>



| <span data-ttu-id="129b6-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="129b6-204">Entry</span></span> | <span data-ttu-id="129b6-205">Wert</span><span class="sxs-lookup"><span data-stu-id="129b6-205">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="129b6-206">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="129b6-206">Description</span></span>    | <span data-ttu-id="129b6-207">Der Bezeichner für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="129b6-207">Identifier for the subscription.</span></span> <span data-ttu-id="129b6-208">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="129b6-208">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="129b6-209">Access</span><span class="sxs-lookup"><span data-stu-id="129b6-209">Access</span></span>         | <span data-ttu-id="129b6-210">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="129b6-210">WriteOnce</span></span>                                                                                                                                                        |
| <span data-ttu-id="129b6-211">type</span><span class="sxs-lookup"><span data-stu-id="129b6-211">Type</span></span>           | <span data-ttu-id="129b6-212">String</span><span class="sxs-lookup"><span data-stu-id="129b6-212">String</span></span>                                                                                                                                                           |
| <span data-ttu-id="129b6-213">Standard</span><span class="sxs-lookup"><span data-stu-id="129b6-213">Default</span></span>        | <Generated>                                                                                                                                                |
| <span data-ttu-id="129b6-214">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="129b6-214">Minimum system</span></span> | <span data-ttu-id="129b6-215">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="129b6-215">Windows 2000</span></span>                                                                                                                                                     |



 

### <a name="interfaceid"></a><span data-ttu-id="129b6-216">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="129b6-216">InterfaceID</span></span>



| <span data-ttu-id="129b6-217">Eingabe</span><span class="sxs-lookup"><span data-stu-id="129b6-217">Entry</span></span> | <span data-ttu-id="129b6-218">Wert</span><span class="sxs-lookup"><span data-stu-id="129b6-218">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="129b6-219">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="129b6-219">Description</span></span>    | <span data-ttu-id="129b6-220">Die IID für die Schnittstelle, die abonniert hat.</span><span class="sxs-lookup"><span data-stu-id="129b6-220">The IID for the interface subscribed to.</span></span> |
| <span data-ttu-id="129b6-221">Access</span><span class="sxs-lookup"><span data-stu-id="129b6-221">Access</span></span>         | <span data-ttu-id="129b6-222">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="129b6-222">ReadWrite</span></span>                                |
| <span data-ttu-id="129b6-223">type</span><span class="sxs-lookup"><span data-stu-id="129b6-223">Type</span></span>           | <span data-ttu-id="129b6-224">String</span><span class="sxs-lookup"><span data-stu-id="129b6-224">String</span></span>                                   |
| <span data-ttu-id="129b6-225">Standard</span><span class="sxs-lookup"><span data-stu-id="129b6-225">Default</span></span>        | <span data-ttu-id="129b6-226">–</span><span class="sxs-lookup"><span data-stu-id="129b6-226">N/A</span></span>                                      |
| <span data-ttu-id="129b6-227">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="129b6-227">Minimum system</span></span> | <span data-ttu-id="129b6-228">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="129b6-228">Windows 2000</span></span>                             |



 

### <a name="machinename"></a><span data-ttu-id="129b6-229">MachineName</span><span class="sxs-lookup"><span data-stu-id="129b6-229">MachineName</span></span>



| <span data-ttu-id="129b6-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="129b6-230">Entry</span></span> | <span data-ttu-id="129b6-231">Wert</span><span class="sxs-lookup"><span data-stu-id="129b6-231">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="129b6-232">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="129b6-232">Description</span></span>    | <span data-ttu-id="129b6-233">Einen Remote Computernamen für Abonnements von Ereignis Klassen auf einem Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="129b6-233">A remote computer name for subscriptions to event classes on a remote computer.</span></span> |
| <span data-ttu-id="129b6-234">Access</span><span class="sxs-lookup"><span data-stu-id="129b6-234">Access</span></span>         | <span data-ttu-id="129b6-235">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="129b6-235">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="129b6-236">type</span><span class="sxs-lookup"><span data-stu-id="129b6-236">Type</span></span>           | <span data-ttu-id="129b6-237">String</span><span class="sxs-lookup"><span data-stu-id="129b6-237">String</span></span>                                                                          |
| <span data-ttu-id="129b6-238">Standard</span><span class="sxs-lookup"><span data-stu-id="129b6-238">Default</span></span>        | <span data-ttu-id="129b6-239">""</span><span class="sxs-lookup"><span data-stu-id="129b6-239">""</span></span>                                                                              |
| <span data-ttu-id="129b6-240">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="129b6-240">Minimum system</span></span> | <span data-ttu-id="129b6-241">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="129b6-241">Windows 2000</span></span>                                                                    |



 

### <a name="methodname"></a><span data-ttu-id="129b6-242">MethodName</span><span class="sxs-lookup"><span data-stu-id="129b6-242">MethodName</span></span>



| <span data-ttu-id="129b6-243">Eingabe</span><span class="sxs-lookup"><span data-stu-id="129b6-243">Entry</span></span> | <span data-ttu-id="129b6-244">Wert</span><span class="sxs-lookup"><span data-stu-id="129b6-244">Value</span></span> |
|----------------|----------------------------------------------|
| <span data-ttu-id="129b6-245">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="129b6-245">Description</span></span>    | <span data-ttu-id="129b6-246">Methode für die Schnittstelle, die abonniert wird.</span><span class="sxs-lookup"><span data-stu-id="129b6-246">Method on the interface being subscribed to.</span></span> |
| <span data-ttu-id="129b6-247">Access</span><span class="sxs-lookup"><span data-stu-id="129b6-247">Access</span></span>         | <span data-ttu-id="129b6-248">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="129b6-248">ReadWrite</span></span>                                    |
| <span data-ttu-id="129b6-249">type</span><span class="sxs-lookup"><span data-stu-id="129b6-249">Type</span></span>           | <span data-ttu-id="129b6-250">String</span><span class="sxs-lookup"><span data-stu-id="129b6-250">String</span></span>                                       |
| <span data-ttu-id="129b6-251">Standard</span><span class="sxs-lookup"><span data-stu-id="129b6-251">Default</span></span>        | <span data-ttu-id="129b6-252">–</span><span class="sxs-lookup"><span data-stu-id="129b6-252">N/A</span></span>                                          |
| <span data-ttu-id="129b6-253">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="129b6-253">Minimum system</span></span> | <span data-ttu-id="129b6-254">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="129b6-254">Windows 2000</span></span>                                 |



 

### <a name="name"></a><span data-ttu-id="129b6-255">Name</span><span class="sxs-lookup"><span data-stu-id="129b6-255">Name</span></span>



| <span data-ttu-id="129b6-256">Eingabe</span><span class="sxs-lookup"><span data-stu-id="129b6-256">Entry</span></span> | <span data-ttu-id="129b6-257">Wert</span><span class="sxs-lookup"><span data-stu-id="129b6-257">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="129b6-258">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="129b6-258">Description</span></span>    | <span data-ttu-id="129b6-259">Der Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="129b6-259">Name for the subscription.</span></span> <span data-ttu-id="129b6-260">Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="129b6-260">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="129b6-261">Access</span><span class="sxs-lookup"><span data-stu-id="129b6-261">Access</span></span>         | <span data-ttu-id="129b6-262">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="129b6-262">ReadWrite</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="129b6-263">type</span><span class="sxs-lookup"><span data-stu-id="129b6-263">Type</span></span>           | <span data-ttu-id="129b6-264">String</span><span class="sxs-lookup"><span data-stu-id="129b6-264">String</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="129b6-265">Standard</span><span class="sxs-lookup"><span data-stu-id="129b6-265">Default</span></span>        | <span data-ttu-id="129b6-266">"Neues Abonnement"</span><span class="sxs-lookup"><span data-stu-id="129b6-266">"New Subscription"</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="129b6-267">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="129b6-267">Minimum system</span></span> | <span data-ttu-id="129b6-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="129b6-268">Windows 2000</span></span>                                                                                                                                                                                                                       |



 

### <a name="peruser"></a><span data-ttu-id="129b6-269">Peruser</span><span class="sxs-lookup"><span data-stu-id="129b6-269">PerUser</span></span>



| <span data-ttu-id="129b6-270">Eingabe</span><span class="sxs-lookup"><span data-stu-id="129b6-270">Entry</span></span> | <span data-ttu-id="129b6-271">Wert</span><span class="sxs-lookup"><span data-stu-id="129b6-271">Value</span></span> |
|----------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="129b6-272">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="129b6-272">Description</span></span>    | <span data-ttu-id="129b6-273">Gibt an, ob das Abonnement nur für einen bestimmten Benutzer (username) gilt.</span><span class="sxs-lookup"><span data-stu-id="129b6-273">Indicates whether the subscription applies only for a given user, UserName.</span></span> |
| <span data-ttu-id="129b6-274">Access</span><span class="sxs-lookup"><span data-stu-id="129b6-274">Access</span></span>         | <span data-ttu-id="129b6-275">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="129b6-275">ReadWrite</span></span>                                                                   |
| <span data-ttu-id="129b6-276">type</span><span class="sxs-lookup"><span data-stu-id="129b6-276">Type</span></span>           | <span data-ttu-id="129b6-277">Bool</span><span class="sxs-lookup"><span data-stu-id="129b6-277">Bool</span></span>                                                                        |
| <span data-ttu-id="129b6-278">Standard</span><span class="sxs-lookup"><span data-stu-id="129b6-278">Default</span></span>        | <span data-ttu-id="129b6-279">Falsch</span><span class="sxs-lookup"><span data-stu-id="129b6-279">False</span></span>                                                                       |
| <span data-ttu-id="129b6-280">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="129b6-280">Minimum system</span></span> | <span data-ttu-id="129b6-281">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="129b6-281">Windows 2000</span></span>                                                                |



 

### <a name="publisherid"></a><span data-ttu-id="129b6-282">PublisherID</span><span class="sxs-lookup"><span data-stu-id="129b6-282">PublisherID</span></span>



| <span data-ttu-id="129b6-283">Eingabe</span><span class="sxs-lookup"><span data-stu-id="129b6-283">Entry</span></span> | <span data-ttu-id="129b6-284">Wert</span><span class="sxs-lookup"><span data-stu-id="129b6-284">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="129b6-285">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="129b6-285">Description</span></span>    | <span data-ttu-id="129b6-286">Die ID für den Verleger.</span><span class="sxs-lookup"><span data-stu-id="129b6-286">The ID for the publisher.</span></span> <span data-ttu-id="129b6-287">Sie können angeben, dass es sich um eine eventclsid oder eine PublisherID handelt, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="129b6-287">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="129b6-288">Access</span><span class="sxs-lookup"><span data-stu-id="129b6-288">Access</span></span>         | <span data-ttu-id="129b6-289">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="129b6-289">WriteOnce</span></span>                                                                               |
| <span data-ttu-id="129b6-290">type</span><span class="sxs-lookup"><span data-stu-id="129b6-290">Type</span></span>           | <span data-ttu-id="129b6-291">String</span><span class="sxs-lookup"><span data-stu-id="129b6-291">String</span></span>                                                                                  |
| <span data-ttu-id="129b6-292">Standard</span><span class="sxs-lookup"><span data-stu-id="129b6-292">Default</span></span>        | <span data-ttu-id="129b6-293">""</span><span class="sxs-lookup"><span data-stu-id="129b6-293">""</span></span>                                                                                      |
| <span data-ttu-id="129b6-294">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="129b6-294">Minimum system</span></span> | <span data-ttu-id="129b6-295">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="129b6-295">Windows 2000</span></span>                                                                            |



 

### <a name="queued"></a><span data-ttu-id="129b6-296">In Warteschlange</span><span class="sxs-lookup"><span data-stu-id="129b6-296">Queued</span></span>



| <span data-ttu-id="129b6-297">Eingabe</span><span class="sxs-lookup"><span data-stu-id="129b6-297">Entry</span></span> | <span data-ttu-id="129b6-298">Wert</span><span class="sxs-lookup"><span data-stu-id="129b6-298">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="129b6-299">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="129b6-299">Description</span></span>    | <span data-ttu-id="129b6-300">Gibt an, ob das Abonnement in die Warteschlange gestellt wird</span><span class="sxs-lookup"><span data-stu-id="129b6-300">Indicates whether the subscription is queued.</span></span> |
| <span data-ttu-id="129b6-301">Access</span><span class="sxs-lookup"><span data-stu-id="129b6-301">Access</span></span>         | <span data-ttu-id="129b6-302">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="129b6-302">ReadWrite</span></span>                                     |
| <span data-ttu-id="129b6-303">type</span><span class="sxs-lookup"><span data-stu-id="129b6-303">Type</span></span>           | <span data-ttu-id="129b6-304">Bool</span><span class="sxs-lookup"><span data-stu-id="129b6-304">Bool</span></span>                                          |
| <span data-ttu-id="129b6-305">Standard</span><span class="sxs-lookup"><span data-stu-id="129b6-305">Default</span></span>        | <span data-ttu-id="129b6-306">Falsch</span><span class="sxs-lookup"><span data-stu-id="129b6-306">False</span></span>                                         |
| <span data-ttu-id="129b6-307">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="129b6-307">Minimum system</span></span> | <span data-ttu-id="129b6-308">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="129b6-308">Windows 2000</span></span>                                  |



 

### <a name="subscribermoniker"></a><span data-ttu-id="129b6-309">Abonniert</span><span class="sxs-lookup"><span data-stu-id="129b6-309">SubscriberMoniker</span></span>



| <span data-ttu-id="129b6-310">Eingabe</span><span class="sxs-lookup"><span data-stu-id="129b6-310">Entry</span></span> | <span data-ttu-id="129b6-311">Wert</span><span class="sxs-lookup"><span data-stu-id="129b6-311">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="129b6-312">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="129b6-312">Description</span></span>    | <span data-ttu-id="129b6-313">Ein Moniker für einen Abonnenten, der als in der Warteschlange markiert ist.</span><span class="sxs-lookup"><span data-stu-id="129b6-313">A moniker for a subscriber marked as Queued.</span></span> <span data-ttu-id="129b6-314">Ein Standardwert wird generiert, wenn die Warteschlange anfänglich auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="129b6-314">A default value is generated when Queued is initially set to True.</span></span> |
| <span data-ttu-id="129b6-315">Access</span><span class="sxs-lookup"><span data-stu-id="129b6-315">Access</span></span>         | <span data-ttu-id="129b6-316">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="129b6-316">ReadWrite</span></span>                                                                                                       |
| <span data-ttu-id="129b6-317">type</span><span class="sxs-lookup"><span data-stu-id="129b6-317">Type</span></span>           | <span data-ttu-id="129b6-318">String</span><span class="sxs-lookup"><span data-stu-id="129b6-318">String</span></span>                                                                                                          |
| <span data-ttu-id="129b6-319">Standard</span><span class="sxs-lookup"><span data-stu-id="129b6-319">Default</span></span>        | <span data-ttu-id="129b6-320">–</span><span class="sxs-lookup"><span data-stu-id="129b6-320">N/A</span></span>                                                                                                             |
| <span data-ttu-id="129b6-321">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="129b6-321">Minimum system</span></span> | <span data-ttu-id="129b6-322">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="129b6-322">Windows 2000</span></span>                                                                                                    |



 

### <a name="subscriberpartitionid"></a><span data-ttu-id="129b6-323">Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="129b6-323">SubscriberPartitionID</span></span>



| <span data-ttu-id="129b6-324">Eingabe</span><span class="sxs-lookup"><span data-stu-id="129b6-324">Entry</span></span> | <span data-ttu-id="129b6-325">Wert</span><span class="sxs-lookup"><span data-stu-id="129b6-325">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="129b6-326">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="129b6-326">Description</span></span>    | <span data-ttu-id="129b6-327">Beim Abonnieren einer Ereignisklasse in derselben Partition wird zur Darstellung der GUID der Partitions-ID des Abonnenten verwendet.</span><span class="sxs-lookup"><span data-stu-id="129b6-327">When subscribing to an event class in the same partition, used to represent the GUID of the partition ID of the subscriber.</span></span> <span data-ttu-id="129b6-328">Beim Abonnieren von Ereignis Klassen hat der Abonnent die Möglichkeit, eine Ereignisklasse in derselben oder in einer anderen Partition zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="129b6-328">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="129b6-329">Access</span><span class="sxs-lookup"><span data-stu-id="129b6-329">Access</span></span>         | <span data-ttu-id="129b6-330">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="129b6-330">WriteOnce</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="129b6-331">type</span><span class="sxs-lookup"><span data-stu-id="129b6-331">Type</span></span>           | <span data-ttu-id="129b6-332">String</span><span class="sxs-lookup"><span data-stu-id="129b6-332">String</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="129b6-333">Standard</span><span class="sxs-lookup"><span data-stu-id="129b6-333">Default</span></span>        | <Generated>                                                                                                                                                                                                                                               |
| <span data-ttu-id="129b6-334">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="129b6-334">Minimum system</span></span> | <span data-ttu-id="129b6-335">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="129b6-335">Windows Server 2003</span></span>                                                                                                                                                                                                                                             |



 

### <a name="username"></a><span data-ttu-id="129b6-336">UserName</span><span class="sxs-lookup"><span data-stu-id="129b6-336">UserName</span></span>



| <span data-ttu-id="129b6-337">Eingabe</span><span class="sxs-lookup"><span data-stu-id="129b6-337">Entry</span></span> | <span data-ttu-id="129b6-338">Wert</span><span class="sxs-lookup"><span data-stu-id="129b6-338">Value</span></span> |
|----------------|--------------------------------------------------------------------------|
| <span data-ttu-id="129b6-339">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="129b6-339">Description</span></span>    | <span data-ttu-id="129b6-340">Der Name des Benutzers, für den das Abonnement gilt, wenn "peruser" den Wert "true" hat.</span><span class="sxs-lookup"><span data-stu-id="129b6-340">The name of user that the subscription applies to, when PerUser is True.</span></span> |
| <span data-ttu-id="129b6-341">Access</span><span class="sxs-lookup"><span data-stu-id="129b6-341">Access</span></span>         | <span data-ttu-id="129b6-342">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="129b6-342">ReadWrite</span></span>                                                                |
| <span data-ttu-id="129b6-343">type</span><span class="sxs-lookup"><span data-stu-id="129b6-343">Type</span></span>           | <span data-ttu-id="129b6-344">String</span><span class="sxs-lookup"><span data-stu-id="129b6-344">String</span></span>                                                                   |
| <span data-ttu-id="129b6-345">Standard</span><span class="sxs-lookup"><span data-stu-id="129b6-345">Default</span></span>        | <span data-ttu-id="129b6-346">–</span><span class="sxs-lookup"><span data-stu-id="129b6-346">N/A</span></span>                                                                      |
| <span data-ttu-id="129b6-347">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="129b6-347">Minimum system</span></span> | <span data-ttu-id="129b6-348">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="129b6-348">Windows 2000</span></span>                                                             |



 

## <a name="see-also"></a><span data-ttu-id="129b6-349">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="129b6-349">See also</span></span>

<dl> <dt>

[<span data-ttu-id="129b6-350">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="129b6-350">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
