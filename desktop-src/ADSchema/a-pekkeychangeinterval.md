---
title: PEK-Key-Change-Interval-Attribut
description: Änderungs Intervall für das Kennwort-Verschlüsselungsschlüssel.
ms.assetid: 2031feda-3f5d-4c76-bb45-42157fd5cb84
ms.tgt_platform: multiple
keywords:
- "\"PEK-Key-Change-Interval\"-Attribut, AD-Schema"
- AD-Schema für das Attribut "Peer Schlüssel changeinterval"
topic_type:
- apiref
api_name:
- Pek-Key-Change-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2259bdd4dfee24bbccfeafa6d5bb06490c24c25c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106341064"
---
# <a name="pek-key-change-interval-attribute"></a><span data-ttu-id="64bcc-105">PEK-Key-Change-Interval-Attribut</span><span class="sxs-lookup"><span data-stu-id="64bcc-105">Pek-Key-Change-Interval attribute</span></span>

<span data-ttu-id="64bcc-106">Änderungs Intervall für das Kennwort-Verschlüsselungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="64bcc-106">Password encryption key change interval.</span></span>



| <span data-ttu-id="64bcc-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64bcc-107">Entry</span></span> | <span data-ttu-id="64bcc-108">Wert</span><span class="sxs-lookup"><span data-stu-id="64bcc-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="64bcc-109">CN</span><span class="sxs-lookup"><span data-stu-id="64bcc-109">CN</span></span>                | <span data-ttu-id="64bcc-110">PEK-Key-Change-Interval</span><span class="sxs-lookup"><span data-stu-id="64bcc-110">Pek-Key-Change-Interval</span></span>              |
| <span data-ttu-id="64bcc-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="64bcc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="64bcc-112">"Peer keychangeinterval"</span><span class="sxs-lookup"><span data-stu-id="64bcc-112">pekKeyChangeInterval</span></span>                 |
| <span data-ttu-id="64bcc-113">Size</span><span class="sxs-lookup"><span data-stu-id="64bcc-113">Size</span></span>              | <span data-ttu-id="64bcc-114">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="64bcc-114">8 bytes</span></span>                              |
| <span data-ttu-id="64bcc-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="64bcc-115">Update Privilege</span></span>  | <span data-ttu-id="64bcc-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64bcc-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="64bcc-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="64bcc-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="64bcc-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="64bcc-118">Attribute-Id</span></span>      | <span data-ttu-id="64bcc-119">1.2.840.113556.1.4.866</span><span class="sxs-lookup"><span data-stu-id="64bcc-119">1.2.840.113556.1.4.866</span></span>               |
| <span data-ttu-id="64bcc-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="64bcc-120">System-Id-Guid</span></span>    | <span data-ttu-id="64bcc-121">07383084-91df-11d1-AEbc-0000e80367c1</span><span class="sxs-lookup"><span data-stu-id="64bcc-121">07383084-91df-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="64bcc-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="64bcc-122">Syntax</span></span>            | [<span data-ttu-id="64bcc-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="64bcc-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="64bcc-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="64bcc-124">Implementations</span></span>

-   [<span data-ttu-id="64bcc-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="64bcc-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="64bcc-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="64bcc-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="64bcc-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="64bcc-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="64bcc-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="64bcc-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="64bcc-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="64bcc-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="64bcc-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="64bcc-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="64bcc-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="64bcc-131">Windows 2000 Server</span></span>



| <span data-ttu-id="64bcc-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64bcc-132">Entry</span></span> | <span data-ttu-id="64bcc-133">Wert</span><span class="sxs-lookup"><span data-stu-id="64bcc-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64bcc-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64bcc-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64bcc-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64bcc-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64bcc-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="64bcc-136">System-Only</span></span>            | <span data-ttu-id="64bcc-137">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-137">False</span></span>                                        |
| <span data-ttu-id="64bcc-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64bcc-138">Is-Single-Valued</span></span>       | <span data-ttu-id="64bcc-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="64bcc-139">True</span></span>                                         |
| <span data-ttu-id="64bcc-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64bcc-140">Is Indexed</span></span>             | <span data-ttu-id="64bcc-141">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-141">False</span></span>                                        |
| <span data-ttu-id="64bcc-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64bcc-142">In Global Catalog</span></span>      | <span data-ttu-id="64bcc-143">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-143">False</span></span>                                        |
| <span data-ttu-id="64bcc-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64bcc-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="64bcc-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64bcc-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64bcc-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64bcc-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64bcc-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64bcc-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64bcc-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64bcc-148">Search-Flags</span></span>           | <span data-ttu-id="64bcc-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64bcc-149">0x00000000</span></span>                                   |
| <span data-ttu-id="64bcc-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64bcc-150">System-Flags</span></span>           | <span data-ttu-id="64bcc-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64bcc-151">0x00000010</span></span>                                   |
| <span data-ttu-id="64bcc-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64bcc-152">Classes used in</span></span>        | [<span data-ttu-id="64bcc-153">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="64bcc-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="64bcc-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="64bcc-154">Windows Server 2003</span></span>



| <span data-ttu-id="64bcc-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64bcc-155">Entry</span></span> | <span data-ttu-id="64bcc-156">Wert</span><span class="sxs-lookup"><span data-stu-id="64bcc-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64bcc-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64bcc-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64bcc-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64bcc-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64bcc-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="64bcc-159">System-Only</span></span>            | <span data-ttu-id="64bcc-160">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-160">False</span></span>                                        |
| <span data-ttu-id="64bcc-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64bcc-161">Is-Single-Valued</span></span>       | <span data-ttu-id="64bcc-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="64bcc-162">True</span></span>                                         |
| <span data-ttu-id="64bcc-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64bcc-163">Is Indexed</span></span>             | <span data-ttu-id="64bcc-164">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-164">False</span></span>                                        |
| <span data-ttu-id="64bcc-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64bcc-165">In Global Catalog</span></span>      | <span data-ttu-id="64bcc-166">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-166">False</span></span>                                        |
| <span data-ttu-id="64bcc-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64bcc-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="64bcc-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64bcc-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64bcc-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64bcc-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64bcc-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64bcc-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64bcc-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64bcc-171">Search-Flags</span></span>           | <span data-ttu-id="64bcc-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64bcc-172">0x00000000</span></span>                                   |
| <span data-ttu-id="64bcc-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64bcc-173">System-Flags</span></span>           | <span data-ttu-id="64bcc-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64bcc-174">0x00000010</span></span>                                   |
| <span data-ttu-id="64bcc-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64bcc-175">Classes used in</span></span>        | [<span data-ttu-id="64bcc-176">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="64bcc-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="64bcc-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="64bcc-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="64bcc-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64bcc-178">Entry</span></span> | <span data-ttu-id="64bcc-179">Wert</span><span class="sxs-lookup"><span data-stu-id="64bcc-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64bcc-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64bcc-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64bcc-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64bcc-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64bcc-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="64bcc-182">System-Only</span></span>            | <span data-ttu-id="64bcc-183">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-183">False</span></span>                                        |
| <span data-ttu-id="64bcc-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64bcc-184">Is-Single-Valued</span></span>       | <span data-ttu-id="64bcc-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="64bcc-185">True</span></span>                                         |
| <span data-ttu-id="64bcc-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64bcc-186">Is Indexed</span></span>             | <span data-ttu-id="64bcc-187">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-187">False</span></span>                                        |
| <span data-ttu-id="64bcc-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64bcc-188">In Global Catalog</span></span>      | <span data-ttu-id="64bcc-189">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-189">False</span></span>                                        |
| <span data-ttu-id="64bcc-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64bcc-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="64bcc-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64bcc-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64bcc-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64bcc-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64bcc-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64bcc-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64bcc-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64bcc-194">Search-Flags</span></span>           | <span data-ttu-id="64bcc-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64bcc-195">0x00000000</span></span>                                   |
| <span data-ttu-id="64bcc-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64bcc-196">System-Flags</span></span>           | <span data-ttu-id="64bcc-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64bcc-197">0x00000010</span></span>                                   |
| <span data-ttu-id="64bcc-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64bcc-198">Classes used in</span></span>        | [<span data-ttu-id="64bcc-199">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="64bcc-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="64bcc-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64bcc-200">Windows Server 2008</span></span>



| <span data-ttu-id="64bcc-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64bcc-201">Entry</span></span> | <span data-ttu-id="64bcc-202">Wert</span><span class="sxs-lookup"><span data-stu-id="64bcc-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64bcc-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64bcc-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64bcc-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64bcc-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64bcc-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="64bcc-205">System-Only</span></span>            | <span data-ttu-id="64bcc-206">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-206">False</span></span>                                        |
| <span data-ttu-id="64bcc-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64bcc-207">Is-Single-Valued</span></span>       | <span data-ttu-id="64bcc-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="64bcc-208">True</span></span>                                         |
| <span data-ttu-id="64bcc-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64bcc-209">Is Indexed</span></span>             | <span data-ttu-id="64bcc-210">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-210">False</span></span>                                        |
| <span data-ttu-id="64bcc-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64bcc-211">In Global Catalog</span></span>      | <span data-ttu-id="64bcc-212">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-212">False</span></span>                                        |
| <span data-ttu-id="64bcc-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64bcc-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="64bcc-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64bcc-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64bcc-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64bcc-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64bcc-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64bcc-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64bcc-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64bcc-217">Search-Flags</span></span>           | <span data-ttu-id="64bcc-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64bcc-218">0x00000000</span></span>                                   |
| <span data-ttu-id="64bcc-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64bcc-219">System-Flags</span></span>           | <span data-ttu-id="64bcc-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64bcc-220">0x00000010</span></span>                                   |
| <span data-ttu-id="64bcc-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64bcc-221">Classes used in</span></span>        | [<span data-ttu-id="64bcc-222">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="64bcc-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="64bcc-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="64bcc-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="64bcc-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64bcc-224">Entry</span></span> | <span data-ttu-id="64bcc-225">Wert</span><span class="sxs-lookup"><span data-stu-id="64bcc-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64bcc-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64bcc-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64bcc-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64bcc-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64bcc-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="64bcc-228">System-Only</span></span>            | <span data-ttu-id="64bcc-229">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-229">False</span></span>                                        |
| <span data-ttu-id="64bcc-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64bcc-230">Is-Single-Valued</span></span>       | <span data-ttu-id="64bcc-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="64bcc-231">True</span></span>                                         |
| <span data-ttu-id="64bcc-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64bcc-232">Is Indexed</span></span>             | <span data-ttu-id="64bcc-233">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-233">False</span></span>                                        |
| <span data-ttu-id="64bcc-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64bcc-234">In Global Catalog</span></span>      | <span data-ttu-id="64bcc-235">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-235">False</span></span>                                        |
| <span data-ttu-id="64bcc-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64bcc-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="64bcc-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64bcc-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64bcc-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64bcc-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64bcc-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64bcc-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64bcc-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64bcc-240">Search-Flags</span></span>           | <span data-ttu-id="64bcc-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64bcc-241">0x00000000</span></span>                                   |
| <span data-ttu-id="64bcc-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64bcc-242">System-Flags</span></span>           | <span data-ttu-id="64bcc-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64bcc-243">0x00000010</span></span>                                   |
| <span data-ttu-id="64bcc-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64bcc-244">Classes used in</span></span>        | [<span data-ttu-id="64bcc-245">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="64bcc-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="64bcc-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="64bcc-246">Windows Server 2012</span></span>



| <span data-ttu-id="64bcc-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64bcc-247">Entry</span></span> | <span data-ttu-id="64bcc-248">Wert</span><span class="sxs-lookup"><span data-stu-id="64bcc-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64bcc-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64bcc-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64bcc-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64bcc-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64bcc-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="64bcc-251">System-Only</span></span>            | <span data-ttu-id="64bcc-252">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-252">False</span></span>                                        |
| <span data-ttu-id="64bcc-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64bcc-253">Is-Single-Valued</span></span>       | <span data-ttu-id="64bcc-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="64bcc-254">True</span></span>                                         |
| <span data-ttu-id="64bcc-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64bcc-255">Is Indexed</span></span>             | <span data-ttu-id="64bcc-256">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-256">False</span></span>                                        |
| <span data-ttu-id="64bcc-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64bcc-257">In Global Catalog</span></span>      | <span data-ttu-id="64bcc-258">False</span><span class="sxs-lookup"><span data-stu-id="64bcc-258">False</span></span>                                        |
| <span data-ttu-id="64bcc-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64bcc-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="64bcc-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64bcc-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64bcc-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64bcc-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64bcc-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64bcc-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64bcc-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64bcc-263">Search-Flags</span></span>           | <span data-ttu-id="64bcc-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64bcc-264">0x00000000</span></span>                                   |
| <span data-ttu-id="64bcc-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64bcc-265">System-Flags</span></span>           | <span data-ttu-id="64bcc-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64bcc-266">0x00000010</span></span>                                   |
| <span data-ttu-id="64bcc-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64bcc-267">Classes used in</span></span>        | [<span data-ttu-id="64bcc-268">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="64bcc-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





