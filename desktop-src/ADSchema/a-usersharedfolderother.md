---
title: Benutzer-Shared-Folder-anderes Attribut
description: Gibt einen UNC-Pfad zum Ordner "weitere freigegebene Dokumente" des Benutzers an. Der Pfad muss ein Netzwerk-UNC-Pfad des Formular \\ \\ Server \\ Freigabe- \\ Verzeichnisses sein. Dieser Wert kann eine NULL-Zeichenfolge sein.
ms.assetid: 7d546cda-b2c1-46a6-a3cf-a7c78ddb1422
ms.tgt_platform: multiple
keywords:
- Benutzer-Shared-Folder-AD-Schema für andere Attribute
- AD-Schema des usersharedfolderother-Attributs
topic_type:
- apiref
api_name:
- User-Shared-Folder-Other
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6087a28df474ff06c1d8bf54d694176df8591b5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744513"
---
# <a name="user-shared-folder-other-attribute"></a><span data-ttu-id="bc6ef-107">Benutzer-Shared-Folder-anderes Attribut</span><span class="sxs-lookup"><span data-stu-id="bc6ef-107">User-Shared-Folder-Other attribute</span></span>

<span data-ttu-id="bc6ef-108">Gibt einen UNC-Pfad zum Ordner "weitere freigegebene Dokumente" des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-108">Specifies a UNC path to the user's additional shared documents folder.</span></span> <span data-ttu-id="bc6ef-109">Der Pfad muss ein Netzwerk-UNC-Pfad des Formular **\\\\** _Server_ *_\\_* _Freigabe_- *_\\_* _Verzeichnisses_ sein.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-109">The path must be a network UNC path of the form **\\\\**_Server_*_\\_*_Share_*_\\_*_Directory_.</span></span> <span data-ttu-id="bc6ef-110">Dieser Wert kann eine NULL-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-110">This value can be a null string.</span></span>



| <span data-ttu-id="bc6ef-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bc6ef-111">Entry</span></span> | <span data-ttu-id="bc6ef-112">Wert</span><span class="sxs-lookup"><span data-stu-id="bc6ef-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="bc6ef-113">CN</span><span class="sxs-lookup"><span data-stu-id="bc6ef-113">CN</span></span>                | <span data-ttu-id="bc6ef-114">Benutzer-Shared-Folder-Sonstiges</span><span class="sxs-lookup"><span data-stu-id="bc6ef-114">User-Shared-Folder-Other</span></span>                                                          |
| <span data-ttu-id="bc6ef-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bc6ef-115">Ldap-Display-Name</span></span> | <span data-ttu-id="bc6ef-116">usersharedfolderother</span><span class="sxs-lookup"><span data-stu-id="bc6ef-116">userSharedFolderOther</span></span>                                                             |
| <span data-ttu-id="bc6ef-117">Size</span><span class="sxs-lookup"><span data-stu-id="bc6ef-117">Size</span></span>              | \-                                                                                |
| <span data-ttu-id="bc6ef-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="bc6ef-118">Update Privilege</span></span>  | <span data-ttu-id="bc6ef-119">Domänen Administrator oder Konto Besitzer.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-119">Domain administrator or account owner.</span></span>                                            |
| <span data-ttu-id="bc6ef-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="bc6ef-120">Update Frequency</span></span>  | <span data-ttu-id="bc6ef-121">Wenn der Benutzerdaten Satz erstellt und der freigegebene Ordner geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-121">When the user's record is created and whenever the shared folder needs to change.</span></span> |
| <span data-ttu-id="bc6ef-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bc6ef-122">Attribute-Id</span></span>      | <span data-ttu-id="bc6ef-123">1.2.840.113556.1.4.752</span><span class="sxs-lookup"><span data-stu-id="bc6ef-123">1.2.840.113556.1.4.752</span></span>                                                            |
| <span data-ttu-id="bc6ef-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bc6ef-124">System-Id-Guid</span></span>    | <span data-ttu-id="bc6ef-125">9a9a0220-4a5b-11d1-a9c3-0000t80367c1</span><span class="sxs-lookup"><span data-stu-id="bc6ef-125">9a9a0220-4a5b-11d1-a9c3-0000f80367c1</span></span>                                              |
| <span data-ttu-id="bc6ef-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc6ef-126">Syntax</span></span>            | [<span data-ttu-id="bc6ef-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bc6ef-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="bc6ef-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="bc6ef-128">Implementations</span></span>

-   [<span data-ttu-id="bc6ef-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bc6ef-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bc6ef-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bc6ef-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bc6ef-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bc6ef-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bc6ef-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bc6ef-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bc6ef-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bc6ef-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bc6ef-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bc6ef-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bc6ef-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bc6ef-135">Windows 2000 Server</span></span>



| <span data-ttu-id="bc6ef-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bc6ef-136">Entry</span></span> | <span data-ttu-id="bc6ef-137">Wert</span><span class="sxs-lookup"><span data-stu-id="bc6ef-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bc6ef-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bc6ef-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bc6ef-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc6ef-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bc6ef-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc6ef-140">System-Only</span></span>            | <span data-ttu-id="bc6ef-141">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-141">False</span></span>                             |
| <span data-ttu-id="bc6ef-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bc6ef-142">Is-Single-Valued</span></span>       | <span data-ttu-id="bc6ef-143">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-143">False</span></span>                             |
| <span data-ttu-id="bc6ef-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bc6ef-144">Is Indexed</span></span>             | <span data-ttu-id="bc6ef-145">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-145">False</span></span>                             |
| <span data-ttu-id="bc6ef-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bc6ef-146">In Global Catalog</span></span>      | <span data-ttu-id="bc6ef-147">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-147">False</span></span>                             |
| <span data-ttu-id="bc6ef-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bc6ef-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc6ef-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bc6ef-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bc6ef-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc6ef-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bc6ef-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc6ef-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bc6ef-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc6ef-152">Search-Flags</span></span>           | <span data-ttu-id="bc6ef-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc6ef-153">0x00000000</span></span>                        |
| <span data-ttu-id="bc6ef-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc6ef-154">System-Flags</span></span>           | <span data-ttu-id="bc6ef-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc6ef-155">0x00000010</span></span>                        |
| <span data-ttu-id="bc6ef-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bc6ef-156">Classes used in</span></span>        | [<span data-ttu-id="bc6ef-157">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="bc6ef-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bc6ef-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bc6ef-158">Windows Server 2003</span></span>



| <span data-ttu-id="bc6ef-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bc6ef-159">Entry</span></span> | <span data-ttu-id="bc6ef-160">Wert</span><span class="sxs-lookup"><span data-stu-id="bc6ef-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bc6ef-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bc6ef-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bc6ef-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc6ef-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bc6ef-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc6ef-163">System-Only</span></span>            | <span data-ttu-id="bc6ef-164">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-164">False</span></span>                             |
| <span data-ttu-id="bc6ef-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bc6ef-165">Is-Single-Valued</span></span>       | <span data-ttu-id="bc6ef-166">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-166">False</span></span>                             |
| <span data-ttu-id="bc6ef-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bc6ef-167">Is Indexed</span></span>             | <span data-ttu-id="bc6ef-168">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-168">False</span></span>                             |
| <span data-ttu-id="bc6ef-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bc6ef-169">In Global Catalog</span></span>      | <span data-ttu-id="bc6ef-170">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-170">False</span></span>                             |
| <span data-ttu-id="bc6ef-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bc6ef-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc6ef-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bc6ef-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bc6ef-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc6ef-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bc6ef-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc6ef-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bc6ef-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc6ef-175">Search-Flags</span></span>           | <span data-ttu-id="bc6ef-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc6ef-176">0x00000000</span></span>                        |
| <span data-ttu-id="bc6ef-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc6ef-177">System-Flags</span></span>           | <span data-ttu-id="bc6ef-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc6ef-178">0x00000010</span></span>                        |
| <span data-ttu-id="bc6ef-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bc6ef-179">Classes used in</span></span>        | [<span data-ttu-id="bc6ef-180">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="bc6ef-180">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bc6ef-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bc6ef-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bc6ef-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bc6ef-182">Entry</span></span> | <span data-ttu-id="bc6ef-183">Wert</span><span class="sxs-lookup"><span data-stu-id="bc6ef-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bc6ef-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bc6ef-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bc6ef-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc6ef-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bc6ef-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc6ef-186">System-Only</span></span>            | <span data-ttu-id="bc6ef-187">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-187">False</span></span>                             |
| <span data-ttu-id="bc6ef-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bc6ef-188">Is-Single-Valued</span></span>       | <span data-ttu-id="bc6ef-189">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-189">False</span></span>                             |
| <span data-ttu-id="bc6ef-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bc6ef-190">Is Indexed</span></span>             | <span data-ttu-id="bc6ef-191">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-191">False</span></span>                             |
| <span data-ttu-id="bc6ef-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bc6ef-192">In Global Catalog</span></span>      | <span data-ttu-id="bc6ef-193">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-193">False</span></span>                             |
| <span data-ttu-id="bc6ef-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bc6ef-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc6ef-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bc6ef-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bc6ef-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc6ef-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bc6ef-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc6ef-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bc6ef-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc6ef-198">Search-Flags</span></span>           | <span data-ttu-id="bc6ef-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc6ef-199">0x00000000</span></span>                        |
| <span data-ttu-id="bc6ef-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc6ef-200">System-Flags</span></span>           | <span data-ttu-id="bc6ef-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc6ef-201">0x00000010</span></span>                        |
| <span data-ttu-id="bc6ef-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bc6ef-202">Classes used in</span></span>        | [<span data-ttu-id="bc6ef-203">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="bc6ef-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bc6ef-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc6ef-204">Windows Server 2008</span></span>



| <span data-ttu-id="bc6ef-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bc6ef-205">Entry</span></span> | <span data-ttu-id="bc6ef-206">Wert</span><span class="sxs-lookup"><span data-stu-id="bc6ef-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bc6ef-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bc6ef-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bc6ef-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc6ef-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bc6ef-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc6ef-209">System-Only</span></span>            | <span data-ttu-id="bc6ef-210">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-210">False</span></span>                             |
| <span data-ttu-id="bc6ef-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bc6ef-211">Is-Single-Valued</span></span>       | <span data-ttu-id="bc6ef-212">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-212">False</span></span>                             |
| <span data-ttu-id="bc6ef-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bc6ef-213">Is Indexed</span></span>             | <span data-ttu-id="bc6ef-214">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-214">False</span></span>                             |
| <span data-ttu-id="bc6ef-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bc6ef-215">In Global Catalog</span></span>      | <span data-ttu-id="bc6ef-216">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-216">False</span></span>                             |
| <span data-ttu-id="bc6ef-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bc6ef-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc6ef-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bc6ef-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bc6ef-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc6ef-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bc6ef-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc6ef-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bc6ef-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc6ef-221">Search-Flags</span></span>           | <span data-ttu-id="bc6ef-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc6ef-222">0x00000000</span></span>                        |
| <span data-ttu-id="bc6ef-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc6ef-223">System-Flags</span></span>           | <span data-ttu-id="bc6ef-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc6ef-224">0x00000010</span></span>                        |
| <span data-ttu-id="bc6ef-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bc6ef-225">Classes used in</span></span>        | [<span data-ttu-id="bc6ef-226">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="bc6ef-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bc6ef-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bc6ef-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bc6ef-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bc6ef-228">Entry</span></span> | <span data-ttu-id="bc6ef-229">Wert</span><span class="sxs-lookup"><span data-stu-id="bc6ef-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bc6ef-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bc6ef-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bc6ef-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc6ef-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bc6ef-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc6ef-232">System-Only</span></span>            | <span data-ttu-id="bc6ef-233">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-233">False</span></span>                             |
| <span data-ttu-id="bc6ef-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bc6ef-234">Is-Single-Valued</span></span>       | <span data-ttu-id="bc6ef-235">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-235">False</span></span>                             |
| <span data-ttu-id="bc6ef-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bc6ef-236">Is Indexed</span></span>             | <span data-ttu-id="bc6ef-237">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-237">False</span></span>                             |
| <span data-ttu-id="bc6ef-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bc6ef-238">In Global Catalog</span></span>      | <span data-ttu-id="bc6ef-239">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-239">False</span></span>                             |
| <span data-ttu-id="bc6ef-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bc6ef-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc6ef-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bc6ef-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bc6ef-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc6ef-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bc6ef-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc6ef-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bc6ef-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc6ef-244">Search-Flags</span></span>           | <span data-ttu-id="bc6ef-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc6ef-245">0x00000000</span></span>                        |
| <span data-ttu-id="bc6ef-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc6ef-246">System-Flags</span></span>           | <span data-ttu-id="bc6ef-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc6ef-247">0x00000010</span></span>                        |
| <span data-ttu-id="bc6ef-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bc6ef-248">Classes used in</span></span>        | [<span data-ttu-id="bc6ef-249">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="bc6ef-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bc6ef-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bc6ef-250">Windows Server 2012</span></span>



| <span data-ttu-id="bc6ef-251">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bc6ef-251">Entry</span></span> | <span data-ttu-id="bc6ef-252">Wert</span><span class="sxs-lookup"><span data-stu-id="bc6ef-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bc6ef-253">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bc6ef-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bc6ef-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc6ef-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bc6ef-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc6ef-255">System-Only</span></span>            | <span data-ttu-id="bc6ef-256">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-256">False</span></span>                             |
| <span data-ttu-id="bc6ef-257">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bc6ef-257">Is-Single-Valued</span></span>       | <span data-ttu-id="bc6ef-258">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-258">False</span></span>                             |
| <span data-ttu-id="bc6ef-259">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bc6ef-259">Is Indexed</span></span>             | <span data-ttu-id="bc6ef-260">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-260">False</span></span>                             |
| <span data-ttu-id="bc6ef-261">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bc6ef-261">In Global Catalog</span></span>      | <span data-ttu-id="bc6ef-262">False</span><span class="sxs-lookup"><span data-stu-id="bc6ef-262">False</span></span>                             |
| <span data-ttu-id="bc6ef-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bc6ef-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc6ef-264">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bc6ef-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bc6ef-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc6ef-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bc6ef-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc6ef-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bc6ef-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc6ef-267">Search-Flags</span></span>           | <span data-ttu-id="bc6ef-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc6ef-268">0x00000000</span></span>                        |
| <span data-ttu-id="bc6ef-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc6ef-269">System-Flags</span></span>           | <span data-ttu-id="bc6ef-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc6ef-270">0x00000010</span></span>                        |
| <span data-ttu-id="bc6ef-271">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bc6ef-271">Classes used in</span></span>        | [<span data-ttu-id="bc6ef-272">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="bc6ef-272">**User**</span></span>](c-user.md)<br/> |



 

 





