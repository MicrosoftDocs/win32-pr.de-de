---
title: Unicode-Pwd-Attribut
description: Das Kennwort des Benutzers im unidirektionalen Windows NT-Format (owf). Windows 2000 verwendet Windows NT owf. Diese Eigenschaft wird nur vom Betriebssystem verwendet. Beachten Sie, dass Sie das eindeutige Kennwort nicht aus der OWF-Form des Kennworts ableiten können.
ms.assetid: 07b29a0c-aff2-4abd-8ca8-95f1ce5b566b
ms.tgt_platform: multiple
keywords:
- AD-Schema für Unicode-Pwd-Attribut
- unicodePwd-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Unicode-Pwd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d00a1df180b7a30b56bdf198a78edc77cc99755
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122642"
---
# <a name="unicode-pwd-attribute"></a><span data-ttu-id="2e97e-108">Unicode-Pwd-Attribut</span><span class="sxs-lookup"><span data-stu-id="2e97e-108">Unicode-Pwd attribute</span></span>

<span data-ttu-id="2e97e-109">Das Kennwort des Benutzers im unidirektionalen Windows NT-Format (owf).</span><span class="sxs-lookup"><span data-stu-id="2e97e-109">The password of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="2e97e-110">Windows 2000 verwendet Windows NT owf.</span><span class="sxs-lookup"><span data-stu-id="2e97e-110">Windows 2000 uses the Windows NT OWF.</span></span> <span data-ttu-id="2e97e-111">Diese Eigenschaft wird nur vom Betriebssystem verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e97e-111">This property is used only by the operating system.</span></span> <span data-ttu-id="2e97e-112">Beachten Sie, dass Sie das eindeutige Kennwort nicht aus der OWF-Form des Kennworts ableiten können.</span><span class="sxs-lookup"><span data-stu-id="2e97e-112">Note that you cannot derive the clear password back from the OWF form of the password.</span></span>



| <span data-ttu-id="2e97e-113">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2e97e-113">Entry</span></span> | <span data-ttu-id="2e97e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="2e97e-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="2e97e-115">CN</span><span class="sxs-lookup"><span data-stu-id="2e97e-115">CN</span></span>                | <span data-ttu-id="2e97e-116">Unicode-Pwd</span><span class="sxs-lookup"><span data-stu-id="2e97e-116">Unicode-Pwd</span></span>                                                                  |
| <span data-ttu-id="2e97e-117">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2e97e-117">Ldap-Display-Name</span></span> | <span data-ttu-id="2e97e-118">unicodePwd</span><span class="sxs-lookup"><span data-stu-id="2e97e-118">unicodePwd</span></span>                                                                   |
| <span data-ttu-id="2e97e-119">Size</span><span class="sxs-lookup"><span data-stu-id="2e97e-119">Size</span></span>              | \-                                                                           |
| <span data-ttu-id="2e97e-120">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2e97e-120">Update Privilege</span></span>  | <span data-ttu-id="2e97e-121">Domänen Administrator oder Konto Besitzer.</span><span class="sxs-lookup"><span data-stu-id="2e97e-121">Domain administrator or account owner.</span></span>                                       |
| <span data-ttu-id="2e97e-122">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="2e97e-122">Update Frequency</span></span>  | <span data-ttu-id="2e97e-123">Wenn der Benutzerdaten Satz erstellt wird und wenn das Kennwort geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="2e97e-123">When the user's record is created and whenever the password needs to change.</span></span> |
| <span data-ttu-id="2e97e-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2e97e-124">Attribute-Id</span></span>      | <span data-ttu-id="2e97e-125">1.2.840.113556.1.4.90</span><span class="sxs-lookup"><span data-stu-id="2e97e-125">1.2.840.113556.1.4.90</span></span>                                                        |
| <span data-ttu-id="2e97e-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2e97e-126">System-Id-Guid</span></span>    | <span data-ttu-id="2e97e-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2e97e-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span></span>                                         |
| <span data-ttu-id="2e97e-128">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e97e-128">Syntax</span></span>            | [<span data-ttu-id="2e97e-129">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="2e97e-129">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="2e97e-130">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="2e97e-130">Implementations</span></span>

-   [<span data-ttu-id="2e97e-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2e97e-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2e97e-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2e97e-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2e97e-133">**Adam**</span><span class="sxs-lookup"><span data-stu-id="2e97e-133">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2e97e-134">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2e97e-134">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2e97e-135">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2e97e-135">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2e97e-136">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2e97e-136">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2e97e-137">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2e97e-137">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2e97e-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e97e-138">Windows 2000 Server</span></span>



| <span data-ttu-id="2e97e-139">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2e97e-139">Entry</span></span> | <span data-ttu-id="2e97e-140">Wert</span><span class="sxs-lookup"><span data-stu-id="2e97e-140">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2e97e-141">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2e97e-141">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2e97e-142">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e97e-142">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2e97e-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e97e-143">System-Only</span></span>            | <span data-ttu-id="2e97e-144">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-144">False</span></span>                             |
| <span data-ttu-id="2e97e-145">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2e97e-145">Is-Single-Valued</span></span>       | <span data-ttu-id="2e97e-146">Richtig</span><span class="sxs-lookup"><span data-stu-id="2e97e-146">True</span></span>                              |
| <span data-ttu-id="2e97e-147">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2e97e-147">Is Indexed</span></span>             | <span data-ttu-id="2e97e-148">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-148">False</span></span>                             |
| <span data-ttu-id="2e97e-149">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2e97e-149">In Global Catalog</span></span>      | <span data-ttu-id="2e97e-150">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-150">False</span></span>                             |
| <span data-ttu-id="2e97e-151">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2e97e-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e97e-152">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2e97e-152">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2e97e-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e97e-153">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2e97e-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e97e-154">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2e97e-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e97e-155">Search-Flags</span></span>           | <span data-ttu-id="2e97e-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e97e-156">0x00000000</span></span>                        |
| <span data-ttu-id="2e97e-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e97e-157">System-Flags</span></span>           | <span data-ttu-id="2e97e-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e97e-158">0x00000010</span></span>                        |
| <span data-ttu-id="2e97e-159">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2e97e-159">Classes used in</span></span>        | [<span data-ttu-id="2e97e-160">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2e97e-160">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2e97e-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2e97e-161">Windows Server 2003</span></span>



| <span data-ttu-id="2e97e-162">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2e97e-162">Entry</span></span> | <span data-ttu-id="2e97e-163">Wert</span><span class="sxs-lookup"><span data-stu-id="2e97e-163">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2e97e-164">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2e97e-164">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2e97e-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e97e-165">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2e97e-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e97e-166">System-Only</span></span>            | <span data-ttu-id="2e97e-167">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-167">False</span></span>                             |
| <span data-ttu-id="2e97e-168">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2e97e-168">Is-Single-Valued</span></span>       | <span data-ttu-id="2e97e-169">Richtig</span><span class="sxs-lookup"><span data-stu-id="2e97e-169">True</span></span>                              |
| <span data-ttu-id="2e97e-170">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2e97e-170">Is Indexed</span></span>             | <span data-ttu-id="2e97e-171">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-171">False</span></span>                             |
| <span data-ttu-id="2e97e-172">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2e97e-172">In Global Catalog</span></span>      | <span data-ttu-id="2e97e-173">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-173">False</span></span>                             |
| <span data-ttu-id="2e97e-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2e97e-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e97e-175">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2e97e-175">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2e97e-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e97e-176">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2e97e-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e97e-177">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2e97e-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e97e-178">Search-Flags</span></span>           | <span data-ttu-id="2e97e-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e97e-179">0x00000000</span></span>                        |
| <span data-ttu-id="2e97e-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e97e-180">System-Flags</span></span>           | <span data-ttu-id="2e97e-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e97e-181">0x00000010</span></span>                        |
| <span data-ttu-id="2e97e-182">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2e97e-182">Classes used in</span></span>        | [<span data-ttu-id="2e97e-183">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2e97e-183">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2e97e-184">Adam</span><span class="sxs-lookup"><span data-stu-id="2e97e-184">ADAM</span></span>



| <span data-ttu-id="2e97e-185">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2e97e-185">Entry</span></span> | <span data-ttu-id="2e97e-186">Wert</span><span class="sxs-lookup"><span data-stu-id="2e97e-186">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2e97e-187">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2e97e-187">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2e97e-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e97e-188">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2e97e-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e97e-189">System-Only</span></span>            | <span data-ttu-id="2e97e-190">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-190">False</span></span>                                                             |
| <span data-ttu-id="2e97e-191">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2e97e-191">Is-Single-Valued</span></span>       | <span data-ttu-id="2e97e-192">Richtig</span><span class="sxs-lookup"><span data-stu-id="2e97e-192">True</span></span>                                                              |
| <span data-ttu-id="2e97e-193">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2e97e-193">Is Indexed</span></span>             | <span data-ttu-id="2e97e-194">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-194">False</span></span>                                                             |
| <span data-ttu-id="2e97e-195">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2e97e-195">In Global Catalog</span></span>      | <span data-ttu-id="2e97e-196">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-196">False</span></span>                                                             |
| <span data-ttu-id="2e97e-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2e97e-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e97e-198">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2e97e-198">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="2e97e-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e97e-199">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="2e97e-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e97e-200">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="2e97e-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e97e-201">Search-Flags</span></span>           | <span data-ttu-id="2e97e-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e97e-202">0x00000000</span></span>                                                        |
| <span data-ttu-id="2e97e-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e97e-203">System-Flags</span></span>           | <span data-ttu-id="2e97e-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e97e-204">0x00000010</span></span>                                                        |
| <span data-ttu-id="2e97e-205">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2e97e-205">Classes used in</span></span>        | [<span data-ttu-id="2e97e-206">**ms-DS-Bindable-Objekt**</span><span class="sxs-lookup"><span data-stu-id="2e97e-206">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2e97e-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2e97e-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2e97e-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2e97e-208">Entry</span></span> | <span data-ttu-id="2e97e-209">Wert</span><span class="sxs-lookup"><span data-stu-id="2e97e-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2e97e-210">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2e97e-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2e97e-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e97e-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2e97e-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e97e-212">System-Only</span></span>            | <span data-ttu-id="2e97e-213">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-213">False</span></span>                             |
| <span data-ttu-id="2e97e-214">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2e97e-214">Is-Single-Valued</span></span>       | <span data-ttu-id="2e97e-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="2e97e-215">True</span></span>                              |
| <span data-ttu-id="2e97e-216">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2e97e-216">Is Indexed</span></span>             | <span data-ttu-id="2e97e-217">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-217">False</span></span>                             |
| <span data-ttu-id="2e97e-218">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2e97e-218">In Global Catalog</span></span>      | <span data-ttu-id="2e97e-219">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-219">False</span></span>                             |
| <span data-ttu-id="2e97e-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2e97e-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e97e-221">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2e97e-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2e97e-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e97e-222">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2e97e-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e97e-223">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2e97e-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e97e-224">Search-Flags</span></span>           | <span data-ttu-id="2e97e-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e97e-225">0x00000000</span></span>                        |
| <span data-ttu-id="2e97e-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e97e-226">System-Flags</span></span>           | <span data-ttu-id="2e97e-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e97e-227">0x00000010</span></span>                        |
| <span data-ttu-id="2e97e-228">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2e97e-228">Classes used in</span></span>        | [<span data-ttu-id="2e97e-229">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2e97e-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2e97e-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e97e-230">Windows Server 2008</span></span>



| <span data-ttu-id="2e97e-231">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2e97e-231">Entry</span></span> | <span data-ttu-id="2e97e-232">Wert</span><span class="sxs-lookup"><span data-stu-id="2e97e-232">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2e97e-233">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2e97e-233">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2e97e-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e97e-234">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2e97e-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e97e-235">System-Only</span></span>            | <span data-ttu-id="2e97e-236">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-236">False</span></span>                             |
| <span data-ttu-id="2e97e-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2e97e-237">Is-Single-Valued</span></span>       | <span data-ttu-id="2e97e-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="2e97e-238">True</span></span>                              |
| <span data-ttu-id="2e97e-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2e97e-239">Is Indexed</span></span>             | <span data-ttu-id="2e97e-240">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-240">False</span></span>                             |
| <span data-ttu-id="2e97e-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2e97e-241">In Global Catalog</span></span>      | <span data-ttu-id="2e97e-242">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-242">False</span></span>                             |
| <span data-ttu-id="2e97e-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2e97e-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e97e-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2e97e-244">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2e97e-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e97e-245">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2e97e-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e97e-246">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2e97e-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e97e-247">Search-Flags</span></span>           | <span data-ttu-id="2e97e-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e97e-248">0x00000000</span></span>                        |
| <span data-ttu-id="2e97e-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e97e-249">System-Flags</span></span>           | <span data-ttu-id="2e97e-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e97e-250">0x00000010</span></span>                        |
| <span data-ttu-id="2e97e-251">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2e97e-251">Classes used in</span></span>        | [<span data-ttu-id="2e97e-252">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2e97e-252">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2e97e-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2e97e-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2e97e-254">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2e97e-254">Entry</span></span> | <span data-ttu-id="2e97e-255">Wert</span><span class="sxs-lookup"><span data-stu-id="2e97e-255">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2e97e-256">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2e97e-256">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2e97e-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e97e-257">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2e97e-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e97e-258">System-Only</span></span>            | <span data-ttu-id="2e97e-259">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-259">False</span></span>                             |
| <span data-ttu-id="2e97e-260">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2e97e-260">Is-Single-Valued</span></span>       | <span data-ttu-id="2e97e-261">Richtig</span><span class="sxs-lookup"><span data-stu-id="2e97e-261">True</span></span>                              |
| <span data-ttu-id="2e97e-262">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2e97e-262">Is Indexed</span></span>             | <span data-ttu-id="2e97e-263">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-263">False</span></span>                             |
| <span data-ttu-id="2e97e-264">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2e97e-264">In Global Catalog</span></span>      | <span data-ttu-id="2e97e-265">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-265">False</span></span>                             |
| <span data-ttu-id="2e97e-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2e97e-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e97e-267">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2e97e-267">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2e97e-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e97e-268">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2e97e-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e97e-269">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2e97e-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e97e-270">Search-Flags</span></span>           | <span data-ttu-id="2e97e-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e97e-271">0x00000000</span></span>                        |
| <span data-ttu-id="2e97e-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e97e-272">System-Flags</span></span>           | <span data-ttu-id="2e97e-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e97e-273">0x00000010</span></span>                        |
| <span data-ttu-id="2e97e-274">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2e97e-274">Classes used in</span></span>        | [<span data-ttu-id="2e97e-275">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2e97e-275">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2e97e-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e97e-276">Windows Server 2012</span></span>



| <span data-ttu-id="2e97e-277">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2e97e-277">Entry</span></span> | <span data-ttu-id="2e97e-278">Wert</span><span class="sxs-lookup"><span data-stu-id="2e97e-278">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2e97e-279">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2e97e-279">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2e97e-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e97e-280">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2e97e-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e97e-281">System-Only</span></span>            | <span data-ttu-id="2e97e-282">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-282">False</span></span>                             |
| <span data-ttu-id="2e97e-283">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2e97e-283">Is-Single-Valued</span></span>       | <span data-ttu-id="2e97e-284">Richtig</span><span class="sxs-lookup"><span data-stu-id="2e97e-284">True</span></span>                              |
| <span data-ttu-id="2e97e-285">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2e97e-285">Is Indexed</span></span>             | <span data-ttu-id="2e97e-286">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-286">False</span></span>                             |
| <span data-ttu-id="2e97e-287">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2e97e-287">In Global Catalog</span></span>      | <span data-ttu-id="2e97e-288">False</span><span class="sxs-lookup"><span data-stu-id="2e97e-288">False</span></span>                             |
| <span data-ttu-id="2e97e-289">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2e97e-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e97e-290">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2e97e-290">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2e97e-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e97e-291">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2e97e-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e97e-292">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2e97e-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e97e-293">Search-Flags</span></span>           | <span data-ttu-id="2e97e-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e97e-294">0x00000000</span></span>                        |
| <span data-ttu-id="2e97e-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e97e-295">System-Flags</span></span>           | <span data-ttu-id="2e97e-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e97e-296">0x00000010</span></span>                        |
| <span data-ttu-id="2e97e-297">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2e97e-297">Classes used in</span></span>        | [<span data-ttu-id="2e97e-298">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2e97e-298">**User**</span></span>](c-user.md)<br/> |



 

 





