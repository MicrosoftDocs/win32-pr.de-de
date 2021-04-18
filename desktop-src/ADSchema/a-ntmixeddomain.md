---
title: NT-Mixed-Domain-Attribut
description: Gibt an, dass sich die Domäne im einheitlichen Modus oder gemischten Modus befindet. Dieses Attribut befindet sich im domainDNS (Head)-Objekt für die Domäne.
ms.assetid: 49872cbc-844f-4d60-89b6-0150b9116740
ms.tgt_platform: multiple
keywords:
- Active Directory-Domänen Attribut (AD-Schema)
- AD-Schema des nTMixedDomain-Attributs
topic_type:
- apiref
api_name:
- NT-Mixed-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d73291f392141b80ca8916b86fffa0055226c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106341066"
---
# <a name="nt-mixed-domain-attribute"></a><span data-ttu-id="4f6b0-106">NT-Mixed-Domain-Attribut</span><span class="sxs-lookup"><span data-stu-id="4f6b0-106">NT-Mixed-Domain attribute</span></span>

<span data-ttu-id="4f6b0-107">Gibt an, dass sich die Domäne im einheitlichen Modus oder gemischten Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="4f6b0-107">Indicates that the domain is in native mode or mixed mode.</span></span> <span data-ttu-id="4f6b0-108">Dieses Attribut befindet sich im domainDNS (Head)-Objekt für die Domäne.</span><span class="sxs-lookup"><span data-stu-id="4f6b0-108">This attribute is found in the domainDNS (head) object for the domain.</span></span>



| <span data-ttu-id="4f6b0-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4f6b0-109">Entry</span></span> | <span data-ttu-id="4f6b0-110">Wert</span><span class="sxs-lookup"><span data-stu-id="4f6b0-110">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="4f6b0-111">CN</span><span class="sxs-lookup"><span data-stu-id="4f6b0-111">CN</span></span>                | <span data-ttu-id="4f6b0-112">NT-gemischte Domäne</span><span class="sxs-lookup"><span data-stu-id="4f6b0-112">NT-Mixed-Domain</span></span>                       |
| <span data-ttu-id="4f6b0-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4f6b0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4f6b0-114">ntMixedDomain</span><span class="sxs-lookup"><span data-stu-id="4f6b0-114">nTMixedDomain</span></span>                         |
| <span data-ttu-id="4f6b0-115">Size</span><span class="sxs-lookup"><span data-stu-id="4f6b0-115">Size</span></span>              | <span data-ttu-id="4f6b0-116">4 Bytes.</span><span class="sxs-lookup"><span data-stu-id="4f6b0-116">4 bytes.</span></span> <span data-ttu-id="4f6b0-117">Gemischter Modus 1, einheitlicher Modus 0.</span><span class="sxs-lookup"><span data-stu-id="4f6b0-117">Mixed mode 1, native mode 0.</span></span> |
| <span data-ttu-id="4f6b0-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="4f6b0-118">Update Privilege</span></span>  | \-                                    |
| <span data-ttu-id="4f6b0-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="4f6b0-119">Update Frequency</span></span>  | \-                                    |
| <span data-ttu-id="4f6b0-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4f6b0-120">Attribute-Id</span></span>      | <span data-ttu-id="4f6b0-121">1.2.840.113556.1.4.357</span><span class="sxs-lookup"><span data-stu-id="4f6b0-121">1.2.840.113556.1.4.357</span></span>                |
| <span data-ttu-id="4f6b0-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4f6b0-122">System-Id-Guid</span></span>    | <span data-ttu-id="4f6b0-123">3e97891f -8c01-11D0-AFDA-00c04f 930c9</span><span class="sxs-lookup"><span data-stu-id="4f6b0-123">3e97891f-8c01-11d0-afda-00c04fd930c9</span></span>  |
| <span data-ttu-id="4f6b0-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f6b0-124">Syntax</span></span>            | [<span data-ttu-id="4f6b0-125">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-125">**Enumeration**</span></span>](s-enumeration.md)  |



## <a name="implementations"></a><span data-ttu-id="4f6b0-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="4f6b0-126">Implementations</span></span>

-   [<span data-ttu-id="4f6b0-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4f6b0-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4f6b0-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4f6b0-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4f6b0-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4f6b0-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4f6b0-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4f6b0-133">Windows 2000 Server</span></span>



| <span data-ttu-id="4f6b0-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4f6b0-134">Entry</span></span> | <span data-ttu-id="4f6b0-135">Wert</span><span class="sxs-lookup"><span data-stu-id="4f6b0-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4f6b0-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4f6b0-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4f6b0-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f6b0-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4f6b0-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f6b0-138">System-Only</span></span>            | <span data-ttu-id="4f6b0-139">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-139">False</span></span>                                        |
| <span data-ttu-id="4f6b0-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4f6b0-140">Is-Single-Valued</span></span>       | <span data-ttu-id="4f6b0-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="4f6b0-141">True</span></span>                                         |
| <span data-ttu-id="4f6b0-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4f6b0-142">Is Indexed</span></span>             | <span data-ttu-id="4f6b0-143">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-143">False</span></span>                                        |
| <span data-ttu-id="4f6b0-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4f6b0-144">In Global Catalog</span></span>      | <span data-ttu-id="4f6b0-145">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-145">False</span></span>                                        |
| <span data-ttu-id="4f6b0-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f6b0-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f6b0-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4f6b0-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4f6b0-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f6b0-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4f6b0-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f6b0-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4f6b0-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f6b0-150">Search-Flags</span></span>           | <span data-ttu-id="4f6b0-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f6b0-151">0x00000000</span></span>                                   |
| <span data-ttu-id="4f6b0-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f6b0-152">System-Flags</span></span>           | <span data-ttu-id="4f6b0-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f6b0-153">0x00000010</span></span>                                   |
| <span data-ttu-id="4f6b0-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4f6b0-154">Classes used in</span></span>        | [<span data-ttu-id="4f6b0-155">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-155">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4f6b0-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4f6b0-156">Windows Server 2003</span></span>



| <span data-ttu-id="4f6b0-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4f6b0-157">Entry</span></span> | <span data-ttu-id="4f6b0-158">Wert</span><span class="sxs-lookup"><span data-stu-id="4f6b0-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f6b0-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4f6b0-159">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="4f6b0-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f6b0-160">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="4f6b0-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f6b0-161">System-Only</span></span>            | <span data-ttu-id="4f6b0-162">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-162">False</span></span>                                                                                   |
| <span data-ttu-id="4f6b0-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4f6b0-163">Is-Single-Valued</span></span>       | <span data-ttu-id="4f6b0-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="4f6b0-164">True</span></span>                                                                                    |
| <span data-ttu-id="4f6b0-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4f6b0-165">Is Indexed</span></span>             | <span data-ttu-id="4f6b0-166">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-166">False</span></span>                                                                                   |
| <span data-ttu-id="4f6b0-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4f6b0-167">In Global Catalog</span></span>      | <span data-ttu-id="4f6b0-168">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-168">False</span></span>                                                                                   |
| <span data-ttu-id="4f6b0-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f6b0-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f6b0-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4f6b0-170">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="4f6b0-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f6b0-171">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="4f6b0-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f6b0-172">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="4f6b0-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f6b0-173">Search-Flags</span></span>           | <span data-ttu-id="4f6b0-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f6b0-174">0x00000000</span></span>                                                                              |
| <span data-ttu-id="4f6b0-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f6b0-175">System-Flags</span></span>           | <span data-ttu-id="4f6b0-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f6b0-176">0x00000010</span></span>                                                                              |
| <span data-ttu-id="4f6b0-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4f6b0-177">Classes used in</span></span>        | [<span data-ttu-id="4f6b0-178">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-178">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="4f6b0-179">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-179">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4f6b0-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4f6b0-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4f6b0-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4f6b0-181">Entry</span></span> | <span data-ttu-id="4f6b0-182">Wert</span><span class="sxs-lookup"><span data-stu-id="4f6b0-182">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f6b0-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4f6b0-183">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="4f6b0-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f6b0-184">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="4f6b0-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f6b0-185">System-Only</span></span>            | <span data-ttu-id="4f6b0-186">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-186">False</span></span>                                                                                   |
| <span data-ttu-id="4f6b0-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4f6b0-187">Is-Single-Valued</span></span>       | <span data-ttu-id="4f6b0-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="4f6b0-188">True</span></span>                                                                                    |
| <span data-ttu-id="4f6b0-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4f6b0-189">Is Indexed</span></span>             | <span data-ttu-id="4f6b0-190">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-190">False</span></span>                                                                                   |
| <span data-ttu-id="4f6b0-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4f6b0-191">In Global Catalog</span></span>      | <span data-ttu-id="4f6b0-192">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-192">False</span></span>                                                                                   |
| <span data-ttu-id="4f6b0-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f6b0-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f6b0-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4f6b0-194">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="4f6b0-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f6b0-195">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="4f6b0-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f6b0-196">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="4f6b0-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f6b0-197">Search-Flags</span></span>           | <span data-ttu-id="4f6b0-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f6b0-198">0x00000000</span></span>                                                                              |
| <span data-ttu-id="4f6b0-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f6b0-199">System-Flags</span></span>           | <span data-ttu-id="4f6b0-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f6b0-200">0x00000010</span></span>                                                                              |
| <span data-ttu-id="4f6b0-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4f6b0-201">Classes used in</span></span>        | [<span data-ttu-id="4f6b0-202">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-202">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="4f6b0-203">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4f6b0-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f6b0-204">Windows Server 2008</span></span>



| <span data-ttu-id="4f6b0-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4f6b0-205">Entry</span></span> | <span data-ttu-id="4f6b0-206">Wert</span><span class="sxs-lookup"><span data-stu-id="4f6b0-206">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f6b0-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4f6b0-207">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="4f6b0-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f6b0-208">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="4f6b0-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f6b0-209">System-Only</span></span>            | <span data-ttu-id="4f6b0-210">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-210">False</span></span>                                                                                   |
| <span data-ttu-id="4f6b0-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4f6b0-211">Is-Single-Valued</span></span>       | <span data-ttu-id="4f6b0-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="4f6b0-212">True</span></span>                                                                                    |
| <span data-ttu-id="4f6b0-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4f6b0-213">Is Indexed</span></span>             | <span data-ttu-id="4f6b0-214">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-214">False</span></span>                                                                                   |
| <span data-ttu-id="4f6b0-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4f6b0-215">In Global Catalog</span></span>      | <span data-ttu-id="4f6b0-216">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-216">False</span></span>                                                                                   |
| <span data-ttu-id="4f6b0-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f6b0-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f6b0-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4f6b0-218">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="4f6b0-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f6b0-219">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="4f6b0-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f6b0-220">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="4f6b0-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f6b0-221">Search-Flags</span></span>           | <span data-ttu-id="4f6b0-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f6b0-222">0x00000000</span></span>                                                                              |
| <span data-ttu-id="4f6b0-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f6b0-223">System-Flags</span></span>           | <span data-ttu-id="4f6b0-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f6b0-224">0x00000010</span></span>                                                                              |
| <span data-ttu-id="4f6b0-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4f6b0-225">Classes used in</span></span>        | [<span data-ttu-id="4f6b0-226">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-226">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="4f6b0-227">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-227">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4f6b0-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4f6b0-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4f6b0-229">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4f6b0-229">Entry</span></span> | <span data-ttu-id="4f6b0-230">Wert</span><span class="sxs-lookup"><span data-stu-id="4f6b0-230">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f6b0-231">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4f6b0-231">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="4f6b0-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f6b0-232">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="4f6b0-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f6b0-233">System-Only</span></span>            | <span data-ttu-id="4f6b0-234">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-234">False</span></span>                                                                                   |
| <span data-ttu-id="4f6b0-235">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4f6b0-235">Is-Single-Valued</span></span>       | <span data-ttu-id="4f6b0-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="4f6b0-236">True</span></span>                                                                                    |
| <span data-ttu-id="4f6b0-237">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4f6b0-237">Is Indexed</span></span>             | <span data-ttu-id="4f6b0-238">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-238">False</span></span>                                                                                   |
| <span data-ttu-id="4f6b0-239">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4f6b0-239">In Global Catalog</span></span>      | <span data-ttu-id="4f6b0-240">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-240">False</span></span>                                                                                   |
| <span data-ttu-id="4f6b0-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f6b0-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f6b0-242">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4f6b0-242">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="4f6b0-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f6b0-243">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="4f6b0-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f6b0-244">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="4f6b0-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f6b0-245">Search-Flags</span></span>           | <span data-ttu-id="4f6b0-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f6b0-246">0x00000000</span></span>                                                                              |
| <span data-ttu-id="4f6b0-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f6b0-247">System-Flags</span></span>           | <span data-ttu-id="4f6b0-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f6b0-248">0x00000010</span></span>                                                                              |
| <span data-ttu-id="4f6b0-249">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4f6b0-249">Classes used in</span></span>        | [<span data-ttu-id="4f6b0-250">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-250">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="4f6b0-251">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-251">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4f6b0-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4f6b0-252">Windows Server 2012</span></span>



| <span data-ttu-id="4f6b0-253">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4f6b0-253">Entry</span></span> | <span data-ttu-id="4f6b0-254">Wert</span><span class="sxs-lookup"><span data-stu-id="4f6b0-254">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f6b0-255">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4f6b0-255">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="4f6b0-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f6b0-256">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="4f6b0-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f6b0-257">System-Only</span></span>            | <span data-ttu-id="4f6b0-258">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-258">False</span></span>                                                                                   |
| <span data-ttu-id="4f6b0-259">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4f6b0-259">Is-Single-Valued</span></span>       | <span data-ttu-id="4f6b0-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="4f6b0-260">True</span></span>                                                                                    |
| <span data-ttu-id="4f6b0-261">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4f6b0-261">Is Indexed</span></span>             | <span data-ttu-id="4f6b0-262">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-262">False</span></span>                                                                                   |
| <span data-ttu-id="4f6b0-263">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4f6b0-263">In Global Catalog</span></span>      | <span data-ttu-id="4f6b0-264">False</span><span class="sxs-lookup"><span data-stu-id="4f6b0-264">False</span></span>                                                                                   |
| <span data-ttu-id="4f6b0-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f6b0-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f6b0-266">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4f6b0-266">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="4f6b0-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f6b0-267">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="4f6b0-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f6b0-268">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="4f6b0-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f6b0-269">Search-Flags</span></span>           | <span data-ttu-id="4f6b0-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f6b0-270">0x00000000</span></span>                                                                              |
| <span data-ttu-id="4f6b0-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f6b0-271">System-Flags</span></span>           | <span data-ttu-id="4f6b0-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f6b0-272">0x00000010</span></span>                                                                              |
| <span data-ttu-id="4f6b0-273">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4f6b0-273">Classes used in</span></span>        | [<span data-ttu-id="4f6b0-274">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-274">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="4f6b0-275">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="4f6b0-275">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





