---
title: Shell-Eigenschaften Seiten-Attribut
description: Die Bestellnummer und die GUID von Eigenschaften Seiten zum Verwalten von Active Directory-Objekten. Auf diese Eigenschaften Seiten kann von der Windows-Shell zugegriffen werden. Weitere Informationen finden Sie im Dokument Erweitern der Benutzeroberfläche für Verzeichnisobjekte.
ms.assetid: e0edd91b-bdb6-47aa-9be2-8a23a89adb26
ms.tgt_platform: multiple
keywords:
- AD-Schema für Shell-Eigenschaften Seiten-Attribut
- shellpropertypages-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Shell-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: befad2334a754843fa0ae412565db8c82260f7cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107523"
---
# <a name="shell-property-pages-attribute"></a><span data-ttu-id="081aa-107">Shell-Eigenschaften Seiten-Attribut</span><span class="sxs-lookup"><span data-stu-id="081aa-107">Shell-Property-Pages attribute</span></span>

<span data-ttu-id="081aa-108">Die Bestellnummer und die GUID von Eigenschaften Seiten zum Verwalten von Active Directory-Objekten.</span><span class="sxs-lookup"><span data-stu-id="081aa-108">The order number and GUID of property pages for managing Active Directory objects.</span></span> <span data-ttu-id="081aa-109">Auf diese Eigenschaften Seiten kann von der Windows-Shell zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="081aa-109">These property pages can be accessed from the Windows shell.</span></span> <span data-ttu-id="081aa-110">Weitere Informationen finden Sie im Dokument Erweitern der Benutzeroberfläche für Verzeichnisobjekte.</span><span class="sxs-lookup"><span data-stu-id="081aa-110">For more information see the document, Extending the User Interface for Directory Objects.</span></span>



| <span data-ttu-id="081aa-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="081aa-111">Entry</span></span> | <span data-ttu-id="081aa-112">Wert</span><span class="sxs-lookup"><span data-stu-id="081aa-112">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="081aa-113">CN</span><span class="sxs-lookup"><span data-stu-id="081aa-113">CN</span></span>                | <span data-ttu-id="081aa-114">Shell-Eigenschaften Seiten</span><span class="sxs-lookup"><span data-stu-id="081aa-114">Shell-Property-Pages</span></span>                           |
| <span data-ttu-id="081aa-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="081aa-115">Ldap-Display-Name</span></span> | <span data-ttu-id="081aa-116">shellpropertypages</span><span class="sxs-lookup"><span data-stu-id="081aa-116">shellPropertyPages</span></span>                             |
| <span data-ttu-id="081aa-117">Size</span><span class="sxs-lookup"><span data-stu-id="081aa-117">Size</span></span>              | \-                                             |
| <span data-ttu-id="081aa-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="081aa-118">Update Privilege</span></span>  | <span data-ttu-id="081aa-119">Domänen Administrator oder Anwendungsentwickler.</span><span class="sxs-lookup"><span data-stu-id="081aa-119">Domain administrator or application developer.</span></span> |
| <span data-ttu-id="081aa-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="081aa-120">Update Frequency</span></span>  | <span data-ttu-id="081aa-121">Immer dann, wenn eine Eigenschaften Seite hinzugefügt oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="081aa-121">Whenever a property page is added or removed.</span></span>  |
| <span data-ttu-id="081aa-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="081aa-122">Attribute-Id</span></span>      | <span data-ttu-id="081aa-123">1.2.840.113556.1.4.563</span><span class="sxs-lookup"><span data-stu-id="081aa-123">1.2.840.113556.1.4.563</span></span>                         |
| <span data-ttu-id="081aa-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="081aa-124">System-Id-Guid</span></span>    | <span data-ttu-id="081aa-125">52458039-ca6a-11D0-affinf-0000f 80367c1</span><span class="sxs-lookup"><span data-stu-id="081aa-125">52458039-ca6a-11d0-afff-0000f80367c1</span></span>           |
| <span data-ttu-id="081aa-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="081aa-126">Syntax</span></span>            | [<span data-ttu-id="081aa-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="081aa-127">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="081aa-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="081aa-128">Implementations</span></span>

-   [<span data-ttu-id="081aa-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="081aa-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="081aa-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="081aa-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="081aa-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="081aa-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="081aa-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="081aa-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="081aa-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="081aa-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="081aa-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="081aa-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="081aa-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="081aa-135">Windows 2000 Server</span></span>



| <span data-ttu-id="081aa-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="081aa-136">Entry</span></span> | <span data-ttu-id="081aa-137">Wert</span><span class="sxs-lookup"><span data-stu-id="081aa-137">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="081aa-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="081aa-138">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="081aa-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="081aa-139">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="081aa-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="081aa-140">System-Only</span></span>            | <span data-ttu-id="081aa-141">False</span><span class="sxs-lookup"><span data-stu-id="081aa-141">False</span></span>                                                      |
| <span data-ttu-id="081aa-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="081aa-142">Is-Single-Valued</span></span>       | <span data-ttu-id="081aa-143">False</span><span class="sxs-lookup"><span data-stu-id="081aa-143">False</span></span>                                                      |
| <span data-ttu-id="081aa-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="081aa-144">Is Indexed</span></span>             | <span data-ttu-id="081aa-145">False</span><span class="sxs-lookup"><span data-stu-id="081aa-145">False</span></span>                                                      |
| <span data-ttu-id="081aa-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="081aa-146">In Global Catalog</span></span>      | <span data-ttu-id="081aa-147">False</span><span class="sxs-lookup"><span data-stu-id="081aa-147">False</span></span>                                                      |
| <span data-ttu-id="081aa-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="081aa-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="081aa-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="081aa-149">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="081aa-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="081aa-150">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="081aa-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="081aa-151">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="081aa-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="081aa-152">Search-Flags</span></span>           | <span data-ttu-id="081aa-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="081aa-153">0x00000000</span></span>                                                 |
| <span data-ttu-id="081aa-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="081aa-154">System-Flags</span></span>           | <span data-ttu-id="081aa-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="081aa-155">0x00000010</span></span>                                                 |
| <span data-ttu-id="081aa-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="081aa-156">Classes used in</span></span>        | [<span data-ttu-id="081aa-157">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="081aa-157">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="081aa-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="081aa-158">Windows Server 2003</span></span>



| <span data-ttu-id="081aa-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="081aa-159">Entry</span></span> | <span data-ttu-id="081aa-160">Wert</span><span class="sxs-lookup"><span data-stu-id="081aa-160">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="081aa-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="081aa-161">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="081aa-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="081aa-162">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="081aa-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="081aa-163">System-Only</span></span>            | <span data-ttu-id="081aa-164">False</span><span class="sxs-lookup"><span data-stu-id="081aa-164">False</span></span>                                                      |
| <span data-ttu-id="081aa-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="081aa-165">Is-Single-Valued</span></span>       | <span data-ttu-id="081aa-166">False</span><span class="sxs-lookup"><span data-stu-id="081aa-166">False</span></span>                                                      |
| <span data-ttu-id="081aa-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="081aa-167">Is Indexed</span></span>             | <span data-ttu-id="081aa-168">False</span><span class="sxs-lookup"><span data-stu-id="081aa-168">False</span></span>                                                      |
| <span data-ttu-id="081aa-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="081aa-169">In Global Catalog</span></span>      | <span data-ttu-id="081aa-170">False</span><span class="sxs-lookup"><span data-stu-id="081aa-170">False</span></span>                                                      |
| <span data-ttu-id="081aa-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="081aa-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="081aa-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="081aa-172">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="081aa-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="081aa-173">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="081aa-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="081aa-174">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="081aa-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="081aa-175">Search-Flags</span></span>           | <span data-ttu-id="081aa-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="081aa-176">0x00000000</span></span>                                                 |
| <span data-ttu-id="081aa-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="081aa-177">System-Flags</span></span>           | <span data-ttu-id="081aa-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="081aa-178">0x00000010</span></span>                                                 |
| <span data-ttu-id="081aa-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="081aa-179">Classes used in</span></span>        | [<span data-ttu-id="081aa-180">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="081aa-180">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="081aa-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="081aa-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="081aa-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="081aa-182">Entry</span></span> | <span data-ttu-id="081aa-183">Wert</span><span class="sxs-lookup"><span data-stu-id="081aa-183">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="081aa-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="081aa-184">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="081aa-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="081aa-185">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="081aa-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="081aa-186">System-Only</span></span>            | <span data-ttu-id="081aa-187">False</span><span class="sxs-lookup"><span data-stu-id="081aa-187">False</span></span>                                                      |
| <span data-ttu-id="081aa-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="081aa-188">Is-Single-Valued</span></span>       | <span data-ttu-id="081aa-189">False</span><span class="sxs-lookup"><span data-stu-id="081aa-189">False</span></span>                                                      |
| <span data-ttu-id="081aa-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="081aa-190">Is Indexed</span></span>             | <span data-ttu-id="081aa-191">False</span><span class="sxs-lookup"><span data-stu-id="081aa-191">False</span></span>                                                      |
| <span data-ttu-id="081aa-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="081aa-192">In Global Catalog</span></span>      | <span data-ttu-id="081aa-193">False</span><span class="sxs-lookup"><span data-stu-id="081aa-193">False</span></span>                                                      |
| <span data-ttu-id="081aa-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="081aa-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="081aa-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="081aa-195">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="081aa-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="081aa-196">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="081aa-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="081aa-197">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="081aa-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="081aa-198">Search-Flags</span></span>           | <span data-ttu-id="081aa-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="081aa-199">0x00000000</span></span>                                                 |
| <span data-ttu-id="081aa-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="081aa-200">System-Flags</span></span>           | <span data-ttu-id="081aa-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="081aa-201">0x00000010</span></span>                                                 |
| <span data-ttu-id="081aa-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="081aa-202">Classes used in</span></span>        | [<span data-ttu-id="081aa-203">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="081aa-203">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="081aa-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="081aa-204">Windows Server 2008</span></span>



| <span data-ttu-id="081aa-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="081aa-205">Entry</span></span> | <span data-ttu-id="081aa-206">Wert</span><span class="sxs-lookup"><span data-stu-id="081aa-206">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="081aa-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="081aa-207">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="081aa-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="081aa-208">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="081aa-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="081aa-209">System-Only</span></span>            | <span data-ttu-id="081aa-210">False</span><span class="sxs-lookup"><span data-stu-id="081aa-210">False</span></span>                                                      |
| <span data-ttu-id="081aa-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="081aa-211">Is-Single-Valued</span></span>       | <span data-ttu-id="081aa-212">False</span><span class="sxs-lookup"><span data-stu-id="081aa-212">False</span></span>                                                      |
| <span data-ttu-id="081aa-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="081aa-213">Is Indexed</span></span>             | <span data-ttu-id="081aa-214">False</span><span class="sxs-lookup"><span data-stu-id="081aa-214">False</span></span>                                                      |
| <span data-ttu-id="081aa-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="081aa-215">In Global Catalog</span></span>      | <span data-ttu-id="081aa-216">False</span><span class="sxs-lookup"><span data-stu-id="081aa-216">False</span></span>                                                      |
| <span data-ttu-id="081aa-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="081aa-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="081aa-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="081aa-218">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="081aa-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="081aa-219">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="081aa-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="081aa-220">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="081aa-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="081aa-221">Search-Flags</span></span>           | <span data-ttu-id="081aa-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="081aa-222">0x00000000</span></span>                                                 |
| <span data-ttu-id="081aa-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="081aa-223">System-Flags</span></span>           | <span data-ttu-id="081aa-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="081aa-224">0x00000010</span></span>                                                 |
| <span data-ttu-id="081aa-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="081aa-225">Classes used in</span></span>        | [<span data-ttu-id="081aa-226">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="081aa-226">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="081aa-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="081aa-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="081aa-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="081aa-228">Entry</span></span> | <span data-ttu-id="081aa-229">Wert</span><span class="sxs-lookup"><span data-stu-id="081aa-229">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="081aa-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="081aa-230">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="081aa-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="081aa-231">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="081aa-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="081aa-232">System-Only</span></span>            | <span data-ttu-id="081aa-233">False</span><span class="sxs-lookup"><span data-stu-id="081aa-233">False</span></span>                                                      |
| <span data-ttu-id="081aa-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="081aa-234">Is-Single-Valued</span></span>       | <span data-ttu-id="081aa-235">False</span><span class="sxs-lookup"><span data-stu-id="081aa-235">False</span></span>                                                      |
| <span data-ttu-id="081aa-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="081aa-236">Is Indexed</span></span>             | <span data-ttu-id="081aa-237">False</span><span class="sxs-lookup"><span data-stu-id="081aa-237">False</span></span>                                                      |
| <span data-ttu-id="081aa-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="081aa-238">In Global Catalog</span></span>      | <span data-ttu-id="081aa-239">False</span><span class="sxs-lookup"><span data-stu-id="081aa-239">False</span></span>                                                      |
| <span data-ttu-id="081aa-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="081aa-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="081aa-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="081aa-241">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="081aa-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="081aa-242">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="081aa-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="081aa-243">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="081aa-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="081aa-244">Search-Flags</span></span>           | <span data-ttu-id="081aa-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="081aa-245">0x00000000</span></span>                                                 |
| <span data-ttu-id="081aa-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="081aa-246">System-Flags</span></span>           | <span data-ttu-id="081aa-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="081aa-247">0x00000010</span></span>                                                 |
| <span data-ttu-id="081aa-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="081aa-248">Classes used in</span></span>        | [<span data-ttu-id="081aa-249">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="081aa-249">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="081aa-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="081aa-250">Windows Server 2012</span></span>



| <span data-ttu-id="081aa-251">Eingabe</span><span class="sxs-lookup"><span data-stu-id="081aa-251">Entry</span></span> | <span data-ttu-id="081aa-252">Wert</span><span class="sxs-lookup"><span data-stu-id="081aa-252">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="081aa-253">Link-ID</span><span class="sxs-lookup"><span data-stu-id="081aa-253">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="081aa-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="081aa-254">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="081aa-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="081aa-255">System-Only</span></span>            | <span data-ttu-id="081aa-256">False</span><span class="sxs-lookup"><span data-stu-id="081aa-256">False</span></span>                                                      |
| <span data-ttu-id="081aa-257">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="081aa-257">Is-Single-Valued</span></span>       | <span data-ttu-id="081aa-258">False</span><span class="sxs-lookup"><span data-stu-id="081aa-258">False</span></span>                                                      |
| <span data-ttu-id="081aa-259">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="081aa-259">Is Indexed</span></span>             | <span data-ttu-id="081aa-260">False</span><span class="sxs-lookup"><span data-stu-id="081aa-260">False</span></span>                                                      |
| <span data-ttu-id="081aa-261">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="081aa-261">In Global Catalog</span></span>      | <span data-ttu-id="081aa-262">False</span><span class="sxs-lookup"><span data-stu-id="081aa-262">False</span></span>                                                      |
| <span data-ttu-id="081aa-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="081aa-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="081aa-264">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="081aa-264">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="081aa-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="081aa-265">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="081aa-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="081aa-266">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="081aa-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="081aa-267">Search-Flags</span></span>           | <span data-ttu-id="081aa-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="081aa-268">0x00000000</span></span>                                                 |
| <span data-ttu-id="081aa-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="081aa-269">System-Flags</span></span>           | <span data-ttu-id="081aa-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="081aa-270">0x00000010</span></span>                                                 |
| <span data-ttu-id="081aa-271">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="081aa-271">Classes used in</span></span>        | [<span data-ttu-id="081aa-272">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="081aa-272">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





