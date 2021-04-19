---
title: MS-PKI-OID-User-Notice-Attribut
description: Die Benutzer Benachrichtigung für die Richtlinien-OID der Unternehmens Aussteller.
ms.assetid: b7cfc5fd-99d8-4ddd-bc8f-5e5505eb1f1b
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-PKI-OID-User-Notice-Attribut
- mspki-OID-User-Notice-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-PKI-OID-User-Notice
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115a40f39dc9d6eb8e033435d2803a658edcaacf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106343105"
---
# <a name="ms-pki-oid-user-notice-attribute"></a><span data-ttu-id="38e52-105">MS-PKI-OID-User-Notice-Attribut</span><span class="sxs-lookup"><span data-stu-id="38e52-105">ms-PKI-OID-User-Notice attribute</span></span>

<span data-ttu-id="38e52-106">Die Benutzer Benachrichtigung für die Richtlinien-OID der Unternehmens Aussteller.</span><span class="sxs-lookup"><span data-stu-id="38e52-106">The user notice for the enterprise issuer policy OID.</span></span>



| <span data-ttu-id="38e52-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38e52-107">Entry</span></span> | <span data-ttu-id="38e52-108">Wert</span><span class="sxs-lookup"><span data-stu-id="38e52-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="38e52-109">CN</span><span class="sxs-lookup"><span data-stu-id="38e52-109">CN</span></span>                | <span data-ttu-id="38e52-110">MS-PKI-OID-Benutzer Hinweis</span><span class="sxs-lookup"><span data-stu-id="38e52-110">ms-PKI-OID-User-Notice</span></span>                                                                     |
| <span data-ttu-id="38e52-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="38e52-111">Ldap-Display-Name</span></span> | <span data-ttu-id="38e52-112">mspki-OID-Benutzer Hinweis</span><span class="sxs-lookup"><span data-stu-id="38e52-112">msPKI-OID-User-Notice</span></span>                                                                      |
| <span data-ttu-id="38e52-113">Size</span><span class="sxs-lookup"><span data-stu-id="38e52-113">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="38e52-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="38e52-114">Update Privilege</span></span>  | <span data-ttu-id="38e52-115">Unternehmensadministrator</span><span class="sxs-lookup"><span data-stu-id="38e52-115">Enterprise administrator</span></span>                                                                   |
| <span data-ttu-id="38e52-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="38e52-116">Update Frequency</span></span>  | <span data-ttu-id="38e52-117">Wenn eine neue Vorlage erstellt wird oder die Attribute vorhandener Vorlagen bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="38e52-117">Whenever a new template is created, or the attributes of an existing templates are edited.</span></span> |
| <span data-ttu-id="38e52-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="38e52-118">Attribute-Id</span></span>      | <span data-ttu-id="38e52-119">1.2.840.113556.1.4.1673</span><span class="sxs-lookup"><span data-stu-id="38e52-119">1.2.840.113556.1.4.1673</span></span>                                                                    |
| <span data-ttu-id="38e52-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="38e52-120">System-Id-Guid</span></span>    | <span data-ttu-id="38e52-121">04c4da7a-e114-4E69-88de-e293f 2d3b395</span><span class="sxs-lookup"><span data-stu-id="38e52-121">04c4da7a-e114-4e69-88de-e293f2d3b395</span></span>                                                       |
| <span data-ttu-id="38e52-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="38e52-122">Syntax</span></span>            | [<span data-ttu-id="38e52-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="38e52-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="38e52-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="38e52-124">Implementations</span></span>

-   [<span data-ttu-id="38e52-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="38e52-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="38e52-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="38e52-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="38e52-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="38e52-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="38e52-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="38e52-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="38e52-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="38e52-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="38e52-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="38e52-130">Windows Server 2003</span></span>



| <span data-ttu-id="38e52-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38e52-131">Entry</span></span> | <span data-ttu-id="38e52-132">Wert</span><span class="sxs-lookup"><span data-stu-id="38e52-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="38e52-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38e52-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="38e52-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38e52-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="38e52-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="38e52-135">System-Only</span></span>            | <span data-ttu-id="38e52-136">False</span><span class="sxs-lookup"><span data-stu-id="38e52-136">False</span></span>                                                              |
| <span data-ttu-id="38e52-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38e52-137">Is-Single-Valued</span></span>       | <span data-ttu-id="38e52-138">False</span><span class="sxs-lookup"><span data-stu-id="38e52-138">False</span></span>                                                              |
| <span data-ttu-id="38e52-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38e52-139">Is Indexed</span></span>             | <span data-ttu-id="38e52-140">False</span><span class="sxs-lookup"><span data-stu-id="38e52-140">False</span></span>                                                              |
| <span data-ttu-id="38e52-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38e52-141">In Global Catalog</span></span>      | <span data-ttu-id="38e52-142">False</span><span class="sxs-lookup"><span data-stu-id="38e52-142">False</span></span>                                                              |
| <span data-ttu-id="38e52-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38e52-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="38e52-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38e52-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="38e52-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38e52-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="38e52-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38e52-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="38e52-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38e52-147">Search-Flags</span></span>           | <span data-ttu-id="38e52-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38e52-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="38e52-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38e52-149">System-Flags</span></span>           | <span data-ttu-id="38e52-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38e52-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="38e52-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38e52-151">Classes used in</span></span>        | [<span data-ttu-id="38e52-152">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="38e52-152">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="38e52-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="38e52-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="38e52-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38e52-154">Entry</span></span> | <span data-ttu-id="38e52-155">Wert</span><span class="sxs-lookup"><span data-stu-id="38e52-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="38e52-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38e52-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="38e52-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38e52-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="38e52-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="38e52-158">System-Only</span></span>            | <span data-ttu-id="38e52-159">False</span><span class="sxs-lookup"><span data-stu-id="38e52-159">False</span></span>                                                              |
| <span data-ttu-id="38e52-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38e52-160">Is-Single-Valued</span></span>       | <span data-ttu-id="38e52-161">False</span><span class="sxs-lookup"><span data-stu-id="38e52-161">False</span></span>                                                              |
| <span data-ttu-id="38e52-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38e52-162">Is Indexed</span></span>             | <span data-ttu-id="38e52-163">False</span><span class="sxs-lookup"><span data-stu-id="38e52-163">False</span></span>                                                              |
| <span data-ttu-id="38e52-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38e52-164">In Global Catalog</span></span>      | <span data-ttu-id="38e52-165">False</span><span class="sxs-lookup"><span data-stu-id="38e52-165">False</span></span>                                                              |
| <span data-ttu-id="38e52-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38e52-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="38e52-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38e52-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="38e52-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38e52-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="38e52-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38e52-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="38e52-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38e52-170">Search-Flags</span></span>           | <span data-ttu-id="38e52-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38e52-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="38e52-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38e52-172">System-Flags</span></span>           | <span data-ttu-id="38e52-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38e52-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="38e52-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38e52-174">Classes used in</span></span>        | [<span data-ttu-id="38e52-175">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="38e52-175">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="38e52-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38e52-176">Windows Server 2008</span></span>



| <span data-ttu-id="38e52-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38e52-177">Entry</span></span> | <span data-ttu-id="38e52-178">Wert</span><span class="sxs-lookup"><span data-stu-id="38e52-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="38e52-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38e52-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="38e52-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38e52-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="38e52-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="38e52-181">System-Only</span></span>            | <span data-ttu-id="38e52-182">False</span><span class="sxs-lookup"><span data-stu-id="38e52-182">False</span></span>                                                              |
| <span data-ttu-id="38e52-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38e52-183">Is-Single-Valued</span></span>       | <span data-ttu-id="38e52-184">False</span><span class="sxs-lookup"><span data-stu-id="38e52-184">False</span></span>                                                              |
| <span data-ttu-id="38e52-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38e52-185">Is Indexed</span></span>             | <span data-ttu-id="38e52-186">False</span><span class="sxs-lookup"><span data-stu-id="38e52-186">False</span></span>                                                              |
| <span data-ttu-id="38e52-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38e52-187">In Global Catalog</span></span>      | <span data-ttu-id="38e52-188">False</span><span class="sxs-lookup"><span data-stu-id="38e52-188">False</span></span>                                                              |
| <span data-ttu-id="38e52-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38e52-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="38e52-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38e52-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="38e52-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38e52-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="38e52-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38e52-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="38e52-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38e52-193">Search-Flags</span></span>           | <span data-ttu-id="38e52-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38e52-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="38e52-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38e52-195">System-Flags</span></span>           | <span data-ttu-id="38e52-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38e52-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="38e52-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38e52-197">Classes used in</span></span>        | [<span data-ttu-id="38e52-198">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="38e52-198">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="38e52-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="38e52-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="38e52-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38e52-200">Entry</span></span> | <span data-ttu-id="38e52-201">Wert</span><span class="sxs-lookup"><span data-stu-id="38e52-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="38e52-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38e52-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="38e52-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38e52-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="38e52-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="38e52-204">System-Only</span></span>            | <span data-ttu-id="38e52-205">False</span><span class="sxs-lookup"><span data-stu-id="38e52-205">False</span></span>                                                              |
| <span data-ttu-id="38e52-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38e52-206">Is-Single-Valued</span></span>       | <span data-ttu-id="38e52-207">False</span><span class="sxs-lookup"><span data-stu-id="38e52-207">False</span></span>                                                              |
| <span data-ttu-id="38e52-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38e52-208">Is Indexed</span></span>             | <span data-ttu-id="38e52-209">False</span><span class="sxs-lookup"><span data-stu-id="38e52-209">False</span></span>                                                              |
| <span data-ttu-id="38e52-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38e52-210">In Global Catalog</span></span>      | <span data-ttu-id="38e52-211">False</span><span class="sxs-lookup"><span data-stu-id="38e52-211">False</span></span>                                                              |
| <span data-ttu-id="38e52-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38e52-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="38e52-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38e52-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="38e52-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38e52-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="38e52-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38e52-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="38e52-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38e52-216">Search-Flags</span></span>           | <span data-ttu-id="38e52-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38e52-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="38e52-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38e52-218">System-Flags</span></span>           | <span data-ttu-id="38e52-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38e52-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="38e52-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38e52-220">Classes used in</span></span>        | [<span data-ttu-id="38e52-221">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="38e52-221">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="38e52-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38e52-222">Windows Server 2012</span></span>



| <span data-ttu-id="38e52-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38e52-223">Entry</span></span> | <span data-ttu-id="38e52-224">Wert</span><span class="sxs-lookup"><span data-stu-id="38e52-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="38e52-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38e52-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="38e52-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38e52-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="38e52-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="38e52-227">System-Only</span></span>            | <span data-ttu-id="38e52-228">False</span><span class="sxs-lookup"><span data-stu-id="38e52-228">False</span></span>                                                              |
| <span data-ttu-id="38e52-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="38e52-229">Is-Single-Valued</span></span>       | <span data-ttu-id="38e52-230">False</span><span class="sxs-lookup"><span data-stu-id="38e52-230">False</span></span>                                                              |
| <span data-ttu-id="38e52-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38e52-231">Is Indexed</span></span>             | <span data-ttu-id="38e52-232">False</span><span class="sxs-lookup"><span data-stu-id="38e52-232">False</span></span>                                                              |
| <span data-ttu-id="38e52-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38e52-233">In Global Catalog</span></span>      | <span data-ttu-id="38e52-234">False</span><span class="sxs-lookup"><span data-stu-id="38e52-234">False</span></span>                                                              |
| <span data-ttu-id="38e52-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38e52-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="38e52-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="38e52-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="38e52-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38e52-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="38e52-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38e52-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="38e52-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38e52-239">Search-Flags</span></span>           | <span data-ttu-id="38e52-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38e52-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="38e52-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38e52-241">System-Flags</span></span>           | <span data-ttu-id="38e52-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38e52-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="38e52-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38e52-243">Classes used in</span></span>        | [<span data-ttu-id="38e52-244">**MS-PKI-Enterprise-OID**</span><span class="sxs-lookup"><span data-stu-id="38e52-244">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



 

 





