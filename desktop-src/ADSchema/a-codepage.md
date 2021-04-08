---
title: Code-Page-Attribut
description: Gibt die Codepage für die Sprache des Benutzers an. Dieser Wert wird von Windows 2000 nicht verwendet.
ms.assetid: f98e6fbe-0c9a-4ee0-8158-3eaaca359675
ms.tgt_platform: multiple
keywords:
- AD-Schema für Code-Page-Attribut
- Codepage-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Code-Page
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c3e9858ba387b98d5556c6010490c024be836b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744401"
---
# <a name="code-page-attribute"></a><span data-ttu-id="2164d-106">Code-Page-Attribut</span><span class="sxs-lookup"><span data-stu-id="2164d-106">Code-Page attribute</span></span>

<span data-ttu-id="2164d-107">Gibt die Codepage für die Sprache des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="2164d-107">Specifies the code page for the user's language of choice.</span></span> <span data-ttu-id="2164d-108">Dieser Wert wird von Windows 2000 nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2164d-108">This value is not used by Windows 2000.</span></span>



| <span data-ttu-id="2164d-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2164d-109">Entry</span></span> | <span data-ttu-id="2164d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="2164d-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="2164d-111">CN</span><span class="sxs-lookup"><span data-stu-id="2164d-111">CN</span></span>                | <span data-ttu-id="2164d-112">Code-Page</span><span class="sxs-lookup"><span data-stu-id="2164d-112">Code-Page</span></span>                                             |
| <span data-ttu-id="2164d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2164d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="2164d-114">Codepage</span><span class="sxs-lookup"><span data-stu-id="2164d-114">codePage</span></span>                                              |
| <span data-ttu-id="2164d-115">Size</span><span class="sxs-lookup"><span data-stu-id="2164d-115">Size</span></span>              | <span data-ttu-id="2164d-116">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="2164d-116">4 bytes</span></span>                                               |
| <span data-ttu-id="2164d-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2164d-117">Update Privilege</span></span>  | <span data-ttu-id="2164d-118">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="2164d-118">Domain administrator</span></span>                                  |
| <span data-ttu-id="2164d-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="2164d-119">Update Frequency</span></span>  | <span data-ttu-id="2164d-120">, Wenn der Benutzer die Standardsprache ändern möchte.</span><span class="sxs-lookup"><span data-stu-id="2164d-120">When the user desires to change the default language.</span></span> |
| <span data-ttu-id="2164d-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2164d-121">Attribute-Id</span></span>      | <span data-ttu-id="2164d-122">1.2.840.113556.1.4.16</span><span class="sxs-lookup"><span data-stu-id="2164d-122">1.2.840.113556.1.4.16</span></span>                                 |
| <span data-ttu-id="2164d-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2164d-123">System-Id-Guid</span></span>    | <span data-ttu-id="2164d-124">bf967938-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2164d-124">bf967938-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="2164d-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="2164d-125">Syntax</span></span>            | [<span data-ttu-id="2164d-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="2164d-126">**Enumeration**</span></span>](s-enumeration.md)                  |



## <a name="implementations"></a><span data-ttu-id="2164d-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="2164d-127">Implementations</span></span>

-   [<span data-ttu-id="2164d-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2164d-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2164d-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2164d-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2164d-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2164d-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2164d-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2164d-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2164d-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2164d-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2164d-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2164d-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2164d-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2164d-134">Windows 2000 Server</span></span>



| <span data-ttu-id="2164d-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2164d-135">Entry</span></span> | <span data-ttu-id="2164d-136">Wert</span><span class="sxs-lookup"><span data-stu-id="2164d-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2164d-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2164d-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2164d-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2164d-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2164d-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="2164d-139">System-Only</span></span>            | <span data-ttu-id="2164d-140">False</span><span class="sxs-lookup"><span data-stu-id="2164d-140">False</span></span>                             |
| <span data-ttu-id="2164d-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2164d-141">Is-Single-Valued</span></span>       | <span data-ttu-id="2164d-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="2164d-142">True</span></span>                              |
| <span data-ttu-id="2164d-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2164d-143">Is Indexed</span></span>             | <span data-ttu-id="2164d-144">False</span><span class="sxs-lookup"><span data-stu-id="2164d-144">False</span></span>                             |
| <span data-ttu-id="2164d-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2164d-145">In Global Catalog</span></span>      | <span data-ttu-id="2164d-146">False</span><span class="sxs-lookup"><span data-stu-id="2164d-146">False</span></span>                             |
| <span data-ttu-id="2164d-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2164d-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="2164d-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2164d-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2164d-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2164d-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2164d-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2164d-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2164d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2164d-151">Search-Flags</span></span>           | <span data-ttu-id="2164d-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2164d-152">0x00000010</span></span>                        |
| <span data-ttu-id="2164d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2164d-153">System-Flags</span></span>           | <span data-ttu-id="2164d-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2164d-154">0x00000010</span></span>                        |
| <span data-ttu-id="2164d-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2164d-155">Classes used in</span></span>        | [<span data-ttu-id="2164d-156">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2164d-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2164d-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2164d-157">Windows Server 2003</span></span>



| <span data-ttu-id="2164d-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2164d-158">Entry</span></span> | <span data-ttu-id="2164d-159">Wert</span><span class="sxs-lookup"><span data-stu-id="2164d-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2164d-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2164d-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2164d-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2164d-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2164d-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="2164d-162">System-Only</span></span>            | <span data-ttu-id="2164d-163">False</span><span class="sxs-lookup"><span data-stu-id="2164d-163">False</span></span>                             |
| <span data-ttu-id="2164d-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2164d-164">Is-Single-Valued</span></span>       | <span data-ttu-id="2164d-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="2164d-165">True</span></span>                              |
| <span data-ttu-id="2164d-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2164d-166">Is Indexed</span></span>             | <span data-ttu-id="2164d-167">False</span><span class="sxs-lookup"><span data-stu-id="2164d-167">False</span></span>                             |
| <span data-ttu-id="2164d-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2164d-168">In Global Catalog</span></span>      | <span data-ttu-id="2164d-169">False</span><span class="sxs-lookup"><span data-stu-id="2164d-169">False</span></span>                             |
| <span data-ttu-id="2164d-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2164d-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="2164d-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2164d-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2164d-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2164d-172">Range-Lower</span></span>            | <span data-ttu-id="2164d-173">0</span><span class="sxs-lookup"><span data-stu-id="2164d-173">0</span></span>                                 |
| <span data-ttu-id="2164d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2164d-174">Range-Upper</span></span>            | <span data-ttu-id="2164d-175">65.535</span><span class="sxs-lookup"><span data-stu-id="2164d-175">65535</span></span>                             |
| <span data-ttu-id="2164d-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2164d-176">Search-Flags</span></span>           | <span data-ttu-id="2164d-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2164d-177">0x00000010</span></span>                        |
| <span data-ttu-id="2164d-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2164d-178">System-Flags</span></span>           | <span data-ttu-id="2164d-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2164d-179">0x00000010</span></span>                        |
| <span data-ttu-id="2164d-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2164d-180">Classes used in</span></span>        | [<span data-ttu-id="2164d-181">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2164d-181">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2164d-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2164d-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2164d-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2164d-183">Entry</span></span> | <span data-ttu-id="2164d-184">Wert</span><span class="sxs-lookup"><span data-stu-id="2164d-184">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2164d-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2164d-185">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2164d-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2164d-186">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2164d-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="2164d-187">System-Only</span></span>            | <span data-ttu-id="2164d-188">False</span><span class="sxs-lookup"><span data-stu-id="2164d-188">False</span></span>                             |
| <span data-ttu-id="2164d-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2164d-189">Is-Single-Valued</span></span>       | <span data-ttu-id="2164d-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="2164d-190">True</span></span>                              |
| <span data-ttu-id="2164d-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2164d-191">Is Indexed</span></span>             | <span data-ttu-id="2164d-192">False</span><span class="sxs-lookup"><span data-stu-id="2164d-192">False</span></span>                             |
| <span data-ttu-id="2164d-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2164d-193">In Global Catalog</span></span>      | <span data-ttu-id="2164d-194">False</span><span class="sxs-lookup"><span data-stu-id="2164d-194">False</span></span>                             |
| <span data-ttu-id="2164d-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2164d-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="2164d-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2164d-196">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2164d-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2164d-197">Range-Lower</span></span>            | <span data-ttu-id="2164d-198">0</span><span class="sxs-lookup"><span data-stu-id="2164d-198">0</span></span>                                 |
| <span data-ttu-id="2164d-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2164d-199">Range-Upper</span></span>            | <span data-ttu-id="2164d-200">65.535</span><span class="sxs-lookup"><span data-stu-id="2164d-200">65535</span></span>                             |
| <span data-ttu-id="2164d-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2164d-201">Search-Flags</span></span>           | <span data-ttu-id="2164d-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2164d-202">0x00000010</span></span>                        |
| <span data-ttu-id="2164d-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2164d-203">System-Flags</span></span>           | <span data-ttu-id="2164d-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2164d-204">0x00000010</span></span>                        |
| <span data-ttu-id="2164d-205">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2164d-205">Classes used in</span></span>        | [<span data-ttu-id="2164d-206">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2164d-206">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2164d-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2164d-207">Windows Server 2008</span></span>



| <span data-ttu-id="2164d-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2164d-208">Entry</span></span> | <span data-ttu-id="2164d-209">Wert</span><span class="sxs-lookup"><span data-stu-id="2164d-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2164d-210">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2164d-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2164d-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2164d-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2164d-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="2164d-212">System-Only</span></span>            | <span data-ttu-id="2164d-213">False</span><span class="sxs-lookup"><span data-stu-id="2164d-213">False</span></span>                             |
| <span data-ttu-id="2164d-214">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2164d-214">Is-Single-Valued</span></span>       | <span data-ttu-id="2164d-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="2164d-215">True</span></span>                              |
| <span data-ttu-id="2164d-216">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2164d-216">Is Indexed</span></span>             | <span data-ttu-id="2164d-217">False</span><span class="sxs-lookup"><span data-stu-id="2164d-217">False</span></span>                             |
| <span data-ttu-id="2164d-218">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2164d-218">In Global Catalog</span></span>      | <span data-ttu-id="2164d-219">False</span><span class="sxs-lookup"><span data-stu-id="2164d-219">False</span></span>                             |
| <span data-ttu-id="2164d-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2164d-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="2164d-221">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2164d-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2164d-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2164d-222">Range-Lower</span></span>            | <span data-ttu-id="2164d-223">0</span><span class="sxs-lookup"><span data-stu-id="2164d-223">0</span></span>                                 |
| <span data-ttu-id="2164d-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2164d-224">Range-Upper</span></span>            | <span data-ttu-id="2164d-225">65.535</span><span class="sxs-lookup"><span data-stu-id="2164d-225">65535</span></span>                             |
| <span data-ttu-id="2164d-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2164d-226">Search-Flags</span></span>           | <span data-ttu-id="2164d-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2164d-227">0x00000010</span></span>                        |
| <span data-ttu-id="2164d-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2164d-228">System-Flags</span></span>           | <span data-ttu-id="2164d-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2164d-229">0x00000010</span></span>                        |
| <span data-ttu-id="2164d-230">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2164d-230">Classes used in</span></span>        | [<span data-ttu-id="2164d-231">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2164d-231">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2164d-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2164d-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2164d-233">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2164d-233">Entry</span></span> | <span data-ttu-id="2164d-234">Wert</span><span class="sxs-lookup"><span data-stu-id="2164d-234">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2164d-235">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2164d-235">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2164d-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2164d-236">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2164d-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="2164d-237">System-Only</span></span>            | <span data-ttu-id="2164d-238">False</span><span class="sxs-lookup"><span data-stu-id="2164d-238">False</span></span>                             |
| <span data-ttu-id="2164d-239">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2164d-239">Is-Single-Valued</span></span>       | <span data-ttu-id="2164d-240">Richtig</span><span class="sxs-lookup"><span data-stu-id="2164d-240">True</span></span>                              |
| <span data-ttu-id="2164d-241">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2164d-241">Is Indexed</span></span>             | <span data-ttu-id="2164d-242">False</span><span class="sxs-lookup"><span data-stu-id="2164d-242">False</span></span>                             |
| <span data-ttu-id="2164d-243">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2164d-243">In Global Catalog</span></span>      | <span data-ttu-id="2164d-244">False</span><span class="sxs-lookup"><span data-stu-id="2164d-244">False</span></span>                             |
| <span data-ttu-id="2164d-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2164d-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="2164d-246">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2164d-246">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2164d-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2164d-247">Range-Lower</span></span>            | <span data-ttu-id="2164d-248">0</span><span class="sxs-lookup"><span data-stu-id="2164d-248">0</span></span>                                 |
| <span data-ttu-id="2164d-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2164d-249">Range-Upper</span></span>            | <span data-ttu-id="2164d-250">65.535</span><span class="sxs-lookup"><span data-stu-id="2164d-250">65535</span></span>                             |
| <span data-ttu-id="2164d-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2164d-251">Search-Flags</span></span>           | <span data-ttu-id="2164d-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2164d-252">0x00000010</span></span>                        |
| <span data-ttu-id="2164d-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2164d-253">System-Flags</span></span>           | <span data-ttu-id="2164d-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2164d-254">0x00000010</span></span>                        |
| <span data-ttu-id="2164d-255">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2164d-255">Classes used in</span></span>        | [<span data-ttu-id="2164d-256">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2164d-256">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2164d-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2164d-257">Windows Server 2012</span></span>



| <span data-ttu-id="2164d-258">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2164d-258">Entry</span></span> | <span data-ttu-id="2164d-259">Wert</span><span class="sxs-lookup"><span data-stu-id="2164d-259">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2164d-260">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2164d-260">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2164d-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2164d-261">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2164d-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="2164d-262">System-Only</span></span>            | <span data-ttu-id="2164d-263">False</span><span class="sxs-lookup"><span data-stu-id="2164d-263">False</span></span>                             |
| <span data-ttu-id="2164d-264">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2164d-264">Is-Single-Valued</span></span>       | <span data-ttu-id="2164d-265">Richtig</span><span class="sxs-lookup"><span data-stu-id="2164d-265">True</span></span>                              |
| <span data-ttu-id="2164d-266">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2164d-266">Is Indexed</span></span>             | <span data-ttu-id="2164d-267">False</span><span class="sxs-lookup"><span data-stu-id="2164d-267">False</span></span>                             |
| <span data-ttu-id="2164d-268">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2164d-268">In Global Catalog</span></span>      | <span data-ttu-id="2164d-269">False</span><span class="sxs-lookup"><span data-stu-id="2164d-269">False</span></span>                             |
| <span data-ttu-id="2164d-270">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2164d-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="2164d-271">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2164d-271">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2164d-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2164d-272">Range-Lower</span></span>            | <span data-ttu-id="2164d-273">0</span><span class="sxs-lookup"><span data-stu-id="2164d-273">0</span></span>                                 |
| <span data-ttu-id="2164d-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2164d-274">Range-Upper</span></span>            | <span data-ttu-id="2164d-275">65.535</span><span class="sxs-lookup"><span data-stu-id="2164d-275">65535</span></span>                             |
| <span data-ttu-id="2164d-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2164d-276">Search-Flags</span></span>           | <span data-ttu-id="2164d-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2164d-277">0x00000010</span></span>                        |
| <span data-ttu-id="2164d-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2164d-278">System-Flags</span></span>           | <span data-ttu-id="2164d-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2164d-279">0x00000010</span></span>                        |
| <span data-ttu-id="2164d-280">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2164d-280">Classes used in</span></span>        | [<span data-ttu-id="2164d-281">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2164d-281">**User**</span></span>](c-user.md)<br/> |



 

 





