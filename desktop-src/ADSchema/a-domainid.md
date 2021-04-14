---
title: Domain-ID-Attribut
description: Verweis auf eine Domäne, die einer Zertifizierungsstelle zugeordnet ist.
ms.assetid: dd2f0822-cf94-485b-8d21-8954dddb81ad
ms.tgt_platform: multiple
keywords:
- Domänen-ID-Attribut, AD-Schema
- domainid-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Domain-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6c321fdea062ccbca907e22a2d72b06c26110ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392262"
---
# <a name="domain-id-attribute"></a><span data-ttu-id="2a6dd-105">Domain-ID-Attribut</span><span class="sxs-lookup"><span data-stu-id="2a6dd-105">Domain-ID attribute</span></span>

<span data-ttu-id="2a6dd-106">Verweis auf eine Domäne, die einer Zertifizierungsstelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2a6dd-106">Reference to a domain that is associated with a certification authority.</span></span>



| <span data-ttu-id="2a6dd-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2a6dd-107">Entry</span></span> | <span data-ttu-id="2a6dd-108">Wert</span><span class="sxs-lookup"><span data-stu-id="2a6dd-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="2a6dd-109">CN</span><span class="sxs-lookup"><span data-stu-id="2a6dd-109">CN</span></span>                | <span data-ttu-id="2a6dd-110">Domänen-ID</span><span class="sxs-lookup"><span data-stu-id="2a6dd-110">Domain-ID</span></span>                               |
| <span data-ttu-id="2a6dd-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2a6dd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2a6dd-112">Domänen-ID</span><span class="sxs-lookup"><span data-stu-id="2a6dd-112">domainID</span></span>                                |
| <span data-ttu-id="2a6dd-113">Size</span><span class="sxs-lookup"><span data-stu-id="2a6dd-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="2a6dd-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2a6dd-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="2a6dd-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="2a6dd-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="2a6dd-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2a6dd-116">Attribute-Id</span></span>      | <span data-ttu-id="2a6dd-117">1.2.840.113556.1.4.686</span><span class="sxs-lookup"><span data-stu-id="2a6dd-117">1.2.840.113556.1.4.686</span></span>                  |
| <span data-ttu-id="2a6dd-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2a6dd-118">System-Id-Guid</span></span>    | <span data-ttu-id="2a6dd-119">963d2734-48be-11d1-a9c3-0000 C1</span><span class="sxs-lookup"><span data-stu-id="2a6dd-119">963d2734-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="2a6dd-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a6dd-120">Syntax</span></span>            | [<span data-ttu-id="2a6dd-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="2a6dd-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="2a6dd-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="2a6dd-122">Implementations</span></span>

-   [<span data-ttu-id="2a6dd-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2a6dd-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2a6dd-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2a6dd-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2a6dd-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2a6dd-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2a6dd-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2a6dd-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2a6dd-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2a6dd-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2a6dd-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2a6dd-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2a6dd-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2a6dd-129">Windows 2000 Server</span></span>



| <span data-ttu-id="2a6dd-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2a6dd-130">Entry</span></span> | <span data-ttu-id="2a6dd-131">Wert</span><span class="sxs-lookup"><span data-stu-id="2a6dd-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="2a6dd-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2a6dd-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2a6dd-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a6dd-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2a6dd-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a6dd-134">System-Only</span></span>            | <span data-ttu-id="2a6dd-135">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-135">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2a6dd-136">Is-Single-Valued</span></span>       | <span data-ttu-id="2a6dd-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="2a6dd-137">True</span></span>                                                                   |
| <span data-ttu-id="2a6dd-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2a6dd-138">Is Indexed</span></span>             | <span data-ttu-id="2a6dd-139">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-139">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2a6dd-140">In Global Catalog</span></span>      | <span data-ttu-id="2a6dd-141">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-141">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2a6dd-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a6dd-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2a6dd-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="2a6dd-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a6dd-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="2a6dd-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a6dd-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="2a6dd-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a6dd-146">Search-Flags</span></span>           | <span data-ttu-id="2a6dd-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a6dd-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="2a6dd-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a6dd-148">System-Flags</span></span>           | <span data-ttu-id="2a6dd-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a6dd-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="2a6dd-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2a6dd-150">Classes used in</span></span>        | [<span data-ttu-id="2a6dd-151">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="2a6dd-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2a6dd-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2a6dd-152">Windows Server 2003</span></span>



| <span data-ttu-id="2a6dd-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2a6dd-153">Entry</span></span> | <span data-ttu-id="2a6dd-154">Wert</span><span class="sxs-lookup"><span data-stu-id="2a6dd-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="2a6dd-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2a6dd-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2a6dd-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a6dd-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2a6dd-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a6dd-157">System-Only</span></span>            | <span data-ttu-id="2a6dd-158">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-158">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2a6dd-159">Is-Single-Valued</span></span>       | <span data-ttu-id="2a6dd-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="2a6dd-160">True</span></span>                                                                   |
| <span data-ttu-id="2a6dd-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2a6dd-161">Is Indexed</span></span>             | <span data-ttu-id="2a6dd-162">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-162">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2a6dd-163">In Global Catalog</span></span>      | <span data-ttu-id="2a6dd-164">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-164">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2a6dd-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a6dd-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2a6dd-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="2a6dd-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a6dd-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="2a6dd-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a6dd-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="2a6dd-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a6dd-169">Search-Flags</span></span>           | <span data-ttu-id="2a6dd-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a6dd-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="2a6dd-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a6dd-171">System-Flags</span></span>           | <span data-ttu-id="2a6dd-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a6dd-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="2a6dd-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2a6dd-173">Classes used in</span></span>        | [<span data-ttu-id="2a6dd-174">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="2a6dd-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2a6dd-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2a6dd-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2a6dd-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2a6dd-176">Entry</span></span> | <span data-ttu-id="2a6dd-177">Wert</span><span class="sxs-lookup"><span data-stu-id="2a6dd-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="2a6dd-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2a6dd-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2a6dd-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a6dd-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2a6dd-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a6dd-180">System-Only</span></span>            | <span data-ttu-id="2a6dd-181">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-181">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2a6dd-182">Is-Single-Valued</span></span>       | <span data-ttu-id="2a6dd-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="2a6dd-183">True</span></span>                                                                   |
| <span data-ttu-id="2a6dd-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2a6dd-184">Is Indexed</span></span>             | <span data-ttu-id="2a6dd-185">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-185">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2a6dd-186">In Global Catalog</span></span>      | <span data-ttu-id="2a6dd-187">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-187">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2a6dd-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a6dd-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2a6dd-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="2a6dd-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a6dd-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="2a6dd-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a6dd-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="2a6dd-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a6dd-192">Search-Flags</span></span>           | <span data-ttu-id="2a6dd-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a6dd-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="2a6dd-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a6dd-194">System-Flags</span></span>           | <span data-ttu-id="2a6dd-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a6dd-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="2a6dd-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2a6dd-196">Classes used in</span></span>        | [<span data-ttu-id="2a6dd-197">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="2a6dd-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2a6dd-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a6dd-198">Windows Server 2008</span></span>



| <span data-ttu-id="2a6dd-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2a6dd-199">Entry</span></span> | <span data-ttu-id="2a6dd-200">Wert</span><span class="sxs-lookup"><span data-stu-id="2a6dd-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="2a6dd-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2a6dd-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2a6dd-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a6dd-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2a6dd-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a6dd-203">System-Only</span></span>            | <span data-ttu-id="2a6dd-204">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-204">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2a6dd-205">Is-Single-Valued</span></span>       | <span data-ttu-id="2a6dd-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="2a6dd-206">True</span></span>                                                                   |
| <span data-ttu-id="2a6dd-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2a6dd-207">Is Indexed</span></span>             | <span data-ttu-id="2a6dd-208">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-208">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2a6dd-209">In Global Catalog</span></span>      | <span data-ttu-id="2a6dd-210">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-210">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2a6dd-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a6dd-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2a6dd-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="2a6dd-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a6dd-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="2a6dd-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a6dd-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="2a6dd-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a6dd-215">Search-Flags</span></span>           | <span data-ttu-id="2a6dd-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a6dd-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="2a6dd-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a6dd-217">System-Flags</span></span>           | <span data-ttu-id="2a6dd-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a6dd-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="2a6dd-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2a6dd-219">Classes used in</span></span>        | [<span data-ttu-id="2a6dd-220">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="2a6dd-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2a6dd-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2a6dd-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2a6dd-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2a6dd-222">Entry</span></span> | <span data-ttu-id="2a6dd-223">Wert</span><span class="sxs-lookup"><span data-stu-id="2a6dd-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="2a6dd-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2a6dd-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2a6dd-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a6dd-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2a6dd-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a6dd-226">System-Only</span></span>            | <span data-ttu-id="2a6dd-227">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-227">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2a6dd-228">Is-Single-Valued</span></span>       | <span data-ttu-id="2a6dd-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="2a6dd-229">True</span></span>                                                                   |
| <span data-ttu-id="2a6dd-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2a6dd-230">Is Indexed</span></span>             | <span data-ttu-id="2a6dd-231">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-231">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2a6dd-232">In Global Catalog</span></span>      | <span data-ttu-id="2a6dd-233">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-233">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2a6dd-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a6dd-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2a6dd-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="2a6dd-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a6dd-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="2a6dd-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a6dd-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="2a6dd-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a6dd-238">Search-Flags</span></span>           | <span data-ttu-id="2a6dd-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a6dd-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="2a6dd-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a6dd-240">System-Flags</span></span>           | <span data-ttu-id="2a6dd-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a6dd-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="2a6dd-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2a6dd-242">Classes used in</span></span>        | [<span data-ttu-id="2a6dd-243">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="2a6dd-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2a6dd-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2a6dd-244">Windows Server 2012</span></span>



| <span data-ttu-id="2a6dd-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2a6dd-245">Entry</span></span> | <span data-ttu-id="2a6dd-246">Wert</span><span class="sxs-lookup"><span data-stu-id="2a6dd-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="2a6dd-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2a6dd-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2a6dd-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a6dd-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2a6dd-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a6dd-249">System-Only</span></span>            | <span data-ttu-id="2a6dd-250">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-250">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2a6dd-251">Is-Single-Valued</span></span>       | <span data-ttu-id="2a6dd-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="2a6dd-252">True</span></span>                                                                   |
| <span data-ttu-id="2a6dd-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2a6dd-253">Is Indexed</span></span>             | <span data-ttu-id="2a6dd-254">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-254">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2a6dd-255">In Global Catalog</span></span>      | <span data-ttu-id="2a6dd-256">False</span><span class="sxs-lookup"><span data-stu-id="2a6dd-256">False</span></span>                                                                  |
| <span data-ttu-id="2a6dd-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2a6dd-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a6dd-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2a6dd-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="2a6dd-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a6dd-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="2a6dd-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a6dd-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="2a6dd-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a6dd-261">Search-Flags</span></span>           | <span data-ttu-id="2a6dd-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a6dd-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="2a6dd-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a6dd-263">System-Flags</span></span>           | <span data-ttu-id="2a6dd-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a6dd-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="2a6dd-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2a6dd-265">Classes used in</span></span>        | [<span data-ttu-id="2a6dd-266">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="2a6dd-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





