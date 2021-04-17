---
title: Letztes festgelegtem Zeit Attribut
description: Der letzte Zeitpunkt, zu dem der geheime Schlüssel geändert wurde.
ms.assetid: 71245cd4-90d8-4aa1-ad96-d46d6b3a7ad0
ms.tgt_platform: multiple
keywords:
- AD-Schema des Last-Set-time-Attributs
- AD-Schema des lastsettime-Attributs
topic_type:
- apiref
api_name:
- Last-Set-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce123377fac6e67de1ba84b906c9498d0a064936
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392290"
---
# <a name="last-set-time-attribute"></a><span data-ttu-id="e0acf-105">Letztes festgelegtem Zeit Attribut</span><span class="sxs-lookup"><span data-stu-id="e0acf-105">Last-Set-Time attribute</span></span>

<span data-ttu-id="e0acf-106">Der letzte Zeitpunkt, zu dem der geheime Schlüssel geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="e0acf-106">The last time the secret was changed.</span></span> <span data-ttu-id="e0acf-107">Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601 (UTC) darstellt.</span><span class="sxs-lookup"><span data-stu-id="e0acf-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span>



| <span data-ttu-id="e0acf-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0acf-108">Entry</span></span> | <span data-ttu-id="e0acf-109">Wert</span><span class="sxs-lookup"><span data-stu-id="e0acf-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e0acf-110">CN</span><span class="sxs-lookup"><span data-stu-id="e0acf-110">CN</span></span>                | <span data-ttu-id="e0acf-111">Letzte festgelegte Zeit</span><span class="sxs-lookup"><span data-stu-id="e0acf-111">Last-Set-Time</span></span>                        |
| <span data-ttu-id="e0acf-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e0acf-112">Ldap-Display-Name</span></span> | <span data-ttu-id="e0acf-113">lastsettime</span><span class="sxs-lookup"><span data-stu-id="e0acf-113">lastSetTime</span></span>                          |
| <span data-ttu-id="e0acf-114">Size</span><span class="sxs-lookup"><span data-stu-id="e0acf-114">Size</span></span>              | <span data-ttu-id="e0acf-115">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="e0acf-115">8 bytes</span></span>                              |
| <span data-ttu-id="e0acf-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e0acf-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e0acf-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="e0acf-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e0acf-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e0acf-118">Attribute-Id</span></span>      | <span data-ttu-id="e0acf-119">1.2.840.113556.1.4.53</span><span class="sxs-lookup"><span data-stu-id="e0acf-119">1.2.840.113556.1.4.53</span></span>                |
| <span data-ttu-id="e0acf-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e0acf-120">System-Id-Guid</span></span>    | <span data-ttu-id="e0acf-121">bf967998-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e0acf-121">bf967998-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="e0acf-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0acf-122">Syntax</span></span>            | [<span data-ttu-id="e0acf-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="e0acf-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="e0acf-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="e0acf-124">Implementations</span></span>

-   [<span data-ttu-id="e0acf-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e0acf-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e0acf-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e0acf-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e0acf-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e0acf-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e0acf-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e0acf-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e0acf-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e0acf-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e0acf-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e0acf-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e0acf-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e0acf-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e0acf-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0acf-132">Entry</span></span> | <span data-ttu-id="e0acf-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e0acf-133">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="e0acf-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e0acf-134">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="e0acf-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0acf-135">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="e0acf-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0acf-136">System-Only</span></span>            | <span data-ttu-id="e0acf-137">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-137">False</span></span>                                 |
| <span data-ttu-id="e0acf-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e0acf-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e0acf-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="e0acf-139">True</span></span>                                  |
| <span data-ttu-id="e0acf-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e0acf-140">Is Indexed</span></span>             | <span data-ttu-id="e0acf-141">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-141">False</span></span>                                 |
| <span data-ttu-id="e0acf-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e0acf-142">In Global Catalog</span></span>      | <span data-ttu-id="e0acf-143">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-143">False</span></span>                                 |
| <span data-ttu-id="e0acf-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0acf-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0acf-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e0acf-145">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="e0acf-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0acf-146">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="e0acf-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0acf-147">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="e0acf-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0acf-148">Search-Flags</span></span>           | <span data-ttu-id="e0acf-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0acf-149">0x00000000</span></span>                            |
| <span data-ttu-id="e0acf-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0acf-150">System-Flags</span></span>           | <span data-ttu-id="e0acf-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0acf-151">0x00000010</span></span>                            |
| <span data-ttu-id="e0acf-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e0acf-152">Classes used in</span></span>        | [<span data-ttu-id="e0acf-153">**Geheimen**</span><span class="sxs-lookup"><span data-stu-id="e0acf-153">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e0acf-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e0acf-154">Windows Server 2003</span></span>



| <span data-ttu-id="e0acf-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0acf-155">Entry</span></span> | <span data-ttu-id="e0acf-156">Wert</span><span class="sxs-lookup"><span data-stu-id="e0acf-156">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="e0acf-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e0acf-157">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="e0acf-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0acf-158">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="e0acf-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0acf-159">System-Only</span></span>            | <span data-ttu-id="e0acf-160">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-160">False</span></span>                                 |
| <span data-ttu-id="e0acf-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e0acf-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e0acf-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="e0acf-162">True</span></span>                                  |
| <span data-ttu-id="e0acf-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e0acf-163">Is Indexed</span></span>             | <span data-ttu-id="e0acf-164">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-164">False</span></span>                                 |
| <span data-ttu-id="e0acf-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e0acf-165">In Global Catalog</span></span>      | <span data-ttu-id="e0acf-166">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-166">False</span></span>                                 |
| <span data-ttu-id="e0acf-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0acf-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0acf-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e0acf-168">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="e0acf-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0acf-169">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="e0acf-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0acf-170">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="e0acf-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0acf-171">Search-Flags</span></span>           | <span data-ttu-id="e0acf-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0acf-172">0x00000000</span></span>                            |
| <span data-ttu-id="e0acf-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0acf-173">System-Flags</span></span>           | <span data-ttu-id="e0acf-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0acf-174">0x00000010</span></span>                            |
| <span data-ttu-id="e0acf-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e0acf-175">Classes used in</span></span>        | [<span data-ttu-id="e0acf-176">**Geheimen**</span><span class="sxs-lookup"><span data-stu-id="e0acf-176">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e0acf-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e0acf-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e0acf-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0acf-178">Entry</span></span> | <span data-ttu-id="e0acf-179">Wert</span><span class="sxs-lookup"><span data-stu-id="e0acf-179">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="e0acf-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e0acf-180">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="e0acf-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0acf-181">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="e0acf-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0acf-182">System-Only</span></span>            | <span data-ttu-id="e0acf-183">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-183">False</span></span>                                 |
| <span data-ttu-id="e0acf-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e0acf-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e0acf-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="e0acf-185">True</span></span>                                  |
| <span data-ttu-id="e0acf-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e0acf-186">Is Indexed</span></span>             | <span data-ttu-id="e0acf-187">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-187">False</span></span>                                 |
| <span data-ttu-id="e0acf-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e0acf-188">In Global Catalog</span></span>      | <span data-ttu-id="e0acf-189">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-189">False</span></span>                                 |
| <span data-ttu-id="e0acf-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0acf-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0acf-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e0acf-191">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="e0acf-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0acf-192">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="e0acf-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0acf-193">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="e0acf-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0acf-194">Search-Flags</span></span>           | <span data-ttu-id="e0acf-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0acf-195">0x00000000</span></span>                            |
| <span data-ttu-id="e0acf-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0acf-196">System-Flags</span></span>           | <span data-ttu-id="e0acf-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0acf-197">0x00000010</span></span>                            |
| <span data-ttu-id="e0acf-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e0acf-198">Classes used in</span></span>        | [<span data-ttu-id="e0acf-199">**Geheimen**</span><span class="sxs-lookup"><span data-stu-id="e0acf-199">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e0acf-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0acf-200">Windows Server 2008</span></span>



| <span data-ttu-id="e0acf-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0acf-201">Entry</span></span> | <span data-ttu-id="e0acf-202">Wert</span><span class="sxs-lookup"><span data-stu-id="e0acf-202">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="e0acf-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e0acf-203">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="e0acf-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0acf-204">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="e0acf-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0acf-205">System-Only</span></span>            | <span data-ttu-id="e0acf-206">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-206">False</span></span>                                 |
| <span data-ttu-id="e0acf-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e0acf-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e0acf-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="e0acf-208">True</span></span>                                  |
| <span data-ttu-id="e0acf-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e0acf-209">Is Indexed</span></span>             | <span data-ttu-id="e0acf-210">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-210">False</span></span>                                 |
| <span data-ttu-id="e0acf-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e0acf-211">In Global Catalog</span></span>      | <span data-ttu-id="e0acf-212">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-212">False</span></span>                                 |
| <span data-ttu-id="e0acf-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0acf-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0acf-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e0acf-214">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="e0acf-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0acf-215">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="e0acf-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0acf-216">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="e0acf-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0acf-217">Search-Flags</span></span>           | <span data-ttu-id="e0acf-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0acf-218">0x00000000</span></span>                            |
| <span data-ttu-id="e0acf-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0acf-219">System-Flags</span></span>           | <span data-ttu-id="e0acf-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0acf-220">0x00000010</span></span>                            |
| <span data-ttu-id="e0acf-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e0acf-221">Classes used in</span></span>        | [<span data-ttu-id="e0acf-222">**Geheimen**</span><span class="sxs-lookup"><span data-stu-id="e0acf-222">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e0acf-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e0acf-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e0acf-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0acf-224">Entry</span></span> | <span data-ttu-id="e0acf-225">Wert</span><span class="sxs-lookup"><span data-stu-id="e0acf-225">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="e0acf-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e0acf-226">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="e0acf-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0acf-227">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="e0acf-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0acf-228">System-Only</span></span>            | <span data-ttu-id="e0acf-229">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-229">False</span></span>                                 |
| <span data-ttu-id="e0acf-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e0acf-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e0acf-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="e0acf-231">True</span></span>                                  |
| <span data-ttu-id="e0acf-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e0acf-232">Is Indexed</span></span>             | <span data-ttu-id="e0acf-233">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-233">False</span></span>                                 |
| <span data-ttu-id="e0acf-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e0acf-234">In Global Catalog</span></span>      | <span data-ttu-id="e0acf-235">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-235">False</span></span>                                 |
| <span data-ttu-id="e0acf-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0acf-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0acf-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e0acf-237">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="e0acf-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0acf-238">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="e0acf-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0acf-239">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="e0acf-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0acf-240">Search-Flags</span></span>           | <span data-ttu-id="e0acf-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0acf-241">0x00000000</span></span>                            |
| <span data-ttu-id="e0acf-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0acf-242">System-Flags</span></span>           | <span data-ttu-id="e0acf-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0acf-243">0x00000010</span></span>                            |
| <span data-ttu-id="e0acf-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e0acf-244">Classes used in</span></span>        | [<span data-ttu-id="e0acf-245">**Geheimen**</span><span class="sxs-lookup"><span data-stu-id="e0acf-245">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e0acf-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0acf-246">Windows Server 2012</span></span>



| <span data-ttu-id="e0acf-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0acf-247">Entry</span></span> | <span data-ttu-id="e0acf-248">Wert</span><span class="sxs-lookup"><span data-stu-id="e0acf-248">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="e0acf-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e0acf-249">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="e0acf-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0acf-250">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="e0acf-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0acf-251">System-Only</span></span>            | <span data-ttu-id="e0acf-252">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-252">False</span></span>                                 |
| <span data-ttu-id="e0acf-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e0acf-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e0acf-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="e0acf-254">True</span></span>                                  |
| <span data-ttu-id="e0acf-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e0acf-255">Is Indexed</span></span>             | <span data-ttu-id="e0acf-256">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-256">False</span></span>                                 |
| <span data-ttu-id="e0acf-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e0acf-257">In Global Catalog</span></span>      | <span data-ttu-id="e0acf-258">False</span><span class="sxs-lookup"><span data-stu-id="e0acf-258">False</span></span>                                 |
| <span data-ttu-id="e0acf-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0acf-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0acf-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e0acf-260">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="e0acf-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0acf-261">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="e0acf-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0acf-262">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="e0acf-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0acf-263">Search-Flags</span></span>           | <span data-ttu-id="e0acf-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0acf-264">0x00000000</span></span>                            |
| <span data-ttu-id="e0acf-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0acf-265">System-Flags</span></span>           | <span data-ttu-id="e0acf-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0acf-266">0x00000010</span></span>                            |
| <span data-ttu-id="e0acf-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e0acf-267">Classes used in</span></span>        | [<span data-ttu-id="e0acf-268">**Geheimen**</span><span class="sxs-lookup"><span data-stu-id="e0acf-268">**Secret**</span></span>](c-secret.md)<br/> |



 

 





