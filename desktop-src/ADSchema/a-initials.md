---
title: Initialen-Attribut
description: Enthält die Initialen für Teile des vollständigen Namens des Benutzers. Diese kann als naher Ausgangswert im Windows-Adressbuch verwendet werden.
ms.assetid: 220b4448-5276-4c3f-8a1b-217cec06135a
ms.tgt_platform: multiple
keywords:
- Initialen-Attribut AD-Schema
- Initialen-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Initials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 946f6c9633c1126a30ae4898274096a54db9a402
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344754"
---
# <a name="initials-attribute"></a><span data-ttu-id="04991-106">Initialen-Attribut</span><span class="sxs-lookup"><span data-stu-id="04991-106">Initials attribute</span></span>

<span data-ttu-id="04991-107">Enthält die Initialen für Teile des vollständigen Namens des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="04991-107">Contains the initials for parts of the user's full name.</span></span> <span data-ttu-id="04991-108">Diese kann als naher Ausgangswert im Windows-Adressbuch verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04991-108">This may be used as the middle initial in the Windows Address Book.</span></span>



| <span data-ttu-id="04991-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04991-109">Entry</span></span> | <span data-ttu-id="04991-110">Wert</span><span class="sxs-lookup"><span data-stu-id="04991-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="04991-111">CN</span><span class="sxs-lookup"><span data-stu-id="04991-111">CN</span></span>                | <span data-ttu-id="04991-112">Initialen</span><span class="sxs-lookup"><span data-stu-id="04991-112">Initials</span></span>                                    |
| <span data-ttu-id="04991-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="04991-113">Ldap-Display-Name</span></span> | <span data-ttu-id="04991-114">Initials</span><span class="sxs-lookup"><span data-stu-id="04991-114">initials</span></span>                                    |
| <span data-ttu-id="04991-115">Size</span><span class="sxs-lookup"><span data-stu-id="04991-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="04991-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="04991-116">Update Privilege</span></span>  | <span data-ttu-id="04991-117">Domänen Administrator oder Konto Besitzer.</span><span class="sxs-lookup"><span data-stu-id="04991-117">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="04991-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="04991-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="04991-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="04991-119">Attribute-Id</span></span>      | <span data-ttu-id="04991-120">2.5.4.43</span><span class="sxs-lookup"><span data-stu-id="04991-120">2.5.4.43</span></span>                                    |
| <span data-ttu-id="04991-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="04991-121">System-Id-Guid</span></span>    | <span data-ttu-id="04991-122">f0f8ff90-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="04991-122">f0f8ff90-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="04991-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="04991-123">Syntax</span></span>            | [<span data-ttu-id="04991-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="04991-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="04991-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="04991-125">Implementations</span></span>

-   [<span data-ttu-id="04991-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="04991-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="04991-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="04991-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="04991-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="04991-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="04991-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="04991-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="04991-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="04991-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="04991-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="04991-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="04991-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04991-132">Windows 2000 Server</span></span>



| <span data-ttu-id="04991-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04991-133">Entry</span></span> | <span data-ttu-id="04991-134">Wert</span><span class="sxs-lookup"><span data-stu-id="04991-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="04991-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04991-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="04991-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04991-136">MAPI-Id</span></span>                | <span data-ttu-id="04991-137">0x3a0a</span><span class="sxs-lookup"><span data-stu-id="04991-137">0x3A0A</span></span>                                                             |
| <span data-ttu-id="04991-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="04991-138">System-Only</span></span>            | <span data-ttu-id="04991-139">False</span><span class="sxs-lookup"><span data-stu-id="04991-139">False</span></span>                                                              |
| <span data-ttu-id="04991-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04991-140">Is-Single-Valued</span></span>       | <span data-ttu-id="04991-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="04991-141">True</span></span>                                                               |
| <span data-ttu-id="04991-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04991-142">Is Indexed</span></span>             | <span data-ttu-id="04991-143">False</span><span class="sxs-lookup"><span data-stu-id="04991-143">False</span></span>                                                              |
| <span data-ttu-id="04991-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04991-144">In Global Catalog</span></span>      | <span data-ttu-id="04991-145">False</span><span class="sxs-lookup"><span data-stu-id="04991-145">False</span></span>                                                              |
| <span data-ttu-id="04991-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04991-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="04991-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04991-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="04991-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04991-148">Range-Lower</span></span>            | <span data-ttu-id="04991-149">1</span><span class="sxs-lookup"><span data-stu-id="04991-149">1</span></span>                                                                  |
| <span data-ttu-id="04991-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04991-150">Range-Upper</span></span>            | <span data-ttu-id="04991-151">6</span><span class="sxs-lookup"><span data-stu-id="04991-151">6</span></span>                                                                  |
| <span data-ttu-id="04991-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04991-152">Search-Flags</span></span>           | <span data-ttu-id="04991-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04991-153">0x00000000</span></span>                                                         |
| <span data-ttu-id="04991-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04991-154">System-Flags</span></span>           | <span data-ttu-id="04991-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04991-155">0x00000010</span></span>                                                         |
| <span data-ttu-id="04991-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04991-156">Classes used in</span></span>        | [<span data-ttu-id="04991-157">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="04991-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="04991-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="04991-158">Windows Server 2003</span></span>



| <span data-ttu-id="04991-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04991-159">Entry</span></span> | <span data-ttu-id="04991-160">Wert</span><span class="sxs-lookup"><span data-stu-id="04991-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04991-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04991-161">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="04991-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04991-162">MAPI-Id</span></span>                | <span data-ttu-id="04991-163">0x3a0a</span><span class="sxs-lookup"><span data-stu-id="04991-163">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="04991-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="04991-164">System-Only</span></span>            | <span data-ttu-id="04991-165">False</span><span class="sxs-lookup"><span data-stu-id="04991-165">False</span></span>                                                                                                                  |
| <span data-ttu-id="04991-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04991-166">Is-Single-Valued</span></span>       | <span data-ttu-id="04991-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="04991-167">True</span></span>                                                                                                                   |
| <span data-ttu-id="04991-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04991-168">Is Indexed</span></span>             | <span data-ttu-id="04991-169">False</span><span class="sxs-lookup"><span data-stu-id="04991-169">False</span></span>                                                                                                                  |
| <span data-ttu-id="04991-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04991-170">In Global Catalog</span></span>      | <span data-ttu-id="04991-171">False</span><span class="sxs-lookup"><span data-stu-id="04991-171">False</span></span>                                                                                                                  |
| <span data-ttu-id="04991-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04991-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="04991-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04991-173">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="04991-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04991-174">Range-Lower</span></span>            | <span data-ttu-id="04991-175">1</span><span class="sxs-lookup"><span data-stu-id="04991-175">1</span></span>                                                                                                                      |
| <span data-ttu-id="04991-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04991-176">Range-Upper</span></span>            | <span data-ttu-id="04991-177">6</span><span class="sxs-lookup"><span data-stu-id="04991-177">6</span></span>                                                                                                                      |
| <span data-ttu-id="04991-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04991-178">Search-Flags</span></span>           | <span data-ttu-id="04991-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04991-179">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="04991-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04991-180">System-Flags</span></span>           | <span data-ttu-id="04991-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04991-181">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="04991-182">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04991-182">Classes used in</span></span>        | [<span data-ttu-id="04991-183">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="04991-183">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="04991-184">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="04991-184">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="04991-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="04991-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="04991-186">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04991-186">Entry</span></span> | <span data-ttu-id="04991-187">Wert</span><span class="sxs-lookup"><span data-stu-id="04991-187">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04991-188">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04991-188">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="04991-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04991-189">MAPI-Id</span></span>                | <span data-ttu-id="04991-190">0x3a0a</span><span class="sxs-lookup"><span data-stu-id="04991-190">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="04991-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="04991-191">System-Only</span></span>            | <span data-ttu-id="04991-192">False</span><span class="sxs-lookup"><span data-stu-id="04991-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="04991-193">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04991-193">Is-Single-Valued</span></span>       | <span data-ttu-id="04991-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="04991-194">True</span></span>                                                                                                                   |
| <span data-ttu-id="04991-195">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04991-195">Is Indexed</span></span>             | <span data-ttu-id="04991-196">False</span><span class="sxs-lookup"><span data-stu-id="04991-196">False</span></span>                                                                                                                  |
| <span data-ttu-id="04991-197">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04991-197">In Global Catalog</span></span>      | <span data-ttu-id="04991-198">False</span><span class="sxs-lookup"><span data-stu-id="04991-198">False</span></span>                                                                                                                  |
| <span data-ttu-id="04991-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04991-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="04991-200">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04991-200">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="04991-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04991-201">Range-Lower</span></span>            | <span data-ttu-id="04991-202">1</span><span class="sxs-lookup"><span data-stu-id="04991-202">1</span></span>                                                                                                                      |
| <span data-ttu-id="04991-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04991-203">Range-Upper</span></span>            | <span data-ttu-id="04991-204">6</span><span class="sxs-lookup"><span data-stu-id="04991-204">6</span></span>                                                                                                                      |
| <span data-ttu-id="04991-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04991-205">Search-Flags</span></span>           | <span data-ttu-id="04991-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04991-206">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="04991-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04991-207">System-Flags</span></span>           | <span data-ttu-id="04991-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04991-208">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="04991-209">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04991-209">Classes used in</span></span>        | [<span data-ttu-id="04991-210">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="04991-210">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="04991-211">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="04991-211">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="04991-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04991-212">Windows Server 2008</span></span>



| <span data-ttu-id="04991-213">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04991-213">Entry</span></span> | <span data-ttu-id="04991-214">Wert</span><span class="sxs-lookup"><span data-stu-id="04991-214">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04991-215">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04991-215">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="04991-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04991-216">MAPI-Id</span></span>                | <span data-ttu-id="04991-217">0x3a0a</span><span class="sxs-lookup"><span data-stu-id="04991-217">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="04991-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="04991-218">System-Only</span></span>            | <span data-ttu-id="04991-219">False</span><span class="sxs-lookup"><span data-stu-id="04991-219">False</span></span>                                                                                                                  |
| <span data-ttu-id="04991-220">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04991-220">Is-Single-Valued</span></span>       | <span data-ttu-id="04991-221">Richtig</span><span class="sxs-lookup"><span data-stu-id="04991-221">True</span></span>                                                                                                                   |
| <span data-ttu-id="04991-222">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04991-222">Is Indexed</span></span>             | <span data-ttu-id="04991-223">False</span><span class="sxs-lookup"><span data-stu-id="04991-223">False</span></span>                                                                                                                  |
| <span data-ttu-id="04991-224">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04991-224">In Global Catalog</span></span>      | <span data-ttu-id="04991-225">False</span><span class="sxs-lookup"><span data-stu-id="04991-225">False</span></span>                                                                                                                  |
| <span data-ttu-id="04991-226">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04991-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="04991-227">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04991-227">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="04991-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04991-228">Range-Lower</span></span>            | <span data-ttu-id="04991-229">1</span><span class="sxs-lookup"><span data-stu-id="04991-229">1</span></span>                                                                                                                      |
| <span data-ttu-id="04991-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04991-230">Range-Upper</span></span>            | <span data-ttu-id="04991-231">6</span><span class="sxs-lookup"><span data-stu-id="04991-231">6</span></span>                                                                                                                      |
| <span data-ttu-id="04991-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04991-232">Search-Flags</span></span>           | <span data-ttu-id="04991-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04991-233">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="04991-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04991-234">System-Flags</span></span>           | <span data-ttu-id="04991-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04991-235">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="04991-236">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04991-236">Classes used in</span></span>        | [<span data-ttu-id="04991-237">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="04991-237">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="04991-238">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="04991-238">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="04991-239">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="04991-239">Windows Server 2008 R2</span></span>



| <span data-ttu-id="04991-240">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04991-240">Entry</span></span> | <span data-ttu-id="04991-241">Wert</span><span class="sxs-lookup"><span data-stu-id="04991-241">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04991-242">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04991-242">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="04991-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04991-243">MAPI-Id</span></span>                | <span data-ttu-id="04991-244">0x3a0a</span><span class="sxs-lookup"><span data-stu-id="04991-244">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="04991-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="04991-245">System-Only</span></span>            | <span data-ttu-id="04991-246">False</span><span class="sxs-lookup"><span data-stu-id="04991-246">False</span></span>                                                                                                                  |
| <span data-ttu-id="04991-247">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04991-247">Is-Single-Valued</span></span>       | <span data-ttu-id="04991-248">Richtig</span><span class="sxs-lookup"><span data-stu-id="04991-248">True</span></span>                                                                                                                   |
| <span data-ttu-id="04991-249">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04991-249">Is Indexed</span></span>             | <span data-ttu-id="04991-250">False</span><span class="sxs-lookup"><span data-stu-id="04991-250">False</span></span>                                                                                                                  |
| <span data-ttu-id="04991-251">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04991-251">In Global Catalog</span></span>      | <span data-ttu-id="04991-252">False</span><span class="sxs-lookup"><span data-stu-id="04991-252">False</span></span>                                                                                                                  |
| <span data-ttu-id="04991-253">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04991-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="04991-254">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04991-254">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="04991-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04991-255">Range-Lower</span></span>            | <span data-ttu-id="04991-256">1</span><span class="sxs-lookup"><span data-stu-id="04991-256">1</span></span>                                                                                                                      |
| <span data-ttu-id="04991-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04991-257">Range-Upper</span></span>            | <span data-ttu-id="04991-258">6</span><span class="sxs-lookup"><span data-stu-id="04991-258">6</span></span>                                                                                                                      |
| <span data-ttu-id="04991-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04991-259">Search-Flags</span></span>           | <span data-ttu-id="04991-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04991-260">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="04991-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04991-261">System-Flags</span></span>           | <span data-ttu-id="04991-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04991-262">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="04991-263">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04991-263">Classes used in</span></span>        | [<span data-ttu-id="04991-264">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="04991-264">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="04991-265">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="04991-265">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="04991-266">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04991-266">Windows Server 2012</span></span>



| <span data-ttu-id="04991-267">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04991-267">Entry</span></span> | <span data-ttu-id="04991-268">Wert</span><span class="sxs-lookup"><span data-stu-id="04991-268">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04991-269">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04991-269">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="04991-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04991-270">MAPI-Id</span></span>                | <span data-ttu-id="04991-271">0x3a0a</span><span class="sxs-lookup"><span data-stu-id="04991-271">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="04991-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="04991-272">System-Only</span></span>            | <span data-ttu-id="04991-273">False</span><span class="sxs-lookup"><span data-stu-id="04991-273">False</span></span>                                                                                                                  |
| <span data-ttu-id="04991-274">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04991-274">Is-Single-Valued</span></span>       | <span data-ttu-id="04991-275">Richtig</span><span class="sxs-lookup"><span data-stu-id="04991-275">True</span></span>                                                                                                                   |
| <span data-ttu-id="04991-276">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04991-276">Is Indexed</span></span>             | <span data-ttu-id="04991-277">False</span><span class="sxs-lookup"><span data-stu-id="04991-277">False</span></span>                                                                                                                  |
| <span data-ttu-id="04991-278">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04991-278">In Global Catalog</span></span>      | <span data-ttu-id="04991-279">False</span><span class="sxs-lookup"><span data-stu-id="04991-279">False</span></span>                                                                                                                  |
| <span data-ttu-id="04991-280">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04991-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="04991-281">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04991-281">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="04991-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04991-282">Range-Lower</span></span>            | <span data-ttu-id="04991-283">1</span><span class="sxs-lookup"><span data-stu-id="04991-283">1</span></span>                                                                                                                      |
| <span data-ttu-id="04991-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04991-284">Range-Upper</span></span>            | <span data-ttu-id="04991-285">6</span><span class="sxs-lookup"><span data-stu-id="04991-285">6</span></span>                                                                                                                      |
| <span data-ttu-id="04991-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04991-286">Search-Flags</span></span>           | <span data-ttu-id="04991-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04991-287">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="04991-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04991-288">System-Flags</span></span>           | <span data-ttu-id="04991-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04991-289">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="04991-290">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04991-290">Classes used in</span></span>        | [<span data-ttu-id="04991-291">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="04991-291">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="04991-292">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="04991-292">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





