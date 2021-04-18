---
title: MS-IEEE-80211-Data-Attribut
description: Speichert eine Liste der bevorzugten Netzwerkkonfigurationen in Gruppenrichtlinie für drahtlose Netzwerke.
ms.assetid: 8e5ae2c6-c048-419d-a684-e450a2445a0e
ms.tgt_platform: multiple
keywords:
- MS-IEEE-80211-Daten Attribut-AD-Schema
- msieee80211-Daten Attribut, AD-Schema
topic_type:
- apiref
api_name:
- ms-ieee-80211-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a53138e15a15e4fafecb998b87ef8b4df71fb2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519788"
---
# <a name="ms-ieee-80211-data-attribute"></a><span data-ttu-id="2266c-105">MS-IEEE-80211-Data-Attribut</span><span class="sxs-lookup"><span data-stu-id="2266c-105">ms-ieee-80211-Data attribute</span></span>

<span data-ttu-id="2266c-106">Speichert eine Liste der bevorzugten Netzwerkkonfigurationen in Gruppenrichtlinie für drahtlose Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="2266c-106">Stores a list of preferred network configurations in Group Policy for wireless networks.</span></span>



| <span data-ttu-id="2266c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2266c-107">Entry</span></span> | <span data-ttu-id="2266c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="2266c-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2266c-109">CN</span><span class="sxs-lookup"><span data-stu-id="2266c-109">CN</span></span>                | <span data-ttu-id="2266c-110">MS-IEEE-80211-Data</span><span class="sxs-lookup"><span data-stu-id="2266c-110">ms-ieee-80211-Data</span></span>                                                               |
| <span data-ttu-id="2266c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2266c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2266c-112">msieee80211-Daten</span><span class="sxs-lookup"><span data-stu-id="2266c-112">msieee80211-Data</span></span>                                                                 |
| <span data-ttu-id="2266c-113">Size</span><span class="sxs-lookup"><span data-stu-id="2266c-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="2266c-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2266c-114">Update Privilege</span></span>  | <span data-ttu-id="2266c-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="2266c-115">Domain administrator</span></span>                                                             |
| <span data-ttu-id="2266c-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="2266c-116">Update Frequency</span></span>  | <span data-ttu-id="2266c-117">Jedes Mal, wenn ein Domänen Administrator die Richtlinie für Drahtlos Netzwerke für eine Domäne oder Organisationseinheit ändert.</span><span class="sxs-lookup"><span data-stu-id="2266c-117">Each time a Domain Admin changes the wireless network policy for a domain or OU.</span></span> |
| <span data-ttu-id="2266c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2266c-118">Attribute-Id</span></span>      | <span data-ttu-id="2266c-119">1.2.840.113556.1.4.1821</span><span class="sxs-lookup"><span data-stu-id="2266c-119">1.2.840.113556.1.4.1821</span></span>                                                          |
| <span data-ttu-id="2266c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2266c-120">System-Id-Guid</span></span>    | <span data-ttu-id="2266c-121">0e0d0938-2658-4580-a9f 6-7a0ac7b566cb</span><span class="sxs-lookup"><span data-stu-id="2266c-121">0e0d0938-2658-4580-a9f6-7a0ac7b566cb</span></span>                                             |
| <span data-ttu-id="2266c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="2266c-122">Syntax</span></span>            | [<span data-ttu-id="2266c-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="2266c-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                            |



## <a name="implementations"></a><span data-ttu-id="2266c-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="2266c-124">Implementations</span></span>

-   [<span data-ttu-id="2266c-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2266c-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2266c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2266c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2266c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2266c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2266c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2266c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2266c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2266c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="2266c-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2266c-130">Windows Server 2003</span></span>



| <span data-ttu-id="2266c-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2266c-131">Entry</span></span> | <span data-ttu-id="2266c-132">Wert</span><span class="sxs-lookup"><span data-stu-id="2266c-132">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="2266c-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2266c-133">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2266c-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2266c-134">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2266c-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="2266c-135">System-Only</span></span>            | <span data-ttu-id="2266c-136">False</span><span class="sxs-lookup"><span data-stu-id="2266c-136">False</span></span>                                                           |
| <span data-ttu-id="2266c-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2266c-137">Is-Single-Valued</span></span>       | <span data-ttu-id="2266c-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="2266c-138">True</span></span>                                                            |
| <span data-ttu-id="2266c-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2266c-139">Is Indexed</span></span>             | <span data-ttu-id="2266c-140">False</span><span class="sxs-lookup"><span data-stu-id="2266c-140">False</span></span>                                                           |
| <span data-ttu-id="2266c-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2266c-141">In Global Catalog</span></span>      | <span data-ttu-id="2266c-142">False</span><span class="sxs-lookup"><span data-stu-id="2266c-142">False</span></span>                                                           |
| <span data-ttu-id="2266c-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2266c-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="2266c-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2266c-144">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="2266c-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2266c-145">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="2266c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2266c-146">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="2266c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2266c-147">Search-Flags</span></span>           | <span data-ttu-id="2266c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2266c-148">0x00000000</span></span>                                                      |
| <span data-ttu-id="2266c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2266c-149">System-Flags</span></span>           | <span data-ttu-id="2266c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2266c-150">0x00000010</span></span>                                                      |
| <span data-ttu-id="2266c-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2266c-151">Classes used in</span></span>        | [<span data-ttu-id="2266c-152">**MS-IEEE-80211-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="2266c-152">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2266c-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2266c-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2266c-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2266c-154">Entry</span></span> | <span data-ttu-id="2266c-155">Wert</span><span class="sxs-lookup"><span data-stu-id="2266c-155">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="2266c-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2266c-156">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2266c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2266c-157">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2266c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2266c-158">System-Only</span></span>            | <span data-ttu-id="2266c-159">False</span><span class="sxs-lookup"><span data-stu-id="2266c-159">False</span></span>                                                           |
| <span data-ttu-id="2266c-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2266c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2266c-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="2266c-161">True</span></span>                                                            |
| <span data-ttu-id="2266c-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2266c-162">Is Indexed</span></span>             | <span data-ttu-id="2266c-163">False</span><span class="sxs-lookup"><span data-stu-id="2266c-163">False</span></span>                                                           |
| <span data-ttu-id="2266c-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2266c-164">In Global Catalog</span></span>      | <span data-ttu-id="2266c-165">False</span><span class="sxs-lookup"><span data-stu-id="2266c-165">False</span></span>                                                           |
| <span data-ttu-id="2266c-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2266c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2266c-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2266c-167">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="2266c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2266c-168">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="2266c-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2266c-169">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="2266c-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2266c-170">Search-Flags</span></span>           | <span data-ttu-id="2266c-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2266c-171">0x00000000</span></span>                                                      |
| <span data-ttu-id="2266c-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2266c-172">System-Flags</span></span>           | <span data-ttu-id="2266c-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2266c-173">0x00000010</span></span>                                                      |
| <span data-ttu-id="2266c-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2266c-174">Classes used in</span></span>        | [<span data-ttu-id="2266c-175">**MS-IEEE-80211-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="2266c-175">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2266c-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2266c-176">Windows Server 2008</span></span>



| <span data-ttu-id="2266c-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2266c-177">Entry</span></span> | <span data-ttu-id="2266c-178">Wert</span><span class="sxs-lookup"><span data-stu-id="2266c-178">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="2266c-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2266c-179">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2266c-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2266c-180">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2266c-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2266c-181">System-Only</span></span>            | <span data-ttu-id="2266c-182">False</span><span class="sxs-lookup"><span data-stu-id="2266c-182">False</span></span>                                                           |
| <span data-ttu-id="2266c-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2266c-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2266c-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="2266c-184">True</span></span>                                                            |
| <span data-ttu-id="2266c-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2266c-185">Is Indexed</span></span>             | <span data-ttu-id="2266c-186">False</span><span class="sxs-lookup"><span data-stu-id="2266c-186">False</span></span>                                                           |
| <span data-ttu-id="2266c-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2266c-187">In Global Catalog</span></span>      | <span data-ttu-id="2266c-188">False</span><span class="sxs-lookup"><span data-stu-id="2266c-188">False</span></span>                                                           |
| <span data-ttu-id="2266c-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2266c-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2266c-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2266c-190">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="2266c-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2266c-191">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="2266c-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2266c-192">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="2266c-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2266c-193">Search-Flags</span></span>           | <span data-ttu-id="2266c-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2266c-194">0x00000000</span></span>                                                      |
| <span data-ttu-id="2266c-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2266c-195">System-Flags</span></span>           | <span data-ttu-id="2266c-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2266c-196">0x00000010</span></span>                                                      |
| <span data-ttu-id="2266c-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2266c-197">Classes used in</span></span>        | [<span data-ttu-id="2266c-198">**MS-IEEE-80211-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="2266c-198">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2266c-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2266c-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2266c-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2266c-200">Entry</span></span> | <span data-ttu-id="2266c-201">Wert</span><span class="sxs-lookup"><span data-stu-id="2266c-201">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="2266c-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2266c-202">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2266c-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2266c-203">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2266c-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="2266c-204">System-Only</span></span>            | <span data-ttu-id="2266c-205">False</span><span class="sxs-lookup"><span data-stu-id="2266c-205">False</span></span>                                                           |
| <span data-ttu-id="2266c-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2266c-206">Is-Single-Valued</span></span>       | <span data-ttu-id="2266c-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="2266c-207">True</span></span>                                                            |
| <span data-ttu-id="2266c-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2266c-208">Is Indexed</span></span>             | <span data-ttu-id="2266c-209">False</span><span class="sxs-lookup"><span data-stu-id="2266c-209">False</span></span>                                                           |
| <span data-ttu-id="2266c-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2266c-210">In Global Catalog</span></span>      | <span data-ttu-id="2266c-211">False</span><span class="sxs-lookup"><span data-stu-id="2266c-211">False</span></span>                                                           |
| <span data-ttu-id="2266c-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2266c-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="2266c-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2266c-213">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="2266c-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2266c-214">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="2266c-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2266c-215">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="2266c-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2266c-216">Search-Flags</span></span>           | <span data-ttu-id="2266c-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2266c-217">0x00000000</span></span>                                                      |
| <span data-ttu-id="2266c-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2266c-218">System-Flags</span></span>           | <span data-ttu-id="2266c-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2266c-219">0x00000010</span></span>                                                      |
| <span data-ttu-id="2266c-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2266c-220">Classes used in</span></span>        | [<span data-ttu-id="2266c-221">**MS-IEEE-80211-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="2266c-221">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2266c-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2266c-222">Windows Server 2012</span></span>



| <span data-ttu-id="2266c-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2266c-223">Entry</span></span> | <span data-ttu-id="2266c-224">Wert</span><span class="sxs-lookup"><span data-stu-id="2266c-224">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="2266c-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2266c-225">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2266c-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2266c-226">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="2266c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="2266c-227">System-Only</span></span>            | <span data-ttu-id="2266c-228">False</span><span class="sxs-lookup"><span data-stu-id="2266c-228">False</span></span>                                                           |
| <span data-ttu-id="2266c-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2266c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="2266c-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="2266c-230">True</span></span>                                                            |
| <span data-ttu-id="2266c-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2266c-231">Is Indexed</span></span>             | <span data-ttu-id="2266c-232">False</span><span class="sxs-lookup"><span data-stu-id="2266c-232">False</span></span>                                                           |
| <span data-ttu-id="2266c-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2266c-233">In Global Catalog</span></span>      | <span data-ttu-id="2266c-234">False</span><span class="sxs-lookup"><span data-stu-id="2266c-234">False</span></span>                                                           |
| <span data-ttu-id="2266c-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2266c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="2266c-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2266c-236">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="2266c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2266c-237">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="2266c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2266c-238">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="2266c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2266c-239">Search-Flags</span></span>           | <span data-ttu-id="2266c-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2266c-240">0x00000000</span></span>                                                      |
| <span data-ttu-id="2266c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2266c-241">System-Flags</span></span>           | <span data-ttu-id="2266c-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2266c-242">0x00000010</span></span>                                                      |
| <span data-ttu-id="2266c-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2266c-243">Classes used in</span></span>        | [<span data-ttu-id="2266c-244">**MS-IEEE-80211-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="2266c-244">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



 

 





