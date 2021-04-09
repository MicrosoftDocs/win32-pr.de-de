---
title: MS-TS-profile-path-Attribut
description: Der Terminal Dienste-Profilpfad gibt einen roamingpfad oder obligatorischen Profilpfad an, der verwendet wird, wenn sich der Benutzer am Terminal Server anmeldet. Der Profilpfad befindet sich im folgenden Netzwerkpfad Format \\ \\ Servername \\ Profile Name Profile Name \\ username.
ms.assetid: 9b13f91d-c3ee-4862-800c-fda831dce859
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-TS-profile-path-Attribut
- mstsprofilepath-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- ms-TS-Profile-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67243c2ef588bd1470a50417c0948b1ea4ea7fa9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957474"
---
# <a name="ms-ts-profile-path-attribute"></a><span data-ttu-id="4af9a-106">MS-TS-profile-path-Attribut</span><span class="sxs-lookup"><span data-stu-id="4af9a-106">ms-TS-Profile-Path attribute</span></span>

<span data-ttu-id="4af9a-107">Der Terminal Dienste-Profilpfad gibt einen roamingpfad oder obligatorischen Profilpfad an, der verwendet wird, wenn sich der Benutzer am Terminal Server anmeldet.</span><span class="sxs-lookup"><span data-stu-id="4af9a-107">Terminal Services Profile Path specifies a roaming or mandatory profile path to use when the user logs on to the terminal server.</span></span> <span data-ttu-id="4af9a-108">Der Profilpfad weist das folgende Format für den Netzwerkpfad auf: **\\\\** _Server_ Name *_\\_* _profilesfoldername_ *_\\_* _Benutzername_.</span><span class="sxs-lookup"><span data-stu-id="4af9a-108">The profile path is in the following network path format: **\\\\**_ServerName_*_\\_*_ProfilesFolderName_*_\\_*_UserName_.</span></span>



| <span data-ttu-id="4af9a-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4af9a-109">Entry</span></span> | <span data-ttu-id="4af9a-110">Wert</span><span class="sxs-lookup"><span data-stu-id="4af9a-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="4af9a-111">CN</span><span class="sxs-lookup"><span data-stu-id="4af9a-111">CN</span></span>                | <span data-ttu-id="4af9a-112">MS-TS-profile-Path</span><span class="sxs-lookup"><span data-stu-id="4af9a-112">ms-TS-Profile-Path</span></span>                          |
| <span data-ttu-id="4af9a-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4af9a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4af9a-114">mstsprofilepath</span><span class="sxs-lookup"><span data-stu-id="4af9a-114">msTSProfilePath</span></span>                             |
| <span data-ttu-id="4af9a-115">Size</span><span class="sxs-lookup"><span data-stu-id="4af9a-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="4af9a-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="4af9a-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="4af9a-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="4af9a-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="4af9a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4af9a-118">Attribute-Id</span></span>      | <span data-ttu-id="4af9a-119">1.2.840.113556.1.4.1976</span><span class="sxs-lookup"><span data-stu-id="4af9a-119">1.2.840.113556.1.4.1976</span></span>                     |
| <span data-ttu-id="4af9a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4af9a-120">System-Id-Guid</span></span>    | <span data-ttu-id="4af9a-121">e65c30db-316c-4060-a3a0-387b083-CD</span><span class="sxs-lookup"><span data-stu-id="4af9a-121">e65c30db-316c-4060-a3a0-387b083f09cd</span></span>        |
| <span data-ttu-id="4af9a-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="4af9a-122">Syntax</span></span>            | [<span data-ttu-id="4af9a-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4af9a-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="4af9a-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="4af9a-124">Implementations</span></span>

-   [<span data-ttu-id="4af9a-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4af9a-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4af9a-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4af9a-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4af9a-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4af9a-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="4af9a-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4af9a-128">Windows Server 2008</span></span>



| <span data-ttu-id="4af9a-129">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4af9a-129">Entry</span></span> | <span data-ttu-id="4af9a-130">Wert</span><span class="sxs-lookup"><span data-stu-id="4af9a-130">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4af9a-131">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4af9a-131">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4af9a-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4af9a-132">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4af9a-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="4af9a-133">System-Only</span></span>            | <span data-ttu-id="4af9a-134">False</span><span class="sxs-lookup"><span data-stu-id="4af9a-134">False</span></span>                             |
| <span data-ttu-id="4af9a-135">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4af9a-135">Is-Single-Valued</span></span>       | <span data-ttu-id="4af9a-136">Richtig</span><span class="sxs-lookup"><span data-stu-id="4af9a-136">True</span></span>                              |
| <span data-ttu-id="4af9a-137">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4af9a-137">Is Indexed</span></span>             | <span data-ttu-id="4af9a-138">False</span><span class="sxs-lookup"><span data-stu-id="4af9a-138">False</span></span>                             |
| <span data-ttu-id="4af9a-139">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4af9a-139">In Global Catalog</span></span>      | <span data-ttu-id="4af9a-140">False</span><span class="sxs-lookup"><span data-stu-id="4af9a-140">False</span></span>                             |
| <span data-ttu-id="4af9a-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4af9a-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="4af9a-142">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4af9a-142">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4af9a-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4af9a-143">Range-Lower</span></span>            | <span data-ttu-id="4af9a-144">0</span><span class="sxs-lookup"><span data-stu-id="4af9a-144">0</span></span>                                 |
| <span data-ttu-id="4af9a-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4af9a-145">Range-Upper</span></span>            | <span data-ttu-id="4af9a-146">32767</span><span class="sxs-lookup"><span data-stu-id="4af9a-146">32767</span></span>                             |
| <span data-ttu-id="4af9a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4af9a-147">Search-Flags</span></span>           | <span data-ttu-id="4af9a-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4af9a-148">0x00000000</span></span>                        |
| <span data-ttu-id="4af9a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4af9a-149">System-Flags</span></span>           | <span data-ttu-id="4af9a-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4af9a-150">0x00000010</span></span>                        |
| <span data-ttu-id="4af9a-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4af9a-151">Classes used in</span></span>        | [<span data-ttu-id="4af9a-152">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="4af9a-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4af9a-153">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4af9a-153">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4af9a-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4af9a-154">Entry</span></span> | <span data-ttu-id="4af9a-155">Wert</span><span class="sxs-lookup"><span data-stu-id="4af9a-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4af9a-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4af9a-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4af9a-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4af9a-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4af9a-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="4af9a-158">System-Only</span></span>            | <span data-ttu-id="4af9a-159">False</span><span class="sxs-lookup"><span data-stu-id="4af9a-159">False</span></span>                             |
| <span data-ttu-id="4af9a-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4af9a-160">Is-Single-Valued</span></span>       | <span data-ttu-id="4af9a-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="4af9a-161">True</span></span>                              |
| <span data-ttu-id="4af9a-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4af9a-162">Is Indexed</span></span>             | <span data-ttu-id="4af9a-163">False</span><span class="sxs-lookup"><span data-stu-id="4af9a-163">False</span></span>                             |
| <span data-ttu-id="4af9a-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4af9a-164">In Global Catalog</span></span>      | <span data-ttu-id="4af9a-165">False</span><span class="sxs-lookup"><span data-stu-id="4af9a-165">False</span></span>                             |
| <span data-ttu-id="4af9a-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4af9a-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="4af9a-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4af9a-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4af9a-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4af9a-168">Range-Lower</span></span>            | <span data-ttu-id="4af9a-169">0</span><span class="sxs-lookup"><span data-stu-id="4af9a-169">0</span></span>                                 |
| <span data-ttu-id="4af9a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4af9a-170">Range-Upper</span></span>            | <span data-ttu-id="4af9a-171">32767</span><span class="sxs-lookup"><span data-stu-id="4af9a-171">32767</span></span>                             |
| <span data-ttu-id="4af9a-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4af9a-172">Search-Flags</span></span>           | <span data-ttu-id="4af9a-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4af9a-173">0x00000000</span></span>                        |
| <span data-ttu-id="4af9a-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4af9a-174">System-Flags</span></span>           | <span data-ttu-id="4af9a-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4af9a-175">0x00000010</span></span>                        |
| <span data-ttu-id="4af9a-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4af9a-176">Classes used in</span></span>        | [<span data-ttu-id="4af9a-177">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="4af9a-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4af9a-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4af9a-178">Windows Server 2012</span></span>



| <span data-ttu-id="4af9a-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4af9a-179">Entry</span></span> | <span data-ttu-id="4af9a-180">Wert</span><span class="sxs-lookup"><span data-stu-id="4af9a-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4af9a-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4af9a-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4af9a-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4af9a-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4af9a-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="4af9a-183">System-Only</span></span>            | <span data-ttu-id="4af9a-184">False</span><span class="sxs-lookup"><span data-stu-id="4af9a-184">False</span></span>                             |
| <span data-ttu-id="4af9a-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4af9a-185">Is-Single-Valued</span></span>       | <span data-ttu-id="4af9a-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="4af9a-186">True</span></span>                              |
| <span data-ttu-id="4af9a-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4af9a-187">Is Indexed</span></span>             | <span data-ttu-id="4af9a-188">False</span><span class="sxs-lookup"><span data-stu-id="4af9a-188">False</span></span>                             |
| <span data-ttu-id="4af9a-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4af9a-189">In Global Catalog</span></span>      | <span data-ttu-id="4af9a-190">False</span><span class="sxs-lookup"><span data-stu-id="4af9a-190">False</span></span>                             |
| <span data-ttu-id="4af9a-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4af9a-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="4af9a-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4af9a-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4af9a-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4af9a-193">Range-Lower</span></span>            | <span data-ttu-id="4af9a-194">0</span><span class="sxs-lookup"><span data-stu-id="4af9a-194">0</span></span>                                 |
| <span data-ttu-id="4af9a-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4af9a-195">Range-Upper</span></span>            | <span data-ttu-id="4af9a-196">32767</span><span class="sxs-lookup"><span data-stu-id="4af9a-196">32767</span></span>                             |
| <span data-ttu-id="4af9a-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4af9a-197">Search-Flags</span></span>           | <span data-ttu-id="4af9a-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4af9a-198">0x00000000</span></span>                        |
| <span data-ttu-id="4af9a-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4af9a-199">System-Flags</span></span>           | <span data-ttu-id="4af9a-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4af9a-200">0x00000010</span></span>                        |
| <span data-ttu-id="4af9a-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4af9a-201">Classes used in</span></span>        | [<span data-ttu-id="4af9a-202">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="4af9a-202">**User**</span></span>](c-user.md)<br/> |



 

 





