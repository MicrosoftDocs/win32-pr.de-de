---
title: DHCP-Type-Attribut
description: Der Typ des DHCP-Servers.
ms.assetid: 46ab7db7-a752-45aa-a10b-1195b5cf6f80
ms.tgt_platform: multiple
keywords:
- AD-Schema für DHCP-Type-Attribut
- dhcptype-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- dhcp-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5a5a331ff7298854f4ca070799a05e2a3497f2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957351"
---
# <a name="dhcp-type-attribute"></a><span data-ttu-id="46e50-105">DHCP-Type-Attribut</span><span class="sxs-lookup"><span data-stu-id="46e50-105">dhcp-Type attribute</span></span>

<span data-ttu-id="46e50-106">Der Typ des DHCP-Servers.</span><span class="sxs-lookup"><span data-stu-id="46e50-106">The type of DHCP server.</span></span> <span data-ttu-id="46e50-107">Dieses Attribut wird für alle Objekte von objectClass [**dhcpclass**](c-dhcpclass.md)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="46e50-107">This attribute is set on all objects of objectClass [**dHCPClass**](c-dhcpclass.md).</span></span> <span data-ttu-id="46e50-108">Der zugehörige Wert definiert den Objekttyp:</span><span class="sxs-lookup"><span data-stu-id="46e50-108">Its value defines the type of object:</span></span>

``` syntax
  0 - DHCP Root Object
  1 - DHCP Server
```



| <span data-ttu-id="46e50-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="46e50-109">Entry</span></span> | <span data-ttu-id="46e50-110">Wert</span><span class="sxs-lookup"><span data-stu-id="46e50-110">Value</span></span> |
|-------------------|--------------------------------------------------------|
| <span data-ttu-id="46e50-111">CN</span><span class="sxs-lookup"><span data-stu-id="46e50-111">CN</span></span>                | <span data-ttu-id="46e50-112">DHCP-Typ</span><span class="sxs-lookup"><span data-stu-id="46e50-112">dhcp-Type</span></span>                                              |
| <span data-ttu-id="46e50-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="46e50-113">Ldap-Display-Name</span></span> | <span data-ttu-id="46e50-114">dhcptype</span><span class="sxs-lookup"><span data-stu-id="46e50-114">dhcpType</span></span>                                               |
| <span data-ttu-id="46e50-115">Size</span><span class="sxs-lookup"><span data-stu-id="46e50-115">Size</span></span>              | <span data-ttu-id="46e50-116">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="46e50-116">4 bytes</span></span>                                                |
| <span data-ttu-id="46e50-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="46e50-117">Update Privilege</span></span>  | <span data-ttu-id="46e50-118">Domänen Administrator.</span><span class="sxs-lookup"><span data-stu-id="46e50-118">Domain administrator.</span></span>                                  |
| <span data-ttu-id="46e50-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="46e50-119">Update Frequency</span></span>  | <span data-ttu-id="46e50-120">Wenn ein neuer Server der Gesamtstruktur hinzugefügt oder daraus entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="46e50-120">When a new server is added or removed from the forest.</span></span> |
| <span data-ttu-id="46e50-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="46e50-121">Attribute-Id</span></span>      | <span data-ttu-id="46e50-122">1.2.840.113556.1.4.699</span><span class="sxs-lookup"><span data-stu-id="46e50-122">1.2.840.113556.1.4.699</span></span>                                 |
| <span data-ttu-id="46e50-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="46e50-123">System-Id-Guid</span></span>    | <span data-ttu-id="46e50-124">963d273b-48be-11d1-a9c3-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="46e50-124">963d273b-48be-11d1-a9c3-0000f80367c1</span></span>                   |
| <span data-ttu-id="46e50-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="46e50-125">Syntax</span></span>            | [<span data-ttu-id="46e50-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="46e50-126">**Enumeration**</span></span>](s-enumeration.md)                   |



## <a name="implementations"></a><span data-ttu-id="46e50-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="46e50-127">Implementations</span></span>

-   [<span data-ttu-id="46e50-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="46e50-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="46e50-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="46e50-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="46e50-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="46e50-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="46e50-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="46e50-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="46e50-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="46e50-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="46e50-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="46e50-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="46e50-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="46e50-134">Windows 2000 Server</span></span>



| <span data-ttu-id="46e50-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="46e50-135">Entry</span></span> | <span data-ttu-id="46e50-136">Wert</span><span class="sxs-lookup"><span data-stu-id="46e50-136">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="46e50-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="46e50-137">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="46e50-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46e50-138">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="46e50-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="46e50-139">System-Only</span></span>            | <span data-ttu-id="46e50-140">False</span><span class="sxs-lookup"><span data-stu-id="46e50-140">False</span></span>                                        |
| <span data-ttu-id="46e50-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="46e50-141">Is-Single-Valued</span></span>       | <span data-ttu-id="46e50-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="46e50-142">True</span></span>                                         |
| <span data-ttu-id="46e50-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="46e50-143">Is Indexed</span></span>             | <span data-ttu-id="46e50-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="46e50-144">True</span></span>                                         |
| <span data-ttu-id="46e50-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="46e50-145">In Global Catalog</span></span>      | <span data-ttu-id="46e50-146">False</span><span class="sxs-lookup"><span data-stu-id="46e50-146">False</span></span>                                        |
| <span data-ttu-id="46e50-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="46e50-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="46e50-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="46e50-148">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="46e50-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46e50-149">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="46e50-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46e50-150">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="46e50-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46e50-151">Search-Flags</span></span>           | <span data-ttu-id="46e50-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="46e50-152">0x00000001</span></span>                                   |
| <span data-ttu-id="46e50-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46e50-153">System-Flags</span></span>           | <span data-ttu-id="46e50-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46e50-154">0x00000010</span></span>                                   |
| <span data-ttu-id="46e50-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="46e50-155">Classes used in</span></span>        | [<span data-ttu-id="46e50-156">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="46e50-156">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="46e50-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="46e50-157">Windows Server 2003</span></span>



| <span data-ttu-id="46e50-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="46e50-158">Entry</span></span> | <span data-ttu-id="46e50-159">Wert</span><span class="sxs-lookup"><span data-stu-id="46e50-159">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="46e50-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="46e50-160">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="46e50-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46e50-161">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="46e50-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="46e50-162">System-Only</span></span>            | <span data-ttu-id="46e50-163">False</span><span class="sxs-lookup"><span data-stu-id="46e50-163">False</span></span>                                        |
| <span data-ttu-id="46e50-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="46e50-164">Is-Single-Valued</span></span>       | <span data-ttu-id="46e50-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="46e50-165">True</span></span>                                         |
| <span data-ttu-id="46e50-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="46e50-166">Is Indexed</span></span>             | <span data-ttu-id="46e50-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="46e50-167">True</span></span>                                         |
| <span data-ttu-id="46e50-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="46e50-168">In Global Catalog</span></span>      | <span data-ttu-id="46e50-169">False</span><span class="sxs-lookup"><span data-stu-id="46e50-169">False</span></span>                                        |
| <span data-ttu-id="46e50-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="46e50-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="46e50-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="46e50-171">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="46e50-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46e50-172">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="46e50-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46e50-173">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="46e50-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46e50-174">Search-Flags</span></span>           | <span data-ttu-id="46e50-175">0x00000001</span><span class="sxs-lookup"><span data-stu-id="46e50-175">0x00000001</span></span>                                   |
| <span data-ttu-id="46e50-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46e50-176">System-Flags</span></span>           | <span data-ttu-id="46e50-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46e50-177">0x00000010</span></span>                                   |
| <span data-ttu-id="46e50-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="46e50-178">Classes used in</span></span>        | [<span data-ttu-id="46e50-179">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="46e50-179">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="46e50-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="46e50-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="46e50-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="46e50-181">Entry</span></span> | <span data-ttu-id="46e50-182">Wert</span><span class="sxs-lookup"><span data-stu-id="46e50-182">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="46e50-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="46e50-183">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="46e50-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46e50-184">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="46e50-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="46e50-185">System-Only</span></span>            | <span data-ttu-id="46e50-186">False</span><span class="sxs-lookup"><span data-stu-id="46e50-186">False</span></span>                                        |
| <span data-ttu-id="46e50-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="46e50-187">Is-Single-Valued</span></span>       | <span data-ttu-id="46e50-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="46e50-188">True</span></span>                                         |
| <span data-ttu-id="46e50-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="46e50-189">Is Indexed</span></span>             | <span data-ttu-id="46e50-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="46e50-190">True</span></span>                                         |
| <span data-ttu-id="46e50-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="46e50-191">In Global Catalog</span></span>      | <span data-ttu-id="46e50-192">False</span><span class="sxs-lookup"><span data-stu-id="46e50-192">False</span></span>                                        |
| <span data-ttu-id="46e50-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="46e50-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="46e50-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="46e50-194">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="46e50-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46e50-195">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="46e50-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46e50-196">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="46e50-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46e50-197">Search-Flags</span></span>           | <span data-ttu-id="46e50-198">0x00000001</span><span class="sxs-lookup"><span data-stu-id="46e50-198">0x00000001</span></span>                                   |
| <span data-ttu-id="46e50-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46e50-199">System-Flags</span></span>           | <span data-ttu-id="46e50-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46e50-200">0x00000010</span></span>                                   |
| <span data-ttu-id="46e50-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="46e50-201">Classes used in</span></span>        | [<span data-ttu-id="46e50-202">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="46e50-202">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="46e50-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46e50-203">Windows Server 2008</span></span>



| <span data-ttu-id="46e50-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="46e50-204">Entry</span></span> | <span data-ttu-id="46e50-205">Wert</span><span class="sxs-lookup"><span data-stu-id="46e50-205">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="46e50-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="46e50-206">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="46e50-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46e50-207">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="46e50-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="46e50-208">System-Only</span></span>            | <span data-ttu-id="46e50-209">False</span><span class="sxs-lookup"><span data-stu-id="46e50-209">False</span></span>                                        |
| <span data-ttu-id="46e50-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="46e50-210">Is-Single-Valued</span></span>       | <span data-ttu-id="46e50-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="46e50-211">True</span></span>                                         |
| <span data-ttu-id="46e50-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="46e50-212">Is Indexed</span></span>             | <span data-ttu-id="46e50-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="46e50-213">True</span></span>                                         |
| <span data-ttu-id="46e50-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="46e50-214">In Global Catalog</span></span>      | <span data-ttu-id="46e50-215">False</span><span class="sxs-lookup"><span data-stu-id="46e50-215">False</span></span>                                        |
| <span data-ttu-id="46e50-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="46e50-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="46e50-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="46e50-217">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="46e50-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46e50-218">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="46e50-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46e50-219">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="46e50-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46e50-220">Search-Flags</span></span>           | <span data-ttu-id="46e50-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="46e50-221">0x00000001</span></span>                                   |
| <span data-ttu-id="46e50-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46e50-222">System-Flags</span></span>           | <span data-ttu-id="46e50-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46e50-223">0x00000010</span></span>                                   |
| <span data-ttu-id="46e50-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="46e50-224">Classes used in</span></span>        | [<span data-ttu-id="46e50-225">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="46e50-225">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="46e50-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="46e50-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="46e50-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="46e50-227">Entry</span></span> | <span data-ttu-id="46e50-228">Wert</span><span class="sxs-lookup"><span data-stu-id="46e50-228">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="46e50-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="46e50-229">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="46e50-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46e50-230">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="46e50-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="46e50-231">System-Only</span></span>            | <span data-ttu-id="46e50-232">False</span><span class="sxs-lookup"><span data-stu-id="46e50-232">False</span></span>                                        |
| <span data-ttu-id="46e50-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="46e50-233">Is-Single-Valued</span></span>       | <span data-ttu-id="46e50-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="46e50-234">True</span></span>                                         |
| <span data-ttu-id="46e50-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="46e50-235">Is Indexed</span></span>             | <span data-ttu-id="46e50-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="46e50-236">True</span></span>                                         |
| <span data-ttu-id="46e50-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="46e50-237">In Global Catalog</span></span>      | <span data-ttu-id="46e50-238">False</span><span class="sxs-lookup"><span data-stu-id="46e50-238">False</span></span>                                        |
| <span data-ttu-id="46e50-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="46e50-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="46e50-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="46e50-240">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="46e50-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46e50-241">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="46e50-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46e50-242">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="46e50-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46e50-243">Search-Flags</span></span>           | <span data-ttu-id="46e50-244">0x00000001</span><span class="sxs-lookup"><span data-stu-id="46e50-244">0x00000001</span></span>                                   |
| <span data-ttu-id="46e50-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46e50-245">System-Flags</span></span>           | <span data-ttu-id="46e50-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46e50-246">0x00000010</span></span>                                   |
| <span data-ttu-id="46e50-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="46e50-247">Classes used in</span></span>        | [<span data-ttu-id="46e50-248">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="46e50-248">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="46e50-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="46e50-249">Windows Server 2012</span></span>



| <span data-ttu-id="46e50-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="46e50-250">Entry</span></span> | <span data-ttu-id="46e50-251">Wert</span><span class="sxs-lookup"><span data-stu-id="46e50-251">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="46e50-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="46e50-252">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="46e50-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46e50-253">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="46e50-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="46e50-254">System-Only</span></span>            | <span data-ttu-id="46e50-255">False</span><span class="sxs-lookup"><span data-stu-id="46e50-255">False</span></span>                                        |
| <span data-ttu-id="46e50-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="46e50-256">Is-Single-Valued</span></span>       | <span data-ttu-id="46e50-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="46e50-257">True</span></span>                                         |
| <span data-ttu-id="46e50-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="46e50-258">Is Indexed</span></span>             | <span data-ttu-id="46e50-259">Richtig</span><span class="sxs-lookup"><span data-stu-id="46e50-259">True</span></span>                                         |
| <span data-ttu-id="46e50-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="46e50-260">In Global Catalog</span></span>      | <span data-ttu-id="46e50-261">False</span><span class="sxs-lookup"><span data-stu-id="46e50-261">False</span></span>                                        |
| <span data-ttu-id="46e50-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="46e50-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="46e50-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="46e50-263">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="46e50-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46e50-264">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="46e50-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46e50-265">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="46e50-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46e50-266">Search-Flags</span></span>           | <span data-ttu-id="46e50-267">0x00000001</span><span class="sxs-lookup"><span data-stu-id="46e50-267">0x00000001</span></span>                                   |
| <span data-ttu-id="46e50-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46e50-268">System-Flags</span></span>           | <span data-ttu-id="46e50-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46e50-269">0x00000010</span></span>                                   |
| <span data-ttu-id="46e50-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="46e50-270">Classes used in</span></span>        | [<span data-ttu-id="46e50-271">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="46e50-271">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



 

 





