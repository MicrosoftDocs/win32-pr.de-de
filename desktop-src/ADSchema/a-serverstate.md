---
title: Server-State-Attribut
description: Gibt an, ob der Server aktiviert oder deaktiviert ist.
ms.assetid: e062cbcf-c845-4dfd-9e9b-e21079276a3c
ms.tgt_platform: multiple
keywords:
- AD-Schema für Server-State-Attribut
- ServerState-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Server-State
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be4e236254486cd512eed480b380058048061fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106340031"
---
# <a name="server-state-attribute"></a><span data-ttu-id="e0fcd-105">Server-State-Attribut</span><span class="sxs-lookup"><span data-stu-id="e0fcd-105">Server-State attribute</span></span>

<span data-ttu-id="e0fcd-106">Gibt an, ob der Server aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e0fcd-106">Indicates whether the server is enabled or disabled.</span></span> <span data-ttu-id="e0fcd-107">Der Wert 1 gibt an, dass der Server aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e0fcd-107">A value of 1 indicates that the server is enabled.</span></span> <span data-ttu-id="e0fcd-108">Der Wert 2 gibt an, dass der Server deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e0fcd-108">A value of 2 indicates that the server is disabled.</span></span> <span data-ttu-id="e0fcd-109">Alle anderen Werte sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="e0fcd-109">All other values are invalid.</span></span>



| <span data-ttu-id="e0fcd-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0fcd-110">Entry</span></span> | <span data-ttu-id="e0fcd-111">Wert</span><span class="sxs-lookup"><span data-stu-id="e0fcd-111">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e0fcd-112">CN</span><span class="sxs-lookup"><span data-stu-id="e0fcd-112">CN</span></span>                | <span data-ttu-id="e0fcd-113">Server-State</span><span class="sxs-lookup"><span data-stu-id="e0fcd-113">Server-State</span></span>                         |
| <span data-ttu-id="e0fcd-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e0fcd-114">Ldap-Display-Name</span></span> | <span data-ttu-id="e0fcd-115">serverState</span><span class="sxs-lookup"><span data-stu-id="e0fcd-115">serverState</span></span>                          |
| <span data-ttu-id="e0fcd-116">Size</span><span class="sxs-lookup"><span data-stu-id="e0fcd-116">Size</span></span>              | \-                                   |
| <span data-ttu-id="e0fcd-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e0fcd-117">Update Privilege</span></span>  | <span data-ttu-id="e0fcd-118">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e0fcd-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="e0fcd-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="e0fcd-119">Update Frequency</span></span>  | <span data-ttu-id="e0fcd-120">Wenn die Richtlinie für einen Benutzer geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e0fcd-120">When the policy for a user changes.</span></span>  |
| <span data-ttu-id="e0fcd-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e0fcd-121">Attribute-Id</span></span>      | <span data-ttu-id="e0fcd-122">1.2.840.113556.1.4.154</span><span class="sxs-lookup"><span data-stu-id="e0fcd-122">1.2.840.113556.1.4.154</span></span>               |
| <span data-ttu-id="e0fcd-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e0fcd-123">System-Id-Guid</span></span>    | <span data-ttu-id="e0fcd-124">bf967a34-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e0fcd-124">bf967a34-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="e0fcd-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0fcd-125">Syntax</span></span>            | [<span data-ttu-id="e0fcd-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="e0fcd-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="e0fcd-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="e0fcd-127">Implementations</span></span>

-   [<span data-ttu-id="e0fcd-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e0fcd-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e0fcd-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e0fcd-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e0fcd-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e0fcd-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e0fcd-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e0fcd-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e0fcd-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e0fcd-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e0fcd-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e0fcd-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e0fcd-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e0fcd-134">Windows 2000 Server</span></span>



| <span data-ttu-id="e0fcd-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0fcd-135">Entry</span></span> | <span data-ttu-id="e0fcd-136">Wert</span><span class="sxs-lookup"><span data-stu-id="e0fcd-136">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="e0fcd-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e0fcd-137">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e0fcd-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0fcd-138">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e0fcd-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0fcd-139">System-Only</span></span>            | <span data-ttu-id="e0fcd-140">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-140">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e0fcd-141">Is-Single-Valued</span></span>       | <span data-ttu-id="e0fcd-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="e0fcd-142">True</span></span>                                                  |
| <span data-ttu-id="e0fcd-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e0fcd-143">Is Indexed</span></span>             | <span data-ttu-id="e0fcd-144">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-144">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e0fcd-145">In Global Catalog</span></span>      | <span data-ttu-id="e0fcd-146">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-146">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0fcd-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0fcd-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e0fcd-148">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="e0fcd-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0fcd-149">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="e0fcd-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0fcd-150">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="e0fcd-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0fcd-151">Search-Flags</span></span>           | <span data-ttu-id="e0fcd-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0fcd-152">0x00000000</span></span>                                            |
| <span data-ttu-id="e0fcd-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0fcd-153">System-Flags</span></span>           | <span data-ttu-id="e0fcd-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e0fcd-154">0x00000011</span></span>                                            |
| <span data-ttu-id="e0fcd-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e0fcd-155">Classes used in</span></span>        | [<span data-ttu-id="e0fcd-156">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="e0fcd-156">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e0fcd-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e0fcd-157">Windows Server 2003</span></span>



| <span data-ttu-id="e0fcd-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0fcd-158">Entry</span></span> | <span data-ttu-id="e0fcd-159">Wert</span><span class="sxs-lookup"><span data-stu-id="e0fcd-159">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="e0fcd-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e0fcd-160">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e0fcd-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0fcd-161">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e0fcd-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0fcd-162">System-Only</span></span>            | <span data-ttu-id="e0fcd-163">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-163">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e0fcd-164">Is-Single-Valued</span></span>       | <span data-ttu-id="e0fcd-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="e0fcd-165">True</span></span>                                                  |
| <span data-ttu-id="e0fcd-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e0fcd-166">Is Indexed</span></span>             | <span data-ttu-id="e0fcd-167">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-167">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e0fcd-168">In Global Catalog</span></span>      | <span data-ttu-id="e0fcd-169">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-169">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0fcd-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0fcd-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e0fcd-171">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="e0fcd-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0fcd-172">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="e0fcd-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0fcd-173">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="e0fcd-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0fcd-174">Search-Flags</span></span>           | <span data-ttu-id="e0fcd-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0fcd-175">0x00000000</span></span>                                            |
| <span data-ttu-id="e0fcd-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0fcd-176">System-Flags</span></span>           | <span data-ttu-id="e0fcd-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e0fcd-177">0x00000011</span></span>                                            |
| <span data-ttu-id="e0fcd-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e0fcd-178">Classes used in</span></span>        | [<span data-ttu-id="e0fcd-179">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="e0fcd-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e0fcd-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e0fcd-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e0fcd-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0fcd-181">Entry</span></span> | <span data-ttu-id="e0fcd-182">Wert</span><span class="sxs-lookup"><span data-stu-id="e0fcd-182">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="e0fcd-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e0fcd-183">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e0fcd-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0fcd-184">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e0fcd-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0fcd-185">System-Only</span></span>            | <span data-ttu-id="e0fcd-186">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-186">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e0fcd-187">Is-Single-Valued</span></span>       | <span data-ttu-id="e0fcd-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="e0fcd-188">True</span></span>                                                  |
| <span data-ttu-id="e0fcd-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e0fcd-189">Is Indexed</span></span>             | <span data-ttu-id="e0fcd-190">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-190">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e0fcd-191">In Global Catalog</span></span>      | <span data-ttu-id="e0fcd-192">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-192">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0fcd-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0fcd-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e0fcd-194">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="e0fcd-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0fcd-195">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="e0fcd-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0fcd-196">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="e0fcd-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0fcd-197">Search-Flags</span></span>           | <span data-ttu-id="e0fcd-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0fcd-198">0x00000000</span></span>                                            |
| <span data-ttu-id="e0fcd-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0fcd-199">System-Flags</span></span>           | <span data-ttu-id="e0fcd-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e0fcd-200">0x00000011</span></span>                                            |
| <span data-ttu-id="e0fcd-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e0fcd-201">Classes used in</span></span>        | [<span data-ttu-id="e0fcd-202">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="e0fcd-202">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e0fcd-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0fcd-203">Windows Server 2008</span></span>



| <span data-ttu-id="e0fcd-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0fcd-204">Entry</span></span> | <span data-ttu-id="e0fcd-205">Wert</span><span class="sxs-lookup"><span data-stu-id="e0fcd-205">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="e0fcd-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e0fcd-206">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e0fcd-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0fcd-207">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e0fcd-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0fcd-208">System-Only</span></span>            | <span data-ttu-id="e0fcd-209">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-209">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e0fcd-210">Is-Single-Valued</span></span>       | <span data-ttu-id="e0fcd-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="e0fcd-211">True</span></span>                                                  |
| <span data-ttu-id="e0fcd-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e0fcd-212">Is Indexed</span></span>             | <span data-ttu-id="e0fcd-213">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-213">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e0fcd-214">In Global Catalog</span></span>      | <span data-ttu-id="e0fcd-215">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-215">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0fcd-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0fcd-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e0fcd-217">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="e0fcd-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0fcd-218">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="e0fcd-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0fcd-219">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="e0fcd-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0fcd-220">Search-Flags</span></span>           | <span data-ttu-id="e0fcd-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0fcd-221">0x00000000</span></span>                                            |
| <span data-ttu-id="e0fcd-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0fcd-222">System-Flags</span></span>           | <span data-ttu-id="e0fcd-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e0fcd-223">0x00000011</span></span>                                            |
| <span data-ttu-id="e0fcd-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e0fcd-224">Classes used in</span></span>        | [<span data-ttu-id="e0fcd-225">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="e0fcd-225">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e0fcd-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e0fcd-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e0fcd-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0fcd-227">Entry</span></span> | <span data-ttu-id="e0fcd-228">Wert</span><span class="sxs-lookup"><span data-stu-id="e0fcd-228">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="e0fcd-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e0fcd-229">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e0fcd-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0fcd-230">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e0fcd-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0fcd-231">System-Only</span></span>            | <span data-ttu-id="e0fcd-232">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-232">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e0fcd-233">Is-Single-Valued</span></span>       | <span data-ttu-id="e0fcd-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="e0fcd-234">True</span></span>                                                  |
| <span data-ttu-id="e0fcd-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e0fcd-235">Is Indexed</span></span>             | <span data-ttu-id="e0fcd-236">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-236">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e0fcd-237">In Global Catalog</span></span>      | <span data-ttu-id="e0fcd-238">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-238">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0fcd-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0fcd-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e0fcd-240">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="e0fcd-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0fcd-241">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="e0fcd-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0fcd-242">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="e0fcd-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0fcd-243">Search-Flags</span></span>           | <span data-ttu-id="e0fcd-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0fcd-244">0x00000000</span></span>                                            |
| <span data-ttu-id="e0fcd-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0fcd-245">System-Flags</span></span>           | <span data-ttu-id="e0fcd-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e0fcd-246">0x00000011</span></span>                                            |
| <span data-ttu-id="e0fcd-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e0fcd-247">Classes used in</span></span>        | [<span data-ttu-id="e0fcd-248">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="e0fcd-248">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e0fcd-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0fcd-249">Windows Server 2012</span></span>



| <span data-ttu-id="e0fcd-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0fcd-250">Entry</span></span> | <span data-ttu-id="e0fcd-251">Wert</span><span class="sxs-lookup"><span data-stu-id="e0fcd-251">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="e0fcd-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e0fcd-252">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e0fcd-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0fcd-253">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e0fcd-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0fcd-254">System-Only</span></span>            | <span data-ttu-id="e0fcd-255">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-255">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e0fcd-256">Is-Single-Valued</span></span>       | <span data-ttu-id="e0fcd-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="e0fcd-257">True</span></span>                                                  |
| <span data-ttu-id="e0fcd-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e0fcd-258">Is Indexed</span></span>             | <span data-ttu-id="e0fcd-259">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-259">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e0fcd-260">In Global Catalog</span></span>      | <span data-ttu-id="e0fcd-261">False</span><span class="sxs-lookup"><span data-stu-id="e0fcd-261">False</span></span>                                                 |
| <span data-ttu-id="e0fcd-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0fcd-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0fcd-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e0fcd-263">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="e0fcd-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0fcd-264">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="e0fcd-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0fcd-265">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="e0fcd-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0fcd-266">Search-Flags</span></span>           | <span data-ttu-id="e0fcd-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0fcd-267">0x00000000</span></span>                                            |
| <span data-ttu-id="e0fcd-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0fcd-268">System-Flags</span></span>           | <span data-ttu-id="e0fcd-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e0fcd-269">0x00000011</span></span>                                            |
| <span data-ttu-id="e0fcd-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e0fcd-270">Classes used in</span></span>        | [<span data-ttu-id="e0fcd-271">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="e0fcd-271">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





