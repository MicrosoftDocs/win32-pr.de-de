---
title: Comment-Attribut
description: Die Kommentare des Benutzers. Diese Zeichenfolge kann eine NULL-Zeichenfolge sein.
ms.assetid: c57493b3-a42a-49ad-8f8c-0afadbb3ba09
ms.tgt_platform: multiple
keywords:
- Kommentar Attribut AD-Schema
- AD-Schema für Info-Attribut
topic_type:
- apiref
api_name:
- Comment
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd84674fce08f75c3162628b32f67a75fb8c026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744209"
---
# <a name="comment-attribute-ad-schema"></a><span data-ttu-id="813ef-106">Comment-Attribut (AD-Schema)</span><span class="sxs-lookup"><span data-stu-id="813ef-106">Comment attribute (AD Schema)</span></span>

<span data-ttu-id="813ef-107">Die Kommentare des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="813ef-107">The user's comments.</span></span> <span data-ttu-id="813ef-108">Diese Zeichenfolge kann eine NULL-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="813ef-108">This string can be a null string.</span></span>



| <span data-ttu-id="813ef-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="813ef-109">Entry</span></span> | <span data-ttu-id="813ef-110">Wert</span><span class="sxs-lookup"><span data-stu-id="813ef-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="813ef-111">CN</span><span class="sxs-lookup"><span data-stu-id="813ef-111">CN</span></span>                | <span data-ttu-id="813ef-112">Kommentar</span><span class="sxs-lookup"><span data-stu-id="813ef-112">Comment</span></span>                                                                  |
| <span data-ttu-id="813ef-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="813ef-113">Ldap-Display-Name</span></span> | <span data-ttu-id="813ef-114">info</span><span class="sxs-lookup"><span data-stu-id="813ef-114">info</span></span>                                                                     |
| <span data-ttu-id="813ef-115">Size</span><span class="sxs-lookup"><span data-stu-id="813ef-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="813ef-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="813ef-116">Update Privilege</span></span>  | <span data-ttu-id="813ef-117">Domänen Administrator oder Konto Besitzer.</span><span class="sxs-lookup"><span data-stu-id="813ef-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="813ef-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="813ef-118">Update Frequency</span></span>  | <span data-ttu-id="813ef-119">Immer dann, wenn der Benutzer oder Administrator Kommentare zum Konto hinzufügen muss.</span><span class="sxs-lookup"><span data-stu-id="813ef-119">Whenever the user or administrator needs to add comments on the account.</span></span> |
| <span data-ttu-id="813ef-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="813ef-120">Attribute-Id</span></span>      | <span data-ttu-id="813ef-121">1.2.840.113556.1.2.81</span><span class="sxs-lookup"><span data-stu-id="813ef-121">1.2.840.113556.1.2.81</span></span>                                                    |
| <span data-ttu-id="813ef-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="813ef-122">System-Id-Guid</span></span>    | <span data-ttu-id="813ef-123">bf96793e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="813ef-123">bf96793e-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="813ef-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="813ef-124">Syntax</span></span>            | [<span data-ttu-id="813ef-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="813ef-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="813ef-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="813ef-126">Implementations</span></span>

-   [<span data-ttu-id="813ef-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="813ef-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="813ef-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="813ef-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="813ef-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="813ef-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="813ef-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="813ef-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="813ef-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="813ef-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="813ef-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="813ef-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="813ef-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="813ef-133">Windows 2000 Server</span></span>



| <span data-ttu-id="813ef-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="813ef-134">Entry</span></span> | <span data-ttu-id="813ef-135">Wert</span><span class="sxs-lookup"><span data-stu-id="813ef-135">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="813ef-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="813ef-136">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="813ef-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="813ef-137">MAPI-Id</span></span>                | <span data-ttu-id="813ef-138">0x3004</span><span class="sxs-lookup"><span data-stu-id="813ef-138">0x3004</span></span>                                               |
| <span data-ttu-id="813ef-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="813ef-139">System-Only</span></span>            | <span data-ttu-id="813ef-140">False</span><span class="sxs-lookup"><span data-stu-id="813ef-140">False</span></span>                                                |
| <span data-ttu-id="813ef-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="813ef-141">Is-Single-Valued</span></span>       | <span data-ttu-id="813ef-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="813ef-142">True</span></span>                                                 |
| <span data-ttu-id="813ef-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="813ef-143">Is Indexed</span></span>             | <span data-ttu-id="813ef-144">False</span><span class="sxs-lookup"><span data-stu-id="813ef-144">False</span></span>                                                |
| <span data-ttu-id="813ef-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="813ef-145">In Global Catalog</span></span>      | <span data-ttu-id="813ef-146">False</span><span class="sxs-lookup"><span data-stu-id="813ef-146">False</span></span>                                                |
| <span data-ttu-id="813ef-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="813ef-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="813ef-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="813ef-148">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="813ef-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="813ef-149">Range-Lower</span></span>            | <span data-ttu-id="813ef-150">1</span><span class="sxs-lookup"><span data-stu-id="813ef-150">1</span></span>                                                    |
| <span data-ttu-id="813ef-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="813ef-151">Range-Upper</span></span>            | <span data-ttu-id="813ef-152">1024</span><span class="sxs-lookup"><span data-stu-id="813ef-152">1024</span></span>                                                 |
| <span data-ttu-id="813ef-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="813ef-153">Search-Flags</span></span>           | <span data-ttu-id="813ef-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="813ef-154">0x00000000</span></span>                                           |
| <span data-ttu-id="813ef-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="813ef-155">System-Flags</span></span>           | <span data-ttu-id="813ef-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="813ef-156">0x00000010</span></span>                                           |
| <span data-ttu-id="813ef-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="813ef-157">Classes used in</span></span>        | [<span data-ttu-id="813ef-158">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="813ef-158">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="813ef-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="813ef-159">Windows Server 2003</span></span>



| <span data-ttu-id="813ef-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="813ef-160">Entry</span></span> | <span data-ttu-id="813ef-161">Wert</span><span class="sxs-lookup"><span data-stu-id="813ef-161">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="813ef-162">Link-ID</span><span class="sxs-lookup"><span data-stu-id="813ef-162">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="813ef-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="813ef-163">MAPI-Id</span></span>                | <span data-ttu-id="813ef-164">0x3004</span><span class="sxs-lookup"><span data-stu-id="813ef-164">0x3004</span></span>                                               |
| <span data-ttu-id="813ef-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="813ef-165">System-Only</span></span>            | <span data-ttu-id="813ef-166">False</span><span class="sxs-lookup"><span data-stu-id="813ef-166">False</span></span>                                                |
| <span data-ttu-id="813ef-167">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="813ef-167">Is-Single-Valued</span></span>       | <span data-ttu-id="813ef-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="813ef-168">True</span></span>                                                 |
| <span data-ttu-id="813ef-169">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="813ef-169">Is Indexed</span></span>             | <span data-ttu-id="813ef-170">False</span><span class="sxs-lookup"><span data-stu-id="813ef-170">False</span></span>                                                |
| <span data-ttu-id="813ef-171">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="813ef-171">In Global Catalog</span></span>      | <span data-ttu-id="813ef-172">False</span><span class="sxs-lookup"><span data-stu-id="813ef-172">False</span></span>                                                |
| <span data-ttu-id="813ef-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="813ef-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="813ef-174">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="813ef-174">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="813ef-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="813ef-175">Range-Lower</span></span>            | <span data-ttu-id="813ef-176">1</span><span class="sxs-lookup"><span data-stu-id="813ef-176">1</span></span>                                                    |
| <span data-ttu-id="813ef-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="813ef-177">Range-Upper</span></span>            | <span data-ttu-id="813ef-178">1024</span><span class="sxs-lookup"><span data-stu-id="813ef-178">1024</span></span>                                                 |
| <span data-ttu-id="813ef-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="813ef-179">Search-Flags</span></span>           | <span data-ttu-id="813ef-180">0x00000000</span><span class="sxs-lookup"><span data-stu-id="813ef-180">0x00000000</span></span>                                           |
| <span data-ttu-id="813ef-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="813ef-181">System-Flags</span></span>           | <span data-ttu-id="813ef-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="813ef-182">0x00000010</span></span>                                           |
| <span data-ttu-id="813ef-183">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="813ef-183">Classes used in</span></span>        | [<span data-ttu-id="813ef-184">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="813ef-184">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="813ef-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="813ef-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="813ef-186">Eingabe</span><span class="sxs-lookup"><span data-stu-id="813ef-186">Entry</span></span> | <span data-ttu-id="813ef-187">Wert</span><span class="sxs-lookup"><span data-stu-id="813ef-187">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="813ef-188">Link-ID</span><span class="sxs-lookup"><span data-stu-id="813ef-188">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="813ef-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="813ef-189">MAPI-Id</span></span>                | <span data-ttu-id="813ef-190">0x3004</span><span class="sxs-lookup"><span data-stu-id="813ef-190">0x3004</span></span>                                               |
| <span data-ttu-id="813ef-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="813ef-191">System-Only</span></span>            | <span data-ttu-id="813ef-192">False</span><span class="sxs-lookup"><span data-stu-id="813ef-192">False</span></span>                                                |
| <span data-ttu-id="813ef-193">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="813ef-193">Is-Single-Valued</span></span>       | <span data-ttu-id="813ef-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="813ef-194">True</span></span>                                                 |
| <span data-ttu-id="813ef-195">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="813ef-195">Is Indexed</span></span>             | <span data-ttu-id="813ef-196">False</span><span class="sxs-lookup"><span data-stu-id="813ef-196">False</span></span>                                                |
| <span data-ttu-id="813ef-197">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="813ef-197">In Global Catalog</span></span>      | <span data-ttu-id="813ef-198">False</span><span class="sxs-lookup"><span data-stu-id="813ef-198">False</span></span>                                                |
| <span data-ttu-id="813ef-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="813ef-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="813ef-200">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="813ef-200">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="813ef-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="813ef-201">Range-Lower</span></span>            | <span data-ttu-id="813ef-202">1</span><span class="sxs-lookup"><span data-stu-id="813ef-202">1</span></span>                                                    |
| <span data-ttu-id="813ef-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="813ef-203">Range-Upper</span></span>            | <span data-ttu-id="813ef-204">1024</span><span class="sxs-lookup"><span data-stu-id="813ef-204">1024</span></span>                                                 |
| <span data-ttu-id="813ef-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="813ef-205">Search-Flags</span></span>           | <span data-ttu-id="813ef-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="813ef-206">0x00000000</span></span>                                           |
| <span data-ttu-id="813ef-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="813ef-207">System-Flags</span></span>           | <span data-ttu-id="813ef-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="813ef-208">0x00000010</span></span>                                           |
| <span data-ttu-id="813ef-209">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="813ef-209">Classes used in</span></span>        | [<span data-ttu-id="813ef-210">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="813ef-210">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="813ef-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="813ef-211">Windows Server 2008</span></span>



| <span data-ttu-id="813ef-212">Eingabe</span><span class="sxs-lookup"><span data-stu-id="813ef-212">Entry</span></span> | <span data-ttu-id="813ef-213">Wert</span><span class="sxs-lookup"><span data-stu-id="813ef-213">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="813ef-214">Link-ID</span><span class="sxs-lookup"><span data-stu-id="813ef-214">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="813ef-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="813ef-215">MAPI-Id</span></span>                | <span data-ttu-id="813ef-216">0x3004</span><span class="sxs-lookup"><span data-stu-id="813ef-216">0x3004</span></span>                                               |
| <span data-ttu-id="813ef-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="813ef-217">System-Only</span></span>            | <span data-ttu-id="813ef-218">False</span><span class="sxs-lookup"><span data-stu-id="813ef-218">False</span></span>                                                |
| <span data-ttu-id="813ef-219">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="813ef-219">Is-Single-Valued</span></span>       | <span data-ttu-id="813ef-220">Richtig</span><span class="sxs-lookup"><span data-stu-id="813ef-220">True</span></span>                                                 |
| <span data-ttu-id="813ef-221">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="813ef-221">Is Indexed</span></span>             | <span data-ttu-id="813ef-222">False</span><span class="sxs-lookup"><span data-stu-id="813ef-222">False</span></span>                                                |
| <span data-ttu-id="813ef-223">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="813ef-223">In Global Catalog</span></span>      | <span data-ttu-id="813ef-224">False</span><span class="sxs-lookup"><span data-stu-id="813ef-224">False</span></span>                                                |
| <span data-ttu-id="813ef-225">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="813ef-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="813ef-226">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="813ef-226">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="813ef-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="813ef-227">Range-Lower</span></span>            | <span data-ttu-id="813ef-228">1</span><span class="sxs-lookup"><span data-stu-id="813ef-228">1</span></span>                                                    |
| <span data-ttu-id="813ef-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="813ef-229">Range-Upper</span></span>            | <span data-ttu-id="813ef-230">1024</span><span class="sxs-lookup"><span data-stu-id="813ef-230">1024</span></span>                                                 |
| <span data-ttu-id="813ef-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="813ef-231">Search-Flags</span></span>           | <span data-ttu-id="813ef-232">0x00000000</span><span class="sxs-lookup"><span data-stu-id="813ef-232">0x00000000</span></span>                                           |
| <span data-ttu-id="813ef-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="813ef-233">System-Flags</span></span>           | <span data-ttu-id="813ef-234">0x00000010</span><span class="sxs-lookup"><span data-stu-id="813ef-234">0x00000010</span></span>                                           |
| <span data-ttu-id="813ef-235">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="813ef-235">Classes used in</span></span>        | [<span data-ttu-id="813ef-236">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="813ef-236">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="813ef-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="813ef-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="813ef-238">Eingabe</span><span class="sxs-lookup"><span data-stu-id="813ef-238">Entry</span></span> | <span data-ttu-id="813ef-239">Wert</span><span class="sxs-lookup"><span data-stu-id="813ef-239">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="813ef-240">Link-ID</span><span class="sxs-lookup"><span data-stu-id="813ef-240">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="813ef-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="813ef-241">MAPI-Id</span></span>                | <span data-ttu-id="813ef-242">0x3004</span><span class="sxs-lookup"><span data-stu-id="813ef-242">0x3004</span></span>                                               |
| <span data-ttu-id="813ef-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="813ef-243">System-Only</span></span>            | <span data-ttu-id="813ef-244">False</span><span class="sxs-lookup"><span data-stu-id="813ef-244">False</span></span>                                                |
| <span data-ttu-id="813ef-245">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="813ef-245">Is-Single-Valued</span></span>       | <span data-ttu-id="813ef-246">Richtig</span><span class="sxs-lookup"><span data-stu-id="813ef-246">True</span></span>                                                 |
| <span data-ttu-id="813ef-247">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="813ef-247">Is Indexed</span></span>             | <span data-ttu-id="813ef-248">False</span><span class="sxs-lookup"><span data-stu-id="813ef-248">False</span></span>                                                |
| <span data-ttu-id="813ef-249">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="813ef-249">In Global Catalog</span></span>      | <span data-ttu-id="813ef-250">False</span><span class="sxs-lookup"><span data-stu-id="813ef-250">False</span></span>                                                |
| <span data-ttu-id="813ef-251">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="813ef-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="813ef-252">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="813ef-252">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="813ef-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="813ef-253">Range-Lower</span></span>            | <span data-ttu-id="813ef-254">1</span><span class="sxs-lookup"><span data-stu-id="813ef-254">1</span></span>                                                    |
| <span data-ttu-id="813ef-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="813ef-255">Range-Upper</span></span>            | <span data-ttu-id="813ef-256">1024</span><span class="sxs-lookup"><span data-stu-id="813ef-256">1024</span></span>                                                 |
| <span data-ttu-id="813ef-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="813ef-257">Search-Flags</span></span>           | <span data-ttu-id="813ef-258">0x00000000</span><span class="sxs-lookup"><span data-stu-id="813ef-258">0x00000000</span></span>                                           |
| <span data-ttu-id="813ef-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="813ef-259">System-Flags</span></span>           | <span data-ttu-id="813ef-260">0x00000010</span><span class="sxs-lookup"><span data-stu-id="813ef-260">0x00000010</span></span>                                           |
| <span data-ttu-id="813ef-261">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="813ef-261">Classes used in</span></span>        | [<span data-ttu-id="813ef-262">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="813ef-262">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="813ef-263">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="813ef-263">Windows Server 2012</span></span>



| <span data-ttu-id="813ef-264">Eingabe</span><span class="sxs-lookup"><span data-stu-id="813ef-264">Entry</span></span> | <span data-ttu-id="813ef-265">Wert</span><span class="sxs-lookup"><span data-stu-id="813ef-265">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="813ef-266">Link-ID</span><span class="sxs-lookup"><span data-stu-id="813ef-266">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="813ef-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="813ef-267">MAPI-Id</span></span>                | <span data-ttu-id="813ef-268">0x3004</span><span class="sxs-lookup"><span data-stu-id="813ef-268">0x3004</span></span>                                               |
| <span data-ttu-id="813ef-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="813ef-269">System-Only</span></span>            | <span data-ttu-id="813ef-270">False</span><span class="sxs-lookup"><span data-stu-id="813ef-270">False</span></span>                                                |
| <span data-ttu-id="813ef-271">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="813ef-271">Is-Single-Valued</span></span>       | <span data-ttu-id="813ef-272">Richtig</span><span class="sxs-lookup"><span data-stu-id="813ef-272">True</span></span>                                                 |
| <span data-ttu-id="813ef-273">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="813ef-273">Is Indexed</span></span>             | <span data-ttu-id="813ef-274">False</span><span class="sxs-lookup"><span data-stu-id="813ef-274">False</span></span>                                                |
| <span data-ttu-id="813ef-275">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="813ef-275">In Global Catalog</span></span>      | <span data-ttu-id="813ef-276">False</span><span class="sxs-lookup"><span data-stu-id="813ef-276">False</span></span>                                                |
| <span data-ttu-id="813ef-277">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="813ef-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="813ef-278">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="813ef-278">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="813ef-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="813ef-279">Range-Lower</span></span>            | <span data-ttu-id="813ef-280">1</span><span class="sxs-lookup"><span data-stu-id="813ef-280">1</span></span>                                                    |
| <span data-ttu-id="813ef-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="813ef-281">Range-Upper</span></span>            | <span data-ttu-id="813ef-282">1024</span><span class="sxs-lookup"><span data-stu-id="813ef-282">1024</span></span>                                                 |
| <span data-ttu-id="813ef-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="813ef-283">Search-Flags</span></span>           | <span data-ttu-id="813ef-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="813ef-284">0x00000000</span></span>                                           |
| <span data-ttu-id="813ef-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="813ef-285">System-Flags</span></span>           | <span data-ttu-id="813ef-286">0x00000010</span><span class="sxs-lookup"><span data-stu-id="813ef-286">0x00000010</span></span>                                           |
| <span data-ttu-id="813ef-287">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="813ef-287">Classes used in</span></span>        | [<span data-ttu-id="813ef-288">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="813ef-288">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 





