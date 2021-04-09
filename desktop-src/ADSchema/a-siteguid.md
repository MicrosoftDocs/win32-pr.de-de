---
title: Site-GUID-Attribut
description: Der eindeutige Bezeichner für eine Website.
ms.assetid: 1baa967e-5aa3-495f-aa4f-14eac74f70e4
ms.tgt_platform: multiple
keywords:
- Site-GUID-Attribut AD-Schema
- SiteGUID-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Site-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3932eb2ced2fe14480010c1120266619cc34456
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957441"
---
# <a name="site-guid-attribute"></a><span data-ttu-id="d3bc8-105">Site-GUID-Attribut</span><span class="sxs-lookup"><span data-stu-id="d3bc8-105">Site-GUID attribute</span></span>

<span data-ttu-id="d3bc8-106">Der eindeutige Bezeichner für eine Website.</span><span class="sxs-lookup"><span data-stu-id="d3bc8-106">The unique identifier for a site.</span></span>



| <span data-ttu-id="d3bc8-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3bc8-107">Entry</span></span> | <span data-ttu-id="d3bc8-108">Wert</span><span class="sxs-lookup"><span data-stu-id="d3bc8-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="d3bc8-109">CN</span><span class="sxs-lookup"><span data-stu-id="d3bc8-109">CN</span></span>                | <span data-ttu-id="d3bc8-110">Site-GUID</span><span class="sxs-lookup"><span data-stu-id="d3bc8-110">Site-GUID</span></span>                                             |
| <span data-ttu-id="d3bc8-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d3bc8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d3bc8-112">SiteGUID</span><span class="sxs-lookup"><span data-stu-id="d3bc8-112">siteGUID</span></span>                                              |
| <span data-ttu-id="d3bc8-113">Size</span><span class="sxs-lookup"><span data-stu-id="d3bc8-113">Size</span></span>              | <span data-ttu-id="d3bc8-114">16 Bytes</span><span class="sxs-lookup"><span data-stu-id="d3bc8-114">16 bytes</span></span>                                              |
| <span data-ttu-id="d3bc8-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d3bc8-115">Update Privilege</span></span>  | <span data-ttu-id="d3bc8-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d3bc8-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="d3bc8-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="d3bc8-117">Update Frequency</span></span>  | <span data-ttu-id="d3bc8-118">Immer dann, wenn eine neue Website erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d3bc8-118">Whenever a new site is created.</span></span>                       |
| <span data-ttu-id="d3bc8-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d3bc8-119">Attribute-Id</span></span>      | <span data-ttu-id="d3bc8-120">1.2.840.113556.1.4.362</span><span class="sxs-lookup"><span data-stu-id="d3bc8-120">1.2.840.113556.1.4.362</span></span>                                |
| <span data-ttu-id="d3bc8-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d3bc8-121">System-Id-Guid</span></span>    | <span data-ttu-id="d3bc8-122">3e978924-8c01-11D0-AFDA-00c04f 930c9</span><span class="sxs-lookup"><span data-stu-id="d3bc8-122">3e978924-8c01-11d0-afda-00c04fd930c9</span></span>                  |
| <span data-ttu-id="d3bc8-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3bc8-123">Syntax</span></span>            | [<span data-ttu-id="d3bc8-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="d3bc8-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="d3bc8-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="d3bc8-125">Implementations</span></span>

-   [<span data-ttu-id="d3bc8-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d3bc8-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d3bc8-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d3bc8-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d3bc8-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d3bc8-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d3bc8-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d3bc8-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d3bc8-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d3bc8-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d3bc8-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d3bc8-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d3bc8-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d3bc8-132">Windows 2000 Server</span></span>



| <span data-ttu-id="d3bc8-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3bc8-133">Entry</span></span> | <span data-ttu-id="d3bc8-134">Wert</span><span class="sxs-lookup"><span data-stu-id="d3bc8-134">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="d3bc8-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3bc8-135">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="d3bc8-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3bc8-136">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="d3bc8-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3bc8-137">System-Only</span></span>            | <span data-ttu-id="d3bc8-138">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-138">False</span></span>                                     |
| <span data-ttu-id="d3bc8-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3bc8-139">Is-Single-Valued</span></span>       | <span data-ttu-id="d3bc8-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="d3bc8-140">True</span></span>                                      |
| <span data-ttu-id="d3bc8-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3bc8-141">Is Indexed</span></span>             | <span data-ttu-id="d3bc8-142">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-142">False</span></span>                                     |
| <span data-ttu-id="d3bc8-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3bc8-143">In Global Catalog</span></span>      | <span data-ttu-id="d3bc8-144">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-144">False</span></span>                                     |
| <span data-ttu-id="d3bc8-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3bc8-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3bc8-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3bc8-146">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="d3bc8-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3bc8-147">Range-Lower</span></span>            | <span data-ttu-id="d3bc8-148">16</span><span class="sxs-lookup"><span data-stu-id="d3bc8-148">16</span></span>                                        |
| <span data-ttu-id="d3bc8-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3bc8-149">Range-Upper</span></span>            | <span data-ttu-id="d3bc8-150">16</span><span class="sxs-lookup"><span data-stu-id="d3bc8-150">16</span></span>                                        |
| <span data-ttu-id="d3bc8-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3bc8-151">Search-Flags</span></span>           | <span data-ttu-id="d3bc8-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3bc8-152">0x00000000</span></span>                                |
| <span data-ttu-id="d3bc8-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3bc8-153">System-Flags</span></span>           | <span data-ttu-id="d3bc8-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3bc8-154">0x00000010</span></span>                                |
| <span data-ttu-id="d3bc8-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3bc8-155">Classes used in</span></span>        | [<span data-ttu-id="d3bc8-156">**Computer**</span><span class="sxs-lookup"><span data-stu-id="d3bc8-156">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d3bc8-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d3bc8-157">Windows Server 2003</span></span>



| <span data-ttu-id="d3bc8-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3bc8-158">Entry</span></span> | <span data-ttu-id="d3bc8-159">Wert</span><span class="sxs-lookup"><span data-stu-id="d3bc8-159">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="d3bc8-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3bc8-160">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="d3bc8-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3bc8-161">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="d3bc8-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3bc8-162">System-Only</span></span>            | <span data-ttu-id="d3bc8-163">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-163">False</span></span>                                     |
| <span data-ttu-id="d3bc8-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3bc8-164">Is-Single-Valued</span></span>       | <span data-ttu-id="d3bc8-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="d3bc8-165">True</span></span>                                      |
| <span data-ttu-id="d3bc8-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3bc8-166">Is Indexed</span></span>             | <span data-ttu-id="d3bc8-167">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-167">False</span></span>                                     |
| <span data-ttu-id="d3bc8-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3bc8-168">In Global Catalog</span></span>      | <span data-ttu-id="d3bc8-169">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-169">False</span></span>                                     |
| <span data-ttu-id="d3bc8-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3bc8-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3bc8-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3bc8-171">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="d3bc8-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3bc8-172">Range-Lower</span></span>            | <span data-ttu-id="d3bc8-173">16</span><span class="sxs-lookup"><span data-stu-id="d3bc8-173">16</span></span>                                        |
| <span data-ttu-id="d3bc8-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3bc8-174">Range-Upper</span></span>            | <span data-ttu-id="d3bc8-175">16</span><span class="sxs-lookup"><span data-stu-id="d3bc8-175">16</span></span>                                        |
| <span data-ttu-id="d3bc8-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3bc8-176">Search-Flags</span></span>           | <span data-ttu-id="d3bc8-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3bc8-177">0x00000000</span></span>                                |
| <span data-ttu-id="d3bc8-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3bc8-178">System-Flags</span></span>           | <span data-ttu-id="d3bc8-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3bc8-179">0x00000010</span></span>                                |
| <span data-ttu-id="d3bc8-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3bc8-180">Classes used in</span></span>        | [<span data-ttu-id="d3bc8-181">**Computer**</span><span class="sxs-lookup"><span data-stu-id="d3bc8-181">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d3bc8-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d3bc8-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d3bc8-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3bc8-183">Entry</span></span> | <span data-ttu-id="d3bc8-184">Wert</span><span class="sxs-lookup"><span data-stu-id="d3bc8-184">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="d3bc8-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3bc8-185">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="d3bc8-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3bc8-186">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="d3bc8-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3bc8-187">System-Only</span></span>            | <span data-ttu-id="d3bc8-188">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-188">False</span></span>                                     |
| <span data-ttu-id="d3bc8-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3bc8-189">Is-Single-Valued</span></span>       | <span data-ttu-id="d3bc8-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="d3bc8-190">True</span></span>                                      |
| <span data-ttu-id="d3bc8-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3bc8-191">Is Indexed</span></span>             | <span data-ttu-id="d3bc8-192">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-192">False</span></span>                                     |
| <span data-ttu-id="d3bc8-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3bc8-193">In Global Catalog</span></span>      | <span data-ttu-id="d3bc8-194">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-194">False</span></span>                                     |
| <span data-ttu-id="d3bc8-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3bc8-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3bc8-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3bc8-196">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="d3bc8-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3bc8-197">Range-Lower</span></span>            | <span data-ttu-id="d3bc8-198">16</span><span class="sxs-lookup"><span data-stu-id="d3bc8-198">16</span></span>                                        |
| <span data-ttu-id="d3bc8-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3bc8-199">Range-Upper</span></span>            | <span data-ttu-id="d3bc8-200">16</span><span class="sxs-lookup"><span data-stu-id="d3bc8-200">16</span></span>                                        |
| <span data-ttu-id="d3bc8-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3bc8-201">Search-Flags</span></span>           | <span data-ttu-id="d3bc8-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3bc8-202">0x00000000</span></span>                                |
| <span data-ttu-id="d3bc8-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3bc8-203">System-Flags</span></span>           | <span data-ttu-id="d3bc8-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3bc8-204">0x00000010</span></span>                                |
| <span data-ttu-id="d3bc8-205">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3bc8-205">Classes used in</span></span>        | [<span data-ttu-id="d3bc8-206">**Computer**</span><span class="sxs-lookup"><span data-stu-id="d3bc8-206">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d3bc8-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3bc8-207">Windows Server 2008</span></span>



| <span data-ttu-id="d3bc8-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3bc8-208">Entry</span></span> | <span data-ttu-id="d3bc8-209">Wert</span><span class="sxs-lookup"><span data-stu-id="d3bc8-209">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="d3bc8-210">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3bc8-210">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="d3bc8-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3bc8-211">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="d3bc8-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3bc8-212">System-Only</span></span>            | <span data-ttu-id="d3bc8-213">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-213">False</span></span>                                     |
| <span data-ttu-id="d3bc8-214">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3bc8-214">Is-Single-Valued</span></span>       | <span data-ttu-id="d3bc8-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="d3bc8-215">True</span></span>                                      |
| <span data-ttu-id="d3bc8-216">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3bc8-216">Is Indexed</span></span>             | <span data-ttu-id="d3bc8-217">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-217">False</span></span>                                     |
| <span data-ttu-id="d3bc8-218">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3bc8-218">In Global Catalog</span></span>      | <span data-ttu-id="d3bc8-219">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-219">False</span></span>                                     |
| <span data-ttu-id="d3bc8-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3bc8-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3bc8-221">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3bc8-221">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="d3bc8-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3bc8-222">Range-Lower</span></span>            | <span data-ttu-id="d3bc8-223">16</span><span class="sxs-lookup"><span data-stu-id="d3bc8-223">16</span></span>                                        |
| <span data-ttu-id="d3bc8-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3bc8-224">Range-Upper</span></span>            | <span data-ttu-id="d3bc8-225">16</span><span class="sxs-lookup"><span data-stu-id="d3bc8-225">16</span></span>                                        |
| <span data-ttu-id="d3bc8-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3bc8-226">Search-Flags</span></span>           | <span data-ttu-id="d3bc8-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3bc8-227">0x00000000</span></span>                                |
| <span data-ttu-id="d3bc8-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3bc8-228">System-Flags</span></span>           | <span data-ttu-id="d3bc8-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3bc8-229">0x00000010</span></span>                                |
| <span data-ttu-id="d3bc8-230">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3bc8-230">Classes used in</span></span>        | [<span data-ttu-id="d3bc8-231">**Computer**</span><span class="sxs-lookup"><span data-stu-id="d3bc8-231">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d3bc8-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d3bc8-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d3bc8-233">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3bc8-233">Entry</span></span> | <span data-ttu-id="d3bc8-234">Wert</span><span class="sxs-lookup"><span data-stu-id="d3bc8-234">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="d3bc8-235">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3bc8-235">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="d3bc8-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3bc8-236">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="d3bc8-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3bc8-237">System-Only</span></span>            | <span data-ttu-id="d3bc8-238">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-238">False</span></span>                                     |
| <span data-ttu-id="d3bc8-239">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3bc8-239">Is-Single-Valued</span></span>       | <span data-ttu-id="d3bc8-240">Richtig</span><span class="sxs-lookup"><span data-stu-id="d3bc8-240">True</span></span>                                      |
| <span data-ttu-id="d3bc8-241">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3bc8-241">Is Indexed</span></span>             | <span data-ttu-id="d3bc8-242">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-242">False</span></span>                                     |
| <span data-ttu-id="d3bc8-243">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3bc8-243">In Global Catalog</span></span>      | <span data-ttu-id="d3bc8-244">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-244">False</span></span>                                     |
| <span data-ttu-id="d3bc8-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3bc8-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3bc8-246">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3bc8-246">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="d3bc8-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3bc8-247">Range-Lower</span></span>            | <span data-ttu-id="d3bc8-248">16</span><span class="sxs-lookup"><span data-stu-id="d3bc8-248">16</span></span>                                        |
| <span data-ttu-id="d3bc8-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3bc8-249">Range-Upper</span></span>            | <span data-ttu-id="d3bc8-250">16</span><span class="sxs-lookup"><span data-stu-id="d3bc8-250">16</span></span>                                        |
| <span data-ttu-id="d3bc8-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3bc8-251">Search-Flags</span></span>           | <span data-ttu-id="d3bc8-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3bc8-252">0x00000000</span></span>                                |
| <span data-ttu-id="d3bc8-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3bc8-253">System-Flags</span></span>           | <span data-ttu-id="d3bc8-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3bc8-254">0x00000010</span></span>                                |
| <span data-ttu-id="d3bc8-255">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3bc8-255">Classes used in</span></span>        | [<span data-ttu-id="d3bc8-256">**Computer**</span><span class="sxs-lookup"><span data-stu-id="d3bc8-256">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d3bc8-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d3bc8-257">Windows Server 2012</span></span>



| <span data-ttu-id="d3bc8-258">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3bc8-258">Entry</span></span> | <span data-ttu-id="d3bc8-259">Wert</span><span class="sxs-lookup"><span data-stu-id="d3bc8-259">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="d3bc8-260">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3bc8-260">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="d3bc8-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3bc8-261">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="d3bc8-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3bc8-262">System-Only</span></span>            | <span data-ttu-id="d3bc8-263">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-263">False</span></span>                                     |
| <span data-ttu-id="d3bc8-264">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3bc8-264">Is-Single-Valued</span></span>       | <span data-ttu-id="d3bc8-265">Richtig</span><span class="sxs-lookup"><span data-stu-id="d3bc8-265">True</span></span>                                      |
| <span data-ttu-id="d3bc8-266">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3bc8-266">Is Indexed</span></span>             | <span data-ttu-id="d3bc8-267">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-267">False</span></span>                                     |
| <span data-ttu-id="d3bc8-268">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3bc8-268">In Global Catalog</span></span>      | <span data-ttu-id="d3bc8-269">False</span><span class="sxs-lookup"><span data-stu-id="d3bc8-269">False</span></span>                                     |
| <span data-ttu-id="d3bc8-270">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3bc8-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3bc8-271">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3bc8-271">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="d3bc8-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3bc8-272">Range-Lower</span></span>            | <span data-ttu-id="d3bc8-273">16</span><span class="sxs-lookup"><span data-stu-id="d3bc8-273">16</span></span>                                        |
| <span data-ttu-id="d3bc8-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3bc8-274">Range-Upper</span></span>            | <span data-ttu-id="d3bc8-275">16</span><span class="sxs-lookup"><span data-stu-id="d3bc8-275">16</span></span>                                        |
| <span data-ttu-id="d3bc8-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3bc8-276">Search-Flags</span></span>           | <span data-ttu-id="d3bc8-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3bc8-277">0x00000000</span></span>                                |
| <span data-ttu-id="d3bc8-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3bc8-278">System-Flags</span></span>           | <span data-ttu-id="d3bc8-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3bc8-279">0x00000010</span></span>                                |
| <span data-ttu-id="d3bc8-280">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3bc8-280">Classes used in</span></span>        | [<span data-ttu-id="d3bc8-281">**Computer**</span><span class="sxs-lookup"><span data-stu-id="d3bc8-281">**Computer**</span></span>](c-computer.md)<br/> |



 

 





