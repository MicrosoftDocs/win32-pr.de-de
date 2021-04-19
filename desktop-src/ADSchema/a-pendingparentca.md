---
title: Pending-Parent-ca-Attribut
description: Verweis auf die Zertifizierungsstellen, die die ausstehenden Zertifikate für diese Zertifizierungsstelle ausgestellt haben.
ms.assetid: 9cdac673-aecd-4a42-93f5-c869fa136186
ms.tgt_platform: multiple
keywords:
- AD-Schema "Pending-Parent-ca-Attribut"
- cschema für das Attribut "pdingcentca"
topic_type:
- apiref
api_name:
- Pending-Parent-CA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5e100a18980780f4086f09ce39a060703462ae
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342522"
---
# <a name="pending-parent-ca-attribute"></a><span data-ttu-id="0557c-105">Pending-Parent-ca-Attribut</span><span class="sxs-lookup"><span data-stu-id="0557c-105">Pending-Parent-CA attribute</span></span>

<span data-ttu-id="0557c-106">Verweis auf die Zertifizierungsstellen, die die ausstehenden Zertifikate für diese Zertifizierungsstelle ausgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="0557c-106">Reference to the certification authorities that issued the pending certificates for this certification authority.</span></span>



| <span data-ttu-id="0557c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0557c-107">Entry</span></span> | <span data-ttu-id="0557c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="0557c-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="0557c-109">CN</span><span class="sxs-lookup"><span data-stu-id="0557c-109">CN</span></span>                | <span data-ttu-id="0557c-110">Pending-Parent-ca</span><span class="sxs-lookup"><span data-stu-id="0557c-110">Pending-Parent-CA</span></span>                       |
| <span data-ttu-id="0557c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0557c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0557c-112">"pdingparameentca"</span><span class="sxs-lookup"><span data-stu-id="0557c-112">pendingParentCA</span></span>                         |
| <span data-ttu-id="0557c-113">Size</span><span class="sxs-lookup"><span data-stu-id="0557c-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="0557c-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0557c-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="0557c-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="0557c-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="0557c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0557c-116">Attribute-Id</span></span>      | <span data-ttu-id="0557c-117">1.2.840.113556.1.4.695</span><span class="sxs-lookup"><span data-stu-id="0557c-117">1.2.840.113556.1.4.695</span></span>                  |
| <span data-ttu-id="0557c-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0557c-118">System-Id-Guid</span></span>    | <span data-ttu-id="0557c-119">963d273e-48be-11d1-a9c3-0000 C1</span><span class="sxs-lookup"><span data-stu-id="0557c-119">963d273e-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="0557c-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="0557c-120">Syntax</span></span>            | [<span data-ttu-id="0557c-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="0557c-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="0557c-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="0557c-122">Implementations</span></span>

-   [<span data-ttu-id="0557c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0557c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0557c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0557c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0557c-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0557c-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0557c-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0557c-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0557c-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0557c-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0557c-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0557c-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0557c-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0557c-129">Windows 2000 Server</span></span>



| <span data-ttu-id="0557c-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0557c-130">Entry</span></span> | <span data-ttu-id="0557c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="0557c-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="0557c-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0557c-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0557c-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0557c-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0557c-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="0557c-134">System-Only</span></span>            | <span data-ttu-id="0557c-135">False</span><span class="sxs-lookup"><span data-stu-id="0557c-135">False</span></span>                                                                  |
| <span data-ttu-id="0557c-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0557c-136">Is-Single-Valued</span></span>       | <span data-ttu-id="0557c-137">False</span><span class="sxs-lookup"><span data-stu-id="0557c-137">False</span></span>                                                                  |
| <span data-ttu-id="0557c-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0557c-138">Is Indexed</span></span>             | <span data-ttu-id="0557c-139">False</span><span class="sxs-lookup"><span data-stu-id="0557c-139">False</span></span>                                                                  |
| <span data-ttu-id="0557c-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0557c-140">In Global Catalog</span></span>      | <span data-ttu-id="0557c-141">False</span><span class="sxs-lookup"><span data-stu-id="0557c-141">False</span></span>                                                                  |
| <span data-ttu-id="0557c-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0557c-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="0557c-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0557c-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="0557c-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0557c-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="0557c-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0557c-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="0557c-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0557c-146">Search-Flags</span></span>           | <span data-ttu-id="0557c-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0557c-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="0557c-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0557c-148">System-Flags</span></span>           | <span data-ttu-id="0557c-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0557c-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="0557c-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0557c-150">Classes used in</span></span>        | [<span data-ttu-id="0557c-151">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="0557c-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0557c-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0557c-152">Windows Server 2003</span></span>



| <span data-ttu-id="0557c-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0557c-153">Entry</span></span> | <span data-ttu-id="0557c-154">Wert</span><span class="sxs-lookup"><span data-stu-id="0557c-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="0557c-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0557c-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0557c-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0557c-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0557c-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="0557c-157">System-Only</span></span>            | <span data-ttu-id="0557c-158">False</span><span class="sxs-lookup"><span data-stu-id="0557c-158">False</span></span>                                                                  |
| <span data-ttu-id="0557c-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0557c-159">Is-Single-Valued</span></span>       | <span data-ttu-id="0557c-160">False</span><span class="sxs-lookup"><span data-stu-id="0557c-160">False</span></span>                                                                  |
| <span data-ttu-id="0557c-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0557c-161">Is Indexed</span></span>             | <span data-ttu-id="0557c-162">False</span><span class="sxs-lookup"><span data-stu-id="0557c-162">False</span></span>                                                                  |
| <span data-ttu-id="0557c-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0557c-163">In Global Catalog</span></span>      | <span data-ttu-id="0557c-164">False</span><span class="sxs-lookup"><span data-stu-id="0557c-164">False</span></span>                                                                  |
| <span data-ttu-id="0557c-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0557c-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="0557c-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0557c-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="0557c-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0557c-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="0557c-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0557c-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="0557c-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0557c-169">Search-Flags</span></span>           | <span data-ttu-id="0557c-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0557c-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="0557c-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0557c-171">System-Flags</span></span>           | <span data-ttu-id="0557c-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0557c-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="0557c-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0557c-173">Classes used in</span></span>        | [<span data-ttu-id="0557c-174">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="0557c-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0557c-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0557c-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0557c-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0557c-176">Entry</span></span> | <span data-ttu-id="0557c-177">Wert</span><span class="sxs-lookup"><span data-stu-id="0557c-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="0557c-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0557c-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0557c-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0557c-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0557c-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="0557c-180">System-Only</span></span>            | <span data-ttu-id="0557c-181">False</span><span class="sxs-lookup"><span data-stu-id="0557c-181">False</span></span>                                                                  |
| <span data-ttu-id="0557c-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0557c-182">Is-Single-Valued</span></span>       | <span data-ttu-id="0557c-183">False</span><span class="sxs-lookup"><span data-stu-id="0557c-183">False</span></span>                                                                  |
| <span data-ttu-id="0557c-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0557c-184">Is Indexed</span></span>             | <span data-ttu-id="0557c-185">False</span><span class="sxs-lookup"><span data-stu-id="0557c-185">False</span></span>                                                                  |
| <span data-ttu-id="0557c-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0557c-186">In Global Catalog</span></span>      | <span data-ttu-id="0557c-187">False</span><span class="sxs-lookup"><span data-stu-id="0557c-187">False</span></span>                                                                  |
| <span data-ttu-id="0557c-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0557c-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="0557c-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0557c-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="0557c-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0557c-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="0557c-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0557c-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="0557c-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0557c-192">Search-Flags</span></span>           | <span data-ttu-id="0557c-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0557c-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="0557c-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0557c-194">System-Flags</span></span>           | <span data-ttu-id="0557c-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0557c-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="0557c-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0557c-196">Classes used in</span></span>        | [<span data-ttu-id="0557c-197">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="0557c-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0557c-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0557c-198">Windows Server 2008</span></span>



| <span data-ttu-id="0557c-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0557c-199">Entry</span></span> | <span data-ttu-id="0557c-200">Wert</span><span class="sxs-lookup"><span data-stu-id="0557c-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="0557c-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0557c-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0557c-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0557c-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0557c-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="0557c-203">System-Only</span></span>            | <span data-ttu-id="0557c-204">False</span><span class="sxs-lookup"><span data-stu-id="0557c-204">False</span></span>                                                                  |
| <span data-ttu-id="0557c-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0557c-205">Is-Single-Valued</span></span>       | <span data-ttu-id="0557c-206">False</span><span class="sxs-lookup"><span data-stu-id="0557c-206">False</span></span>                                                                  |
| <span data-ttu-id="0557c-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0557c-207">Is Indexed</span></span>             | <span data-ttu-id="0557c-208">False</span><span class="sxs-lookup"><span data-stu-id="0557c-208">False</span></span>                                                                  |
| <span data-ttu-id="0557c-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0557c-209">In Global Catalog</span></span>      | <span data-ttu-id="0557c-210">False</span><span class="sxs-lookup"><span data-stu-id="0557c-210">False</span></span>                                                                  |
| <span data-ttu-id="0557c-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0557c-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="0557c-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0557c-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="0557c-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0557c-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="0557c-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0557c-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="0557c-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0557c-215">Search-Flags</span></span>           | <span data-ttu-id="0557c-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0557c-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="0557c-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0557c-217">System-Flags</span></span>           | <span data-ttu-id="0557c-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0557c-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="0557c-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0557c-219">Classes used in</span></span>        | [<span data-ttu-id="0557c-220">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="0557c-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0557c-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0557c-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0557c-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0557c-222">Entry</span></span> | <span data-ttu-id="0557c-223">Wert</span><span class="sxs-lookup"><span data-stu-id="0557c-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="0557c-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0557c-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0557c-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0557c-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0557c-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="0557c-226">System-Only</span></span>            | <span data-ttu-id="0557c-227">False</span><span class="sxs-lookup"><span data-stu-id="0557c-227">False</span></span>                                                                  |
| <span data-ttu-id="0557c-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0557c-228">Is-Single-Valued</span></span>       | <span data-ttu-id="0557c-229">False</span><span class="sxs-lookup"><span data-stu-id="0557c-229">False</span></span>                                                                  |
| <span data-ttu-id="0557c-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0557c-230">Is Indexed</span></span>             | <span data-ttu-id="0557c-231">False</span><span class="sxs-lookup"><span data-stu-id="0557c-231">False</span></span>                                                                  |
| <span data-ttu-id="0557c-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0557c-232">In Global Catalog</span></span>      | <span data-ttu-id="0557c-233">False</span><span class="sxs-lookup"><span data-stu-id="0557c-233">False</span></span>                                                                  |
| <span data-ttu-id="0557c-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0557c-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="0557c-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0557c-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="0557c-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0557c-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="0557c-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0557c-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="0557c-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0557c-238">Search-Flags</span></span>           | <span data-ttu-id="0557c-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0557c-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="0557c-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0557c-240">System-Flags</span></span>           | <span data-ttu-id="0557c-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0557c-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="0557c-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0557c-242">Classes used in</span></span>        | [<span data-ttu-id="0557c-243">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="0557c-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0557c-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0557c-244">Windows Server 2012</span></span>



| <span data-ttu-id="0557c-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0557c-245">Entry</span></span> | <span data-ttu-id="0557c-246">Wert</span><span class="sxs-lookup"><span data-stu-id="0557c-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="0557c-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0557c-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0557c-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0557c-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="0557c-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="0557c-249">System-Only</span></span>            | <span data-ttu-id="0557c-250">False</span><span class="sxs-lookup"><span data-stu-id="0557c-250">False</span></span>                                                                  |
| <span data-ttu-id="0557c-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0557c-251">Is-Single-Valued</span></span>       | <span data-ttu-id="0557c-252">False</span><span class="sxs-lookup"><span data-stu-id="0557c-252">False</span></span>                                                                  |
| <span data-ttu-id="0557c-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0557c-253">Is Indexed</span></span>             | <span data-ttu-id="0557c-254">False</span><span class="sxs-lookup"><span data-stu-id="0557c-254">False</span></span>                                                                  |
| <span data-ttu-id="0557c-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0557c-255">In Global Catalog</span></span>      | <span data-ttu-id="0557c-256">False</span><span class="sxs-lookup"><span data-stu-id="0557c-256">False</span></span>                                                                  |
| <span data-ttu-id="0557c-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0557c-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="0557c-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0557c-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="0557c-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0557c-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="0557c-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0557c-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="0557c-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0557c-261">Search-Flags</span></span>           | <span data-ttu-id="0557c-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0557c-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="0557c-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0557c-263">System-Flags</span></span>           | <span data-ttu-id="0557c-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0557c-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="0557c-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0557c-265">Classes used in</span></span>        | [<span data-ttu-id="0557c-266">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="0557c-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





