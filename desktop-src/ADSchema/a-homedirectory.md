---
title: Home-Directory-Attribut
description: Das Basisverzeichnis für das Konto.
ms.assetid: 7fd431f2-f2e0-476f-82ed-04f776c234eb
ms.tgt_platform: multiple
keywords:
- AD-Schema für Home-Directory-Attribut
- AD-Schema für Homedirectory-Attribut
topic_type:
- apiref
api_name:
- Home-Directory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 070285336284e6d07b6333d28eff5c85c4dc6c5a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744849"
---
# <a name="home-directory-attribute"></a><span data-ttu-id="676fc-105">Home-Directory-Attribut</span><span class="sxs-lookup"><span data-stu-id="676fc-105">Home-Directory attribute</span></span>

<span data-ttu-id="676fc-106">Das Basisverzeichnis für das Konto.</span><span class="sxs-lookup"><span data-stu-id="676fc-106">The home directory for the account.</span></span> <span data-ttu-id="676fc-107">Wenn [**HOMEDRIVE**](a-homedrive.md) festgelegt ist und einen Laufwerk Buchstaben angibt, muss das **Homedirectory** ein UNC-Pfad sein.</span><span class="sxs-lookup"><span data-stu-id="676fc-107">If [**homeDrive**](a-homedrive.md) is set and specifies a drive letter, **homeDirectory** must be a UNC path.</span></span> <span data-ttu-id="676fc-108">Andernfalls ist **Homedirectory** ein voll qualifizierter lokaler Pfad einschließlich des Laufwerk Buchstabens (z. b. Laufwerk Buchstabe \*\*\*\*: \\**_Verzeichnis_* _\\_ \* _Ordner_).</span><span class="sxs-lookup"><span data-stu-id="676fc-108">Otherwise, **homeDirectory** is a fully qualified local path including the drive letter (for example, *DriveLetter\***:\\**_Directory_*_\\_\*_Folder_).</span></span> <span data-ttu-id="676fc-109">Dieser Wert kann eine NULL-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="676fc-109">This value can be a null string.</span></span>



| <span data-ttu-id="676fc-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="676fc-110">Entry</span></span> | <span data-ttu-id="676fc-111">Wert</span><span class="sxs-lookup"><span data-stu-id="676fc-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="676fc-112">CN</span><span class="sxs-lookup"><span data-stu-id="676fc-112">CN</span></span>                | <span data-ttu-id="676fc-113">Home-Directory</span><span class="sxs-lookup"><span data-stu-id="676fc-113">Home-Directory</span></span>                                                                     |
| <span data-ttu-id="676fc-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="676fc-114">Ldap-Display-Name</span></span> | <span data-ttu-id="676fc-115">homedirectory</span><span class="sxs-lookup"><span data-stu-id="676fc-115">homeDirectory</span></span>                                                                      |
| <span data-ttu-id="676fc-116">Size</span><span class="sxs-lookup"><span data-stu-id="676fc-116">Size</span></span>              | \-                                                                                 |
| <span data-ttu-id="676fc-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="676fc-117">Update Privilege</span></span>  | <span data-ttu-id="676fc-118">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="676fc-118">Domain administrator</span></span>                                                               |
| <span data-ttu-id="676fc-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="676fc-119">Update Frequency</span></span>  | <span data-ttu-id="676fc-120">Wenn der Benutzerdaten Satz erstellt wird, und immer dann, wenn das Basisverzeichnis geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="676fc-120">When the user's record is created and whenever the home directory needs to change.</span></span> |
| <span data-ttu-id="676fc-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="676fc-121">Attribute-Id</span></span>      | <span data-ttu-id="676fc-122">1.2.840.113556.1.4.44</span><span class="sxs-lookup"><span data-stu-id="676fc-122">1.2.840.113556.1.4.44</span></span>                                                              |
| <span data-ttu-id="676fc-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="676fc-123">System-Id-Guid</span></span>    | <span data-ttu-id="676fc-124">bf967985-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="676fc-124">bf967985-0de6-11d0-a285-00aa003049e2</span></span>                                               |
| <span data-ttu-id="676fc-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="676fc-125">Syntax</span></span>            | [<span data-ttu-id="676fc-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="676fc-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                        |



## <a name="implementations"></a><span data-ttu-id="676fc-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="676fc-127">Implementations</span></span>

-   [<span data-ttu-id="676fc-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="676fc-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="676fc-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="676fc-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="676fc-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="676fc-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="676fc-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="676fc-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="676fc-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="676fc-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="676fc-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="676fc-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="676fc-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="676fc-134">Windows 2000 Server</span></span>



| <span data-ttu-id="676fc-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="676fc-135">Entry</span></span> | <span data-ttu-id="676fc-136">Wert</span><span class="sxs-lookup"><span data-stu-id="676fc-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="676fc-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="676fc-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="676fc-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676fc-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="676fc-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="676fc-139">System-Only</span></span>            | <span data-ttu-id="676fc-140">False</span><span class="sxs-lookup"><span data-stu-id="676fc-140">False</span></span>                             |
| <span data-ttu-id="676fc-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="676fc-141">Is-Single-Valued</span></span>       | <span data-ttu-id="676fc-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="676fc-142">True</span></span>                              |
| <span data-ttu-id="676fc-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="676fc-143">Is Indexed</span></span>             | <span data-ttu-id="676fc-144">False</span><span class="sxs-lookup"><span data-stu-id="676fc-144">False</span></span>                             |
| <span data-ttu-id="676fc-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="676fc-145">In Global Catalog</span></span>      | <span data-ttu-id="676fc-146">False</span><span class="sxs-lookup"><span data-stu-id="676fc-146">False</span></span>                             |
| <span data-ttu-id="676fc-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="676fc-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="676fc-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="676fc-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="676fc-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676fc-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="676fc-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676fc-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="676fc-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-151">Search-Flags</span></span>           | <span data-ttu-id="676fc-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676fc-152">0x00000010</span></span>                        |
| <span data-ttu-id="676fc-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-153">System-Flags</span></span>           | <span data-ttu-id="676fc-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676fc-154">0x00000010</span></span>                        |
| <span data-ttu-id="676fc-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="676fc-155">Classes used in</span></span>        | [<span data-ttu-id="676fc-156">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="676fc-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="676fc-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="676fc-157">Windows Server 2003</span></span>



| <span data-ttu-id="676fc-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="676fc-158">Entry</span></span> | <span data-ttu-id="676fc-159">Wert</span><span class="sxs-lookup"><span data-stu-id="676fc-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="676fc-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="676fc-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="676fc-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676fc-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="676fc-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="676fc-162">System-Only</span></span>            | <span data-ttu-id="676fc-163">False</span><span class="sxs-lookup"><span data-stu-id="676fc-163">False</span></span>                             |
| <span data-ttu-id="676fc-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="676fc-164">Is-Single-Valued</span></span>       | <span data-ttu-id="676fc-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="676fc-165">True</span></span>                              |
| <span data-ttu-id="676fc-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="676fc-166">Is Indexed</span></span>             | <span data-ttu-id="676fc-167">False</span><span class="sxs-lookup"><span data-stu-id="676fc-167">False</span></span>                             |
| <span data-ttu-id="676fc-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="676fc-168">In Global Catalog</span></span>      | <span data-ttu-id="676fc-169">False</span><span class="sxs-lookup"><span data-stu-id="676fc-169">False</span></span>                             |
| <span data-ttu-id="676fc-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="676fc-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="676fc-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="676fc-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="676fc-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676fc-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="676fc-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676fc-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="676fc-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-174">Search-Flags</span></span>           | <span data-ttu-id="676fc-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676fc-175">0x00000010</span></span>                        |
| <span data-ttu-id="676fc-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-176">System-Flags</span></span>           | <span data-ttu-id="676fc-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676fc-177">0x00000010</span></span>                        |
| <span data-ttu-id="676fc-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="676fc-178">Classes used in</span></span>        | [<span data-ttu-id="676fc-179">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="676fc-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="676fc-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="676fc-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="676fc-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="676fc-181">Entry</span></span> | <span data-ttu-id="676fc-182">Wert</span><span class="sxs-lookup"><span data-stu-id="676fc-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="676fc-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="676fc-183">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="676fc-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676fc-184">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="676fc-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="676fc-185">System-Only</span></span>            | <span data-ttu-id="676fc-186">False</span><span class="sxs-lookup"><span data-stu-id="676fc-186">False</span></span>                                                                               |
| <span data-ttu-id="676fc-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="676fc-187">Is-Single-Valued</span></span>       | <span data-ttu-id="676fc-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="676fc-188">True</span></span>                                                                                |
| <span data-ttu-id="676fc-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="676fc-189">Is Indexed</span></span>             | <span data-ttu-id="676fc-190">False</span><span class="sxs-lookup"><span data-stu-id="676fc-190">False</span></span>                                                                               |
| <span data-ttu-id="676fc-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="676fc-191">In Global Catalog</span></span>      | <span data-ttu-id="676fc-192">False</span><span class="sxs-lookup"><span data-stu-id="676fc-192">False</span></span>                                                                               |
| <span data-ttu-id="676fc-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="676fc-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="676fc-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="676fc-194">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="676fc-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676fc-195">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="676fc-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676fc-196">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="676fc-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-197">Search-Flags</span></span>           | <span data-ttu-id="676fc-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676fc-198">0x00000010</span></span>                                                                          |
| <span data-ttu-id="676fc-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-199">System-Flags</span></span>           | <span data-ttu-id="676fc-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676fc-200">0x00000010</span></span>                                                                          |
| <span data-ttu-id="676fc-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="676fc-201">Classes used in</span></span>        | [<span data-ttu-id="676fc-202">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="676fc-202">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="676fc-203">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="676fc-203">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="676fc-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="676fc-204">Windows Server 2008</span></span>



| <span data-ttu-id="676fc-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="676fc-205">Entry</span></span> | <span data-ttu-id="676fc-206">Wert</span><span class="sxs-lookup"><span data-stu-id="676fc-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="676fc-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="676fc-207">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="676fc-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676fc-208">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="676fc-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="676fc-209">System-Only</span></span>            | <span data-ttu-id="676fc-210">False</span><span class="sxs-lookup"><span data-stu-id="676fc-210">False</span></span>                                                                               |
| <span data-ttu-id="676fc-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="676fc-211">Is-Single-Valued</span></span>       | <span data-ttu-id="676fc-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="676fc-212">True</span></span>                                                                                |
| <span data-ttu-id="676fc-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="676fc-213">Is Indexed</span></span>             | <span data-ttu-id="676fc-214">False</span><span class="sxs-lookup"><span data-stu-id="676fc-214">False</span></span>                                                                               |
| <span data-ttu-id="676fc-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="676fc-215">In Global Catalog</span></span>      | <span data-ttu-id="676fc-216">False</span><span class="sxs-lookup"><span data-stu-id="676fc-216">False</span></span>                                                                               |
| <span data-ttu-id="676fc-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="676fc-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="676fc-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="676fc-218">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="676fc-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676fc-219">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="676fc-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676fc-220">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="676fc-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-221">Search-Flags</span></span>           | <span data-ttu-id="676fc-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676fc-222">0x00000010</span></span>                                                                          |
| <span data-ttu-id="676fc-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-223">System-Flags</span></span>           | <span data-ttu-id="676fc-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676fc-224">0x00000010</span></span>                                                                          |
| <span data-ttu-id="676fc-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="676fc-225">Classes used in</span></span>        | [<span data-ttu-id="676fc-226">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="676fc-226">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="676fc-227">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="676fc-227">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="676fc-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="676fc-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="676fc-229">Eingabe</span><span class="sxs-lookup"><span data-stu-id="676fc-229">Entry</span></span> | <span data-ttu-id="676fc-230">Wert</span><span class="sxs-lookup"><span data-stu-id="676fc-230">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="676fc-231">Link-ID</span><span class="sxs-lookup"><span data-stu-id="676fc-231">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="676fc-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676fc-232">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="676fc-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="676fc-233">System-Only</span></span>            | <span data-ttu-id="676fc-234">False</span><span class="sxs-lookup"><span data-stu-id="676fc-234">False</span></span>                                                                               |
| <span data-ttu-id="676fc-235">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="676fc-235">Is-Single-Valued</span></span>       | <span data-ttu-id="676fc-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="676fc-236">True</span></span>                                                                                |
| <span data-ttu-id="676fc-237">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="676fc-237">Is Indexed</span></span>             | <span data-ttu-id="676fc-238">False</span><span class="sxs-lookup"><span data-stu-id="676fc-238">False</span></span>                                                                               |
| <span data-ttu-id="676fc-239">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="676fc-239">In Global Catalog</span></span>      | <span data-ttu-id="676fc-240">False</span><span class="sxs-lookup"><span data-stu-id="676fc-240">False</span></span>                                                                               |
| <span data-ttu-id="676fc-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="676fc-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="676fc-242">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="676fc-242">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="676fc-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676fc-243">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="676fc-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676fc-244">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="676fc-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-245">Search-Flags</span></span>           | <span data-ttu-id="676fc-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676fc-246">0x00000010</span></span>                                                                          |
| <span data-ttu-id="676fc-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-247">System-Flags</span></span>           | <span data-ttu-id="676fc-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676fc-248">0x00000010</span></span>                                                                          |
| <span data-ttu-id="676fc-249">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="676fc-249">Classes used in</span></span>        | [<span data-ttu-id="676fc-250">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="676fc-250">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="676fc-251">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="676fc-251">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="676fc-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="676fc-252">Windows Server 2012</span></span>



| <span data-ttu-id="676fc-253">Eingabe</span><span class="sxs-lookup"><span data-stu-id="676fc-253">Entry</span></span> | <span data-ttu-id="676fc-254">Wert</span><span class="sxs-lookup"><span data-stu-id="676fc-254">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="676fc-255">Link-ID</span><span class="sxs-lookup"><span data-stu-id="676fc-255">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="676fc-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676fc-256">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="676fc-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="676fc-257">System-Only</span></span>            | <span data-ttu-id="676fc-258">False</span><span class="sxs-lookup"><span data-stu-id="676fc-258">False</span></span>                                                                               |
| <span data-ttu-id="676fc-259">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="676fc-259">Is-Single-Valued</span></span>       | <span data-ttu-id="676fc-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="676fc-260">True</span></span>                                                                                |
| <span data-ttu-id="676fc-261">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="676fc-261">Is Indexed</span></span>             | <span data-ttu-id="676fc-262">False</span><span class="sxs-lookup"><span data-stu-id="676fc-262">False</span></span>                                                                               |
| <span data-ttu-id="676fc-263">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="676fc-263">In Global Catalog</span></span>      | <span data-ttu-id="676fc-264">False</span><span class="sxs-lookup"><span data-stu-id="676fc-264">False</span></span>                                                                               |
| <span data-ttu-id="676fc-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="676fc-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="676fc-266">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="676fc-266">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="676fc-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676fc-267">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="676fc-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676fc-268">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="676fc-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-269">Search-Flags</span></span>           | <span data-ttu-id="676fc-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676fc-270">0x00000010</span></span>                                                                          |
| <span data-ttu-id="676fc-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-271">System-Flags</span></span>           | <span data-ttu-id="676fc-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676fc-272">0x00000010</span></span>                                                                          |
| <span data-ttu-id="676fc-273">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="676fc-273">Classes used in</span></span>        | [<span data-ttu-id="676fc-274">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="676fc-274">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="676fc-275">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="676fc-275">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="676fc-276">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="676fc-276">See also</span></span>

<dl> <dt>

[<span data-ttu-id="676fc-277">**homeDrive**</span><span class="sxs-lookup"><span data-stu-id="676fc-277">**homeDrive**</span></span>](a-homedrive.md)
</dt> </dl>

 

 





