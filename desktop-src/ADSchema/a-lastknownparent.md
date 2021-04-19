---
title: Letztes-bekannt/übergeordnetes Attribut
description: Der Distinguished Name (DN) des letzten bekannten übergeordneten Elements eines verwaisten Objekts.
ms.assetid: 6cf7be1a-8ff0-42f7-9e7a-c15cbc652ec5
ms.tgt_platform: multiple
keywords:
- AD-Schema für das zuletzt bekannte übergeordnete Attribut
- lastKnownParent-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Last-Known-Parent
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d83ae15f910d2e2f2dbc23ff39bb28cd27d56b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346370"
---
# <a name="last-known-parent-attribute"></a><span data-ttu-id="ba383-105">Letztes-bekannt/übergeordnetes Attribut</span><span class="sxs-lookup"><span data-stu-id="ba383-105">Last-Known-Parent attribute</span></span>

<span data-ttu-id="ba383-106">Der Distinguished Name (DN) des letzten bekannten übergeordneten Elements eines verwaisten Objekts.</span><span class="sxs-lookup"><span data-stu-id="ba383-106">The Distinguished Name (DN) of the last known parent of an orphaned object.</span></span>



| <span data-ttu-id="ba383-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ba383-107">Entry</span></span> | <span data-ttu-id="ba383-108">Wert</span><span class="sxs-lookup"><span data-stu-id="ba383-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="ba383-109">CN</span><span class="sxs-lookup"><span data-stu-id="ba383-109">CN</span></span>                | <span data-ttu-id="ba383-110">Letztes-bekannt/übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="ba383-110">Last-Known-Parent</span></span>                       |
| <span data-ttu-id="ba383-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ba383-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ba383-112">lastKnownParent</span><span class="sxs-lookup"><span data-stu-id="ba383-112">lastKnownParent</span></span>                         |
| <span data-ttu-id="ba383-113">Size</span><span class="sxs-lookup"><span data-stu-id="ba383-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="ba383-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ba383-114">Update Privilege</span></span>  | <span data-ttu-id="ba383-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ba383-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="ba383-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="ba383-116">Update Frequency</span></span>  | <span data-ttu-id="ba383-117">Jedes Mal, wenn ein Objekt verwaist ist.</span><span class="sxs-lookup"><span data-stu-id="ba383-117">Whenever an object is orphaned.</span></span>         |
| <span data-ttu-id="ba383-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ba383-118">Attribute-Id</span></span>      | <span data-ttu-id="ba383-119">1.2.840.113556.1.4.781</span><span class="sxs-lookup"><span data-stu-id="ba383-119">1.2.840.113556.1.4.781</span></span>                  |
| <span data-ttu-id="ba383-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ba383-120">System-Id-Guid</span></span>    | <span data-ttu-id="ba383-121">52ab8670-5709-11d1-a9c6-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="ba383-121">52ab8670-5709-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="ba383-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba383-122">Syntax</span></span>            | [<span data-ttu-id="ba383-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="ba383-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="ba383-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ba383-124">Implementations</span></span>

-   [<span data-ttu-id="ba383-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ba383-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ba383-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ba383-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ba383-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="ba383-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ba383-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ba383-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ba383-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ba383-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ba383-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ba383-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ba383-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ba383-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ba383-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ba383-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ba383-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ba383-133">Entry</span></span> | <span data-ttu-id="ba383-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ba383-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ba383-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ba383-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ba383-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba383-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ba383-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba383-137">System-Only</span></span>            | <span data-ttu-id="ba383-138">False</span><span class="sxs-lookup"><span data-stu-id="ba383-138">False</span></span>                           |
| <span data-ttu-id="ba383-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ba383-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ba383-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="ba383-140">True</span></span>                            |
| <span data-ttu-id="ba383-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ba383-141">Is Indexed</span></span>             | <span data-ttu-id="ba383-142">False</span><span class="sxs-lookup"><span data-stu-id="ba383-142">False</span></span>                           |
| <span data-ttu-id="ba383-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ba383-143">In Global Catalog</span></span>      | <span data-ttu-id="ba383-144">False</span><span class="sxs-lookup"><span data-stu-id="ba383-144">False</span></span>                           |
| <span data-ttu-id="ba383-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ba383-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba383-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ba383-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ba383-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba383-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ba383-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba383-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ba383-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba383-149">Search-Flags</span></span>           | <span data-ttu-id="ba383-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba383-150">0x00000000</span></span>                      |
| <span data-ttu-id="ba383-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba383-151">System-Flags</span></span>           | <span data-ttu-id="ba383-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba383-152">0x00000010</span></span>                      |
| <span data-ttu-id="ba383-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ba383-153">Classes used in</span></span>        | [<span data-ttu-id="ba383-154">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="ba383-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ba383-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ba383-155">Windows Server 2003</span></span>



| <span data-ttu-id="ba383-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ba383-156">Entry</span></span> | <span data-ttu-id="ba383-157">Wert</span><span class="sxs-lookup"><span data-stu-id="ba383-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ba383-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ba383-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ba383-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba383-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ba383-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba383-160">System-Only</span></span>            | <span data-ttu-id="ba383-161">False</span><span class="sxs-lookup"><span data-stu-id="ba383-161">False</span></span>                           |
| <span data-ttu-id="ba383-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ba383-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ba383-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="ba383-163">True</span></span>                            |
| <span data-ttu-id="ba383-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ba383-164">Is Indexed</span></span>             | <span data-ttu-id="ba383-165">False</span><span class="sxs-lookup"><span data-stu-id="ba383-165">False</span></span>                           |
| <span data-ttu-id="ba383-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ba383-166">In Global Catalog</span></span>      | <span data-ttu-id="ba383-167">False</span><span class="sxs-lookup"><span data-stu-id="ba383-167">False</span></span>                           |
| <span data-ttu-id="ba383-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ba383-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba383-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ba383-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ba383-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba383-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ba383-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba383-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ba383-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba383-172">Search-Flags</span></span>           | <span data-ttu-id="ba383-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba383-173">0x00000000</span></span>                      |
| <span data-ttu-id="ba383-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba383-174">System-Flags</span></span>           | <span data-ttu-id="ba383-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba383-175">0x00000010</span></span>                      |
| <span data-ttu-id="ba383-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ba383-176">Classes used in</span></span>        | [<span data-ttu-id="ba383-177">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="ba383-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ba383-178">Adam</span><span class="sxs-lookup"><span data-stu-id="ba383-178">ADAM</span></span>



| <span data-ttu-id="ba383-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ba383-179">Entry</span></span> | <span data-ttu-id="ba383-180">Wert</span><span class="sxs-lookup"><span data-stu-id="ba383-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ba383-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ba383-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ba383-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba383-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ba383-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba383-183">System-Only</span></span>            | <span data-ttu-id="ba383-184">False</span><span class="sxs-lookup"><span data-stu-id="ba383-184">False</span></span>                           |
| <span data-ttu-id="ba383-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ba383-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ba383-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="ba383-186">True</span></span>                            |
| <span data-ttu-id="ba383-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ba383-187">Is Indexed</span></span>             | <span data-ttu-id="ba383-188">False</span><span class="sxs-lookup"><span data-stu-id="ba383-188">False</span></span>                           |
| <span data-ttu-id="ba383-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ba383-189">In Global Catalog</span></span>      | <span data-ttu-id="ba383-190">False</span><span class="sxs-lookup"><span data-stu-id="ba383-190">False</span></span>                           |
| <span data-ttu-id="ba383-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ba383-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba383-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ba383-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ba383-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba383-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ba383-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba383-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ba383-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba383-195">Search-Flags</span></span>           | <span data-ttu-id="ba383-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba383-196">0x00000000</span></span>                      |
| <span data-ttu-id="ba383-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba383-197">System-Flags</span></span>           | <span data-ttu-id="ba383-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba383-198">0x00000010</span></span>                      |
| <span data-ttu-id="ba383-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ba383-199">Classes used in</span></span>        | [<span data-ttu-id="ba383-200">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="ba383-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ba383-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ba383-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ba383-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ba383-202">Entry</span></span> | <span data-ttu-id="ba383-203">Wert</span><span class="sxs-lookup"><span data-stu-id="ba383-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ba383-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ba383-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ba383-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba383-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ba383-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba383-206">System-Only</span></span>            | <span data-ttu-id="ba383-207">False</span><span class="sxs-lookup"><span data-stu-id="ba383-207">False</span></span>                           |
| <span data-ttu-id="ba383-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ba383-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ba383-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="ba383-209">True</span></span>                            |
| <span data-ttu-id="ba383-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ba383-210">Is Indexed</span></span>             | <span data-ttu-id="ba383-211">False</span><span class="sxs-lookup"><span data-stu-id="ba383-211">False</span></span>                           |
| <span data-ttu-id="ba383-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ba383-212">In Global Catalog</span></span>      | <span data-ttu-id="ba383-213">False</span><span class="sxs-lookup"><span data-stu-id="ba383-213">False</span></span>                           |
| <span data-ttu-id="ba383-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ba383-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba383-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ba383-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ba383-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba383-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ba383-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba383-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ba383-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba383-218">Search-Flags</span></span>           | <span data-ttu-id="ba383-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba383-219">0x00000000</span></span>                      |
| <span data-ttu-id="ba383-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba383-220">System-Flags</span></span>           | <span data-ttu-id="ba383-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba383-221">0x00000010</span></span>                      |
| <span data-ttu-id="ba383-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ba383-222">Classes used in</span></span>        | [<span data-ttu-id="ba383-223">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="ba383-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ba383-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba383-224">Windows Server 2008</span></span>



| <span data-ttu-id="ba383-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ba383-225">Entry</span></span> | <span data-ttu-id="ba383-226">Wert</span><span class="sxs-lookup"><span data-stu-id="ba383-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ba383-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ba383-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ba383-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba383-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ba383-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba383-229">System-Only</span></span>            | <span data-ttu-id="ba383-230">False</span><span class="sxs-lookup"><span data-stu-id="ba383-230">False</span></span>                           |
| <span data-ttu-id="ba383-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ba383-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ba383-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="ba383-232">True</span></span>                            |
| <span data-ttu-id="ba383-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ba383-233">Is Indexed</span></span>             | <span data-ttu-id="ba383-234">False</span><span class="sxs-lookup"><span data-stu-id="ba383-234">False</span></span>                           |
| <span data-ttu-id="ba383-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ba383-235">In Global Catalog</span></span>      | <span data-ttu-id="ba383-236">False</span><span class="sxs-lookup"><span data-stu-id="ba383-236">False</span></span>                           |
| <span data-ttu-id="ba383-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ba383-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba383-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ba383-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ba383-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba383-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ba383-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba383-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ba383-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba383-241">Search-Flags</span></span>           | <span data-ttu-id="ba383-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba383-242">0x00000000</span></span>                      |
| <span data-ttu-id="ba383-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba383-243">System-Flags</span></span>           | <span data-ttu-id="ba383-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba383-244">0x00000010</span></span>                      |
| <span data-ttu-id="ba383-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ba383-245">Classes used in</span></span>        | [<span data-ttu-id="ba383-246">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="ba383-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ba383-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ba383-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ba383-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ba383-248">Entry</span></span> | <span data-ttu-id="ba383-249">Wert</span><span class="sxs-lookup"><span data-stu-id="ba383-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ba383-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ba383-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ba383-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba383-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ba383-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba383-252">System-Only</span></span>            | <span data-ttu-id="ba383-253">False</span><span class="sxs-lookup"><span data-stu-id="ba383-253">False</span></span>                           |
| <span data-ttu-id="ba383-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ba383-254">Is-Single-Valued</span></span>       | <span data-ttu-id="ba383-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="ba383-255">True</span></span>                            |
| <span data-ttu-id="ba383-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ba383-256">Is Indexed</span></span>             | <span data-ttu-id="ba383-257">False</span><span class="sxs-lookup"><span data-stu-id="ba383-257">False</span></span>                           |
| <span data-ttu-id="ba383-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ba383-258">In Global Catalog</span></span>      | <span data-ttu-id="ba383-259">False</span><span class="sxs-lookup"><span data-stu-id="ba383-259">False</span></span>                           |
| <span data-ttu-id="ba383-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ba383-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba383-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ba383-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ba383-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba383-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ba383-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba383-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ba383-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba383-264">Search-Flags</span></span>           | <span data-ttu-id="ba383-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba383-265">0x00000000</span></span>                      |
| <span data-ttu-id="ba383-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba383-266">System-Flags</span></span>           | <span data-ttu-id="ba383-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba383-267">0x00000010</span></span>                      |
| <span data-ttu-id="ba383-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ba383-268">Classes used in</span></span>        | [<span data-ttu-id="ba383-269">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="ba383-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ba383-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ba383-270">Windows Server 2012</span></span>



| <span data-ttu-id="ba383-271">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ba383-271">Entry</span></span> | <span data-ttu-id="ba383-272">Wert</span><span class="sxs-lookup"><span data-stu-id="ba383-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ba383-273">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ba383-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ba383-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba383-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ba383-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba383-275">System-Only</span></span>            | <span data-ttu-id="ba383-276">False</span><span class="sxs-lookup"><span data-stu-id="ba383-276">False</span></span>                           |
| <span data-ttu-id="ba383-277">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ba383-277">Is-Single-Valued</span></span>       | <span data-ttu-id="ba383-278">Richtig</span><span class="sxs-lookup"><span data-stu-id="ba383-278">True</span></span>                            |
| <span data-ttu-id="ba383-279">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ba383-279">Is Indexed</span></span>             | <span data-ttu-id="ba383-280">False</span><span class="sxs-lookup"><span data-stu-id="ba383-280">False</span></span>                           |
| <span data-ttu-id="ba383-281">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ba383-281">In Global Catalog</span></span>      | <span data-ttu-id="ba383-282">False</span><span class="sxs-lookup"><span data-stu-id="ba383-282">False</span></span>                           |
| <span data-ttu-id="ba383-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ba383-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba383-284">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ba383-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ba383-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba383-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ba383-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba383-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ba383-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba383-287">Search-Flags</span></span>           | <span data-ttu-id="ba383-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba383-288">0x00000000</span></span>                      |
| <span data-ttu-id="ba383-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba383-289">System-Flags</span></span>           | <span data-ttu-id="ba383-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba383-290">0x00000010</span></span>                      |
| <span data-ttu-id="ba383-291">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ba383-291">Classes used in</span></span>        | [<span data-ttu-id="ba383-292">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="ba383-292">**Top**</span></span>](c-top.md)<br/> |



 

 





