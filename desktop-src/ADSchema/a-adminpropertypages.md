---
title: Admin-Property-Pages-Attribut
description: Die Bestellnummer und die GUID der Eigenschaften Seiten für ein Objekt, das auf Active Directory Verwaltungs Bildschirmen angezeigt werden soll. Weitere Informationen finden Sie im Dokument Erweitern der Benutzeroberfläche für Verzeichnisobjekte.
ms.assetid: 70455768-11e0-4d12-ad44-4b3115aa1594
ms.tgt_platform: multiple
keywords:
- Adschema des Admin-Eigenschaften-Pages-Attributs
- adminPropertyPages-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Admin-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d4e3814662cc8acf1a987cb92a1b9579cc43a4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344557"
---
# <a name="admin-property-pages-attribute"></a><span data-ttu-id="4d626-106">Admin-Property-Pages-Attribut</span><span class="sxs-lookup"><span data-stu-id="4d626-106">Admin-Property-Pages attribute</span></span>

<span data-ttu-id="4d626-107">Die Bestellnummer und die GUID der Eigenschaften Seiten für ein Objekt, das auf Active Directory Verwaltungs Bildschirmen angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d626-107">The order number and GUID of the property pages for an object to be displayed on Active Directory administration screens.</span></span> <span data-ttu-id="4d626-108">Weitere Informationen finden Sie im Dokument Erweitern der Benutzeroberfläche für Verzeichnisobjekte.</span><span class="sxs-lookup"><span data-stu-id="4d626-108">For more information see the document, Extending the User Interface for Directory Objects.</span></span>



| <span data-ttu-id="4d626-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4d626-109">Entry</span></span> | <span data-ttu-id="4d626-110">Wert</span><span class="sxs-lookup"><span data-stu-id="4d626-110">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="4d626-111">CN</span><span class="sxs-lookup"><span data-stu-id="4d626-111">CN</span></span>                | <span data-ttu-id="4d626-112">Admin-Eigenschaften Seiten</span><span class="sxs-lookup"><span data-stu-id="4d626-112">Admin-Property-Pages</span></span>                           |
| <span data-ttu-id="4d626-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4d626-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4d626-114">adminPropertyPages</span><span class="sxs-lookup"><span data-stu-id="4d626-114">adminPropertyPages</span></span>                             |
| <span data-ttu-id="4d626-115">Size</span><span class="sxs-lookup"><span data-stu-id="4d626-115">Size</span></span>              | \-                                             |
| <span data-ttu-id="4d626-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="4d626-116">Update Privilege</span></span>  | <span data-ttu-id="4d626-117">Domänen Administrator oder Anwendungsentwickler.</span><span class="sxs-lookup"><span data-stu-id="4d626-117">Domain administrator or application developer.</span></span> |
| <span data-ttu-id="4d626-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="4d626-118">Update Frequency</span></span>  | <span data-ttu-id="4d626-119">Immer dann, wenn eine Eigenschaften Seite hinzugefügt oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4d626-119">Whenever a property page is added or removed.</span></span>  |
| <span data-ttu-id="4d626-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4d626-120">Attribute-Id</span></span>      | <span data-ttu-id="4d626-121">1.2.840.113556.1.4.562</span><span class="sxs-lookup"><span data-stu-id="4d626-121">1.2.840.113556.1.4.562</span></span>                         |
| <span data-ttu-id="4d626-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4d626-122">System-Id-Guid</span></span>    | <span data-ttu-id="4d626-123">52458038-ca6a-11D0-affinf-0000f 80367c1</span><span class="sxs-lookup"><span data-stu-id="4d626-123">52458038-ca6a-11d0-afff-0000f80367c1</span></span>           |
| <span data-ttu-id="4d626-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d626-124">Syntax</span></span>            | [<span data-ttu-id="4d626-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4d626-125">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="4d626-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="4d626-126">Implementations</span></span>

-   [<span data-ttu-id="4d626-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4d626-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4d626-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4d626-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4d626-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4d626-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4d626-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4d626-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4d626-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4d626-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4d626-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4d626-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4d626-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4d626-133">Windows 2000 Server</span></span>



| <span data-ttu-id="4d626-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4d626-134">Entry</span></span> | <span data-ttu-id="4d626-135">Wert</span><span class="sxs-lookup"><span data-stu-id="4d626-135">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="4d626-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4d626-136">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4d626-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d626-137">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4d626-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d626-138">System-Only</span></span>            | <span data-ttu-id="4d626-139">False</span><span class="sxs-lookup"><span data-stu-id="4d626-139">False</span></span>                                                      |
| <span data-ttu-id="4d626-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4d626-140">Is-Single-Valued</span></span>       | <span data-ttu-id="4d626-141">False</span><span class="sxs-lookup"><span data-stu-id="4d626-141">False</span></span>                                                      |
| <span data-ttu-id="4d626-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4d626-142">Is Indexed</span></span>             | <span data-ttu-id="4d626-143">False</span><span class="sxs-lookup"><span data-stu-id="4d626-143">False</span></span>                                                      |
| <span data-ttu-id="4d626-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4d626-144">In Global Catalog</span></span>      | <span data-ttu-id="4d626-145">False</span><span class="sxs-lookup"><span data-stu-id="4d626-145">False</span></span>                                                      |
| <span data-ttu-id="4d626-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4d626-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d626-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4d626-147">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="4d626-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d626-148">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="4d626-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d626-149">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="4d626-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d626-150">Search-Flags</span></span>           | <span data-ttu-id="4d626-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d626-151">0x00000000</span></span>                                                 |
| <span data-ttu-id="4d626-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d626-152">System-Flags</span></span>           | <span data-ttu-id="4d626-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d626-153">0x00000010</span></span>                                                 |
| <span data-ttu-id="4d626-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4d626-154">Classes used in</span></span>        | [<span data-ttu-id="4d626-155">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="4d626-155">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4d626-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4d626-156">Windows Server 2003</span></span>



| <span data-ttu-id="4d626-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4d626-157">Entry</span></span> | <span data-ttu-id="4d626-158">Wert</span><span class="sxs-lookup"><span data-stu-id="4d626-158">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="4d626-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4d626-159">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4d626-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d626-160">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4d626-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d626-161">System-Only</span></span>            | <span data-ttu-id="4d626-162">False</span><span class="sxs-lookup"><span data-stu-id="4d626-162">False</span></span>                                                      |
| <span data-ttu-id="4d626-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4d626-163">Is-Single-Valued</span></span>       | <span data-ttu-id="4d626-164">False</span><span class="sxs-lookup"><span data-stu-id="4d626-164">False</span></span>                                                      |
| <span data-ttu-id="4d626-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4d626-165">Is Indexed</span></span>             | <span data-ttu-id="4d626-166">False</span><span class="sxs-lookup"><span data-stu-id="4d626-166">False</span></span>                                                      |
| <span data-ttu-id="4d626-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4d626-167">In Global Catalog</span></span>      | <span data-ttu-id="4d626-168">False</span><span class="sxs-lookup"><span data-stu-id="4d626-168">False</span></span>                                                      |
| <span data-ttu-id="4d626-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4d626-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d626-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4d626-170">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="4d626-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d626-171">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="4d626-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d626-172">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="4d626-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d626-173">Search-Flags</span></span>           | <span data-ttu-id="4d626-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d626-174">0x00000000</span></span>                                                 |
| <span data-ttu-id="4d626-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d626-175">System-Flags</span></span>           | <span data-ttu-id="4d626-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d626-176">0x00000010</span></span>                                                 |
| <span data-ttu-id="4d626-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4d626-177">Classes used in</span></span>        | [<span data-ttu-id="4d626-178">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="4d626-178">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4d626-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4d626-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4d626-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4d626-180">Entry</span></span> | <span data-ttu-id="4d626-181">Wert</span><span class="sxs-lookup"><span data-stu-id="4d626-181">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="4d626-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4d626-182">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4d626-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d626-183">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4d626-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d626-184">System-Only</span></span>            | <span data-ttu-id="4d626-185">False</span><span class="sxs-lookup"><span data-stu-id="4d626-185">False</span></span>                                                      |
| <span data-ttu-id="4d626-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4d626-186">Is-Single-Valued</span></span>       | <span data-ttu-id="4d626-187">False</span><span class="sxs-lookup"><span data-stu-id="4d626-187">False</span></span>                                                      |
| <span data-ttu-id="4d626-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4d626-188">Is Indexed</span></span>             | <span data-ttu-id="4d626-189">False</span><span class="sxs-lookup"><span data-stu-id="4d626-189">False</span></span>                                                      |
| <span data-ttu-id="4d626-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4d626-190">In Global Catalog</span></span>      | <span data-ttu-id="4d626-191">False</span><span class="sxs-lookup"><span data-stu-id="4d626-191">False</span></span>                                                      |
| <span data-ttu-id="4d626-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4d626-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d626-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4d626-193">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="4d626-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d626-194">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="4d626-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d626-195">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="4d626-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d626-196">Search-Flags</span></span>           | <span data-ttu-id="4d626-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d626-197">0x00000000</span></span>                                                 |
| <span data-ttu-id="4d626-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d626-198">System-Flags</span></span>           | <span data-ttu-id="4d626-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d626-199">0x00000010</span></span>                                                 |
| <span data-ttu-id="4d626-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4d626-200">Classes used in</span></span>        | [<span data-ttu-id="4d626-201">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="4d626-201">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4d626-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d626-202">Windows Server 2008</span></span>



| <span data-ttu-id="4d626-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4d626-203">Entry</span></span> | <span data-ttu-id="4d626-204">Wert</span><span class="sxs-lookup"><span data-stu-id="4d626-204">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="4d626-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4d626-205">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4d626-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d626-206">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4d626-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d626-207">System-Only</span></span>            | <span data-ttu-id="4d626-208">False</span><span class="sxs-lookup"><span data-stu-id="4d626-208">False</span></span>                                                      |
| <span data-ttu-id="4d626-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4d626-209">Is-Single-Valued</span></span>       | <span data-ttu-id="4d626-210">False</span><span class="sxs-lookup"><span data-stu-id="4d626-210">False</span></span>                                                      |
| <span data-ttu-id="4d626-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4d626-211">Is Indexed</span></span>             | <span data-ttu-id="4d626-212">False</span><span class="sxs-lookup"><span data-stu-id="4d626-212">False</span></span>                                                      |
| <span data-ttu-id="4d626-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4d626-213">In Global Catalog</span></span>      | <span data-ttu-id="4d626-214">False</span><span class="sxs-lookup"><span data-stu-id="4d626-214">False</span></span>                                                      |
| <span data-ttu-id="4d626-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4d626-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d626-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4d626-216">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="4d626-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d626-217">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="4d626-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d626-218">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="4d626-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d626-219">Search-Flags</span></span>           | <span data-ttu-id="4d626-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d626-220">0x00000000</span></span>                                                 |
| <span data-ttu-id="4d626-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d626-221">System-Flags</span></span>           | <span data-ttu-id="4d626-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d626-222">0x00000010</span></span>                                                 |
| <span data-ttu-id="4d626-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4d626-223">Classes used in</span></span>        | [<span data-ttu-id="4d626-224">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="4d626-224">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4d626-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4d626-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4d626-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4d626-226">Entry</span></span> | <span data-ttu-id="4d626-227">Wert</span><span class="sxs-lookup"><span data-stu-id="4d626-227">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="4d626-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4d626-228">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4d626-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d626-229">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4d626-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d626-230">System-Only</span></span>            | <span data-ttu-id="4d626-231">False</span><span class="sxs-lookup"><span data-stu-id="4d626-231">False</span></span>                                                      |
| <span data-ttu-id="4d626-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4d626-232">Is-Single-Valued</span></span>       | <span data-ttu-id="4d626-233">False</span><span class="sxs-lookup"><span data-stu-id="4d626-233">False</span></span>                                                      |
| <span data-ttu-id="4d626-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4d626-234">Is Indexed</span></span>             | <span data-ttu-id="4d626-235">False</span><span class="sxs-lookup"><span data-stu-id="4d626-235">False</span></span>                                                      |
| <span data-ttu-id="4d626-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4d626-236">In Global Catalog</span></span>      | <span data-ttu-id="4d626-237">False</span><span class="sxs-lookup"><span data-stu-id="4d626-237">False</span></span>                                                      |
| <span data-ttu-id="4d626-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4d626-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d626-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4d626-239">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="4d626-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d626-240">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="4d626-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d626-241">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="4d626-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d626-242">Search-Flags</span></span>           | <span data-ttu-id="4d626-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d626-243">0x00000000</span></span>                                                 |
| <span data-ttu-id="4d626-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d626-244">System-Flags</span></span>           | <span data-ttu-id="4d626-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d626-245">0x00000010</span></span>                                                 |
| <span data-ttu-id="4d626-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4d626-246">Classes used in</span></span>        | [<span data-ttu-id="4d626-247">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="4d626-247">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4d626-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4d626-248">Windows Server 2012</span></span>



| <span data-ttu-id="4d626-249">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4d626-249">Entry</span></span> | <span data-ttu-id="4d626-250">Wert</span><span class="sxs-lookup"><span data-stu-id="4d626-250">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="4d626-251">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4d626-251">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4d626-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d626-252">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4d626-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d626-253">System-Only</span></span>            | <span data-ttu-id="4d626-254">False</span><span class="sxs-lookup"><span data-stu-id="4d626-254">False</span></span>                                                      |
| <span data-ttu-id="4d626-255">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4d626-255">Is-Single-Valued</span></span>       | <span data-ttu-id="4d626-256">False</span><span class="sxs-lookup"><span data-stu-id="4d626-256">False</span></span>                                                      |
| <span data-ttu-id="4d626-257">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4d626-257">Is Indexed</span></span>             | <span data-ttu-id="4d626-258">False</span><span class="sxs-lookup"><span data-stu-id="4d626-258">False</span></span>                                                      |
| <span data-ttu-id="4d626-259">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4d626-259">In Global Catalog</span></span>      | <span data-ttu-id="4d626-260">False</span><span class="sxs-lookup"><span data-stu-id="4d626-260">False</span></span>                                                      |
| <span data-ttu-id="4d626-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4d626-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d626-262">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4d626-262">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="4d626-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d626-263">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="4d626-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d626-264">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="4d626-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d626-265">Search-Flags</span></span>           | <span data-ttu-id="4d626-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d626-266">0x00000000</span></span>                                                 |
| <span data-ttu-id="4d626-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d626-267">System-Flags</span></span>           | <span data-ttu-id="4d626-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d626-268">0x00000010</span></span>                                                 |
| <span data-ttu-id="4d626-269">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4d626-269">Classes used in</span></span>        | [<span data-ttu-id="4d626-270">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="4d626-270">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





