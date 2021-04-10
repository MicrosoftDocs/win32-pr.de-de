---
title: ACS-Berechtigung-Bits-Attribut
description: Ermöglicht die Verwendung von Multicast Flüssen für einen bestimmten Benutzer.
ms.assetid: c7e7866d-b906-4a64-bd51-4e9cc7b8fb86
ms.tgt_platform: multiple
keywords:
- AD-Schema des ACS-Berechtigungs Bits-Attributs
- acspermissionbits-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- ACS-Permission-Bits
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a27370178dd46fd50df44b1226686db5a70a846
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107324"
---
# <a name="acs-permission-bits-attribute"></a><span data-ttu-id="3c6ef-105">ACS-Berechtigung-Bits-Attribut</span><span class="sxs-lookup"><span data-stu-id="3c6ef-105">ACS-Permission-Bits attribute</span></span>

<span data-ttu-id="3c6ef-106">Ermöglicht die Verwendung von Multicast Flüssen für einen bestimmten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="3c6ef-106">Allows multicast flow origination for a given user.</span></span>



| <span data-ttu-id="3c6ef-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3c6ef-107">Entry</span></span> | <span data-ttu-id="3c6ef-108">Wert</span><span class="sxs-lookup"><span data-stu-id="3c6ef-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="3c6ef-109">CN</span><span class="sxs-lookup"><span data-stu-id="3c6ef-109">CN</span></span>                | <span data-ttu-id="3c6ef-110">ACS-Berechtigung (Bits)</span><span class="sxs-lookup"><span data-stu-id="3c6ef-110">ACS-Permission-Bits</span></span>                  |
| <span data-ttu-id="3c6ef-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3c6ef-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3c6ef-112">acspermissionbits</span><span class="sxs-lookup"><span data-stu-id="3c6ef-112">aCSPermissionBits</span></span>                    |
| <span data-ttu-id="3c6ef-113">Size</span><span class="sxs-lookup"><span data-stu-id="3c6ef-113">Size</span></span>              | <span data-ttu-id="3c6ef-114">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="3c6ef-114">8 bytes</span></span>                              |
| <span data-ttu-id="3c6ef-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="3c6ef-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="3c6ef-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="3c6ef-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="3c6ef-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3c6ef-117">Attribute-Id</span></span>      | <span data-ttu-id="3c6ef-118">1.2.840.113556.1.4.765</span><span class="sxs-lookup"><span data-stu-id="3c6ef-118">1.2.840.113556.1.4.765</span></span>               |
| <span data-ttu-id="3c6ef-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3c6ef-119">System-Id-Guid</span></span>    | <span data-ttu-id="3c6ef-120">7b561282-5301-11d1-a9c5-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="3c6ef-120">7f561282-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="3c6ef-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c6ef-121">Syntax</span></span>            | [<span data-ttu-id="3c6ef-122">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="3c6ef-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="3c6ef-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="3c6ef-123">Implementations</span></span>

-   [<span data-ttu-id="3c6ef-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3c6ef-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3c6ef-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3c6ef-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3c6ef-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3c6ef-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3c6ef-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3c6ef-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3c6ef-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3c6ef-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3c6ef-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3c6ef-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3c6ef-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3c6ef-130">Windows 2000 Server</span></span>



| <span data-ttu-id="3c6ef-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3c6ef-131">Entry</span></span> | <span data-ttu-id="3c6ef-132">Wert</span><span class="sxs-lookup"><span data-stu-id="3c6ef-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3c6ef-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3c6ef-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3c6ef-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c6ef-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3c6ef-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c6ef-135">System-Only</span></span>            | <span data-ttu-id="3c6ef-136">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-136">False</span></span>                                        |
| <span data-ttu-id="3c6ef-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3c6ef-137">Is-Single-Valued</span></span>       | <span data-ttu-id="3c6ef-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="3c6ef-138">True</span></span>                                         |
| <span data-ttu-id="3c6ef-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3c6ef-139">Is Indexed</span></span>             | <span data-ttu-id="3c6ef-140">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-140">False</span></span>                                        |
| <span data-ttu-id="3c6ef-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3c6ef-141">In Global Catalog</span></span>      | <span data-ttu-id="3c6ef-142">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-142">False</span></span>                                        |
| <span data-ttu-id="3c6ef-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3c6ef-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c6ef-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3c6ef-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3c6ef-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c6ef-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3c6ef-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c6ef-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3c6ef-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c6ef-147">Search-Flags</span></span>           | <span data-ttu-id="3c6ef-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c6ef-148">0x00000000</span></span>                                   |
| <span data-ttu-id="3c6ef-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c6ef-149">System-Flags</span></span>           | <span data-ttu-id="3c6ef-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c6ef-150">0x00000010</span></span>                                   |
| <span data-ttu-id="3c6ef-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3c6ef-151">Classes used in</span></span>        | [<span data-ttu-id="3c6ef-152">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="3c6ef-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3c6ef-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3c6ef-153">Windows Server 2003</span></span>



| <span data-ttu-id="3c6ef-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3c6ef-154">Entry</span></span> | <span data-ttu-id="3c6ef-155">Wert</span><span class="sxs-lookup"><span data-stu-id="3c6ef-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3c6ef-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3c6ef-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3c6ef-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c6ef-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3c6ef-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c6ef-158">System-Only</span></span>            | <span data-ttu-id="3c6ef-159">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-159">False</span></span>                                        |
| <span data-ttu-id="3c6ef-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3c6ef-160">Is-Single-Valued</span></span>       | <span data-ttu-id="3c6ef-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="3c6ef-161">True</span></span>                                         |
| <span data-ttu-id="3c6ef-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3c6ef-162">Is Indexed</span></span>             | <span data-ttu-id="3c6ef-163">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-163">False</span></span>                                        |
| <span data-ttu-id="3c6ef-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3c6ef-164">In Global Catalog</span></span>      | <span data-ttu-id="3c6ef-165">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-165">False</span></span>                                        |
| <span data-ttu-id="3c6ef-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3c6ef-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c6ef-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3c6ef-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3c6ef-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c6ef-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3c6ef-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c6ef-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3c6ef-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c6ef-170">Search-Flags</span></span>           | <span data-ttu-id="3c6ef-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c6ef-171">0x00000000</span></span>                                   |
| <span data-ttu-id="3c6ef-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c6ef-172">System-Flags</span></span>           | <span data-ttu-id="3c6ef-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c6ef-173">0x00000010</span></span>                                   |
| <span data-ttu-id="3c6ef-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3c6ef-174">Classes used in</span></span>        | [<span data-ttu-id="3c6ef-175">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="3c6ef-175">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3c6ef-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3c6ef-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3c6ef-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3c6ef-177">Entry</span></span> | <span data-ttu-id="3c6ef-178">Wert</span><span class="sxs-lookup"><span data-stu-id="3c6ef-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3c6ef-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3c6ef-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3c6ef-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c6ef-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3c6ef-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c6ef-181">System-Only</span></span>            | <span data-ttu-id="3c6ef-182">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-182">False</span></span>                                        |
| <span data-ttu-id="3c6ef-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3c6ef-183">Is-Single-Valued</span></span>       | <span data-ttu-id="3c6ef-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="3c6ef-184">True</span></span>                                         |
| <span data-ttu-id="3c6ef-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3c6ef-185">Is Indexed</span></span>             | <span data-ttu-id="3c6ef-186">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-186">False</span></span>                                        |
| <span data-ttu-id="3c6ef-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3c6ef-187">In Global Catalog</span></span>      | <span data-ttu-id="3c6ef-188">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-188">False</span></span>                                        |
| <span data-ttu-id="3c6ef-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3c6ef-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c6ef-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3c6ef-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3c6ef-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c6ef-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3c6ef-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c6ef-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3c6ef-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c6ef-193">Search-Flags</span></span>           | <span data-ttu-id="3c6ef-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c6ef-194">0x00000000</span></span>                                   |
| <span data-ttu-id="3c6ef-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c6ef-195">System-Flags</span></span>           | <span data-ttu-id="3c6ef-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c6ef-196">0x00000010</span></span>                                   |
| <span data-ttu-id="3c6ef-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3c6ef-197">Classes used in</span></span>        | [<span data-ttu-id="3c6ef-198">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="3c6ef-198">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3c6ef-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c6ef-199">Windows Server 2008</span></span>



| <span data-ttu-id="3c6ef-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3c6ef-200">Entry</span></span> | <span data-ttu-id="3c6ef-201">Wert</span><span class="sxs-lookup"><span data-stu-id="3c6ef-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3c6ef-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3c6ef-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3c6ef-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c6ef-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3c6ef-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c6ef-204">System-Only</span></span>            | <span data-ttu-id="3c6ef-205">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-205">False</span></span>                                        |
| <span data-ttu-id="3c6ef-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3c6ef-206">Is-Single-Valued</span></span>       | <span data-ttu-id="3c6ef-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="3c6ef-207">True</span></span>                                         |
| <span data-ttu-id="3c6ef-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3c6ef-208">Is Indexed</span></span>             | <span data-ttu-id="3c6ef-209">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-209">False</span></span>                                        |
| <span data-ttu-id="3c6ef-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3c6ef-210">In Global Catalog</span></span>      | <span data-ttu-id="3c6ef-211">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-211">False</span></span>                                        |
| <span data-ttu-id="3c6ef-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3c6ef-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c6ef-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3c6ef-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3c6ef-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c6ef-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3c6ef-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c6ef-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3c6ef-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c6ef-216">Search-Flags</span></span>           | <span data-ttu-id="3c6ef-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c6ef-217">0x00000000</span></span>                                   |
| <span data-ttu-id="3c6ef-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c6ef-218">System-Flags</span></span>           | <span data-ttu-id="3c6ef-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c6ef-219">0x00000010</span></span>                                   |
| <span data-ttu-id="3c6ef-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3c6ef-220">Classes used in</span></span>        | [<span data-ttu-id="3c6ef-221">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="3c6ef-221">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3c6ef-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3c6ef-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3c6ef-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3c6ef-223">Entry</span></span> | <span data-ttu-id="3c6ef-224">Wert</span><span class="sxs-lookup"><span data-stu-id="3c6ef-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3c6ef-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3c6ef-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3c6ef-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c6ef-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3c6ef-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c6ef-227">System-Only</span></span>            | <span data-ttu-id="3c6ef-228">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-228">False</span></span>                                        |
| <span data-ttu-id="3c6ef-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3c6ef-229">Is-Single-Valued</span></span>       | <span data-ttu-id="3c6ef-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="3c6ef-230">True</span></span>                                         |
| <span data-ttu-id="3c6ef-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3c6ef-231">Is Indexed</span></span>             | <span data-ttu-id="3c6ef-232">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-232">False</span></span>                                        |
| <span data-ttu-id="3c6ef-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3c6ef-233">In Global Catalog</span></span>      | <span data-ttu-id="3c6ef-234">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-234">False</span></span>                                        |
| <span data-ttu-id="3c6ef-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3c6ef-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c6ef-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3c6ef-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3c6ef-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c6ef-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3c6ef-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c6ef-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3c6ef-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c6ef-239">Search-Flags</span></span>           | <span data-ttu-id="3c6ef-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c6ef-240">0x00000000</span></span>                                   |
| <span data-ttu-id="3c6ef-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c6ef-241">System-Flags</span></span>           | <span data-ttu-id="3c6ef-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c6ef-242">0x00000010</span></span>                                   |
| <span data-ttu-id="3c6ef-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3c6ef-243">Classes used in</span></span>        | [<span data-ttu-id="3c6ef-244">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="3c6ef-244">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3c6ef-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3c6ef-245">Windows Server 2012</span></span>



| <span data-ttu-id="3c6ef-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3c6ef-246">Entry</span></span> | <span data-ttu-id="3c6ef-247">Wert</span><span class="sxs-lookup"><span data-stu-id="3c6ef-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3c6ef-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3c6ef-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3c6ef-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c6ef-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3c6ef-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c6ef-250">System-Only</span></span>            | <span data-ttu-id="3c6ef-251">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-251">False</span></span>                                        |
| <span data-ttu-id="3c6ef-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3c6ef-252">Is-Single-Valued</span></span>       | <span data-ttu-id="3c6ef-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="3c6ef-253">True</span></span>                                         |
| <span data-ttu-id="3c6ef-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3c6ef-254">Is Indexed</span></span>             | <span data-ttu-id="3c6ef-255">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-255">False</span></span>                                        |
| <span data-ttu-id="3c6ef-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3c6ef-256">In Global Catalog</span></span>      | <span data-ttu-id="3c6ef-257">False</span><span class="sxs-lookup"><span data-stu-id="3c6ef-257">False</span></span>                                        |
| <span data-ttu-id="3c6ef-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3c6ef-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c6ef-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3c6ef-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3c6ef-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c6ef-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3c6ef-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c6ef-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3c6ef-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c6ef-262">Search-Flags</span></span>           | <span data-ttu-id="3c6ef-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c6ef-263">0x00000000</span></span>                                   |
| <span data-ttu-id="3c6ef-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c6ef-264">System-Flags</span></span>           | <span data-ttu-id="3c6ef-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c6ef-265">0x00000010</span></span>                                   |
| <span data-ttu-id="3c6ef-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3c6ef-266">Classes used in</span></span>        | [<span data-ttu-id="3c6ef-267">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="3c6ef-267">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





