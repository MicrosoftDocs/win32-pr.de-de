---
description: Ruft Informationen für importierte Anwendungen ab.
ms.assetid: 9ed4bc3f-3490-4c36-ba94-bc803886a4d2
title: Sammlung "filesforimport"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilesForImport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8e7ba3b0bd44cf2f6bb40ecf89f86dd68c21cf3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127144"
---
# <a name="filesforimport-collection"></a><span data-ttu-id="c259c-103">Sammlung "filesforimport"</span><span class="sxs-lookup"><span data-stu-id="c259c-103">FilesForImport collection</span></span>

<span data-ttu-id="c259c-104">Ruft Informationen für importierte Anwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="c259c-104">Retrieves information for applications that are imported.</span></span>

<span data-ttu-id="c259c-105">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="c259c-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="c259c-106">Member</span><span class="sxs-lookup"><span data-stu-id="c259c-106">Members</span></span>

<span data-ttu-id="c259c-107">Die Sammlung " **filesforimport** " erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="c259c-107">The **FilesForImport** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="c259c-108">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="c259c-108">Related Collections</span></span>

<span data-ttu-id="c259c-109">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="c259c-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="c259c-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="c259c-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="c259c-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="c259c-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="c259c-112">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="c259c-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="c259c-113">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="c259c-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="c259c-114">**Fasst**</span><span class="sxs-lookup"><span data-stu-id="c259c-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="c259c-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c259c-115">Properties</span></span>

<span data-ttu-id="c259c-116">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c259c-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="c259c-117">Applicationfilename</span><span class="sxs-lookup"><span data-stu-id="c259c-117">ApplicationFileName</span></span>](#applicationfilename)
-   [<span data-ttu-id="c259c-118">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="c259c-118">ApplicationName</span></span>](#applicationname)
-   [<span data-ttu-id="c259c-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c259c-119">Description</span></span>](#partitiondescription)
-   [<span data-ttu-id="c259c-120">FileName</span><span class="sxs-lookup"><span data-stu-id="c259c-120">FileName</span></span>](#applicationfilename)
-   [<span data-ttu-id="c259c-121">Hasusers</span><span class="sxs-lookup"><span data-stu-id="c259c-121">HasUsers</span></span>](#hasusers)
-   [<span data-ttu-id="c259c-122">IsProxy</span><span class="sxs-lookup"><span data-stu-id="c259c-122">IsProxy</span></span>](#isproxy)
-   [<span data-ttu-id="c259c-123">IsService</span><span class="sxs-lookup"><span data-stu-id="c259c-123">IsService</span></span>](#isservice)
-   [<span data-ttu-id="c259c-124">PartitionDescription</span><span class="sxs-lookup"><span data-stu-id="c259c-124">PartitionDescription</span></span>](#partitiondescription)
-   [<span data-ttu-id="c259c-125">PartitionID</span><span class="sxs-lookup"><span data-stu-id="c259c-125">PartitionID</span></span>](#partitionid)
-   [<span data-ttu-id="c259c-126">PartitionName</span><span class="sxs-lookup"><span data-stu-id="c259c-126">PartitionName</span></span>](#partitionname)

### <a name="applicationfilename"></a><span data-ttu-id="c259c-127">Applicationfilename</span><span class="sxs-lookup"><span data-stu-id="c259c-127">ApplicationFileName</span></span>



| <span data-ttu-id="c259c-128">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c259c-128">Entry</span></span> | <span data-ttu-id="c259c-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c259c-129">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c259c-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c259c-130">Description</span></span>    | <span data-ttu-id="c259c-131">Der Name der MSI-Datei, die die Anwendung enthält, die importiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c259c-131">The name of the MSI file that contains the application that can be imported.</span></span> |
| <span data-ttu-id="c259c-132">Access</span><span class="sxs-lookup"><span data-stu-id="c259c-132">Access</span></span>         | <span data-ttu-id="c259c-133">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c259c-133">ReadOnly</span></span>                                                                     |
| <span data-ttu-id="c259c-134">type</span><span class="sxs-lookup"><span data-stu-id="c259c-134">Type</span></span>           | <span data-ttu-id="c259c-135">String</span><span class="sxs-lookup"><span data-stu-id="c259c-135">String</span></span>                                                                       |
| <span data-ttu-id="c259c-136">Standard</span><span class="sxs-lookup"><span data-stu-id="c259c-136">Default</span></span>        | <span data-ttu-id="c259c-137">–</span><span class="sxs-lookup"><span data-stu-id="c259c-137">N/A</span></span>                                                                          |
| <span data-ttu-id="c259c-138">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="c259c-138">Minimum system</span></span> | <span data-ttu-id="c259c-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c259c-139">Windows XP</span></span>                                                                   |



 

### <a name="applicationname"></a><span data-ttu-id="c259c-140">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="c259c-140">ApplicationName</span></span>



| <span data-ttu-id="c259c-141">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c259c-141">Entry</span></span> | <span data-ttu-id="c259c-142">Wert</span><span class="sxs-lookup"><span data-stu-id="c259c-142">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="c259c-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c259c-143">Description</span></span>    | <span data-ttu-id="c259c-144">Der Namen der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c259c-144">The name of the application.</span></span> |
| <span data-ttu-id="c259c-145">Access</span><span class="sxs-lookup"><span data-stu-id="c259c-145">Access</span></span>         | <span data-ttu-id="c259c-146">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c259c-146">ReadOnly</span></span>                     |
| <span data-ttu-id="c259c-147">type</span><span class="sxs-lookup"><span data-stu-id="c259c-147">Type</span></span>           | <span data-ttu-id="c259c-148">String</span><span class="sxs-lookup"><span data-stu-id="c259c-148">String</span></span>                       |
| <span data-ttu-id="c259c-149">Standard</span><span class="sxs-lookup"><span data-stu-id="c259c-149">Default</span></span>        | <span data-ttu-id="c259c-150">""</span><span class="sxs-lookup"><span data-stu-id="c259c-150">""</span></span>                           |
| <span data-ttu-id="c259c-151">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="c259c-151">Minimum system</span></span> | <span data-ttu-id="c259c-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c259c-152">Windows XP</span></span>                   |



 

### <a name="description"></a><span data-ttu-id="c259c-153">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c259c-153">Description</span></span>



| <span data-ttu-id="c259c-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c259c-154">Entry</span></span> | <span data-ttu-id="c259c-155">Wert</span><span class="sxs-lookup"><span data-stu-id="c259c-155">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="c259c-156">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c259c-156">Description</span></span>    | <span data-ttu-id="c259c-157">Eine Beschreibung der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c259c-157">A description of the application.</span></span> |
| <span data-ttu-id="c259c-158">Access</span><span class="sxs-lookup"><span data-stu-id="c259c-158">Access</span></span>         | <span data-ttu-id="c259c-159">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c259c-159">ReadOnly</span></span>                          |
| <span data-ttu-id="c259c-160">type</span><span class="sxs-lookup"><span data-stu-id="c259c-160">Type</span></span>           | <span data-ttu-id="c259c-161">String</span><span class="sxs-lookup"><span data-stu-id="c259c-161">String</span></span>                            |
| <span data-ttu-id="c259c-162">Standard</span><span class="sxs-lookup"><span data-stu-id="c259c-162">Default</span></span>        | <span data-ttu-id="c259c-163">""</span><span class="sxs-lookup"><span data-stu-id="c259c-163">""</span></span>                                |
| <span data-ttu-id="c259c-164">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="c259c-164">Minimum system</span></span> | <span data-ttu-id="c259c-165">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c259c-165">Windows XP</span></span>                        |



 

### <a name="filename"></a><span data-ttu-id="c259c-166">FileName</span><span class="sxs-lookup"><span data-stu-id="c259c-166">FileName</span></span>



| <span data-ttu-id="c259c-167">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c259c-167">Entry</span></span> | <span data-ttu-id="c259c-168">Wert</span><span class="sxs-lookup"><span data-stu-id="c259c-168">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c259c-169">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c259c-169">Description</span></span>    | <span data-ttu-id="c259c-170">Der Name der DLL-oder exe-Datei, die die Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="c259c-170">The name of the DLL or EXE file that contains the application.</span></span> <span data-ttu-id="c259c-171">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c259c-171">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="c259c-172">Access</span><span class="sxs-lookup"><span data-stu-id="c259c-172">Access</span></span>         | <span data-ttu-id="c259c-173">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c259c-173">ReadOnly</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="c259c-174">type</span><span class="sxs-lookup"><span data-stu-id="c259c-174">Type</span></span>           | <span data-ttu-id="c259c-175">String</span><span class="sxs-lookup"><span data-stu-id="c259c-175">String</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="c259c-176">Standard</span><span class="sxs-lookup"><span data-stu-id="c259c-176">Default</span></span>        | <span data-ttu-id="c259c-177">""</span><span class="sxs-lookup"><span data-stu-id="c259c-177">""</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="c259c-178">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="c259c-178">Minimum system</span></span> | <span data-ttu-id="c259c-179">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c259c-179">Windows XP</span></span>                                                                                                                                                                                                                            |



 

### <a name="hasusers"></a><span data-ttu-id="c259c-180">Hasusers</span><span class="sxs-lookup"><span data-stu-id="c259c-180">HasUsers</span></span>



| <span data-ttu-id="c259c-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c259c-181">Entry</span></span> | <span data-ttu-id="c259c-182">Wert</span><span class="sxs-lookup"><span data-stu-id="c259c-182">Value</span></span> |
|----------------|--------------------------------------------------|
| <span data-ttu-id="c259c-183">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c259c-183">Description</span></span>    | <span data-ttu-id="c259c-184">Gibt an, ob die Anwendung über Benutzer verfügt.</span><span class="sxs-lookup"><span data-stu-id="c259c-184">Indicates whether the application has any users.</span></span> |
| <span data-ttu-id="c259c-185">Access</span><span class="sxs-lookup"><span data-stu-id="c259c-185">Access</span></span>         | <span data-ttu-id="c259c-186">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c259c-186">ReadOnly</span></span>                                         |
| <span data-ttu-id="c259c-187">type</span><span class="sxs-lookup"><span data-stu-id="c259c-187">Type</span></span>           | <span data-ttu-id="c259c-188">Bool</span><span class="sxs-lookup"><span data-stu-id="c259c-188">Bool</span></span>                                             |
| <span data-ttu-id="c259c-189">Standard</span><span class="sxs-lookup"><span data-stu-id="c259c-189">Default</span></span>        | <span data-ttu-id="c259c-190">Falsch</span><span class="sxs-lookup"><span data-stu-id="c259c-190">False</span></span>                                            |
| <span data-ttu-id="c259c-191">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="c259c-191">Minimum system</span></span> | <span data-ttu-id="c259c-192">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c259c-192">Windows XP</span></span>                                       |



 

### <a name="isproxy"></a><span data-ttu-id="c259c-193">IsProxy</span><span class="sxs-lookup"><span data-stu-id="c259c-193">IsProxy</span></span>



| <span data-ttu-id="c259c-194">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c259c-194">Entry</span></span> | <span data-ttu-id="c259c-195">Wert</span><span class="sxs-lookup"><span data-stu-id="c259c-195">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="c259c-196">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c259c-196">Description</span></span>    | <span data-ttu-id="c259c-197">Gibt an, ob die Anwendung ein Proxy ist.</span><span class="sxs-lookup"><span data-stu-id="c259c-197">Indicates whether the application is a proxy.</span></span> |
| <span data-ttu-id="c259c-198">Access</span><span class="sxs-lookup"><span data-stu-id="c259c-198">Access</span></span>         | <span data-ttu-id="c259c-199">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c259c-199">ReadOnly</span></span>                                      |
| <span data-ttu-id="c259c-200">type</span><span class="sxs-lookup"><span data-stu-id="c259c-200">Type</span></span>           | <span data-ttu-id="c259c-201">Bool</span><span class="sxs-lookup"><span data-stu-id="c259c-201">Bool</span></span>                                          |
| <span data-ttu-id="c259c-202">Standard</span><span class="sxs-lookup"><span data-stu-id="c259c-202">Default</span></span>        | <span data-ttu-id="c259c-203">Falsch</span><span class="sxs-lookup"><span data-stu-id="c259c-203">False</span></span>                                         |
| <span data-ttu-id="c259c-204">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="c259c-204">Minimum system</span></span> | <span data-ttu-id="c259c-205">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c259c-205">Windows XP</span></span>                                    |



 

### <a name="isservice"></a><span data-ttu-id="c259c-206">IsService</span><span class="sxs-lookup"><span data-stu-id="c259c-206">IsService</span></span>



| <span data-ttu-id="c259c-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c259c-207">Entry</span></span> | <span data-ttu-id="c259c-208">Wert</span><span class="sxs-lookup"><span data-stu-id="c259c-208">Value</span></span> |
|----------------|-------------------------------------------------|
| <span data-ttu-id="c259c-209">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c259c-209">Description</span></span>    | <span data-ttu-id="c259c-210">Gibt an, ob die Anwendung ein Dienst ist.</span><span class="sxs-lookup"><span data-stu-id="c259c-210">Indicates whether the application is a service.</span></span> |
| <span data-ttu-id="c259c-211">Access</span><span class="sxs-lookup"><span data-stu-id="c259c-211">Access</span></span>         | <span data-ttu-id="c259c-212">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c259c-212">ReadOnly</span></span>                                        |
| <span data-ttu-id="c259c-213">type</span><span class="sxs-lookup"><span data-stu-id="c259c-213">Type</span></span>           | <span data-ttu-id="c259c-214">Bool</span><span class="sxs-lookup"><span data-stu-id="c259c-214">Bool</span></span>                                            |
| <span data-ttu-id="c259c-215">Standard</span><span class="sxs-lookup"><span data-stu-id="c259c-215">Default</span></span>        | <span data-ttu-id="c259c-216">Falsch</span><span class="sxs-lookup"><span data-stu-id="c259c-216">False</span></span>                                           |
| <span data-ttu-id="c259c-217">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="c259c-217">Minimum system</span></span> | <span data-ttu-id="c259c-218">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c259c-218">Windows XP</span></span>                                      |



 

### <a name="partitiondescription"></a><span data-ttu-id="c259c-219">PartitionDescription</span><span class="sxs-lookup"><span data-stu-id="c259c-219">PartitionDescription</span></span>



| <span data-ttu-id="c259c-220">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c259c-220">Entry</span></span> | <span data-ttu-id="c259c-221">Wert</span><span class="sxs-lookup"><span data-stu-id="c259c-221">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="c259c-222">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c259c-222">Description</span></span>    | <span data-ttu-id="c259c-223">Eine Beschreibung der Anwendungs Partition.</span><span class="sxs-lookup"><span data-stu-id="c259c-223">A description of the application's partition.</span></span> |
| <span data-ttu-id="c259c-224">Access</span><span class="sxs-lookup"><span data-stu-id="c259c-224">Access</span></span>         | <span data-ttu-id="c259c-225">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c259c-225">ReadOnly</span></span>                                      |
| <span data-ttu-id="c259c-226">type</span><span class="sxs-lookup"><span data-stu-id="c259c-226">Type</span></span>           | <span data-ttu-id="c259c-227">String</span><span class="sxs-lookup"><span data-stu-id="c259c-227">String</span></span>                                        |
| <span data-ttu-id="c259c-228">Standard</span><span class="sxs-lookup"><span data-stu-id="c259c-228">Default</span></span>        | <span data-ttu-id="c259c-229">""</span><span class="sxs-lookup"><span data-stu-id="c259c-229">""</span></span>                                            |
| <span data-ttu-id="c259c-230">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="c259c-230">Minimum system</span></span> | <span data-ttu-id="c259c-231">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c259c-231">Windows Server 2003</span></span>                           |



 

### <a name="partitionid"></a><span data-ttu-id="c259c-232">PartitionID</span><span class="sxs-lookup"><span data-stu-id="c259c-232">PartitionID</span></span>



| <span data-ttu-id="c259c-233">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c259c-233">Entry</span></span> | <span data-ttu-id="c259c-234">Wert</span><span class="sxs-lookup"><span data-stu-id="c259c-234">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="c259c-235">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c259c-235">Description</span></span>    | <span data-ttu-id="c259c-236">Die GUID der Anwendungs Partition.</span><span class="sxs-lookup"><span data-stu-id="c259c-236">The GUID of the application's partition.</span></span> |
| <span data-ttu-id="c259c-237">Access</span><span class="sxs-lookup"><span data-stu-id="c259c-237">Access</span></span>         | <span data-ttu-id="c259c-238">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c259c-238">ReadOnly</span></span>                                 |
| <span data-ttu-id="c259c-239">type</span><span class="sxs-lookup"><span data-stu-id="c259c-239">Type</span></span>           | <span data-ttu-id="c259c-240">String</span><span class="sxs-lookup"><span data-stu-id="c259c-240">String</span></span>                                   |
| <span data-ttu-id="c259c-241">Standard</span><span class="sxs-lookup"><span data-stu-id="c259c-241">Default</span></span>        | <span data-ttu-id="c259c-242">""</span><span class="sxs-lookup"><span data-stu-id="c259c-242">""</span></span>                                       |
| <span data-ttu-id="c259c-243">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="c259c-243">Minimum system</span></span> | <span data-ttu-id="c259c-244">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c259c-244">Windows Server 2003</span></span>                      |



 

### <a name="partitionname"></a><span data-ttu-id="c259c-245">PartitionName</span><span class="sxs-lookup"><span data-stu-id="c259c-245">PartitionName</span></span>



| <span data-ttu-id="c259c-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c259c-246">Entry</span></span> | <span data-ttu-id="c259c-247">Wert</span><span class="sxs-lookup"><span data-stu-id="c259c-247">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="c259c-248">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c259c-248">Description</span></span>    | <span data-ttu-id="c259c-249">Der Name der Partition der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c259c-249">The name of the application's partition.</span></span> |
| <span data-ttu-id="c259c-250">Access</span><span class="sxs-lookup"><span data-stu-id="c259c-250">Access</span></span>         | <span data-ttu-id="c259c-251">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c259c-251">ReadOnly</span></span>                                 |
| <span data-ttu-id="c259c-252">type</span><span class="sxs-lookup"><span data-stu-id="c259c-252">Type</span></span>           | <span data-ttu-id="c259c-253">String</span><span class="sxs-lookup"><span data-stu-id="c259c-253">String</span></span>                                   |
| <span data-ttu-id="c259c-254">Standard</span><span class="sxs-lookup"><span data-stu-id="c259c-254">Default</span></span>        | <span data-ttu-id="c259c-255">""</span><span class="sxs-lookup"><span data-stu-id="c259c-255">""</span></span>                                       |
| <span data-ttu-id="c259c-256">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="c259c-256">Minimum system</span></span> | <span data-ttu-id="c259c-257">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c259c-257">Windows Server 2003</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="c259c-258">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c259c-258">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c259c-259">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="c259c-259">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
