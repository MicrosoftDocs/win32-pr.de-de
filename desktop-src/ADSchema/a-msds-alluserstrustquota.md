---
title: MS-DS-all-users-Trust-Quota-Attribut
description: Wird verwendet, um ein kombiniertes Benutzer Kontingent für die Gesamtanzahl der Trusted-Domain Objekte zu erzwingen, die mit dem neuen Zugriffsrecht "Create-Inbound-Forest-Trust" erstellt wurden.
ms.assetid: 77e70a26-99b4-4b49-a984-6809d02f6fb8
ms.tgt_platform: multiple
keywords:
- "\"Ms-DS-all-users-Trust-Quota\"-Attribut AD-Schema"
- AD-Schema des msDS-alluserstrustquota-Attributs
topic_type:
- apiref
api_name:
- MS-DS-All-Users-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0538ff38f1eb57f339a8e0e244a378a36dd92498
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103745185"
---
# <a name="ms-ds-all-users-trust-quota-attribute"></a><span data-ttu-id="53dda-105">MS-DS-all-users-Trust-Quota-Attribut</span><span class="sxs-lookup"><span data-stu-id="53dda-105">MS-DS-All-Users-Trust-Quota attribute</span></span>

<span data-ttu-id="53dda-106">Wird verwendet, um ein kombiniertes Benutzer Kontingent für die Gesamtanzahl der Trusted-Domain Objekte zu erzwingen, die mit dem neuen Zugriffsrecht "Create-Inbound-Forest-Trust" erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="53dda-106">Used to enforce a combined users quota on the total number of Trusted-Domain objects created by using the new control access right, Create-Inbound-Forest-Trust.</span></span>



| <span data-ttu-id="53dda-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53dda-107">Entry</span></span> | <span data-ttu-id="53dda-108">Wert</span><span class="sxs-lookup"><span data-stu-id="53dda-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="53dda-109">CN</span><span class="sxs-lookup"><span data-stu-id="53dda-109">CN</span></span>                | <span data-ttu-id="53dda-110">MS-DS-all-users-Trust-Quota</span><span class="sxs-lookup"><span data-stu-id="53dda-110">MS-DS-All-Users-Trust-Quota</span></span>               |
| <span data-ttu-id="53dda-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="53dda-111">Ldap-Display-Name</span></span> | <span data-ttu-id="53dda-112">MSDS-alluserstrustquota</span><span class="sxs-lookup"><span data-stu-id="53dda-112">msDS-AllUsersTrustQuota</span></span>                   |
| <span data-ttu-id="53dda-113">Size</span><span class="sxs-lookup"><span data-stu-id="53dda-113">Size</span></span>              | \-                                        |
| <span data-ttu-id="53dda-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="53dda-114">Update Privilege</span></span>  | <span data-ttu-id="53dda-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="53dda-115">Domain administrator</span></span>                      |
| <span data-ttu-id="53dda-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="53dda-116">Update Frequency</span></span>  | <span data-ttu-id="53dda-117">Bei der Gesamtstruktur Erstellung und selten danach.</span><span class="sxs-lookup"><span data-stu-id="53dda-117">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="53dda-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="53dda-118">Attribute-Id</span></span>      | <span data-ttu-id="53dda-119">1.2.840.113556.1.4.1789</span><span class="sxs-lookup"><span data-stu-id="53dda-119">1.2.840.113556.1.4.1789</span></span>                   |
| <span data-ttu-id="53dda-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="53dda-120">System-Id-Guid</span></span>    | <span data-ttu-id="53dda-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span><span class="sxs-lookup"><span data-stu-id="53dda-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span></span>      |
| <span data-ttu-id="53dda-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="53dda-122">Syntax</span></span>            | [<span data-ttu-id="53dda-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="53dda-123">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="53dda-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="53dda-124">Implementations</span></span>

-   [<span data-ttu-id="53dda-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="53dda-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="53dda-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="53dda-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="53dda-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="53dda-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="53dda-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="53dda-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="53dda-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="53dda-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="53dda-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="53dda-130">Windows Server 2003</span></span>



| <span data-ttu-id="53dda-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53dda-131">Entry</span></span> | <span data-ttu-id="53dda-132">Wert</span><span class="sxs-lookup"><span data-stu-id="53dda-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="53dda-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53dda-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="53dda-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53dda-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="53dda-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="53dda-135">System-Only</span></span>            | <span data-ttu-id="53dda-136">False</span><span class="sxs-lookup"><span data-stu-id="53dda-136">False</span></span>                                        |
| <span data-ttu-id="53dda-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53dda-137">Is-Single-Valued</span></span>       | <span data-ttu-id="53dda-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="53dda-138">True</span></span>                                         |
| <span data-ttu-id="53dda-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53dda-139">Is Indexed</span></span>             | <span data-ttu-id="53dda-140">False</span><span class="sxs-lookup"><span data-stu-id="53dda-140">False</span></span>                                        |
| <span data-ttu-id="53dda-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53dda-141">In Global Catalog</span></span>      | <span data-ttu-id="53dda-142">False</span><span class="sxs-lookup"><span data-stu-id="53dda-142">False</span></span>                                        |
| <span data-ttu-id="53dda-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53dda-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="53dda-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53dda-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="53dda-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53dda-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="53dda-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53dda-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="53dda-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53dda-147">Search-Flags</span></span>           | <span data-ttu-id="53dda-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53dda-148">0x00000000</span></span>                                   |
| <span data-ttu-id="53dda-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53dda-149">System-Flags</span></span>           | <span data-ttu-id="53dda-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53dda-150">0x00000010</span></span>                                   |
| <span data-ttu-id="53dda-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53dda-151">Classes used in</span></span>        | [<span data-ttu-id="53dda-152">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="53dda-152">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="53dda-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="53dda-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="53dda-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53dda-154">Entry</span></span> | <span data-ttu-id="53dda-155">Wert</span><span class="sxs-lookup"><span data-stu-id="53dda-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="53dda-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53dda-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="53dda-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53dda-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="53dda-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="53dda-158">System-Only</span></span>            | <span data-ttu-id="53dda-159">False</span><span class="sxs-lookup"><span data-stu-id="53dda-159">False</span></span>                                        |
| <span data-ttu-id="53dda-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53dda-160">Is-Single-Valued</span></span>       | <span data-ttu-id="53dda-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="53dda-161">True</span></span>                                         |
| <span data-ttu-id="53dda-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53dda-162">Is Indexed</span></span>             | <span data-ttu-id="53dda-163">False</span><span class="sxs-lookup"><span data-stu-id="53dda-163">False</span></span>                                        |
| <span data-ttu-id="53dda-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53dda-164">In Global Catalog</span></span>      | <span data-ttu-id="53dda-165">False</span><span class="sxs-lookup"><span data-stu-id="53dda-165">False</span></span>                                        |
| <span data-ttu-id="53dda-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53dda-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="53dda-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53dda-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="53dda-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53dda-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="53dda-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53dda-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="53dda-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53dda-170">Search-Flags</span></span>           | <span data-ttu-id="53dda-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53dda-171">0x00000000</span></span>                                   |
| <span data-ttu-id="53dda-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53dda-172">System-Flags</span></span>           | <span data-ttu-id="53dda-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53dda-173">0x00000010</span></span>                                   |
| <span data-ttu-id="53dda-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53dda-174">Classes used in</span></span>        | [<span data-ttu-id="53dda-175">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="53dda-175">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="53dda-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53dda-176">Windows Server 2008</span></span>



| <span data-ttu-id="53dda-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53dda-177">Entry</span></span> | <span data-ttu-id="53dda-178">Wert</span><span class="sxs-lookup"><span data-stu-id="53dda-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="53dda-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53dda-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="53dda-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53dda-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="53dda-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="53dda-181">System-Only</span></span>            | <span data-ttu-id="53dda-182">False</span><span class="sxs-lookup"><span data-stu-id="53dda-182">False</span></span>                                        |
| <span data-ttu-id="53dda-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53dda-183">Is-Single-Valued</span></span>       | <span data-ttu-id="53dda-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="53dda-184">True</span></span>                                         |
| <span data-ttu-id="53dda-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53dda-185">Is Indexed</span></span>             | <span data-ttu-id="53dda-186">False</span><span class="sxs-lookup"><span data-stu-id="53dda-186">False</span></span>                                        |
| <span data-ttu-id="53dda-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53dda-187">In Global Catalog</span></span>      | <span data-ttu-id="53dda-188">False</span><span class="sxs-lookup"><span data-stu-id="53dda-188">False</span></span>                                        |
| <span data-ttu-id="53dda-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53dda-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="53dda-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53dda-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="53dda-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53dda-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="53dda-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53dda-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="53dda-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53dda-193">Search-Flags</span></span>           | <span data-ttu-id="53dda-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53dda-194">0x00000000</span></span>                                   |
| <span data-ttu-id="53dda-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53dda-195">System-Flags</span></span>           | <span data-ttu-id="53dda-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53dda-196">0x00000010</span></span>                                   |
| <span data-ttu-id="53dda-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53dda-197">Classes used in</span></span>        | [<span data-ttu-id="53dda-198">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="53dda-198">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="53dda-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="53dda-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="53dda-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53dda-200">Entry</span></span> | <span data-ttu-id="53dda-201">Wert</span><span class="sxs-lookup"><span data-stu-id="53dda-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="53dda-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53dda-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="53dda-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53dda-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="53dda-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="53dda-204">System-Only</span></span>            | <span data-ttu-id="53dda-205">False</span><span class="sxs-lookup"><span data-stu-id="53dda-205">False</span></span>                                        |
| <span data-ttu-id="53dda-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53dda-206">Is-Single-Valued</span></span>       | <span data-ttu-id="53dda-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="53dda-207">True</span></span>                                         |
| <span data-ttu-id="53dda-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53dda-208">Is Indexed</span></span>             | <span data-ttu-id="53dda-209">False</span><span class="sxs-lookup"><span data-stu-id="53dda-209">False</span></span>                                        |
| <span data-ttu-id="53dda-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53dda-210">In Global Catalog</span></span>      | <span data-ttu-id="53dda-211">False</span><span class="sxs-lookup"><span data-stu-id="53dda-211">False</span></span>                                        |
| <span data-ttu-id="53dda-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53dda-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="53dda-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53dda-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="53dda-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53dda-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="53dda-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53dda-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="53dda-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53dda-216">Search-Flags</span></span>           | <span data-ttu-id="53dda-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53dda-217">0x00000000</span></span>                                   |
| <span data-ttu-id="53dda-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53dda-218">System-Flags</span></span>           | <span data-ttu-id="53dda-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53dda-219">0x00000010</span></span>                                   |
| <span data-ttu-id="53dda-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53dda-220">Classes used in</span></span>        | [<span data-ttu-id="53dda-221">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="53dda-221">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="53dda-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53dda-222">Windows Server 2012</span></span>



| <span data-ttu-id="53dda-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53dda-223">Entry</span></span> | <span data-ttu-id="53dda-224">Wert</span><span class="sxs-lookup"><span data-stu-id="53dda-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="53dda-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53dda-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="53dda-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53dda-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="53dda-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="53dda-227">System-Only</span></span>            | <span data-ttu-id="53dda-228">False</span><span class="sxs-lookup"><span data-stu-id="53dda-228">False</span></span>                                        |
| <span data-ttu-id="53dda-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53dda-229">Is-Single-Valued</span></span>       | <span data-ttu-id="53dda-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="53dda-230">True</span></span>                                         |
| <span data-ttu-id="53dda-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53dda-231">Is Indexed</span></span>             | <span data-ttu-id="53dda-232">False</span><span class="sxs-lookup"><span data-stu-id="53dda-232">False</span></span>                                        |
| <span data-ttu-id="53dda-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53dda-233">In Global Catalog</span></span>      | <span data-ttu-id="53dda-234">False</span><span class="sxs-lookup"><span data-stu-id="53dda-234">False</span></span>                                        |
| <span data-ttu-id="53dda-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53dda-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="53dda-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53dda-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="53dda-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53dda-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="53dda-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53dda-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="53dda-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53dda-239">Search-Flags</span></span>           | <span data-ttu-id="53dda-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53dda-240">0x00000000</span></span>                                   |
| <span data-ttu-id="53dda-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53dda-241">System-Flags</span></span>           | <span data-ttu-id="53dda-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53dda-242">0x00000010</span></span>                                   |
| <span data-ttu-id="53dda-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53dda-243">Classes used in</span></span>        | [<span data-ttu-id="53dda-244">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="53dda-244">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





