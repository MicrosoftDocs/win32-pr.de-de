---
title: MS-IEEE-80211-ID-Attribut
description: Ein Bezeichner, der für ein drahtlos Richtlinien Objekt in AD verwendet wird.
ms.assetid: 751eb9e1-a97f-4a94-a726-151e85ae2dbf
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-IEEE-80211-ID-Attributs
- msieee80211-ID-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- ms-ieee-80211-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1b380617cadf5cfc8b5048e6c9513d40001504
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957500"
---
# <a name="ms-ieee-80211-id-attribute"></a><span data-ttu-id="4580d-105">MS-IEEE-80211-ID-Attribut</span><span class="sxs-lookup"><span data-stu-id="4580d-105">ms-ieee-80211-ID attribute</span></span>

<span data-ttu-id="4580d-106">Ein Bezeichner, der für ein drahtlos Richtlinien Objekt in AD verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4580d-106">An identifier used for a wireless policy object on AD.</span></span>



| <span data-ttu-id="4580d-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4580d-107">Entry</span></span> | <span data-ttu-id="4580d-108">Wert</span><span class="sxs-lookup"><span data-stu-id="4580d-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4580d-109">CN</span><span class="sxs-lookup"><span data-stu-id="4580d-109">CN</span></span>                | <span data-ttu-id="4580d-110">MS-IEEE-80211-ID</span><span class="sxs-lookup"><span data-stu-id="4580d-110">ms-ieee-80211-ID</span></span>                                                                 |
| <span data-ttu-id="4580d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4580d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4580d-112">msieee80211-ID</span><span class="sxs-lookup"><span data-stu-id="4580d-112">msieee80211-ID</span></span>                                                                   |
| <span data-ttu-id="4580d-113">Size</span><span class="sxs-lookup"><span data-stu-id="4580d-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="4580d-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="4580d-114">Update Privilege</span></span>  | <span data-ttu-id="4580d-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="4580d-115">Domain administrator</span></span>                                                             |
| <span data-ttu-id="4580d-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="4580d-116">Update Frequency</span></span>  | <span data-ttu-id="4580d-117">Jedes Mal, wenn ein Domänen Administrator die Richtlinie für Drahtlos Netzwerke für eine Domäne oder Organisationseinheit ändert.</span><span class="sxs-lookup"><span data-stu-id="4580d-117">Each time a Domain Admin changes the wireless network policy for a domain or OU.</span></span> |
| <span data-ttu-id="4580d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4580d-118">Attribute-Id</span></span>      | <span data-ttu-id="4580d-119">1.2.840.113556.1.4.1823</span><span class="sxs-lookup"><span data-stu-id="4580d-119">1.2.840.113556.1.4.1823</span></span>                                                          |
| <span data-ttu-id="4580d-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4580d-120">System-Id-Guid</span></span>    | <span data-ttu-id="4580d-121">7F 73ef75-14c9-4c23-81de-dd07a06s9e8b</span><span class="sxs-lookup"><span data-stu-id="4580d-121">7f73ef75-14c9-4c23-81de-dd07a06f9e8b</span></span>                                             |
| <span data-ttu-id="4580d-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="4580d-122">Syntax</span></span>            | [<span data-ttu-id="4580d-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4580d-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="4580d-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="4580d-124">Implementations</span></span>

-   [<span data-ttu-id="4580d-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4580d-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4580d-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4580d-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4580d-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4580d-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4580d-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4580d-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4580d-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4580d-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="4580d-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4580d-130">Windows Server 2003</span></span>



| <span data-ttu-id="4580d-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4580d-131">Entry</span></span> | <span data-ttu-id="4580d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="4580d-132">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4580d-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4580d-133">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4580d-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4580d-134">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4580d-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="4580d-135">System-Only</span></span>            | <span data-ttu-id="4580d-136">False</span><span class="sxs-lookup"><span data-stu-id="4580d-136">False</span></span>                                                           |
| <span data-ttu-id="4580d-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4580d-137">Is-Single-Valued</span></span>       | <span data-ttu-id="4580d-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="4580d-138">True</span></span>                                                            |
| <span data-ttu-id="4580d-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4580d-139">Is Indexed</span></span>             | <span data-ttu-id="4580d-140">False</span><span class="sxs-lookup"><span data-stu-id="4580d-140">False</span></span>                                                           |
| <span data-ttu-id="4580d-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4580d-141">In Global Catalog</span></span>      | <span data-ttu-id="4580d-142">False</span><span class="sxs-lookup"><span data-stu-id="4580d-142">False</span></span>                                                           |
| <span data-ttu-id="4580d-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4580d-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="4580d-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4580d-144">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4580d-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4580d-145">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="4580d-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4580d-146">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="4580d-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4580d-147">Search-Flags</span></span>           | <span data-ttu-id="4580d-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4580d-148">0x00000000</span></span>                                                      |
| <span data-ttu-id="4580d-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4580d-149">System-Flags</span></span>           | <span data-ttu-id="4580d-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4580d-150">0x00000010</span></span>                                                      |
| <span data-ttu-id="4580d-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4580d-151">Classes used in</span></span>        | [<span data-ttu-id="4580d-152">**MS-IEEE-80211-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="4580d-152">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4580d-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4580d-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4580d-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4580d-154">Entry</span></span> | <span data-ttu-id="4580d-155">Wert</span><span class="sxs-lookup"><span data-stu-id="4580d-155">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4580d-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4580d-156">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4580d-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4580d-157">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4580d-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="4580d-158">System-Only</span></span>            | <span data-ttu-id="4580d-159">False</span><span class="sxs-lookup"><span data-stu-id="4580d-159">False</span></span>                                                           |
| <span data-ttu-id="4580d-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4580d-160">Is-Single-Valued</span></span>       | <span data-ttu-id="4580d-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="4580d-161">True</span></span>                                                            |
| <span data-ttu-id="4580d-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4580d-162">Is Indexed</span></span>             | <span data-ttu-id="4580d-163">False</span><span class="sxs-lookup"><span data-stu-id="4580d-163">False</span></span>                                                           |
| <span data-ttu-id="4580d-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4580d-164">In Global Catalog</span></span>      | <span data-ttu-id="4580d-165">False</span><span class="sxs-lookup"><span data-stu-id="4580d-165">False</span></span>                                                           |
| <span data-ttu-id="4580d-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4580d-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="4580d-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4580d-167">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4580d-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4580d-168">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="4580d-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4580d-169">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="4580d-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4580d-170">Search-Flags</span></span>           | <span data-ttu-id="4580d-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4580d-171">0x00000000</span></span>                                                      |
| <span data-ttu-id="4580d-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4580d-172">System-Flags</span></span>           | <span data-ttu-id="4580d-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4580d-173">0x00000010</span></span>                                                      |
| <span data-ttu-id="4580d-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4580d-174">Classes used in</span></span>        | [<span data-ttu-id="4580d-175">**MS-IEEE-80211-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="4580d-175">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4580d-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4580d-176">Windows Server 2008</span></span>



| <span data-ttu-id="4580d-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4580d-177">Entry</span></span> | <span data-ttu-id="4580d-178">Wert</span><span class="sxs-lookup"><span data-stu-id="4580d-178">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4580d-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4580d-179">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4580d-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4580d-180">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4580d-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="4580d-181">System-Only</span></span>            | <span data-ttu-id="4580d-182">False</span><span class="sxs-lookup"><span data-stu-id="4580d-182">False</span></span>                                                           |
| <span data-ttu-id="4580d-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4580d-183">Is-Single-Valued</span></span>       | <span data-ttu-id="4580d-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="4580d-184">True</span></span>                                                            |
| <span data-ttu-id="4580d-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4580d-185">Is Indexed</span></span>             | <span data-ttu-id="4580d-186">False</span><span class="sxs-lookup"><span data-stu-id="4580d-186">False</span></span>                                                           |
| <span data-ttu-id="4580d-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4580d-187">In Global Catalog</span></span>      | <span data-ttu-id="4580d-188">False</span><span class="sxs-lookup"><span data-stu-id="4580d-188">False</span></span>                                                           |
| <span data-ttu-id="4580d-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4580d-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="4580d-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4580d-190">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4580d-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4580d-191">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="4580d-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4580d-192">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="4580d-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4580d-193">Search-Flags</span></span>           | <span data-ttu-id="4580d-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4580d-194">0x00000000</span></span>                                                      |
| <span data-ttu-id="4580d-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4580d-195">System-Flags</span></span>           | <span data-ttu-id="4580d-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4580d-196">0x00000010</span></span>                                                      |
| <span data-ttu-id="4580d-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4580d-197">Classes used in</span></span>        | [<span data-ttu-id="4580d-198">**MS-IEEE-80211-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="4580d-198">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4580d-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4580d-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4580d-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4580d-200">Entry</span></span> | <span data-ttu-id="4580d-201">Wert</span><span class="sxs-lookup"><span data-stu-id="4580d-201">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4580d-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4580d-202">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4580d-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4580d-203">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4580d-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="4580d-204">System-Only</span></span>            | <span data-ttu-id="4580d-205">False</span><span class="sxs-lookup"><span data-stu-id="4580d-205">False</span></span>                                                           |
| <span data-ttu-id="4580d-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4580d-206">Is-Single-Valued</span></span>       | <span data-ttu-id="4580d-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="4580d-207">True</span></span>                                                            |
| <span data-ttu-id="4580d-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4580d-208">Is Indexed</span></span>             | <span data-ttu-id="4580d-209">False</span><span class="sxs-lookup"><span data-stu-id="4580d-209">False</span></span>                                                           |
| <span data-ttu-id="4580d-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4580d-210">In Global Catalog</span></span>      | <span data-ttu-id="4580d-211">False</span><span class="sxs-lookup"><span data-stu-id="4580d-211">False</span></span>                                                           |
| <span data-ttu-id="4580d-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4580d-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="4580d-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4580d-213">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4580d-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4580d-214">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="4580d-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4580d-215">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="4580d-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4580d-216">Search-Flags</span></span>           | <span data-ttu-id="4580d-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4580d-217">0x00000000</span></span>                                                      |
| <span data-ttu-id="4580d-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4580d-218">System-Flags</span></span>           | <span data-ttu-id="4580d-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4580d-219">0x00000010</span></span>                                                      |
| <span data-ttu-id="4580d-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4580d-220">Classes used in</span></span>        | [<span data-ttu-id="4580d-221">**MS-IEEE-80211-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="4580d-221">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4580d-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4580d-222">Windows Server 2012</span></span>



| <span data-ttu-id="4580d-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4580d-223">Entry</span></span> | <span data-ttu-id="4580d-224">Wert</span><span class="sxs-lookup"><span data-stu-id="4580d-224">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4580d-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4580d-225">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4580d-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4580d-226">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4580d-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="4580d-227">System-Only</span></span>            | <span data-ttu-id="4580d-228">False</span><span class="sxs-lookup"><span data-stu-id="4580d-228">False</span></span>                                                           |
| <span data-ttu-id="4580d-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4580d-229">Is-Single-Valued</span></span>       | <span data-ttu-id="4580d-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="4580d-230">True</span></span>                                                            |
| <span data-ttu-id="4580d-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4580d-231">Is Indexed</span></span>             | <span data-ttu-id="4580d-232">False</span><span class="sxs-lookup"><span data-stu-id="4580d-232">False</span></span>                                                           |
| <span data-ttu-id="4580d-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4580d-233">In Global Catalog</span></span>      | <span data-ttu-id="4580d-234">False</span><span class="sxs-lookup"><span data-stu-id="4580d-234">False</span></span>                                                           |
| <span data-ttu-id="4580d-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4580d-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="4580d-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4580d-236">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4580d-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4580d-237">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="4580d-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4580d-238">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="4580d-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4580d-239">Search-Flags</span></span>           | <span data-ttu-id="4580d-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4580d-240">0x00000000</span></span>                                                      |
| <span data-ttu-id="4580d-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4580d-241">System-Flags</span></span>           | <span data-ttu-id="4580d-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4580d-242">0x00000010</span></span>                                                      |
| <span data-ttu-id="4580d-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4580d-243">Classes used in</span></span>        | [<span data-ttu-id="4580d-244">**MS-IEEE-80211-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="4580d-244">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



 

 





