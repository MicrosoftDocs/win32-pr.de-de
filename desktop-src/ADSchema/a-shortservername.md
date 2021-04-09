---
title: Short-Server-Name-Attribut
description: Windows-kompatibler Servername (Pre-Windows 2000) für Druckserver.
ms.assetid: 639704f4-e2b6-43e1-9b1b-6afffe8f0f6a
ms.tgt_platform: multiple
keywords:
- AD-Schema für das Short-Server-Name-Attribut
- shortservername-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Short-Server-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e71b7cf5687b530bf76c673187d5152089d885d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957578"
---
# <a name="short-server-name-attribute"></a><span data-ttu-id="55ec0-105">Short-Server-Name-Attribut</span><span class="sxs-lookup"><span data-stu-id="55ec0-105">Short-Server-Name attribute</span></span>

<span data-ttu-id="55ec0-106">Windows-kompatibler Servername (Pre-Windows 2000) für Druckserver.</span><span class="sxs-lookup"><span data-stu-id="55ec0-106">Pre-Windows 2000 compatible server name for print servers.</span></span>



| <span data-ttu-id="55ec0-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="55ec0-107">Entry</span></span> | <span data-ttu-id="55ec0-108">Wert</span><span class="sxs-lookup"><span data-stu-id="55ec0-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="55ec0-109">CN</span><span class="sxs-lookup"><span data-stu-id="55ec0-109">CN</span></span>                | <span data-ttu-id="55ec0-110">Short-Server-Name</span><span class="sxs-lookup"><span data-stu-id="55ec0-110">Short-Server-Name</span></span>                           |
| <span data-ttu-id="55ec0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="55ec0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="55ec0-112">shortServerName</span><span class="sxs-lookup"><span data-stu-id="55ec0-112">shortServerName</span></span>                             |
| <span data-ttu-id="55ec0-113">Size</span><span class="sxs-lookup"><span data-stu-id="55ec0-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="55ec0-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="55ec0-114">Update Privilege</span></span>  | <span data-ttu-id="55ec0-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="55ec0-115">Domain administrator</span></span>                        |
| <span data-ttu-id="55ec0-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="55ec0-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="55ec0-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="55ec0-117">Attribute-Id</span></span>      | <span data-ttu-id="55ec0-118">1.2.840.113556.1.4.1209</span><span class="sxs-lookup"><span data-stu-id="55ec0-118">1.2.840.113556.1.4.1209</span></span>                     |
| <span data-ttu-id="55ec0-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="55ec0-119">System-Id-Guid</span></span>    | <span data-ttu-id="55ec0-120">45b01501-c419-11d1-bbc9-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="55ec0-120">45b01501-c419-11d1-bbc9-0080c76670c0</span></span>        |
| <span data-ttu-id="55ec0-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="55ec0-121">Syntax</span></span>            | [<span data-ttu-id="55ec0-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="55ec0-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="55ec0-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="55ec0-123">Implementations</span></span>

-   [<span data-ttu-id="55ec0-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="55ec0-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="55ec0-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="55ec0-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="55ec0-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="55ec0-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="55ec0-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="55ec0-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="55ec0-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="55ec0-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="55ec0-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="55ec0-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="55ec0-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="55ec0-130">Windows 2000 Server</span></span>



| <span data-ttu-id="55ec0-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="55ec0-131">Entry</span></span> | <span data-ttu-id="55ec0-132">Wert</span><span class="sxs-lookup"><span data-stu-id="55ec0-132">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="55ec0-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="55ec0-133">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="55ec0-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55ec0-134">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="55ec0-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="55ec0-135">System-Only</span></span>            | <span data-ttu-id="55ec0-136">False</span><span class="sxs-lookup"><span data-stu-id="55ec0-136">False</span></span>                                          |
| <span data-ttu-id="55ec0-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="55ec0-137">Is-Single-Valued</span></span>       | <span data-ttu-id="55ec0-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="55ec0-138">True</span></span>                                           |
| <span data-ttu-id="55ec0-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="55ec0-139">Is Indexed</span></span>             | <span data-ttu-id="55ec0-140">False</span><span class="sxs-lookup"><span data-stu-id="55ec0-140">False</span></span>                                          |
| <span data-ttu-id="55ec0-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="55ec0-141">In Global Catalog</span></span>      | <span data-ttu-id="55ec0-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="55ec0-142">True</span></span>                                           |
| <span data-ttu-id="55ec0-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="55ec0-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="55ec0-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="55ec0-144">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="55ec0-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55ec0-145">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="55ec0-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55ec0-146">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="55ec0-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55ec0-147">Search-Flags</span></span>           | <span data-ttu-id="55ec0-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55ec0-148">0x00000000</span></span>                                     |
| <span data-ttu-id="55ec0-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55ec0-149">System-Flags</span></span>           | <span data-ttu-id="55ec0-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55ec0-150">0x00000010</span></span>                                     |
| <span data-ttu-id="55ec0-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="55ec0-151">Classes used in</span></span>        | [<span data-ttu-id="55ec0-152">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="55ec0-152">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="55ec0-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="55ec0-153">Windows Server 2003</span></span>



| <span data-ttu-id="55ec0-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="55ec0-154">Entry</span></span> | <span data-ttu-id="55ec0-155">Wert</span><span class="sxs-lookup"><span data-stu-id="55ec0-155">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="55ec0-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="55ec0-156">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="55ec0-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55ec0-157">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="55ec0-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="55ec0-158">System-Only</span></span>            | <span data-ttu-id="55ec0-159">False</span><span class="sxs-lookup"><span data-stu-id="55ec0-159">False</span></span>                                          |
| <span data-ttu-id="55ec0-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="55ec0-160">Is-Single-Valued</span></span>       | <span data-ttu-id="55ec0-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="55ec0-161">True</span></span>                                           |
| <span data-ttu-id="55ec0-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="55ec0-162">Is Indexed</span></span>             | <span data-ttu-id="55ec0-163">False</span><span class="sxs-lookup"><span data-stu-id="55ec0-163">False</span></span>                                          |
| <span data-ttu-id="55ec0-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="55ec0-164">In Global Catalog</span></span>      | <span data-ttu-id="55ec0-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="55ec0-165">True</span></span>                                           |
| <span data-ttu-id="55ec0-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="55ec0-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="55ec0-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="55ec0-167">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="55ec0-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55ec0-168">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="55ec0-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55ec0-169">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="55ec0-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55ec0-170">Search-Flags</span></span>           | <span data-ttu-id="55ec0-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55ec0-171">0x00000000</span></span>                                     |
| <span data-ttu-id="55ec0-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55ec0-172">System-Flags</span></span>           | <span data-ttu-id="55ec0-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55ec0-173">0x00000010</span></span>                                     |
| <span data-ttu-id="55ec0-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="55ec0-174">Classes used in</span></span>        | [<span data-ttu-id="55ec0-175">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="55ec0-175">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="55ec0-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="55ec0-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="55ec0-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="55ec0-177">Entry</span></span> | <span data-ttu-id="55ec0-178">Wert</span><span class="sxs-lookup"><span data-stu-id="55ec0-178">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="55ec0-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="55ec0-179">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="55ec0-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55ec0-180">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="55ec0-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="55ec0-181">System-Only</span></span>            | <span data-ttu-id="55ec0-182">False</span><span class="sxs-lookup"><span data-stu-id="55ec0-182">False</span></span>                                          |
| <span data-ttu-id="55ec0-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="55ec0-183">Is-Single-Valued</span></span>       | <span data-ttu-id="55ec0-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="55ec0-184">True</span></span>                                           |
| <span data-ttu-id="55ec0-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="55ec0-185">Is Indexed</span></span>             | <span data-ttu-id="55ec0-186">False</span><span class="sxs-lookup"><span data-stu-id="55ec0-186">False</span></span>                                          |
| <span data-ttu-id="55ec0-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="55ec0-187">In Global Catalog</span></span>      | <span data-ttu-id="55ec0-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="55ec0-188">True</span></span>                                           |
| <span data-ttu-id="55ec0-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="55ec0-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="55ec0-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="55ec0-190">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="55ec0-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55ec0-191">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="55ec0-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55ec0-192">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="55ec0-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55ec0-193">Search-Flags</span></span>           | <span data-ttu-id="55ec0-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55ec0-194">0x00000000</span></span>                                     |
| <span data-ttu-id="55ec0-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55ec0-195">System-Flags</span></span>           | <span data-ttu-id="55ec0-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55ec0-196">0x00000010</span></span>                                     |
| <span data-ttu-id="55ec0-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="55ec0-197">Classes used in</span></span>        | [<span data-ttu-id="55ec0-198">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="55ec0-198">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="55ec0-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55ec0-199">Windows Server 2008</span></span>



| <span data-ttu-id="55ec0-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="55ec0-200">Entry</span></span> | <span data-ttu-id="55ec0-201">Wert</span><span class="sxs-lookup"><span data-stu-id="55ec0-201">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="55ec0-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="55ec0-202">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="55ec0-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55ec0-203">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="55ec0-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="55ec0-204">System-Only</span></span>            | <span data-ttu-id="55ec0-205">False</span><span class="sxs-lookup"><span data-stu-id="55ec0-205">False</span></span>                                          |
| <span data-ttu-id="55ec0-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="55ec0-206">Is-Single-Valued</span></span>       | <span data-ttu-id="55ec0-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="55ec0-207">True</span></span>                                           |
| <span data-ttu-id="55ec0-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="55ec0-208">Is Indexed</span></span>             | <span data-ttu-id="55ec0-209">False</span><span class="sxs-lookup"><span data-stu-id="55ec0-209">False</span></span>                                          |
| <span data-ttu-id="55ec0-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="55ec0-210">In Global Catalog</span></span>      | <span data-ttu-id="55ec0-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="55ec0-211">True</span></span>                                           |
| <span data-ttu-id="55ec0-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="55ec0-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="55ec0-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="55ec0-213">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="55ec0-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55ec0-214">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="55ec0-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55ec0-215">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="55ec0-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55ec0-216">Search-Flags</span></span>           | <span data-ttu-id="55ec0-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55ec0-217">0x00000000</span></span>                                     |
| <span data-ttu-id="55ec0-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55ec0-218">System-Flags</span></span>           | <span data-ttu-id="55ec0-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55ec0-219">0x00000010</span></span>                                     |
| <span data-ttu-id="55ec0-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="55ec0-220">Classes used in</span></span>        | [<span data-ttu-id="55ec0-221">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="55ec0-221">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="55ec0-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="55ec0-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="55ec0-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="55ec0-223">Entry</span></span> | <span data-ttu-id="55ec0-224">Wert</span><span class="sxs-lookup"><span data-stu-id="55ec0-224">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="55ec0-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="55ec0-225">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="55ec0-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55ec0-226">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="55ec0-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="55ec0-227">System-Only</span></span>            | <span data-ttu-id="55ec0-228">False</span><span class="sxs-lookup"><span data-stu-id="55ec0-228">False</span></span>                                          |
| <span data-ttu-id="55ec0-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="55ec0-229">Is-Single-Valued</span></span>       | <span data-ttu-id="55ec0-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="55ec0-230">True</span></span>                                           |
| <span data-ttu-id="55ec0-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="55ec0-231">Is Indexed</span></span>             | <span data-ttu-id="55ec0-232">False</span><span class="sxs-lookup"><span data-stu-id="55ec0-232">False</span></span>                                          |
| <span data-ttu-id="55ec0-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="55ec0-233">In Global Catalog</span></span>      | <span data-ttu-id="55ec0-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="55ec0-234">True</span></span>                                           |
| <span data-ttu-id="55ec0-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="55ec0-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="55ec0-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="55ec0-236">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="55ec0-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55ec0-237">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="55ec0-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55ec0-238">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="55ec0-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55ec0-239">Search-Flags</span></span>           | <span data-ttu-id="55ec0-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55ec0-240">0x00000000</span></span>                                     |
| <span data-ttu-id="55ec0-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55ec0-241">System-Flags</span></span>           | <span data-ttu-id="55ec0-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55ec0-242">0x00000010</span></span>                                     |
| <span data-ttu-id="55ec0-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="55ec0-243">Classes used in</span></span>        | [<span data-ttu-id="55ec0-244">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="55ec0-244">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="55ec0-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="55ec0-245">Windows Server 2012</span></span>



| <span data-ttu-id="55ec0-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="55ec0-246">Entry</span></span> | <span data-ttu-id="55ec0-247">Wert</span><span class="sxs-lookup"><span data-stu-id="55ec0-247">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="55ec0-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="55ec0-248">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="55ec0-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55ec0-249">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="55ec0-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="55ec0-250">System-Only</span></span>            | <span data-ttu-id="55ec0-251">False</span><span class="sxs-lookup"><span data-stu-id="55ec0-251">False</span></span>                                          |
| <span data-ttu-id="55ec0-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="55ec0-252">Is-Single-Valued</span></span>       | <span data-ttu-id="55ec0-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="55ec0-253">True</span></span>                                           |
| <span data-ttu-id="55ec0-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="55ec0-254">Is Indexed</span></span>             | <span data-ttu-id="55ec0-255">False</span><span class="sxs-lookup"><span data-stu-id="55ec0-255">False</span></span>                                          |
| <span data-ttu-id="55ec0-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="55ec0-256">In Global Catalog</span></span>      | <span data-ttu-id="55ec0-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="55ec0-257">True</span></span>                                           |
| <span data-ttu-id="55ec0-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="55ec0-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="55ec0-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="55ec0-259">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="55ec0-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55ec0-260">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="55ec0-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55ec0-261">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="55ec0-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55ec0-262">Search-Flags</span></span>           | <span data-ttu-id="55ec0-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55ec0-263">0x00000000</span></span>                                     |
| <span data-ttu-id="55ec0-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55ec0-264">System-Flags</span></span>           | <span data-ttu-id="55ec0-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55ec0-265">0x00000010</span></span>                                     |
| <span data-ttu-id="55ec0-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="55ec0-266">Classes used in</span></span>        | [<span data-ttu-id="55ec0-267">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="55ec0-267">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





