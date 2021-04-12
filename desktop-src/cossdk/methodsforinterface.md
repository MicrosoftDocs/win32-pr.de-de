---
description: Enthält ein-Objekt für jede Methode in der Schnittstelle, mit der die Auflistung verknüpft ist.
ms.assetid: e64b007f-e44d-4b6b-97b2-1e017c5a7dbe
title: Methodsforinterface-Auflistung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MethodsForInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6057d06d4a67222095d5bb0b5ae6da0d603fb4ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393226"
---
# <a name="methodsforinterface-collection"></a><span data-ttu-id="2167d-103">Methodsforinterface-Auflistung</span><span class="sxs-lookup"><span data-stu-id="2167d-103">MethodsForInterface collection</span></span>

<span data-ttu-id="2167d-104">Enthält ein-Objekt für jede Methode in der Schnittstelle, mit der die Auflistung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="2167d-104">Contains an object for each method on the interface to which the collection is related.</span></span>

<span data-ttu-id="2167d-105">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts nicht.</span><span class="sxs-lookup"><span data-stu-id="2167d-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="2167d-106">Member</span><span class="sxs-lookup"><span data-stu-id="2167d-106">Members</span></span>

<span data-ttu-id="2167d-107">Die **methodsforinterface** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="2167d-107">The **MethodsForInterface** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="2167d-108">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="2167d-108">Related Collections</span></span>

<span data-ttu-id="2167d-109">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="2167d-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="2167d-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="2167d-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="2167d-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="2167d-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="2167d-112">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="2167d-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="2167d-113">**Rolesformethod**</span><span class="sxs-lookup"><span data-stu-id="2167d-113">**RolesForMethod**</span></span>](rolesformethod.md)

<span data-ttu-id="2167d-114">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="2167d-114">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="2167d-115">**Interfakesforcomponent**</span><span class="sxs-lookup"><span data-stu-id="2167d-115">**InterfacesForComponent**</span></span>](interfacesforcomponent.md)

## <a name="properties"></a><span data-ttu-id="2167d-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2167d-116">Properties</span></span>

<span data-ttu-id="2167d-117">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="2167d-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="2167d-118">Auto Vervollständigen</span><span class="sxs-lookup"><span data-stu-id="2167d-118">AutoComplete</span></span>](#autocomplete)
-   [<span data-ttu-id="2167d-119">CLSID</span><span class="sxs-lookup"><span data-stu-id="2167d-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="2167d-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2167d-120">Description</span></span>](#description)
-   [<span data-ttu-id="2167d-121">IID</span><span class="sxs-lookup"><span data-stu-id="2167d-121">IID</span></span>](#iid)
-   [<span data-ttu-id="2167d-122">Index</span><span class="sxs-lookup"><span data-stu-id="2167d-122">Index</span></span>](#index)
-   [<span data-ttu-id="2167d-123">Name</span><span class="sxs-lookup"><span data-stu-id="2167d-123">Name</span></span>](#name)

### <a name="autocomplete"></a><span data-ttu-id="2167d-124">AutoComplete</span><span class="sxs-lookup"><span data-stu-id="2167d-124">AutoComplete</span></span>



| <span data-ttu-id="2167d-125">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2167d-125">Entry</span></span> | <span data-ttu-id="2167d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2167d-126">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2167d-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2167d-127">Description</span></span>    | <span data-ttu-id="2167d-128">Bestimmt, ob das Objekt automatisch deaktiviert wird, wenn die Methode abgeschlossen wird, ohne dass SetComplete oder SetAbort unbedingt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2167d-128">Determines whether the object is automatically deactivated when the method completes, without SetComplete or SetAbort necessarily being called.</span></span> <span data-ttu-id="2167d-129">Dies wirkt sich nur auf die Standardeinstellung des Bits "Done" der JIT-Aktivierung beim Starten der Methode aus. Dieses Bit kann (wie bei SetComplete oder SetAbort) innerhalb der-Methode zurückgesetzt werden, um den Standardwert zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="2167d-129">This affects only the default setting of the JIT Activation "Done" bit at method start; this bit can be reset (as with SetComplete or SetAbort) within the method to override the default.</span></span> |
| <span data-ttu-id="2167d-130">Access</span><span class="sxs-lookup"><span data-stu-id="2167d-130">Access</span></span>         | <span data-ttu-id="2167d-131">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2167d-131">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2167d-132">type</span><span class="sxs-lookup"><span data-stu-id="2167d-132">Type</span></span>           | <span data-ttu-id="2167d-133">Bool</span><span class="sxs-lookup"><span data-stu-id="2167d-133">Bool</span></span>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2167d-134">Standard</span><span class="sxs-lookup"><span data-stu-id="2167d-134">Default</span></span>        | <span data-ttu-id="2167d-135">Falsch</span><span class="sxs-lookup"><span data-stu-id="2167d-135">False</span></span>                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="2167d-136">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="2167d-136">Minimum system</span></span> | <span data-ttu-id="2167d-137">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="2167d-137">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                               |



 

### <a name="clsid"></a><span data-ttu-id="2167d-138">CLSID</span><span class="sxs-lookup"><span data-stu-id="2167d-138">CLSID</span></span>



| <span data-ttu-id="2167d-139">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2167d-139">Entry</span></span> | <span data-ttu-id="2167d-140">Wert</span><span class="sxs-lookup"><span data-stu-id="2167d-140">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="2167d-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2167d-141">Description</span></span>    | <span data-ttu-id="2167d-142">Eine GUID für die Komponente.</span><span class="sxs-lookup"><span data-stu-id="2167d-142">A GUID for the component.</span></span> |
| <span data-ttu-id="2167d-143">Access</span><span class="sxs-lookup"><span data-stu-id="2167d-143">Access</span></span>         | <span data-ttu-id="2167d-144">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2167d-144">ReadOnly</span></span>                  |
| <span data-ttu-id="2167d-145">type</span><span class="sxs-lookup"><span data-stu-id="2167d-145">Type</span></span>           | <span data-ttu-id="2167d-146">String</span><span class="sxs-lookup"><span data-stu-id="2167d-146">String</span></span>                    |
| <span data-ttu-id="2167d-147">Standard</span><span class="sxs-lookup"><span data-stu-id="2167d-147">Default</span></span>        | <span data-ttu-id="2167d-148">–</span><span class="sxs-lookup"><span data-stu-id="2167d-148">N/A</span></span>                       |
| <span data-ttu-id="2167d-149">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="2167d-149">Minimum system</span></span> | <span data-ttu-id="2167d-150">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="2167d-150">Windows 2000</span></span>              |



 

### <a name="description"></a><span data-ttu-id="2167d-151">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2167d-151">Description</span></span>



| <span data-ttu-id="2167d-152">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2167d-152">Entry</span></span> | <span data-ttu-id="2167d-153">Wert</span><span class="sxs-lookup"><span data-stu-id="2167d-153">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="2167d-154">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2167d-154">Description</span></span>    | <span data-ttu-id="2167d-155">Eine Beschreibung der Methode.</span><span class="sxs-lookup"><span data-stu-id="2167d-155">A description of the method.</span></span> |
| <span data-ttu-id="2167d-156">Access</span><span class="sxs-lookup"><span data-stu-id="2167d-156">Access</span></span>         | <span data-ttu-id="2167d-157">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2167d-157">ReadWrite</span></span>                    |
| <span data-ttu-id="2167d-158">type</span><span class="sxs-lookup"><span data-stu-id="2167d-158">Type</span></span>           | <span data-ttu-id="2167d-159">String</span><span class="sxs-lookup"><span data-stu-id="2167d-159">String</span></span>                       |
| <span data-ttu-id="2167d-160">Standard</span><span class="sxs-lookup"><span data-stu-id="2167d-160">Default</span></span>        | <span data-ttu-id="2167d-161">""</span><span class="sxs-lookup"><span data-stu-id="2167d-161">""</span></span>                           |
| <span data-ttu-id="2167d-162">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="2167d-162">Minimum system</span></span> | <span data-ttu-id="2167d-163">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="2167d-163">Windows 2000</span></span>                 |



 

### <a name="iid"></a><span data-ttu-id="2167d-164">IID</span><span class="sxs-lookup"><span data-stu-id="2167d-164">IID</span></span>



| <span data-ttu-id="2167d-165">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2167d-165">Entry</span></span> | <span data-ttu-id="2167d-166">Wert</span><span class="sxs-lookup"><span data-stu-id="2167d-166">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="2167d-167">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2167d-167">Description</span></span>    | <span data-ttu-id="2167d-168">Eine GUID für die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2167d-168">A GUID for the interface.</span></span> |
| <span data-ttu-id="2167d-169">Access</span><span class="sxs-lookup"><span data-stu-id="2167d-169">Access</span></span>         | <span data-ttu-id="2167d-170">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2167d-170">ReadOnly</span></span>                  |
| <span data-ttu-id="2167d-171">type</span><span class="sxs-lookup"><span data-stu-id="2167d-171">Type</span></span>           | <span data-ttu-id="2167d-172">String</span><span class="sxs-lookup"><span data-stu-id="2167d-172">String</span></span>                    |
| <span data-ttu-id="2167d-173">Standard</span><span class="sxs-lookup"><span data-stu-id="2167d-173">Default</span></span>        | <span data-ttu-id="2167d-174">–</span><span class="sxs-lookup"><span data-stu-id="2167d-174">N/A</span></span>                       |
| <span data-ttu-id="2167d-175">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="2167d-175">Minimum system</span></span> | <span data-ttu-id="2167d-176">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="2167d-176">Windows 2000</span></span>              |



 

### <a name="index"></a><span data-ttu-id="2167d-177">Index</span><span class="sxs-lookup"><span data-stu-id="2167d-177">Index</span></span>



| <span data-ttu-id="2167d-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2167d-178">Entry</span></span> | <span data-ttu-id="2167d-179">Wert</span><span class="sxs-lookup"><span data-stu-id="2167d-179">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2167d-180">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2167d-180">Description</span></span>    | <span data-ttu-id="2167d-181">Der Methoden Dispatchbezeichner.</span><span class="sxs-lookup"><span data-stu-id="2167d-181">The method dispatch identifier.</span></span> <span data-ttu-id="2167d-182">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2167d-182">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="2167d-183">Access</span><span class="sxs-lookup"><span data-stu-id="2167d-183">Access</span></span>         | <span data-ttu-id="2167d-184">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2167d-184">ReadOnly</span></span>                                                                                                                                                        |
| <span data-ttu-id="2167d-185">type</span><span class="sxs-lookup"><span data-stu-id="2167d-185">Type</span></span>           | <span data-ttu-id="2167d-186">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="2167d-186">**DWORD**</span></span>                                                                                                                                                       |
| <span data-ttu-id="2167d-187">Standard</span><span class="sxs-lookup"><span data-stu-id="2167d-187">Default</span></span>        | <span data-ttu-id="2167d-188">–</span><span class="sxs-lookup"><span data-stu-id="2167d-188">N/A</span></span>                                                                                                                                                             |
| <span data-ttu-id="2167d-189">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="2167d-189">Minimum system</span></span> | <span data-ttu-id="2167d-190">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="2167d-190">Windows 2000</span></span>                                                                                                                                                    |



 

### <a name="name"></a><span data-ttu-id="2167d-191">Name</span><span class="sxs-lookup"><span data-stu-id="2167d-191">Name</span></span>



| <span data-ttu-id="2167d-192">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2167d-192">Entry</span></span> | <span data-ttu-id="2167d-193">Wert</span><span class="sxs-lookup"><span data-stu-id="2167d-193">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2167d-194">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2167d-194">Description</span></span>    | <span data-ttu-id="2167d-195">Der Methodenname.</span><span class="sxs-lookup"><span data-stu-id="2167d-195">The method name.</span></span> <span data-ttu-id="2167d-196">Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2167d-196">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="2167d-197">Access</span><span class="sxs-lookup"><span data-stu-id="2167d-197">Access</span></span>         | <span data-ttu-id="2167d-198">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2167d-198">ReadOnly</span></span>                                                                                                                                           |
| <span data-ttu-id="2167d-199">type</span><span class="sxs-lookup"><span data-stu-id="2167d-199">Type</span></span>           | <span data-ttu-id="2167d-200">String</span><span class="sxs-lookup"><span data-stu-id="2167d-200">String</span></span>                                                                                                                                             |
| <span data-ttu-id="2167d-201">Standard</span><span class="sxs-lookup"><span data-stu-id="2167d-201">Default</span></span>        | <span data-ttu-id="2167d-202">–</span><span class="sxs-lookup"><span data-stu-id="2167d-202">N/A</span></span>                                                                                                                                                |
| <span data-ttu-id="2167d-203">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="2167d-203">Minimum system</span></span> | <span data-ttu-id="2167d-204">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="2167d-204">Windows 2000</span></span>                                                                                                                                       |



 

## <a name="see-also"></a><span data-ttu-id="2167d-205">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2167d-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2167d-206">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="2167d-206">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
