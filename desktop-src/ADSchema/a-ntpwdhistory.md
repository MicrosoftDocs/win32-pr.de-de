---
title: NT-pwd-History-Attribut
description: Der Kenn Wort Verlauf des Benutzers im unidirektionalen Windows NT-Format (owf). Windows 2000 verwendet Windows NT owf.
ms.assetid: 7c6a0fe2-561e-43a2-af46-7505e7e13288
ms.tgt_platform: multiple
keywords:
- AD-Schema des NT-pwd-History-Attributs
- AD-Schema des ntpwdhistory-Attributs
topic_type:
- apiref
api_name:
- Nt-Pwd-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41ed3196109d13d4fb6cfae7e23be7ffdfb8c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104520063"
---
# <a name="nt-pwd-history-attribute"></a><span data-ttu-id="b6094-106">NT-pwd-History-Attribut</span><span class="sxs-lookup"><span data-stu-id="b6094-106">Nt-Pwd-History attribute</span></span>

<span data-ttu-id="b6094-107">Der Kenn Wort Verlauf des Benutzers im unidirektionalen Windows NT-Format (owf).</span><span class="sxs-lookup"><span data-stu-id="b6094-107">The password history of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="b6094-108">Windows 2000 verwendet Windows NT owf.</span><span class="sxs-lookup"><span data-stu-id="b6094-108">Windows 2000 uses the Windows NT OWF.</span></span>



| <span data-ttu-id="b6094-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6094-109">Entry</span></span> | <span data-ttu-id="b6094-110">Wert</span><span class="sxs-lookup"><span data-stu-id="b6094-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b6094-111">CN</span><span class="sxs-lookup"><span data-stu-id="b6094-111">CN</span></span>                | <span data-ttu-id="b6094-112">NT-pwd-Verlauf</span><span class="sxs-lookup"><span data-stu-id="b6094-112">Nt-Pwd-History</span></span>                                        |
| <span data-ttu-id="b6094-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b6094-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b6094-114">ntpwdhistory</span><span class="sxs-lookup"><span data-stu-id="b6094-114">ntPwdHistory</span></span>                                          |
| <span data-ttu-id="b6094-115">Size</span><span class="sxs-lookup"><span data-stu-id="b6094-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="b6094-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b6094-116">Update Privilege</span></span>  | <span data-ttu-id="b6094-117">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b6094-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="b6094-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b6094-118">Update Frequency</span></span>  | <span data-ttu-id="b6094-119">Jedes Mal, wenn der Benutzer Kenn Wörter ändert.</span><span class="sxs-lookup"><span data-stu-id="b6094-119">Each time the user changes passwords.</span></span>                 |
| <span data-ttu-id="b6094-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b6094-120">Attribute-Id</span></span>      | <span data-ttu-id="b6094-121">1.2.840.113556.1.4.94</span><span class="sxs-lookup"><span data-stu-id="b6094-121">1.2.840.113556.1.4.94</span></span>                                 |
| <span data-ttu-id="b6094-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b6094-122">System-Id-Guid</span></span>    | <span data-ttu-id="b6094-123">bf9679e2-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b6094-123">bf9679e2-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="b6094-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6094-124">Syntax</span></span>            | [<span data-ttu-id="b6094-125">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="b6094-125">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="b6094-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b6094-126">Implementations</span></span>

-   [<span data-ttu-id="b6094-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b6094-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b6094-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b6094-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b6094-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="b6094-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b6094-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b6094-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b6094-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b6094-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b6094-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b6094-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b6094-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b6094-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b6094-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b6094-134">Windows 2000 Server</span></span>



| <span data-ttu-id="b6094-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6094-135">Entry</span></span> | <span data-ttu-id="b6094-136">Wert</span><span class="sxs-lookup"><span data-stu-id="b6094-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b6094-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b6094-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b6094-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6094-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b6094-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6094-139">System-Only</span></span>            | <span data-ttu-id="b6094-140">False</span><span class="sxs-lookup"><span data-stu-id="b6094-140">False</span></span>                             |
| <span data-ttu-id="b6094-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b6094-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b6094-142">False</span><span class="sxs-lookup"><span data-stu-id="b6094-142">False</span></span>                             |
| <span data-ttu-id="b6094-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b6094-143">Is Indexed</span></span>             | <span data-ttu-id="b6094-144">False</span><span class="sxs-lookup"><span data-stu-id="b6094-144">False</span></span>                             |
| <span data-ttu-id="b6094-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b6094-145">In Global Catalog</span></span>      | <span data-ttu-id="b6094-146">False</span><span class="sxs-lookup"><span data-stu-id="b6094-146">False</span></span>                             |
| <span data-ttu-id="b6094-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b6094-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6094-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b6094-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b6094-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6094-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b6094-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6094-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b6094-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6094-151">Search-Flags</span></span>           | <span data-ttu-id="b6094-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6094-152">0x00000000</span></span>                        |
| <span data-ttu-id="b6094-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6094-153">System-Flags</span></span>           | <span data-ttu-id="b6094-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6094-154">0x00000010</span></span>                        |
| <span data-ttu-id="b6094-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b6094-155">Classes used in</span></span>        | [<span data-ttu-id="b6094-156">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b6094-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b6094-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b6094-157">Windows Server 2003</span></span>



| <span data-ttu-id="b6094-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6094-158">Entry</span></span> | <span data-ttu-id="b6094-159">Wert</span><span class="sxs-lookup"><span data-stu-id="b6094-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b6094-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b6094-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b6094-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6094-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b6094-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6094-162">System-Only</span></span>            | <span data-ttu-id="b6094-163">False</span><span class="sxs-lookup"><span data-stu-id="b6094-163">False</span></span>                             |
| <span data-ttu-id="b6094-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b6094-164">Is-Single-Valued</span></span>       | <span data-ttu-id="b6094-165">False</span><span class="sxs-lookup"><span data-stu-id="b6094-165">False</span></span>                             |
| <span data-ttu-id="b6094-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b6094-166">Is Indexed</span></span>             | <span data-ttu-id="b6094-167">False</span><span class="sxs-lookup"><span data-stu-id="b6094-167">False</span></span>                             |
| <span data-ttu-id="b6094-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b6094-168">In Global Catalog</span></span>      | <span data-ttu-id="b6094-169">False</span><span class="sxs-lookup"><span data-stu-id="b6094-169">False</span></span>                             |
| <span data-ttu-id="b6094-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b6094-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6094-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b6094-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b6094-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6094-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b6094-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6094-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b6094-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6094-174">Search-Flags</span></span>           | <span data-ttu-id="b6094-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6094-175">0x00000000</span></span>                        |
| <span data-ttu-id="b6094-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6094-176">System-Flags</span></span>           | <span data-ttu-id="b6094-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6094-177">0x00000010</span></span>                        |
| <span data-ttu-id="b6094-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b6094-178">Classes used in</span></span>        | [<span data-ttu-id="b6094-179">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b6094-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b6094-180">Adam</span><span class="sxs-lookup"><span data-stu-id="b6094-180">ADAM</span></span>



| <span data-ttu-id="b6094-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6094-181">Entry</span></span> | <span data-ttu-id="b6094-182">Wert</span><span class="sxs-lookup"><span data-stu-id="b6094-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="b6094-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b6094-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="b6094-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6094-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="b6094-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6094-185">System-Only</span></span>            | <span data-ttu-id="b6094-186">False</span><span class="sxs-lookup"><span data-stu-id="b6094-186">False</span></span>                                                             |
| <span data-ttu-id="b6094-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b6094-187">Is-Single-Valued</span></span>       | <span data-ttu-id="b6094-188">False</span><span class="sxs-lookup"><span data-stu-id="b6094-188">False</span></span>                                                             |
| <span data-ttu-id="b6094-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b6094-189">Is Indexed</span></span>             | <span data-ttu-id="b6094-190">False</span><span class="sxs-lookup"><span data-stu-id="b6094-190">False</span></span>                                                             |
| <span data-ttu-id="b6094-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b6094-191">In Global Catalog</span></span>      | <span data-ttu-id="b6094-192">False</span><span class="sxs-lookup"><span data-stu-id="b6094-192">False</span></span>                                                             |
| <span data-ttu-id="b6094-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b6094-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6094-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b6094-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="b6094-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6094-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="b6094-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6094-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="b6094-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6094-197">Search-Flags</span></span>           | <span data-ttu-id="b6094-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6094-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="b6094-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6094-199">System-Flags</span></span>           | <span data-ttu-id="b6094-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6094-200">0x00000010</span></span>                                                        |
| <span data-ttu-id="b6094-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b6094-201">Classes used in</span></span>        | [<span data-ttu-id="b6094-202">**ms-DS-Bindable-Objekt**</span><span class="sxs-lookup"><span data-stu-id="b6094-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b6094-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b6094-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b6094-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6094-204">Entry</span></span> | <span data-ttu-id="b6094-205">Wert</span><span class="sxs-lookup"><span data-stu-id="b6094-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b6094-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b6094-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b6094-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6094-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b6094-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6094-208">System-Only</span></span>            | <span data-ttu-id="b6094-209">False</span><span class="sxs-lookup"><span data-stu-id="b6094-209">False</span></span>                             |
| <span data-ttu-id="b6094-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b6094-210">Is-Single-Valued</span></span>       | <span data-ttu-id="b6094-211">False</span><span class="sxs-lookup"><span data-stu-id="b6094-211">False</span></span>                             |
| <span data-ttu-id="b6094-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b6094-212">Is Indexed</span></span>             | <span data-ttu-id="b6094-213">False</span><span class="sxs-lookup"><span data-stu-id="b6094-213">False</span></span>                             |
| <span data-ttu-id="b6094-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b6094-214">In Global Catalog</span></span>      | <span data-ttu-id="b6094-215">False</span><span class="sxs-lookup"><span data-stu-id="b6094-215">False</span></span>                             |
| <span data-ttu-id="b6094-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b6094-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6094-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b6094-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b6094-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6094-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b6094-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6094-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b6094-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6094-220">Search-Flags</span></span>           | <span data-ttu-id="b6094-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6094-221">0x00000000</span></span>                        |
| <span data-ttu-id="b6094-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6094-222">System-Flags</span></span>           | <span data-ttu-id="b6094-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6094-223">0x00000010</span></span>                        |
| <span data-ttu-id="b6094-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b6094-224">Classes used in</span></span>        | [<span data-ttu-id="b6094-225">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b6094-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b6094-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6094-226">Windows Server 2008</span></span>



| <span data-ttu-id="b6094-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6094-227">Entry</span></span> | <span data-ttu-id="b6094-228">Wert</span><span class="sxs-lookup"><span data-stu-id="b6094-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b6094-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b6094-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b6094-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6094-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b6094-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6094-231">System-Only</span></span>            | <span data-ttu-id="b6094-232">False</span><span class="sxs-lookup"><span data-stu-id="b6094-232">False</span></span>                             |
| <span data-ttu-id="b6094-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b6094-233">Is-Single-Valued</span></span>       | <span data-ttu-id="b6094-234">False</span><span class="sxs-lookup"><span data-stu-id="b6094-234">False</span></span>                             |
| <span data-ttu-id="b6094-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b6094-235">Is Indexed</span></span>             | <span data-ttu-id="b6094-236">False</span><span class="sxs-lookup"><span data-stu-id="b6094-236">False</span></span>                             |
| <span data-ttu-id="b6094-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b6094-237">In Global Catalog</span></span>      | <span data-ttu-id="b6094-238">False</span><span class="sxs-lookup"><span data-stu-id="b6094-238">False</span></span>                             |
| <span data-ttu-id="b6094-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b6094-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6094-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b6094-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b6094-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6094-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b6094-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6094-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b6094-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6094-243">Search-Flags</span></span>           | <span data-ttu-id="b6094-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6094-244">0x00000000</span></span>                        |
| <span data-ttu-id="b6094-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6094-245">System-Flags</span></span>           | <span data-ttu-id="b6094-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6094-246">0x00000010</span></span>                        |
| <span data-ttu-id="b6094-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b6094-247">Classes used in</span></span>        | [<span data-ttu-id="b6094-248">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b6094-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b6094-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b6094-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b6094-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6094-250">Entry</span></span> | <span data-ttu-id="b6094-251">Wert</span><span class="sxs-lookup"><span data-stu-id="b6094-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b6094-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b6094-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b6094-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6094-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b6094-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6094-254">System-Only</span></span>            | <span data-ttu-id="b6094-255">False</span><span class="sxs-lookup"><span data-stu-id="b6094-255">False</span></span>                             |
| <span data-ttu-id="b6094-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b6094-256">Is-Single-Valued</span></span>       | <span data-ttu-id="b6094-257">False</span><span class="sxs-lookup"><span data-stu-id="b6094-257">False</span></span>                             |
| <span data-ttu-id="b6094-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b6094-258">Is Indexed</span></span>             | <span data-ttu-id="b6094-259">False</span><span class="sxs-lookup"><span data-stu-id="b6094-259">False</span></span>                             |
| <span data-ttu-id="b6094-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b6094-260">In Global Catalog</span></span>      | <span data-ttu-id="b6094-261">False</span><span class="sxs-lookup"><span data-stu-id="b6094-261">False</span></span>                             |
| <span data-ttu-id="b6094-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b6094-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6094-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b6094-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b6094-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6094-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b6094-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6094-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b6094-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6094-266">Search-Flags</span></span>           | <span data-ttu-id="b6094-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6094-267">0x00000000</span></span>                        |
| <span data-ttu-id="b6094-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6094-268">System-Flags</span></span>           | <span data-ttu-id="b6094-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6094-269">0x00000010</span></span>                        |
| <span data-ttu-id="b6094-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b6094-270">Classes used in</span></span>        | [<span data-ttu-id="b6094-271">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b6094-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b6094-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b6094-272">Windows Server 2012</span></span>



| <span data-ttu-id="b6094-273">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6094-273">Entry</span></span> | <span data-ttu-id="b6094-274">Wert</span><span class="sxs-lookup"><span data-stu-id="b6094-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b6094-275">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b6094-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b6094-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6094-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b6094-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6094-277">System-Only</span></span>            | <span data-ttu-id="b6094-278">False</span><span class="sxs-lookup"><span data-stu-id="b6094-278">False</span></span>                             |
| <span data-ttu-id="b6094-279">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b6094-279">Is-Single-Valued</span></span>       | <span data-ttu-id="b6094-280">False</span><span class="sxs-lookup"><span data-stu-id="b6094-280">False</span></span>                             |
| <span data-ttu-id="b6094-281">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b6094-281">Is Indexed</span></span>             | <span data-ttu-id="b6094-282">False</span><span class="sxs-lookup"><span data-stu-id="b6094-282">False</span></span>                             |
| <span data-ttu-id="b6094-283">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b6094-283">In Global Catalog</span></span>      | <span data-ttu-id="b6094-284">False</span><span class="sxs-lookup"><span data-stu-id="b6094-284">False</span></span>                             |
| <span data-ttu-id="b6094-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b6094-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6094-286">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b6094-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b6094-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6094-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b6094-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6094-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b6094-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6094-289">Search-Flags</span></span>           | <span data-ttu-id="b6094-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6094-290">0x00000000</span></span>                        |
| <span data-ttu-id="b6094-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6094-291">System-Flags</span></span>           | <span data-ttu-id="b6094-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6094-292">0x00000010</span></span>                        |
| <span data-ttu-id="b6094-293">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b6094-293">Classes used in</span></span>        | [<span data-ttu-id="b6094-294">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b6094-294">**User**</span></span>](c-user.md)<br/> |



 

 





