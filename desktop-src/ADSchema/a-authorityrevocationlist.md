---
title: Authority-Sperrung-List-Attribut
description: Zertifikat übergreifende Zertifikat Sperr Liste.
ms.assetid: a9bc7ed3-4600-41a7-bbe5-4ec546a421fa
ms.tgt_platform: multiple
keywords:
- AD-Schema für Authority-Sperrung-List-Attribut
- AD-Schema des Autorität revocationlist-Attributs
topic_type:
- apiref
api_name:
- Authority-Revocation-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fccc08cfb43bf4175bb51f2324e22c247d01f042
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123187"
---
# <a name="authority-revocation-list-attribute"></a><span data-ttu-id="c7593-105">Authority-Sperrung-List-Attribut</span><span class="sxs-lookup"><span data-stu-id="c7593-105">Authority-Revocation-List attribute</span></span>

<span data-ttu-id="c7593-106">Zertifikat übergreifende Zertifikat Sperr Liste.</span><span class="sxs-lookup"><span data-stu-id="c7593-106">Cross certificate, Certificate Revocation List.</span></span>



| <span data-ttu-id="c7593-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c7593-107">Entry</span></span> | <span data-ttu-id="c7593-108">Wert</span><span class="sxs-lookup"><span data-stu-id="c7593-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="c7593-109">CN</span><span class="sxs-lookup"><span data-stu-id="c7593-109">CN</span></span>                | <span data-ttu-id="c7593-110">Authority-Sperrungs Liste</span><span class="sxs-lookup"><span data-stu-id="c7593-110">Authority-Revocation-List</span></span>                             |
| <span data-ttu-id="c7593-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c7593-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c7593-112">Autorität revocationlist</span><span class="sxs-lookup"><span data-stu-id="c7593-112">authorityRevocationList</span></span>                               |
| <span data-ttu-id="c7593-113">Size</span><span class="sxs-lookup"><span data-stu-id="c7593-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="c7593-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c7593-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="c7593-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="c7593-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="c7593-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c7593-116">Attribute-Id</span></span>      | <span data-ttu-id="c7593-117">2.5.4.38</span><span class="sxs-lookup"><span data-stu-id="c7593-117">2.5.4.38</span></span>                                              |
| <span data-ttu-id="c7593-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c7593-118">System-Id-Guid</span></span>    | <span data-ttu-id="c7593-119">1677578d-47b3-11d1-a9c3-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="c7593-119">1677578d-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="c7593-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7593-120">Syntax</span></span>            | [<span data-ttu-id="c7593-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="c7593-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="c7593-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="c7593-122">Implementations</span></span>

-   [<span data-ttu-id="c7593-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c7593-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c7593-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c7593-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c7593-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c7593-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c7593-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c7593-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c7593-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c7593-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c7593-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c7593-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c7593-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c7593-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c7593-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c7593-130">Entry</span></span> | <span data-ttu-id="c7593-131">Wert</span><span class="sxs-lookup"><span data-stu-id="c7593-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7593-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c7593-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="c7593-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7593-133">MAPI-Id</span></span>                | <span data-ttu-id="c7593-134">0x8026</span><span class="sxs-lookup"><span data-stu-id="c7593-134">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="c7593-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7593-135">System-Only</span></span>            | <span data-ttu-id="c7593-136">False</span><span class="sxs-lookup"><span data-stu-id="c7593-136">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c7593-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c7593-138">False</span><span class="sxs-lookup"><span data-stu-id="c7593-138">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c7593-139">Is Indexed</span></span>             | <span data-ttu-id="c7593-140">False</span><span class="sxs-lookup"><span data-stu-id="c7593-140">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c7593-141">In Global Catalog</span></span>      | <span data-ttu-id="c7593-142">False</span><span class="sxs-lookup"><span data-stu-id="c7593-142">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c7593-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7593-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c7593-144">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="c7593-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7593-145">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c7593-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7593-146">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c7593-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7593-147">Search-Flags</span></span>           | <span data-ttu-id="c7593-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7593-148">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="c7593-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7593-149">System-Flags</span></span>           | <span data-ttu-id="c7593-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7593-150">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="c7593-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c7593-151">Classes used in</span></span>        | [<span data-ttu-id="c7593-152">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="c7593-152">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="c7593-153">**CRL-Verteilungs Punkt**</span><span class="sxs-lookup"><span data-stu-id="c7593-153">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c7593-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c7593-154">Windows Server 2003</span></span>



| <span data-ttu-id="c7593-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c7593-155">Entry</span></span> | <span data-ttu-id="c7593-156">Wert</span><span class="sxs-lookup"><span data-stu-id="c7593-156">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7593-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c7593-157">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="c7593-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7593-158">MAPI-Id</span></span>                | <span data-ttu-id="c7593-159">0x8026</span><span class="sxs-lookup"><span data-stu-id="c7593-159">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="c7593-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7593-160">System-Only</span></span>            | <span data-ttu-id="c7593-161">False</span><span class="sxs-lookup"><span data-stu-id="c7593-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c7593-162">Is-Single-Valued</span></span>       | <span data-ttu-id="c7593-163">False</span><span class="sxs-lookup"><span data-stu-id="c7593-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c7593-164">Is Indexed</span></span>             | <span data-ttu-id="c7593-165">False</span><span class="sxs-lookup"><span data-stu-id="c7593-165">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c7593-166">In Global Catalog</span></span>      | <span data-ttu-id="c7593-167">False</span><span class="sxs-lookup"><span data-stu-id="c7593-167">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c7593-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7593-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c7593-169">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="c7593-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7593-170">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c7593-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7593-171">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c7593-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7593-172">Search-Flags</span></span>           | <span data-ttu-id="c7593-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7593-173">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="c7593-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7593-174">System-Flags</span></span>           | <span data-ttu-id="c7593-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7593-175">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="c7593-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c7593-176">Classes used in</span></span>        | [<span data-ttu-id="c7593-177">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="c7593-177">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="c7593-178">**CRL-Verteilungs Punkt**</span><span class="sxs-lookup"><span data-stu-id="c7593-178">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c7593-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c7593-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c7593-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c7593-180">Entry</span></span> | <span data-ttu-id="c7593-181">Wert</span><span class="sxs-lookup"><span data-stu-id="c7593-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7593-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c7593-182">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="c7593-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7593-183">MAPI-Id</span></span>                | <span data-ttu-id="c7593-184">0x8026</span><span class="sxs-lookup"><span data-stu-id="c7593-184">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="c7593-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7593-185">System-Only</span></span>            | <span data-ttu-id="c7593-186">False</span><span class="sxs-lookup"><span data-stu-id="c7593-186">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c7593-187">Is-Single-Valued</span></span>       | <span data-ttu-id="c7593-188">False</span><span class="sxs-lookup"><span data-stu-id="c7593-188">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c7593-189">Is Indexed</span></span>             | <span data-ttu-id="c7593-190">False</span><span class="sxs-lookup"><span data-stu-id="c7593-190">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c7593-191">In Global Catalog</span></span>      | <span data-ttu-id="c7593-192">False</span><span class="sxs-lookup"><span data-stu-id="c7593-192">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c7593-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7593-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c7593-194">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="c7593-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7593-195">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c7593-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7593-196">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c7593-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7593-197">Search-Flags</span></span>           | <span data-ttu-id="c7593-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7593-198">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="c7593-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7593-199">System-Flags</span></span>           | <span data-ttu-id="c7593-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7593-200">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="c7593-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c7593-201">Classes used in</span></span>        | [<span data-ttu-id="c7593-202">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="c7593-202">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="c7593-203">**CRL-Verteilungs Punkt**</span><span class="sxs-lookup"><span data-stu-id="c7593-203">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c7593-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7593-204">Windows Server 2008</span></span>



| <span data-ttu-id="c7593-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c7593-205">Entry</span></span> | <span data-ttu-id="c7593-206">Wert</span><span class="sxs-lookup"><span data-stu-id="c7593-206">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7593-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c7593-207">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="c7593-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7593-208">MAPI-Id</span></span>                | <span data-ttu-id="c7593-209">0x8026</span><span class="sxs-lookup"><span data-stu-id="c7593-209">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="c7593-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7593-210">System-Only</span></span>            | <span data-ttu-id="c7593-211">False</span><span class="sxs-lookup"><span data-stu-id="c7593-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c7593-212">Is-Single-Valued</span></span>       | <span data-ttu-id="c7593-213">False</span><span class="sxs-lookup"><span data-stu-id="c7593-213">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c7593-214">Is Indexed</span></span>             | <span data-ttu-id="c7593-215">False</span><span class="sxs-lookup"><span data-stu-id="c7593-215">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c7593-216">In Global Catalog</span></span>      | <span data-ttu-id="c7593-217">False</span><span class="sxs-lookup"><span data-stu-id="c7593-217">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c7593-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7593-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c7593-219">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="c7593-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7593-220">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c7593-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7593-221">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c7593-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7593-222">Search-Flags</span></span>           | <span data-ttu-id="c7593-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7593-223">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="c7593-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7593-224">System-Flags</span></span>           | <span data-ttu-id="c7593-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7593-225">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="c7593-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c7593-226">Classes used in</span></span>        | [<span data-ttu-id="c7593-227">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="c7593-227">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="c7593-228">**CRL-Verteilungs Punkt**</span><span class="sxs-lookup"><span data-stu-id="c7593-228">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c7593-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c7593-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c7593-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c7593-230">Entry</span></span> | <span data-ttu-id="c7593-231">Wert</span><span class="sxs-lookup"><span data-stu-id="c7593-231">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7593-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c7593-232">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="c7593-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7593-233">MAPI-Id</span></span>                | <span data-ttu-id="c7593-234">0x8026</span><span class="sxs-lookup"><span data-stu-id="c7593-234">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="c7593-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7593-235">System-Only</span></span>            | <span data-ttu-id="c7593-236">False</span><span class="sxs-lookup"><span data-stu-id="c7593-236">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c7593-237">Is-Single-Valued</span></span>       | <span data-ttu-id="c7593-238">False</span><span class="sxs-lookup"><span data-stu-id="c7593-238">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c7593-239">Is Indexed</span></span>             | <span data-ttu-id="c7593-240">False</span><span class="sxs-lookup"><span data-stu-id="c7593-240">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c7593-241">In Global Catalog</span></span>      | <span data-ttu-id="c7593-242">False</span><span class="sxs-lookup"><span data-stu-id="c7593-242">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c7593-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7593-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c7593-244">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="c7593-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7593-245">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c7593-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7593-246">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c7593-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7593-247">Search-Flags</span></span>           | <span data-ttu-id="c7593-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7593-248">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="c7593-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7593-249">System-Flags</span></span>           | <span data-ttu-id="c7593-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7593-250">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="c7593-251">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c7593-251">Classes used in</span></span>        | [<span data-ttu-id="c7593-252">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="c7593-252">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="c7593-253">**CRL-Verteilungs Punkt**</span><span class="sxs-lookup"><span data-stu-id="c7593-253">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c7593-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c7593-254">Windows Server 2012</span></span>



| <span data-ttu-id="c7593-255">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c7593-255">Entry</span></span> | <span data-ttu-id="c7593-256">Wert</span><span class="sxs-lookup"><span data-stu-id="c7593-256">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7593-257">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c7593-257">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="c7593-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7593-258">MAPI-Id</span></span>                | <span data-ttu-id="c7593-259">0x8026</span><span class="sxs-lookup"><span data-stu-id="c7593-259">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="c7593-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7593-260">System-Only</span></span>            | <span data-ttu-id="c7593-261">False</span><span class="sxs-lookup"><span data-stu-id="c7593-261">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-262">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c7593-262">Is-Single-Valued</span></span>       | <span data-ttu-id="c7593-263">False</span><span class="sxs-lookup"><span data-stu-id="c7593-263">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-264">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c7593-264">Is Indexed</span></span>             | <span data-ttu-id="c7593-265">False</span><span class="sxs-lookup"><span data-stu-id="c7593-265">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-266">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c7593-266">In Global Catalog</span></span>      | <span data-ttu-id="c7593-267">False</span><span class="sxs-lookup"><span data-stu-id="c7593-267">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c7593-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c7593-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7593-269">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c7593-269">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="c7593-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7593-270">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c7593-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7593-271">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c7593-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7593-272">Search-Flags</span></span>           | <span data-ttu-id="c7593-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7593-273">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="c7593-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7593-274">System-Flags</span></span>           | <span data-ttu-id="c7593-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7593-275">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="c7593-276">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c7593-276">Classes used in</span></span>        | [<span data-ttu-id="c7593-277">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="c7593-277">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="c7593-278">**CRL-Verteilungs Punkt**</span><span class="sxs-lookup"><span data-stu-id="c7593-278">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 





