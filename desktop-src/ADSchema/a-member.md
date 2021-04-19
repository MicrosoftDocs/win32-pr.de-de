---
title: Member-Attribut
description: Die Liste der Benutzer, die zur Gruppe gehören.
ms.assetid: 0f5e249e-1fa1-4191-90e6-94c0b657b7fc
ms.tgt_platform: multiple
keywords:
- AD-Schema des Mitglieds Attributs
- AD-Schema des Mitglieds Attributs
topic_type:
- apiref
api_name:
- Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c237c7cb7b41ae73bcbdff5a13f6cb34f546449b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344735"
---
# <a name="member-attribute"></a><span data-ttu-id="b158b-105">Member-Attribut</span><span class="sxs-lookup"><span data-stu-id="b158b-105">Member attribute</span></span>

<span data-ttu-id="b158b-106">Die Liste der Benutzer, die zur Gruppe gehören.</span><span class="sxs-lookup"><span data-stu-id="b158b-106">The list of users that belong to the group.</span></span>



| <span data-ttu-id="b158b-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b158b-107">Entry</span></span> | <span data-ttu-id="b158b-108">Wert</span><span class="sxs-lookup"><span data-stu-id="b158b-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b158b-109">CN</span><span class="sxs-lookup"><span data-stu-id="b158b-109">CN</span></span>                | <span data-ttu-id="b158b-110">Member</span><span class="sxs-lookup"><span data-stu-id="b158b-110">Member</span></span>                                                |
| <span data-ttu-id="b158b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b158b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b158b-112">Member</span><span class="sxs-lookup"><span data-stu-id="b158b-112">member</span></span>                                                |
| <span data-ttu-id="b158b-113">Size</span><span class="sxs-lookup"><span data-stu-id="b158b-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="b158b-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b158b-114">Update Privilege</span></span>  | <span data-ttu-id="b158b-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="b158b-115">Domain administrator</span></span>                                  |
| <span data-ttu-id="b158b-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b158b-116">Update Frequency</span></span>  | <span data-ttu-id="b158b-117">Jedes Mal, wenn ein Benutzer einer Gruppe hinzugefügt oder daraus entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b158b-117">Each time a user is added to or removed from a group.</span></span> |
| <span data-ttu-id="b158b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b158b-118">Attribute-Id</span></span>      | <span data-ttu-id="b158b-119">2.5.4.31</span><span class="sxs-lookup"><span data-stu-id="b158b-119">2.5.4.31</span></span>                                              |
| <span data-ttu-id="b158b-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b158b-120">System-Id-Guid</span></span>    | <span data-ttu-id="b158b-121">bf9679c0-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b158b-121">bf9679c0-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="b158b-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="b158b-122">Syntax</span></span>            | [<span data-ttu-id="b158b-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="b158b-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)               |



## <a name="implementations"></a><span data-ttu-id="b158b-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b158b-124">Implementations</span></span>

-   [<span data-ttu-id="b158b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b158b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b158b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b158b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b158b-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="b158b-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b158b-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b158b-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b158b-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b158b-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b158b-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b158b-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b158b-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b158b-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b158b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b158b-132">Windows 2000 Server</span></span>



| <span data-ttu-id="b158b-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b158b-133">Entry</span></span> | <span data-ttu-id="b158b-134">Wert</span><span class="sxs-lookup"><span data-stu-id="b158b-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b158b-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b158b-135">Link-Id</span></span>                | <span data-ttu-id="b158b-136">2</span><span class="sxs-lookup"><span data-stu-id="b158b-136">2</span></span>                                                                                       |
| <span data-ttu-id="b158b-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b158b-137">MAPI-Id</span></span>                | <span data-ttu-id="b158b-138">0x8009</span><span class="sxs-lookup"><span data-stu-id="b158b-138">0x8009</span></span>                                                                                  |
| <span data-ttu-id="b158b-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b158b-139">System-Only</span></span>            | <span data-ttu-id="b158b-140">False</span><span class="sxs-lookup"><span data-stu-id="b158b-140">False</span></span>                                                                                   |
| <span data-ttu-id="b158b-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b158b-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b158b-142">False</span><span class="sxs-lookup"><span data-stu-id="b158b-142">False</span></span>                                                                                   |
| <span data-ttu-id="b158b-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b158b-143">Is Indexed</span></span>             | <span data-ttu-id="b158b-144">False</span><span class="sxs-lookup"><span data-stu-id="b158b-144">False</span></span>                                                                                   |
| <span data-ttu-id="b158b-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b158b-145">In Global Catalog</span></span>      | <span data-ttu-id="b158b-146">Richtig</span><span class="sxs-lookup"><span data-stu-id="b158b-146">True</span></span>                                                                                    |
| <span data-ttu-id="b158b-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b158b-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b158b-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b158b-148">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="b158b-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b158b-149">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="b158b-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b158b-150">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="b158b-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b158b-151">Search-Flags</span></span>           | <span data-ttu-id="b158b-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b158b-152">0x00000000</span></span>                                                                              |
| <span data-ttu-id="b158b-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b158b-153">System-Flags</span></span>           | <span data-ttu-id="b158b-154">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b158b-154">0x00000012</span></span>                                                                              |
| <span data-ttu-id="b158b-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b158b-155">Classes used in</span></span>        | [<span data-ttu-id="b158b-156">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="b158b-156">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="b158b-157">**Gruppe von Namen**</span><span class="sxs-lookup"><span data-stu-id="b158b-157">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b158b-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b158b-158">Windows Server 2003</span></span>



| <span data-ttu-id="b158b-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b158b-159">Entry</span></span> | <span data-ttu-id="b158b-160">Wert</span><span class="sxs-lookup"><span data-stu-id="b158b-160">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b158b-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b158b-161">Link-Id</span></span>                | <span data-ttu-id="b158b-162">2</span><span class="sxs-lookup"><span data-stu-id="b158b-162">2</span></span>                                                                                                                                     |
| <span data-ttu-id="b158b-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b158b-163">MAPI-Id</span></span>                | <span data-ttu-id="b158b-164">0x8009</span><span class="sxs-lookup"><span data-stu-id="b158b-164">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="b158b-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="b158b-165">System-Only</span></span>            | <span data-ttu-id="b158b-166">False</span><span class="sxs-lookup"><span data-stu-id="b158b-166">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b158b-167">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b158b-167">Is-Single-Valued</span></span>       | <span data-ttu-id="b158b-168">False</span><span class="sxs-lookup"><span data-stu-id="b158b-168">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b158b-169">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b158b-169">Is Indexed</span></span>             | <span data-ttu-id="b158b-170">False</span><span class="sxs-lookup"><span data-stu-id="b158b-170">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b158b-171">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b158b-171">In Global Catalog</span></span>      | <span data-ttu-id="b158b-172">Richtig</span><span class="sxs-lookup"><span data-stu-id="b158b-172">True</span></span>                                                                                                                                  |
| <span data-ttu-id="b158b-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b158b-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="b158b-174">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b158b-174">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="b158b-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b158b-175">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b158b-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b158b-176">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b158b-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b158b-177">Search-Flags</span></span>           | <span data-ttu-id="b158b-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b158b-178">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="b158b-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b158b-179">System-Flags</span></span>           | <span data-ttu-id="b158b-180">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b158b-180">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="b158b-181">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b158b-181">Classes used in</span></span>        | [<span data-ttu-id="b158b-182">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="b158b-182">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="b158b-183">**Gruppe von Namen**</span><span class="sxs-lookup"><span data-stu-id="b158b-183">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="b158b-184">**MSMQ-Gruppe**</span><span class="sxs-lookup"><span data-stu-id="b158b-184">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b158b-185">Adam</span><span class="sxs-lookup"><span data-stu-id="b158b-185">ADAM</span></span>



| <span data-ttu-id="b158b-186">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b158b-186">Entry</span></span> | <span data-ttu-id="b158b-187">Wert</span><span class="sxs-lookup"><span data-stu-id="b158b-187">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="b158b-188">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b158b-188">Link-Id</span></span>                | <span data-ttu-id="b158b-189">2</span><span class="sxs-lookup"><span data-stu-id="b158b-189">2</span></span>                                   |
| <span data-ttu-id="b158b-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b158b-190">MAPI-Id</span></span>                | <span data-ttu-id="b158b-191">0x8009</span><span class="sxs-lookup"><span data-stu-id="b158b-191">0x8009</span></span>                              |
| <span data-ttu-id="b158b-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="b158b-192">System-Only</span></span>            | <span data-ttu-id="b158b-193">False</span><span class="sxs-lookup"><span data-stu-id="b158b-193">False</span></span>                               |
| <span data-ttu-id="b158b-194">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b158b-194">Is-Single-Valued</span></span>       | <span data-ttu-id="b158b-195">False</span><span class="sxs-lookup"><span data-stu-id="b158b-195">False</span></span>                               |
| <span data-ttu-id="b158b-196">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b158b-196">Is Indexed</span></span>             | <span data-ttu-id="b158b-197">False</span><span class="sxs-lookup"><span data-stu-id="b158b-197">False</span></span>                               |
| <span data-ttu-id="b158b-198">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b158b-198">In Global Catalog</span></span>      | <span data-ttu-id="b158b-199">Richtig</span><span class="sxs-lookup"><span data-stu-id="b158b-199">True</span></span>                                |
| <span data-ttu-id="b158b-200">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b158b-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="b158b-201">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b158b-201">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="b158b-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b158b-202">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="b158b-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b158b-203">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="b158b-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b158b-204">Search-Flags</span></span>           | <span data-ttu-id="b158b-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b158b-205">0x00000000</span></span>                          |
| <span data-ttu-id="b158b-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b158b-206">System-Flags</span></span>           | <span data-ttu-id="b158b-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b158b-207">0x00000012</span></span>                          |
| <span data-ttu-id="b158b-208">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b158b-208">Classes used in</span></span>        | [<span data-ttu-id="b158b-209">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="b158b-209">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b158b-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b158b-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b158b-211">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b158b-211">Entry</span></span> | <span data-ttu-id="b158b-212">Wert</span><span class="sxs-lookup"><span data-stu-id="b158b-212">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b158b-213">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b158b-213">Link-Id</span></span>                | <span data-ttu-id="b158b-214">2</span><span class="sxs-lookup"><span data-stu-id="b158b-214">2</span></span>                                                                                                                                     |
| <span data-ttu-id="b158b-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b158b-215">MAPI-Id</span></span>                | <span data-ttu-id="b158b-216">0x8009</span><span class="sxs-lookup"><span data-stu-id="b158b-216">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="b158b-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="b158b-217">System-Only</span></span>            | <span data-ttu-id="b158b-218">False</span><span class="sxs-lookup"><span data-stu-id="b158b-218">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b158b-219">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b158b-219">Is-Single-Valued</span></span>       | <span data-ttu-id="b158b-220">False</span><span class="sxs-lookup"><span data-stu-id="b158b-220">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b158b-221">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b158b-221">Is Indexed</span></span>             | <span data-ttu-id="b158b-222">False</span><span class="sxs-lookup"><span data-stu-id="b158b-222">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b158b-223">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b158b-223">In Global Catalog</span></span>      | <span data-ttu-id="b158b-224">Richtig</span><span class="sxs-lookup"><span data-stu-id="b158b-224">True</span></span>                                                                                                                                  |
| <span data-ttu-id="b158b-225">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b158b-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="b158b-226">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b158b-226">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="b158b-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b158b-227">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b158b-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b158b-228">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b158b-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b158b-229">Search-Flags</span></span>           | <span data-ttu-id="b158b-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b158b-230">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="b158b-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b158b-231">System-Flags</span></span>           | <span data-ttu-id="b158b-232">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b158b-232">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="b158b-233">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b158b-233">Classes used in</span></span>        | [<span data-ttu-id="b158b-234">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="b158b-234">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="b158b-235">**Gruppe von Namen**</span><span class="sxs-lookup"><span data-stu-id="b158b-235">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="b158b-236">**MSMQ-Gruppe**</span><span class="sxs-lookup"><span data-stu-id="b158b-236">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b158b-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b158b-237">Windows Server 2008</span></span>



| <span data-ttu-id="b158b-238">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b158b-238">Entry</span></span> | <span data-ttu-id="b158b-239">Wert</span><span class="sxs-lookup"><span data-stu-id="b158b-239">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b158b-240">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b158b-240">Link-Id</span></span>                | <span data-ttu-id="b158b-241">2</span><span class="sxs-lookup"><span data-stu-id="b158b-241">2</span></span>                                                                                                                                     |
| <span data-ttu-id="b158b-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b158b-242">MAPI-Id</span></span>                | <span data-ttu-id="b158b-243">0x8009</span><span class="sxs-lookup"><span data-stu-id="b158b-243">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="b158b-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="b158b-244">System-Only</span></span>            | <span data-ttu-id="b158b-245">False</span><span class="sxs-lookup"><span data-stu-id="b158b-245">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b158b-246">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b158b-246">Is-Single-Valued</span></span>       | <span data-ttu-id="b158b-247">False</span><span class="sxs-lookup"><span data-stu-id="b158b-247">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b158b-248">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b158b-248">Is Indexed</span></span>             | <span data-ttu-id="b158b-249">False</span><span class="sxs-lookup"><span data-stu-id="b158b-249">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b158b-250">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b158b-250">In Global Catalog</span></span>      | <span data-ttu-id="b158b-251">Richtig</span><span class="sxs-lookup"><span data-stu-id="b158b-251">True</span></span>                                                                                                                                  |
| <span data-ttu-id="b158b-252">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b158b-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="b158b-253">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b158b-253">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="b158b-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b158b-254">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b158b-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b158b-255">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b158b-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b158b-256">Search-Flags</span></span>           | <span data-ttu-id="b158b-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b158b-257">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="b158b-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b158b-258">System-Flags</span></span>           | <span data-ttu-id="b158b-259">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b158b-259">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="b158b-260">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b158b-260">Classes used in</span></span>        | [<span data-ttu-id="b158b-261">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="b158b-261">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="b158b-262">**Gruppe von Namen**</span><span class="sxs-lookup"><span data-stu-id="b158b-262">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="b158b-263">**MSMQ-Gruppe**</span><span class="sxs-lookup"><span data-stu-id="b158b-263">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b158b-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b158b-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b158b-265">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b158b-265">Entry</span></span> | <span data-ttu-id="b158b-266">Wert</span><span class="sxs-lookup"><span data-stu-id="b158b-266">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b158b-267">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b158b-267">Link-Id</span></span>                | <span data-ttu-id="b158b-268">2</span><span class="sxs-lookup"><span data-stu-id="b158b-268">2</span></span>                                                                                                                                     |
| <span data-ttu-id="b158b-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b158b-269">MAPI-Id</span></span>                | <span data-ttu-id="b158b-270">0x8009</span><span class="sxs-lookup"><span data-stu-id="b158b-270">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="b158b-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="b158b-271">System-Only</span></span>            | <span data-ttu-id="b158b-272">False</span><span class="sxs-lookup"><span data-stu-id="b158b-272">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b158b-273">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b158b-273">Is-Single-Valued</span></span>       | <span data-ttu-id="b158b-274">False</span><span class="sxs-lookup"><span data-stu-id="b158b-274">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b158b-275">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b158b-275">Is Indexed</span></span>             | <span data-ttu-id="b158b-276">False</span><span class="sxs-lookup"><span data-stu-id="b158b-276">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b158b-277">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b158b-277">In Global Catalog</span></span>      | <span data-ttu-id="b158b-278">Richtig</span><span class="sxs-lookup"><span data-stu-id="b158b-278">True</span></span>                                                                                                                                  |
| <span data-ttu-id="b158b-279">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b158b-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="b158b-280">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b158b-280">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="b158b-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b158b-281">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b158b-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b158b-282">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b158b-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b158b-283">Search-Flags</span></span>           | <span data-ttu-id="b158b-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b158b-284">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="b158b-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b158b-285">System-Flags</span></span>           | <span data-ttu-id="b158b-286">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b158b-286">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="b158b-287">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b158b-287">Classes used in</span></span>        | [<span data-ttu-id="b158b-288">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="b158b-288">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="b158b-289">**Gruppe von Namen**</span><span class="sxs-lookup"><span data-stu-id="b158b-289">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="b158b-290">**MSMQ-Gruppe**</span><span class="sxs-lookup"><span data-stu-id="b158b-290">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b158b-291">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b158b-291">Windows Server 2012</span></span>



| <span data-ttu-id="b158b-292">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b158b-292">Entry</span></span> | <span data-ttu-id="b158b-293">Wert</span><span class="sxs-lookup"><span data-stu-id="b158b-293">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b158b-294">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b158b-294">Link-Id</span></span>                | <span data-ttu-id="b158b-295">2</span><span class="sxs-lookup"><span data-stu-id="b158b-295">2</span></span>                                                                                                                                     |
| <span data-ttu-id="b158b-296">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b158b-296">MAPI-Id</span></span>                | <span data-ttu-id="b158b-297">0x8009</span><span class="sxs-lookup"><span data-stu-id="b158b-297">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="b158b-298">System-Only</span><span class="sxs-lookup"><span data-stu-id="b158b-298">System-Only</span></span>            | <span data-ttu-id="b158b-299">False</span><span class="sxs-lookup"><span data-stu-id="b158b-299">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b158b-300">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b158b-300">Is-Single-Valued</span></span>       | <span data-ttu-id="b158b-301">False</span><span class="sxs-lookup"><span data-stu-id="b158b-301">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b158b-302">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b158b-302">Is Indexed</span></span>             | <span data-ttu-id="b158b-303">False</span><span class="sxs-lookup"><span data-stu-id="b158b-303">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b158b-304">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b158b-304">In Global Catalog</span></span>      | <span data-ttu-id="b158b-305">Richtig</span><span class="sxs-lookup"><span data-stu-id="b158b-305">True</span></span>                                                                                                                                  |
| <span data-ttu-id="b158b-306">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b158b-306">NT-Security-Descriptor</span></span> | <span data-ttu-id="b158b-307">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b158b-307">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="b158b-308">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b158b-308">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b158b-309">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b158b-309">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b158b-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b158b-310">Search-Flags</span></span>           | <span data-ttu-id="b158b-311">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b158b-311">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="b158b-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b158b-312">System-Flags</span></span>           | <span data-ttu-id="b158b-313">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b158b-313">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="b158b-314">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b158b-314">Classes used in</span></span>        | [<span data-ttu-id="b158b-315">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="b158b-315">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="b158b-316">**Gruppe von Namen**</span><span class="sxs-lookup"><span data-stu-id="b158b-316">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="b158b-317">**MSMQ-Gruppe**</span><span class="sxs-lookup"><span data-stu-id="b158b-317">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



 

 





