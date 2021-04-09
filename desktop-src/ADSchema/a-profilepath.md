---
title: Profile-Path-Attribut
description: Gibt einen Pfad zum Profil des Benutzers an. Dieser Wert kann eine NULL-Zeichenfolge, ein lokaler absoluter Pfad oder ein UNC-Pfad sein.
ms.assetid: 03891152-52c6-4799-ae79-3be284204391
ms.tgt_platform: multiple
keywords:
- AD-Schema für Profile-Path-Attribut
- AD-Schema des ProfilePath-Attributs
topic_type:
- apiref
api_name:
- Profile-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d1c255843cf578301ce330b79f3ca983030952
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957592"
---
# <a name="profile-path-attribute"></a><span data-ttu-id="39209-106">Profile-Path-Attribut</span><span class="sxs-lookup"><span data-stu-id="39209-106">Profile-Path attribute</span></span>

<span data-ttu-id="39209-107">Gibt einen Pfad zum Profil des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="39209-107">Specifies a path to the user's profile.</span></span> <span data-ttu-id="39209-108">Dieser Wert kann eine NULL-Zeichenfolge, ein lokaler absoluter Pfad oder ein UNC-Pfad sein.</span><span class="sxs-lookup"><span data-stu-id="39209-108">This value can be a null string, a local absolute path, or a UNC path.</span></span>



| <span data-ttu-id="39209-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39209-109">Entry</span></span> | <span data-ttu-id="39209-110">Wert</span><span class="sxs-lookup"><span data-stu-id="39209-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="39209-111">CN</span><span class="sxs-lookup"><span data-stu-id="39209-111">CN</span></span>                | <span data-ttu-id="39209-112">Profile-Path</span><span class="sxs-lookup"><span data-stu-id="39209-112">Profile-Path</span></span>                                                             |
| <span data-ttu-id="39209-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="39209-113">Ldap-Display-Name</span></span> | <span data-ttu-id="39209-114">Profilpfad</span><span class="sxs-lookup"><span data-stu-id="39209-114">profilePath</span></span>                                                              |
| <span data-ttu-id="39209-115">Size</span><span class="sxs-lookup"><span data-stu-id="39209-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="39209-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="39209-116">Update Privilege</span></span>  | <span data-ttu-id="39209-117">Domänen Administrator oder Konto Besitzer.</span><span class="sxs-lookup"><span data-stu-id="39209-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="39209-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="39209-118">Update Frequency</span></span>  | <span data-ttu-id="39209-119">Wenn der Benutzerdaten Satz erstellt und der Pfad geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="39209-119">When the user's record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="39209-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="39209-120">Attribute-Id</span></span>      | <span data-ttu-id="39209-121">1.2.840.113556.1.4.139</span><span class="sxs-lookup"><span data-stu-id="39209-121">1.2.840.113556.1.4.139</span></span>                                                   |
| <span data-ttu-id="39209-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="39209-122">System-Id-Guid</span></span>    | <span data-ttu-id="39209-123">bf967a05-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="39209-123">bf967a05-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="39209-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="39209-124">Syntax</span></span>            | [<span data-ttu-id="39209-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="39209-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="39209-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="39209-126">Implementations</span></span>

-   [<span data-ttu-id="39209-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="39209-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="39209-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="39209-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="39209-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="39209-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="39209-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="39209-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="39209-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="39209-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="39209-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="39209-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="39209-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="39209-133">Windows 2000 Server</span></span>



| <span data-ttu-id="39209-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39209-134">Entry</span></span> | <span data-ttu-id="39209-135">Wert</span><span class="sxs-lookup"><span data-stu-id="39209-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="39209-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39209-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="39209-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39209-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="39209-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="39209-138">System-Only</span></span>            | <span data-ttu-id="39209-139">False</span><span class="sxs-lookup"><span data-stu-id="39209-139">False</span></span>                             |
| <span data-ttu-id="39209-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39209-140">Is-Single-Valued</span></span>       | <span data-ttu-id="39209-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="39209-141">True</span></span>                              |
| <span data-ttu-id="39209-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39209-142">Is Indexed</span></span>             | <span data-ttu-id="39209-143">False</span><span class="sxs-lookup"><span data-stu-id="39209-143">False</span></span>                             |
| <span data-ttu-id="39209-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39209-144">In Global Catalog</span></span>      | <span data-ttu-id="39209-145">False</span><span class="sxs-lookup"><span data-stu-id="39209-145">False</span></span>                             |
| <span data-ttu-id="39209-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39209-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="39209-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39209-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="39209-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39209-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="39209-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39209-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="39209-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39209-150">Search-Flags</span></span>           | <span data-ttu-id="39209-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39209-151">0x00000010</span></span>                        |
| <span data-ttu-id="39209-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39209-152">System-Flags</span></span>           | <span data-ttu-id="39209-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39209-153">0x00000010</span></span>                        |
| <span data-ttu-id="39209-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39209-154">Classes used in</span></span>        | [<span data-ttu-id="39209-155">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="39209-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="39209-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="39209-156">Windows Server 2003</span></span>



| <span data-ttu-id="39209-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39209-157">Entry</span></span> | <span data-ttu-id="39209-158">Wert</span><span class="sxs-lookup"><span data-stu-id="39209-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="39209-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39209-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="39209-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39209-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="39209-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="39209-161">System-Only</span></span>            | <span data-ttu-id="39209-162">False</span><span class="sxs-lookup"><span data-stu-id="39209-162">False</span></span>                             |
| <span data-ttu-id="39209-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39209-163">Is-Single-Valued</span></span>       | <span data-ttu-id="39209-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="39209-164">True</span></span>                              |
| <span data-ttu-id="39209-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39209-165">Is Indexed</span></span>             | <span data-ttu-id="39209-166">False</span><span class="sxs-lookup"><span data-stu-id="39209-166">False</span></span>                             |
| <span data-ttu-id="39209-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39209-167">In Global Catalog</span></span>      | <span data-ttu-id="39209-168">False</span><span class="sxs-lookup"><span data-stu-id="39209-168">False</span></span>                             |
| <span data-ttu-id="39209-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39209-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="39209-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39209-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="39209-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39209-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="39209-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39209-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="39209-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39209-173">Search-Flags</span></span>           | <span data-ttu-id="39209-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39209-174">0x00000010</span></span>                        |
| <span data-ttu-id="39209-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39209-175">System-Flags</span></span>           | <span data-ttu-id="39209-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39209-176">0x00000010</span></span>                        |
| <span data-ttu-id="39209-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39209-177">Classes used in</span></span>        | [<span data-ttu-id="39209-178">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="39209-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="39209-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="39209-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="39209-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39209-180">Entry</span></span> | <span data-ttu-id="39209-181">Wert</span><span class="sxs-lookup"><span data-stu-id="39209-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="39209-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39209-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="39209-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39209-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="39209-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="39209-184">System-Only</span></span>            | <span data-ttu-id="39209-185">False</span><span class="sxs-lookup"><span data-stu-id="39209-185">False</span></span>                             |
| <span data-ttu-id="39209-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39209-186">Is-Single-Valued</span></span>       | <span data-ttu-id="39209-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="39209-187">True</span></span>                              |
| <span data-ttu-id="39209-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39209-188">Is Indexed</span></span>             | <span data-ttu-id="39209-189">False</span><span class="sxs-lookup"><span data-stu-id="39209-189">False</span></span>                             |
| <span data-ttu-id="39209-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39209-190">In Global Catalog</span></span>      | <span data-ttu-id="39209-191">False</span><span class="sxs-lookup"><span data-stu-id="39209-191">False</span></span>                             |
| <span data-ttu-id="39209-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39209-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="39209-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39209-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="39209-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39209-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="39209-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39209-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="39209-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39209-196">Search-Flags</span></span>           | <span data-ttu-id="39209-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39209-197">0x00000010</span></span>                        |
| <span data-ttu-id="39209-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39209-198">System-Flags</span></span>           | <span data-ttu-id="39209-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39209-199">0x00000010</span></span>                        |
| <span data-ttu-id="39209-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39209-200">Classes used in</span></span>        | [<span data-ttu-id="39209-201">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="39209-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="39209-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39209-202">Windows Server 2008</span></span>



| <span data-ttu-id="39209-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39209-203">Entry</span></span> | <span data-ttu-id="39209-204">Wert</span><span class="sxs-lookup"><span data-stu-id="39209-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="39209-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39209-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="39209-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39209-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="39209-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="39209-207">System-Only</span></span>            | <span data-ttu-id="39209-208">False</span><span class="sxs-lookup"><span data-stu-id="39209-208">False</span></span>                             |
| <span data-ttu-id="39209-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39209-209">Is-Single-Valued</span></span>       | <span data-ttu-id="39209-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="39209-210">True</span></span>                              |
| <span data-ttu-id="39209-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39209-211">Is Indexed</span></span>             | <span data-ttu-id="39209-212">False</span><span class="sxs-lookup"><span data-stu-id="39209-212">False</span></span>                             |
| <span data-ttu-id="39209-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39209-213">In Global Catalog</span></span>      | <span data-ttu-id="39209-214">False</span><span class="sxs-lookup"><span data-stu-id="39209-214">False</span></span>                             |
| <span data-ttu-id="39209-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39209-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="39209-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39209-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="39209-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39209-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="39209-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39209-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="39209-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39209-219">Search-Flags</span></span>           | <span data-ttu-id="39209-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39209-220">0x00000010</span></span>                        |
| <span data-ttu-id="39209-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39209-221">System-Flags</span></span>           | <span data-ttu-id="39209-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39209-222">0x00000010</span></span>                        |
| <span data-ttu-id="39209-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39209-223">Classes used in</span></span>        | [<span data-ttu-id="39209-224">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="39209-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="39209-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39209-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="39209-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39209-226">Entry</span></span> | <span data-ttu-id="39209-227">Wert</span><span class="sxs-lookup"><span data-stu-id="39209-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="39209-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39209-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="39209-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39209-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="39209-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="39209-230">System-Only</span></span>            | <span data-ttu-id="39209-231">False</span><span class="sxs-lookup"><span data-stu-id="39209-231">False</span></span>                             |
| <span data-ttu-id="39209-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39209-232">Is-Single-Valued</span></span>       | <span data-ttu-id="39209-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="39209-233">True</span></span>                              |
| <span data-ttu-id="39209-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39209-234">Is Indexed</span></span>             | <span data-ttu-id="39209-235">False</span><span class="sxs-lookup"><span data-stu-id="39209-235">False</span></span>                             |
| <span data-ttu-id="39209-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39209-236">In Global Catalog</span></span>      | <span data-ttu-id="39209-237">False</span><span class="sxs-lookup"><span data-stu-id="39209-237">False</span></span>                             |
| <span data-ttu-id="39209-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39209-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="39209-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39209-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="39209-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39209-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="39209-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39209-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="39209-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39209-242">Search-Flags</span></span>           | <span data-ttu-id="39209-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39209-243">0x00000010</span></span>                        |
| <span data-ttu-id="39209-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39209-244">System-Flags</span></span>           | <span data-ttu-id="39209-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39209-245">0x00000010</span></span>                        |
| <span data-ttu-id="39209-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39209-246">Classes used in</span></span>        | [<span data-ttu-id="39209-247">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="39209-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="39209-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="39209-248">Windows Server 2012</span></span>



| <span data-ttu-id="39209-249">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39209-249">Entry</span></span> | <span data-ttu-id="39209-250">Wert</span><span class="sxs-lookup"><span data-stu-id="39209-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="39209-251">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39209-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="39209-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39209-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="39209-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="39209-253">System-Only</span></span>            | <span data-ttu-id="39209-254">False</span><span class="sxs-lookup"><span data-stu-id="39209-254">False</span></span>                             |
| <span data-ttu-id="39209-255">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39209-255">Is-Single-Valued</span></span>       | <span data-ttu-id="39209-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="39209-256">True</span></span>                              |
| <span data-ttu-id="39209-257">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39209-257">Is Indexed</span></span>             | <span data-ttu-id="39209-258">False</span><span class="sxs-lookup"><span data-stu-id="39209-258">False</span></span>                             |
| <span data-ttu-id="39209-259">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39209-259">In Global Catalog</span></span>      | <span data-ttu-id="39209-260">False</span><span class="sxs-lookup"><span data-stu-id="39209-260">False</span></span>                             |
| <span data-ttu-id="39209-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39209-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="39209-262">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39209-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="39209-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39209-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="39209-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39209-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="39209-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39209-265">Search-Flags</span></span>           | <span data-ttu-id="39209-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39209-266">0x00000010</span></span>                        |
| <span data-ttu-id="39209-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39209-267">System-Flags</span></span>           | <span data-ttu-id="39209-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39209-268">0x00000010</span></span>                        |
| <span data-ttu-id="39209-269">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39209-269">Classes used in</span></span>        | [<span data-ttu-id="39209-270">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="39209-270">**User**</span></span>](c-user.md)<br/> |



 

 





