---
title: ms-DS-Allowed-DNS-Suffixes-Attribut
description: Die Liste der zulässigen Suffixe für das dNSHostName-Attribut in Computer Objekten.
ms.assetid: acd57af8-a021-4704-8a56-304126cd3d4b
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-Allowed-DNS-Suffixes-Attribut
- AD-Schema des msDS-attribuweddnssuffixes-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Allowed-DNS-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46c3e4848f96c68041bfdc5f3f1cc9533b52d3e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744745"
---
# <a name="ms-ds-allowed-dns-suffixes-attribute"></a><span data-ttu-id="84f3a-105">ms-DS-Allowed-DNS-Suffixes-Attribut</span><span class="sxs-lookup"><span data-stu-id="84f3a-105">ms-DS-Allowed-DNS-Suffixes attribute</span></span>

<span data-ttu-id="84f3a-106">Die Liste der zulässigen Suffixe für das dNSHostName-Attribut in Computer Objekten.</span><span class="sxs-lookup"><span data-stu-id="84f3a-106">The list of allowed suffixes for the dNSHostName attribute in computer objects.</span></span>



| <span data-ttu-id="84f3a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="84f3a-107">Entry</span></span> | <span data-ttu-id="84f3a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="84f3a-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="84f3a-109">CN</span><span class="sxs-lookup"><span data-stu-id="84f3a-109">CN</span></span>                | <span data-ttu-id="84f3a-110">ms-DS-zulässige DNS-Suffixe</span><span class="sxs-lookup"><span data-stu-id="84f3a-110">ms-DS-Allowed-DNS-Suffixes</span></span>                  |
| <span data-ttu-id="84f3a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="84f3a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="84f3a-112">MSDS-Zuweisung</span><span class="sxs-lookup"><span data-stu-id="84f3a-112">msDS-AllowedDNSSuffixes</span></span>                     |
| <span data-ttu-id="84f3a-113">Size</span><span class="sxs-lookup"><span data-stu-id="84f3a-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="84f3a-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="84f3a-114">Update Privilege</span></span>  | <span data-ttu-id="84f3a-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="84f3a-115">Domain administrator</span></span>                        |
| <span data-ttu-id="84f3a-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="84f3a-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="84f3a-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="84f3a-117">Attribute-Id</span></span>      | <span data-ttu-id="84f3a-118">1.2.840.113556.1.4.1710</span><span class="sxs-lookup"><span data-stu-id="84f3a-118">1.2.840.113556.1.4.1710</span></span>                     |
| <span data-ttu-id="84f3a-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="84f3a-119">System-Id-Guid</span></span>    | <span data-ttu-id="84f3a-120">8469441b-9ac4-4e45-8205-bd219dbf 672D</span><span class="sxs-lookup"><span data-stu-id="84f3a-120">8469441b-9ac4-4e45-8205-bd219dbf672d</span></span>        |
| <span data-ttu-id="84f3a-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="84f3a-121">Syntax</span></span>            | [<span data-ttu-id="84f3a-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="84f3a-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="84f3a-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="84f3a-123">Implementations</span></span>

-   [<span data-ttu-id="84f3a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="84f3a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="84f3a-125">**Adam**</span><span class="sxs-lookup"><span data-stu-id="84f3a-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="84f3a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="84f3a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="84f3a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="84f3a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="84f3a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="84f3a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="84f3a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="84f3a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="84f3a-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="84f3a-130">Windows Server 2003</span></span>



| <span data-ttu-id="84f3a-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="84f3a-131">Entry</span></span> | <span data-ttu-id="84f3a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="84f3a-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="84f3a-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="84f3a-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="84f3a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f3a-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="84f3a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f3a-135">System-Only</span></span>            | <span data-ttu-id="84f3a-136">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-136">False</span></span>                                        |
| <span data-ttu-id="84f3a-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="84f3a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="84f3a-138">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-138">False</span></span>                                        |
| <span data-ttu-id="84f3a-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="84f3a-139">Is Indexed</span></span>             | <span data-ttu-id="84f3a-140">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-140">False</span></span>                                        |
| <span data-ttu-id="84f3a-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="84f3a-141">In Global Catalog</span></span>      | <span data-ttu-id="84f3a-142">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-142">False</span></span>                                        |
| <span data-ttu-id="84f3a-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="84f3a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f3a-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="84f3a-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="84f3a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f3a-145">Range-Lower</span></span>            | <span data-ttu-id="84f3a-146">0</span><span class="sxs-lookup"><span data-stu-id="84f3a-146">0</span></span>                                            |
| <span data-ttu-id="84f3a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f3a-147">Range-Upper</span></span>            | <span data-ttu-id="84f3a-148">2048</span><span class="sxs-lookup"><span data-stu-id="84f3a-148">2048</span></span>                                         |
| <span data-ttu-id="84f3a-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f3a-149">Search-Flags</span></span>           | <span data-ttu-id="84f3a-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f3a-150">0x00000000</span></span>                                   |
| <span data-ttu-id="84f3a-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f3a-151">System-Flags</span></span>           | <span data-ttu-id="84f3a-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f3a-152">0x00000010</span></span>                                   |
| <span data-ttu-id="84f3a-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="84f3a-153">Classes used in</span></span>        | [<span data-ttu-id="84f3a-154">**Domäne: DNS**</span><span class="sxs-lookup"><span data-stu-id="84f3a-154">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="adam"></a><span data-ttu-id="84f3a-155">Adam</span><span class="sxs-lookup"><span data-stu-id="84f3a-155">ADAM</span></span>



| <span data-ttu-id="84f3a-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="84f3a-156">Entry</span></span> | <span data-ttu-id="84f3a-157">Wert</span><span class="sxs-lookup"><span data-stu-id="84f3a-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="84f3a-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="84f3a-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="84f3a-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f3a-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="84f3a-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f3a-160">System-Only</span></span>            | <span data-ttu-id="84f3a-161">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-161">False</span></span>                                        |
| <span data-ttu-id="84f3a-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="84f3a-162">Is-Single-Valued</span></span>       | <span data-ttu-id="84f3a-163">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-163">False</span></span>                                        |
| <span data-ttu-id="84f3a-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="84f3a-164">Is Indexed</span></span>             | <span data-ttu-id="84f3a-165">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-165">False</span></span>                                        |
| <span data-ttu-id="84f3a-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="84f3a-166">In Global Catalog</span></span>      | <span data-ttu-id="84f3a-167">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-167">False</span></span>                                        |
| <span data-ttu-id="84f3a-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="84f3a-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f3a-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="84f3a-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="84f3a-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f3a-170">Range-Lower</span></span>            | <span data-ttu-id="84f3a-171">0</span><span class="sxs-lookup"><span data-stu-id="84f3a-171">0</span></span>                                            |
| <span data-ttu-id="84f3a-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f3a-172">Range-Upper</span></span>            | <span data-ttu-id="84f3a-173">2048</span><span class="sxs-lookup"><span data-stu-id="84f3a-173">2048</span></span>                                         |
| <span data-ttu-id="84f3a-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f3a-174">Search-Flags</span></span>           | <span data-ttu-id="84f3a-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f3a-175">0x00000000</span></span>                                   |
| <span data-ttu-id="84f3a-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f3a-176">System-Flags</span></span>           | <span data-ttu-id="84f3a-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f3a-177">0x00000010</span></span>                                   |
| <span data-ttu-id="84f3a-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="84f3a-178">Classes used in</span></span>        | [<span data-ttu-id="84f3a-179">**Domäne: DNS**</span><span class="sxs-lookup"><span data-stu-id="84f3a-179">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="84f3a-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="84f3a-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="84f3a-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="84f3a-181">Entry</span></span> | <span data-ttu-id="84f3a-182">Wert</span><span class="sxs-lookup"><span data-stu-id="84f3a-182">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="84f3a-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="84f3a-183">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="84f3a-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f3a-184">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="84f3a-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f3a-185">System-Only</span></span>            | <span data-ttu-id="84f3a-186">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-186">False</span></span>                                        |
| <span data-ttu-id="84f3a-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="84f3a-187">Is-Single-Valued</span></span>       | <span data-ttu-id="84f3a-188">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-188">False</span></span>                                        |
| <span data-ttu-id="84f3a-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="84f3a-189">Is Indexed</span></span>             | <span data-ttu-id="84f3a-190">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-190">False</span></span>                                        |
| <span data-ttu-id="84f3a-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="84f3a-191">In Global Catalog</span></span>      | <span data-ttu-id="84f3a-192">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-192">False</span></span>                                        |
| <span data-ttu-id="84f3a-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="84f3a-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f3a-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="84f3a-194">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="84f3a-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f3a-195">Range-Lower</span></span>            | <span data-ttu-id="84f3a-196">0</span><span class="sxs-lookup"><span data-stu-id="84f3a-196">0</span></span>                                            |
| <span data-ttu-id="84f3a-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f3a-197">Range-Upper</span></span>            | <span data-ttu-id="84f3a-198">2048</span><span class="sxs-lookup"><span data-stu-id="84f3a-198">2048</span></span>                                         |
| <span data-ttu-id="84f3a-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f3a-199">Search-Flags</span></span>           | <span data-ttu-id="84f3a-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f3a-200">0x00000000</span></span>                                   |
| <span data-ttu-id="84f3a-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f3a-201">System-Flags</span></span>           | <span data-ttu-id="84f3a-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f3a-202">0x00000010</span></span>                                   |
| <span data-ttu-id="84f3a-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="84f3a-203">Classes used in</span></span>        | [<span data-ttu-id="84f3a-204">**Domäne: DNS**</span><span class="sxs-lookup"><span data-stu-id="84f3a-204">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="84f3a-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84f3a-205">Windows Server 2008</span></span>



| <span data-ttu-id="84f3a-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="84f3a-206">Entry</span></span> | <span data-ttu-id="84f3a-207">Wert</span><span class="sxs-lookup"><span data-stu-id="84f3a-207">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="84f3a-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="84f3a-208">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="84f3a-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f3a-209">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="84f3a-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f3a-210">System-Only</span></span>            | <span data-ttu-id="84f3a-211">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-211">False</span></span>                                        |
| <span data-ttu-id="84f3a-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="84f3a-212">Is-Single-Valued</span></span>       | <span data-ttu-id="84f3a-213">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-213">False</span></span>                                        |
| <span data-ttu-id="84f3a-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="84f3a-214">Is Indexed</span></span>             | <span data-ttu-id="84f3a-215">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-215">False</span></span>                                        |
| <span data-ttu-id="84f3a-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="84f3a-216">In Global Catalog</span></span>      | <span data-ttu-id="84f3a-217">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-217">False</span></span>                                        |
| <span data-ttu-id="84f3a-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="84f3a-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f3a-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="84f3a-219">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="84f3a-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f3a-220">Range-Lower</span></span>            | <span data-ttu-id="84f3a-221">0</span><span class="sxs-lookup"><span data-stu-id="84f3a-221">0</span></span>                                            |
| <span data-ttu-id="84f3a-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f3a-222">Range-Upper</span></span>            | <span data-ttu-id="84f3a-223">2048</span><span class="sxs-lookup"><span data-stu-id="84f3a-223">2048</span></span>                                         |
| <span data-ttu-id="84f3a-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f3a-224">Search-Flags</span></span>           | <span data-ttu-id="84f3a-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f3a-225">0x00000000</span></span>                                   |
| <span data-ttu-id="84f3a-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f3a-226">System-Flags</span></span>           | <span data-ttu-id="84f3a-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f3a-227">0x00000010</span></span>                                   |
| <span data-ttu-id="84f3a-228">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="84f3a-228">Classes used in</span></span>        | [<span data-ttu-id="84f3a-229">**Domäne: DNS**</span><span class="sxs-lookup"><span data-stu-id="84f3a-229">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="84f3a-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="84f3a-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="84f3a-231">Eingabe</span><span class="sxs-lookup"><span data-stu-id="84f3a-231">Entry</span></span> | <span data-ttu-id="84f3a-232">Wert</span><span class="sxs-lookup"><span data-stu-id="84f3a-232">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="84f3a-233">Link-ID</span><span class="sxs-lookup"><span data-stu-id="84f3a-233">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="84f3a-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f3a-234">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="84f3a-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f3a-235">System-Only</span></span>            | <span data-ttu-id="84f3a-236">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-236">False</span></span>                                        |
| <span data-ttu-id="84f3a-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="84f3a-237">Is-Single-Valued</span></span>       | <span data-ttu-id="84f3a-238">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-238">False</span></span>                                        |
| <span data-ttu-id="84f3a-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="84f3a-239">Is Indexed</span></span>             | <span data-ttu-id="84f3a-240">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-240">False</span></span>                                        |
| <span data-ttu-id="84f3a-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="84f3a-241">In Global Catalog</span></span>      | <span data-ttu-id="84f3a-242">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-242">False</span></span>                                        |
| <span data-ttu-id="84f3a-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="84f3a-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f3a-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="84f3a-244">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="84f3a-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f3a-245">Range-Lower</span></span>            | <span data-ttu-id="84f3a-246">0</span><span class="sxs-lookup"><span data-stu-id="84f3a-246">0</span></span>                                            |
| <span data-ttu-id="84f3a-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f3a-247">Range-Upper</span></span>            | <span data-ttu-id="84f3a-248">2048</span><span class="sxs-lookup"><span data-stu-id="84f3a-248">2048</span></span>                                         |
| <span data-ttu-id="84f3a-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f3a-249">Search-Flags</span></span>           | <span data-ttu-id="84f3a-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f3a-250">0x00000000</span></span>                                   |
| <span data-ttu-id="84f3a-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f3a-251">System-Flags</span></span>           | <span data-ttu-id="84f3a-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f3a-252">0x00000010</span></span>                                   |
| <span data-ttu-id="84f3a-253">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="84f3a-253">Classes used in</span></span>        | [<span data-ttu-id="84f3a-254">**Domäne: DNS**</span><span class="sxs-lookup"><span data-stu-id="84f3a-254">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="84f3a-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84f3a-255">Windows Server 2012</span></span>



| <span data-ttu-id="84f3a-256">Eingabe</span><span class="sxs-lookup"><span data-stu-id="84f3a-256">Entry</span></span> | <span data-ttu-id="84f3a-257">Wert</span><span class="sxs-lookup"><span data-stu-id="84f3a-257">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="84f3a-258">Link-ID</span><span class="sxs-lookup"><span data-stu-id="84f3a-258">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="84f3a-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f3a-259">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="84f3a-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f3a-260">System-Only</span></span>            | <span data-ttu-id="84f3a-261">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-261">False</span></span>                                        |
| <span data-ttu-id="84f3a-262">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="84f3a-262">Is-Single-Valued</span></span>       | <span data-ttu-id="84f3a-263">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-263">False</span></span>                                        |
| <span data-ttu-id="84f3a-264">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="84f3a-264">Is Indexed</span></span>             | <span data-ttu-id="84f3a-265">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-265">False</span></span>                                        |
| <span data-ttu-id="84f3a-266">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="84f3a-266">In Global Catalog</span></span>      | <span data-ttu-id="84f3a-267">False</span><span class="sxs-lookup"><span data-stu-id="84f3a-267">False</span></span>                                        |
| <span data-ttu-id="84f3a-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="84f3a-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f3a-269">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="84f3a-269">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="84f3a-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f3a-270">Range-Lower</span></span>            | <span data-ttu-id="84f3a-271">0</span><span class="sxs-lookup"><span data-stu-id="84f3a-271">0</span></span>                                            |
| <span data-ttu-id="84f3a-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f3a-272">Range-Upper</span></span>            | <span data-ttu-id="84f3a-273">2048</span><span class="sxs-lookup"><span data-stu-id="84f3a-273">2048</span></span>                                         |
| <span data-ttu-id="84f3a-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f3a-274">Search-Flags</span></span>           | <span data-ttu-id="84f3a-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f3a-275">0x00000000</span></span>                                   |
| <span data-ttu-id="84f3a-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f3a-276">System-Flags</span></span>           | <span data-ttu-id="84f3a-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f3a-277">0x00000010</span></span>                                   |
| <span data-ttu-id="84f3a-278">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="84f3a-278">Classes used in</span></span>        | [<span data-ttu-id="84f3a-279">**Domäne: DNS**</span><span class="sxs-lookup"><span data-stu-id="84f3a-279">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



 

 





