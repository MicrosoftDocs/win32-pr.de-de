---
title: MS-PKI-Template-Minor-Revision-Attribut
description: Verfolgt die Attribute in der-Klasse, die sich ändern. Dadurch wird jedoch keine automatische Registrierung auslöst.
ms.assetid: ff08b621-9a77-48a9-847d-f390ffb41326
ms.tgt_platform: multiple
keywords:
- "\"MS-PKI-Template-Minor-Revision\"-Attribut AD-Schema"
- mspki-Template-Minor-Revision-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-PKI-Template-Minor-Revision
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c44e80fa634067ea8b0336cbc63cbf33c09ab2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480303"
---
# <a name="ms-pki-template-minor-revision-attribute"></a><span data-ttu-id="9a831-106">MS-PKI-Template-Minor-Revision-Attribut</span><span class="sxs-lookup"><span data-stu-id="9a831-106">ms-PKI-Template-Minor-Revision attribute</span></span>

<span data-ttu-id="9a831-107">Verfolgt die Attribute in der-Klasse, die sich ändern.</span><span class="sxs-lookup"><span data-stu-id="9a831-107">Keeps track of attributes in the class changing.</span></span> <span data-ttu-id="9a831-108">Dadurch wird jedoch keine automatische Registrierung auslöst.</span><span class="sxs-lookup"><span data-stu-id="9a831-108">However, this will not trigger auto-enrollment.</span></span>



| <span data-ttu-id="9a831-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a831-109">Entry</span></span> | <span data-ttu-id="9a831-110">Wert</span><span class="sxs-lookup"><span data-stu-id="9a831-110">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a831-111">CN</span><span class="sxs-lookup"><span data-stu-id="9a831-111">CN</span></span>                | <span data-ttu-id="9a831-112">MS-PKI-Template-Minor-Revision</span><span class="sxs-lookup"><span data-stu-id="9a831-112">ms-PKI-Template-Minor-Revision</span></span>                                                                    |
| <span data-ttu-id="9a831-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9a831-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9a831-114">mspki-Template-Minor-Revision</span><span class="sxs-lookup"><span data-stu-id="9a831-114">msPKI-Template-Minor-Revision</span></span>                                                                     |
| <span data-ttu-id="9a831-115">Size</span><span class="sxs-lookup"><span data-stu-id="9a831-115">Size</span></span>              | <span data-ttu-id="9a831-116">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="9a831-116">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="9a831-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="9a831-117">Update Privilege</span></span>  | <span data-ttu-id="9a831-118">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="9a831-118">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="9a831-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="9a831-119">Update Frequency</span></span>  | <span data-ttu-id="9a831-120">Wenn das Objekt Vorlage (MS-PKI-Certificate-template) bearbeitet, erstellt oder geklont wird.</span><span class="sxs-lookup"><span data-stu-id="9a831-120">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="9a831-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9a831-121">Attribute-Id</span></span>      | <span data-ttu-id="9a831-122">1.2.840.113556.1.4.1435</span><span class="sxs-lookup"><span data-stu-id="9a831-122">1.2.840.113556.1.4.1435</span></span>                                                                           |
| <span data-ttu-id="9a831-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9a831-123">System-Id-Guid</span></span>    | <span data-ttu-id="9a831-124">13F 5236c-1884-46b1-b5d0-484e38990d58</span><span class="sxs-lookup"><span data-stu-id="9a831-124">13f5236c-1884-46b1-b5d0-484e38990d58</span></span>                                                              |
| <span data-ttu-id="9a831-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a831-125">Syntax</span></span>            | [<span data-ttu-id="9a831-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="9a831-126">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="9a831-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="9a831-127">Implementations</span></span>

-   [<span data-ttu-id="9a831-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9a831-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9a831-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9a831-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9a831-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9a831-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9a831-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9a831-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9a831-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9a831-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9a831-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9a831-133">Windows Server 2003</span></span>



| <span data-ttu-id="9a831-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a831-134">Entry</span></span> | <span data-ttu-id="9a831-135">Wert</span><span class="sxs-lookup"><span data-stu-id="9a831-135">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9a831-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a831-136">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9a831-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a831-137">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9a831-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a831-138">System-Only</span></span>            | <span data-ttu-id="9a831-139">False</span><span class="sxs-lookup"><span data-stu-id="9a831-139">False</span></span>                                                                   |
| <span data-ttu-id="9a831-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a831-140">Is-Single-Valued</span></span>       | <span data-ttu-id="9a831-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a831-141">True</span></span>                                                                    |
| <span data-ttu-id="9a831-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a831-142">Is Indexed</span></span>             | <span data-ttu-id="9a831-143">False</span><span class="sxs-lookup"><span data-stu-id="9a831-143">False</span></span>                                                                   |
| <span data-ttu-id="9a831-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a831-144">In Global Catalog</span></span>      | <span data-ttu-id="9a831-145">False</span><span class="sxs-lookup"><span data-stu-id="9a831-145">False</span></span>                                                                   |
| <span data-ttu-id="9a831-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a831-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a831-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a831-147">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9a831-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a831-148">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9a831-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a831-149">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9a831-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a831-150">Search-Flags</span></span>           | <span data-ttu-id="9a831-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a831-151">0x00000000</span></span>                                                              |
| <span data-ttu-id="9a831-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a831-152">System-Flags</span></span>           | <span data-ttu-id="9a831-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a831-153">0x00000010</span></span>                                                              |
| <span data-ttu-id="9a831-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a831-154">Classes used in</span></span>        | [<span data-ttu-id="9a831-155">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="9a831-155">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9a831-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9a831-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9a831-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a831-157">Entry</span></span> | <span data-ttu-id="9a831-158">Wert</span><span class="sxs-lookup"><span data-stu-id="9a831-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9a831-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a831-159">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9a831-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a831-160">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9a831-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a831-161">System-Only</span></span>            | <span data-ttu-id="9a831-162">False</span><span class="sxs-lookup"><span data-stu-id="9a831-162">False</span></span>                                                                   |
| <span data-ttu-id="9a831-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a831-163">Is-Single-Valued</span></span>       | <span data-ttu-id="9a831-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a831-164">True</span></span>                                                                    |
| <span data-ttu-id="9a831-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a831-165">Is Indexed</span></span>             | <span data-ttu-id="9a831-166">False</span><span class="sxs-lookup"><span data-stu-id="9a831-166">False</span></span>                                                                   |
| <span data-ttu-id="9a831-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a831-167">In Global Catalog</span></span>      | <span data-ttu-id="9a831-168">False</span><span class="sxs-lookup"><span data-stu-id="9a831-168">False</span></span>                                                                   |
| <span data-ttu-id="9a831-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a831-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a831-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a831-170">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9a831-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a831-171">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9a831-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a831-172">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9a831-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a831-173">Search-Flags</span></span>           | <span data-ttu-id="9a831-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a831-174">0x00000000</span></span>                                                              |
| <span data-ttu-id="9a831-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a831-175">System-Flags</span></span>           | <span data-ttu-id="9a831-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a831-176">0x00000010</span></span>                                                              |
| <span data-ttu-id="9a831-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a831-177">Classes used in</span></span>        | [<span data-ttu-id="9a831-178">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="9a831-178">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9a831-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a831-179">Windows Server 2008</span></span>



| <span data-ttu-id="9a831-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a831-180">Entry</span></span> | <span data-ttu-id="9a831-181">Wert</span><span class="sxs-lookup"><span data-stu-id="9a831-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9a831-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a831-182">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9a831-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a831-183">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9a831-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a831-184">System-Only</span></span>            | <span data-ttu-id="9a831-185">False</span><span class="sxs-lookup"><span data-stu-id="9a831-185">False</span></span>                                                                   |
| <span data-ttu-id="9a831-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a831-186">Is-Single-Valued</span></span>       | <span data-ttu-id="9a831-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a831-187">True</span></span>                                                                    |
| <span data-ttu-id="9a831-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a831-188">Is Indexed</span></span>             | <span data-ttu-id="9a831-189">False</span><span class="sxs-lookup"><span data-stu-id="9a831-189">False</span></span>                                                                   |
| <span data-ttu-id="9a831-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a831-190">In Global Catalog</span></span>      | <span data-ttu-id="9a831-191">False</span><span class="sxs-lookup"><span data-stu-id="9a831-191">False</span></span>                                                                   |
| <span data-ttu-id="9a831-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a831-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a831-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a831-193">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9a831-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a831-194">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9a831-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a831-195">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9a831-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a831-196">Search-Flags</span></span>           | <span data-ttu-id="9a831-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a831-197">0x00000000</span></span>                                                              |
| <span data-ttu-id="9a831-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a831-198">System-Flags</span></span>           | <span data-ttu-id="9a831-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a831-199">0x00000010</span></span>                                                              |
| <span data-ttu-id="9a831-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a831-200">Classes used in</span></span>        | [<span data-ttu-id="9a831-201">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="9a831-201">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9a831-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9a831-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9a831-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a831-203">Entry</span></span> | <span data-ttu-id="9a831-204">Wert</span><span class="sxs-lookup"><span data-stu-id="9a831-204">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9a831-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a831-205">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9a831-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a831-206">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9a831-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a831-207">System-Only</span></span>            | <span data-ttu-id="9a831-208">False</span><span class="sxs-lookup"><span data-stu-id="9a831-208">False</span></span>                                                                   |
| <span data-ttu-id="9a831-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a831-209">Is-Single-Valued</span></span>       | <span data-ttu-id="9a831-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a831-210">True</span></span>                                                                    |
| <span data-ttu-id="9a831-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a831-211">Is Indexed</span></span>             | <span data-ttu-id="9a831-212">False</span><span class="sxs-lookup"><span data-stu-id="9a831-212">False</span></span>                                                                   |
| <span data-ttu-id="9a831-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a831-213">In Global Catalog</span></span>      | <span data-ttu-id="9a831-214">False</span><span class="sxs-lookup"><span data-stu-id="9a831-214">False</span></span>                                                                   |
| <span data-ttu-id="9a831-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a831-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a831-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a831-216">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9a831-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a831-217">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9a831-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a831-218">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9a831-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a831-219">Search-Flags</span></span>           | <span data-ttu-id="9a831-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a831-220">0x00000000</span></span>                                                              |
| <span data-ttu-id="9a831-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a831-221">System-Flags</span></span>           | <span data-ttu-id="9a831-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a831-222">0x00000010</span></span>                                                              |
| <span data-ttu-id="9a831-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a831-223">Classes used in</span></span>        | [<span data-ttu-id="9a831-224">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="9a831-224">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9a831-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9a831-225">Windows Server 2012</span></span>



| <span data-ttu-id="9a831-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a831-226">Entry</span></span> | <span data-ttu-id="9a831-227">Wert</span><span class="sxs-lookup"><span data-stu-id="9a831-227">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9a831-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a831-228">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9a831-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a831-229">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9a831-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a831-230">System-Only</span></span>            | <span data-ttu-id="9a831-231">False</span><span class="sxs-lookup"><span data-stu-id="9a831-231">False</span></span>                                                                   |
| <span data-ttu-id="9a831-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a831-232">Is-Single-Valued</span></span>       | <span data-ttu-id="9a831-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a831-233">True</span></span>                                                                    |
| <span data-ttu-id="9a831-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a831-234">Is Indexed</span></span>             | <span data-ttu-id="9a831-235">False</span><span class="sxs-lookup"><span data-stu-id="9a831-235">False</span></span>                                                                   |
| <span data-ttu-id="9a831-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a831-236">In Global Catalog</span></span>      | <span data-ttu-id="9a831-237">False</span><span class="sxs-lookup"><span data-stu-id="9a831-237">False</span></span>                                                                   |
| <span data-ttu-id="9a831-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a831-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a831-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a831-239">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9a831-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a831-240">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9a831-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a831-241">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9a831-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a831-242">Search-Flags</span></span>           | <span data-ttu-id="9a831-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a831-243">0x00000000</span></span>                                                              |
| <span data-ttu-id="9a831-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a831-244">System-Flags</span></span>           | <span data-ttu-id="9a831-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a831-245">0x00000010</span></span>                                                              |
| <span data-ttu-id="9a831-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a831-246">Classes used in</span></span>        | [<span data-ttu-id="9a831-247">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="9a831-247">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





