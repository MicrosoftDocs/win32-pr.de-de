---
title: MSMQ-Multicast-Address-Attribut
description: Dies ist Teil eines MSMQ-Objekts, das durch den Aufruf der API auf MQCreateQueue oder mqsetproperties festgelegt wird. Es steuert, ob MSMQ Nachrichten von einer Multicast Adresse annimmt.
ms.assetid: 65622cc9-81d9-42c6-b208-cac703f32244
ms.tgt_platform: multiple
keywords:
- AD-Schema für MSMQ-Multicast-Address-Attribut
- AD-Schema für MSMQ-MulticastAddress-Attribut
topic_type:
- apiref
api_name:
- MSMQ-Multicast-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b90543c40e22d8dd5fdc2b3e5195bd9382357
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519772"
---
# <a name="msmq-multicast-address-attribute"></a><span data-ttu-id="b2599-106">MSMQ-Multicast-Address-Attribut</span><span class="sxs-lookup"><span data-stu-id="b2599-106">MSMQ-Multicast-Address attribute</span></span>

<span data-ttu-id="b2599-107">Dies ist Teil eines MSMQ-Objekts, das durch den Aufruf der API auf MQCreateQueue oder mqsetproperties festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b2599-107">This is part of an MSMQ object, it is set by calling API to MQCreateQueue or MQSetProperties.</span></span> <span data-ttu-id="b2599-108">Es steuert, ob MSMQ Nachrichten von einer Multicast Adresse annimmt.</span><span class="sxs-lookup"><span data-stu-id="b2599-108">It controls whether MSMQ will accept messages from a multicast address.</span></span>



| <span data-ttu-id="b2599-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b2599-109">Entry</span></span> | <span data-ttu-id="b2599-110">Wert</span><span class="sxs-lookup"><span data-stu-id="b2599-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b2599-111">CN</span><span class="sxs-lookup"><span data-stu-id="b2599-111">CN</span></span>                | <span data-ttu-id="b2599-112">MSMQ-Multicast Adresse</span><span class="sxs-lookup"><span data-stu-id="b2599-112">MSMQ-Multicast-Address</span></span>                      |
| <span data-ttu-id="b2599-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b2599-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b2599-114">MSMQ-MulticastAddress</span><span class="sxs-lookup"><span data-stu-id="b2599-114">MSMQ-MulticastAddress</span></span>                       |
| <span data-ttu-id="b2599-115">Size</span><span class="sxs-lookup"><span data-stu-id="b2599-115">Size</span></span>              | <span data-ttu-id="b2599-116">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="b2599-116">4 bytes</span></span>                                     |
| <span data-ttu-id="b2599-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b2599-117">Update Privilege</span></span>  | <span data-ttu-id="b2599-118">Der Besitzer der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="b2599-118">The queue owner.</span></span>                            |
| <span data-ttu-id="b2599-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b2599-119">Update Frequency</span></span>  | <span data-ttu-id="b2599-120">Wenn eine Warteschlange erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b2599-120">When a queue is created.</span></span>                    |
| <span data-ttu-id="b2599-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b2599-121">Attribute-Id</span></span>      | <span data-ttu-id="b2599-122">1.2.840.113556.1.4.1714</span><span class="sxs-lookup"><span data-stu-id="b2599-122">1.2.840.113556.1.4.1714</span></span>                     |
| <span data-ttu-id="b2599-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b2599-123">System-Id-Guid</span></span>    | <span data-ttu-id="b2599-124">1d2f 4412-B48-6e5b125 cd265</span><span class="sxs-lookup"><span data-stu-id="b2599-124">1d2f4412-f10d-4337-9b48-6e5b125cd265</span></span>        |
| <span data-ttu-id="b2599-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2599-125">Syntax</span></span>            | [<span data-ttu-id="b2599-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b2599-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b2599-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b2599-127">Implementations</span></span>

-   [<span data-ttu-id="b2599-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b2599-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b2599-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b2599-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b2599-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b2599-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b2599-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b2599-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b2599-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b2599-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b2599-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b2599-133">Windows Server 2003</span></span>



| <span data-ttu-id="b2599-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b2599-134">Entry</span></span> | <span data-ttu-id="b2599-135">Wert</span><span class="sxs-lookup"><span data-stu-id="b2599-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b2599-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b2599-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2599-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2599-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2599-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2599-138">System-Only</span></span>            | <span data-ttu-id="b2599-139">False</span><span class="sxs-lookup"><span data-stu-id="b2599-139">False</span></span>                                        |
| <span data-ttu-id="b2599-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b2599-140">Is-Single-Valued</span></span>       | <span data-ttu-id="b2599-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="b2599-141">True</span></span>                                         |
| <span data-ttu-id="b2599-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b2599-142">Is Indexed</span></span>             | <span data-ttu-id="b2599-143">False</span><span class="sxs-lookup"><span data-stu-id="b2599-143">False</span></span>                                        |
| <span data-ttu-id="b2599-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b2599-144">In Global Catalog</span></span>      | <span data-ttu-id="b2599-145">Richtig</span><span class="sxs-lookup"><span data-stu-id="b2599-145">True</span></span>                                         |
| <span data-ttu-id="b2599-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b2599-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2599-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b2599-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b2599-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2599-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b2599-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2599-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b2599-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2599-150">Search-Flags</span></span>           | <span data-ttu-id="b2599-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2599-151">0x00000000</span></span>                                   |
| <span data-ttu-id="b2599-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2599-152">System-Flags</span></span>           | <span data-ttu-id="b2599-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2599-153">0x00000010</span></span>                                   |
| <span data-ttu-id="b2599-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b2599-154">Classes used in</span></span>        | [<span data-ttu-id="b2599-155">**MSMQ-Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="b2599-155">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b2599-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b2599-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b2599-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b2599-157">Entry</span></span> | <span data-ttu-id="b2599-158">Wert</span><span class="sxs-lookup"><span data-stu-id="b2599-158">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b2599-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b2599-159">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2599-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2599-160">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2599-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2599-161">System-Only</span></span>            | <span data-ttu-id="b2599-162">False</span><span class="sxs-lookup"><span data-stu-id="b2599-162">False</span></span>                                        |
| <span data-ttu-id="b2599-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b2599-163">Is-Single-Valued</span></span>       | <span data-ttu-id="b2599-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="b2599-164">True</span></span>                                         |
| <span data-ttu-id="b2599-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b2599-165">Is Indexed</span></span>             | <span data-ttu-id="b2599-166">False</span><span class="sxs-lookup"><span data-stu-id="b2599-166">False</span></span>                                        |
| <span data-ttu-id="b2599-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b2599-167">In Global Catalog</span></span>      | <span data-ttu-id="b2599-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="b2599-168">True</span></span>                                         |
| <span data-ttu-id="b2599-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b2599-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2599-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b2599-170">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b2599-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2599-171">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b2599-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2599-172">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b2599-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2599-173">Search-Flags</span></span>           | <span data-ttu-id="b2599-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2599-174">0x00000000</span></span>                                   |
| <span data-ttu-id="b2599-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2599-175">System-Flags</span></span>           | <span data-ttu-id="b2599-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2599-176">0x00000010</span></span>                                   |
| <span data-ttu-id="b2599-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b2599-177">Classes used in</span></span>        | [<span data-ttu-id="b2599-178">**MSMQ-Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="b2599-178">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b2599-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2599-179">Windows Server 2008</span></span>



| <span data-ttu-id="b2599-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b2599-180">Entry</span></span> | <span data-ttu-id="b2599-181">Wert</span><span class="sxs-lookup"><span data-stu-id="b2599-181">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b2599-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b2599-182">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2599-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2599-183">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2599-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2599-184">System-Only</span></span>            | <span data-ttu-id="b2599-185">False</span><span class="sxs-lookup"><span data-stu-id="b2599-185">False</span></span>                                        |
| <span data-ttu-id="b2599-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b2599-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b2599-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="b2599-187">True</span></span>                                         |
| <span data-ttu-id="b2599-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b2599-188">Is Indexed</span></span>             | <span data-ttu-id="b2599-189">False</span><span class="sxs-lookup"><span data-stu-id="b2599-189">False</span></span>                                        |
| <span data-ttu-id="b2599-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b2599-190">In Global Catalog</span></span>      | <span data-ttu-id="b2599-191">Richtig</span><span class="sxs-lookup"><span data-stu-id="b2599-191">True</span></span>                                         |
| <span data-ttu-id="b2599-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b2599-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2599-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b2599-193">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b2599-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2599-194">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b2599-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2599-195">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b2599-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2599-196">Search-Flags</span></span>           | <span data-ttu-id="b2599-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2599-197">0x00000000</span></span>                                   |
| <span data-ttu-id="b2599-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2599-198">System-Flags</span></span>           | <span data-ttu-id="b2599-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2599-199">0x00000010</span></span>                                   |
| <span data-ttu-id="b2599-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b2599-200">Classes used in</span></span>        | [<span data-ttu-id="b2599-201">**MSMQ-Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="b2599-201">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b2599-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b2599-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b2599-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b2599-203">Entry</span></span> | <span data-ttu-id="b2599-204">Wert</span><span class="sxs-lookup"><span data-stu-id="b2599-204">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b2599-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b2599-205">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2599-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2599-206">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2599-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2599-207">System-Only</span></span>            | <span data-ttu-id="b2599-208">False</span><span class="sxs-lookup"><span data-stu-id="b2599-208">False</span></span>                                        |
| <span data-ttu-id="b2599-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b2599-209">Is-Single-Valued</span></span>       | <span data-ttu-id="b2599-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="b2599-210">True</span></span>                                         |
| <span data-ttu-id="b2599-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b2599-211">Is Indexed</span></span>             | <span data-ttu-id="b2599-212">False</span><span class="sxs-lookup"><span data-stu-id="b2599-212">False</span></span>                                        |
| <span data-ttu-id="b2599-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b2599-213">In Global Catalog</span></span>      | <span data-ttu-id="b2599-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="b2599-214">True</span></span>                                         |
| <span data-ttu-id="b2599-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b2599-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2599-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b2599-216">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b2599-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2599-217">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b2599-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2599-218">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b2599-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2599-219">Search-Flags</span></span>           | <span data-ttu-id="b2599-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2599-220">0x00000000</span></span>                                   |
| <span data-ttu-id="b2599-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2599-221">System-Flags</span></span>           | <span data-ttu-id="b2599-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2599-222">0x00000010</span></span>                                   |
| <span data-ttu-id="b2599-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b2599-223">Classes used in</span></span>        | [<span data-ttu-id="b2599-224">**MSMQ-Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="b2599-224">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b2599-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b2599-225">Windows Server 2012</span></span>



| <span data-ttu-id="b2599-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b2599-226">Entry</span></span> | <span data-ttu-id="b2599-227">Wert</span><span class="sxs-lookup"><span data-stu-id="b2599-227">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b2599-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b2599-228">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2599-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2599-229">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b2599-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2599-230">System-Only</span></span>            | <span data-ttu-id="b2599-231">False</span><span class="sxs-lookup"><span data-stu-id="b2599-231">False</span></span>                                        |
| <span data-ttu-id="b2599-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b2599-232">Is-Single-Valued</span></span>       | <span data-ttu-id="b2599-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="b2599-233">True</span></span>                                         |
| <span data-ttu-id="b2599-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b2599-234">Is Indexed</span></span>             | <span data-ttu-id="b2599-235">False</span><span class="sxs-lookup"><span data-stu-id="b2599-235">False</span></span>                                        |
| <span data-ttu-id="b2599-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b2599-236">In Global Catalog</span></span>      | <span data-ttu-id="b2599-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="b2599-237">True</span></span>                                         |
| <span data-ttu-id="b2599-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b2599-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2599-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b2599-239">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b2599-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2599-240">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b2599-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2599-241">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b2599-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2599-242">Search-Flags</span></span>           | <span data-ttu-id="b2599-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2599-243">0x00000000</span></span>                                   |
| <span data-ttu-id="b2599-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2599-244">System-Flags</span></span>           | <span data-ttu-id="b2599-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2599-245">0x00000010</span></span>                                   |
| <span data-ttu-id="b2599-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b2599-246">Classes used in</span></span>        | [<span data-ttu-id="b2599-247">**MSMQ-Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="b2599-247">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





