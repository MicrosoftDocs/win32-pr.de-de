---
title: LM-pwd-History-Attribut
description: Der Kenn Wort Verlauf des Benutzers im LAN-Manager (LM) (unidirektionales Format). Der LM-owf wird für die Kompatibilität mit LAN-Manager 2. x-Clients, Windows 95 und Windows 98 verwendet.
ms.assetid: c4cb2e74-b37d-4c76-8d21-d71bc9c19a4a
ms.tgt_platform: multiple
keywords:
- AD-Schema des LM-pwd-History-Attributs
- lmpwdhistory-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Lm-Pwd-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28f5c73b35bb0ea2cae9d01324d82e1568485541
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859723"
---
# <a name="lm-pwd-history-attribute"></a><span data-ttu-id="0c123-106">LM-pwd-History-Attribut</span><span class="sxs-lookup"><span data-stu-id="0c123-106">Lm-Pwd-History attribute</span></span>

<span data-ttu-id="0c123-107">Der Kenn Wort Verlauf des Benutzers im LAN-Manager (LM) (unidirektionales Format).</span><span class="sxs-lookup"><span data-stu-id="0c123-107">The password history of the user in LAN Manager (LM) one-way format (OWF).</span></span> <span data-ttu-id="0c123-108">Der LM-owf-Wert wird für die Kompatibilität mit LAN-Manager 2 verwendet. *x* -Clients, Windows 95 und Windows 98.</span><span class="sxs-lookup"><span data-stu-id="0c123-108">The LM OWF is used for compatibility with LAN Manager 2.*x* clients, Windows 95, and Windows 98.</span></span>



| <span data-ttu-id="0c123-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c123-109">Entry</span></span> | <span data-ttu-id="0c123-110">Wert</span><span class="sxs-lookup"><span data-stu-id="0c123-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="0c123-111">CN</span><span class="sxs-lookup"><span data-stu-id="0c123-111">CN</span></span>                | <span data-ttu-id="0c123-112">LM-pwd-Verlauf</span><span class="sxs-lookup"><span data-stu-id="0c123-112">Lm-Pwd-History</span></span>                                        |
| <span data-ttu-id="0c123-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0c123-113">Ldap-Display-Name</span></span> | <span data-ttu-id="0c123-114">lmpwdhistory</span><span class="sxs-lookup"><span data-stu-id="0c123-114">lmPwdHistory</span></span>                                          |
| <span data-ttu-id="0c123-115">Size</span><span class="sxs-lookup"><span data-stu-id="0c123-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="0c123-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0c123-116">Update Privilege</span></span>  | <span data-ttu-id="0c123-117">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="0c123-117">Domain administrator</span></span>                                  |
| <span data-ttu-id="0c123-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="0c123-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="0c123-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0c123-119">Attribute-Id</span></span>      | <span data-ttu-id="0c123-120">1.2.840.113556.1.4.160</span><span class="sxs-lookup"><span data-stu-id="0c123-120">1.2.840.113556.1.4.160</span></span>                                |
| <span data-ttu-id="0c123-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0c123-121">System-Id-Guid</span></span>    | <span data-ttu-id="0c123-122">bf96799d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0c123-122">bf96799d-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="0c123-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c123-123">Syntax</span></span>            | [<span data-ttu-id="0c123-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="0c123-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="0c123-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="0c123-125">Implementations</span></span>

-   [<span data-ttu-id="0c123-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0c123-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0c123-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0c123-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0c123-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0c123-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0c123-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0c123-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0c123-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0c123-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0c123-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0c123-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0c123-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c123-132">Windows 2000 Server</span></span>



| <span data-ttu-id="0c123-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c123-133">Entry</span></span> | <span data-ttu-id="0c123-134">Wert</span><span class="sxs-lookup"><span data-stu-id="0c123-134">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0c123-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0c123-135">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0c123-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c123-136">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0c123-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c123-137">System-Only</span></span>            | <span data-ttu-id="0c123-138">False</span><span class="sxs-lookup"><span data-stu-id="0c123-138">False</span></span>                             |
| <span data-ttu-id="0c123-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0c123-139">Is-Single-Valued</span></span>       | <span data-ttu-id="0c123-140">False</span><span class="sxs-lookup"><span data-stu-id="0c123-140">False</span></span>                             |
| <span data-ttu-id="0c123-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0c123-141">Is Indexed</span></span>             | <span data-ttu-id="0c123-142">False</span><span class="sxs-lookup"><span data-stu-id="0c123-142">False</span></span>                             |
| <span data-ttu-id="0c123-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0c123-143">In Global Catalog</span></span>      | <span data-ttu-id="0c123-144">False</span><span class="sxs-lookup"><span data-stu-id="0c123-144">False</span></span>                             |
| <span data-ttu-id="0c123-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c123-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c123-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0c123-146">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0c123-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c123-147">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0c123-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c123-148">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0c123-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c123-149">Search-Flags</span></span>           | <span data-ttu-id="0c123-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c123-150">0x00000000</span></span>                        |
| <span data-ttu-id="0c123-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c123-151">System-Flags</span></span>           | <span data-ttu-id="0c123-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c123-152">0x00000010</span></span>                        |
| <span data-ttu-id="0c123-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0c123-153">Classes used in</span></span>        | [<span data-ttu-id="0c123-154">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="0c123-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0c123-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c123-155">Windows Server 2003</span></span>



| <span data-ttu-id="0c123-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c123-156">Entry</span></span> | <span data-ttu-id="0c123-157">Wert</span><span class="sxs-lookup"><span data-stu-id="0c123-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0c123-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0c123-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0c123-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c123-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0c123-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c123-160">System-Only</span></span>            | <span data-ttu-id="0c123-161">False</span><span class="sxs-lookup"><span data-stu-id="0c123-161">False</span></span>                             |
| <span data-ttu-id="0c123-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0c123-162">Is-Single-Valued</span></span>       | <span data-ttu-id="0c123-163">False</span><span class="sxs-lookup"><span data-stu-id="0c123-163">False</span></span>                             |
| <span data-ttu-id="0c123-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0c123-164">Is Indexed</span></span>             | <span data-ttu-id="0c123-165">False</span><span class="sxs-lookup"><span data-stu-id="0c123-165">False</span></span>                             |
| <span data-ttu-id="0c123-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0c123-166">In Global Catalog</span></span>      | <span data-ttu-id="0c123-167">False</span><span class="sxs-lookup"><span data-stu-id="0c123-167">False</span></span>                             |
| <span data-ttu-id="0c123-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c123-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c123-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0c123-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0c123-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c123-170">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0c123-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c123-171">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0c123-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c123-172">Search-Flags</span></span>           | <span data-ttu-id="0c123-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c123-173">0x00000000</span></span>                        |
| <span data-ttu-id="0c123-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c123-174">System-Flags</span></span>           | <span data-ttu-id="0c123-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c123-175">0x00000010</span></span>                        |
| <span data-ttu-id="0c123-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0c123-176">Classes used in</span></span>        | [<span data-ttu-id="0c123-177">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="0c123-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0c123-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0c123-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0c123-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c123-179">Entry</span></span> | <span data-ttu-id="0c123-180">Wert</span><span class="sxs-lookup"><span data-stu-id="0c123-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0c123-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0c123-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0c123-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c123-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0c123-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c123-183">System-Only</span></span>            | <span data-ttu-id="0c123-184">False</span><span class="sxs-lookup"><span data-stu-id="0c123-184">False</span></span>                             |
| <span data-ttu-id="0c123-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0c123-185">Is-Single-Valued</span></span>       | <span data-ttu-id="0c123-186">False</span><span class="sxs-lookup"><span data-stu-id="0c123-186">False</span></span>                             |
| <span data-ttu-id="0c123-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0c123-187">Is Indexed</span></span>             | <span data-ttu-id="0c123-188">False</span><span class="sxs-lookup"><span data-stu-id="0c123-188">False</span></span>                             |
| <span data-ttu-id="0c123-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0c123-189">In Global Catalog</span></span>      | <span data-ttu-id="0c123-190">False</span><span class="sxs-lookup"><span data-stu-id="0c123-190">False</span></span>                             |
| <span data-ttu-id="0c123-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c123-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c123-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0c123-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0c123-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c123-193">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0c123-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c123-194">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0c123-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c123-195">Search-Flags</span></span>           | <span data-ttu-id="0c123-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c123-196">0x00000000</span></span>                        |
| <span data-ttu-id="0c123-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c123-197">System-Flags</span></span>           | <span data-ttu-id="0c123-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c123-198">0x00000010</span></span>                        |
| <span data-ttu-id="0c123-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0c123-199">Classes used in</span></span>        | [<span data-ttu-id="0c123-200">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="0c123-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0c123-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c123-201">Windows Server 2008</span></span>



| <span data-ttu-id="0c123-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c123-202">Entry</span></span> | <span data-ttu-id="0c123-203">Wert</span><span class="sxs-lookup"><span data-stu-id="0c123-203">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0c123-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0c123-204">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0c123-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c123-205">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0c123-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c123-206">System-Only</span></span>            | <span data-ttu-id="0c123-207">False</span><span class="sxs-lookup"><span data-stu-id="0c123-207">False</span></span>                             |
| <span data-ttu-id="0c123-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0c123-208">Is-Single-Valued</span></span>       | <span data-ttu-id="0c123-209">False</span><span class="sxs-lookup"><span data-stu-id="0c123-209">False</span></span>                             |
| <span data-ttu-id="0c123-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0c123-210">Is Indexed</span></span>             | <span data-ttu-id="0c123-211">False</span><span class="sxs-lookup"><span data-stu-id="0c123-211">False</span></span>                             |
| <span data-ttu-id="0c123-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0c123-212">In Global Catalog</span></span>      | <span data-ttu-id="0c123-213">False</span><span class="sxs-lookup"><span data-stu-id="0c123-213">False</span></span>                             |
| <span data-ttu-id="0c123-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c123-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c123-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0c123-215">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0c123-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c123-216">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0c123-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c123-217">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0c123-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c123-218">Search-Flags</span></span>           | <span data-ttu-id="0c123-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c123-219">0x00000000</span></span>                        |
| <span data-ttu-id="0c123-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c123-220">System-Flags</span></span>           | <span data-ttu-id="0c123-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c123-221">0x00000010</span></span>                        |
| <span data-ttu-id="0c123-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0c123-222">Classes used in</span></span>        | [<span data-ttu-id="0c123-223">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="0c123-223">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0c123-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0c123-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0c123-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c123-225">Entry</span></span> | <span data-ttu-id="0c123-226">Wert</span><span class="sxs-lookup"><span data-stu-id="0c123-226">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0c123-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0c123-227">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0c123-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c123-228">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0c123-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c123-229">System-Only</span></span>            | <span data-ttu-id="0c123-230">False</span><span class="sxs-lookup"><span data-stu-id="0c123-230">False</span></span>                             |
| <span data-ttu-id="0c123-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0c123-231">Is-Single-Valued</span></span>       | <span data-ttu-id="0c123-232">False</span><span class="sxs-lookup"><span data-stu-id="0c123-232">False</span></span>                             |
| <span data-ttu-id="0c123-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0c123-233">Is Indexed</span></span>             | <span data-ttu-id="0c123-234">False</span><span class="sxs-lookup"><span data-stu-id="0c123-234">False</span></span>                             |
| <span data-ttu-id="0c123-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0c123-235">In Global Catalog</span></span>      | <span data-ttu-id="0c123-236">False</span><span class="sxs-lookup"><span data-stu-id="0c123-236">False</span></span>                             |
| <span data-ttu-id="0c123-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c123-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c123-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0c123-238">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0c123-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c123-239">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0c123-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c123-240">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0c123-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c123-241">Search-Flags</span></span>           | <span data-ttu-id="0c123-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c123-242">0x00000000</span></span>                        |
| <span data-ttu-id="0c123-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c123-243">System-Flags</span></span>           | <span data-ttu-id="0c123-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c123-244">0x00000010</span></span>                        |
| <span data-ttu-id="0c123-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0c123-245">Classes used in</span></span>        | [<span data-ttu-id="0c123-246">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="0c123-246">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0c123-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0c123-247">Windows Server 2012</span></span>



| <span data-ttu-id="0c123-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c123-248">Entry</span></span> | <span data-ttu-id="0c123-249">Wert</span><span class="sxs-lookup"><span data-stu-id="0c123-249">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0c123-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0c123-250">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0c123-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c123-251">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0c123-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c123-252">System-Only</span></span>            | <span data-ttu-id="0c123-253">False</span><span class="sxs-lookup"><span data-stu-id="0c123-253">False</span></span>                             |
| <span data-ttu-id="0c123-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0c123-254">Is-Single-Valued</span></span>       | <span data-ttu-id="0c123-255">False</span><span class="sxs-lookup"><span data-stu-id="0c123-255">False</span></span>                             |
| <span data-ttu-id="0c123-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0c123-256">Is Indexed</span></span>             | <span data-ttu-id="0c123-257">False</span><span class="sxs-lookup"><span data-stu-id="0c123-257">False</span></span>                             |
| <span data-ttu-id="0c123-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0c123-258">In Global Catalog</span></span>      | <span data-ttu-id="0c123-259">False</span><span class="sxs-lookup"><span data-stu-id="0c123-259">False</span></span>                             |
| <span data-ttu-id="0c123-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c123-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c123-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0c123-261">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0c123-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c123-262">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0c123-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c123-263">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0c123-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c123-264">Search-Flags</span></span>           | <span data-ttu-id="0c123-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c123-265">0x00000000</span></span>                        |
| <span data-ttu-id="0c123-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c123-266">System-Flags</span></span>           | <span data-ttu-id="0c123-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c123-267">0x00000010</span></span>                        |
| <span data-ttu-id="0c123-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0c123-268">Classes used in</span></span>        | [<span data-ttu-id="0c123-269">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="0c123-269">**User**</span></span>](c-user.md)<br/> |



 

 





