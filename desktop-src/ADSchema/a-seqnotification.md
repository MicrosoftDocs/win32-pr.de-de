---
title: Seq-Notification-Attribut
description: Dieses Attribut enthält einen gegen Tag inkrementierten Wert. Dieser Leistungswert wird an den Link Überwachungsdienst übergeben, der den Wert seinen Volumes hinzufügt und Quelldateien verknüpft, wenn diese aktualisiert werden. Der Domänen Controller behält diesen Wert bei.
ms.assetid: 63fbded5-a21f-4a0e-aadc-568e199e8b9e
ms.tgt_platform: multiple
keywords:
- AD-Schema für Seq-Notification-Attribut
- seqnotification-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Seq-Notification
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31fc3abc61a8102ced02c87897d5e7a4f706dbbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107535"
---
# <a name="seq-notification-attribute"></a><span data-ttu-id="da029-107">Seq-Notification-Attribut</span><span class="sxs-lookup"><span data-stu-id="da029-107">Seq-Notification attribute</span></span>

<span data-ttu-id="da029-108">Dieses Attribut enthält einen gegen Tag inkrementierten Wert.</span><span class="sxs-lookup"><span data-stu-id="da029-108">This attribute contains a counter that is incremented daily.</span></span> <span data-ttu-id="da029-109">Dieser Leistungswert wird an den Link Überwachungsdienst übergeben, der den Wert seinen Volumes hinzufügt und Quelldateien verknüpft, wenn diese aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="da029-109">This counter value is given to the link tracking service which adds the value to its volumes and link source files when they are refreshed.</span></span> <span data-ttu-id="da029-110">Der Domänen Controller behält diesen Wert bei.</span><span class="sxs-lookup"><span data-stu-id="da029-110">The domain controller maintains this value.</span></span>



| <span data-ttu-id="da029-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da029-111">Entry</span></span> | <span data-ttu-id="da029-112">Wert</span><span class="sxs-lookup"><span data-stu-id="da029-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="da029-113">CN</span><span class="sxs-lookup"><span data-stu-id="da029-113">CN</span></span>                | <span data-ttu-id="da029-114">Seq-Notification</span><span class="sxs-lookup"><span data-stu-id="da029-114">Seq-Notification</span></span>                     |
| <span data-ttu-id="da029-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="da029-115">Ldap-Display-Name</span></span> | <span data-ttu-id="da029-116">"Abmeldung"</span><span class="sxs-lookup"><span data-stu-id="da029-116">seqNotification</span></span>                      |
| <span data-ttu-id="da029-117">Size</span><span class="sxs-lookup"><span data-stu-id="da029-117">Size</span></span>              | \-                                   |
| <span data-ttu-id="da029-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="da029-118">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="da029-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="da029-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="da029-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="da029-120">Attribute-Id</span></span>      | <span data-ttu-id="da029-121">1.2.840.113556.1.4.504</span><span class="sxs-lookup"><span data-stu-id="da029-121">1.2.840.113556.1.4.504</span></span>               |
| <span data-ttu-id="da029-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="da029-122">System-Id-Guid</span></span>    | <span data-ttu-id="da029-123">ddac0cf2-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="da029-123">ddac0cf2-af8f-11d0-afeb-00c04fd930c9</span></span> |
| <span data-ttu-id="da029-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="da029-124">Syntax</span></span>            | [<span data-ttu-id="da029-125">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="da029-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="da029-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="da029-126">Implementations</span></span>

-   [<span data-ttu-id="da029-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="da029-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="da029-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="da029-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="da029-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="da029-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="da029-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="da029-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="da029-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="da029-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="da029-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="da029-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="da029-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="da029-133">Windows 2000 Server</span></span>



| <span data-ttu-id="da029-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da029-134">Entry</span></span> | <span data-ttu-id="da029-135">Wert</span><span class="sxs-lookup"><span data-stu-id="da029-135">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="da029-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da029-136">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="da029-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da029-137">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="da029-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="da029-138">System-Only</span></span>            | <span data-ttu-id="da029-139">False</span><span class="sxs-lookup"><span data-stu-id="da029-139">False</span></span>                                                          |
| <span data-ttu-id="da029-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da029-140">Is-Single-Valued</span></span>       | <span data-ttu-id="da029-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="da029-141">True</span></span>                                                           |
| <span data-ttu-id="da029-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da029-142">Is Indexed</span></span>             | <span data-ttu-id="da029-143">False</span><span class="sxs-lookup"><span data-stu-id="da029-143">False</span></span>                                                          |
| <span data-ttu-id="da029-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da029-144">In Global Catalog</span></span>      | <span data-ttu-id="da029-145">False</span><span class="sxs-lookup"><span data-stu-id="da029-145">False</span></span>                                                          |
| <span data-ttu-id="da029-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da029-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="da029-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da029-147">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="da029-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da029-148">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="da029-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da029-149">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="da029-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da029-150">Search-Flags</span></span>           | <span data-ttu-id="da029-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da029-151">0x00000000</span></span>                                                     |
| <span data-ttu-id="da029-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da029-152">System-Flags</span></span>           | <span data-ttu-id="da029-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da029-153">0x00000010</span></span>                                                     |
| <span data-ttu-id="da029-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da029-154">Classes used in</span></span>        | [<span data-ttu-id="da029-155">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="da029-155">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="da029-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="da029-156">Windows Server 2003</span></span>



| <span data-ttu-id="da029-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da029-157">Entry</span></span> | <span data-ttu-id="da029-158">Wert</span><span class="sxs-lookup"><span data-stu-id="da029-158">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="da029-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da029-159">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="da029-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da029-160">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="da029-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="da029-161">System-Only</span></span>            | <span data-ttu-id="da029-162">False</span><span class="sxs-lookup"><span data-stu-id="da029-162">False</span></span>                                                          |
| <span data-ttu-id="da029-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da029-163">Is-Single-Valued</span></span>       | <span data-ttu-id="da029-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="da029-164">True</span></span>                                                           |
| <span data-ttu-id="da029-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da029-165">Is Indexed</span></span>             | <span data-ttu-id="da029-166">False</span><span class="sxs-lookup"><span data-stu-id="da029-166">False</span></span>                                                          |
| <span data-ttu-id="da029-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da029-167">In Global Catalog</span></span>      | <span data-ttu-id="da029-168">False</span><span class="sxs-lookup"><span data-stu-id="da029-168">False</span></span>                                                          |
| <span data-ttu-id="da029-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da029-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="da029-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da029-170">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="da029-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da029-171">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="da029-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da029-172">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="da029-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da029-173">Search-Flags</span></span>           | <span data-ttu-id="da029-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da029-174">0x00000000</span></span>                                                     |
| <span data-ttu-id="da029-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da029-175">System-Flags</span></span>           | <span data-ttu-id="da029-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da029-176">0x00000010</span></span>                                                     |
| <span data-ttu-id="da029-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da029-177">Classes used in</span></span>        | [<span data-ttu-id="da029-178">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="da029-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="da029-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="da029-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="da029-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da029-180">Entry</span></span> | <span data-ttu-id="da029-181">Wert</span><span class="sxs-lookup"><span data-stu-id="da029-181">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="da029-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da029-182">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="da029-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da029-183">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="da029-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="da029-184">System-Only</span></span>            | <span data-ttu-id="da029-185">False</span><span class="sxs-lookup"><span data-stu-id="da029-185">False</span></span>                                                          |
| <span data-ttu-id="da029-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da029-186">Is-Single-Valued</span></span>       | <span data-ttu-id="da029-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="da029-187">True</span></span>                                                           |
| <span data-ttu-id="da029-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da029-188">Is Indexed</span></span>             | <span data-ttu-id="da029-189">False</span><span class="sxs-lookup"><span data-stu-id="da029-189">False</span></span>                                                          |
| <span data-ttu-id="da029-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da029-190">In Global Catalog</span></span>      | <span data-ttu-id="da029-191">False</span><span class="sxs-lookup"><span data-stu-id="da029-191">False</span></span>                                                          |
| <span data-ttu-id="da029-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da029-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="da029-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da029-193">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="da029-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da029-194">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="da029-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da029-195">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="da029-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da029-196">Search-Flags</span></span>           | <span data-ttu-id="da029-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da029-197">0x00000000</span></span>                                                     |
| <span data-ttu-id="da029-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da029-198">System-Flags</span></span>           | <span data-ttu-id="da029-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da029-199">0x00000010</span></span>                                                     |
| <span data-ttu-id="da029-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da029-200">Classes used in</span></span>        | [<span data-ttu-id="da029-201">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="da029-201">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="da029-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da029-202">Windows Server 2008</span></span>



| <span data-ttu-id="da029-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da029-203">Entry</span></span> | <span data-ttu-id="da029-204">Wert</span><span class="sxs-lookup"><span data-stu-id="da029-204">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="da029-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da029-205">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="da029-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da029-206">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="da029-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="da029-207">System-Only</span></span>            | <span data-ttu-id="da029-208">False</span><span class="sxs-lookup"><span data-stu-id="da029-208">False</span></span>                                                          |
| <span data-ttu-id="da029-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da029-209">Is-Single-Valued</span></span>       | <span data-ttu-id="da029-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="da029-210">True</span></span>                                                           |
| <span data-ttu-id="da029-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da029-211">Is Indexed</span></span>             | <span data-ttu-id="da029-212">False</span><span class="sxs-lookup"><span data-stu-id="da029-212">False</span></span>                                                          |
| <span data-ttu-id="da029-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da029-213">In Global Catalog</span></span>      | <span data-ttu-id="da029-214">False</span><span class="sxs-lookup"><span data-stu-id="da029-214">False</span></span>                                                          |
| <span data-ttu-id="da029-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da029-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="da029-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da029-216">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="da029-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da029-217">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="da029-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da029-218">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="da029-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da029-219">Search-Flags</span></span>           | <span data-ttu-id="da029-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da029-220">0x00000000</span></span>                                                     |
| <span data-ttu-id="da029-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da029-221">System-Flags</span></span>           | <span data-ttu-id="da029-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da029-222">0x00000010</span></span>                                                     |
| <span data-ttu-id="da029-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da029-223">Classes used in</span></span>        | [<span data-ttu-id="da029-224">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="da029-224">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="da029-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="da029-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="da029-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da029-226">Entry</span></span> | <span data-ttu-id="da029-227">Wert</span><span class="sxs-lookup"><span data-stu-id="da029-227">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="da029-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da029-228">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="da029-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da029-229">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="da029-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="da029-230">System-Only</span></span>            | <span data-ttu-id="da029-231">False</span><span class="sxs-lookup"><span data-stu-id="da029-231">False</span></span>                                                          |
| <span data-ttu-id="da029-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da029-232">Is-Single-Valued</span></span>       | <span data-ttu-id="da029-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="da029-233">True</span></span>                                                           |
| <span data-ttu-id="da029-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da029-234">Is Indexed</span></span>             | <span data-ttu-id="da029-235">False</span><span class="sxs-lookup"><span data-stu-id="da029-235">False</span></span>                                                          |
| <span data-ttu-id="da029-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da029-236">In Global Catalog</span></span>      | <span data-ttu-id="da029-237">False</span><span class="sxs-lookup"><span data-stu-id="da029-237">False</span></span>                                                          |
| <span data-ttu-id="da029-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da029-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="da029-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da029-239">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="da029-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da029-240">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="da029-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da029-241">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="da029-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da029-242">Search-Flags</span></span>           | <span data-ttu-id="da029-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da029-243">0x00000000</span></span>                                                     |
| <span data-ttu-id="da029-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da029-244">System-Flags</span></span>           | <span data-ttu-id="da029-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da029-245">0x00000010</span></span>                                                     |
| <span data-ttu-id="da029-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da029-246">Classes used in</span></span>        | [<span data-ttu-id="da029-247">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="da029-247">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="da029-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="da029-248">Windows Server 2012</span></span>



| <span data-ttu-id="da029-249">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da029-249">Entry</span></span> | <span data-ttu-id="da029-250">Wert</span><span class="sxs-lookup"><span data-stu-id="da029-250">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="da029-251">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da029-251">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="da029-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da029-252">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="da029-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="da029-253">System-Only</span></span>            | <span data-ttu-id="da029-254">False</span><span class="sxs-lookup"><span data-stu-id="da029-254">False</span></span>                                                          |
| <span data-ttu-id="da029-255">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da029-255">Is-Single-Valued</span></span>       | <span data-ttu-id="da029-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="da029-256">True</span></span>                                                           |
| <span data-ttu-id="da029-257">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da029-257">Is Indexed</span></span>             | <span data-ttu-id="da029-258">False</span><span class="sxs-lookup"><span data-stu-id="da029-258">False</span></span>                                                          |
| <span data-ttu-id="da029-259">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da029-259">In Global Catalog</span></span>      | <span data-ttu-id="da029-260">False</span><span class="sxs-lookup"><span data-stu-id="da029-260">False</span></span>                                                          |
| <span data-ttu-id="da029-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da029-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="da029-262">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da029-262">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="da029-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da029-263">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="da029-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da029-264">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="da029-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da029-265">Search-Flags</span></span>           | <span data-ttu-id="da029-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da029-266">0x00000000</span></span>                                                     |
| <span data-ttu-id="da029-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da029-267">System-Flags</span></span>           | <span data-ttu-id="da029-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da029-268">0x00000010</span></span>                                                     |
| <span data-ttu-id="da029-269">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da029-269">Classes used in</span></span>        | [<span data-ttu-id="da029-270">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="da029-270">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





