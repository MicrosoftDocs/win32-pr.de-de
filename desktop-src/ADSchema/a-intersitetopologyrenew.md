---
title: Inter-Site-Topology-Renew-Attribut
description: Diese Klasse gibt an, wie oft der standortübergreifende Topologiegenerator die Keep-Alive-Nachricht aktualisiert, die an Domänen Controller am selben Standort gesendet wird.
ms.assetid: 523d8161-0678-482f-8d66-55a112995fe5
ms.tgt_platform: multiple
keywords:
- Inter-Site-Topology-Renew-Attribut AD-Schema
- "\"intersitetopologyrenew\"-Attribut, AD-Schema"
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Renew
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821bd294f777fd29738ff102955cd170a42205e2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106343515"
---
# <a name="inter-site-topology-renew-attribute"></a><span data-ttu-id="d5c55-105">Inter-Site-Topology-Renew-Attribut</span><span class="sxs-lookup"><span data-stu-id="d5c55-105">Inter-Site-Topology-Renew attribute</span></span>

<span data-ttu-id="d5c55-106">Diese Klasse gibt an, wie oft der standortübergreifende Topologiegenerator die Keep-Alive-Nachricht aktualisiert, die an Domänen Controller am selben Standort gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d5c55-106">This class indicates how often the intersite topology generator updates the keep-alive message that is sent to domain controllers contained in the same site.</span></span>



| <span data-ttu-id="d5c55-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d5c55-107">Entry</span></span> | <span data-ttu-id="d5c55-108">Wert</span><span class="sxs-lookup"><span data-stu-id="d5c55-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d5c55-109">CN</span><span class="sxs-lookup"><span data-stu-id="d5c55-109">CN</span></span>                | <span data-ttu-id="d5c55-110">Standortübergreifende Topologie-Erneuerung</span><span class="sxs-lookup"><span data-stu-id="d5c55-110">Inter-Site-Topology-Renew</span></span>            |
| <span data-ttu-id="d5c55-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d5c55-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d5c55-112">intersitetopologyrenew</span><span class="sxs-lookup"><span data-stu-id="d5c55-112">interSiteTopologyRenew</span></span>               |
| <span data-ttu-id="d5c55-113">Size</span><span class="sxs-lookup"><span data-stu-id="d5c55-113">Size</span></span>              | <span data-ttu-id="d5c55-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="d5c55-114">4 bytes</span></span>                              |
| <span data-ttu-id="d5c55-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d5c55-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="d5c55-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="d5c55-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="d5c55-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d5c55-117">Attribute-Id</span></span>      | <span data-ttu-id="d5c55-118">1.2.840.113556.1.4.1247</span><span class="sxs-lookup"><span data-stu-id="d5c55-118">1.2.840.113556.1.4.1247</span></span>              |
| <span data-ttu-id="d5c55-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d5c55-119">System-Id-Guid</span></span>    | <span data-ttu-id="d5c55-120">b7c69e5f-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="d5c55-120">b7c69e5f-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="d5c55-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5c55-121">Syntax</span></span>            | [<span data-ttu-id="d5c55-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="d5c55-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="d5c55-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="d5c55-123">Implementations</span></span>

-   [<span data-ttu-id="d5c55-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d5c55-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d5c55-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d5c55-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d5c55-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="d5c55-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d5c55-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d5c55-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d5c55-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d5c55-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d5c55-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d5c55-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d5c55-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d5c55-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d5c55-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d5c55-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d5c55-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d5c55-132">Entry</span></span> | <span data-ttu-id="d5c55-133">Wert</span><span class="sxs-lookup"><span data-stu-id="d5c55-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5c55-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d5c55-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5c55-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c55-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5c55-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c55-136">System-Only</span></span>            | <span data-ttu-id="d5c55-137">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-137">False</span></span>                                                       |
| <span data-ttu-id="d5c55-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d5c55-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c55-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="d5c55-139">True</span></span>                                                        |
| <span data-ttu-id="d5c55-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d5c55-140">Is Indexed</span></span>             | <span data-ttu-id="d5c55-141">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-141">False</span></span>                                                       |
| <span data-ttu-id="d5c55-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d5c55-142">In Global Catalog</span></span>      | <span data-ttu-id="d5c55-143">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-143">False</span></span>                                                       |
| <span data-ttu-id="d5c55-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d5c55-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c55-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d5c55-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d5c55-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c55-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d5c55-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c55-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d5c55-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c55-148">Search-Flags</span></span>           | <span data-ttu-id="d5c55-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c55-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="d5c55-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c55-150">System-Flags</span></span>           | <span data-ttu-id="d5c55-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c55-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="d5c55-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d5c55-152">Classes used in</span></span>        | [<span data-ttu-id="d5c55-153">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="d5c55-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d5c55-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d5c55-154">Windows Server 2003</span></span>



| <span data-ttu-id="d5c55-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d5c55-155">Entry</span></span> | <span data-ttu-id="d5c55-156">Wert</span><span class="sxs-lookup"><span data-stu-id="d5c55-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5c55-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d5c55-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5c55-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c55-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5c55-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c55-159">System-Only</span></span>            | <span data-ttu-id="d5c55-160">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-160">False</span></span>                                                       |
| <span data-ttu-id="d5c55-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d5c55-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c55-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="d5c55-162">True</span></span>                                                        |
| <span data-ttu-id="d5c55-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d5c55-163">Is Indexed</span></span>             | <span data-ttu-id="d5c55-164">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-164">False</span></span>                                                       |
| <span data-ttu-id="d5c55-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d5c55-165">In Global Catalog</span></span>      | <span data-ttu-id="d5c55-166">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-166">False</span></span>                                                       |
| <span data-ttu-id="d5c55-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d5c55-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c55-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d5c55-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d5c55-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c55-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d5c55-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c55-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d5c55-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c55-171">Search-Flags</span></span>           | <span data-ttu-id="d5c55-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c55-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="d5c55-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c55-173">System-Flags</span></span>           | <span data-ttu-id="d5c55-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c55-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="d5c55-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d5c55-175">Classes used in</span></span>        | [<span data-ttu-id="d5c55-176">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="d5c55-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d5c55-177">Adam</span><span class="sxs-lookup"><span data-stu-id="d5c55-177">ADAM</span></span>



| <span data-ttu-id="d5c55-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d5c55-178">Entry</span></span> | <span data-ttu-id="d5c55-179">Wert</span><span class="sxs-lookup"><span data-stu-id="d5c55-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5c55-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d5c55-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5c55-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c55-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5c55-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c55-182">System-Only</span></span>            | <span data-ttu-id="d5c55-183">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-183">False</span></span>                                                       |
| <span data-ttu-id="d5c55-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d5c55-184">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c55-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="d5c55-185">True</span></span>                                                        |
| <span data-ttu-id="d5c55-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d5c55-186">Is Indexed</span></span>             | <span data-ttu-id="d5c55-187">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-187">False</span></span>                                                       |
| <span data-ttu-id="d5c55-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d5c55-188">In Global Catalog</span></span>      | <span data-ttu-id="d5c55-189">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-189">False</span></span>                                                       |
| <span data-ttu-id="d5c55-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d5c55-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c55-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d5c55-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d5c55-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c55-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d5c55-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c55-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d5c55-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c55-194">Search-Flags</span></span>           | <span data-ttu-id="d5c55-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c55-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="d5c55-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c55-196">System-Flags</span></span>           | <span data-ttu-id="d5c55-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c55-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="d5c55-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d5c55-198">Classes used in</span></span>        | [<span data-ttu-id="d5c55-199">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="d5c55-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d5c55-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d5c55-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d5c55-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d5c55-201">Entry</span></span> | <span data-ttu-id="d5c55-202">Wert</span><span class="sxs-lookup"><span data-stu-id="d5c55-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5c55-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d5c55-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5c55-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c55-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5c55-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c55-205">System-Only</span></span>            | <span data-ttu-id="d5c55-206">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-206">False</span></span>                                                       |
| <span data-ttu-id="d5c55-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d5c55-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c55-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="d5c55-208">True</span></span>                                                        |
| <span data-ttu-id="d5c55-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d5c55-209">Is Indexed</span></span>             | <span data-ttu-id="d5c55-210">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-210">False</span></span>                                                       |
| <span data-ttu-id="d5c55-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d5c55-211">In Global Catalog</span></span>      | <span data-ttu-id="d5c55-212">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-212">False</span></span>                                                       |
| <span data-ttu-id="d5c55-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d5c55-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c55-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d5c55-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d5c55-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c55-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d5c55-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c55-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d5c55-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c55-217">Search-Flags</span></span>           | <span data-ttu-id="d5c55-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c55-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="d5c55-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c55-219">System-Flags</span></span>           | <span data-ttu-id="d5c55-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c55-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="d5c55-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d5c55-221">Classes used in</span></span>        | [<span data-ttu-id="d5c55-222">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="d5c55-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d5c55-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5c55-223">Windows Server 2008</span></span>



| <span data-ttu-id="d5c55-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d5c55-224">Entry</span></span> | <span data-ttu-id="d5c55-225">Wert</span><span class="sxs-lookup"><span data-stu-id="d5c55-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5c55-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d5c55-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5c55-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c55-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5c55-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c55-228">System-Only</span></span>            | <span data-ttu-id="d5c55-229">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-229">False</span></span>                                                       |
| <span data-ttu-id="d5c55-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d5c55-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c55-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="d5c55-231">True</span></span>                                                        |
| <span data-ttu-id="d5c55-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d5c55-232">Is Indexed</span></span>             | <span data-ttu-id="d5c55-233">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-233">False</span></span>                                                       |
| <span data-ttu-id="d5c55-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d5c55-234">In Global Catalog</span></span>      | <span data-ttu-id="d5c55-235">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-235">False</span></span>                                                       |
| <span data-ttu-id="d5c55-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d5c55-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c55-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d5c55-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d5c55-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c55-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d5c55-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c55-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d5c55-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c55-240">Search-Flags</span></span>           | <span data-ttu-id="d5c55-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c55-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="d5c55-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c55-242">System-Flags</span></span>           | <span data-ttu-id="d5c55-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c55-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="d5c55-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d5c55-244">Classes used in</span></span>        | [<span data-ttu-id="d5c55-245">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="d5c55-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d5c55-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d5c55-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d5c55-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d5c55-247">Entry</span></span> | <span data-ttu-id="d5c55-248">Wert</span><span class="sxs-lookup"><span data-stu-id="d5c55-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5c55-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d5c55-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5c55-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c55-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5c55-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c55-251">System-Only</span></span>            | <span data-ttu-id="d5c55-252">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-252">False</span></span>                                                       |
| <span data-ttu-id="d5c55-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d5c55-253">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c55-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="d5c55-254">True</span></span>                                                        |
| <span data-ttu-id="d5c55-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d5c55-255">Is Indexed</span></span>             | <span data-ttu-id="d5c55-256">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-256">False</span></span>                                                       |
| <span data-ttu-id="d5c55-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d5c55-257">In Global Catalog</span></span>      | <span data-ttu-id="d5c55-258">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-258">False</span></span>                                                       |
| <span data-ttu-id="d5c55-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d5c55-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c55-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d5c55-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d5c55-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c55-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d5c55-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c55-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d5c55-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c55-263">Search-Flags</span></span>           | <span data-ttu-id="d5c55-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c55-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="d5c55-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c55-265">System-Flags</span></span>           | <span data-ttu-id="d5c55-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c55-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="d5c55-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d5c55-267">Classes used in</span></span>        | [<span data-ttu-id="d5c55-268">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="d5c55-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d5c55-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d5c55-269">Windows Server 2012</span></span>



| <span data-ttu-id="d5c55-270">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d5c55-270">Entry</span></span> | <span data-ttu-id="d5c55-271">Wert</span><span class="sxs-lookup"><span data-stu-id="d5c55-271">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5c55-272">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d5c55-272">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5c55-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c55-273">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5c55-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c55-274">System-Only</span></span>            | <span data-ttu-id="d5c55-275">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-275">False</span></span>                                                       |
| <span data-ttu-id="d5c55-276">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d5c55-276">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c55-277">Richtig</span><span class="sxs-lookup"><span data-stu-id="d5c55-277">True</span></span>                                                        |
| <span data-ttu-id="d5c55-278">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d5c55-278">Is Indexed</span></span>             | <span data-ttu-id="d5c55-279">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-279">False</span></span>                                                       |
| <span data-ttu-id="d5c55-280">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d5c55-280">In Global Catalog</span></span>      | <span data-ttu-id="d5c55-281">False</span><span class="sxs-lookup"><span data-stu-id="d5c55-281">False</span></span>                                                       |
| <span data-ttu-id="d5c55-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d5c55-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c55-283">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d5c55-283">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d5c55-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c55-284">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d5c55-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c55-285">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d5c55-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c55-286">Search-Flags</span></span>           | <span data-ttu-id="d5c55-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c55-287">0x00000000</span></span>                                                  |
| <span data-ttu-id="d5c55-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c55-288">System-Flags</span></span>           | <span data-ttu-id="d5c55-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c55-289">0x00000010</span></span>                                                  |
| <span data-ttu-id="d5c55-290">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d5c55-290">Classes used in</span></span>        | [<span data-ttu-id="d5c55-291">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="d5c55-291">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





