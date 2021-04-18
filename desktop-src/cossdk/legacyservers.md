---
description: Identisch mit der inprocservers-Auflistung, mit der Ausnahme, dass diese Sammlung auch lokale Server enthält.
ms.assetid: b185f568-ec97-4710-b744-5d69e71d6f60
title: Legacyservers-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2ea542fa539ea1eb1cceae0f4cb8ba8dc2012085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344199"
---
# <a name="legacyservers-collection"></a><span data-ttu-id="3269a-103">Legacyservers-Sammlung</span><span class="sxs-lookup"><span data-stu-id="3269a-103">LegacyServers collection</span></span>

<span data-ttu-id="3269a-104">Identisch mit der [**inprocservers**](inprocservers.md) -Auflistung, mit der Ausnahme, dass diese Sammlung auch lokale Server enthält.</span><span class="sxs-lookup"><span data-stu-id="3269a-104">Identical to the [**InprocServers**](inprocservers.md) collection except that this collection also includes local servers.</span></span>

<span data-ttu-id="3269a-105">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts nicht.</span><span class="sxs-lookup"><span data-stu-id="3269a-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="3269a-106">Member</span><span class="sxs-lookup"><span data-stu-id="3269a-106">Members</span></span>

<span data-ttu-id="3269a-107">Die **Legacyservers** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="3269a-107">The **LegacyServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="3269a-108">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="3269a-108">Related Collections</span></span>

<span data-ttu-id="3269a-109">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="3269a-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="3269a-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="3269a-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="3269a-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="3269a-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="3269a-112">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="3269a-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="3269a-113">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="3269a-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="3269a-114">**Fasst**</span><span class="sxs-lookup"><span data-stu-id="3269a-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="3269a-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3269a-115">Properties</span></span>

<span data-ttu-id="3269a-116">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="3269a-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="3269a-117">ClassName</span><span class="sxs-lookup"><span data-stu-id="3269a-117">ClassName</span></span>](#classname)
-   [<span data-ttu-id="3269a-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="3269a-118">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="3269a-119">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="3269a-119">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="3269a-120">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="3269a-120">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="3269a-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="3269a-121">ProgID</span></span>](#progid)

### <a name="classname"></a><span data-ttu-id="3269a-122">ClassName</span><span class="sxs-lookup"><span data-stu-id="3269a-122">ClassName</span></span>



| <span data-ttu-id="3269a-123">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3269a-123">Entry</span></span> | <span data-ttu-id="3269a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="3269a-124">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="3269a-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3269a-125">Description</span></span>    | <span data-ttu-id="3269a-126">Der Name der Klasse.</span><span class="sxs-lookup"><span data-stu-id="3269a-126">The name of the class.</span></span> |
| <span data-ttu-id="3269a-127">Access</span><span class="sxs-lookup"><span data-stu-id="3269a-127">Access</span></span>         | <span data-ttu-id="3269a-128">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3269a-128">ReadOnly</span></span>               |
| <span data-ttu-id="3269a-129">type</span><span class="sxs-lookup"><span data-stu-id="3269a-129">Type</span></span>           | <span data-ttu-id="3269a-130">String</span><span class="sxs-lookup"><span data-stu-id="3269a-130">String</span></span>                 |
| <span data-ttu-id="3269a-131">Standard</span><span class="sxs-lookup"><span data-stu-id="3269a-131">Default</span></span>        | <span data-ttu-id="3269a-132">–</span><span class="sxs-lookup"><span data-stu-id="3269a-132">N/A</span></span>                    |
| <span data-ttu-id="3269a-133">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3269a-133">Minimum system</span></span> | <span data-ttu-id="3269a-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3269a-134">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="3269a-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="3269a-135">CLSID</span></span>



| <span data-ttu-id="3269a-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3269a-136">Entry</span></span> | <span data-ttu-id="3269a-137">Wert</span><span class="sxs-lookup"><span data-stu-id="3269a-137">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3269a-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3269a-138">Description</span></span>    | <span data-ttu-id="3269a-139">Eine GUID für die Komponente.</span><span class="sxs-lookup"><span data-stu-id="3269a-139">A GUID for the component.</span></span> <span data-ttu-id="3269a-140">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3269a-140">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="3269a-141">Access</span><span class="sxs-lookup"><span data-stu-id="3269a-141">Access</span></span>         | <span data-ttu-id="3269a-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3269a-142">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="3269a-143">type</span><span class="sxs-lookup"><span data-stu-id="3269a-143">Type</span></span>           | <span data-ttu-id="3269a-144">String</span><span class="sxs-lookup"><span data-stu-id="3269a-144">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="3269a-145">Standard</span><span class="sxs-lookup"><span data-stu-id="3269a-145">Default</span></span>        | <span data-ttu-id="3269a-146">–</span><span class="sxs-lookup"><span data-stu-id="3269a-146">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="3269a-147">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3269a-147">Minimum system</span></span> | <span data-ttu-id="3269a-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3269a-148">Windows XP</span></span>                                                                                                                                                |



 

### <a name="inprocserver32"></a><span data-ttu-id="3269a-149">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="3269a-149">InprocServer32</span></span>



| <span data-ttu-id="3269a-150">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3269a-150">Entry</span></span> | <span data-ttu-id="3269a-151">Wert</span><span class="sxs-lookup"><span data-stu-id="3269a-151">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="3269a-152">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3269a-152">Description</span></span>    | <span data-ttu-id="3269a-153">Der Dateipfad für die Komponente.</span><span class="sxs-lookup"><span data-stu-id="3269a-153">The file path for the component.</span></span> |
| <span data-ttu-id="3269a-154">Access</span><span class="sxs-lookup"><span data-stu-id="3269a-154">Access</span></span>         | <span data-ttu-id="3269a-155">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3269a-155">ReadOnly</span></span>                         |
| <span data-ttu-id="3269a-156">type</span><span class="sxs-lookup"><span data-stu-id="3269a-156">Type</span></span>           | <span data-ttu-id="3269a-157">String</span><span class="sxs-lookup"><span data-stu-id="3269a-157">String</span></span>                           |
| <span data-ttu-id="3269a-158">Standard</span><span class="sxs-lookup"><span data-stu-id="3269a-158">Default</span></span>        | <span data-ttu-id="3269a-159">–</span><span class="sxs-lookup"><span data-stu-id="3269a-159">N/A</span></span>                              |
| <span data-ttu-id="3269a-160">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3269a-160">Minimum system</span></span> | <span data-ttu-id="3269a-161">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3269a-161">Windows XP</span></span>                       |



 

### <a name="localserver32"></a><span data-ttu-id="3269a-162">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="3269a-162">LocalServer32</span></span>



| <span data-ttu-id="3269a-163">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3269a-163">Entry</span></span> | <span data-ttu-id="3269a-164">Wert</span><span class="sxs-lookup"><span data-stu-id="3269a-164">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="3269a-165">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3269a-165">Description</span></span>    | <span data-ttu-id="3269a-166">Gibt den vollständigen Pfad zu einer lokalen 32-Bit-Serveranwendung an.</span><span class="sxs-lookup"><span data-stu-id="3269a-166">Specifies the full path to a 32-bit local server application.</span></span> |
| <span data-ttu-id="3269a-167">Access</span><span class="sxs-lookup"><span data-stu-id="3269a-167">Access</span></span>         | <span data-ttu-id="3269a-168">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3269a-168">ReadOnly</span></span>                                                      |
| <span data-ttu-id="3269a-169">type</span><span class="sxs-lookup"><span data-stu-id="3269a-169">Type</span></span>           | <span data-ttu-id="3269a-170">String</span><span class="sxs-lookup"><span data-stu-id="3269a-170">String</span></span>                                                        |
| <span data-ttu-id="3269a-171">Standard</span><span class="sxs-lookup"><span data-stu-id="3269a-171">Default</span></span>        | <span data-ttu-id="3269a-172">–</span><span class="sxs-lookup"><span data-stu-id="3269a-172">N/A</span></span>                                                           |
| <span data-ttu-id="3269a-173">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3269a-173">Minimum system</span></span> | <span data-ttu-id="3269a-174">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3269a-174">Windows XP</span></span>                                                    |



 

### <a name="progid"></a><span data-ttu-id="3269a-175">ProgID</span><span class="sxs-lookup"><span data-stu-id="3269a-175">ProgID</span></span>



| <span data-ttu-id="3269a-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3269a-176">Entry</span></span> | <span data-ttu-id="3269a-177">Wert</span><span class="sxs-lookup"><span data-stu-id="3269a-177">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3269a-178">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3269a-178">Description</span></span>    | <span data-ttu-id="3269a-179">Ein Name, der die Komponente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3269a-179">A name identifying the component.</span></span> <span data-ttu-id="3269a-180">Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3269a-180">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="3269a-181">Access</span><span class="sxs-lookup"><span data-stu-id="3269a-181">Access</span></span>         | <span data-ttu-id="3269a-182">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3269a-182">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="3269a-183">type</span><span class="sxs-lookup"><span data-stu-id="3269a-183">Type</span></span>           | <span data-ttu-id="3269a-184">String</span><span class="sxs-lookup"><span data-stu-id="3269a-184">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="3269a-185">Standard</span><span class="sxs-lookup"><span data-stu-id="3269a-185">Default</span></span>        | <span data-ttu-id="3269a-186">–</span><span class="sxs-lookup"><span data-stu-id="3269a-186">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="3269a-187">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3269a-187">Minimum system</span></span> | <span data-ttu-id="3269a-188">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3269a-188">Windows XP</span></span>                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="3269a-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3269a-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3269a-190">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="3269a-190">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
