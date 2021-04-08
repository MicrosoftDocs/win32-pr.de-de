---
title: ACS-Cache-Timeout-Attribut
description: Die Zeitspanne vor dem Ablauf von ACS-Objekten, die vom ACS-Dienst zwischengespeichert werden.
ms.assetid: 8927ca01-d550-42df-8a14-96ddbea3fdb8
ms.tgt_platform: multiple
keywords:
- AD-Schema des ACS-Cache-Timeout-Attributs
- AD-Schema des acscachetimeout-Attributs
topic_type:
- apiref
api_name:
- ACS-Cache-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bb72ca9708c3e4edd8f1229d887439ff133d201
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859505"
---
# <a name="acs-cache-timeout-attribute"></a><span data-ttu-id="663c2-105">ACS-Cache-Timeout-Attribut</span><span class="sxs-lookup"><span data-stu-id="663c2-105">ACS-Cache-Timeout attribute</span></span>

<span data-ttu-id="663c2-106">Die Zeitspanne vor dem Ablauf von ACS-Objekten, die vom ACS-Dienst zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="663c2-106">The amount of time before the expiration of ACS objects that are cached by the ACS service.</span></span>



| <span data-ttu-id="663c2-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="663c2-107">Entry</span></span> | <span data-ttu-id="663c2-108">Wert</span><span class="sxs-lookup"><span data-stu-id="663c2-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="663c2-109">CN</span><span class="sxs-lookup"><span data-stu-id="663c2-109">CN</span></span>                | <span data-ttu-id="663c2-110">ACS-Cache-Timeout</span><span class="sxs-lookup"><span data-stu-id="663c2-110">ACS-Cache-Timeout</span></span>                    |
| <span data-ttu-id="663c2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="663c2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="663c2-112">acscachetimeout</span><span class="sxs-lookup"><span data-stu-id="663c2-112">aCSCacheTimeout</span></span>                      |
| <span data-ttu-id="663c2-113">Size</span><span class="sxs-lookup"><span data-stu-id="663c2-113">Size</span></span>              | <span data-ttu-id="663c2-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="663c2-114">4 bytes</span></span>                              |
| <span data-ttu-id="663c2-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="663c2-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="663c2-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="663c2-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="663c2-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="663c2-117">Attribute-Id</span></span>      | <span data-ttu-id="663c2-118">1.2.840.113556.1.4.779</span><span class="sxs-lookup"><span data-stu-id="663c2-118">1.2.840.113556.1.4.779</span></span>               |
| <span data-ttu-id="663c2-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="663c2-119">System-Id-Guid</span></span>    | <span data-ttu-id="663c2-120">1cb355a1-56d0-11d1-a9c6-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="663c2-120">1cb355a1-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="663c2-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="663c2-121">Syntax</span></span>            | [<span data-ttu-id="663c2-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="663c2-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="663c2-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="663c2-123">Implementations</span></span>

-   [<span data-ttu-id="663c2-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="663c2-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="663c2-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="663c2-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="663c2-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="663c2-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="663c2-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="663c2-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="663c2-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="663c2-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="663c2-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="663c2-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="663c2-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="663c2-130">Windows 2000 Server</span></span>



| <span data-ttu-id="663c2-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="663c2-131">Entry</span></span> | <span data-ttu-id="663c2-132">Wert</span><span class="sxs-lookup"><span data-stu-id="663c2-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="663c2-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="663c2-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="663c2-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="663c2-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="663c2-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="663c2-135">System-Only</span></span>            | <span data-ttu-id="663c2-136">False</span><span class="sxs-lookup"><span data-stu-id="663c2-136">False</span></span>                                        |
| <span data-ttu-id="663c2-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="663c2-137">Is-Single-Valued</span></span>       | <span data-ttu-id="663c2-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="663c2-138">True</span></span>                                         |
| <span data-ttu-id="663c2-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="663c2-139">Is Indexed</span></span>             | <span data-ttu-id="663c2-140">False</span><span class="sxs-lookup"><span data-stu-id="663c2-140">False</span></span>                                        |
| <span data-ttu-id="663c2-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="663c2-141">In Global Catalog</span></span>      | <span data-ttu-id="663c2-142">False</span><span class="sxs-lookup"><span data-stu-id="663c2-142">False</span></span>                                        |
| <span data-ttu-id="663c2-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="663c2-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="663c2-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="663c2-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="663c2-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="663c2-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="663c2-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="663c2-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="663c2-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="663c2-147">Search-Flags</span></span>           | <span data-ttu-id="663c2-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="663c2-148">0x00000000</span></span>                                   |
| <span data-ttu-id="663c2-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="663c2-149">System-Flags</span></span>           | <span data-ttu-id="663c2-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="663c2-150">0x00000010</span></span>                                   |
| <span data-ttu-id="663c2-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="663c2-151">Classes used in</span></span>        | [<span data-ttu-id="663c2-152">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="663c2-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="663c2-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="663c2-153">Windows Server 2003</span></span>



| <span data-ttu-id="663c2-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="663c2-154">Entry</span></span> | <span data-ttu-id="663c2-155">Wert</span><span class="sxs-lookup"><span data-stu-id="663c2-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="663c2-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="663c2-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="663c2-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="663c2-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="663c2-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="663c2-158">System-Only</span></span>            | <span data-ttu-id="663c2-159">False</span><span class="sxs-lookup"><span data-stu-id="663c2-159">False</span></span>                                        |
| <span data-ttu-id="663c2-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="663c2-160">Is-Single-Valued</span></span>       | <span data-ttu-id="663c2-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="663c2-161">True</span></span>                                         |
| <span data-ttu-id="663c2-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="663c2-162">Is Indexed</span></span>             | <span data-ttu-id="663c2-163">False</span><span class="sxs-lookup"><span data-stu-id="663c2-163">False</span></span>                                        |
| <span data-ttu-id="663c2-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="663c2-164">In Global Catalog</span></span>      | <span data-ttu-id="663c2-165">False</span><span class="sxs-lookup"><span data-stu-id="663c2-165">False</span></span>                                        |
| <span data-ttu-id="663c2-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="663c2-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="663c2-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="663c2-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="663c2-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="663c2-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="663c2-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="663c2-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="663c2-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="663c2-170">Search-Flags</span></span>           | <span data-ttu-id="663c2-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="663c2-171">0x00000000</span></span>                                   |
| <span data-ttu-id="663c2-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="663c2-172">System-Flags</span></span>           | <span data-ttu-id="663c2-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="663c2-173">0x00000010</span></span>                                   |
| <span data-ttu-id="663c2-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="663c2-174">Classes used in</span></span>        | [<span data-ttu-id="663c2-175">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="663c2-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="663c2-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="663c2-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="663c2-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="663c2-177">Entry</span></span> | <span data-ttu-id="663c2-178">Wert</span><span class="sxs-lookup"><span data-stu-id="663c2-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="663c2-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="663c2-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="663c2-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="663c2-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="663c2-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="663c2-181">System-Only</span></span>            | <span data-ttu-id="663c2-182">False</span><span class="sxs-lookup"><span data-stu-id="663c2-182">False</span></span>                                        |
| <span data-ttu-id="663c2-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="663c2-183">Is-Single-Valued</span></span>       | <span data-ttu-id="663c2-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="663c2-184">True</span></span>                                         |
| <span data-ttu-id="663c2-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="663c2-185">Is Indexed</span></span>             | <span data-ttu-id="663c2-186">False</span><span class="sxs-lookup"><span data-stu-id="663c2-186">False</span></span>                                        |
| <span data-ttu-id="663c2-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="663c2-187">In Global Catalog</span></span>      | <span data-ttu-id="663c2-188">False</span><span class="sxs-lookup"><span data-stu-id="663c2-188">False</span></span>                                        |
| <span data-ttu-id="663c2-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="663c2-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="663c2-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="663c2-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="663c2-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="663c2-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="663c2-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="663c2-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="663c2-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="663c2-193">Search-Flags</span></span>           | <span data-ttu-id="663c2-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="663c2-194">0x00000000</span></span>                                   |
| <span data-ttu-id="663c2-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="663c2-195">System-Flags</span></span>           | <span data-ttu-id="663c2-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="663c2-196">0x00000010</span></span>                                   |
| <span data-ttu-id="663c2-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="663c2-197">Classes used in</span></span>        | [<span data-ttu-id="663c2-198">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="663c2-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="663c2-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="663c2-199">Windows Server 2008</span></span>



| <span data-ttu-id="663c2-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="663c2-200">Entry</span></span> | <span data-ttu-id="663c2-201">Wert</span><span class="sxs-lookup"><span data-stu-id="663c2-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="663c2-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="663c2-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="663c2-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="663c2-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="663c2-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="663c2-204">System-Only</span></span>            | <span data-ttu-id="663c2-205">False</span><span class="sxs-lookup"><span data-stu-id="663c2-205">False</span></span>                                        |
| <span data-ttu-id="663c2-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="663c2-206">Is-Single-Valued</span></span>       | <span data-ttu-id="663c2-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="663c2-207">True</span></span>                                         |
| <span data-ttu-id="663c2-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="663c2-208">Is Indexed</span></span>             | <span data-ttu-id="663c2-209">False</span><span class="sxs-lookup"><span data-stu-id="663c2-209">False</span></span>                                        |
| <span data-ttu-id="663c2-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="663c2-210">In Global Catalog</span></span>      | <span data-ttu-id="663c2-211">False</span><span class="sxs-lookup"><span data-stu-id="663c2-211">False</span></span>                                        |
| <span data-ttu-id="663c2-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="663c2-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="663c2-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="663c2-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="663c2-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="663c2-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="663c2-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="663c2-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="663c2-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="663c2-216">Search-Flags</span></span>           | <span data-ttu-id="663c2-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="663c2-217">0x00000000</span></span>                                   |
| <span data-ttu-id="663c2-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="663c2-218">System-Flags</span></span>           | <span data-ttu-id="663c2-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="663c2-219">0x00000010</span></span>                                   |
| <span data-ttu-id="663c2-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="663c2-220">Classes used in</span></span>        | [<span data-ttu-id="663c2-221">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="663c2-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="663c2-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="663c2-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="663c2-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="663c2-223">Entry</span></span> | <span data-ttu-id="663c2-224">Wert</span><span class="sxs-lookup"><span data-stu-id="663c2-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="663c2-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="663c2-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="663c2-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="663c2-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="663c2-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="663c2-227">System-Only</span></span>            | <span data-ttu-id="663c2-228">False</span><span class="sxs-lookup"><span data-stu-id="663c2-228">False</span></span>                                        |
| <span data-ttu-id="663c2-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="663c2-229">Is-Single-Valued</span></span>       | <span data-ttu-id="663c2-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="663c2-230">True</span></span>                                         |
| <span data-ttu-id="663c2-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="663c2-231">Is Indexed</span></span>             | <span data-ttu-id="663c2-232">False</span><span class="sxs-lookup"><span data-stu-id="663c2-232">False</span></span>                                        |
| <span data-ttu-id="663c2-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="663c2-233">In Global Catalog</span></span>      | <span data-ttu-id="663c2-234">False</span><span class="sxs-lookup"><span data-stu-id="663c2-234">False</span></span>                                        |
| <span data-ttu-id="663c2-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="663c2-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="663c2-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="663c2-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="663c2-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="663c2-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="663c2-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="663c2-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="663c2-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="663c2-239">Search-Flags</span></span>           | <span data-ttu-id="663c2-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="663c2-240">0x00000000</span></span>                                   |
| <span data-ttu-id="663c2-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="663c2-241">System-Flags</span></span>           | <span data-ttu-id="663c2-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="663c2-242">0x00000010</span></span>                                   |
| <span data-ttu-id="663c2-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="663c2-243">Classes used in</span></span>        | [<span data-ttu-id="663c2-244">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="663c2-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="663c2-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="663c2-245">Windows Server 2012</span></span>



| <span data-ttu-id="663c2-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="663c2-246">Entry</span></span> | <span data-ttu-id="663c2-247">Wert</span><span class="sxs-lookup"><span data-stu-id="663c2-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="663c2-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="663c2-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="663c2-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="663c2-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="663c2-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="663c2-250">System-Only</span></span>            | <span data-ttu-id="663c2-251">False</span><span class="sxs-lookup"><span data-stu-id="663c2-251">False</span></span>                                        |
| <span data-ttu-id="663c2-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="663c2-252">Is-Single-Valued</span></span>       | <span data-ttu-id="663c2-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="663c2-253">True</span></span>                                         |
| <span data-ttu-id="663c2-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="663c2-254">Is Indexed</span></span>             | <span data-ttu-id="663c2-255">False</span><span class="sxs-lookup"><span data-stu-id="663c2-255">False</span></span>                                        |
| <span data-ttu-id="663c2-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="663c2-256">In Global Catalog</span></span>      | <span data-ttu-id="663c2-257">False</span><span class="sxs-lookup"><span data-stu-id="663c2-257">False</span></span>                                        |
| <span data-ttu-id="663c2-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="663c2-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="663c2-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="663c2-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="663c2-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="663c2-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="663c2-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="663c2-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="663c2-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="663c2-262">Search-Flags</span></span>           | <span data-ttu-id="663c2-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="663c2-263">0x00000000</span></span>                                   |
| <span data-ttu-id="663c2-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="663c2-264">System-Flags</span></span>           | <span data-ttu-id="663c2-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="663c2-265">0x00000010</span></span>                                   |
| <span data-ttu-id="663c2-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="663c2-266">Classes used in</span></span>        | [<span data-ttu-id="663c2-267">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="663c2-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





