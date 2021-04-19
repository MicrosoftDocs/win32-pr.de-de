---
title: Lockout-Time-Attribut
description: Das Datum und die Uhrzeit (UTC), an denen dieses Konto gesperrt wurde.
ms.assetid: 4a0a66a3-9f7f-48ec-9b96-a9c3e72b2b6b
ms.tgt_platform: multiple
keywords:
- AD-Schema für Lockout-Time-Attribut
- AD-Schema des lockoutTime-Attributs
topic_type:
- apiref
api_name:
- Lockout-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adebe8bf76ba04fe4ba774726da7cd5c54e64ab1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342913"
---
# <a name="lockout-time-attribute"></a><span data-ttu-id="30378-105">Lockout-Time-Attribut</span><span class="sxs-lookup"><span data-stu-id="30378-105">Lockout-Time attribute</span></span>

<span data-ttu-id="30378-106">Das Datum und die Uhrzeit (UTC), an denen dieses Konto gesperrt wurde. Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601 (UTC) darstellt.</span><span class="sxs-lookup"><span data-stu-id="30378-106">The date and time (UTC) that this account was locked out. This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="30378-107">Der Wert 0 (null) bedeutet, dass das Konto zurzeit nicht gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="30378-107">A value of zero means that the account is not currently locked out.</span></span>



| <span data-ttu-id="30378-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="30378-108">Entry</span></span> | <span data-ttu-id="30378-109">Wert</span><span class="sxs-lookup"><span data-stu-id="30378-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="30378-110">CN</span><span class="sxs-lookup"><span data-stu-id="30378-110">CN</span></span>                | <span data-ttu-id="30378-111">Lockout-Time</span><span class="sxs-lookup"><span data-stu-id="30378-111">Lockout-Time</span></span>                                                                     |
| <span data-ttu-id="30378-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="30378-112">Ldap-Display-Name</span></span> | <span data-ttu-id="30378-113">lockoutTime</span><span class="sxs-lookup"><span data-stu-id="30378-113">lockoutTime</span></span>                                                                      |
| <span data-ttu-id="30378-114">Size</span><span class="sxs-lookup"><span data-stu-id="30378-114">Size</span></span>              | <span data-ttu-id="30378-115">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="30378-115">8 bytes</span></span>                                                                          |
| <span data-ttu-id="30378-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="30378-116">Update Privilege</span></span>  | <span data-ttu-id="30378-117">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="30378-117">Domain administrator</span></span>                                                             |
| <span data-ttu-id="30378-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="30378-118">Update Frequency</span></span>  | <span data-ttu-id="30378-119">Wenn der Benutzerdaten Satz erstellt wird und die Sperr Zeit geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="30378-119">When the user's record is created and whenever the lockout time needs to change.</span></span> |
| <span data-ttu-id="30378-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="30378-120">Attribute-Id</span></span>      | <span data-ttu-id="30378-121">1.2.840.113556.1.4.662</span><span class="sxs-lookup"><span data-stu-id="30378-121">1.2.840.113556.1.4.662</span></span>                                                           |
| <span data-ttu-id="30378-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="30378-122">System-Id-Guid</span></span>    | <span data-ttu-id="30378-123">28630ebf -41d5-11d1-a9c1-0000 C1</span><span class="sxs-lookup"><span data-stu-id="30378-123">28630ebf-41d5-11d1-a9c1-0000f80367c1</span></span>                                             |
| <span data-ttu-id="30378-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="30378-124">Syntax</span></span>            | [<span data-ttu-id="30378-125">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="30378-125">**Interval**</span></span>](s-interval.md)                                                   |



## <a name="implementations"></a><span data-ttu-id="30378-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="30378-126">Implementations</span></span>

-   [<span data-ttu-id="30378-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="30378-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="30378-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="30378-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="30378-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="30378-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="30378-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="30378-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="30378-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="30378-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="30378-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="30378-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="30378-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="30378-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="30378-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="30378-134">Windows 2000 Server</span></span>



| <span data-ttu-id="30378-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="30378-135">Entry</span></span> | <span data-ttu-id="30378-136">Wert</span><span class="sxs-lookup"><span data-stu-id="30378-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="30378-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="30378-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="30378-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30378-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="30378-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="30378-139">System-Only</span></span>            | <span data-ttu-id="30378-140">False</span><span class="sxs-lookup"><span data-stu-id="30378-140">False</span></span>                             |
| <span data-ttu-id="30378-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="30378-141">Is-Single-Valued</span></span>       | <span data-ttu-id="30378-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="30378-142">True</span></span>                              |
| <span data-ttu-id="30378-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="30378-143">Is Indexed</span></span>             | <span data-ttu-id="30378-144">False</span><span class="sxs-lookup"><span data-stu-id="30378-144">False</span></span>                             |
| <span data-ttu-id="30378-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="30378-145">In Global Catalog</span></span>      | <span data-ttu-id="30378-146">False</span><span class="sxs-lookup"><span data-stu-id="30378-146">False</span></span>                             |
| <span data-ttu-id="30378-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="30378-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="30378-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="30378-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="30378-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30378-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="30378-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30378-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="30378-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30378-151">Search-Flags</span></span>           | <span data-ttu-id="30378-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30378-152">0x00000000</span></span>                        |
| <span data-ttu-id="30378-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30378-153">System-Flags</span></span>           | <span data-ttu-id="30378-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30378-154">0x00000010</span></span>                        |
| <span data-ttu-id="30378-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="30378-155">Classes used in</span></span>        | [<span data-ttu-id="30378-156">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="30378-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="30378-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="30378-157">Windows Server 2003</span></span>



| <span data-ttu-id="30378-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="30378-158">Entry</span></span> | <span data-ttu-id="30378-159">Wert</span><span class="sxs-lookup"><span data-stu-id="30378-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="30378-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="30378-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="30378-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30378-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="30378-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="30378-162">System-Only</span></span>            | <span data-ttu-id="30378-163">False</span><span class="sxs-lookup"><span data-stu-id="30378-163">False</span></span>                             |
| <span data-ttu-id="30378-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="30378-164">Is-Single-Valued</span></span>       | <span data-ttu-id="30378-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="30378-165">True</span></span>                              |
| <span data-ttu-id="30378-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="30378-166">Is Indexed</span></span>             | <span data-ttu-id="30378-167">False</span><span class="sxs-lookup"><span data-stu-id="30378-167">False</span></span>                             |
| <span data-ttu-id="30378-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="30378-168">In Global Catalog</span></span>      | <span data-ttu-id="30378-169">False</span><span class="sxs-lookup"><span data-stu-id="30378-169">False</span></span>                             |
| <span data-ttu-id="30378-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="30378-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="30378-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="30378-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="30378-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30378-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="30378-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30378-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="30378-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30378-174">Search-Flags</span></span>           | <span data-ttu-id="30378-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30378-175">0x00000000</span></span>                        |
| <span data-ttu-id="30378-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30378-176">System-Flags</span></span>           | <span data-ttu-id="30378-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30378-177">0x00000010</span></span>                        |
| <span data-ttu-id="30378-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="30378-178">Classes used in</span></span>        | [<span data-ttu-id="30378-179">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="30378-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="30378-180">Adam</span><span class="sxs-lookup"><span data-stu-id="30378-180">ADAM</span></span>



| <span data-ttu-id="30378-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="30378-181">Entry</span></span> | <span data-ttu-id="30378-182">Wert</span><span class="sxs-lookup"><span data-stu-id="30378-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="30378-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="30378-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="30378-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30378-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="30378-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="30378-185">System-Only</span></span>            | <span data-ttu-id="30378-186">False</span><span class="sxs-lookup"><span data-stu-id="30378-186">False</span></span>                                                             |
| <span data-ttu-id="30378-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="30378-187">Is-Single-Valued</span></span>       | <span data-ttu-id="30378-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="30378-188">True</span></span>                                                              |
| <span data-ttu-id="30378-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="30378-189">Is Indexed</span></span>             | <span data-ttu-id="30378-190">False</span><span class="sxs-lookup"><span data-stu-id="30378-190">False</span></span>                                                             |
| <span data-ttu-id="30378-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="30378-191">In Global Catalog</span></span>      | <span data-ttu-id="30378-192">False</span><span class="sxs-lookup"><span data-stu-id="30378-192">False</span></span>                                                             |
| <span data-ttu-id="30378-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="30378-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="30378-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="30378-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="30378-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30378-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="30378-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30378-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="30378-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30378-197">Search-Flags</span></span>           | <span data-ttu-id="30378-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30378-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="30378-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30378-199">System-Flags</span></span>           | <span data-ttu-id="30378-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30378-200">0x00000010</span></span>                                                        |
| <span data-ttu-id="30378-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="30378-201">Classes used in</span></span>        | [<span data-ttu-id="30378-202">**ms-DS-Bindable-Objekt**</span><span class="sxs-lookup"><span data-stu-id="30378-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="30378-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="30378-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="30378-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="30378-204">Entry</span></span> | <span data-ttu-id="30378-205">Wert</span><span class="sxs-lookup"><span data-stu-id="30378-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="30378-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="30378-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="30378-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30378-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="30378-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="30378-208">System-Only</span></span>            | <span data-ttu-id="30378-209">False</span><span class="sxs-lookup"><span data-stu-id="30378-209">False</span></span>                             |
| <span data-ttu-id="30378-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="30378-210">Is-Single-Valued</span></span>       | <span data-ttu-id="30378-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="30378-211">True</span></span>                              |
| <span data-ttu-id="30378-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="30378-212">Is Indexed</span></span>             | <span data-ttu-id="30378-213">False</span><span class="sxs-lookup"><span data-stu-id="30378-213">False</span></span>                             |
| <span data-ttu-id="30378-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="30378-214">In Global Catalog</span></span>      | <span data-ttu-id="30378-215">False</span><span class="sxs-lookup"><span data-stu-id="30378-215">False</span></span>                             |
| <span data-ttu-id="30378-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="30378-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="30378-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="30378-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="30378-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30378-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="30378-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30378-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="30378-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30378-220">Search-Flags</span></span>           | <span data-ttu-id="30378-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30378-221">0x00000000</span></span>                        |
| <span data-ttu-id="30378-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30378-222">System-Flags</span></span>           | <span data-ttu-id="30378-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30378-223">0x00000010</span></span>                        |
| <span data-ttu-id="30378-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="30378-224">Classes used in</span></span>        | [<span data-ttu-id="30378-225">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="30378-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="30378-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30378-226">Windows Server 2008</span></span>



| <span data-ttu-id="30378-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="30378-227">Entry</span></span> | <span data-ttu-id="30378-228">Wert</span><span class="sxs-lookup"><span data-stu-id="30378-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="30378-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="30378-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="30378-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30378-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="30378-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="30378-231">System-Only</span></span>            | <span data-ttu-id="30378-232">False</span><span class="sxs-lookup"><span data-stu-id="30378-232">False</span></span>                             |
| <span data-ttu-id="30378-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="30378-233">Is-Single-Valued</span></span>       | <span data-ttu-id="30378-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="30378-234">True</span></span>                              |
| <span data-ttu-id="30378-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="30378-235">Is Indexed</span></span>             | <span data-ttu-id="30378-236">False</span><span class="sxs-lookup"><span data-stu-id="30378-236">False</span></span>                             |
| <span data-ttu-id="30378-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="30378-237">In Global Catalog</span></span>      | <span data-ttu-id="30378-238">False</span><span class="sxs-lookup"><span data-stu-id="30378-238">False</span></span>                             |
| <span data-ttu-id="30378-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="30378-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="30378-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="30378-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="30378-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30378-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="30378-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30378-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="30378-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30378-243">Search-Flags</span></span>           | <span data-ttu-id="30378-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30378-244">0x00000000</span></span>                        |
| <span data-ttu-id="30378-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30378-245">System-Flags</span></span>           | <span data-ttu-id="30378-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30378-246">0x00000010</span></span>                        |
| <span data-ttu-id="30378-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="30378-247">Classes used in</span></span>        | [<span data-ttu-id="30378-248">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="30378-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="30378-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="30378-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="30378-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="30378-250">Entry</span></span> | <span data-ttu-id="30378-251">Wert</span><span class="sxs-lookup"><span data-stu-id="30378-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="30378-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="30378-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="30378-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30378-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="30378-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="30378-254">System-Only</span></span>            | <span data-ttu-id="30378-255">False</span><span class="sxs-lookup"><span data-stu-id="30378-255">False</span></span>                             |
| <span data-ttu-id="30378-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="30378-256">Is-Single-Valued</span></span>       | <span data-ttu-id="30378-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="30378-257">True</span></span>                              |
| <span data-ttu-id="30378-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="30378-258">Is Indexed</span></span>             | <span data-ttu-id="30378-259">False</span><span class="sxs-lookup"><span data-stu-id="30378-259">False</span></span>                             |
| <span data-ttu-id="30378-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="30378-260">In Global Catalog</span></span>      | <span data-ttu-id="30378-261">False</span><span class="sxs-lookup"><span data-stu-id="30378-261">False</span></span>                             |
| <span data-ttu-id="30378-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="30378-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="30378-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="30378-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="30378-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30378-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="30378-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30378-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="30378-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30378-266">Search-Flags</span></span>           | <span data-ttu-id="30378-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30378-267">0x00000000</span></span>                        |
| <span data-ttu-id="30378-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30378-268">System-Flags</span></span>           | <span data-ttu-id="30378-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30378-269">0x00000010</span></span>                        |
| <span data-ttu-id="30378-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="30378-270">Classes used in</span></span>        | [<span data-ttu-id="30378-271">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="30378-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="30378-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="30378-272">Windows Server 2012</span></span>



| <span data-ttu-id="30378-273">Eingabe</span><span class="sxs-lookup"><span data-stu-id="30378-273">Entry</span></span> | <span data-ttu-id="30378-274">Wert</span><span class="sxs-lookup"><span data-stu-id="30378-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="30378-275">Link-ID</span><span class="sxs-lookup"><span data-stu-id="30378-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="30378-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30378-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="30378-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="30378-277">System-Only</span></span>            | <span data-ttu-id="30378-278">False</span><span class="sxs-lookup"><span data-stu-id="30378-278">False</span></span>                             |
| <span data-ttu-id="30378-279">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="30378-279">Is-Single-Valued</span></span>       | <span data-ttu-id="30378-280">Richtig</span><span class="sxs-lookup"><span data-stu-id="30378-280">True</span></span>                              |
| <span data-ttu-id="30378-281">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="30378-281">Is Indexed</span></span>             | <span data-ttu-id="30378-282">False</span><span class="sxs-lookup"><span data-stu-id="30378-282">False</span></span>                             |
| <span data-ttu-id="30378-283">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="30378-283">In Global Catalog</span></span>      | <span data-ttu-id="30378-284">False</span><span class="sxs-lookup"><span data-stu-id="30378-284">False</span></span>                             |
| <span data-ttu-id="30378-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="30378-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="30378-286">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="30378-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="30378-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30378-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="30378-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30378-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="30378-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30378-289">Search-Flags</span></span>           | <span data-ttu-id="30378-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30378-290">0x00000000</span></span>                        |
| <span data-ttu-id="30378-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30378-291">System-Flags</span></span>           | <span data-ttu-id="30378-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30378-292">0x00000010</span></span>                        |
| <span data-ttu-id="30378-293">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="30378-293">Classes used in</span></span>        | [<span data-ttu-id="30378-294">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="30378-294">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="30378-295">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30378-295">Remarks</span></span>

<span data-ttu-id="30378-296">Der hohe Teil dieser großen Ganzzahl entspricht dem **dwHighDateTime** -Member der [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Struktur, und der niedrige Teil entspricht dem **dwLowDateTime** -Member der **FILETIME** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="30378-296">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="30378-297">Dieser Attribut Wert wird nur zurückgesetzt, wenn das Konto erfolgreich bei angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="30378-297">This attribute value is only reset when the account is logged onto successfully.</span></span> <span data-ttu-id="30378-298">Dies bedeutet, dass dieser Wert möglicherweise nicht NULL ist, aber das Konto nicht gesperrt ist. Um genau festzustellen, ob das Konto gesperrt ist, müssen Sie dieser Zeit die [**Lockout-Dauer**](a-lockoutduration.md) hinzufügen und das Ergebnis mit der aktuellen Zeit vergleichen, wobei lokale Zeitzonen und Sommerzeit berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="30378-298">This means that this value may be non zero, yet the account is not locked out. To accurately determine if the account is locked out, you must add the [**Lockout-Duration**](a-lockoutduration.md) to this time and compare the result to the current time, accounting for local time zones and daylight savings time.</span></span>

## <a name="see-also"></a><span data-ttu-id="30378-299">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30378-299">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30378-300">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="30378-300">**FILETIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[<span data-ttu-id="30378-301">**Sperr Dauer**</span><span class="sxs-lookup"><span data-stu-id="30378-301">**Lockout-Duration**</span></span>](a-lockoutduration.md)
</dt> </dl>

 

