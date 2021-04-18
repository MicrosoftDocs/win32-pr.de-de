---
title: Server-Role-Attribut
description: Aus Gründen der Kompatibilität mit Pre-2000 Windows Server Server Server-Servern. Ein Computer, auf dem Windows NT Server ausgeführt wird, kann ein eigenständiger Server, ein primärer Domänen Controller (PDC) oder ein Sicherungs Domänen Controller (BDC) sein.
ms.assetid: 0c2e5b18-14ad-4f77-a62c-eeb95aabbb99
ms.tgt_platform: multiple
keywords:
- AD-Schema für Server-Role-Attribut
- "\"serverRole\"-Attribut AD-Schema"
topic_type:
- apiref
api_name:
- Server-Role
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58a127a94cd1ecc2bfce3701c11ee2a5e0c2376c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106338832"
---
# <a name="server-role-attribute"></a><span data-ttu-id="d9a8b-106">Server-Role-Attribut</span><span class="sxs-lookup"><span data-stu-id="d9a8b-106">Server-Role attribute</span></span>

<span data-ttu-id="d9a8b-107">Aus Gründen der Kompatibilität mit Pre-2000 Windows Server Server Server-Servern.</span><span class="sxs-lookup"><span data-stu-id="d9a8b-107">For compatibility with pre-Windows 2000 Server servers.</span></span> <span data-ttu-id="d9a8b-108">Ein Computer, auf dem Windows NT Server ausgeführt wird, kann ein eigenständiger Server, ein primärer Domänen Controller (PDC) oder ein Sicherungs Domänen Controller (BDC) sein.</span><span class="sxs-lookup"><span data-stu-id="d9a8b-108">A computer running Windows NT Server can be a standalone server, a primary domain controller (PDC), or a backup domain controller (BDC).</span></span>



| <span data-ttu-id="d9a8b-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9a8b-109">Entry</span></span> | <span data-ttu-id="d9a8b-110">Wert</span><span class="sxs-lookup"><span data-stu-id="d9a8b-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d9a8b-111">CN</span><span class="sxs-lookup"><span data-stu-id="d9a8b-111">CN</span></span>                | <span data-ttu-id="d9a8b-112">Server-Role</span><span class="sxs-lookup"><span data-stu-id="d9a8b-112">Server-Role</span></span>                          |
| <span data-ttu-id="d9a8b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d9a8b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d9a8b-114">serverRole</span><span class="sxs-lookup"><span data-stu-id="d9a8b-114">serverRole</span></span>                           |
| <span data-ttu-id="d9a8b-115">Size</span><span class="sxs-lookup"><span data-stu-id="d9a8b-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="d9a8b-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d9a8b-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="d9a8b-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="d9a8b-117">Update Frequency</span></span>  | <span data-ttu-id="d9a8b-118">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="d9a8b-118">4 bytes</span></span>                              |
| <span data-ttu-id="d9a8b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d9a8b-119">Attribute-Id</span></span>      | <span data-ttu-id="d9a8b-120">1.2.840.113556.1.4.157</span><span class="sxs-lookup"><span data-stu-id="d9a8b-120">1.2.840.113556.1.4.157</span></span>               |
| <span data-ttu-id="d9a8b-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d9a8b-121">System-Id-Guid</span></span>    | <span data-ttu-id="d9a8b-122">bf967a33-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="d9a8b-122">bf967a33-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="d9a8b-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9a8b-123">Syntax</span></span>            | [<span data-ttu-id="d9a8b-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="d9a8b-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="d9a8b-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="d9a8b-125">Implementations</span></span>

-   [<span data-ttu-id="d9a8b-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d9a8b-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d9a8b-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d9a8b-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d9a8b-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d9a8b-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d9a8b-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d9a8b-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d9a8b-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d9a8b-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d9a8b-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d9a8b-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d9a8b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d9a8b-132">Windows 2000 Server</span></span>



| <span data-ttu-id="d9a8b-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9a8b-133">Entry</span></span> | <span data-ttu-id="d9a8b-134">Wert</span><span class="sxs-lookup"><span data-stu-id="d9a8b-134">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="d9a8b-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d9a8b-135">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="d9a8b-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9a8b-136">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="d9a8b-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9a8b-137">System-Only</span></span>            | <span data-ttu-id="d9a8b-138">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-138">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d9a8b-139">Is-Single-Valued</span></span>       | <span data-ttu-id="d9a8b-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="d9a8b-140">True</span></span>                                                  |
| <span data-ttu-id="d9a8b-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d9a8b-141">Is Indexed</span></span>             | <span data-ttu-id="d9a8b-142">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-142">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d9a8b-143">In Global Catalog</span></span>      | <span data-ttu-id="d9a8b-144">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-144">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d9a8b-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9a8b-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d9a8b-146">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="d9a8b-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9a8b-147">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="d9a8b-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9a8b-148">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="d9a8b-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a8b-149">Search-Flags</span></span>           | <span data-ttu-id="d9a8b-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9a8b-150">0x00000000</span></span>                                            |
| <span data-ttu-id="d9a8b-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a8b-151">System-Flags</span></span>           | <span data-ttu-id="d9a8b-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9a8b-152">0x00000010</span></span>                                            |
| <span data-ttu-id="d9a8b-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d9a8b-153">Classes used in</span></span>        | [<span data-ttu-id="d9a8b-154">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="d9a8b-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d9a8b-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d9a8b-155">Windows Server 2003</span></span>



| <span data-ttu-id="d9a8b-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9a8b-156">Entry</span></span> | <span data-ttu-id="d9a8b-157">Wert</span><span class="sxs-lookup"><span data-stu-id="d9a8b-157">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="d9a8b-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d9a8b-158">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="d9a8b-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9a8b-159">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="d9a8b-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9a8b-160">System-Only</span></span>            | <span data-ttu-id="d9a8b-161">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-161">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d9a8b-162">Is-Single-Valued</span></span>       | <span data-ttu-id="d9a8b-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="d9a8b-163">True</span></span>                                                  |
| <span data-ttu-id="d9a8b-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d9a8b-164">Is Indexed</span></span>             | <span data-ttu-id="d9a8b-165">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-165">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d9a8b-166">In Global Catalog</span></span>      | <span data-ttu-id="d9a8b-167">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-167">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d9a8b-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9a8b-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d9a8b-169">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="d9a8b-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9a8b-170">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="d9a8b-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9a8b-171">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="d9a8b-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a8b-172">Search-Flags</span></span>           | <span data-ttu-id="d9a8b-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9a8b-173">0x00000000</span></span>                                            |
| <span data-ttu-id="d9a8b-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a8b-174">System-Flags</span></span>           | <span data-ttu-id="d9a8b-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9a8b-175">0x00000010</span></span>                                            |
| <span data-ttu-id="d9a8b-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d9a8b-176">Classes used in</span></span>        | [<span data-ttu-id="d9a8b-177">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="d9a8b-177">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d9a8b-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d9a8b-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d9a8b-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9a8b-179">Entry</span></span> | <span data-ttu-id="d9a8b-180">Wert</span><span class="sxs-lookup"><span data-stu-id="d9a8b-180">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="d9a8b-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d9a8b-181">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="d9a8b-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9a8b-182">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="d9a8b-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9a8b-183">System-Only</span></span>            | <span data-ttu-id="d9a8b-184">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-184">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d9a8b-185">Is-Single-Valued</span></span>       | <span data-ttu-id="d9a8b-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="d9a8b-186">True</span></span>                                                  |
| <span data-ttu-id="d9a8b-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d9a8b-187">Is Indexed</span></span>             | <span data-ttu-id="d9a8b-188">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-188">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d9a8b-189">In Global Catalog</span></span>      | <span data-ttu-id="d9a8b-190">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-190">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d9a8b-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9a8b-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d9a8b-192">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="d9a8b-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9a8b-193">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="d9a8b-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9a8b-194">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="d9a8b-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a8b-195">Search-Flags</span></span>           | <span data-ttu-id="d9a8b-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9a8b-196">0x00000000</span></span>                                            |
| <span data-ttu-id="d9a8b-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a8b-197">System-Flags</span></span>           | <span data-ttu-id="d9a8b-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9a8b-198">0x00000010</span></span>                                            |
| <span data-ttu-id="d9a8b-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d9a8b-199">Classes used in</span></span>        | [<span data-ttu-id="d9a8b-200">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="d9a8b-200">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d9a8b-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9a8b-201">Windows Server 2008</span></span>



| <span data-ttu-id="d9a8b-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9a8b-202">Entry</span></span> | <span data-ttu-id="d9a8b-203">Wert</span><span class="sxs-lookup"><span data-stu-id="d9a8b-203">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="d9a8b-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d9a8b-204">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="d9a8b-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9a8b-205">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="d9a8b-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9a8b-206">System-Only</span></span>            | <span data-ttu-id="d9a8b-207">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-207">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d9a8b-208">Is-Single-Valued</span></span>       | <span data-ttu-id="d9a8b-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="d9a8b-209">True</span></span>                                                  |
| <span data-ttu-id="d9a8b-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d9a8b-210">Is Indexed</span></span>             | <span data-ttu-id="d9a8b-211">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-211">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d9a8b-212">In Global Catalog</span></span>      | <span data-ttu-id="d9a8b-213">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-213">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d9a8b-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9a8b-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d9a8b-215">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="d9a8b-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9a8b-216">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="d9a8b-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9a8b-217">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="d9a8b-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a8b-218">Search-Flags</span></span>           | <span data-ttu-id="d9a8b-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9a8b-219">0x00000000</span></span>                                            |
| <span data-ttu-id="d9a8b-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a8b-220">System-Flags</span></span>           | <span data-ttu-id="d9a8b-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9a8b-221">0x00000010</span></span>                                            |
| <span data-ttu-id="d9a8b-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d9a8b-222">Classes used in</span></span>        | [<span data-ttu-id="d9a8b-223">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="d9a8b-223">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d9a8b-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d9a8b-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d9a8b-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9a8b-225">Entry</span></span> | <span data-ttu-id="d9a8b-226">Wert</span><span class="sxs-lookup"><span data-stu-id="d9a8b-226">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="d9a8b-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d9a8b-227">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="d9a8b-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9a8b-228">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="d9a8b-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9a8b-229">System-Only</span></span>            | <span data-ttu-id="d9a8b-230">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-230">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d9a8b-231">Is-Single-Valued</span></span>       | <span data-ttu-id="d9a8b-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="d9a8b-232">True</span></span>                                                  |
| <span data-ttu-id="d9a8b-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d9a8b-233">Is Indexed</span></span>             | <span data-ttu-id="d9a8b-234">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-234">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d9a8b-235">In Global Catalog</span></span>      | <span data-ttu-id="d9a8b-236">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-236">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d9a8b-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9a8b-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d9a8b-238">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="d9a8b-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9a8b-239">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="d9a8b-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9a8b-240">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="d9a8b-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a8b-241">Search-Flags</span></span>           | <span data-ttu-id="d9a8b-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9a8b-242">0x00000000</span></span>                                            |
| <span data-ttu-id="d9a8b-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a8b-243">System-Flags</span></span>           | <span data-ttu-id="d9a8b-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9a8b-244">0x00000010</span></span>                                            |
| <span data-ttu-id="d9a8b-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d9a8b-245">Classes used in</span></span>        | [<span data-ttu-id="d9a8b-246">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="d9a8b-246">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d9a8b-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d9a8b-247">Windows Server 2012</span></span>



| <span data-ttu-id="d9a8b-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9a8b-248">Entry</span></span> | <span data-ttu-id="d9a8b-249">Wert</span><span class="sxs-lookup"><span data-stu-id="d9a8b-249">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="d9a8b-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d9a8b-250">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="d9a8b-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9a8b-251">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="d9a8b-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9a8b-252">System-Only</span></span>            | <span data-ttu-id="d9a8b-253">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-253">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d9a8b-254">Is-Single-Valued</span></span>       | <span data-ttu-id="d9a8b-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="d9a8b-255">True</span></span>                                                  |
| <span data-ttu-id="d9a8b-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d9a8b-256">Is Indexed</span></span>             | <span data-ttu-id="d9a8b-257">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-257">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d9a8b-258">In Global Catalog</span></span>      | <span data-ttu-id="d9a8b-259">False</span><span class="sxs-lookup"><span data-stu-id="d9a8b-259">False</span></span>                                                 |
| <span data-ttu-id="d9a8b-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d9a8b-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9a8b-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d9a8b-261">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="d9a8b-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9a8b-262">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="d9a8b-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9a8b-263">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="d9a8b-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a8b-264">Search-Flags</span></span>           | <span data-ttu-id="d9a8b-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9a8b-265">0x00000000</span></span>                                            |
| <span data-ttu-id="d9a8b-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a8b-266">System-Flags</span></span>           | <span data-ttu-id="d9a8b-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9a8b-267">0x00000010</span></span>                                            |
| <span data-ttu-id="d9a8b-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d9a8b-268">Classes used in</span></span>        | [<span data-ttu-id="d9a8b-269">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="d9a8b-269">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





