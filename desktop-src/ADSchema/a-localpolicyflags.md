---
title: Local-Policy-Flags-Attribut
description: Flags, die bestimmen, wo ein Computer seine Richtlinie erhält. Local-Policy-Reference.
ms.assetid: 1f2fa723-507a-4e27-a325-8bd6f6cb6bd6
ms.tgt_platform: multiple
keywords:
- AD-Schema für das lokale Policy-Flags-Attribut
- localpolicyflags-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Local-Policy-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc077fe793a523b41974280ada7e54b82335d733
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344750"
---
# <a name="local-policy-flags-attribute"></a><span data-ttu-id="5a84d-106">Local-Policy-Flags-Attribut</span><span class="sxs-lookup"><span data-stu-id="5a84d-106">Local-Policy-Flags attribute</span></span>

<span data-ttu-id="5a84d-107">Flags, die bestimmen, wo ein Computer seine Richtlinie erhält.</span><span class="sxs-lookup"><span data-stu-id="5a84d-107">Flags that determine where a computer gets its policy.</span></span> <span data-ttu-id="5a84d-108">Local-Policy-Reference.</span><span class="sxs-lookup"><span data-stu-id="5a84d-108">Local-Policy-Reference.</span></span>



| <span data-ttu-id="5a84d-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a84d-109">Entry</span></span> | <span data-ttu-id="5a84d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="5a84d-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5a84d-111">CN</span><span class="sxs-lookup"><span data-stu-id="5a84d-111">CN</span></span>                | <span data-ttu-id="5a84d-112">Lokale Richtlinienflags</span><span class="sxs-lookup"><span data-stu-id="5a84d-112">Local-Policy-Flags</span></span>                   |
| <span data-ttu-id="5a84d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5a84d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5a84d-114">localpolicyflags</span><span class="sxs-lookup"><span data-stu-id="5a84d-114">localPolicyFlags</span></span>                     |
| <span data-ttu-id="5a84d-115">Size</span><span class="sxs-lookup"><span data-stu-id="5a84d-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="5a84d-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5a84d-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="5a84d-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="5a84d-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="5a84d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5a84d-118">Attribute-Id</span></span>      | <span data-ttu-id="5a84d-119">1.2.840.113556.1.4.56</span><span class="sxs-lookup"><span data-stu-id="5a84d-119">1.2.840.113556.1.4.56</span></span>                |
| <span data-ttu-id="5a84d-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5a84d-120">System-Id-Guid</span></span>    | <span data-ttu-id="5a84d-121">bf96799e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="5a84d-121">bf96799e-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="5a84d-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a84d-122">Syntax</span></span>            | [<span data-ttu-id="5a84d-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="5a84d-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="5a84d-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="5a84d-124">Implementations</span></span>

-   [<span data-ttu-id="5a84d-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5a84d-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5a84d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5a84d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5a84d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5a84d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5a84d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5a84d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5a84d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5a84d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5a84d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5a84d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5a84d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5a84d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="5a84d-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a84d-132">Entry</span></span> | <span data-ttu-id="5a84d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="5a84d-133">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5a84d-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a84d-134">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5a84d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a84d-135">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5a84d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a84d-136">System-Only</span></span>            | <span data-ttu-id="5a84d-137">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-137">False</span></span>                                     |
| <span data-ttu-id="5a84d-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a84d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="5a84d-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a84d-139">True</span></span>                                      |
| <span data-ttu-id="5a84d-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a84d-140">Is Indexed</span></span>             | <span data-ttu-id="5a84d-141">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-141">False</span></span>                                     |
| <span data-ttu-id="5a84d-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a84d-142">In Global Catalog</span></span>      | <span data-ttu-id="5a84d-143">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-143">False</span></span>                                     |
| <span data-ttu-id="5a84d-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a84d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a84d-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a84d-145">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5a84d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a84d-146">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="5a84d-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a84d-147">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="5a84d-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a84d-148">Search-Flags</span></span>           | <span data-ttu-id="5a84d-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a84d-149">0x00000000</span></span>                                |
| <span data-ttu-id="5a84d-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a84d-150">System-Flags</span></span>           | <span data-ttu-id="5a84d-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a84d-151">0x00000010</span></span>                                |
| <span data-ttu-id="5a84d-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a84d-152">Classes used in</span></span>        | [<span data-ttu-id="5a84d-153">**Computer**</span><span class="sxs-lookup"><span data-stu-id="5a84d-153">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5a84d-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5a84d-154">Windows Server 2003</span></span>



| <span data-ttu-id="5a84d-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a84d-155">Entry</span></span> | <span data-ttu-id="5a84d-156">Wert</span><span class="sxs-lookup"><span data-stu-id="5a84d-156">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5a84d-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a84d-157">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5a84d-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a84d-158">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5a84d-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a84d-159">System-Only</span></span>            | <span data-ttu-id="5a84d-160">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-160">False</span></span>                                     |
| <span data-ttu-id="5a84d-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a84d-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5a84d-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a84d-162">True</span></span>                                      |
| <span data-ttu-id="5a84d-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a84d-163">Is Indexed</span></span>             | <span data-ttu-id="5a84d-164">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-164">False</span></span>                                     |
| <span data-ttu-id="5a84d-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a84d-165">In Global Catalog</span></span>      | <span data-ttu-id="5a84d-166">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-166">False</span></span>                                     |
| <span data-ttu-id="5a84d-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a84d-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a84d-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a84d-168">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5a84d-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a84d-169">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="5a84d-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a84d-170">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="5a84d-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a84d-171">Search-Flags</span></span>           | <span data-ttu-id="5a84d-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a84d-172">0x00000000</span></span>                                |
| <span data-ttu-id="5a84d-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a84d-173">System-Flags</span></span>           | <span data-ttu-id="5a84d-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a84d-174">0x00000010</span></span>                                |
| <span data-ttu-id="5a84d-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a84d-175">Classes used in</span></span>        | [<span data-ttu-id="5a84d-176">**Computer**</span><span class="sxs-lookup"><span data-stu-id="5a84d-176">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5a84d-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5a84d-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5a84d-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a84d-178">Entry</span></span> | <span data-ttu-id="5a84d-179">Wert</span><span class="sxs-lookup"><span data-stu-id="5a84d-179">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5a84d-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a84d-180">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5a84d-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a84d-181">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5a84d-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a84d-182">System-Only</span></span>            | <span data-ttu-id="5a84d-183">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-183">False</span></span>                                     |
| <span data-ttu-id="5a84d-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a84d-184">Is-Single-Valued</span></span>       | <span data-ttu-id="5a84d-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a84d-185">True</span></span>                                      |
| <span data-ttu-id="5a84d-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a84d-186">Is Indexed</span></span>             | <span data-ttu-id="5a84d-187">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-187">False</span></span>                                     |
| <span data-ttu-id="5a84d-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a84d-188">In Global Catalog</span></span>      | <span data-ttu-id="5a84d-189">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-189">False</span></span>                                     |
| <span data-ttu-id="5a84d-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a84d-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a84d-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a84d-191">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5a84d-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a84d-192">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="5a84d-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a84d-193">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="5a84d-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a84d-194">Search-Flags</span></span>           | <span data-ttu-id="5a84d-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a84d-195">0x00000000</span></span>                                |
| <span data-ttu-id="5a84d-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a84d-196">System-Flags</span></span>           | <span data-ttu-id="5a84d-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a84d-197">0x00000010</span></span>                                |
| <span data-ttu-id="5a84d-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a84d-198">Classes used in</span></span>        | [<span data-ttu-id="5a84d-199">**Computer**</span><span class="sxs-lookup"><span data-stu-id="5a84d-199">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5a84d-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a84d-200">Windows Server 2008</span></span>



| <span data-ttu-id="5a84d-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a84d-201">Entry</span></span> | <span data-ttu-id="5a84d-202">Wert</span><span class="sxs-lookup"><span data-stu-id="5a84d-202">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5a84d-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a84d-203">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5a84d-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a84d-204">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5a84d-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a84d-205">System-Only</span></span>            | <span data-ttu-id="5a84d-206">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-206">False</span></span>                                     |
| <span data-ttu-id="5a84d-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a84d-207">Is-Single-Valued</span></span>       | <span data-ttu-id="5a84d-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a84d-208">True</span></span>                                      |
| <span data-ttu-id="5a84d-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a84d-209">Is Indexed</span></span>             | <span data-ttu-id="5a84d-210">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-210">False</span></span>                                     |
| <span data-ttu-id="5a84d-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a84d-211">In Global Catalog</span></span>      | <span data-ttu-id="5a84d-212">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-212">False</span></span>                                     |
| <span data-ttu-id="5a84d-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a84d-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a84d-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a84d-214">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5a84d-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a84d-215">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="5a84d-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a84d-216">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="5a84d-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a84d-217">Search-Flags</span></span>           | <span data-ttu-id="5a84d-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a84d-218">0x00000000</span></span>                                |
| <span data-ttu-id="5a84d-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a84d-219">System-Flags</span></span>           | <span data-ttu-id="5a84d-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a84d-220">0x00000010</span></span>                                |
| <span data-ttu-id="5a84d-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a84d-221">Classes used in</span></span>        | [<span data-ttu-id="5a84d-222">**Computer**</span><span class="sxs-lookup"><span data-stu-id="5a84d-222">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5a84d-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5a84d-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5a84d-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a84d-224">Entry</span></span> | <span data-ttu-id="5a84d-225">Wert</span><span class="sxs-lookup"><span data-stu-id="5a84d-225">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5a84d-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a84d-226">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5a84d-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a84d-227">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5a84d-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a84d-228">System-Only</span></span>            | <span data-ttu-id="5a84d-229">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-229">False</span></span>                                     |
| <span data-ttu-id="5a84d-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a84d-230">Is-Single-Valued</span></span>       | <span data-ttu-id="5a84d-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a84d-231">True</span></span>                                      |
| <span data-ttu-id="5a84d-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a84d-232">Is Indexed</span></span>             | <span data-ttu-id="5a84d-233">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-233">False</span></span>                                     |
| <span data-ttu-id="5a84d-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a84d-234">In Global Catalog</span></span>      | <span data-ttu-id="5a84d-235">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-235">False</span></span>                                     |
| <span data-ttu-id="5a84d-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a84d-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a84d-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a84d-237">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5a84d-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a84d-238">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="5a84d-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a84d-239">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="5a84d-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a84d-240">Search-Flags</span></span>           | <span data-ttu-id="5a84d-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a84d-241">0x00000000</span></span>                                |
| <span data-ttu-id="5a84d-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a84d-242">System-Flags</span></span>           | <span data-ttu-id="5a84d-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a84d-243">0x00000010</span></span>                                |
| <span data-ttu-id="5a84d-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a84d-244">Classes used in</span></span>        | [<span data-ttu-id="5a84d-245">**Computer**</span><span class="sxs-lookup"><span data-stu-id="5a84d-245">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5a84d-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5a84d-246">Windows Server 2012</span></span>



| <span data-ttu-id="5a84d-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a84d-247">Entry</span></span> | <span data-ttu-id="5a84d-248">Wert</span><span class="sxs-lookup"><span data-stu-id="5a84d-248">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5a84d-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a84d-249">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5a84d-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a84d-250">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5a84d-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a84d-251">System-Only</span></span>            | <span data-ttu-id="5a84d-252">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-252">False</span></span>                                     |
| <span data-ttu-id="5a84d-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a84d-253">Is-Single-Valued</span></span>       | <span data-ttu-id="5a84d-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a84d-254">True</span></span>                                      |
| <span data-ttu-id="5a84d-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a84d-255">Is Indexed</span></span>             | <span data-ttu-id="5a84d-256">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-256">False</span></span>                                     |
| <span data-ttu-id="5a84d-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a84d-257">In Global Catalog</span></span>      | <span data-ttu-id="5a84d-258">False</span><span class="sxs-lookup"><span data-stu-id="5a84d-258">False</span></span>                                     |
| <span data-ttu-id="5a84d-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a84d-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a84d-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a84d-260">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5a84d-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a84d-261">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="5a84d-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a84d-262">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="5a84d-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a84d-263">Search-Flags</span></span>           | <span data-ttu-id="5a84d-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a84d-264">0x00000000</span></span>                                |
| <span data-ttu-id="5a84d-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a84d-265">System-Flags</span></span>           | <span data-ttu-id="5a84d-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a84d-266">0x00000010</span></span>                                |
| <span data-ttu-id="5a84d-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a84d-267">Classes used in</span></span>        | [<span data-ttu-id="5a84d-268">**Computer**</span><span class="sxs-lookup"><span data-stu-id="5a84d-268">**Computer**</span></span>](c-computer.md)<br/> |



 

 





