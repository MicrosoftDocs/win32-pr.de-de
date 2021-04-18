---
title: MS-PKI-Ablösung-Templates-Attribut
description: Gibt die Namen der Zertifikat Vorlagen an, die durch die aktuelle Vorlage abgelöst werden.
ms.assetid: 4e247932-1c50-4bfb-b723-52b7c36a8571
ms.tgt_platform: multiple
keywords:
- MS-PKI-Ablösung-Templates-Attribut AD-Schema
- 'mspki-abgelöst-Attribut: AD-Schema für Vorlagen'
topic_type:
- apiref
api_name:
- ms-PKI-Supersede-Templates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd11ac2b96846912b0c6b1e8d01c6fd558f5f6db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519759"
---
# <a name="ms-pki-supersede-templates-attribute"></a><span data-ttu-id="2be31-105">MS-PKI-Ablösung-Templates-Attribut</span><span class="sxs-lookup"><span data-stu-id="2be31-105">ms-PKI-Supersede-Templates attribute</span></span>

<span data-ttu-id="2be31-106">Gibt die Namen der Zertifikat Vorlagen an, die durch die aktuelle Vorlage abgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="2be31-106">Specifies the names of the certificate templates that are superseded by the current template.</span></span>



| <span data-ttu-id="2be31-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2be31-107">Entry</span></span> | <span data-ttu-id="2be31-108">Wert</span><span class="sxs-lookup"><span data-stu-id="2be31-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2be31-109">CN</span><span class="sxs-lookup"><span data-stu-id="2be31-109">CN</span></span>                | <span data-ttu-id="2be31-110">MS-PKI-abgelöst-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="2be31-110">ms-PKI-Supersede-Templates</span></span>                                                                        |
| <span data-ttu-id="2be31-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2be31-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2be31-112">mspki-abgelöst-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="2be31-112">msPKI-Supersede-Templates</span></span>                                                                         |
| <span data-ttu-id="2be31-113">Size</span><span class="sxs-lookup"><span data-stu-id="2be31-113">Size</span></span>              | <span data-ttu-id="2be31-114">64 Bytes</span><span class="sxs-lookup"><span data-stu-id="2be31-114">64 bytes</span></span>                                                                                          |
| <span data-ttu-id="2be31-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2be31-115">Update Privilege</span></span>  | <span data-ttu-id="2be31-116">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="2be31-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="2be31-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="2be31-117">Update Frequency</span></span>  | <span data-ttu-id="2be31-118">Wenn das Objekt Vorlage (MS-PKI-Certificate-template) bearbeitet, erstellt oder geklont wird.</span><span class="sxs-lookup"><span data-stu-id="2be31-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="2be31-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2be31-119">Attribute-Id</span></span>      | <span data-ttu-id="2be31-120">1.2.840.113556.1.4.1437</span><span class="sxs-lookup"><span data-stu-id="2be31-120">1.2.840.113556.1.4.1437</span></span>                                                                           |
| <span data-ttu-id="2be31-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2be31-121">System-Id-Guid</span></span>    | <span data-ttu-id="2be31-122">9ab8ae7d-7a5b-421D-b5e4-061F 79dfd5d7</span><span class="sxs-lookup"><span data-stu-id="2be31-122">9de8ae7d-7a5b-421d-b5e4-061f79dfd5d7</span></span>                                                              |
| <span data-ttu-id="2be31-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="2be31-123">Syntax</span></span>            | [<span data-ttu-id="2be31-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="2be31-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="2be31-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="2be31-125">Implementations</span></span>

-   [<span data-ttu-id="2be31-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2be31-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2be31-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2be31-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2be31-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2be31-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2be31-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2be31-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2be31-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2be31-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="2be31-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2be31-131">Windows Server 2003</span></span>



| <span data-ttu-id="2be31-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2be31-132">Entry</span></span> | <span data-ttu-id="2be31-133">Wert</span><span class="sxs-lookup"><span data-stu-id="2be31-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2be31-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2be31-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2be31-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2be31-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2be31-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="2be31-136">System-Only</span></span>            | <span data-ttu-id="2be31-137">False</span><span class="sxs-lookup"><span data-stu-id="2be31-137">False</span></span>                                                                   |
| <span data-ttu-id="2be31-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2be31-138">Is-Single-Valued</span></span>       | <span data-ttu-id="2be31-139">False</span><span class="sxs-lookup"><span data-stu-id="2be31-139">False</span></span>                                                                   |
| <span data-ttu-id="2be31-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2be31-140">Is Indexed</span></span>             | <span data-ttu-id="2be31-141">False</span><span class="sxs-lookup"><span data-stu-id="2be31-141">False</span></span>                                                                   |
| <span data-ttu-id="2be31-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2be31-142">In Global Catalog</span></span>      | <span data-ttu-id="2be31-143">False</span><span class="sxs-lookup"><span data-stu-id="2be31-143">False</span></span>                                                                   |
| <span data-ttu-id="2be31-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2be31-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="2be31-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2be31-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2be31-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2be31-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2be31-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2be31-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2be31-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2be31-148">Search-Flags</span></span>           | <span data-ttu-id="2be31-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2be31-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="2be31-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2be31-150">System-Flags</span></span>           | <span data-ttu-id="2be31-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2be31-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="2be31-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2be31-152">Classes used in</span></span>        | [<span data-ttu-id="2be31-153">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="2be31-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2be31-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2be31-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2be31-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2be31-155">Entry</span></span> | <span data-ttu-id="2be31-156">Wert</span><span class="sxs-lookup"><span data-stu-id="2be31-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2be31-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2be31-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2be31-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2be31-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2be31-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="2be31-159">System-Only</span></span>            | <span data-ttu-id="2be31-160">False</span><span class="sxs-lookup"><span data-stu-id="2be31-160">False</span></span>                                                                   |
| <span data-ttu-id="2be31-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2be31-161">Is-Single-Valued</span></span>       | <span data-ttu-id="2be31-162">False</span><span class="sxs-lookup"><span data-stu-id="2be31-162">False</span></span>                                                                   |
| <span data-ttu-id="2be31-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2be31-163">Is Indexed</span></span>             | <span data-ttu-id="2be31-164">False</span><span class="sxs-lookup"><span data-stu-id="2be31-164">False</span></span>                                                                   |
| <span data-ttu-id="2be31-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2be31-165">In Global Catalog</span></span>      | <span data-ttu-id="2be31-166">False</span><span class="sxs-lookup"><span data-stu-id="2be31-166">False</span></span>                                                                   |
| <span data-ttu-id="2be31-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2be31-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="2be31-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2be31-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2be31-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2be31-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2be31-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2be31-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2be31-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2be31-171">Search-Flags</span></span>           | <span data-ttu-id="2be31-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2be31-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="2be31-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2be31-173">System-Flags</span></span>           | <span data-ttu-id="2be31-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2be31-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="2be31-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2be31-175">Classes used in</span></span>        | [<span data-ttu-id="2be31-176">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="2be31-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2be31-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2be31-177">Windows Server 2008</span></span>



| <span data-ttu-id="2be31-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2be31-178">Entry</span></span> | <span data-ttu-id="2be31-179">Wert</span><span class="sxs-lookup"><span data-stu-id="2be31-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2be31-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2be31-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2be31-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2be31-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2be31-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="2be31-182">System-Only</span></span>            | <span data-ttu-id="2be31-183">False</span><span class="sxs-lookup"><span data-stu-id="2be31-183">False</span></span>                                                                   |
| <span data-ttu-id="2be31-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2be31-184">Is-Single-Valued</span></span>       | <span data-ttu-id="2be31-185">False</span><span class="sxs-lookup"><span data-stu-id="2be31-185">False</span></span>                                                                   |
| <span data-ttu-id="2be31-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2be31-186">Is Indexed</span></span>             | <span data-ttu-id="2be31-187">False</span><span class="sxs-lookup"><span data-stu-id="2be31-187">False</span></span>                                                                   |
| <span data-ttu-id="2be31-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2be31-188">In Global Catalog</span></span>      | <span data-ttu-id="2be31-189">False</span><span class="sxs-lookup"><span data-stu-id="2be31-189">False</span></span>                                                                   |
| <span data-ttu-id="2be31-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2be31-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="2be31-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2be31-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2be31-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2be31-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2be31-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2be31-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2be31-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2be31-194">Search-Flags</span></span>           | <span data-ttu-id="2be31-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2be31-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="2be31-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2be31-196">System-Flags</span></span>           | <span data-ttu-id="2be31-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2be31-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="2be31-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2be31-198">Classes used in</span></span>        | [<span data-ttu-id="2be31-199">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="2be31-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2be31-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2be31-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2be31-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2be31-201">Entry</span></span> | <span data-ttu-id="2be31-202">Wert</span><span class="sxs-lookup"><span data-stu-id="2be31-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2be31-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2be31-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2be31-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2be31-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2be31-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="2be31-205">System-Only</span></span>            | <span data-ttu-id="2be31-206">False</span><span class="sxs-lookup"><span data-stu-id="2be31-206">False</span></span>                                                                   |
| <span data-ttu-id="2be31-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2be31-207">Is-Single-Valued</span></span>       | <span data-ttu-id="2be31-208">False</span><span class="sxs-lookup"><span data-stu-id="2be31-208">False</span></span>                                                                   |
| <span data-ttu-id="2be31-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2be31-209">Is Indexed</span></span>             | <span data-ttu-id="2be31-210">False</span><span class="sxs-lookup"><span data-stu-id="2be31-210">False</span></span>                                                                   |
| <span data-ttu-id="2be31-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2be31-211">In Global Catalog</span></span>      | <span data-ttu-id="2be31-212">False</span><span class="sxs-lookup"><span data-stu-id="2be31-212">False</span></span>                                                                   |
| <span data-ttu-id="2be31-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2be31-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="2be31-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2be31-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2be31-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2be31-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2be31-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2be31-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2be31-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2be31-217">Search-Flags</span></span>           | <span data-ttu-id="2be31-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2be31-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="2be31-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2be31-219">System-Flags</span></span>           | <span data-ttu-id="2be31-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2be31-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="2be31-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2be31-221">Classes used in</span></span>        | [<span data-ttu-id="2be31-222">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="2be31-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2be31-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2be31-223">Windows Server 2012</span></span>



| <span data-ttu-id="2be31-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2be31-224">Entry</span></span> | <span data-ttu-id="2be31-225">Wert</span><span class="sxs-lookup"><span data-stu-id="2be31-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2be31-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2be31-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2be31-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2be31-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2be31-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="2be31-228">System-Only</span></span>            | <span data-ttu-id="2be31-229">False</span><span class="sxs-lookup"><span data-stu-id="2be31-229">False</span></span>                                                                   |
| <span data-ttu-id="2be31-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2be31-230">Is-Single-Valued</span></span>       | <span data-ttu-id="2be31-231">False</span><span class="sxs-lookup"><span data-stu-id="2be31-231">False</span></span>                                                                   |
| <span data-ttu-id="2be31-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2be31-232">Is Indexed</span></span>             | <span data-ttu-id="2be31-233">False</span><span class="sxs-lookup"><span data-stu-id="2be31-233">False</span></span>                                                                   |
| <span data-ttu-id="2be31-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2be31-234">In Global Catalog</span></span>      | <span data-ttu-id="2be31-235">False</span><span class="sxs-lookup"><span data-stu-id="2be31-235">False</span></span>                                                                   |
| <span data-ttu-id="2be31-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2be31-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="2be31-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2be31-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2be31-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2be31-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2be31-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2be31-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2be31-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2be31-240">Search-Flags</span></span>           | <span data-ttu-id="2be31-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2be31-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="2be31-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2be31-242">System-Flags</span></span>           | <span data-ttu-id="2be31-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2be31-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="2be31-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2be31-244">Classes used in</span></span>        | [<span data-ttu-id="2be31-245">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="2be31-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





