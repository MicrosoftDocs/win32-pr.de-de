---
title: LSA-Erstellungszeit Attribut
description: Das LSA-Creation-time-Attribut wird zur Unterstützung der Replikation in Windows NT 4,0-Domänen verwendet.
ms.assetid: a5446cbf-aa35-4ea6-a2e0-9d0ea58edaf1
ms.tgt_platform: multiple
keywords:
- LSA-Erstellungszeit Attribut AD-Schema
- AD-Schema des lsacreationtime-Attributs
topic_type:
- apiref
api_name:
- LSA-Creation-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f32092e7d71d02807f4700d381da0ce099ccaf7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392254"
---
# <a name="lsa-creation-time-attribute"></a><span data-ttu-id="753cf-105">LSA-Erstellungszeit Attribut</span><span class="sxs-lookup"><span data-stu-id="753cf-105">LSA-Creation-Time attribute</span></span>

<span data-ttu-id="753cf-106">Das **LSA-Creation-time** -Attribut wird zur Unterstützung der Replikation in Windows NT 4,0-Domänen verwendet.</span><span class="sxs-lookup"><span data-stu-id="753cf-106">The **LSA-Creation-Time** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="753cf-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="753cf-107">Entry</span></span> | <span data-ttu-id="753cf-108">Wert</span><span class="sxs-lookup"><span data-stu-id="753cf-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="753cf-109">CN</span><span class="sxs-lookup"><span data-stu-id="753cf-109">CN</span></span>                | <span data-ttu-id="753cf-110">LSA-Erstellungszeit</span><span class="sxs-lookup"><span data-stu-id="753cf-110">LSA-Creation-Time</span></span>                    |
| <span data-ttu-id="753cf-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="753cf-111">Ldap-Display-Name</span></span> | <span data-ttu-id="753cf-112">lsacreationtime</span><span class="sxs-lookup"><span data-stu-id="753cf-112">lSACreationTime</span></span>                      |
| <span data-ttu-id="753cf-113">Size</span><span class="sxs-lookup"><span data-stu-id="753cf-113">Size</span></span>              | <span data-ttu-id="753cf-114">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="753cf-114">8 bytes</span></span>                              |
| <span data-ttu-id="753cf-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="753cf-115">Update Privilege</span></span>  | <span data-ttu-id="753cf-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="753cf-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="753cf-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="753cf-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="753cf-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="753cf-118">Attribute-Id</span></span>      | <span data-ttu-id="753cf-119">1.2.840.113556.1.4.66</span><span class="sxs-lookup"><span data-stu-id="753cf-119">1.2.840.113556.1.4.66</span></span>                |
| <span data-ttu-id="753cf-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="753cf-120">System-Id-Guid</span></span>    | <span data-ttu-id="753cf-121">bf9679ad-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="753cf-121">bf9679ad-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="753cf-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="753cf-122">Syntax</span></span>            | [<span data-ttu-id="753cf-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="753cf-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="753cf-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="753cf-124">Implementations</span></span>

-   [<span data-ttu-id="753cf-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="753cf-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="753cf-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="753cf-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="753cf-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="753cf-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="753cf-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="753cf-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="753cf-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="753cf-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="753cf-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="753cf-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="753cf-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="753cf-131">Windows 2000 Server</span></span>



| <span data-ttu-id="753cf-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="753cf-132">Entry</span></span> | <span data-ttu-id="753cf-133">Wert</span><span class="sxs-lookup"><span data-stu-id="753cf-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="753cf-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="753cf-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="753cf-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="753cf-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="753cf-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="753cf-136">System-Only</span></span>            | <span data-ttu-id="753cf-137">False</span><span class="sxs-lookup"><span data-stu-id="753cf-137">False</span></span>                                        |
| <span data-ttu-id="753cf-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="753cf-138">Is-Single-Valued</span></span>       | <span data-ttu-id="753cf-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="753cf-139">True</span></span>                                         |
| <span data-ttu-id="753cf-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="753cf-140">Is Indexed</span></span>             | <span data-ttu-id="753cf-141">False</span><span class="sxs-lookup"><span data-stu-id="753cf-141">False</span></span>                                        |
| <span data-ttu-id="753cf-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="753cf-142">In Global Catalog</span></span>      | <span data-ttu-id="753cf-143">False</span><span class="sxs-lookup"><span data-stu-id="753cf-143">False</span></span>                                        |
| <span data-ttu-id="753cf-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="753cf-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="753cf-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="753cf-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="753cf-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="753cf-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="753cf-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="753cf-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="753cf-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="753cf-148">Search-Flags</span></span>           | <span data-ttu-id="753cf-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="753cf-149">0x00000000</span></span>                                   |
| <span data-ttu-id="753cf-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="753cf-150">System-Flags</span></span>           | <span data-ttu-id="753cf-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="753cf-151">0x00000010</span></span>                                   |
| <span data-ttu-id="753cf-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="753cf-152">Classes used in</span></span>        | [<span data-ttu-id="753cf-153">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="753cf-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="753cf-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="753cf-154">Windows Server 2003</span></span>



| <span data-ttu-id="753cf-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="753cf-155">Entry</span></span> | <span data-ttu-id="753cf-156">Wert</span><span class="sxs-lookup"><span data-stu-id="753cf-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="753cf-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="753cf-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="753cf-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="753cf-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="753cf-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="753cf-159">System-Only</span></span>            | <span data-ttu-id="753cf-160">False</span><span class="sxs-lookup"><span data-stu-id="753cf-160">False</span></span>                                        |
| <span data-ttu-id="753cf-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="753cf-161">Is-Single-Valued</span></span>       | <span data-ttu-id="753cf-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="753cf-162">True</span></span>                                         |
| <span data-ttu-id="753cf-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="753cf-163">Is Indexed</span></span>             | <span data-ttu-id="753cf-164">False</span><span class="sxs-lookup"><span data-stu-id="753cf-164">False</span></span>                                        |
| <span data-ttu-id="753cf-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="753cf-165">In Global Catalog</span></span>      | <span data-ttu-id="753cf-166">False</span><span class="sxs-lookup"><span data-stu-id="753cf-166">False</span></span>                                        |
| <span data-ttu-id="753cf-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="753cf-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="753cf-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="753cf-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="753cf-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="753cf-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="753cf-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="753cf-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="753cf-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="753cf-171">Search-Flags</span></span>           | <span data-ttu-id="753cf-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="753cf-172">0x00000000</span></span>                                   |
| <span data-ttu-id="753cf-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="753cf-173">System-Flags</span></span>           | <span data-ttu-id="753cf-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="753cf-174">0x00000010</span></span>                                   |
| <span data-ttu-id="753cf-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="753cf-175">Classes used in</span></span>        | [<span data-ttu-id="753cf-176">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="753cf-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="753cf-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="753cf-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="753cf-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="753cf-178">Entry</span></span> | <span data-ttu-id="753cf-179">Wert</span><span class="sxs-lookup"><span data-stu-id="753cf-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="753cf-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="753cf-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="753cf-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="753cf-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="753cf-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="753cf-182">System-Only</span></span>            | <span data-ttu-id="753cf-183">False</span><span class="sxs-lookup"><span data-stu-id="753cf-183">False</span></span>                                        |
| <span data-ttu-id="753cf-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="753cf-184">Is-Single-Valued</span></span>       | <span data-ttu-id="753cf-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="753cf-185">True</span></span>                                         |
| <span data-ttu-id="753cf-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="753cf-186">Is Indexed</span></span>             | <span data-ttu-id="753cf-187">False</span><span class="sxs-lookup"><span data-stu-id="753cf-187">False</span></span>                                        |
| <span data-ttu-id="753cf-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="753cf-188">In Global Catalog</span></span>      | <span data-ttu-id="753cf-189">False</span><span class="sxs-lookup"><span data-stu-id="753cf-189">False</span></span>                                        |
| <span data-ttu-id="753cf-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="753cf-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="753cf-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="753cf-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="753cf-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="753cf-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="753cf-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="753cf-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="753cf-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="753cf-194">Search-Flags</span></span>           | <span data-ttu-id="753cf-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="753cf-195">0x00000000</span></span>                                   |
| <span data-ttu-id="753cf-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="753cf-196">System-Flags</span></span>           | <span data-ttu-id="753cf-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="753cf-197">0x00000010</span></span>                                   |
| <span data-ttu-id="753cf-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="753cf-198">Classes used in</span></span>        | [<span data-ttu-id="753cf-199">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="753cf-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="753cf-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="753cf-200">Windows Server 2008</span></span>



| <span data-ttu-id="753cf-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="753cf-201">Entry</span></span> | <span data-ttu-id="753cf-202">Wert</span><span class="sxs-lookup"><span data-stu-id="753cf-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="753cf-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="753cf-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="753cf-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="753cf-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="753cf-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="753cf-205">System-Only</span></span>            | <span data-ttu-id="753cf-206">False</span><span class="sxs-lookup"><span data-stu-id="753cf-206">False</span></span>                                        |
| <span data-ttu-id="753cf-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="753cf-207">Is-Single-Valued</span></span>       | <span data-ttu-id="753cf-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="753cf-208">True</span></span>                                         |
| <span data-ttu-id="753cf-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="753cf-209">Is Indexed</span></span>             | <span data-ttu-id="753cf-210">False</span><span class="sxs-lookup"><span data-stu-id="753cf-210">False</span></span>                                        |
| <span data-ttu-id="753cf-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="753cf-211">In Global Catalog</span></span>      | <span data-ttu-id="753cf-212">False</span><span class="sxs-lookup"><span data-stu-id="753cf-212">False</span></span>                                        |
| <span data-ttu-id="753cf-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="753cf-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="753cf-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="753cf-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="753cf-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="753cf-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="753cf-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="753cf-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="753cf-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="753cf-217">Search-Flags</span></span>           | <span data-ttu-id="753cf-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="753cf-218">0x00000000</span></span>                                   |
| <span data-ttu-id="753cf-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="753cf-219">System-Flags</span></span>           | <span data-ttu-id="753cf-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="753cf-220">0x00000010</span></span>                                   |
| <span data-ttu-id="753cf-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="753cf-221">Classes used in</span></span>        | [<span data-ttu-id="753cf-222">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="753cf-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="753cf-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="753cf-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="753cf-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="753cf-224">Entry</span></span> | <span data-ttu-id="753cf-225">Wert</span><span class="sxs-lookup"><span data-stu-id="753cf-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="753cf-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="753cf-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="753cf-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="753cf-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="753cf-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="753cf-228">System-Only</span></span>            | <span data-ttu-id="753cf-229">False</span><span class="sxs-lookup"><span data-stu-id="753cf-229">False</span></span>                                        |
| <span data-ttu-id="753cf-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="753cf-230">Is-Single-Valued</span></span>       | <span data-ttu-id="753cf-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="753cf-231">True</span></span>                                         |
| <span data-ttu-id="753cf-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="753cf-232">Is Indexed</span></span>             | <span data-ttu-id="753cf-233">False</span><span class="sxs-lookup"><span data-stu-id="753cf-233">False</span></span>                                        |
| <span data-ttu-id="753cf-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="753cf-234">In Global Catalog</span></span>      | <span data-ttu-id="753cf-235">False</span><span class="sxs-lookup"><span data-stu-id="753cf-235">False</span></span>                                        |
| <span data-ttu-id="753cf-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="753cf-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="753cf-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="753cf-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="753cf-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="753cf-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="753cf-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="753cf-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="753cf-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="753cf-240">Search-Flags</span></span>           | <span data-ttu-id="753cf-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="753cf-241">0x00000000</span></span>                                   |
| <span data-ttu-id="753cf-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="753cf-242">System-Flags</span></span>           | <span data-ttu-id="753cf-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="753cf-243">0x00000010</span></span>                                   |
| <span data-ttu-id="753cf-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="753cf-244">Classes used in</span></span>        | [<span data-ttu-id="753cf-245">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="753cf-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="753cf-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="753cf-246">Windows Server 2012</span></span>



| <span data-ttu-id="753cf-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="753cf-247">Entry</span></span> | <span data-ttu-id="753cf-248">Wert</span><span class="sxs-lookup"><span data-stu-id="753cf-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="753cf-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="753cf-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="753cf-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="753cf-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="753cf-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="753cf-251">System-Only</span></span>            | <span data-ttu-id="753cf-252">False</span><span class="sxs-lookup"><span data-stu-id="753cf-252">False</span></span>                                        |
| <span data-ttu-id="753cf-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="753cf-253">Is-Single-Valued</span></span>       | <span data-ttu-id="753cf-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="753cf-254">True</span></span>                                         |
| <span data-ttu-id="753cf-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="753cf-255">Is Indexed</span></span>             | <span data-ttu-id="753cf-256">False</span><span class="sxs-lookup"><span data-stu-id="753cf-256">False</span></span>                                        |
| <span data-ttu-id="753cf-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="753cf-257">In Global Catalog</span></span>      | <span data-ttu-id="753cf-258">False</span><span class="sxs-lookup"><span data-stu-id="753cf-258">False</span></span>                                        |
| <span data-ttu-id="753cf-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="753cf-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="753cf-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="753cf-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="753cf-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="753cf-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="753cf-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="753cf-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="753cf-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="753cf-263">Search-Flags</span></span>           | <span data-ttu-id="753cf-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="753cf-264">0x00000000</span></span>                                   |
| <span data-ttu-id="753cf-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="753cf-265">System-Flags</span></span>           | <span data-ttu-id="753cf-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="753cf-266">0x00000010</span></span>                                   |
| <span data-ttu-id="753cf-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="753cf-267">Classes used in</span></span>        | [<span data-ttu-id="753cf-268">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="753cf-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





