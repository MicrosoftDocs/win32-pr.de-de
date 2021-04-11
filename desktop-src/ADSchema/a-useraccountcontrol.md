---
title: Attribut "Benutzerkontensteuerung"
description: Flags, die das Verhalten des Benutzerkontos steuern.
ms.assetid: fc81a16a-f537-44cc-957c-5d7ca66b9755
ms.tgt_platform: multiple
keywords:
- AD-Schema für Benutzerkonten Steuerungs Attribut
- userAccountControl-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- User-Account-Control
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f60297d22aad76b229c691a667ac22a87271402c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122635"
---
# <a name="user-account-control-attribute"></a><span data-ttu-id="092ab-105">Attribut "Benutzerkontensteuerung"</span><span class="sxs-lookup"><span data-stu-id="092ab-105">User-Account-Control attribute</span></span>

<span data-ttu-id="092ab-106">Flags, die das Verhalten des Benutzerkontos steuern.</span><span class="sxs-lookup"><span data-stu-id="092ab-106">Flags that control the behavior of the user account.</span></span>



| <span data-ttu-id="092ab-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="092ab-107">Entry</span></span> | <span data-ttu-id="092ab-108">Wert</span><span class="sxs-lookup"><span data-stu-id="092ab-108">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="092ab-109">CN</span><span class="sxs-lookup"><span data-stu-id="092ab-109">CN</span></span>                | <span data-ttu-id="092ab-110">Benutzerkontensteuerung</span><span class="sxs-lookup"><span data-stu-id="092ab-110">User-Account-Control</span></span>                  |
| <span data-ttu-id="092ab-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="092ab-111">Ldap-Display-Name</span></span> | <span data-ttu-id="092ab-112">userAccountControl</span><span class="sxs-lookup"><span data-stu-id="092ab-112">userAccountControl</span></span>                    |
| <span data-ttu-id="092ab-113">Size</span><span class="sxs-lookup"><span data-stu-id="092ab-113">Size</span></span>              | <span data-ttu-id="092ab-114">4 Bytes.</span><span class="sxs-lookup"><span data-stu-id="092ab-114">4 bytes.</span></span>                              |
| <span data-ttu-id="092ab-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="092ab-115">Update Privilege</span></span>  | <span data-ttu-id="092ab-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="092ab-116">This value is set by the system.</span></span>      |
| <span data-ttu-id="092ab-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="092ab-117">Update Frequency</span></span>  | <span data-ttu-id="092ab-118">Jedes Mal, wenn die Konto Richtlinie geändert wird.</span><span class="sxs-lookup"><span data-stu-id="092ab-118">Each time the account policy changes.</span></span> |
| <span data-ttu-id="092ab-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="092ab-119">Attribute-Id</span></span>      | <span data-ttu-id="092ab-120">1.2.840.113556.1.4.8</span><span class="sxs-lookup"><span data-stu-id="092ab-120">1.2.840.113556.1.4.8</span></span>                  |
| <span data-ttu-id="092ab-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="092ab-121">System-Id-Guid</span></span>    | <span data-ttu-id="092ab-122">bf967a68-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="092ab-122">bf967a68-0de6-11d0-a285-00aa003049e2</span></span>  |
| <span data-ttu-id="092ab-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="092ab-123">Syntax</span></span>            | [<span data-ttu-id="092ab-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="092ab-124">**Enumeration**</span></span>](s-enumeration.md)  |



## <a name="implementations"></a><span data-ttu-id="092ab-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="092ab-125">Implementations</span></span>

-   [<span data-ttu-id="092ab-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="092ab-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="092ab-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="092ab-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="092ab-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="092ab-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="092ab-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="092ab-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="092ab-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="092ab-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="092ab-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="092ab-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="092ab-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="092ab-132">Windows 2000 Server</span></span>



| <span data-ttu-id="092ab-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="092ab-133">Entry</span></span> | <span data-ttu-id="092ab-134">Wert</span><span class="sxs-lookup"><span data-stu-id="092ab-134">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="092ab-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="092ab-135">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="092ab-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="092ab-136">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="092ab-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="092ab-137">System-Only</span></span>            | <span data-ttu-id="092ab-138">False</span><span class="sxs-lookup"><span data-stu-id="092ab-138">False</span></span>                             |
| <span data-ttu-id="092ab-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="092ab-139">Is-Single-Valued</span></span>       | <span data-ttu-id="092ab-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-140">True</span></span>                              |
| <span data-ttu-id="092ab-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="092ab-141">Is Indexed</span></span>             | <span data-ttu-id="092ab-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-142">True</span></span>                              |
| <span data-ttu-id="092ab-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="092ab-143">In Global Catalog</span></span>      | <span data-ttu-id="092ab-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-144">True</span></span>                              |
| <span data-ttu-id="092ab-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="092ab-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="092ab-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="092ab-146">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="092ab-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="092ab-147">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="092ab-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="092ab-148">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="092ab-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="092ab-149">Search-Flags</span></span>           | <span data-ttu-id="092ab-150">0x00000019</span><span class="sxs-lookup"><span data-stu-id="092ab-150">0x00000019</span></span>                        |
| <span data-ttu-id="092ab-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="092ab-151">System-Flags</span></span>           | <span data-ttu-id="092ab-152">0x00000012</span><span class="sxs-lookup"><span data-stu-id="092ab-152">0x00000012</span></span>                        |
| <span data-ttu-id="092ab-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="092ab-153">Classes used in</span></span>        | [<span data-ttu-id="092ab-154">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="092ab-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="092ab-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="092ab-155">Windows Server 2003</span></span>



| <span data-ttu-id="092ab-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="092ab-156">Entry</span></span> | <span data-ttu-id="092ab-157">Wert</span><span class="sxs-lookup"><span data-stu-id="092ab-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="092ab-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="092ab-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="092ab-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="092ab-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="092ab-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="092ab-160">System-Only</span></span>            | <span data-ttu-id="092ab-161">False</span><span class="sxs-lookup"><span data-stu-id="092ab-161">False</span></span>                             |
| <span data-ttu-id="092ab-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="092ab-162">Is-Single-Valued</span></span>       | <span data-ttu-id="092ab-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-163">True</span></span>                              |
| <span data-ttu-id="092ab-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="092ab-164">Is Indexed</span></span>             | <span data-ttu-id="092ab-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-165">True</span></span>                              |
| <span data-ttu-id="092ab-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="092ab-166">In Global Catalog</span></span>      | <span data-ttu-id="092ab-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-167">True</span></span>                              |
| <span data-ttu-id="092ab-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="092ab-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="092ab-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="092ab-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="092ab-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="092ab-170">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="092ab-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="092ab-171">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="092ab-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="092ab-172">Search-Flags</span></span>           | <span data-ttu-id="092ab-173">0x00000019</span><span class="sxs-lookup"><span data-stu-id="092ab-173">0x00000019</span></span>                        |
| <span data-ttu-id="092ab-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="092ab-174">System-Flags</span></span>           | <span data-ttu-id="092ab-175">0x00000012</span><span class="sxs-lookup"><span data-stu-id="092ab-175">0x00000012</span></span>                        |
| <span data-ttu-id="092ab-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="092ab-176">Classes used in</span></span>        | [<span data-ttu-id="092ab-177">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="092ab-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="092ab-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="092ab-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="092ab-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="092ab-179">Entry</span></span> | <span data-ttu-id="092ab-180">Wert</span><span class="sxs-lookup"><span data-stu-id="092ab-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="092ab-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="092ab-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="092ab-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="092ab-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="092ab-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="092ab-183">System-Only</span></span>            | <span data-ttu-id="092ab-184">False</span><span class="sxs-lookup"><span data-stu-id="092ab-184">False</span></span>                             |
| <span data-ttu-id="092ab-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="092ab-185">Is-Single-Valued</span></span>       | <span data-ttu-id="092ab-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-186">True</span></span>                              |
| <span data-ttu-id="092ab-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="092ab-187">Is Indexed</span></span>             | <span data-ttu-id="092ab-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-188">True</span></span>                              |
| <span data-ttu-id="092ab-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="092ab-189">In Global Catalog</span></span>      | <span data-ttu-id="092ab-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-190">True</span></span>                              |
| <span data-ttu-id="092ab-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="092ab-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="092ab-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="092ab-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="092ab-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="092ab-193">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="092ab-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="092ab-194">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="092ab-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="092ab-195">Search-Flags</span></span>           | <span data-ttu-id="092ab-196">0x00000019</span><span class="sxs-lookup"><span data-stu-id="092ab-196">0x00000019</span></span>                        |
| <span data-ttu-id="092ab-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="092ab-197">System-Flags</span></span>           | <span data-ttu-id="092ab-198">0x00000012</span><span class="sxs-lookup"><span data-stu-id="092ab-198">0x00000012</span></span>                        |
| <span data-ttu-id="092ab-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="092ab-199">Classes used in</span></span>        | [<span data-ttu-id="092ab-200">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="092ab-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="092ab-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="092ab-201">Windows Server 2008</span></span>



| <span data-ttu-id="092ab-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="092ab-202">Entry</span></span> | <span data-ttu-id="092ab-203">Wert</span><span class="sxs-lookup"><span data-stu-id="092ab-203">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="092ab-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="092ab-204">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="092ab-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="092ab-205">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="092ab-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="092ab-206">System-Only</span></span>            | <span data-ttu-id="092ab-207">False</span><span class="sxs-lookup"><span data-stu-id="092ab-207">False</span></span>                             |
| <span data-ttu-id="092ab-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="092ab-208">Is-Single-Valued</span></span>       | <span data-ttu-id="092ab-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-209">True</span></span>                              |
| <span data-ttu-id="092ab-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="092ab-210">Is Indexed</span></span>             | <span data-ttu-id="092ab-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-211">True</span></span>                              |
| <span data-ttu-id="092ab-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="092ab-212">In Global Catalog</span></span>      | <span data-ttu-id="092ab-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-213">True</span></span>                              |
| <span data-ttu-id="092ab-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="092ab-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="092ab-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="092ab-215">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="092ab-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="092ab-216">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="092ab-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="092ab-217">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="092ab-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="092ab-218">Search-Flags</span></span>           | <span data-ttu-id="092ab-219">0x00000019</span><span class="sxs-lookup"><span data-stu-id="092ab-219">0x00000019</span></span>                        |
| <span data-ttu-id="092ab-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="092ab-220">System-Flags</span></span>           | <span data-ttu-id="092ab-221">0x00000012</span><span class="sxs-lookup"><span data-stu-id="092ab-221">0x00000012</span></span>                        |
| <span data-ttu-id="092ab-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="092ab-222">Classes used in</span></span>        | [<span data-ttu-id="092ab-223">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="092ab-223">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="092ab-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="092ab-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="092ab-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="092ab-225">Entry</span></span> | <span data-ttu-id="092ab-226">Wert</span><span class="sxs-lookup"><span data-stu-id="092ab-226">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="092ab-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="092ab-227">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="092ab-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="092ab-228">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="092ab-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="092ab-229">System-Only</span></span>            | <span data-ttu-id="092ab-230">False</span><span class="sxs-lookup"><span data-stu-id="092ab-230">False</span></span>                             |
| <span data-ttu-id="092ab-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="092ab-231">Is-Single-Valued</span></span>       | <span data-ttu-id="092ab-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-232">True</span></span>                              |
| <span data-ttu-id="092ab-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="092ab-233">Is Indexed</span></span>             | <span data-ttu-id="092ab-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-234">True</span></span>                              |
| <span data-ttu-id="092ab-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="092ab-235">In Global Catalog</span></span>      | <span data-ttu-id="092ab-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-236">True</span></span>                              |
| <span data-ttu-id="092ab-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="092ab-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="092ab-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="092ab-238">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="092ab-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="092ab-239">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="092ab-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="092ab-240">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="092ab-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="092ab-241">Search-Flags</span></span>           | <span data-ttu-id="092ab-242">0x00000019</span><span class="sxs-lookup"><span data-stu-id="092ab-242">0x00000019</span></span>                        |
| <span data-ttu-id="092ab-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="092ab-243">System-Flags</span></span>           | <span data-ttu-id="092ab-244">0x00000012</span><span class="sxs-lookup"><span data-stu-id="092ab-244">0x00000012</span></span>                        |
| <span data-ttu-id="092ab-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="092ab-245">Classes used in</span></span>        | [<span data-ttu-id="092ab-246">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="092ab-246">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="092ab-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="092ab-247">Windows Server 2012</span></span>



| <span data-ttu-id="092ab-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="092ab-248">Entry</span></span> | <span data-ttu-id="092ab-249">Wert</span><span class="sxs-lookup"><span data-stu-id="092ab-249">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="092ab-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="092ab-250">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="092ab-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="092ab-251">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="092ab-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="092ab-252">System-Only</span></span>            | <span data-ttu-id="092ab-253">False</span><span class="sxs-lookup"><span data-stu-id="092ab-253">False</span></span>                             |
| <span data-ttu-id="092ab-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="092ab-254">Is-Single-Valued</span></span>       | <span data-ttu-id="092ab-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-255">True</span></span>                              |
| <span data-ttu-id="092ab-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="092ab-256">Is Indexed</span></span>             | <span data-ttu-id="092ab-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-257">True</span></span>                              |
| <span data-ttu-id="092ab-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="092ab-258">In Global Catalog</span></span>      | <span data-ttu-id="092ab-259">Richtig</span><span class="sxs-lookup"><span data-stu-id="092ab-259">True</span></span>                              |
| <span data-ttu-id="092ab-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="092ab-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="092ab-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="092ab-261">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="092ab-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="092ab-262">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="092ab-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="092ab-263">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="092ab-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="092ab-264">Search-Flags</span></span>           | <span data-ttu-id="092ab-265">0x00000019</span><span class="sxs-lookup"><span data-stu-id="092ab-265">0x00000019</span></span>                        |
| <span data-ttu-id="092ab-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="092ab-266">System-Flags</span></span>           | <span data-ttu-id="092ab-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="092ab-267">0x00000012</span></span>                        |
| <span data-ttu-id="092ab-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="092ab-268">Classes used in</span></span>        | [<span data-ttu-id="092ab-269">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="092ab-269">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="092ab-270">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="092ab-270">Remarks</span></span>

<span data-ttu-id="092ab-271">Dieser Attribut Wert kann NULL oder eine Kombination aus einem oder mehreren der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="092ab-271">This attribute value can be zero or a combination of one or more of the following values.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="092ab-272">Hexadezimalwert</span><span class="sxs-lookup"><span data-stu-id="092ab-272">Hexadecimal value</span></span></th>
<th><span data-ttu-id="092ab-273">Bezeichner (definiert in "IADs. h")</span><span class="sxs-lookup"><span data-stu-id="092ab-273">Identifier (defined in iads.h)</span></span></th>
<th><span data-ttu-id="092ab-274">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="092ab-274">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="092ab-275">0x00000001</span><span class="sxs-lookup"><span data-stu-id="092ab-275">0x00000001</span></span></td>
<td><span data-ttu-id="092ab-276"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-276"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></span></span></td>
<td><span data-ttu-id="092ab-277">Das Anmelde Skript wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="092ab-277">The logon script is executed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="092ab-278">0x00000002</span><span class="sxs-lookup"><span data-stu-id="092ab-278">0x00000002</span></span></td>
<td><span data-ttu-id="092ab-279"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-279"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></span></span></td>
<td><span data-ttu-id="092ab-280">Das Benutzerkonto ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="092ab-280">The user account is disabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="092ab-281">0x00000008</span><span class="sxs-lookup"><span data-stu-id="092ab-281">0x00000008</span></span></td>
<td><span data-ttu-id="092ab-282"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-282"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></span></span></td>
<td><span data-ttu-id="092ab-283">Das Basisverzeichnis ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="092ab-283">The home directory is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="092ab-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="092ab-284">0x00000010</span></span></td>
<td><span data-ttu-id="092ab-285"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-285"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></span></span></td>
<td><span data-ttu-id="092ab-286">Das Konto ist zurzeit gesperrt.</span><span class="sxs-lookup"><span data-stu-id="092ab-286">The account is currently locked out.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="092ab-287">0x00000020</span><span class="sxs-lookup"><span data-stu-id="092ab-287">0x00000020</span></span></td>
<td><span data-ttu-id="092ab-288"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-288"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></span></span></td>
<td><span data-ttu-id="092ab-289">Es ist kein Kennwort erforderlich.</span><span class="sxs-lookup"><span data-stu-id="092ab-289">No password is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="092ab-290">0x00000040</span><span class="sxs-lookup"><span data-stu-id="092ab-290">0x00000040</span></span></td>
<td><span data-ttu-id="092ab-291"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-291"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="092ab-292">Der Benutzer kann das Kennwort nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="092ab-292">The user cannot change the password.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="092ab-293">Sie können die Berechtigungseinstellungen von PASSWD_CANT_CHANGE nicht zuweisen, indem Sie das userAccountControl-Attribut direkt ändern.</span><span class="sxs-lookup"><span data-stu-id="092ab-293">You cannot assign the permission settings of PASSWD_CANT_CHANGE by directly modifying the UserAccountControl attribute.</span></span> <span data-ttu-id="092ab-294">Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie verhindern können, dass Benutzer das Kennwort ändern, finden Sie unter Benutzer kann das Kennwort <a href="/windows/desktop/ADSI/user-cannot-change-password">nicht ändern</a>.</span><span class="sxs-lookup"><span data-stu-id="092ab-294">For more information and a code example that shows how to prevent a user from changing the password, see <a href="/windows/desktop/ADSI/user-cannot-change-password">User Cannot Change Password</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="092ab-295">:</span><span class="sxs-lookup"><span data-stu-id="092ab-295">:</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="092ab-296">0x00000080</span><span class="sxs-lookup"><span data-stu-id="092ab-296">0x00000080</span></span></td>
<td><span data-ttu-id="092ab-297"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-297"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></span></span></td>
<td><span data-ttu-id="092ab-298">Der Benutzer kann ein verschlüsseltes Kennwort senden.</span><span class="sxs-lookup"><span data-stu-id="092ab-298">The user can send an encrypted password.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="092ab-299">0x00000100</span><span class="sxs-lookup"><span data-stu-id="092ab-299">0x00000100</span></span></td>
<td><span data-ttu-id="092ab-300"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-300"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="092ab-301">Dies ist ein Konto für Benutzer, deren primäres Konto sich in einer anderen Domäne befindet.</span><span class="sxs-lookup"><span data-stu-id="092ab-301">This is an account for users whose primary account is in another domain.</span></span> <span data-ttu-id="092ab-302">Dieses Konto ermöglicht dem Benutzer den Zugriff auf diese Domäne, jedoch nicht auf eine Domäne, die dieser Domäne vertraut.</span><span class="sxs-lookup"><span data-stu-id="092ab-302">This account provides user access to this domain, but not to any domain that trusts this domain.</span></span> <span data-ttu-id="092ab-303">Wird auch als lokales Benutzerkonto bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="092ab-303">Also known as a local user account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="092ab-304">0x00000200</span><span class="sxs-lookup"><span data-stu-id="092ab-304">0x00000200</span></span></td>
<td><span data-ttu-id="092ab-305"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-305"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="092ab-306">Dies ist ein Standard Kontotyp, der einen typischen Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="092ab-306">This is a default account type that represents a typical user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="092ab-307">0x00000800</span><span class="sxs-lookup"><span data-stu-id="092ab-307">0x00000800</span></span></td>
<td><span data-ttu-id="092ab-308"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-308"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="092ab-309">Dies ist eine Zulassungsberechtigung für ein Vertrauensstellungs Konto für eine System Domäne, die anderen Domänen vertraut.</span><span class="sxs-lookup"><span data-stu-id="092ab-309">This is a permit to trust account for a system domain that trusts other domains.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="092ab-310">0x00001000</span><span class="sxs-lookup"><span data-stu-id="092ab-310">0x00001000</span></span></td>
<td><span data-ttu-id="092ab-311"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-311"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="092ab-312">Hierbei handelt es sich um ein Computer Konto für einen Computer, der Mitglied dieser Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="092ab-312">This is a computer account for a computer that is a member of this domain.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="092ab-313">0x00002000</span><span class="sxs-lookup"><span data-stu-id="092ab-313">0x00002000</span></span></td>
<td><span data-ttu-id="092ab-314"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-314"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="092ab-315">Hierbei handelt es sich um ein Computer Konto für einen Domänen Controller der Systemsicherung, der Mitglied dieser Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="092ab-315">This is a computer account for a system backup domain controller that is a member of this domain.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="092ab-316">0x00004000</span><span class="sxs-lookup"><span data-stu-id="092ab-316">0x00004000</span></span></td>
<td><span data-ttu-id="092ab-317">–</span><span class="sxs-lookup"><span data-stu-id="092ab-317">N/A</span></span></td>
<td><span data-ttu-id="092ab-318">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="092ab-318">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="092ab-319">0x00008000</span><span class="sxs-lookup"><span data-stu-id="092ab-319">0x00008000</span></span></td>
<td><span data-ttu-id="092ab-320">–</span><span class="sxs-lookup"><span data-stu-id="092ab-320">N/A</span></span></td>
<td><span data-ttu-id="092ab-321">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="092ab-321">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="092ab-322">0x00010000</span><span class="sxs-lookup"><span data-stu-id="092ab-322">0x00010000</span></span></td>
<td><span data-ttu-id="092ab-323"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-323"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></span></span></td>
<td><span data-ttu-id="092ab-324">Das Kennwort für dieses Konto läuft nie ab.</span><span class="sxs-lookup"><span data-stu-id="092ab-324">The password for this account will never expire.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="092ab-325">0x00020000</span><span class="sxs-lookup"><span data-stu-id="092ab-325">0x00020000</span></span></td>
<td><span data-ttu-id="092ab-326"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-326"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="092ab-327">Hierbei handelt es sich um ein MNS-Anmelde Konto.</span><span class="sxs-lookup"><span data-stu-id="092ab-327">This is an MNS logon account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="092ab-328">0x00040000</span><span class="sxs-lookup"><span data-stu-id="092ab-328">0x00040000</span></span></td>
<td><span data-ttu-id="092ab-329"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-329"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></span></span></td>
<td><span data-ttu-id="092ab-330">Der Benutzer muss sich mit einer Smartcard anmelden.</span><span class="sxs-lookup"><span data-stu-id="092ab-330">The user must log on using a smart card.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="092ab-331">0x00080000</span><span class="sxs-lookup"><span data-stu-id="092ab-331">0x00080000</span></span></td>
<td><span data-ttu-id="092ab-332"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-332"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></span></span></td>
<td><span data-ttu-id="092ab-333">Das Dienst Konto (Benutzer oder Computer Konto), unter dem ein-Dienst ausgeführt wird, wird für die Kerberos-Delegierung als vertrauenswürdig eingestuft.</span><span class="sxs-lookup"><span data-stu-id="092ab-333">The service account (user or computer account), under which a service runs, is trusted for Kerberos delegation.</span></span> <span data-ttu-id="092ab-334">Ein solcher Dienst kann die Identität eines Clients annehmen, der den Dienst anfordert.</span><span class="sxs-lookup"><span data-stu-id="092ab-334">Any such service can impersonate a client requesting the service.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="092ab-335">0x00100000</span><span class="sxs-lookup"><span data-stu-id="092ab-335">0x00100000</span></span></td>
<td><span data-ttu-id="092ab-336"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-336"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></span></span></td>
<td><span data-ttu-id="092ab-337">Der Sicherheitskontext des Benutzers wird nicht an einen Dienst delegiert, auch wenn das Dienst Konto für die Kerberos-Delegierung als vertrauenswürdig festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="092ab-337">The security context of the user will not be delegated to a service even if the service account is set as trusted for Kerberos delegation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="092ab-338">0x00200000</span><span class="sxs-lookup"><span data-stu-id="092ab-338">0x00200000</span></span></td>
<td><span data-ttu-id="092ab-339"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-339"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></span></span></td>
<td><span data-ttu-id="092ab-340">Schränken Sie diesen Prinzipal so ein, dass nur Daten Verschlüsselungs Standard-Verschlüsselungstypen für Schlüssel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="092ab-340">Restrict this principal to use only Data Encryption Standard (DES) encryption types for keys.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="092ab-341">0x00400000</span><span class="sxs-lookup"><span data-stu-id="092ab-341">0x00400000</span></span></td>
<td><span data-ttu-id="092ab-342"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-342"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></span></span></td>
<td><span data-ttu-id="092ab-343">Für dieses Konto ist keine Kerberos-Vorauthentifizierung für die Anmeldung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="092ab-343">This account does not require Kerberos pre-authentication for logon.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="092ab-344">0x00800000</span><span class="sxs-lookup"><span data-stu-id="092ab-344">0x00800000</span></span></td>
<td><span data-ttu-id="092ab-345"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-345"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></span></span></td>
<td><span data-ttu-id="092ab-346">Das Benutzer Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="092ab-346">The user password has expired.</span></span> <span data-ttu-id="092ab-347">Dieses Flag wird vom System mithilfe von Daten aus dem <a href="a-pwdlastset.md"><strong>Pwd-Last Satz</strong></a> -Attribut und der Domänen Richtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="092ab-347">This flag is created by the system using data from the <a href="a-pwdlastset.md"><strong>Pwd-Last-Set</strong></a> attribute and the domain policy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="092ab-348">0x01000000</span><span class="sxs-lookup"><span data-stu-id="092ab-348">0x01000000</span></span></td>
<td><span data-ttu-id="092ab-349"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="092ab-349"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></span></span></td>
<td><span data-ttu-id="092ab-350">Das Konto ist für die Delegierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="092ab-350">The account is enabled for delegation.</span></span> <span data-ttu-id="092ab-351">Dies ist eine sicherheitsrelevante Einstellung. Konten, bei denen diese Option aktiviert ist, sollten streng gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="092ab-351">This is a security-sensitive setting; accounts with this option enabled should be strictly controlled.</span></span> <span data-ttu-id="092ab-352">Mit dieser Einstellung kann ein Dienst, der unter dem Konto ausgeführt wird, eine Client Identität annehmen und sich als dieser Benutzer bei anderen Remote Servern im Netzwerk authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="092ab-352">This setting enables a service running under the account to assume a client identity and authenticate as that user to other remote servers on the network.</span></span></td>
</tr>
</tbody>
</table>



 

