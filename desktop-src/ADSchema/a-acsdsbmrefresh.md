---
title: ACS-DSBM-Refresh-Attribut
description: Dieses Attribut enthält den Zeit Geber Wert des Intervalls, der bestimmt, wann der designierte subnetzbandbreiten-Manager (DSBM) eine Aktualisierungs Nachricht ( \_ \_ DSBM) an alle subnetzbandbreiten-Manager in einer Domäne sendet.
ms.assetid: 018fd748-ca2e-41e1-a920-224a32e13e21
ms.tgt_platform: multiple
keywords:
- AD-Schema für ACS-DSBM-Refresh-Attribut
- acsdsbmrefresh-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- ACS-DSBM-Refresh
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d662b886a8c97f3d155d3c1b40efcef67f7f1f0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957396"
---
# <a name="acs-dsbm-refresh-attribute"></a><span data-ttu-id="81071-105">ACS-DSBM-Refresh-Attribut</span><span class="sxs-lookup"><span data-stu-id="81071-105">ACS-DSBM-Refresh attribute</span></span>

<span data-ttu-id="81071-106">Dieses Attribut enthält den Zeit Geber Wert des Intervalls, der bestimmt, wann der designierte subnetzbandbreiten-Manager (DSBM) eine Aktualisierungs Nachricht ( \_ \_ DSBM) an alle subnetzbandbreiten-Manager in einer Domäne sendet.</span><span class="sxs-lookup"><span data-stu-id="81071-106">This attribute contains the interval timer value that determines when the Designated Subnet Bandwidth Manager (DSBM) sends out a refresh message (I\_AM\_DSBM) to all of the Subnet Bandwidth Managers in a domain.</span></span>



| <span data-ttu-id="81071-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="81071-107">Entry</span></span> | <span data-ttu-id="81071-108">Wert</span><span class="sxs-lookup"><span data-stu-id="81071-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="81071-109">CN</span><span class="sxs-lookup"><span data-stu-id="81071-109">CN</span></span>                | <span data-ttu-id="81071-110">ACS-DSBM-aktualisieren</span><span class="sxs-lookup"><span data-stu-id="81071-110">ACS-DSBM-Refresh</span></span>                     |
| <span data-ttu-id="81071-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="81071-111">Ldap-Display-Name</span></span> | <span data-ttu-id="81071-112">acsdsbmrefresh</span><span class="sxs-lookup"><span data-stu-id="81071-112">aCSDSBMRefresh</span></span>                       |
| <span data-ttu-id="81071-113">Size</span><span class="sxs-lookup"><span data-stu-id="81071-113">Size</span></span>              | <span data-ttu-id="81071-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="81071-114">4 bytes</span></span>                              |
| <span data-ttu-id="81071-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="81071-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="81071-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="81071-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="81071-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="81071-117">Attribute-Id</span></span>      | <span data-ttu-id="81071-118">1.2.840.113556.1.4.777</span><span class="sxs-lookup"><span data-stu-id="81071-118">1.2.840.113556.1.4.777</span></span>               |
| <span data-ttu-id="81071-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="81071-119">System-Id-Guid</span></span>    | <span data-ttu-id="81071-120">1cb3559b-56d0-11d1-a9c6-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="81071-120">1cb3559f-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="81071-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="81071-121">Syntax</span></span>            | [<span data-ttu-id="81071-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="81071-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="81071-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="81071-123">Implementations</span></span>

-   [<span data-ttu-id="81071-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="81071-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="81071-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="81071-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="81071-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="81071-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="81071-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="81071-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="81071-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="81071-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="81071-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="81071-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="81071-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="81071-130">Windows 2000 Server</span></span>



| <span data-ttu-id="81071-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="81071-131">Entry</span></span> | <span data-ttu-id="81071-132">Wert</span><span class="sxs-lookup"><span data-stu-id="81071-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="81071-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="81071-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="81071-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81071-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="81071-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="81071-135">System-Only</span></span>            | <span data-ttu-id="81071-136">False</span><span class="sxs-lookup"><span data-stu-id="81071-136">False</span></span>                                        |
| <span data-ttu-id="81071-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="81071-137">Is-Single-Valued</span></span>       | <span data-ttu-id="81071-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="81071-138">True</span></span>                                         |
| <span data-ttu-id="81071-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="81071-139">Is Indexed</span></span>             | <span data-ttu-id="81071-140">False</span><span class="sxs-lookup"><span data-stu-id="81071-140">False</span></span>                                        |
| <span data-ttu-id="81071-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="81071-141">In Global Catalog</span></span>      | <span data-ttu-id="81071-142">False</span><span class="sxs-lookup"><span data-stu-id="81071-142">False</span></span>                                        |
| <span data-ttu-id="81071-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="81071-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="81071-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="81071-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="81071-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81071-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="81071-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81071-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="81071-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81071-147">Search-Flags</span></span>           | <span data-ttu-id="81071-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81071-148">0x00000000</span></span>                                   |
| <span data-ttu-id="81071-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81071-149">System-Flags</span></span>           | <span data-ttu-id="81071-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81071-150">0x00000010</span></span>                                   |
| <span data-ttu-id="81071-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="81071-151">Classes used in</span></span>        | [<span data-ttu-id="81071-152">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="81071-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="81071-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="81071-153">Windows Server 2003</span></span>



| <span data-ttu-id="81071-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="81071-154">Entry</span></span> | <span data-ttu-id="81071-155">Wert</span><span class="sxs-lookup"><span data-stu-id="81071-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="81071-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="81071-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="81071-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81071-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="81071-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="81071-158">System-Only</span></span>            | <span data-ttu-id="81071-159">False</span><span class="sxs-lookup"><span data-stu-id="81071-159">False</span></span>                                        |
| <span data-ttu-id="81071-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="81071-160">Is-Single-Valued</span></span>       | <span data-ttu-id="81071-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="81071-161">True</span></span>                                         |
| <span data-ttu-id="81071-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="81071-162">Is Indexed</span></span>             | <span data-ttu-id="81071-163">False</span><span class="sxs-lookup"><span data-stu-id="81071-163">False</span></span>                                        |
| <span data-ttu-id="81071-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="81071-164">In Global Catalog</span></span>      | <span data-ttu-id="81071-165">False</span><span class="sxs-lookup"><span data-stu-id="81071-165">False</span></span>                                        |
| <span data-ttu-id="81071-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="81071-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="81071-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="81071-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="81071-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81071-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="81071-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81071-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="81071-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81071-170">Search-Flags</span></span>           | <span data-ttu-id="81071-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81071-171">0x00000000</span></span>                                   |
| <span data-ttu-id="81071-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81071-172">System-Flags</span></span>           | <span data-ttu-id="81071-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81071-173">0x00000010</span></span>                                   |
| <span data-ttu-id="81071-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="81071-174">Classes used in</span></span>        | [<span data-ttu-id="81071-175">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="81071-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="81071-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="81071-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="81071-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="81071-177">Entry</span></span> | <span data-ttu-id="81071-178">Wert</span><span class="sxs-lookup"><span data-stu-id="81071-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="81071-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="81071-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="81071-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81071-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="81071-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="81071-181">System-Only</span></span>            | <span data-ttu-id="81071-182">False</span><span class="sxs-lookup"><span data-stu-id="81071-182">False</span></span>                                        |
| <span data-ttu-id="81071-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="81071-183">Is-Single-Valued</span></span>       | <span data-ttu-id="81071-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="81071-184">True</span></span>                                         |
| <span data-ttu-id="81071-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="81071-185">Is Indexed</span></span>             | <span data-ttu-id="81071-186">False</span><span class="sxs-lookup"><span data-stu-id="81071-186">False</span></span>                                        |
| <span data-ttu-id="81071-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="81071-187">In Global Catalog</span></span>      | <span data-ttu-id="81071-188">False</span><span class="sxs-lookup"><span data-stu-id="81071-188">False</span></span>                                        |
| <span data-ttu-id="81071-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="81071-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="81071-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="81071-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="81071-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81071-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="81071-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81071-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="81071-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81071-193">Search-Flags</span></span>           | <span data-ttu-id="81071-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81071-194">0x00000000</span></span>                                   |
| <span data-ttu-id="81071-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81071-195">System-Flags</span></span>           | <span data-ttu-id="81071-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81071-196">0x00000010</span></span>                                   |
| <span data-ttu-id="81071-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="81071-197">Classes used in</span></span>        | [<span data-ttu-id="81071-198">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="81071-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="81071-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81071-199">Windows Server 2008</span></span>



| <span data-ttu-id="81071-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="81071-200">Entry</span></span> | <span data-ttu-id="81071-201">Wert</span><span class="sxs-lookup"><span data-stu-id="81071-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="81071-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="81071-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="81071-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81071-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="81071-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="81071-204">System-Only</span></span>            | <span data-ttu-id="81071-205">False</span><span class="sxs-lookup"><span data-stu-id="81071-205">False</span></span>                                        |
| <span data-ttu-id="81071-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="81071-206">Is-Single-Valued</span></span>       | <span data-ttu-id="81071-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="81071-207">True</span></span>                                         |
| <span data-ttu-id="81071-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="81071-208">Is Indexed</span></span>             | <span data-ttu-id="81071-209">False</span><span class="sxs-lookup"><span data-stu-id="81071-209">False</span></span>                                        |
| <span data-ttu-id="81071-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="81071-210">In Global Catalog</span></span>      | <span data-ttu-id="81071-211">False</span><span class="sxs-lookup"><span data-stu-id="81071-211">False</span></span>                                        |
| <span data-ttu-id="81071-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="81071-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="81071-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="81071-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="81071-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81071-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="81071-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81071-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="81071-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81071-216">Search-Flags</span></span>           | <span data-ttu-id="81071-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81071-217">0x00000000</span></span>                                   |
| <span data-ttu-id="81071-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81071-218">System-Flags</span></span>           | <span data-ttu-id="81071-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81071-219">0x00000010</span></span>                                   |
| <span data-ttu-id="81071-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="81071-220">Classes used in</span></span>        | [<span data-ttu-id="81071-221">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="81071-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="81071-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="81071-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="81071-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="81071-223">Entry</span></span> | <span data-ttu-id="81071-224">Wert</span><span class="sxs-lookup"><span data-stu-id="81071-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="81071-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="81071-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="81071-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81071-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="81071-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="81071-227">System-Only</span></span>            | <span data-ttu-id="81071-228">False</span><span class="sxs-lookup"><span data-stu-id="81071-228">False</span></span>                                        |
| <span data-ttu-id="81071-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="81071-229">Is-Single-Valued</span></span>       | <span data-ttu-id="81071-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="81071-230">True</span></span>                                         |
| <span data-ttu-id="81071-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="81071-231">Is Indexed</span></span>             | <span data-ttu-id="81071-232">False</span><span class="sxs-lookup"><span data-stu-id="81071-232">False</span></span>                                        |
| <span data-ttu-id="81071-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="81071-233">In Global Catalog</span></span>      | <span data-ttu-id="81071-234">False</span><span class="sxs-lookup"><span data-stu-id="81071-234">False</span></span>                                        |
| <span data-ttu-id="81071-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="81071-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="81071-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="81071-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="81071-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81071-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="81071-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81071-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="81071-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81071-239">Search-Flags</span></span>           | <span data-ttu-id="81071-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81071-240">0x00000000</span></span>                                   |
| <span data-ttu-id="81071-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81071-241">System-Flags</span></span>           | <span data-ttu-id="81071-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81071-242">0x00000010</span></span>                                   |
| <span data-ttu-id="81071-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="81071-243">Classes used in</span></span>        | [<span data-ttu-id="81071-244">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="81071-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="81071-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81071-245">Windows Server 2012</span></span>



| <span data-ttu-id="81071-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="81071-246">Entry</span></span> | <span data-ttu-id="81071-247">Wert</span><span class="sxs-lookup"><span data-stu-id="81071-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="81071-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="81071-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="81071-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81071-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="81071-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="81071-250">System-Only</span></span>            | <span data-ttu-id="81071-251">False</span><span class="sxs-lookup"><span data-stu-id="81071-251">False</span></span>                                        |
| <span data-ttu-id="81071-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="81071-252">Is-Single-Valued</span></span>       | <span data-ttu-id="81071-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="81071-253">True</span></span>                                         |
| <span data-ttu-id="81071-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="81071-254">Is Indexed</span></span>             | <span data-ttu-id="81071-255">False</span><span class="sxs-lookup"><span data-stu-id="81071-255">False</span></span>                                        |
| <span data-ttu-id="81071-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="81071-256">In Global Catalog</span></span>      | <span data-ttu-id="81071-257">False</span><span class="sxs-lookup"><span data-stu-id="81071-257">False</span></span>                                        |
| <span data-ttu-id="81071-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="81071-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="81071-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="81071-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="81071-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81071-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="81071-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81071-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="81071-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81071-262">Search-Flags</span></span>           | <span data-ttu-id="81071-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81071-263">0x00000000</span></span>                                   |
| <span data-ttu-id="81071-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81071-264">System-Flags</span></span>           | <span data-ttu-id="81071-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81071-265">0x00000010</span></span>                                   |
| <span data-ttu-id="81071-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="81071-266">Classes used in</span></span>        | [<span data-ttu-id="81071-267">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="81071-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





