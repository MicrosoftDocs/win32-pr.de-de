---
title: Trust-POSIX-Offset-Attribut
description: Der Offset der portablen Betriebs System Schnittstelle (POSIX) für die vertrauenswürdige Domäne.
ms.assetid: a1263f9f-1577-44b8-b7cc-317a8ecb37f1
ms.tgt_platform: multiple
keywords:
- Trust-POSIX-Offset-Attribut AD-Schema
- Trust posixoffset-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Trust-Posix-Offset
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8f3dca090d44ea545dcc290b04d99131d50dc7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104041080"
---
# <a name="trust-posix-offset-attribute"></a><span data-ttu-id="5bea1-105">Trust-POSIX-Offset-Attribut</span><span class="sxs-lookup"><span data-stu-id="5bea1-105">Trust-Posix-Offset attribute</span></span>

<span data-ttu-id="5bea1-106">Der Offset der portablen Betriebs System Schnittstelle (POSIX) für die vertrauenswürdige Domäne.</span><span class="sxs-lookup"><span data-stu-id="5bea1-106">The Portable Operating System Interface (POSIX) offset for the trusted domain.</span></span>



| <span data-ttu-id="5bea1-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5bea1-107">Entry</span></span> | <span data-ttu-id="5bea1-108">Wert</span><span class="sxs-lookup"><span data-stu-id="5bea1-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5bea1-109">CN</span><span class="sxs-lookup"><span data-stu-id="5bea1-109">CN</span></span>                | <span data-ttu-id="5bea1-110">Trust-POSIX-Offset</span><span class="sxs-lookup"><span data-stu-id="5bea1-110">Trust-Posix-Offset</span></span>                   |
| <span data-ttu-id="5bea1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5bea1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5bea1-112">trustposixoffset</span><span class="sxs-lookup"><span data-stu-id="5bea1-112">trustPosixOffset</span></span>                     |
| <span data-ttu-id="5bea1-113">Size</span><span class="sxs-lookup"><span data-stu-id="5bea1-113">Size</span></span>              | <span data-ttu-id="5bea1-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="5bea1-114">4 bytes</span></span>                              |
| <span data-ttu-id="5bea1-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5bea1-115">Update Privilege</span></span>  | <span data-ttu-id="5bea1-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5bea1-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="5bea1-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="5bea1-117">Update Frequency</span></span>  | <span data-ttu-id="5bea1-118">Wenn eine neue Vertrauensstellung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5bea1-118">When a new trust is created.</span></span>         |
| <span data-ttu-id="5bea1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5bea1-119">Attribute-Id</span></span>      | <span data-ttu-id="5bea1-120">1.2.840.113556.1.4.134</span><span class="sxs-lookup"><span data-stu-id="5bea1-120">1.2.840.113556.1.4.134</span></span>               |
| <span data-ttu-id="5bea1-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5bea1-121">System-Id-Guid</span></span>    | <span data-ttu-id="5bea1-122">bf967a5e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="5bea1-122">bf967a5e-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="5bea1-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bea1-123">Syntax</span></span>            | [<span data-ttu-id="5bea1-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="5bea1-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="5bea1-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="5bea1-125">Implementations</span></span>

-   [<span data-ttu-id="5bea1-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5bea1-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5bea1-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5bea1-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5bea1-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5bea1-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5bea1-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5bea1-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5bea1-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5bea1-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5bea1-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5bea1-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5bea1-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5bea1-132">Windows 2000 Server</span></span>



| <span data-ttu-id="5bea1-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5bea1-133">Entry</span></span> | <span data-ttu-id="5bea1-134">Wert</span><span class="sxs-lookup"><span data-stu-id="5bea1-134">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5bea1-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5bea1-135">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5bea1-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bea1-136">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5bea1-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bea1-137">System-Only</span></span>            | <span data-ttu-id="5bea1-138">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-138">False</span></span>                                                |
| <span data-ttu-id="5bea1-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5bea1-139">Is-Single-Valued</span></span>       | <span data-ttu-id="5bea1-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="5bea1-140">True</span></span>                                                 |
| <span data-ttu-id="5bea1-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5bea1-141">Is Indexed</span></span>             | <span data-ttu-id="5bea1-142">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-142">False</span></span>                                                |
| <span data-ttu-id="5bea1-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5bea1-143">In Global Catalog</span></span>      | <span data-ttu-id="5bea1-144">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-144">False</span></span>                                                |
| <span data-ttu-id="5bea1-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bea1-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bea1-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5bea1-146">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5bea1-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bea1-147">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5bea1-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bea1-148">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5bea1-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bea1-149">Search-Flags</span></span>           | <span data-ttu-id="5bea1-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bea1-150">0x00000000</span></span>                                           |
| <span data-ttu-id="5bea1-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bea1-151">System-Flags</span></span>           | <span data-ttu-id="5bea1-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bea1-152">0x00000010</span></span>                                           |
| <span data-ttu-id="5bea1-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5bea1-153">Classes used in</span></span>        | [<span data-ttu-id="5bea1-154">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="5bea1-154">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5bea1-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5bea1-155">Windows Server 2003</span></span>



| <span data-ttu-id="5bea1-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5bea1-156">Entry</span></span> | <span data-ttu-id="5bea1-157">Wert</span><span class="sxs-lookup"><span data-stu-id="5bea1-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5bea1-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5bea1-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5bea1-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bea1-159">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5bea1-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bea1-160">System-Only</span></span>            | <span data-ttu-id="5bea1-161">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-161">False</span></span>                                                |
| <span data-ttu-id="5bea1-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5bea1-162">Is-Single-Valued</span></span>       | <span data-ttu-id="5bea1-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="5bea1-163">True</span></span>                                                 |
| <span data-ttu-id="5bea1-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5bea1-164">Is Indexed</span></span>             | <span data-ttu-id="5bea1-165">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-165">False</span></span>                                                |
| <span data-ttu-id="5bea1-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5bea1-166">In Global Catalog</span></span>      | <span data-ttu-id="5bea1-167">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-167">False</span></span>                                                |
| <span data-ttu-id="5bea1-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bea1-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bea1-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5bea1-169">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5bea1-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bea1-170">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5bea1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bea1-171">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5bea1-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bea1-172">Search-Flags</span></span>           | <span data-ttu-id="5bea1-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bea1-173">0x00000000</span></span>                                           |
| <span data-ttu-id="5bea1-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bea1-174">System-Flags</span></span>           | <span data-ttu-id="5bea1-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bea1-175">0x00000010</span></span>                                           |
| <span data-ttu-id="5bea1-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5bea1-176">Classes used in</span></span>        | [<span data-ttu-id="5bea1-177">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="5bea1-177">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5bea1-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5bea1-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5bea1-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5bea1-179">Entry</span></span> | <span data-ttu-id="5bea1-180">Wert</span><span class="sxs-lookup"><span data-stu-id="5bea1-180">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5bea1-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5bea1-181">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5bea1-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bea1-182">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5bea1-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bea1-183">System-Only</span></span>            | <span data-ttu-id="5bea1-184">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-184">False</span></span>                                                |
| <span data-ttu-id="5bea1-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5bea1-185">Is-Single-Valued</span></span>       | <span data-ttu-id="5bea1-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="5bea1-186">True</span></span>                                                 |
| <span data-ttu-id="5bea1-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5bea1-187">Is Indexed</span></span>             | <span data-ttu-id="5bea1-188">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-188">False</span></span>                                                |
| <span data-ttu-id="5bea1-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5bea1-189">In Global Catalog</span></span>      | <span data-ttu-id="5bea1-190">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-190">False</span></span>                                                |
| <span data-ttu-id="5bea1-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bea1-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bea1-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5bea1-192">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5bea1-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bea1-193">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5bea1-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bea1-194">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5bea1-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bea1-195">Search-Flags</span></span>           | <span data-ttu-id="5bea1-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bea1-196">0x00000000</span></span>                                           |
| <span data-ttu-id="5bea1-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bea1-197">System-Flags</span></span>           | <span data-ttu-id="5bea1-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bea1-198">0x00000010</span></span>                                           |
| <span data-ttu-id="5bea1-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5bea1-199">Classes used in</span></span>        | [<span data-ttu-id="5bea1-200">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="5bea1-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5bea1-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5bea1-201">Windows Server 2008</span></span>



| <span data-ttu-id="5bea1-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5bea1-202">Entry</span></span> | <span data-ttu-id="5bea1-203">Wert</span><span class="sxs-lookup"><span data-stu-id="5bea1-203">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5bea1-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5bea1-204">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5bea1-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bea1-205">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5bea1-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bea1-206">System-Only</span></span>            | <span data-ttu-id="5bea1-207">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-207">False</span></span>                                                |
| <span data-ttu-id="5bea1-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5bea1-208">Is-Single-Valued</span></span>       | <span data-ttu-id="5bea1-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="5bea1-209">True</span></span>                                                 |
| <span data-ttu-id="5bea1-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5bea1-210">Is Indexed</span></span>             | <span data-ttu-id="5bea1-211">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-211">False</span></span>                                                |
| <span data-ttu-id="5bea1-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5bea1-212">In Global Catalog</span></span>      | <span data-ttu-id="5bea1-213">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-213">False</span></span>                                                |
| <span data-ttu-id="5bea1-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bea1-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bea1-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5bea1-215">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5bea1-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bea1-216">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5bea1-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bea1-217">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5bea1-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bea1-218">Search-Flags</span></span>           | <span data-ttu-id="5bea1-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bea1-219">0x00000000</span></span>                                           |
| <span data-ttu-id="5bea1-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bea1-220">System-Flags</span></span>           | <span data-ttu-id="5bea1-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bea1-221">0x00000010</span></span>                                           |
| <span data-ttu-id="5bea1-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5bea1-222">Classes used in</span></span>        | [<span data-ttu-id="5bea1-223">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="5bea1-223">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5bea1-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5bea1-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5bea1-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5bea1-225">Entry</span></span> | <span data-ttu-id="5bea1-226">Wert</span><span class="sxs-lookup"><span data-stu-id="5bea1-226">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5bea1-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5bea1-227">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5bea1-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bea1-228">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5bea1-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bea1-229">System-Only</span></span>            | <span data-ttu-id="5bea1-230">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-230">False</span></span>                                                |
| <span data-ttu-id="5bea1-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5bea1-231">Is-Single-Valued</span></span>       | <span data-ttu-id="5bea1-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="5bea1-232">True</span></span>                                                 |
| <span data-ttu-id="5bea1-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5bea1-233">Is Indexed</span></span>             | <span data-ttu-id="5bea1-234">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-234">False</span></span>                                                |
| <span data-ttu-id="5bea1-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5bea1-235">In Global Catalog</span></span>      | <span data-ttu-id="5bea1-236">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-236">False</span></span>                                                |
| <span data-ttu-id="5bea1-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bea1-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bea1-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5bea1-238">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5bea1-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bea1-239">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5bea1-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bea1-240">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5bea1-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bea1-241">Search-Flags</span></span>           | <span data-ttu-id="5bea1-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bea1-242">0x00000000</span></span>                                           |
| <span data-ttu-id="5bea1-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bea1-243">System-Flags</span></span>           | <span data-ttu-id="5bea1-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bea1-244">0x00000010</span></span>                                           |
| <span data-ttu-id="5bea1-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5bea1-245">Classes used in</span></span>        | [<span data-ttu-id="5bea1-246">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="5bea1-246">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5bea1-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5bea1-247">Windows Server 2012</span></span>



| <span data-ttu-id="5bea1-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5bea1-248">Entry</span></span> | <span data-ttu-id="5bea1-249">Wert</span><span class="sxs-lookup"><span data-stu-id="5bea1-249">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5bea1-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5bea1-250">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5bea1-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bea1-251">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5bea1-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bea1-252">System-Only</span></span>            | <span data-ttu-id="5bea1-253">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-253">False</span></span>                                                |
| <span data-ttu-id="5bea1-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5bea1-254">Is-Single-Valued</span></span>       | <span data-ttu-id="5bea1-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="5bea1-255">True</span></span>                                                 |
| <span data-ttu-id="5bea1-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5bea1-256">Is Indexed</span></span>             | <span data-ttu-id="5bea1-257">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-257">False</span></span>                                                |
| <span data-ttu-id="5bea1-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5bea1-258">In Global Catalog</span></span>      | <span data-ttu-id="5bea1-259">False</span><span class="sxs-lookup"><span data-stu-id="5bea1-259">False</span></span>                                                |
| <span data-ttu-id="5bea1-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bea1-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bea1-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5bea1-261">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5bea1-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bea1-262">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5bea1-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bea1-263">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5bea1-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bea1-264">Search-Flags</span></span>           | <span data-ttu-id="5bea1-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bea1-265">0x00000000</span></span>                                           |
| <span data-ttu-id="5bea1-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bea1-266">System-Flags</span></span>           | <span data-ttu-id="5bea1-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bea1-267">0x00000010</span></span>                                           |
| <span data-ttu-id="5bea1-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5bea1-268">Classes used in</span></span>        | [<span data-ttu-id="5bea1-269">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="5bea1-269">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





