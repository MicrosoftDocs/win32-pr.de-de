---
title: MS-PKI-Certificate-Name-Flag-Attribut
description: Enthält die Flags, die sich auf das Erstellen des Antragsteller namens in einem ausgestellten Zertifikat beziehen.
ms.assetid: 7aeeff69-86b5-4251-bd64-bd99b7c9ef4a
ms.tgt_platform: multiple
keywords:
- "\"MS-PKI-Certificate-Name-Flag\"-Attribut AD-Schema"
- "\"mspki-Certificate-Name-Flag\"-Attribut AD-Schema"
topic_type:
- apiref
api_name:
- ms-PKI-Certificate-Name-Flag
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a9a5f8d6db36c3e3b86945fa529572df38ff6df
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392302"
---
# <a name="ms-pki-certificate-name-flag-attribute"></a><span data-ttu-id="e42ad-105">MS-PKI-Certificate-Name-Flag-Attribut</span><span class="sxs-lookup"><span data-stu-id="e42ad-105">ms-PKI-Certificate-Name-Flag attribute</span></span>

<span data-ttu-id="e42ad-106">Enthält die Flags, die sich auf das Erstellen des Antragsteller namens in einem ausgestellten Zertifikat beziehen.</span><span class="sxs-lookup"><span data-stu-id="e42ad-106">Contains the flags related to constructing the subject name in an issued certificate.</span></span>



| <span data-ttu-id="e42ad-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e42ad-107">Entry</span></span> | <span data-ttu-id="e42ad-108">Wert</span><span class="sxs-lookup"><span data-stu-id="e42ad-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e42ad-109">CN</span><span class="sxs-lookup"><span data-stu-id="e42ad-109">CN</span></span>                | <span data-ttu-id="e42ad-110">MS-PKI-Certificate-Name-Flag</span><span class="sxs-lookup"><span data-stu-id="e42ad-110">ms-PKI-Certificate-Name-Flag</span></span>                                                                      |
| <span data-ttu-id="e42ad-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e42ad-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e42ad-112">mspki-Certificate-Name-Flag</span><span class="sxs-lookup"><span data-stu-id="e42ad-112">msPKI-Certificate-Name-Flag</span></span>                                                                       |
| <span data-ttu-id="e42ad-113">Size</span><span class="sxs-lookup"><span data-stu-id="e42ad-113">Size</span></span>              | <span data-ttu-id="e42ad-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="e42ad-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="e42ad-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e42ad-115">Update Privilege</span></span>  | <span data-ttu-id="e42ad-116">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="e42ad-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="e42ad-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="e42ad-117">Update Frequency</span></span>  | <span data-ttu-id="e42ad-118">Wenn das Objekt Vorlage (MS-PKI-Certificate-template) bearbeitet, erstellt oder geklont wird.</span><span class="sxs-lookup"><span data-stu-id="e42ad-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="e42ad-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e42ad-119">Attribute-Id</span></span>      | <span data-ttu-id="e42ad-120">1.2.840.113556.1.4.1432</span><span class="sxs-lookup"><span data-stu-id="e42ad-120">1.2.840.113556.1.4.1432</span></span>                                                                           |
| <span data-ttu-id="e42ad-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e42ad-121">System-Id-Guid</span></span>    | <span data-ttu-id="e42ad-122">ea1dddc4-60ff-416e-8cc0-17cee534bce7</span><span class="sxs-lookup"><span data-stu-id="e42ad-122">ea1dddc4-60ff-416e-8cc0-17cee534bce7</span></span>                                                              |
| <span data-ttu-id="e42ad-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="e42ad-123">Syntax</span></span>            | [<span data-ttu-id="e42ad-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="e42ad-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="e42ad-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="e42ad-125">Implementations</span></span>

-   [<span data-ttu-id="e42ad-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e42ad-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e42ad-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e42ad-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e42ad-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e42ad-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e42ad-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e42ad-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e42ad-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e42ad-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e42ad-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e42ad-131">Windows Server 2003</span></span>



| <span data-ttu-id="e42ad-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e42ad-132">Entry</span></span> | <span data-ttu-id="e42ad-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e42ad-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e42ad-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e42ad-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e42ad-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e42ad-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e42ad-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e42ad-136">System-Only</span></span>            | <span data-ttu-id="e42ad-137">False</span><span class="sxs-lookup"><span data-stu-id="e42ad-137">False</span></span>                                                                   |
| <span data-ttu-id="e42ad-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e42ad-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e42ad-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="e42ad-139">True</span></span>                                                                    |
| <span data-ttu-id="e42ad-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e42ad-140">Is Indexed</span></span>             | <span data-ttu-id="e42ad-141">False</span><span class="sxs-lookup"><span data-stu-id="e42ad-141">False</span></span>                                                                   |
| <span data-ttu-id="e42ad-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e42ad-142">In Global Catalog</span></span>      | <span data-ttu-id="e42ad-143">False</span><span class="sxs-lookup"><span data-stu-id="e42ad-143">False</span></span>                                                                   |
| <span data-ttu-id="e42ad-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e42ad-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e42ad-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e42ad-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e42ad-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e42ad-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e42ad-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e42ad-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e42ad-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e42ad-148">Search-Flags</span></span>           | <span data-ttu-id="e42ad-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e42ad-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="e42ad-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e42ad-150">System-Flags</span></span>           | <span data-ttu-id="e42ad-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e42ad-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="e42ad-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e42ad-152">Classes used in</span></span>        | [<span data-ttu-id="e42ad-153">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="e42ad-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e42ad-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e42ad-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e42ad-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e42ad-155">Entry</span></span> | <span data-ttu-id="e42ad-156">Wert</span><span class="sxs-lookup"><span data-stu-id="e42ad-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e42ad-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e42ad-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e42ad-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e42ad-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e42ad-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e42ad-159">System-Only</span></span>            | <span data-ttu-id="e42ad-160">False</span><span class="sxs-lookup"><span data-stu-id="e42ad-160">False</span></span>                                                                   |
| <span data-ttu-id="e42ad-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e42ad-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e42ad-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="e42ad-162">True</span></span>                                                                    |
| <span data-ttu-id="e42ad-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e42ad-163">Is Indexed</span></span>             | <span data-ttu-id="e42ad-164">False</span><span class="sxs-lookup"><span data-stu-id="e42ad-164">False</span></span>                                                                   |
| <span data-ttu-id="e42ad-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e42ad-165">In Global Catalog</span></span>      | <span data-ttu-id="e42ad-166">False</span><span class="sxs-lookup"><span data-stu-id="e42ad-166">False</span></span>                                                                   |
| <span data-ttu-id="e42ad-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e42ad-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e42ad-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e42ad-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e42ad-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e42ad-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e42ad-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e42ad-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e42ad-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e42ad-171">Search-Flags</span></span>           | <span data-ttu-id="e42ad-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e42ad-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="e42ad-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e42ad-173">System-Flags</span></span>           | <span data-ttu-id="e42ad-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e42ad-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="e42ad-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e42ad-175">Classes used in</span></span>        | [<span data-ttu-id="e42ad-176">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="e42ad-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e42ad-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e42ad-177">Windows Server 2008</span></span>



| <span data-ttu-id="e42ad-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e42ad-178">Entry</span></span> | <span data-ttu-id="e42ad-179">Wert</span><span class="sxs-lookup"><span data-stu-id="e42ad-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e42ad-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e42ad-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e42ad-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e42ad-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e42ad-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e42ad-182">System-Only</span></span>            | <span data-ttu-id="e42ad-183">False</span><span class="sxs-lookup"><span data-stu-id="e42ad-183">False</span></span>                                                                   |
| <span data-ttu-id="e42ad-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e42ad-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e42ad-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="e42ad-185">True</span></span>                                                                    |
| <span data-ttu-id="e42ad-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e42ad-186">Is Indexed</span></span>             | <span data-ttu-id="e42ad-187">False</span><span class="sxs-lookup"><span data-stu-id="e42ad-187">False</span></span>                                                                   |
| <span data-ttu-id="e42ad-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e42ad-188">In Global Catalog</span></span>      | <span data-ttu-id="e42ad-189">False</span><span class="sxs-lookup"><span data-stu-id="e42ad-189">False</span></span>                                                                   |
| <span data-ttu-id="e42ad-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e42ad-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e42ad-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e42ad-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e42ad-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e42ad-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e42ad-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e42ad-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e42ad-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e42ad-194">Search-Flags</span></span>           | <span data-ttu-id="e42ad-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e42ad-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="e42ad-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e42ad-196">System-Flags</span></span>           | <span data-ttu-id="e42ad-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e42ad-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="e42ad-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e42ad-198">Classes used in</span></span>        | [<span data-ttu-id="e42ad-199">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="e42ad-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e42ad-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e42ad-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e42ad-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e42ad-201">Entry</span></span> | <span data-ttu-id="e42ad-202">Wert</span><span class="sxs-lookup"><span data-stu-id="e42ad-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e42ad-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e42ad-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e42ad-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e42ad-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e42ad-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e42ad-205">System-Only</span></span>            | <span data-ttu-id="e42ad-206">False</span><span class="sxs-lookup"><span data-stu-id="e42ad-206">False</span></span>                                                                   |
| <span data-ttu-id="e42ad-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e42ad-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e42ad-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="e42ad-208">True</span></span>                                                                    |
| <span data-ttu-id="e42ad-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e42ad-209">Is Indexed</span></span>             | <span data-ttu-id="e42ad-210">False</span><span class="sxs-lookup"><span data-stu-id="e42ad-210">False</span></span>                                                                   |
| <span data-ttu-id="e42ad-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e42ad-211">In Global Catalog</span></span>      | <span data-ttu-id="e42ad-212">False</span><span class="sxs-lookup"><span data-stu-id="e42ad-212">False</span></span>                                                                   |
| <span data-ttu-id="e42ad-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e42ad-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e42ad-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e42ad-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e42ad-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e42ad-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e42ad-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e42ad-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e42ad-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e42ad-217">Search-Flags</span></span>           | <span data-ttu-id="e42ad-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e42ad-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="e42ad-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e42ad-219">System-Flags</span></span>           | <span data-ttu-id="e42ad-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e42ad-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="e42ad-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e42ad-221">Classes used in</span></span>        | [<span data-ttu-id="e42ad-222">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="e42ad-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e42ad-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e42ad-223">Windows Server 2012</span></span>



| <span data-ttu-id="e42ad-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e42ad-224">Entry</span></span> | <span data-ttu-id="e42ad-225">Wert</span><span class="sxs-lookup"><span data-stu-id="e42ad-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e42ad-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e42ad-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e42ad-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e42ad-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e42ad-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e42ad-228">System-Only</span></span>            | <span data-ttu-id="e42ad-229">False</span><span class="sxs-lookup"><span data-stu-id="e42ad-229">False</span></span>                                                                   |
| <span data-ttu-id="e42ad-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e42ad-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e42ad-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="e42ad-231">True</span></span>                                                                    |
| <span data-ttu-id="e42ad-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e42ad-232">Is Indexed</span></span>             | <span data-ttu-id="e42ad-233">False</span><span class="sxs-lookup"><span data-stu-id="e42ad-233">False</span></span>                                                                   |
| <span data-ttu-id="e42ad-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e42ad-234">In Global Catalog</span></span>      | <span data-ttu-id="e42ad-235">False</span><span class="sxs-lookup"><span data-stu-id="e42ad-235">False</span></span>                                                                   |
| <span data-ttu-id="e42ad-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e42ad-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e42ad-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e42ad-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e42ad-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e42ad-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e42ad-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e42ad-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e42ad-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e42ad-240">Search-Flags</span></span>           | <span data-ttu-id="e42ad-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e42ad-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="e42ad-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e42ad-242">System-Flags</span></span>           | <span data-ttu-id="e42ad-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e42ad-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="e42ad-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e42ad-244">Classes used in</span></span>        | [<span data-ttu-id="e42ad-245">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="e42ad-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





