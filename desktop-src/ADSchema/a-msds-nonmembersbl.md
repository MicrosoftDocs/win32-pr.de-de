---
title: ms-DS-Non-Members-BL-Attribut
description: Rückwärts Verknüpfung von einer nicht-Mitgliedergruppe oder einem Benutzer zu AZ Groups, die mit ihm verknüpft sind (dieselbe Funktion wie nicht Security-Member-BL).
ms.assetid: 51725a95-a9c0-4c88-a390-b8e35b8fd3e1
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-Non-Members-BL-Attribut
- AD-Schema des msDS-nonmembership-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Non-Members-BL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88483757e5c9f87771ce8d71f21d26ea3154f975
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346375"
---
# <a name="ms-ds-non-members-bl-attribute"></a><span data-ttu-id="452d3-105">ms-DS-Non-Members-BL-Attribut</span><span class="sxs-lookup"><span data-stu-id="452d3-105">ms-DS-Non-Members-BL attribute</span></span>

<span data-ttu-id="452d3-106">Rückwärts Verknüpfung von einer nicht-Mitgliedergruppe oder einem Benutzer zu AZ Groups, die mit ihm verknüpft sind (dieselbe Funktion wie nicht Security-Member-BL).</span><span class="sxs-lookup"><span data-stu-id="452d3-106">Backward link from non-member group or user to Az groups that link to it (same functionality as Non-Security-Member-BL).</span></span>



| <span data-ttu-id="452d3-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="452d3-107">Entry</span></span> | <span data-ttu-id="452d3-108">Wert</span><span class="sxs-lookup"><span data-stu-id="452d3-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="452d3-109">CN</span><span class="sxs-lookup"><span data-stu-id="452d3-109">CN</span></span>                | <span data-ttu-id="452d3-110">ms-DS-Non-Members-BL</span><span class="sxs-lookup"><span data-stu-id="452d3-110">ms-DS-Non-Members-BL</span></span>                    |
| <span data-ttu-id="452d3-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="452d3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="452d3-112">MSDS-nonmembership</span><span class="sxs-lookup"><span data-stu-id="452d3-112">msDS-NonMembersBL</span></span>                       |
| <span data-ttu-id="452d3-113">Size</span><span class="sxs-lookup"><span data-stu-id="452d3-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="452d3-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="452d3-114">Update Privilege</span></span>  | <span data-ttu-id="452d3-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="452d3-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="452d3-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="452d3-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="452d3-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="452d3-117">Attribute-Id</span></span>      | <span data-ttu-id="452d3-118">1.2.840.113556.1.4.1794</span><span class="sxs-lookup"><span data-stu-id="452d3-118">1.2.840.113556.1.4.1794</span></span>                 |
| <span data-ttu-id="452d3-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="452d3-119">System-Id-Guid</span></span>    | <span data-ttu-id="452d3-120">2a8c68fc-3a7a-4e87-8720-fe77c51cbe74</span><span class="sxs-lookup"><span data-stu-id="452d3-120">2a8c68fc-3a7a-4e87-8720-fe77c51cbe74</span></span>    |
| <span data-ttu-id="452d3-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="452d3-121">Syntax</span></span>            | [<span data-ttu-id="452d3-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="452d3-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="452d3-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="452d3-123">Implementations</span></span>

-   [<span data-ttu-id="452d3-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="452d3-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="452d3-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="452d3-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="452d3-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="452d3-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="452d3-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="452d3-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="452d3-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="452d3-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="452d3-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="452d3-129">Windows Server 2003</span></span>



| <span data-ttu-id="452d3-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="452d3-130">Entry</span></span> | <span data-ttu-id="452d3-131">Wert</span><span class="sxs-lookup"><span data-stu-id="452d3-131">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="452d3-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="452d3-132">Link-Id</span></span>                | <span data-ttu-id="452d3-133">2015</span><span class="sxs-lookup"><span data-stu-id="452d3-133">2015</span></span>                            |
| <span data-ttu-id="452d3-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="452d3-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="452d3-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="452d3-135">System-Only</span></span>            | <span data-ttu-id="452d3-136">Richtig</span><span class="sxs-lookup"><span data-stu-id="452d3-136">True</span></span>                            |
| <span data-ttu-id="452d3-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="452d3-137">Is-Single-Valued</span></span>       | <span data-ttu-id="452d3-138">False</span><span class="sxs-lookup"><span data-stu-id="452d3-138">False</span></span>                           |
| <span data-ttu-id="452d3-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="452d3-139">Is Indexed</span></span>             | <span data-ttu-id="452d3-140">False</span><span class="sxs-lookup"><span data-stu-id="452d3-140">False</span></span>                           |
| <span data-ttu-id="452d3-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="452d3-141">In Global Catalog</span></span>      | <span data-ttu-id="452d3-142">False</span><span class="sxs-lookup"><span data-stu-id="452d3-142">False</span></span>                           |
| <span data-ttu-id="452d3-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="452d3-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="452d3-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="452d3-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="452d3-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="452d3-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="452d3-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="452d3-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="452d3-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="452d3-147">Search-Flags</span></span>           | <span data-ttu-id="452d3-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="452d3-148">0x00000000</span></span>                      |
| <span data-ttu-id="452d3-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="452d3-149">System-Flags</span></span>           | <span data-ttu-id="452d3-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="452d3-150">0x00000010</span></span>                      |
| <span data-ttu-id="452d3-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="452d3-151">Classes used in</span></span>        | [<span data-ttu-id="452d3-152">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="452d3-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="452d3-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="452d3-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="452d3-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="452d3-154">Entry</span></span> | <span data-ttu-id="452d3-155">Wert</span><span class="sxs-lookup"><span data-stu-id="452d3-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="452d3-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="452d3-156">Link-Id</span></span>                | <span data-ttu-id="452d3-157">2015</span><span class="sxs-lookup"><span data-stu-id="452d3-157">2015</span></span>                            |
| <span data-ttu-id="452d3-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="452d3-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="452d3-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="452d3-159">System-Only</span></span>            | <span data-ttu-id="452d3-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="452d3-160">True</span></span>                            |
| <span data-ttu-id="452d3-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="452d3-161">Is-Single-Valued</span></span>       | <span data-ttu-id="452d3-162">False</span><span class="sxs-lookup"><span data-stu-id="452d3-162">False</span></span>                           |
| <span data-ttu-id="452d3-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="452d3-163">Is Indexed</span></span>             | <span data-ttu-id="452d3-164">False</span><span class="sxs-lookup"><span data-stu-id="452d3-164">False</span></span>                           |
| <span data-ttu-id="452d3-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="452d3-165">In Global Catalog</span></span>      | <span data-ttu-id="452d3-166">False</span><span class="sxs-lookup"><span data-stu-id="452d3-166">False</span></span>                           |
| <span data-ttu-id="452d3-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="452d3-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="452d3-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="452d3-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="452d3-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="452d3-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="452d3-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="452d3-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="452d3-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="452d3-171">Search-Flags</span></span>           | <span data-ttu-id="452d3-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="452d3-172">0x00000000</span></span>                      |
| <span data-ttu-id="452d3-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="452d3-173">System-Flags</span></span>           | <span data-ttu-id="452d3-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="452d3-174">0x00000010</span></span>                      |
| <span data-ttu-id="452d3-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="452d3-175">Classes used in</span></span>        | [<span data-ttu-id="452d3-176">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="452d3-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="452d3-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="452d3-177">Windows Server 2008</span></span>



| <span data-ttu-id="452d3-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="452d3-178">Entry</span></span> | <span data-ttu-id="452d3-179">Wert</span><span class="sxs-lookup"><span data-stu-id="452d3-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="452d3-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="452d3-180">Link-Id</span></span>                | <span data-ttu-id="452d3-181">2015</span><span class="sxs-lookup"><span data-stu-id="452d3-181">2015</span></span>                            |
| <span data-ttu-id="452d3-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="452d3-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="452d3-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="452d3-183">System-Only</span></span>            | <span data-ttu-id="452d3-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="452d3-184">True</span></span>                            |
| <span data-ttu-id="452d3-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="452d3-185">Is-Single-Valued</span></span>       | <span data-ttu-id="452d3-186">False</span><span class="sxs-lookup"><span data-stu-id="452d3-186">False</span></span>                           |
| <span data-ttu-id="452d3-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="452d3-187">Is Indexed</span></span>             | <span data-ttu-id="452d3-188">False</span><span class="sxs-lookup"><span data-stu-id="452d3-188">False</span></span>                           |
| <span data-ttu-id="452d3-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="452d3-189">In Global Catalog</span></span>      | <span data-ttu-id="452d3-190">False</span><span class="sxs-lookup"><span data-stu-id="452d3-190">False</span></span>                           |
| <span data-ttu-id="452d3-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="452d3-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="452d3-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="452d3-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="452d3-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="452d3-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="452d3-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="452d3-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="452d3-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="452d3-195">Search-Flags</span></span>           | <span data-ttu-id="452d3-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="452d3-196">0x00000000</span></span>                      |
| <span data-ttu-id="452d3-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="452d3-197">System-Flags</span></span>           | <span data-ttu-id="452d3-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="452d3-198">0x00000010</span></span>                      |
| <span data-ttu-id="452d3-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="452d3-199">Classes used in</span></span>        | [<span data-ttu-id="452d3-200">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="452d3-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="452d3-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="452d3-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="452d3-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="452d3-202">Entry</span></span> | <span data-ttu-id="452d3-203">Wert</span><span class="sxs-lookup"><span data-stu-id="452d3-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="452d3-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="452d3-204">Link-Id</span></span>                | <span data-ttu-id="452d3-205">2015</span><span class="sxs-lookup"><span data-stu-id="452d3-205">2015</span></span>                            |
| <span data-ttu-id="452d3-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="452d3-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="452d3-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="452d3-207">System-Only</span></span>            | <span data-ttu-id="452d3-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="452d3-208">True</span></span>                            |
| <span data-ttu-id="452d3-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="452d3-209">Is-Single-Valued</span></span>       | <span data-ttu-id="452d3-210">False</span><span class="sxs-lookup"><span data-stu-id="452d3-210">False</span></span>                           |
| <span data-ttu-id="452d3-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="452d3-211">Is Indexed</span></span>             | <span data-ttu-id="452d3-212">False</span><span class="sxs-lookup"><span data-stu-id="452d3-212">False</span></span>                           |
| <span data-ttu-id="452d3-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="452d3-213">In Global Catalog</span></span>      | <span data-ttu-id="452d3-214">False</span><span class="sxs-lookup"><span data-stu-id="452d3-214">False</span></span>                           |
| <span data-ttu-id="452d3-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="452d3-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="452d3-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="452d3-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="452d3-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="452d3-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="452d3-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="452d3-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="452d3-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="452d3-219">Search-Flags</span></span>           | <span data-ttu-id="452d3-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="452d3-220">0x00000000</span></span>                      |
| <span data-ttu-id="452d3-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="452d3-221">System-Flags</span></span>           | <span data-ttu-id="452d3-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="452d3-222">0x00000010</span></span>                      |
| <span data-ttu-id="452d3-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="452d3-223">Classes used in</span></span>        | [<span data-ttu-id="452d3-224">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="452d3-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="452d3-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="452d3-225">Windows Server 2012</span></span>



| <span data-ttu-id="452d3-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="452d3-226">Entry</span></span> | <span data-ttu-id="452d3-227">Wert</span><span class="sxs-lookup"><span data-stu-id="452d3-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="452d3-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="452d3-228">Link-Id</span></span>                | <span data-ttu-id="452d3-229">2015</span><span class="sxs-lookup"><span data-stu-id="452d3-229">2015</span></span>                            |
| <span data-ttu-id="452d3-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="452d3-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="452d3-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="452d3-231">System-Only</span></span>            | <span data-ttu-id="452d3-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="452d3-232">True</span></span>                            |
| <span data-ttu-id="452d3-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="452d3-233">Is-Single-Valued</span></span>       | <span data-ttu-id="452d3-234">False</span><span class="sxs-lookup"><span data-stu-id="452d3-234">False</span></span>                           |
| <span data-ttu-id="452d3-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="452d3-235">Is Indexed</span></span>             | <span data-ttu-id="452d3-236">False</span><span class="sxs-lookup"><span data-stu-id="452d3-236">False</span></span>                           |
| <span data-ttu-id="452d3-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="452d3-237">In Global Catalog</span></span>      | <span data-ttu-id="452d3-238">False</span><span class="sxs-lookup"><span data-stu-id="452d3-238">False</span></span>                           |
| <span data-ttu-id="452d3-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="452d3-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="452d3-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="452d3-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="452d3-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="452d3-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="452d3-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="452d3-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="452d3-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="452d3-243">Search-Flags</span></span>           | <span data-ttu-id="452d3-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="452d3-244">0x00000000</span></span>                      |
| <span data-ttu-id="452d3-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="452d3-245">System-Flags</span></span>           | <span data-ttu-id="452d3-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="452d3-246">0x00000010</span></span>                      |
| <span data-ttu-id="452d3-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="452d3-247">Classes used in</span></span>        | [<span data-ttu-id="452d3-248">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="452d3-248">**Top**</span></span>](c-top.md)<br/> |



 

 





