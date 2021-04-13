---
title: MSMQ-sicheres Quell Attribut
description: Dies ist Teil eines MSMQ-Objekts, das durch den Aufruf der API auf MQCreateQueue oder mqsetproperties festgelegt wird. Es steuert, ob MSMQ Nachrichten nur von einer gesicherten Quelle (z. b. HTTPS) für diese Warteschlange akzeptiert.
ms.assetid: 780d164f-c7fa-4c65-b46e-3a67ead92163
ms.tgt_platform: multiple
keywords:
- AD-Schema für MSMQ-sicheres Quell Attribut
- AD-Schema für MSMQ-SecuredSource-Attribut
topic_type:
- apiref
api_name:
- MSMQ-Secured-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5dd005cedcd650aa0604a85e78a46d10f1e01b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519767"
---
# <a name="msmq-secured-source-attribute"></a><span data-ttu-id="9b889-106">MSMQ-sicheres Quell Attribut</span><span class="sxs-lookup"><span data-stu-id="9b889-106">MSMQ-Secured-Source attribute</span></span>

<span data-ttu-id="9b889-107">Dies ist Teil eines MSMQ-Objekts, das durch den Aufruf der API auf MQCreateQueue oder mqsetproperties festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="9b889-107">This is part of an MSMQ object, it is set by calling API to MQCreateQueue or MQSetProperties.</span></span> <span data-ttu-id="9b889-108">Es steuert, ob MSMQ Nachrichten nur von einer gesicherten Quelle (z. b. HTTPS) für diese Warteschlange akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="9b889-108">It controls whether MSMQ accepts messages only from a secured source (for example, https) for this queue.</span></span>



| <span data-ttu-id="9b889-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9b889-109">Entry</span></span> | <span data-ttu-id="9b889-110">Wert</span><span class="sxs-lookup"><span data-stu-id="9b889-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9b889-111">CN</span><span class="sxs-lookup"><span data-stu-id="9b889-111">CN</span></span>                | <span data-ttu-id="9b889-112">MSMQ-gesicherte Quelle</span><span class="sxs-lookup"><span data-stu-id="9b889-112">MSMQ-Secured-Source</span></span>                  |
| <span data-ttu-id="9b889-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9b889-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9b889-114">MSMQ-SecuredSource</span><span class="sxs-lookup"><span data-stu-id="9b889-114">MSMQ-SecuredSource</span></span>                   |
| <span data-ttu-id="9b889-115">Size</span><span class="sxs-lookup"><span data-stu-id="9b889-115">Size</span></span>              | <span data-ttu-id="9b889-116">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="9b889-116">4 bytes</span></span>                              |
| <span data-ttu-id="9b889-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="9b889-117">Update Privilege</span></span>  | <span data-ttu-id="9b889-118">Der Besitzer der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="9b889-118">The queue owner.</span></span>                     |
| <span data-ttu-id="9b889-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="9b889-119">Update Frequency</span></span>  | <span data-ttu-id="9b889-120">Wenn eine Warteschlange erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9b889-120">When a queue is created.</span></span>             |
| <span data-ttu-id="9b889-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9b889-121">Attribute-Id</span></span>      | <span data-ttu-id="9b889-122">1.2.840.113556.1.4.1713</span><span class="sxs-lookup"><span data-stu-id="9b889-122">1.2.840.113556.1.4.1713</span></span>              |
| <span data-ttu-id="9b889-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9b889-123">System-Id-Guid</span></span>    | <span data-ttu-id="9b889-124">8bf 0221b-7a06-4d63-91-Dienst-D3</span><span class="sxs-lookup"><span data-stu-id="9b889-124">8bf0221b-7a06-4d63-91f0-1499941813d3</span></span> |
| <span data-ttu-id="9b889-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b889-125">Syntax</span></span>            | [<span data-ttu-id="9b889-126">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="9b889-126">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="9b889-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="9b889-127">Implementations</span></span>

-   [<span data-ttu-id="9b889-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9b889-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9b889-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9b889-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9b889-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9b889-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9b889-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9b889-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9b889-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9b889-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9b889-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9b889-133">Windows Server 2003</span></span>



| <span data-ttu-id="9b889-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9b889-134">Entry</span></span> | <span data-ttu-id="9b889-135">Wert</span><span class="sxs-lookup"><span data-stu-id="9b889-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9b889-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9b889-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b889-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b889-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b889-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b889-138">System-Only</span></span>            | <span data-ttu-id="9b889-139">False</span><span class="sxs-lookup"><span data-stu-id="9b889-139">False</span></span>                                        |
| <span data-ttu-id="9b889-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9b889-140">Is-Single-Valued</span></span>       | <span data-ttu-id="9b889-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="9b889-141">True</span></span>                                         |
| <span data-ttu-id="9b889-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9b889-142">Is Indexed</span></span>             | <span data-ttu-id="9b889-143">False</span><span class="sxs-lookup"><span data-stu-id="9b889-143">False</span></span>                                        |
| <span data-ttu-id="9b889-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9b889-144">In Global Catalog</span></span>      | <span data-ttu-id="9b889-145">Richtig</span><span class="sxs-lookup"><span data-stu-id="9b889-145">True</span></span>                                         |
| <span data-ttu-id="9b889-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9b889-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b889-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9b889-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9b889-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b889-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9b889-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b889-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9b889-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b889-150">Search-Flags</span></span>           | <span data-ttu-id="9b889-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b889-151">0x00000000</span></span>                                   |
| <span data-ttu-id="9b889-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b889-152">System-Flags</span></span>           | <span data-ttu-id="9b889-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b889-153">0x00000010</span></span>                                   |
| <span data-ttu-id="9b889-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9b889-154">Classes used in</span></span>        | [<span data-ttu-id="9b889-155">**MSMQ-Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="9b889-155">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9b889-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9b889-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9b889-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9b889-157">Entry</span></span> | <span data-ttu-id="9b889-158">Wert</span><span class="sxs-lookup"><span data-stu-id="9b889-158">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9b889-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9b889-159">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b889-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b889-160">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b889-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b889-161">System-Only</span></span>            | <span data-ttu-id="9b889-162">False</span><span class="sxs-lookup"><span data-stu-id="9b889-162">False</span></span>                                        |
| <span data-ttu-id="9b889-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9b889-163">Is-Single-Valued</span></span>       | <span data-ttu-id="9b889-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="9b889-164">True</span></span>                                         |
| <span data-ttu-id="9b889-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9b889-165">Is Indexed</span></span>             | <span data-ttu-id="9b889-166">False</span><span class="sxs-lookup"><span data-stu-id="9b889-166">False</span></span>                                        |
| <span data-ttu-id="9b889-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9b889-167">In Global Catalog</span></span>      | <span data-ttu-id="9b889-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="9b889-168">True</span></span>                                         |
| <span data-ttu-id="9b889-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9b889-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b889-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9b889-170">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9b889-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b889-171">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9b889-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b889-172">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9b889-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b889-173">Search-Flags</span></span>           | <span data-ttu-id="9b889-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b889-174">0x00000000</span></span>                                   |
| <span data-ttu-id="9b889-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b889-175">System-Flags</span></span>           | <span data-ttu-id="9b889-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b889-176">0x00000010</span></span>                                   |
| <span data-ttu-id="9b889-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9b889-177">Classes used in</span></span>        | [<span data-ttu-id="9b889-178">**MSMQ-Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="9b889-178">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9b889-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b889-179">Windows Server 2008</span></span>



| <span data-ttu-id="9b889-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9b889-180">Entry</span></span> | <span data-ttu-id="9b889-181">Wert</span><span class="sxs-lookup"><span data-stu-id="9b889-181">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9b889-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9b889-182">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b889-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b889-183">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b889-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b889-184">System-Only</span></span>            | <span data-ttu-id="9b889-185">False</span><span class="sxs-lookup"><span data-stu-id="9b889-185">False</span></span>                                        |
| <span data-ttu-id="9b889-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9b889-186">Is-Single-Valued</span></span>       | <span data-ttu-id="9b889-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="9b889-187">True</span></span>                                         |
| <span data-ttu-id="9b889-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9b889-188">Is Indexed</span></span>             | <span data-ttu-id="9b889-189">False</span><span class="sxs-lookup"><span data-stu-id="9b889-189">False</span></span>                                        |
| <span data-ttu-id="9b889-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9b889-190">In Global Catalog</span></span>      | <span data-ttu-id="9b889-191">Richtig</span><span class="sxs-lookup"><span data-stu-id="9b889-191">True</span></span>                                         |
| <span data-ttu-id="9b889-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9b889-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b889-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9b889-193">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9b889-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b889-194">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9b889-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b889-195">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9b889-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b889-196">Search-Flags</span></span>           | <span data-ttu-id="9b889-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b889-197">0x00000000</span></span>                                   |
| <span data-ttu-id="9b889-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b889-198">System-Flags</span></span>           | <span data-ttu-id="9b889-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b889-199">0x00000010</span></span>                                   |
| <span data-ttu-id="9b889-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9b889-200">Classes used in</span></span>        | [<span data-ttu-id="9b889-201">**MSMQ-Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="9b889-201">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9b889-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9b889-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9b889-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9b889-203">Entry</span></span> | <span data-ttu-id="9b889-204">Wert</span><span class="sxs-lookup"><span data-stu-id="9b889-204">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9b889-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9b889-205">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b889-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b889-206">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b889-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b889-207">System-Only</span></span>            | <span data-ttu-id="9b889-208">False</span><span class="sxs-lookup"><span data-stu-id="9b889-208">False</span></span>                                        |
| <span data-ttu-id="9b889-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9b889-209">Is-Single-Valued</span></span>       | <span data-ttu-id="9b889-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="9b889-210">True</span></span>                                         |
| <span data-ttu-id="9b889-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9b889-211">Is Indexed</span></span>             | <span data-ttu-id="9b889-212">False</span><span class="sxs-lookup"><span data-stu-id="9b889-212">False</span></span>                                        |
| <span data-ttu-id="9b889-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9b889-213">In Global Catalog</span></span>      | <span data-ttu-id="9b889-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="9b889-214">True</span></span>                                         |
| <span data-ttu-id="9b889-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9b889-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b889-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9b889-216">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9b889-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b889-217">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9b889-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b889-218">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9b889-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b889-219">Search-Flags</span></span>           | <span data-ttu-id="9b889-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b889-220">0x00000000</span></span>                                   |
| <span data-ttu-id="9b889-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b889-221">System-Flags</span></span>           | <span data-ttu-id="9b889-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b889-222">0x00000010</span></span>                                   |
| <span data-ttu-id="9b889-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9b889-223">Classes used in</span></span>        | [<span data-ttu-id="9b889-224">**MSMQ-Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="9b889-224">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9b889-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9b889-225">Windows Server 2012</span></span>



| <span data-ttu-id="9b889-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9b889-226">Entry</span></span> | <span data-ttu-id="9b889-227">Wert</span><span class="sxs-lookup"><span data-stu-id="9b889-227">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9b889-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9b889-228">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b889-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b889-229">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b889-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b889-230">System-Only</span></span>            | <span data-ttu-id="9b889-231">False</span><span class="sxs-lookup"><span data-stu-id="9b889-231">False</span></span>                                        |
| <span data-ttu-id="9b889-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9b889-232">Is-Single-Valued</span></span>       | <span data-ttu-id="9b889-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="9b889-233">True</span></span>                                         |
| <span data-ttu-id="9b889-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9b889-234">Is Indexed</span></span>             | <span data-ttu-id="9b889-235">False</span><span class="sxs-lookup"><span data-stu-id="9b889-235">False</span></span>                                        |
| <span data-ttu-id="9b889-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9b889-236">In Global Catalog</span></span>      | <span data-ttu-id="9b889-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="9b889-237">True</span></span>                                         |
| <span data-ttu-id="9b889-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9b889-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b889-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9b889-239">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9b889-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b889-240">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9b889-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b889-241">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9b889-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b889-242">Search-Flags</span></span>           | <span data-ttu-id="9b889-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b889-243">0x00000000</span></span>                                   |
| <span data-ttu-id="9b889-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b889-244">System-Flags</span></span>           | <span data-ttu-id="9b889-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b889-245">0x00000010</span></span>                                   |
| <span data-ttu-id="9b889-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9b889-246">Classes used in</span></span>        | [<span data-ttu-id="9b889-247">**MSMQ-Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="9b889-247">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





