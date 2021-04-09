---
title: NetBoot-GUID-Attribut
description: Starten Sie einen Computer mit der on-Board-GUID eines Computers. Entspricht der Mac-Adresse für die Netzwerkkarte des Computers.
ms.assetid: 60ce0482-79a3-499a-9607-f1f496e297d0
ms.tgt_platform: multiple
keywords:
- NetBoot-GUID-Attribut, AD-Schema
- netbootguid-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Netboot-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7c09d6f9139580ad329b47f13999d348abf5a87
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859801"
---
# <a name="netboot-guid-attribute"></a><span data-ttu-id="faaea-106">NetBoot-GUID-Attribut</span><span class="sxs-lookup"><span data-stu-id="faaea-106">Netboot-GUID attribute</span></span>

<span data-ttu-id="faaea-107">Start ohne Datenträger: die on-Board-GUID eines Computers.</span><span class="sxs-lookup"><span data-stu-id="faaea-107">Diskless boot: A computer's on-board GUID.</span></span> <span data-ttu-id="faaea-108">Entspricht der Mac-Adresse für die Netzwerkkarte des Computers.</span><span class="sxs-lookup"><span data-stu-id="faaea-108">Corresponds to the computer's network card MAC address.</span></span>



| <span data-ttu-id="faaea-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="faaea-109">Entry</span></span> | <span data-ttu-id="faaea-110">Wert</span><span class="sxs-lookup"><span data-stu-id="faaea-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="faaea-111">CN</span><span class="sxs-lookup"><span data-stu-id="faaea-111">CN</span></span>                | <span data-ttu-id="faaea-112">NetBoot-GUID</span><span class="sxs-lookup"><span data-stu-id="faaea-112">Netboot-GUID</span></span>                                          |
| <span data-ttu-id="faaea-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="faaea-113">Ldap-Display-Name</span></span> | <span data-ttu-id="faaea-114">netbootguid</span><span class="sxs-lookup"><span data-stu-id="faaea-114">netbootGUID</span></span>                                           |
| <span data-ttu-id="faaea-115">Size</span><span class="sxs-lookup"><span data-stu-id="faaea-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="faaea-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="faaea-116">Update Privilege</span></span>  | <span data-ttu-id="faaea-117">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="faaea-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="faaea-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="faaea-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="faaea-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="faaea-119">Attribute-Id</span></span>      | <span data-ttu-id="faaea-120">1.2.840.113556.1.4.359</span><span class="sxs-lookup"><span data-stu-id="faaea-120">1.2.840.113556.1.4.359</span></span>                                |
| <span data-ttu-id="faaea-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="faaea-121">System-Id-Guid</span></span>    | <span data-ttu-id="faaea-122">3e978921-8c01-11D0-AFDA-00c04f 930c9</span><span class="sxs-lookup"><span data-stu-id="faaea-122">3e978921-8c01-11d0-afda-00c04fd930c9</span></span>                  |
| <span data-ttu-id="faaea-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="faaea-123">Syntax</span></span>            | [<span data-ttu-id="faaea-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="faaea-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="faaea-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="faaea-125">Implementations</span></span>

-   [<span data-ttu-id="faaea-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="faaea-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="faaea-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="faaea-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="faaea-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="faaea-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="faaea-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="faaea-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="faaea-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="faaea-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="faaea-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="faaea-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="faaea-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="faaea-132">Windows 2000 Server</span></span>



| <span data-ttu-id="faaea-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="faaea-133">Entry</span></span> | <span data-ttu-id="faaea-134">Wert</span><span class="sxs-lookup"><span data-stu-id="faaea-134">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="faaea-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="faaea-135">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="faaea-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="faaea-136">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="faaea-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="faaea-137">System-Only</span></span>            | <span data-ttu-id="faaea-138">False</span><span class="sxs-lookup"><span data-stu-id="faaea-138">False</span></span>                                     |
| <span data-ttu-id="faaea-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="faaea-139">Is-Single-Valued</span></span>       | <span data-ttu-id="faaea-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-140">True</span></span>                                      |
| <span data-ttu-id="faaea-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="faaea-141">Is Indexed</span></span>             | <span data-ttu-id="faaea-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-142">True</span></span>                                      |
| <span data-ttu-id="faaea-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="faaea-143">In Global Catalog</span></span>      | <span data-ttu-id="faaea-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-144">True</span></span>                                      |
| <span data-ttu-id="faaea-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="faaea-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="faaea-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="faaea-146">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="faaea-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="faaea-147">Range-Lower</span></span>            | <span data-ttu-id="faaea-148">16</span><span class="sxs-lookup"><span data-stu-id="faaea-148">16</span></span>                                        |
| <span data-ttu-id="faaea-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="faaea-149">Range-Upper</span></span>            | <span data-ttu-id="faaea-150">16</span><span class="sxs-lookup"><span data-stu-id="faaea-150">16</span></span>                                        |
| <span data-ttu-id="faaea-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="faaea-151">Search-Flags</span></span>           | <span data-ttu-id="faaea-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="faaea-152">0x00000001</span></span>                                |
| <span data-ttu-id="faaea-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="faaea-153">System-Flags</span></span>           | <span data-ttu-id="faaea-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="faaea-154">0x00000010</span></span>                                |
| <span data-ttu-id="faaea-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="faaea-155">Classes used in</span></span>        | [<span data-ttu-id="faaea-156">**Computer**</span><span class="sxs-lookup"><span data-stu-id="faaea-156">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="faaea-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="faaea-157">Windows Server 2003</span></span>



| <span data-ttu-id="faaea-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="faaea-158">Entry</span></span> | <span data-ttu-id="faaea-159">Wert</span><span class="sxs-lookup"><span data-stu-id="faaea-159">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="faaea-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="faaea-160">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="faaea-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="faaea-161">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="faaea-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="faaea-162">System-Only</span></span>            | <span data-ttu-id="faaea-163">False</span><span class="sxs-lookup"><span data-stu-id="faaea-163">False</span></span>                                     |
| <span data-ttu-id="faaea-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="faaea-164">Is-Single-Valued</span></span>       | <span data-ttu-id="faaea-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-165">True</span></span>                                      |
| <span data-ttu-id="faaea-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="faaea-166">Is Indexed</span></span>             | <span data-ttu-id="faaea-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-167">True</span></span>                                      |
| <span data-ttu-id="faaea-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="faaea-168">In Global Catalog</span></span>      | <span data-ttu-id="faaea-169">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-169">True</span></span>                                      |
| <span data-ttu-id="faaea-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="faaea-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="faaea-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="faaea-171">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="faaea-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="faaea-172">Range-Lower</span></span>            | <span data-ttu-id="faaea-173">16</span><span class="sxs-lookup"><span data-stu-id="faaea-173">16</span></span>                                        |
| <span data-ttu-id="faaea-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="faaea-174">Range-Upper</span></span>            | <span data-ttu-id="faaea-175">16</span><span class="sxs-lookup"><span data-stu-id="faaea-175">16</span></span>                                        |
| <span data-ttu-id="faaea-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="faaea-176">Search-Flags</span></span>           | <span data-ttu-id="faaea-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="faaea-177">0x00000001</span></span>                                |
| <span data-ttu-id="faaea-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="faaea-178">System-Flags</span></span>           | <span data-ttu-id="faaea-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="faaea-179">0x00000010</span></span>                                |
| <span data-ttu-id="faaea-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="faaea-180">Classes used in</span></span>        | [<span data-ttu-id="faaea-181">**Computer**</span><span class="sxs-lookup"><span data-stu-id="faaea-181">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="faaea-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="faaea-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="faaea-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="faaea-183">Entry</span></span> | <span data-ttu-id="faaea-184">Wert</span><span class="sxs-lookup"><span data-stu-id="faaea-184">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="faaea-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="faaea-185">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="faaea-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="faaea-186">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="faaea-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="faaea-187">System-Only</span></span>            | <span data-ttu-id="faaea-188">False</span><span class="sxs-lookup"><span data-stu-id="faaea-188">False</span></span>                                     |
| <span data-ttu-id="faaea-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="faaea-189">Is-Single-Valued</span></span>       | <span data-ttu-id="faaea-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-190">True</span></span>                                      |
| <span data-ttu-id="faaea-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="faaea-191">Is Indexed</span></span>             | <span data-ttu-id="faaea-192">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-192">True</span></span>                                      |
| <span data-ttu-id="faaea-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="faaea-193">In Global Catalog</span></span>      | <span data-ttu-id="faaea-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-194">True</span></span>                                      |
| <span data-ttu-id="faaea-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="faaea-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="faaea-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="faaea-196">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="faaea-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="faaea-197">Range-Lower</span></span>            | <span data-ttu-id="faaea-198">16</span><span class="sxs-lookup"><span data-stu-id="faaea-198">16</span></span>                                        |
| <span data-ttu-id="faaea-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="faaea-199">Range-Upper</span></span>            | <span data-ttu-id="faaea-200">16</span><span class="sxs-lookup"><span data-stu-id="faaea-200">16</span></span>                                        |
| <span data-ttu-id="faaea-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="faaea-201">Search-Flags</span></span>           | <span data-ttu-id="faaea-202">0x00000001</span><span class="sxs-lookup"><span data-stu-id="faaea-202">0x00000001</span></span>                                |
| <span data-ttu-id="faaea-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="faaea-203">System-Flags</span></span>           | <span data-ttu-id="faaea-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="faaea-204">0x00000010</span></span>                                |
| <span data-ttu-id="faaea-205">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="faaea-205">Classes used in</span></span>        | [<span data-ttu-id="faaea-206">**Computer**</span><span class="sxs-lookup"><span data-stu-id="faaea-206">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="faaea-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="faaea-207">Windows Server 2008</span></span>



| <span data-ttu-id="faaea-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="faaea-208">Entry</span></span> | <span data-ttu-id="faaea-209">Wert</span><span class="sxs-lookup"><span data-stu-id="faaea-209">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="faaea-210">Link-ID</span><span class="sxs-lookup"><span data-stu-id="faaea-210">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="faaea-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="faaea-211">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="faaea-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="faaea-212">System-Only</span></span>            | <span data-ttu-id="faaea-213">False</span><span class="sxs-lookup"><span data-stu-id="faaea-213">False</span></span>                                     |
| <span data-ttu-id="faaea-214">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="faaea-214">Is-Single-Valued</span></span>       | <span data-ttu-id="faaea-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-215">True</span></span>                                      |
| <span data-ttu-id="faaea-216">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="faaea-216">Is Indexed</span></span>             | <span data-ttu-id="faaea-217">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-217">True</span></span>                                      |
| <span data-ttu-id="faaea-218">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="faaea-218">In Global Catalog</span></span>      | <span data-ttu-id="faaea-219">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-219">True</span></span>                                      |
| <span data-ttu-id="faaea-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="faaea-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="faaea-221">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="faaea-221">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="faaea-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="faaea-222">Range-Lower</span></span>            | <span data-ttu-id="faaea-223">16</span><span class="sxs-lookup"><span data-stu-id="faaea-223">16</span></span>                                        |
| <span data-ttu-id="faaea-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="faaea-224">Range-Upper</span></span>            | <span data-ttu-id="faaea-225">16</span><span class="sxs-lookup"><span data-stu-id="faaea-225">16</span></span>                                        |
| <span data-ttu-id="faaea-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="faaea-226">Search-Flags</span></span>           | <span data-ttu-id="faaea-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="faaea-227">0x00000001</span></span>                                |
| <span data-ttu-id="faaea-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="faaea-228">System-Flags</span></span>           | <span data-ttu-id="faaea-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="faaea-229">0x00000010</span></span>                                |
| <span data-ttu-id="faaea-230">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="faaea-230">Classes used in</span></span>        | [<span data-ttu-id="faaea-231">**Computer**</span><span class="sxs-lookup"><span data-stu-id="faaea-231">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="faaea-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="faaea-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="faaea-233">Eingabe</span><span class="sxs-lookup"><span data-stu-id="faaea-233">Entry</span></span> | <span data-ttu-id="faaea-234">Wert</span><span class="sxs-lookup"><span data-stu-id="faaea-234">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="faaea-235">Link-ID</span><span class="sxs-lookup"><span data-stu-id="faaea-235">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="faaea-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="faaea-236">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="faaea-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="faaea-237">System-Only</span></span>            | <span data-ttu-id="faaea-238">False</span><span class="sxs-lookup"><span data-stu-id="faaea-238">False</span></span>                                     |
| <span data-ttu-id="faaea-239">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="faaea-239">Is-Single-Valued</span></span>       | <span data-ttu-id="faaea-240">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-240">True</span></span>                                      |
| <span data-ttu-id="faaea-241">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="faaea-241">Is Indexed</span></span>             | <span data-ttu-id="faaea-242">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-242">True</span></span>                                      |
| <span data-ttu-id="faaea-243">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="faaea-243">In Global Catalog</span></span>      | <span data-ttu-id="faaea-244">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-244">True</span></span>                                      |
| <span data-ttu-id="faaea-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="faaea-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="faaea-246">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="faaea-246">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="faaea-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="faaea-247">Range-Lower</span></span>            | <span data-ttu-id="faaea-248">16</span><span class="sxs-lookup"><span data-stu-id="faaea-248">16</span></span>                                        |
| <span data-ttu-id="faaea-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="faaea-249">Range-Upper</span></span>            | <span data-ttu-id="faaea-250">16</span><span class="sxs-lookup"><span data-stu-id="faaea-250">16</span></span>                                        |
| <span data-ttu-id="faaea-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="faaea-251">Search-Flags</span></span>           | <span data-ttu-id="faaea-252">0x00000001</span><span class="sxs-lookup"><span data-stu-id="faaea-252">0x00000001</span></span>                                |
| <span data-ttu-id="faaea-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="faaea-253">System-Flags</span></span>           | <span data-ttu-id="faaea-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="faaea-254">0x00000010</span></span>                                |
| <span data-ttu-id="faaea-255">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="faaea-255">Classes used in</span></span>        | [<span data-ttu-id="faaea-256">**Computer**</span><span class="sxs-lookup"><span data-stu-id="faaea-256">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="faaea-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="faaea-257">Windows Server 2012</span></span>



| <span data-ttu-id="faaea-258">Eingabe</span><span class="sxs-lookup"><span data-stu-id="faaea-258">Entry</span></span> | <span data-ttu-id="faaea-259">Wert</span><span class="sxs-lookup"><span data-stu-id="faaea-259">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="faaea-260">Link-ID</span><span class="sxs-lookup"><span data-stu-id="faaea-260">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="faaea-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="faaea-261">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="faaea-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="faaea-262">System-Only</span></span>            | <span data-ttu-id="faaea-263">False</span><span class="sxs-lookup"><span data-stu-id="faaea-263">False</span></span>                                     |
| <span data-ttu-id="faaea-264">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="faaea-264">Is-Single-Valued</span></span>       | <span data-ttu-id="faaea-265">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-265">True</span></span>                                      |
| <span data-ttu-id="faaea-266">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="faaea-266">Is Indexed</span></span>             | <span data-ttu-id="faaea-267">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-267">True</span></span>                                      |
| <span data-ttu-id="faaea-268">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="faaea-268">In Global Catalog</span></span>      | <span data-ttu-id="faaea-269">Richtig</span><span class="sxs-lookup"><span data-stu-id="faaea-269">True</span></span>                                      |
| <span data-ttu-id="faaea-270">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="faaea-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="faaea-271">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="faaea-271">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="faaea-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="faaea-272">Range-Lower</span></span>            | <span data-ttu-id="faaea-273">16</span><span class="sxs-lookup"><span data-stu-id="faaea-273">16</span></span>                                        |
| <span data-ttu-id="faaea-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="faaea-274">Range-Upper</span></span>            | <span data-ttu-id="faaea-275">16</span><span class="sxs-lookup"><span data-stu-id="faaea-275">16</span></span>                                        |
| <span data-ttu-id="faaea-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="faaea-276">Search-Flags</span></span>           | <span data-ttu-id="faaea-277">0x00000001</span><span class="sxs-lookup"><span data-stu-id="faaea-277">0x00000001</span></span>                                |
| <span data-ttu-id="faaea-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="faaea-278">System-Flags</span></span>           | <span data-ttu-id="faaea-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="faaea-279">0x00000010</span></span>                                |
| <span data-ttu-id="faaea-280">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="faaea-280">Classes used in</span></span>        | [<span data-ttu-id="faaea-281">**Computer**</span><span class="sxs-lookup"><span data-stu-id="faaea-281">**Computer**</span></span>](c-computer.md)<br/> |



 

 





