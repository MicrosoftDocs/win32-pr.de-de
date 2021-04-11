---
title: MS-PKI-RA-Application-Policies-Attribut
description: Die erforderliche Registrierungsrichtlinien-OID der Registrierungsstelle in den gegen Signaturen der Zertifikat Anforderung.
ms.assetid: 1ce61107-01aa-4a03-8a00-21890fb610d7
ms.tgt_platform: multiple
keywords:
- MS-PKI-RA-Application-Policies-Attribut AD-Schema
- mspki-RA-Application-Policies-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-PKI-RA-Application-Policies
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01aab7c8da5c6267efe954cac71dc8c9c98c18f4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104213765"
---
# <a name="ms-pki-ra-application-policies-attribute"></a><span data-ttu-id="3069e-105">MS-PKI-RA-Application-Policies-Attribut</span><span class="sxs-lookup"><span data-stu-id="3069e-105">ms-PKI-RA-Application-Policies attribute</span></span>

<span data-ttu-id="3069e-106">Die erforderliche Registrierungsrichtlinien-OID der Registrierungsstelle in den gegen Signaturen der Zertifikat Anforderung.</span><span class="sxs-lookup"><span data-stu-id="3069e-106">The required RA application policy OID in the counter signatures of the certificate request.</span></span>



| <span data-ttu-id="3069e-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3069e-107">Entry</span></span> | <span data-ttu-id="3069e-108">Wert</span><span class="sxs-lookup"><span data-stu-id="3069e-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3069e-109">CN</span><span class="sxs-lookup"><span data-stu-id="3069e-109">CN</span></span>                | <span data-ttu-id="3069e-110">MS-PKI-RA-Application-Policies</span><span class="sxs-lookup"><span data-stu-id="3069e-110">ms-PKI-RA-Application-Policies</span></span>                                                             |
| <span data-ttu-id="3069e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3069e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3069e-112">mspki-RA-Application-Policies</span><span class="sxs-lookup"><span data-stu-id="3069e-112">msPKI-RA-Application-Policies</span></span>                                                              |
| <span data-ttu-id="3069e-113">Size</span><span class="sxs-lookup"><span data-stu-id="3069e-113">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="3069e-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="3069e-114">Update Privilege</span></span>  | <span data-ttu-id="3069e-115">Unternehmensadministrator</span><span class="sxs-lookup"><span data-stu-id="3069e-115">Enterprise administrator</span></span>                                                                   |
| <span data-ttu-id="3069e-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="3069e-116">Update Frequency</span></span>  | <span data-ttu-id="3069e-117">Wenn eine neue Vorlage erstellt wird oder die Attribute vorhandener Vorlagen bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="3069e-117">Whenever a new template is created, or the attributes of an existing templates are edited.</span></span> |
| <span data-ttu-id="3069e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3069e-118">Attribute-Id</span></span>      | <span data-ttu-id="3069e-119">1.2.840.113556.1.4.1675</span><span class="sxs-lookup"><span data-stu-id="3069e-119">1.2.840.113556.1.4.1675</span></span>                                                                    |
| <span data-ttu-id="3069e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3069e-120">System-Id-Guid</span></span>    | <span data-ttu-id="3069e-121">3c91fbbf-4773-4ccd-a87b-85d53e7bcf6a</span><span class="sxs-lookup"><span data-stu-id="3069e-121">3c91fbbf-4773-4ccd-a87b-85d53e7bcf6a</span></span>                                                       |
| <span data-ttu-id="3069e-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="3069e-122">Syntax</span></span>            | [<span data-ttu-id="3069e-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3069e-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="3069e-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="3069e-124">Implementations</span></span>

-   [<span data-ttu-id="3069e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3069e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3069e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3069e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3069e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3069e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3069e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3069e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3069e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3069e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="3069e-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3069e-130">Windows Server 2003</span></span>



| <span data-ttu-id="3069e-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3069e-131">Entry</span></span> | <span data-ttu-id="3069e-132">Wert</span><span class="sxs-lookup"><span data-stu-id="3069e-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3069e-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3069e-133">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3069e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3069e-134">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3069e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="3069e-135">System-Only</span></span>            | <span data-ttu-id="3069e-136">False</span><span class="sxs-lookup"><span data-stu-id="3069e-136">False</span></span>                                                                   |
| <span data-ttu-id="3069e-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3069e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="3069e-138">False</span><span class="sxs-lookup"><span data-stu-id="3069e-138">False</span></span>                                                                   |
| <span data-ttu-id="3069e-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3069e-139">Is Indexed</span></span>             | <span data-ttu-id="3069e-140">False</span><span class="sxs-lookup"><span data-stu-id="3069e-140">False</span></span>                                                                   |
| <span data-ttu-id="3069e-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3069e-141">In Global Catalog</span></span>      | <span data-ttu-id="3069e-142">False</span><span class="sxs-lookup"><span data-stu-id="3069e-142">False</span></span>                                                                   |
| <span data-ttu-id="3069e-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3069e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="3069e-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3069e-144">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="3069e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3069e-145">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="3069e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3069e-146">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="3069e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3069e-147">Search-Flags</span></span>           | <span data-ttu-id="3069e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3069e-148">0x00000000</span></span>                                                              |
| <span data-ttu-id="3069e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3069e-149">System-Flags</span></span>           | <span data-ttu-id="3069e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3069e-150">0x00000010</span></span>                                                              |
| <span data-ttu-id="3069e-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3069e-151">Classes used in</span></span>        | [<span data-ttu-id="3069e-152">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="3069e-152">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3069e-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3069e-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3069e-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3069e-154">Entry</span></span> | <span data-ttu-id="3069e-155">Wert</span><span class="sxs-lookup"><span data-stu-id="3069e-155">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3069e-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3069e-156">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3069e-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3069e-157">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3069e-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="3069e-158">System-Only</span></span>            | <span data-ttu-id="3069e-159">False</span><span class="sxs-lookup"><span data-stu-id="3069e-159">False</span></span>                                                                   |
| <span data-ttu-id="3069e-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3069e-160">Is-Single-Valued</span></span>       | <span data-ttu-id="3069e-161">False</span><span class="sxs-lookup"><span data-stu-id="3069e-161">False</span></span>                                                                   |
| <span data-ttu-id="3069e-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3069e-162">Is Indexed</span></span>             | <span data-ttu-id="3069e-163">False</span><span class="sxs-lookup"><span data-stu-id="3069e-163">False</span></span>                                                                   |
| <span data-ttu-id="3069e-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3069e-164">In Global Catalog</span></span>      | <span data-ttu-id="3069e-165">False</span><span class="sxs-lookup"><span data-stu-id="3069e-165">False</span></span>                                                                   |
| <span data-ttu-id="3069e-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3069e-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="3069e-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3069e-167">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="3069e-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3069e-168">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="3069e-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3069e-169">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="3069e-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3069e-170">Search-Flags</span></span>           | <span data-ttu-id="3069e-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3069e-171">0x00000000</span></span>                                                              |
| <span data-ttu-id="3069e-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3069e-172">System-Flags</span></span>           | <span data-ttu-id="3069e-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3069e-173">0x00000010</span></span>                                                              |
| <span data-ttu-id="3069e-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3069e-174">Classes used in</span></span>        | [<span data-ttu-id="3069e-175">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="3069e-175">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3069e-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3069e-176">Windows Server 2008</span></span>



| <span data-ttu-id="3069e-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3069e-177">Entry</span></span> | <span data-ttu-id="3069e-178">Wert</span><span class="sxs-lookup"><span data-stu-id="3069e-178">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3069e-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3069e-179">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3069e-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3069e-180">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3069e-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="3069e-181">System-Only</span></span>            | <span data-ttu-id="3069e-182">False</span><span class="sxs-lookup"><span data-stu-id="3069e-182">False</span></span>                                                                   |
| <span data-ttu-id="3069e-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3069e-183">Is-Single-Valued</span></span>       | <span data-ttu-id="3069e-184">False</span><span class="sxs-lookup"><span data-stu-id="3069e-184">False</span></span>                                                                   |
| <span data-ttu-id="3069e-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3069e-185">Is Indexed</span></span>             | <span data-ttu-id="3069e-186">False</span><span class="sxs-lookup"><span data-stu-id="3069e-186">False</span></span>                                                                   |
| <span data-ttu-id="3069e-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3069e-187">In Global Catalog</span></span>      | <span data-ttu-id="3069e-188">False</span><span class="sxs-lookup"><span data-stu-id="3069e-188">False</span></span>                                                                   |
| <span data-ttu-id="3069e-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3069e-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="3069e-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3069e-190">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="3069e-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3069e-191">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="3069e-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3069e-192">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="3069e-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3069e-193">Search-Flags</span></span>           | <span data-ttu-id="3069e-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3069e-194">0x00000000</span></span>                                                              |
| <span data-ttu-id="3069e-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3069e-195">System-Flags</span></span>           | <span data-ttu-id="3069e-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3069e-196">0x00000010</span></span>                                                              |
| <span data-ttu-id="3069e-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3069e-197">Classes used in</span></span>        | [<span data-ttu-id="3069e-198">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="3069e-198">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3069e-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3069e-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3069e-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3069e-200">Entry</span></span> | <span data-ttu-id="3069e-201">Wert</span><span class="sxs-lookup"><span data-stu-id="3069e-201">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3069e-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3069e-202">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3069e-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3069e-203">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3069e-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="3069e-204">System-Only</span></span>            | <span data-ttu-id="3069e-205">False</span><span class="sxs-lookup"><span data-stu-id="3069e-205">False</span></span>                                                                   |
| <span data-ttu-id="3069e-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3069e-206">Is-Single-Valued</span></span>       | <span data-ttu-id="3069e-207">False</span><span class="sxs-lookup"><span data-stu-id="3069e-207">False</span></span>                                                                   |
| <span data-ttu-id="3069e-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3069e-208">Is Indexed</span></span>             | <span data-ttu-id="3069e-209">False</span><span class="sxs-lookup"><span data-stu-id="3069e-209">False</span></span>                                                                   |
| <span data-ttu-id="3069e-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3069e-210">In Global Catalog</span></span>      | <span data-ttu-id="3069e-211">False</span><span class="sxs-lookup"><span data-stu-id="3069e-211">False</span></span>                                                                   |
| <span data-ttu-id="3069e-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3069e-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="3069e-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3069e-213">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="3069e-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3069e-214">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="3069e-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3069e-215">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="3069e-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3069e-216">Search-Flags</span></span>           | <span data-ttu-id="3069e-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3069e-217">0x00000000</span></span>                                                              |
| <span data-ttu-id="3069e-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3069e-218">System-Flags</span></span>           | <span data-ttu-id="3069e-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3069e-219">0x00000010</span></span>                                                              |
| <span data-ttu-id="3069e-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3069e-220">Classes used in</span></span>        | [<span data-ttu-id="3069e-221">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="3069e-221">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3069e-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3069e-222">Windows Server 2012</span></span>



| <span data-ttu-id="3069e-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3069e-223">Entry</span></span> | <span data-ttu-id="3069e-224">Wert</span><span class="sxs-lookup"><span data-stu-id="3069e-224">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3069e-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3069e-225">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3069e-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3069e-226">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3069e-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="3069e-227">System-Only</span></span>            | <span data-ttu-id="3069e-228">False</span><span class="sxs-lookup"><span data-stu-id="3069e-228">False</span></span>                                                                   |
| <span data-ttu-id="3069e-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3069e-229">Is-Single-Valued</span></span>       | <span data-ttu-id="3069e-230">False</span><span class="sxs-lookup"><span data-stu-id="3069e-230">False</span></span>                                                                   |
| <span data-ttu-id="3069e-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3069e-231">Is Indexed</span></span>             | <span data-ttu-id="3069e-232">False</span><span class="sxs-lookup"><span data-stu-id="3069e-232">False</span></span>                                                                   |
| <span data-ttu-id="3069e-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3069e-233">In Global Catalog</span></span>      | <span data-ttu-id="3069e-234">False</span><span class="sxs-lookup"><span data-stu-id="3069e-234">False</span></span>                                                                   |
| <span data-ttu-id="3069e-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3069e-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="3069e-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3069e-236">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="3069e-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3069e-237">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="3069e-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3069e-238">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="3069e-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3069e-239">Search-Flags</span></span>           | <span data-ttu-id="3069e-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3069e-240">0x00000000</span></span>                                                              |
| <span data-ttu-id="3069e-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3069e-241">System-Flags</span></span>           | <span data-ttu-id="3069e-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3069e-242">0x00000010</span></span>                                                              |
| <span data-ttu-id="3069e-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3069e-243">Classes used in</span></span>        | [<span data-ttu-id="3069e-244">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="3069e-244">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





