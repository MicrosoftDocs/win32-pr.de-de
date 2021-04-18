---
title: MS-DS-pro-User-Trust-Tombstones-Quota-Attribut
description: Wird verwendet, um ein pro-Benutzer-Kontingent zum Löschen von Trusted-Domain Objekten zu erzwingen, wenn die Autorisierung auf der Übereinstimmung der SID des Benutzers basiert.
ms.assetid: 4db98754-a2d1-43a4-b9cb-0e3fcbbf3ed9
ms.tgt_platform: multiple
keywords:
- MS-DS-pro-User-Trust-Tombstones-Quota-Attribut AD-Schema
- AD-Schema des msDS-perusertrusttombstonesquota-Attributs
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Tombstones-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c94bb62b822552a863df99dac83e98462514c42
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344293"
---
# <a name="ms-ds-per-user-trust-tombstones-quota-attribute"></a><span data-ttu-id="feda9-105">MS-DS-pro-User-Trust-Tombstones-Quota-Attribut</span><span class="sxs-lookup"><span data-stu-id="feda9-105">MS-DS-Per-User-Trust-Tombstones-Quota attribute</span></span>

<span data-ttu-id="feda9-106">Wird verwendet, um ein pro-Benutzer-Kontingent zum Löschen von Trusted-Domain Objekten zu erzwingen, wenn die Autorisierung auf der Übereinstimmung der SID des Benutzers basiert.</span><span class="sxs-lookup"><span data-stu-id="feda9-106">Used to enforce a per-user quota for deleting Trusted-Domain objects when authorization is based on matching the user's SID.</span></span>



| <span data-ttu-id="feda9-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="feda9-107">Entry</span></span> | <span data-ttu-id="feda9-108">Wert</span><span class="sxs-lookup"><span data-stu-id="feda9-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="feda9-109">CN</span><span class="sxs-lookup"><span data-stu-id="feda9-109">CN</span></span>                | <span data-ttu-id="feda9-110">MS-DS-pro Benutzer-Trust-Tombstones-Quota</span><span class="sxs-lookup"><span data-stu-id="feda9-110">MS-DS-Per-User-Trust-Tombstones-Quota</span></span>     |
| <span data-ttu-id="feda9-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="feda9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="feda9-112">MSDS-perusertrusttombstones-Kontingent</span><span class="sxs-lookup"><span data-stu-id="feda9-112">msDS-PerUserTrustTombstonesQuota</span></span>          |
| <span data-ttu-id="feda9-113">Size</span><span class="sxs-lookup"><span data-stu-id="feda9-113">Size</span></span>              | \-                                        |
| <span data-ttu-id="feda9-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="feda9-114">Update Privilege</span></span>  | <span data-ttu-id="feda9-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="feda9-115">Domain administrator</span></span>                      |
| <span data-ttu-id="feda9-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="feda9-116">Update Frequency</span></span>  | <span data-ttu-id="feda9-117">Bei der Gesamtstruktur Erstellung und selten danach.</span><span class="sxs-lookup"><span data-stu-id="feda9-117">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="feda9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="feda9-118">Attribute-Id</span></span>      | <span data-ttu-id="feda9-119">1.2.840.113556.1.4.1790</span><span class="sxs-lookup"><span data-stu-id="feda9-119">1.2.840.113556.1.4.1790</span></span>                   |
| <span data-ttu-id="feda9-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="feda9-120">System-Id-Guid</span></span>    | <span data-ttu-id="feda9-121">8b70a6c6-50s9-4fa3-a71e-1ce03040449b</span><span class="sxs-lookup"><span data-stu-id="feda9-121">8b70a6c6-50f9-4fa3-a71e-1ce03040449b</span></span>      |
| <span data-ttu-id="feda9-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="feda9-122">Syntax</span></span>            | [<span data-ttu-id="feda9-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="feda9-123">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="feda9-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="feda9-124">Implementations</span></span>

-   [<span data-ttu-id="feda9-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="feda9-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="feda9-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="feda9-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="feda9-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="feda9-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="feda9-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="feda9-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="feda9-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="feda9-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="feda9-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="feda9-130">Windows Server 2003</span></span>



| <span data-ttu-id="feda9-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="feda9-131">Entry</span></span> | <span data-ttu-id="feda9-132">Wert</span><span class="sxs-lookup"><span data-stu-id="feda9-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="feda9-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="feda9-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="feda9-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="feda9-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="feda9-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="feda9-135">System-Only</span></span>            | <span data-ttu-id="feda9-136">False</span><span class="sxs-lookup"><span data-stu-id="feda9-136">False</span></span>                                        |
| <span data-ttu-id="feda9-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="feda9-137">Is-Single-Valued</span></span>       | <span data-ttu-id="feda9-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="feda9-138">True</span></span>                                         |
| <span data-ttu-id="feda9-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="feda9-139">Is Indexed</span></span>             | <span data-ttu-id="feda9-140">False</span><span class="sxs-lookup"><span data-stu-id="feda9-140">False</span></span>                                        |
| <span data-ttu-id="feda9-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="feda9-141">In Global Catalog</span></span>      | <span data-ttu-id="feda9-142">False</span><span class="sxs-lookup"><span data-stu-id="feda9-142">False</span></span>                                        |
| <span data-ttu-id="feda9-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="feda9-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="feda9-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="feda9-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="feda9-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="feda9-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="feda9-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="feda9-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="feda9-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="feda9-147">Search-Flags</span></span>           | <span data-ttu-id="feda9-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="feda9-148">0x00000000</span></span>                                   |
| <span data-ttu-id="feda9-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="feda9-149">System-Flags</span></span>           | <span data-ttu-id="feda9-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="feda9-150">0x00000010</span></span>                                   |
| <span data-ttu-id="feda9-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="feda9-151">Classes used in</span></span>        | [<span data-ttu-id="feda9-152">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="feda9-152">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="feda9-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="feda9-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="feda9-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="feda9-154">Entry</span></span> | <span data-ttu-id="feda9-155">Wert</span><span class="sxs-lookup"><span data-stu-id="feda9-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="feda9-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="feda9-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="feda9-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="feda9-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="feda9-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="feda9-158">System-Only</span></span>            | <span data-ttu-id="feda9-159">False</span><span class="sxs-lookup"><span data-stu-id="feda9-159">False</span></span>                                        |
| <span data-ttu-id="feda9-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="feda9-160">Is-Single-Valued</span></span>       | <span data-ttu-id="feda9-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="feda9-161">True</span></span>                                         |
| <span data-ttu-id="feda9-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="feda9-162">Is Indexed</span></span>             | <span data-ttu-id="feda9-163">False</span><span class="sxs-lookup"><span data-stu-id="feda9-163">False</span></span>                                        |
| <span data-ttu-id="feda9-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="feda9-164">In Global Catalog</span></span>      | <span data-ttu-id="feda9-165">False</span><span class="sxs-lookup"><span data-stu-id="feda9-165">False</span></span>                                        |
| <span data-ttu-id="feda9-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="feda9-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="feda9-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="feda9-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="feda9-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="feda9-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="feda9-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="feda9-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="feda9-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="feda9-170">Search-Flags</span></span>           | <span data-ttu-id="feda9-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="feda9-171">0x00000000</span></span>                                   |
| <span data-ttu-id="feda9-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="feda9-172">System-Flags</span></span>           | <span data-ttu-id="feda9-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="feda9-173">0x00000010</span></span>                                   |
| <span data-ttu-id="feda9-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="feda9-174">Classes used in</span></span>        | [<span data-ttu-id="feda9-175">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="feda9-175">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="feda9-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="feda9-176">Windows Server 2008</span></span>



| <span data-ttu-id="feda9-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="feda9-177">Entry</span></span> | <span data-ttu-id="feda9-178">Wert</span><span class="sxs-lookup"><span data-stu-id="feda9-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="feda9-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="feda9-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="feda9-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="feda9-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="feda9-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="feda9-181">System-Only</span></span>            | <span data-ttu-id="feda9-182">False</span><span class="sxs-lookup"><span data-stu-id="feda9-182">False</span></span>                                        |
| <span data-ttu-id="feda9-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="feda9-183">Is-Single-Valued</span></span>       | <span data-ttu-id="feda9-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="feda9-184">True</span></span>                                         |
| <span data-ttu-id="feda9-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="feda9-185">Is Indexed</span></span>             | <span data-ttu-id="feda9-186">False</span><span class="sxs-lookup"><span data-stu-id="feda9-186">False</span></span>                                        |
| <span data-ttu-id="feda9-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="feda9-187">In Global Catalog</span></span>      | <span data-ttu-id="feda9-188">False</span><span class="sxs-lookup"><span data-stu-id="feda9-188">False</span></span>                                        |
| <span data-ttu-id="feda9-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="feda9-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="feda9-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="feda9-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="feda9-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="feda9-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="feda9-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="feda9-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="feda9-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="feda9-193">Search-Flags</span></span>           | <span data-ttu-id="feda9-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="feda9-194">0x00000000</span></span>                                   |
| <span data-ttu-id="feda9-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="feda9-195">System-Flags</span></span>           | <span data-ttu-id="feda9-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="feda9-196">0x00000010</span></span>                                   |
| <span data-ttu-id="feda9-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="feda9-197">Classes used in</span></span>        | [<span data-ttu-id="feda9-198">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="feda9-198">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="feda9-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="feda9-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="feda9-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="feda9-200">Entry</span></span> | <span data-ttu-id="feda9-201">Wert</span><span class="sxs-lookup"><span data-stu-id="feda9-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="feda9-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="feda9-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="feda9-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="feda9-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="feda9-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="feda9-204">System-Only</span></span>            | <span data-ttu-id="feda9-205">False</span><span class="sxs-lookup"><span data-stu-id="feda9-205">False</span></span>                                        |
| <span data-ttu-id="feda9-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="feda9-206">Is-Single-Valued</span></span>       | <span data-ttu-id="feda9-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="feda9-207">True</span></span>                                         |
| <span data-ttu-id="feda9-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="feda9-208">Is Indexed</span></span>             | <span data-ttu-id="feda9-209">False</span><span class="sxs-lookup"><span data-stu-id="feda9-209">False</span></span>                                        |
| <span data-ttu-id="feda9-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="feda9-210">In Global Catalog</span></span>      | <span data-ttu-id="feda9-211">False</span><span class="sxs-lookup"><span data-stu-id="feda9-211">False</span></span>                                        |
| <span data-ttu-id="feda9-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="feda9-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="feda9-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="feda9-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="feda9-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="feda9-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="feda9-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="feda9-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="feda9-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="feda9-216">Search-Flags</span></span>           | <span data-ttu-id="feda9-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="feda9-217">0x00000000</span></span>                                   |
| <span data-ttu-id="feda9-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="feda9-218">System-Flags</span></span>           | <span data-ttu-id="feda9-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="feda9-219">0x00000010</span></span>                                   |
| <span data-ttu-id="feda9-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="feda9-220">Classes used in</span></span>        | [<span data-ttu-id="feda9-221">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="feda9-221">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="feda9-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="feda9-222">Windows Server 2012</span></span>



| <span data-ttu-id="feda9-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="feda9-223">Entry</span></span> | <span data-ttu-id="feda9-224">Wert</span><span class="sxs-lookup"><span data-stu-id="feda9-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="feda9-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="feda9-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="feda9-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="feda9-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="feda9-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="feda9-227">System-Only</span></span>            | <span data-ttu-id="feda9-228">False</span><span class="sxs-lookup"><span data-stu-id="feda9-228">False</span></span>                                        |
| <span data-ttu-id="feda9-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="feda9-229">Is-Single-Valued</span></span>       | <span data-ttu-id="feda9-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="feda9-230">True</span></span>                                         |
| <span data-ttu-id="feda9-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="feda9-231">Is Indexed</span></span>             | <span data-ttu-id="feda9-232">False</span><span class="sxs-lookup"><span data-stu-id="feda9-232">False</span></span>                                        |
| <span data-ttu-id="feda9-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="feda9-233">In Global Catalog</span></span>      | <span data-ttu-id="feda9-234">False</span><span class="sxs-lookup"><span data-stu-id="feda9-234">False</span></span>                                        |
| <span data-ttu-id="feda9-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="feda9-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="feda9-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="feda9-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="feda9-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="feda9-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="feda9-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="feda9-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="feda9-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="feda9-239">Search-Flags</span></span>           | <span data-ttu-id="feda9-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="feda9-240">0x00000000</span></span>                                   |
| <span data-ttu-id="feda9-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="feda9-241">System-Flags</span></span>           | <span data-ttu-id="feda9-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="feda9-242">0x00000010</span></span>                                   |
| <span data-ttu-id="feda9-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="feda9-243">Classes used in</span></span>        | [<span data-ttu-id="feda9-244">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="feda9-244">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





