---
title: MS-PKI-Minimum-Key-size-Attribut
description: Gibt die minimale Größe des privaten Schlüssels an.
ms.assetid: e38fbab5-14db-40d1-80c4-c14477c6f0da
ms.tgt_platform: multiple
keywords:
- MS-PKI-das AD-Schema der minimal Schlüsselgröße
- mspki-Attribut für das AD-Schema mit minimaler Schlüsselgröße
topic_type:
- apiref
api_name:
- ms-PKI-Minimal-Key-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb1a3f168393bb203f7c590ba52924670d3dab2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107721"
---
# <a name="ms-pki-minimal-key-size-attribute"></a><span data-ttu-id="fabd8-105">MS-PKI-Minimum-Key-size-Attribut</span><span class="sxs-lookup"><span data-stu-id="fabd8-105">ms-PKI-Minimal-Key-Size attribute</span></span>

<span data-ttu-id="fabd8-106">Gibt die minimale Größe des privaten Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="fabd8-106">Indicates the minimum private key size.</span></span>



| <span data-ttu-id="fabd8-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fabd8-107">Entry</span></span> | <span data-ttu-id="fabd8-108">Wert</span><span class="sxs-lookup"><span data-stu-id="fabd8-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fabd8-109">CN</span><span class="sxs-lookup"><span data-stu-id="fabd8-109">CN</span></span>                | <span data-ttu-id="fabd8-110">MS-PKI-minimale Schlüsselgröße</span><span class="sxs-lookup"><span data-stu-id="fabd8-110">ms-PKI-Minimal-Key-Size</span></span>                                                                           |
| <span data-ttu-id="fabd8-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fabd8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fabd8-112">mspki-minimale Schlüsselgröße</span><span class="sxs-lookup"><span data-stu-id="fabd8-112">msPKI-Minimal-Key-Size</span></span>                                                                            |
| <span data-ttu-id="fabd8-113">Size</span><span class="sxs-lookup"><span data-stu-id="fabd8-113">Size</span></span>              | <span data-ttu-id="fabd8-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="fabd8-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="fabd8-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="fabd8-115">Update Privilege</span></span>  | <span data-ttu-id="fabd8-116">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="fabd8-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="fabd8-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="fabd8-117">Update Frequency</span></span>  | <span data-ttu-id="fabd8-118">Wenn das Objekt Vorlage (MS-PKI-Certificate-template) bearbeitet, erstellt oder geklont wird.</span><span class="sxs-lookup"><span data-stu-id="fabd8-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="fabd8-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fabd8-119">Attribute-Id</span></span>      | <span data-ttu-id="fabd8-120">1.2.840.113556.1.4.1433</span><span class="sxs-lookup"><span data-stu-id="fabd8-120">1.2.840.113556.1.4.1433</span></span>                                                                           |
| <span data-ttu-id="fabd8-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fabd8-121">System-Id-Guid</span></span>    | <span data-ttu-id="fabd8-122">e96a63f5-417f-46d3-be52-db7703c503df</span><span class="sxs-lookup"><span data-stu-id="fabd8-122">e96a63f5-417f-46d3-be52-db7703c503df</span></span>                                                              |
| <span data-ttu-id="fabd8-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="fabd8-123">Syntax</span></span>            | [<span data-ttu-id="fabd8-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="fabd8-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="fabd8-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="fabd8-125">Implementations</span></span>

-   [<span data-ttu-id="fabd8-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fabd8-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fabd8-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fabd8-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fabd8-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fabd8-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fabd8-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fabd8-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fabd8-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fabd8-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="fabd8-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fabd8-131">Windows Server 2003</span></span>



| <span data-ttu-id="fabd8-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fabd8-132">Entry</span></span> | <span data-ttu-id="fabd8-133">Wert</span><span class="sxs-lookup"><span data-stu-id="fabd8-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fabd8-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fabd8-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fabd8-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fabd8-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fabd8-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="fabd8-136">System-Only</span></span>            | <span data-ttu-id="fabd8-137">False</span><span class="sxs-lookup"><span data-stu-id="fabd8-137">False</span></span>                                                                   |
| <span data-ttu-id="fabd8-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fabd8-138">Is-Single-Valued</span></span>       | <span data-ttu-id="fabd8-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="fabd8-139">True</span></span>                                                                    |
| <span data-ttu-id="fabd8-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fabd8-140">Is Indexed</span></span>             | <span data-ttu-id="fabd8-141">False</span><span class="sxs-lookup"><span data-stu-id="fabd8-141">False</span></span>                                                                   |
| <span data-ttu-id="fabd8-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fabd8-142">In Global Catalog</span></span>      | <span data-ttu-id="fabd8-143">False</span><span class="sxs-lookup"><span data-stu-id="fabd8-143">False</span></span>                                                                   |
| <span data-ttu-id="fabd8-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fabd8-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="fabd8-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fabd8-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="fabd8-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fabd8-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="fabd8-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fabd8-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="fabd8-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fabd8-148">Search-Flags</span></span>           | <span data-ttu-id="fabd8-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fabd8-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="fabd8-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fabd8-150">System-Flags</span></span>           | <span data-ttu-id="fabd8-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fabd8-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="fabd8-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fabd8-152">Classes used in</span></span>        | [<span data-ttu-id="fabd8-153">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="fabd8-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fabd8-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fabd8-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fabd8-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fabd8-155">Entry</span></span> | <span data-ttu-id="fabd8-156">Wert</span><span class="sxs-lookup"><span data-stu-id="fabd8-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fabd8-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fabd8-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fabd8-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fabd8-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fabd8-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="fabd8-159">System-Only</span></span>            | <span data-ttu-id="fabd8-160">False</span><span class="sxs-lookup"><span data-stu-id="fabd8-160">False</span></span>                                                                   |
| <span data-ttu-id="fabd8-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fabd8-161">Is-Single-Valued</span></span>       | <span data-ttu-id="fabd8-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="fabd8-162">True</span></span>                                                                    |
| <span data-ttu-id="fabd8-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fabd8-163">Is Indexed</span></span>             | <span data-ttu-id="fabd8-164">False</span><span class="sxs-lookup"><span data-stu-id="fabd8-164">False</span></span>                                                                   |
| <span data-ttu-id="fabd8-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fabd8-165">In Global Catalog</span></span>      | <span data-ttu-id="fabd8-166">False</span><span class="sxs-lookup"><span data-stu-id="fabd8-166">False</span></span>                                                                   |
| <span data-ttu-id="fabd8-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fabd8-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="fabd8-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fabd8-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="fabd8-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fabd8-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="fabd8-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fabd8-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="fabd8-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fabd8-171">Search-Flags</span></span>           | <span data-ttu-id="fabd8-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fabd8-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="fabd8-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fabd8-173">System-Flags</span></span>           | <span data-ttu-id="fabd8-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fabd8-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="fabd8-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fabd8-175">Classes used in</span></span>        | [<span data-ttu-id="fabd8-176">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="fabd8-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fabd8-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fabd8-177">Windows Server 2008</span></span>



| <span data-ttu-id="fabd8-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fabd8-178">Entry</span></span> | <span data-ttu-id="fabd8-179">Wert</span><span class="sxs-lookup"><span data-stu-id="fabd8-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fabd8-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fabd8-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fabd8-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fabd8-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fabd8-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="fabd8-182">System-Only</span></span>            | <span data-ttu-id="fabd8-183">False</span><span class="sxs-lookup"><span data-stu-id="fabd8-183">False</span></span>                                                                   |
| <span data-ttu-id="fabd8-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fabd8-184">Is-Single-Valued</span></span>       | <span data-ttu-id="fabd8-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="fabd8-185">True</span></span>                                                                    |
| <span data-ttu-id="fabd8-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fabd8-186">Is Indexed</span></span>             | <span data-ttu-id="fabd8-187">False</span><span class="sxs-lookup"><span data-stu-id="fabd8-187">False</span></span>                                                                   |
| <span data-ttu-id="fabd8-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fabd8-188">In Global Catalog</span></span>      | <span data-ttu-id="fabd8-189">False</span><span class="sxs-lookup"><span data-stu-id="fabd8-189">False</span></span>                                                                   |
| <span data-ttu-id="fabd8-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fabd8-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="fabd8-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fabd8-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="fabd8-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fabd8-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="fabd8-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fabd8-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="fabd8-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fabd8-194">Search-Flags</span></span>           | <span data-ttu-id="fabd8-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fabd8-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="fabd8-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fabd8-196">System-Flags</span></span>           | <span data-ttu-id="fabd8-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fabd8-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="fabd8-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fabd8-198">Classes used in</span></span>        | [<span data-ttu-id="fabd8-199">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="fabd8-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fabd8-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fabd8-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fabd8-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fabd8-201">Entry</span></span> | <span data-ttu-id="fabd8-202">Wert</span><span class="sxs-lookup"><span data-stu-id="fabd8-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fabd8-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fabd8-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fabd8-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fabd8-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fabd8-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="fabd8-205">System-Only</span></span>            | <span data-ttu-id="fabd8-206">False</span><span class="sxs-lookup"><span data-stu-id="fabd8-206">False</span></span>                                                                   |
| <span data-ttu-id="fabd8-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fabd8-207">Is-Single-Valued</span></span>       | <span data-ttu-id="fabd8-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="fabd8-208">True</span></span>                                                                    |
| <span data-ttu-id="fabd8-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fabd8-209">Is Indexed</span></span>             | <span data-ttu-id="fabd8-210">False</span><span class="sxs-lookup"><span data-stu-id="fabd8-210">False</span></span>                                                                   |
| <span data-ttu-id="fabd8-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fabd8-211">In Global Catalog</span></span>      | <span data-ttu-id="fabd8-212">False</span><span class="sxs-lookup"><span data-stu-id="fabd8-212">False</span></span>                                                                   |
| <span data-ttu-id="fabd8-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fabd8-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="fabd8-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fabd8-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="fabd8-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fabd8-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="fabd8-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fabd8-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="fabd8-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fabd8-217">Search-Flags</span></span>           | <span data-ttu-id="fabd8-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fabd8-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="fabd8-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fabd8-219">System-Flags</span></span>           | <span data-ttu-id="fabd8-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fabd8-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="fabd8-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fabd8-221">Classes used in</span></span>        | [<span data-ttu-id="fabd8-222">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="fabd8-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fabd8-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fabd8-223">Windows Server 2012</span></span>



| <span data-ttu-id="fabd8-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fabd8-224">Entry</span></span> | <span data-ttu-id="fabd8-225">Wert</span><span class="sxs-lookup"><span data-stu-id="fabd8-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fabd8-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fabd8-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fabd8-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fabd8-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="fabd8-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="fabd8-228">System-Only</span></span>            | <span data-ttu-id="fabd8-229">False</span><span class="sxs-lookup"><span data-stu-id="fabd8-229">False</span></span>                                                                   |
| <span data-ttu-id="fabd8-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fabd8-230">Is-Single-Valued</span></span>       | <span data-ttu-id="fabd8-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="fabd8-231">True</span></span>                                                                    |
| <span data-ttu-id="fabd8-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fabd8-232">Is Indexed</span></span>             | <span data-ttu-id="fabd8-233">False</span><span class="sxs-lookup"><span data-stu-id="fabd8-233">False</span></span>                                                                   |
| <span data-ttu-id="fabd8-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fabd8-234">In Global Catalog</span></span>      | <span data-ttu-id="fabd8-235">False</span><span class="sxs-lookup"><span data-stu-id="fabd8-235">False</span></span>                                                                   |
| <span data-ttu-id="fabd8-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fabd8-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="fabd8-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fabd8-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="fabd8-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fabd8-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="fabd8-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fabd8-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="fabd8-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fabd8-240">Search-Flags</span></span>           | <span data-ttu-id="fabd8-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fabd8-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="fabd8-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fabd8-242">System-Flags</span></span>           | <span data-ttu-id="fabd8-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fabd8-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="fabd8-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fabd8-244">Classes used in</span></span>        | [<span data-ttu-id="fabd8-245">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="fabd8-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





