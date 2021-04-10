---
title: UPN-Suffixes-Attribut
description: Die Liste der Benutzer Prinzipal Namen-Suffixe für eine Domäne.
ms.assetid: ad861d2d-b643-468c-a346-36ad6a828359
ms.tgt_platform: multiple
keywords:
- AD-Schema für UPN-Suffixes-Attribut
- upnSuffixes-Attribut AD-Schema
topic_type:
- apiref
api_name:
- UPN-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4aa5fb9398478e4b91fb8f36b8cf96a244935fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859743"
---
# <a name="upn-suffixes-attribute"></a><span data-ttu-id="0c181-105">UPN-Suffixes-Attribut</span><span class="sxs-lookup"><span data-stu-id="0c181-105">UPN-Suffixes attribute</span></span>

<span data-ttu-id="0c181-106">Die Liste der Benutzer Prinzipal Namen-Suffixe für eine Domäne.</span><span class="sxs-lookup"><span data-stu-id="0c181-106">The list of User-Principal-Name suffixes for a domain.</span></span>



| <span data-ttu-id="0c181-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c181-107">Entry</span></span> | <span data-ttu-id="0c181-108">Wert</span><span class="sxs-lookup"><span data-stu-id="0c181-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="0c181-109">CN</span><span class="sxs-lookup"><span data-stu-id="0c181-109">CN</span></span>                | <span data-ttu-id="0c181-110">UPN-Suffixes</span><span class="sxs-lookup"><span data-stu-id="0c181-110">UPN-Suffixes</span></span>                                |
| <span data-ttu-id="0c181-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0c181-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0c181-112">upnsuffixe</span><span class="sxs-lookup"><span data-stu-id="0c181-112">uPNSuffixes</span></span>                                 |
| <span data-ttu-id="0c181-113">Size</span><span class="sxs-lookup"><span data-stu-id="0c181-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="0c181-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0c181-114">Update Privilege</span></span>  | <span data-ttu-id="0c181-115">Domänenadministrator</span><span class="sxs-lookup"><span data-stu-id="0c181-115">Domain Administrator</span></span>                        |
| <span data-ttu-id="0c181-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="0c181-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="0c181-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0c181-117">Attribute-Id</span></span>      | <span data-ttu-id="0c181-118">1.2.840.113556.1.4.890</span><span class="sxs-lookup"><span data-stu-id="0c181-118">1.2.840.113556.1.4.890</span></span>                      |
| <span data-ttu-id="0c181-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0c181-119">System-Id-Guid</span></span>    | <span data-ttu-id="0c181-120">032160bf -9824-11d1-aec0-0000e80367c1</span><span class="sxs-lookup"><span data-stu-id="0c181-120">032160bf-9824-11d1-aec0-0000f80367c1</span></span>        |
| <span data-ttu-id="0c181-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c181-121">Syntax</span></span>            | [<span data-ttu-id="0c181-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="0c181-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="0c181-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="0c181-123">Implementations</span></span>

-   [<span data-ttu-id="0c181-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0c181-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0c181-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0c181-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0c181-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="0c181-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0c181-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0c181-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0c181-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0c181-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0c181-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0c181-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0c181-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0c181-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0c181-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c181-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0c181-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c181-132">Entry</span></span> | <span data-ttu-id="0c181-133">Wert</span><span class="sxs-lookup"><span data-stu-id="0c181-133">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c181-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0c181-134">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="0c181-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c181-135">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="0c181-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c181-136">System-Only</span></span>            | <span data-ttu-id="0c181-137">False</span><span class="sxs-lookup"><span data-stu-id="0c181-137">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0c181-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0c181-139">False</span><span class="sxs-lookup"><span data-stu-id="0c181-139">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0c181-140">Is Indexed</span></span>             | <span data-ttu-id="0c181-141">False</span><span class="sxs-lookup"><span data-stu-id="0c181-141">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0c181-142">In Global Catalog</span></span>      | <span data-ttu-id="0c181-143">False</span><span class="sxs-lookup"><span data-stu-id="0c181-143">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c181-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c181-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0c181-145">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="0c181-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c181-146">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="0c181-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c181-147">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="0c181-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c181-148">Search-Flags</span></span>           | <span data-ttu-id="0c181-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c181-149">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="0c181-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c181-150">System-Flags</span></span>           | <span data-ttu-id="0c181-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c181-151">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="0c181-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0c181-152">Classes used in</span></span>        | [<span data-ttu-id="0c181-153">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="0c181-153">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="0c181-154">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="0c181-154">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0c181-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c181-155">Windows Server 2003</span></span>



| <span data-ttu-id="0c181-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c181-156">Entry</span></span> | <span data-ttu-id="0c181-157">Wert</span><span class="sxs-lookup"><span data-stu-id="0c181-157">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c181-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0c181-158">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="0c181-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c181-159">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="0c181-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c181-160">System-Only</span></span>            | <span data-ttu-id="0c181-161">False</span><span class="sxs-lookup"><span data-stu-id="0c181-161">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0c181-162">Is-Single-Valued</span></span>       | <span data-ttu-id="0c181-163">False</span><span class="sxs-lookup"><span data-stu-id="0c181-163">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0c181-164">Is Indexed</span></span>             | <span data-ttu-id="0c181-165">False</span><span class="sxs-lookup"><span data-stu-id="0c181-165">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0c181-166">In Global Catalog</span></span>      | <span data-ttu-id="0c181-167">False</span><span class="sxs-lookup"><span data-stu-id="0c181-167">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c181-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c181-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0c181-169">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="0c181-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c181-170">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="0c181-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c181-171">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="0c181-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c181-172">Search-Flags</span></span>           | <span data-ttu-id="0c181-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c181-173">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="0c181-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c181-174">System-Flags</span></span>           | <span data-ttu-id="0c181-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c181-175">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="0c181-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0c181-176">Classes used in</span></span>        | [<span data-ttu-id="0c181-177">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="0c181-177">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="0c181-178">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="0c181-178">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0c181-179">Adam</span><span class="sxs-lookup"><span data-stu-id="0c181-179">ADAM</span></span>



| <span data-ttu-id="0c181-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c181-180">Entry</span></span> | <span data-ttu-id="0c181-181">Wert</span><span class="sxs-lookup"><span data-stu-id="0c181-181">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c181-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0c181-182">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="0c181-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c181-183">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="0c181-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c181-184">System-Only</span></span>            | <span data-ttu-id="0c181-185">False</span><span class="sxs-lookup"><span data-stu-id="0c181-185">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0c181-186">Is-Single-Valued</span></span>       | <span data-ttu-id="0c181-187">False</span><span class="sxs-lookup"><span data-stu-id="0c181-187">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0c181-188">Is Indexed</span></span>             | <span data-ttu-id="0c181-189">False</span><span class="sxs-lookup"><span data-stu-id="0c181-189">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0c181-190">In Global Catalog</span></span>      | <span data-ttu-id="0c181-191">False</span><span class="sxs-lookup"><span data-stu-id="0c181-191">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c181-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c181-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0c181-193">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="0c181-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c181-194">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="0c181-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c181-195">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="0c181-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c181-196">Search-Flags</span></span>           | <span data-ttu-id="0c181-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c181-197">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="0c181-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c181-198">System-Flags</span></span>           | <span data-ttu-id="0c181-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c181-199">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="0c181-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0c181-200">Classes used in</span></span>        | [<span data-ttu-id="0c181-201">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="0c181-201">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="0c181-202">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="0c181-202">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0c181-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0c181-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0c181-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c181-204">Entry</span></span> | <span data-ttu-id="0c181-205">Wert</span><span class="sxs-lookup"><span data-stu-id="0c181-205">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c181-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0c181-206">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="0c181-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c181-207">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="0c181-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c181-208">System-Only</span></span>            | <span data-ttu-id="0c181-209">False</span><span class="sxs-lookup"><span data-stu-id="0c181-209">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0c181-210">Is-Single-Valued</span></span>       | <span data-ttu-id="0c181-211">False</span><span class="sxs-lookup"><span data-stu-id="0c181-211">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0c181-212">Is Indexed</span></span>             | <span data-ttu-id="0c181-213">False</span><span class="sxs-lookup"><span data-stu-id="0c181-213">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0c181-214">In Global Catalog</span></span>      | <span data-ttu-id="0c181-215">False</span><span class="sxs-lookup"><span data-stu-id="0c181-215">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c181-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c181-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0c181-217">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="0c181-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c181-218">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="0c181-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c181-219">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="0c181-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c181-220">Search-Flags</span></span>           | <span data-ttu-id="0c181-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c181-221">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="0c181-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c181-222">System-Flags</span></span>           | <span data-ttu-id="0c181-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c181-223">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="0c181-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0c181-224">Classes used in</span></span>        | [<span data-ttu-id="0c181-225">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="0c181-225">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="0c181-226">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="0c181-226">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0c181-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c181-227">Windows Server 2008</span></span>



| <span data-ttu-id="0c181-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c181-228">Entry</span></span> | <span data-ttu-id="0c181-229">Wert</span><span class="sxs-lookup"><span data-stu-id="0c181-229">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c181-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0c181-230">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="0c181-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c181-231">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="0c181-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c181-232">System-Only</span></span>            | <span data-ttu-id="0c181-233">False</span><span class="sxs-lookup"><span data-stu-id="0c181-233">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0c181-234">Is-Single-Valued</span></span>       | <span data-ttu-id="0c181-235">False</span><span class="sxs-lookup"><span data-stu-id="0c181-235">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0c181-236">Is Indexed</span></span>             | <span data-ttu-id="0c181-237">False</span><span class="sxs-lookup"><span data-stu-id="0c181-237">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0c181-238">In Global Catalog</span></span>      | <span data-ttu-id="0c181-239">False</span><span class="sxs-lookup"><span data-stu-id="0c181-239">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c181-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c181-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0c181-241">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="0c181-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c181-242">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="0c181-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c181-243">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="0c181-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c181-244">Search-Flags</span></span>           | <span data-ttu-id="0c181-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c181-245">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="0c181-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c181-246">System-Flags</span></span>           | <span data-ttu-id="0c181-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c181-247">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="0c181-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0c181-248">Classes used in</span></span>        | [<span data-ttu-id="0c181-249">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="0c181-249">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="0c181-250">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="0c181-250">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0c181-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0c181-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0c181-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c181-252">Entry</span></span> | <span data-ttu-id="0c181-253">Wert</span><span class="sxs-lookup"><span data-stu-id="0c181-253">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c181-254">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0c181-254">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="0c181-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c181-255">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="0c181-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c181-256">System-Only</span></span>            | <span data-ttu-id="0c181-257">False</span><span class="sxs-lookup"><span data-stu-id="0c181-257">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-258">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0c181-258">Is-Single-Valued</span></span>       | <span data-ttu-id="0c181-259">False</span><span class="sxs-lookup"><span data-stu-id="0c181-259">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-260">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0c181-260">Is Indexed</span></span>             | <span data-ttu-id="0c181-261">False</span><span class="sxs-lookup"><span data-stu-id="0c181-261">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-262">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0c181-262">In Global Catalog</span></span>      | <span data-ttu-id="0c181-263">False</span><span class="sxs-lookup"><span data-stu-id="0c181-263">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c181-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c181-265">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0c181-265">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="0c181-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c181-266">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="0c181-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c181-267">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="0c181-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c181-268">Search-Flags</span></span>           | <span data-ttu-id="0c181-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c181-269">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="0c181-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c181-270">System-Flags</span></span>           | <span data-ttu-id="0c181-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c181-271">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="0c181-272">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0c181-272">Classes used in</span></span>        | [<span data-ttu-id="0c181-273">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="0c181-273">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="0c181-274">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="0c181-274">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0c181-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0c181-275">Windows Server 2012</span></span>



| <span data-ttu-id="0c181-276">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c181-276">Entry</span></span> | <span data-ttu-id="0c181-277">Wert</span><span class="sxs-lookup"><span data-stu-id="0c181-277">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c181-278">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0c181-278">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="0c181-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c181-279">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="0c181-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c181-280">System-Only</span></span>            | <span data-ttu-id="0c181-281">False</span><span class="sxs-lookup"><span data-stu-id="0c181-281">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-282">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0c181-282">Is-Single-Valued</span></span>       | <span data-ttu-id="0c181-283">False</span><span class="sxs-lookup"><span data-stu-id="0c181-283">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-284">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0c181-284">Is Indexed</span></span>             | <span data-ttu-id="0c181-285">False</span><span class="sxs-lookup"><span data-stu-id="0c181-285">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-286">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0c181-286">In Global Catalog</span></span>      | <span data-ttu-id="0c181-287">False</span><span class="sxs-lookup"><span data-stu-id="0c181-287">False</span></span>                                                                                                                        |
| <span data-ttu-id="0c181-288">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c181-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c181-289">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0c181-289">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="0c181-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c181-290">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="0c181-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c181-291">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="0c181-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c181-292">Search-Flags</span></span>           | <span data-ttu-id="0c181-293">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c181-293">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="0c181-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c181-294">System-Flags</span></span>           | <span data-ttu-id="0c181-295">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c181-295">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="0c181-296">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0c181-296">Classes used in</span></span>        | [<span data-ttu-id="0c181-297">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="0c181-297">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="0c181-298">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="0c181-298">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



 

 





