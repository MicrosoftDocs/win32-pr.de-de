---
title: MS-PKI-OID-CPS-Attribut
description: Die CPS (Certificate Policy-Anweisung) für die Richtlinien-OID des Unternehmens.
ms.assetid: 94c5115e-a8d2-49d1-9fd2-f362e95550dc
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-PKI-OID-CPS-Attribut
- AD-Schema für das mspki-OID-CPS-Attribut
topic_type:
- apiref
api_name:
- ms-PKI-OID-CPS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 218fc0eabe7311f46dba769f84b972a495138d3a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859640"
---
# <a name="ms-pki-oid-cps-attribute"></a><span data-ttu-id="ce438-105">MS-PKI-OID-CPS-Attribut</span><span class="sxs-lookup"><span data-stu-id="ce438-105">ms-PKI-OID-CPS attribute</span></span>

<span data-ttu-id="ce438-106">Die CPS (Certificate Policy-Anweisung) für die Richtlinien-OID des Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="ce438-106">The CPS (Certificate Policy Statement) for the enterprise issuer policy OID.</span></span>



| <span data-ttu-id="ce438-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ce438-107">Entry</span></span> | <span data-ttu-id="ce438-108">Wert</span><span class="sxs-lookup"><span data-stu-id="ce438-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce438-109">CN</span><span class="sxs-lookup"><span data-stu-id="ce438-109">CN</span></span>                | <span data-ttu-id="ce438-110">MS-PKI-OID-CPS</span><span class="sxs-lookup"><span data-stu-id="ce438-110">ms-PKI-OID-CPS</span></span>                                                                             |
| <span data-ttu-id="ce438-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ce438-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ce438-112">mspki-OID-CPS</span><span class="sxs-lookup"><span data-stu-id="ce438-112">msPKI-OID-CPS</span></span>                                                                              |
| <span data-ttu-id="ce438-113">Size</span><span class="sxs-lookup"><span data-stu-id="ce438-113">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="ce438-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ce438-114">Update Privilege</span></span>  | <span data-ttu-id="ce438-115">Unternehmensadministrator</span><span class="sxs-lookup"><span data-stu-id="ce438-115">Enterprise administrator</span></span>                                                                   |
| <span data-ttu-id="ce438-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="ce438-116">Update Frequency</span></span>  | <span data-ttu-id="ce438-117">Wenn eine neue Vorlage erstellt wird oder die Attribute vorhandener Vorlagen bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ce438-117">Whenever a new template is created, or the attributes of an existing templates are edited.</span></span> |
| <span data-ttu-id="ce438-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ce438-118">Attribute-Id</span></span>      | <span data-ttu-id="ce438-119">1.2.840.113556.1.4.1672</span><span class="sxs-lookup"><span data-stu-id="ce438-119">1.2.840.113556.1.4.1672</span></span>                                                                    |
| <span data-ttu-id="ce438-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ce438-120">System-Id-Guid</span></span>    | <span data-ttu-id="ce438-121">5f49940e-a79f-4a51-bb6f-3d446a54dc6b</span><span class="sxs-lookup"><span data-stu-id="ce438-121">5f49940e-a79f-4a51-bb6f-3d446a54dc6b</span></span>                                                       |
| <span data-ttu-id="ce438-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce438-122">Syntax</span></span>            | [<span data-ttu-id="ce438-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ce438-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="ce438-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ce438-124">Implementations</span></span>

-   [<span data-ttu-id="ce438-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ce438-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ce438-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ce438-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ce438-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ce438-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ce438-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ce438-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ce438-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ce438-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ce438-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ce438-130">Windows Server 2003</span></span>



| <span data-ttu-id="ce438-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ce438-131">Entry</span></span> | <span data-ttu-id="ce438-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ce438-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ce438-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ce438-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ce438-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce438-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ce438-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce438-135">System-Only</span></span>            | <span data-ttu-id="ce438-136">False</span><span class="sxs-lookup"><span data-stu-id="ce438-136">False</span></span>                                                              |
| <span data-ttu-id="ce438-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ce438-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ce438-138">False</span><span class="sxs-lookup"><span data-stu-id="ce438-138">False</span></span>                                                              |
| <span data-ttu-id="ce438-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ce438-139">Is Indexed</span></span>             | <span data-ttu-id="ce438-140">False</span><span class="sxs-lookup"><span data-stu-id="ce438-140">False</span></span>                                                              |
| <span data-ttu-id="ce438-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ce438-141">In Global Catalog</span></span>      | <span data-ttu-id="ce438-142">False</span><span class="sxs-lookup"><span data-stu-id="ce438-142">False</span></span>                                                              |
| <span data-ttu-id="ce438-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ce438-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce438-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ce438-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ce438-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce438-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="ce438-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce438-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="ce438-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce438-147">Search-Flags</span></span>           | <span data-ttu-id="ce438-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce438-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="ce438-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce438-149">System-Flags</span></span>           | <span data-ttu-id="ce438-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce438-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="ce438-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ce438-151">Classes used in</span></span>        | [<span data-ttu-id="ce438-152">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="ce438-152">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ce438-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ce438-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ce438-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ce438-154">Entry</span></span> | <span data-ttu-id="ce438-155">Wert</span><span class="sxs-lookup"><span data-stu-id="ce438-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ce438-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ce438-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ce438-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce438-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ce438-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce438-158">System-Only</span></span>            | <span data-ttu-id="ce438-159">False</span><span class="sxs-lookup"><span data-stu-id="ce438-159">False</span></span>                                                              |
| <span data-ttu-id="ce438-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ce438-160">Is-Single-Valued</span></span>       | <span data-ttu-id="ce438-161">False</span><span class="sxs-lookup"><span data-stu-id="ce438-161">False</span></span>                                                              |
| <span data-ttu-id="ce438-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ce438-162">Is Indexed</span></span>             | <span data-ttu-id="ce438-163">False</span><span class="sxs-lookup"><span data-stu-id="ce438-163">False</span></span>                                                              |
| <span data-ttu-id="ce438-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ce438-164">In Global Catalog</span></span>      | <span data-ttu-id="ce438-165">False</span><span class="sxs-lookup"><span data-stu-id="ce438-165">False</span></span>                                                              |
| <span data-ttu-id="ce438-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ce438-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce438-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ce438-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ce438-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce438-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="ce438-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce438-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="ce438-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce438-170">Search-Flags</span></span>           | <span data-ttu-id="ce438-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce438-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="ce438-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce438-172">System-Flags</span></span>           | <span data-ttu-id="ce438-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce438-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="ce438-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ce438-174">Classes used in</span></span>        | [<span data-ttu-id="ce438-175">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="ce438-175">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ce438-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce438-176">Windows Server 2008</span></span>



| <span data-ttu-id="ce438-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ce438-177">Entry</span></span> | <span data-ttu-id="ce438-178">Wert</span><span class="sxs-lookup"><span data-stu-id="ce438-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ce438-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ce438-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ce438-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce438-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ce438-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce438-181">System-Only</span></span>            | <span data-ttu-id="ce438-182">False</span><span class="sxs-lookup"><span data-stu-id="ce438-182">False</span></span>                                                              |
| <span data-ttu-id="ce438-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ce438-183">Is-Single-Valued</span></span>       | <span data-ttu-id="ce438-184">False</span><span class="sxs-lookup"><span data-stu-id="ce438-184">False</span></span>                                                              |
| <span data-ttu-id="ce438-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ce438-185">Is Indexed</span></span>             | <span data-ttu-id="ce438-186">False</span><span class="sxs-lookup"><span data-stu-id="ce438-186">False</span></span>                                                              |
| <span data-ttu-id="ce438-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ce438-187">In Global Catalog</span></span>      | <span data-ttu-id="ce438-188">False</span><span class="sxs-lookup"><span data-stu-id="ce438-188">False</span></span>                                                              |
| <span data-ttu-id="ce438-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ce438-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce438-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ce438-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ce438-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce438-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="ce438-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce438-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="ce438-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce438-193">Search-Flags</span></span>           | <span data-ttu-id="ce438-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce438-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="ce438-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce438-195">System-Flags</span></span>           | <span data-ttu-id="ce438-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce438-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="ce438-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ce438-197">Classes used in</span></span>        | [<span data-ttu-id="ce438-198">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="ce438-198">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ce438-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ce438-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ce438-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ce438-200">Entry</span></span> | <span data-ttu-id="ce438-201">Wert</span><span class="sxs-lookup"><span data-stu-id="ce438-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ce438-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ce438-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ce438-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce438-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ce438-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce438-204">System-Only</span></span>            | <span data-ttu-id="ce438-205">False</span><span class="sxs-lookup"><span data-stu-id="ce438-205">False</span></span>                                                              |
| <span data-ttu-id="ce438-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ce438-206">Is-Single-Valued</span></span>       | <span data-ttu-id="ce438-207">False</span><span class="sxs-lookup"><span data-stu-id="ce438-207">False</span></span>                                                              |
| <span data-ttu-id="ce438-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ce438-208">Is Indexed</span></span>             | <span data-ttu-id="ce438-209">False</span><span class="sxs-lookup"><span data-stu-id="ce438-209">False</span></span>                                                              |
| <span data-ttu-id="ce438-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ce438-210">In Global Catalog</span></span>      | <span data-ttu-id="ce438-211">False</span><span class="sxs-lookup"><span data-stu-id="ce438-211">False</span></span>                                                              |
| <span data-ttu-id="ce438-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ce438-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce438-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ce438-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ce438-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce438-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="ce438-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce438-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="ce438-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce438-216">Search-Flags</span></span>           | <span data-ttu-id="ce438-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce438-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="ce438-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce438-218">System-Flags</span></span>           | <span data-ttu-id="ce438-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce438-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="ce438-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ce438-220">Classes used in</span></span>        | [<span data-ttu-id="ce438-221">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="ce438-221">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ce438-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ce438-222">Windows Server 2012</span></span>



| <span data-ttu-id="ce438-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ce438-223">Entry</span></span> | <span data-ttu-id="ce438-224">Wert</span><span class="sxs-lookup"><span data-stu-id="ce438-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ce438-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ce438-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ce438-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce438-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ce438-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce438-227">System-Only</span></span>            | <span data-ttu-id="ce438-228">False</span><span class="sxs-lookup"><span data-stu-id="ce438-228">False</span></span>                                                              |
| <span data-ttu-id="ce438-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ce438-229">Is-Single-Valued</span></span>       | <span data-ttu-id="ce438-230">False</span><span class="sxs-lookup"><span data-stu-id="ce438-230">False</span></span>                                                              |
| <span data-ttu-id="ce438-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ce438-231">Is Indexed</span></span>             | <span data-ttu-id="ce438-232">False</span><span class="sxs-lookup"><span data-stu-id="ce438-232">False</span></span>                                                              |
| <span data-ttu-id="ce438-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ce438-233">In Global Catalog</span></span>      | <span data-ttu-id="ce438-234">False</span><span class="sxs-lookup"><span data-stu-id="ce438-234">False</span></span>                                                              |
| <span data-ttu-id="ce438-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ce438-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce438-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ce438-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ce438-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce438-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="ce438-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce438-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="ce438-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce438-239">Search-Flags</span></span>           | <span data-ttu-id="ce438-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce438-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="ce438-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce438-241">System-Flags</span></span>           | <span data-ttu-id="ce438-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce438-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="ce438-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ce438-243">Classes used in</span></span>        | [<span data-ttu-id="ce438-244">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="ce438-244">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



 

 





