---
title: Computer weites Richtlinien Attribut
description: Wird verwendet, um die Benutzer erweiterbare Richtlinie auf die Clients zu replizieren.
ms.assetid: e8ce40b8-7658-4e4b-b0e1-b68031811dd1
ms.tgt_platform: multiple
keywords:
- AD-Schema für das Computer weite Richtlinien Attribut
- machinewientpolicy-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Machine-Wide-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd3af77dfb501000369b3c4ae23b3f5f64f0da9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957374"
---
# <a name="machine-wide-policy-attribute"></a><span data-ttu-id="22f9f-105">Computer weites Richtlinien Attribut</span><span class="sxs-lookup"><span data-stu-id="22f9f-105">Machine-Wide-Policy attribute</span></span>

<span data-ttu-id="22f9f-106">Wird verwendet, um die Benutzer erweiterbare Richtlinie auf die Clients zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="22f9f-106">Used to replicate the user-extensible policy to the clients.</span></span>



| <span data-ttu-id="22f9f-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22f9f-107">Entry</span></span> | <span data-ttu-id="22f9f-108">Wert</span><span class="sxs-lookup"><span data-stu-id="22f9f-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="22f9f-109">CN</span><span class="sxs-lookup"><span data-stu-id="22f9f-109">CN</span></span>                | <span data-ttu-id="22f9f-110">Computer weite Richtlinie</span><span class="sxs-lookup"><span data-stu-id="22f9f-110">Machine-Wide-Policy</span></span>                                   |
| <span data-ttu-id="22f9f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="22f9f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="22f9f-112">machinewientpolicy</span><span class="sxs-lookup"><span data-stu-id="22f9f-112">machineWidePolicy</span></span>                                     |
| <span data-ttu-id="22f9f-113">Size</span><span class="sxs-lookup"><span data-stu-id="22f9f-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="22f9f-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="22f9f-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="22f9f-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="22f9f-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="22f9f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="22f9f-116">Attribute-Id</span></span>      | <span data-ttu-id="22f9f-117">1.2.840.113556.1.4.459</span><span class="sxs-lookup"><span data-stu-id="22f9f-117">1.2.840.113556.1.4.459</span></span>                                |
| <span data-ttu-id="22f9f-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="22f9f-118">System-Id-Guid</span></span>    | <span data-ttu-id="22f9f-119">80a67e4f -922-11D0-AFDD-00c04f-930c9</span><span class="sxs-lookup"><span data-stu-id="22f9f-119">80a67e4f-9f22-11d0-afdd-00c04fd930c9</span></span>                  |
| <span data-ttu-id="22f9f-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="22f9f-120">Syntax</span></span>            | [<span data-ttu-id="22f9f-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="22f9f-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="22f9f-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="22f9f-122">Implementations</span></span>

-   [<span data-ttu-id="22f9f-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="22f9f-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="22f9f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="22f9f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="22f9f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="22f9f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="22f9f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="22f9f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="22f9f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="22f9f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="22f9f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="22f9f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="22f9f-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="22f9f-129">Windows 2000 Server</span></span>



| <span data-ttu-id="22f9f-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22f9f-130">Entry</span></span> | <span data-ttu-id="22f9f-131">Wert</span><span class="sxs-lookup"><span data-stu-id="22f9f-131">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="22f9f-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="22f9f-132">Link-Id</span></span>                | \-           |
| <span data-ttu-id="22f9f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22f9f-133">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="22f9f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="22f9f-134">System-Only</span></span>            | <span data-ttu-id="22f9f-135">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-135">False</span></span>        |
| <span data-ttu-id="22f9f-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="22f9f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="22f9f-137">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-137">False</span></span>        |
| <span data-ttu-id="22f9f-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="22f9f-138">Is Indexed</span></span>             | <span data-ttu-id="22f9f-139">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-139">False</span></span>        |
| <span data-ttu-id="22f9f-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="22f9f-140">In Global Catalog</span></span>      | <span data-ttu-id="22f9f-141">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-141">False</span></span>        |
| <span data-ttu-id="22f9f-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22f9f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="22f9f-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="22f9f-143">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="22f9f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22f9f-144">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="22f9f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22f9f-145">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="22f9f-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22f9f-146">Search-Flags</span></span>           | <span data-ttu-id="22f9f-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22f9f-147">0x00000000</span></span>   |
| <span data-ttu-id="22f9f-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22f9f-148">System-Flags</span></span>           | <span data-ttu-id="22f9f-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22f9f-149">0x00000010</span></span>   |
| <span data-ttu-id="22f9f-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="22f9f-150">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="22f9f-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="22f9f-151">Windows Server 2003</span></span>



| <span data-ttu-id="22f9f-152">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22f9f-152">Entry</span></span> | <span data-ttu-id="22f9f-153">Wert</span><span class="sxs-lookup"><span data-stu-id="22f9f-153">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="22f9f-154">Link-ID</span><span class="sxs-lookup"><span data-stu-id="22f9f-154">Link-Id</span></span>                | \-           |
| <span data-ttu-id="22f9f-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22f9f-155">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="22f9f-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="22f9f-156">System-Only</span></span>            | <span data-ttu-id="22f9f-157">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-157">False</span></span>        |
| <span data-ttu-id="22f9f-158">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="22f9f-158">Is-Single-Valued</span></span>       | <span data-ttu-id="22f9f-159">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-159">False</span></span>        |
| <span data-ttu-id="22f9f-160">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="22f9f-160">Is Indexed</span></span>             | <span data-ttu-id="22f9f-161">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-161">False</span></span>        |
| <span data-ttu-id="22f9f-162">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="22f9f-162">In Global Catalog</span></span>      | <span data-ttu-id="22f9f-163">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-163">False</span></span>        |
| <span data-ttu-id="22f9f-164">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22f9f-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="22f9f-165">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="22f9f-165">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="22f9f-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22f9f-166">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="22f9f-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22f9f-167">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="22f9f-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22f9f-168">Search-Flags</span></span>           | <span data-ttu-id="22f9f-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22f9f-169">0x00000000</span></span>   |
| <span data-ttu-id="22f9f-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22f9f-170">System-Flags</span></span>           | <span data-ttu-id="22f9f-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22f9f-171">0x00000010</span></span>   |
| <span data-ttu-id="22f9f-172">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="22f9f-172">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="22f9f-173">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="22f9f-173">Windows Server 2003 R2</span></span>



| <span data-ttu-id="22f9f-174">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22f9f-174">Entry</span></span> | <span data-ttu-id="22f9f-175">Wert</span><span class="sxs-lookup"><span data-stu-id="22f9f-175">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="22f9f-176">Link-ID</span><span class="sxs-lookup"><span data-stu-id="22f9f-176">Link-Id</span></span>                | \-           |
| <span data-ttu-id="22f9f-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22f9f-177">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="22f9f-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="22f9f-178">System-Only</span></span>            | <span data-ttu-id="22f9f-179">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-179">False</span></span>        |
| <span data-ttu-id="22f9f-180">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="22f9f-180">Is-Single-Valued</span></span>       | <span data-ttu-id="22f9f-181">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-181">False</span></span>        |
| <span data-ttu-id="22f9f-182">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="22f9f-182">Is Indexed</span></span>             | <span data-ttu-id="22f9f-183">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-183">False</span></span>        |
| <span data-ttu-id="22f9f-184">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="22f9f-184">In Global Catalog</span></span>      | <span data-ttu-id="22f9f-185">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-185">False</span></span>        |
| <span data-ttu-id="22f9f-186">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22f9f-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="22f9f-187">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="22f9f-187">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="22f9f-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22f9f-188">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="22f9f-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22f9f-189">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="22f9f-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22f9f-190">Search-Flags</span></span>           | <span data-ttu-id="22f9f-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22f9f-191">0x00000000</span></span>   |
| <span data-ttu-id="22f9f-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22f9f-192">System-Flags</span></span>           | <span data-ttu-id="22f9f-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22f9f-193">0x00000010</span></span>   |
| <span data-ttu-id="22f9f-194">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="22f9f-194">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="22f9f-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22f9f-195">Windows Server 2008</span></span>



| <span data-ttu-id="22f9f-196">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22f9f-196">Entry</span></span> | <span data-ttu-id="22f9f-197">Wert</span><span class="sxs-lookup"><span data-stu-id="22f9f-197">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="22f9f-198">Link-ID</span><span class="sxs-lookup"><span data-stu-id="22f9f-198">Link-Id</span></span>                | \-           |
| <span data-ttu-id="22f9f-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22f9f-199">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="22f9f-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="22f9f-200">System-Only</span></span>            | <span data-ttu-id="22f9f-201">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-201">False</span></span>        |
| <span data-ttu-id="22f9f-202">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="22f9f-202">Is-Single-Valued</span></span>       | <span data-ttu-id="22f9f-203">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-203">False</span></span>        |
| <span data-ttu-id="22f9f-204">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="22f9f-204">Is Indexed</span></span>             | <span data-ttu-id="22f9f-205">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-205">False</span></span>        |
| <span data-ttu-id="22f9f-206">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="22f9f-206">In Global Catalog</span></span>      | <span data-ttu-id="22f9f-207">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-207">False</span></span>        |
| <span data-ttu-id="22f9f-208">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22f9f-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="22f9f-209">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="22f9f-209">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="22f9f-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22f9f-210">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="22f9f-211">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22f9f-211">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="22f9f-212">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22f9f-212">Search-Flags</span></span>           | <span data-ttu-id="22f9f-213">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22f9f-213">0x00000000</span></span>   |
| <span data-ttu-id="22f9f-214">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22f9f-214">System-Flags</span></span>           | <span data-ttu-id="22f9f-215">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22f9f-215">0x00000010</span></span>   |
| <span data-ttu-id="22f9f-216">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="22f9f-216">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="22f9f-217">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="22f9f-217">Windows Server 2008 R2</span></span>



| <span data-ttu-id="22f9f-218">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22f9f-218">Entry</span></span> | <span data-ttu-id="22f9f-219">Wert</span><span class="sxs-lookup"><span data-stu-id="22f9f-219">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="22f9f-220">Link-ID</span><span class="sxs-lookup"><span data-stu-id="22f9f-220">Link-Id</span></span>                | \-           |
| <span data-ttu-id="22f9f-221">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22f9f-221">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="22f9f-222">System-Only</span><span class="sxs-lookup"><span data-stu-id="22f9f-222">System-Only</span></span>            | <span data-ttu-id="22f9f-223">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-223">False</span></span>        |
| <span data-ttu-id="22f9f-224">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="22f9f-224">Is-Single-Valued</span></span>       | <span data-ttu-id="22f9f-225">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-225">False</span></span>        |
| <span data-ttu-id="22f9f-226">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="22f9f-226">Is Indexed</span></span>             | <span data-ttu-id="22f9f-227">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-227">False</span></span>        |
| <span data-ttu-id="22f9f-228">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="22f9f-228">In Global Catalog</span></span>      | <span data-ttu-id="22f9f-229">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-229">False</span></span>        |
| <span data-ttu-id="22f9f-230">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22f9f-230">NT-Security-Descriptor</span></span> | <span data-ttu-id="22f9f-231">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="22f9f-231">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="22f9f-232">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22f9f-232">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="22f9f-233">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22f9f-233">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="22f9f-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22f9f-234">Search-Flags</span></span>           | <span data-ttu-id="22f9f-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22f9f-235">0x00000000</span></span>   |
| <span data-ttu-id="22f9f-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22f9f-236">System-Flags</span></span>           | <span data-ttu-id="22f9f-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22f9f-237">0x00000010</span></span>   |
| <span data-ttu-id="22f9f-238">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="22f9f-238">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="22f9f-239">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="22f9f-239">Windows Server 2012</span></span>



| <span data-ttu-id="22f9f-240">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22f9f-240">Entry</span></span> | <span data-ttu-id="22f9f-241">Wert</span><span class="sxs-lookup"><span data-stu-id="22f9f-241">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="22f9f-242">Link-ID</span><span class="sxs-lookup"><span data-stu-id="22f9f-242">Link-Id</span></span>                | \-           |
| <span data-ttu-id="22f9f-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22f9f-243">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="22f9f-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="22f9f-244">System-Only</span></span>            | <span data-ttu-id="22f9f-245">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-245">False</span></span>        |
| <span data-ttu-id="22f9f-246">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="22f9f-246">Is-Single-Valued</span></span>       | <span data-ttu-id="22f9f-247">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-247">False</span></span>        |
| <span data-ttu-id="22f9f-248">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="22f9f-248">Is Indexed</span></span>             | <span data-ttu-id="22f9f-249">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-249">False</span></span>        |
| <span data-ttu-id="22f9f-250">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="22f9f-250">In Global Catalog</span></span>      | <span data-ttu-id="22f9f-251">False</span><span class="sxs-lookup"><span data-stu-id="22f9f-251">False</span></span>        |
| <span data-ttu-id="22f9f-252">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22f9f-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="22f9f-253">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="22f9f-253">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="22f9f-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22f9f-254">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="22f9f-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22f9f-255">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="22f9f-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22f9f-256">Search-Flags</span></span>           | <span data-ttu-id="22f9f-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22f9f-257">0x00000000</span></span>   |
| <span data-ttu-id="22f9f-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22f9f-258">System-Flags</span></span>           | <span data-ttu-id="22f9f-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22f9f-259">0x00000010</span></span>   |
| <span data-ttu-id="22f9f-260">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="22f9f-260">Classes used in</span></span>        | \-           |



 

 




