---
title: Signature-Algorithms-Attribut
description: Dieses Attribut gibt den Algorithmustyp an, der verwendet werden muss, um eine digitale Signatur während des Authentifizierungs Vorgangs zu decodieren.
ms.assetid: f602a009-6823-42e7-b5e4-fb433535b4cc
ms.tgt_platform: multiple
keywords:
- AD-Schema für Signature-Algorithms-Attribut
- signaturealgorithms-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Signature-Algorithms
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6487155ed8d13735a8201a41c9d1d5b087bb3711
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104213781"
---
# <a name="signature-algorithms-attribute"></a><span data-ttu-id="f2e41-105">Signature-Algorithms-Attribut</span><span class="sxs-lookup"><span data-stu-id="f2e41-105">Signature-Algorithms attribute</span></span>

<span data-ttu-id="f2e41-106">Dieses Attribut gibt den Algorithmustyp an, der verwendet werden muss, um eine digitale Signatur während des Authentifizierungs Vorgangs zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="f2e41-106">This attribute indicates the type of algorithm that must be used to decode a digital signature during the authentication process.</span></span>



| <span data-ttu-id="f2e41-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2e41-107">Entry</span></span> | <span data-ttu-id="f2e41-108">Wert</span><span class="sxs-lookup"><span data-stu-id="f2e41-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f2e41-109">CN</span><span class="sxs-lookup"><span data-stu-id="f2e41-109">CN</span></span>                | <span data-ttu-id="f2e41-110">Signature-Algorithms</span><span class="sxs-lookup"><span data-stu-id="f2e41-110">Signature-Algorithms</span></span>                        |
| <span data-ttu-id="f2e41-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f2e41-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f2e41-112">signaturealgorithms</span><span class="sxs-lookup"><span data-stu-id="f2e41-112">signatureAlgorithms</span></span>                         |
| <span data-ttu-id="f2e41-113">Size</span><span class="sxs-lookup"><span data-stu-id="f2e41-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="f2e41-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f2e41-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="f2e41-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f2e41-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="f2e41-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f2e41-116">Attribute-Id</span></span>      | <span data-ttu-id="f2e41-117">1.2.840.113556.1.4.824</span><span class="sxs-lookup"><span data-stu-id="f2e41-117">1.2.840.113556.1.4.824</span></span>                      |
| <span data-ttu-id="f2e41-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f2e41-118">System-Id-Guid</span></span>    | <span data-ttu-id="f2e41-119">2a39c5b2-8960-11d1-AEbc-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="f2e41-119">2a39c5b2-8960-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="f2e41-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2e41-120">Syntax</span></span>            | [<span data-ttu-id="f2e41-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f2e41-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f2e41-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f2e41-122">Implementations</span></span>

-   [<span data-ttu-id="f2e41-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f2e41-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f2e41-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f2e41-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f2e41-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f2e41-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f2e41-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f2e41-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f2e41-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f2e41-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f2e41-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f2e41-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f2e41-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f2e41-129">Windows 2000 Server</span></span>



| <span data-ttu-id="f2e41-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2e41-130">Entry</span></span> | <span data-ttu-id="f2e41-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f2e41-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e41-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f2e41-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2e41-133">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2e41-134">System-Only</span></span>            | <span data-ttu-id="f2e41-135">False</span><span class="sxs-lookup"><span data-stu-id="f2e41-135">False</span></span>                                                                                                                                      |
| <span data-ttu-id="f2e41-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f2e41-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f2e41-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2e41-137">True</span></span>                                                                                                                                       |
| <span data-ttu-id="f2e41-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f2e41-138">Is Indexed</span></span>             | <span data-ttu-id="f2e41-139">False</span><span class="sxs-lookup"><span data-stu-id="f2e41-139">False</span></span>                                                                                                                                      |
| <span data-ttu-id="f2e41-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f2e41-140">In Global Catalog</span></span>      | <span data-ttu-id="f2e41-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2e41-141">True</span></span>                                                                                                                                       |
| <span data-ttu-id="f2e41-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f2e41-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2e41-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f2e41-143">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="f2e41-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2e41-144">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2e41-145">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e41-146">Search-Flags</span></span>           | <span data-ttu-id="f2e41-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2e41-147">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="f2e41-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e41-148">System-Flags</span></span>           | <span data-ttu-id="f2e41-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2e41-149">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="f2e41-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f2e41-150">Classes used in</span></span>        | [<span data-ttu-id="f2e41-151">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="f2e41-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="f2e41-152">**PKI-Registrierung-Dienst**</span><span class="sxs-lookup"><span data-stu-id="f2e41-152">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f2e41-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f2e41-153">Windows Server 2003</span></span>



| <span data-ttu-id="f2e41-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2e41-154">Entry</span></span> | <span data-ttu-id="f2e41-155">Wert</span><span class="sxs-lookup"><span data-stu-id="f2e41-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e41-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f2e41-156">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2e41-157">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2e41-158">System-Only</span></span>            | <span data-ttu-id="f2e41-159">False</span><span class="sxs-lookup"><span data-stu-id="f2e41-159">False</span></span>                                                                                                                                      |
| <span data-ttu-id="f2e41-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f2e41-160">Is-Single-Valued</span></span>       | <span data-ttu-id="f2e41-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2e41-161">True</span></span>                                                                                                                                       |
| <span data-ttu-id="f2e41-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f2e41-162">Is Indexed</span></span>             | <span data-ttu-id="f2e41-163">False</span><span class="sxs-lookup"><span data-stu-id="f2e41-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="f2e41-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f2e41-164">In Global Catalog</span></span>      | <span data-ttu-id="f2e41-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2e41-165">True</span></span>                                                                                                                                       |
| <span data-ttu-id="f2e41-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f2e41-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2e41-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f2e41-167">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="f2e41-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2e41-168">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2e41-169">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e41-170">Search-Flags</span></span>           | <span data-ttu-id="f2e41-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2e41-171">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="f2e41-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e41-172">System-Flags</span></span>           | <span data-ttu-id="f2e41-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2e41-173">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="f2e41-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f2e41-174">Classes used in</span></span>        | [<span data-ttu-id="f2e41-175">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="f2e41-175">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="f2e41-176">**PKI-Registrierung-Dienst**</span><span class="sxs-lookup"><span data-stu-id="f2e41-176">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f2e41-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f2e41-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f2e41-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2e41-178">Entry</span></span> | <span data-ttu-id="f2e41-179">Wert</span><span class="sxs-lookup"><span data-stu-id="f2e41-179">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e41-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f2e41-180">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2e41-181">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2e41-182">System-Only</span></span>            | <span data-ttu-id="f2e41-183">False</span><span class="sxs-lookup"><span data-stu-id="f2e41-183">False</span></span>                                                                                                                                      |
| <span data-ttu-id="f2e41-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f2e41-184">Is-Single-Valued</span></span>       | <span data-ttu-id="f2e41-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2e41-185">True</span></span>                                                                                                                                       |
| <span data-ttu-id="f2e41-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f2e41-186">Is Indexed</span></span>             | <span data-ttu-id="f2e41-187">False</span><span class="sxs-lookup"><span data-stu-id="f2e41-187">False</span></span>                                                                                                                                      |
| <span data-ttu-id="f2e41-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f2e41-188">In Global Catalog</span></span>      | <span data-ttu-id="f2e41-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2e41-189">True</span></span>                                                                                                                                       |
| <span data-ttu-id="f2e41-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f2e41-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2e41-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f2e41-191">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="f2e41-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2e41-192">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2e41-193">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e41-194">Search-Flags</span></span>           | <span data-ttu-id="f2e41-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2e41-195">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="f2e41-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e41-196">System-Flags</span></span>           | <span data-ttu-id="f2e41-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2e41-197">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="f2e41-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f2e41-198">Classes used in</span></span>        | [<span data-ttu-id="f2e41-199">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="f2e41-199">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="f2e41-200">**PKI-Registrierung-Dienst**</span><span class="sxs-lookup"><span data-stu-id="f2e41-200">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f2e41-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2e41-201">Windows Server 2008</span></span>



| <span data-ttu-id="f2e41-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2e41-202">Entry</span></span> | <span data-ttu-id="f2e41-203">Wert</span><span class="sxs-lookup"><span data-stu-id="f2e41-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e41-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f2e41-204">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2e41-205">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2e41-206">System-Only</span></span>            | <span data-ttu-id="f2e41-207">False</span><span class="sxs-lookup"><span data-stu-id="f2e41-207">False</span></span>                                                                                                                                      |
| <span data-ttu-id="f2e41-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f2e41-208">Is-Single-Valued</span></span>       | <span data-ttu-id="f2e41-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2e41-209">True</span></span>                                                                                                                                       |
| <span data-ttu-id="f2e41-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f2e41-210">Is Indexed</span></span>             | <span data-ttu-id="f2e41-211">False</span><span class="sxs-lookup"><span data-stu-id="f2e41-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="f2e41-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f2e41-212">In Global Catalog</span></span>      | <span data-ttu-id="f2e41-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2e41-213">True</span></span>                                                                                                                                       |
| <span data-ttu-id="f2e41-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f2e41-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2e41-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f2e41-215">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="f2e41-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2e41-216">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2e41-217">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e41-218">Search-Flags</span></span>           | <span data-ttu-id="f2e41-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2e41-219">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="f2e41-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e41-220">System-Flags</span></span>           | <span data-ttu-id="f2e41-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2e41-221">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="f2e41-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f2e41-222">Classes used in</span></span>        | [<span data-ttu-id="f2e41-223">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="f2e41-223">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="f2e41-224">**PKI-Registrierung-Dienst**</span><span class="sxs-lookup"><span data-stu-id="f2e41-224">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f2e41-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f2e41-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f2e41-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2e41-226">Entry</span></span> | <span data-ttu-id="f2e41-227">Wert</span><span class="sxs-lookup"><span data-stu-id="f2e41-227">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e41-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f2e41-228">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2e41-229">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2e41-230">System-Only</span></span>            | <span data-ttu-id="f2e41-231">False</span><span class="sxs-lookup"><span data-stu-id="f2e41-231">False</span></span>                                                                                                                                      |
| <span data-ttu-id="f2e41-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f2e41-232">Is-Single-Valued</span></span>       | <span data-ttu-id="f2e41-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2e41-233">True</span></span>                                                                                                                                       |
| <span data-ttu-id="f2e41-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f2e41-234">Is Indexed</span></span>             | <span data-ttu-id="f2e41-235">False</span><span class="sxs-lookup"><span data-stu-id="f2e41-235">False</span></span>                                                                                                                                      |
| <span data-ttu-id="f2e41-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f2e41-236">In Global Catalog</span></span>      | <span data-ttu-id="f2e41-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2e41-237">True</span></span>                                                                                                                                       |
| <span data-ttu-id="f2e41-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f2e41-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2e41-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f2e41-239">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="f2e41-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2e41-240">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2e41-241">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e41-242">Search-Flags</span></span>           | <span data-ttu-id="f2e41-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2e41-243">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="f2e41-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e41-244">System-Flags</span></span>           | <span data-ttu-id="f2e41-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2e41-245">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="f2e41-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f2e41-246">Classes used in</span></span>        | [<span data-ttu-id="f2e41-247">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="f2e41-247">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="f2e41-248">**PKI-Registrierung-Dienst**</span><span class="sxs-lookup"><span data-stu-id="f2e41-248">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f2e41-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2e41-249">Windows Server 2012</span></span>



| <span data-ttu-id="f2e41-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2e41-250">Entry</span></span> | <span data-ttu-id="f2e41-251">Wert</span><span class="sxs-lookup"><span data-stu-id="f2e41-251">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e41-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f2e41-252">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2e41-253">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2e41-254">System-Only</span></span>            | <span data-ttu-id="f2e41-255">False</span><span class="sxs-lookup"><span data-stu-id="f2e41-255">False</span></span>                                                                                                                                      |
| <span data-ttu-id="f2e41-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f2e41-256">Is-Single-Valued</span></span>       | <span data-ttu-id="f2e41-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2e41-257">True</span></span>                                                                                                                                       |
| <span data-ttu-id="f2e41-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f2e41-258">Is Indexed</span></span>             | <span data-ttu-id="f2e41-259">False</span><span class="sxs-lookup"><span data-stu-id="f2e41-259">False</span></span>                                                                                                                                      |
| <span data-ttu-id="f2e41-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f2e41-260">In Global Catalog</span></span>      | <span data-ttu-id="f2e41-261">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2e41-261">True</span></span>                                                                                                                                       |
| <span data-ttu-id="f2e41-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f2e41-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2e41-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f2e41-263">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="f2e41-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2e41-264">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2e41-265">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="f2e41-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e41-266">Search-Flags</span></span>           | <span data-ttu-id="f2e41-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2e41-267">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="f2e41-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2e41-268">System-Flags</span></span>           | <span data-ttu-id="f2e41-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2e41-269">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="f2e41-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f2e41-270">Classes used in</span></span>        | [<span data-ttu-id="f2e41-271">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="f2e41-271">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="f2e41-272">**PKI-Registrierung-Dienst**</span><span class="sxs-lookup"><span data-stu-id="f2e41-272">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



 

 





