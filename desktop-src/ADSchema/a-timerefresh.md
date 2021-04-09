---
title: Time-Refresh-Attribut
description: Dieses Attribut verfügt über das Intervall, in dem ein in einer Active Directory integrierter Zone enthaltener Ressourcen Daten Satz für den DNS-Server aktualisiert werden soll. Das Standardintervall beträgt 7 Tage.
ms.assetid: 9e473c29-7fcf-4d6d-8a7c-2791c7822c7d
ms.tgt_platform: multiple
keywords:
- AD-Schema für Time-Refresh-Attribut
- timerefresh-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Time-Refresh
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87bc360686b1692d2dbda1ee23ad6351e69d3afe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957571"
---
# <a name="time-refresh-attribute"></a><span data-ttu-id="acdae-106">Time-Refresh-Attribut</span><span class="sxs-lookup"><span data-stu-id="acdae-106">Time-Refresh attribute</span></span>

<span data-ttu-id="acdae-107">Dieses Attribut verfügt über das Intervall, in dem ein in einer Active Directory integrierter Zone enthaltener Ressourcen Daten Satz für den DNS-Server aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="acdae-107">This attribute has the interval during which a resource record that is contained in an Active Directory integrated zone should be refreshed for the DNS server.</span></span> <span data-ttu-id="acdae-108">Das Standardintervall beträgt 7 Tage.</span><span class="sxs-lookup"><span data-stu-id="acdae-108">The default interval is 7 days.</span></span>



| <span data-ttu-id="acdae-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="acdae-109">Entry</span></span> | <span data-ttu-id="acdae-110">Wert</span><span class="sxs-lookup"><span data-stu-id="acdae-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="acdae-111">CN</span><span class="sxs-lookup"><span data-stu-id="acdae-111">CN</span></span>                | <span data-ttu-id="acdae-112">Time-Refresh</span><span class="sxs-lookup"><span data-stu-id="acdae-112">Time-Refresh</span></span>                         |
| <span data-ttu-id="acdae-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="acdae-113">Ldap-Display-Name</span></span> | <span data-ttu-id="acdae-114">timerefresh</span><span class="sxs-lookup"><span data-stu-id="acdae-114">timeRefresh</span></span>                          |
| <span data-ttu-id="acdae-115">Size</span><span class="sxs-lookup"><span data-stu-id="acdae-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="acdae-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="acdae-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="acdae-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="acdae-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="acdae-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="acdae-118">Attribute-Id</span></span>      | <span data-ttu-id="acdae-119">1.2.840.113556.1.4.503</span><span class="sxs-lookup"><span data-stu-id="acdae-119">1.2.840.113556.1.4.503</span></span>               |
| <span data-ttu-id="acdae-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="acdae-120">System-Id-Guid</span></span>    | <span data-ttu-id="acdae-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="acdae-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span></span> |
| <span data-ttu-id="acdae-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="acdae-122">Syntax</span></span>            | [<span data-ttu-id="acdae-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="acdae-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="acdae-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="acdae-124">Implementations</span></span>

-   [<span data-ttu-id="acdae-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="acdae-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="acdae-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="acdae-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="acdae-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="acdae-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="acdae-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="acdae-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="acdae-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="acdae-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="acdae-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="acdae-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="acdae-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="acdae-131">Windows 2000 Server</span></span>



| <span data-ttu-id="acdae-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="acdae-132">Entry</span></span> | <span data-ttu-id="acdae-133">Wert</span><span class="sxs-lookup"><span data-stu-id="acdae-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acdae-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="acdae-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="acdae-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acdae-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="acdae-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="acdae-136">System-Only</span></span>            | <span data-ttu-id="acdae-137">False</span><span class="sxs-lookup"><span data-stu-id="acdae-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="acdae-138">Is-Single-Valued</span></span>       | <span data-ttu-id="acdae-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="acdae-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="acdae-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="acdae-140">Is Indexed</span></span>             | <span data-ttu-id="acdae-141">False</span><span class="sxs-lookup"><span data-stu-id="acdae-141">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="acdae-142">In Global Catalog</span></span>      | <span data-ttu-id="acdae-143">False</span><span class="sxs-lookup"><span data-stu-id="acdae-143">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="acdae-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="acdae-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="acdae-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="acdae-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acdae-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="acdae-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acdae-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="acdae-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acdae-148">Search-Flags</span></span>           | <span data-ttu-id="acdae-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acdae-149">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="acdae-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acdae-150">System-Flags</span></span>           | <span data-ttu-id="acdae-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acdae-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="acdae-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="acdae-152">Classes used in</span></span>        | [<span data-ttu-id="acdae-153">**Link-Track-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="acdae-153">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="acdae-154">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="acdae-154">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="acdae-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="acdae-155">Windows Server 2003</span></span>



| <span data-ttu-id="acdae-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="acdae-156">Entry</span></span> | <span data-ttu-id="acdae-157">Wert</span><span class="sxs-lookup"><span data-stu-id="acdae-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acdae-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="acdae-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="acdae-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acdae-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="acdae-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="acdae-160">System-Only</span></span>            | <span data-ttu-id="acdae-161">False</span><span class="sxs-lookup"><span data-stu-id="acdae-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="acdae-162">Is-Single-Valued</span></span>       | <span data-ttu-id="acdae-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="acdae-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="acdae-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="acdae-164">Is Indexed</span></span>             | <span data-ttu-id="acdae-165">False</span><span class="sxs-lookup"><span data-stu-id="acdae-165">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="acdae-166">In Global Catalog</span></span>      | <span data-ttu-id="acdae-167">False</span><span class="sxs-lookup"><span data-stu-id="acdae-167">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="acdae-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="acdae-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="acdae-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="acdae-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acdae-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="acdae-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acdae-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="acdae-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acdae-172">Search-Flags</span></span>           | <span data-ttu-id="acdae-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acdae-173">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="acdae-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acdae-174">System-Flags</span></span>           | <span data-ttu-id="acdae-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acdae-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="acdae-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="acdae-176">Classes used in</span></span>        | [<span data-ttu-id="acdae-177">**Link-Track-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="acdae-177">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="acdae-178">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="acdae-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="acdae-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="acdae-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="acdae-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="acdae-180">Entry</span></span> | <span data-ttu-id="acdae-181">Wert</span><span class="sxs-lookup"><span data-stu-id="acdae-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acdae-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="acdae-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="acdae-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acdae-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="acdae-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="acdae-184">System-Only</span></span>            | <span data-ttu-id="acdae-185">False</span><span class="sxs-lookup"><span data-stu-id="acdae-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="acdae-186">Is-Single-Valued</span></span>       | <span data-ttu-id="acdae-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="acdae-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="acdae-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="acdae-188">Is Indexed</span></span>             | <span data-ttu-id="acdae-189">False</span><span class="sxs-lookup"><span data-stu-id="acdae-189">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="acdae-190">In Global Catalog</span></span>      | <span data-ttu-id="acdae-191">False</span><span class="sxs-lookup"><span data-stu-id="acdae-191">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="acdae-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="acdae-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="acdae-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="acdae-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acdae-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="acdae-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acdae-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="acdae-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acdae-196">Search-Flags</span></span>           | <span data-ttu-id="acdae-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acdae-197">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="acdae-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acdae-198">System-Flags</span></span>           | <span data-ttu-id="acdae-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acdae-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="acdae-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="acdae-200">Classes used in</span></span>        | [<span data-ttu-id="acdae-201">**Link-Track-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="acdae-201">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="acdae-202">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="acdae-202">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="acdae-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acdae-203">Windows Server 2008</span></span>



| <span data-ttu-id="acdae-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="acdae-204">Entry</span></span> | <span data-ttu-id="acdae-205">Wert</span><span class="sxs-lookup"><span data-stu-id="acdae-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acdae-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="acdae-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="acdae-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acdae-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="acdae-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="acdae-208">System-Only</span></span>            | <span data-ttu-id="acdae-209">False</span><span class="sxs-lookup"><span data-stu-id="acdae-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="acdae-210">Is-Single-Valued</span></span>       | <span data-ttu-id="acdae-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="acdae-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="acdae-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="acdae-212">Is Indexed</span></span>             | <span data-ttu-id="acdae-213">False</span><span class="sxs-lookup"><span data-stu-id="acdae-213">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="acdae-214">In Global Catalog</span></span>      | <span data-ttu-id="acdae-215">False</span><span class="sxs-lookup"><span data-stu-id="acdae-215">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="acdae-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="acdae-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="acdae-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="acdae-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acdae-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="acdae-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acdae-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="acdae-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acdae-220">Search-Flags</span></span>           | <span data-ttu-id="acdae-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acdae-221">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="acdae-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acdae-222">System-Flags</span></span>           | <span data-ttu-id="acdae-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acdae-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="acdae-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="acdae-224">Classes used in</span></span>        | [<span data-ttu-id="acdae-225">**Link-Track-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="acdae-225">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="acdae-226">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="acdae-226">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="acdae-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="acdae-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="acdae-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="acdae-228">Entry</span></span> | <span data-ttu-id="acdae-229">Wert</span><span class="sxs-lookup"><span data-stu-id="acdae-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acdae-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="acdae-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="acdae-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acdae-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="acdae-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="acdae-232">System-Only</span></span>            | <span data-ttu-id="acdae-233">False</span><span class="sxs-lookup"><span data-stu-id="acdae-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="acdae-234">Is-Single-Valued</span></span>       | <span data-ttu-id="acdae-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="acdae-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="acdae-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="acdae-236">Is Indexed</span></span>             | <span data-ttu-id="acdae-237">False</span><span class="sxs-lookup"><span data-stu-id="acdae-237">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="acdae-238">In Global Catalog</span></span>      | <span data-ttu-id="acdae-239">False</span><span class="sxs-lookup"><span data-stu-id="acdae-239">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="acdae-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="acdae-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="acdae-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="acdae-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acdae-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="acdae-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acdae-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="acdae-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acdae-244">Search-Flags</span></span>           | <span data-ttu-id="acdae-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acdae-245">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="acdae-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acdae-246">System-Flags</span></span>           | <span data-ttu-id="acdae-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acdae-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="acdae-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="acdae-248">Classes used in</span></span>        | [<span data-ttu-id="acdae-249">**Link-Track-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="acdae-249">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="acdae-250">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="acdae-250">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="acdae-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="acdae-251">Windows Server 2012</span></span>



| <span data-ttu-id="acdae-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="acdae-252">Entry</span></span> | <span data-ttu-id="acdae-253">Wert</span><span class="sxs-lookup"><span data-stu-id="acdae-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acdae-254">Link-ID</span><span class="sxs-lookup"><span data-stu-id="acdae-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="acdae-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acdae-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="acdae-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="acdae-256">System-Only</span></span>            | <span data-ttu-id="acdae-257">False</span><span class="sxs-lookup"><span data-stu-id="acdae-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-258">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="acdae-258">Is-Single-Valued</span></span>       | <span data-ttu-id="acdae-259">Richtig</span><span class="sxs-lookup"><span data-stu-id="acdae-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="acdae-260">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="acdae-260">Is Indexed</span></span>             | <span data-ttu-id="acdae-261">False</span><span class="sxs-lookup"><span data-stu-id="acdae-261">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-262">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="acdae-262">In Global Catalog</span></span>      | <span data-ttu-id="acdae-263">False</span><span class="sxs-lookup"><span data-stu-id="acdae-263">False</span></span>                                                                                                                         |
| <span data-ttu-id="acdae-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="acdae-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="acdae-265">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="acdae-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="acdae-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acdae-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="acdae-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acdae-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="acdae-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acdae-268">Search-Flags</span></span>           | <span data-ttu-id="acdae-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acdae-269">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="acdae-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acdae-270">System-Flags</span></span>           | <span data-ttu-id="acdae-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acdae-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="acdae-272">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="acdae-272">Classes used in</span></span>        | [<span data-ttu-id="acdae-273">**Link-Track-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="acdae-273">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="acdae-274">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="acdae-274">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





