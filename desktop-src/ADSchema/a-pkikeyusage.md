---
title: PKI-Schlüssel-Usage-Attribut
description: Die Schlüssel Verwendungs Erweiterung für die Zertifikat Vorlage.
ms.assetid: 9b3bb28e-7519-4911-9777-f9612bff2d51
ms.tgt_platform: multiple
keywords:
- PKI-Schlüssel-Verwendung-Attribut AD-Schema
- pkikeyusage-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- PKI-Key-Usage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08c5c5b72091060fb475f3becba4f230293c875
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859589"
---
# <a name="pki-key-usage-attribute"></a><span data-ttu-id="350ec-105">PKI-Schlüssel-Usage-Attribut</span><span class="sxs-lookup"><span data-stu-id="350ec-105">PKI-Key-Usage attribute</span></span>

<span data-ttu-id="350ec-106">Die Schlüssel Verwendungs Erweiterung für die Zertifikat Vorlage.</span><span class="sxs-lookup"><span data-stu-id="350ec-106">The key usage extension for the certificate template.</span></span>



| <span data-ttu-id="350ec-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="350ec-107">Entry</span></span> | <span data-ttu-id="350ec-108">Wert</span><span class="sxs-lookup"><span data-stu-id="350ec-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="350ec-109">CN</span><span class="sxs-lookup"><span data-stu-id="350ec-109">CN</span></span>                | <span data-ttu-id="350ec-110">PKI-Schlüssel-Verwendung</span><span class="sxs-lookup"><span data-stu-id="350ec-110">PKI-Key-Usage</span></span>                                         |
| <span data-ttu-id="350ec-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="350ec-111">Ldap-Display-Name</span></span> | <span data-ttu-id="350ec-112">pkikeyusage</span><span class="sxs-lookup"><span data-stu-id="350ec-112">pKIKeyUsage</span></span>                                           |
| <span data-ttu-id="350ec-113">Size</span><span class="sxs-lookup"><span data-stu-id="350ec-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="350ec-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="350ec-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="350ec-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="350ec-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="350ec-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="350ec-116">Attribute-Id</span></span>      | <span data-ttu-id="350ec-117">1.2.840.113556.1.4.1328</span><span class="sxs-lookup"><span data-stu-id="350ec-117">1.2.840.113556.1.4.1328</span></span>                               |
| <span data-ttu-id="350ec-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="350ec-118">System-Id-Guid</span></span>    | <span data-ttu-id="350ec-119">e9b0a87e-3b9d-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="350ec-119">e9b0a87e-3b9d-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="350ec-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="350ec-120">Syntax</span></span>            | [<span data-ttu-id="350ec-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="350ec-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="350ec-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="350ec-122">Implementations</span></span>

-   [<span data-ttu-id="350ec-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="350ec-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="350ec-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="350ec-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="350ec-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="350ec-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="350ec-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="350ec-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="350ec-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="350ec-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="350ec-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="350ec-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="350ec-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="350ec-129">Windows 2000 Server</span></span>



| <span data-ttu-id="350ec-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="350ec-130">Entry</span></span> | <span data-ttu-id="350ec-131">Wert</span><span class="sxs-lookup"><span data-stu-id="350ec-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="350ec-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="350ec-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="350ec-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="350ec-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="350ec-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="350ec-134">System-Only</span></span>            | <span data-ttu-id="350ec-135">False</span><span class="sxs-lookup"><span data-stu-id="350ec-135">False</span></span>                                                                   |
| <span data-ttu-id="350ec-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="350ec-136">Is-Single-Valued</span></span>       | <span data-ttu-id="350ec-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="350ec-137">True</span></span>                                                                    |
| <span data-ttu-id="350ec-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="350ec-138">Is Indexed</span></span>             | <span data-ttu-id="350ec-139">False</span><span class="sxs-lookup"><span data-stu-id="350ec-139">False</span></span>                                                                   |
| <span data-ttu-id="350ec-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="350ec-140">In Global Catalog</span></span>      | <span data-ttu-id="350ec-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="350ec-141">True</span></span>                                                                    |
| <span data-ttu-id="350ec-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="350ec-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="350ec-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="350ec-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="350ec-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="350ec-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="350ec-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="350ec-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="350ec-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="350ec-146">Search-Flags</span></span>           | <span data-ttu-id="350ec-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="350ec-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="350ec-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="350ec-148">System-Flags</span></span>           | <span data-ttu-id="350ec-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="350ec-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="350ec-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="350ec-150">Classes used in</span></span>        | [<span data-ttu-id="350ec-151">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="350ec-151">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="350ec-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="350ec-152">Windows Server 2003</span></span>



| <span data-ttu-id="350ec-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="350ec-153">Entry</span></span> | <span data-ttu-id="350ec-154">Wert</span><span class="sxs-lookup"><span data-stu-id="350ec-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="350ec-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="350ec-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="350ec-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="350ec-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="350ec-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="350ec-157">System-Only</span></span>            | <span data-ttu-id="350ec-158">False</span><span class="sxs-lookup"><span data-stu-id="350ec-158">False</span></span>                                                                   |
| <span data-ttu-id="350ec-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="350ec-159">Is-Single-Valued</span></span>       | <span data-ttu-id="350ec-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="350ec-160">True</span></span>                                                                    |
| <span data-ttu-id="350ec-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="350ec-161">Is Indexed</span></span>             | <span data-ttu-id="350ec-162">False</span><span class="sxs-lookup"><span data-stu-id="350ec-162">False</span></span>                                                                   |
| <span data-ttu-id="350ec-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="350ec-163">In Global Catalog</span></span>      | <span data-ttu-id="350ec-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="350ec-164">True</span></span>                                                                    |
| <span data-ttu-id="350ec-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="350ec-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="350ec-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="350ec-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="350ec-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="350ec-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="350ec-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="350ec-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="350ec-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="350ec-169">Search-Flags</span></span>           | <span data-ttu-id="350ec-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="350ec-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="350ec-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="350ec-171">System-Flags</span></span>           | <span data-ttu-id="350ec-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="350ec-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="350ec-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="350ec-173">Classes used in</span></span>        | [<span data-ttu-id="350ec-174">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="350ec-174">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="350ec-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="350ec-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="350ec-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="350ec-176">Entry</span></span> | <span data-ttu-id="350ec-177">Wert</span><span class="sxs-lookup"><span data-stu-id="350ec-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="350ec-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="350ec-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="350ec-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="350ec-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="350ec-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="350ec-180">System-Only</span></span>            | <span data-ttu-id="350ec-181">False</span><span class="sxs-lookup"><span data-stu-id="350ec-181">False</span></span>                                                                   |
| <span data-ttu-id="350ec-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="350ec-182">Is-Single-Valued</span></span>       | <span data-ttu-id="350ec-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="350ec-183">True</span></span>                                                                    |
| <span data-ttu-id="350ec-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="350ec-184">Is Indexed</span></span>             | <span data-ttu-id="350ec-185">False</span><span class="sxs-lookup"><span data-stu-id="350ec-185">False</span></span>                                                                   |
| <span data-ttu-id="350ec-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="350ec-186">In Global Catalog</span></span>      | <span data-ttu-id="350ec-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="350ec-187">True</span></span>                                                                    |
| <span data-ttu-id="350ec-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="350ec-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="350ec-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="350ec-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="350ec-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="350ec-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="350ec-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="350ec-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="350ec-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="350ec-192">Search-Flags</span></span>           | <span data-ttu-id="350ec-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="350ec-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="350ec-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="350ec-194">System-Flags</span></span>           | <span data-ttu-id="350ec-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="350ec-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="350ec-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="350ec-196">Classes used in</span></span>        | [<span data-ttu-id="350ec-197">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="350ec-197">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="350ec-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="350ec-198">Windows Server 2008</span></span>



| <span data-ttu-id="350ec-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="350ec-199">Entry</span></span> | <span data-ttu-id="350ec-200">Wert</span><span class="sxs-lookup"><span data-stu-id="350ec-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="350ec-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="350ec-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="350ec-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="350ec-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="350ec-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="350ec-203">System-Only</span></span>            | <span data-ttu-id="350ec-204">False</span><span class="sxs-lookup"><span data-stu-id="350ec-204">False</span></span>                                                                   |
| <span data-ttu-id="350ec-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="350ec-205">Is-Single-Valued</span></span>       | <span data-ttu-id="350ec-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="350ec-206">True</span></span>                                                                    |
| <span data-ttu-id="350ec-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="350ec-207">Is Indexed</span></span>             | <span data-ttu-id="350ec-208">False</span><span class="sxs-lookup"><span data-stu-id="350ec-208">False</span></span>                                                                   |
| <span data-ttu-id="350ec-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="350ec-209">In Global Catalog</span></span>      | <span data-ttu-id="350ec-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="350ec-210">True</span></span>                                                                    |
| <span data-ttu-id="350ec-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="350ec-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="350ec-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="350ec-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="350ec-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="350ec-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="350ec-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="350ec-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="350ec-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="350ec-215">Search-Flags</span></span>           | <span data-ttu-id="350ec-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="350ec-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="350ec-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="350ec-217">System-Flags</span></span>           | <span data-ttu-id="350ec-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="350ec-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="350ec-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="350ec-219">Classes used in</span></span>        | [<span data-ttu-id="350ec-220">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="350ec-220">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="350ec-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="350ec-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="350ec-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="350ec-222">Entry</span></span> | <span data-ttu-id="350ec-223">Wert</span><span class="sxs-lookup"><span data-stu-id="350ec-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="350ec-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="350ec-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="350ec-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="350ec-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="350ec-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="350ec-226">System-Only</span></span>            | <span data-ttu-id="350ec-227">False</span><span class="sxs-lookup"><span data-stu-id="350ec-227">False</span></span>                                                                   |
| <span data-ttu-id="350ec-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="350ec-228">Is-Single-Valued</span></span>       | <span data-ttu-id="350ec-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="350ec-229">True</span></span>                                                                    |
| <span data-ttu-id="350ec-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="350ec-230">Is Indexed</span></span>             | <span data-ttu-id="350ec-231">False</span><span class="sxs-lookup"><span data-stu-id="350ec-231">False</span></span>                                                                   |
| <span data-ttu-id="350ec-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="350ec-232">In Global Catalog</span></span>      | <span data-ttu-id="350ec-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="350ec-233">True</span></span>                                                                    |
| <span data-ttu-id="350ec-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="350ec-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="350ec-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="350ec-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="350ec-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="350ec-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="350ec-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="350ec-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="350ec-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="350ec-238">Search-Flags</span></span>           | <span data-ttu-id="350ec-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="350ec-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="350ec-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="350ec-240">System-Flags</span></span>           | <span data-ttu-id="350ec-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="350ec-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="350ec-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="350ec-242">Classes used in</span></span>        | [<span data-ttu-id="350ec-243">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="350ec-243">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="350ec-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="350ec-244">Windows Server 2012</span></span>



| <span data-ttu-id="350ec-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="350ec-245">Entry</span></span> | <span data-ttu-id="350ec-246">Wert</span><span class="sxs-lookup"><span data-stu-id="350ec-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="350ec-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="350ec-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="350ec-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="350ec-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="350ec-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="350ec-249">System-Only</span></span>            | <span data-ttu-id="350ec-250">False</span><span class="sxs-lookup"><span data-stu-id="350ec-250">False</span></span>                                                                   |
| <span data-ttu-id="350ec-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="350ec-251">Is-Single-Valued</span></span>       | <span data-ttu-id="350ec-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="350ec-252">True</span></span>                                                                    |
| <span data-ttu-id="350ec-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="350ec-253">Is Indexed</span></span>             | <span data-ttu-id="350ec-254">False</span><span class="sxs-lookup"><span data-stu-id="350ec-254">False</span></span>                                                                   |
| <span data-ttu-id="350ec-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="350ec-255">In Global Catalog</span></span>      | <span data-ttu-id="350ec-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="350ec-256">True</span></span>                                                                    |
| <span data-ttu-id="350ec-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="350ec-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="350ec-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="350ec-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="350ec-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="350ec-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="350ec-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="350ec-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="350ec-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="350ec-261">Search-Flags</span></span>           | <span data-ttu-id="350ec-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="350ec-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="350ec-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="350ec-263">System-Flags</span></span>           | <span data-ttu-id="350ec-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="350ec-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="350ec-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="350ec-265">Classes used in</span></span>        | [<span data-ttu-id="350ec-266">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="350ec-266">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





