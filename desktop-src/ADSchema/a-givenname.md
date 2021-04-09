---
title: Given-Name-Attribut
description: Enthält den angegebenen Namen (Vorname) des Benutzers.
ms.assetid: acffe751-9911-4e80-8a26-351a21a6385e
ms.tgt_platform: multiple
keywords:
- AD-Schema für Given-Name-Attribut
- givenName-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Given-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76ab181c6aaf03c2a497be1718df789bfddc6b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859732"
---
# <a name="given-name-attribute"></a><span data-ttu-id="f2773-105">Given-Name-Attribut</span><span class="sxs-lookup"><span data-stu-id="f2773-105">Given-Name attribute</span></span>

<span data-ttu-id="f2773-106">Enthält den angegebenen Namen (Vorname) des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="f2773-106">Contains the given name (first name) of the user.</span></span>



| <span data-ttu-id="f2773-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2773-107">Entry</span></span> | <span data-ttu-id="f2773-108">Wert</span><span class="sxs-lookup"><span data-stu-id="f2773-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f2773-109">CN</span><span class="sxs-lookup"><span data-stu-id="f2773-109">CN</span></span>                | <span data-ttu-id="f2773-110">Vorname</span><span class="sxs-lookup"><span data-stu-id="f2773-110">Given-Name</span></span>                                  |
| <span data-ttu-id="f2773-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f2773-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f2773-112">givenName</span><span class="sxs-lookup"><span data-stu-id="f2773-112">givenName</span></span>                                   |
| <span data-ttu-id="f2773-113">Size</span><span class="sxs-lookup"><span data-stu-id="f2773-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="f2773-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f2773-114">Update Privilege</span></span>  | <span data-ttu-id="f2773-115">Domänen Administrator oder Konto Besitzer.</span><span class="sxs-lookup"><span data-stu-id="f2773-115">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="f2773-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f2773-116">Update Frequency</span></span>  | <span data-ttu-id="f2773-117">Wenn der Benutzerdaten Satz erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f2773-117">When the user's record is created.</span></span>          |
| <span data-ttu-id="f2773-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f2773-118">Attribute-Id</span></span>      | <span data-ttu-id="f2773-119">2.5.4.42</span><span class="sxs-lookup"><span data-stu-id="f2773-119">2.5.4.42</span></span>                                    |
| <span data-ttu-id="f2773-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f2773-120">System-Id-Guid</span></span>    | <span data-ttu-id="f2773-121">f0f8ff8e-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="f2773-121">f0f8ff8e-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="f2773-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2773-122">Syntax</span></span>            | [<span data-ttu-id="f2773-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f2773-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f2773-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f2773-124">Implementations</span></span>

-   [<span data-ttu-id="f2773-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f2773-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f2773-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f2773-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f2773-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f2773-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f2773-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f2773-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f2773-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f2773-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f2773-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f2773-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f2773-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f2773-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f2773-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2773-132">Entry</span></span> | <span data-ttu-id="f2773-133">Wert</span><span class="sxs-lookup"><span data-stu-id="f2773-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="f2773-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f2773-134">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="f2773-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2773-135">MAPI-Id</span></span>                | <span data-ttu-id="f2773-136">0x3a06</span><span class="sxs-lookup"><span data-stu-id="f2773-136">0x3A06</span></span>                                                             |
| <span data-ttu-id="f2773-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2773-137">System-Only</span></span>            | <span data-ttu-id="f2773-138">False</span><span class="sxs-lookup"><span data-stu-id="f2773-138">False</span></span>                                                              |
| <span data-ttu-id="f2773-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f2773-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f2773-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-140">True</span></span>                                                               |
| <span data-ttu-id="f2773-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f2773-141">Is Indexed</span></span>             | <span data-ttu-id="f2773-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-142">True</span></span>                                                               |
| <span data-ttu-id="f2773-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f2773-143">In Global Catalog</span></span>      | <span data-ttu-id="f2773-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-144">True</span></span>                                                               |
| <span data-ttu-id="f2773-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f2773-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2773-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f2773-146">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="f2773-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2773-147">Range-Lower</span></span>            | <span data-ttu-id="f2773-148">1</span><span class="sxs-lookup"><span data-stu-id="f2773-148">1</span></span>                                                                  |
| <span data-ttu-id="f2773-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2773-149">Range-Upper</span></span>            | <span data-ttu-id="f2773-150">64</span><span class="sxs-lookup"><span data-stu-id="f2773-150">64</span></span>                                                                 |
| <span data-ttu-id="f2773-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2773-151">Search-Flags</span></span>           | <span data-ttu-id="f2773-152">0x00000005</span><span class="sxs-lookup"><span data-stu-id="f2773-152">0x00000005</span></span>                                                         |
| <span data-ttu-id="f2773-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2773-153">System-Flags</span></span>           | <span data-ttu-id="f2773-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2773-154">0x00000010</span></span>                                                         |
| <span data-ttu-id="f2773-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f2773-155">Classes used in</span></span>        | [<span data-ttu-id="f2773-156">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="f2773-156">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f2773-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f2773-157">Windows Server 2003</span></span>



| <span data-ttu-id="f2773-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2773-158">Entry</span></span> | <span data-ttu-id="f2773-159">Wert</span><span class="sxs-lookup"><span data-stu-id="f2773-159">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2773-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f2773-160">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f2773-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2773-161">MAPI-Id</span></span>                | <span data-ttu-id="f2773-162">0x3a06</span><span class="sxs-lookup"><span data-stu-id="f2773-162">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="f2773-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2773-163">System-Only</span></span>            | <span data-ttu-id="f2773-164">False</span><span class="sxs-lookup"><span data-stu-id="f2773-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="f2773-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f2773-165">Is-Single-Valued</span></span>       | <span data-ttu-id="f2773-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-166">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2773-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f2773-167">Is Indexed</span></span>             | <span data-ttu-id="f2773-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-168">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2773-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f2773-169">In Global Catalog</span></span>      | <span data-ttu-id="f2773-170">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-170">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2773-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f2773-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2773-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f2773-172">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="f2773-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2773-173">Range-Lower</span></span>            | <span data-ttu-id="f2773-174">1</span><span class="sxs-lookup"><span data-stu-id="f2773-174">1</span></span>                                                                                                                      |
| <span data-ttu-id="f2773-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2773-175">Range-Upper</span></span>            | <span data-ttu-id="f2773-176">64</span><span class="sxs-lookup"><span data-stu-id="f2773-176">64</span></span>                                                                                                                     |
| <span data-ttu-id="f2773-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2773-177">Search-Flags</span></span>           | <span data-ttu-id="f2773-178">0x00000005</span><span class="sxs-lookup"><span data-stu-id="f2773-178">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="f2773-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2773-179">System-Flags</span></span>           | <span data-ttu-id="f2773-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2773-180">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="f2773-181">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f2773-181">Classes used in</span></span>        | [<span data-ttu-id="f2773-182">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="f2773-182">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="f2773-183">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="f2773-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f2773-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f2773-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f2773-185">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2773-185">Entry</span></span> | <span data-ttu-id="f2773-186">Wert</span><span class="sxs-lookup"><span data-stu-id="f2773-186">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2773-187">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f2773-187">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f2773-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2773-188">MAPI-Id</span></span>                | <span data-ttu-id="f2773-189">0x3a06</span><span class="sxs-lookup"><span data-stu-id="f2773-189">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="f2773-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2773-190">System-Only</span></span>            | <span data-ttu-id="f2773-191">False</span><span class="sxs-lookup"><span data-stu-id="f2773-191">False</span></span>                                                                                                                  |
| <span data-ttu-id="f2773-192">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f2773-192">Is-Single-Valued</span></span>       | <span data-ttu-id="f2773-193">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-193">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2773-194">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f2773-194">Is Indexed</span></span>             | <span data-ttu-id="f2773-195">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-195">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2773-196">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f2773-196">In Global Catalog</span></span>      | <span data-ttu-id="f2773-197">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-197">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2773-198">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f2773-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2773-199">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f2773-199">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="f2773-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2773-200">Range-Lower</span></span>            | <span data-ttu-id="f2773-201">1</span><span class="sxs-lookup"><span data-stu-id="f2773-201">1</span></span>                                                                                                                      |
| <span data-ttu-id="f2773-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2773-202">Range-Upper</span></span>            | <span data-ttu-id="f2773-203">64</span><span class="sxs-lookup"><span data-stu-id="f2773-203">64</span></span>                                                                                                                     |
| <span data-ttu-id="f2773-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2773-204">Search-Flags</span></span>           | <span data-ttu-id="f2773-205">0x00000005</span><span class="sxs-lookup"><span data-stu-id="f2773-205">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="f2773-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2773-206">System-Flags</span></span>           | <span data-ttu-id="f2773-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2773-207">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="f2773-208">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f2773-208">Classes used in</span></span>        | [<span data-ttu-id="f2773-209">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="f2773-209">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="f2773-210">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="f2773-210">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f2773-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2773-211">Windows Server 2008</span></span>



| <span data-ttu-id="f2773-212">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2773-212">Entry</span></span> | <span data-ttu-id="f2773-213">Wert</span><span class="sxs-lookup"><span data-stu-id="f2773-213">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2773-214">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f2773-214">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f2773-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2773-215">MAPI-Id</span></span>                | <span data-ttu-id="f2773-216">0x3a06</span><span class="sxs-lookup"><span data-stu-id="f2773-216">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="f2773-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2773-217">System-Only</span></span>            | <span data-ttu-id="f2773-218">False</span><span class="sxs-lookup"><span data-stu-id="f2773-218">False</span></span>                                                                                                                  |
| <span data-ttu-id="f2773-219">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f2773-219">Is-Single-Valued</span></span>       | <span data-ttu-id="f2773-220">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-220">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2773-221">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f2773-221">Is Indexed</span></span>             | <span data-ttu-id="f2773-222">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-222">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2773-223">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f2773-223">In Global Catalog</span></span>      | <span data-ttu-id="f2773-224">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-224">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2773-225">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f2773-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2773-226">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f2773-226">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="f2773-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2773-227">Range-Lower</span></span>            | <span data-ttu-id="f2773-228">1</span><span class="sxs-lookup"><span data-stu-id="f2773-228">1</span></span>                                                                                                                      |
| <span data-ttu-id="f2773-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2773-229">Range-Upper</span></span>            | <span data-ttu-id="f2773-230">64</span><span class="sxs-lookup"><span data-stu-id="f2773-230">64</span></span>                                                                                                                     |
| <span data-ttu-id="f2773-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2773-231">Search-Flags</span></span>           | <span data-ttu-id="f2773-232">0x00000005</span><span class="sxs-lookup"><span data-stu-id="f2773-232">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="f2773-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2773-233">System-Flags</span></span>           | <span data-ttu-id="f2773-234">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2773-234">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="f2773-235">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f2773-235">Classes used in</span></span>        | [<span data-ttu-id="f2773-236">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="f2773-236">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="f2773-237">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="f2773-237">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f2773-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f2773-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f2773-239">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2773-239">Entry</span></span> | <span data-ttu-id="f2773-240">Wert</span><span class="sxs-lookup"><span data-stu-id="f2773-240">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2773-241">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f2773-241">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f2773-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2773-242">MAPI-Id</span></span>                | <span data-ttu-id="f2773-243">0x3a06</span><span class="sxs-lookup"><span data-stu-id="f2773-243">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="f2773-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2773-244">System-Only</span></span>            | <span data-ttu-id="f2773-245">False</span><span class="sxs-lookup"><span data-stu-id="f2773-245">False</span></span>                                                                                                                  |
| <span data-ttu-id="f2773-246">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f2773-246">Is-Single-Valued</span></span>       | <span data-ttu-id="f2773-247">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-247">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2773-248">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f2773-248">Is Indexed</span></span>             | <span data-ttu-id="f2773-249">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-249">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2773-250">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f2773-250">In Global Catalog</span></span>      | <span data-ttu-id="f2773-251">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-251">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2773-252">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f2773-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2773-253">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f2773-253">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="f2773-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2773-254">Range-Lower</span></span>            | <span data-ttu-id="f2773-255">1</span><span class="sxs-lookup"><span data-stu-id="f2773-255">1</span></span>                                                                                                                      |
| <span data-ttu-id="f2773-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2773-256">Range-Upper</span></span>            | <span data-ttu-id="f2773-257">64</span><span class="sxs-lookup"><span data-stu-id="f2773-257">64</span></span>                                                                                                                     |
| <span data-ttu-id="f2773-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2773-258">Search-Flags</span></span>           | <span data-ttu-id="f2773-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="f2773-259">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="f2773-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2773-260">System-Flags</span></span>           | <span data-ttu-id="f2773-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2773-261">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="f2773-262">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f2773-262">Classes used in</span></span>        | [<span data-ttu-id="f2773-263">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="f2773-263">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="f2773-264">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="f2773-264">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f2773-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2773-265">Windows Server 2012</span></span>



| <span data-ttu-id="f2773-266">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2773-266">Entry</span></span> | <span data-ttu-id="f2773-267">Wert</span><span class="sxs-lookup"><span data-stu-id="f2773-267">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2773-268">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f2773-268">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f2773-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2773-269">MAPI-Id</span></span>                | <span data-ttu-id="f2773-270">0x3a06</span><span class="sxs-lookup"><span data-stu-id="f2773-270">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="f2773-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2773-271">System-Only</span></span>            | <span data-ttu-id="f2773-272">False</span><span class="sxs-lookup"><span data-stu-id="f2773-272">False</span></span>                                                                                                                  |
| <span data-ttu-id="f2773-273">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f2773-273">Is-Single-Valued</span></span>       | <span data-ttu-id="f2773-274">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-274">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2773-275">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f2773-275">Is Indexed</span></span>             | <span data-ttu-id="f2773-276">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-276">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2773-277">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f2773-277">In Global Catalog</span></span>      | <span data-ttu-id="f2773-278">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2773-278">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2773-279">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f2773-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2773-280">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f2773-280">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="f2773-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2773-281">Range-Lower</span></span>            | <span data-ttu-id="f2773-282">1</span><span class="sxs-lookup"><span data-stu-id="f2773-282">1</span></span>                                                                                                                      |
| <span data-ttu-id="f2773-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2773-283">Range-Upper</span></span>            | <span data-ttu-id="f2773-284">64</span><span class="sxs-lookup"><span data-stu-id="f2773-284">64</span></span>                                                                                                                     |
| <span data-ttu-id="f2773-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2773-285">Search-Flags</span></span>           | <span data-ttu-id="f2773-286">0x00000005</span><span class="sxs-lookup"><span data-stu-id="f2773-286">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="f2773-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2773-287">System-Flags</span></span>           | <span data-ttu-id="f2773-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2773-288">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="f2773-289">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f2773-289">Classes used in</span></span>        | [<span data-ttu-id="f2773-290">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="f2773-290">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="f2773-291">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="f2773-291">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





