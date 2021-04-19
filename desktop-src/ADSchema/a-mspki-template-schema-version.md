---
title: MS-PKI-Template-Schema-Version-Attribut
description: Verfolgt Schema Aktualisierungen der PKI-Certificate-Template-Klasse.
ms.assetid: 7ad55f1a-cdb9-4eea-bd09-db4f5e6373ba
ms.tgt_platform: multiple
keywords:
- MS-PKI-Template-Schema-Version-Attribut AD-Schema
- mspki-Template-Schema-Version-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-PKI-Template-Schema-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc3b7952b55b346da29119775bb9c0f8b825c50
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106345368"
---
# <a name="ms-pki-template-schema-version-attribute"></a><span data-ttu-id="fb354-105">MS-PKI-Template-Schema-Version-Attribut</span><span class="sxs-lookup"><span data-stu-id="fb354-105">ms-PKI-Template-Schema-Version attribute</span></span>

<span data-ttu-id="fb354-106">Verfolgt Schema Aktualisierungen der PKI-Certificate-Template-Klasse.</span><span class="sxs-lookup"><span data-stu-id="fb354-106">Keeps track of schema updates of the PKI-Certificate-Template class.</span></span>



| <span data-ttu-id="fb354-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fb354-107">Entry</span></span> | <span data-ttu-id="fb354-108">Wert</span><span class="sxs-lookup"><span data-stu-id="fb354-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb354-109">CN</span><span class="sxs-lookup"><span data-stu-id="fb354-109">CN</span></span>                | <span data-ttu-id="fb354-110">MS-PKI-Template-Schema-Version</span><span class="sxs-lookup"><span data-stu-id="fb354-110">ms-PKI-Template-Schema-Version</span></span>                                                                    |
| <span data-ttu-id="fb354-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fb354-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fb354-112">mspki-Template-Schema-Version</span><span class="sxs-lookup"><span data-stu-id="fb354-112">msPKI-Template-Schema-Version</span></span>                                                                     |
| <span data-ttu-id="fb354-113">Size</span><span class="sxs-lookup"><span data-stu-id="fb354-113">Size</span></span>              | <span data-ttu-id="fb354-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="fb354-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="fb354-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="fb354-115">Update Privilege</span></span>  | <span data-ttu-id="fb354-116">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="fb354-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="fb354-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="fb354-117">Update Frequency</span></span>  | <span data-ttu-id="fb354-118">Wenn das Objekt Vorlage (MS-PKI-Certificate-template) bearbeitet, erstellt oder geklont wird.</span><span class="sxs-lookup"><span data-stu-id="fb354-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="fb354-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fb354-119">Attribute-Id</span></span>      | <span data-ttu-id="fb354-120">1.2.840.113556.1.4.1434</span><span class="sxs-lookup"><span data-stu-id="fb354-120">1.2.840.113556.1.4.1434</span></span>                                                                           |
| <span data-ttu-id="fb354-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fb354-121">System-Id-Guid</span></span>    | <span data-ttu-id="fb354-122">0c15e9f 5-491d-4594-918 a091da9</span><span class="sxs-lookup"><span data-stu-id="fb354-122">0c15e9f5-491d-4594-918f-32813a091da9</span></span>                                                              |
| <span data-ttu-id="fb354-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb354-123">Syntax</span></span>            | [<span data-ttu-id="fb354-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="fb354-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="fb354-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="fb354-125">Implementations</span></span>

-   [<span data-ttu-id="fb354-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fb354-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fb354-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fb354-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fb354-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fb354-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fb354-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fb354-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fb354-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fb354-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="fb354-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fb354-131">Windows Server 2003</span></span>



| <span data-ttu-id="fb354-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fb354-132">Entry</span></span> | <span data-ttu-id="fb354-133">Wert</span><span class="sxs-lookup"><span data-stu-id="fb354-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fb354-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fb354-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fb354-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fb354-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fb354-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="fb354-136">System-Only</span></span>            | <span data-ttu-id="fb354-137">False</span><span class="sxs-lookup"><span data-stu-id="fb354-137">False</span></span>                                                                   |
| <span data-ttu-id="fb354-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fb354-138">Is-Single-Valued</span></span>       | <span data-ttu-id="fb354-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="fb354-139">True</span></span>                                                                    |
| <span data-ttu-id="fb354-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fb354-140">Is Indexed</span></span>             | <span data-ttu-id="fb354-141">False</span><span class="sxs-lookup"><span data-stu-id="fb354-141">False</span></span>                                                                   |
| <span data-ttu-id="fb354-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fb354-142">In Global Catalog</span></span>      | <span data-ttu-id="fb354-143">False</span><span class="sxs-lookup"><span data-stu-id="fb354-143">False</span></span>                                                                   |
| <span data-ttu-id="fb354-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fb354-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="fb354-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fb354-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="fb354-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fb354-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="fb354-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fb354-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="fb354-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fb354-148">Search-Flags</span></span>           | <span data-ttu-id="fb354-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fb354-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="fb354-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fb354-150">System-Flags</span></span>           | <span data-ttu-id="fb354-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fb354-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="fb354-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fb354-152">Classes used in</span></span>        | [<span data-ttu-id="fb354-153">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="fb354-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fb354-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fb354-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fb354-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fb354-155">Entry</span></span> | <span data-ttu-id="fb354-156">Wert</span><span class="sxs-lookup"><span data-stu-id="fb354-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fb354-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fb354-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fb354-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fb354-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fb354-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="fb354-159">System-Only</span></span>            | <span data-ttu-id="fb354-160">False</span><span class="sxs-lookup"><span data-stu-id="fb354-160">False</span></span>                                                                   |
| <span data-ttu-id="fb354-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fb354-161">Is-Single-Valued</span></span>       | <span data-ttu-id="fb354-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="fb354-162">True</span></span>                                                                    |
| <span data-ttu-id="fb354-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fb354-163">Is Indexed</span></span>             | <span data-ttu-id="fb354-164">False</span><span class="sxs-lookup"><span data-stu-id="fb354-164">False</span></span>                                                                   |
| <span data-ttu-id="fb354-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fb354-165">In Global Catalog</span></span>      | <span data-ttu-id="fb354-166">False</span><span class="sxs-lookup"><span data-stu-id="fb354-166">False</span></span>                                                                   |
| <span data-ttu-id="fb354-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fb354-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="fb354-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fb354-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="fb354-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fb354-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="fb354-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fb354-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="fb354-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fb354-171">Search-Flags</span></span>           | <span data-ttu-id="fb354-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fb354-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="fb354-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fb354-173">System-Flags</span></span>           | <span data-ttu-id="fb354-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fb354-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="fb354-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fb354-175">Classes used in</span></span>        | [<span data-ttu-id="fb354-176">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="fb354-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fb354-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb354-177">Windows Server 2008</span></span>



| <span data-ttu-id="fb354-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fb354-178">Entry</span></span> | <span data-ttu-id="fb354-179">Wert</span><span class="sxs-lookup"><span data-stu-id="fb354-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fb354-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fb354-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fb354-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fb354-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fb354-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="fb354-182">System-Only</span></span>            | <span data-ttu-id="fb354-183">False</span><span class="sxs-lookup"><span data-stu-id="fb354-183">False</span></span>                                                                   |
| <span data-ttu-id="fb354-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fb354-184">Is-Single-Valued</span></span>       | <span data-ttu-id="fb354-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="fb354-185">True</span></span>                                                                    |
| <span data-ttu-id="fb354-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fb354-186">Is Indexed</span></span>             | <span data-ttu-id="fb354-187">False</span><span class="sxs-lookup"><span data-stu-id="fb354-187">False</span></span>                                                                   |
| <span data-ttu-id="fb354-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fb354-188">In Global Catalog</span></span>      | <span data-ttu-id="fb354-189">False</span><span class="sxs-lookup"><span data-stu-id="fb354-189">False</span></span>                                                                   |
| <span data-ttu-id="fb354-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fb354-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="fb354-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fb354-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="fb354-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fb354-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="fb354-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fb354-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="fb354-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fb354-194">Search-Flags</span></span>           | <span data-ttu-id="fb354-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fb354-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="fb354-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fb354-196">System-Flags</span></span>           | <span data-ttu-id="fb354-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fb354-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="fb354-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fb354-198">Classes used in</span></span>        | [<span data-ttu-id="fb354-199">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="fb354-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fb354-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fb354-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fb354-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fb354-201">Entry</span></span> | <span data-ttu-id="fb354-202">Wert</span><span class="sxs-lookup"><span data-stu-id="fb354-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fb354-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fb354-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fb354-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fb354-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fb354-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="fb354-205">System-Only</span></span>            | <span data-ttu-id="fb354-206">False</span><span class="sxs-lookup"><span data-stu-id="fb354-206">False</span></span>                                                                   |
| <span data-ttu-id="fb354-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fb354-207">Is-Single-Valued</span></span>       | <span data-ttu-id="fb354-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="fb354-208">True</span></span>                                                                    |
| <span data-ttu-id="fb354-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fb354-209">Is Indexed</span></span>             | <span data-ttu-id="fb354-210">False</span><span class="sxs-lookup"><span data-stu-id="fb354-210">False</span></span>                                                                   |
| <span data-ttu-id="fb354-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fb354-211">In Global Catalog</span></span>      | <span data-ttu-id="fb354-212">False</span><span class="sxs-lookup"><span data-stu-id="fb354-212">False</span></span>                                                                   |
| <span data-ttu-id="fb354-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fb354-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="fb354-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fb354-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="fb354-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fb354-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="fb354-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fb354-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="fb354-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fb354-217">Search-Flags</span></span>           | <span data-ttu-id="fb354-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fb354-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="fb354-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fb354-219">System-Flags</span></span>           | <span data-ttu-id="fb354-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fb354-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="fb354-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fb354-221">Classes used in</span></span>        | [<span data-ttu-id="fb354-222">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="fb354-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fb354-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fb354-223">Windows Server 2012</span></span>



| <span data-ttu-id="fb354-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fb354-224">Entry</span></span> | <span data-ttu-id="fb354-225">Wert</span><span class="sxs-lookup"><span data-stu-id="fb354-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fb354-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fb354-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fb354-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fb354-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fb354-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="fb354-228">System-Only</span></span>            | <span data-ttu-id="fb354-229">False</span><span class="sxs-lookup"><span data-stu-id="fb354-229">False</span></span>                                                                   |
| <span data-ttu-id="fb354-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fb354-230">Is-Single-Valued</span></span>       | <span data-ttu-id="fb354-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="fb354-231">True</span></span>                                                                    |
| <span data-ttu-id="fb354-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fb354-232">Is Indexed</span></span>             | <span data-ttu-id="fb354-233">False</span><span class="sxs-lookup"><span data-stu-id="fb354-233">False</span></span>                                                                   |
| <span data-ttu-id="fb354-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fb354-234">In Global Catalog</span></span>      | <span data-ttu-id="fb354-235">False</span><span class="sxs-lookup"><span data-stu-id="fb354-235">False</span></span>                                                                   |
| <span data-ttu-id="fb354-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fb354-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="fb354-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fb354-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="fb354-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fb354-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="fb354-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fb354-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="fb354-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fb354-240">Search-Flags</span></span>           | <span data-ttu-id="fb354-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fb354-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="fb354-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fb354-242">System-Flags</span></span>           | <span data-ttu-id="fb354-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fb354-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="fb354-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fb354-244">Classes used in</span></span>        | [<span data-ttu-id="fb354-245">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="fb354-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





