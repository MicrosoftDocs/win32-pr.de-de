---
title: Dns-Record-Attribut
description: Wird zum Speichern binärer DNS-Ressourcen Einträge in DNS-Objekten verwendet.
ms.assetid: 2d5a17da-0efc-450e-b247-3ab6d2de3a5d
ms.tgt_platform: multiple
keywords:
- AD-Schema für Dns-Record-Attribut
- dnsrecord-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Dns-Record
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 013fa5ef4a9fcec151f996c347cdfd525438aa7d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123068"
---
# <a name="dns-record-attribute"></a><span data-ttu-id="4b7b2-105">Dns-Record-Attribut</span><span class="sxs-lookup"><span data-stu-id="4b7b2-105">Dns-Record attribute</span></span>

<span data-ttu-id="4b7b2-106">Wird zum Speichern binärer DNS-Ressourcen Einträge in DNS-Objekten verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b7b2-106">Used to store binary DNS resource records on DNS objects.</span></span>



| <span data-ttu-id="4b7b2-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4b7b2-107">Entry</span></span> | <span data-ttu-id="4b7b2-108">Wert</span><span class="sxs-lookup"><span data-stu-id="4b7b2-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="4b7b2-109">CN</span><span class="sxs-lookup"><span data-stu-id="4b7b2-109">CN</span></span>                | <span data-ttu-id="4b7b2-110">Dns-Record</span><span class="sxs-lookup"><span data-stu-id="4b7b2-110">Dns-Record</span></span>                                            |
| <span data-ttu-id="4b7b2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4b7b2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4b7b2-112">dnsrecord</span><span class="sxs-lookup"><span data-stu-id="4b7b2-112">dnsRecord</span></span>                                             |
| <span data-ttu-id="4b7b2-113">Size</span><span class="sxs-lookup"><span data-stu-id="4b7b2-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="4b7b2-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="4b7b2-114">Update Privilege</span></span>  | <span data-ttu-id="4b7b2-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4b7b2-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="4b7b2-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="4b7b2-116">Update Frequency</span></span>  | <span data-ttu-id="4b7b2-117">Wenn sich die DNS-Ressourcen Einträge ändern.</span><span class="sxs-lookup"><span data-stu-id="4b7b2-117">Whenever DNS resource records change.</span></span>                 |
| <span data-ttu-id="4b7b2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4b7b2-118">Attribute-Id</span></span>      | <span data-ttu-id="4b7b2-119">1.2.840.113556.1.4.382</span><span class="sxs-lookup"><span data-stu-id="4b7b2-119">1.2.840.113556.1.4.382</span></span>                                |
| <span data-ttu-id="4b7b2-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4b7b2-120">System-Id-Guid</span></span>    | <span data-ttu-id="4b7b2-121">e0fa1e69-9b45-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="4b7b2-121">e0fa1e69-9b45-11d0-afdd-00c04fd930c9</span></span>                  |
| <span data-ttu-id="4b7b2-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b7b2-122">Syntax</span></span>            | [<span data-ttu-id="4b7b2-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="4b7b2-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="4b7b2-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="4b7b2-124">Implementations</span></span>

-   [<span data-ttu-id="4b7b2-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4b7b2-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4b7b2-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4b7b2-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4b7b2-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4b7b2-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4b7b2-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4b7b2-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4b7b2-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4b7b2-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4b7b2-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4b7b2-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4b7b2-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4b7b2-131">Windows 2000 Server</span></span>



| <span data-ttu-id="4b7b2-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4b7b2-132">Entry</span></span> | <span data-ttu-id="4b7b2-133">Wert</span><span class="sxs-lookup"><span data-stu-id="4b7b2-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4b7b2-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4b7b2-134">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4b7b2-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b7b2-135">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4b7b2-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b7b2-136">System-Only</span></span>            | <span data-ttu-id="4b7b2-137">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-137">False</span></span>                                    |
| <span data-ttu-id="4b7b2-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4b7b2-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4b7b2-139">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-139">False</span></span>                                    |
| <span data-ttu-id="4b7b2-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4b7b2-140">Is Indexed</span></span>             | <span data-ttu-id="4b7b2-141">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-141">False</span></span>                                    |
| <span data-ttu-id="4b7b2-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4b7b2-142">In Global Catalog</span></span>      | <span data-ttu-id="4b7b2-143">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-143">False</span></span>                                    |
| <span data-ttu-id="4b7b2-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4b7b2-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b7b2-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4b7b2-145">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4b7b2-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b7b2-146">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4b7b2-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b7b2-147">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4b7b2-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b7b2-148">Search-Flags</span></span>           | <span data-ttu-id="4b7b2-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b7b2-149">0x00000000</span></span>                               |
| <span data-ttu-id="4b7b2-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b7b2-150">System-Flags</span></span>           | <span data-ttu-id="4b7b2-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b7b2-151">0x00000010</span></span>                               |
| <span data-ttu-id="4b7b2-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4b7b2-152">Classes used in</span></span>        | [<span data-ttu-id="4b7b2-153">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="4b7b2-153">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4b7b2-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4b7b2-154">Windows Server 2003</span></span>



| <span data-ttu-id="4b7b2-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4b7b2-155">Entry</span></span> | <span data-ttu-id="4b7b2-156">Wert</span><span class="sxs-lookup"><span data-stu-id="4b7b2-156">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4b7b2-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4b7b2-157">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4b7b2-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b7b2-158">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4b7b2-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b7b2-159">System-Only</span></span>            | <span data-ttu-id="4b7b2-160">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-160">False</span></span>                                    |
| <span data-ttu-id="4b7b2-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4b7b2-161">Is-Single-Valued</span></span>       | <span data-ttu-id="4b7b2-162">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-162">False</span></span>                                    |
| <span data-ttu-id="4b7b2-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4b7b2-163">Is Indexed</span></span>             | <span data-ttu-id="4b7b2-164">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-164">False</span></span>                                    |
| <span data-ttu-id="4b7b2-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4b7b2-165">In Global Catalog</span></span>      | <span data-ttu-id="4b7b2-166">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-166">False</span></span>                                    |
| <span data-ttu-id="4b7b2-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4b7b2-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b7b2-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4b7b2-168">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4b7b2-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b7b2-169">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4b7b2-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b7b2-170">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4b7b2-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b7b2-171">Search-Flags</span></span>           | <span data-ttu-id="4b7b2-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b7b2-172">0x00000000</span></span>                               |
| <span data-ttu-id="4b7b2-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b7b2-173">System-Flags</span></span>           | <span data-ttu-id="4b7b2-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b7b2-174">0x00000010</span></span>                               |
| <span data-ttu-id="4b7b2-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4b7b2-175">Classes used in</span></span>        | [<span data-ttu-id="4b7b2-176">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="4b7b2-176">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4b7b2-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4b7b2-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4b7b2-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4b7b2-178">Entry</span></span> | <span data-ttu-id="4b7b2-179">Wert</span><span class="sxs-lookup"><span data-stu-id="4b7b2-179">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4b7b2-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4b7b2-180">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4b7b2-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b7b2-181">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4b7b2-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b7b2-182">System-Only</span></span>            | <span data-ttu-id="4b7b2-183">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-183">False</span></span>                                    |
| <span data-ttu-id="4b7b2-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4b7b2-184">Is-Single-Valued</span></span>       | <span data-ttu-id="4b7b2-185">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-185">False</span></span>                                    |
| <span data-ttu-id="4b7b2-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4b7b2-186">Is Indexed</span></span>             | <span data-ttu-id="4b7b2-187">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-187">False</span></span>                                    |
| <span data-ttu-id="4b7b2-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4b7b2-188">In Global Catalog</span></span>      | <span data-ttu-id="4b7b2-189">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-189">False</span></span>                                    |
| <span data-ttu-id="4b7b2-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4b7b2-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b7b2-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4b7b2-191">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4b7b2-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b7b2-192">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4b7b2-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b7b2-193">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4b7b2-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b7b2-194">Search-Flags</span></span>           | <span data-ttu-id="4b7b2-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b7b2-195">0x00000000</span></span>                               |
| <span data-ttu-id="4b7b2-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b7b2-196">System-Flags</span></span>           | <span data-ttu-id="4b7b2-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b7b2-197">0x00000010</span></span>                               |
| <span data-ttu-id="4b7b2-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4b7b2-198">Classes used in</span></span>        | [<span data-ttu-id="4b7b2-199">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="4b7b2-199">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4b7b2-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b7b2-200">Windows Server 2008</span></span>



| <span data-ttu-id="4b7b2-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4b7b2-201">Entry</span></span> | <span data-ttu-id="4b7b2-202">Wert</span><span class="sxs-lookup"><span data-stu-id="4b7b2-202">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4b7b2-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4b7b2-203">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4b7b2-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b7b2-204">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4b7b2-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b7b2-205">System-Only</span></span>            | <span data-ttu-id="4b7b2-206">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-206">False</span></span>                                    |
| <span data-ttu-id="4b7b2-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4b7b2-207">Is-Single-Valued</span></span>       | <span data-ttu-id="4b7b2-208">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-208">False</span></span>                                    |
| <span data-ttu-id="4b7b2-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4b7b2-209">Is Indexed</span></span>             | <span data-ttu-id="4b7b2-210">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-210">False</span></span>                                    |
| <span data-ttu-id="4b7b2-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4b7b2-211">In Global Catalog</span></span>      | <span data-ttu-id="4b7b2-212">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-212">False</span></span>                                    |
| <span data-ttu-id="4b7b2-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4b7b2-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b7b2-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4b7b2-214">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4b7b2-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b7b2-215">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4b7b2-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b7b2-216">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4b7b2-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b7b2-217">Search-Flags</span></span>           | <span data-ttu-id="4b7b2-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b7b2-218">0x00000000</span></span>                               |
| <span data-ttu-id="4b7b2-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b7b2-219">System-Flags</span></span>           | <span data-ttu-id="4b7b2-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b7b2-220">0x00000010</span></span>                               |
| <span data-ttu-id="4b7b2-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4b7b2-221">Classes used in</span></span>        | [<span data-ttu-id="4b7b2-222">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="4b7b2-222">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4b7b2-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4b7b2-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4b7b2-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4b7b2-224">Entry</span></span> | <span data-ttu-id="4b7b2-225">Wert</span><span class="sxs-lookup"><span data-stu-id="4b7b2-225">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4b7b2-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4b7b2-226">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4b7b2-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b7b2-227">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4b7b2-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b7b2-228">System-Only</span></span>            | <span data-ttu-id="4b7b2-229">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-229">False</span></span>                                    |
| <span data-ttu-id="4b7b2-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4b7b2-230">Is-Single-Valued</span></span>       | <span data-ttu-id="4b7b2-231">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-231">False</span></span>                                    |
| <span data-ttu-id="4b7b2-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4b7b2-232">Is Indexed</span></span>             | <span data-ttu-id="4b7b2-233">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-233">False</span></span>                                    |
| <span data-ttu-id="4b7b2-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4b7b2-234">In Global Catalog</span></span>      | <span data-ttu-id="4b7b2-235">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-235">False</span></span>                                    |
| <span data-ttu-id="4b7b2-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4b7b2-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b7b2-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4b7b2-237">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4b7b2-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b7b2-238">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4b7b2-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b7b2-239">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4b7b2-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b7b2-240">Search-Flags</span></span>           | <span data-ttu-id="4b7b2-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b7b2-241">0x00000000</span></span>                               |
| <span data-ttu-id="4b7b2-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b7b2-242">System-Flags</span></span>           | <span data-ttu-id="4b7b2-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b7b2-243">0x00000010</span></span>                               |
| <span data-ttu-id="4b7b2-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4b7b2-244">Classes used in</span></span>        | [<span data-ttu-id="4b7b2-245">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="4b7b2-245">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4b7b2-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4b7b2-246">Windows Server 2012</span></span>



| <span data-ttu-id="4b7b2-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4b7b2-247">Entry</span></span> | <span data-ttu-id="4b7b2-248">Wert</span><span class="sxs-lookup"><span data-stu-id="4b7b2-248">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4b7b2-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4b7b2-249">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4b7b2-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b7b2-250">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4b7b2-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b7b2-251">System-Only</span></span>            | <span data-ttu-id="4b7b2-252">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-252">False</span></span>                                    |
| <span data-ttu-id="4b7b2-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4b7b2-253">Is-Single-Valued</span></span>       | <span data-ttu-id="4b7b2-254">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-254">False</span></span>                                    |
| <span data-ttu-id="4b7b2-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4b7b2-255">Is Indexed</span></span>             | <span data-ttu-id="4b7b2-256">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-256">False</span></span>                                    |
| <span data-ttu-id="4b7b2-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4b7b2-257">In Global Catalog</span></span>      | <span data-ttu-id="4b7b2-258">False</span><span class="sxs-lookup"><span data-stu-id="4b7b2-258">False</span></span>                                    |
| <span data-ttu-id="4b7b2-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4b7b2-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b7b2-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4b7b2-260">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4b7b2-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b7b2-261">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4b7b2-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b7b2-262">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4b7b2-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b7b2-263">Search-Flags</span></span>           | <span data-ttu-id="4b7b2-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b7b2-264">0x00000000</span></span>                               |
| <span data-ttu-id="4b7b2-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b7b2-265">System-Flags</span></span>           | <span data-ttu-id="4b7b2-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b7b2-266">0x00000010</span></span>                               |
| <span data-ttu-id="4b7b2-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4b7b2-267">Classes used in</span></span>        | [<span data-ttu-id="4b7b2-268">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="4b7b2-268">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



 

 





