---
title: MS-PKI-Certificate-Policy-Attribut
description: Enthält die Liste der Richtlinien-OIDs und ihrer optionalen CSPs im ausgestellten Zertifikat.
ms.assetid: bc84c5ff-9cb1-406c-825c-97fa479d52eb
ms.tgt_platform: multiple
keywords:
- MS-PKI-Certificate-Policy-Attribut AD-Schema
- mspki-Certificate-Policy-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-PKI-Certificate-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2d6857b6035cc72271c7276b679b8a497aaab9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859641"
---
# <a name="ms-pki-certificate-policy-attribute"></a><span data-ttu-id="b5fe4-105">MS-PKI-Certificate-Policy-Attribut</span><span class="sxs-lookup"><span data-stu-id="b5fe4-105">ms-PKI-Certificate-Policy attribute</span></span>

<span data-ttu-id="b5fe4-106">Enthält die Liste der Richtlinien-OIDs und ihrer optionalen CSPs im ausgestellten Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="b5fe4-106">Contains the list of policy OIDs and their optional CSPs in the issued certificate.</span></span>



| <span data-ttu-id="b5fe4-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5fe4-107">Entry</span></span> | <span data-ttu-id="b5fe4-108">Wert</span><span class="sxs-lookup"><span data-stu-id="b5fe4-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5fe4-109">CN</span><span class="sxs-lookup"><span data-stu-id="b5fe4-109">CN</span></span>                | <span data-ttu-id="b5fe4-110">MS-PKI-Certificate-Policy</span><span class="sxs-lookup"><span data-stu-id="b5fe4-110">ms-PKI-Certificate-Policy</span></span>                                                                         |
| <span data-ttu-id="b5fe4-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b5fe4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b5fe4-112">mspki-Zertifikat-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="b5fe4-112">msPKI-Certificate-Policy</span></span>                                                                          |
| <span data-ttu-id="b5fe4-113">Size</span><span class="sxs-lookup"><span data-stu-id="b5fe4-113">Size</span></span>              | <span data-ttu-id="b5fe4-114">64 Byte-Mal die Anzahl der Einträge.</span><span class="sxs-lookup"><span data-stu-id="b5fe4-114">64 bytes times the number of entries.</span></span>                                                             |
| <span data-ttu-id="b5fe4-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b5fe4-115">Update Privilege</span></span>  | <span data-ttu-id="b5fe4-116">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="b5fe4-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="b5fe4-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b5fe4-117">Update Frequency</span></span>  | <span data-ttu-id="b5fe4-118">Wenn das Objekt Vorlage (MS-PKI-Certificate-template) bearbeitet, erstellt oder geklont wird.</span><span class="sxs-lookup"><span data-stu-id="b5fe4-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="b5fe4-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b5fe4-119">Attribute-Id</span></span>      | <span data-ttu-id="b5fe4-120">1.2.840.113556.1.4.1439</span><span class="sxs-lookup"><span data-stu-id="b5fe4-120">1.2.840.113556.1.4.1439</span></span>                                                                           |
| <span data-ttu-id="b5fe4-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b5fe4-121">System-Id-Guid</span></span>    | <span data-ttu-id="b5fe4-122">38942346-cc5b-424b-a7d8-6ffd12029c5f</span><span class="sxs-lookup"><span data-stu-id="b5fe4-122">38942346-cc5b-424b-a7d8-6ffd12029c5f</span></span>                                                              |
| <span data-ttu-id="b5fe4-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5fe4-123">Syntax</span></span>            | [<span data-ttu-id="b5fe4-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b5fe4-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="b5fe4-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b5fe4-125">Implementations</span></span>

-   [<span data-ttu-id="b5fe4-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b5fe4-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b5fe4-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b5fe4-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b5fe4-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b5fe4-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b5fe4-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b5fe4-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b5fe4-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b5fe4-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b5fe4-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b5fe4-131">Windows Server 2003</span></span>



| <span data-ttu-id="b5fe4-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5fe4-132">Entry</span></span> | <span data-ttu-id="b5fe4-133">Wert</span><span class="sxs-lookup"><span data-stu-id="b5fe4-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b5fe4-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b5fe4-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b5fe4-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5fe4-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b5fe4-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5fe4-136">System-Only</span></span>            | <span data-ttu-id="b5fe4-137">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-137">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b5fe4-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b5fe4-139">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-139">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b5fe4-140">Is Indexed</span></span>             | <span data-ttu-id="b5fe4-141">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-141">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b5fe4-142">In Global Catalog</span></span>      | <span data-ttu-id="b5fe4-143">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-143">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b5fe4-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5fe4-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b5fe4-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b5fe4-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5fe4-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b5fe4-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5fe4-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b5fe4-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5fe4-148">Search-Flags</span></span>           | <span data-ttu-id="b5fe4-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5fe4-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="b5fe4-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5fe4-150">System-Flags</span></span>           | <span data-ttu-id="b5fe4-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5fe4-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="b5fe4-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b5fe4-152">Classes used in</span></span>        | [<span data-ttu-id="b5fe4-153">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="b5fe4-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b5fe4-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b5fe4-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b5fe4-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5fe4-155">Entry</span></span> | <span data-ttu-id="b5fe4-156">Wert</span><span class="sxs-lookup"><span data-stu-id="b5fe4-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b5fe4-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b5fe4-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b5fe4-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5fe4-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b5fe4-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5fe4-159">System-Only</span></span>            | <span data-ttu-id="b5fe4-160">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-160">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b5fe4-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b5fe4-162">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-162">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b5fe4-163">Is Indexed</span></span>             | <span data-ttu-id="b5fe4-164">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-164">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b5fe4-165">In Global Catalog</span></span>      | <span data-ttu-id="b5fe4-166">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-166">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b5fe4-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5fe4-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b5fe4-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b5fe4-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5fe4-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b5fe4-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5fe4-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b5fe4-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5fe4-171">Search-Flags</span></span>           | <span data-ttu-id="b5fe4-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5fe4-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="b5fe4-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5fe4-173">System-Flags</span></span>           | <span data-ttu-id="b5fe4-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5fe4-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="b5fe4-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b5fe4-175">Classes used in</span></span>        | [<span data-ttu-id="b5fe4-176">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="b5fe4-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b5fe4-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5fe4-177">Windows Server 2008</span></span>



| <span data-ttu-id="b5fe4-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5fe4-178">Entry</span></span> | <span data-ttu-id="b5fe4-179">Wert</span><span class="sxs-lookup"><span data-stu-id="b5fe4-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b5fe4-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b5fe4-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b5fe4-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5fe4-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b5fe4-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5fe4-182">System-Only</span></span>            | <span data-ttu-id="b5fe4-183">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-183">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b5fe4-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b5fe4-185">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-185">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b5fe4-186">Is Indexed</span></span>             | <span data-ttu-id="b5fe4-187">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-187">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b5fe4-188">In Global Catalog</span></span>      | <span data-ttu-id="b5fe4-189">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-189">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b5fe4-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5fe4-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b5fe4-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b5fe4-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5fe4-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b5fe4-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5fe4-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b5fe4-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5fe4-194">Search-Flags</span></span>           | <span data-ttu-id="b5fe4-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5fe4-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="b5fe4-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5fe4-196">System-Flags</span></span>           | <span data-ttu-id="b5fe4-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5fe4-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="b5fe4-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b5fe4-198">Classes used in</span></span>        | [<span data-ttu-id="b5fe4-199">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="b5fe4-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b5fe4-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b5fe4-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b5fe4-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5fe4-201">Entry</span></span> | <span data-ttu-id="b5fe4-202">Wert</span><span class="sxs-lookup"><span data-stu-id="b5fe4-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b5fe4-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b5fe4-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b5fe4-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5fe4-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b5fe4-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5fe4-205">System-Only</span></span>            | <span data-ttu-id="b5fe4-206">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-206">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b5fe4-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b5fe4-208">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-208">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b5fe4-209">Is Indexed</span></span>             | <span data-ttu-id="b5fe4-210">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-210">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b5fe4-211">In Global Catalog</span></span>      | <span data-ttu-id="b5fe4-212">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-212">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b5fe4-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5fe4-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b5fe4-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b5fe4-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5fe4-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b5fe4-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5fe4-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b5fe4-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5fe4-217">Search-Flags</span></span>           | <span data-ttu-id="b5fe4-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5fe4-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="b5fe4-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5fe4-219">System-Flags</span></span>           | <span data-ttu-id="b5fe4-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5fe4-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="b5fe4-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b5fe4-221">Classes used in</span></span>        | [<span data-ttu-id="b5fe4-222">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="b5fe4-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b5fe4-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b5fe4-223">Windows Server 2012</span></span>



| <span data-ttu-id="b5fe4-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5fe4-224">Entry</span></span> | <span data-ttu-id="b5fe4-225">Wert</span><span class="sxs-lookup"><span data-stu-id="b5fe4-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b5fe4-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b5fe4-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b5fe4-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5fe4-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b5fe4-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5fe4-228">System-Only</span></span>            | <span data-ttu-id="b5fe4-229">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-229">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b5fe4-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b5fe4-231">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-231">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b5fe4-232">Is Indexed</span></span>             | <span data-ttu-id="b5fe4-233">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-233">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b5fe4-234">In Global Catalog</span></span>      | <span data-ttu-id="b5fe4-235">False</span><span class="sxs-lookup"><span data-stu-id="b5fe4-235">False</span></span>                                                                   |
| <span data-ttu-id="b5fe4-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b5fe4-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5fe4-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b5fe4-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b5fe4-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5fe4-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b5fe4-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5fe4-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b5fe4-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5fe4-240">Search-Flags</span></span>           | <span data-ttu-id="b5fe4-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5fe4-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="b5fe4-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5fe4-242">System-Flags</span></span>           | <span data-ttu-id="b5fe4-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5fe4-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="b5fe4-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b5fe4-244">Classes used in</span></span>        | [<span data-ttu-id="b5fe4-245">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="b5fe4-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





