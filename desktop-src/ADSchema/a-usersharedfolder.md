---
title: Benutzer-Shared-Folder-Attribut
description: Gibt einen UNC-Pfad zum freigegebenen Dokument Ordner des Benutzers an. Der Pfad muss ein Netzwerk-UNC-Pfad des Formular \\ \\ Server \\ Freigabe- \\ Verzeichnisses sein. Dieser Wert kann eine NULL-Zeichenfolge sein.
ms.assetid: 23b4177a-0a05-4111-affe-d81bc115580d
ms.tgt_platform: multiple
keywords:
- AD-Schema des Benutzer-Shared-Folder-Attributs
- usersharedfolder-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- User-Shared-Folder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a20e9772302e79837fccd301943554191cf3b862
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957565"
---
# <a name="user-shared-folder-attribute"></a><span data-ttu-id="6d934-107">Benutzer-Shared-Folder-Attribut</span><span class="sxs-lookup"><span data-stu-id="6d934-107">User-Shared-Folder attribute</span></span>

<span data-ttu-id="6d934-108">Gibt einen UNC-Pfad zum freigegebenen Dokument Ordner des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="6d934-108">Specifies a UNC path to the user's shared documents folder.</span></span> <span data-ttu-id="6d934-109">Der Pfad muss ein Netzwerk-UNC-Pfad des Formular **\\\\** _Server_ *_\\_* _Freigabe_- *_\\_* _Verzeichnisses_ sein.</span><span class="sxs-lookup"><span data-stu-id="6d934-109">The path must be a network UNC path of the form **\\\\**_Server_*_\\_*_Share_*_\\_*_Directory_.</span></span> <span data-ttu-id="6d934-110">Dieser Wert kann eine NULL-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="6d934-110">This value can be a null string.</span></span>



| <span data-ttu-id="6d934-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d934-111">Entry</span></span> | <span data-ttu-id="6d934-112">Wert</span><span class="sxs-lookup"><span data-stu-id="6d934-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6d934-113">CN</span><span class="sxs-lookup"><span data-stu-id="6d934-113">CN</span></span>                | <span data-ttu-id="6d934-114">Benutzer-Shared-Folder</span><span class="sxs-lookup"><span data-stu-id="6d934-114">User-Shared-Folder</span></span>                                                                |
| <span data-ttu-id="6d934-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6d934-115">Ldap-Display-Name</span></span> | <span data-ttu-id="6d934-116">usersharedfolder</span><span class="sxs-lookup"><span data-stu-id="6d934-116">userSharedFolder</span></span>                                                                  |
| <span data-ttu-id="6d934-117">Size</span><span class="sxs-lookup"><span data-stu-id="6d934-117">Size</span></span>              | \-                                                                                |
| <span data-ttu-id="6d934-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="6d934-118">Update Privilege</span></span>  | <span data-ttu-id="6d934-119">Domänen Administrator oder Konto Besitzer.</span><span class="sxs-lookup"><span data-stu-id="6d934-119">Domain administrator or account owner.</span></span>                                            |
| <span data-ttu-id="6d934-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="6d934-120">Update Frequency</span></span>  | <span data-ttu-id="6d934-121">Wenn der Benutzerdaten Satz erstellt und der freigegebene Ordner geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="6d934-121">When the user's record is created and whenever the shared folder needs to change.</span></span> |
| <span data-ttu-id="6d934-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6d934-122">Attribute-Id</span></span>      | <span data-ttu-id="6d934-123">1.2.840.113556.1.4.751</span><span class="sxs-lookup"><span data-stu-id="6d934-123">1.2.840.113556.1.4.751</span></span>                                                            |
| <span data-ttu-id="6d934-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6d934-124">System-Id-Guid</span></span>    | <span data-ttu-id="6d934-125">9a9a021b-4a5b-11d1-a9c3-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="6d934-125">9a9a021f-4a5b-11d1-a9c3-0000f80367c1</span></span>                                              |
| <span data-ttu-id="6d934-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d934-126">Syntax</span></span>            | [<span data-ttu-id="6d934-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6d934-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="6d934-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="6d934-128">Implementations</span></span>

-   [<span data-ttu-id="6d934-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6d934-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6d934-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6d934-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6d934-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6d934-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6d934-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6d934-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6d934-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6d934-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6d934-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6d934-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6d934-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6d934-135">Windows 2000 Server</span></span>



| <span data-ttu-id="6d934-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d934-136">Entry</span></span> | <span data-ttu-id="6d934-137">Wert</span><span class="sxs-lookup"><span data-stu-id="6d934-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d934-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d934-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d934-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d934-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d934-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d934-140">System-Only</span></span>            | <span data-ttu-id="6d934-141">False</span><span class="sxs-lookup"><span data-stu-id="6d934-141">False</span></span>                             |
| <span data-ttu-id="6d934-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d934-142">Is-Single-Valued</span></span>       | <span data-ttu-id="6d934-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d934-143">True</span></span>                              |
| <span data-ttu-id="6d934-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d934-144">Is Indexed</span></span>             | <span data-ttu-id="6d934-145">False</span><span class="sxs-lookup"><span data-stu-id="6d934-145">False</span></span>                             |
| <span data-ttu-id="6d934-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d934-146">In Global Catalog</span></span>      | <span data-ttu-id="6d934-147">False</span><span class="sxs-lookup"><span data-stu-id="6d934-147">False</span></span>                             |
| <span data-ttu-id="6d934-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d934-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d934-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d934-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d934-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d934-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d934-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d934-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d934-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d934-152">Search-Flags</span></span>           | <span data-ttu-id="6d934-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d934-153">0x00000000</span></span>                        |
| <span data-ttu-id="6d934-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d934-154">System-Flags</span></span>           | <span data-ttu-id="6d934-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d934-155">0x00000010</span></span>                        |
| <span data-ttu-id="6d934-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d934-156">Classes used in</span></span>        | [<span data-ttu-id="6d934-157">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="6d934-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6d934-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6d934-158">Windows Server 2003</span></span>



| <span data-ttu-id="6d934-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d934-159">Entry</span></span> | <span data-ttu-id="6d934-160">Wert</span><span class="sxs-lookup"><span data-stu-id="6d934-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d934-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d934-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d934-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d934-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d934-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d934-163">System-Only</span></span>            | <span data-ttu-id="6d934-164">False</span><span class="sxs-lookup"><span data-stu-id="6d934-164">False</span></span>                             |
| <span data-ttu-id="6d934-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d934-165">Is-Single-Valued</span></span>       | <span data-ttu-id="6d934-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d934-166">True</span></span>                              |
| <span data-ttu-id="6d934-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d934-167">Is Indexed</span></span>             | <span data-ttu-id="6d934-168">False</span><span class="sxs-lookup"><span data-stu-id="6d934-168">False</span></span>                             |
| <span data-ttu-id="6d934-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d934-169">In Global Catalog</span></span>      | <span data-ttu-id="6d934-170">False</span><span class="sxs-lookup"><span data-stu-id="6d934-170">False</span></span>                             |
| <span data-ttu-id="6d934-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d934-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d934-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d934-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d934-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d934-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d934-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d934-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d934-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d934-175">Search-Flags</span></span>           | <span data-ttu-id="6d934-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d934-176">0x00000000</span></span>                        |
| <span data-ttu-id="6d934-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d934-177">System-Flags</span></span>           | <span data-ttu-id="6d934-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d934-178">0x00000010</span></span>                        |
| <span data-ttu-id="6d934-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d934-179">Classes used in</span></span>        | [<span data-ttu-id="6d934-180">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="6d934-180">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6d934-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6d934-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6d934-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d934-182">Entry</span></span> | <span data-ttu-id="6d934-183">Wert</span><span class="sxs-lookup"><span data-stu-id="6d934-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d934-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d934-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d934-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d934-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d934-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d934-186">System-Only</span></span>            | <span data-ttu-id="6d934-187">False</span><span class="sxs-lookup"><span data-stu-id="6d934-187">False</span></span>                             |
| <span data-ttu-id="6d934-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d934-188">Is-Single-Valued</span></span>       | <span data-ttu-id="6d934-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d934-189">True</span></span>                              |
| <span data-ttu-id="6d934-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d934-190">Is Indexed</span></span>             | <span data-ttu-id="6d934-191">False</span><span class="sxs-lookup"><span data-stu-id="6d934-191">False</span></span>                             |
| <span data-ttu-id="6d934-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d934-192">In Global Catalog</span></span>      | <span data-ttu-id="6d934-193">False</span><span class="sxs-lookup"><span data-stu-id="6d934-193">False</span></span>                             |
| <span data-ttu-id="6d934-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d934-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d934-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d934-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d934-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d934-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d934-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d934-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d934-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d934-198">Search-Flags</span></span>           | <span data-ttu-id="6d934-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d934-199">0x00000000</span></span>                        |
| <span data-ttu-id="6d934-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d934-200">System-Flags</span></span>           | <span data-ttu-id="6d934-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d934-201">0x00000010</span></span>                        |
| <span data-ttu-id="6d934-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d934-202">Classes used in</span></span>        | [<span data-ttu-id="6d934-203">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="6d934-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6d934-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d934-204">Windows Server 2008</span></span>



| <span data-ttu-id="6d934-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d934-205">Entry</span></span> | <span data-ttu-id="6d934-206">Wert</span><span class="sxs-lookup"><span data-stu-id="6d934-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d934-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d934-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d934-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d934-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d934-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d934-209">System-Only</span></span>            | <span data-ttu-id="6d934-210">False</span><span class="sxs-lookup"><span data-stu-id="6d934-210">False</span></span>                             |
| <span data-ttu-id="6d934-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d934-211">Is-Single-Valued</span></span>       | <span data-ttu-id="6d934-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d934-212">True</span></span>                              |
| <span data-ttu-id="6d934-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d934-213">Is Indexed</span></span>             | <span data-ttu-id="6d934-214">False</span><span class="sxs-lookup"><span data-stu-id="6d934-214">False</span></span>                             |
| <span data-ttu-id="6d934-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d934-215">In Global Catalog</span></span>      | <span data-ttu-id="6d934-216">False</span><span class="sxs-lookup"><span data-stu-id="6d934-216">False</span></span>                             |
| <span data-ttu-id="6d934-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d934-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d934-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d934-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d934-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d934-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d934-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d934-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d934-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d934-221">Search-Flags</span></span>           | <span data-ttu-id="6d934-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d934-222">0x00000000</span></span>                        |
| <span data-ttu-id="6d934-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d934-223">System-Flags</span></span>           | <span data-ttu-id="6d934-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d934-224">0x00000010</span></span>                        |
| <span data-ttu-id="6d934-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d934-225">Classes used in</span></span>        | [<span data-ttu-id="6d934-226">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="6d934-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6d934-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6d934-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6d934-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d934-228">Entry</span></span> | <span data-ttu-id="6d934-229">Wert</span><span class="sxs-lookup"><span data-stu-id="6d934-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d934-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d934-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d934-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d934-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d934-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d934-232">System-Only</span></span>            | <span data-ttu-id="6d934-233">False</span><span class="sxs-lookup"><span data-stu-id="6d934-233">False</span></span>                             |
| <span data-ttu-id="6d934-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d934-234">Is-Single-Valued</span></span>       | <span data-ttu-id="6d934-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d934-235">True</span></span>                              |
| <span data-ttu-id="6d934-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d934-236">Is Indexed</span></span>             | <span data-ttu-id="6d934-237">False</span><span class="sxs-lookup"><span data-stu-id="6d934-237">False</span></span>                             |
| <span data-ttu-id="6d934-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d934-238">In Global Catalog</span></span>      | <span data-ttu-id="6d934-239">False</span><span class="sxs-lookup"><span data-stu-id="6d934-239">False</span></span>                             |
| <span data-ttu-id="6d934-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d934-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d934-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d934-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d934-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d934-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d934-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d934-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d934-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d934-244">Search-Flags</span></span>           | <span data-ttu-id="6d934-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d934-245">0x00000000</span></span>                        |
| <span data-ttu-id="6d934-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d934-246">System-Flags</span></span>           | <span data-ttu-id="6d934-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d934-247">0x00000010</span></span>                        |
| <span data-ttu-id="6d934-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d934-248">Classes used in</span></span>        | [<span data-ttu-id="6d934-249">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="6d934-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6d934-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6d934-250">Windows Server 2012</span></span>



| <span data-ttu-id="6d934-251">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d934-251">Entry</span></span> | <span data-ttu-id="6d934-252">Wert</span><span class="sxs-lookup"><span data-stu-id="6d934-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d934-253">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6d934-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d934-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d934-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d934-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d934-255">System-Only</span></span>            | <span data-ttu-id="6d934-256">False</span><span class="sxs-lookup"><span data-stu-id="6d934-256">False</span></span>                             |
| <span data-ttu-id="6d934-257">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6d934-257">Is-Single-Valued</span></span>       | <span data-ttu-id="6d934-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="6d934-258">True</span></span>                              |
| <span data-ttu-id="6d934-259">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6d934-259">Is Indexed</span></span>             | <span data-ttu-id="6d934-260">False</span><span class="sxs-lookup"><span data-stu-id="6d934-260">False</span></span>                             |
| <span data-ttu-id="6d934-261">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6d934-261">In Global Catalog</span></span>      | <span data-ttu-id="6d934-262">False</span><span class="sxs-lookup"><span data-stu-id="6d934-262">False</span></span>                             |
| <span data-ttu-id="6d934-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6d934-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d934-264">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6d934-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d934-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d934-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d934-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d934-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d934-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d934-267">Search-Flags</span></span>           | <span data-ttu-id="6d934-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d934-268">0x00000000</span></span>                        |
| <span data-ttu-id="6d934-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d934-269">System-Flags</span></span>           | <span data-ttu-id="6d934-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d934-270">0x00000010</span></span>                        |
| <span data-ttu-id="6d934-271">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6d934-271">Classes used in</span></span>        | [<span data-ttu-id="6d934-272">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="6d934-272">**User**</span></span>](c-user.md)<br/> |



 

 





