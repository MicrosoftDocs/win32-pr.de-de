---
title: 'Standortübergreifende Topologie: Failover-Attribut'
description: Gibt an, wie viel Zeit seit dem letzten Keep-Alive für den standortübergreifenden Topologiegenerator in Erwägung gezogen werden muss.
ms.assetid: d351dbec-d5a3-46e1-87a9-0856d19e07c6
ms.tgt_platform: multiple
keywords:
- Standortübergreifende Topologie-Failover-Attribut AD-Schema
- intersitetopologyfailover-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Failover
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4e9cad98bade7fd69178a8fce795d0b92f35b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480191"
---
# <a name="inter-site-topology-failover-attribute"></a><span data-ttu-id="7a152-105">Standortübergreifende Topologie: Failover-Attribut</span><span class="sxs-lookup"><span data-stu-id="7a152-105">Inter-Site-Topology-Failover attribute</span></span>

<span data-ttu-id="7a152-106">Gibt an, wie viel Zeit seit dem letzten Keep-Alive für den standortübergreifenden Topologiegenerator in Erwägung gezogen werden muss.</span><span class="sxs-lookup"><span data-stu-id="7a152-106">Indicates how much time must transpire since the last keep-alive for the inter-site topology generator to be considered dead.</span></span>



| <span data-ttu-id="7a152-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a152-107">Entry</span></span> | <span data-ttu-id="7a152-108">Wert</span><span class="sxs-lookup"><span data-stu-id="7a152-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7a152-109">CN</span><span class="sxs-lookup"><span data-stu-id="7a152-109">CN</span></span>                | <span data-ttu-id="7a152-110">Standortübergreifende Topologie-Failover</span><span class="sxs-lookup"><span data-stu-id="7a152-110">Inter-Site-Topology-Failover</span></span>         |
| <span data-ttu-id="7a152-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7a152-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7a152-112">intersitetopologyfailover</span><span class="sxs-lookup"><span data-stu-id="7a152-112">interSiteTopologyFailover</span></span>            |
| <span data-ttu-id="7a152-113">Size</span><span class="sxs-lookup"><span data-stu-id="7a152-113">Size</span></span>              | <span data-ttu-id="7a152-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="7a152-114">4 bytes</span></span>                              |
| <span data-ttu-id="7a152-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="7a152-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="7a152-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="7a152-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7a152-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7a152-117">Attribute-Id</span></span>      | <span data-ttu-id="7a152-118">1.2.840.113556.1.4.1248</span><span class="sxs-lookup"><span data-stu-id="7a152-118">1.2.840.113556.1.4.1248</span></span>              |
| <span data-ttu-id="7a152-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7a152-119">System-Id-Guid</span></span>    | <span data-ttu-id="7a152-120">b7c69e60-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="7a152-120">b7c69e60-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="7a152-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a152-121">Syntax</span></span>            | [<span data-ttu-id="7a152-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="7a152-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="7a152-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="7a152-123">Implementations</span></span>

-   [<span data-ttu-id="7a152-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7a152-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7a152-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7a152-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7a152-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="7a152-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7a152-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7a152-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7a152-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7a152-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7a152-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7a152-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7a152-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7a152-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7a152-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7a152-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7a152-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a152-132">Entry</span></span> | <span data-ttu-id="7a152-133">Wert</span><span class="sxs-lookup"><span data-stu-id="7a152-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7a152-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7a152-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7a152-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a152-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7a152-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a152-136">System-Only</span></span>            | <span data-ttu-id="7a152-137">False</span><span class="sxs-lookup"><span data-stu-id="7a152-137">False</span></span>                                                       |
| <span data-ttu-id="7a152-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7a152-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7a152-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a152-139">True</span></span>                                                        |
| <span data-ttu-id="7a152-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7a152-140">Is Indexed</span></span>             | <span data-ttu-id="7a152-141">False</span><span class="sxs-lookup"><span data-stu-id="7a152-141">False</span></span>                                                       |
| <span data-ttu-id="7a152-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7a152-142">In Global Catalog</span></span>      | <span data-ttu-id="7a152-143">False</span><span class="sxs-lookup"><span data-stu-id="7a152-143">False</span></span>                                                       |
| <span data-ttu-id="7a152-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a152-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a152-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7a152-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7a152-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a152-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7a152-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a152-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7a152-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a152-148">Search-Flags</span></span>           | <span data-ttu-id="7a152-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a152-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="7a152-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a152-150">System-Flags</span></span>           | <span data-ttu-id="7a152-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a152-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="7a152-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7a152-152">Classes used in</span></span>        | [<span data-ttu-id="7a152-153">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7a152-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7a152-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7a152-154">Windows Server 2003</span></span>



| <span data-ttu-id="7a152-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a152-155">Entry</span></span> | <span data-ttu-id="7a152-156">Wert</span><span class="sxs-lookup"><span data-stu-id="7a152-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7a152-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7a152-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7a152-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a152-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7a152-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a152-159">System-Only</span></span>            | <span data-ttu-id="7a152-160">False</span><span class="sxs-lookup"><span data-stu-id="7a152-160">False</span></span>                                                       |
| <span data-ttu-id="7a152-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7a152-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7a152-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a152-162">True</span></span>                                                        |
| <span data-ttu-id="7a152-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7a152-163">Is Indexed</span></span>             | <span data-ttu-id="7a152-164">False</span><span class="sxs-lookup"><span data-stu-id="7a152-164">False</span></span>                                                       |
| <span data-ttu-id="7a152-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7a152-165">In Global Catalog</span></span>      | <span data-ttu-id="7a152-166">False</span><span class="sxs-lookup"><span data-stu-id="7a152-166">False</span></span>                                                       |
| <span data-ttu-id="7a152-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a152-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a152-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7a152-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7a152-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a152-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7a152-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a152-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7a152-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a152-171">Search-Flags</span></span>           | <span data-ttu-id="7a152-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a152-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="7a152-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a152-173">System-Flags</span></span>           | <span data-ttu-id="7a152-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a152-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="7a152-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7a152-175">Classes used in</span></span>        | [<span data-ttu-id="7a152-176">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7a152-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7a152-177">Adam</span><span class="sxs-lookup"><span data-stu-id="7a152-177">ADAM</span></span>



| <span data-ttu-id="7a152-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a152-178">Entry</span></span> | <span data-ttu-id="7a152-179">Wert</span><span class="sxs-lookup"><span data-stu-id="7a152-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7a152-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7a152-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7a152-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a152-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7a152-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a152-182">System-Only</span></span>            | <span data-ttu-id="7a152-183">False</span><span class="sxs-lookup"><span data-stu-id="7a152-183">False</span></span>                                                       |
| <span data-ttu-id="7a152-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7a152-184">Is-Single-Valued</span></span>       | <span data-ttu-id="7a152-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a152-185">True</span></span>                                                        |
| <span data-ttu-id="7a152-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7a152-186">Is Indexed</span></span>             | <span data-ttu-id="7a152-187">False</span><span class="sxs-lookup"><span data-stu-id="7a152-187">False</span></span>                                                       |
| <span data-ttu-id="7a152-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7a152-188">In Global Catalog</span></span>      | <span data-ttu-id="7a152-189">False</span><span class="sxs-lookup"><span data-stu-id="7a152-189">False</span></span>                                                       |
| <span data-ttu-id="7a152-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a152-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a152-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7a152-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7a152-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a152-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7a152-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a152-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7a152-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a152-194">Search-Flags</span></span>           | <span data-ttu-id="7a152-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a152-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="7a152-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a152-196">System-Flags</span></span>           | <span data-ttu-id="7a152-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a152-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="7a152-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7a152-198">Classes used in</span></span>        | [<span data-ttu-id="7a152-199">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7a152-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7a152-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7a152-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7a152-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a152-201">Entry</span></span> | <span data-ttu-id="7a152-202">Wert</span><span class="sxs-lookup"><span data-stu-id="7a152-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7a152-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7a152-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7a152-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a152-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7a152-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a152-205">System-Only</span></span>            | <span data-ttu-id="7a152-206">False</span><span class="sxs-lookup"><span data-stu-id="7a152-206">False</span></span>                                                       |
| <span data-ttu-id="7a152-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7a152-207">Is-Single-Valued</span></span>       | <span data-ttu-id="7a152-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a152-208">True</span></span>                                                        |
| <span data-ttu-id="7a152-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7a152-209">Is Indexed</span></span>             | <span data-ttu-id="7a152-210">False</span><span class="sxs-lookup"><span data-stu-id="7a152-210">False</span></span>                                                       |
| <span data-ttu-id="7a152-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7a152-211">In Global Catalog</span></span>      | <span data-ttu-id="7a152-212">False</span><span class="sxs-lookup"><span data-stu-id="7a152-212">False</span></span>                                                       |
| <span data-ttu-id="7a152-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a152-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a152-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7a152-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7a152-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a152-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7a152-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a152-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7a152-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a152-217">Search-Flags</span></span>           | <span data-ttu-id="7a152-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a152-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="7a152-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a152-219">System-Flags</span></span>           | <span data-ttu-id="7a152-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a152-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="7a152-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7a152-221">Classes used in</span></span>        | [<span data-ttu-id="7a152-222">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7a152-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7a152-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a152-223">Windows Server 2008</span></span>



| <span data-ttu-id="7a152-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a152-224">Entry</span></span> | <span data-ttu-id="7a152-225">Wert</span><span class="sxs-lookup"><span data-stu-id="7a152-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7a152-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7a152-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7a152-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a152-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7a152-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a152-228">System-Only</span></span>            | <span data-ttu-id="7a152-229">False</span><span class="sxs-lookup"><span data-stu-id="7a152-229">False</span></span>                                                       |
| <span data-ttu-id="7a152-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7a152-230">Is-Single-Valued</span></span>       | <span data-ttu-id="7a152-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a152-231">True</span></span>                                                        |
| <span data-ttu-id="7a152-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7a152-232">Is Indexed</span></span>             | <span data-ttu-id="7a152-233">False</span><span class="sxs-lookup"><span data-stu-id="7a152-233">False</span></span>                                                       |
| <span data-ttu-id="7a152-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7a152-234">In Global Catalog</span></span>      | <span data-ttu-id="7a152-235">False</span><span class="sxs-lookup"><span data-stu-id="7a152-235">False</span></span>                                                       |
| <span data-ttu-id="7a152-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a152-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a152-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7a152-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7a152-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a152-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7a152-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a152-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7a152-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a152-240">Search-Flags</span></span>           | <span data-ttu-id="7a152-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a152-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="7a152-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a152-242">System-Flags</span></span>           | <span data-ttu-id="7a152-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a152-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="7a152-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7a152-244">Classes used in</span></span>        | [<span data-ttu-id="7a152-245">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7a152-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7a152-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7a152-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7a152-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a152-247">Entry</span></span> | <span data-ttu-id="7a152-248">Wert</span><span class="sxs-lookup"><span data-stu-id="7a152-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7a152-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7a152-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7a152-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a152-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7a152-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a152-251">System-Only</span></span>            | <span data-ttu-id="7a152-252">False</span><span class="sxs-lookup"><span data-stu-id="7a152-252">False</span></span>                                                       |
| <span data-ttu-id="7a152-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7a152-253">Is-Single-Valued</span></span>       | <span data-ttu-id="7a152-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a152-254">True</span></span>                                                        |
| <span data-ttu-id="7a152-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7a152-255">Is Indexed</span></span>             | <span data-ttu-id="7a152-256">False</span><span class="sxs-lookup"><span data-stu-id="7a152-256">False</span></span>                                                       |
| <span data-ttu-id="7a152-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7a152-257">In Global Catalog</span></span>      | <span data-ttu-id="7a152-258">False</span><span class="sxs-lookup"><span data-stu-id="7a152-258">False</span></span>                                                       |
| <span data-ttu-id="7a152-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a152-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a152-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7a152-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7a152-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a152-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7a152-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a152-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7a152-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a152-263">Search-Flags</span></span>           | <span data-ttu-id="7a152-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a152-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="7a152-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a152-265">System-Flags</span></span>           | <span data-ttu-id="7a152-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a152-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="7a152-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7a152-267">Classes used in</span></span>        | [<span data-ttu-id="7a152-268">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7a152-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7a152-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7a152-269">Windows Server 2012</span></span>



| <span data-ttu-id="7a152-270">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a152-270">Entry</span></span> | <span data-ttu-id="7a152-271">Wert</span><span class="sxs-lookup"><span data-stu-id="7a152-271">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7a152-272">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7a152-272">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7a152-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a152-273">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7a152-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a152-274">System-Only</span></span>            | <span data-ttu-id="7a152-275">False</span><span class="sxs-lookup"><span data-stu-id="7a152-275">False</span></span>                                                       |
| <span data-ttu-id="7a152-276">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7a152-276">Is-Single-Valued</span></span>       | <span data-ttu-id="7a152-277">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a152-277">True</span></span>                                                        |
| <span data-ttu-id="7a152-278">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7a152-278">Is Indexed</span></span>             | <span data-ttu-id="7a152-279">False</span><span class="sxs-lookup"><span data-stu-id="7a152-279">False</span></span>                                                       |
| <span data-ttu-id="7a152-280">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7a152-280">In Global Catalog</span></span>      | <span data-ttu-id="7a152-281">False</span><span class="sxs-lookup"><span data-stu-id="7a152-281">False</span></span>                                                       |
| <span data-ttu-id="7a152-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a152-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a152-283">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7a152-283">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7a152-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a152-284">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7a152-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a152-285">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7a152-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a152-286">Search-Flags</span></span>           | <span data-ttu-id="7a152-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a152-287">0x00000000</span></span>                                                  |
| <span data-ttu-id="7a152-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a152-288">System-Flags</span></span>           | <span data-ttu-id="7a152-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a152-289">0x00000010</span></span>                                                  |
| <span data-ttu-id="7a152-290">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7a152-290">Classes used in</span></span>        | [<span data-ttu-id="7a152-291">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7a152-291">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





