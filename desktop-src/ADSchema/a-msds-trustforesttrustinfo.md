---
title: ms-DS-Trust-Forest-Trust-Info-Attribut
description: Enthält Gesamtstruktur-Vertrauensstellungs Informationen (ein binäres Blob), die vom System für ein Trusted-Domain Objekt verwendet werden.
ms.assetid: 60944ff6-d2b1-4f53-8557-7d79a7d9df51
ms.tgt_platform: multiple
keywords:
- ms-DS-Trust-Forest-Trust-Info-Attribut AD-Schema
- das msDS-trustforesttrustinfo-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- ms-DS-Trust-Forest-Trust-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e259abaeae4d99b80b8ff6a390901f1c9f51e6a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744680"
---
# <a name="ms-ds-trust-forest-trust-info-attribute"></a><span data-ttu-id="d1c43-105">ms-DS-Trust-Forest-Trust-Info-Attribut</span><span class="sxs-lookup"><span data-stu-id="d1c43-105">ms-DS-Trust-Forest-Trust-Info attribute</span></span>

<span data-ttu-id="d1c43-106">Enthält Gesamtstruktur-Vertrauensstellungs Informationen (ein binäres Blob), die vom System für ein Trusted-Domain Objekt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1c43-106">Contains forest trust information (a binary BLOB) that is used by the system for a Trusted-Domain object.</span></span>



| <span data-ttu-id="d1c43-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d1c43-107">Entry</span></span> | <span data-ttu-id="d1c43-108">Wert</span><span class="sxs-lookup"><span data-stu-id="d1c43-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c43-109">CN</span><span class="sxs-lookup"><span data-stu-id="d1c43-109">CN</span></span>                | <span data-ttu-id="d1c43-110">ms-DS-Trust-Forest-Trust-Info</span><span class="sxs-lookup"><span data-stu-id="d1c43-110">ms-DS-Trust-Forest-Trust-Info</span></span>                                                                                      |
| <span data-ttu-id="d1c43-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d1c43-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d1c43-112">MSDS-trustforesttrustinfo</span><span class="sxs-lookup"><span data-stu-id="d1c43-112">msDS-TrustForestTrustInfo</span></span>                                                                                          |
| <span data-ttu-id="d1c43-113">Size</span><span class="sxs-lookup"><span data-stu-id="d1c43-113">Size</span></span>              | \-                                                                                                                 |
| <span data-ttu-id="d1c43-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d1c43-114">Update Privilege</span></span>  | \-                                                                                                                 |
| <span data-ttu-id="d1c43-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="d1c43-115">Update Frequency</span></span>  | <span data-ttu-id="d1c43-116">Nur, wenn die Vertrauensstellung zwischen Gesamtstrukturen geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d1c43-116">Only when trust relationship between forests changes.</span></span> <span data-ttu-id="d1c43-117">Dies kann vorkommen, wenn die Topologie einer vertrauenswürdigen Gesamtstruktur geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d1c43-117">This can happen if the topology of a trusted forest changes.</span></span> |
| <span data-ttu-id="d1c43-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d1c43-118">Attribute-Id</span></span>      | <span data-ttu-id="d1c43-119">1.2.840.113556.1.4.1702</span><span class="sxs-lookup"><span data-stu-id="d1c43-119">1.2.840.113556.1.4.1702</span></span>                                                                                            |
| <span data-ttu-id="d1c43-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d1c43-120">System-Id-Guid</span></span>    | <span data-ttu-id="d1c43-121">29cc866e-49d3-4969-942e-1dbc0925d183</span><span class="sxs-lookup"><span data-stu-id="d1c43-121">29cc866e-49d3-4969-942e-1dbc0925d183</span></span>                                                                               |
| <span data-ttu-id="d1c43-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1c43-122">Syntax</span></span>            | [<span data-ttu-id="d1c43-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="d1c43-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="d1c43-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="d1c43-124">Implementations</span></span>

-   [<span data-ttu-id="d1c43-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d1c43-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d1c43-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d1c43-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d1c43-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d1c43-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d1c43-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d1c43-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d1c43-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d1c43-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d1c43-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d1c43-130">Windows Server 2003</span></span>



| <span data-ttu-id="d1c43-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d1c43-131">Entry</span></span> | <span data-ttu-id="d1c43-132">Wert</span><span class="sxs-lookup"><span data-stu-id="d1c43-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d1c43-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d1c43-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d1c43-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1c43-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d1c43-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1c43-135">System-Only</span></span>            | <span data-ttu-id="d1c43-136">False</span><span class="sxs-lookup"><span data-stu-id="d1c43-136">False</span></span>                                                |
| <span data-ttu-id="d1c43-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d1c43-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d1c43-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="d1c43-138">True</span></span>                                                 |
| <span data-ttu-id="d1c43-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d1c43-139">Is Indexed</span></span>             | <span data-ttu-id="d1c43-140">False</span><span class="sxs-lookup"><span data-stu-id="d1c43-140">False</span></span>                                                |
| <span data-ttu-id="d1c43-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d1c43-141">In Global Catalog</span></span>      | <span data-ttu-id="d1c43-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="d1c43-142">True</span></span>                                                 |
| <span data-ttu-id="d1c43-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d1c43-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1c43-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d1c43-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d1c43-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1c43-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d1c43-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1c43-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d1c43-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1c43-147">Search-Flags</span></span>           | <span data-ttu-id="d1c43-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1c43-148">0x00000000</span></span>                                           |
| <span data-ttu-id="d1c43-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1c43-149">System-Flags</span></span>           | <span data-ttu-id="d1c43-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1c43-150">0x00000010</span></span>                                           |
| <span data-ttu-id="d1c43-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d1c43-151">Classes used in</span></span>        | [<span data-ttu-id="d1c43-152">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="d1c43-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d1c43-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d1c43-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d1c43-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d1c43-154">Entry</span></span> | <span data-ttu-id="d1c43-155">Wert</span><span class="sxs-lookup"><span data-stu-id="d1c43-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d1c43-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d1c43-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d1c43-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1c43-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d1c43-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1c43-158">System-Only</span></span>            | <span data-ttu-id="d1c43-159">False</span><span class="sxs-lookup"><span data-stu-id="d1c43-159">False</span></span>                                                |
| <span data-ttu-id="d1c43-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d1c43-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d1c43-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="d1c43-161">True</span></span>                                                 |
| <span data-ttu-id="d1c43-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d1c43-162">Is Indexed</span></span>             | <span data-ttu-id="d1c43-163">False</span><span class="sxs-lookup"><span data-stu-id="d1c43-163">False</span></span>                                                |
| <span data-ttu-id="d1c43-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d1c43-164">In Global Catalog</span></span>      | <span data-ttu-id="d1c43-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="d1c43-165">True</span></span>                                                 |
| <span data-ttu-id="d1c43-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d1c43-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1c43-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d1c43-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d1c43-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1c43-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d1c43-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1c43-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d1c43-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1c43-170">Search-Flags</span></span>           | <span data-ttu-id="d1c43-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1c43-171">0x00000000</span></span>                                           |
| <span data-ttu-id="d1c43-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1c43-172">System-Flags</span></span>           | <span data-ttu-id="d1c43-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1c43-173">0x00000010</span></span>                                           |
| <span data-ttu-id="d1c43-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d1c43-174">Classes used in</span></span>        | [<span data-ttu-id="d1c43-175">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="d1c43-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d1c43-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1c43-176">Windows Server 2008</span></span>



| <span data-ttu-id="d1c43-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d1c43-177">Entry</span></span> | <span data-ttu-id="d1c43-178">Wert</span><span class="sxs-lookup"><span data-stu-id="d1c43-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d1c43-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d1c43-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d1c43-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1c43-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d1c43-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1c43-181">System-Only</span></span>            | <span data-ttu-id="d1c43-182">False</span><span class="sxs-lookup"><span data-stu-id="d1c43-182">False</span></span>                                                |
| <span data-ttu-id="d1c43-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d1c43-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d1c43-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="d1c43-184">True</span></span>                                                 |
| <span data-ttu-id="d1c43-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d1c43-185">Is Indexed</span></span>             | <span data-ttu-id="d1c43-186">False</span><span class="sxs-lookup"><span data-stu-id="d1c43-186">False</span></span>                                                |
| <span data-ttu-id="d1c43-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d1c43-187">In Global Catalog</span></span>      | <span data-ttu-id="d1c43-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="d1c43-188">True</span></span>                                                 |
| <span data-ttu-id="d1c43-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d1c43-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1c43-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d1c43-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d1c43-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1c43-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d1c43-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1c43-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d1c43-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1c43-193">Search-Flags</span></span>           | <span data-ttu-id="d1c43-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1c43-194">0x00000000</span></span>                                           |
| <span data-ttu-id="d1c43-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1c43-195">System-Flags</span></span>           | <span data-ttu-id="d1c43-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1c43-196">0x00000010</span></span>                                           |
| <span data-ttu-id="d1c43-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d1c43-197">Classes used in</span></span>        | [<span data-ttu-id="d1c43-198">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="d1c43-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d1c43-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d1c43-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d1c43-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d1c43-200">Entry</span></span> | <span data-ttu-id="d1c43-201">Wert</span><span class="sxs-lookup"><span data-stu-id="d1c43-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d1c43-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d1c43-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d1c43-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1c43-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d1c43-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1c43-204">System-Only</span></span>            | <span data-ttu-id="d1c43-205">False</span><span class="sxs-lookup"><span data-stu-id="d1c43-205">False</span></span>                                                |
| <span data-ttu-id="d1c43-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d1c43-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d1c43-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="d1c43-207">True</span></span>                                                 |
| <span data-ttu-id="d1c43-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d1c43-208">Is Indexed</span></span>             | <span data-ttu-id="d1c43-209">False</span><span class="sxs-lookup"><span data-stu-id="d1c43-209">False</span></span>                                                |
| <span data-ttu-id="d1c43-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d1c43-210">In Global Catalog</span></span>      | <span data-ttu-id="d1c43-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="d1c43-211">True</span></span>                                                 |
| <span data-ttu-id="d1c43-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d1c43-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1c43-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d1c43-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d1c43-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1c43-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d1c43-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1c43-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d1c43-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1c43-216">Search-Flags</span></span>           | <span data-ttu-id="d1c43-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1c43-217">0x00000000</span></span>                                           |
| <span data-ttu-id="d1c43-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1c43-218">System-Flags</span></span>           | <span data-ttu-id="d1c43-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1c43-219">0x00000010</span></span>                                           |
| <span data-ttu-id="d1c43-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d1c43-220">Classes used in</span></span>        | [<span data-ttu-id="d1c43-221">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="d1c43-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d1c43-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d1c43-222">Windows Server 2012</span></span>



| <span data-ttu-id="d1c43-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d1c43-223">Entry</span></span> | <span data-ttu-id="d1c43-224">Wert</span><span class="sxs-lookup"><span data-stu-id="d1c43-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d1c43-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d1c43-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d1c43-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1c43-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d1c43-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1c43-227">System-Only</span></span>            | <span data-ttu-id="d1c43-228">False</span><span class="sxs-lookup"><span data-stu-id="d1c43-228">False</span></span>                                                |
| <span data-ttu-id="d1c43-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d1c43-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d1c43-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="d1c43-230">True</span></span>                                                 |
| <span data-ttu-id="d1c43-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d1c43-231">Is Indexed</span></span>             | <span data-ttu-id="d1c43-232">False</span><span class="sxs-lookup"><span data-stu-id="d1c43-232">False</span></span>                                                |
| <span data-ttu-id="d1c43-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d1c43-233">In Global Catalog</span></span>      | <span data-ttu-id="d1c43-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="d1c43-234">True</span></span>                                                 |
| <span data-ttu-id="d1c43-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d1c43-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1c43-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d1c43-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d1c43-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1c43-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d1c43-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1c43-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d1c43-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1c43-239">Search-Flags</span></span>           | <span data-ttu-id="d1c43-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1c43-240">0x00000000</span></span>                                           |
| <span data-ttu-id="d1c43-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1c43-241">System-Flags</span></span>           | <span data-ttu-id="d1c43-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1c43-242">0x00000010</span></span>                                           |
| <span data-ttu-id="d1c43-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d1c43-243">Classes used in</span></span>        | [<span data-ttu-id="d1c43-244">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="d1c43-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





