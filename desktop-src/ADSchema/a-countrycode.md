---
title: Country-Code-Attribut
description: Gibt den Länder-/Regionscode für die bevorzugte Sprache des Benutzers an. Dieser Wert wird von Windows 2000 nicht verwendet.
ms.assetid: 7011cb76-aa86-4203-bcc4-0136bb11c403
ms.tgt_platform: multiple
keywords:
- AD-Schema für Country-Code-Attribut
- AD-Schema für CountryCode-Attribut
topic_type:
- apiref
api_name:
- Country-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9523a5aab21e81c2b0a5479def8ed8923751daed
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342713"
---
# <a name="country-code-attribute"></a><span data-ttu-id="019b2-106">Country-Code-Attribut</span><span class="sxs-lookup"><span data-stu-id="019b2-106">Country-Code attribute</span></span>

<span data-ttu-id="019b2-107">Gibt den Länder-/Regionscode für die bevorzugte Sprache des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="019b2-107">Specifies the country/region code for the user's language of choice.</span></span> <span data-ttu-id="019b2-108">Dieser Wert wird von Windows 2000 nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="019b2-108">This value is not used by Windows 2000.</span></span>



| <span data-ttu-id="019b2-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="019b2-109">Entry</span></span> | <span data-ttu-id="019b2-110">Wert</span><span class="sxs-lookup"><span data-stu-id="019b2-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="019b2-111">CN</span><span class="sxs-lookup"><span data-stu-id="019b2-111">CN</span></span>                | <span data-ttu-id="019b2-112">Country-Code</span><span class="sxs-lookup"><span data-stu-id="019b2-112">Country-Code</span></span>                            |
| <span data-ttu-id="019b2-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="019b2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="019b2-114">countryCode</span><span class="sxs-lookup"><span data-stu-id="019b2-114">countryCode</span></span>                             |
| <span data-ttu-id="019b2-115">Size</span><span class="sxs-lookup"><span data-stu-id="019b2-115">Size</span></span>              | <span data-ttu-id="019b2-116">2 Bytes</span><span class="sxs-lookup"><span data-stu-id="019b2-116">2 bytes</span></span>                                 |
| <span data-ttu-id="019b2-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="019b2-117">Update Privilege</span></span>  | <span data-ttu-id="019b2-118">Konto Besitzer oder Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="019b2-118">Account owner or domain administrator</span></span>   |
| <span data-ttu-id="019b2-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="019b2-119">Update Frequency</span></span>  | <span data-ttu-id="019b2-120">Wenn das Land oder die Region des Benutzers geändert wird.</span><span class="sxs-lookup"><span data-stu-id="019b2-120">When the user's country/region changes.</span></span> |
| <span data-ttu-id="019b2-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="019b2-121">Attribute-Id</span></span>      | <span data-ttu-id="019b2-122">1.2.840.113556.1.4.25</span><span class="sxs-lookup"><span data-stu-id="019b2-122">1.2.840.113556.1.4.25</span></span>                   |
| <span data-ttu-id="019b2-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="019b2-123">System-Id-Guid</span></span>    | <span data-ttu-id="019b2-124">5F d42471-1262-11D0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="019b2-124">5fd42471-1262-11d0-a060-00aa006c33ed</span></span>    |
| <span data-ttu-id="019b2-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="019b2-125">Syntax</span></span>            | [<span data-ttu-id="019b2-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="019b2-126">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="019b2-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="019b2-127">Implementations</span></span>

-   [<span data-ttu-id="019b2-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="019b2-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="019b2-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="019b2-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="019b2-130">**Adam**</span><span class="sxs-lookup"><span data-stu-id="019b2-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="019b2-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="019b2-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="019b2-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="019b2-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="019b2-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="019b2-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="019b2-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="019b2-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="019b2-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="019b2-135">Windows 2000 Server</span></span>



| <span data-ttu-id="019b2-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="019b2-136">Entry</span></span> | <span data-ttu-id="019b2-137">Wert</span><span class="sxs-lookup"><span data-stu-id="019b2-137">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="019b2-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="019b2-138">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="019b2-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="019b2-139">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="019b2-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="019b2-140">System-Only</span></span>            | <span data-ttu-id="019b2-141">False</span><span class="sxs-lookup"><span data-stu-id="019b2-141">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="019b2-142">Is-Single-Valued</span></span>       | <span data-ttu-id="019b2-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="019b2-143">True</span></span>                                                                                                                              |
| <span data-ttu-id="019b2-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="019b2-144">Is Indexed</span></span>             | <span data-ttu-id="019b2-145">False</span><span class="sxs-lookup"><span data-stu-id="019b2-145">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="019b2-146">In Global Catalog</span></span>      | <span data-ttu-id="019b2-147">False</span><span class="sxs-lookup"><span data-stu-id="019b2-147">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="019b2-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="019b2-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="019b2-149">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="019b2-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="019b2-150">Range-Lower</span></span>            | \-                                                                                                                                |
| <span data-ttu-id="019b2-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="019b2-151">Range-Upper</span></span>            | \-                                                                                                                                |
| <span data-ttu-id="019b2-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="019b2-152">Search-Flags</span></span>           | <span data-ttu-id="019b2-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019b2-153">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="019b2-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="019b2-154">System-Flags</span></span>           | <span data-ttu-id="019b2-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019b2-155">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="019b2-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="019b2-156">Classes used in</span></span>        | [<span data-ttu-id="019b2-157">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="019b2-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="019b2-158">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="019b2-158">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="019b2-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="019b2-159">Windows Server 2003</span></span>



| <span data-ttu-id="019b2-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="019b2-160">Entry</span></span> | <span data-ttu-id="019b2-161">Wert</span><span class="sxs-lookup"><span data-stu-id="019b2-161">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="019b2-162">Link-ID</span><span class="sxs-lookup"><span data-stu-id="019b2-162">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="019b2-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="019b2-163">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="019b2-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="019b2-164">System-Only</span></span>            | <span data-ttu-id="019b2-165">False</span><span class="sxs-lookup"><span data-stu-id="019b2-165">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="019b2-166">Is-Single-Valued</span></span>       | <span data-ttu-id="019b2-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="019b2-167">True</span></span>                                                                                                                              |
| <span data-ttu-id="019b2-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="019b2-168">Is Indexed</span></span>             | <span data-ttu-id="019b2-169">False</span><span class="sxs-lookup"><span data-stu-id="019b2-169">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="019b2-170">In Global Catalog</span></span>      | <span data-ttu-id="019b2-171">False</span><span class="sxs-lookup"><span data-stu-id="019b2-171">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="019b2-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="019b2-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="019b2-173">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="019b2-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="019b2-174">Range-Lower</span></span>            | <span data-ttu-id="019b2-175">0</span><span class="sxs-lookup"><span data-stu-id="019b2-175">0</span></span>                                                                                                                                 |
| <span data-ttu-id="019b2-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="019b2-176">Range-Upper</span></span>            | <span data-ttu-id="019b2-177">65.535</span><span class="sxs-lookup"><span data-stu-id="019b2-177">65535</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="019b2-178">Search-Flags</span></span>           | <span data-ttu-id="019b2-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019b2-179">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="019b2-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="019b2-180">System-Flags</span></span>           | <span data-ttu-id="019b2-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019b2-181">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="019b2-182">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="019b2-182">Classes used in</span></span>        | [<span data-ttu-id="019b2-183">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="019b2-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="019b2-184">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="019b2-184">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="adam"></a><span data-ttu-id="019b2-185">Adam</span><span class="sxs-lookup"><span data-stu-id="019b2-185">ADAM</span></span>



| <span data-ttu-id="019b2-186">Eingabe</span><span class="sxs-lookup"><span data-stu-id="019b2-186">Entry</span></span> | <span data-ttu-id="019b2-187">Wert</span><span class="sxs-lookup"><span data-stu-id="019b2-187">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="019b2-188">Link-ID</span><span class="sxs-lookup"><span data-stu-id="019b2-188">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="019b2-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="019b2-189">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="019b2-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="019b2-190">System-Only</span></span>            | <span data-ttu-id="019b2-191">False</span><span class="sxs-lookup"><span data-stu-id="019b2-191">False</span></span>                                                          |
| <span data-ttu-id="019b2-192">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="019b2-192">Is-Single-Valued</span></span>       | <span data-ttu-id="019b2-193">Richtig</span><span class="sxs-lookup"><span data-stu-id="019b2-193">True</span></span>                                                           |
| <span data-ttu-id="019b2-194">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="019b2-194">Is Indexed</span></span>             | <span data-ttu-id="019b2-195">False</span><span class="sxs-lookup"><span data-stu-id="019b2-195">False</span></span>                                                          |
| <span data-ttu-id="019b2-196">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="019b2-196">In Global Catalog</span></span>      | <span data-ttu-id="019b2-197">False</span><span class="sxs-lookup"><span data-stu-id="019b2-197">False</span></span>                                                          |
| <span data-ttu-id="019b2-198">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="019b2-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="019b2-199">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="019b2-199">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="019b2-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="019b2-200">Range-Lower</span></span>            | <span data-ttu-id="019b2-201">0</span><span class="sxs-lookup"><span data-stu-id="019b2-201">0</span></span>                                                              |
| <span data-ttu-id="019b2-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="019b2-202">Range-Upper</span></span>            | <span data-ttu-id="019b2-203">65.535</span><span class="sxs-lookup"><span data-stu-id="019b2-203">65535</span></span>                                                          |
| <span data-ttu-id="019b2-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="019b2-204">Search-Flags</span></span>           | <span data-ttu-id="019b2-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019b2-205">0x00000010</span></span>                                                     |
| <span data-ttu-id="019b2-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="019b2-206">System-Flags</span></span>           | <span data-ttu-id="019b2-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019b2-207">0x00000010</span></span>                                                     |
| <span data-ttu-id="019b2-208">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="019b2-208">Classes used in</span></span>        | [<span data-ttu-id="019b2-209">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="019b2-209">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="019b2-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="019b2-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="019b2-211">Eingabe</span><span class="sxs-lookup"><span data-stu-id="019b2-211">Entry</span></span> | <span data-ttu-id="019b2-212">Wert</span><span class="sxs-lookup"><span data-stu-id="019b2-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="019b2-213">Link-ID</span><span class="sxs-lookup"><span data-stu-id="019b2-213">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="019b2-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="019b2-214">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="019b2-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="019b2-215">System-Only</span></span>            | <span data-ttu-id="019b2-216">False</span><span class="sxs-lookup"><span data-stu-id="019b2-216">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-217">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="019b2-217">Is-Single-Valued</span></span>       | <span data-ttu-id="019b2-218">Richtig</span><span class="sxs-lookup"><span data-stu-id="019b2-218">True</span></span>                                                                                                                              |
| <span data-ttu-id="019b2-219">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="019b2-219">Is Indexed</span></span>             | <span data-ttu-id="019b2-220">False</span><span class="sxs-lookup"><span data-stu-id="019b2-220">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-221">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="019b2-221">In Global Catalog</span></span>      | <span data-ttu-id="019b2-222">False</span><span class="sxs-lookup"><span data-stu-id="019b2-222">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="019b2-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="019b2-224">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="019b2-224">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="019b2-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="019b2-225">Range-Lower</span></span>            | <span data-ttu-id="019b2-226">0</span><span class="sxs-lookup"><span data-stu-id="019b2-226">0</span></span>                                                                                                                                 |
| <span data-ttu-id="019b2-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="019b2-227">Range-Upper</span></span>            | <span data-ttu-id="019b2-228">65.535</span><span class="sxs-lookup"><span data-stu-id="019b2-228">65535</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="019b2-229">Search-Flags</span></span>           | <span data-ttu-id="019b2-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019b2-230">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="019b2-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="019b2-231">System-Flags</span></span>           | <span data-ttu-id="019b2-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019b2-232">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="019b2-233">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="019b2-233">Classes used in</span></span>        | [<span data-ttu-id="019b2-234">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="019b2-234">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="019b2-235">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="019b2-235">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="019b2-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="019b2-236">Windows Server 2008</span></span>



| <span data-ttu-id="019b2-237">Eingabe</span><span class="sxs-lookup"><span data-stu-id="019b2-237">Entry</span></span> | <span data-ttu-id="019b2-238">Wert</span><span class="sxs-lookup"><span data-stu-id="019b2-238">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="019b2-239">Link-ID</span><span class="sxs-lookup"><span data-stu-id="019b2-239">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="019b2-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="019b2-240">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="019b2-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="019b2-241">System-Only</span></span>            | <span data-ttu-id="019b2-242">False</span><span class="sxs-lookup"><span data-stu-id="019b2-242">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-243">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="019b2-243">Is-Single-Valued</span></span>       | <span data-ttu-id="019b2-244">Richtig</span><span class="sxs-lookup"><span data-stu-id="019b2-244">True</span></span>                                                                                                                              |
| <span data-ttu-id="019b2-245">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="019b2-245">Is Indexed</span></span>             | <span data-ttu-id="019b2-246">False</span><span class="sxs-lookup"><span data-stu-id="019b2-246">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-247">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="019b2-247">In Global Catalog</span></span>      | <span data-ttu-id="019b2-248">False</span><span class="sxs-lookup"><span data-stu-id="019b2-248">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-249">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="019b2-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="019b2-250">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="019b2-250">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="019b2-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="019b2-251">Range-Lower</span></span>            | <span data-ttu-id="019b2-252">0</span><span class="sxs-lookup"><span data-stu-id="019b2-252">0</span></span>                                                                                                                                 |
| <span data-ttu-id="019b2-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="019b2-253">Range-Upper</span></span>            | <span data-ttu-id="019b2-254">65.535</span><span class="sxs-lookup"><span data-stu-id="019b2-254">65535</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="019b2-255">Search-Flags</span></span>           | <span data-ttu-id="019b2-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019b2-256">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="019b2-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="019b2-257">System-Flags</span></span>           | <span data-ttu-id="019b2-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019b2-258">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="019b2-259">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="019b2-259">Classes used in</span></span>        | [<span data-ttu-id="019b2-260">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="019b2-260">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="019b2-261">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="019b2-261">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="019b2-262">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="019b2-262">Windows Server 2008 R2</span></span>



| <span data-ttu-id="019b2-263">Eingabe</span><span class="sxs-lookup"><span data-stu-id="019b2-263">Entry</span></span> | <span data-ttu-id="019b2-264">Wert</span><span class="sxs-lookup"><span data-stu-id="019b2-264">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="019b2-265">Link-ID</span><span class="sxs-lookup"><span data-stu-id="019b2-265">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="019b2-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="019b2-266">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="019b2-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="019b2-267">System-Only</span></span>            | <span data-ttu-id="019b2-268">False</span><span class="sxs-lookup"><span data-stu-id="019b2-268">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-269">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="019b2-269">Is-Single-Valued</span></span>       | <span data-ttu-id="019b2-270">Richtig</span><span class="sxs-lookup"><span data-stu-id="019b2-270">True</span></span>                                                                                                                              |
| <span data-ttu-id="019b2-271">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="019b2-271">Is Indexed</span></span>             | <span data-ttu-id="019b2-272">False</span><span class="sxs-lookup"><span data-stu-id="019b2-272">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-273">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="019b2-273">In Global Catalog</span></span>      | <span data-ttu-id="019b2-274">False</span><span class="sxs-lookup"><span data-stu-id="019b2-274">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-275">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="019b2-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="019b2-276">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="019b2-276">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="019b2-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="019b2-277">Range-Lower</span></span>            | <span data-ttu-id="019b2-278">0</span><span class="sxs-lookup"><span data-stu-id="019b2-278">0</span></span>                                                                                                                                 |
| <span data-ttu-id="019b2-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="019b2-279">Range-Upper</span></span>            | <span data-ttu-id="019b2-280">65.535</span><span class="sxs-lookup"><span data-stu-id="019b2-280">65535</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="019b2-281">Search-Flags</span></span>           | <span data-ttu-id="019b2-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019b2-282">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="019b2-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="019b2-283">System-Flags</span></span>           | <span data-ttu-id="019b2-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019b2-284">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="019b2-285">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="019b2-285">Classes used in</span></span>        | [<span data-ttu-id="019b2-286">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="019b2-286">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="019b2-287">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="019b2-287">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="019b2-288">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="019b2-288">Windows Server 2012</span></span>



| <span data-ttu-id="019b2-289">Eingabe</span><span class="sxs-lookup"><span data-stu-id="019b2-289">Entry</span></span> | <span data-ttu-id="019b2-290">Wert</span><span class="sxs-lookup"><span data-stu-id="019b2-290">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="019b2-291">Link-ID</span><span class="sxs-lookup"><span data-stu-id="019b2-291">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="019b2-292">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="019b2-292">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="019b2-293">System-Only</span><span class="sxs-lookup"><span data-stu-id="019b2-293">System-Only</span></span>            | <span data-ttu-id="019b2-294">False</span><span class="sxs-lookup"><span data-stu-id="019b2-294">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-295">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="019b2-295">Is-Single-Valued</span></span>       | <span data-ttu-id="019b2-296">Richtig</span><span class="sxs-lookup"><span data-stu-id="019b2-296">True</span></span>                                                                                                                              |
| <span data-ttu-id="019b2-297">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="019b2-297">Is Indexed</span></span>             | <span data-ttu-id="019b2-298">False</span><span class="sxs-lookup"><span data-stu-id="019b2-298">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-299">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="019b2-299">In Global Catalog</span></span>      | <span data-ttu-id="019b2-300">False</span><span class="sxs-lookup"><span data-stu-id="019b2-300">False</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-301">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="019b2-301">NT-Security-Descriptor</span></span> | <span data-ttu-id="019b2-302">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="019b2-302">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="019b2-303">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="019b2-303">Range-Lower</span></span>            | <span data-ttu-id="019b2-304">0</span><span class="sxs-lookup"><span data-stu-id="019b2-304">0</span></span>                                                                                                                                 |
| <span data-ttu-id="019b2-305">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="019b2-305">Range-Upper</span></span>            | <span data-ttu-id="019b2-306">65.535</span><span class="sxs-lookup"><span data-stu-id="019b2-306">65535</span></span>                                                                                                                             |
| <span data-ttu-id="019b2-307">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="019b2-307">Search-Flags</span></span>           | <span data-ttu-id="019b2-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019b2-308">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="019b2-309">System-Flags</span><span class="sxs-lookup"><span data-stu-id="019b2-309">System-Flags</span></span>           | <span data-ttu-id="019b2-310">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019b2-310">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="019b2-311">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="019b2-311">Classes used in</span></span>        | [<span data-ttu-id="019b2-312">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="019b2-312">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="019b2-313">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="019b2-313">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



 

 





