---
title: Home-Drive-Attribut
description: Gibt den Laufwerk Buchstaben an, dem der von Homedirectory angegebene UNC-Pfad zugeordnet werden soll.
ms.assetid: fa402e14-febf-4ed9-bcc6-a6bfd405068c
ms.tgt_platform: multiple
keywords:
- AD-Schema für Home-Drive-Attribut
- AD-Schema für HOMEDRIVE-Attribut
topic_type:
- apiref
api_name:
- Home-Drive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce9bff87662cc3b9da962b0c5647e79e90a3068
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344278"
---
# <a name="home-drive-attribute"></a><span data-ttu-id="01f9a-105">Home-Drive-Attribut</span><span class="sxs-lookup"><span data-stu-id="01f9a-105">Home-Drive attribute</span></span>

<span data-ttu-id="01f9a-106">Gibt den Laufwerk Buchstaben an, dem der von [**Homedirectory**](a-homedirectory.md)angegebene UNC-Pfad zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="01f9a-106">Specifies the drive letter to which to map the UNC path specified by [**homeDirectory**](a-homedirectory.md).</span></span> <span data-ttu-id="01f9a-107">Der Laufwerk Buchstabe muss in der Form "Laufwerk Buchstabe \*\* \* \*:\*\*" angegeben werden, wobei " *DriveLetter* " der Buchstabe des zuzuordnenden Laufwerks ist.</span><span class="sxs-lookup"><span data-stu-id="01f9a-107">The drive letter must be specified in the form *DriveLetter\*\*\*:*\* where *DriveLetter* is the letter of the drive to map.</span></span> <span data-ttu-id="01f9a-108">Der *DriveLetter* muss ein einzelner, Großbuchstabe und der Doppelpunkt (:) ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="01f9a-108">The *DriveLetter* must be a single, uppercase letter and the colon (:) is required.</span></span>



| <span data-ttu-id="01f9a-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="01f9a-109">Entry</span></span> | <span data-ttu-id="01f9a-110">Wert</span><span class="sxs-lookup"><span data-stu-id="01f9a-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="01f9a-111">CN</span><span class="sxs-lookup"><span data-stu-id="01f9a-111">CN</span></span>                | <span data-ttu-id="01f9a-112">Home-Drive</span><span class="sxs-lookup"><span data-stu-id="01f9a-112">Home-Drive</span></span>                                                                        |
| <span data-ttu-id="01f9a-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="01f9a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="01f9a-114">homeDrive</span><span class="sxs-lookup"><span data-stu-id="01f9a-114">homeDrive</span></span>                                                                         |
| <span data-ttu-id="01f9a-115">Size</span><span class="sxs-lookup"><span data-stu-id="01f9a-115">Size</span></span>              | <span data-ttu-id="01f9a-116">2 Bytes</span><span class="sxs-lookup"><span data-stu-id="01f9a-116">2 bytes</span></span>                                                                           |
| <span data-ttu-id="01f9a-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="01f9a-117">Update Privilege</span></span>  | <span data-ttu-id="01f9a-118">Der Domänen Administrator legt diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="01f9a-118">The domain administrator sets this value.</span></span>                                         |
| <span data-ttu-id="01f9a-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="01f9a-119">Update Frequency</span></span>  | <span data-ttu-id="01f9a-120">Wenn der Datensatz eines Benutzers erstellt wird und jedes Mal, wenn das Basis Laufwerk geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="01f9a-120">When the record of a user is created and whenever the home drive needs to change.</span></span> |
| <span data-ttu-id="01f9a-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="01f9a-121">Attribute-Id</span></span>      | <span data-ttu-id="01f9a-122">1.2.840.113556.1.4.45</span><span class="sxs-lookup"><span data-stu-id="01f9a-122">1.2.840.113556.1.4.45</span></span>                                                             |
| <span data-ttu-id="01f9a-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="01f9a-123">System-Id-Guid</span></span>    | <span data-ttu-id="01f9a-124">bf967986-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="01f9a-124">bf967986-0de6-11d0-a285-00aa003049e2</span></span>                                              |
| <span data-ttu-id="01f9a-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="01f9a-125">Syntax</span></span>            | [<span data-ttu-id="01f9a-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="01f9a-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="01f9a-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="01f9a-127">Implementations</span></span>

-   [<span data-ttu-id="01f9a-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="01f9a-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="01f9a-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="01f9a-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="01f9a-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="01f9a-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="01f9a-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="01f9a-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="01f9a-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="01f9a-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="01f9a-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="01f9a-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="01f9a-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="01f9a-134">Windows 2000 Server</span></span>



| <span data-ttu-id="01f9a-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="01f9a-135">Entry</span></span> | <span data-ttu-id="01f9a-136">Wert</span><span class="sxs-lookup"><span data-stu-id="01f9a-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="01f9a-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="01f9a-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="01f9a-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01f9a-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="01f9a-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="01f9a-139">System-Only</span></span>            | <span data-ttu-id="01f9a-140">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-140">False</span></span>                             |
| <span data-ttu-id="01f9a-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="01f9a-141">Is-Single-Valued</span></span>       | <span data-ttu-id="01f9a-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="01f9a-142">True</span></span>                              |
| <span data-ttu-id="01f9a-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="01f9a-143">Is Indexed</span></span>             | <span data-ttu-id="01f9a-144">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-144">False</span></span>                             |
| <span data-ttu-id="01f9a-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="01f9a-145">In Global Catalog</span></span>      | <span data-ttu-id="01f9a-146">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-146">False</span></span>                             |
| <span data-ttu-id="01f9a-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="01f9a-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="01f9a-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="01f9a-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="01f9a-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01f9a-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="01f9a-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01f9a-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="01f9a-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01f9a-151">Search-Flags</span></span>           | <span data-ttu-id="01f9a-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f9a-152">0x00000010</span></span>                        |
| <span data-ttu-id="01f9a-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01f9a-153">System-Flags</span></span>           | <span data-ttu-id="01f9a-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f9a-154">0x00000010</span></span>                        |
| <span data-ttu-id="01f9a-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="01f9a-155">Classes used in</span></span>        | [<span data-ttu-id="01f9a-156">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="01f9a-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="01f9a-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="01f9a-157">Windows Server 2003</span></span>



| <span data-ttu-id="01f9a-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="01f9a-158">Entry</span></span> | <span data-ttu-id="01f9a-159">Wert</span><span class="sxs-lookup"><span data-stu-id="01f9a-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="01f9a-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="01f9a-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="01f9a-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01f9a-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="01f9a-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="01f9a-162">System-Only</span></span>            | <span data-ttu-id="01f9a-163">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-163">False</span></span>                             |
| <span data-ttu-id="01f9a-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="01f9a-164">Is-Single-Valued</span></span>       | <span data-ttu-id="01f9a-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="01f9a-165">True</span></span>                              |
| <span data-ttu-id="01f9a-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="01f9a-166">Is Indexed</span></span>             | <span data-ttu-id="01f9a-167">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-167">False</span></span>                             |
| <span data-ttu-id="01f9a-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="01f9a-168">In Global Catalog</span></span>      | <span data-ttu-id="01f9a-169">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-169">False</span></span>                             |
| <span data-ttu-id="01f9a-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="01f9a-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="01f9a-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="01f9a-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="01f9a-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01f9a-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="01f9a-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01f9a-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="01f9a-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01f9a-174">Search-Flags</span></span>           | <span data-ttu-id="01f9a-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f9a-175">0x00000010</span></span>                        |
| <span data-ttu-id="01f9a-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01f9a-176">System-Flags</span></span>           | <span data-ttu-id="01f9a-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f9a-177">0x00000010</span></span>                        |
| <span data-ttu-id="01f9a-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="01f9a-178">Classes used in</span></span>        | [<span data-ttu-id="01f9a-179">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="01f9a-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="01f9a-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="01f9a-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="01f9a-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="01f9a-181">Entry</span></span> | <span data-ttu-id="01f9a-182">Wert</span><span class="sxs-lookup"><span data-stu-id="01f9a-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="01f9a-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="01f9a-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="01f9a-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01f9a-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="01f9a-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="01f9a-185">System-Only</span></span>            | <span data-ttu-id="01f9a-186">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-186">False</span></span>                             |
| <span data-ttu-id="01f9a-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="01f9a-187">Is-Single-Valued</span></span>       | <span data-ttu-id="01f9a-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="01f9a-188">True</span></span>                              |
| <span data-ttu-id="01f9a-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="01f9a-189">Is Indexed</span></span>             | <span data-ttu-id="01f9a-190">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-190">False</span></span>                             |
| <span data-ttu-id="01f9a-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="01f9a-191">In Global Catalog</span></span>      | <span data-ttu-id="01f9a-192">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-192">False</span></span>                             |
| <span data-ttu-id="01f9a-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="01f9a-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="01f9a-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="01f9a-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="01f9a-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01f9a-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="01f9a-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01f9a-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="01f9a-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01f9a-197">Search-Flags</span></span>           | <span data-ttu-id="01f9a-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f9a-198">0x00000010</span></span>                        |
| <span data-ttu-id="01f9a-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01f9a-199">System-Flags</span></span>           | <span data-ttu-id="01f9a-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f9a-200">0x00000010</span></span>                        |
| <span data-ttu-id="01f9a-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="01f9a-201">Classes used in</span></span>        | [<span data-ttu-id="01f9a-202">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="01f9a-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="01f9a-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01f9a-203">Windows Server 2008</span></span>



| <span data-ttu-id="01f9a-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="01f9a-204">Entry</span></span> | <span data-ttu-id="01f9a-205">Wert</span><span class="sxs-lookup"><span data-stu-id="01f9a-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="01f9a-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="01f9a-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="01f9a-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01f9a-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="01f9a-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="01f9a-208">System-Only</span></span>            | <span data-ttu-id="01f9a-209">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-209">False</span></span>                             |
| <span data-ttu-id="01f9a-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="01f9a-210">Is-Single-Valued</span></span>       | <span data-ttu-id="01f9a-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="01f9a-211">True</span></span>                              |
| <span data-ttu-id="01f9a-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="01f9a-212">Is Indexed</span></span>             | <span data-ttu-id="01f9a-213">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-213">False</span></span>                             |
| <span data-ttu-id="01f9a-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="01f9a-214">In Global Catalog</span></span>      | <span data-ttu-id="01f9a-215">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-215">False</span></span>                             |
| <span data-ttu-id="01f9a-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="01f9a-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="01f9a-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="01f9a-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="01f9a-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01f9a-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="01f9a-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01f9a-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="01f9a-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01f9a-220">Search-Flags</span></span>           | <span data-ttu-id="01f9a-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f9a-221">0x00000010</span></span>                        |
| <span data-ttu-id="01f9a-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01f9a-222">System-Flags</span></span>           | <span data-ttu-id="01f9a-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f9a-223">0x00000010</span></span>                        |
| <span data-ttu-id="01f9a-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="01f9a-224">Classes used in</span></span>        | [<span data-ttu-id="01f9a-225">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="01f9a-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="01f9a-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="01f9a-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="01f9a-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="01f9a-227">Entry</span></span> | <span data-ttu-id="01f9a-228">Wert</span><span class="sxs-lookup"><span data-stu-id="01f9a-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="01f9a-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="01f9a-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="01f9a-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01f9a-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="01f9a-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="01f9a-231">System-Only</span></span>            | <span data-ttu-id="01f9a-232">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-232">False</span></span>                             |
| <span data-ttu-id="01f9a-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="01f9a-233">Is-Single-Valued</span></span>       | <span data-ttu-id="01f9a-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="01f9a-234">True</span></span>                              |
| <span data-ttu-id="01f9a-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="01f9a-235">Is Indexed</span></span>             | <span data-ttu-id="01f9a-236">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-236">False</span></span>                             |
| <span data-ttu-id="01f9a-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="01f9a-237">In Global Catalog</span></span>      | <span data-ttu-id="01f9a-238">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-238">False</span></span>                             |
| <span data-ttu-id="01f9a-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="01f9a-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="01f9a-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="01f9a-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="01f9a-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01f9a-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="01f9a-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01f9a-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="01f9a-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01f9a-243">Search-Flags</span></span>           | <span data-ttu-id="01f9a-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f9a-244">0x00000010</span></span>                        |
| <span data-ttu-id="01f9a-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01f9a-245">System-Flags</span></span>           | <span data-ttu-id="01f9a-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f9a-246">0x00000010</span></span>                        |
| <span data-ttu-id="01f9a-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="01f9a-247">Classes used in</span></span>        | [<span data-ttu-id="01f9a-248">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="01f9a-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="01f9a-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="01f9a-249">Windows Server 2012</span></span>



| <span data-ttu-id="01f9a-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="01f9a-250">Entry</span></span> | <span data-ttu-id="01f9a-251">Wert</span><span class="sxs-lookup"><span data-stu-id="01f9a-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="01f9a-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="01f9a-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="01f9a-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01f9a-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="01f9a-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="01f9a-254">System-Only</span></span>            | <span data-ttu-id="01f9a-255">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-255">False</span></span>                             |
| <span data-ttu-id="01f9a-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="01f9a-256">Is-Single-Valued</span></span>       | <span data-ttu-id="01f9a-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="01f9a-257">True</span></span>                              |
| <span data-ttu-id="01f9a-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="01f9a-258">Is Indexed</span></span>             | <span data-ttu-id="01f9a-259">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-259">False</span></span>                             |
| <span data-ttu-id="01f9a-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="01f9a-260">In Global Catalog</span></span>      | <span data-ttu-id="01f9a-261">False</span><span class="sxs-lookup"><span data-stu-id="01f9a-261">False</span></span>                             |
| <span data-ttu-id="01f9a-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="01f9a-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="01f9a-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="01f9a-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="01f9a-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01f9a-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="01f9a-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01f9a-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="01f9a-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01f9a-266">Search-Flags</span></span>           | <span data-ttu-id="01f9a-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f9a-267">0x00000010</span></span>                        |
| <span data-ttu-id="01f9a-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01f9a-268">System-Flags</span></span>           | <span data-ttu-id="01f9a-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01f9a-269">0x00000010</span></span>                        |
| <span data-ttu-id="01f9a-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="01f9a-270">Classes used in</span></span>        | [<span data-ttu-id="01f9a-271">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="01f9a-271">**User**</span></span>](c-user.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="01f9a-272">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01f9a-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01f9a-273">**homedirectory**</span><span class="sxs-lookup"><span data-stu-id="01f9a-273">**homeDirectory**</span></span>](a-homedirectory.md)
</dt> </dl>

 

 





