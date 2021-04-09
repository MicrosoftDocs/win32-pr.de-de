---
title: MS-PKI-Registrierungsflag-Attribut
description: Enthält die Registrierungs bezogenen Flags.
ms.assetid: e854acb1-75f4-4379-b404-8fa096419ee6
ms.tgt_platform: multiple
keywords:
- 'MS-PKI-Registrierungsflag: AD-Schema'
- 'mspki-Registrierungsflag: AD-Schema für Attribut'
topic_type:
- apiref
api_name:
- ms-PKI-Enrollment-Flag
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2df092e28633bd5825c422e306bf7a65982b32a8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957488"
---
# <a name="ms-pki-enrollment-flag-attribute"></a><span data-ttu-id="61ba9-105">MS-PKI-Registrierungsflag-Attribut</span><span class="sxs-lookup"><span data-stu-id="61ba9-105">ms-PKI-Enrollment-Flag attribute</span></span>

<span data-ttu-id="61ba9-106">Enthält die Registrierungs bezogenen Flags.</span><span class="sxs-lookup"><span data-stu-id="61ba9-106">Contains the enrollment related flags.</span></span>



| <span data-ttu-id="61ba9-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="61ba9-107">Entry</span></span> | <span data-ttu-id="61ba9-108">Wert</span><span class="sxs-lookup"><span data-stu-id="61ba9-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61ba9-109">CN</span><span class="sxs-lookup"><span data-stu-id="61ba9-109">CN</span></span>                | <span data-ttu-id="61ba9-110">MS-PKI-Registrierungsflag</span><span class="sxs-lookup"><span data-stu-id="61ba9-110">ms-PKI-Enrollment-Flag</span></span>                                                                            |
| <span data-ttu-id="61ba9-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="61ba9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="61ba9-112">mspki-Registrierungsflag</span><span class="sxs-lookup"><span data-stu-id="61ba9-112">msPKI-Enrollment-Flag</span></span>                                                                             |
| <span data-ttu-id="61ba9-113">Size</span><span class="sxs-lookup"><span data-stu-id="61ba9-113">Size</span></span>              | <span data-ttu-id="61ba9-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="61ba9-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="61ba9-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="61ba9-115">Update Privilege</span></span>  | <span data-ttu-id="61ba9-116">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="61ba9-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="61ba9-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="61ba9-117">Update Frequency</span></span>  | <span data-ttu-id="61ba9-118">Wenn das Objekt Vorlage (MS-PKI-Certificate-template) bearbeitet, erstellt oder geklont wird.</span><span class="sxs-lookup"><span data-stu-id="61ba9-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="61ba9-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="61ba9-119">Attribute-Id</span></span>      | <span data-ttu-id="61ba9-120">1.2.840.113556.1.4.1430</span><span class="sxs-lookup"><span data-stu-id="61ba9-120">1.2.840.113556.1.4.1430</span></span>                                                                           |
| <span data-ttu-id="61ba9-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="61ba9-121">System-Id-Guid</span></span>    | <span data-ttu-id="61ba9-122">d15ef7d8-f226-46db-ae79-b34e560bd12c</span><span class="sxs-lookup"><span data-stu-id="61ba9-122">d15ef7d8-f226-46db-ae79-b34e560bd12c</span></span>                                                              |
| <span data-ttu-id="61ba9-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="61ba9-123">Syntax</span></span>            | [<span data-ttu-id="61ba9-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="61ba9-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="61ba9-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="61ba9-125">Implementations</span></span>

-   [<span data-ttu-id="61ba9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="61ba9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="61ba9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="61ba9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="61ba9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="61ba9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="61ba9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="61ba9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="61ba9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="61ba9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="61ba9-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="61ba9-131">Windows Server 2003</span></span>



| <span data-ttu-id="61ba9-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="61ba9-132">Entry</span></span> | <span data-ttu-id="61ba9-133">Wert</span><span class="sxs-lookup"><span data-stu-id="61ba9-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="61ba9-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="61ba9-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="61ba9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ba9-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="61ba9-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ba9-136">System-Only</span></span>            | <span data-ttu-id="61ba9-137">False</span><span class="sxs-lookup"><span data-stu-id="61ba9-137">False</span></span>                                                                   |
| <span data-ttu-id="61ba9-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="61ba9-138">Is-Single-Valued</span></span>       | <span data-ttu-id="61ba9-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="61ba9-139">True</span></span>                                                                    |
| <span data-ttu-id="61ba9-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="61ba9-140">Is Indexed</span></span>             | <span data-ttu-id="61ba9-141">False</span><span class="sxs-lookup"><span data-stu-id="61ba9-141">False</span></span>                                                                   |
| <span data-ttu-id="61ba9-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="61ba9-142">In Global Catalog</span></span>      | <span data-ttu-id="61ba9-143">False</span><span class="sxs-lookup"><span data-stu-id="61ba9-143">False</span></span>                                                                   |
| <span data-ttu-id="61ba9-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="61ba9-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ba9-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="61ba9-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="61ba9-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ba9-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="61ba9-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ba9-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="61ba9-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba9-148">Search-Flags</span></span>           | <span data-ttu-id="61ba9-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ba9-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="61ba9-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba9-150">System-Flags</span></span>           | <span data-ttu-id="61ba9-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61ba9-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="61ba9-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="61ba9-152">Classes used in</span></span>        | [<span data-ttu-id="61ba9-153">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="61ba9-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="61ba9-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="61ba9-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="61ba9-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="61ba9-155">Entry</span></span> | <span data-ttu-id="61ba9-156">Wert</span><span class="sxs-lookup"><span data-stu-id="61ba9-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="61ba9-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="61ba9-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="61ba9-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ba9-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="61ba9-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ba9-159">System-Only</span></span>            | <span data-ttu-id="61ba9-160">False</span><span class="sxs-lookup"><span data-stu-id="61ba9-160">False</span></span>                                                                   |
| <span data-ttu-id="61ba9-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="61ba9-161">Is-Single-Valued</span></span>       | <span data-ttu-id="61ba9-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="61ba9-162">True</span></span>                                                                    |
| <span data-ttu-id="61ba9-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="61ba9-163">Is Indexed</span></span>             | <span data-ttu-id="61ba9-164">False</span><span class="sxs-lookup"><span data-stu-id="61ba9-164">False</span></span>                                                                   |
| <span data-ttu-id="61ba9-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="61ba9-165">In Global Catalog</span></span>      | <span data-ttu-id="61ba9-166">False</span><span class="sxs-lookup"><span data-stu-id="61ba9-166">False</span></span>                                                                   |
| <span data-ttu-id="61ba9-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="61ba9-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ba9-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="61ba9-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="61ba9-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ba9-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="61ba9-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ba9-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="61ba9-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba9-171">Search-Flags</span></span>           | <span data-ttu-id="61ba9-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ba9-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="61ba9-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba9-173">System-Flags</span></span>           | <span data-ttu-id="61ba9-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61ba9-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="61ba9-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="61ba9-175">Classes used in</span></span>        | [<span data-ttu-id="61ba9-176">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="61ba9-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="61ba9-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61ba9-177">Windows Server 2008</span></span>



| <span data-ttu-id="61ba9-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="61ba9-178">Entry</span></span> | <span data-ttu-id="61ba9-179">Wert</span><span class="sxs-lookup"><span data-stu-id="61ba9-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="61ba9-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="61ba9-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="61ba9-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ba9-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="61ba9-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ba9-182">System-Only</span></span>            | <span data-ttu-id="61ba9-183">False</span><span class="sxs-lookup"><span data-stu-id="61ba9-183">False</span></span>                                                                   |
| <span data-ttu-id="61ba9-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="61ba9-184">Is-Single-Valued</span></span>       | <span data-ttu-id="61ba9-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="61ba9-185">True</span></span>                                                                    |
| <span data-ttu-id="61ba9-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="61ba9-186">Is Indexed</span></span>             | <span data-ttu-id="61ba9-187">False</span><span class="sxs-lookup"><span data-stu-id="61ba9-187">False</span></span>                                                                   |
| <span data-ttu-id="61ba9-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="61ba9-188">In Global Catalog</span></span>      | <span data-ttu-id="61ba9-189">False</span><span class="sxs-lookup"><span data-stu-id="61ba9-189">False</span></span>                                                                   |
| <span data-ttu-id="61ba9-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="61ba9-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ba9-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="61ba9-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="61ba9-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ba9-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="61ba9-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ba9-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="61ba9-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba9-194">Search-Flags</span></span>           | <span data-ttu-id="61ba9-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ba9-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="61ba9-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba9-196">System-Flags</span></span>           | <span data-ttu-id="61ba9-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61ba9-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="61ba9-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="61ba9-198">Classes used in</span></span>        | [<span data-ttu-id="61ba9-199">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="61ba9-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="61ba9-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="61ba9-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="61ba9-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="61ba9-201">Entry</span></span> | <span data-ttu-id="61ba9-202">Wert</span><span class="sxs-lookup"><span data-stu-id="61ba9-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="61ba9-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="61ba9-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="61ba9-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ba9-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="61ba9-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ba9-205">System-Only</span></span>            | <span data-ttu-id="61ba9-206">False</span><span class="sxs-lookup"><span data-stu-id="61ba9-206">False</span></span>                                                                   |
| <span data-ttu-id="61ba9-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="61ba9-207">Is-Single-Valued</span></span>       | <span data-ttu-id="61ba9-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="61ba9-208">True</span></span>                                                                    |
| <span data-ttu-id="61ba9-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="61ba9-209">Is Indexed</span></span>             | <span data-ttu-id="61ba9-210">False</span><span class="sxs-lookup"><span data-stu-id="61ba9-210">False</span></span>                                                                   |
| <span data-ttu-id="61ba9-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="61ba9-211">In Global Catalog</span></span>      | <span data-ttu-id="61ba9-212">False</span><span class="sxs-lookup"><span data-stu-id="61ba9-212">False</span></span>                                                                   |
| <span data-ttu-id="61ba9-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="61ba9-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ba9-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="61ba9-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="61ba9-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ba9-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="61ba9-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ba9-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="61ba9-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba9-217">Search-Flags</span></span>           | <span data-ttu-id="61ba9-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ba9-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="61ba9-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba9-219">System-Flags</span></span>           | <span data-ttu-id="61ba9-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61ba9-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="61ba9-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="61ba9-221">Classes used in</span></span>        | [<span data-ttu-id="61ba9-222">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="61ba9-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="61ba9-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61ba9-223">Windows Server 2012</span></span>



| <span data-ttu-id="61ba9-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="61ba9-224">Entry</span></span> | <span data-ttu-id="61ba9-225">Wert</span><span class="sxs-lookup"><span data-stu-id="61ba9-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="61ba9-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="61ba9-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="61ba9-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ba9-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="61ba9-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ba9-228">System-Only</span></span>            | <span data-ttu-id="61ba9-229">False</span><span class="sxs-lookup"><span data-stu-id="61ba9-229">False</span></span>                                                                   |
| <span data-ttu-id="61ba9-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="61ba9-230">Is-Single-Valued</span></span>       | <span data-ttu-id="61ba9-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="61ba9-231">True</span></span>                                                                    |
| <span data-ttu-id="61ba9-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="61ba9-232">Is Indexed</span></span>             | <span data-ttu-id="61ba9-233">False</span><span class="sxs-lookup"><span data-stu-id="61ba9-233">False</span></span>                                                                   |
| <span data-ttu-id="61ba9-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="61ba9-234">In Global Catalog</span></span>      | <span data-ttu-id="61ba9-235">False</span><span class="sxs-lookup"><span data-stu-id="61ba9-235">False</span></span>                                                                   |
| <span data-ttu-id="61ba9-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="61ba9-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ba9-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="61ba9-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="61ba9-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ba9-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="61ba9-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ba9-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="61ba9-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba9-240">Search-Flags</span></span>           | <span data-ttu-id="61ba9-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ba9-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="61ba9-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba9-242">System-Flags</span></span>           | <span data-ttu-id="61ba9-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61ba9-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="61ba9-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="61ba9-244">Classes used in</span></span>        | [<span data-ttu-id="61ba9-245">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="61ba9-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





