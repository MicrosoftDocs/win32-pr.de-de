---
title: User-Workstations-Attribut
description: Enthält die NetBIOS-oder DNS-Namen der Computer, auf denen die Windows NT-Arbeitsstation oder Windows 2000 Professional ausgeführt wird, von der der Benutzer sich anmelden kann.
ms.assetid: 92af070b-dadd-404d-8305-d85974639958
ms.tgt_platform: multiple
keywords:
- AD-Schema für User-Workstations-Attribut
- userworkstations-Attribut AD-Schema
topic_type:
- apiref
api_name:
- User-Workstations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cad59905dbf24c8baa13969d9a2ce5452767163
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859553"
---
# <a name="user-workstations-attribute"></a><span data-ttu-id="96721-105">User-Workstations-Attribut</span><span class="sxs-lookup"><span data-stu-id="96721-105">User-Workstations attribute</span></span>

<span data-ttu-id="96721-106">Enthält die NetBIOS-oder DNS-Namen der Computer, auf denen die Windows NT-Arbeitsstation oder Windows 2000 Professional ausgeführt wird, von der der Benutzer sich anmelden kann.</span><span class="sxs-lookup"><span data-stu-id="96721-106">Contains the NetBIOS or DNS names of the computers running Windows NT Workstation or Windows 2000 Professional from which the user can log on.</span></span> <span data-ttu-id="96721-107">Jeder NetBIOS-Name wird durch ein Komma getrennt.</span><span class="sxs-lookup"><span data-stu-id="96721-107">Each NetBIOS name is separated by a comma.</span></span> <span data-ttu-id="96721-108">Mehrere Namen sollten durch Kommas getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="96721-108">Multiple names should be separated by commas.</span></span>

>[!Note]
><span data-ttu-id="96721-109">Dieses Benutzer Attribut sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96721-109">This user attribute should not be used anymore.</span></span> <span data-ttu-id="96721-110">Zum Verwalten der Konten, die sich bei den Arbeitsstationen anmelden können, empfiehlt es sich, die Option "Lokales anmelden zulassen" und "Lokal anmelden zulassen" oder "Anmelden über Remotedesktopdienste zulassen" und "anmelden durch Remotedesktopdienste zulassen" zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="96721-110">To manage what accounts can logon to which workstations, we recommend using the “Allow Log on locally” and “Deny Log on locally” or “Allow log on through Remote Desktop Services” and “Deny log on through Remote Desktop Services”.</span></span>

| <span data-ttu-id="96721-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96721-111">Entry</span></span> | <span data-ttu-id="96721-112">Wert</span><span class="sxs-lookup"><span data-stu-id="96721-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="96721-113">CN</span><span class="sxs-lookup"><span data-stu-id="96721-113">CN</span></span>                | <span data-ttu-id="96721-114">User-Workstations</span><span class="sxs-lookup"><span data-stu-id="96721-114">User-Workstations</span></span>                                                                          |
| <span data-ttu-id="96721-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="96721-115">Ldap-Display-Name</span></span> | <span data-ttu-id="96721-116">Benutzer Arbeitsstationen</span><span class="sxs-lookup"><span data-stu-id="96721-116">userWorkstations</span></span>                                                                           |
| <span data-ttu-id="96721-117">Size</span><span class="sxs-lookup"><span data-stu-id="96721-117">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="96721-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="96721-118">Update Privilege</span></span>  | <span data-ttu-id="96721-119">Domänen Administrator oder Konto Besitzer.</span><span class="sxs-lookup"><span data-stu-id="96721-119">Domain administrator or account owner.</span></span>                                                     |
| <span data-ttu-id="96721-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="96721-120">Update Frequency</span></span>  | <span data-ttu-id="96721-121">Wenn der Benutzerdaten Satz erstellt wird, und immer dann, wenn die Anmelde Berechtigung des Benutzers geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="96721-121">When the user's record is created and whenever the user's login privilege needs to change.</span></span> |
| <span data-ttu-id="96721-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="96721-122">Attribute-Id</span></span>      | <span data-ttu-id="96721-123">1.2.840.113556.1.4.86</span><span class="sxs-lookup"><span data-stu-id="96721-123">1.2.840.113556.1.4.86</span></span>                                                                      |
| <span data-ttu-id="96721-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="96721-124">System-Id-Guid</span></span>    | <span data-ttu-id="96721-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="96721-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span></span>                                                       |
| <span data-ttu-id="96721-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="96721-126">Syntax</span></span>            | [<span data-ttu-id="96721-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="96721-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="96721-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="96721-128">Implementations</span></span>

-   [<span data-ttu-id="96721-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="96721-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="96721-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="96721-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="96721-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="96721-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="96721-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="96721-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="96721-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="96721-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="96721-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="96721-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="96721-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="96721-135">Windows 2000 Server</span></span>



| <span data-ttu-id="96721-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96721-136">Entry</span></span> | <span data-ttu-id="96721-137">Wert</span><span class="sxs-lookup"><span data-stu-id="96721-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96721-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96721-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96721-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96721-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96721-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="96721-140">System-Only</span></span>            | <span data-ttu-id="96721-141">False</span><span class="sxs-lookup"><span data-stu-id="96721-141">False</span></span>                             |
| <span data-ttu-id="96721-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96721-142">Is-Single-Valued</span></span>       | <span data-ttu-id="96721-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="96721-143">True</span></span>                              |
| <span data-ttu-id="96721-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96721-144">Is Indexed</span></span>             | <span data-ttu-id="96721-145">False</span><span class="sxs-lookup"><span data-stu-id="96721-145">False</span></span>                             |
| <span data-ttu-id="96721-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96721-146">In Global Catalog</span></span>      | <span data-ttu-id="96721-147">False</span><span class="sxs-lookup"><span data-stu-id="96721-147">False</span></span>                             |
| <span data-ttu-id="96721-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96721-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="96721-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96721-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96721-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96721-150">Range-Lower</span></span>            | <span data-ttu-id="96721-151">0</span><span class="sxs-lookup"><span data-stu-id="96721-151">0</span></span>                                 |
| <span data-ttu-id="96721-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96721-152">Range-Upper</span></span>            | <span data-ttu-id="96721-153">1024</span><span class="sxs-lookup"><span data-stu-id="96721-153">1024</span></span>                              |
| <span data-ttu-id="96721-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96721-154">Search-Flags</span></span>           | <span data-ttu-id="96721-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96721-155">0x00000010</span></span>                        |
| <span data-ttu-id="96721-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96721-156">System-Flags</span></span>           | <span data-ttu-id="96721-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96721-157">0x00000010</span></span>                        |
| <span data-ttu-id="96721-158">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96721-158">Classes used in</span></span>        | [<span data-ttu-id="96721-159">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="96721-159">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="96721-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="96721-160">Windows Server 2003</span></span>



| <span data-ttu-id="96721-161">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96721-161">Entry</span></span> | <span data-ttu-id="96721-162">Wert</span><span class="sxs-lookup"><span data-stu-id="96721-162">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96721-163">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96721-163">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96721-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96721-164">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96721-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="96721-165">System-Only</span></span>            | <span data-ttu-id="96721-166">False</span><span class="sxs-lookup"><span data-stu-id="96721-166">False</span></span>                             |
| <span data-ttu-id="96721-167">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96721-167">Is-Single-Valued</span></span>       | <span data-ttu-id="96721-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="96721-168">True</span></span>                              |
| <span data-ttu-id="96721-169">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96721-169">Is Indexed</span></span>             | <span data-ttu-id="96721-170">False</span><span class="sxs-lookup"><span data-stu-id="96721-170">False</span></span>                             |
| <span data-ttu-id="96721-171">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96721-171">In Global Catalog</span></span>      | <span data-ttu-id="96721-172">False</span><span class="sxs-lookup"><span data-stu-id="96721-172">False</span></span>                             |
| <span data-ttu-id="96721-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96721-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="96721-174">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96721-174">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96721-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96721-175">Range-Lower</span></span>            | <span data-ttu-id="96721-176">0</span><span class="sxs-lookup"><span data-stu-id="96721-176">0</span></span>                                 |
| <span data-ttu-id="96721-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96721-177">Range-Upper</span></span>            | <span data-ttu-id="96721-178">1024</span><span class="sxs-lookup"><span data-stu-id="96721-178">1024</span></span>                              |
| <span data-ttu-id="96721-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96721-179">Search-Flags</span></span>           | <span data-ttu-id="96721-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96721-180">0x00000010</span></span>                        |
| <span data-ttu-id="96721-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96721-181">System-Flags</span></span>           | <span data-ttu-id="96721-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96721-182">0x00000010</span></span>                        |
| <span data-ttu-id="96721-183">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96721-183">Classes used in</span></span>        | [<span data-ttu-id="96721-184">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="96721-184">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="96721-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="96721-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="96721-186">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96721-186">Entry</span></span> | <span data-ttu-id="96721-187">Wert</span><span class="sxs-lookup"><span data-stu-id="96721-187">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96721-188">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96721-188">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96721-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96721-189">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96721-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="96721-190">System-Only</span></span>            | <span data-ttu-id="96721-191">False</span><span class="sxs-lookup"><span data-stu-id="96721-191">False</span></span>                             |
| <span data-ttu-id="96721-192">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96721-192">Is-Single-Valued</span></span>       | <span data-ttu-id="96721-193">Richtig</span><span class="sxs-lookup"><span data-stu-id="96721-193">True</span></span>                              |
| <span data-ttu-id="96721-194">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96721-194">Is Indexed</span></span>             | <span data-ttu-id="96721-195">False</span><span class="sxs-lookup"><span data-stu-id="96721-195">False</span></span>                             |
| <span data-ttu-id="96721-196">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96721-196">In Global Catalog</span></span>      | <span data-ttu-id="96721-197">False</span><span class="sxs-lookup"><span data-stu-id="96721-197">False</span></span>                             |
| <span data-ttu-id="96721-198">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96721-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="96721-199">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96721-199">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96721-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96721-200">Range-Lower</span></span>            | <span data-ttu-id="96721-201">0</span><span class="sxs-lookup"><span data-stu-id="96721-201">0</span></span>                                 |
| <span data-ttu-id="96721-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96721-202">Range-Upper</span></span>            | <span data-ttu-id="96721-203">1024</span><span class="sxs-lookup"><span data-stu-id="96721-203">1024</span></span>                              |
| <span data-ttu-id="96721-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96721-204">Search-Flags</span></span>           | <span data-ttu-id="96721-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96721-205">0x00000010</span></span>                        |
| <span data-ttu-id="96721-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96721-206">System-Flags</span></span>           | <span data-ttu-id="96721-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96721-207">0x00000010</span></span>                        |
| <span data-ttu-id="96721-208">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96721-208">Classes used in</span></span>        | [<span data-ttu-id="96721-209">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="96721-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="96721-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96721-210">Windows Server 2008</span></span>



| <span data-ttu-id="96721-211">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96721-211">Entry</span></span> | <span data-ttu-id="96721-212">Wert</span><span class="sxs-lookup"><span data-stu-id="96721-212">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96721-213">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96721-213">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96721-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96721-214">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96721-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="96721-215">System-Only</span></span>            | <span data-ttu-id="96721-216">False</span><span class="sxs-lookup"><span data-stu-id="96721-216">False</span></span>                             |
| <span data-ttu-id="96721-217">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96721-217">Is-Single-Valued</span></span>       | <span data-ttu-id="96721-218">Richtig</span><span class="sxs-lookup"><span data-stu-id="96721-218">True</span></span>                              |
| <span data-ttu-id="96721-219">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96721-219">Is Indexed</span></span>             | <span data-ttu-id="96721-220">False</span><span class="sxs-lookup"><span data-stu-id="96721-220">False</span></span>                             |
| <span data-ttu-id="96721-221">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96721-221">In Global Catalog</span></span>      | <span data-ttu-id="96721-222">False</span><span class="sxs-lookup"><span data-stu-id="96721-222">False</span></span>                             |
| <span data-ttu-id="96721-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96721-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="96721-224">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96721-224">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96721-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96721-225">Range-Lower</span></span>            | <span data-ttu-id="96721-226">0</span><span class="sxs-lookup"><span data-stu-id="96721-226">0</span></span>                                 |
| <span data-ttu-id="96721-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96721-227">Range-Upper</span></span>            | <span data-ttu-id="96721-228">1024</span><span class="sxs-lookup"><span data-stu-id="96721-228">1024</span></span>                              |
| <span data-ttu-id="96721-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96721-229">Search-Flags</span></span>           | <span data-ttu-id="96721-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96721-230">0x00000010</span></span>                        |
| <span data-ttu-id="96721-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96721-231">System-Flags</span></span>           | <span data-ttu-id="96721-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96721-232">0x00000010</span></span>                        |
| <span data-ttu-id="96721-233">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96721-233">Classes used in</span></span>        | [<span data-ttu-id="96721-234">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="96721-234">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="96721-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="96721-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="96721-236">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96721-236">Entry</span></span> | <span data-ttu-id="96721-237">Wert</span><span class="sxs-lookup"><span data-stu-id="96721-237">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96721-238">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96721-238">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96721-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96721-239">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96721-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="96721-240">System-Only</span></span>            | <span data-ttu-id="96721-241">False</span><span class="sxs-lookup"><span data-stu-id="96721-241">False</span></span>                             |
| <span data-ttu-id="96721-242">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96721-242">Is-Single-Valued</span></span>       | <span data-ttu-id="96721-243">Richtig</span><span class="sxs-lookup"><span data-stu-id="96721-243">True</span></span>                              |
| <span data-ttu-id="96721-244">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96721-244">Is Indexed</span></span>             | <span data-ttu-id="96721-245">False</span><span class="sxs-lookup"><span data-stu-id="96721-245">False</span></span>                             |
| <span data-ttu-id="96721-246">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96721-246">In Global Catalog</span></span>      | <span data-ttu-id="96721-247">False</span><span class="sxs-lookup"><span data-stu-id="96721-247">False</span></span>                             |
| <span data-ttu-id="96721-248">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96721-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="96721-249">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96721-249">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96721-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96721-250">Range-Lower</span></span>            | <span data-ttu-id="96721-251">0</span><span class="sxs-lookup"><span data-stu-id="96721-251">0</span></span>                                 |
| <span data-ttu-id="96721-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96721-252">Range-Upper</span></span>            | <span data-ttu-id="96721-253">1024</span><span class="sxs-lookup"><span data-stu-id="96721-253">1024</span></span>                              |
| <span data-ttu-id="96721-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96721-254">Search-Flags</span></span>           | <span data-ttu-id="96721-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96721-255">0x00000010</span></span>                        |
| <span data-ttu-id="96721-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96721-256">System-Flags</span></span>           | <span data-ttu-id="96721-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96721-257">0x00000010</span></span>                        |
| <span data-ttu-id="96721-258">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96721-258">Classes used in</span></span>        | [<span data-ttu-id="96721-259">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="96721-259">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="96721-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="96721-260">Windows Server 2012</span></span>



| <span data-ttu-id="96721-261">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96721-261">Entry</span></span> | <span data-ttu-id="96721-262">Wert</span><span class="sxs-lookup"><span data-stu-id="96721-262">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="96721-263">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96721-263">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="96721-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96721-264">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="96721-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="96721-265">System-Only</span></span>            | <span data-ttu-id="96721-266">False</span><span class="sxs-lookup"><span data-stu-id="96721-266">False</span></span>                             |
| <span data-ttu-id="96721-267">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96721-267">Is-Single-Valued</span></span>       | <span data-ttu-id="96721-268">Richtig</span><span class="sxs-lookup"><span data-stu-id="96721-268">True</span></span>                              |
| <span data-ttu-id="96721-269">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96721-269">Is Indexed</span></span>             | <span data-ttu-id="96721-270">False</span><span class="sxs-lookup"><span data-stu-id="96721-270">False</span></span>                             |
| <span data-ttu-id="96721-271">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96721-271">In Global Catalog</span></span>      | <span data-ttu-id="96721-272">False</span><span class="sxs-lookup"><span data-stu-id="96721-272">False</span></span>                             |
| <span data-ttu-id="96721-273">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96721-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="96721-274">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96721-274">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="96721-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96721-275">Range-Lower</span></span>            | <span data-ttu-id="96721-276">0</span><span class="sxs-lookup"><span data-stu-id="96721-276">0</span></span>                                 |
| <span data-ttu-id="96721-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96721-277">Range-Upper</span></span>            | <span data-ttu-id="96721-278">1024</span><span class="sxs-lookup"><span data-stu-id="96721-278">1024</span></span>                              |
| <span data-ttu-id="96721-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96721-279">Search-Flags</span></span>           | <span data-ttu-id="96721-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96721-280">0x00000010</span></span>                        |
| <span data-ttu-id="96721-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96721-281">System-Flags</span></span>           | <span data-ttu-id="96721-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96721-282">0x00000010</span></span>                        |
| <span data-ttu-id="96721-283">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96721-283">Classes used in</span></span>        | [<span data-ttu-id="96721-284">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="96721-284">**User**</span></span>](c-user.md)<br/> |



 

 





