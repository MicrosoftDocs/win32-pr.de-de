---
title: Options-Location-Attribut
description: Für DHCP enthält der Speicherort der Optionen den DN für alternative Standorte, die die Options Informationen enthalten.
ms.assetid: 2b357733-620f-4ad7-ba69-209095e98aa6
ms.tgt_platform: multiple
keywords:
- AD-Schema für Options-Location-Attribut
- optionslokation-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Options-Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72b33089770d4d9b7cd869cb6375f6224ecd361a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480279"
---
# <a name="options-location-attribute"></a><span data-ttu-id="db3d4-105">Options-Location-Attribut</span><span class="sxs-lookup"><span data-stu-id="db3d4-105">Options-Location attribute</span></span>

<span data-ttu-id="db3d4-106">Für DHCP enthält der Speicherort der Optionen den DN für alternative Standorte, die die Options Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="db3d4-106">For DHCP, the options location contains the DN for alternate sites that contain the options information.</span></span>



| <span data-ttu-id="db3d4-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db3d4-107">Entry</span></span> | <span data-ttu-id="db3d4-108">Wert</span><span class="sxs-lookup"><span data-stu-id="db3d4-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="db3d4-109">CN</span><span class="sxs-lookup"><span data-stu-id="db3d4-109">CN</span></span>                | <span data-ttu-id="db3d4-110">Options-Location</span><span class="sxs-lookup"><span data-stu-id="db3d4-110">Options-Location</span></span>                     |
| <span data-ttu-id="db3d4-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="db3d4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="db3d4-112">optionslokation</span><span class="sxs-lookup"><span data-stu-id="db3d4-112">optionsLocation</span></span>                      |
| <span data-ttu-id="db3d4-113">Size</span><span class="sxs-lookup"><span data-stu-id="db3d4-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="db3d4-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="db3d4-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="db3d4-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="db3d4-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="db3d4-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="db3d4-116">Attribute-Id</span></span>      | <span data-ttu-id="db3d4-117">1.2.840.113556.1.4.713</span><span class="sxs-lookup"><span data-stu-id="db3d4-117">1.2.840.113556.1.4.713</span></span>               |
| <span data-ttu-id="db3d4-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="db3d4-118">System-Id-Guid</span></span>    | <span data-ttu-id="db3d4-119">963d274e-48be-11d1-a9c3-0000 C1</span><span class="sxs-lookup"><span data-stu-id="db3d4-119">963d274e-48be-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="db3d4-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="db3d4-120">Syntax</span></span>            | [<span data-ttu-id="db3d4-121">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="db3d4-121">**String(IA5)**</span></span>](s-string-ia5.md)  |



## <a name="implementations"></a><span data-ttu-id="db3d4-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="db3d4-122">Implementations</span></span>

-   [<span data-ttu-id="db3d4-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="db3d4-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="db3d4-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="db3d4-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="db3d4-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="db3d4-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="db3d4-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="db3d4-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="db3d4-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="db3d4-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="db3d4-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="db3d4-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="db3d4-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="db3d4-129">Windows 2000 Server</span></span>



| <span data-ttu-id="db3d4-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db3d4-130">Entry</span></span> | <span data-ttu-id="db3d4-131">Wert</span><span class="sxs-lookup"><span data-stu-id="db3d4-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="db3d4-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db3d4-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="db3d4-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db3d4-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="db3d4-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="db3d4-134">System-Only</span></span>            | <span data-ttu-id="db3d4-135">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-135">False</span></span>                                        |
| <span data-ttu-id="db3d4-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db3d4-136">Is-Single-Valued</span></span>       | <span data-ttu-id="db3d4-137">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-137">False</span></span>                                        |
| <span data-ttu-id="db3d4-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db3d4-138">Is Indexed</span></span>             | <span data-ttu-id="db3d4-139">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-139">False</span></span>                                        |
| <span data-ttu-id="db3d4-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db3d4-140">In Global Catalog</span></span>      | <span data-ttu-id="db3d4-141">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-141">False</span></span>                                        |
| <span data-ttu-id="db3d4-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db3d4-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="db3d4-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db3d4-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="db3d4-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db3d4-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="db3d4-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db3d4-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="db3d4-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db3d4-146">Search-Flags</span></span>           | <span data-ttu-id="db3d4-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db3d4-147">0x00000000</span></span>                                   |
| <span data-ttu-id="db3d4-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db3d4-148">System-Flags</span></span>           | <span data-ttu-id="db3d4-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db3d4-149">0x00000010</span></span>                                   |
| <span data-ttu-id="db3d4-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db3d4-150">Classes used in</span></span>        | [<span data-ttu-id="db3d4-151">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="db3d4-151">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="db3d4-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="db3d4-152">Windows Server 2003</span></span>



| <span data-ttu-id="db3d4-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db3d4-153">Entry</span></span> | <span data-ttu-id="db3d4-154">Wert</span><span class="sxs-lookup"><span data-stu-id="db3d4-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="db3d4-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db3d4-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="db3d4-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db3d4-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="db3d4-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="db3d4-157">System-Only</span></span>            | <span data-ttu-id="db3d4-158">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-158">False</span></span>                                        |
| <span data-ttu-id="db3d4-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db3d4-159">Is-Single-Valued</span></span>       | <span data-ttu-id="db3d4-160">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-160">False</span></span>                                        |
| <span data-ttu-id="db3d4-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db3d4-161">Is Indexed</span></span>             | <span data-ttu-id="db3d4-162">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-162">False</span></span>                                        |
| <span data-ttu-id="db3d4-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db3d4-163">In Global Catalog</span></span>      | <span data-ttu-id="db3d4-164">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-164">False</span></span>                                        |
| <span data-ttu-id="db3d4-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db3d4-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="db3d4-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db3d4-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="db3d4-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db3d4-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="db3d4-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db3d4-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="db3d4-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db3d4-169">Search-Flags</span></span>           | <span data-ttu-id="db3d4-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db3d4-170">0x00000000</span></span>                                   |
| <span data-ttu-id="db3d4-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db3d4-171">System-Flags</span></span>           | <span data-ttu-id="db3d4-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db3d4-172">0x00000010</span></span>                                   |
| <span data-ttu-id="db3d4-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db3d4-173">Classes used in</span></span>        | [<span data-ttu-id="db3d4-174">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="db3d4-174">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="db3d4-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="db3d4-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="db3d4-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db3d4-176">Entry</span></span> | <span data-ttu-id="db3d4-177">Wert</span><span class="sxs-lookup"><span data-stu-id="db3d4-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="db3d4-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db3d4-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="db3d4-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db3d4-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="db3d4-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="db3d4-180">System-Only</span></span>            | <span data-ttu-id="db3d4-181">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-181">False</span></span>                                        |
| <span data-ttu-id="db3d4-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db3d4-182">Is-Single-Valued</span></span>       | <span data-ttu-id="db3d4-183">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-183">False</span></span>                                        |
| <span data-ttu-id="db3d4-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db3d4-184">Is Indexed</span></span>             | <span data-ttu-id="db3d4-185">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-185">False</span></span>                                        |
| <span data-ttu-id="db3d4-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db3d4-186">In Global Catalog</span></span>      | <span data-ttu-id="db3d4-187">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-187">False</span></span>                                        |
| <span data-ttu-id="db3d4-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db3d4-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="db3d4-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db3d4-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="db3d4-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db3d4-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="db3d4-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db3d4-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="db3d4-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db3d4-192">Search-Flags</span></span>           | <span data-ttu-id="db3d4-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db3d4-193">0x00000000</span></span>                                   |
| <span data-ttu-id="db3d4-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db3d4-194">System-Flags</span></span>           | <span data-ttu-id="db3d4-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db3d4-195">0x00000010</span></span>                                   |
| <span data-ttu-id="db3d4-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db3d4-196">Classes used in</span></span>        | [<span data-ttu-id="db3d4-197">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="db3d4-197">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="db3d4-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db3d4-198">Windows Server 2008</span></span>



| <span data-ttu-id="db3d4-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db3d4-199">Entry</span></span> | <span data-ttu-id="db3d4-200">Wert</span><span class="sxs-lookup"><span data-stu-id="db3d4-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="db3d4-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db3d4-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="db3d4-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db3d4-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="db3d4-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="db3d4-203">System-Only</span></span>            | <span data-ttu-id="db3d4-204">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-204">False</span></span>                                        |
| <span data-ttu-id="db3d4-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db3d4-205">Is-Single-Valued</span></span>       | <span data-ttu-id="db3d4-206">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-206">False</span></span>                                        |
| <span data-ttu-id="db3d4-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db3d4-207">Is Indexed</span></span>             | <span data-ttu-id="db3d4-208">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-208">False</span></span>                                        |
| <span data-ttu-id="db3d4-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db3d4-209">In Global Catalog</span></span>      | <span data-ttu-id="db3d4-210">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-210">False</span></span>                                        |
| <span data-ttu-id="db3d4-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db3d4-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="db3d4-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db3d4-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="db3d4-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db3d4-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="db3d4-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db3d4-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="db3d4-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db3d4-215">Search-Flags</span></span>           | <span data-ttu-id="db3d4-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db3d4-216">0x00000000</span></span>                                   |
| <span data-ttu-id="db3d4-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db3d4-217">System-Flags</span></span>           | <span data-ttu-id="db3d4-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db3d4-218">0x00000010</span></span>                                   |
| <span data-ttu-id="db3d4-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db3d4-219">Classes used in</span></span>        | [<span data-ttu-id="db3d4-220">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="db3d4-220">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="db3d4-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="db3d4-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="db3d4-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db3d4-222">Entry</span></span> | <span data-ttu-id="db3d4-223">Wert</span><span class="sxs-lookup"><span data-stu-id="db3d4-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="db3d4-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db3d4-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="db3d4-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db3d4-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="db3d4-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="db3d4-226">System-Only</span></span>            | <span data-ttu-id="db3d4-227">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-227">False</span></span>                                        |
| <span data-ttu-id="db3d4-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db3d4-228">Is-Single-Valued</span></span>       | <span data-ttu-id="db3d4-229">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-229">False</span></span>                                        |
| <span data-ttu-id="db3d4-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db3d4-230">Is Indexed</span></span>             | <span data-ttu-id="db3d4-231">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-231">False</span></span>                                        |
| <span data-ttu-id="db3d4-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db3d4-232">In Global Catalog</span></span>      | <span data-ttu-id="db3d4-233">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-233">False</span></span>                                        |
| <span data-ttu-id="db3d4-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db3d4-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="db3d4-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db3d4-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="db3d4-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db3d4-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="db3d4-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db3d4-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="db3d4-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db3d4-238">Search-Flags</span></span>           | <span data-ttu-id="db3d4-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db3d4-239">0x00000000</span></span>                                   |
| <span data-ttu-id="db3d4-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db3d4-240">System-Flags</span></span>           | <span data-ttu-id="db3d4-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db3d4-241">0x00000010</span></span>                                   |
| <span data-ttu-id="db3d4-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db3d4-242">Classes used in</span></span>        | [<span data-ttu-id="db3d4-243">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="db3d4-243">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="db3d4-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="db3d4-244">Windows Server 2012</span></span>



| <span data-ttu-id="db3d4-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db3d4-245">Entry</span></span> | <span data-ttu-id="db3d4-246">Wert</span><span class="sxs-lookup"><span data-stu-id="db3d4-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="db3d4-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db3d4-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="db3d4-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db3d4-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="db3d4-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="db3d4-249">System-Only</span></span>            | <span data-ttu-id="db3d4-250">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-250">False</span></span>                                        |
| <span data-ttu-id="db3d4-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db3d4-251">Is-Single-Valued</span></span>       | <span data-ttu-id="db3d4-252">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-252">False</span></span>                                        |
| <span data-ttu-id="db3d4-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db3d4-253">Is Indexed</span></span>             | <span data-ttu-id="db3d4-254">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-254">False</span></span>                                        |
| <span data-ttu-id="db3d4-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db3d4-255">In Global Catalog</span></span>      | <span data-ttu-id="db3d4-256">False</span><span class="sxs-lookup"><span data-stu-id="db3d4-256">False</span></span>                                        |
| <span data-ttu-id="db3d4-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db3d4-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="db3d4-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db3d4-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="db3d4-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db3d4-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="db3d4-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db3d4-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="db3d4-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db3d4-261">Search-Flags</span></span>           | <span data-ttu-id="db3d4-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db3d4-262">0x00000000</span></span>                                   |
| <span data-ttu-id="db3d4-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db3d4-263">System-Flags</span></span>           | <span data-ttu-id="db3d4-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db3d4-264">0x00000010</span></span>                                   |
| <span data-ttu-id="db3d4-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db3d4-265">Classes used in</span></span>        | [<span data-ttu-id="db3d4-266">**DHCP-Klasse**</span><span class="sxs-lookup"><span data-stu-id="db3d4-266">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



 

 





