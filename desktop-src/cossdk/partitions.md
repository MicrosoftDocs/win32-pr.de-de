---
description: Gibt die Anwendungen an, die in jeder Partition enthalten sind.
ms.assetid: 264a35fd-ba71-4ae9-908a-24a72167c26b
title: Partitions Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Partitions
api_type:
- COM
api_location: ''
ms.openlocfilehash: b1016ae932d6841a5db590f2d24496113d3cefc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749080"
---
# <a name="partitions-collection"></a><span data-ttu-id="a3966-103">Partitions Sammlung</span><span class="sxs-lookup"><span data-stu-id="a3966-103">Partitions collection</span></span>

<span data-ttu-id="a3966-104">Gibt die Anwendungen an, die in jeder Partition enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a3966-104">Specifies the applications contained within each partition.</span></span>

<span data-ttu-id="a3966-105">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="a3966-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="a3966-106">Member</span><span class="sxs-lookup"><span data-stu-id="a3966-106">Members</span></span>

<span data-ttu-id="a3966-107">Die **Partitions** Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="a3966-107">The **Partitions** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="a3966-108">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="a3966-108">Related Collections</span></span>

<span data-ttu-id="a3966-109">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="a3966-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="a3966-110">**Anwendungen**</span><span class="sxs-lookup"><span data-stu-id="a3966-110">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="a3966-111">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="a3966-111">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="a3966-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="a3966-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="a3966-113">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="a3966-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="a3966-114">**Rolesforpartition**</span><span class="sxs-lookup"><span data-stu-id="a3966-114">**RolesForPartition**</span></span>](rolesforpartition.md)

<span data-ttu-id="a3966-115">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="a3966-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="a3966-116">**Fasst**</span><span class="sxs-lookup"><span data-stu-id="a3966-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="a3966-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a3966-117">Properties</span></span>

<span data-ttu-id="a3966-118">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="a3966-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="a3966-119">Austauschbar</span><span class="sxs-lookup"><span data-stu-id="a3966-119">Changeable</span></span>](#changeable)
-   [<span data-ttu-id="a3966-120">Gelöscht werden</span><span class="sxs-lookup"><span data-stu-id="a3966-120">Deleteable</span></span>](#deleteable)
-   [<span data-ttu-id="a3966-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3966-121">Description</span></span>](#description)
-   [<span data-ttu-id="a3966-122">ID</span><span class="sxs-lookup"><span data-stu-id="a3966-122">ID</span></span>](#partitions-collection)
-   [<span data-ttu-id="a3966-123">Name</span><span class="sxs-lookup"><span data-stu-id="a3966-123">Name</span></span>](#name)

### <a name="changeable"></a><span data-ttu-id="a3966-124">Austauschbar</span><span class="sxs-lookup"><span data-stu-id="a3966-124">Changeable</span></span>



| <span data-ttu-id="a3966-125">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3966-125">Entry</span></span> | <span data-ttu-id="a3966-126">Wert</span><span class="sxs-lookup"><span data-stu-id="a3966-126">Value</span></span> |
|----------------|--------------------------------------------------|
| <span data-ttu-id="a3966-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3966-127">Description</span></span>    | <span data-ttu-id="a3966-128">Bestimmt, ob diese Partition änderbar ist.</span><span class="sxs-lookup"><span data-stu-id="a3966-128">Determines whether this partition is changeable.</span></span> |
| <span data-ttu-id="a3966-129">Access</span><span class="sxs-lookup"><span data-stu-id="a3966-129">Access</span></span>         | <span data-ttu-id="a3966-130">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a3966-130">ReadWrite</span></span>                                        |
| <span data-ttu-id="a3966-131">type</span><span class="sxs-lookup"><span data-stu-id="a3966-131">Type</span></span>           | <span data-ttu-id="a3966-132">Bool</span><span class="sxs-lookup"><span data-stu-id="a3966-132">Bool</span></span>                                             |
| <span data-ttu-id="a3966-133">Standard</span><span class="sxs-lookup"><span data-stu-id="a3966-133">Default</span></span>        | <span data-ttu-id="a3966-134">Richtig</span><span class="sxs-lookup"><span data-stu-id="a3966-134">True</span></span>                                             |
| <span data-ttu-id="a3966-135">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="a3966-135">Minimum system</span></span> | <span data-ttu-id="a3966-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3966-136">Windows Server 2003</span></span>                              |



 

### <a name="deleteable"></a><span data-ttu-id="a3966-137">Gelöscht werden</span><span class="sxs-lookup"><span data-stu-id="a3966-137">Deleteable</span></span>



| <span data-ttu-id="a3966-138">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3966-138">Entry</span></span> | <span data-ttu-id="a3966-139">Wert</span><span class="sxs-lookup"><span data-stu-id="a3966-139">Value</span></span> |
|----------------|---------------------------------------------------|
| <span data-ttu-id="a3966-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3966-140">Description</span></span>    | <span data-ttu-id="a3966-141">Bestimmt, ob diese Partition gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="a3966-141">Determines whether this partition can be deleted.</span></span> |
| <span data-ttu-id="a3966-142">Access</span><span class="sxs-lookup"><span data-stu-id="a3966-142">Access</span></span>         | <span data-ttu-id="a3966-143">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a3966-143">ReadWrite</span></span>                                         |
| <span data-ttu-id="a3966-144">type</span><span class="sxs-lookup"><span data-stu-id="a3966-144">Type</span></span>           | <span data-ttu-id="a3966-145">Bool</span><span class="sxs-lookup"><span data-stu-id="a3966-145">Bool</span></span>                                              |
| <span data-ttu-id="a3966-146">Standard</span><span class="sxs-lookup"><span data-stu-id="a3966-146">Default</span></span>        | <span data-ttu-id="a3966-147">Richtig</span><span class="sxs-lookup"><span data-stu-id="a3966-147">True</span></span>                                              |
| <span data-ttu-id="a3966-148">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="a3966-148">Minimum system</span></span> | <span data-ttu-id="a3966-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3966-149">Windows Server 2003</span></span>                               |



 

### <a name="description"></a><span data-ttu-id="a3966-150">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3966-150">Description</span></span>



| <span data-ttu-id="a3966-151">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3966-151">Entry</span></span> | <span data-ttu-id="a3966-152">Wert</span><span class="sxs-lookup"><span data-stu-id="a3966-152">Value</span></span> |
|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="a3966-153">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3966-153">Description</span></span>    | <span data-ttu-id="a3966-154">Diese Eigenschaft stellt die Beschreibung dar, die die Partition identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a3966-154">This property represents the description identifying the partition.</span></span> |
| <span data-ttu-id="a3966-155">Access</span><span class="sxs-lookup"><span data-stu-id="a3966-155">Access</span></span>         | <span data-ttu-id="a3966-156">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a3966-156">ReadWrite</span></span>                                                           |
| <span data-ttu-id="a3966-157">type</span><span class="sxs-lookup"><span data-stu-id="a3966-157">Type</span></span>           | <span data-ttu-id="a3966-158">String</span><span class="sxs-lookup"><span data-stu-id="a3966-158">String</span></span>                                                              |
| <span data-ttu-id="a3966-159">Standard</span><span class="sxs-lookup"><span data-stu-id="a3966-159">Default</span></span>        | <span data-ttu-id="a3966-160">""</span><span class="sxs-lookup"><span data-stu-id="a3966-160">""</span></span>                                                                  |
| <span data-ttu-id="a3966-161">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="a3966-161">Minimum system</span></span> | <span data-ttu-id="a3966-162">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3966-162">Windows Server 2003</span></span>                                                 |



 

### <a name="id"></a><span data-ttu-id="a3966-163">id</span><span class="sxs-lookup"><span data-stu-id="a3966-163">ID</span></span>



| <span data-ttu-id="a3966-164">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3966-164">Entry</span></span> | <span data-ttu-id="a3966-165">Wert</span><span class="sxs-lookup"><span data-stu-id="a3966-165">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3966-166">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3966-166">Description</span></span>    | <span data-ttu-id="a3966-167">Eine GUID, die die Partition darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3966-167">A GUID representing the partition.</span></span> <span data-ttu-id="a3966-168">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a3966-168">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="a3966-169">Access</span><span class="sxs-lookup"><span data-stu-id="a3966-169">Access</span></span>         | <span data-ttu-id="a3966-170">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="a3966-170">WriteOnce</span></span>                                                                                                                                                          |
| <span data-ttu-id="a3966-171">type</span><span class="sxs-lookup"><span data-stu-id="a3966-171">Type</span></span>           | <span data-ttu-id="a3966-172">String</span><span class="sxs-lookup"><span data-stu-id="a3966-172">String</span></span>                                                                                                                                                             |
| <span data-ttu-id="a3966-173">Standard</span><span class="sxs-lookup"><span data-stu-id="a3966-173">Default</span></span>        | <Generated>                                                                                                                                                  |
| <span data-ttu-id="a3966-174">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="a3966-174">Minimum system</span></span> | <span data-ttu-id="a3966-175">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3966-175">Windows Server 2003</span></span>                                                                                                                                                |



 

### <a name="name"></a><span data-ttu-id="a3966-176">Name</span><span class="sxs-lookup"><span data-stu-id="a3966-176">Name</span></span>



| <span data-ttu-id="a3966-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3966-177">Entry</span></span> | <span data-ttu-id="a3966-178">Wert</span><span class="sxs-lookup"><span data-stu-id="a3966-178">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3966-179">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3966-179">Description</span></span>    | <span data-ttu-id="a3966-180">Stellt den Partitionsnamen dar.</span><span class="sxs-lookup"><span data-stu-id="a3966-180">Represents the partition name.</span></span> <span data-ttu-id="a3966-181">Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a3966-181">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="a3966-182">Access</span><span class="sxs-lookup"><span data-stu-id="a3966-182">Access</span></span>         | <span data-ttu-id="a3966-183">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a3966-183">ReadWrite</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="a3966-184">type</span><span class="sxs-lookup"><span data-stu-id="a3966-184">Type</span></span>           | <span data-ttu-id="a3966-185">String</span><span class="sxs-lookup"><span data-stu-id="a3966-185">String</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="a3966-186">Standard</span><span class="sxs-lookup"><span data-stu-id="a3966-186">Default</span></span>        | <span data-ttu-id="a3966-187">"Neue Partition"</span><span class="sxs-lookup"><span data-stu-id="a3966-187">"New Partition"</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="a3966-188">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="a3966-188">Minimum system</span></span> | <span data-ttu-id="a3966-189">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3966-189">Windows Server 2003</span></span>                                                                                                                                                                                                                    |



 

## <a name="see-also"></a><span data-ttu-id="a3966-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3966-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3966-191">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="a3966-191">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
