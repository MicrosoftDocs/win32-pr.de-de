---
title: Extra-Columns-Attribut
description: Dabei handelt es sich um ein mehr wertiges Attribut, dessen Werte aus einem 5 Tupel (Attribut Name), (Spaltentitel), (Standard Sichtbarkeit (0,0)), (Spaltenbreite (\ 8211; 1 für automatische Breite)), 0 (für die zukünftige Verwendung reserviert sein muss), 0 (null) ist.
ms.assetid: aafe4657-0295-4af2-a7d0-8c7561516e17
ms.tgt_platform: multiple
keywords:
- AD-Schema für Extra-Columns-Attribut
- extraColumns-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Extra-Columns
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0bc74532296c5e0f23da9635bb26df299ae60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744377"
---
# <a name="extra-columns-attribute"></a><span data-ttu-id="73f36-105">Extra-Columns-Attribut</span><span class="sxs-lookup"><span data-stu-id="73f36-105">Extra-Columns attribute</span></span>

<span data-ttu-id="73f36-106">Dabei handelt es sich um ein mehr wertiges Attribut, dessen Werte aus einem fünf Tupel bestehen: (Attribut Name), (Spaltentitel), (Standard Sichtbarkeit (0,0)), (Spaltenbreite (1 für automatische Breite)), 0 (für die zukünftige Verwendung reserviert muss NULL sein).</span><span class="sxs-lookup"><span data-stu-id="73f36-106">This is a multivalued attribute whose values consist of a 5 tuple: (attribute name), (column title), (default visibility (0,1)), (column width ( 1 for auto width)), 0 (reserved for future use must be zero).</span></span> <span data-ttu-id="73f36-107">Dieser Wert wird von der Konsole AD-Benutzer und-Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="73f36-107">This value is used by the AD Users and Computers console.</span></span>



| <span data-ttu-id="73f36-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="73f36-108">Entry</span></span> | <span data-ttu-id="73f36-109">Wert</span><span class="sxs-lookup"><span data-stu-id="73f36-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73f36-110">CN</span><span class="sxs-lookup"><span data-stu-id="73f36-110">CN</span></span>                | <span data-ttu-id="73f36-111">Extra-Columns</span><span class="sxs-lookup"><span data-stu-id="73f36-111">Extra-Columns</span></span>                                                                                                                                                        |
| <span data-ttu-id="73f36-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="73f36-112">Ldap-Display-Name</span></span> | <span data-ttu-id="73f36-113">extraColumns</span><span class="sxs-lookup"><span data-stu-id="73f36-113">extraColumns</span></span>                                                                                                                                                         |
| <span data-ttu-id="73f36-114">Size</span><span class="sxs-lookup"><span data-stu-id="73f36-114">Size</span></span>              | <span data-ttu-id="73f36-115">Jeder Wert wäre die Größe der Zeichenfolge des 5 Tupels oben.</span><span class="sxs-lookup"><span data-stu-id="73f36-115">Each value would be the size of the string of the 5 tuple above.</span></span> <span data-ttu-id="73f36-116">Standardmäßig sind 22 Werte im Display specifier-Container für das default-Display-Objekt vorhanden.</span><span class="sxs-lookup"><span data-stu-id="73f36-116">By default there will be 22 values on the default-Display object in the DisplaySpecifier container.</span></span> |
| <span data-ttu-id="73f36-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="73f36-117">Update Privilege</span></span>  | <span data-ttu-id="73f36-118">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="73f36-118">Domain administrator</span></span>                                                                                                                                                 |
| <span data-ttu-id="73f36-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="73f36-119">Update Frequency</span></span>  | <span data-ttu-id="73f36-120">Dies wird nur aktualisiert, wenn ein Dienst wie Exchange installiert ist.</span><span class="sxs-lookup"><span data-stu-id="73f36-120">This will only be updated if a service like Exchange is installed.</span></span>                                                                                                   |
| <span data-ttu-id="73f36-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="73f36-121">Attribute-Id</span></span>      | <span data-ttu-id="73f36-122">1.2.840.113556.1.4.1687</span><span class="sxs-lookup"><span data-stu-id="73f36-122">1.2.840.113556.1.4.1687</span></span>                                                                                                                                              |
| <span data-ttu-id="73f36-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="73f36-123">System-Id-Guid</span></span>    | <span data-ttu-id="73f36-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span><span class="sxs-lookup"><span data-stu-id="73f36-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span></span>                                                                                                                                 |
| <span data-ttu-id="73f36-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="73f36-125">Syntax</span></span>            | [<span data-ttu-id="73f36-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="73f36-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a><span data-ttu-id="73f36-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="73f36-127">Implementations</span></span>

-   [<span data-ttu-id="73f36-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="73f36-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="73f36-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="73f36-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="73f36-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="73f36-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="73f36-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="73f36-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="73f36-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="73f36-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="73f36-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="73f36-133">Windows Server 2003</span></span>



| <span data-ttu-id="73f36-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="73f36-134">Entry</span></span> | <span data-ttu-id="73f36-135">Wert</span><span class="sxs-lookup"><span data-stu-id="73f36-135">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="73f36-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="73f36-136">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="73f36-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73f36-137">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="73f36-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="73f36-138">System-Only</span></span>            | <span data-ttu-id="73f36-139">False</span><span class="sxs-lookup"><span data-stu-id="73f36-139">False</span></span>                                                      |
| <span data-ttu-id="73f36-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="73f36-140">Is-Single-Valued</span></span>       | <span data-ttu-id="73f36-141">False</span><span class="sxs-lookup"><span data-stu-id="73f36-141">False</span></span>                                                      |
| <span data-ttu-id="73f36-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="73f36-142">Is Indexed</span></span>             | <span data-ttu-id="73f36-143">False</span><span class="sxs-lookup"><span data-stu-id="73f36-143">False</span></span>                                                      |
| <span data-ttu-id="73f36-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="73f36-144">In Global Catalog</span></span>      | <span data-ttu-id="73f36-145">False</span><span class="sxs-lookup"><span data-stu-id="73f36-145">False</span></span>                                                      |
| <span data-ttu-id="73f36-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="73f36-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="73f36-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="73f36-147">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="73f36-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73f36-148">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="73f36-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73f36-149">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="73f36-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73f36-150">Search-Flags</span></span>           | <span data-ttu-id="73f36-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73f36-151">0x00000000</span></span>                                                 |
| <span data-ttu-id="73f36-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73f36-152">System-Flags</span></span>           | <span data-ttu-id="73f36-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73f36-153">0x00000010</span></span>                                                 |
| <span data-ttu-id="73f36-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="73f36-154">Classes used in</span></span>        | [<span data-ttu-id="73f36-155">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="73f36-155">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="73f36-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="73f36-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="73f36-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="73f36-157">Entry</span></span> | <span data-ttu-id="73f36-158">Wert</span><span class="sxs-lookup"><span data-stu-id="73f36-158">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="73f36-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="73f36-159">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="73f36-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73f36-160">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="73f36-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="73f36-161">System-Only</span></span>            | <span data-ttu-id="73f36-162">False</span><span class="sxs-lookup"><span data-stu-id="73f36-162">False</span></span>                                                      |
| <span data-ttu-id="73f36-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="73f36-163">Is-Single-Valued</span></span>       | <span data-ttu-id="73f36-164">False</span><span class="sxs-lookup"><span data-stu-id="73f36-164">False</span></span>                                                      |
| <span data-ttu-id="73f36-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="73f36-165">Is Indexed</span></span>             | <span data-ttu-id="73f36-166">False</span><span class="sxs-lookup"><span data-stu-id="73f36-166">False</span></span>                                                      |
| <span data-ttu-id="73f36-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="73f36-167">In Global Catalog</span></span>      | <span data-ttu-id="73f36-168">False</span><span class="sxs-lookup"><span data-stu-id="73f36-168">False</span></span>                                                      |
| <span data-ttu-id="73f36-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="73f36-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="73f36-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="73f36-170">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="73f36-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73f36-171">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="73f36-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73f36-172">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="73f36-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73f36-173">Search-Flags</span></span>           | <span data-ttu-id="73f36-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73f36-174">0x00000000</span></span>                                                 |
| <span data-ttu-id="73f36-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73f36-175">System-Flags</span></span>           | <span data-ttu-id="73f36-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73f36-176">0x00000010</span></span>                                                 |
| <span data-ttu-id="73f36-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="73f36-177">Classes used in</span></span>        | [<span data-ttu-id="73f36-178">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="73f36-178">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="73f36-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73f36-179">Windows Server 2008</span></span>



| <span data-ttu-id="73f36-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="73f36-180">Entry</span></span> | <span data-ttu-id="73f36-181">Wert</span><span class="sxs-lookup"><span data-stu-id="73f36-181">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="73f36-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="73f36-182">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="73f36-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73f36-183">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="73f36-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="73f36-184">System-Only</span></span>            | <span data-ttu-id="73f36-185">False</span><span class="sxs-lookup"><span data-stu-id="73f36-185">False</span></span>                                                      |
| <span data-ttu-id="73f36-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="73f36-186">Is-Single-Valued</span></span>       | <span data-ttu-id="73f36-187">False</span><span class="sxs-lookup"><span data-stu-id="73f36-187">False</span></span>                                                      |
| <span data-ttu-id="73f36-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="73f36-188">Is Indexed</span></span>             | <span data-ttu-id="73f36-189">False</span><span class="sxs-lookup"><span data-stu-id="73f36-189">False</span></span>                                                      |
| <span data-ttu-id="73f36-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="73f36-190">In Global Catalog</span></span>      | <span data-ttu-id="73f36-191">False</span><span class="sxs-lookup"><span data-stu-id="73f36-191">False</span></span>                                                      |
| <span data-ttu-id="73f36-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="73f36-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="73f36-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="73f36-193">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="73f36-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73f36-194">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="73f36-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73f36-195">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="73f36-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73f36-196">Search-Flags</span></span>           | <span data-ttu-id="73f36-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73f36-197">0x00000000</span></span>                                                 |
| <span data-ttu-id="73f36-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73f36-198">System-Flags</span></span>           | <span data-ttu-id="73f36-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73f36-199">0x00000010</span></span>                                                 |
| <span data-ttu-id="73f36-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="73f36-200">Classes used in</span></span>        | [<span data-ttu-id="73f36-201">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="73f36-201">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="73f36-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="73f36-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="73f36-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="73f36-203">Entry</span></span> | <span data-ttu-id="73f36-204">Wert</span><span class="sxs-lookup"><span data-stu-id="73f36-204">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="73f36-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="73f36-205">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="73f36-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73f36-206">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="73f36-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="73f36-207">System-Only</span></span>            | <span data-ttu-id="73f36-208">False</span><span class="sxs-lookup"><span data-stu-id="73f36-208">False</span></span>                                                      |
| <span data-ttu-id="73f36-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="73f36-209">Is-Single-Valued</span></span>       | <span data-ttu-id="73f36-210">False</span><span class="sxs-lookup"><span data-stu-id="73f36-210">False</span></span>                                                      |
| <span data-ttu-id="73f36-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="73f36-211">Is Indexed</span></span>             | <span data-ttu-id="73f36-212">False</span><span class="sxs-lookup"><span data-stu-id="73f36-212">False</span></span>                                                      |
| <span data-ttu-id="73f36-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="73f36-213">In Global Catalog</span></span>      | <span data-ttu-id="73f36-214">False</span><span class="sxs-lookup"><span data-stu-id="73f36-214">False</span></span>                                                      |
| <span data-ttu-id="73f36-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="73f36-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="73f36-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="73f36-216">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="73f36-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73f36-217">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="73f36-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73f36-218">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="73f36-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73f36-219">Search-Flags</span></span>           | <span data-ttu-id="73f36-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73f36-220">0x00000000</span></span>                                                 |
| <span data-ttu-id="73f36-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73f36-221">System-Flags</span></span>           | <span data-ttu-id="73f36-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73f36-222">0x00000010</span></span>                                                 |
| <span data-ttu-id="73f36-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="73f36-223">Classes used in</span></span>        | [<span data-ttu-id="73f36-224">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="73f36-224">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="73f36-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="73f36-225">Windows Server 2012</span></span>



| <span data-ttu-id="73f36-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="73f36-226">Entry</span></span> | <span data-ttu-id="73f36-227">Wert</span><span class="sxs-lookup"><span data-stu-id="73f36-227">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="73f36-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="73f36-228">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="73f36-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73f36-229">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="73f36-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="73f36-230">System-Only</span></span>            | <span data-ttu-id="73f36-231">False</span><span class="sxs-lookup"><span data-stu-id="73f36-231">False</span></span>                                                      |
| <span data-ttu-id="73f36-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="73f36-232">Is-Single-Valued</span></span>       | <span data-ttu-id="73f36-233">False</span><span class="sxs-lookup"><span data-stu-id="73f36-233">False</span></span>                                                      |
| <span data-ttu-id="73f36-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="73f36-234">Is Indexed</span></span>             | <span data-ttu-id="73f36-235">False</span><span class="sxs-lookup"><span data-stu-id="73f36-235">False</span></span>                                                      |
| <span data-ttu-id="73f36-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="73f36-236">In Global Catalog</span></span>      | <span data-ttu-id="73f36-237">False</span><span class="sxs-lookup"><span data-stu-id="73f36-237">False</span></span>                                                      |
| <span data-ttu-id="73f36-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="73f36-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="73f36-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="73f36-239">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="73f36-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73f36-240">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="73f36-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73f36-241">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="73f36-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73f36-242">Search-Flags</span></span>           | <span data-ttu-id="73f36-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73f36-243">0x00000000</span></span>                                                 |
| <span data-ttu-id="73f36-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73f36-244">System-Flags</span></span>           | <span data-ttu-id="73f36-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73f36-245">0x00000010</span></span>                                                 |
| <span data-ttu-id="73f36-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="73f36-246">Classes used in</span></span>        | [<span data-ttu-id="73f36-247">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="73f36-247">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





