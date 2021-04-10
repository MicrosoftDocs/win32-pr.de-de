---
title: Logon-Count-Attribut
description: Gibt an, wie oft sich das Konto erfolgreich angemeldet hat. Der Wert 0 gibt an, dass der Wert unbekannt ist.
ms.assetid: 8b12bea7-dfc3-46e3-a4a2-92b5f1239b98
ms.tgt_platform: multiple
keywords:
- AD-Schema für Logon-Count-Attribut
- LogonCount-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Logon-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ba7865cb3b90f42ede71b169f98f8ce45e722d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859721"
---
# <a name="logon-count-attribute"></a><span data-ttu-id="c0ef2-106">Logon-Count-Attribut</span><span class="sxs-lookup"><span data-stu-id="c0ef2-106">Logon-Count attribute</span></span>

<span data-ttu-id="c0ef2-107">Gibt an, wie oft sich das Konto erfolgreich angemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="c0ef2-107">The number of times the account has successfully logged on.</span></span> <span data-ttu-id="c0ef2-108">Der Wert 0 gibt an, dass der Wert unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="c0ef2-108">A value of 0 indicates that the value is unknown.</span></span>



| <span data-ttu-id="c0ef2-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c0ef2-109">Entry</span></span> | <span data-ttu-id="c0ef2-110">Wert</span><span class="sxs-lookup"><span data-stu-id="c0ef2-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c0ef2-111">CN</span><span class="sxs-lookup"><span data-stu-id="c0ef2-111">CN</span></span>                | <span data-ttu-id="c0ef2-112">Logon-Count</span><span class="sxs-lookup"><span data-stu-id="c0ef2-112">Logon-Count</span></span>                          |
| <span data-ttu-id="c0ef2-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c0ef2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c0ef2-114">LogonCount</span><span class="sxs-lookup"><span data-stu-id="c0ef2-114">logonCount</span></span>                           |
| <span data-ttu-id="c0ef2-115">Size</span><span class="sxs-lookup"><span data-stu-id="c0ef2-115">Size</span></span>              | <span data-ttu-id="c0ef2-116">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="c0ef2-116">4 bytes</span></span>                              |
| <span data-ttu-id="c0ef2-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c0ef2-117">Update Privilege</span></span>  | <span data-ttu-id="c0ef2-118">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="c0ef2-118">Domain administrator</span></span>                 |
| <span data-ttu-id="c0ef2-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="c0ef2-119">Update Frequency</span></span>  | <span data-ttu-id="c0ef2-120">Jedes Mal, wenn sich der Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="c0ef2-120">Each time the user logs on.</span></span>          |
| <span data-ttu-id="c0ef2-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c0ef2-121">Attribute-Id</span></span>      | <span data-ttu-id="c0ef2-122">1.2.840.113556.1.4.169</span><span class="sxs-lookup"><span data-stu-id="c0ef2-122">1.2.840.113556.1.4.169</span></span>               |
| <span data-ttu-id="c0ef2-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c0ef2-123">System-Id-Guid</span></span>    | <span data-ttu-id="c0ef2-124">bf9679aa-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c0ef2-124">bf9679aa-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="c0ef2-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0ef2-125">Syntax</span></span>            | [<span data-ttu-id="c0ef2-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="c0ef2-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="c0ef2-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="c0ef2-127">Implementations</span></span>

-   [<span data-ttu-id="c0ef2-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c0ef2-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c0ef2-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c0ef2-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c0ef2-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c0ef2-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c0ef2-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c0ef2-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c0ef2-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c0ef2-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c0ef2-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c0ef2-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c0ef2-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c0ef2-134">Windows 2000 Server</span></span>



| <span data-ttu-id="c0ef2-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c0ef2-135">Entry</span></span> | <span data-ttu-id="c0ef2-136">Wert</span><span class="sxs-lookup"><span data-stu-id="c0ef2-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c0ef2-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c0ef2-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c0ef2-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0ef2-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c0ef2-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0ef2-139">System-Only</span></span>            | <span data-ttu-id="c0ef2-140">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-140">False</span></span>                             |
| <span data-ttu-id="c0ef2-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c0ef2-141">Is-Single-Valued</span></span>       | <span data-ttu-id="c0ef2-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="c0ef2-142">True</span></span>                              |
| <span data-ttu-id="c0ef2-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c0ef2-143">Is Indexed</span></span>             | <span data-ttu-id="c0ef2-144">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-144">False</span></span>                             |
| <span data-ttu-id="c0ef2-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c0ef2-145">In Global Catalog</span></span>      | <span data-ttu-id="c0ef2-146">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-146">False</span></span>                             |
| <span data-ttu-id="c0ef2-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c0ef2-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0ef2-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c0ef2-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c0ef2-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0ef2-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c0ef2-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0ef2-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c0ef2-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0ef2-151">Search-Flags</span></span>           | <span data-ttu-id="c0ef2-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0ef2-152">0x00000000</span></span>                        |
| <span data-ttu-id="c0ef2-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0ef2-153">System-Flags</span></span>           | <span data-ttu-id="c0ef2-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c0ef2-154">0x00000011</span></span>                        |
| <span data-ttu-id="c0ef2-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c0ef2-155">Classes used in</span></span>        | [<span data-ttu-id="c0ef2-156">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c0ef2-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c0ef2-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c0ef2-157">Windows Server 2003</span></span>



| <span data-ttu-id="c0ef2-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c0ef2-158">Entry</span></span> | <span data-ttu-id="c0ef2-159">Wert</span><span class="sxs-lookup"><span data-stu-id="c0ef2-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c0ef2-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c0ef2-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c0ef2-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0ef2-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c0ef2-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0ef2-162">System-Only</span></span>            | <span data-ttu-id="c0ef2-163">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-163">False</span></span>                             |
| <span data-ttu-id="c0ef2-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c0ef2-164">Is-Single-Valued</span></span>       | <span data-ttu-id="c0ef2-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="c0ef2-165">True</span></span>                              |
| <span data-ttu-id="c0ef2-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c0ef2-166">Is Indexed</span></span>             | <span data-ttu-id="c0ef2-167">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-167">False</span></span>                             |
| <span data-ttu-id="c0ef2-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c0ef2-168">In Global Catalog</span></span>      | <span data-ttu-id="c0ef2-169">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-169">False</span></span>                             |
| <span data-ttu-id="c0ef2-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c0ef2-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0ef2-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c0ef2-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c0ef2-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0ef2-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c0ef2-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0ef2-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c0ef2-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0ef2-174">Search-Flags</span></span>           | <span data-ttu-id="c0ef2-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0ef2-175">0x00000000</span></span>                        |
| <span data-ttu-id="c0ef2-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0ef2-176">System-Flags</span></span>           | <span data-ttu-id="c0ef2-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c0ef2-177">0x00000011</span></span>                        |
| <span data-ttu-id="c0ef2-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c0ef2-178">Classes used in</span></span>        | [<span data-ttu-id="c0ef2-179">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c0ef2-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c0ef2-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c0ef2-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c0ef2-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c0ef2-181">Entry</span></span> | <span data-ttu-id="c0ef2-182">Wert</span><span class="sxs-lookup"><span data-stu-id="c0ef2-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c0ef2-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c0ef2-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c0ef2-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0ef2-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c0ef2-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0ef2-185">System-Only</span></span>            | <span data-ttu-id="c0ef2-186">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-186">False</span></span>                             |
| <span data-ttu-id="c0ef2-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c0ef2-187">Is-Single-Valued</span></span>       | <span data-ttu-id="c0ef2-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="c0ef2-188">True</span></span>                              |
| <span data-ttu-id="c0ef2-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c0ef2-189">Is Indexed</span></span>             | <span data-ttu-id="c0ef2-190">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-190">False</span></span>                             |
| <span data-ttu-id="c0ef2-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c0ef2-191">In Global Catalog</span></span>      | <span data-ttu-id="c0ef2-192">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-192">False</span></span>                             |
| <span data-ttu-id="c0ef2-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c0ef2-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0ef2-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c0ef2-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c0ef2-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0ef2-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c0ef2-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0ef2-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c0ef2-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0ef2-197">Search-Flags</span></span>           | <span data-ttu-id="c0ef2-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0ef2-198">0x00000000</span></span>                        |
| <span data-ttu-id="c0ef2-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0ef2-199">System-Flags</span></span>           | <span data-ttu-id="c0ef2-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c0ef2-200">0x00000011</span></span>                        |
| <span data-ttu-id="c0ef2-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c0ef2-201">Classes used in</span></span>        | [<span data-ttu-id="c0ef2-202">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c0ef2-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c0ef2-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0ef2-203">Windows Server 2008</span></span>



| <span data-ttu-id="c0ef2-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c0ef2-204">Entry</span></span> | <span data-ttu-id="c0ef2-205">Wert</span><span class="sxs-lookup"><span data-stu-id="c0ef2-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c0ef2-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c0ef2-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c0ef2-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0ef2-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c0ef2-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0ef2-208">System-Only</span></span>            | <span data-ttu-id="c0ef2-209">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-209">False</span></span>                             |
| <span data-ttu-id="c0ef2-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c0ef2-210">Is-Single-Valued</span></span>       | <span data-ttu-id="c0ef2-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="c0ef2-211">True</span></span>                              |
| <span data-ttu-id="c0ef2-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c0ef2-212">Is Indexed</span></span>             | <span data-ttu-id="c0ef2-213">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-213">False</span></span>                             |
| <span data-ttu-id="c0ef2-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c0ef2-214">In Global Catalog</span></span>      | <span data-ttu-id="c0ef2-215">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-215">False</span></span>                             |
| <span data-ttu-id="c0ef2-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c0ef2-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0ef2-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c0ef2-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c0ef2-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0ef2-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c0ef2-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0ef2-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c0ef2-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0ef2-220">Search-Flags</span></span>           | <span data-ttu-id="c0ef2-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0ef2-221">0x00000000</span></span>                        |
| <span data-ttu-id="c0ef2-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0ef2-222">System-Flags</span></span>           | <span data-ttu-id="c0ef2-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c0ef2-223">0x00000011</span></span>                        |
| <span data-ttu-id="c0ef2-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c0ef2-224">Classes used in</span></span>        | [<span data-ttu-id="c0ef2-225">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c0ef2-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c0ef2-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c0ef2-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c0ef2-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c0ef2-227">Entry</span></span> | <span data-ttu-id="c0ef2-228">Wert</span><span class="sxs-lookup"><span data-stu-id="c0ef2-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c0ef2-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c0ef2-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c0ef2-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0ef2-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c0ef2-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0ef2-231">System-Only</span></span>            | <span data-ttu-id="c0ef2-232">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-232">False</span></span>                             |
| <span data-ttu-id="c0ef2-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c0ef2-233">Is-Single-Valued</span></span>       | <span data-ttu-id="c0ef2-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="c0ef2-234">True</span></span>                              |
| <span data-ttu-id="c0ef2-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c0ef2-235">Is Indexed</span></span>             | <span data-ttu-id="c0ef2-236">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-236">False</span></span>                             |
| <span data-ttu-id="c0ef2-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c0ef2-237">In Global Catalog</span></span>      | <span data-ttu-id="c0ef2-238">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-238">False</span></span>                             |
| <span data-ttu-id="c0ef2-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c0ef2-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0ef2-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c0ef2-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c0ef2-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0ef2-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c0ef2-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0ef2-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c0ef2-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0ef2-243">Search-Flags</span></span>           | <span data-ttu-id="c0ef2-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0ef2-244">0x00000000</span></span>                        |
| <span data-ttu-id="c0ef2-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0ef2-245">System-Flags</span></span>           | <span data-ttu-id="c0ef2-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c0ef2-246">0x00000011</span></span>                        |
| <span data-ttu-id="c0ef2-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c0ef2-247">Classes used in</span></span>        | [<span data-ttu-id="c0ef2-248">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c0ef2-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c0ef2-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c0ef2-249">Windows Server 2012</span></span>



| <span data-ttu-id="c0ef2-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c0ef2-250">Entry</span></span> | <span data-ttu-id="c0ef2-251">Wert</span><span class="sxs-lookup"><span data-stu-id="c0ef2-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c0ef2-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c0ef2-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c0ef2-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0ef2-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c0ef2-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0ef2-254">System-Only</span></span>            | <span data-ttu-id="c0ef2-255">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-255">False</span></span>                             |
| <span data-ttu-id="c0ef2-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c0ef2-256">Is-Single-Valued</span></span>       | <span data-ttu-id="c0ef2-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="c0ef2-257">True</span></span>                              |
| <span data-ttu-id="c0ef2-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c0ef2-258">Is Indexed</span></span>             | <span data-ttu-id="c0ef2-259">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-259">False</span></span>                             |
| <span data-ttu-id="c0ef2-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c0ef2-260">In Global Catalog</span></span>      | <span data-ttu-id="c0ef2-261">False</span><span class="sxs-lookup"><span data-stu-id="c0ef2-261">False</span></span>                             |
| <span data-ttu-id="c0ef2-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c0ef2-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0ef2-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c0ef2-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c0ef2-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0ef2-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c0ef2-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0ef2-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c0ef2-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0ef2-266">Search-Flags</span></span>           | <span data-ttu-id="c0ef2-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0ef2-267">0x00000000</span></span>                        |
| <span data-ttu-id="c0ef2-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0ef2-268">System-Flags</span></span>           | <span data-ttu-id="c0ef2-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c0ef2-269">0x00000011</span></span>                        |
| <span data-ttu-id="c0ef2-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c0ef2-270">Classes used in</span></span>        | [<span data-ttu-id="c0ef2-271">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c0ef2-271">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c0ef2-272">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0ef2-272">Remarks</span></span>

<span data-ttu-id="c0ef2-273">Dieses Attribut wird nicht repliziert und auf jedem Domänen Controller in der Domäne verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c0ef2-273">This attribute is not replicated and is maintained on each domain controller in the domain.</span></span> <span data-ttu-id="c0ef2-274">Um einen exakten Wert für die Gesamtzahl erfolgreicher Anmeldeversuche in der Domäne des Benutzers zu erhalten, muss jeder Domänen Controller in der Domäne abgefragt werden, und die Summe der Werte sollte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0ef2-274">To get an accurate value for the user's total number of successful logon attempts in the domain, each domain controller in the domain must be queried and the sum of the values should be used.</span></span> <span data-ttu-id="c0ef2-275">Beachten Sie, dass das Attribut nicht repliziert wird, daher können auch bei nicht abgekoppelten Domänen Controllern ggf. Anmeldungen für den Benutzer gezählt werden, die in der Anzahl fehlen.</span><span class="sxs-lookup"><span data-stu-id="c0ef2-275">Keep in mind that the attribute is not replicated, therefore domain controllers that are retired may have counted logons for the user as well, and these will be missing from the count.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c0ef2-276">Aufgrund der Kompatibilität mit 16-Bit-Versionen von LAN Manager hat das-Attribut eine Obergrenze von 65535.</span><span class="sxs-lookup"><span data-stu-id="c0ef2-276">Due to compatibility with 16-bit versions of LAN Manager, the attribute has an upper limit of 65535.</span></span> <span data-ttu-id="c0ef2-277">Nachdem dieser Grenzwert erreicht wurde, kann er nicht als Indikator für die Benutzeraktivität auf diesem Domänen Controller verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0ef2-277">After this limit has been reached, you cannot use it as an indicator of user activity on this domain controller.</span></span>

 

 

 





