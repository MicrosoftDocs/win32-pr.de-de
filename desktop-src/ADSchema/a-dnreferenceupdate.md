---
title: DN-Reference-Update-Attribut
description: Wenn ein Objekt umbenannt wird, wird dieses Attribut verwendet, um alle vorherigen und aktuellen Namen zu verfolgen, die einem Objekt zugewiesen wurden, damit verknüpfte Objekte es noch finden können.
ms.assetid: 28e02a38-eed8-475c-a381-145857477ec6
ms.tgt_platform: multiple
keywords:
- DN-Reference-Update-Attribut für AD-Schema
- dnreferenceupdate-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- DN-Reference-Update
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71e8360be6e7ed6697363daa0f6ff32e2ec5fb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346583"
---
# <a name="dn-reference-update-attribute"></a><span data-ttu-id="c2c05-105">DN-Reference-Update-Attribut</span><span class="sxs-lookup"><span data-stu-id="c2c05-105">DN-Reference-Update attribute</span></span>

<span data-ttu-id="c2c05-106">Wenn ein Objekt umbenannt wird, wird dieses Attribut verwendet, um alle vorherigen und aktuellen Namen zu verfolgen, die einem Objekt zugewiesen wurden, damit verknüpfte Objekte es noch finden können.</span><span class="sxs-lookup"><span data-stu-id="c2c05-106">If an object is renamed, this attribute is used to track all of the previous and current names that have been assigned to an object so that linked objects can still find it.</span></span>



| <span data-ttu-id="c2c05-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c2c05-107">Entry</span></span> | <span data-ttu-id="c2c05-108">Wert</span><span class="sxs-lookup"><span data-stu-id="c2c05-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c2c05-109">CN</span><span class="sxs-lookup"><span data-stu-id="c2c05-109">CN</span></span>                | <span data-ttu-id="c2c05-110">DN-Referenz-Update</span><span class="sxs-lookup"><span data-stu-id="c2c05-110">DN-Reference-Update</span></span>                     |
| <span data-ttu-id="c2c05-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c2c05-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c2c05-112">dnreferenceupdate</span><span class="sxs-lookup"><span data-stu-id="c2c05-112">dNReferenceUpdate</span></span>                       |
| <span data-ttu-id="c2c05-113">Size</span><span class="sxs-lookup"><span data-stu-id="c2c05-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="c2c05-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c2c05-114">Update Privilege</span></span>  | <span data-ttu-id="c2c05-115">Dies wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c2c05-115">This is set by the system.</span></span>              |
| <span data-ttu-id="c2c05-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="c2c05-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="c2c05-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c2c05-117">Attribute-Id</span></span>      | <span data-ttu-id="c2c05-118">1.2.840.113556.1.4.1242</span><span class="sxs-lookup"><span data-stu-id="c2c05-118">1.2.840.113556.1.4.1242</span></span>                 |
| <span data-ttu-id="c2c05-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c2c05-119">System-Id-Guid</span></span>    | <span data-ttu-id="c2c05-120">2df90d86-009F -11d2-aa4c-00c04f d83a</span><span class="sxs-lookup"><span data-stu-id="c2c05-120">2df90d86-009f-11d2-aa4c-00c04fd7d83a</span></span>    |
| <span data-ttu-id="c2c05-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2c05-121">Syntax</span></span>            | [<span data-ttu-id="c2c05-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c2c05-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c2c05-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="c2c05-123">Implementations</span></span>

-   [<span data-ttu-id="c2c05-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c2c05-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c2c05-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c2c05-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c2c05-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c2c05-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c2c05-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c2c05-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c2c05-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c2c05-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c2c05-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c2c05-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c2c05-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c2c05-130">Windows 2000 Server</span></span>



| <span data-ttu-id="c2c05-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c2c05-131">Entry</span></span> | <span data-ttu-id="c2c05-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c2c05-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c2c05-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c2c05-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c2c05-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2c05-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c2c05-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2c05-135">System-Only</span></span>            | <span data-ttu-id="c2c05-136">Richtig</span><span class="sxs-lookup"><span data-stu-id="c2c05-136">True</span></span>                                                               |
| <span data-ttu-id="c2c05-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c2c05-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c2c05-138">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-138">False</span></span>                                                              |
| <span data-ttu-id="c2c05-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c2c05-139">Is Indexed</span></span>             | <span data-ttu-id="c2c05-140">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-140">False</span></span>                                                              |
| <span data-ttu-id="c2c05-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c2c05-141">In Global Catalog</span></span>      | <span data-ttu-id="c2c05-142">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-142">False</span></span>                                                              |
| <span data-ttu-id="c2c05-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c2c05-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2c05-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c2c05-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c2c05-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2c05-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="c2c05-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2c05-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="c2c05-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2c05-147">Search-Flags</span></span>           | <span data-ttu-id="c2c05-148">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c2c05-148">0x00000008</span></span>                                                         |
| <span data-ttu-id="c2c05-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2c05-149">System-Flags</span></span>           | <span data-ttu-id="c2c05-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2c05-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="c2c05-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c2c05-151">Classes used in</span></span>        | [<span data-ttu-id="c2c05-152">**Infrastruktur-aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="c2c05-152">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c2c05-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c2c05-153">Windows Server 2003</span></span>



| <span data-ttu-id="c2c05-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c2c05-154">Entry</span></span> | <span data-ttu-id="c2c05-155">Wert</span><span class="sxs-lookup"><span data-stu-id="c2c05-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c2c05-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c2c05-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c2c05-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2c05-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c2c05-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2c05-158">System-Only</span></span>            | <span data-ttu-id="c2c05-159">Richtig</span><span class="sxs-lookup"><span data-stu-id="c2c05-159">True</span></span>                                                               |
| <span data-ttu-id="c2c05-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c2c05-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c2c05-161">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-161">False</span></span>                                                              |
| <span data-ttu-id="c2c05-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c2c05-162">Is Indexed</span></span>             | <span data-ttu-id="c2c05-163">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-163">False</span></span>                                                              |
| <span data-ttu-id="c2c05-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c2c05-164">In Global Catalog</span></span>      | <span data-ttu-id="c2c05-165">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-165">False</span></span>                                                              |
| <span data-ttu-id="c2c05-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c2c05-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2c05-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c2c05-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c2c05-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2c05-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="c2c05-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2c05-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="c2c05-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2c05-170">Search-Flags</span></span>           | <span data-ttu-id="c2c05-171">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c2c05-171">0x00000008</span></span>                                                         |
| <span data-ttu-id="c2c05-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2c05-172">System-Flags</span></span>           | <span data-ttu-id="c2c05-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2c05-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="c2c05-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c2c05-174">Classes used in</span></span>        | [<span data-ttu-id="c2c05-175">**Infrastruktur-aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="c2c05-175">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c2c05-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c2c05-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c2c05-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c2c05-177">Entry</span></span> | <span data-ttu-id="c2c05-178">Wert</span><span class="sxs-lookup"><span data-stu-id="c2c05-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c2c05-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c2c05-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c2c05-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2c05-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c2c05-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2c05-181">System-Only</span></span>            | <span data-ttu-id="c2c05-182">Richtig</span><span class="sxs-lookup"><span data-stu-id="c2c05-182">True</span></span>                                                               |
| <span data-ttu-id="c2c05-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c2c05-183">Is-Single-Valued</span></span>       | <span data-ttu-id="c2c05-184">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-184">False</span></span>                                                              |
| <span data-ttu-id="c2c05-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c2c05-185">Is Indexed</span></span>             | <span data-ttu-id="c2c05-186">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-186">False</span></span>                                                              |
| <span data-ttu-id="c2c05-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c2c05-187">In Global Catalog</span></span>      | <span data-ttu-id="c2c05-188">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-188">False</span></span>                                                              |
| <span data-ttu-id="c2c05-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c2c05-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2c05-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c2c05-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c2c05-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2c05-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="c2c05-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2c05-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="c2c05-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2c05-193">Search-Flags</span></span>           | <span data-ttu-id="c2c05-194">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c2c05-194">0x00000008</span></span>                                                         |
| <span data-ttu-id="c2c05-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2c05-195">System-Flags</span></span>           | <span data-ttu-id="c2c05-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2c05-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="c2c05-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c2c05-197">Classes used in</span></span>        | [<span data-ttu-id="c2c05-198">**Infrastruktur-aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="c2c05-198">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c2c05-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2c05-199">Windows Server 2008</span></span>



| <span data-ttu-id="c2c05-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c2c05-200">Entry</span></span> | <span data-ttu-id="c2c05-201">Wert</span><span class="sxs-lookup"><span data-stu-id="c2c05-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c2c05-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c2c05-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c2c05-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2c05-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c2c05-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2c05-204">System-Only</span></span>            | <span data-ttu-id="c2c05-205">Richtig</span><span class="sxs-lookup"><span data-stu-id="c2c05-205">True</span></span>                                                               |
| <span data-ttu-id="c2c05-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c2c05-206">Is-Single-Valued</span></span>       | <span data-ttu-id="c2c05-207">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-207">False</span></span>                                                              |
| <span data-ttu-id="c2c05-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c2c05-208">Is Indexed</span></span>             | <span data-ttu-id="c2c05-209">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-209">False</span></span>                                                              |
| <span data-ttu-id="c2c05-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c2c05-210">In Global Catalog</span></span>      | <span data-ttu-id="c2c05-211">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-211">False</span></span>                                                              |
| <span data-ttu-id="c2c05-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c2c05-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2c05-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c2c05-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c2c05-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2c05-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="c2c05-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2c05-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="c2c05-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2c05-216">Search-Flags</span></span>           | <span data-ttu-id="c2c05-217">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c2c05-217">0x00000008</span></span>                                                         |
| <span data-ttu-id="c2c05-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2c05-218">System-Flags</span></span>           | <span data-ttu-id="c2c05-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2c05-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="c2c05-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c2c05-220">Classes used in</span></span>        | [<span data-ttu-id="c2c05-221">**Infrastruktur-aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="c2c05-221">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c2c05-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2c05-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c2c05-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c2c05-223">Entry</span></span> | <span data-ttu-id="c2c05-224">Wert</span><span class="sxs-lookup"><span data-stu-id="c2c05-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c2c05-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c2c05-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c2c05-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2c05-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c2c05-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2c05-227">System-Only</span></span>            | <span data-ttu-id="c2c05-228">Richtig</span><span class="sxs-lookup"><span data-stu-id="c2c05-228">True</span></span>                                                               |
| <span data-ttu-id="c2c05-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c2c05-229">Is-Single-Valued</span></span>       | <span data-ttu-id="c2c05-230">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-230">False</span></span>                                                              |
| <span data-ttu-id="c2c05-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c2c05-231">Is Indexed</span></span>             | <span data-ttu-id="c2c05-232">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-232">False</span></span>                                                              |
| <span data-ttu-id="c2c05-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c2c05-233">In Global Catalog</span></span>      | <span data-ttu-id="c2c05-234">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-234">False</span></span>                                                              |
| <span data-ttu-id="c2c05-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c2c05-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2c05-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c2c05-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c2c05-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2c05-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="c2c05-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2c05-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="c2c05-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2c05-239">Search-Flags</span></span>           | <span data-ttu-id="c2c05-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c2c05-240">0x00000008</span></span>                                                         |
| <span data-ttu-id="c2c05-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2c05-241">System-Flags</span></span>           | <span data-ttu-id="c2c05-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2c05-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="c2c05-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c2c05-243">Classes used in</span></span>        | [<span data-ttu-id="c2c05-244">**Infrastruktur-aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="c2c05-244">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c2c05-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c2c05-245">Windows Server 2012</span></span>



| <span data-ttu-id="c2c05-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c2c05-246">Entry</span></span> | <span data-ttu-id="c2c05-247">Wert</span><span class="sxs-lookup"><span data-stu-id="c2c05-247">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c2c05-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c2c05-248">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c2c05-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2c05-249">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c2c05-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2c05-250">System-Only</span></span>            | <span data-ttu-id="c2c05-251">Richtig</span><span class="sxs-lookup"><span data-stu-id="c2c05-251">True</span></span>                                                               |
| <span data-ttu-id="c2c05-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c2c05-252">Is-Single-Valued</span></span>       | <span data-ttu-id="c2c05-253">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-253">False</span></span>                                                              |
| <span data-ttu-id="c2c05-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c2c05-254">Is Indexed</span></span>             | <span data-ttu-id="c2c05-255">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-255">False</span></span>                                                              |
| <span data-ttu-id="c2c05-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c2c05-256">In Global Catalog</span></span>      | <span data-ttu-id="c2c05-257">False</span><span class="sxs-lookup"><span data-stu-id="c2c05-257">False</span></span>                                                              |
| <span data-ttu-id="c2c05-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c2c05-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2c05-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c2c05-259">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c2c05-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2c05-260">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="c2c05-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2c05-261">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="c2c05-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2c05-262">Search-Flags</span></span>           | <span data-ttu-id="c2c05-263">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c2c05-263">0x00000008</span></span>                                                         |
| <span data-ttu-id="c2c05-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2c05-264">System-Flags</span></span>           | <span data-ttu-id="c2c05-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2c05-265">0x00000010</span></span>                                                         |
| <span data-ttu-id="c2c05-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c2c05-266">Classes used in</span></span>        | [<span data-ttu-id="c2c05-267">**Infrastruktur-aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="c2c05-267">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



 

 





