---
title: Script-Path-Attribut
description: Dieses Attribut gibt den Pfad für das Anmelde Skript des Benutzers an. Die Zeichenfolge kann NULL sein.
ms.assetid: 356f2ba0-ceca-4805-a536-286c6a8b54fc
ms.tgt_platform: multiple
keywords:
- AD-Schema für Script-Path-Attribut
- AD-Schema für ScriptPath-Attribut
topic_type:
- apiref
api_name:
- Script-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0909c35c41ae65f75481910d1377aa2761e99487
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122683"
---
# <a name="script-path-attribute"></a><span data-ttu-id="6d551-106">Script-Path-Attribut</span><span class="sxs-lookup"><span data-stu-id="6d551-106">Script-Path attribute</span></span>

<span data-ttu-id="6d551-107">Dieses Attribut gibt den Pfad für das Anmelde Skript des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="6d551-107">This attribute specifies the path for the user's logon script.</span></span> <span data-ttu-id="6d551-108">Die Zeichenfolge kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="6d551-108">The string can be null.</span></span>



| <span data-ttu-id="6d551-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d551-109">Entry</span></span> | <span data-ttu-id="6d551-110">Wert</span><span class="sxs-lookup"><span data-stu-id="6d551-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6d551-111">CN</span><span class="sxs-lookup"><span data-stu-id="6d551-111">CN</span></span>                | <span data-ttu-id="6d551-112">Script-Path</span><span class="sxs-lookup"><span data-stu-id="6d551-112">Script-Path</span></span>                                                            |
| <span data-ttu-id="6d551-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6d551-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6d551-114">scriptPath</span><span class="sxs-lookup"><span data-stu-id="6d551-114">scriptPath</span></span>                                                             |
| <span data-ttu-id="6d551-115">Size</span><span class="sxs-lookup"><span data-stu-id="6d551-115">Size</span></span>              | \-                                                                     |
| <span data-ttu-id="6d551-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="6d551-116">Update Privilege</span></span>  | <span data-ttu-id="6d551-117">Domänen Administrator oder Konto Besitzer.</span><span class="sxs-lookup"><span data-stu-id="6d551-117">Domain administrator or account owner.</span></span>                                 |
| <span data-ttu-id="6d551-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="6d551-118">Update Frequency</span></span>  | <span data-ttu-id="6d551-119">Wenn der Benutzerdaten Satz erstellt und der Pfad geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="6d551-119">When the user record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="6d551-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6d551-120">Attribute-Id</span></span>      | <span data-ttu-id="6d551-121">1.2.840.113556.1.4.62</span><span class="sxs-lookup"><span data-stu-id="6d551-121">1.2.840.113556.1.4.62</span></span>                                                  |
| <span data-ttu-id="6d551-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6d551-122">System-Id-Guid</span></span>    | <span data-ttu-id="6d551-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6d551-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span></span>                                   |
| <span data-ttu-id="6d551-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d551-124">Syntax</span></span>            | [<span data-ttu-id="6d551-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6d551-125">**String(Unicode)**</span></span>](s-string-unicode.md)                            |



## <a name="implementations"></a><span data-ttu-id="6d551-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="6d551-126">Implementations</span></span>

-   [<span data-ttu-id="6d551-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6d551-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6d551-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6d551-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6d551-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6d551-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6d551-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6d551-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6d551-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6d551-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6d551-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6d551-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6d551-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6d551-133">Windows 2000 Server</span></span>



| <span data-ttu-id="6d551-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d551-134">Entry</span></span> | <span data-ttu-id="6d551-135">Wert</span><span class="sxs-lookup"><span data-stu-id="6d551-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d551-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d551-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d551-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d551-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d551-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d551-138">System-Only</span></span>            | <span data-ttu-id="6d551-139">False</span><span class="sxs-lookup"><span data-stu-id="6d551-139">False</span></span>                             |
| <span data-ttu-id="6d551-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d551-140">Is-Single-Valued</span></span>       | <span data-ttu-id="6d551-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d551-141">True</span></span>                              |
| <span data-ttu-id="6d551-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d551-142">Is Indexed</span></span>             | <span data-ttu-id="6d551-143">False</span><span class="sxs-lookup"><span data-stu-id="6d551-143">False</span></span>                             |
| <span data-ttu-id="6d551-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d551-144">In Global Catalog</span></span>      | <span data-ttu-id="6d551-145">False</span><span class="sxs-lookup"><span data-stu-id="6d551-145">False</span></span>                             |
| <span data-ttu-id="6d551-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d551-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d551-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d551-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d551-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d551-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d551-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d551-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d551-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d551-150">Search-Flags</span></span>           | <span data-ttu-id="6d551-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d551-151">0x00000010</span></span>                        |
| <span data-ttu-id="6d551-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d551-152">System-Flags</span></span>           | <span data-ttu-id="6d551-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d551-153">0x00000010</span></span>                        |
| <span data-ttu-id="6d551-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d551-154">Classes used in</span></span>        | [<span data-ttu-id="6d551-155">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="6d551-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6d551-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6d551-156">Windows Server 2003</span></span>



| <span data-ttu-id="6d551-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d551-157">Entry</span></span> | <span data-ttu-id="6d551-158">Wert</span><span class="sxs-lookup"><span data-stu-id="6d551-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d551-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d551-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d551-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d551-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d551-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d551-161">System-Only</span></span>            | <span data-ttu-id="6d551-162">False</span><span class="sxs-lookup"><span data-stu-id="6d551-162">False</span></span>                             |
| <span data-ttu-id="6d551-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d551-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6d551-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d551-164">True</span></span>                              |
| <span data-ttu-id="6d551-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d551-165">Is Indexed</span></span>             | <span data-ttu-id="6d551-166">False</span><span class="sxs-lookup"><span data-stu-id="6d551-166">False</span></span>                             |
| <span data-ttu-id="6d551-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d551-167">In Global Catalog</span></span>      | <span data-ttu-id="6d551-168">False</span><span class="sxs-lookup"><span data-stu-id="6d551-168">False</span></span>                             |
| <span data-ttu-id="6d551-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d551-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d551-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d551-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d551-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d551-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d551-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d551-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d551-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d551-173">Search-Flags</span></span>           | <span data-ttu-id="6d551-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d551-174">0x00000010</span></span>                        |
| <span data-ttu-id="6d551-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d551-175">System-Flags</span></span>           | <span data-ttu-id="6d551-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d551-176">0x00000010</span></span>                        |
| <span data-ttu-id="6d551-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d551-177">Classes used in</span></span>        | [<span data-ttu-id="6d551-178">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="6d551-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6d551-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6d551-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6d551-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d551-180">Entry</span></span> | <span data-ttu-id="6d551-181">Wert</span><span class="sxs-lookup"><span data-stu-id="6d551-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d551-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d551-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d551-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d551-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d551-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d551-184">System-Only</span></span>            | <span data-ttu-id="6d551-185">False</span><span class="sxs-lookup"><span data-stu-id="6d551-185">False</span></span>                             |
| <span data-ttu-id="6d551-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d551-186">Is-Single-Valued</span></span>       | <span data-ttu-id="6d551-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d551-187">True</span></span>                              |
| <span data-ttu-id="6d551-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d551-188">Is Indexed</span></span>             | <span data-ttu-id="6d551-189">False</span><span class="sxs-lookup"><span data-stu-id="6d551-189">False</span></span>                             |
| <span data-ttu-id="6d551-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d551-190">In Global Catalog</span></span>      | <span data-ttu-id="6d551-191">False</span><span class="sxs-lookup"><span data-stu-id="6d551-191">False</span></span>                             |
| <span data-ttu-id="6d551-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d551-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d551-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d551-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d551-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d551-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d551-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d551-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d551-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d551-196">Search-Flags</span></span>           | <span data-ttu-id="6d551-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d551-197">0x00000010</span></span>                        |
| <span data-ttu-id="6d551-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d551-198">System-Flags</span></span>           | <span data-ttu-id="6d551-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d551-199">0x00000010</span></span>                        |
| <span data-ttu-id="6d551-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d551-200">Classes used in</span></span>        | [<span data-ttu-id="6d551-201">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="6d551-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6d551-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d551-202">Windows Server 2008</span></span>



| <span data-ttu-id="6d551-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d551-203">Entry</span></span> | <span data-ttu-id="6d551-204">Wert</span><span class="sxs-lookup"><span data-stu-id="6d551-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d551-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d551-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d551-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d551-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d551-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d551-207">System-Only</span></span>            | <span data-ttu-id="6d551-208">False</span><span class="sxs-lookup"><span data-stu-id="6d551-208">False</span></span>                             |
| <span data-ttu-id="6d551-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d551-209">Is-Single-Valued</span></span>       | <span data-ttu-id="6d551-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d551-210">True</span></span>                              |
| <span data-ttu-id="6d551-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d551-211">Is Indexed</span></span>             | <span data-ttu-id="6d551-212">False</span><span class="sxs-lookup"><span data-stu-id="6d551-212">False</span></span>                             |
| <span data-ttu-id="6d551-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d551-213">In Global Catalog</span></span>      | <span data-ttu-id="6d551-214">False</span><span class="sxs-lookup"><span data-stu-id="6d551-214">False</span></span>                             |
| <span data-ttu-id="6d551-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d551-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d551-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d551-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d551-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d551-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d551-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d551-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d551-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d551-219">Search-Flags</span></span>           | <span data-ttu-id="6d551-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d551-220">0x00000010</span></span>                        |
| <span data-ttu-id="6d551-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d551-221">System-Flags</span></span>           | <span data-ttu-id="6d551-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d551-222">0x00000010</span></span>                        |
| <span data-ttu-id="6d551-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d551-223">Classes used in</span></span>        | [<span data-ttu-id="6d551-224">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="6d551-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6d551-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6d551-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6d551-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d551-226">Entry</span></span> | <span data-ttu-id="6d551-227">Wert</span><span class="sxs-lookup"><span data-stu-id="6d551-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d551-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d551-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d551-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d551-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d551-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d551-230">System-Only</span></span>            | <span data-ttu-id="6d551-231">False</span><span class="sxs-lookup"><span data-stu-id="6d551-231">False</span></span>                             |
| <span data-ttu-id="6d551-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d551-232">Is-Single-Valued</span></span>       | <span data-ttu-id="6d551-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d551-233">True</span></span>                              |
| <span data-ttu-id="6d551-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d551-234">Is Indexed</span></span>             | <span data-ttu-id="6d551-235">False</span><span class="sxs-lookup"><span data-stu-id="6d551-235">False</span></span>                             |
| <span data-ttu-id="6d551-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d551-236">In Global Catalog</span></span>      | <span data-ttu-id="6d551-237">False</span><span class="sxs-lookup"><span data-stu-id="6d551-237">False</span></span>                             |
| <span data-ttu-id="6d551-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d551-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d551-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d551-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d551-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d551-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d551-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d551-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d551-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d551-242">Search-Flags</span></span>           | <span data-ttu-id="6d551-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d551-243">0x00000010</span></span>                        |
| <span data-ttu-id="6d551-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d551-244">System-Flags</span></span>           | <span data-ttu-id="6d551-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d551-245">0x00000010</span></span>                        |
| <span data-ttu-id="6d551-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d551-246">Classes used in</span></span>        | [<span data-ttu-id="6d551-247">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="6d551-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6d551-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6d551-248">Windows Server 2012</span></span>



| <span data-ttu-id="6d551-249">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d551-249">Entry</span></span> | <span data-ttu-id="6d551-250">Wert</span><span class="sxs-lookup"><span data-stu-id="6d551-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d551-251">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d551-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d551-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d551-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d551-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d551-253">System-Only</span></span>            | <span data-ttu-id="6d551-254">False</span><span class="sxs-lookup"><span data-stu-id="6d551-254">False</span></span>                             |
| <span data-ttu-id="6d551-255">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d551-255">Is-Single-Valued</span></span>       | <span data-ttu-id="6d551-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d551-256">True</span></span>                              |
| <span data-ttu-id="6d551-257">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d551-257">Is Indexed</span></span>             | <span data-ttu-id="6d551-258">False</span><span class="sxs-lookup"><span data-stu-id="6d551-258">False</span></span>                             |
| <span data-ttu-id="6d551-259">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d551-259">In Global Catalog</span></span>      | <span data-ttu-id="6d551-260">False</span><span class="sxs-lookup"><span data-stu-id="6d551-260">False</span></span>                             |
| <span data-ttu-id="6d551-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d551-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d551-262">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d551-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d551-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d551-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d551-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d551-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d551-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d551-265">Search-Flags</span></span>           | <span data-ttu-id="6d551-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d551-266">0x00000010</span></span>                        |
| <span data-ttu-id="6d551-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d551-267">System-Flags</span></span>           | <span data-ttu-id="6d551-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d551-268">0x00000010</span></span>                        |
| <span data-ttu-id="6d551-269">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d551-269">Classes used in</span></span>        | [<span data-ttu-id="6d551-270">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="6d551-270">**User**</span></span>](c-user.md)<br/> |



 

 





