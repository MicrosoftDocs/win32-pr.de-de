---
title: User-Parameters-Attribut
description: Parameter des Benutzers.
ms.assetid: e3d6d22d-5112-4dfe-af55-a17a63e5f2e4
ms.tgt_platform: multiple
keywords:
- AD-Schema für User-Parameters-Attribut
- userparameters-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- User-Parameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c1d593f0a655dea4fa3ddb25753de712ab83cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519959"
---
# <a name="user-parameters-attribute"></a><span data-ttu-id="96cba-105">User-Parameters-Attribut</span><span class="sxs-lookup"><span data-stu-id="96cba-105">User-Parameters attribute</span></span>

<span data-ttu-id="96cba-106">Parameter des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="96cba-106">Parameters of the user.</span></span> <span data-ttu-id="96cba-107">Verweist auf eine Unicode-Zeichenfolge, die für die Verwendung durch Anwendungen reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="96cba-107">Points to a Unicode string that is set aside for use by applications.</span></span> <span data-ttu-id="96cba-108">Diese Zeichenfolge kann eine NULL-Zeichenfolge oder eine beliebige Anzahl von Zeichen vor dem abschließenden NULL-Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="96cba-108">This string can be a null string, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="96cba-109">Microsoft-Produkte verwenden dieses Mitglied zum Speichern von Benutzerdaten, die für das jeweilige Programm spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="96cba-109">Microsoft products use this member to store user data specific to the individual program.</span></span>



| <span data-ttu-id="96cba-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96cba-110">Entry</span></span> | <span data-ttu-id="96cba-111">Wert</span><span class="sxs-lookup"><span data-stu-id="96cba-111">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="96cba-112">CN</span><span class="sxs-lookup"><span data-stu-id="96cba-112">CN</span></span>                | <span data-ttu-id="96cba-113">User-Parameters</span><span class="sxs-lookup"><span data-stu-id="96cba-113">User-Parameters</span></span>                             |
| <span data-ttu-id="96cba-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="96cba-114">Ldap-Display-Name</span></span> | <span data-ttu-id="96cba-115">userparameters</span><span class="sxs-lookup"><span data-stu-id="96cba-115">userParameters</span></span>                              |
| <span data-ttu-id="96cba-116">Size</span><span class="sxs-lookup"><span data-stu-id="96cba-116">Size</span></span>              | \-                                          |
| <span data-ttu-id="96cba-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="96cba-117">Update Privilege</span></span>  | <span data-ttu-id="96cba-118">Geändert von Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="96cba-118">Modified by applications.</span></span>                   |
| <span data-ttu-id="96cba-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="96cba-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="96cba-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="96cba-120">Attribute-Id</span></span>      | <span data-ttu-id="96cba-121">1.2.840.113556.1.4.138</span><span class="sxs-lookup"><span data-stu-id="96cba-121">1.2.840.113556.1.4.138</span></span>                      |
| <span data-ttu-id="96cba-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="96cba-122">System-Id-Guid</span></span>    | <span data-ttu-id="96cba-123">bf967a6d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="96cba-123">bf967a6d-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="96cba-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="96cba-124">Syntax</span></span>            | [<span data-ttu-id="96cba-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="96cba-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="96cba-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="96cba-126">Implementations</span></span>

-   [<span data-ttu-id="96cba-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="96cba-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="96cba-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="96cba-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="96cba-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="96cba-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="96cba-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="96cba-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="96cba-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="96cba-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="96cba-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="96cba-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="96cba-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="96cba-133">Windows 2000 Server</span></span>



| <span data-ttu-id="96cba-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96cba-134">Entry</span></span> | <span data-ttu-id="96cba-135">Wert</span><span class="sxs-lookup"><span data-stu-id="96cba-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96cba-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96cba-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96cba-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96cba-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96cba-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="96cba-138">System-Only</span></span>            | <span data-ttu-id="96cba-139">False</span><span class="sxs-lookup"><span data-stu-id="96cba-139">False</span></span>                             |
| <span data-ttu-id="96cba-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96cba-140">Is-Single-Valued</span></span>       | <span data-ttu-id="96cba-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="96cba-141">True</span></span>                              |
| <span data-ttu-id="96cba-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96cba-142">Is Indexed</span></span>             | <span data-ttu-id="96cba-143">False</span><span class="sxs-lookup"><span data-stu-id="96cba-143">False</span></span>                             |
| <span data-ttu-id="96cba-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96cba-144">In Global Catalog</span></span>      | <span data-ttu-id="96cba-145">False</span><span class="sxs-lookup"><span data-stu-id="96cba-145">False</span></span>                             |
| <span data-ttu-id="96cba-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96cba-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="96cba-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96cba-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96cba-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96cba-148">Range-Lower</span></span>            | <span data-ttu-id="96cba-149">0</span><span class="sxs-lookup"><span data-stu-id="96cba-149">0</span></span>                                 |
| <span data-ttu-id="96cba-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96cba-150">Range-Upper</span></span>            | <span data-ttu-id="96cba-151">32767</span><span class="sxs-lookup"><span data-stu-id="96cba-151">32767</span></span>                             |
| <span data-ttu-id="96cba-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96cba-152">Search-Flags</span></span>           | <span data-ttu-id="96cba-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96cba-153">0x00000000</span></span>                        |
| <span data-ttu-id="96cba-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96cba-154">System-Flags</span></span>           | <span data-ttu-id="96cba-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96cba-155">0x00000010</span></span>                        |
| <span data-ttu-id="96cba-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96cba-156">Classes used in</span></span>        | [<span data-ttu-id="96cba-157">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="96cba-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="96cba-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="96cba-158">Windows Server 2003</span></span>



| <span data-ttu-id="96cba-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96cba-159">Entry</span></span> | <span data-ttu-id="96cba-160">Wert</span><span class="sxs-lookup"><span data-stu-id="96cba-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96cba-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96cba-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96cba-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96cba-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96cba-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="96cba-163">System-Only</span></span>            | <span data-ttu-id="96cba-164">False</span><span class="sxs-lookup"><span data-stu-id="96cba-164">False</span></span>                             |
| <span data-ttu-id="96cba-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96cba-165">Is-Single-Valued</span></span>       | <span data-ttu-id="96cba-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="96cba-166">True</span></span>                              |
| <span data-ttu-id="96cba-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96cba-167">Is Indexed</span></span>             | <span data-ttu-id="96cba-168">False</span><span class="sxs-lookup"><span data-stu-id="96cba-168">False</span></span>                             |
| <span data-ttu-id="96cba-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96cba-169">In Global Catalog</span></span>      | <span data-ttu-id="96cba-170">False</span><span class="sxs-lookup"><span data-stu-id="96cba-170">False</span></span>                             |
| <span data-ttu-id="96cba-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96cba-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="96cba-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96cba-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96cba-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96cba-173">Range-Lower</span></span>            | <span data-ttu-id="96cba-174">0</span><span class="sxs-lookup"><span data-stu-id="96cba-174">0</span></span>                                 |
| <span data-ttu-id="96cba-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96cba-175">Range-Upper</span></span>            | <span data-ttu-id="96cba-176">32767</span><span class="sxs-lookup"><span data-stu-id="96cba-176">32767</span></span>                             |
| <span data-ttu-id="96cba-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96cba-177">Search-Flags</span></span>           | <span data-ttu-id="96cba-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96cba-178">0x00000000</span></span>                        |
| <span data-ttu-id="96cba-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96cba-179">System-Flags</span></span>           | <span data-ttu-id="96cba-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96cba-180">0x00000010</span></span>                        |
| <span data-ttu-id="96cba-181">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96cba-181">Classes used in</span></span>        | [<span data-ttu-id="96cba-182">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="96cba-182">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="96cba-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="96cba-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="96cba-184">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96cba-184">Entry</span></span> | <span data-ttu-id="96cba-185">Wert</span><span class="sxs-lookup"><span data-stu-id="96cba-185">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96cba-186">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96cba-186">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96cba-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96cba-187">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96cba-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="96cba-188">System-Only</span></span>            | <span data-ttu-id="96cba-189">False</span><span class="sxs-lookup"><span data-stu-id="96cba-189">False</span></span>                             |
| <span data-ttu-id="96cba-190">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96cba-190">Is-Single-Valued</span></span>       | <span data-ttu-id="96cba-191">Richtig</span><span class="sxs-lookup"><span data-stu-id="96cba-191">True</span></span>                              |
| <span data-ttu-id="96cba-192">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96cba-192">Is Indexed</span></span>             | <span data-ttu-id="96cba-193">False</span><span class="sxs-lookup"><span data-stu-id="96cba-193">False</span></span>                             |
| <span data-ttu-id="96cba-194">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96cba-194">In Global Catalog</span></span>      | <span data-ttu-id="96cba-195">False</span><span class="sxs-lookup"><span data-stu-id="96cba-195">False</span></span>                             |
| <span data-ttu-id="96cba-196">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96cba-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="96cba-197">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96cba-197">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96cba-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96cba-198">Range-Lower</span></span>            | <span data-ttu-id="96cba-199">0</span><span class="sxs-lookup"><span data-stu-id="96cba-199">0</span></span>                                 |
| <span data-ttu-id="96cba-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96cba-200">Range-Upper</span></span>            | <span data-ttu-id="96cba-201">32767</span><span class="sxs-lookup"><span data-stu-id="96cba-201">32767</span></span>                             |
| <span data-ttu-id="96cba-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96cba-202">Search-Flags</span></span>           | <span data-ttu-id="96cba-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96cba-203">0x00000000</span></span>                        |
| <span data-ttu-id="96cba-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96cba-204">System-Flags</span></span>           | <span data-ttu-id="96cba-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96cba-205">0x00000010</span></span>                        |
| <span data-ttu-id="96cba-206">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96cba-206">Classes used in</span></span>        | [<span data-ttu-id="96cba-207">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="96cba-207">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="96cba-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96cba-208">Windows Server 2008</span></span>



| <span data-ttu-id="96cba-209">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96cba-209">Entry</span></span> | <span data-ttu-id="96cba-210">Wert</span><span class="sxs-lookup"><span data-stu-id="96cba-210">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96cba-211">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96cba-211">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96cba-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96cba-212">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96cba-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="96cba-213">System-Only</span></span>            | <span data-ttu-id="96cba-214">False</span><span class="sxs-lookup"><span data-stu-id="96cba-214">False</span></span>                             |
| <span data-ttu-id="96cba-215">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96cba-215">Is-Single-Valued</span></span>       | <span data-ttu-id="96cba-216">Richtig</span><span class="sxs-lookup"><span data-stu-id="96cba-216">True</span></span>                              |
| <span data-ttu-id="96cba-217">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96cba-217">Is Indexed</span></span>             | <span data-ttu-id="96cba-218">False</span><span class="sxs-lookup"><span data-stu-id="96cba-218">False</span></span>                             |
| <span data-ttu-id="96cba-219">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96cba-219">In Global Catalog</span></span>      | <span data-ttu-id="96cba-220">False</span><span class="sxs-lookup"><span data-stu-id="96cba-220">False</span></span>                             |
| <span data-ttu-id="96cba-221">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96cba-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="96cba-222">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96cba-222">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96cba-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96cba-223">Range-Lower</span></span>            | <span data-ttu-id="96cba-224">0</span><span class="sxs-lookup"><span data-stu-id="96cba-224">0</span></span>                                 |
| <span data-ttu-id="96cba-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96cba-225">Range-Upper</span></span>            | <span data-ttu-id="96cba-226">32767</span><span class="sxs-lookup"><span data-stu-id="96cba-226">32767</span></span>                             |
| <span data-ttu-id="96cba-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96cba-227">Search-Flags</span></span>           | <span data-ttu-id="96cba-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96cba-228">0x00000000</span></span>                        |
| <span data-ttu-id="96cba-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96cba-229">System-Flags</span></span>           | <span data-ttu-id="96cba-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96cba-230">0x00000010</span></span>                        |
| <span data-ttu-id="96cba-231">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96cba-231">Classes used in</span></span>        | [<span data-ttu-id="96cba-232">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="96cba-232">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="96cba-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="96cba-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="96cba-234">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96cba-234">Entry</span></span> | <span data-ttu-id="96cba-235">Wert</span><span class="sxs-lookup"><span data-stu-id="96cba-235">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96cba-236">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96cba-236">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96cba-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96cba-237">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96cba-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="96cba-238">System-Only</span></span>            | <span data-ttu-id="96cba-239">False</span><span class="sxs-lookup"><span data-stu-id="96cba-239">False</span></span>                             |
| <span data-ttu-id="96cba-240">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96cba-240">Is-Single-Valued</span></span>       | <span data-ttu-id="96cba-241">Richtig</span><span class="sxs-lookup"><span data-stu-id="96cba-241">True</span></span>                              |
| <span data-ttu-id="96cba-242">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96cba-242">Is Indexed</span></span>             | <span data-ttu-id="96cba-243">False</span><span class="sxs-lookup"><span data-stu-id="96cba-243">False</span></span>                             |
| <span data-ttu-id="96cba-244">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96cba-244">In Global Catalog</span></span>      | <span data-ttu-id="96cba-245">False</span><span class="sxs-lookup"><span data-stu-id="96cba-245">False</span></span>                             |
| <span data-ttu-id="96cba-246">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96cba-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="96cba-247">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96cba-247">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96cba-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96cba-248">Range-Lower</span></span>            | <span data-ttu-id="96cba-249">0</span><span class="sxs-lookup"><span data-stu-id="96cba-249">0</span></span>                                 |
| <span data-ttu-id="96cba-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96cba-250">Range-Upper</span></span>            | <span data-ttu-id="96cba-251">32767</span><span class="sxs-lookup"><span data-stu-id="96cba-251">32767</span></span>                             |
| <span data-ttu-id="96cba-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96cba-252">Search-Flags</span></span>           | <span data-ttu-id="96cba-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96cba-253">0x00000000</span></span>                        |
| <span data-ttu-id="96cba-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96cba-254">System-Flags</span></span>           | <span data-ttu-id="96cba-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96cba-255">0x00000010</span></span>                        |
| <span data-ttu-id="96cba-256">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96cba-256">Classes used in</span></span>        | [<span data-ttu-id="96cba-257">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="96cba-257">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="96cba-258">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="96cba-258">Windows Server 2012</span></span>



| <span data-ttu-id="96cba-259">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96cba-259">Entry</span></span> | <span data-ttu-id="96cba-260">Wert</span><span class="sxs-lookup"><span data-stu-id="96cba-260">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96cba-261">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96cba-261">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96cba-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96cba-262">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96cba-263">System-Only</span><span class="sxs-lookup"><span data-stu-id="96cba-263">System-Only</span></span>            | <span data-ttu-id="96cba-264">False</span><span class="sxs-lookup"><span data-stu-id="96cba-264">False</span></span>                             |
| <span data-ttu-id="96cba-265">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96cba-265">Is-Single-Valued</span></span>       | <span data-ttu-id="96cba-266">Richtig</span><span class="sxs-lookup"><span data-stu-id="96cba-266">True</span></span>                              |
| <span data-ttu-id="96cba-267">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96cba-267">Is Indexed</span></span>             | <span data-ttu-id="96cba-268">False</span><span class="sxs-lookup"><span data-stu-id="96cba-268">False</span></span>                             |
| <span data-ttu-id="96cba-269">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96cba-269">In Global Catalog</span></span>      | <span data-ttu-id="96cba-270">False</span><span class="sxs-lookup"><span data-stu-id="96cba-270">False</span></span>                             |
| <span data-ttu-id="96cba-271">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96cba-271">NT-Security-Descriptor</span></span> | <span data-ttu-id="96cba-272">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96cba-272">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96cba-273">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96cba-273">Range-Lower</span></span>            | <span data-ttu-id="96cba-274">0</span><span class="sxs-lookup"><span data-stu-id="96cba-274">0</span></span>                                 |
| <span data-ttu-id="96cba-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96cba-275">Range-Upper</span></span>            | <span data-ttu-id="96cba-276">32767</span><span class="sxs-lookup"><span data-stu-id="96cba-276">32767</span></span>                             |
| <span data-ttu-id="96cba-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96cba-277">Search-Flags</span></span>           | <span data-ttu-id="96cba-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96cba-278">0x00000000</span></span>                        |
| <span data-ttu-id="96cba-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96cba-279">System-Flags</span></span>           | <span data-ttu-id="96cba-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96cba-280">0x00000010</span></span>                        |
| <span data-ttu-id="96cba-281">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96cba-281">Classes used in</span></span>        | [<span data-ttu-id="96cba-282">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="96cba-282">**User**</span></span>](c-user.md)<br/> |



 

 





