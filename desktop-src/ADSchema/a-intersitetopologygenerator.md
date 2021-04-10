---
title: Standort übergreifender Topologiegenerator-Attribut
description: Dieses Attribut wird verwendet, um ein Failover für den Computer zu unterstützen, der die Wissens Konsistenzprüfung der standortübergreifenden Topologiegenerierung an einem bestimmten Standort ausführt.
ms.assetid: 077f4331-ead9-4f17-942e-d55cf253d03b
ms.tgt_platform: multiple
keywords:
- AD-Schema für standortübergreifende Topologie-Generator-Attribut
- AD-Schema für das InterSiteTopologyGenerator-Attribut
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Generator
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df7b354d05e882373715e4c49498c9daff41652
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107025"
---
# <a name="inter-site-topology-generator-attribute"></a><span data-ttu-id="7500c-105">Standort übergreifender Topologiegenerator-Attribut</span><span class="sxs-lookup"><span data-stu-id="7500c-105">Inter-Site-Topology-Generator attribute</span></span>

<span data-ttu-id="7500c-106">Dieses Attribut wird verwendet, um ein Failover für den Computer zu unterstützen, der die Wissens Konsistenzprüfung der standortübergreifenden Topologiegenerierung an einem bestimmten Standort ausführt.</span><span class="sxs-lookup"><span data-stu-id="7500c-106">This attribute will be used to support failover for the computer designated as the one that runs Knowledge Consistency Checker inter-site topology generation in a given site.</span></span>



| <span data-ttu-id="7500c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7500c-107">Entry</span></span> | <span data-ttu-id="7500c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="7500c-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="7500c-109">CN</span><span class="sxs-lookup"><span data-stu-id="7500c-109">CN</span></span>                | <span data-ttu-id="7500c-110">Standort übergreifender Topologiegenerator</span><span class="sxs-lookup"><span data-stu-id="7500c-110">Inter-Site-Topology-Generator</span></span>           |
| <span data-ttu-id="7500c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7500c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7500c-112">InterSiteTopologyGenerator</span><span class="sxs-lookup"><span data-stu-id="7500c-112">interSiteTopologyGenerator</span></span>              |
| <span data-ttu-id="7500c-113">Size</span><span class="sxs-lookup"><span data-stu-id="7500c-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="7500c-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="7500c-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="7500c-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="7500c-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="7500c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7500c-116">Attribute-Id</span></span>      | <span data-ttu-id="7500c-117">1.2.840.113556.1.4.1246</span><span class="sxs-lookup"><span data-stu-id="7500c-117">1.2.840.113556.1.4.1246</span></span>                 |
| <span data-ttu-id="7500c-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7500c-118">System-Id-Guid</span></span>    | <span data-ttu-id="7500c-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="7500c-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span></span>    |
| <span data-ttu-id="7500c-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="7500c-120">Syntax</span></span>            | [<span data-ttu-id="7500c-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="7500c-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="7500c-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="7500c-122">Implementations</span></span>

-   [<span data-ttu-id="7500c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7500c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7500c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7500c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7500c-125">**Adam**</span><span class="sxs-lookup"><span data-stu-id="7500c-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7500c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7500c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7500c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7500c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7500c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7500c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7500c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7500c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7500c-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7500c-130">Windows 2000 Server</span></span>



| <span data-ttu-id="7500c-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7500c-131">Entry</span></span> | <span data-ttu-id="7500c-132">Wert</span><span class="sxs-lookup"><span data-stu-id="7500c-132">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7500c-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7500c-133">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7500c-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7500c-134">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7500c-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7500c-135">System-Only</span></span>            | <span data-ttu-id="7500c-136">False</span><span class="sxs-lookup"><span data-stu-id="7500c-136">False</span></span>                                                       |
| <span data-ttu-id="7500c-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7500c-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7500c-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="7500c-138">True</span></span>                                                        |
| <span data-ttu-id="7500c-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7500c-139">Is Indexed</span></span>             | <span data-ttu-id="7500c-140">False</span><span class="sxs-lookup"><span data-stu-id="7500c-140">False</span></span>                                                       |
| <span data-ttu-id="7500c-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7500c-141">In Global Catalog</span></span>      | <span data-ttu-id="7500c-142">False</span><span class="sxs-lookup"><span data-stu-id="7500c-142">False</span></span>                                                       |
| <span data-ttu-id="7500c-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7500c-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7500c-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7500c-144">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7500c-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7500c-145">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7500c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7500c-146">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7500c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7500c-147">Search-Flags</span></span>           | <span data-ttu-id="7500c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7500c-148">0x00000000</span></span>                                                  |
| <span data-ttu-id="7500c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7500c-149">System-Flags</span></span>           | <span data-ttu-id="7500c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7500c-150">0x00000010</span></span>                                                  |
| <span data-ttu-id="7500c-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7500c-151">Classes used in</span></span>        | [<span data-ttu-id="7500c-152">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7500c-152">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7500c-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7500c-153">Windows Server 2003</span></span>



| <span data-ttu-id="7500c-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7500c-154">Entry</span></span> | <span data-ttu-id="7500c-155">Wert</span><span class="sxs-lookup"><span data-stu-id="7500c-155">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7500c-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7500c-156">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7500c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7500c-157">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7500c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="7500c-158">System-Only</span></span>            | <span data-ttu-id="7500c-159">False</span><span class="sxs-lookup"><span data-stu-id="7500c-159">False</span></span>                                                       |
| <span data-ttu-id="7500c-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7500c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="7500c-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="7500c-161">True</span></span>                                                        |
| <span data-ttu-id="7500c-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7500c-162">Is Indexed</span></span>             | <span data-ttu-id="7500c-163">False</span><span class="sxs-lookup"><span data-stu-id="7500c-163">False</span></span>                                                       |
| <span data-ttu-id="7500c-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7500c-164">In Global Catalog</span></span>      | <span data-ttu-id="7500c-165">False</span><span class="sxs-lookup"><span data-stu-id="7500c-165">False</span></span>                                                       |
| <span data-ttu-id="7500c-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7500c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="7500c-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7500c-167">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7500c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7500c-168">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7500c-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7500c-169">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7500c-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7500c-170">Search-Flags</span></span>           | <span data-ttu-id="7500c-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7500c-171">0x00000000</span></span>                                                  |
| <span data-ttu-id="7500c-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7500c-172">System-Flags</span></span>           | <span data-ttu-id="7500c-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7500c-173">0x00000010</span></span>                                                  |
| <span data-ttu-id="7500c-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7500c-174">Classes used in</span></span>        | [<span data-ttu-id="7500c-175">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7500c-175">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7500c-176">Adam</span><span class="sxs-lookup"><span data-stu-id="7500c-176">ADAM</span></span>



| <span data-ttu-id="7500c-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7500c-177">Entry</span></span> | <span data-ttu-id="7500c-178">Wert</span><span class="sxs-lookup"><span data-stu-id="7500c-178">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7500c-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7500c-179">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7500c-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7500c-180">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7500c-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7500c-181">System-Only</span></span>            | <span data-ttu-id="7500c-182">False</span><span class="sxs-lookup"><span data-stu-id="7500c-182">False</span></span>                                                       |
| <span data-ttu-id="7500c-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7500c-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7500c-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="7500c-184">True</span></span>                                                        |
| <span data-ttu-id="7500c-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7500c-185">Is Indexed</span></span>             | <span data-ttu-id="7500c-186">False</span><span class="sxs-lookup"><span data-stu-id="7500c-186">False</span></span>                                                       |
| <span data-ttu-id="7500c-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7500c-187">In Global Catalog</span></span>      | <span data-ttu-id="7500c-188">False</span><span class="sxs-lookup"><span data-stu-id="7500c-188">False</span></span>                                                       |
| <span data-ttu-id="7500c-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7500c-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7500c-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7500c-190">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7500c-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7500c-191">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7500c-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7500c-192">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7500c-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7500c-193">Search-Flags</span></span>           | <span data-ttu-id="7500c-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7500c-194">0x00000000</span></span>                                                  |
| <span data-ttu-id="7500c-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7500c-195">System-Flags</span></span>           | <span data-ttu-id="7500c-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7500c-196">0x00000010</span></span>                                                  |
| <span data-ttu-id="7500c-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7500c-197">Classes used in</span></span>        | [<span data-ttu-id="7500c-198">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7500c-198">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7500c-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7500c-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7500c-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7500c-200">Entry</span></span> | <span data-ttu-id="7500c-201">Wert</span><span class="sxs-lookup"><span data-stu-id="7500c-201">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7500c-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7500c-202">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7500c-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7500c-203">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7500c-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="7500c-204">System-Only</span></span>            | <span data-ttu-id="7500c-205">False</span><span class="sxs-lookup"><span data-stu-id="7500c-205">False</span></span>                                                       |
| <span data-ttu-id="7500c-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7500c-206">Is-Single-Valued</span></span>       | <span data-ttu-id="7500c-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="7500c-207">True</span></span>                                                        |
| <span data-ttu-id="7500c-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7500c-208">Is Indexed</span></span>             | <span data-ttu-id="7500c-209">False</span><span class="sxs-lookup"><span data-stu-id="7500c-209">False</span></span>                                                       |
| <span data-ttu-id="7500c-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7500c-210">In Global Catalog</span></span>      | <span data-ttu-id="7500c-211">False</span><span class="sxs-lookup"><span data-stu-id="7500c-211">False</span></span>                                                       |
| <span data-ttu-id="7500c-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7500c-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="7500c-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7500c-213">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7500c-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7500c-214">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7500c-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7500c-215">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7500c-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7500c-216">Search-Flags</span></span>           | <span data-ttu-id="7500c-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7500c-217">0x00000000</span></span>                                                  |
| <span data-ttu-id="7500c-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7500c-218">System-Flags</span></span>           | <span data-ttu-id="7500c-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7500c-219">0x00000010</span></span>                                                  |
| <span data-ttu-id="7500c-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7500c-220">Classes used in</span></span>        | [<span data-ttu-id="7500c-221">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7500c-221">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7500c-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7500c-222">Windows Server 2008</span></span>



| <span data-ttu-id="7500c-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7500c-223">Entry</span></span> | <span data-ttu-id="7500c-224">Wert</span><span class="sxs-lookup"><span data-stu-id="7500c-224">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7500c-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7500c-225">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7500c-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7500c-226">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7500c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="7500c-227">System-Only</span></span>            | <span data-ttu-id="7500c-228">False</span><span class="sxs-lookup"><span data-stu-id="7500c-228">False</span></span>                                                       |
| <span data-ttu-id="7500c-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7500c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="7500c-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="7500c-230">True</span></span>                                                        |
| <span data-ttu-id="7500c-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7500c-231">Is Indexed</span></span>             | <span data-ttu-id="7500c-232">False</span><span class="sxs-lookup"><span data-stu-id="7500c-232">False</span></span>                                                       |
| <span data-ttu-id="7500c-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7500c-233">In Global Catalog</span></span>      | <span data-ttu-id="7500c-234">False</span><span class="sxs-lookup"><span data-stu-id="7500c-234">False</span></span>                                                       |
| <span data-ttu-id="7500c-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7500c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="7500c-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7500c-236">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7500c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7500c-237">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7500c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7500c-238">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7500c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7500c-239">Search-Flags</span></span>           | <span data-ttu-id="7500c-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7500c-240">0x00000000</span></span>                                                  |
| <span data-ttu-id="7500c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7500c-241">System-Flags</span></span>           | <span data-ttu-id="7500c-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7500c-242">0x00000010</span></span>                                                  |
| <span data-ttu-id="7500c-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7500c-243">Classes used in</span></span>        | [<span data-ttu-id="7500c-244">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7500c-244">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7500c-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7500c-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7500c-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7500c-246">Entry</span></span> | <span data-ttu-id="7500c-247">Wert</span><span class="sxs-lookup"><span data-stu-id="7500c-247">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7500c-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7500c-248">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7500c-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7500c-249">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7500c-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="7500c-250">System-Only</span></span>            | <span data-ttu-id="7500c-251">False</span><span class="sxs-lookup"><span data-stu-id="7500c-251">False</span></span>                                                       |
| <span data-ttu-id="7500c-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7500c-252">Is-Single-Valued</span></span>       | <span data-ttu-id="7500c-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="7500c-253">True</span></span>                                                        |
| <span data-ttu-id="7500c-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7500c-254">Is Indexed</span></span>             | <span data-ttu-id="7500c-255">False</span><span class="sxs-lookup"><span data-stu-id="7500c-255">False</span></span>                                                       |
| <span data-ttu-id="7500c-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7500c-256">In Global Catalog</span></span>      | <span data-ttu-id="7500c-257">False</span><span class="sxs-lookup"><span data-stu-id="7500c-257">False</span></span>                                                       |
| <span data-ttu-id="7500c-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7500c-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="7500c-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7500c-259">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7500c-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7500c-260">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7500c-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7500c-261">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7500c-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7500c-262">Search-Flags</span></span>           | <span data-ttu-id="7500c-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7500c-263">0x00000000</span></span>                                                  |
| <span data-ttu-id="7500c-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7500c-264">System-Flags</span></span>           | <span data-ttu-id="7500c-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7500c-265">0x00000010</span></span>                                                  |
| <span data-ttu-id="7500c-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7500c-266">Classes used in</span></span>        | [<span data-ttu-id="7500c-267">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7500c-267">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7500c-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7500c-268">Windows Server 2012</span></span>



| <span data-ttu-id="7500c-269">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7500c-269">Entry</span></span> | <span data-ttu-id="7500c-270">Wert</span><span class="sxs-lookup"><span data-stu-id="7500c-270">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7500c-271">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7500c-271">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7500c-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7500c-272">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7500c-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="7500c-273">System-Only</span></span>            | <span data-ttu-id="7500c-274">False</span><span class="sxs-lookup"><span data-stu-id="7500c-274">False</span></span>                                                       |
| <span data-ttu-id="7500c-275">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7500c-275">Is-Single-Valued</span></span>       | <span data-ttu-id="7500c-276">Richtig</span><span class="sxs-lookup"><span data-stu-id="7500c-276">True</span></span>                                                        |
| <span data-ttu-id="7500c-277">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7500c-277">Is Indexed</span></span>             | <span data-ttu-id="7500c-278">False</span><span class="sxs-lookup"><span data-stu-id="7500c-278">False</span></span>                                                       |
| <span data-ttu-id="7500c-279">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7500c-279">In Global Catalog</span></span>      | <span data-ttu-id="7500c-280">False</span><span class="sxs-lookup"><span data-stu-id="7500c-280">False</span></span>                                                       |
| <span data-ttu-id="7500c-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7500c-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="7500c-282">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7500c-282">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7500c-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7500c-283">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7500c-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7500c-284">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7500c-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7500c-285">Search-Flags</span></span>           | <span data-ttu-id="7500c-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7500c-286">0x00000000</span></span>                                                  |
| <span data-ttu-id="7500c-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7500c-287">System-Flags</span></span>           | <span data-ttu-id="7500c-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7500c-288">0x00000010</span></span>                                                  |
| <span data-ttu-id="7500c-289">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7500c-289">Classes used in</span></span>        | [<span data-ttu-id="7500c-290">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7500c-290">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





