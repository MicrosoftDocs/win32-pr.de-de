---
title: DNS-Property-Attribut
description: Wird zum Speichern von Binär Einstellungen (Eigenschaften) in DNS-Zonen Objekten verwendet.
ms.assetid: 55ea38cd-6b5b-4500-8e68-ae4d35e4b177
ms.tgt_platform: multiple
keywords:
- AD-Schema für DNS-Property-Attribut
- dnsproperty-Attribut AD-Schema
topic_type:
- apiref
api_name:
- DNS-Property
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f8fd18f4524ec0bf61a609d21a361668ed295b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346550"
---
# <a name="dns-property-attribute"></a><span data-ttu-id="ac6a1-105">DNS-Property-Attribut</span><span class="sxs-lookup"><span data-stu-id="ac6a1-105">DNS-Property attribute</span></span>

<span data-ttu-id="ac6a1-106">Wird zum Speichern von Binär Einstellungen (Eigenschaften) in DNS-Zonen Objekten verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac6a1-106">Used to store binary settings (properties) on DNS zone objects.</span></span>



| <span data-ttu-id="ac6a1-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ac6a1-107">Entry</span></span> | <span data-ttu-id="ac6a1-108">Wert</span><span class="sxs-lookup"><span data-stu-id="ac6a1-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="ac6a1-109">CN</span><span class="sxs-lookup"><span data-stu-id="ac6a1-109">CN</span></span>                | <span data-ttu-id="ac6a1-110">DNS-Property</span><span class="sxs-lookup"><span data-stu-id="ac6a1-110">DNS-Property</span></span>                                          |
| <span data-ttu-id="ac6a1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ac6a1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ac6a1-112">dnsproperty</span><span class="sxs-lookup"><span data-stu-id="ac6a1-112">dNSProperty</span></span>                                           |
| <span data-ttu-id="ac6a1-113">Size</span><span class="sxs-lookup"><span data-stu-id="ac6a1-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="ac6a1-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ac6a1-114">Update Privilege</span></span>  | <span data-ttu-id="ac6a1-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ac6a1-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="ac6a1-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="ac6a1-116">Update Frequency</span></span>  | <span data-ttu-id="ac6a1-117">Wenn sich die DNS-Zonendaten Sätze ändern.</span><span class="sxs-lookup"><span data-stu-id="ac6a1-117">Whenever DNS zone records change.</span></span>                     |
| <span data-ttu-id="ac6a1-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ac6a1-118">Attribute-Id</span></span>      | <span data-ttu-id="ac6a1-119">1.2.840.113556.1.4.1306</span><span class="sxs-lookup"><span data-stu-id="ac6a1-119">1.2.840.113556.1.4.1306</span></span>                               |
| <span data-ttu-id="ac6a1-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ac6a1-120">System-Id-Guid</span></span>    | <span data-ttu-id="ac6a1-121">675a15fe-3b70-11d2-90cc-00c04f d91ab1</span><span class="sxs-lookup"><span data-stu-id="ac6a1-121">675a15fe-3b70-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="ac6a1-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac6a1-122">Syntax</span></span>            | [<span data-ttu-id="ac6a1-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="ac6a1-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ac6a1-124">Implementations</span></span>

-   [<span data-ttu-id="ac6a1-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ac6a1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ac6a1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ac6a1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ac6a1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ac6a1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ac6a1-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ac6a1-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ac6a1-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ac6a1-132">Entry</span></span> | <span data-ttu-id="ac6a1-133">Wert</span><span class="sxs-lookup"><span data-stu-id="ac6a1-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ac6a1-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ac6a1-134">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="ac6a1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac6a1-135">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="ac6a1-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac6a1-136">System-Only</span></span>            | <span data-ttu-id="ac6a1-137">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-137">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ac6a1-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ac6a1-139">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-139">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ac6a1-140">Is Indexed</span></span>             | <span data-ttu-id="ac6a1-141">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-141">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ac6a1-142">In Global Catalog</span></span>      | <span data-ttu-id="ac6a1-143">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-143">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ac6a1-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac6a1-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ac6a1-145">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="ac6a1-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac6a1-146">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="ac6a1-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac6a1-147">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="ac6a1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac6a1-148">Search-Flags</span></span>           | <span data-ttu-id="ac6a1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac6a1-149">0x00000000</span></span>                                                                        |
| <span data-ttu-id="ac6a1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac6a1-150">System-Flags</span></span>           | <span data-ttu-id="ac6a1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac6a1-151">0x00000010</span></span>                                                                        |
| <span data-ttu-id="ac6a1-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ac6a1-152">Classes used in</span></span>        | [<span data-ttu-id="ac6a1-153">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-153">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="ac6a1-154">**DNS-Zone**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-154">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ac6a1-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ac6a1-155">Windows Server 2003</span></span>



| <span data-ttu-id="ac6a1-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ac6a1-156">Entry</span></span> | <span data-ttu-id="ac6a1-157">Wert</span><span class="sxs-lookup"><span data-stu-id="ac6a1-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ac6a1-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ac6a1-158">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="ac6a1-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac6a1-159">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="ac6a1-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac6a1-160">System-Only</span></span>            | <span data-ttu-id="ac6a1-161">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-161">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ac6a1-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ac6a1-163">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-163">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ac6a1-164">Is Indexed</span></span>             | <span data-ttu-id="ac6a1-165">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-165">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ac6a1-166">In Global Catalog</span></span>      | <span data-ttu-id="ac6a1-167">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-167">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ac6a1-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac6a1-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ac6a1-169">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="ac6a1-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac6a1-170">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="ac6a1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac6a1-171">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="ac6a1-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac6a1-172">Search-Flags</span></span>           | <span data-ttu-id="ac6a1-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac6a1-173">0x00000000</span></span>                                                                        |
| <span data-ttu-id="ac6a1-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac6a1-174">System-Flags</span></span>           | <span data-ttu-id="ac6a1-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac6a1-175">0x00000010</span></span>                                                                        |
| <span data-ttu-id="ac6a1-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ac6a1-176">Classes used in</span></span>        | [<span data-ttu-id="ac6a1-177">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-177">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="ac6a1-178">**DNS-Zone**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-178">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ac6a1-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ac6a1-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ac6a1-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ac6a1-180">Entry</span></span> | <span data-ttu-id="ac6a1-181">Wert</span><span class="sxs-lookup"><span data-stu-id="ac6a1-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ac6a1-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ac6a1-182">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="ac6a1-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac6a1-183">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="ac6a1-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac6a1-184">System-Only</span></span>            | <span data-ttu-id="ac6a1-185">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-185">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ac6a1-186">Is-Single-Valued</span></span>       | <span data-ttu-id="ac6a1-187">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-187">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ac6a1-188">Is Indexed</span></span>             | <span data-ttu-id="ac6a1-189">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-189">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ac6a1-190">In Global Catalog</span></span>      | <span data-ttu-id="ac6a1-191">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-191">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ac6a1-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac6a1-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ac6a1-193">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="ac6a1-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac6a1-194">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="ac6a1-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac6a1-195">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="ac6a1-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac6a1-196">Search-Flags</span></span>           | <span data-ttu-id="ac6a1-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac6a1-197">0x00000000</span></span>                                                                        |
| <span data-ttu-id="ac6a1-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac6a1-198">System-Flags</span></span>           | <span data-ttu-id="ac6a1-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac6a1-199">0x00000010</span></span>                                                                        |
| <span data-ttu-id="ac6a1-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ac6a1-200">Classes used in</span></span>        | [<span data-ttu-id="ac6a1-201">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-201">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="ac6a1-202">**DNS-Zone**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-202">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ac6a1-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac6a1-203">Windows Server 2008</span></span>



| <span data-ttu-id="ac6a1-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ac6a1-204">Entry</span></span> | <span data-ttu-id="ac6a1-205">Wert</span><span class="sxs-lookup"><span data-stu-id="ac6a1-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ac6a1-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ac6a1-206">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="ac6a1-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac6a1-207">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="ac6a1-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac6a1-208">System-Only</span></span>            | <span data-ttu-id="ac6a1-209">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-209">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ac6a1-210">Is-Single-Valued</span></span>       | <span data-ttu-id="ac6a1-211">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-211">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ac6a1-212">Is Indexed</span></span>             | <span data-ttu-id="ac6a1-213">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-213">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ac6a1-214">In Global Catalog</span></span>      | <span data-ttu-id="ac6a1-215">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-215">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ac6a1-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac6a1-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ac6a1-217">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="ac6a1-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac6a1-218">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="ac6a1-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac6a1-219">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="ac6a1-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac6a1-220">Search-Flags</span></span>           | <span data-ttu-id="ac6a1-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac6a1-221">0x00000000</span></span>                                                                        |
| <span data-ttu-id="ac6a1-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac6a1-222">System-Flags</span></span>           | <span data-ttu-id="ac6a1-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac6a1-223">0x00000010</span></span>                                                                        |
| <span data-ttu-id="ac6a1-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ac6a1-224">Classes used in</span></span>        | [<span data-ttu-id="ac6a1-225">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-225">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="ac6a1-226">**DNS-Zone**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-226">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ac6a1-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ac6a1-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ac6a1-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ac6a1-228">Entry</span></span> | <span data-ttu-id="ac6a1-229">Wert</span><span class="sxs-lookup"><span data-stu-id="ac6a1-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ac6a1-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ac6a1-230">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="ac6a1-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac6a1-231">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="ac6a1-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac6a1-232">System-Only</span></span>            | <span data-ttu-id="ac6a1-233">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-233">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ac6a1-234">Is-Single-Valued</span></span>       | <span data-ttu-id="ac6a1-235">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-235">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ac6a1-236">Is Indexed</span></span>             | <span data-ttu-id="ac6a1-237">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-237">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ac6a1-238">In Global Catalog</span></span>      | <span data-ttu-id="ac6a1-239">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-239">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ac6a1-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac6a1-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ac6a1-241">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="ac6a1-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac6a1-242">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="ac6a1-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac6a1-243">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="ac6a1-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac6a1-244">Search-Flags</span></span>           | <span data-ttu-id="ac6a1-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac6a1-245">0x00000000</span></span>                                                                        |
| <span data-ttu-id="ac6a1-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac6a1-246">System-Flags</span></span>           | <span data-ttu-id="ac6a1-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac6a1-247">0x00000010</span></span>                                                                        |
| <span data-ttu-id="ac6a1-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ac6a1-248">Classes used in</span></span>        | [<span data-ttu-id="ac6a1-249">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-249">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="ac6a1-250">**DNS-Zone**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-250">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ac6a1-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ac6a1-251">Windows Server 2012</span></span>



| <span data-ttu-id="ac6a1-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ac6a1-252">Entry</span></span> | <span data-ttu-id="ac6a1-253">Wert</span><span class="sxs-lookup"><span data-stu-id="ac6a1-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ac6a1-254">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ac6a1-254">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="ac6a1-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac6a1-255">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="ac6a1-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac6a1-256">System-Only</span></span>            | <span data-ttu-id="ac6a1-257">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-257">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-258">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ac6a1-258">Is-Single-Valued</span></span>       | <span data-ttu-id="ac6a1-259">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-259">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-260">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ac6a1-260">Is Indexed</span></span>             | <span data-ttu-id="ac6a1-261">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-261">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-262">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ac6a1-262">In Global Catalog</span></span>      | <span data-ttu-id="ac6a1-263">False</span><span class="sxs-lookup"><span data-stu-id="ac6a1-263">False</span></span>                                                                             |
| <span data-ttu-id="ac6a1-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ac6a1-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac6a1-265">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ac6a1-265">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="ac6a1-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac6a1-266">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="ac6a1-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac6a1-267">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="ac6a1-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac6a1-268">Search-Flags</span></span>           | <span data-ttu-id="ac6a1-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac6a1-269">0x00000000</span></span>                                                                        |
| <span data-ttu-id="ac6a1-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac6a1-270">System-Flags</span></span>           | <span data-ttu-id="ac6a1-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac6a1-271">0x00000010</span></span>                                                                        |
| <span data-ttu-id="ac6a1-272">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ac6a1-272">Classes used in</span></span>        | [<span data-ttu-id="ac6a1-273">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-273">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="ac6a1-274">**DNS-Zone**</span><span class="sxs-lookup"><span data-stu-id="ac6a1-274">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 





