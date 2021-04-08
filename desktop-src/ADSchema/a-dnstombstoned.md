---
title: DNS-Tombstoned-Attribut
description: True, wenn für dieses Objekt ein tombstoning durchgearbeitet wurde. Dieses Attribut ist vorhanden, um die Suche nach tombstoning-Datensätzen zu vereinfachen und zu beschleunigen. Objekte mit tombstoning sind Objekte, die gelöscht, aber noch nicht aus dem Verzeichnis entfernt wurden.
ms.assetid: d876a6d7-d5bc-4fe2-af03-1fff3381708f
ms.tgt_platform: multiple
keywords:
- AD-Schema für DNS-Tombstoned-Attribut
- dnstombstoning-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- DNS-Tombstoned
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dba61706861b808f28d7f6874a9bfd93d4152c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859490"
---
# <a name="dns-tombstoned-attribute"></a><span data-ttu-id="27867-107">DNS-Tombstoned-Attribut</span><span class="sxs-lookup"><span data-stu-id="27867-107">DNS-Tombstoned attribute</span></span>

<span data-ttu-id="27867-108">True, wenn für dieses Objekt ein tombstoning durchgearbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="27867-108">True if this object has been tombstoned.</span></span> <span data-ttu-id="27867-109">Dieses Attribut ist vorhanden, um die Suche nach tombstoning-Datensätzen zu vereinfachen und zu beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="27867-109">This attribute exists to make searching for tombstoned records easier and faster.</span></span> <span data-ttu-id="27867-110">Objekte mit tombstoning sind Objekte, die gelöscht, aber noch nicht aus dem Verzeichnis entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="27867-110">Tombstoned objects are objects that have been deleted but not yet removed from the directory.</span></span>



| <span data-ttu-id="27867-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="27867-111">Entry</span></span> | <span data-ttu-id="27867-112">Wert</span><span class="sxs-lookup"><span data-stu-id="27867-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="27867-113">CN</span><span class="sxs-lookup"><span data-stu-id="27867-113">CN</span></span>                | <span data-ttu-id="27867-114">DNS-Tombstoned</span><span class="sxs-lookup"><span data-stu-id="27867-114">DNS-Tombstoned</span></span>                       |
| <span data-ttu-id="27867-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="27867-115">Ldap-Display-Name</span></span> | <span data-ttu-id="27867-116">dnstombstoning</span><span class="sxs-lookup"><span data-stu-id="27867-116">dNSTombstoned</span></span>                        |
| <span data-ttu-id="27867-117">Size</span><span class="sxs-lookup"><span data-stu-id="27867-117">Size</span></span>              | <span data-ttu-id="27867-118">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="27867-118">4 bytes</span></span>                              |
| <span data-ttu-id="27867-119">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="27867-119">Update Privilege</span></span>  | <span data-ttu-id="27867-120">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="27867-120">This value is set by the system.</span></span>     |
| <span data-ttu-id="27867-121">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="27867-121">Update Frequency</span></span>  | <span data-ttu-id="27867-122">Jedes Mal, wenn ein Objekt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="27867-122">Whenever an object is deleted.</span></span>       |
| <span data-ttu-id="27867-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="27867-123">Attribute-Id</span></span>      | <span data-ttu-id="27867-124">1.2.840.113556.1.4.1414</span><span class="sxs-lookup"><span data-stu-id="27867-124">1.2.840.113556.1.4.1414</span></span>              |
| <span data-ttu-id="27867-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="27867-125">System-Id-Guid</span></span>    | <span data-ttu-id="27867-126">d5eb2eb7-be4e-463b-a214-634a44d7392e</span><span class="sxs-lookup"><span data-stu-id="27867-126">d5eb2eb7-be4e-463b-a214-634a44d7392e</span></span> |
| <span data-ttu-id="27867-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="27867-127">Syntax</span></span>            | [<span data-ttu-id="27867-128">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="27867-128">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="27867-129">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="27867-129">Implementations</span></span>

-   [<span data-ttu-id="27867-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="27867-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="27867-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="27867-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="27867-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="27867-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="27867-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="27867-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="27867-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="27867-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="27867-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="27867-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="27867-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27867-136">Windows 2000 Server</span></span>



| <span data-ttu-id="27867-137">Eingabe</span><span class="sxs-lookup"><span data-stu-id="27867-137">Entry</span></span> | <span data-ttu-id="27867-138">Wert</span><span class="sxs-lookup"><span data-stu-id="27867-138">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="27867-139">Link-ID</span><span class="sxs-lookup"><span data-stu-id="27867-139">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="27867-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27867-140">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="27867-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="27867-141">System-Only</span></span>            | <span data-ttu-id="27867-142">False</span><span class="sxs-lookup"><span data-stu-id="27867-142">False</span></span>                                    |
| <span data-ttu-id="27867-143">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="27867-143">Is-Single-Valued</span></span>       | <span data-ttu-id="27867-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="27867-144">True</span></span>                                     |
| <span data-ttu-id="27867-145">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="27867-145">Is Indexed</span></span>             | <span data-ttu-id="27867-146">Richtig</span><span class="sxs-lookup"><span data-stu-id="27867-146">True</span></span>                                     |
| <span data-ttu-id="27867-147">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="27867-147">In Global Catalog</span></span>      | <span data-ttu-id="27867-148">False</span><span class="sxs-lookup"><span data-stu-id="27867-148">False</span></span>                                    |
| <span data-ttu-id="27867-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27867-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="27867-150">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="27867-150">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="27867-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27867-151">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="27867-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27867-152">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="27867-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27867-153">Search-Flags</span></span>           | <span data-ttu-id="27867-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="27867-154">0x00000001</span></span>                               |
| <span data-ttu-id="27867-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27867-155">System-Flags</span></span>           | <span data-ttu-id="27867-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27867-156">0x00000010</span></span>                               |
| <span data-ttu-id="27867-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="27867-157">Classes used in</span></span>        | [<span data-ttu-id="27867-158">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="27867-158">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="27867-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27867-159">Windows Server 2003</span></span>



| <span data-ttu-id="27867-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="27867-160">Entry</span></span> | <span data-ttu-id="27867-161">Wert</span><span class="sxs-lookup"><span data-stu-id="27867-161">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="27867-162">Link-ID</span><span class="sxs-lookup"><span data-stu-id="27867-162">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="27867-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27867-163">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="27867-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="27867-164">System-Only</span></span>            | <span data-ttu-id="27867-165">False</span><span class="sxs-lookup"><span data-stu-id="27867-165">False</span></span>                                    |
| <span data-ttu-id="27867-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="27867-166">Is-Single-Valued</span></span>       | <span data-ttu-id="27867-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="27867-167">True</span></span>                                     |
| <span data-ttu-id="27867-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="27867-168">Is Indexed</span></span>             | <span data-ttu-id="27867-169">Richtig</span><span class="sxs-lookup"><span data-stu-id="27867-169">True</span></span>                                     |
| <span data-ttu-id="27867-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="27867-170">In Global Catalog</span></span>      | <span data-ttu-id="27867-171">False</span><span class="sxs-lookup"><span data-stu-id="27867-171">False</span></span>                                    |
| <span data-ttu-id="27867-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27867-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="27867-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="27867-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="27867-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27867-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="27867-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27867-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="27867-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27867-176">Search-Flags</span></span>           | <span data-ttu-id="27867-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="27867-177">0x00000001</span></span>                               |
| <span data-ttu-id="27867-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27867-178">System-Flags</span></span>           | <span data-ttu-id="27867-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27867-179">0x00000010</span></span>                               |
| <span data-ttu-id="27867-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="27867-180">Classes used in</span></span>        | [<span data-ttu-id="27867-181">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="27867-181">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="27867-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="27867-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="27867-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="27867-183">Entry</span></span> | <span data-ttu-id="27867-184">Wert</span><span class="sxs-lookup"><span data-stu-id="27867-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="27867-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="27867-185">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="27867-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27867-186">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="27867-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="27867-187">System-Only</span></span>            | <span data-ttu-id="27867-188">False</span><span class="sxs-lookup"><span data-stu-id="27867-188">False</span></span>                                    |
| <span data-ttu-id="27867-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="27867-189">Is-Single-Valued</span></span>       | <span data-ttu-id="27867-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="27867-190">True</span></span>                                     |
| <span data-ttu-id="27867-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="27867-191">Is Indexed</span></span>             | <span data-ttu-id="27867-192">Richtig</span><span class="sxs-lookup"><span data-stu-id="27867-192">True</span></span>                                     |
| <span data-ttu-id="27867-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="27867-193">In Global Catalog</span></span>      | <span data-ttu-id="27867-194">False</span><span class="sxs-lookup"><span data-stu-id="27867-194">False</span></span>                                    |
| <span data-ttu-id="27867-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27867-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="27867-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="27867-196">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="27867-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27867-197">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="27867-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27867-198">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="27867-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27867-199">Search-Flags</span></span>           | <span data-ttu-id="27867-200">0x00000001</span><span class="sxs-lookup"><span data-stu-id="27867-200">0x00000001</span></span>                               |
| <span data-ttu-id="27867-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27867-201">System-Flags</span></span>           | <span data-ttu-id="27867-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27867-202">0x00000010</span></span>                               |
| <span data-ttu-id="27867-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="27867-203">Classes used in</span></span>        | [<span data-ttu-id="27867-204">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="27867-204">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="27867-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27867-205">Windows Server 2008</span></span>



| <span data-ttu-id="27867-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="27867-206">Entry</span></span> | <span data-ttu-id="27867-207">Wert</span><span class="sxs-lookup"><span data-stu-id="27867-207">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="27867-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="27867-208">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="27867-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27867-209">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="27867-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="27867-210">System-Only</span></span>            | <span data-ttu-id="27867-211">False</span><span class="sxs-lookup"><span data-stu-id="27867-211">False</span></span>                                    |
| <span data-ttu-id="27867-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="27867-212">Is-Single-Valued</span></span>       | <span data-ttu-id="27867-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="27867-213">True</span></span>                                     |
| <span data-ttu-id="27867-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="27867-214">Is Indexed</span></span>             | <span data-ttu-id="27867-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="27867-215">True</span></span>                                     |
| <span data-ttu-id="27867-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="27867-216">In Global Catalog</span></span>      | <span data-ttu-id="27867-217">False</span><span class="sxs-lookup"><span data-stu-id="27867-217">False</span></span>                                    |
| <span data-ttu-id="27867-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27867-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="27867-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="27867-219">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="27867-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27867-220">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="27867-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27867-221">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="27867-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27867-222">Search-Flags</span></span>           | <span data-ttu-id="27867-223">0x00000001</span><span class="sxs-lookup"><span data-stu-id="27867-223">0x00000001</span></span>                               |
| <span data-ttu-id="27867-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27867-224">System-Flags</span></span>           | <span data-ttu-id="27867-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27867-225">0x00000010</span></span>                               |
| <span data-ttu-id="27867-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="27867-226">Classes used in</span></span>        | [<span data-ttu-id="27867-227">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="27867-227">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="27867-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="27867-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="27867-229">Eingabe</span><span class="sxs-lookup"><span data-stu-id="27867-229">Entry</span></span> | <span data-ttu-id="27867-230">Wert</span><span class="sxs-lookup"><span data-stu-id="27867-230">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="27867-231">Link-ID</span><span class="sxs-lookup"><span data-stu-id="27867-231">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="27867-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27867-232">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="27867-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="27867-233">System-Only</span></span>            | <span data-ttu-id="27867-234">False</span><span class="sxs-lookup"><span data-stu-id="27867-234">False</span></span>                                    |
| <span data-ttu-id="27867-235">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="27867-235">Is-Single-Valued</span></span>       | <span data-ttu-id="27867-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="27867-236">True</span></span>                                     |
| <span data-ttu-id="27867-237">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="27867-237">Is Indexed</span></span>             | <span data-ttu-id="27867-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="27867-238">True</span></span>                                     |
| <span data-ttu-id="27867-239">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="27867-239">In Global Catalog</span></span>      | <span data-ttu-id="27867-240">False</span><span class="sxs-lookup"><span data-stu-id="27867-240">False</span></span>                                    |
| <span data-ttu-id="27867-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27867-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="27867-242">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="27867-242">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="27867-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27867-243">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="27867-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27867-244">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="27867-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27867-245">Search-Flags</span></span>           | <span data-ttu-id="27867-246">0x00000001</span><span class="sxs-lookup"><span data-stu-id="27867-246">0x00000001</span></span>                               |
| <span data-ttu-id="27867-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27867-247">System-Flags</span></span>           | <span data-ttu-id="27867-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27867-248">0x00000010</span></span>                               |
| <span data-ttu-id="27867-249">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="27867-249">Classes used in</span></span>        | [<span data-ttu-id="27867-250">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="27867-250">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="27867-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27867-251">Windows Server 2012</span></span>



| <span data-ttu-id="27867-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="27867-252">Entry</span></span> | <span data-ttu-id="27867-253">Wert</span><span class="sxs-lookup"><span data-stu-id="27867-253">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="27867-254">Link-ID</span><span class="sxs-lookup"><span data-stu-id="27867-254">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="27867-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27867-255">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="27867-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="27867-256">System-Only</span></span>            | <span data-ttu-id="27867-257">False</span><span class="sxs-lookup"><span data-stu-id="27867-257">False</span></span>                                    |
| <span data-ttu-id="27867-258">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="27867-258">Is-Single-Valued</span></span>       | <span data-ttu-id="27867-259">Richtig</span><span class="sxs-lookup"><span data-stu-id="27867-259">True</span></span>                                     |
| <span data-ttu-id="27867-260">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="27867-260">Is Indexed</span></span>             | <span data-ttu-id="27867-261">Richtig</span><span class="sxs-lookup"><span data-stu-id="27867-261">True</span></span>                                     |
| <span data-ttu-id="27867-262">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="27867-262">In Global Catalog</span></span>      | <span data-ttu-id="27867-263">False</span><span class="sxs-lookup"><span data-stu-id="27867-263">False</span></span>                                    |
| <span data-ttu-id="27867-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27867-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="27867-265">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="27867-265">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="27867-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27867-266">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="27867-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27867-267">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="27867-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27867-268">Search-Flags</span></span>           | <span data-ttu-id="27867-269">0x00000001</span><span class="sxs-lookup"><span data-stu-id="27867-269">0x00000001</span></span>                               |
| <span data-ttu-id="27867-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27867-270">System-Flags</span></span>           | <span data-ttu-id="27867-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27867-271">0x00000010</span></span>                               |
| <span data-ttu-id="27867-272">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="27867-272">Classes used in</span></span>        | [<span data-ttu-id="27867-273">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="27867-273">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



 

 





