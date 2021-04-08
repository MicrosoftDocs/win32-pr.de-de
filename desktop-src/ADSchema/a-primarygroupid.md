---
title: Primary-Group-ID-Attribut
description: Enthält den relativen Bezeichner (RID) für die primäre Gruppe des Benutzers. Standardmäßig ist dies die RID für die Gruppe der Domänen Benutzer.
ms.assetid: 80803734-f7dd-4348-a110-ca6b8bccb60b
ms.tgt_platform: multiple
keywords:
- "\"Primary-Group-ID\"-Attribut AD-Schema"
- primaryGroupId-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Primary-Group-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2b6237ff6e49a01da3b960b58103ae10dca7b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744960"
---
# <a name="primary-group-id-attribute"></a><span data-ttu-id="77aa4-106">Primary-Group-ID-Attribut</span><span class="sxs-lookup"><span data-stu-id="77aa4-106">Primary-Group-ID attribute</span></span>

<span data-ttu-id="77aa4-107">Enthält den relativen Bezeichner (RID) für die primäre Gruppe des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="77aa4-107">Contains the relative identifier (RID) for the primary group of the user.</span></span> <span data-ttu-id="77aa4-108">Standardmäßig ist dies die RID für die Gruppe der Domänen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="77aa4-108">By default, this is the RID for the Domain Users group.</span></span>



| <span data-ttu-id="77aa4-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="77aa4-109">Entry</span></span> | <span data-ttu-id="77aa4-110">Wert</span><span class="sxs-lookup"><span data-stu-id="77aa4-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="77aa4-111">CN</span><span class="sxs-lookup"><span data-stu-id="77aa4-111">CN</span></span>                | <span data-ttu-id="77aa4-112">Primary-Group-ID</span><span class="sxs-lookup"><span data-stu-id="77aa4-112">Primary-Group-ID</span></span>                     |
| <span data-ttu-id="77aa4-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="77aa4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="77aa4-114">primaryGroupId</span><span class="sxs-lookup"><span data-stu-id="77aa4-114">primaryGroupID</span></span>                       |
| <span data-ttu-id="77aa4-115">Size</span><span class="sxs-lookup"><span data-stu-id="77aa4-115">Size</span></span>              | <span data-ttu-id="77aa4-116">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="77aa4-116">4 bytes</span></span>                              |
| <span data-ttu-id="77aa4-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="77aa4-117">Update Privilege</span></span>  | <span data-ttu-id="77aa4-118">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="77aa4-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="77aa4-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="77aa4-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="77aa4-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="77aa4-120">Attribute-Id</span></span>      | <span data-ttu-id="77aa4-121">1.2.840.113556.1.4.98</span><span class="sxs-lookup"><span data-stu-id="77aa4-121">1.2.840.113556.1.4.98</span></span>                |
| <span data-ttu-id="77aa4-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="77aa4-122">System-Id-Guid</span></span>    | <span data-ttu-id="77aa4-123">bf967a00-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="77aa4-123">bf967a00-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="77aa4-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="77aa4-124">Syntax</span></span>            | [<span data-ttu-id="77aa4-125">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="77aa4-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="77aa4-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="77aa4-126">Implementations</span></span>

-   [<span data-ttu-id="77aa4-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="77aa4-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="77aa4-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="77aa4-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="77aa4-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="77aa4-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="77aa4-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="77aa4-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="77aa4-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="77aa4-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="77aa4-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="77aa4-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="77aa4-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="77aa4-133">Windows 2000 Server</span></span>



| <span data-ttu-id="77aa4-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="77aa4-134">Entry</span></span> | <span data-ttu-id="77aa4-135">Wert</span><span class="sxs-lookup"><span data-stu-id="77aa4-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="77aa4-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="77aa4-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="77aa4-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77aa4-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="77aa4-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="77aa4-138">System-Only</span></span>            | <span data-ttu-id="77aa4-139">False</span><span class="sxs-lookup"><span data-stu-id="77aa4-139">False</span></span>                             |
| <span data-ttu-id="77aa4-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="77aa4-140">Is-Single-Valued</span></span>       | <span data-ttu-id="77aa4-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-141">True</span></span>                              |
| <span data-ttu-id="77aa4-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="77aa4-142">Is Indexed</span></span>             | <span data-ttu-id="77aa4-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-143">True</span></span>                              |
| <span data-ttu-id="77aa4-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="77aa4-144">In Global Catalog</span></span>      | <span data-ttu-id="77aa4-145">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-145">True</span></span>                              |
| <span data-ttu-id="77aa4-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77aa4-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="77aa4-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="77aa4-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="77aa4-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77aa4-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="77aa4-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77aa4-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="77aa4-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77aa4-150">Search-Flags</span></span>           | <span data-ttu-id="77aa4-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="77aa4-151">0x00000011</span></span>                        |
| <span data-ttu-id="77aa4-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77aa4-152">System-Flags</span></span>           | <span data-ttu-id="77aa4-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="77aa4-153">0x00000012</span></span>                        |
| <span data-ttu-id="77aa4-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="77aa4-154">Classes used in</span></span>        | [<span data-ttu-id="77aa4-155">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="77aa4-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="77aa4-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="77aa4-156">Windows Server 2003</span></span>



| <span data-ttu-id="77aa4-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="77aa4-157">Entry</span></span> | <span data-ttu-id="77aa4-158">Wert</span><span class="sxs-lookup"><span data-stu-id="77aa4-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="77aa4-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="77aa4-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="77aa4-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77aa4-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="77aa4-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="77aa4-161">System-Only</span></span>            | <span data-ttu-id="77aa4-162">False</span><span class="sxs-lookup"><span data-stu-id="77aa4-162">False</span></span>                             |
| <span data-ttu-id="77aa4-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="77aa4-163">Is-Single-Valued</span></span>       | <span data-ttu-id="77aa4-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-164">True</span></span>                              |
| <span data-ttu-id="77aa4-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="77aa4-165">Is Indexed</span></span>             | <span data-ttu-id="77aa4-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-166">True</span></span>                              |
| <span data-ttu-id="77aa4-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="77aa4-167">In Global Catalog</span></span>      | <span data-ttu-id="77aa4-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-168">True</span></span>                              |
| <span data-ttu-id="77aa4-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77aa4-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="77aa4-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="77aa4-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="77aa4-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77aa4-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="77aa4-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77aa4-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="77aa4-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77aa4-173">Search-Flags</span></span>           | <span data-ttu-id="77aa4-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="77aa4-174">0x00000011</span></span>                        |
| <span data-ttu-id="77aa4-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77aa4-175">System-Flags</span></span>           | <span data-ttu-id="77aa4-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="77aa4-176">0x00000012</span></span>                        |
| <span data-ttu-id="77aa4-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="77aa4-177">Classes used in</span></span>        | [<span data-ttu-id="77aa4-178">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="77aa4-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="77aa4-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="77aa4-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="77aa4-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="77aa4-180">Entry</span></span> | <span data-ttu-id="77aa4-181">Wert</span><span class="sxs-lookup"><span data-stu-id="77aa4-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="77aa4-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="77aa4-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="77aa4-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77aa4-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="77aa4-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="77aa4-184">System-Only</span></span>            | <span data-ttu-id="77aa4-185">False</span><span class="sxs-lookup"><span data-stu-id="77aa4-185">False</span></span>                             |
| <span data-ttu-id="77aa4-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="77aa4-186">Is-Single-Valued</span></span>       | <span data-ttu-id="77aa4-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-187">True</span></span>                              |
| <span data-ttu-id="77aa4-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="77aa4-188">Is Indexed</span></span>             | <span data-ttu-id="77aa4-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-189">True</span></span>                              |
| <span data-ttu-id="77aa4-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="77aa4-190">In Global Catalog</span></span>      | <span data-ttu-id="77aa4-191">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-191">True</span></span>                              |
| <span data-ttu-id="77aa4-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77aa4-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="77aa4-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="77aa4-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="77aa4-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77aa4-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="77aa4-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77aa4-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="77aa4-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77aa4-196">Search-Flags</span></span>           | <span data-ttu-id="77aa4-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="77aa4-197">0x00000011</span></span>                        |
| <span data-ttu-id="77aa4-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77aa4-198">System-Flags</span></span>           | <span data-ttu-id="77aa4-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="77aa4-199">0x00000012</span></span>                        |
| <span data-ttu-id="77aa4-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="77aa4-200">Classes used in</span></span>        | [<span data-ttu-id="77aa4-201">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="77aa4-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="77aa4-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77aa4-202">Windows Server 2008</span></span>



| <span data-ttu-id="77aa4-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="77aa4-203">Entry</span></span> | <span data-ttu-id="77aa4-204">Wert</span><span class="sxs-lookup"><span data-stu-id="77aa4-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="77aa4-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="77aa4-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="77aa4-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77aa4-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="77aa4-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="77aa4-207">System-Only</span></span>            | <span data-ttu-id="77aa4-208">False</span><span class="sxs-lookup"><span data-stu-id="77aa4-208">False</span></span>                             |
| <span data-ttu-id="77aa4-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="77aa4-209">Is-Single-Valued</span></span>       | <span data-ttu-id="77aa4-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-210">True</span></span>                              |
| <span data-ttu-id="77aa4-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="77aa4-211">Is Indexed</span></span>             | <span data-ttu-id="77aa4-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-212">True</span></span>                              |
| <span data-ttu-id="77aa4-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="77aa4-213">In Global Catalog</span></span>      | <span data-ttu-id="77aa4-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-214">True</span></span>                              |
| <span data-ttu-id="77aa4-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77aa4-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="77aa4-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="77aa4-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="77aa4-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77aa4-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="77aa4-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77aa4-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="77aa4-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77aa4-219">Search-Flags</span></span>           | <span data-ttu-id="77aa4-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="77aa4-220">0x00000011</span></span>                        |
| <span data-ttu-id="77aa4-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77aa4-221">System-Flags</span></span>           | <span data-ttu-id="77aa4-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="77aa4-222">0x00000012</span></span>                        |
| <span data-ttu-id="77aa4-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="77aa4-223">Classes used in</span></span>        | [<span data-ttu-id="77aa4-224">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="77aa4-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="77aa4-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="77aa4-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="77aa4-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="77aa4-226">Entry</span></span> | <span data-ttu-id="77aa4-227">Wert</span><span class="sxs-lookup"><span data-stu-id="77aa4-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="77aa4-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="77aa4-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="77aa4-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77aa4-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="77aa4-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="77aa4-230">System-Only</span></span>            | <span data-ttu-id="77aa4-231">False</span><span class="sxs-lookup"><span data-stu-id="77aa4-231">False</span></span>                             |
| <span data-ttu-id="77aa4-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="77aa4-232">Is-Single-Valued</span></span>       | <span data-ttu-id="77aa4-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-233">True</span></span>                              |
| <span data-ttu-id="77aa4-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="77aa4-234">Is Indexed</span></span>             | <span data-ttu-id="77aa4-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-235">True</span></span>                              |
| <span data-ttu-id="77aa4-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="77aa4-236">In Global Catalog</span></span>      | <span data-ttu-id="77aa4-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-237">True</span></span>                              |
| <span data-ttu-id="77aa4-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77aa4-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="77aa4-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="77aa4-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="77aa4-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77aa4-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="77aa4-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77aa4-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="77aa4-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77aa4-242">Search-Flags</span></span>           | <span data-ttu-id="77aa4-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="77aa4-243">0x00000011</span></span>                        |
| <span data-ttu-id="77aa4-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77aa4-244">System-Flags</span></span>           | <span data-ttu-id="77aa4-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="77aa4-245">0x00000012</span></span>                        |
| <span data-ttu-id="77aa4-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="77aa4-246">Classes used in</span></span>        | [<span data-ttu-id="77aa4-247">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="77aa4-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="77aa4-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="77aa4-248">Windows Server 2012</span></span>



| <span data-ttu-id="77aa4-249">Eingabe</span><span class="sxs-lookup"><span data-stu-id="77aa4-249">Entry</span></span> | <span data-ttu-id="77aa4-250">Wert</span><span class="sxs-lookup"><span data-stu-id="77aa4-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="77aa4-251">Link-ID</span><span class="sxs-lookup"><span data-stu-id="77aa4-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="77aa4-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77aa4-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="77aa4-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="77aa4-253">System-Only</span></span>            | <span data-ttu-id="77aa4-254">False</span><span class="sxs-lookup"><span data-stu-id="77aa4-254">False</span></span>                             |
| <span data-ttu-id="77aa4-255">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="77aa4-255">Is-Single-Valued</span></span>       | <span data-ttu-id="77aa4-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-256">True</span></span>                              |
| <span data-ttu-id="77aa4-257">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="77aa4-257">Is Indexed</span></span>             | <span data-ttu-id="77aa4-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-258">True</span></span>                              |
| <span data-ttu-id="77aa4-259">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="77aa4-259">In Global Catalog</span></span>      | <span data-ttu-id="77aa4-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="77aa4-260">True</span></span>                              |
| <span data-ttu-id="77aa4-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77aa4-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="77aa4-262">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="77aa4-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="77aa4-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77aa4-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="77aa4-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77aa4-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="77aa4-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77aa4-265">Search-Flags</span></span>           | <span data-ttu-id="77aa4-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="77aa4-266">0x00000011</span></span>                        |
| <span data-ttu-id="77aa4-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77aa4-267">System-Flags</span></span>           | <span data-ttu-id="77aa4-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="77aa4-268">0x00000012</span></span>                        |
| <span data-ttu-id="77aa4-269">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="77aa4-269">Classes used in</span></span>        | [<span data-ttu-id="77aa4-270">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="77aa4-270">**User**</span></span>](c-user.md)<br/> |



 

 





