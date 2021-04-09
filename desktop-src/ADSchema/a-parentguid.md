---
title: Parent-GUID-Attribut
description: Dies ist ein konstruiertes Attribut, das zur Unterstützung des Dirsync-Steuer Elements erfunden wurde. Dieses Attribut enthält die objectGUID des übergeordneten Elements eines Objekts beim Replizieren der Erstellung, Umbenennung oder Verschiebung eines Objekts.
ms.assetid: caf2491b-c0bf-4ea1-80ec-d44cf9307551
ms.tgt_platform: multiple
keywords:
- AD-Schema für Parent-GUID-Attribut
- cschema für das Attribut "parametriguid"
topic_type:
- apiref
api_name:
- Parent-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b01faf958f4add9c7788d630321d7c225f5026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859784"
---
# <a name="parent-guid-attribute"></a><span data-ttu-id="28a00-106">Parent-GUID-Attribut</span><span class="sxs-lookup"><span data-stu-id="28a00-106">Parent-GUID attribute</span></span>

<span data-ttu-id="28a00-107">Dies ist ein konstruiertes Attribut, das zur Unterstützung des Dirsync-Steuer Elements erfunden wurde.</span><span class="sxs-lookup"><span data-stu-id="28a00-107">This is a constructed attribute, invented to support the DirSync control.</span></span> <span data-ttu-id="28a00-108">Dieses Attribut enthält die objectGUID des übergeordneten Elements eines Objekts beim Replizieren der Erstellung, Umbenennung oder Verschiebung eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="28a00-108">This attribute holds the objectGuid of an object's parent when replicating an object's creation, rename, or move.</span></span>



| <span data-ttu-id="28a00-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="28a00-109">Entry</span></span> | <span data-ttu-id="28a00-110">Wert</span><span class="sxs-lookup"><span data-stu-id="28a00-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="28a00-111">CN</span><span class="sxs-lookup"><span data-stu-id="28a00-111">CN</span></span>                | <span data-ttu-id="28a00-112">Parent-GUID</span><span class="sxs-lookup"><span data-stu-id="28a00-112">Parent-GUID</span></span>                                           |
| <span data-ttu-id="28a00-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="28a00-113">Ldap-Display-Name</span></span> | <span data-ttu-id="28a00-114">parametriguid</span><span class="sxs-lookup"><span data-stu-id="28a00-114">parentGUID</span></span>                                            |
| <span data-ttu-id="28a00-115">Size</span><span class="sxs-lookup"><span data-stu-id="28a00-115">Size</span></span>              | <span data-ttu-id="28a00-116">16 Bytes</span><span class="sxs-lookup"><span data-stu-id="28a00-116">16 bytes</span></span>                                              |
| <span data-ttu-id="28a00-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="28a00-117">Update Privilege</span></span>  | <span data-ttu-id="28a00-118">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="28a00-118">This value is set by the system.</span></span>                      |
| <span data-ttu-id="28a00-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="28a00-119">Update Frequency</span></span>  | <span data-ttu-id="28a00-120">Während der Replikation</span><span class="sxs-lookup"><span data-stu-id="28a00-120">During replication</span></span>                                    |
| <span data-ttu-id="28a00-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="28a00-121">Attribute-Id</span></span>      | <span data-ttu-id="28a00-122">1.2.840.113556.1.4.1224</span><span class="sxs-lookup"><span data-stu-id="28a00-122">1.2.840.113556.1.4.1224</span></span>                               |
| <span data-ttu-id="28a00-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="28a00-123">System-Id-Guid</span></span>    | <span data-ttu-id="28a00-124">2df90d74-009F -11d2-aa4c-00c04f d83a</span><span class="sxs-lookup"><span data-stu-id="28a00-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span></span>                  |
| <span data-ttu-id="28a00-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="28a00-125">Syntax</span></span>            | [<span data-ttu-id="28a00-126">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="28a00-126">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="28a00-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="28a00-127">Implementations</span></span>

-   [<span data-ttu-id="28a00-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="28a00-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="28a00-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="28a00-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="28a00-130">**Adam**</span><span class="sxs-lookup"><span data-stu-id="28a00-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="28a00-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="28a00-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="28a00-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="28a00-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="28a00-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="28a00-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="28a00-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="28a00-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="28a00-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28a00-135">Windows 2000 Server</span></span>



| <span data-ttu-id="28a00-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="28a00-136">Entry</span></span> | <span data-ttu-id="28a00-137">Wert</span><span class="sxs-lookup"><span data-stu-id="28a00-137">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="28a00-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="28a00-138">Link-Id</span></span>                | \-           |
| <span data-ttu-id="28a00-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28a00-139">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="28a00-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="28a00-140">System-Only</span></span>            | <span data-ttu-id="28a00-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="28a00-141">True</span></span>         |
| <span data-ttu-id="28a00-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="28a00-142">Is-Single-Valued</span></span>       | <span data-ttu-id="28a00-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="28a00-143">True</span></span>         |
| <span data-ttu-id="28a00-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="28a00-144">Is Indexed</span></span>             | <span data-ttu-id="28a00-145">False</span><span class="sxs-lookup"><span data-stu-id="28a00-145">False</span></span>        |
| <span data-ttu-id="28a00-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="28a00-146">In Global Catalog</span></span>      | <span data-ttu-id="28a00-147">False</span><span class="sxs-lookup"><span data-stu-id="28a00-147">False</span></span>        |
| <span data-ttu-id="28a00-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28a00-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="28a00-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="28a00-149">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="28a00-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28a00-150">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="28a00-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28a00-151">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="28a00-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28a00-152">Search-Flags</span></span>           | <span data-ttu-id="28a00-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28a00-153">0x00000000</span></span>   |
| <span data-ttu-id="28a00-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28a00-154">System-Flags</span></span>           | <span data-ttu-id="28a00-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="28a00-155">0x08000014</span></span>   |
| <span data-ttu-id="28a00-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="28a00-156">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="28a00-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="28a00-157">Windows Server 2003</span></span>



| <span data-ttu-id="28a00-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="28a00-158">Entry</span></span> | <span data-ttu-id="28a00-159">Wert</span><span class="sxs-lookup"><span data-stu-id="28a00-159">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="28a00-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="28a00-160">Link-Id</span></span>                | \-           |
| <span data-ttu-id="28a00-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28a00-161">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="28a00-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="28a00-162">System-Only</span></span>            | <span data-ttu-id="28a00-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="28a00-163">True</span></span>         |
| <span data-ttu-id="28a00-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="28a00-164">Is-Single-Valued</span></span>       | <span data-ttu-id="28a00-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="28a00-165">True</span></span>         |
| <span data-ttu-id="28a00-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="28a00-166">Is Indexed</span></span>             | <span data-ttu-id="28a00-167">False</span><span class="sxs-lookup"><span data-stu-id="28a00-167">False</span></span>        |
| <span data-ttu-id="28a00-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="28a00-168">In Global Catalog</span></span>      | <span data-ttu-id="28a00-169">False</span><span class="sxs-lookup"><span data-stu-id="28a00-169">False</span></span>        |
| <span data-ttu-id="28a00-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28a00-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="28a00-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="28a00-171">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="28a00-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28a00-172">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="28a00-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28a00-173">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="28a00-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28a00-174">Search-Flags</span></span>           | <span data-ttu-id="28a00-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28a00-175">0x00000000</span></span>   |
| <span data-ttu-id="28a00-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28a00-176">System-Flags</span></span>           | <span data-ttu-id="28a00-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="28a00-177">0x08000014</span></span>   |
| <span data-ttu-id="28a00-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="28a00-178">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="28a00-179">Adam</span><span class="sxs-lookup"><span data-stu-id="28a00-179">ADAM</span></span>



| <span data-ttu-id="28a00-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="28a00-180">Entry</span></span> | <span data-ttu-id="28a00-181">Wert</span><span class="sxs-lookup"><span data-stu-id="28a00-181">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="28a00-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="28a00-182">Link-Id</span></span>                | \-           |
| <span data-ttu-id="28a00-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28a00-183">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="28a00-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="28a00-184">System-Only</span></span>            | <span data-ttu-id="28a00-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="28a00-185">True</span></span>         |
| <span data-ttu-id="28a00-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="28a00-186">Is-Single-Valued</span></span>       | <span data-ttu-id="28a00-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="28a00-187">True</span></span>         |
| <span data-ttu-id="28a00-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="28a00-188">Is Indexed</span></span>             | <span data-ttu-id="28a00-189">False</span><span class="sxs-lookup"><span data-stu-id="28a00-189">False</span></span>        |
| <span data-ttu-id="28a00-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="28a00-190">In Global Catalog</span></span>      | <span data-ttu-id="28a00-191">False</span><span class="sxs-lookup"><span data-stu-id="28a00-191">False</span></span>        |
| <span data-ttu-id="28a00-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28a00-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="28a00-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="28a00-193">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="28a00-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28a00-194">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="28a00-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28a00-195">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="28a00-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28a00-196">Search-Flags</span></span>           | <span data-ttu-id="28a00-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28a00-197">0x00000000</span></span>   |
| <span data-ttu-id="28a00-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28a00-198">System-Flags</span></span>           | <span data-ttu-id="28a00-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="28a00-199">0x08000014</span></span>   |
| <span data-ttu-id="28a00-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="28a00-200">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="28a00-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="28a00-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="28a00-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="28a00-202">Entry</span></span> | <span data-ttu-id="28a00-203">Wert</span><span class="sxs-lookup"><span data-stu-id="28a00-203">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="28a00-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="28a00-204">Link-Id</span></span>                | \-           |
| <span data-ttu-id="28a00-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28a00-205">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="28a00-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="28a00-206">System-Only</span></span>            | <span data-ttu-id="28a00-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="28a00-207">True</span></span>         |
| <span data-ttu-id="28a00-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="28a00-208">Is-Single-Valued</span></span>       | <span data-ttu-id="28a00-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="28a00-209">True</span></span>         |
| <span data-ttu-id="28a00-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="28a00-210">Is Indexed</span></span>             | <span data-ttu-id="28a00-211">False</span><span class="sxs-lookup"><span data-stu-id="28a00-211">False</span></span>        |
| <span data-ttu-id="28a00-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="28a00-212">In Global Catalog</span></span>      | <span data-ttu-id="28a00-213">False</span><span class="sxs-lookup"><span data-stu-id="28a00-213">False</span></span>        |
| <span data-ttu-id="28a00-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28a00-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="28a00-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="28a00-215">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="28a00-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28a00-216">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="28a00-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28a00-217">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="28a00-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28a00-218">Search-Flags</span></span>           | <span data-ttu-id="28a00-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28a00-219">0x00000000</span></span>   |
| <span data-ttu-id="28a00-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28a00-220">System-Flags</span></span>           | <span data-ttu-id="28a00-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="28a00-221">0x08000014</span></span>   |
| <span data-ttu-id="28a00-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="28a00-222">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="28a00-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28a00-223">Windows Server 2008</span></span>



| <span data-ttu-id="28a00-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="28a00-224">Entry</span></span> | <span data-ttu-id="28a00-225">Wert</span><span class="sxs-lookup"><span data-stu-id="28a00-225">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="28a00-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="28a00-226">Link-Id</span></span>                | \-           |
| <span data-ttu-id="28a00-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28a00-227">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="28a00-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="28a00-228">System-Only</span></span>            | <span data-ttu-id="28a00-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="28a00-229">True</span></span>         |
| <span data-ttu-id="28a00-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="28a00-230">Is-Single-Valued</span></span>       | <span data-ttu-id="28a00-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="28a00-231">True</span></span>         |
| <span data-ttu-id="28a00-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="28a00-232">Is Indexed</span></span>             | <span data-ttu-id="28a00-233">False</span><span class="sxs-lookup"><span data-stu-id="28a00-233">False</span></span>        |
| <span data-ttu-id="28a00-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="28a00-234">In Global Catalog</span></span>      | <span data-ttu-id="28a00-235">False</span><span class="sxs-lookup"><span data-stu-id="28a00-235">False</span></span>        |
| <span data-ttu-id="28a00-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28a00-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="28a00-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="28a00-237">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="28a00-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28a00-238">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="28a00-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28a00-239">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="28a00-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28a00-240">Search-Flags</span></span>           | <span data-ttu-id="28a00-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28a00-241">0x00000000</span></span>   |
| <span data-ttu-id="28a00-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28a00-242">System-Flags</span></span>           | <span data-ttu-id="28a00-243">0x08000014</span><span class="sxs-lookup"><span data-stu-id="28a00-243">0x08000014</span></span>   |
| <span data-ttu-id="28a00-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="28a00-244">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="28a00-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="28a00-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="28a00-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="28a00-246">Entry</span></span> | <span data-ttu-id="28a00-247">Wert</span><span class="sxs-lookup"><span data-stu-id="28a00-247">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="28a00-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="28a00-248">Link-Id</span></span>                | \-           |
| <span data-ttu-id="28a00-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28a00-249">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="28a00-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="28a00-250">System-Only</span></span>            | <span data-ttu-id="28a00-251">Richtig</span><span class="sxs-lookup"><span data-stu-id="28a00-251">True</span></span>         |
| <span data-ttu-id="28a00-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="28a00-252">Is-Single-Valued</span></span>       | <span data-ttu-id="28a00-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="28a00-253">True</span></span>         |
| <span data-ttu-id="28a00-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="28a00-254">Is Indexed</span></span>             | <span data-ttu-id="28a00-255">False</span><span class="sxs-lookup"><span data-stu-id="28a00-255">False</span></span>        |
| <span data-ttu-id="28a00-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="28a00-256">In Global Catalog</span></span>      | <span data-ttu-id="28a00-257">False</span><span class="sxs-lookup"><span data-stu-id="28a00-257">False</span></span>        |
| <span data-ttu-id="28a00-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28a00-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="28a00-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="28a00-259">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="28a00-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28a00-260">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="28a00-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28a00-261">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="28a00-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28a00-262">Search-Flags</span></span>           | <span data-ttu-id="28a00-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28a00-263">0x00000000</span></span>   |
| <span data-ttu-id="28a00-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28a00-264">System-Flags</span></span>           | <span data-ttu-id="28a00-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="28a00-265">0x08000014</span></span>   |
| <span data-ttu-id="28a00-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="28a00-266">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="28a00-267">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="28a00-267">Windows Server 2012</span></span>



| <span data-ttu-id="28a00-268">Eingabe</span><span class="sxs-lookup"><span data-stu-id="28a00-268">Entry</span></span> | <span data-ttu-id="28a00-269">Wert</span><span class="sxs-lookup"><span data-stu-id="28a00-269">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="28a00-270">Link-ID</span><span class="sxs-lookup"><span data-stu-id="28a00-270">Link-Id</span></span>                | \-           |
| <span data-ttu-id="28a00-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28a00-271">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="28a00-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="28a00-272">System-Only</span></span>            | <span data-ttu-id="28a00-273">Richtig</span><span class="sxs-lookup"><span data-stu-id="28a00-273">True</span></span>         |
| <span data-ttu-id="28a00-274">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="28a00-274">Is-Single-Valued</span></span>       | <span data-ttu-id="28a00-275">Richtig</span><span class="sxs-lookup"><span data-stu-id="28a00-275">True</span></span>         |
| <span data-ttu-id="28a00-276">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="28a00-276">Is Indexed</span></span>             | <span data-ttu-id="28a00-277">False</span><span class="sxs-lookup"><span data-stu-id="28a00-277">False</span></span>        |
| <span data-ttu-id="28a00-278">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="28a00-278">In Global Catalog</span></span>      | <span data-ttu-id="28a00-279">False</span><span class="sxs-lookup"><span data-stu-id="28a00-279">False</span></span>        |
| <span data-ttu-id="28a00-280">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28a00-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="28a00-281">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="28a00-281">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="28a00-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28a00-282">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="28a00-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28a00-283">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="28a00-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28a00-284">Search-Flags</span></span>           | <span data-ttu-id="28a00-285">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28a00-285">0x00000000</span></span>   |
| <span data-ttu-id="28a00-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28a00-286">System-Flags</span></span>           | <span data-ttu-id="28a00-287">0x08000014</span><span class="sxs-lookup"><span data-stu-id="28a00-287">0x08000014</span></span>   |
| <span data-ttu-id="28a00-288">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="28a00-288">Classes used in</span></span>        | \-           |



 

 




