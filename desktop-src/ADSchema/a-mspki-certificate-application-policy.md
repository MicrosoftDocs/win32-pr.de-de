---
title: MS-PKI-Certificate-Application-Policy-Attribut
description: Die Anwendungsrichtlinien-OID in einem Zertifikat.
ms.assetid: 91e98ec9-0e8d-4950-a62c-9b6901ec4d97
ms.tgt_platform: multiple
keywords:
- MS-PKI-Certificate-Application-Policy-Attribut AD-Schema
- mspki-Zertifikat-Anwendungsrichtlinien Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-PKI-Certificate-Application-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9436415fb9361454fc5f872802516fa455ff980b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392276"
---
# <a name="ms-pki-certificate-application-policy-attribute"></a><span data-ttu-id="3877d-105">MS-PKI-Certificate-Application-Policy-Attribut</span><span class="sxs-lookup"><span data-stu-id="3877d-105">ms-PKI-Certificate-Application-Policy attribute</span></span>

<span data-ttu-id="3877d-106">Die Anwendungsrichtlinien-OID in einem Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="3877d-106">The application policy OID's in a certificate.</span></span>



| <span data-ttu-id="3877d-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3877d-107">Entry</span></span> | <span data-ttu-id="3877d-108">Wert</span><span class="sxs-lookup"><span data-stu-id="3877d-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3877d-109">CN</span><span class="sxs-lookup"><span data-stu-id="3877d-109">CN</span></span>                | <span data-ttu-id="3877d-110">MS-PKI-Certificate-Application-Policy</span><span class="sxs-lookup"><span data-stu-id="3877d-110">ms-PKI-Certificate-Application-Policy</span></span>                                                      |
| <span data-ttu-id="3877d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3877d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3877d-112">mspki-Zertifikat-Anwendungs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="3877d-112">msPKI-Certificate-Application-Policy</span></span>                                                       |
| <span data-ttu-id="3877d-113">Size</span><span class="sxs-lookup"><span data-stu-id="3877d-113">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="3877d-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="3877d-114">Update Privilege</span></span>  | <span data-ttu-id="3877d-115">Unternehmensadministrator</span><span class="sxs-lookup"><span data-stu-id="3877d-115">Enterprise administrator</span></span>                                                                   |
| <span data-ttu-id="3877d-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="3877d-116">Update Frequency</span></span>  | <span data-ttu-id="3877d-117">Wenn eine neue Vorlage erstellt wird oder die Attribute vorhandener Vorlagen bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="3877d-117">Whenever a new template is created, or the attributes of an existing templates are edited.</span></span> |
| <span data-ttu-id="3877d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3877d-118">Attribute-Id</span></span>      | <span data-ttu-id="3877d-119">1.2.840.113556.1.4.1674</span><span class="sxs-lookup"><span data-stu-id="3877d-119">1.2.840.113556.1.4.1674</span></span>                                                                    |
| <span data-ttu-id="3877d-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3877d-120">System-Id-Guid</span></span>    | <span data-ttu-id="3877d-121">dbd90548-aa37-4202-9966-8c537ba5ce32</span><span class="sxs-lookup"><span data-stu-id="3877d-121">dbd90548-aa37-4202-9966-8c537ba5ce32</span></span>                                                       |
| <span data-ttu-id="3877d-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="3877d-122">Syntax</span></span>            | [<span data-ttu-id="3877d-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3877d-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="3877d-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="3877d-124">Implementations</span></span>

-   [<span data-ttu-id="3877d-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3877d-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3877d-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3877d-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3877d-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3877d-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3877d-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3877d-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3877d-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3877d-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="3877d-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3877d-130">Windows Server 2003</span></span>



| <span data-ttu-id="3877d-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3877d-131">Entry</span></span> | <span data-ttu-id="3877d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="3877d-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3877d-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3877d-133">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3877d-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3877d-134">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3877d-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="3877d-135">System-Only</span></span>            | <span data-ttu-id="3877d-136">False</span><span class="sxs-lookup"><span data-stu-id="3877d-136">False</span></span>                                                                   |
| <span data-ttu-id="3877d-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3877d-137">Is-Single-Valued</span></span>       | <span data-ttu-id="3877d-138">False</span><span class="sxs-lookup"><span data-stu-id="3877d-138">False</span></span>                                                                   |
| <span data-ttu-id="3877d-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3877d-139">Is Indexed</span></span>             | <span data-ttu-id="3877d-140">False</span><span class="sxs-lookup"><span data-stu-id="3877d-140">False</span></span>                                                                   |
| <span data-ttu-id="3877d-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3877d-141">In Global Catalog</span></span>      | <span data-ttu-id="3877d-142">False</span><span class="sxs-lookup"><span data-stu-id="3877d-142">False</span></span>                                                                   |
| <span data-ttu-id="3877d-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3877d-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="3877d-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3877d-144">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="3877d-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3877d-145">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="3877d-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3877d-146">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="3877d-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3877d-147">Search-Flags</span></span>           | <span data-ttu-id="3877d-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3877d-148">0x00000000</span></span>                                                              |
| <span data-ttu-id="3877d-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3877d-149">System-Flags</span></span>           | <span data-ttu-id="3877d-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3877d-150">0x00000010</span></span>                                                              |
| <span data-ttu-id="3877d-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3877d-151">Classes used in</span></span>        | [<span data-ttu-id="3877d-152">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="3877d-152">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3877d-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3877d-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3877d-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3877d-154">Entry</span></span> | <span data-ttu-id="3877d-155">Wert</span><span class="sxs-lookup"><span data-stu-id="3877d-155">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3877d-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3877d-156">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3877d-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3877d-157">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3877d-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="3877d-158">System-Only</span></span>            | <span data-ttu-id="3877d-159">False</span><span class="sxs-lookup"><span data-stu-id="3877d-159">False</span></span>                                                                   |
| <span data-ttu-id="3877d-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3877d-160">Is-Single-Valued</span></span>       | <span data-ttu-id="3877d-161">False</span><span class="sxs-lookup"><span data-stu-id="3877d-161">False</span></span>                                                                   |
| <span data-ttu-id="3877d-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3877d-162">Is Indexed</span></span>             | <span data-ttu-id="3877d-163">False</span><span class="sxs-lookup"><span data-stu-id="3877d-163">False</span></span>                                                                   |
| <span data-ttu-id="3877d-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3877d-164">In Global Catalog</span></span>      | <span data-ttu-id="3877d-165">False</span><span class="sxs-lookup"><span data-stu-id="3877d-165">False</span></span>                                                                   |
| <span data-ttu-id="3877d-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3877d-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="3877d-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3877d-167">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="3877d-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3877d-168">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="3877d-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3877d-169">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="3877d-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3877d-170">Search-Flags</span></span>           | <span data-ttu-id="3877d-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3877d-171">0x00000000</span></span>                                                              |
| <span data-ttu-id="3877d-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3877d-172">System-Flags</span></span>           | <span data-ttu-id="3877d-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3877d-173">0x00000010</span></span>                                                              |
| <span data-ttu-id="3877d-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3877d-174">Classes used in</span></span>        | [<span data-ttu-id="3877d-175">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="3877d-175">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3877d-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3877d-176">Windows Server 2008</span></span>



| <span data-ttu-id="3877d-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3877d-177">Entry</span></span> | <span data-ttu-id="3877d-178">Wert</span><span class="sxs-lookup"><span data-stu-id="3877d-178">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3877d-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3877d-179">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3877d-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3877d-180">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3877d-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="3877d-181">System-Only</span></span>            | <span data-ttu-id="3877d-182">False</span><span class="sxs-lookup"><span data-stu-id="3877d-182">False</span></span>                                                                   |
| <span data-ttu-id="3877d-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3877d-183">Is-Single-Valued</span></span>       | <span data-ttu-id="3877d-184">False</span><span class="sxs-lookup"><span data-stu-id="3877d-184">False</span></span>                                                                   |
| <span data-ttu-id="3877d-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3877d-185">Is Indexed</span></span>             | <span data-ttu-id="3877d-186">False</span><span class="sxs-lookup"><span data-stu-id="3877d-186">False</span></span>                                                                   |
| <span data-ttu-id="3877d-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3877d-187">In Global Catalog</span></span>      | <span data-ttu-id="3877d-188">False</span><span class="sxs-lookup"><span data-stu-id="3877d-188">False</span></span>                                                                   |
| <span data-ttu-id="3877d-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3877d-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="3877d-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3877d-190">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="3877d-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3877d-191">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="3877d-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3877d-192">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="3877d-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3877d-193">Search-Flags</span></span>           | <span data-ttu-id="3877d-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3877d-194">0x00000000</span></span>                                                              |
| <span data-ttu-id="3877d-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3877d-195">System-Flags</span></span>           | <span data-ttu-id="3877d-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3877d-196">0x00000010</span></span>                                                              |
| <span data-ttu-id="3877d-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3877d-197">Classes used in</span></span>        | [<span data-ttu-id="3877d-198">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="3877d-198">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3877d-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3877d-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3877d-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3877d-200">Entry</span></span> | <span data-ttu-id="3877d-201">Wert</span><span class="sxs-lookup"><span data-stu-id="3877d-201">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3877d-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3877d-202">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3877d-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3877d-203">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3877d-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="3877d-204">System-Only</span></span>            | <span data-ttu-id="3877d-205">False</span><span class="sxs-lookup"><span data-stu-id="3877d-205">False</span></span>                                                                   |
| <span data-ttu-id="3877d-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3877d-206">Is-Single-Valued</span></span>       | <span data-ttu-id="3877d-207">False</span><span class="sxs-lookup"><span data-stu-id="3877d-207">False</span></span>                                                                   |
| <span data-ttu-id="3877d-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3877d-208">Is Indexed</span></span>             | <span data-ttu-id="3877d-209">False</span><span class="sxs-lookup"><span data-stu-id="3877d-209">False</span></span>                                                                   |
| <span data-ttu-id="3877d-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3877d-210">In Global Catalog</span></span>      | <span data-ttu-id="3877d-211">False</span><span class="sxs-lookup"><span data-stu-id="3877d-211">False</span></span>                                                                   |
| <span data-ttu-id="3877d-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3877d-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="3877d-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3877d-213">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="3877d-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3877d-214">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="3877d-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3877d-215">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="3877d-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3877d-216">Search-Flags</span></span>           | <span data-ttu-id="3877d-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3877d-217">0x00000000</span></span>                                                              |
| <span data-ttu-id="3877d-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3877d-218">System-Flags</span></span>           | <span data-ttu-id="3877d-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3877d-219">0x00000010</span></span>                                                              |
| <span data-ttu-id="3877d-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3877d-220">Classes used in</span></span>        | [<span data-ttu-id="3877d-221">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="3877d-221">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3877d-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3877d-222">Windows Server 2012</span></span>



| <span data-ttu-id="3877d-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3877d-223">Entry</span></span> | <span data-ttu-id="3877d-224">Wert</span><span class="sxs-lookup"><span data-stu-id="3877d-224">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3877d-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3877d-225">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3877d-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3877d-226">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3877d-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="3877d-227">System-Only</span></span>            | <span data-ttu-id="3877d-228">False</span><span class="sxs-lookup"><span data-stu-id="3877d-228">False</span></span>                                                                   |
| <span data-ttu-id="3877d-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3877d-229">Is-Single-Valued</span></span>       | <span data-ttu-id="3877d-230">False</span><span class="sxs-lookup"><span data-stu-id="3877d-230">False</span></span>                                                                   |
| <span data-ttu-id="3877d-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3877d-231">Is Indexed</span></span>             | <span data-ttu-id="3877d-232">False</span><span class="sxs-lookup"><span data-stu-id="3877d-232">False</span></span>                                                                   |
| <span data-ttu-id="3877d-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3877d-233">In Global Catalog</span></span>      | <span data-ttu-id="3877d-234">False</span><span class="sxs-lookup"><span data-stu-id="3877d-234">False</span></span>                                                                   |
| <span data-ttu-id="3877d-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3877d-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="3877d-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3877d-236">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="3877d-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3877d-237">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="3877d-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3877d-238">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="3877d-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3877d-239">Search-Flags</span></span>           | <span data-ttu-id="3877d-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3877d-240">0x00000000</span></span>                                                              |
| <span data-ttu-id="3877d-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3877d-241">System-Flags</span></span>           | <span data-ttu-id="3877d-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3877d-242">0x00000010</span></span>                                                              |
| <span data-ttu-id="3877d-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3877d-243">Classes used in</span></span>        | [<span data-ttu-id="3877d-244">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="3877d-244">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





