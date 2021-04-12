---
description: Ruft Informationen zu laufenden Anwendungen ab.
ms.assetid: 148e42aa-e99e-4fa2-8b74-a7ebf82b99d0
title: ApplicationInstance-Auflistung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationInstances
api_type:
- COM
api_location: ''
ms.openlocfilehash: 56680a81cc564466dc3586bf0381cf4db97f914b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483163"
---
# <a name="applicationinstances-collection"></a><span data-ttu-id="6b7ef-103">ApplicationInstance-Auflistung</span><span class="sxs-lookup"><span data-stu-id="6b7ef-103">ApplicationInstances collection</span></span>

<span data-ttu-id="6b7ef-104">Ruft Informationen zu laufenden Anwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="6b7ef-104">Retrieves information regarding running applications.</span></span>

<span data-ttu-id="6b7ef-105">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="6b7ef-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="6b7ef-106">Member</span><span class="sxs-lookup"><span data-stu-id="6b7ef-106">Members</span></span>

<span data-ttu-id="6b7ef-107">Die **ApplicationInstance** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="6b7ef-107">The **ApplicationInstances** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="6b7ef-108">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="6b7ef-108">Related Collections</span></span>

<span data-ttu-id="6b7ef-109">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="6b7ef-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="6b7ef-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="6b7ef-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="6b7ef-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="6b7ef-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="6b7ef-112">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="6b7ef-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="6b7ef-113">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="6b7ef-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="6b7ef-114">**Anwendungen**</span><span class="sxs-lookup"><span data-stu-id="6b7ef-114">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="6b7ef-115">**Fasst**</span><span class="sxs-lookup"><span data-stu-id="6b7ef-115">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="6b7ef-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b7ef-116">Properties</span></span>

<span data-ttu-id="6b7ef-117">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="6b7ef-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="6b7ef-118">Anwendung</span><span class="sxs-lookup"><span data-stu-id="6b7ef-118">Application</span></span>](#applicationinstances-collection)
-   [<span data-ttu-id="6b7ef-119">Hasrecycelt</span><span class="sxs-lookup"><span data-stu-id="6b7ef-119">HasRecycled</span></span>](#hasrecycled)
-   [<span data-ttu-id="6b7ef-120">InstanceID</span><span class="sxs-lookup"><span data-stu-id="6b7ef-120">InstanceID</span></span>](#instanceid)
-   [<span data-ttu-id="6b7ef-121">IsPaused</span><span class="sxs-lookup"><span data-stu-id="6b7ef-121">IsPaused</span></span>](#ispaused)
-   [<span data-ttu-id="6b7ef-122">PartitionID</span><span class="sxs-lookup"><span data-stu-id="6b7ef-122">PartitionID</span></span>](#partitionid)
-   [<span data-ttu-id="6b7ef-123">ProcessID</span><span class="sxs-lookup"><span data-stu-id="6b7ef-123">ProcessID</span></span>](#processid)

### <a name="application"></a><span data-ttu-id="6b7ef-124">Application</span><span class="sxs-lookup"><span data-stu-id="6b7ef-124">Application</span></span>



| <span data-ttu-id="6b7ef-125">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6b7ef-125">Entry</span></span> | <span data-ttu-id="6b7ef-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6b7ef-126">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="6b7ef-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b7ef-127">Description</span></span>    | <span data-ttu-id="6b7ef-128">Die ID für die laufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6b7ef-128">The ID for the running application.</span></span> |
| <span data-ttu-id="6b7ef-129">Access</span><span class="sxs-lookup"><span data-stu-id="6b7ef-129">Access</span></span>         | <span data-ttu-id="6b7ef-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6b7ef-130">ReadOnly</span></span>                            |
| <span data-ttu-id="6b7ef-131">type</span><span class="sxs-lookup"><span data-stu-id="6b7ef-131">Type</span></span>           | <span data-ttu-id="6b7ef-132">String</span><span class="sxs-lookup"><span data-stu-id="6b7ef-132">String</span></span>                              |
| <span data-ttu-id="6b7ef-133">Standard</span><span class="sxs-lookup"><span data-stu-id="6b7ef-133">Default</span></span>        | <span data-ttu-id="6b7ef-134">–</span><span class="sxs-lookup"><span data-stu-id="6b7ef-134">N/A</span></span>                                 |
| <span data-ttu-id="6b7ef-135">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="6b7ef-135">Minimum system</span></span> | <span data-ttu-id="6b7ef-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6b7ef-136">Windows XP</span></span>                          |



 

### <a name="hasrecycled"></a><span data-ttu-id="6b7ef-137">Hasrecycelt</span><span class="sxs-lookup"><span data-stu-id="6b7ef-137">HasRecycled</span></span>



| <span data-ttu-id="6b7ef-138">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6b7ef-138">Entry</span></span> | <span data-ttu-id="6b7ef-139">Wert</span><span class="sxs-lookup"><span data-stu-id="6b7ef-139">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="6b7ef-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b7ef-140">Description</span></span>    | <span data-ttu-id="6b7ef-141">Gibt an, ob die Anwendungs Instanz wieder verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6b7ef-141">Indicates whether the application instance has been recycled.</span></span> |
| <span data-ttu-id="6b7ef-142">Access</span><span class="sxs-lookup"><span data-stu-id="6b7ef-142">Access</span></span>         | <span data-ttu-id="6b7ef-143">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6b7ef-143">ReadOnly</span></span>                                                      |
| <span data-ttu-id="6b7ef-144">type</span><span class="sxs-lookup"><span data-stu-id="6b7ef-144">Type</span></span>           | <span data-ttu-id="6b7ef-145">Bool</span><span class="sxs-lookup"><span data-stu-id="6b7ef-145">Bool</span></span>                                                          |
| <span data-ttu-id="6b7ef-146">Standard</span><span class="sxs-lookup"><span data-stu-id="6b7ef-146">Default</span></span>        | <span data-ttu-id="6b7ef-147">Falsch</span><span class="sxs-lookup"><span data-stu-id="6b7ef-147">False</span></span>                                                         |
| <span data-ttu-id="6b7ef-148">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="6b7ef-148">Minimum system</span></span> | <span data-ttu-id="6b7ef-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6b7ef-149">Windows XP</span></span>                                                    |



 

### <a name="instanceid"></a><span data-ttu-id="6b7ef-150">InstanceID</span><span class="sxs-lookup"><span data-stu-id="6b7ef-150">InstanceID</span></span>



| <span data-ttu-id="6b7ef-151">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6b7ef-151">Entry</span></span> | <span data-ttu-id="6b7ef-152">Wert</span><span class="sxs-lookup"><span data-stu-id="6b7ef-152">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b7ef-153">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b7ef-153">Description</span></span>    | <span data-ttu-id="6b7ef-154">Der Globally Unique Identifier für die Anwendungs Instanz.</span><span class="sxs-lookup"><span data-stu-id="6b7ef-154">The globally unique identifier for the application instance.</span></span> <span data-ttu-id="6b7ef-155">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6b7ef-155">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="6b7ef-156">Access</span><span class="sxs-lookup"><span data-stu-id="6b7ef-156">Access</span></span>         | <span data-ttu-id="6b7ef-157">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6b7ef-157">ReadOnly</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="6b7ef-158">type</span><span class="sxs-lookup"><span data-stu-id="6b7ef-158">Type</span></span>           | <span data-ttu-id="6b7ef-159">String</span><span class="sxs-lookup"><span data-stu-id="6b7ef-159">String</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="6b7ef-160">Standard</span><span class="sxs-lookup"><span data-stu-id="6b7ef-160">Default</span></span>        | <span data-ttu-id="6b7ef-161">–</span><span class="sxs-lookup"><span data-stu-id="6b7ef-161">N/A</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="6b7ef-162">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="6b7ef-162">Minimum system</span></span> | <span data-ttu-id="6b7ef-163">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6b7ef-163">Windows XP</span></span>                                                                                                                                                                                                                          |



 

### <a name="ispaused"></a><span data-ttu-id="6b7ef-164">IsPaused</span><span class="sxs-lookup"><span data-stu-id="6b7ef-164">IsPaused</span></span>



| <span data-ttu-id="6b7ef-165">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6b7ef-165">Entry</span></span> | <span data-ttu-id="6b7ef-166">Wert</span><span class="sxs-lookup"><span data-stu-id="6b7ef-166">Value</span></span> |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="6b7ef-167">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b7ef-167">Description</span></span>    | <span data-ttu-id="6b7ef-168">Gibt an, ob die Anwendungs Instanz zurzeit angehalten ist.</span><span class="sxs-lookup"><span data-stu-id="6b7ef-168">Indicates whether the application instance is currently paused.</span></span> |
| <span data-ttu-id="6b7ef-169">Access</span><span class="sxs-lookup"><span data-stu-id="6b7ef-169">Access</span></span>         | <span data-ttu-id="6b7ef-170">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6b7ef-170">ReadOnly</span></span>                                                        |
| <span data-ttu-id="6b7ef-171">type</span><span class="sxs-lookup"><span data-stu-id="6b7ef-171">Type</span></span>           | <span data-ttu-id="6b7ef-172">Bool</span><span class="sxs-lookup"><span data-stu-id="6b7ef-172">Bool</span></span>                                                            |
| <span data-ttu-id="6b7ef-173">Standard</span><span class="sxs-lookup"><span data-stu-id="6b7ef-173">Default</span></span>        | <span data-ttu-id="6b7ef-174">Falsch</span><span class="sxs-lookup"><span data-stu-id="6b7ef-174">False</span></span>                                                           |
| <span data-ttu-id="6b7ef-175">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="6b7ef-175">Minimum system</span></span> | <span data-ttu-id="6b7ef-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6b7ef-176">Windows XP</span></span>                                                      |



 

### <a name="partitionid"></a><span data-ttu-id="6b7ef-177">PartitionID</span><span class="sxs-lookup"><span data-stu-id="6b7ef-177">PartitionID</span></span>



| <span data-ttu-id="6b7ef-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6b7ef-178">Entry</span></span> | <span data-ttu-id="6b7ef-179">Wert</span><span class="sxs-lookup"><span data-stu-id="6b7ef-179">Value</span></span> |
|----------------|-------------------------------------------------|
| <span data-ttu-id="6b7ef-180">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b7ef-180">Description</span></span>    | <span data-ttu-id="6b7ef-181">Die Partitions-ID, die von der Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b7ef-181">The partition ID that the application is using.</span></span> |
| <span data-ttu-id="6b7ef-182">Access</span><span class="sxs-lookup"><span data-stu-id="6b7ef-182">Access</span></span>         | <span data-ttu-id="6b7ef-183">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6b7ef-183">ReadOnly</span></span>                                        |
| <span data-ttu-id="6b7ef-184">type</span><span class="sxs-lookup"><span data-stu-id="6b7ef-184">Type</span></span>           | <span data-ttu-id="6b7ef-185">String</span><span class="sxs-lookup"><span data-stu-id="6b7ef-185">String</span></span>                                          |
| <span data-ttu-id="6b7ef-186">Standard</span><span class="sxs-lookup"><span data-stu-id="6b7ef-186">Default</span></span>        | <span data-ttu-id="6b7ef-187">–</span><span class="sxs-lookup"><span data-stu-id="6b7ef-187">N/A</span></span>                                             |
| <span data-ttu-id="6b7ef-188">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="6b7ef-188">Minimum system</span></span> | <span data-ttu-id="6b7ef-189">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6b7ef-189">Windows XP</span></span>                                      |



 

### <a name="processid"></a><span data-ttu-id="6b7ef-190">ProcessID</span><span class="sxs-lookup"><span data-stu-id="6b7ef-190">ProcessID</span></span>



| <span data-ttu-id="6b7ef-191">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6b7ef-191">Entry</span></span> | <span data-ttu-id="6b7ef-192">Wert</span><span class="sxs-lookup"><span data-stu-id="6b7ef-192">Value</span></span> |
|----------------|---------------------------------------------|
| <span data-ttu-id="6b7ef-193">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b7ef-193">Description</span></span>    | <span data-ttu-id="6b7ef-194">Die Prozess-ID der Anwendungs Instanz.</span><span class="sxs-lookup"><span data-stu-id="6b7ef-194">The process ID of the application instance.</span></span> |
| <span data-ttu-id="6b7ef-195">Access</span><span class="sxs-lookup"><span data-stu-id="6b7ef-195">Access</span></span>         | <span data-ttu-id="6b7ef-196">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6b7ef-196">ReadOnly</span></span>                                    |
| <span data-ttu-id="6b7ef-197">type</span><span class="sxs-lookup"><span data-stu-id="6b7ef-197">Type</span></span>           | <span data-ttu-id="6b7ef-198">String</span><span class="sxs-lookup"><span data-stu-id="6b7ef-198">String</span></span>                                      |
| <span data-ttu-id="6b7ef-199">Standard</span><span class="sxs-lookup"><span data-stu-id="6b7ef-199">Default</span></span>        | <span data-ttu-id="6b7ef-200">–</span><span class="sxs-lookup"><span data-stu-id="6b7ef-200">N/A</span></span>                                         |
| <span data-ttu-id="6b7ef-201">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="6b7ef-201">Minimum system</span></span> | <span data-ttu-id="6b7ef-202">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6b7ef-202">Windows XP</span></span>                                  |



 

## <a name="see-also"></a><span data-ttu-id="6b7ef-203">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b7ef-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b7ef-204">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="6b7ef-204">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
