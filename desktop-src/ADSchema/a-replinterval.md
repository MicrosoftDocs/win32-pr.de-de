---
title: Repl-Interval-Attribut
description: Das-Attribut von Site-Link-Objekten, das das Intervall in Minuten zwischen den Replikations Zyklen zwischen den Standorten in der Site Liste definiert.
ms.assetid: ef4cbf75-7283-4930-9f98-1ffd6eb05669
ms.tgt_platform: multiple
keywords:
- AD-Schema für Repl-Interval-Attribut
- replInterval-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Repl-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e681b01fbc60b775b0cb947007056dc1d3d3adbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107589"
---
# <a name="repl-interval-attribute"></a><span data-ttu-id="b6af0-105">Repl-Interval-Attribut</span><span class="sxs-lookup"><span data-stu-id="b6af0-105">Repl-Interval attribute</span></span>

<span data-ttu-id="b6af0-106">Das-Attribut von Site-Link-Objekten, das das Intervall in Minuten zwischen den Replikations Zyklen zwischen den Standorten in der Site Liste definiert.</span><span class="sxs-lookup"><span data-stu-id="b6af0-106">The attribute of Site-Link objects that defines the interval, in minutes, between replication cycles between the sites in the Site-List.</span></span> <span data-ttu-id="b6af0-107">Muss ein Vielfaches von 15 Minuten (die Granularität der standortübergreifenden DS-Replikation), mindestens 15 Minuten und maximal 10.080 Minuten (eine Woche) sein.</span><span class="sxs-lookup"><span data-stu-id="b6af0-107">Must be a multiple of 15 minutes (the granularity of cross-site DS replication), a minimum of 15 minutes, and a maximum of 10,080 minutes (one week).</span></span>



| <span data-ttu-id="b6af0-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6af0-108">Entry</span></span> | <span data-ttu-id="b6af0-109">Wert</span><span class="sxs-lookup"><span data-stu-id="b6af0-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="b6af0-110">CN</span><span class="sxs-lookup"><span data-stu-id="b6af0-110">CN</span></span>                | <span data-ttu-id="b6af0-111">Repl-Interval</span><span class="sxs-lookup"><span data-stu-id="b6af0-111">Repl-Interval</span></span>                                  |
| <span data-ttu-id="b6af0-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b6af0-112">Ldap-Display-Name</span></span> | <span data-ttu-id="b6af0-113">replInterval</span><span class="sxs-lookup"><span data-stu-id="b6af0-113">replInterval</span></span>                                   |
| <span data-ttu-id="b6af0-114">Size</span><span class="sxs-lookup"><span data-stu-id="b6af0-114">Size</span></span>              | <span data-ttu-id="b6af0-115">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="b6af0-115">4 bytes</span></span>                                        |
| <span data-ttu-id="b6af0-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b6af0-116">Update Privilege</span></span>  | <span data-ttu-id="b6af0-117">Unternehmensadministrator</span><span class="sxs-lookup"><span data-stu-id="b6af0-117">Enterprise administrator</span></span>                       |
| <span data-ttu-id="b6af0-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b6af0-118">Update Frequency</span></span>  | <span data-ttu-id="b6af0-119">Wann das Replikations Intervall geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="b6af0-119">When the replication interval needs to change.</span></span> |
| <span data-ttu-id="b6af0-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b6af0-120">Attribute-Id</span></span>      | <span data-ttu-id="b6af0-121">1.2.840.113556.1.4.1336</span><span class="sxs-lookup"><span data-stu-id="b6af0-121">1.2.840.113556.1.4.1336</span></span>                        |
| <span data-ttu-id="b6af0-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b6af0-122">System-Id-Guid</span></span>    | <span data-ttu-id="b6af0-123">45ba9d1a-56fa-11d2-90d0-00c04f d91ab1</span><span class="sxs-lookup"><span data-stu-id="b6af0-123">45ba9d1a-56fa-11d2-90d0-00c04fd91ab1</span></span>           |
| <span data-ttu-id="b6af0-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6af0-124">Syntax</span></span>            | [<span data-ttu-id="b6af0-125">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="b6af0-125">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="b6af0-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b6af0-126">Implementations</span></span>

-   [<span data-ttu-id="b6af0-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b6af0-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b6af0-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b6af0-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b6af0-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="b6af0-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b6af0-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b6af0-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b6af0-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b6af0-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b6af0-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b6af0-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b6af0-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b6af0-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b6af0-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b6af0-134">Windows 2000 Server</span></span>



| <span data-ttu-id="b6af0-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6af0-135">Entry</span></span> | <span data-ttu-id="b6af0-136">Wert</span><span class="sxs-lookup"><span data-stu-id="b6af0-136">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6af0-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b6af0-137">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="b6af0-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6af0-138">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="b6af0-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6af0-139">System-Only</span></span>            | <span data-ttu-id="b6af0-140">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-140">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b6af0-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b6af0-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="b6af0-142">True</span></span>                                                                                                       |
| <span data-ttu-id="b6af0-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b6af0-143">Is Indexed</span></span>             | <span data-ttu-id="b6af0-144">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-144">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b6af0-145">In Global Catalog</span></span>      | <span data-ttu-id="b6af0-146">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-146">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b6af0-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6af0-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b6af0-148">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="b6af0-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6af0-149">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="b6af0-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6af0-150">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="b6af0-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6af0-151">Search-Flags</span></span>           | <span data-ttu-id="b6af0-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6af0-152">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="b6af0-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6af0-153">System-Flags</span></span>           | <span data-ttu-id="b6af0-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6af0-154">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="b6af0-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b6af0-155">Classes used in</span></span>        | [<span data-ttu-id="b6af0-156">**Standort übergreifender Transport**</span><span class="sxs-lookup"><span data-stu-id="b6af0-156">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="b6af0-157">**Standort Link**</span><span class="sxs-lookup"><span data-stu-id="b6af0-157">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b6af0-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b6af0-158">Windows Server 2003</span></span>



| <span data-ttu-id="b6af0-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6af0-159">Entry</span></span> | <span data-ttu-id="b6af0-160">Wert</span><span class="sxs-lookup"><span data-stu-id="b6af0-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6af0-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b6af0-161">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="b6af0-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6af0-162">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="b6af0-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6af0-163">System-Only</span></span>            | <span data-ttu-id="b6af0-164">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-164">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b6af0-165">Is-Single-Valued</span></span>       | <span data-ttu-id="b6af0-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="b6af0-166">True</span></span>                                                                                                       |
| <span data-ttu-id="b6af0-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b6af0-167">Is Indexed</span></span>             | <span data-ttu-id="b6af0-168">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-168">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b6af0-169">In Global Catalog</span></span>      | <span data-ttu-id="b6af0-170">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-170">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b6af0-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6af0-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b6af0-172">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="b6af0-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6af0-173">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="b6af0-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6af0-174">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="b6af0-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6af0-175">Search-Flags</span></span>           | <span data-ttu-id="b6af0-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6af0-176">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="b6af0-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6af0-177">System-Flags</span></span>           | <span data-ttu-id="b6af0-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6af0-178">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="b6af0-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b6af0-179">Classes used in</span></span>        | [<span data-ttu-id="b6af0-180">**Standort übergreifender Transport**</span><span class="sxs-lookup"><span data-stu-id="b6af0-180">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="b6af0-181">**Standort Link**</span><span class="sxs-lookup"><span data-stu-id="b6af0-181">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b6af0-182">Adam</span><span class="sxs-lookup"><span data-stu-id="b6af0-182">ADAM</span></span>



| <span data-ttu-id="b6af0-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6af0-183">Entry</span></span> | <span data-ttu-id="b6af0-184">Wert</span><span class="sxs-lookup"><span data-stu-id="b6af0-184">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6af0-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b6af0-185">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="b6af0-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6af0-186">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="b6af0-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6af0-187">System-Only</span></span>            | <span data-ttu-id="b6af0-188">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-188">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b6af0-189">Is-Single-Valued</span></span>       | <span data-ttu-id="b6af0-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="b6af0-190">True</span></span>                                                                                                       |
| <span data-ttu-id="b6af0-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b6af0-191">Is Indexed</span></span>             | <span data-ttu-id="b6af0-192">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-192">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b6af0-193">In Global Catalog</span></span>      | <span data-ttu-id="b6af0-194">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-194">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b6af0-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6af0-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b6af0-196">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="b6af0-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6af0-197">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="b6af0-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6af0-198">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="b6af0-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6af0-199">Search-Flags</span></span>           | <span data-ttu-id="b6af0-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6af0-200">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="b6af0-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6af0-201">System-Flags</span></span>           | <span data-ttu-id="b6af0-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6af0-202">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="b6af0-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b6af0-203">Classes used in</span></span>        | [<span data-ttu-id="b6af0-204">**Standort übergreifender Transport**</span><span class="sxs-lookup"><span data-stu-id="b6af0-204">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="b6af0-205">**Standort Link**</span><span class="sxs-lookup"><span data-stu-id="b6af0-205">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b6af0-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b6af0-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b6af0-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6af0-207">Entry</span></span> | <span data-ttu-id="b6af0-208">Wert</span><span class="sxs-lookup"><span data-stu-id="b6af0-208">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6af0-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b6af0-209">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="b6af0-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6af0-210">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="b6af0-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6af0-211">System-Only</span></span>            | <span data-ttu-id="b6af0-212">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-212">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b6af0-213">Is-Single-Valued</span></span>       | <span data-ttu-id="b6af0-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="b6af0-214">True</span></span>                                                                                                       |
| <span data-ttu-id="b6af0-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b6af0-215">Is Indexed</span></span>             | <span data-ttu-id="b6af0-216">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-216">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b6af0-217">In Global Catalog</span></span>      | <span data-ttu-id="b6af0-218">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-218">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b6af0-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6af0-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b6af0-220">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="b6af0-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6af0-221">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="b6af0-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6af0-222">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="b6af0-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6af0-223">Search-Flags</span></span>           | <span data-ttu-id="b6af0-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6af0-224">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="b6af0-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6af0-225">System-Flags</span></span>           | <span data-ttu-id="b6af0-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6af0-226">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="b6af0-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b6af0-227">Classes used in</span></span>        | [<span data-ttu-id="b6af0-228">**Standort übergreifender Transport**</span><span class="sxs-lookup"><span data-stu-id="b6af0-228">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="b6af0-229">**Standort Link**</span><span class="sxs-lookup"><span data-stu-id="b6af0-229">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b6af0-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6af0-230">Windows Server 2008</span></span>



| <span data-ttu-id="b6af0-231">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6af0-231">Entry</span></span> | <span data-ttu-id="b6af0-232">Wert</span><span class="sxs-lookup"><span data-stu-id="b6af0-232">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6af0-233">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b6af0-233">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="b6af0-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6af0-234">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="b6af0-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6af0-235">System-Only</span></span>            | <span data-ttu-id="b6af0-236">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-236">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b6af0-237">Is-Single-Valued</span></span>       | <span data-ttu-id="b6af0-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="b6af0-238">True</span></span>                                                                                                       |
| <span data-ttu-id="b6af0-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b6af0-239">Is Indexed</span></span>             | <span data-ttu-id="b6af0-240">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-240">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b6af0-241">In Global Catalog</span></span>      | <span data-ttu-id="b6af0-242">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-242">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b6af0-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6af0-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b6af0-244">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="b6af0-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6af0-245">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="b6af0-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6af0-246">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="b6af0-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6af0-247">Search-Flags</span></span>           | <span data-ttu-id="b6af0-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6af0-248">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="b6af0-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6af0-249">System-Flags</span></span>           | <span data-ttu-id="b6af0-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6af0-250">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="b6af0-251">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b6af0-251">Classes used in</span></span>        | [<span data-ttu-id="b6af0-252">**Standort übergreifender Transport**</span><span class="sxs-lookup"><span data-stu-id="b6af0-252">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="b6af0-253">**Standort Link**</span><span class="sxs-lookup"><span data-stu-id="b6af0-253">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b6af0-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b6af0-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b6af0-255">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6af0-255">Entry</span></span> | <span data-ttu-id="b6af0-256">Wert</span><span class="sxs-lookup"><span data-stu-id="b6af0-256">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6af0-257">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b6af0-257">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="b6af0-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6af0-258">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="b6af0-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6af0-259">System-Only</span></span>            | <span data-ttu-id="b6af0-260">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-260">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-261">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b6af0-261">Is-Single-Valued</span></span>       | <span data-ttu-id="b6af0-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="b6af0-262">True</span></span>                                                                                                       |
| <span data-ttu-id="b6af0-263">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b6af0-263">Is Indexed</span></span>             | <span data-ttu-id="b6af0-264">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-264">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-265">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b6af0-265">In Global Catalog</span></span>      | <span data-ttu-id="b6af0-266">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-266">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b6af0-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6af0-268">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b6af0-268">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="b6af0-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6af0-269">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="b6af0-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6af0-270">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="b6af0-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6af0-271">Search-Flags</span></span>           | <span data-ttu-id="b6af0-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6af0-272">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="b6af0-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6af0-273">System-Flags</span></span>           | <span data-ttu-id="b6af0-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6af0-274">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="b6af0-275">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b6af0-275">Classes used in</span></span>        | [<span data-ttu-id="b6af0-276">**Standort übergreifender Transport**</span><span class="sxs-lookup"><span data-stu-id="b6af0-276">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="b6af0-277">**Standort Link**</span><span class="sxs-lookup"><span data-stu-id="b6af0-277">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b6af0-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b6af0-278">Windows Server 2012</span></span>



| <span data-ttu-id="b6af0-279">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6af0-279">Entry</span></span> | <span data-ttu-id="b6af0-280">Wert</span><span class="sxs-lookup"><span data-stu-id="b6af0-280">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6af0-281">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b6af0-281">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="b6af0-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6af0-282">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="b6af0-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6af0-283">System-Only</span></span>            | <span data-ttu-id="b6af0-284">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-284">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-285">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b6af0-285">Is-Single-Valued</span></span>       | <span data-ttu-id="b6af0-286">Richtig</span><span class="sxs-lookup"><span data-stu-id="b6af0-286">True</span></span>                                                                                                       |
| <span data-ttu-id="b6af0-287">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b6af0-287">Is Indexed</span></span>             | <span data-ttu-id="b6af0-288">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-288">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-289">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b6af0-289">In Global Catalog</span></span>      | <span data-ttu-id="b6af0-290">False</span><span class="sxs-lookup"><span data-stu-id="b6af0-290">False</span></span>                                                                                                      |
| <span data-ttu-id="b6af0-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b6af0-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6af0-292">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b6af0-292">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="b6af0-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6af0-293">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="b6af0-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6af0-294">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="b6af0-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6af0-295">Search-Flags</span></span>           | <span data-ttu-id="b6af0-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6af0-296">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="b6af0-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6af0-297">System-Flags</span></span>           | <span data-ttu-id="b6af0-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6af0-298">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="b6af0-299">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b6af0-299">Classes used in</span></span>        | [<span data-ttu-id="b6af0-300">**Standort übergreifender Transport**</span><span class="sxs-lookup"><span data-stu-id="b6af0-300">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="b6af0-301">**Standort Link**</span><span class="sxs-lookup"><span data-stu-id="b6af0-301">**Site-Link**</span></span>](c-sitelink.md)<br/> |



 

 





