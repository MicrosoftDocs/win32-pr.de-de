---
title: Remote-Source-Attribut
description: Rückwärts Zeiger auf fremde Objekte.
ms.assetid: 99d6d80f-b11a-48f2-93c9-866a99105488
ms.tgt_platform: multiple
keywords:
- AD-Schema für Remote-Source-Attribut
- AD-Schema des remotesource-Attributs
topic_type:
- apiref
api_name:
- Remote-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 147cfb24c72c4e0250d03def69d5cb5408778780
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859579"
---
# <a name="remote-source-attribute"></a><span data-ttu-id="53fab-105">Remote-Source-Attribut</span><span class="sxs-lookup"><span data-stu-id="53fab-105">Remote-Source attribute</span></span>

<span data-ttu-id="53fab-106">Rückwärts Zeiger auf fremde Objekte.</span><span class="sxs-lookup"><span data-stu-id="53fab-106">Backward pointer to foreign objects.</span></span>



| <span data-ttu-id="53fab-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53fab-107">Entry</span></span> | <span data-ttu-id="53fab-108">Wert</span><span class="sxs-lookup"><span data-stu-id="53fab-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="53fab-109">CN</span><span class="sxs-lookup"><span data-stu-id="53fab-109">CN</span></span>                | <span data-ttu-id="53fab-110">Remote-Source</span><span class="sxs-lookup"><span data-stu-id="53fab-110">Remote-Source</span></span>                               |
| <span data-ttu-id="53fab-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="53fab-111">Ldap-Display-Name</span></span> | <span data-ttu-id="53fab-112">remotesource</span><span class="sxs-lookup"><span data-stu-id="53fab-112">remoteSource</span></span>                                |
| <span data-ttu-id="53fab-113">Size</span><span class="sxs-lookup"><span data-stu-id="53fab-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="53fab-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="53fab-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="53fab-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="53fab-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="53fab-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="53fab-116">Attribute-Id</span></span>      | <span data-ttu-id="53fab-117">1.2.840.113556.1.4.107</span><span class="sxs-lookup"><span data-stu-id="53fab-117">1.2.840.113556.1.4.107</span></span>                      |
| <span data-ttu-id="53fab-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="53fab-118">System-Id-Guid</span></span>    | <span data-ttu-id="53fab-119">bf967a14-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="53fab-119">bf967a14-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="53fab-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="53fab-120">Syntax</span></span>            | [<span data-ttu-id="53fab-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="53fab-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="53fab-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="53fab-122">Implementations</span></span>

-   [<span data-ttu-id="53fab-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="53fab-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="53fab-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="53fab-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="53fab-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="53fab-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="53fab-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="53fab-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="53fab-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="53fab-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="53fab-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="53fab-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="53fab-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="53fab-129">Windows 2000 Server</span></span>



| <span data-ttu-id="53fab-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53fab-130">Entry</span></span> | <span data-ttu-id="53fab-131">Wert</span><span class="sxs-lookup"><span data-stu-id="53fab-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="53fab-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53fab-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="53fab-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53fab-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="53fab-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="53fab-134">System-Only</span></span>            | <span data-ttu-id="53fab-135">False</span><span class="sxs-lookup"><span data-stu-id="53fab-135">False</span></span>                                                             |
| <span data-ttu-id="53fab-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53fab-136">Is-Single-Valued</span></span>       | <span data-ttu-id="53fab-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="53fab-137">True</span></span>                                                              |
| <span data-ttu-id="53fab-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53fab-138">Is Indexed</span></span>             | <span data-ttu-id="53fab-139">False</span><span class="sxs-lookup"><span data-stu-id="53fab-139">False</span></span>                                                             |
| <span data-ttu-id="53fab-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53fab-140">In Global Catalog</span></span>      | <span data-ttu-id="53fab-141">False</span><span class="sxs-lookup"><span data-stu-id="53fab-141">False</span></span>                                                             |
| <span data-ttu-id="53fab-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53fab-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="53fab-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53fab-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="53fab-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53fab-144">Range-Lower</span></span>            | <span data-ttu-id="53fab-145">1</span><span class="sxs-lookup"><span data-stu-id="53fab-145">1</span></span>                                                                 |
| <span data-ttu-id="53fab-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53fab-146">Range-Upper</span></span>            | <span data-ttu-id="53fab-147">1024</span><span class="sxs-lookup"><span data-stu-id="53fab-147">1024</span></span>                                                              |
| <span data-ttu-id="53fab-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53fab-148">Search-Flags</span></span>           | <span data-ttu-id="53fab-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53fab-149">0x00000000</span></span>                                                        |
| <span data-ttu-id="53fab-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53fab-150">System-Flags</span></span>           | <span data-ttu-id="53fab-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53fab-151">0x00000010</span></span>                                                        |
| <span data-ttu-id="53fab-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53fab-152">Classes used in</span></span>        | [<span data-ttu-id="53fab-153">**Remote-e-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="53fab-153">**Remote-Mail-Recipient**</span></span>](c-remotemailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="53fab-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="53fab-154">Windows Server 2003</span></span>



| <span data-ttu-id="53fab-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53fab-155">Entry</span></span> | <span data-ttu-id="53fab-156">Wert</span><span class="sxs-lookup"><span data-stu-id="53fab-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="53fab-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53fab-157">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="53fab-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53fab-158">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="53fab-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="53fab-159">System-Only</span></span>            | <span data-ttu-id="53fab-160">False</span><span class="sxs-lookup"><span data-stu-id="53fab-160">False</span></span>                                                             |
| <span data-ttu-id="53fab-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53fab-161">Is-Single-Valued</span></span>       | <span data-ttu-id="53fab-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="53fab-162">True</span></span>                                                              |
| <span data-ttu-id="53fab-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53fab-163">Is Indexed</span></span>             | <span data-ttu-id="53fab-164">False</span><span class="sxs-lookup"><span data-stu-id="53fab-164">False</span></span>                                                             |
| <span data-ttu-id="53fab-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53fab-165">In Global Catalog</span></span>      | <span data-ttu-id="53fab-166">False</span><span class="sxs-lookup"><span data-stu-id="53fab-166">False</span></span>                                                             |
| <span data-ttu-id="53fab-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53fab-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="53fab-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53fab-168">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="53fab-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53fab-169">Range-Lower</span></span>            | <span data-ttu-id="53fab-170">1</span><span class="sxs-lookup"><span data-stu-id="53fab-170">1</span></span>                                                                 |
| <span data-ttu-id="53fab-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53fab-171">Range-Upper</span></span>            | <span data-ttu-id="53fab-172">1024</span><span class="sxs-lookup"><span data-stu-id="53fab-172">1024</span></span>                                                              |
| <span data-ttu-id="53fab-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53fab-173">Search-Flags</span></span>           | <span data-ttu-id="53fab-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53fab-174">0x00000000</span></span>                                                        |
| <span data-ttu-id="53fab-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53fab-175">System-Flags</span></span>           | <span data-ttu-id="53fab-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53fab-176">0x00000010</span></span>                                                        |
| <span data-ttu-id="53fab-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53fab-177">Classes used in</span></span>        | [<span data-ttu-id="53fab-178">**Remote-e-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="53fab-178">**Remote-Mail-Recipient**</span></span>](c-remotemailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="53fab-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="53fab-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="53fab-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53fab-180">Entry</span></span> | <span data-ttu-id="53fab-181">Wert</span><span class="sxs-lookup"><span data-stu-id="53fab-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="53fab-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53fab-182">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="53fab-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53fab-183">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="53fab-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="53fab-184">System-Only</span></span>            | <span data-ttu-id="53fab-185">False</span><span class="sxs-lookup"><span data-stu-id="53fab-185">False</span></span>                                                             |
| <span data-ttu-id="53fab-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53fab-186">Is-Single-Valued</span></span>       | <span data-ttu-id="53fab-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="53fab-187">True</span></span>                                                              |
| <span data-ttu-id="53fab-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53fab-188">Is Indexed</span></span>             | <span data-ttu-id="53fab-189">False</span><span class="sxs-lookup"><span data-stu-id="53fab-189">False</span></span>                                                             |
| <span data-ttu-id="53fab-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53fab-190">In Global Catalog</span></span>      | <span data-ttu-id="53fab-191">False</span><span class="sxs-lookup"><span data-stu-id="53fab-191">False</span></span>                                                             |
| <span data-ttu-id="53fab-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53fab-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="53fab-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53fab-193">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="53fab-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53fab-194">Range-Lower</span></span>            | <span data-ttu-id="53fab-195">1</span><span class="sxs-lookup"><span data-stu-id="53fab-195">1</span></span>                                                                 |
| <span data-ttu-id="53fab-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53fab-196">Range-Upper</span></span>            | <span data-ttu-id="53fab-197">1024</span><span class="sxs-lookup"><span data-stu-id="53fab-197">1024</span></span>                                                              |
| <span data-ttu-id="53fab-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53fab-198">Search-Flags</span></span>           | <span data-ttu-id="53fab-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53fab-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="53fab-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53fab-200">System-Flags</span></span>           | <span data-ttu-id="53fab-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53fab-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="53fab-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53fab-202">Classes used in</span></span>        | [<span data-ttu-id="53fab-203">**Remote-e-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="53fab-203">**Remote-Mail-Recipient**</span></span>](c-remotemailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="53fab-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53fab-204">Windows Server 2008</span></span>



| <span data-ttu-id="53fab-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53fab-205">Entry</span></span> | <span data-ttu-id="53fab-206">Wert</span><span class="sxs-lookup"><span data-stu-id="53fab-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="53fab-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53fab-207">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="53fab-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53fab-208">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="53fab-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="53fab-209">System-Only</span></span>            | <span data-ttu-id="53fab-210">False</span><span class="sxs-lookup"><span data-stu-id="53fab-210">False</span></span>                                                             |
| <span data-ttu-id="53fab-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53fab-211">Is-Single-Valued</span></span>       | <span data-ttu-id="53fab-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="53fab-212">True</span></span>                                                              |
| <span data-ttu-id="53fab-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53fab-213">Is Indexed</span></span>             | <span data-ttu-id="53fab-214">False</span><span class="sxs-lookup"><span data-stu-id="53fab-214">False</span></span>                                                             |
| <span data-ttu-id="53fab-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53fab-215">In Global Catalog</span></span>      | <span data-ttu-id="53fab-216">False</span><span class="sxs-lookup"><span data-stu-id="53fab-216">False</span></span>                                                             |
| <span data-ttu-id="53fab-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53fab-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="53fab-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53fab-218">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="53fab-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53fab-219">Range-Lower</span></span>            | <span data-ttu-id="53fab-220">1</span><span class="sxs-lookup"><span data-stu-id="53fab-220">1</span></span>                                                                 |
| <span data-ttu-id="53fab-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53fab-221">Range-Upper</span></span>            | <span data-ttu-id="53fab-222">1024</span><span class="sxs-lookup"><span data-stu-id="53fab-222">1024</span></span>                                                              |
| <span data-ttu-id="53fab-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53fab-223">Search-Flags</span></span>           | <span data-ttu-id="53fab-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53fab-224">0x00000000</span></span>                                                        |
| <span data-ttu-id="53fab-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53fab-225">System-Flags</span></span>           | <span data-ttu-id="53fab-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53fab-226">0x00000010</span></span>                                                        |
| <span data-ttu-id="53fab-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53fab-227">Classes used in</span></span>        | [<span data-ttu-id="53fab-228">**Remote-e-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="53fab-228">**Remote-Mail-Recipient**</span></span>](c-remotemailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="53fab-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="53fab-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="53fab-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53fab-230">Entry</span></span> | <span data-ttu-id="53fab-231">Wert</span><span class="sxs-lookup"><span data-stu-id="53fab-231">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="53fab-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53fab-232">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="53fab-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53fab-233">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="53fab-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="53fab-234">System-Only</span></span>            | <span data-ttu-id="53fab-235">False</span><span class="sxs-lookup"><span data-stu-id="53fab-235">False</span></span>                                                             |
| <span data-ttu-id="53fab-236">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53fab-236">Is-Single-Valued</span></span>       | <span data-ttu-id="53fab-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="53fab-237">True</span></span>                                                              |
| <span data-ttu-id="53fab-238">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53fab-238">Is Indexed</span></span>             | <span data-ttu-id="53fab-239">False</span><span class="sxs-lookup"><span data-stu-id="53fab-239">False</span></span>                                                             |
| <span data-ttu-id="53fab-240">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53fab-240">In Global Catalog</span></span>      | <span data-ttu-id="53fab-241">False</span><span class="sxs-lookup"><span data-stu-id="53fab-241">False</span></span>                                                             |
| <span data-ttu-id="53fab-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53fab-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="53fab-243">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53fab-243">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="53fab-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53fab-244">Range-Lower</span></span>            | <span data-ttu-id="53fab-245">1</span><span class="sxs-lookup"><span data-stu-id="53fab-245">1</span></span>                                                                 |
| <span data-ttu-id="53fab-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53fab-246">Range-Upper</span></span>            | <span data-ttu-id="53fab-247">1024</span><span class="sxs-lookup"><span data-stu-id="53fab-247">1024</span></span>                                                              |
| <span data-ttu-id="53fab-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53fab-248">Search-Flags</span></span>           | <span data-ttu-id="53fab-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53fab-249">0x00000000</span></span>                                                        |
| <span data-ttu-id="53fab-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53fab-250">System-Flags</span></span>           | <span data-ttu-id="53fab-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53fab-251">0x00000010</span></span>                                                        |
| <span data-ttu-id="53fab-252">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53fab-252">Classes used in</span></span>        | [<span data-ttu-id="53fab-253">**Remote-e-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="53fab-253">**Remote-Mail-Recipient**</span></span>](c-remotemailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="53fab-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53fab-254">Windows Server 2012</span></span>



| <span data-ttu-id="53fab-255">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53fab-255">Entry</span></span> | <span data-ttu-id="53fab-256">Wert</span><span class="sxs-lookup"><span data-stu-id="53fab-256">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="53fab-257">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53fab-257">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="53fab-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53fab-258">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="53fab-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="53fab-259">System-Only</span></span>            | <span data-ttu-id="53fab-260">False</span><span class="sxs-lookup"><span data-stu-id="53fab-260">False</span></span>                                                             |
| <span data-ttu-id="53fab-261">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53fab-261">Is-Single-Valued</span></span>       | <span data-ttu-id="53fab-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="53fab-262">True</span></span>                                                              |
| <span data-ttu-id="53fab-263">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53fab-263">Is Indexed</span></span>             | <span data-ttu-id="53fab-264">False</span><span class="sxs-lookup"><span data-stu-id="53fab-264">False</span></span>                                                             |
| <span data-ttu-id="53fab-265">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53fab-265">In Global Catalog</span></span>      | <span data-ttu-id="53fab-266">False</span><span class="sxs-lookup"><span data-stu-id="53fab-266">False</span></span>                                                             |
| <span data-ttu-id="53fab-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53fab-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="53fab-268">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53fab-268">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="53fab-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53fab-269">Range-Lower</span></span>            | <span data-ttu-id="53fab-270">1</span><span class="sxs-lookup"><span data-stu-id="53fab-270">1</span></span>                                                                 |
| <span data-ttu-id="53fab-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53fab-271">Range-Upper</span></span>            | <span data-ttu-id="53fab-272">1024</span><span class="sxs-lookup"><span data-stu-id="53fab-272">1024</span></span>                                                              |
| <span data-ttu-id="53fab-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53fab-273">Search-Flags</span></span>           | <span data-ttu-id="53fab-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53fab-274">0x00000000</span></span>                                                        |
| <span data-ttu-id="53fab-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53fab-275">System-Flags</span></span>           | <span data-ttu-id="53fab-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53fab-276">0x00000010</span></span>                                                        |
| <span data-ttu-id="53fab-277">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53fab-277">Classes used in</span></span>        | [<span data-ttu-id="53fab-278">**Remote-e-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="53fab-278">**Remote-Mail-Recipient**</span></span>](c-remotemailrecipient.md)<br/> |



 

 





