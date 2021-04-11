---
title: Sync-with-SID-Attribut
description: Für das Objekt "Sam Builtin Group"/"lokale Richtlinie" ist dies die lokale Gruppe, der ein Objekt entspricht.
ms.assetid: b983210d-1c54-4355-bc37-771e51016175
ms.tgt_platform: multiple
keywords:
- AD-Schema für Sync-with-SID-Attribut
- AD-Schema des syncwithsid-Attributs
topic_type:
- apiref
api_name:
- Sync-With-SID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 845a95b737a56a853fa7fb4e77d5612f1efc3c37
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122654"
---
# <a name="sync-with-sid-attribute"></a><span data-ttu-id="8f36d-105">Sync-with-SID-Attribut</span><span class="sxs-lookup"><span data-stu-id="8f36d-105">Sync-With-SID attribute</span></span>

<span data-ttu-id="8f36d-106">Für das Objekt "Sam Builtin Group"/"lokale Richtlinie" ist dies die lokale Gruppe, der ein Objekt entspricht.</span><span class="sxs-lookup"><span data-stu-id="8f36d-106">For the SAM builtin group object/ local policy synchronization, this is the local group to which an object corresponds.</span></span>



| <span data-ttu-id="8f36d-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8f36d-107">Entry</span></span> | <span data-ttu-id="8f36d-108">Wert</span><span class="sxs-lookup"><span data-stu-id="8f36d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8f36d-109">CN</span><span class="sxs-lookup"><span data-stu-id="8f36d-109">CN</span></span>                | <span data-ttu-id="8f36d-110">Sync-with-sid</span><span class="sxs-lookup"><span data-stu-id="8f36d-110">Sync-With-SID</span></span>                        |
| <span data-ttu-id="8f36d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8f36d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8f36d-112">syncwithsid</span><span class="sxs-lookup"><span data-stu-id="8f36d-112">syncWithSID</span></span>                          |
| <span data-ttu-id="8f36d-113">Size</span><span class="sxs-lookup"><span data-stu-id="8f36d-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="8f36d-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="8f36d-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="8f36d-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="8f36d-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8f36d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8f36d-116">Attribute-Id</span></span>      | <span data-ttu-id="8f36d-117">1.2.840.113556.1.4.667</span><span class="sxs-lookup"><span data-stu-id="8f36d-117">1.2.840.113556.1.4.667</span></span>               |
| <span data-ttu-id="8f36d-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8f36d-118">System-Id-Guid</span></span>    | <span data-ttu-id="8f36d-119">037651e5-441d-11d1-a9c3-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="8f36d-119">037651e5-441d-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="8f36d-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f36d-120">Syntax</span></span>            | [<span data-ttu-id="8f36d-121">**Zeichenfolge (SID)**</span><span class="sxs-lookup"><span data-stu-id="8f36d-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="8f36d-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="8f36d-122">Implementations</span></span>

-   [<span data-ttu-id="8f36d-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8f36d-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8f36d-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8f36d-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8f36d-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8f36d-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8f36d-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8f36d-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8f36d-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8f36d-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8f36d-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8f36d-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8f36d-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8f36d-129">Windows 2000 Server</span></span>



| <span data-ttu-id="8f36d-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8f36d-130">Entry</span></span> | <span data-ttu-id="8f36d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="8f36d-131">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="8f36d-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8f36d-132">Link-Id</span></span>                | \-           |
| <span data-ttu-id="8f36d-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f36d-133">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="8f36d-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f36d-134">System-Only</span></span>            | <span data-ttu-id="8f36d-135">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-135">False</span></span>        |
| <span data-ttu-id="8f36d-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8f36d-136">Is-Single-Valued</span></span>       | <span data-ttu-id="8f36d-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="8f36d-137">True</span></span>         |
| <span data-ttu-id="8f36d-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8f36d-138">Is Indexed</span></span>             | <span data-ttu-id="8f36d-139">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-139">False</span></span>        |
| <span data-ttu-id="8f36d-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8f36d-140">In Global Catalog</span></span>      | <span data-ttu-id="8f36d-141">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-141">False</span></span>        |
| <span data-ttu-id="8f36d-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8f36d-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f36d-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8f36d-143">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="8f36d-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f36d-144">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="8f36d-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f36d-145">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="8f36d-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f36d-146">Search-Flags</span></span>           | <span data-ttu-id="8f36d-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f36d-147">0x00000000</span></span>   |
| <span data-ttu-id="8f36d-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f36d-148">System-Flags</span></span>           | <span data-ttu-id="8f36d-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f36d-149">0x00000010</span></span>   |
| <span data-ttu-id="8f36d-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8f36d-150">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="8f36d-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f36d-151">Windows Server 2003</span></span>



| <span data-ttu-id="8f36d-152">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8f36d-152">Entry</span></span> | <span data-ttu-id="8f36d-153">Wert</span><span class="sxs-lookup"><span data-stu-id="8f36d-153">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="8f36d-154">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8f36d-154">Link-Id</span></span>                | \-           |
| <span data-ttu-id="8f36d-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f36d-155">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="8f36d-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f36d-156">System-Only</span></span>            | <span data-ttu-id="8f36d-157">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-157">False</span></span>        |
| <span data-ttu-id="8f36d-158">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8f36d-158">Is-Single-Valued</span></span>       | <span data-ttu-id="8f36d-159">Richtig</span><span class="sxs-lookup"><span data-stu-id="8f36d-159">True</span></span>         |
| <span data-ttu-id="8f36d-160">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8f36d-160">Is Indexed</span></span>             | <span data-ttu-id="8f36d-161">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-161">False</span></span>        |
| <span data-ttu-id="8f36d-162">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8f36d-162">In Global Catalog</span></span>      | <span data-ttu-id="8f36d-163">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-163">False</span></span>        |
| <span data-ttu-id="8f36d-164">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8f36d-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f36d-165">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8f36d-165">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="8f36d-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f36d-166">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="8f36d-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f36d-167">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="8f36d-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f36d-168">Search-Flags</span></span>           | <span data-ttu-id="8f36d-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f36d-169">0x00000000</span></span>   |
| <span data-ttu-id="8f36d-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f36d-170">System-Flags</span></span>           | <span data-ttu-id="8f36d-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f36d-171">0x00000010</span></span>   |
| <span data-ttu-id="8f36d-172">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8f36d-172">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8f36d-173">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8f36d-173">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8f36d-174">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8f36d-174">Entry</span></span> | <span data-ttu-id="8f36d-175">Wert</span><span class="sxs-lookup"><span data-stu-id="8f36d-175">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="8f36d-176">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8f36d-176">Link-Id</span></span>                | \-           |
| <span data-ttu-id="8f36d-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f36d-177">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="8f36d-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f36d-178">System-Only</span></span>            | <span data-ttu-id="8f36d-179">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-179">False</span></span>        |
| <span data-ttu-id="8f36d-180">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8f36d-180">Is-Single-Valued</span></span>       | <span data-ttu-id="8f36d-181">Richtig</span><span class="sxs-lookup"><span data-stu-id="8f36d-181">True</span></span>         |
| <span data-ttu-id="8f36d-182">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8f36d-182">Is Indexed</span></span>             | <span data-ttu-id="8f36d-183">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-183">False</span></span>        |
| <span data-ttu-id="8f36d-184">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8f36d-184">In Global Catalog</span></span>      | <span data-ttu-id="8f36d-185">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-185">False</span></span>        |
| <span data-ttu-id="8f36d-186">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8f36d-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f36d-187">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8f36d-187">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="8f36d-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f36d-188">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="8f36d-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f36d-189">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="8f36d-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f36d-190">Search-Flags</span></span>           | <span data-ttu-id="8f36d-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f36d-191">0x00000000</span></span>   |
| <span data-ttu-id="8f36d-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f36d-192">System-Flags</span></span>           | <span data-ttu-id="8f36d-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f36d-193">0x00000010</span></span>   |
| <span data-ttu-id="8f36d-194">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8f36d-194">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="8f36d-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f36d-195">Windows Server 2008</span></span>



| <span data-ttu-id="8f36d-196">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8f36d-196">Entry</span></span> | <span data-ttu-id="8f36d-197">Wert</span><span class="sxs-lookup"><span data-stu-id="8f36d-197">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="8f36d-198">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8f36d-198">Link-Id</span></span>                | \-           |
| <span data-ttu-id="8f36d-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f36d-199">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="8f36d-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f36d-200">System-Only</span></span>            | <span data-ttu-id="8f36d-201">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-201">False</span></span>        |
| <span data-ttu-id="8f36d-202">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8f36d-202">Is-Single-Valued</span></span>       | <span data-ttu-id="8f36d-203">Richtig</span><span class="sxs-lookup"><span data-stu-id="8f36d-203">True</span></span>         |
| <span data-ttu-id="8f36d-204">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8f36d-204">Is Indexed</span></span>             | <span data-ttu-id="8f36d-205">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-205">False</span></span>        |
| <span data-ttu-id="8f36d-206">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8f36d-206">In Global Catalog</span></span>      | <span data-ttu-id="8f36d-207">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-207">False</span></span>        |
| <span data-ttu-id="8f36d-208">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8f36d-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f36d-209">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8f36d-209">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="8f36d-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f36d-210">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="8f36d-211">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f36d-211">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="8f36d-212">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f36d-212">Search-Flags</span></span>           | <span data-ttu-id="8f36d-213">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f36d-213">0x00000000</span></span>   |
| <span data-ttu-id="8f36d-214">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f36d-214">System-Flags</span></span>           | <span data-ttu-id="8f36d-215">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f36d-215">0x00000010</span></span>   |
| <span data-ttu-id="8f36d-216">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8f36d-216">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8f36d-217">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8f36d-217">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8f36d-218">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8f36d-218">Entry</span></span> | <span data-ttu-id="8f36d-219">Wert</span><span class="sxs-lookup"><span data-stu-id="8f36d-219">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="8f36d-220">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8f36d-220">Link-Id</span></span>                | \-           |
| <span data-ttu-id="8f36d-221">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f36d-221">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="8f36d-222">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f36d-222">System-Only</span></span>            | <span data-ttu-id="8f36d-223">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-223">False</span></span>        |
| <span data-ttu-id="8f36d-224">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8f36d-224">Is-Single-Valued</span></span>       | <span data-ttu-id="8f36d-225">Richtig</span><span class="sxs-lookup"><span data-stu-id="8f36d-225">True</span></span>         |
| <span data-ttu-id="8f36d-226">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8f36d-226">Is Indexed</span></span>             | <span data-ttu-id="8f36d-227">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-227">False</span></span>        |
| <span data-ttu-id="8f36d-228">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8f36d-228">In Global Catalog</span></span>      | <span data-ttu-id="8f36d-229">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-229">False</span></span>        |
| <span data-ttu-id="8f36d-230">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8f36d-230">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f36d-231">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8f36d-231">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="8f36d-232">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f36d-232">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="8f36d-233">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f36d-233">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="8f36d-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f36d-234">Search-Flags</span></span>           | <span data-ttu-id="8f36d-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f36d-235">0x00000000</span></span>   |
| <span data-ttu-id="8f36d-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f36d-236">System-Flags</span></span>           | <span data-ttu-id="8f36d-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f36d-237">0x00000010</span></span>   |
| <span data-ttu-id="8f36d-238">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8f36d-238">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="8f36d-239">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8f36d-239">Windows Server 2012</span></span>



| <span data-ttu-id="8f36d-240">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8f36d-240">Entry</span></span> | <span data-ttu-id="8f36d-241">Wert</span><span class="sxs-lookup"><span data-stu-id="8f36d-241">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="8f36d-242">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8f36d-242">Link-Id</span></span>                | \-           |
| <span data-ttu-id="8f36d-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f36d-243">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="8f36d-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f36d-244">System-Only</span></span>            | <span data-ttu-id="8f36d-245">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-245">False</span></span>        |
| <span data-ttu-id="8f36d-246">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8f36d-246">Is-Single-Valued</span></span>       | <span data-ttu-id="8f36d-247">Richtig</span><span class="sxs-lookup"><span data-stu-id="8f36d-247">True</span></span>         |
| <span data-ttu-id="8f36d-248">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8f36d-248">Is Indexed</span></span>             | <span data-ttu-id="8f36d-249">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-249">False</span></span>        |
| <span data-ttu-id="8f36d-250">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8f36d-250">In Global Catalog</span></span>      | <span data-ttu-id="8f36d-251">False</span><span class="sxs-lookup"><span data-stu-id="8f36d-251">False</span></span>        |
| <span data-ttu-id="8f36d-252">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8f36d-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f36d-253">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8f36d-253">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="8f36d-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f36d-254">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="8f36d-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f36d-255">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="8f36d-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f36d-256">Search-Flags</span></span>           | <span data-ttu-id="8f36d-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f36d-257">0x00000000</span></span>   |
| <span data-ttu-id="8f36d-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f36d-258">System-Flags</span></span>           | <span data-ttu-id="8f36d-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f36d-259">0x00000010</span></span>   |
| <span data-ttu-id="8f36d-260">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8f36d-260">Classes used in</span></span>        | \-           |



 

 




