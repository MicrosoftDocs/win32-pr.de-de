---
title: Attribut "ACS-Non-reserved-size"
description: Die tokenbucket-Größe, die eine Anwendung verwenden kann, bevor eine Reservierung erfolgt.
ms.assetid: 67a0d6fd-b556-49d2-8c5b-6efebf1052c3
ms.tgt_platform: multiple
keywords:
- AD-Schema des ACS-nicht reservierten TX-size-Attributs
- acsnonreservedtxsize-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Tx-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cd19dde97e3a9fc6ef58165c8dbcbfbebba729
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859931"
---
# <a name="acs-non-reserved-tx-size-attribute"></a><span data-ttu-id="2bb4e-105">Attribut "ACS-Non-reserved-size"</span><span class="sxs-lookup"><span data-stu-id="2bb4e-105">ACS-Non-Reserved-Tx-Size attribute</span></span>

<span data-ttu-id="2bb4e-106">Die tokenbucket-Größe, die eine Anwendung verwenden kann, bevor eine Reservierung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="2bb4e-106">The token bucket size an application can use before a reservation is in place.</span></span>



| <span data-ttu-id="2bb4e-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2bb4e-107">Entry</span></span> | <span data-ttu-id="2bb4e-108">Wert</span><span class="sxs-lookup"><span data-stu-id="2bb4e-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2bb4e-109">CN</span><span class="sxs-lookup"><span data-stu-id="2bb4e-109">CN</span></span>                | <span data-ttu-id="2bb4e-110">ACS-nicht reserviert-TX-Größe</span><span class="sxs-lookup"><span data-stu-id="2bb4e-110">ACS-Non-Reserved-Tx-Size</span></span>             |
| <span data-ttu-id="2bb4e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2bb4e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2bb4e-112">acsnonreservedtxsize</span><span class="sxs-lookup"><span data-stu-id="2bb4e-112">aCSNonReservedTxSize</span></span>                 |
| <span data-ttu-id="2bb4e-113">Size</span><span class="sxs-lookup"><span data-stu-id="2bb4e-113">Size</span></span>              | <span data-ttu-id="2bb4e-114">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="2bb4e-114">8 bytes</span></span>                              |
| <span data-ttu-id="2bb4e-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2bb4e-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="2bb4e-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="2bb4e-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2bb4e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2bb4e-117">Attribute-Id</span></span>      | <span data-ttu-id="2bb4e-118">1.2.840.113556.1.4.898</span><span class="sxs-lookup"><span data-stu-id="2bb4e-118">1.2.840.113556.1.4.898</span></span>               |
| <span data-ttu-id="2bb4e-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2bb4e-119">System-Id-Guid</span></span>    | <span data-ttu-id="2bb4e-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="2bb4e-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span></span> |
| <span data-ttu-id="2bb4e-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bb4e-121">Syntax</span></span>            | [<span data-ttu-id="2bb4e-122">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="2bb4e-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="2bb4e-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="2bb4e-123">Implementations</span></span>

-   [<span data-ttu-id="2bb4e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2bb4e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2bb4e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2bb4e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2bb4e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2bb4e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2bb4e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2bb4e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2bb4e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2bb4e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2bb4e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2bb4e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2bb4e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2bb4e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="2bb4e-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2bb4e-131">Entry</span></span> | <span data-ttu-id="2bb4e-132">Wert</span><span class="sxs-lookup"><span data-stu-id="2bb4e-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2bb4e-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2bb4e-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2bb4e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2bb4e-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2bb4e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="2bb4e-135">System-Only</span></span>            | <span data-ttu-id="2bb4e-136">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-136">False</span></span>                                        |
| <span data-ttu-id="2bb4e-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2bb4e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="2bb4e-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="2bb4e-138">True</span></span>                                         |
| <span data-ttu-id="2bb4e-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2bb4e-139">Is Indexed</span></span>             | <span data-ttu-id="2bb4e-140">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-140">False</span></span>                                        |
| <span data-ttu-id="2bb4e-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2bb4e-141">In Global Catalog</span></span>      | <span data-ttu-id="2bb4e-142">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-142">False</span></span>                                        |
| <span data-ttu-id="2bb4e-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2bb4e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="2bb4e-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2bb4e-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2bb4e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2bb4e-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2bb4e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2bb4e-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2bb4e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2bb4e-147">Search-Flags</span></span>           | <span data-ttu-id="2bb4e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2bb4e-148">0x00000000</span></span>                                   |
| <span data-ttu-id="2bb4e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2bb4e-149">System-Flags</span></span>           | <span data-ttu-id="2bb4e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2bb4e-150">0x00000010</span></span>                                   |
| <span data-ttu-id="2bb4e-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2bb4e-151">Classes used in</span></span>        | [<span data-ttu-id="2bb4e-152">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="2bb4e-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2bb4e-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2bb4e-153">Windows Server 2003</span></span>



| <span data-ttu-id="2bb4e-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2bb4e-154">Entry</span></span> | <span data-ttu-id="2bb4e-155">Wert</span><span class="sxs-lookup"><span data-stu-id="2bb4e-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2bb4e-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2bb4e-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2bb4e-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2bb4e-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2bb4e-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2bb4e-158">System-Only</span></span>            | <span data-ttu-id="2bb4e-159">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-159">False</span></span>                                        |
| <span data-ttu-id="2bb4e-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2bb4e-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2bb4e-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="2bb4e-161">True</span></span>                                         |
| <span data-ttu-id="2bb4e-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2bb4e-162">Is Indexed</span></span>             | <span data-ttu-id="2bb4e-163">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-163">False</span></span>                                        |
| <span data-ttu-id="2bb4e-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2bb4e-164">In Global Catalog</span></span>      | <span data-ttu-id="2bb4e-165">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-165">False</span></span>                                        |
| <span data-ttu-id="2bb4e-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2bb4e-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2bb4e-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2bb4e-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2bb4e-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2bb4e-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2bb4e-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2bb4e-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2bb4e-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2bb4e-170">Search-Flags</span></span>           | <span data-ttu-id="2bb4e-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2bb4e-171">0x00000000</span></span>                                   |
| <span data-ttu-id="2bb4e-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2bb4e-172">System-Flags</span></span>           | <span data-ttu-id="2bb4e-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2bb4e-173">0x00000010</span></span>                                   |
| <span data-ttu-id="2bb4e-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2bb4e-174">Classes used in</span></span>        | [<span data-ttu-id="2bb4e-175">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="2bb4e-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2bb4e-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2bb4e-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2bb4e-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2bb4e-177">Entry</span></span> | <span data-ttu-id="2bb4e-178">Wert</span><span class="sxs-lookup"><span data-stu-id="2bb4e-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2bb4e-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2bb4e-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2bb4e-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2bb4e-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2bb4e-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2bb4e-181">System-Only</span></span>            | <span data-ttu-id="2bb4e-182">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-182">False</span></span>                                        |
| <span data-ttu-id="2bb4e-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2bb4e-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2bb4e-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="2bb4e-184">True</span></span>                                         |
| <span data-ttu-id="2bb4e-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2bb4e-185">Is Indexed</span></span>             | <span data-ttu-id="2bb4e-186">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-186">False</span></span>                                        |
| <span data-ttu-id="2bb4e-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2bb4e-187">In Global Catalog</span></span>      | <span data-ttu-id="2bb4e-188">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-188">False</span></span>                                        |
| <span data-ttu-id="2bb4e-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2bb4e-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2bb4e-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2bb4e-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2bb4e-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2bb4e-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2bb4e-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2bb4e-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2bb4e-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2bb4e-193">Search-Flags</span></span>           | <span data-ttu-id="2bb4e-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2bb4e-194">0x00000000</span></span>                                   |
| <span data-ttu-id="2bb4e-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2bb4e-195">System-Flags</span></span>           | <span data-ttu-id="2bb4e-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2bb4e-196">0x00000010</span></span>                                   |
| <span data-ttu-id="2bb4e-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2bb4e-197">Classes used in</span></span>        | [<span data-ttu-id="2bb4e-198">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="2bb4e-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2bb4e-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2bb4e-199">Windows Server 2008</span></span>



| <span data-ttu-id="2bb4e-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2bb4e-200">Entry</span></span> | <span data-ttu-id="2bb4e-201">Wert</span><span class="sxs-lookup"><span data-stu-id="2bb4e-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2bb4e-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2bb4e-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2bb4e-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2bb4e-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2bb4e-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="2bb4e-204">System-Only</span></span>            | <span data-ttu-id="2bb4e-205">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-205">False</span></span>                                        |
| <span data-ttu-id="2bb4e-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2bb4e-206">Is-Single-Valued</span></span>       | <span data-ttu-id="2bb4e-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="2bb4e-207">True</span></span>                                         |
| <span data-ttu-id="2bb4e-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2bb4e-208">Is Indexed</span></span>             | <span data-ttu-id="2bb4e-209">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-209">False</span></span>                                        |
| <span data-ttu-id="2bb4e-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2bb4e-210">In Global Catalog</span></span>      | <span data-ttu-id="2bb4e-211">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-211">False</span></span>                                        |
| <span data-ttu-id="2bb4e-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2bb4e-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="2bb4e-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2bb4e-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2bb4e-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2bb4e-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2bb4e-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2bb4e-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2bb4e-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2bb4e-216">Search-Flags</span></span>           | <span data-ttu-id="2bb4e-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2bb4e-217">0x00000000</span></span>                                   |
| <span data-ttu-id="2bb4e-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2bb4e-218">System-Flags</span></span>           | <span data-ttu-id="2bb4e-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2bb4e-219">0x00000010</span></span>                                   |
| <span data-ttu-id="2bb4e-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2bb4e-220">Classes used in</span></span>        | [<span data-ttu-id="2bb4e-221">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="2bb4e-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2bb4e-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2bb4e-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2bb4e-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2bb4e-223">Entry</span></span> | <span data-ttu-id="2bb4e-224">Wert</span><span class="sxs-lookup"><span data-stu-id="2bb4e-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2bb4e-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2bb4e-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2bb4e-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2bb4e-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2bb4e-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="2bb4e-227">System-Only</span></span>            | <span data-ttu-id="2bb4e-228">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-228">False</span></span>                                        |
| <span data-ttu-id="2bb4e-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2bb4e-229">Is-Single-Valued</span></span>       | <span data-ttu-id="2bb4e-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="2bb4e-230">True</span></span>                                         |
| <span data-ttu-id="2bb4e-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2bb4e-231">Is Indexed</span></span>             | <span data-ttu-id="2bb4e-232">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-232">False</span></span>                                        |
| <span data-ttu-id="2bb4e-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2bb4e-233">In Global Catalog</span></span>      | <span data-ttu-id="2bb4e-234">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-234">False</span></span>                                        |
| <span data-ttu-id="2bb4e-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2bb4e-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="2bb4e-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2bb4e-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2bb4e-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2bb4e-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2bb4e-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2bb4e-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2bb4e-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2bb4e-239">Search-Flags</span></span>           | <span data-ttu-id="2bb4e-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2bb4e-240">0x00000000</span></span>                                   |
| <span data-ttu-id="2bb4e-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2bb4e-241">System-Flags</span></span>           | <span data-ttu-id="2bb4e-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2bb4e-242">0x00000010</span></span>                                   |
| <span data-ttu-id="2bb4e-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2bb4e-243">Classes used in</span></span>        | [<span data-ttu-id="2bb4e-244">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="2bb4e-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2bb4e-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2bb4e-245">Windows Server 2012</span></span>



| <span data-ttu-id="2bb4e-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2bb4e-246">Entry</span></span> | <span data-ttu-id="2bb4e-247">Wert</span><span class="sxs-lookup"><span data-stu-id="2bb4e-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2bb4e-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2bb4e-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2bb4e-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2bb4e-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2bb4e-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="2bb4e-250">System-Only</span></span>            | <span data-ttu-id="2bb4e-251">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-251">False</span></span>                                        |
| <span data-ttu-id="2bb4e-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2bb4e-252">Is-Single-Valued</span></span>       | <span data-ttu-id="2bb4e-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="2bb4e-253">True</span></span>                                         |
| <span data-ttu-id="2bb4e-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2bb4e-254">Is Indexed</span></span>             | <span data-ttu-id="2bb4e-255">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-255">False</span></span>                                        |
| <span data-ttu-id="2bb4e-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2bb4e-256">In Global Catalog</span></span>      | <span data-ttu-id="2bb4e-257">False</span><span class="sxs-lookup"><span data-stu-id="2bb4e-257">False</span></span>                                        |
| <span data-ttu-id="2bb4e-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2bb4e-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="2bb4e-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2bb4e-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2bb4e-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2bb4e-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2bb4e-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2bb4e-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2bb4e-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2bb4e-262">Search-Flags</span></span>           | <span data-ttu-id="2bb4e-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2bb4e-263">0x00000000</span></span>                                   |
| <span data-ttu-id="2bb4e-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2bb4e-264">System-Flags</span></span>           | <span data-ttu-id="2bb4e-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2bb4e-265">0x00000010</span></span>                                   |
| <span data-ttu-id="2bb4e-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2bb4e-266">Classes used in</span></span>        | [<span data-ttu-id="2bb4e-267">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="2bb4e-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





