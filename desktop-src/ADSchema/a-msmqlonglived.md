---
title: MSMQ-langlebiges Attribut
description: Die Standard Gültigkeitsdauer von MSMQ-Nachrichten.
ms.assetid: e47bcb0e-6e30-4300-9cfa-c553c2842416
ms.tgt_platform: multiple
keywords:
- AD-Schema für MSMQ-langes Attribut
- AD-Schema des msmqlonglived-Attributs
topic_type:
- apiref
api_name:
- MSMQ-Long-Lived
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d175a6ed59114eaa591f8e45a9c1291652d9e037
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480039"
---
# <a name="msmq-long-lived-attribute"></a><span data-ttu-id="06078-105">MSMQ-langlebiges Attribut</span><span class="sxs-lookup"><span data-stu-id="06078-105">MSMQ-Long-Lived attribute</span></span>

<span data-ttu-id="06078-106">Die Standard Gültigkeitsdauer von MSMQ-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="06078-106">The default time to live of MSMQ messages.</span></span>



| <span data-ttu-id="06078-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="06078-107">Entry</span></span> | <span data-ttu-id="06078-108">Wert</span><span class="sxs-lookup"><span data-stu-id="06078-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="06078-109">CN</span><span class="sxs-lookup"><span data-stu-id="06078-109">CN</span></span>                | <span data-ttu-id="06078-110">MSMQ-langlebig</span><span class="sxs-lookup"><span data-stu-id="06078-110">MSMQ-Long-Lived</span></span>                      |
| <span data-ttu-id="06078-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="06078-111">Ldap-Display-Name</span></span> | <span data-ttu-id="06078-112">msmqlonglived</span><span class="sxs-lookup"><span data-stu-id="06078-112">mSMQLongLived</span></span>                        |
| <span data-ttu-id="06078-113">Size</span><span class="sxs-lookup"><span data-stu-id="06078-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="06078-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="06078-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="06078-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="06078-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="06078-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="06078-116">Attribute-Id</span></span>      | <span data-ttu-id="06078-117">1.2.840.113556.1.4.941</span><span class="sxs-lookup"><span data-stu-id="06078-117">1.2.840.113556.1.4.941</span></span>               |
| <span data-ttu-id="06078-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="06078-118">System-Id-Guid</span></span>    | <span data-ttu-id="06078-119">9a0dc335-C100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="06078-119">9a0dc335-c100-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="06078-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="06078-120">Syntax</span></span>            | [<span data-ttu-id="06078-121">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="06078-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="06078-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="06078-122">Implementations</span></span>

-   [<span data-ttu-id="06078-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="06078-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="06078-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="06078-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="06078-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="06078-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="06078-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="06078-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="06078-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="06078-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="06078-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="06078-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="06078-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="06078-129">Windows 2000 Server</span></span>



| <span data-ttu-id="06078-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="06078-130">Entry</span></span> | <span data-ttu-id="06078-131">Wert</span><span class="sxs-lookup"><span data-stu-id="06078-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="06078-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="06078-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="06078-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06078-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="06078-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="06078-134">System-Only</span></span>            | <span data-ttu-id="06078-135">False</span><span class="sxs-lookup"><span data-stu-id="06078-135">False</span></span>                                                                   |
| <span data-ttu-id="06078-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="06078-136">Is-Single-Valued</span></span>       | <span data-ttu-id="06078-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="06078-137">True</span></span>                                                                    |
| <span data-ttu-id="06078-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="06078-138">Is Indexed</span></span>             | <span data-ttu-id="06078-139">False</span><span class="sxs-lookup"><span data-stu-id="06078-139">False</span></span>                                                                   |
| <span data-ttu-id="06078-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="06078-140">In Global Catalog</span></span>      | <span data-ttu-id="06078-141">False</span><span class="sxs-lookup"><span data-stu-id="06078-141">False</span></span>                                                                   |
| <span data-ttu-id="06078-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06078-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="06078-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="06078-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="06078-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06078-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="06078-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06078-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="06078-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-146">Search-Flags</span></span>           | <span data-ttu-id="06078-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06078-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="06078-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-148">System-Flags</span></span>           | <span data-ttu-id="06078-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06078-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="06078-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="06078-150">Classes used in</span></span>        | [<span data-ttu-id="06078-151">**MSMQ-Enterprise-Settings**</span><span class="sxs-lookup"><span data-stu-id="06078-151">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="06078-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="06078-152">Windows Server 2003</span></span>



| <span data-ttu-id="06078-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="06078-153">Entry</span></span> | <span data-ttu-id="06078-154">Wert</span><span class="sxs-lookup"><span data-stu-id="06078-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="06078-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="06078-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="06078-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06078-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="06078-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="06078-157">System-Only</span></span>            | <span data-ttu-id="06078-158">False</span><span class="sxs-lookup"><span data-stu-id="06078-158">False</span></span>                                                                   |
| <span data-ttu-id="06078-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="06078-159">Is-Single-Valued</span></span>       | <span data-ttu-id="06078-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="06078-160">True</span></span>                                                                    |
| <span data-ttu-id="06078-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="06078-161">Is Indexed</span></span>             | <span data-ttu-id="06078-162">False</span><span class="sxs-lookup"><span data-stu-id="06078-162">False</span></span>                                                                   |
| <span data-ttu-id="06078-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="06078-163">In Global Catalog</span></span>      | <span data-ttu-id="06078-164">False</span><span class="sxs-lookup"><span data-stu-id="06078-164">False</span></span>                                                                   |
| <span data-ttu-id="06078-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06078-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="06078-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="06078-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="06078-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06078-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="06078-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06078-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="06078-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-169">Search-Flags</span></span>           | <span data-ttu-id="06078-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06078-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="06078-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-171">System-Flags</span></span>           | <span data-ttu-id="06078-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06078-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="06078-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="06078-173">Classes used in</span></span>        | [<span data-ttu-id="06078-174">**MSMQ-Enterprise-Settings**</span><span class="sxs-lookup"><span data-stu-id="06078-174">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="06078-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="06078-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="06078-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="06078-176">Entry</span></span> | <span data-ttu-id="06078-177">Wert</span><span class="sxs-lookup"><span data-stu-id="06078-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="06078-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="06078-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="06078-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06078-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="06078-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="06078-180">System-Only</span></span>            | <span data-ttu-id="06078-181">False</span><span class="sxs-lookup"><span data-stu-id="06078-181">False</span></span>                                                                   |
| <span data-ttu-id="06078-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="06078-182">Is-Single-Valued</span></span>       | <span data-ttu-id="06078-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="06078-183">True</span></span>                                                                    |
| <span data-ttu-id="06078-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="06078-184">Is Indexed</span></span>             | <span data-ttu-id="06078-185">False</span><span class="sxs-lookup"><span data-stu-id="06078-185">False</span></span>                                                                   |
| <span data-ttu-id="06078-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="06078-186">In Global Catalog</span></span>      | <span data-ttu-id="06078-187">False</span><span class="sxs-lookup"><span data-stu-id="06078-187">False</span></span>                                                                   |
| <span data-ttu-id="06078-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06078-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="06078-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="06078-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="06078-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06078-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="06078-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06078-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="06078-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-192">Search-Flags</span></span>           | <span data-ttu-id="06078-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06078-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="06078-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-194">System-Flags</span></span>           | <span data-ttu-id="06078-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06078-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="06078-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="06078-196">Classes used in</span></span>        | [<span data-ttu-id="06078-197">**MSMQ-Enterprise-Settings**</span><span class="sxs-lookup"><span data-stu-id="06078-197">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="06078-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06078-198">Windows Server 2008</span></span>



| <span data-ttu-id="06078-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="06078-199">Entry</span></span> | <span data-ttu-id="06078-200">Wert</span><span class="sxs-lookup"><span data-stu-id="06078-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="06078-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="06078-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="06078-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06078-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="06078-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="06078-203">System-Only</span></span>            | <span data-ttu-id="06078-204">False</span><span class="sxs-lookup"><span data-stu-id="06078-204">False</span></span>                                                                   |
| <span data-ttu-id="06078-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="06078-205">Is-Single-Valued</span></span>       | <span data-ttu-id="06078-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="06078-206">True</span></span>                                                                    |
| <span data-ttu-id="06078-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="06078-207">Is Indexed</span></span>             | <span data-ttu-id="06078-208">False</span><span class="sxs-lookup"><span data-stu-id="06078-208">False</span></span>                                                                   |
| <span data-ttu-id="06078-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="06078-209">In Global Catalog</span></span>      | <span data-ttu-id="06078-210">False</span><span class="sxs-lookup"><span data-stu-id="06078-210">False</span></span>                                                                   |
| <span data-ttu-id="06078-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06078-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="06078-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="06078-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="06078-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06078-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="06078-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06078-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="06078-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-215">Search-Flags</span></span>           | <span data-ttu-id="06078-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06078-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="06078-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-217">System-Flags</span></span>           | <span data-ttu-id="06078-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06078-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="06078-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="06078-219">Classes used in</span></span>        | [<span data-ttu-id="06078-220">**MSMQ-Enterprise-Settings**</span><span class="sxs-lookup"><span data-stu-id="06078-220">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="06078-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="06078-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="06078-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="06078-222">Entry</span></span> | <span data-ttu-id="06078-223">Wert</span><span class="sxs-lookup"><span data-stu-id="06078-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="06078-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="06078-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="06078-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06078-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="06078-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="06078-226">System-Only</span></span>            | <span data-ttu-id="06078-227">False</span><span class="sxs-lookup"><span data-stu-id="06078-227">False</span></span>                                                                   |
| <span data-ttu-id="06078-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="06078-228">Is-Single-Valued</span></span>       | <span data-ttu-id="06078-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="06078-229">True</span></span>                                                                    |
| <span data-ttu-id="06078-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="06078-230">Is Indexed</span></span>             | <span data-ttu-id="06078-231">False</span><span class="sxs-lookup"><span data-stu-id="06078-231">False</span></span>                                                                   |
| <span data-ttu-id="06078-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="06078-232">In Global Catalog</span></span>      | <span data-ttu-id="06078-233">False</span><span class="sxs-lookup"><span data-stu-id="06078-233">False</span></span>                                                                   |
| <span data-ttu-id="06078-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06078-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="06078-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="06078-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="06078-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06078-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="06078-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06078-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="06078-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-238">Search-Flags</span></span>           | <span data-ttu-id="06078-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06078-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="06078-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-240">System-Flags</span></span>           | <span data-ttu-id="06078-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06078-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="06078-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="06078-242">Classes used in</span></span>        | [<span data-ttu-id="06078-243">**MSMQ-Enterprise-Settings**</span><span class="sxs-lookup"><span data-stu-id="06078-243">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="06078-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="06078-244">Windows Server 2012</span></span>



| <span data-ttu-id="06078-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="06078-245">Entry</span></span> | <span data-ttu-id="06078-246">Wert</span><span class="sxs-lookup"><span data-stu-id="06078-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="06078-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="06078-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="06078-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06078-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="06078-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="06078-249">System-Only</span></span>            | <span data-ttu-id="06078-250">False</span><span class="sxs-lookup"><span data-stu-id="06078-250">False</span></span>                                                                   |
| <span data-ttu-id="06078-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="06078-251">Is-Single-Valued</span></span>       | <span data-ttu-id="06078-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="06078-252">True</span></span>                                                                    |
| <span data-ttu-id="06078-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="06078-253">Is Indexed</span></span>             | <span data-ttu-id="06078-254">False</span><span class="sxs-lookup"><span data-stu-id="06078-254">False</span></span>                                                                   |
| <span data-ttu-id="06078-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="06078-255">In Global Catalog</span></span>      | <span data-ttu-id="06078-256">False</span><span class="sxs-lookup"><span data-stu-id="06078-256">False</span></span>                                                                   |
| <span data-ttu-id="06078-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06078-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="06078-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="06078-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="06078-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06078-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="06078-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06078-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="06078-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-261">Search-Flags</span></span>           | <span data-ttu-id="06078-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06078-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="06078-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-263">System-Flags</span></span>           | <span data-ttu-id="06078-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06078-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="06078-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="06078-265">Classes used in</span></span>        | [<span data-ttu-id="06078-266">**MSMQ-Enterprise-Settings**</span><span class="sxs-lookup"><span data-stu-id="06078-266">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



 

 





