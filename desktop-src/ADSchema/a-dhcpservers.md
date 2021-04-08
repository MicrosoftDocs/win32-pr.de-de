---
title: DHCP-Server-Attribut
description: Enthält eine Liste von Servern, die im Unternehmen autorisiert sind.
ms.assetid: f712b2d2-ff9c-4ee2-aede-b68023e3e6b6
ms.tgt_platform: multiple
keywords:
- AD-Schema für DHCP-Server-Attribut
- dhcpservers-Attribut AD-Schema
topic_type:
- apiref
api_name:
- dhcp-Servers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e43018c91e5bb495ee39476f07f40756cfcf097
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957353"
---
# <a name="dhcp-servers-attribute"></a><span data-ttu-id="dbd96-105">DHCP-Server-Attribut</span><span class="sxs-lookup"><span data-stu-id="dbd96-105">dhcp-Servers attribute</span></span>

<span data-ttu-id="dbd96-106">Enthält eine Liste von Servern, die im Unternehmen autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="dbd96-106">Contains a list of servers that are authorized in the enterprise.</span></span>



| <span data-ttu-id="dbd96-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dbd96-107">Entry</span></span> | <span data-ttu-id="dbd96-108">Wert</span><span class="sxs-lookup"><span data-stu-id="dbd96-108">Value</span></span> |
|-------------------|--------------------------------------------------------|
| <span data-ttu-id="dbd96-109">CN</span><span class="sxs-lookup"><span data-stu-id="dbd96-109">CN</span></span>                | <span data-ttu-id="dbd96-110">DHCP-Server</span><span class="sxs-lookup"><span data-stu-id="dbd96-110">dhcp-Servers</span></span>                                           |
| <span data-ttu-id="dbd96-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="dbd96-111">Ldap-Display-Name</span></span> | <span data-ttu-id="dbd96-112">Gruppe dhcpservers gespeicherte</span><span class="sxs-lookup"><span data-stu-id="dbd96-112">dhcpServers</span></span>                                            |
| <span data-ttu-id="dbd96-113">Size</span><span class="sxs-lookup"><span data-stu-id="dbd96-113">Size</span></span>              | \-                                                     |
| <span data-ttu-id="dbd96-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="dbd96-114">Update Privilege</span></span>  | <span data-ttu-id="dbd96-115">Domänen Administrator.</span><span class="sxs-lookup"><span data-stu-id="dbd96-115">Domain administrator.</span></span>                                  |
| <span data-ttu-id="dbd96-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="dbd96-116">Update Frequency</span></span>  | <span data-ttu-id="dbd96-117">Wenn ein neuer Server der Gesamtstruktur hinzugefügt oder daraus entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="dbd96-117">When a new server is added or removed from the forest.</span></span> |
| <span data-ttu-id="dbd96-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dbd96-118">Attribute-Id</span></span>      | <span data-ttu-id="dbd96-119">1.2.840.113556.1.4.704</span><span class="sxs-lookup"><span data-stu-id="dbd96-119">1.2.840.113556.1.4.704</span></span>                                 |
| <span data-ttu-id="dbd96-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dbd96-120">System-Id-Guid</span></span>    | <span data-ttu-id="dbd96-121">963d2745-48be-11d1-a9c3-0000 C1</span><span class="sxs-lookup"><span data-stu-id="dbd96-121">963d2745-48be-11d1-a9c3-0000f80367c1</span></span>                   |
| <span data-ttu-id="dbd96-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbd96-122">Syntax</span></span>            | [<span data-ttu-id="dbd96-123">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="dbd96-123">**String(IA5)**</span></span>](s-string-ia5.md)                    |



## <a name="implementations"></a><span data-ttu-id="dbd96-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="dbd96-124">Implementations</span></span>

-   [<span data-ttu-id="dbd96-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dbd96-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dbd96-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dbd96-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dbd96-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dbd96-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dbd96-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dbd96-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dbd96-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dbd96-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dbd96-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dbd96-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dbd96-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dbd96-131">Windows 2000 Server</span></span>



| <span data-ttu-id="dbd96-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dbd96-132">Entry</span></span> | <span data-ttu-id="dbd96-133">Wert</span><span class="sxs-lookup"><span data-stu-id="dbd96-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dbd96-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dbd96-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dbd96-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbd96-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dbd96-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbd96-136">System-Only</span></span>            | <span data-ttu-id="dbd96-137">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-137">False</span></span>                                        |
| <span data-ttu-id="dbd96-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dbd96-138">Is-Single-Valued</span></span>       | <span data-ttu-id="dbd96-139">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-139">False</span></span>                                        |
| <span data-ttu-id="dbd96-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dbd96-140">Is Indexed</span></span>             | <span data-ttu-id="dbd96-141">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-141">False</span></span>                                        |
| <span data-ttu-id="dbd96-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dbd96-142">In Global Catalog</span></span>      | <span data-ttu-id="dbd96-143">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-143">False</span></span>                                        |
| <span data-ttu-id="dbd96-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dbd96-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbd96-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dbd96-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dbd96-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbd96-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dbd96-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbd96-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dbd96-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbd96-148">Search-Flags</span></span>           | <span data-ttu-id="dbd96-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbd96-149">0x00000000</span></span>                                   |
| <span data-ttu-id="dbd96-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbd96-150">System-Flags</span></span>           | <span data-ttu-id="dbd96-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dbd96-151">0x00000010</span></span>                                   |
| <span data-ttu-id="dbd96-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dbd96-152">Classes used in</span></span>        | [<span data-ttu-id="dbd96-153">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="dbd96-153">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dbd96-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dbd96-154">Windows Server 2003</span></span>



| <span data-ttu-id="dbd96-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dbd96-155">Entry</span></span> | <span data-ttu-id="dbd96-156">Wert</span><span class="sxs-lookup"><span data-stu-id="dbd96-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dbd96-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dbd96-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dbd96-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbd96-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dbd96-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbd96-159">System-Only</span></span>            | <span data-ttu-id="dbd96-160">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-160">False</span></span>                                        |
| <span data-ttu-id="dbd96-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dbd96-161">Is-Single-Valued</span></span>       | <span data-ttu-id="dbd96-162">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-162">False</span></span>                                        |
| <span data-ttu-id="dbd96-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dbd96-163">Is Indexed</span></span>             | <span data-ttu-id="dbd96-164">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-164">False</span></span>                                        |
| <span data-ttu-id="dbd96-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dbd96-165">In Global Catalog</span></span>      | <span data-ttu-id="dbd96-166">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-166">False</span></span>                                        |
| <span data-ttu-id="dbd96-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dbd96-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbd96-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dbd96-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dbd96-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbd96-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dbd96-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbd96-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dbd96-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbd96-171">Search-Flags</span></span>           | <span data-ttu-id="dbd96-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbd96-172">0x00000000</span></span>                                   |
| <span data-ttu-id="dbd96-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbd96-173">System-Flags</span></span>           | <span data-ttu-id="dbd96-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dbd96-174">0x00000010</span></span>                                   |
| <span data-ttu-id="dbd96-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dbd96-175">Classes used in</span></span>        | [<span data-ttu-id="dbd96-176">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="dbd96-176">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dbd96-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dbd96-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dbd96-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dbd96-178">Entry</span></span> | <span data-ttu-id="dbd96-179">Wert</span><span class="sxs-lookup"><span data-stu-id="dbd96-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dbd96-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dbd96-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dbd96-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbd96-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dbd96-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbd96-182">System-Only</span></span>            | <span data-ttu-id="dbd96-183">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-183">False</span></span>                                        |
| <span data-ttu-id="dbd96-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dbd96-184">Is-Single-Valued</span></span>       | <span data-ttu-id="dbd96-185">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-185">False</span></span>                                        |
| <span data-ttu-id="dbd96-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dbd96-186">Is Indexed</span></span>             | <span data-ttu-id="dbd96-187">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-187">False</span></span>                                        |
| <span data-ttu-id="dbd96-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dbd96-188">In Global Catalog</span></span>      | <span data-ttu-id="dbd96-189">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-189">False</span></span>                                        |
| <span data-ttu-id="dbd96-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dbd96-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbd96-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dbd96-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dbd96-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbd96-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dbd96-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbd96-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dbd96-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbd96-194">Search-Flags</span></span>           | <span data-ttu-id="dbd96-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbd96-195">0x00000000</span></span>                                   |
| <span data-ttu-id="dbd96-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbd96-196">System-Flags</span></span>           | <span data-ttu-id="dbd96-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dbd96-197">0x00000010</span></span>                                   |
| <span data-ttu-id="dbd96-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dbd96-198">Classes used in</span></span>        | [<span data-ttu-id="dbd96-199">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="dbd96-199">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dbd96-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbd96-200">Windows Server 2008</span></span>



| <span data-ttu-id="dbd96-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dbd96-201">Entry</span></span> | <span data-ttu-id="dbd96-202">Wert</span><span class="sxs-lookup"><span data-stu-id="dbd96-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dbd96-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dbd96-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dbd96-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbd96-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dbd96-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbd96-205">System-Only</span></span>            | <span data-ttu-id="dbd96-206">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-206">False</span></span>                                        |
| <span data-ttu-id="dbd96-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dbd96-207">Is-Single-Valued</span></span>       | <span data-ttu-id="dbd96-208">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-208">False</span></span>                                        |
| <span data-ttu-id="dbd96-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dbd96-209">Is Indexed</span></span>             | <span data-ttu-id="dbd96-210">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-210">False</span></span>                                        |
| <span data-ttu-id="dbd96-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dbd96-211">In Global Catalog</span></span>      | <span data-ttu-id="dbd96-212">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-212">False</span></span>                                        |
| <span data-ttu-id="dbd96-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dbd96-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbd96-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dbd96-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dbd96-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbd96-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dbd96-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbd96-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dbd96-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbd96-217">Search-Flags</span></span>           | <span data-ttu-id="dbd96-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbd96-218">0x00000000</span></span>                                   |
| <span data-ttu-id="dbd96-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbd96-219">System-Flags</span></span>           | <span data-ttu-id="dbd96-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dbd96-220">0x00000010</span></span>                                   |
| <span data-ttu-id="dbd96-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dbd96-221">Classes used in</span></span>        | [<span data-ttu-id="dbd96-222">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="dbd96-222">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dbd96-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dbd96-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dbd96-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dbd96-224">Entry</span></span> | <span data-ttu-id="dbd96-225">Wert</span><span class="sxs-lookup"><span data-stu-id="dbd96-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dbd96-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dbd96-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dbd96-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbd96-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dbd96-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbd96-228">System-Only</span></span>            | <span data-ttu-id="dbd96-229">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-229">False</span></span>                                        |
| <span data-ttu-id="dbd96-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dbd96-230">Is-Single-Valued</span></span>       | <span data-ttu-id="dbd96-231">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-231">False</span></span>                                        |
| <span data-ttu-id="dbd96-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dbd96-232">Is Indexed</span></span>             | <span data-ttu-id="dbd96-233">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-233">False</span></span>                                        |
| <span data-ttu-id="dbd96-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dbd96-234">In Global Catalog</span></span>      | <span data-ttu-id="dbd96-235">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-235">False</span></span>                                        |
| <span data-ttu-id="dbd96-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dbd96-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbd96-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dbd96-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dbd96-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbd96-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dbd96-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbd96-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dbd96-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbd96-240">Search-Flags</span></span>           | <span data-ttu-id="dbd96-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbd96-241">0x00000000</span></span>                                   |
| <span data-ttu-id="dbd96-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbd96-242">System-Flags</span></span>           | <span data-ttu-id="dbd96-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dbd96-243">0x00000010</span></span>                                   |
| <span data-ttu-id="dbd96-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dbd96-244">Classes used in</span></span>        | [<span data-ttu-id="dbd96-245">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="dbd96-245">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dbd96-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dbd96-246">Windows Server 2012</span></span>



| <span data-ttu-id="dbd96-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dbd96-247">Entry</span></span> | <span data-ttu-id="dbd96-248">Wert</span><span class="sxs-lookup"><span data-stu-id="dbd96-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dbd96-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dbd96-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dbd96-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbd96-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dbd96-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbd96-251">System-Only</span></span>            | <span data-ttu-id="dbd96-252">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-252">False</span></span>                                        |
| <span data-ttu-id="dbd96-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dbd96-253">Is-Single-Valued</span></span>       | <span data-ttu-id="dbd96-254">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-254">False</span></span>                                        |
| <span data-ttu-id="dbd96-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dbd96-255">Is Indexed</span></span>             | <span data-ttu-id="dbd96-256">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-256">False</span></span>                                        |
| <span data-ttu-id="dbd96-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dbd96-257">In Global Catalog</span></span>      | <span data-ttu-id="dbd96-258">False</span><span class="sxs-lookup"><span data-stu-id="dbd96-258">False</span></span>                                        |
| <span data-ttu-id="dbd96-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dbd96-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbd96-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dbd96-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dbd96-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbd96-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dbd96-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbd96-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dbd96-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbd96-263">Search-Flags</span></span>           | <span data-ttu-id="dbd96-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbd96-264">0x00000000</span></span>                                   |
| <span data-ttu-id="dbd96-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbd96-265">System-Flags</span></span>           | <span data-ttu-id="dbd96-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dbd96-266">0x00000010</span></span>                                   |
| <span data-ttu-id="dbd96-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dbd96-267">Classes used in</span></span>        | [<span data-ttu-id="dbd96-268">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="dbd96-268">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



 

 





