---
title: Address-Type-Attribut
description: Eine Zeichenfolge, die das Format der Benutzer Adresse beschreibt. Adresstypen sind Adressformaten zugeordnet. Das heißt, wenn Sie sich einen Adresstyp eines Empfängers ansehen, können Client Anwendungen bestimmen, wie eine für den Empfänger geeignete Adresse formatiert werden soll.
ms.assetid: ff39b1f5-1844-43e9-a4a5-2b5f7c396f34
ms.tgt_platform: multiple
keywords:
- AD-Schema für Address-Type-Attribut
- AD-Schema des Adresstype-Attributs
topic_type:
- apiref
api_name:
- Address-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ece3b396d619272c616ff1a959d01efb64ccd46
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344558"
---
# <a name="address-type-attribute"></a><span data-ttu-id="7ba71-107">Address-Type-Attribut</span><span class="sxs-lookup"><span data-stu-id="7ba71-107">Address-Type attribute</span></span>

<span data-ttu-id="7ba71-108">Eine Zeichenfolge, die das Format der Benutzer Adresse beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7ba71-108">A character string that describes the format of the user's address.</span></span> <span data-ttu-id="7ba71-109">Adresstypen sind Adressformaten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7ba71-109">Address types map to address formats.</span></span> <span data-ttu-id="7ba71-110">Das heißt, wenn Sie sich einen Adresstyp eines Empfängers ansehen, können Client Anwendungen bestimmen, wie eine für den Empfänger geeignete Adresse formatiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ba71-110">That is, by looking at a recipient's address type, client applications can determine how to format an address that is appropriate for the recipient.</span></span>



| <span data-ttu-id="7ba71-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7ba71-111">Entry</span></span> | <span data-ttu-id="7ba71-112">Wert</span><span class="sxs-lookup"><span data-stu-id="7ba71-112">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ba71-113">CN</span><span class="sxs-lookup"><span data-stu-id="7ba71-113">CN</span></span>                | <span data-ttu-id="7ba71-114">Address-Type</span><span class="sxs-lookup"><span data-stu-id="7ba71-114">Address-Type</span></span>                                                                                                              |
| <span data-ttu-id="7ba71-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7ba71-115">Ldap-Display-Name</span></span> | <span data-ttu-id="7ba71-116">AddressType</span><span class="sxs-lookup"><span data-stu-id="7ba71-116">addressType</span></span>                                                                                                               |
| <span data-ttu-id="7ba71-117">Size</span><span class="sxs-lookup"><span data-stu-id="7ba71-117">Size</span></span>              | <span data-ttu-id="7ba71-118">Adresstypen: 3Com, ATT, CCMAIL, compuservice, ex, Fax, MSFAX, MCI, MHS, MS, MSA, MSN, PROFS, SMTP, SNADS, Telex, X400, x500</span><span class="sxs-lookup"><span data-stu-id="7ba71-118">Address types: 3COM, ATT, CCMAIL, COMPUSERVE, EX, FAX, MSFAX, MCI, MHS, MS, MSA, MSN,PROFS,SMTP, SNADS, TELEX, X400, X500</span></span> |
| <span data-ttu-id="7ba71-119">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="7ba71-119">Update Privilege</span></span>  | <span data-ttu-id="7ba71-120">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7ba71-120">This value is set by the system.</span></span>                                                                                          |
| <span data-ttu-id="7ba71-121">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="7ba71-121">Update Frequency</span></span>  | <span data-ttu-id="7ba71-122">Wird festgelegt, wenn das Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7ba71-122">Set when the object is created.</span></span>                                                                                           |
| <span data-ttu-id="7ba71-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7ba71-123">Attribute-Id</span></span>      | <span data-ttu-id="7ba71-124">1.2.840.113556.1.2.350</span><span class="sxs-lookup"><span data-stu-id="7ba71-124">1.2.840.113556.1.2.350</span></span>                                                                                                    |
| <span data-ttu-id="7ba71-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7ba71-125">System-Id-Guid</span></span>    | <span data-ttu-id="7ba71-126">5F d42464-1262-11D0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="7ba71-126">5fd42464-1262-11d0-a060-00aa006c33ed</span></span>                                                                                      |
| <span data-ttu-id="7ba71-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ba71-127">Syntax</span></span>            | [<span data-ttu-id="7ba71-128">**String(Teletex)**</span><span class="sxs-lookup"><span data-stu-id="7ba71-128">**String(Teletex)**</span></span>](s-string-teletex.md)                                                                               |



## <a name="implementations"></a><span data-ttu-id="7ba71-129">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="7ba71-129">Implementations</span></span>

-   [<span data-ttu-id="7ba71-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7ba71-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7ba71-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7ba71-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7ba71-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7ba71-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7ba71-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7ba71-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7ba71-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7ba71-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7ba71-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7ba71-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7ba71-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7ba71-136">Windows 2000 Server</span></span>



| <span data-ttu-id="7ba71-137">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7ba71-137">Entry</span></span> | <span data-ttu-id="7ba71-138">Wert</span><span class="sxs-lookup"><span data-stu-id="7ba71-138">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="7ba71-139">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7ba71-139">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="7ba71-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ba71-140">MAPI-Id</span></span>                | <span data-ttu-id="7ba71-141">0x8048</span><span class="sxs-lookup"><span data-stu-id="7ba71-141">0x8048</span></span>                                                   |
| <span data-ttu-id="7ba71-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ba71-142">System-Only</span></span>            | <span data-ttu-id="7ba71-143">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-143">False</span></span>                                                    |
| <span data-ttu-id="7ba71-144">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7ba71-144">Is-Single-Valued</span></span>       | <span data-ttu-id="7ba71-145">Richtig</span><span class="sxs-lookup"><span data-stu-id="7ba71-145">True</span></span>                                                     |
| <span data-ttu-id="7ba71-146">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7ba71-146">Is Indexed</span></span>             | <span data-ttu-id="7ba71-147">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-147">False</span></span>                                                    |
| <span data-ttu-id="7ba71-148">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7ba71-148">In Global Catalog</span></span>      | <span data-ttu-id="7ba71-149">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-149">False</span></span>                                                    |
| <span data-ttu-id="7ba71-150">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7ba71-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ba71-151">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7ba71-151">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="7ba71-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ba71-152">Range-Lower</span></span>            | <span data-ttu-id="7ba71-153">1</span><span class="sxs-lookup"><span data-stu-id="7ba71-153">1</span></span>                                                        |
| <span data-ttu-id="7ba71-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ba71-154">Range-Upper</span></span>            | <span data-ttu-id="7ba71-155">32</span><span class="sxs-lookup"><span data-stu-id="7ba71-155">32</span></span>                                                       |
| <span data-ttu-id="7ba71-156">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ba71-156">Search-Flags</span></span>           | <span data-ttu-id="7ba71-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ba71-157">0x00000000</span></span>                                               |
| <span data-ttu-id="7ba71-158">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ba71-158">System-Flags</span></span>           | <span data-ttu-id="7ba71-159">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ba71-159">0x00000010</span></span>                                               |
| <span data-ttu-id="7ba71-160">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7ba71-160">Classes used in</span></span>        | [<span data-ttu-id="7ba71-161">**Address-Template**</span><span class="sxs-lookup"><span data-stu-id="7ba71-161">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7ba71-162">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7ba71-162">Windows Server 2003</span></span>



| <span data-ttu-id="7ba71-163">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7ba71-163">Entry</span></span> | <span data-ttu-id="7ba71-164">Wert</span><span class="sxs-lookup"><span data-stu-id="7ba71-164">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="7ba71-165">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7ba71-165">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="7ba71-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ba71-166">MAPI-Id</span></span>                | <span data-ttu-id="7ba71-167">0x8048</span><span class="sxs-lookup"><span data-stu-id="7ba71-167">0x8048</span></span>                                                   |
| <span data-ttu-id="7ba71-168">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ba71-168">System-Only</span></span>            | <span data-ttu-id="7ba71-169">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-169">False</span></span>                                                    |
| <span data-ttu-id="7ba71-170">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7ba71-170">Is-Single-Valued</span></span>       | <span data-ttu-id="7ba71-171">Richtig</span><span class="sxs-lookup"><span data-stu-id="7ba71-171">True</span></span>                                                     |
| <span data-ttu-id="7ba71-172">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7ba71-172">Is Indexed</span></span>             | <span data-ttu-id="7ba71-173">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-173">False</span></span>                                                    |
| <span data-ttu-id="7ba71-174">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7ba71-174">In Global Catalog</span></span>      | <span data-ttu-id="7ba71-175">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-175">False</span></span>                                                    |
| <span data-ttu-id="7ba71-176">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7ba71-176">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ba71-177">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7ba71-177">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="7ba71-178">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ba71-178">Range-Lower</span></span>            | <span data-ttu-id="7ba71-179">1</span><span class="sxs-lookup"><span data-stu-id="7ba71-179">1</span></span>                                                        |
| <span data-ttu-id="7ba71-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ba71-180">Range-Upper</span></span>            | <span data-ttu-id="7ba71-181">32</span><span class="sxs-lookup"><span data-stu-id="7ba71-181">32</span></span>                                                       |
| <span data-ttu-id="7ba71-182">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ba71-182">Search-Flags</span></span>           | <span data-ttu-id="7ba71-183">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ba71-183">0x00000000</span></span>                                               |
| <span data-ttu-id="7ba71-184">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ba71-184">System-Flags</span></span>           | <span data-ttu-id="7ba71-185">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ba71-185">0x00000010</span></span>                                               |
| <span data-ttu-id="7ba71-186">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7ba71-186">Classes used in</span></span>        | [<span data-ttu-id="7ba71-187">**Address-Template**</span><span class="sxs-lookup"><span data-stu-id="7ba71-187">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7ba71-188">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7ba71-188">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7ba71-189">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7ba71-189">Entry</span></span> | <span data-ttu-id="7ba71-190">Wert</span><span class="sxs-lookup"><span data-stu-id="7ba71-190">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="7ba71-191">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7ba71-191">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="7ba71-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ba71-192">MAPI-Id</span></span>                | <span data-ttu-id="7ba71-193">0x8048</span><span class="sxs-lookup"><span data-stu-id="7ba71-193">0x8048</span></span>                                                   |
| <span data-ttu-id="7ba71-194">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ba71-194">System-Only</span></span>            | <span data-ttu-id="7ba71-195">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-195">False</span></span>                                                    |
| <span data-ttu-id="7ba71-196">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7ba71-196">Is-Single-Valued</span></span>       | <span data-ttu-id="7ba71-197">Richtig</span><span class="sxs-lookup"><span data-stu-id="7ba71-197">True</span></span>                                                     |
| <span data-ttu-id="7ba71-198">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7ba71-198">Is Indexed</span></span>             | <span data-ttu-id="7ba71-199">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-199">False</span></span>                                                    |
| <span data-ttu-id="7ba71-200">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7ba71-200">In Global Catalog</span></span>      | <span data-ttu-id="7ba71-201">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-201">False</span></span>                                                    |
| <span data-ttu-id="7ba71-202">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7ba71-202">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ba71-203">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7ba71-203">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="7ba71-204">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ba71-204">Range-Lower</span></span>            | <span data-ttu-id="7ba71-205">1</span><span class="sxs-lookup"><span data-stu-id="7ba71-205">1</span></span>                                                        |
| <span data-ttu-id="7ba71-206">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ba71-206">Range-Upper</span></span>            | <span data-ttu-id="7ba71-207">32</span><span class="sxs-lookup"><span data-stu-id="7ba71-207">32</span></span>                                                       |
| <span data-ttu-id="7ba71-208">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ba71-208">Search-Flags</span></span>           | <span data-ttu-id="7ba71-209">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ba71-209">0x00000000</span></span>                                               |
| <span data-ttu-id="7ba71-210">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ba71-210">System-Flags</span></span>           | <span data-ttu-id="7ba71-211">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ba71-211">0x00000010</span></span>                                               |
| <span data-ttu-id="7ba71-212">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7ba71-212">Classes used in</span></span>        | [<span data-ttu-id="7ba71-213">**Address-Template**</span><span class="sxs-lookup"><span data-stu-id="7ba71-213">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7ba71-214">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ba71-214">Windows Server 2008</span></span>



| <span data-ttu-id="7ba71-215">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7ba71-215">Entry</span></span> | <span data-ttu-id="7ba71-216">Wert</span><span class="sxs-lookup"><span data-stu-id="7ba71-216">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="7ba71-217">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7ba71-217">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="7ba71-218">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ba71-218">MAPI-Id</span></span>                | <span data-ttu-id="7ba71-219">0x8048</span><span class="sxs-lookup"><span data-stu-id="7ba71-219">0x8048</span></span>                                                   |
| <span data-ttu-id="7ba71-220">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ba71-220">System-Only</span></span>            | <span data-ttu-id="7ba71-221">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-221">False</span></span>                                                    |
| <span data-ttu-id="7ba71-222">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7ba71-222">Is-Single-Valued</span></span>       | <span data-ttu-id="7ba71-223">Richtig</span><span class="sxs-lookup"><span data-stu-id="7ba71-223">True</span></span>                                                     |
| <span data-ttu-id="7ba71-224">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7ba71-224">Is Indexed</span></span>             | <span data-ttu-id="7ba71-225">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-225">False</span></span>                                                    |
| <span data-ttu-id="7ba71-226">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7ba71-226">In Global Catalog</span></span>      | <span data-ttu-id="7ba71-227">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-227">False</span></span>                                                    |
| <span data-ttu-id="7ba71-228">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7ba71-228">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ba71-229">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7ba71-229">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="7ba71-230">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ba71-230">Range-Lower</span></span>            | <span data-ttu-id="7ba71-231">1</span><span class="sxs-lookup"><span data-stu-id="7ba71-231">1</span></span>                                                        |
| <span data-ttu-id="7ba71-232">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ba71-232">Range-Upper</span></span>            | <span data-ttu-id="7ba71-233">32</span><span class="sxs-lookup"><span data-stu-id="7ba71-233">32</span></span>                                                       |
| <span data-ttu-id="7ba71-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ba71-234">Search-Flags</span></span>           | <span data-ttu-id="7ba71-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ba71-235">0x00000000</span></span>                                               |
| <span data-ttu-id="7ba71-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ba71-236">System-Flags</span></span>           | <span data-ttu-id="7ba71-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ba71-237">0x00000010</span></span>                                               |
| <span data-ttu-id="7ba71-238">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7ba71-238">Classes used in</span></span>        | [<span data-ttu-id="7ba71-239">**Address-Template**</span><span class="sxs-lookup"><span data-stu-id="7ba71-239">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7ba71-240">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7ba71-240">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7ba71-241">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7ba71-241">Entry</span></span> | <span data-ttu-id="7ba71-242">Wert</span><span class="sxs-lookup"><span data-stu-id="7ba71-242">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="7ba71-243">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7ba71-243">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="7ba71-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ba71-244">MAPI-Id</span></span>                | <span data-ttu-id="7ba71-245">0x8048</span><span class="sxs-lookup"><span data-stu-id="7ba71-245">0x8048</span></span>                                                   |
| <span data-ttu-id="7ba71-246">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ba71-246">System-Only</span></span>            | <span data-ttu-id="7ba71-247">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-247">False</span></span>                                                    |
| <span data-ttu-id="7ba71-248">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7ba71-248">Is-Single-Valued</span></span>       | <span data-ttu-id="7ba71-249">Richtig</span><span class="sxs-lookup"><span data-stu-id="7ba71-249">True</span></span>                                                     |
| <span data-ttu-id="7ba71-250">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7ba71-250">Is Indexed</span></span>             | <span data-ttu-id="7ba71-251">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-251">False</span></span>                                                    |
| <span data-ttu-id="7ba71-252">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7ba71-252">In Global Catalog</span></span>      | <span data-ttu-id="7ba71-253">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-253">False</span></span>                                                    |
| <span data-ttu-id="7ba71-254">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7ba71-254">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ba71-255">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7ba71-255">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="7ba71-256">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ba71-256">Range-Lower</span></span>            | <span data-ttu-id="7ba71-257">1</span><span class="sxs-lookup"><span data-stu-id="7ba71-257">1</span></span>                                                        |
| <span data-ttu-id="7ba71-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ba71-258">Range-Upper</span></span>            | <span data-ttu-id="7ba71-259">32</span><span class="sxs-lookup"><span data-stu-id="7ba71-259">32</span></span>                                                       |
| <span data-ttu-id="7ba71-260">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ba71-260">Search-Flags</span></span>           | <span data-ttu-id="7ba71-261">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ba71-261">0x00000000</span></span>                                               |
| <span data-ttu-id="7ba71-262">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ba71-262">System-Flags</span></span>           | <span data-ttu-id="7ba71-263">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ba71-263">0x00000010</span></span>                                               |
| <span data-ttu-id="7ba71-264">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7ba71-264">Classes used in</span></span>        | [<span data-ttu-id="7ba71-265">**Address-Template**</span><span class="sxs-lookup"><span data-stu-id="7ba71-265">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7ba71-266">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ba71-266">Windows Server 2012</span></span>



| <span data-ttu-id="7ba71-267">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7ba71-267">Entry</span></span> | <span data-ttu-id="7ba71-268">Wert</span><span class="sxs-lookup"><span data-stu-id="7ba71-268">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="7ba71-269">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7ba71-269">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="7ba71-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ba71-270">MAPI-Id</span></span>                | <span data-ttu-id="7ba71-271">0x8048</span><span class="sxs-lookup"><span data-stu-id="7ba71-271">0x8048</span></span>                                                   |
| <span data-ttu-id="7ba71-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ba71-272">System-Only</span></span>            | <span data-ttu-id="7ba71-273">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-273">False</span></span>                                                    |
| <span data-ttu-id="7ba71-274">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7ba71-274">Is-Single-Valued</span></span>       | <span data-ttu-id="7ba71-275">Richtig</span><span class="sxs-lookup"><span data-stu-id="7ba71-275">True</span></span>                                                     |
| <span data-ttu-id="7ba71-276">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7ba71-276">Is Indexed</span></span>             | <span data-ttu-id="7ba71-277">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-277">False</span></span>                                                    |
| <span data-ttu-id="7ba71-278">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7ba71-278">In Global Catalog</span></span>      | <span data-ttu-id="7ba71-279">False</span><span class="sxs-lookup"><span data-stu-id="7ba71-279">False</span></span>                                                    |
| <span data-ttu-id="7ba71-280">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7ba71-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ba71-281">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7ba71-281">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="7ba71-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ba71-282">Range-Lower</span></span>            | <span data-ttu-id="7ba71-283">1</span><span class="sxs-lookup"><span data-stu-id="7ba71-283">1</span></span>                                                        |
| <span data-ttu-id="7ba71-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ba71-284">Range-Upper</span></span>            | <span data-ttu-id="7ba71-285">32</span><span class="sxs-lookup"><span data-stu-id="7ba71-285">32</span></span>                                                       |
| <span data-ttu-id="7ba71-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ba71-286">Search-Flags</span></span>           | <span data-ttu-id="7ba71-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ba71-287">0x00000000</span></span>                                               |
| <span data-ttu-id="7ba71-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ba71-288">System-Flags</span></span>           | <span data-ttu-id="7ba71-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ba71-289">0x00000010</span></span>                                               |
| <span data-ttu-id="7ba71-290">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7ba71-290">Classes used in</span></span>        | [<span data-ttu-id="7ba71-291">**Address-Template**</span><span class="sxs-lookup"><span data-stu-id="7ba71-291">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



 

 





