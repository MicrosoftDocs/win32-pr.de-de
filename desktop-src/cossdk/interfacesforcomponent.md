---
description: Enthält ein-Objekt für jede Schnittstelle, die von der Komponente verfügbar gemacht wird, mit der die Auflistung verknüpft ist.
ms.assetid: ee755693-e3ff-4bb1-9fde-a2bfee9c3d29
title: Interfakesforcomponent-Auflistung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InterfacesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9450c898e694e5459dbb126d7f7bf11b853e33d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127025"
---
# <a name="interfacesforcomponent-collection"></a><span data-ttu-id="d2db2-103">Interfakesforcomponent-Auflistung</span><span class="sxs-lookup"><span data-stu-id="d2db2-103">InterfacesForComponent collection</span></span>

<span data-ttu-id="d2db2-104">Enthält ein-Objekt für jede Schnittstelle, die von der Komponente verfügbar gemacht wird, mit der die Auflistung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="d2db2-104">Contains an object for each interface exposed by the component to which the collection is related.</span></span>

<span data-ttu-id="d2db2-105">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts nicht.</span><span class="sxs-lookup"><span data-stu-id="d2db2-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="d2db2-106">Member</span><span class="sxs-lookup"><span data-stu-id="d2db2-106">Members</span></span>

<span data-ttu-id="d2db2-107">Die **interfakesforcomponent** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="d2db2-107">The **InterfacesForComponent** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="d2db2-108">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="d2db2-108">Related Collections</span></span>

<span data-ttu-id="d2db2-109">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="d2db2-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="d2db2-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="d2db2-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="d2db2-111">**Methodsforinterface**</span><span class="sxs-lookup"><span data-stu-id="d2db2-111">**MethodsForInterface**</span></span>](methodsforinterface.md)
-   [<span data-ttu-id="d2db2-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="d2db2-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="d2db2-113">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="d2db2-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="d2db2-114">**Rolesforinterface**</span><span class="sxs-lookup"><span data-stu-id="d2db2-114">**RolesForInterface**</span></span>](rolesforinterface.md)

<span data-ttu-id="d2db2-115">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="d2db2-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="d2db2-116">**Komponenten**</span><span class="sxs-lookup"><span data-stu-id="d2db2-116">**Components**</span></span>](components.md)

## <a name="properties"></a><span data-ttu-id="d2db2-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d2db2-117">Properties</span></span>

<span data-ttu-id="d2db2-118">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d2db2-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="d2db2-119">CLSID</span><span class="sxs-lookup"><span data-stu-id="d2db2-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="d2db2-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2db2-120">Description</span></span>](#description)
-   [<span data-ttu-id="d2db2-121">IID</span><span class="sxs-lookup"><span data-stu-id="d2db2-121">IID</span></span>](#iid)
-   [<span data-ttu-id="d2db2-122">Name</span><span class="sxs-lookup"><span data-stu-id="d2db2-122">Name</span></span>](#name)
-   [<span data-ttu-id="d2db2-123">Queuingenabled</span><span class="sxs-lookup"><span data-stu-id="d2db2-123">QueuingEnabled</span></span>](#queuingenabled)
-   [<span data-ttu-id="d2db2-124">Queueingsupported</span><span class="sxs-lookup"><span data-stu-id="d2db2-124">QueueingSupported</span></span>](#queueingsupported)

### <a name="clsid"></a><span data-ttu-id="d2db2-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="d2db2-125">CLSID</span></span>



| <span data-ttu-id="d2db2-126">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2db2-126">Entry</span></span> | <span data-ttu-id="d2db2-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d2db2-127">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="d2db2-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2db2-128">Description</span></span>    | <span data-ttu-id="d2db2-129">Eine GUID für die Komponente.</span><span class="sxs-lookup"><span data-stu-id="d2db2-129">A GUID for the component.</span></span> |
| <span data-ttu-id="d2db2-130">Access</span><span class="sxs-lookup"><span data-stu-id="d2db2-130">Access</span></span>         | <span data-ttu-id="d2db2-131">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="d2db2-131">ReadOnly</span></span>                  |
| <span data-ttu-id="d2db2-132">type</span><span class="sxs-lookup"><span data-stu-id="d2db2-132">Type</span></span>           | <span data-ttu-id="d2db2-133">String</span><span class="sxs-lookup"><span data-stu-id="d2db2-133">String</span></span>                    |
| <span data-ttu-id="d2db2-134">Standard</span><span class="sxs-lookup"><span data-stu-id="d2db2-134">Default</span></span>        | <span data-ttu-id="d2db2-135">–</span><span class="sxs-lookup"><span data-stu-id="d2db2-135">N/A</span></span>                       |
| <span data-ttu-id="d2db2-136">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="d2db2-136">Minimum system</span></span> | <span data-ttu-id="d2db2-137">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d2db2-137">Windows 2000</span></span>              |



 

### <a name="description"></a><span data-ttu-id="d2db2-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2db2-138">Description</span></span>



| <span data-ttu-id="d2db2-139">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2db2-139">Entry</span></span> | <span data-ttu-id="d2db2-140">Wert</span><span class="sxs-lookup"><span data-stu-id="d2db2-140">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="d2db2-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2db2-141">Description</span></span>    | <span data-ttu-id="d2db2-142">Eine Beschreibung für die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d2db2-142">A description for the interface.</span></span> |
| <span data-ttu-id="d2db2-143">Access</span><span class="sxs-lookup"><span data-stu-id="d2db2-143">Access</span></span>         | <span data-ttu-id="d2db2-144">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2db2-144">ReadWrite</span></span>                        |
| <span data-ttu-id="d2db2-145">type</span><span class="sxs-lookup"><span data-stu-id="d2db2-145">Type</span></span>           | <span data-ttu-id="d2db2-146">String</span><span class="sxs-lookup"><span data-stu-id="d2db2-146">String</span></span>                           |
| <span data-ttu-id="d2db2-147">Standard</span><span class="sxs-lookup"><span data-stu-id="d2db2-147">Default</span></span>        | <span data-ttu-id="d2db2-148">""</span><span class="sxs-lookup"><span data-stu-id="d2db2-148">""</span></span>                               |
| <span data-ttu-id="d2db2-149">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="d2db2-149">Minimum system</span></span> | <span data-ttu-id="d2db2-150">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d2db2-150">Windows 2000</span></span>                     |



 

### <a name="iid"></a><span data-ttu-id="d2db2-151">IID</span><span class="sxs-lookup"><span data-stu-id="d2db2-151">IID</span></span>



| <span data-ttu-id="d2db2-152">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2db2-152">Entry</span></span> | <span data-ttu-id="d2db2-153">Wert</span><span class="sxs-lookup"><span data-stu-id="d2db2-153">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2db2-154">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2db2-154">Description</span></span>    | <span data-ttu-id="d2db2-155">Eine GUID für die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d2db2-155">A GUID for the interface.</span></span> <span data-ttu-id="d2db2-156">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d2db2-156">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="d2db2-157">Access</span><span class="sxs-lookup"><span data-stu-id="d2db2-157">Access</span></span>         | <span data-ttu-id="d2db2-158">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="d2db2-158">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="d2db2-159">type</span><span class="sxs-lookup"><span data-stu-id="d2db2-159">Type</span></span>           | <span data-ttu-id="d2db2-160">String</span><span class="sxs-lookup"><span data-stu-id="d2db2-160">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="d2db2-161">Standard</span><span class="sxs-lookup"><span data-stu-id="d2db2-161">Default</span></span>        | <span data-ttu-id="d2db2-162">–</span><span class="sxs-lookup"><span data-stu-id="d2db2-162">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="d2db2-163">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="d2db2-163">Minimum system</span></span> | <span data-ttu-id="d2db2-164">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d2db2-164">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="name"></a><span data-ttu-id="d2db2-165">Name</span><span class="sxs-lookup"><span data-stu-id="d2db2-165">Name</span></span>



| <span data-ttu-id="d2db2-166">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2db2-166">Entry</span></span> | <span data-ttu-id="d2db2-167">Wert</span><span class="sxs-lookup"><span data-stu-id="d2db2-167">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2db2-168">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2db2-168">Description</span></span>    | <span data-ttu-id="d2db2-169">Ein Name für die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d2db2-169">A name for the interface.</span></span> <span data-ttu-id="d2db2-170">Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d2db2-170">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="d2db2-171">Access</span><span class="sxs-lookup"><span data-stu-id="d2db2-171">Access</span></span>         | <span data-ttu-id="d2db2-172">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="d2db2-172">ReadOnly</span></span>                                                                                                                                                    |
| <span data-ttu-id="d2db2-173">type</span><span class="sxs-lookup"><span data-stu-id="d2db2-173">Type</span></span>           | <span data-ttu-id="d2db2-174">String</span><span class="sxs-lookup"><span data-stu-id="d2db2-174">String</span></span>                                                                                                                                                      |
| <span data-ttu-id="d2db2-175">Standard</span><span class="sxs-lookup"><span data-stu-id="d2db2-175">Default</span></span>        | <span data-ttu-id="d2db2-176">–</span><span class="sxs-lookup"><span data-stu-id="d2db2-176">N/A</span></span>                                                                                                                                                         |
| <span data-ttu-id="d2db2-177">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="d2db2-177">Minimum system</span></span> | <span data-ttu-id="d2db2-178">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d2db2-178">Windows 2000</span></span>                                                                                                                                                |



 

### <a name="queuingenabled"></a><span data-ttu-id="d2db2-179">Queuingenabled</span><span class="sxs-lookup"><span data-stu-id="d2db2-179">QueuingEnabled</span></span>



| <span data-ttu-id="d2db2-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2db2-180">Entry</span></span> | <span data-ttu-id="d2db2-181">Wert</span><span class="sxs-lookup"><span data-stu-id="d2db2-181">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2db2-182">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2db2-182">Description</span></span>    | <span data-ttu-id="d2db2-183">Markiert die Schnittstelle als Warteschlange und kann mithilfe des Verwaltungs Tools admin SDK oder Komponenten Dienste festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d2db2-183">Marks the interface as queuable and can be set by using the Admin SDK or Component Services administrative tool.</span></span> <span data-ttu-id="d2db2-184">Allerdings kann für nur eine Schnittstelle, für die das in der **Warteschlange** stehende Flag festgelegt ist, das **queuingaktivierte** Flag festgelegt</span><span class="sxs-lookup"><span data-stu-id="d2db2-184">However, only an interface that has the **Queuing Supported** flag set can have the **Queuing Enabled** flag set.</span></span> |
| <span data-ttu-id="d2db2-185">Access</span><span class="sxs-lookup"><span data-stu-id="d2db2-185">Access</span></span>         | <span data-ttu-id="d2db2-186">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2db2-186">ReadWrite</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="d2db2-187">type</span><span class="sxs-lookup"><span data-stu-id="d2db2-187">Type</span></span>           | <span data-ttu-id="d2db2-188">Bool</span><span class="sxs-lookup"><span data-stu-id="d2db2-188">Bool</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="d2db2-189">Standard</span><span class="sxs-lookup"><span data-stu-id="d2db2-189">Default</span></span>        | <span data-ttu-id="d2db2-190">Falsch</span><span class="sxs-lookup"><span data-stu-id="d2db2-190">False</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="d2db2-191">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="d2db2-191">Minimum system</span></span> | <span data-ttu-id="d2db2-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d2db2-192">Windows 2000</span></span>                                                                                                                                                                                                                       |



 

### <a name="queueingsupported"></a><span data-ttu-id="d2db2-193">Queueingsupported</span><span class="sxs-lookup"><span data-stu-id="d2db2-193">QueueingSupported</span></span>



| <span data-ttu-id="d2db2-194">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2db2-194">Entry</span></span> | <span data-ttu-id="d2db2-195">Wert</span><span class="sxs-lookup"><span data-stu-id="d2db2-195">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2db2-196">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2db2-196">Description</span></span>    | <span data-ttu-id="d2db2-197">Schnittstelle unterstützt Warteschlangen.</span><span class="sxs-lookup"><span data-stu-id="d2db2-197">Interface supports queuing.</span></span> <span data-ttu-id="d2db2-198">Damit eine Schnittstelle Warteschlangen unterstützt, sollten alle Methoden nur in den Parametern enthalten.</span><span class="sxs-lookup"><span data-stu-id="d2db2-198">For an interface to support queuing, all methods should have only in parameters.</span></span> <span data-ttu-id="d2db2-199">**Unterstützte Warteschlangen werden** als schreibgeschützte Eigenschaft verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="d2db2-199">**Queuing Supported** is exposed as a read-only property.</span></span> |
| <span data-ttu-id="d2db2-200">Access</span><span class="sxs-lookup"><span data-stu-id="d2db2-200">Access</span></span>         | <span data-ttu-id="d2db2-201">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="d2db2-201">ReadOnly</span></span>                                                                                                                                                               |
| <span data-ttu-id="d2db2-202">type</span><span class="sxs-lookup"><span data-stu-id="d2db2-202">Type</span></span>           | <span data-ttu-id="d2db2-203">Bool</span><span class="sxs-lookup"><span data-stu-id="d2db2-203">Bool</span></span>                                                                                                                                                                   |
| <span data-ttu-id="d2db2-204">Standard</span><span class="sxs-lookup"><span data-stu-id="d2db2-204">Default</span></span>        | <span data-ttu-id="d2db2-205">Falsch</span><span class="sxs-lookup"><span data-stu-id="d2db2-205">False</span></span>                                                                                                                                                                  |
| <span data-ttu-id="d2db2-206">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="d2db2-206">Minimum system</span></span> | <span data-ttu-id="d2db2-207">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d2db2-207">Windows 2000</span></span>                                                                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="d2db2-208">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2db2-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2db2-209">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="d2db2-209">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
