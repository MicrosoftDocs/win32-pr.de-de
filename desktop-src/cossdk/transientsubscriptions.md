---
description: Enthält ein-Objekt für jedes vorübergehende Abonnement. Vorübergehende Abonnements können dynamisch für das Ausführen von Objektinstanzen erstellt werden, und Sie verschwinden, wenn das Objekt zerstört wird.
ms.assetid: beee291c-e03f-4ee0-b1f2-99dcf113c46e
title: Transientabonnements-Auflistung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriptions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6421cff326f4c33f0c77ae47d00e17c79c971443
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861284"
---
# <a name="transientsubscriptions-collection"></a><span data-ttu-id="5fb7b-104">Transientabonnements-Auflistung</span><span class="sxs-lookup"><span data-stu-id="5fb7b-104">TransientSubscriptions collection</span></span>

<span data-ttu-id="5fb7b-105">Enthält ein-Objekt für jedes vorübergehende Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-105">Contains an object for each transient subscription.</span></span> <span data-ttu-id="5fb7b-106">Vorübergehende Abonnements können dynamisch für das Ausführen von Objektinstanzen erstellt werden, und Sie verschwinden, wenn das Objekt zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-106">Transient subscriptions can be created on the fly for running object instances, and they vanish when the object is destroyed.</span></span>

<span data-ttu-id="5fb7b-107">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="5fb7b-108">Member</span><span class="sxs-lookup"><span data-stu-id="5fb7b-108">Members</span></span>

<span data-ttu-id="5fb7b-109">Die **transientabonnements** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-109">The **TransientSubscriptions** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="5fb7b-110">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="5fb7b-110">Related Collections</span></span>

<span data-ttu-id="5fb7b-111">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="5fb7b-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="5fb7b-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="5fb7b-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="5fb7b-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="5fb7b-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="5fb7b-114">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="5fb7b-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="5fb7b-115">**Transientpublisherproperties**</span><span class="sxs-lookup"><span data-stu-id="5fb7b-115">**TransientPublisherProperties**</span></span>](transientpublisherproperties.md)
-   [<span data-ttu-id="5fb7b-116">**Transientabonberproperties**</span><span class="sxs-lookup"><span data-stu-id="5fb7b-116">**TransientSubscriberProperties**</span></span>](transientsubscriberproperties.md)

<span data-ttu-id="5fb7b-117">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="5fb7b-117">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="5fb7b-118">**Fasst**</span><span class="sxs-lookup"><span data-stu-id="5fb7b-118">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="5fb7b-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5fb7b-119">Properties</span></span>

<span data-ttu-id="5fb7b-120">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="5fb7b-120">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="5fb7b-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5fb7b-121">Description</span></span>](#description)
-   [<span data-ttu-id="5fb7b-122">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="5fb7b-122">Enabled</span></span>](#enabled)
-   [<span data-ttu-id="5fb7b-123">Eventclasspartitionid</span><span class="sxs-lookup"><span data-stu-id="5fb7b-123">EventClassPartitionID</span></span>](#eventclasspartitionid)
-   [<span data-ttu-id="5fb7b-124">Eventclsid</span><span class="sxs-lookup"><span data-stu-id="5fb7b-124">EventCLSID</span></span>](#eventclsid)
-   [<span data-ttu-id="5fb7b-125">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="5fb7b-125">FilterCriteria</span></span>](#filtercriteria)
-   [<span data-ttu-id="5fb7b-126">ID</span><span class="sxs-lookup"><span data-stu-id="5fb7b-126">ID</span></span>](#transientsubscriptions-collection)
-   [<span data-ttu-id="5fb7b-127">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="5fb7b-127">InterfaceID</span></span>](#interfaceid)
-   [<span data-ttu-id="5fb7b-128">MethodName</span><span class="sxs-lookup"><span data-stu-id="5fb7b-128">MethodName</span></span>](#methodname)
-   [<span data-ttu-id="5fb7b-129">Name</span><span class="sxs-lookup"><span data-stu-id="5fb7b-129">Name</span></span>](#methodname)
-   [<span data-ttu-id="5fb7b-130">Peruser</span><span class="sxs-lookup"><span data-stu-id="5fb7b-130">PerUser</span></span>](#peruser)
-   [<span data-ttu-id="5fb7b-131">PublisherID</span><span class="sxs-lookup"><span data-stu-id="5fb7b-131">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="5fb7b-132">Abonnement Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5fb7b-132">SubscriberInterface</span></span>](#subscriberinterface)
-   [<span data-ttu-id="5fb7b-133">Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="5fb7b-133">SubscriberPartitionID</span></span>](#subscriberpartitionid)
-   [<span data-ttu-id="5fb7b-134">UserName</span><span class="sxs-lookup"><span data-stu-id="5fb7b-134">UserName</span></span>](#username)

### <a name="description"></a><span data-ttu-id="5fb7b-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fb7b-135">Description</span></span>



| <span data-ttu-id="5fb7b-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fb7b-136">Entry</span></span> | <span data-ttu-id="5fb7b-137">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb7b-137">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="5fb7b-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fb7b-138">Description</span></span>    | <span data-ttu-id="5fb7b-139">Eine Beschreibung für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-139">A description for the subscription.</span></span> |
| <span data-ttu-id="5fb7b-140">Access</span><span class="sxs-lookup"><span data-stu-id="5fb7b-140">Access</span></span>         | <span data-ttu-id="5fb7b-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5fb7b-141">ReadWrite</span></span>                           |
| <span data-ttu-id="5fb7b-142">type</span><span class="sxs-lookup"><span data-stu-id="5fb7b-142">Type</span></span>           | <span data-ttu-id="5fb7b-143">String</span><span class="sxs-lookup"><span data-stu-id="5fb7b-143">String</span></span>                              |
| <span data-ttu-id="5fb7b-144">Standard</span><span class="sxs-lookup"><span data-stu-id="5fb7b-144">Default</span></span>        | <span data-ttu-id="5fb7b-145">""</span><span class="sxs-lookup"><span data-stu-id="5fb7b-145">""</span></span>                                  |
| <span data-ttu-id="5fb7b-146">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="5fb7b-146">Minimum system</span></span> | <span data-ttu-id="5fb7b-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5fb7b-147">Windows 2000</span></span>                        |



 

### <a name="enabled"></a><span data-ttu-id="5fb7b-148">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="5fb7b-148">Enabled</span></span>



| <span data-ttu-id="5fb7b-149">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fb7b-149">Entry</span></span> | <span data-ttu-id="5fb7b-150">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb7b-150">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="5fb7b-151">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fb7b-151">Description</span></span>    | <span data-ttu-id="5fb7b-152">Gibt an, ob das Abonnement derzeit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-152">Indicates whether the subscription is presently enabled.</span></span> |
| <span data-ttu-id="5fb7b-153">Access</span><span class="sxs-lookup"><span data-stu-id="5fb7b-153">Access</span></span>         | <span data-ttu-id="5fb7b-154">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5fb7b-154">ReadWrite</span></span>                                                |
| <span data-ttu-id="5fb7b-155">type</span><span class="sxs-lookup"><span data-stu-id="5fb7b-155">Type</span></span>           | <span data-ttu-id="5fb7b-156">Bool</span><span class="sxs-lookup"><span data-stu-id="5fb7b-156">Bool</span></span>                                                     |
| <span data-ttu-id="5fb7b-157">Standard</span><span class="sxs-lookup"><span data-stu-id="5fb7b-157">Default</span></span>        | <span data-ttu-id="5fb7b-158">Richtig</span><span class="sxs-lookup"><span data-stu-id="5fb7b-158">True</span></span>                                                     |
| <span data-ttu-id="5fb7b-159">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="5fb7b-159">Minimum system</span></span> | <span data-ttu-id="5fb7b-160">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5fb7b-160">Windows 2000</span></span>                                             |



 

### <a name="eventclasspartitionid"></a><span data-ttu-id="5fb7b-161">Eventclasspartitionid</span><span class="sxs-lookup"><span data-stu-id="5fb7b-161">EventClassPartitionID</span></span>



| <span data-ttu-id="5fb7b-162">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fb7b-162">Entry</span></span> | <span data-ttu-id="5fb7b-163">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb7b-163">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb7b-164">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fb7b-164">Description</span></span>    | <span data-ttu-id="5fb7b-165">Beim Abonnieren einer Ereignisklasse wird verwendet, um die GUID der Partitions-ID darzustellen, die die Ereignisklasse enthält.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-165">When subscribing to an event class, used to represent the GUID of the partition ID containing the event class.</span></span> <span data-ttu-id="5fb7b-166">Beim Abonnieren von Ereignis Klassen hat der Abonnent die Möglichkeit, eine Ereignisklasse in derselben oder in einer anderen Partition zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-166">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="5fb7b-167">Access</span><span class="sxs-lookup"><span data-stu-id="5fb7b-167">Access</span></span>         | <span data-ttu-id="5fb7b-168">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5fb7b-168">ReadWrite</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="5fb7b-169">type</span><span class="sxs-lookup"><span data-stu-id="5fb7b-169">Type</span></span>           | <span data-ttu-id="5fb7b-170">String</span><span class="sxs-lookup"><span data-stu-id="5fb7b-170">String</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="5fb7b-171">Standard</span><span class="sxs-lookup"><span data-stu-id="5fb7b-171">Default</span></span>        | <span data-ttu-id="5fb7b-172">NULL</span><span class="sxs-lookup"><span data-stu-id="5fb7b-172">NULL</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="5fb7b-173">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="5fb7b-173">Minimum system</span></span> | <span data-ttu-id="5fb7b-174">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5fb7b-174">Windows Server 2003</span></span>                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a><span data-ttu-id="5fb7b-175">Eventclsid</span><span class="sxs-lookup"><span data-stu-id="5fb7b-175">EventCLSID</span></span>



| <span data-ttu-id="5fb7b-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fb7b-176">Entry</span></span> | <span data-ttu-id="5fb7b-177">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb7b-177">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb7b-178">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fb7b-178">Description</span></span>    | <span data-ttu-id="5fb7b-179">Die CLSID für die Ereignisklasse.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-179">The CLSID for the event class.</span></span> <span data-ttu-id="5fb7b-180">Sie können angeben, dass es sich um eine eventclsid oder eine PublisherID handelt, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-180">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="5fb7b-181">Access</span><span class="sxs-lookup"><span data-stu-id="5fb7b-181">Access</span></span>         | <span data-ttu-id="5fb7b-182">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="5fb7b-182">WriteOnce</span></span>                                                                                    |
| <span data-ttu-id="5fb7b-183">type</span><span class="sxs-lookup"><span data-stu-id="5fb7b-183">Type</span></span>           | <span data-ttu-id="5fb7b-184">String</span><span class="sxs-lookup"><span data-stu-id="5fb7b-184">String</span></span>                                                                                       |
| <span data-ttu-id="5fb7b-185">Standard</span><span class="sxs-lookup"><span data-stu-id="5fb7b-185">Default</span></span>        | <span data-ttu-id="5fb7b-186">–</span><span class="sxs-lookup"><span data-stu-id="5fb7b-186">N/A</span></span>                                                                                          |
| <span data-ttu-id="5fb7b-187">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="5fb7b-187">Minimum system</span></span> | <span data-ttu-id="5fb7b-188">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5fb7b-188">Windows 2000</span></span>                                                                                 |



 

### <a name="filtercriteria"></a><span data-ttu-id="5fb7b-189">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="5fb7b-189">FilterCriteria</span></span>



| <span data-ttu-id="5fb7b-190">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fb7b-190">Entry</span></span> | <span data-ttu-id="5fb7b-191">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb7b-191">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb7b-192">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fb7b-192">Description</span></span>    | <span data-ttu-id="5fb7b-193">Eine Zeichenfolge, die die Filterkriterien angibt.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-193">A string that indicates the filter criteria.</span></span> <span data-ttu-id="5fb7b-194">Kann eine CLSID für eine [**publisherfilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) -Klasse sein.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-194">Can be a CLSID for a [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) class.</span></span> |
| <span data-ttu-id="5fb7b-195">Access</span><span class="sxs-lookup"><span data-stu-id="5fb7b-195">Access</span></span>         | <span data-ttu-id="5fb7b-196">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5fb7b-196">ReadWrite</span></span>                                                                                                            |
| <span data-ttu-id="5fb7b-197">type</span><span class="sxs-lookup"><span data-stu-id="5fb7b-197">Type</span></span>           | <span data-ttu-id="5fb7b-198">String</span><span class="sxs-lookup"><span data-stu-id="5fb7b-198">String</span></span>                                                                                                               |
| <span data-ttu-id="5fb7b-199">Standard</span><span class="sxs-lookup"><span data-stu-id="5fb7b-199">Default</span></span>        | <span data-ttu-id="5fb7b-200">–</span><span class="sxs-lookup"><span data-stu-id="5fb7b-200">N/A</span></span>                                                                                                                  |
| <span data-ttu-id="5fb7b-201">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="5fb7b-201">Minimum system</span></span> | <span data-ttu-id="5fb7b-202">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5fb7b-202">Windows 2000</span></span>                                                                                                         |



 

### <a name="id"></a><span data-ttu-id="5fb7b-203">id</span><span class="sxs-lookup"><span data-stu-id="5fb7b-203">ID</span></span>



| <span data-ttu-id="5fb7b-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fb7b-204">Entry</span></span> | <span data-ttu-id="5fb7b-205">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb7b-205">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb7b-206">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fb7b-206">Description</span></span>    | <span data-ttu-id="5fb7b-207">Der Bezeichner für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-207">Identifier for the subscription.</span></span> <span data-ttu-id="5fb7b-208">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-208">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="5fb7b-209">Access</span><span class="sxs-lookup"><span data-stu-id="5fb7b-209">Access</span></span>         | <span data-ttu-id="5fb7b-210">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="5fb7b-210">WriteOnce</span></span>                                                                                                                                                        |
| <span data-ttu-id="5fb7b-211">type</span><span class="sxs-lookup"><span data-stu-id="5fb7b-211">Type</span></span>           | <span data-ttu-id="5fb7b-212">String</span><span class="sxs-lookup"><span data-stu-id="5fb7b-212">String</span></span>                                                                                                                                                           |
| <span data-ttu-id="5fb7b-213">Standard</span><span class="sxs-lookup"><span data-stu-id="5fb7b-213">Default</span></span>        | <Generated>                                                                                                                                                |
| <span data-ttu-id="5fb7b-214">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="5fb7b-214">Minimum system</span></span> | <span data-ttu-id="5fb7b-215">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5fb7b-215">Windows 2000</span></span>                                                                                                                                                     |



 

### <a name="interfaceid"></a><span data-ttu-id="5fb7b-216">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="5fb7b-216">InterfaceID</span></span>



| <span data-ttu-id="5fb7b-217">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fb7b-217">Entry</span></span> | <span data-ttu-id="5fb7b-218">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb7b-218">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="5fb7b-219">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fb7b-219">Description</span></span>    | <span data-ttu-id="5fb7b-220">IID für die Schnittstelle, die abonniert hat.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-220">IID for interface subscribed to.</span></span> |
| <span data-ttu-id="5fb7b-221">Access</span><span class="sxs-lookup"><span data-stu-id="5fb7b-221">Access</span></span>         | <span data-ttu-id="5fb7b-222">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="5fb7b-222">WriteOnce</span></span>                        |
| <span data-ttu-id="5fb7b-223">type</span><span class="sxs-lookup"><span data-stu-id="5fb7b-223">Type</span></span>           | <span data-ttu-id="5fb7b-224">String</span><span class="sxs-lookup"><span data-stu-id="5fb7b-224">String</span></span>                           |
| <span data-ttu-id="5fb7b-225">Standard</span><span class="sxs-lookup"><span data-stu-id="5fb7b-225">Default</span></span>        | <span data-ttu-id="5fb7b-226">–</span><span class="sxs-lookup"><span data-stu-id="5fb7b-226">N/A</span></span>                              |
| <span data-ttu-id="5fb7b-227">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="5fb7b-227">Minimum system</span></span> | <span data-ttu-id="5fb7b-228">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5fb7b-228">Windows 2000</span></span>                     |



 

### <a name="methodname"></a><span data-ttu-id="5fb7b-229">MethodName</span><span class="sxs-lookup"><span data-stu-id="5fb7b-229">MethodName</span></span>



| <span data-ttu-id="5fb7b-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fb7b-230">Entry</span></span> | <span data-ttu-id="5fb7b-231">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb7b-231">Value</span></span> |
|----------------|----------------------------------------------|
| <span data-ttu-id="5fb7b-232">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fb7b-232">Description</span></span>    | <span data-ttu-id="5fb7b-233">Methode für die Schnittstelle, die abonniert wird.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-233">Method on the interface being subscribed to.</span></span> |
| <span data-ttu-id="5fb7b-234">Access</span><span class="sxs-lookup"><span data-stu-id="5fb7b-234">Access</span></span>         | <span data-ttu-id="5fb7b-235">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5fb7b-235">ReadWrite</span></span>                                    |
| <span data-ttu-id="5fb7b-236">type</span><span class="sxs-lookup"><span data-stu-id="5fb7b-236">Type</span></span>           | <span data-ttu-id="5fb7b-237">String</span><span class="sxs-lookup"><span data-stu-id="5fb7b-237">String</span></span>                                       |
| <span data-ttu-id="5fb7b-238">Standard</span><span class="sxs-lookup"><span data-stu-id="5fb7b-238">Default</span></span>        | <span data-ttu-id="5fb7b-239">–</span><span class="sxs-lookup"><span data-stu-id="5fb7b-239">N/A</span></span>                                          |
| <span data-ttu-id="5fb7b-240">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="5fb7b-240">Minimum system</span></span> | <span data-ttu-id="5fb7b-241">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5fb7b-241">Windows 2000</span></span>                                 |



 

### <a name="name"></a><span data-ttu-id="5fb7b-242">Name</span><span class="sxs-lookup"><span data-stu-id="5fb7b-242">Name</span></span>



| <span data-ttu-id="5fb7b-243">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fb7b-243">Entry</span></span> | <span data-ttu-id="5fb7b-244">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb7b-244">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb7b-245">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fb7b-245">Description</span></span>    | <span data-ttu-id="5fb7b-246">Der Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-246">The name for the subscription.</span></span> <span data-ttu-id="5fb7b-247">Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-247">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="5fb7b-248">Access</span><span class="sxs-lookup"><span data-stu-id="5fb7b-248">Access</span></span>         | <span data-ttu-id="5fb7b-249">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5fb7b-249">ReadWrite</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="5fb7b-250">type</span><span class="sxs-lookup"><span data-stu-id="5fb7b-250">Type</span></span>           | <span data-ttu-id="5fb7b-251">String</span><span class="sxs-lookup"><span data-stu-id="5fb7b-251">String</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="5fb7b-252">Standard</span><span class="sxs-lookup"><span data-stu-id="5fb7b-252">Default</span></span>        | <span data-ttu-id="5fb7b-253">"Neues Abonnement"</span><span class="sxs-lookup"><span data-stu-id="5fb7b-253">"New Subscription"</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="5fb7b-254">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="5fb7b-254">Minimum system</span></span> | <span data-ttu-id="5fb7b-255">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5fb7b-255">Windows 2000</span></span>                                                                                                                                                                                                                           |



 

### <a name="peruser"></a><span data-ttu-id="5fb7b-256">Peruser</span><span class="sxs-lookup"><span data-stu-id="5fb7b-256">PerUser</span></span>



| <span data-ttu-id="5fb7b-257">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fb7b-257">Entry</span></span> | <span data-ttu-id="5fb7b-258">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb7b-258">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb7b-259">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fb7b-259">Description</span></span>    | <span data-ttu-id="5fb7b-260">Gibt an, ob das Abonnement nur für einen bestimmten Benutzer gilt, der durch die UserName-Eigenschaft dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-260">Indicates whether the subscription applies only for a given user, represented by the UserName property.</span></span> |
| <span data-ttu-id="5fb7b-261">Access</span><span class="sxs-lookup"><span data-stu-id="5fb7b-261">Access</span></span>         | <span data-ttu-id="5fb7b-262">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5fb7b-262">ReadWrite</span></span>                                                                                               |
| <span data-ttu-id="5fb7b-263">type</span><span class="sxs-lookup"><span data-stu-id="5fb7b-263">Type</span></span>           | <span data-ttu-id="5fb7b-264">Bool</span><span class="sxs-lookup"><span data-stu-id="5fb7b-264">Bool</span></span>                                                                                                    |
| <span data-ttu-id="5fb7b-265">Standard</span><span class="sxs-lookup"><span data-stu-id="5fb7b-265">Default</span></span>        | <span data-ttu-id="5fb7b-266">Falsch</span><span class="sxs-lookup"><span data-stu-id="5fb7b-266">False</span></span>                                                                                                   |
| <span data-ttu-id="5fb7b-267">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="5fb7b-267">Minimum system</span></span> | <span data-ttu-id="5fb7b-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5fb7b-268">Windows 2000</span></span>                                                                                            |



 

### <a name="publisherid"></a><span data-ttu-id="5fb7b-269">PublisherID</span><span class="sxs-lookup"><span data-stu-id="5fb7b-269">PublisherID</span></span>



| <span data-ttu-id="5fb7b-270">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fb7b-270">Entry</span></span> | <span data-ttu-id="5fb7b-271">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb7b-271">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb7b-272">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fb7b-272">Description</span></span>    | <span data-ttu-id="5fb7b-273">ID für den Verleger.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-273">ID for the publisher.</span></span> <span data-ttu-id="5fb7b-274">Sie können angeben, dass es sich um eine eventclsid oder eine PublisherID handelt, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-274">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="5fb7b-275">Access</span><span class="sxs-lookup"><span data-stu-id="5fb7b-275">Access</span></span>         | <span data-ttu-id="5fb7b-276">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="5fb7b-276">WriteOnce</span></span>                                                                           |
| <span data-ttu-id="5fb7b-277">type</span><span class="sxs-lookup"><span data-stu-id="5fb7b-277">Type</span></span>           | <span data-ttu-id="5fb7b-278">String</span><span class="sxs-lookup"><span data-stu-id="5fb7b-278">String</span></span>                                                                              |
| <span data-ttu-id="5fb7b-279">Standard</span><span class="sxs-lookup"><span data-stu-id="5fb7b-279">Default</span></span>        | <span data-ttu-id="5fb7b-280">""</span><span class="sxs-lookup"><span data-stu-id="5fb7b-280">""</span></span>                                                                                  |
| <span data-ttu-id="5fb7b-281">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="5fb7b-281">Minimum system</span></span> | <span data-ttu-id="5fb7b-282">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5fb7b-282">Windows 2000</span></span>                                                                        |



 

### <a name="subscriberinterface"></a><span data-ttu-id="5fb7b-283">Abonnement Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5fb7b-283">SubscriberInterface</span></span>



| <span data-ttu-id="5fb7b-284">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fb7b-284">Entry</span></span> | <span data-ttu-id="5fb7b-285">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb7b-285">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="5fb7b-286">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fb7b-286">Description</span></span>    | <span data-ttu-id="5fb7b-287">Ein Zeiger auf die-Schnittstelle des Abonnenten.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-287">A pointer to the subscriber's interface.</span></span> |
| <span data-ttu-id="5fb7b-288">Access</span><span class="sxs-lookup"><span data-stu-id="5fb7b-288">Access</span></span>         | <span data-ttu-id="5fb7b-289">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5fb7b-289">ReadWrite</span></span>                                |
| <span data-ttu-id="5fb7b-290">type</span><span class="sxs-lookup"><span data-stu-id="5fb7b-290">Type</span></span>           | <span data-ttu-id="5fb7b-291">Variant</span><span class="sxs-lookup"><span data-stu-id="5fb7b-291">Variant</span></span>                                  |
| <span data-ttu-id="5fb7b-292">Standard</span><span class="sxs-lookup"><span data-stu-id="5fb7b-292">Default</span></span>        | <span data-ttu-id="5fb7b-293">–</span><span class="sxs-lookup"><span data-stu-id="5fb7b-293">N/A</span></span>                                      |
| <span data-ttu-id="5fb7b-294">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="5fb7b-294">Minimum system</span></span> | <span data-ttu-id="5fb7b-295">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5fb7b-295">Windows 2000</span></span>                             |



 

### <a name="subscriberpartitionid"></a><span data-ttu-id="5fb7b-296">Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="5fb7b-296">SubscriberPartitionID</span></span>



| <span data-ttu-id="5fb7b-297">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fb7b-297">Entry</span></span> | <span data-ttu-id="5fb7b-298">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb7b-298">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb7b-299">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fb7b-299">Description</span></span>    | <span data-ttu-id="5fb7b-300">Beim Abonnieren einer Ereignisklasse in derselben Partition wird zur Darstellung der GUID der Partitions-ID des Abonnenten verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-300">When subscribing to an event class in the same partition, used to represent the GUID of the partition ID of the subscriber.</span></span> <span data-ttu-id="5fb7b-301">Beim Abonnieren von Ereignis Klassen hat der Abonnent die Möglichkeit, eine Ereignisklasse in derselben oder in einer anderen Partition zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-301">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="5fb7b-302">Access</span><span class="sxs-lookup"><span data-stu-id="5fb7b-302">Access</span></span>         | <span data-ttu-id="5fb7b-303">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="5fb7b-303">WriteOnce</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="5fb7b-304">type</span><span class="sxs-lookup"><span data-stu-id="5fb7b-304">Type</span></span>           | <span data-ttu-id="5fb7b-305">String</span><span class="sxs-lookup"><span data-stu-id="5fb7b-305">String</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="5fb7b-306">Standard</span><span class="sxs-lookup"><span data-stu-id="5fb7b-306">Default</span></span>        | <Generated>                                                                                                                                                                                                                                               |
| <span data-ttu-id="5fb7b-307">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="5fb7b-307">Minimum system</span></span> | <span data-ttu-id="5fb7b-308">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5fb7b-308">Windows Server 2003</span></span>                                                                                                                                                                                                                                             |



 

### <a name="username"></a><span data-ttu-id="5fb7b-309">UserName</span><span class="sxs-lookup"><span data-stu-id="5fb7b-309">UserName</span></span>



| <span data-ttu-id="5fb7b-310">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fb7b-310">Entry</span></span> | <span data-ttu-id="5fb7b-311">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb7b-311">Value</span></span> |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="5fb7b-312">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fb7b-312">Description</span></span>    | <span data-ttu-id="5fb7b-313">Der Name des Benutzers, für den das Abonnement gilt, wenn peruser den Wert true hat.</span><span class="sxs-lookup"><span data-stu-id="5fb7b-313">The name of user that the subscription applies to when PerUser is True.</span></span> |
| <span data-ttu-id="5fb7b-314">Access</span><span class="sxs-lookup"><span data-stu-id="5fb7b-314">Access</span></span>         | <span data-ttu-id="5fb7b-315">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5fb7b-315">ReadWrite</span></span>                                                               |
| <span data-ttu-id="5fb7b-316">type</span><span class="sxs-lookup"><span data-stu-id="5fb7b-316">Type</span></span>           | <span data-ttu-id="5fb7b-317">String</span><span class="sxs-lookup"><span data-stu-id="5fb7b-317">String</span></span>                                                                  |
| <span data-ttu-id="5fb7b-318">Standard</span><span class="sxs-lookup"><span data-stu-id="5fb7b-318">Default</span></span>        | <span data-ttu-id="5fb7b-319">–</span><span class="sxs-lookup"><span data-stu-id="5fb7b-319">N/A</span></span>                                                                     |
| <span data-ttu-id="5fb7b-320">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="5fb7b-320">Minimum system</span></span> | <span data-ttu-id="5fb7b-321">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5fb7b-321">Windows 2000</span></span>                                                            |



 

## <a name="see-also"></a><span data-ttu-id="5fb7b-322">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fb7b-322">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fb7b-323">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="5fb7b-323">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
