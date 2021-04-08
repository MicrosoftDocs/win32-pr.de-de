---
title: MS-PKI-RA-Policies-Attribut
description: Enthält die Liste der erforderlichen Richtlinien-OIDs von Registrierungsstellen, die die Registrierungs Anforderung signieren.
ms.assetid: ebbdf95e-05c8-4b54-b7a5-4bb81d425225
ms.tgt_platform: multiple
keywords:
- MS-PKI-RA-Policies-Attribut AD-Schema
- mspki-RA-Richtlinien-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-PKI-RA-Policies
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b948dac7a95ae8b46972ace4d1ab46260b476da
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957616"
---
# <a name="ms-pki-ra-policies-attribute"></a><span data-ttu-id="e8ffb-105">MS-PKI-RA-Policies-Attribut</span><span class="sxs-lookup"><span data-stu-id="e8ffb-105">ms-PKI-RA-Policies attribute</span></span>

<span data-ttu-id="e8ffb-106">Enthält die Liste der erforderlichen Richtlinien-OIDs von Registrierungsstellen, die die Registrierungs Anforderung signieren.</span><span class="sxs-lookup"><span data-stu-id="e8ffb-106">Contains the list of required policy OIDs from registration authorities who sign the enrollment request.</span></span>



| <span data-ttu-id="e8ffb-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e8ffb-107">Entry</span></span> | <span data-ttu-id="e8ffb-108">Wert</span><span class="sxs-lookup"><span data-stu-id="e8ffb-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8ffb-109">CN</span><span class="sxs-lookup"><span data-stu-id="e8ffb-109">CN</span></span>                | <span data-ttu-id="e8ffb-110">MS-PKI-RA-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="e8ffb-110">ms-PKI-RA-Policies</span></span>                                                                                |
| <span data-ttu-id="e8ffb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e8ffb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e8ffb-112">mspki-RA-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="e8ffb-112">msPKI-RA-Policies</span></span>                                                                                 |
| <span data-ttu-id="e8ffb-113">Size</span><span class="sxs-lookup"><span data-stu-id="e8ffb-113">Size</span></span>              | <span data-ttu-id="e8ffb-114">64 Byte-Mal die Anzahl der Einträge.</span><span class="sxs-lookup"><span data-stu-id="e8ffb-114">64 bytes times the number of entries.</span></span>                                                             |
| <span data-ttu-id="e8ffb-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e8ffb-115">Update Privilege</span></span>  | <span data-ttu-id="e8ffb-116">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="e8ffb-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="e8ffb-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="e8ffb-117">Update Frequency</span></span>  | <span data-ttu-id="e8ffb-118">Wenn das Objekt Vorlage (MS-PKI-Certificate-template) bearbeitet, erstellt oder geklont wird.</span><span class="sxs-lookup"><span data-stu-id="e8ffb-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="e8ffb-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e8ffb-119">Attribute-Id</span></span>      | <span data-ttu-id="e8ffb-120">1.2.840.113556.1.4.1438</span><span class="sxs-lookup"><span data-stu-id="e8ffb-120">1.2.840.113556.1.4.1438</span></span>                                                                           |
| <span data-ttu-id="e8ffb-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e8ffb-121">System-Id-Guid</span></span>    | <span data-ttu-id="e8ffb-122">d546ae22-0951-4d47-817e-1c9f96faad46</span><span class="sxs-lookup"><span data-stu-id="e8ffb-122">d546ae22-0951-4d47-817e-1c9f96faad46</span></span>                                                              |
| <span data-ttu-id="e8ffb-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8ffb-123">Syntax</span></span>            | [<span data-ttu-id="e8ffb-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e8ffb-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="e8ffb-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="e8ffb-125">Implementations</span></span>

-   [<span data-ttu-id="e8ffb-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e8ffb-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e8ffb-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e8ffb-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e8ffb-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e8ffb-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e8ffb-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e8ffb-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e8ffb-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e8ffb-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e8ffb-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e8ffb-131">Windows Server 2003</span></span>



| <span data-ttu-id="e8ffb-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e8ffb-132">Entry</span></span> | <span data-ttu-id="e8ffb-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e8ffb-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e8ffb-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e8ffb-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e8ffb-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8ffb-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e8ffb-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8ffb-136">System-Only</span></span>            | <span data-ttu-id="e8ffb-137">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-137">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e8ffb-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e8ffb-139">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-139">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e8ffb-140">Is Indexed</span></span>             | <span data-ttu-id="e8ffb-141">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-141">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e8ffb-142">In Global Catalog</span></span>      | <span data-ttu-id="e8ffb-143">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-143">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e8ffb-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8ffb-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e8ffb-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e8ffb-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8ffb-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e8ffb-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8ffb-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e8ffb-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8ffb-148">Search-Flags</span></span>           | <span data-ttu-id="e8ffb-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8ffb-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="e8ffb-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8ffb-150">System-Flags</span></span>           | <span data-ttu-id="e8ffb-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8ffb-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="e8ffb-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e8ffb-152">Classes used in</span></span>        | [<span data-ttu-id="e8ffb-153">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="e8ffb-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e8ffb-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e8ffb-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e8ffb-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e8ffb-155">Entry</span></span> | <span data-ttu-id="e8ffb-156">Wert</span><span class="sxs-lookup"><span data-stu-id="e8ffb-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e8ffb-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e8ffb-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e8ffb-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8ffb-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e8ffb-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8ffb-159">System-Only</span></span>            | <span data-ttu-id="e8ffb-160">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-160">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e8ffb-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e8ffb-162">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-162">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e8ffb-163">Is Indexed</span></span>             | <span data-ttu-id="e8ffb-164">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-164">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e8ffb-165">In Global Catalog</span></span>      | <span data-ttu-id="e8ffb-166">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-166">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e8ffb-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8ffb-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e8ffb-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e8ffb-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8ffb-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e8ffb-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8ffb-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e8ffb-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8ffb-171">Search-Flags</span></span>           | <span data-ttu-id="e8ffb-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8ffb-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="e8ffb-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8ffb-173">System-Flags</span></span>           | <span data-ttu-id="e8ffb-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8ffb-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="e8ffb-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e8ffb-175">Classes used in</span></span>        | [<span data-ttu-id="e8ffb-176">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="e8ffb-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e8ffb-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8ffb-177">Windows Server 2008</span></span>



| <span data-ttu-id="e8ffb-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e8ffb-178">Entry</span></span> | <span data-ttu-id="e8ffb-179">Wert</span><span class="sxs-lookup"><span data-stu-id="e8ffb-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e8ffb-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e8ffb-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e8ffb-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8ffb-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e8ffb-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8ffb-182">System-Only</span></span>            | <span data-ttu-id="e8ffb-183">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-183">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e8ffb-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e8ffb-185">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-185">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e8ffb-186">Is Indexed</span></span>             | <span data-ttu-id="e8ffb-187">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-187">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e8ffb-188">In Global Catalog</span></span>      | <span data-ttu-id="e8ffb-189">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-189">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e8ffb-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8ffb-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e8ffb-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e8ffb-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8ffb-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e8ffb-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8ffb-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e8ffb-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8ffb-194">Search-Flags</span></span>           | <span data-ttu-id="e8ffb-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8ffb-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="e8ffb-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8ffb-196">System-Flags</span></span>           | <span data-ttu-id="e8ffb-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8ffb-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="e8ffb-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e8ffb-198">Classes used in</span></span>        | [<span data-ttu-id="e8ffb-199">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="e8ffb-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e8ffb-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e8ffb-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e8ffb-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e8ffb-201">Entry</span></span> | <span data-ttu-id="e8ffb-202">Wert</span><span class="sxs-lookup"><span data-stu-id="e8ffb-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e8ffb-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e8ffb-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e8ffb-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8ffb-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e8ffb-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8ffb-205">System-Only</span></span>            | <span data-ttu-id="e8ffb-206">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-206">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e8ffb-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e8ffb-208">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-208">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e8ffb-209">Is Indexed</span></span>             | <span data-ttu-id="e8ffb-210">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-210">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e8ffb-211">In Global Catalog</span></span>      | <span data-ttu-id="e8ffb-212">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-212">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e8ffb-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8ffb-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e8ffb-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e8ffb-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8ffb-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e8ffb-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8ffb-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e8ffb-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8ffb-217">Search-Flags</span></span>           | <span data-ttu-id="e8ffb-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8ffb-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="e8ffb-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8ffb-219">System-Flags</span></span>           | <span data-ttu-id="e8ffb-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8ffb-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="e8ffb-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e8ffb-221">Classes used in</span></span>        | [<span data-ttu-id="e8ffb-222">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="e8ffb-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e8ffb-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e8ffb-223">Windows Server 2012</span></span>



| <span data-ttu-id="e8ffb-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e8ffb-224">Entry</span></span> | <span data-ttu-id="e8ffb-225">Wert</span><span class="sxs-lookup"><span data-stu-id="e8ffb-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e8ffb-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e8ffb-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e8ffb-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8ffb-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e8ffb-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8ffb-228">System-Only</span></span>            | <span data-ttu-id="e8ffb-229">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-229">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e8ffb-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e8ffb-231">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-231">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e8ffb-232">Is Indexed</span></span>             | <span data-ttu-id="e8ffb-233">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-233">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e8ffb-234">In Global Catalog</span></span>      | <span data-ttu-id="e8ffb-235">False</span><span class="sxs-lookup"><span data-stu-id="e8ffb-235">False</span></span>                                                                   |
| <span data-ttu-id="e8ffb-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e8ffb-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8ffb-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e8ffb-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e8ffb-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8ffb-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e8ffb-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8ffb-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e8ffb-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8ffb-240">Search-Flags</span></span>           | <span data-ttu-id="e8ffb-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8ffb-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="e8ffb-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8ffb-242">System-Flags</span></span>           | <span data-ttu-id="e8ffb-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8ffb-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="e8ffb-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e8ffb-244">Classes used in</span></span>        | [<span data-ttu-id="e8ffb-245">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="e8ffb-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





