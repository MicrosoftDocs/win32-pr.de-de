---
title: MS-PKI-RA-Signature-Attribut
description: Gibt die Anzahl der Registrierungs Registrierungsstellen-Signaturen an, die bei einer Registrierungs Anforderung erforderlich sind.
ms.assetid: da9d9357-6826-4511-b589-594c73114713
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-PKI-RA-Signature-Attributs
- "\"mspki-RA-Signature\"-Attribut AD-Schema"
topic_type:
- apiref
api_name:
- ms-PKI-RA-Signature
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 170793e46095e16a62d8e025ec16b67bf2be7131
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106338826"
---
# <a name="ms-pki-ra-signature-attribute"></a><span data-ttu-id="56814-105">MS-PKI-RA-Signature-Attribut</span><span class="sxs-lookup"><span data-stu-id="56814-105">ms-PKI-RA-Signature attribute</span></span>

<span data-ttu-id="56814-106">Gibt die Anzahl der Registrierungs Registrierungsstellen-Signaturen an, die bei einer Registrierungs Anforderung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="56814-106">Specifies the number of enrollment registration authority signatures that are required in an enrollment request.</span></span>



| <span data-ttu-id="56814-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56814-107">Entry</span></span> | <span data-ttu-id="56814-108">Wert</span><span class="sxs-lookup"><span data-stu-id="56814-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56814-109">CN</span><span class="sxs-lookup"><span data-stu-id="56814-109">CN</span></span>                | <span data-ttu-id="56814-110">MS-PKI-RA-Signature</span><span class="sxs-lookup"><span data-stu-id="56814-110">ms-PKI-RA-Signature</span></span>                                                                               |
| <span data-ttu-id="56814-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="56814-111">Ldap-Display-Name</span></span> | <span data-ttu-id="56814-112">mspki-RA-Signature</span><span class="sxs-lookup"><span data-stu-id="56814-112">msPKI-RA-Signature</span></span>                                                                                |
| <span data-ttu-id="56814-113">Size</span><span class="sxs-lookup"><span data-stu-id="56814-113">Size</span></span>              | <span data-ttu-id="56814-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="56814-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="56814-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="56814-115">Update Privilege</span></span>  | <span data-ttu-id="56814-116">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="56814-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="56814-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="56814-117">Update Frequency</span></span>  | <span data-ttu-id="56814-118">Wenn das Objekt Vorlage (MS-PKI-Certificate-template) bearbeitet, erstellt oder geklont wird.</span><span class="sxs-lookup"><span data-stu-id="56814-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="56814-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="56814-119">Attribute-Id</span></span>      | <span data-ttu-id="56814-120">1.2.840.113556.1.4.1429</span><span class="sxs-lookup"><span data-stu-id="56814-120">1.2.840.113556.1.4.1429</span></span>                                                                           |
| <span data-ttu-id="56814-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="56814-121">System-Id-Guid</span></span>    | <span data-ttu-id="56814-122">fe17e04b-937d-4f7e-8e0e-9292c8d5683e</span><span class="sxs-lookup"><span data-stu-id="56814-122">fe17e04b-937d-4f7e-8e0e-9292c8d5683e</span></span>                                                              |
| <span data-ttu-id="56814-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="56814-123">Syntax</span></span>            | [<span data-ttu-id="56814-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="56814-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="56814-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="56814-125">Implementations</span></span>

-   [<span data-ttu-id="56814-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="56814-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="56814-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="56814-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="56814-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="56814-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="56814-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="56814-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="56814-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="56814-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="56814-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="56814-131">Windows Server 2003</span></span>



| <span data-ttu-id="56814-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56814-132">Entry</span></span> | <span data-ttu-id="56814-133">Wert</span><span class="sxs-lookup"><span data-stu-id="56814-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="56814-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="56814-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="56814-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56814-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="56814-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="56814-136">System-Only</span></span>            | <span data-ttu-id="56814-137">False</span><span class="sxs-lookup"><span data-stu-id="56814-137">False</span></span>                                                                   |
| <span data-ttu-id="56814-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="56814-138">Is-Single-Valued</span></span>       | <span data-ttu-id="56814-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="56814-139">True</span></span>                                                                    |
| <span data-ttu-id="56814-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="56814-140">Is Indexed</span></span>             | <span data-ttu-id="56814-141">False</span><span class="sxs-lookup"><span data-stu-id="56814-141">False</span></span>                                                                   |
| <span data-ttu-id="56814-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="56814-142">In Global Catalog</span></span>      | <span data-ttu-id="56814-143">False</span><span class="sxs-lookup"><span data-stu-id="56814-143">False</span></span>                                                                   |
| <span data-ttu-id="56814-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56814-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="56814-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="56814-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="56814-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56814-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="56814-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56814-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="56814-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56814-148">Search-Flags</span></span>           | <span data-ttu-id="56814-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56814-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="56814-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56814-150">System-Flags</span></span>           | <span data-ttu-id="56814-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56814-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="56814-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="56814-152">Classes used in</span></span>        | [<span data-ttu-id="56814-153">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="56814-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="56814-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="56814-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="56814-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56814-155">Entry</span></span> | <span data-ttu-id="56814-156">Wert</span><span class="sxs-lookup"><span data-stu-id="56814-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="56814-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="56814-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="56814-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56814-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="56814-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="56814-159">System-Only</span></span>            | <span data-ttu-id="56814-160">False</span><span class="sxs-lookup"><span data-stu-id="56814-160">False</span></span>                                                                   |
| <span data-ttu-id="56814-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="56814-161">Is-Single-Valued</span></span>       | <span data-ttu-id="56814-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="56814-162">True</span></span>                                                                    |
| <span data-ttu-id="56814-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="56814-163">Is Indexed</span></span>             | <span data-ttu-id="56814-164">False</span><span class="sxs-lookup"><span data-stu-id="56814-164">False</span></span>                                                                   |
| <span data-ttu-id="56814-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="56814-165">In Global Catalog</span></span>      | <span data-ttu-id="56814-166">False</span><span class="sxs-lookup"><span data-stu-id="56814-166">False</span></span>                                                                   |
| <span data-ttu-id="56814-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56814-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="56814-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="56814-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="56814-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56814-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="56814-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56814-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="56814-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56814-171">Search-Flags</span></span>           | <span data-ttu-id="56814-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56814-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="56814-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56814-173">System-Flags</span></span>           | <span data-ttu-id="56814-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56814-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="56814-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="56814-175">Classes used in</span></span>        | [<span data-ttu-id="56814-176">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="56814-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="56814-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56814-177">Windows Server 2008</span></span>



| <span data-ttu-id="56814-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56814-178">Entry</span></span> | <span data-ttu-id="56814-179">Wert</span><span class="sxs-lookup"><span data-stu-id="56814-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="56814-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="56814-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="56814-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56814-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="56814-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="56814-182">System-Only</span></span>            | <span data-ttu-id="56814-183">False</span><span class="sxs-lookup"><span data-stu-id="56814-183">False</span></span>                                                                   |
| <span data-ttu-id="56814-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="56814-184">Is-Single-Valued</span></span>       | <span data-ttu-id="56814-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="56814-185">True</span></span>                                                                    |
| <span data-ttu-id="56814-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="56814-186">Is Indexed</span></span>             | <span data-ttu-id="56814-187">False</span><span class="sxs-lookup"><span data-stu-id="56814-187">False</span></span>                                                                   |
| <span data-ttu-id="56814-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="56814-188">In Global Catalog</span></span>      | <span data-ttu-id="56814-189">False</span><span class="sxs-lookup"><span data-stu-id="56814-189">False</span></span>                                                                   |
| <span data-ttu-id="56814-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56814-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="56814-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="56814-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="56814-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56814-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="56814-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56814-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="56814-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56814-194">Search-Flags</span></span>           | <span data-ttu-id="56814-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56814-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="56814-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56814-196">System-Flags</span></span>           | <span data-ttu-id="56814-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56814-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="56814-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="56814-198">Classes used in</span></span>        | [<span data-ttu-id="56814-199">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="56814-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="56814-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="56814-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="56814-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56814-201">Entry</span></span> | <span data-ttu-id="56814-202">Wert</span><span class="sxs-lookup"><span data-stu-id="56814-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="56814-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="56814-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="56814-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56814-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="56814-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="56814-205">System-Only</span></span>            | <span data-ttu-id="56814-206">False</span><span class="sxs-lookup"><span data-stu-id="56814-206">False</span></span>                                                                   |
| <span data-ttu-id="56814-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="56814-207">Is-Single-Valued</span></span>       | <span data-ttu-id="56814-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="56814-208">True</span></span>                                                                    |
| <span data-ttu-id="56814-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="56814-209">Is Indexed</span></span>             | <span data-ttu-id="56814-210">False</span><span class="sxs-lookup"><span data-stu-id="56814-210">False</span></span>                                                                   |
| <span data-ttu-id="56814-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="56814-211">In Global Catalog</span></span>      | <span data-ttu-id="56814-212">False</span><span class="sxs-lookup"><span data-stu-id="56814-212">False</span></span>                                                                   |
| <span data-ttu-id="56814-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56814-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="56814-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="56814-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="56814-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56814-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="56814-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56814-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="56814-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56814-217">Search-Flags</span></span>           | <span data-ttu-id="56814-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56814-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="56814-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56814-219">System-Flags</span></span>           | <span data-ttu-id="56814-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56814-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="56814-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="56814-221">Classes used in</span></span>        | [<span data-ttu-id="56814-222">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="56814-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="56814-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="56814-223">Windows Server 2012</span></span>



| <span data-ttu-id="56814-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56814-224">Entry</span></span> | <span data-ttu-id="56814-225">Wert</span><span class="sxs-lookup"><span data-stu-id="56814-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="56814-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="56814-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="56814-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56814-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="56814-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="56814-228">System-Only</span></span>            | <span data-ttu-id="56814-229">False</span><span class="sxs-lookup"><span data-stu-id="56814-229">False</span></span>                                                                   |
| <span data-ttu-id="56814-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="56814-230">Is-Single-Valued</span></span>       | <span data-ttu-id="56814-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="56814-231">True</span></span>                                                                    |
| <span data-ttu-id="56814-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="56814-232">Is Indexed</span></span>             | <span data-ttu-id="56814-233">False</span><span class="sxs-lookup"><span data-stu-id="56814-233">False</span></span>                                                                   |
| <span data-ttu-id="56814-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="56814-234">In Global Catalog</span></span>      | <span data-ttu-id="56814-235">False</span><span class="sxs-lookup"><span data-stu-id="56814-235">False</span></span>                                                                   |
| <span data-ttu-id="56814-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56814-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="56814-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="56814-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="56814-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56814-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="56814-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56814-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="56814-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56814-240">Search-Flags</span></span>           | <span data-ttu-id="56814-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56814-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="56814-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56814-242">System-Flags</span></span>           | <span data-ttu-id="56814-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56814-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="56814-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="56814-244">Classes used in</span></span>        | [<span data-ttu-id="56814-245">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="56814-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





