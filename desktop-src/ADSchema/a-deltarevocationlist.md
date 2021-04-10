---
title: Delta-Sperr Listen Attribut
description: Liste der Zertifikate, die seit dem letzten Delta Update widerrufen wurden.
ms.assetid: fc755c22-6d4f-4509-abb8-47c4f2f37545
ms.tgt_platform: multiple
keywords:
- AD-Schema des Delta-Sperr Listen-Attributs
- ctarevocationlist-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Delta-Revocation-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e866090dfb754c11fb4a25bbe904d5922a8fafd6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107138"
---
# <a name="delta-revocation-list-attribute"></a><span data-ttu-id="4335b-105">Delta-Sperr Listen Attribut</span><span class="sxs-lookup"><span data-stu-id="4335b-105">Delta-Revocation-List attribute</span></span>

<span data-ttu-id="4335b-106">Liste der Zertifikate, die seit dem letzten Delta Update widerrufen wurden.</span><span class="sxs-lookup"><span data-stu-id="4335b-106">List of certificates that have been revoked since the last delta update.</span></span>



| <span data-ttu-id="4335b-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4335b-107">Entry</span></span> | <span data-ttu-id="4335b-108">Wert</span><span class="sxs-lookup"><span data-stu-id="4335b-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="4335b-109">CN</span><span class="sxs-lookup"><span data-stu-id="4335b-109">CN</span></span>                | <span data-ttu-id="4335b-110">Delta-Sperr Liste</span><span class="sxs-lookup"><span data-stu-id="4335b-110">Delta-Revocation-List</span></span>                                 |
| <span data-ttu-id="4335b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4335b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4335b-112">Delta-evocationlist</span><span class="sxs-lookup"><span data-stu-id="4335b-112">deltaRevocationList</span></span>                                   |
| <span data-ttu-id="4335b-113">Size</span><span class="sxs-lookup"><span data-stu-id="4335b-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="4335b-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="4335b-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="4335b-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="4335b-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="4335b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4335b-116">Attribute-Id</span></span>      | <span data-ttu-id="4335b-117">2.5.4.53</span><span class="sxs-lookup"><span data-stu-id="4335b-117">2.5.4.53</span></span>                                              |
| <span data-ttu-id="4335b-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4335b-118">System-Id-Guid</span></span>    | <span data-ttu-id="4335b-119">167757b5-47F 3-11d1-a9c3-0000b C1</span><span class="sxs-lookup"><span data-stu-id="4335b-119">167757b5-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="4335b-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="4335b-120">Syntax</span></span>            | [<span data-ttu-id="4335b-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="4335b-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="4335b-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="4335b-122">Implementations</span></span>

-   [<span data-ttu-id="4335b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4335b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4335b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4335b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4335b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4335b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4335b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4335b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4335b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4335b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4335b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4335b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4335b-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4335b-129">Windows 2000 Server</span></span>



| <span data-ttu-id="4335b-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4335b-130">Entry</span></span> | <span data-ttu-id="4335b-131">Wert</span><span class="sxs-lookup"><span data-stu-id="4335b-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4335b-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4335b-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="4335b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4335b-133">MAPI-Id</span></span>                | <span data-ttu-id="4335b-134">0x8c46</span><span class="sxs-lookup"><span data-stu-id="4335b-134">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="4335b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="4335b-135">System-Only</span></span>            | <span data-ttu-id="4335b-136">False</span><span class="sxs-lookup"><span data-stu-id="4335b-136">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4335b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="4335b-138">False</span><span class="sxs-lookup"><span data-stu-id="4335b-138">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4335b-139">Is Indexed</span></span>             | <span data-ttu-id="4335b-140">False</span><span class="sxs-lookup"><span data-stu-id="4335b-140">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4335b-141">In Global Catalog</span></span>      | <span data-ttu-id="4335b-142">False</span><span class="sxs-lookup"><span data-stu-id="4335b-142">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4335b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="4335b-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4335b-144">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="4335b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4335b-145">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="4335b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4335b-146">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="4335b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4335b-147">Search-Flags</span></span>           | <span data-ttu-id="4335b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4335b-148">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="4335b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4335b-149">System-Flags</span></span>           | <span data-ttu-id="4335b-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4335b-150">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="4335b-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4335b-151">Classes used in</span></span>        | [<span data-ttu-id="4335b-152">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="4335b-152">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="4335b-153">**CRL-Verteilungs Punkt**</span><span class="sxs-lookup"><span data-stu-id="4335b-153">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4335b-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4335b-154">Windows Server 2003</span></span>



| <span data-ttu-id="4335b-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4335b-155">Entry</span></span> | <span data-ttu-id="4335b-156">Wert</span><span class="sxs-lookup"><span data-stu-id="4335b-156">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4335b-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4335b-157">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="4335b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4335b-158">MAPI-Id</span></span>                | <span data-ttu-id="4335b-159">0x8c46</span><span class="sxs-lookup"><span data-stu-id="4335b-159">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="4335b-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="4335b-160">System-Only</span></span>            | <span data-ttu-id="4335b-161">False</span><span class="sxs-lookup"><span data-stu-id="4335b-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4335b-162">Is-Single-Valued</span></span>       | <span data-ttu-id="4335b-163">False</span><span class="sxs-lookup"><span data-stu-id="4335b-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4335b-164">Is Indexed</span></span>             | <span data-ttu-id="4335b-165">False</span><span class="sxs-lookup"><span data-stu-id="4335b-165">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4335b-166">In Global Catalog</span></span>      | <span data-ttu-id="4335b-167">False</span><span class="sxs-lookup"><span data-stu-id="4335b-167">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4335b-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="4335b-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4335b-169">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="4335b-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4335b-170">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="4335b-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4335b-171">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="4335b-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4335b-172">Search-Flags</span></span>           | <span data-ttu-id="4335b-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4335b-173">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="4335b-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4335b-174">System-Flags</span></span>           | <span data-ttu-id="4335b-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4335b-175">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="4335b-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4335b-176">Classes used in</span></span>        | [<span data-ttu-id="4335b-177">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="4335b-177">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="4335b-178">**CRL-Verteilungs Punkt**</span><span class="sxs-lookup"><span data-stu-id="4335b-178">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4335b-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4335b-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4335b-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4335b-180">Entry</span></span> | <span data-ttu-id="4335b-181">Wert</span><span class="sxs-lookup"><span data-stu-id="4335b-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4335b-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4335b-182">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="4335b-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4335b-183">MAPI-Id</span></span>                | <span data-ttu-id="4335b-184">0x8c46</span><span class="sxs-lookup"><span data-stu-id="4335b-184">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="4335b-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="4335b-185">System-Only</span></span>            | <span data-ttu-id="4335b-186">False</span><span class="sxs-lookup"><span data-stu-id="4335b-186">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4335b-187">Is-Single-Valued</span></span>       | <span data-ttu-id="4335b-188">False</span><span class="sxs-lookup"><span data-stu-id="4335b-188">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4335b-189">Is Indexed</span></span>             | <span data-ttu-id="4335b-190">False</span><span class="sxs-lookup"><span data-stu-id="4335b-190">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4335b-191">In Global Catalog</span></span>      | <span data-ttu-id="4335b-192">False</span><span class="sxs-lookup"><span data-stu-id="4335b-192">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4335b-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="4335b-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4335b-194">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="4335b-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4335b-195">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="4335b-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4335b-196">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="4335b-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4335b-197">Search-Flags</span></span>           | <span data-ttu-id="4335b-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4335b-198">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="4335b-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4335b-199">System-Flags</span></span>           | <span data-ttu-id="4335b-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4335b-200">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="4335b-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4335b-201">Classes used in</span></span>        | [<span data-ttu-id="4335b-202">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="4335b-202">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="4335b-203">**CRL-Verteilungs Punkt**</span><span class="sxs-lookup"><span data-stu-id="4335b-203">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4335b-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4335b-204">Windows Server 2008</span></span>



| <span data-ttu-id="4335b-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4335b-205">Entry</span></span> | <span data-ttu-id="4335b-206">Wert</span><span class="sxs-lookup"><span data-stu-id="4335b-206">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4335b-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4335b-207">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="4335b-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4335b-208">MAPI-Id</span></span>                | <span data-ttu-id="4335b-209">0x8c46</span><span class="sxs-lookup"><span data-stu-id="4335b-209">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="4335b-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="4335b-210">System-Only</span></span>            | <span data-ttu-id="4335b-211">False</span><span class="sxs-lookup"><span data-stu-id="4335b-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4335b-212">Is-Single-Valued</span></span>       | <span data-ttu-id="4335b-213">False</span><span class="sxs-lookup"><span data-stu-id="4335b-213">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4335b-214">Is Indexed</span></span>             | <span data-ttu-id="4335b-215">False</span><span class="sxs-lookup"><span data-stu-id="4335b-215">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4335b-216">In Global Catalog</span></span>      | <span data-ttu-id="4335b-217">False</span><span class="sxs-lookup"><span data-stu-id="4335b-217">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4335b-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="4335b-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4335b-219">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="4335b-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4335b-220">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="4335b-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4335b-221">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="4335b-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4335b-222">Search-Flags</span></span>           | <span data-ttu-id="4335b-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4335b-223">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="4335b-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4335b-224">System-Flags</span></span>           | <span data-ttu-id="4335b-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4335b-225">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="4335b-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4335b-226">Classes used in</span></span>        | [<span data-ttu-id="4335b-227">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="4335b-227">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="4335b-228">**CRL-Verteilungs Punkt**</span><span class="sxs-lookup"><span data-stu-id="4335b-228">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4335b-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4335b-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4335b-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4335b-230">Entry</span></span> | <span data-ttu-id="4335b-231">Wert</span><span class="sxs-lookup"><span data-stu-id="4335b-231">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4335b-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4335b-232">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="4335b-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4335b-233">MAPI-Id</span></span>                | <span data-ttu-id="4335b-234">0x8c46</span><span class="sxs-lookup"><span data-stu-id="4335b-234">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="4335b-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="4335b-235">System-Only</span></span>            | <span data-ttu-id="4335b-236">False</span><span class="sxs-lookup"><span data-stu-id="4335b-236">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4335b-237">Is-Single-Valued</span></span>       | <span data-ttu-id="4335b-238">False</span><span class="sxs-lookup"><span data-stu-id="4335b-238">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4335b-239">Is Indexed</span></span>             | <span data-ttu-id="4335b-240">False</span><span class="sxs-lookup"><span data-stu-id="4335b-240">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4335b-241">In Global Catalog</span></span>      | <span data-ttu-id="4335b-242">False</span><span class="sxs-lookup"><span data-stu-id="4335b-242">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4335b-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="4335b-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4335b-244">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="4335b-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4335b-245">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="4335b-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4335b-246">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="4335b-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4335b-247">Search-Flags</span></span>           | <span data-ttu-id="4335b-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4335b-248">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="4335b-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4335b-249">System-Flags</span></span>           | <span data-ttu-id="4335b-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4335b-250">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="4335b-251">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4335b-251">Classes used in</span></span>        | [<span data-ttu-id="4335b-252">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="4335b-252">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="4335b-253">**CRL-Verteilungs Punkt**</span><span class="sxs-lookup"><span data-stu-id="4335b-253">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4335b-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4335b-254">Windows Server 2012</span></span>



| <span data-ttu-id="4335b-255">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4335b-255">Entry</span></span> | <span data-ttu-id="4335b-256">Wert</span><span class="sxs-lookup"><span data-stu-id="4335b-256">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4335b-257">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4335b-257">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="4335b-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4335b-258">MAPI-Id</span></span>                | <span data-ttu-id="4335b-259">0x8c46</span><span class="sxs-lookup"><span data-stu-id="4335b-259">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="4335b-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="4335b-260">System-Only</span></span>            | <span data-ttu-id="4335b-261">False</span><span class="sxs-lookup"><span data-stu-id="4335b-261">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-262">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4335b-262">Is-Single-Valued</span></span>       | <span data-ttu-id="4335b-263">False</span><span class="sxs-lookup"><span data-stu-id="4335b-263">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-264">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4335b-264">Is Indexed</span></span>             | <span data-ttu-id="4335b-265">False</span><span class="sxs-lookup"><span data-stu-id="4335b-265">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-266">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4335b-266">In Global Catalog</span></span>      | <span data-ttu-id="4335b-267">False</span><span class="sxs-lookup"><span data-stu-id="4335b-267">False</span></span>                                                                                                                                      |
| <span data-ttu-id="4335b-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4335b-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="4335b-269">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4335b-269">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="4335b-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4335b-270">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="4335b-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4335b-271">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="4335b-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4335b-272">Search-Flags</span></span>           | <span data-ttu-id="4335b-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4335b-273">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="4335b-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4335b-274">System-Flags</span></span>           | <span data-ttu-id="4335b-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4335b-275">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="4335b-276">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4335b-276">Classes used in</span></span>        | [<span data-ttu-id="4335b-277">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="4335b-277">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="4335b-278">**CRL-Verteilungs Punkt**</span><span class="sxs-lookup"><span data-stu-id="4335b-278">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 





