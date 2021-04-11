---
title: MSMQ-Recipient-Formatname-Attribut
description: Wird als Empfänger Format Name in der MSMQ-Custom-Recipient-Klasse verwendet.
ms.assetid: 26ee4cec-4e69-412e-914b-437f2f4cd88e
ms.tgt_platform: multiple
keywords:
- MSMQ-Recipient-Formatname-Attribut AD-Schema
- MSMQ-Recipient-Formatname-Attribut AD-Schema
topic_type:
- apiref
api_name:
- MSMQ-Recipient-FormatName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57fbeee49ddf0c734212bc91926e5c848a9e8d1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122899"
---
# <a name="msmq-recipient-formatname-attribute"></a><span data-ttu-id="edab9-105">MSMQ-Recipient-Formatname-Attribut</span><span class="sxs-lookup"><span data-stu-id="edab9-105">MSMQ-Recipient-FormatName attribute</span></span>

<span data-ttu-id="edab9-106">Wird als Empfänger Format Name in der MSMQ-Custom-Recipient-Klasse verwendet.</span><span class="sxs-lookup"><span data-stu-id="edab9-106">Used as the recipient format name in the MSMQ-Custom-Recipient class.</span></span>



| <span data-ttu-id="edab9-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="edab9-107">Entry</span></span> | <span data-ttu-id="edab9-108">Wert</span><span class="sxs-lookup"><span data-stu-id="edab9-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="edab9-109">CN</span><span class="sxs-lookup"><span data-stu-id="edab9-109">CN</span></span>                | <span data-ttu-id="edab9-110">MSMQ-Recipient-Format Name</span><span class="sxs-lookup"><span data-stu-id="edab9-110">MSMQ-Recipient-FormatName</span></span>                   |
| <span data-ttu-id="edab9-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="edab9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="edab9-112">MSMQ-Recipient-Format Name</span><span class="sxs-lookup"><span data-stu-id="edab9-112">msMQ-Recipient-FormatName</span></span>                   |
| <span data-ttu-id="edab9-113">Size</span><span class="sxs-lookup"><span data-stu-id="edab9-113">Size</span></span>              | <span data-ttu-id="edab9-114">1 bis 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="edab9-114">1 to 255 characters.</span></span>                        |
| <span data-ttu-id="edab9-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="edab9-115">Update Privilege</span></span>  | <span data-ttu-id="edab9-116">Der Besitzer der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="edab9-116">The queue owner.</span></span>                            |
| <span data-ttu-id="edab9-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="edab9-117">Update Frequency</span></span>  | <span data-ttu-id="edab9-118">Erst nachdem die externe Warteschlange verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="edab9-118">Only after the external queue was moved.</span></span>    |
| <span data-ttu-id="edab9-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="edab9-119">Attribute-Id</span></span>      | <span data-ttu-id="edab9-120">1.2.840.113556.1.4.1695</span><span class="sxs-lookup"><span data-stu-id="edab9-120">1.2.840.113556.1.4.1695</span></span>                     |
| <span data-ttu-id="edab9-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="edab9-121">System-Id-Guid</span></span>    | <span data-ttu-id="edab9-122">3bfe6748-b544-485A-B067-1b310c4334bf</span><span class="sxs-lookup"><span data-stu-id="edab9-122">3bfe6748-b544-485a-b067-1b310c4334bf</span></span>        |
| <span data-ttu-id="edab9-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="edab9-123">Syntax</span></span>            | [<span data-ttu-id="edab9-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="edab9-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="edab9-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="edab9-125">Implementations</span></span>

-   [<span data-ttu-id="edab9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="edab9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="edab9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="edab9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="edab9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="edab9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="edab9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="edab9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="edab9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="edab9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="edab9-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="edab9-131">Windows Server 2003</span></span>



| <span data-ttu-id="edab9-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="edab9-132">Entry</span></span> | <span data-ttu-id="edab9-133">Wert</span><span class="sxs-lookup"><span data-stu-id="edab9-133">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="edab9-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="edab9-134">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="edab9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edab9-135">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="edab9-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="edab9-136">System-Only</span></span>            | <span data-ttu-id="edab9-137">False</span><span class="sxs-lookup"><span data-stu-id="edab9-137">False</span></span>                                                               |
| <span data-ttu-id="edab9-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="edab9-138">Is-Single-Valued</span></span>       | <span data-ttu-id="edab9-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="edab9-139">True</span></span>                                                                |
| <span data-ttu-id="edab9-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="edab9-140">Is Indexed</span></span>             | <span data-ttu-id="edab9-141">False</span><span class="sxs-lookup"><span data-stu-id="edab9-141">False</span></span>                                                               |
| <span data-ttu-id="edab9-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="edab9-142">In Global Catalog</span></span>      | <span data-ttu-id="edab9-143">False</span><span class="sxs-lookup"><span data-stu-id="edab9-143">False</span></span>                                                               |
| <span data-ttu-id="edab9-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="edab9-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="edab9-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="edab9-145">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="edab9-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edab9-146">Range-Lower</span></span>            | <span data-ttu-id="edab9-147">1</span><span class="sxs-lookup"><span data-stu-id="edab9-147">1</span></span>                                                                   |
| <span data-ttu-id="edab9-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edab9-148">Range-Upper</span></span>            | <span data-ttu-id="edab9-149">255</span><span class="sxs-lookup"><span data-stu-id="edab9-149">255</span></span>                                                                 |
| <span data-ttu-id="edab9-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edab9-150">Search-Flags</span></span>           | <span data-ttu-id="edab9-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edab9-151">0x00000000</span></span>                                                          |
| <span data-ttu-id="edab9-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edab9-152">System-Flags</span></span>           | <span data-ttu-id="edab9-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edab9-153">0x00000010</span></span>                                                          |
| <span data-ttu-id="edab9-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="edab9-154">Classes used in</span></span>        | [<span data-ttu-id="edab9-155">**MSMQ-Custom-Recipient**</span><span class="sxs-lookup"><span data-stu-id="edab9-155">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="edab9-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="edab9-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="edab9-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="edab9-157">Entry</span></span> | <span data-ttu-id="edab9-158">Wert</span><span class="sxs-lookup"><span data-stu-id="edab9-158">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="edab9-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="edab9-159">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="edab9-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edab9-160">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="edab9-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="edab9-161">System-Only</span></span>            | <span data-ttu-id="edab9-162">False</span><span class="sxs-lookup"><span data-stu-id="edab9-162">False</span></span>                                                               |
| <span data-ttu-id="edab9-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="edab9-163">Is-Single-Valued</span></span>       | <span data-ttu-id="edab9-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="edab9-164">True</span></span>                                                                |
| <span data-ttu-id="edab9-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="edab9-165">Is Indexed</span></span>             | <span data-ttu-id="edab9-166">False</span><span class="sxs-lookup"><span data-stu-id="edab9-166">False</span></span>                                                               |
| <span data-ttu-id="edab9-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="edab9-167">In Global Catalog</span></span>      | <span data-ttu-id="edab9-168">False</span><span class="sxs-lookup"><span data-stu-id="edab9-168">False</span></span>                                                               |
| <span data-ttu-id="edab9-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="edab9-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="edab9-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="edab9-170">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="edab9-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edab9-171">Range-Lower</span></span>            | <span data-ttu-id="edab9-172">1</span><span class="sxs-lookup"><span data-stu-id="edab9-172">1</span></span>                                                                   |
| <span data-ttu-id="edab9-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edab9-173">Range-Upper</span></span>            | <span data-ttu-id="edab9-174">255</span><span class="sxs-lookup"><span data-stu-id="edab9-174">255</span></span>                                                                 |
| <span data-ttu-id="edab9-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edab9-175">Search-Flags</span></span>           | <span data-ttu-id="edab9-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edab9-176">0x00000000</span></span>                                                          |
| <span data-ttu-id="edab9-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edab9-177">System-Flags</span></span>           | <span data-ttu-id="edab9-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edab9-178">0x00000010</span></span>                                                          |
| <span data-ttu-id="edab9-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="edab9-179">Classes used in</span></span>        | [<span data-ttu-id="edab9-180">**MSMQ-Custom-Recipient**</span><span class="sxs-lookup"><span data-stu-id="edab9-180">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="edab9-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="edab9-181">Windows Server 2008</span></span>



| <span data-ttu-id="edab9-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="edab9-182">Entry</span></span> | <span data-ttu-id="edab9-183">Wert</span><span class="sxs-lookup"><span data-stu-id="edab9-183">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="edab9-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="edab9-184">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="edab9-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edab9-185">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="edab9-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="edab9-186">System-Only</span></span>            | <span data-ttu-id="edab9-187">False</span><span class="sxs-lookup"><span data-stu-id="edab9-187">False</span></span>                                                               |
| <span data-ttu-id="edab9-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="edab9-188">Is-Single-Valued</span></span>       | <span data-ttu-id="edab9-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="edab9-189">True</span></span>                                                                |
| <span data-ttu-id="edab9-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="edab9-190">Is Indexed</span></span>             | <span data-ttu-id="edab9-191">False</span><span class="sxs-lookup"><span data-stu-id="edab9-191">False</span></span>                                                               |
| <span data-ttu-id="edab9-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="edab9-192">In Global Catalog</span></span>      | <span data-ttu-id="edab9-193">False</span><span class="sxs-lookup"><span data-stu-id="edab9-193">False</span></span>                                                               |
| <span data-ttu-id="edab9-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="edab9-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="edab9-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="edab9-195">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="edab9-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edab9-196">Range-Lower</span></span>            | <span data-ttu-id="edab9-197">1</span><span class="sxs-lookup"><span data-stu-id="edab9-197">1</span></span>                                                                   |
| <span data-ttu-id="edab9-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edab9-198">Range-Upper</span></span>            | <span data-ttu-id="edab9-199">255</span><span class="sxs-lookup"><span data-stu-id="edab9-199">255</span></span>                                                                 |
| <span data-ttu-id="edab9-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edab9-200">Search-Flags</span></span>           | <span data-ttu-id="edab9-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edab9-201">0x00000000</span></span>                                                          |
| <span data-ttu-id="edab9-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edab9-202">System-Flags</span></span>           | <span data-ttu-id="edab9-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edab9-203">0x00000010</span></span>                                                          |
| <span data-ttu-id="edab9-204">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="edab9-204">Classes used in</span></span>        | [<span data-ttu-id="edab9-205">**MSMQ-Custom-Recipient**</span><span class="sxs-lookup"><span data-stu-id="edab9-205">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="edab9-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="edab9-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="edab9-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="edab9-207">Entry</span></span> | <span data-ttu-id="edab9-208">Wert</span><span class="sxs-lookup"><span data-stu-id="edab9-208">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="edab9-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="edab9-209">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="edab9-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edab9-210">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="edab9-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="edab9-211">System-Only</span></span>            | <span data-ttu-id="edab9-212">False</span><span class="sxs-lookup"><span data-stu-id="edab9-212">False</span></span>                                                               |
| <span data-ttu-id="edab9-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="edab9-213">Is-Single-Valued</span></span>       | <span data-ttu-id="edab9-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="edab9-214">True</span></span>                                                                |
| <span data-ttu-id="edab9-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="edab9-215">Is Indexed</span></span>             | <span data-ttu-id="edab9-216">False</span><span class="sxs-lookup"><span data-stu-id="edab9-216">False</span></span>                                                               |
| <span data-ttu-id="edab9-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="edab9-217">In Global Catalog</span></span>      | <span data-ttu-id="edab9-218">False</span><span class="sxs-lookup"><span data-stu-id="edab9-218">False</span></span>                                                               |
| <span data-ttu-id="edab9-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="edab9-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="edab9-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="edab9-220">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="edab9-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edab9-221">Range-Lower</span></span>            | <span data-ttu-id="edab9-222">1</span><span class="sxs-lookup"><span data-stu-id="edab9-222">1</span></span>                                                                   |
| <span data-ttu-id="edab9-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edab9-223">Range-Upper</span></span>            | <span data-ttu-id="edab9-224">255</span><span class="sxs-lookup"><span data-stu-id="edab9-224">255</span></span>                                                                 |
| <span data-ttu-id="edab9-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edab9-225">Search-Flags</span></span>           | <span data-ttu-id="edab9-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edab9-226">0x00000000</span></span>                                                          |
| <span data-ttu-id="edab9-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edab9-227">System-Flags</span></span>           | <span data-ttu-id="edab9-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edab9-228">0x00000010</span></span>                                                          |
| <span data-ttu-id="edab9-229">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="edab9-229">Classes used in</span></span>        | [<span data-ttu-id="edab9-230">**MSMQ-Custom-Recipient**</span><span class="sxs-lookup"><span data-stu-id="edab9-230">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="edab9-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="edab9-231">Windows Server 2012</span></span>



| <span data-ttu-id="edab9-232">Eingabe</span><span class="sxs-lookup"><span data-stu-id="edab9-232">Entry</span></span> | <span data-ttu-id="edab9-233">Wert</span><span class="sxs-lookup"><span data-stu-id="edab9-233">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="edab9-234">Link-ID</span><span class="sxs-lookup"><span data-stu-id="edab9-234">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="edab9-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edab9-235">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="edab9-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="edab9-236">System-Only</span></span>            | <span data-ttu-id="edab9-237">False</span><span class="sxs-lookup"><span data-stu-id="edab9-237">False</span></span>                                                               |
| <span data-ttu-id="edab9-238">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="edab9-238">Is-Single-Valued</span></span>       | <span data-ttu-id="edab9-239">Richtig</span><span class="sxs-lookup"><span data-stu-id="edab9-239">True</span></span>                                                                |
| <span data-ttu-id="edab9-240">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="edab9-240">Is Indexed</span></span>             | <span data-ttu-id="edab9-241">False</span><span class="sxs-lookup"><span data-stu-id="edab9-241">False</span></span>                                                               |
| <span data-ttu-id="edab9-242">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="edab9-242">In Global Catalog</span></span>      | <span data-ttu-id="edab9-243">False</span><span class="sxs-lookup"><span data-stu-id="edab9-243">False</span></span>                                                               |
| <span data-ttu-id="edab9-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="edab9-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="edab9-245">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="edab9-245">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="edab9-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edab9-246">Range-Lower</span></span>            | <span data-ttu-id="edab9-247">1</span><span class="sxs-lookup"><span data-stu-id="edab9-247">1</span></span>                                                                   |
| <span data-ttu-id="edab9-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edab9-248">Range-Upper</span></span>            | <span data-ttu-id="edab9-249">255</span><span class="sxs-lookup"><span data-stu-id="edab9-249">255</span></span>                                                                 |
| <span data-ttu-id="edab9-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edab9-250">Search-Flags</span></span>           | <span data-ttu-id="edab9-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edab9-251">0x00000000</span></span>                                                          |
| <span data-ttu-id="edab9-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edab9-252">System-Flags</span></span>           | <span data-ttu-id="edab9-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edab9-253">0x00000010</span></span>                                                          |
| <span data-ttu-id="edab9-254">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="edab9-254">Classes used in</span></span>        | [<span data-ttu-id="edab9-255">**MSMQ-Custom-Recipient**</span><span class="sxs-lookup"><span data-stu-id="edab9-255">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



 

 





