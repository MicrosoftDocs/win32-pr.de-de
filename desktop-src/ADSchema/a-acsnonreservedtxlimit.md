---
title: ACS-Non-reserved-TX-Limit-Attribut
description: Die maximale Bandbreite, die eine Benutzeranwendung übertragen kann, bevor eine Reservierung erfolgt.
ms.assetid: 5ead8e5b-31e8-438e-8d1b-9aae8601dfc9
ms.tgt_platform: multiple
keywords:
- AD-Schema für ACS-Non-reserved-TX-Limit
- acsnonreservedtxlimit-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Tx-Limit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 999b1775640624b7825b38ae1632d70773bc75b3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106339615"
---
# <a name="acs-non-reserved-tx-limit-attribute"></a><span data-ttu-id="262f0-105">ACS-Non-reserved-TX-Limit-Attribut</span><span class="sxs-lookup"><span data-stu-id="262f0-105">ACS-Non-Reserved-Tx-Limit attribute</span></span>

<span data-ttu-id="262f0-106">Die maximale Bandbreite, die eine Benutzeranwendung übertragen kann, bevor eine Reservierung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="262f0-106">The maximum bandwidth a user application can transmit before a reservation is in place.</span></span>



| <span data-ttu-id="262f0-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="262f0-107">Entry</span></span> | <span data-ttu-id="262f0-108">Wert</span><span class="sxs-lookup"><span data-stu-id="262f0-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="262f0-109">CN</span><span class="sxs-lookup"><span data-stu-id="262f0-109">CN</span></span>                | <span data-ttu-id="262f0-110">ACS-Non-reserved-TX-Limit</span><span class="sxs-lookup"><span data-stu-id="262f0-110">ACS-Non-Reserved-Tx-Limit</span></span>            |
| <span data-ttu-id="262f0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="262f0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="262f0-112">acsnonreservedtxlimit</span><span class="sxs-lookup"><span data-stu-id="262f0-112">aCSNonReservedTxLimit</span></span>                |
| <span data-ttu-id="262f0-113">Size</span><span class="sxs-lookup"><span data-stu-id="262f0-113">Size</span></span>              | <span data-ttu-id="262f0-114">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="262f0-114">8 bytes</span></span>                              |
| <span data-ttu-id="262f0-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="262f0-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="262f0-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="262f0-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="262f0-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="262f0-117">Attribute-Id</span></span>      | <span data-ttu-id="262f0-118">1.2.840.113556.1.4.780</span><span class="sxs-lookup"><span data-stu-id="262f0-118">1.2.840.113556.1.4.780</span></span>               |
| <span data-ttu-id="262f0-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="262f0-119">System-Id-Guid</span></span>    | <span data-ttu-id="262f0-120">1cb355a2-56d0-11d1-a9c6-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="262f0-120">1cb355a2-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="262f0-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="262f0-121">Syntax</span></span>            | [<span data-ttu-id="262f0-122">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="262f0-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="262f0-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="262f0-123">Implementations</span></span>

-   [<span data-ttu-id="262f0-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="262f0-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="262f0-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="262f0-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="262f0-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="262f0-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="262f0-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="262f0-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="262f0-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="262f0-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="262f0-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="262f0-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="262f0-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="262f0-130">Windows 2000 Server</span></span>



| <span data-ttu-id="262f0-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="262f0-131">Entry</span></span> | <span data-ttu-id="262f0-132">Wert</span><span class="sxs-lookup"><span data-stu-id="262f0-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="262f0-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="262f0-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="262f0-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="262f0-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="262f0-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="262f0-135">System-Only</span></span>            | <span data-ttu-id="262f0-136">False</span><span class="sxs-lookup"><span data-stu-id="262f0-136">False</span></span>                                        |
| <span data-ttu-id="262f0-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="262f0-137">Is-Single-Valued</span></span>       | <span data-ttu-id="262f0-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="262f0-138">True</span></span>                                         |
| <span data-ttu-id="262f0-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="262f0-139">Is Indexed</span></span>             | <span data-ttu-id="262f0-140">False</span><span class="sxs-lookup"><span data-stu-id="262f0-140">False</span></span>                                        |
| <span data-ttu-id="262f0-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="262f0-141">In Global Catalog</span></span>      | <span data-ttu-id="262f0-142">False</span><span class="sxs-lookup"><span data-stu-id="262f0-142">False</span></span>                                        |
| <span data-ttu-id="262f0-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="262f0-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="262f0-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="262f0-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="262f0-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="262f0-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="262f0-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="262f0-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="262f0-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="262f0-147">Search-Flags</span></span>           | <span data-ttu-id="262f0-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="262f0-148">0x00000000</span></span>                                   |
| <span data-ttu-id="262f0-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="262f0-149">System-Flags</span></span>           | <span data-ttu-id="262f0-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="262f0-150">0x00000010</span></span>                                   |
| <span data-ttu-id="262f0-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="262f0-151">Classes used in</span></span>        | [<span data-ttu-id="262f0-152">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="262f0-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="262f0-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="262f0-153">Windows Server 2003</span></span>



| <span data-ttu-id="262f0-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="262f0-154">Entry</span></span> | <span data-ttu-id="262f0-155">Wert</span><span class="sxs-lookup"><span data-stu-id="262f0-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="262f0-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="262f0-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="262f0-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="262f0-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="262f0-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="262f0-158">System-Only</span></span>            | <span data-ttu-id="262f0-159">False</span><span class="sxs-lookup"><span data-stu-id="262f0-159">False</span></span>                                        |
| <span data-ttu-id="262f0-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="262f0-160">Is-Single-Valued</span></span>       | <span data-ttu-id="262f0-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="262f0-161">True</span></span>                                         |
| <span data-ttu-id="262f0-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="262f0-162">Is Indexed</span></span>             | <span data-ttu-id="262f0-163">False</span><span class="sxs-lookup"><span data-stu-id="262f0-163">False</span></span>                                        |
| <span data-ttu-id="262f0-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="262f0-164">In Global Catalog</span></span>      | <span data-ttu-id="262f0-165">False</span><span class="sxs-lookup"><span data-stu-id="262f0-165">False</span></span>                                        |
| <span data-ttu-id="262f0-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="262f0-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="262f0-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="262f0-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="262f0-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="262f0-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="262f0-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="262f0-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="262f0-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="262f0-170">Search-Flags</span></span>           | <span data-ttu-id="262f0-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="262f0-171">0x00000000</span></span>                                   |
| <span data-ttu-id="262f0-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="262f0-172">System-Flags</span></span>           | <span data-ttu-id="262f0-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="262f0-173">0x00000010</span></span>                                   |
| <span data-ttu-id="262f0-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="262f0-174">Classes used in</span></span>        | [<span data-ttu-id="262f0-175">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="262f0-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="262f0-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="262f0-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="262f0-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="262f0-177">Entry</span></span> | <span data-ttu-id="262f0-178">Wert</span><span class="sxs-lookup"><span data-stu-id="262f0-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="262f0-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="262f0-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="262f0-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="262f0-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="262f0-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="262f0-181">System-Only</span></span>            | <span data-ttu-id="262f0-182">False</span><span class="sxs-lookup"><span data-stu-id="262f0-182">False</span></span>                                        |
| <span data-ttu-id="262f0-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="262f0-183">Is-Single-Valued</span></span>       | <span data-ttu-id="262f0-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="262f0-184">True</span></span>                                         |
| <span data-ttu-id="262f0-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="262f0-185">Is Indexed</span></span>             | <span data-ttu-id="262f0-186">False</span><span class="sxs-lookup"><span data-stu-id="262f0-186">False</span></span>                                        |
| <span data-ttu-id="262f0-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="262f0-187">In Global Catalog</span></span>      | <span data-ttu-id="262f0-188">False</span><span class="sxs-lookup"><span data-stu-id="262f0-188">False</span></span>                                        |
| <span data-ttu-id="262f0-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="262f0-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="262f0-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="262f0-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="262f0-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="262f0-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="262f0-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="262f0-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="262f0-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="262f0-193">Search-Flags</span></span>           | <span data-ttu-id="262f0-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="262f0-194">0x00000000</span></span>                                   |
| <span data-ttu-id="262f0-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="262f0-195">System-Flags</span></span>           | <span data-ttu-id="262f0-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="262f0-196">0x00000010</span></span>                                   |
| <span data-ttu-id="262f0-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="262f0-197">Classes used in</span></span>        | [<span data-ttu-id="262f0-198">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="262f0-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="262f0-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="262f0-199">Windows Server 2008</span></span>



| <span data-ttu-id="262f0-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="262f0-200">Entry</span></span> | <span data-ttu-id="262f0-201">Wert</span><span class="sxs-lookup"><span data-stu-id="262f0-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="262f0-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="262f0-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="262f0-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="262f0-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="262f0-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="262f0-204">System-Only</span></span>            | <span data-ttu-id="262f0-205">False</span><span class="sxs-lookup"><span data-stu-id="262f0-205">False</span></span>                                        |
| <span data-ttu-id="262f0-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="262f0-206">Is-Single-Valued</span></span>       | <span data-ttu-id="262f0-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="262f0-207">True</span></span>                                         |
| <span data-ttu-id="262f0-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="262f0-208">Is Indexed</span></span>             | <span data-ttu-id="262f0-209">False</span><span class="sxs-lookup"><span data-stu-id="262f0-209">False</span></span>                                        |
| <span data-ttu-id="262f0-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="262f0-210">In Global Catalog</span></span>      | <span data-ttu-id="262f0-211">False</span><span class="sxs-lookup"><span data-stu-id="262f0-211">False</span></span>                                        |
| <span data-ttu-id="262f0-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="262f0-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="262f0-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="262f0-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="262f0-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="262f0-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="262f0-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="262f0-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="262f0-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="262f0-216">Search-Flags</span></span>           | <span data-ttu-id="262f0-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="262f0-217">0x00000000</span></span>                                   |
| <span data-ttu-id="262f0-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="262f0-218">System-Flags</span></span>           | <span data-ttu-id="262f0-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="262f0-219">0x00000010</span></span>                                   |
| <span data-ttu-id="262f0-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="262f0-220">Classes used in</span></span>        | [<span data-ttu-id="262f0-221">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="262f0-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="262f0-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="262f0-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="262f0-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="262f0-223">Entry</span></span> | <span data-ttu-id="262f0-224">Wert</span><span class="sxs-lookup"><span data-stu-id="262f0-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="262f0-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="262f0-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="262f0-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="262f0-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="262f0-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="262f0-227">System-Only</span></span>            | <span data-ttu-id="262f0-228">False</span><span class="sxs-lookup"><span data-stu-id="262f0-228">False</span></span>                                        |
| <span data-ttu-id="262f0-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="262f0-229">Is-Single-Valued</span></span>       | <span data-ttu-id="262f0-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="262f0-230">True</span></span>                                         |
| <span data-ttu-id="262f0-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="262f0-231">Is Indexed</span></span>             | <span data-ttu-id="262f0-232">False</span><span class="sxs-lookup"><span data-stu-id="262f0-232">False</span></span>                                        |
| <span data-ttu-id="262f0-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="262f0-233">In Global Catalog</span></span>      | <span data-ttu-id="262f0-234">False</span><span class="sxs-lookup"><span data-stu-id="262f0-234">False</span></span>                                        |
| <span data-ttu-id="262f0-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="262f0-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="262f0-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="262f0-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="262f0-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="262f0-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="262f0-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="262f0-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="262f0-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="262f0-239">Search-Flags</span></span>           | <span data-ttu-id="262f0-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="262f0-240">0x00000000</span></span>                                   |
| <span data-ttu-id="262f0-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="262f0-241">System-Flags</span></span>           | <span data-ttu-id="262f0-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="262f0-242">0x00000010</span></span>                                   |
| <span data-ttu-id="262f0-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="262f0-243">Classes used in</span></span>        | [<span data-ttu-id="262f0-244">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="262f0-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="262f0-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="262f0-245">Windows Server 2012</span></span>



| <span data-ttu-id="262f0-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="262f0-246">Entry</span></span> | <span data-ttu-id="262f0-247">Wert</span><span class="sxs-lookup"><span data-stu-id="262f0-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="262f0-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="262f0-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="262f0-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="262f0-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="262f0-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="262f0-250">System-Only</span></span>            | <span data-ttu-id="262f0-251">False</span><span class="sxs-lookup"><span data-stu-id="262f0-251">False</span></span>                                        |
| <span data-ttu-id="262f0-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="262f0-252">Is-Single-Valued</span></span>       | <span data-ttu-id="262f0-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="262f0-253">True</span></span>                                         |
| <span data-ttu-id="262f0-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="262f0-254">Is Indexed</span></span>             | <span data-ttu-id="262f0-255">False</span><span class="sxs-lookup"><span data-stu-id="262f0-255">False</span></span>                                        |
| <span data-ttu-id="262f0-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="262f0-256">In Global Catalog</span></span>      | <span data-ttu-id="262f0-257">False</span><span class="sxs-lookup"><span data-stu-id="262f0-257">False</span></span>                                        |
| <span data-ttu-id="262f0-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="262f0-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="262f0-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="262f0-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="262f0-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="262f0-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="262f0-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="262f0-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="262f0-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="262f0-262">Search-Flags</span></span>           | <span data-ttu-id="262f0-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="262f0-263">0x00000000</span></span>                                   |
| <span data-ttu-id="262f0-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="262f0-264">System-Flags</span></span>           | <span data-ttu-id="262f0-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="262f0-265">0x00000010</span></span>                                   |
| <span data-ttu-id="262f0-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="262f0-266">Classes used in</span></span>        | [<span data-ttu-id="262f0-267">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="262f0-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





