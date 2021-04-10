---
title: Ungültiges-pwd-count-Attribut
description: Gibt an, wie oft der Benutzer versucht hat, sich mit einem falschen Kennwort beim Konto anzumelden.
ms.assetid: 1161b0c1-1b28-4349-ad43-82ce68428c44
ms.tgt_platform: multiple
keywords:
- "\"Bad-pwd-count\"-Attribut AD-Schema"
- BadPwdCount-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Bad-Pwd-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3a406058737773781874a81e9968786e1523d8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107283"
---
# <a name="bad-pwd-count-attribute"></a><span data-ttu-id="89d4f-105">Ungültiges-pwd-count-Attribut</span><span class="sxs-lookup"><span data-stu-id="89d4f-105">Bad-Pwd-Count attribute</span></span>

<span data-ttu-id="89d4f-106">Gibt an, wie oft der Benutzer versucht hat, sich mit einem falschen Kennwort beim Konto anzumelden.</span><span class="sxs-lookup"><span data-stu-id="89d4f-106">The number of times the user tried to log on to the account using an incorrect password.</span></span> <span data-ttu-id="89d4f-107">Der Wert 0 gibt an, dass der Wert unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="89d4f-107">A value of 0 indicates that the value is unknown.</span></span>



| <span data-ttu-id="89d4f-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="89d4f-108">Entry</span></span> | <span data-ttu-id="89d4f-109">Wert</span><span class="sxs-lookup"><span data-stu-id="89d4f-109">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="89d4f-110">CN</span><span class="sxs-lookup"><span data-stu-id="89d4f-110">CN</span></span>                | <span data-ttu-id="89d4f-111">Falsch-pwd-Anzahl</span><span class="sxs-lookup"><span data-stu-id="89d4f-111">Bad-Pwd-Count</span></span>                             |
| <span data-ttu-id="89d4f-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="89d4f-112">Ldap-Display-Name</span></span> | <span data-ttu-id="89d4f-113">BadPwdCount</span><span class="sxs-lookup"><span data-stu-id="89d4f-113">badPwdCount</span></span>                               |
| <span data-ttu-id="89d4f-114">Size</span><span class="sxs-lookup"><span data-stu-id="89d4f-114">Size</span></span>              | <span data-ttu-id="89d4f-115">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="89d4f-115">4 bytes</span></span>                                   |
| <span data-ttu-id="89d4f-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="89d4f-116">Update Privilege</span></span>  | <span data-ttu-id="89d4f-117">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="89d4f-117">This value is set by the system.</span></span>          |
| <span data-ttu-id="89d4f-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="89d4f-118">Update Frequency</span></span>  | <span data-ttu-id="89d4f-119">Jedes Mal, wenn der Benutzer ein ungültiges Kennwort eingibt.</span><span class="sxs-lookup"><span data-stu-id="89d4f-119">Each time the user enters a bad password.</span></span> |
| <span data-ttu-id="89d4f-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="89d4f-120">Attribute-Id</span></span>      | <span data-ttu-id="89d4f-121">1.2.840.113556.1.4.12</span><span class="sxs-lookup"><span data-stu-id="89d4f-121">1.2.840.113556.1.4.12</span></span>                     |
| <span data-ttu-id="89d4f-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="89d4f-122">System-Id-Guid</span></span>    | <span data-ttu-id="89d4f-123">bf96792e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="89d4f-123">bf96792e-0de6-11d0-a285-00aa003049e2</span></span>      |
| <span data-ttu-id="89d4f-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="89d4f-124">Syntax</span></span>            | [<span data-ttu-id="89d4f-125">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="89d4f-125">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="89d4f-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="89d4f-126">Implementations</span></span>

-   [<span data-ttu-id="89d4f-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="89d4f-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="89d4f-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="89d4f-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="89d4f-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="89d4f-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="89d4f-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="89d4f-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="89d4f-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="89d4f-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="89d4f-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="89d4f-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="89d4f-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="89d4f-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="89d4f-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="89d4f-134">Windows 2000 Server</span></span>



| <span data-ttu-id="89d4f-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="89d4f-135">Entry</span></span> | <span data-ttu-id="89d4f-136">Wert</span><span class="sxs-lookup"><span data-stu-id="89d4f-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="89d4f-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="89d4f-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="89d4f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89d4f-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="89d4f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="89d4f-139">System-Only</span></span>            | <span data-ttu-id="89d4f-140">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-140">False</span></span>                             |
| <span data-ttu-id="89d4f-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="89d4f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="89d4f-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="89d4f-142">True</span></span>                              |
| <span data-ttu-id="89d4f-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="89d4f-143">Is Indexed</span></span>             | <span data-ttu-id="89d4f-144">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-144">False</span></span>                             |
| <span data-ttu-id="89d4f-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="89d4f-145">In Global Catalog</span></span>      | <span data-ttu-id="89d4f-146">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-146">False</span></span>                             |
| <span data-ttu-id="89d4f-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="89d4f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="89d4f-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="89d4f-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="89d4f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89d4f-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="89d4f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89d4f-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="89d4f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89d4f-151">Search-Flags</span></span>           | <span data-ttu-id="89d4f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89d4f-152">0x00000000</span></span>                        |
| <span data-ttu-id="89d4f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89d4f-153">System-Flags</span></span>           | <span data-ttu-id="89d4f-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="89d4f-154">0x00000011</span></span>                        |
| <span data-ttu-id="89d4f-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="89d4f-155">Classes used in</span></span>        | [<span data-ttu-id="89d4f-156">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="89d4f-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="89d4f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="89d4f-157">Windows Server 2003</span></span>



| <span data-ttu-id="89d4f-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="89d4f-158">Entry</span></span> | <span data-ttu-id="89d4f-159">Wert</span><span class="sxs-lookup"><span data-stu-id="89d4f-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="89d4f-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="89d4f-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="89d4f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89d4f-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="89d4f-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="89d4f-162">System-Only</span></span>            | <span data-ttu-id="89d4f-163">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-163">False</span></span>                             |
| <span data-ttu-id="89d4f-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="89d4f-164">Is-Single-Valued</span></span>       | <span data-ttu-id="89d4f-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="89d4f-165">True</span></span>                              |
| <span data-ttu-id="89d4f-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="89d4f-166">Is Indexed</span></span>             | <span data-ttu-id="89d4f-167">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-167">False</span></span>                             |
| <span data-ttu-id="89d4f-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="89d4f-168">In Global Catalog</span></span>      | <span data-ttu-id="89d4f-169">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-169">False</span></span>                             |
| <span data-ttu-id="89d4f-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="89d4f-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="89d4f-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="89d4f-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="89d4f-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89d4f-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="89d4f-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89d4f-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="89d4f-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89d4f-174">Search-Flags</span></span>           | <span data-ttu-id="89d4f-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89d4f-175">0x00000000</span></span>                        |
| <span data-ttu-id="89d4f-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89d4f-176">System-Flags</span></span>           | <span data-ttu-id="89d4f-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="89d4f-177">0x00000011</span></span>                        |
| <span data-ttu-id="89d4f-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="89d4f-178">Classes used in</span></span>        | [<span data-ttu-id="89d4f-179">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="89d4f-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="89d4f-180">Adam</span><span class="sxs-lookup"><span data-stu-id="89d4f-180">ADAM</span></span>



| <span data-ttu-id="89d4f-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="89d4f-181">Entry</span></span> | <span data-ttu-id="89d4f-182">Wert</span><span class="sxs-lookup"><span data-stu-id="89d4f-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="89d4f-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="89d4f-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="89d4f-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89d4f-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="89d4f-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="89d4f-185">System-Only</span></span>            | <span data-ttu-id="89d4f-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="89d4f-186">True</span></span>                                                              |
| <span data-ttu-id="89d4f-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="89d4f-187">Is-Single-Valued</span></span>       | <span data-ttu-id="89d4f-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="89d4f-188">True</span></span>                                                              |
| <span data-ttu-id="89d4f-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="89d4f-189">Is Indexed</span></span>             | <span data-ttu-id="89d4f-190">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-190">False</span></span>                                                             |
| <span data-ttu-id="89d4f-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="89d4f-191">In Global Catalog</span></span>      | <span data-ttu-id="89d4f-192">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-192">False</span></span>                                                             |
| <span data-ttu-id="89d4f-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="89d4f-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="89d4f-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="89d4f-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="89d4f-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89d4f-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="89d4f-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89d4f-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="89d4f-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89d4f-197">Search-Flags</span></span>           | <span data-ttu-id="89d4f-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89d4f-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="89d4f-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89d4f-199">System-Flags</span></span>           | <span data-ttu-id="89d4f-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="89d4f-200">0x00000011</span></span>                                                        |
| <span data-ttu-id="89d4f-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="89d4f-201">Classes used in</span></span>        | [<span data-ttu-id="89d4f-202">**ms-DS-Bindable-Objekt**</span><span class="sxs-lookup"><span data-stu-id="89d4f-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="89d4f-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="89d4f-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="89d4f-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="89d4f-204">Entry</span></span> | <span data-ttu-id="89d4f-205">Wert</span><span class="sxs-lookup"><span data-stu-id="89d4f-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="89d4f-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="89d4f-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="89d4f-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89d4f-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="89d4f-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="89d4f-208">System-Only</span></span>            | <span data-ttu-id="89d4f-209">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-209">False</span></span>                             |
| <span data-ttu-id="89d4f-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="89d4f-210">Is-Single-Valued</span></span>       | <span data-ttu-id="89d4f-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="89d4f-211">True</span></span>                              |
| <span data-ttu-id="89d4f-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="89d4f-212">Is Indexed</span></span>             | <span data-ttu-id="89d4f-213">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-213">False</span></span>                             |
| <span data-ttu-id="89d4f-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="89d4f-214">In Global Catalog</span></span>      | <span data-ttu-id="89d4f-215">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-215">False</span></span>                             |
| <span data-ttu-id="89d4f-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="89d4f-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="89d4f-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="89d4f-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="89d4f-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89d4f-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="89d4f-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89d4f-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="89d4f-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89d4f-220">Search-Flags</span></span>           | <span data-ttu-id="89d4f-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89d4f-221">0x00000000</span></span>                        |
| <span data-ttu-id="89d4f-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89d4f-222">System-Flags</span></span>           | <span data-ttu-id="89d4f-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="89d4f-223">0x00000011</span></span>                        |
| <span data-ttu-id="89d4f-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="89d4f-224">Classes used in</span></span>        | [<span data-ttu-id="89d4f-225">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="89d4f-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="89d4f-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89d4f-226">Windows Server 2008</span></span>



| <span data-ttu-id="89d4f-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="89d4f-227">Entry</span></span> | <span data-ttu-id="89d4f-228">Wert</span><span class="sxs-lookup"><span data-stu-id="89d4f-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="89d4f-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="89d4f-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="89d4f-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89d4f-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="89d4f-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="89d4f-231">System-Only</span></span>            | <span data-ttu-id="89d4f-232">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-232">False</span></span>                             |
| <span data-ttu-id="89d4f-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="89d4f-233">Is-Single-Valued</span></span>       | <span data-ttu-id="89d4f-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="89d4f-234">True</span></span>                              |
| <span data-ttu-id="89d4f-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="89d4f-235">Is Indexed</span></span>             | <span data-ttu-id="89d4f-236">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-236">False</span></span>                             |
| <span data-ttu-id="89d4f-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="89d4f-237">In Global Catalog</span></span>      | <span data-ttu-id="89d4f-238">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-238">False</span></span>                             |
| <span data-ttu-id="89d4f-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="89d4f-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="89d4f-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="89d4f-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="89d4f-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89d4f-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="89d4f-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89d4f-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="89d4f-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89d4f-243">Search-Flags</span></span>           | <span data-ttu-id="89d4f-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89d4f-244">0x00000000</span></span>                        |
| <span data-ttu-id="89d4f-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89d4f-245">System-Flags</span></span>           | <span data-ttu-id="89d4f-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="89d4f-246">0x00000011</span></span>                        |
| <span data-ttu-id="89d4f-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="89d4f-247">Classes used in</span></span>        | [<span data-ttu-id="89d4f-248">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="89d4f-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="89d4f-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="89d4f-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="89d4f-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="89d4f-250">Entry</span></span> | <span data-ttu-id="89d4f-251">Wert</span><span class="sxs-lookup"><span data-stu-id="89d4f-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="89d4f-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="89d4f-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="89d4f-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89d4f-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="89d4f-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="89d4f-254">System-Only</span></span>            | <span data-ttu-id="89d4f-255">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-255">False</span></span>                             |
| <span data-ttu-id="89d4f-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="89d4f-256">Is-Single-Valued</span></span>       | <span data-ttu-id="89d4f-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="89d4f-257">True</span></span>                              |
| <span data-ttu-id="89d4f-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="89d4f-258">Is Indexed</span></span>             | <span data-ttu-id="89d4f-259">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-259">False</span></span>                             |
| <span data-ttu-id="89d4f-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="89d4f-260">In Global Catalog</span></span>      | <span data-ttu-id="89d4f-261">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-261">False</span></span>                             |
| <span data-ttu-id="89d4f-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="89d4f-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="89d4f-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="89d4f-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="89d4f-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89d4f-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="89d4f-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89d4f-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="89d4f-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89d4f-266">Search-Flags</span></span>           | <span data-ttu-id="89d4f-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89d4f-267">0x00000000</span></span>                        |
| <span data-ttu-id="89d4f-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89d4f-268">System-Flags</span></span>           | <span data-ttu-id="89d4f-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="89d4f-269">0x00000011</span></span>                        |
| <span data-ttu-id="89d4f-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="89d4f-270">Classes used in</span></span>        | [<span data-ttu-id="89d4f-271">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="89d4f-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="89d4f-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="89d4f-272">Windows Server 2012</span></span>



| <span data-ttu-id="89d4f-273">Eingabe</span><span class="sxs-lookup"><span data-stu-id="89d4f-273">Entry</span></span> | <span data-ttu-id="89d4f-274">Wert</span><span class="sxs-lookup"><span data-stu-id="89d4f-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="89d4f-275">Link-ID</span><span class="sxs-lookup"><span data-stu-id="89d4f-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="89d4f-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89d4f-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="89d4f-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="89d4f-277">System-Only</span></span>            | <span data-ttu-id="89d4f-278">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-278">False</span></span>                             |
| <span data-ttu-id="89d4f-279">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="89d4f-279">Is-Single-Valued</span></span>       | <span data-ttu-id="89d4f-280">Richtig</span><span class="sxs-lookup"><span data-stu-id="89d4f-280">True</span></span>                              |
| <span data-ttu-id="89d4f-281">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="89d4f-281">Is Indexed</span></span>             | <span data-ttu-id="89d4f-282">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-282">False</span></span>                             |
| <span data-ttu-id="89d4f-283">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="89d4f-283">In Global Catalog</span></span>      | <span data-ttu-id="89d4f-284">False</span><span class="sxs-lookup"><span data-stu-id="89d4f-284">False</span></span>                             |
| <span data-ttu-id="89d4f-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="89d4f-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="89d4f-286">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="89d4f-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="89d4f-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89d4f-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="89d4f-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89d4f-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="89d4f-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89d4f-289">Search-Flags</span></span>           | <span data-ttu-id="89d4f-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89d4f-290">0x00000000</span></span>                        |
| <span data-ttu-id="89d4f-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89d4f-291">System-Flags</span></span>           | <span data-ttu-id="89d4f-292">0x00000011</span><span class="sxs-lookup"><span data-stu-id="89d4f-292">0x00000011</span></span>                        |
| <span data-ttu-id="89d4f-293">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="89d4f-293">Classes used in</span></span>        | [<span data-ttu-id="89d4f-294">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="89d4f-294">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="89d4f-295">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89d4f-295">Remarks</span></span>

<span data-ttu-id="89d4f-296">Dieses Attribut wird nicht repliziert und auf jedem Domänen Controller in der Domäne separat verwaltet.</span><span class="sxs-lookup"><span data-stu-id="89d4f-296">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span>

<span data-ttu-id="89d4f-297">Dieses Attribut wird auf einem bestimmten Domänen Controller zurückgesetzt, wenn sich der Benutzer erfolgreich auf diesem Domänen Controller anmeldet.</span><span class="sxs-lookup"><span data-stu-id="89d4f-297">This attribute is reset on a specific domain controller when the user successfully logs onto that domain controller.</span></span>

 

 





