---
title: Domain-Certificate-Autoritäten-Attribut
description: Liste der Zertifizierungsstellen für eine bestimmte Domäne.
ms.assetid: d773bf84-c318-4616-8e16-c14457707722
ms.tgt_platform: multiple
keywords:
- Domain-Certificate-Autoritäten-Attribut AD-Schema
- domaincas-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Domain-Certificate-Authorities
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abf68db97be2121bf1efaa0c0854736bd31e6127
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957666"
---
# <a name="domain-certificate-authorities-attribute"></a><span data-ttu-id="f3eab-105">Domain-Certificate-Autoritäten-Attribut</span><span class="sxs-lookup"><span data-stu-id="f3eab-105">Domain-Certificate-Authorities attribute</span></span>

<span data-ttu-id="f3eab-106">Liste der Zertifizierungsstellen für eine bestimmte Domäne.</span><span class="sxs-lookup"><span data-stu-id="f3eab-106">List of certification authorities for a given domain.</span></span>



| <span data-ttu-id="f3eab-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f3eab-107">Entry</span></span> | <span data-ttu-id="f3eab-108">Wert</span><span class="sxs-lookup"><span data-stu-id="f3eab-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="f3eab-109">CN</span><span class="sxs-lookup"><span data-stu-id="f3eab-109">CN</span></span>                | <span data-ttu-id="f3eab-110">Domänen Zertifizierungsstellen</span><span class="sxs-lookup"><span data-stu-id="f3eab-110">Domain-Certificate-Authorities</span></span>          |
| <span data-ttu-id="f3eab-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f3eab-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f3eab-112">Domänen CAS</span><span class="sxs-lookup"><span data-stu-id="f3eab-112">domainCAs</span></span>                               |
| <span data-ttu-id="f3eab-113">Size</span><span class="sxs-lookup"><span data-stu-id="f3eab-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="f3eab-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f3eab-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="f3eab-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f3eab-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="f3eab-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f3eab-116">Attribute-Id</span></span>      | <span data-ttu-id="f3eab-117">1.2.840.113556.1.4.668</span><span class="sxs-lookup"><span data-stu-id="f3eab-117">1.2.840.113556.1.4.668</span></span>                  |
| <span data-ttu-id="f3eab-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f3eab-118">System-Id-Guid</span></span>    | <span data-ttu-id="f3eab-119">7bf dcb7a-4807-11d1-a9c3-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="f3eab-119">7bfdcb7a-4807-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="f3eab-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3eab-120">Syntax</span></span>            | [<span data-ttu-id="f3eab-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f3eab-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="f3eab-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f3eab-122">Implementations</span></span>

-   [<span data-ttu-id="f3eab-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f3eab-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f3eab-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f3eab-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f3eab-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f3eab-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f3eab-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f3eab-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f3eab-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f3eab-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f3eab-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f3eab-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f3eab-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f3eab-129">Windows 2000 Server</span></span>



| <span data-ttu-id="f3eab-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f3eab-130">Entry</span></span> | <span data-ttu-id="f3eab-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f3eab-131">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="f3eab-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f3eab-132">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="f3eab-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3eab-133">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="f3eab-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3eab-134">System-Only</span></span>            | <span data-ttu-id="f3eab-135">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-135">False</span></span>                                              |
| <span data-ttu-id="f3eab-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f3eab-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f3eab-137">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-137">False</span></span>                                              |
| <span data-ttu-id="f3eab-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f3eab-138">Is Indexed</span></span>             | <span data-ttu-id="f3eab-139">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-139">False</span></span>                                              |
| <span data-ttu-id="f3eab-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f3eab-140">In Global Catalog</span></span>      | <span data-ttu-id="f3eab-141">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-141">False</span></span>                                              |
| <span data-ttu-id="f3eab-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3eab-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3eab-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f3eab-143">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="f3eab-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3eab-144">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="f3eab-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3eab-145">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="f3eab-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3eab-146">Search-Flags</span></span>           | <span data-ttu-id="f3eab-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3eab-147">0x00000000</span></span>                                         |
| <span data-ttu-id="f3eab-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3eab-148">System-Flags</span></span>           | <span data-ttu-id="f3eab-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3eab-149">0x00000010</span></span>                                         |
| <span data-ttu-id="f3eab-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f3eab-150">Classes used in</span></span>        | [<span data-ttu-id="f3eab-151">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="f3eab-151">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f3eab-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f3eab-152">Windows Server 2003</span></span>



| <span data-ttu-id="f3eab-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f3eab-153">Entry</span></span> | <span data-ttu-id="f3eab-154">Wert</span><span class="sxs-lookup"><span data-stu-id="f3eab-154">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="f3eab-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f3eab-155">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="f3eab-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3eab-156">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="f3eab-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3eab-157">System-Only</span></span>            | <span data-ttu-id="f3eab-158">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-158">False</span></span>                                              |
| <span data-ttu-id="f3eab-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f3eab-159">Is-Single-Valued</span></span>       | <span data-ttu-id="f3eab-160">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-160">False</span></span>                                              |
| <span data-ttu-id="f3eab-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f3eab-161">Is Indexed</span></span>             | <span data-ttu-id="f3eab-162">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-162">False</span></span>                                              |
| <span data-ttu-id="f3eab-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f3eab-163">In Global Catalog</span></span>      | <span data-ttu-id="f3eab-164">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-164">False</span></span>                                              |
| <span data-ttu-id="f3eab-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3eab-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3eab-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f3eab-166">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="f3eab-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3eab-167">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="f3eab-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3eab-168">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="f3eab-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3eab-169">Search-Flags</span></span>           | <span data-ttu-id="f3eab-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3eab-170">0x00000000</span></span>                                         |
| <span data-ttu-id="f3eab-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3eab-171">System-Flags</span></span>           | <span data-ttu-id="f3eab-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3eab-172">0x00000010</span></span>                                         |
| <span data-ttu-id="f3eab-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f3eab-173">Classes used in</span></span>        | [<span data-ttu-id="f3eab-174">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="f3eab-174">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f3eab-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f3eab-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f3eab-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f3eab-176">Entry</span></span> | <span data-ttu-id="f3eab-177">Wert</span><span class="sxs-lookup"><span data-stu-id="f3eab-177">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="f3eab-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f3eab-178">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="f3eab-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3eab-179">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="f3eab-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3eab-180">System-Only</span></span>            | <span data-ttu-id="f3eab-181">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-181">False</span></span>                                              |
| <span data-ttu-id="f3eab-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f3eab-182">Is-Single-Valued</span></span>       | <span data-ttu-id="f3eab-183">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-183">False</span></span>                                              |
| <span data-ttu-id="f3eab-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f3eab-184">Is Indexed</span></span>             | <span data-ttu-id="f3eab-185">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-185">False</span></span>                                              |
| <span data-ttu-id="f3eab-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f3eab-186">In Global Catalog</span></span>      | <span data-ttu-id="f3eab-187">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-187">False</span></span>                                              |
| <span data-ttu-id="f3eab-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3eab-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3eab-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f3eab-189">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="f3eab-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3eab-190">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="f3eab-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3eab-191">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="f3eab-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3eab-192">Search-Flags</span></span>           | <span data-ttu-id="f3eab-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3eab-193">0x00000000</span></span>                                         |
| <span data-ttu-id="f3eab-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3eab-194">System-Flags</span></span>           | <span data-ttu-id="f3eab-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3eab-195">0x00000010</span></span>                                         |
| <span data-ttu-id="f3eab-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f3eab-196">Classes used in</span></span>        | [<span data-ttu-id="f3eab-197">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="f3eab-197">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f3eab-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3eab-198">Windows Server 2008</span></span>



| <span data-ttu-id="f3eab-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f3eab-199">Entry</span></span> | <span data-ttu-id="f3eab-200">Wert</span><span class="sxs-lookup"><span data-stu-id="f3eab-200">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="f3eab-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f3eab-201">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="f3eab-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3eab-202">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="f3eab-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3eab-203">System-Only</span></span>            | <span data-ttu-id="f3eab-204">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-204">False</span></span>                                              |
| <span data-ttu-id="f3eab-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f3eab-205">Is-Single-Valued</span></span>       | <span data-ttu-id="f3eab-206">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-206">False</span></span>                                              |
| <span data-ttu-id="f3eab-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f3eab-207">Is Indexed</span></span>             | <span data-ttu-id="f3eab-208">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-208">False</span></span>                                              |
| <span data-ttu-id="f3eab-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f3eab-209">In Global Catalog</span></span>      | <span data-ttu-id="f3eab-210">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-210">False</span></span>                                              |
| <span data-ttu-id="f3eab-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3eab-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3eab-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f3eab-212">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="f3eab-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3eab-213">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="f3eab-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3eab-214">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="f3eab-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3eab-215">Search-Flags</span></span>           | <span data-ttu-id="f3eab-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3eab-216">0x00000000</span></span>                                         |
| <span data-ttu-id="f3eab-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3eab-217">System-Flags</span></span>           | <span data-ttu-id="f3eab-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3eab-218">0x00000010</span></span>                                         |
| <span data-ttu-id="f3eab-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f3eab-219">Classes used in</span></span>        | [<span data-ttu-id="f3eab-220">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="f3eab-220">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f3eab-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f3eab-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f3eab-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f3eab-222">Entry</span></span> | <span data-ttu-id="f3eab-223">Wert</span><span class="sxs-lookup"><span data-stu-id="f3eab-223">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="f3eab-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f3eab-224">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="f3eab-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3eab-225">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="f3eab-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3eab-226">System-Only</span></span>            | <span data-ttu-id="f3eab-227">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-227">False</span></span>                                              |
| <span data-ttu-id="f3eab-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f3eab-228">Is-Single-Valued</span></span>       | <span data-ttu-id="f3eab-229">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-229">False</span></span>                                              |
| <span data-ttu-id="f3eab-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f3eab-230">Is Indexed</span></span>             | <span data-ttu-id="f3eab-231">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-231">False</span></span>                                              |
| <span data-ttu-id="f3eab-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f3eab-232">In Global Catalog</span></span>      | <span data-ttu-id="f3eab-233">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-233">False</span></span>                                              |
| <span data-ttu-id="f3eab-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3eab-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3eab-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f3eab-235">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="f3eab-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3eab-236">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="f3eab-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3eab-237">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="f3eab-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3eab-238">Search-Flags</span></span>           | <span data-ttu-id="f3eab-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3eab-239">0x00000000</span></span>                                         |
| <span data-ttu-id="f3eab-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3eab-240">System-Flags</span></span>           | <span data-ttu-id="f3eab-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3eab-241">0x00000010</span></span>                                         |
| <span data-ttu-id="f3eab-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f3eab-242">Classes used in</span></span>        | [<span data-ttu-id="f3eab-243">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="f3eab-243">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f3eab-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f3eab-244">Windows Server 2012</span></span>



| <span data-ttu-id="f3eab-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f3eab-245">Entry</span></span> | <span data-ttu-id="f3eab-246">Wert</span><span class="sxs-lookup"><span data-stu-id="f3eab-246">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="f3eab-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f3eab-247">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="f3eab-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3eab-248">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="f3eab-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3eab-249">System-Only</span></span>            | <span data-ttu-id="f3eab-250">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-250">False</span></span>                                              |
| <span data-ttu-id="f3eab-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f3eab-251">Is-Single-Valued</span></span>       | <span data-ttu-id="f3eab-252">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-252">False</span></span>                                              |
| <span data-ttu-id="f3eab-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f3eab-253">Is Indexed</span></span>             | <span data-ttu-id="f3eab-254">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-254">False</span></span>                                              |
| <span data-ttu-id="f3eab-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f3eab-255">In Global Catalog</span></span>      | <span data-ttu-id="f3eab-256">False</span><span class="sxs-lookup"><span data-stu-id="f3eab-256">False</span></span>                                              |
| <span data-ttu-id="f3eab-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3eab-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3eab-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f3eab-258">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="f3eab-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3eab-259">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="f3eab-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3eab-260">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="f3eab-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3eab-261">Search-Flags</span></span>           | <span data-ttu-id="f3eab-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3eab-262">0x00000000</span></span>                                         |
| <span data-ttu-id="f3eab-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3eab-263">System-Flags</span></span>           | <span data-ttu-id="f3eab-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3eab-264">0x00000010</span></span>                                         |
| <span data-ttu-id="f3eab-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f3eab-265">Classes used in</span></span>        | [<span data-ttu-id="f3eab-266">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="f3eab-266">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





