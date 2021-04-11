---
title: ms-DS-Filter-Containers-Attribut
description: Eine Zeichenfolge mit mehreren Werten, die die Namen der Klassen enthält, mit denen bestimmt wird, welche Containertypen beim Filtern von dem Active Directory-Benutzer und-Computer-Snap-in angezeigt werden sollen.
ms.assetid: 765ac0e1-59d2-44a9-a01e-9cdf7d040c93
ms.tgt_platform: multiple
keywords:
- "\"ms-DS-Filter-Containers\"-Attribut AD-Schema"
- adschema des msDS-filtercontainers-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Filter-Containers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8156b1baa2fe86ec0322a9161ce5231a7e23f32e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122959"
---
# <a name="ms-ds-filter-containers-attribute"></a><span data-ttu-id="caa55-105">ms-DS-Filter-Containers-Attribut</span><span class="sxs-lookup"><span data-stu-id="caa55-105">ms-DS-Filter-Containers attribute</span></span>

<span data-ttu-id="caa55-106">Eine Zeichenfolge mit mehreren Werten, die die Namen der Klassen enthält, mit denen bestimmt wird, welche Containertypen beim Filtern von dem Active Directory-Benutzer und-Computer-Snap-in angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="caa55-106">A multiple-valued string that contains the names of classes used to determine which container types should be shown by the Active Directory Users and Computers snap-in when filtering.</span></span>



| <span data-ttu-id="caa55-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="caa55-107">Entry</span></span> | <span data-ttu-id="caa55-108">Wert</span><span class="sxs-lookup"><span data-stu-id="caa55-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="caa55-109">CN</span><span class="sxs-lookup"><span data-stu-id="caa55-109">CN</span></span>                | <span data-ttu-id="caa55-110">ms-DS-Filter-Container</span><span class="sxs-lookup"><span data-stu-id="caa55-110">ms-DS-Filter-Containers</span></span>                     |
| <span data-ttu-id="caa55-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="caa55-111">Ldap-Display-Name</span></span> | <span data-ttu-id="caa55-112">MSDS-filtercontainers</span><span class="sxs-lookup"><span data-stu-id="caa55-112">msDS-FilterContainers</span></span>                       |
| <span data-ttu-id="caa55-113">Size</span><span class="sxs-lookup"><span data-stu-id="caa55-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="caa55-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="caa55-114">Update Privilege</span></span>  | <span data-ttu-id="caa55-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="caa55-115">Domain administrator</span></span>                        |
| <span data-ttu-id="caa55-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="caa55-116">Update Frequency</span></span>  | <span data-ttu-id="caa55-117">Wenn die Liste der Containertypen geändert wird.</span><span class="sxs-lookup"><span data-stu-id="caa55-117">When the list of container types changes.</span></span>   |
| <span data-ttu-id="caa55-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="caa55-118">Attribute-Id</span></span>      | <span data-ttu-id="caa55-119">1.2.840.113556.1.4.1703</span><span class="sxs-lookup"><span data-stu-id="caa55-119">1.2.840.113556.1.4.1703</span></span>                     |
| <span data-ttu-id="caa55-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="caa55-120">System-Id-Guid</span></span>    | <span data-ttu-id="caa55-121">fb00dcdf-ac37-483a-9c12-ac53a6603033</span><span class="sxs-lookup"><span data-stu-id="caa55-121">fb00dcdf-ac37-483a-9c12-ac53a6603033</span></span>        |
| <span data-ttu-id="caa55-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="caa55-122">Syntax</span></span>            | [<span data-ttu-id="caa55-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="caa55-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="caa55-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="caa55-124">Implementations</span></span>

-   [<span data-ttu-id="caa55-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="caa55-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="caa55-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="caa55-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="caa55-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="caa55-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="caa55-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="caa55-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="caa55-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="caa55-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="caa55-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="caa55-130">Windows Server 2003</span></span>



| <span data-ttu-id="caa55-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="caa55-131">Entry</span></span> | <span data-ttu-id="caa55-132">Wert</span><span class="sxs-lookup"><span data-stu-id="caa55-132">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="caa55-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="caa55-133">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="caa55-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="caa55-134">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="caa55-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="caa55-135">System-Only</span></span>            | <span data-ttu-id="caa55-136">False</span><span class="sxs-lookup"><span data-stu-id="caa55-136">False</span></span>                                               |
| <span data-ttu-id="caa55-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="caa55-137">Is-Single-Valued</span></span>       | <span data-ttu-id="caa55-138">False</span><span class="sxs-lookup"><span data-stu-id="caa55-138">False</span></span>                                               |
| <span data-ttu-id="caa55-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="caa55-139">Is Indexed</span></span>             | <span data-ttu-id="caa55-140">False</span><span class="sxs-lookup"><span data-stu-id="caa55-140">False</span></span>                                               |
| <span data-ttu-id="caa55-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="caa55-141">In Global Catalog</span></span>      | <span data-ttu-id="caa55-142">False</span><span class="sxs-lookup"><span data-stu-id="caa55-142">False</span></span>                                               |
| <span data-ttu-id="caa55-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="caa55-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="caa55-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="caa55-144">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="caa55-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="caa55-145">Range-Lower</span></span>            | <span data-ttu-id="caa55-146">1</span><span class="sxs-lookup"><span data-stu-id="caa55-146">1</span></span>                                                   |
| <span data-ttu-id="caa55-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="caa55-147">Range-Upper</span></span>            | <span data-ttu-id="caa55-148">64</span><span class="sxs-lookup"><span data-stu-id="caa55-148">64</span></span>                                                  |
| <span data-ttu-id="caa55-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="caa55-149">Search-Flags</span></span>           | <span data-ttu-id="caa55-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="caa55-150">0x00000000</span></span>                                          |
| <span data-ttu-id="caa55-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="caa55-151">System-Flags</span></span>           | <span data-ttu-id="caa55-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="caa55-152">0x00000010</span></span>                                          |
| <span data-ttu-id="caa55-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="caa55-153">Classes used in</span></span>        | [<span data-ttu-id="caa55-154">**DS-UI-Settings**</span><span class="sxs-lookup"><span data-stu-id="caa55-154">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="caa55-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="caa55-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="caa55-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="caa55-156">Entry</span></span> | <span data-ttu-id="caa55-157">Wert</span><span class="sxs-lookup"><span data-stu-id="caa55-157">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="caa55-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="caa55-158">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="caa55-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="caa55-159">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="caa55-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="caa55-160">System-Only</span></span>            | <span data-ttu-id="caa55-161">False</span><span class="sxs-lookup"><span data-stu-id="caa55-161">False</span></span>                                               |
| <span data-ttu-id="caa55-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="caa55-162">Is-Single-Valued</span></span>       | <span data-ttu-id="caa55-163">False</span><span class="sxs-lookup"><span data-stu-id="caa55-163">False</span></span>                                               |
| <span data-ttu-id="caa55-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="caa55-164">Is Indexed</span></span>             | <span data-ttu-id="caa55-165">False</span><span class="sxs-lookup"><span data-stu-id="caa55-165">False</span></span>                                               |
| <span data-ttu-id="caa55-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="caa55-166">In Global Catalog</span></span>      | <span data-ttu-id="caa55-167">False</span><span class="sxs-lookup"><span data-stu-id="caa55-167">False</span></span>                                               |
| <span data-ttu-id="caa55-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="caa55-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="caa55-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="caa55-169">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="caa55-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="caa55-170">Range-Lower</span></span>            | <span data-ttu-id="caa55-171">1</span><span class="sxs-lookup"><span data-stu-id="caa55-171">1</span></span>                                                   |
| <span data-ttu-id="caa55-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="caa55-172">Range-Upper</span></span>            | <span data-ttu-id="caa55-173">64</span><span class="sxs-lookup"><span data-stu-id="caa55-173">64</span></span>                                                  |
| <span data-ttu-id="caa55-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="caa55-174">Search-Flags</span></span>           | <span data-ttu-id="caa55-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="caa55-175">0x00000000</span></span>                                          |
| <span data-ttu-id="caa55-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="caa55-176">System-Flags</span></span>           | <span data-ttu-id="caa55-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="caa55-177">0x00000010</span></span>                                          |
| <span data-ttu-id="caa55-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="caa55-178">Classes used in</span></span>        | [<span data-ttu-id="caa55-179">**DS-UI-Settings**</span><span class="sxs-lookup"><span data-stu-id="caa55-179">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="caa55-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="caa55-180">Windows Server 2008</span></span>



| <span data-ttu-id="caa55-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="caa55-181">Entry</span></span> | <span data-ttu-id="caa55-182">Wert</span><span class="sxs-lookup"><span data-stu-id="caa55-182">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="caa55-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="caa55-183">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="caa55-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="caa55-184">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="caa55-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="caa55-185">System-Only</span></span>            | <span data-ttu-id="caa55-186">False</span><span class="sxs-lookup"><span data-stu-id="caa55-186">False</span></span>                                               |
| <span data-ttu-id="caa55-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="caa55-187">Is-Single-Valued</span></span>       | <span data-ttu-id="caa55-188">False</span><span class="sxs-lookup"><span data-stu-id="caa55-188">False</span></span>                                               |
| <span data-ttu-id="caa55-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="caa55-189">Is Indexed</span></span>             | <span data-ttu-id="caa55-190">False</span><span class="sxs-lookup"><span data-stu-id="caa55-190">False</span></span>                                               |
| <span data-ttu-id="caa55-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="caa55-191">In Global Catalog</span></span>      | <span data-ttu-id="caa55-192">False</span><span class="sxs-lookup"><span data-stu-id="caa55-192">False</span></span>                                               |
| <span data-ttu-id="caa55-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="caa55-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="caa55-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="caa55-194">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="caa55-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="caa55-195">Range-Lower</span></span>            | <span data-ttu-id="caa55-196">1</span><span class="sxs-lookup"><span data-stu-id="caa55-196">1</span></span>                                                   |
| <span data-ttu-id="caa55-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="caa55-197">Range-Upper</span></span>            | <span data-ttu-id="caa55-198">64</span><span class="sxs-lookup"><span data-stu-id="caa55-198">64</span></span>                                                  |
| <span data-ttu-id="caa55-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="caa55-199">Search-Flags</span></span>           | <span data-ttu-id="caa55-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="caa55-200">0x00000000</span></span>                                          |
| <span data-ttu-id="caa55-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="caa55-201">System-Flags</span></span>           | <span data-ttu-id="caa55-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="caa55-202">0x00000010</span></span>                                          |
| <span data-ttu-id="caa55-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="caa55-203">Classes used in</span></span>        | [<span data-ttu-id="caa55-204">**DS-UI-Settings**</span><span class="sxs-lookup"><span data-stu-id="caa55-204">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="caa55-205">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="caa55-205">Windows Server 2008 R2</span></span>



| <span data-ttu-id="caa55-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="caa55-206">Entry</span></span> | <span data-ttu-id="caa55-207">Wert</span><span class="sxs-lookup"><span data-stu-id="caa55-207">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="caa55-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="caa55-208">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="caa55-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="caa55-209">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="caa55-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="caa55-210">System-Only</span></span>            | <span data-ttu-id="caa55-211">False</span><span class="sxs-lookup"><span data-stu-id="caa55-211">False</span></span>                                               |
| <span data-ttu-id="caa55-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="caa55-212">Is-Single-Valued</span></span>       | <span data-ttu-id="caa55-213">False</span><span class="sxs-lookup"><span data-stu-id="caa55-213">False</span></span>                                               |
| <span data-ttu-id="caa55-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="caa55-214">Is Indexed</span></span>             | <span data-ttu-id="caa55-215">False</span><span class="sxs-lookup"><span data-stu-id="caa55-215">False</span></span>                                               |
| <span data-ttu-id="caa55-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="caa55-216">In Global Catalog</span></span>      | <span data-ttu-id="caa55-217">False</span><span class="sxs-lookup"><span data-stu-id="caa55-217">False</span></span>                                               |
| <span data-ttu-id="caa55-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="caa55-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="caa55-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="caa55-219">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="caa55-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="caa55-220">Range-Lower</span></span>            | <span data-ttu-id="caa55-221">1</span><span class="sxs-lookup"><span data-stu-id="caa55-221">1</span></span>                                                   |
| <span data-ttu-id="caa55-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="caa55-222">Range-Upper</span></span>            | <span data-ttu-id="caa55-223">64</span><span class="sxs-lookup"><span data-stu-id="caa55-223">64</span></span>                                                  |
| <span data-ttu-id="caa55-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="caa55-224">Search-Flags</span></span>           | <span data-ttu-id="caa55-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="caa55-225">0x00000000</span></span>                                          |
| <span data-ttu-id="caa55-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="caa55-226">System-Flags</span></span>           | <span data-ttu-id="caa55-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="caa55-227">0x00000010</span></span>                                          |
| <span data-ttu-id="caa55-228">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="caa55-228">Classes used in</span></span>        | [<span data-ttu-id="caa55-229">**DS-UI-Settings**</span><span class="sxs-lookup"><span data-stu-id="caa55-229">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="caa55-230">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="caa55-230">Windows Server 2012</span></span>



| <span data-ttu-id="caa55-231">Eingabe</span><span class="sxs-lookup"><span data-stu-id="caa55-231">Entry</span></span> | <span data-ttu-id="caa55-232">Wert</span><span class="sxs-lookup"><span data-stu-id="caa55-232">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="caa55-233">Link-ID</span><span class="sxs-lookup"><span data-stu-id="caa55-233">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="caa55-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="caa55-234">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="caa55-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="caa55-235">System-Only</span></span>            | <span data-ttu-id="caa55-236">False</span><span class="sxs-lookup"><span data-stu-id="caa55-236">False</span></span>                                               |
| <span data-ttu-id="caa55-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="caa55-237">Is-Single-Valued</span></span>       | <span data-ttu-id="caa55-238">False</span><span class="sxs-lookup"><span data-stu-id="caa55-238">False</span></span>                                               |
| <span data-ttu-id="caa55-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="caa55-239">Is Indexed</span></span>             | <span data-ttu-id="caa55-240">False</span><span class="sxs-lookup"><span data-stu-id="caa55-240">False</span></span>                                               |
| <span data-ttu-id="caa55-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="caa55-241">In Global Catalog</span></span>      | <span data-ttu-id="caa55-242">False</span><span class="sxs-lookup"><span data-stu-id="caa55-242">False</span></span>                                               |
| <span data-ttu-id="caa55-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="caa55-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="caa55-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="caa55-244">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="caa55-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="caa55-245">Range-Lower</span></span>            | <span data-ttu-id="caa55-246">1</span><span class="sxs-lookup"><span data-stu-id="caa55-246">1</span></span>                                                   |
| <span data-ttu-id="caa55-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="caa55-247">Range-Upper</span></span>            | <span data-ttu-id="caa55-248">64</span><span class="sxs-lookup"><span data-stu-id="caa55-248">64</span></span>                                                  |
| <span data-ttu-id="caa55-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="caa55-249">Search-Flags</span></span>           | <span data-ttu-id="caa55-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="caa55-250">0x00000000</span></span>                                          |
| <span data-ttu-id="caa55-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="caa55-251">System-Flags</span></span>           | <span data-ttu-id="caa55-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="caa55-252">0x00000010</span></span>                                          |
| <span data-ttu-id="caa55-253">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="caa55-253">Classes used in</span></span>        | [<span data-ttu-id="caa55-254">**DS-UI-Settings**</span><span class="sxs-lookup"><span data-stu-id="caa55-254">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



 

 





