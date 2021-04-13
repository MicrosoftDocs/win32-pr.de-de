---
title: Site-Link-list-Attribut
description: Liste der Standort Verknüpfungen, die dieser Bridge zugeordnet sind.
ms.assetid: 79ec0ae2-ceb3-4321-8b6d-ce5c3bda667a
ms.tgt_platform: multiple
keywords:
- AD-Schema für Site-Link-list-Attribut
- sitelinklist-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Site-Link-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e71284e4650a3cb146b1656c846483e33a6dd66
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392294"
---
# <a name="site-link-list-attribute"></a><span data-ttu-id="00d5c-105">Site-Link-list-Attribut</span><span class="sxs-lookup"><span data-stu-id="00d5c-105">Site-Link-List attribute</span></span>

<span data-ttu-id="00d5c-106">Liste der Standort Verknüpfungen, die dieser Bridge zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="00d5c-106">List of site links that are associated with this bridge.</span></span>



| <span data-ttu-id="00d5c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="00d5c-107">Entry</span></span> | <span data-ttu-id="00d5c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="00d5c-108">Value</span></span> |
|-------------------|--------------------------------------------------------------|
| <span data-ttu-id="00d5c-109">CN</span><span class="sxs-lookup"><span data-stu-id="00d5c-109">CN</span></span>                | <span data-ttu-id="00d5c-110">Site-Link-List</span><span class="sxs-lookup"><span data-stu-id="00d5c-110">Site-Link-List</span></span>                                               |
| <span data-ttu-id="00d5c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="00d5c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="00d5c-112">sitelinklist</span><span class="sxs-lookup"><span data-stu-id="00d5c-112">siteLinkList</span></span>                                                 |
| <span data-ttu-id="00d5c-113">Size</span><span class="sxs-lookup"><span data-stu-id="00d5c-113">Size</span></span>              | \-                                                           |
| <span data-ttu-id="00d5c-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="00d5c-114">Update Privilege</span></span>  | <span data-ttu-id="00d5c-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="00d5c-115">Domain administrator</span></span>                                         |
| <span data-ttu-id="00d5c-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="00d5c-116">Update Frequency</span></span>  | <span data-ttu-id="00d5c-117">Jedes Mal, wenn der Bridge eine Standort Verknüpfung hinzugefügt oder daraus entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="00d5c-117">Whenever a site link is added to or removed from the bridge.</span></span> |
| <span data-ttu-id="00d5c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="00d5c-118">Attribute-Id</span></span>      | <span data-ttu-id="00d5c-119">1.2.840.113556.1.4.822</span><span class="sxs-lookup"><span data-stu-id="00d5c-119">1.2.840.113556.1.4.822</span></span>                                       |
| <span data-ttu-id="00d5c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="00d5c-120">System-Id-Guid</span></span>    | <span data-ttu-id="00d5c-121">d50c2cdd-8951-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="00d5c-121">d50c2cdd-8951-11d1-aebc-0000f80367c1</span></span>                         |
| <span data-ttu-id="00d5c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="00d5c-122">Syntax</span></span>            | [<span data-ttu-id="00d5c-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="00d5c-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                      |



## <a name="implementations"></a><span data-ttu-id="00d5c-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="00d5c-124">Implementations</span></span>

-   [<span data-ttu-id="00d5c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="00d5c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="00d5c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="00d5c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="00d5c-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="00d5c-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="00d5c-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="00d5c-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="00d5c-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="00d5c-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="00d5c-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="00d5c-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="00d5c-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="00d5c-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="00d5c-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="00d5c-132">Windows 2000 Server</span></span>



| <span data-ttu-id="00d5c-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="00d5c-133">Entry</span></span> | <span data-ttu-id="00d5c-134">Wert</span><span class="sxs-lookup"><span data-stu-id="00d5c-134">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="00d5c-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="00d5c-135">Link-Id</span></span>                | <span data-ttu-id="00d5c-136">142</span><span class="sxs-lookup"><span data-stu-id="00d5c-136">142</span></span>                                                     |
| <span data-ttu-id="00d5c-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d5c-137">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="00d5c-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d5c-138">System-Only</span></span>            | <span data-ttu-id="00d5c-139">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-139">False</span></span>                                                   |
| <span data-ttu-id="00d5c-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="00d5c-140">Is-Single-Valued</span></span>       | <span data-ttu-id="00d5c-141">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-141">False</span></span>                                                   |
| <span data-ttu-id="00d5c-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="00d5c-142">Is Indexed</span></span>             | <span data-ttu-id="00d5c-143">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-143">False</span></span>                                                   |
| <span data-ttu-id="00d5c-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="00d5c-144">In Global Catalog</span></span>      | <span data-ttu-id="00d5c-145">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-145">False</span></span>                                                   |
| <span data-ttu-id="00d5c-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="00d5c-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d5c-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="00d5c-147">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="00d5c-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d5c-148">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="00d5c-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d5c-149">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="00d5c-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d5c-150">Search-Flags</span></span>           | <span data-ttu-id="00d5c-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d5c-151">0x00000000</span></span>                                              |
| <span data-ttu-id="00d5c-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d5c-152">System-Flags</span></span>           | <span data-ttu-id="00d5c-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d5c-153">0x00000010</span></span>                                              |
| <span data-ttu-id="00d5c-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="00d5c-154">Classes used in</span></span>        | [<span data-ttu-id="00d5c-155">**Site-Link-Bridge**</span><span class="sxs-lookup"><span data-stu-id="00d5c-155">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="00d5c-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00d5c-156">Windows Server 2003</span></span>



| <span data-ttu-id="00d5c-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="00d5c-157">Entry</span></span> | <span data-ttu-id="00d5c-158">Wert</span><span class="sxs-lookup"><span data-stu-id="00d5c-158">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="00d5c-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="00d5c-159">Link-Id</span></span>                | <span data-ttu-id="00d5c-160">142</span><span class="sxs-lookup"><span data-stu-id="00d5c-160">142</span></span>                                                     |
| <span data-ttu-id="00d5c-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d5c-161">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="00d5c-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d5c-162">System-Only</span></span>            | <span data-ttu-id="00d5c-163">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-163">False</span></span>                                                   |
| <span data-ttu-id="00d5c-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="00d5c-164">Is-Single-Valued</span></span>       | <span data-ttu-id="00d5c-165">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-165">False</span></span>                                                   |
| <span data-ttu-id="00d5c-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="00d5c-166">Is Indexed</span></span>             | <span data-ttu-id="00d5c-167">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-167">False</span></span>                                                   |
| <span data-ttu-id="00d5c-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="00d5c-168">In Global Catalog</span></span>      | <span data-ttu-id="00d5c-169">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-169">False</span></span>                                                   |
| <span data-ttu-id="00d5c-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="00d5c-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d5c-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="00d5c-171">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="00d5c-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d5c-172">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="00d5c-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d5c-173">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="00d5c-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d5c-174">Search-Flags</span></span>           | <span data-ttu-id="00d5c-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d5c-175">0x00000000</span></span>                                              |
| <span data-ttu-id="00d5c-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d5c-176">System-Flags</span></span>           | <span data-ttu-id="00d5c-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d5c-177">0x00000010</span></span>                                              |
| <span data-ttu-id="00d5c-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="00d5c-178">Classes used in</span></span>        | [<span data-ttu-id="00d5c-179">**Site-Link-Bridge**</span><span class="sxs-lookup"><span data-stu-id="00d5c-179">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="adam"></a><span data-ttu-id="00d5c-180">Adam</span><span class="sxs-lookup"><span data-stu-id="00d5c-180">ADAM</span></span>



| <span data-ttu-id="00d5c-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="00d5c-181">Entry</span></span> | <span data-ttu-id="00d5c-182">Wert</span><span class="sxs-lookup"><span data-stu-id="00d5c-182">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="00d5c-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="00d5c-183">Link-Id</span></span>                | <span data-ttu-id="00d5c-184">142</span><span class="sxs-lookup"><span data-stu-id="00d5c-184">142</span></span>                                                     |
| <span data-ttu-id="00d5c-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d5c-185">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="00d5c-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d5c-186">System-Only</span></span>            | <span data-ttu-id="00d5c-187">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-187">False</span></span>                                                   |
| <span data-ttu-id="00d5c-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="00d5c-188">Is-Single-Valued</span></span>       | <span data-ttu-id="00d5c-189">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-189">False</span></span>                                                   |
| <span data-ttu-id="00d5c-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="00d5c-190">Is Indexed</span></span>             | <span data-ttu-id="00d5c-191">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-191">False</span></span>                                                   |
| <span data-ttu-id="00d5c-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="00d5c-192">In Global Catalog</span></span>      | <span data-ttu-id="00d5c-193">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-193">False</span></span>                                                   |
| <span data-ttu-id="00d5c-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="00d5c-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d5c-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="00d5c-195">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="00d5c-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d5c-196">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="00d5c-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d5c-197">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="00d5c-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d5c-198">Search-Flags</span></span>           | <span data-ttu-id="00d5c-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d5c-199">0x00000000</span></span>                                              |
| <span data-ttu-id="00d5c-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d5c-200">System-Flags</span></span>           | <span data-ttu-id="00d5c-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d5c-201">0x00000010</span></span>                                              |
| <span data-ttu-id="00d5c-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="00d5c-202">Classes used in</span></span>        | [<span data-ttu-id="00d5c-203">**Site-Link-Bridge**</span><span class="sxs-lookup"><span data-stu-id="00d5c-203">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="00d5c-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="00d5c-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="00d5c-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="00d5c-205">Entry</span></span> | <span data-ttu-id="00d5c-206">Wert</span><span class="sxs-lookup"><span data-stu-id="00d5c-206">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="00d5c-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="00d5c-207">Link-Id</span></span>                | <span data-ttu-id="00d5c-208">142</span><span class="sxs-lookup"><span data-stu-id="00d5c-208">142</span></span>                                                     |
| <span data-ttu-id="00d5c-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d5c-209">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="00d5c-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d5c-210">System-Only</span></span>            | <span data-ttu-id="00d5c-211">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-211">False</span></span>                                                   |
| <span data-ttu-id="00d5c-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="00d5c-212">Is-Single-Valued</span></span>       | <span data-ttu-id="00d5c-213">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-213">False</span></span>                                                   |
| <span data-ttu-id="00d5c-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="00d5c-214">Is Indexed</span></span>             | <span data-ttu-id="00d5c-215">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-215">False</span></span>                                                   |
| <span data-ttu-id="00d5c-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="00d5c-216">In Global Catalog</span></span>      | <span data-ttu-id="00d5c-217">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-217">False</span></span>                                                   |
| <span data-ttu-id="00d5c-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="00d5c-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d5c-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="00d5c-219">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="00d5c-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d5c-220">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="00d5c-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d5c-221">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="00d5c-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d5c-222">Search-Flags</span></span>           | <span data-ttu-id="00d5c-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d5c-223">0x00000000</span></span>                                              |
| <span data-ttu-id="00d5c-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d5c-224">System-Flags</span></span>           | <span data-ttu-id="00d5c-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d5c-225">0x00000010</span></span>                                              |
| <span data-ttu-id="00d5c-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="00d5c-226">Classes used in</span></span>        | [<span data-ttu-id="00d5c-227">**Site-Link-Bridge**</span><span class="sxs-lookup"><span data-stu-id="00d5c-227">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="00d5c-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00d5c-228">Windows Server 2008</span></span>



| <span data-ttu-id="00d5c-229">Eingabe</span><span class="sxs-lookup"><span data-stu-id="00d5c-229">Entry</span></span> | <span data-ttu-id="00d5c-230">Wert</span><span class="sxs-lookup"><span data-stu-id="00d5c-230">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="00d5c-231">Link-ID</span><span class="sxs-lookup"><span data-stu-id="00d5c-231">Link-Id</span></span>                | <span data-ttu-id="00d5c-232">142</span><span class="sxs-lookup"><span data-stu-id="00d5c-232">142</span></span>                                                     |
| <span data-ttu-id="00d5c-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d5c-233">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="00d5c-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d5c-234">System-Only</span></span>            | <span data-ttu-id="00d5c-235">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-235">False</span></span>                                                   |
| <span data-ttu-id="00d5c-236">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="00d5c-236">Is-Single-Valued</span></span>       | <span data-ttu-id="00d5c-237">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-237">False</span></span>                                                   |
| <span data-ttu-id="00d5c-238">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="00d5c-238">Is Indexed</span></span>             | <span data-ttu-id="00d5c-239">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-239">False</span></span>                                                   |
| <span data-ttu-id="00d5c-240">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="00d5c-240">In Global Catalog</span></span>      | <span data-ttu-id="00d5c-241">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-241">False</span></span>                                                   |
| <span data-ttu-id="00d5c-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="00d5c-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d5c-243">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="00d5c-243">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="00d5c-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d5c-244">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="00d5c-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d5c-245">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="00d5c-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d5c-246">Search-Flags</span></span>           | <span data-ttu-id="00d5c-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d5c-247">0x00000000</span></span>                                              |
| <span data-ttu-id="00d5c-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d5c-248">System-Flags</span></span>           | <span data-ttu-id="00d5c-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d5c-249">0x00000010</span></span>                                              |
| <span data-ttu-id="00d5c-250">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="00d5c-250">Classes used in</span></span>        | [<span data-ttu-id="00d5c-251">**Site-Link-Bridge**</span><span class="sxs-lookup"><span data-stu-id="00d5c-251">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="00d5c-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="00d5c-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="00d5c-253">Eingabe</span><span class="sxs-lookup"><span data-stu-id="00d5c-253">Entry</span></span> | <span data-ttu-id="00d5c-254">Wert</span><span class="sxs-lookup"><span data-stu-id="00d5c-254">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="00d5c-255">Link-ID</span><span class="sxs-lookup"><span data-stu-id="00d5c-255">Link-Id</span></span>                | <span data-ttu-id="00d5c-256">142</span><span class="sxs-lookup"><span data-stu-id="00d5c-256">142</span></span>                                                     |
| <span data-ttu-id="00d5c-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d5c-257">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="00d5c-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d5c-258">System-Only</span></span>            | <span data-ttu-id="00d5c-259">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-259">False</span></span>                                                   |
| <span data-ttu-id="00d5c-260">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="00d5c-260">Is-Single-Valued</span></span>       | <span data-ttu-id="00d5c-261">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-261">False</span></span>                                                   |
| <span data-ttu-id="00d5c-262">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="00d5c-262">Is Indexed</span></span>             | <span data-ttu-id="00d5c-263">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-263">False</span></span>                                                   |
| <span data-ttu-id="00d5c-264">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="00d5c-264">In Global Catalog</span></span>      | <span data-ttu-id="00d5c-265">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-265">False</span></span>                                                   |
| <span data-ttu-id="00d5c-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="00d5c-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d5c-267">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="00d5c-267">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="00d5c-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d5c-268">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="00d5c-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d5c-269">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="00d5c-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d5c-270">Search-Flags</span></span>           | <span data-ttu-id="00d5c-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d5c-271">0x00000000</span></span>                                              |
| <span data-ttu-id="00d5c-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d5c-272">System-Flags</span></span>           | <span data-ttu-id="00d5c-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d5c-273">0x00000010</span></span>                                              |
| <span data-ttu-id="00d5c-274">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="00d5c-274">Classes used in</span></span>        | [<span data-ttu-id="00d5c-275">**Site-Link-Bridge**</span><span class="sxs-lookup"><span data-stu-id="00d5c-275">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="00d5c-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="00d5c-276">Windows Server 2012</span></span>



| <span data-ttu-id="00d5c-277">Eingabe</span><span class="sxs-lookup"><span data-stu-id="00d5c-277">Entry</span></span> | <span data-ttu-id="00d5c-278">Wert</span><span class="sxs-lookup"><span data-stu-id="00d5c-278">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="00d5c-279">Link-ID</span><span class="sxs-lookup"><span data-stu-id="00d5c-279">Link-Id</span></span>                | <span data-ttu-id="00d5c-280">142</span><span class="sxs-lookup"><span data-stu-id="00d5c-280">142</span></span>                                                     |
| <span data-ttu-id="00d5c-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d5c-281">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="00d5c-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d5c-282">System-Only</span></span>            | <span data-ttu-id="00d5c-283">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-283">False</span></span>                                                   |
| <span data-ttu-id="00d5c-284">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="00d5c-284">Is-Single-Valued</span></span>       | <span data-ttu-id="00d5c-285">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-285">False</span></span>                                                   |
| <span data-ttu-id="00d5c-286">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="00d5c-286">Is Indexed</span></span>             | <span data-ttu-id="00d5c-287">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-287">False</span></span>                                                   |
| <span data-ttu-id="00d5c-288">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="00d5c-288">In Global Catalog</span></span>      | <span data-ttu-id="00d5c-289">False</span><span class="sxs-lookup"><span data-stu-id="00d5c-289">False</span></span>                                                   |
| <span data-ttu-id="00d5c-290">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="00d5c-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d5c-291">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="00d5c-291">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="00d5c-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d5c-292">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="00d5c-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d5c-293">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="00d5c-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d5c-294">Search-Flags</span></span>           | <span data-ttu-id="00d5c-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d5c-295">0x00000000</span></span>                                              |
| <span data-ttu-id="00d5c-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d5c-296">System-Flags</span></span>           | <span data-ttu-id="00d5c-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d5c-297">0x00000010</span></span>                                              |
| <span data-ttu-id="00d5c-298">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="00d5c-298">Classes used in</span></span>        | [<span data-ttu-id="00d5c-299">**Site-Link-Bridge**</span><span class="sxs-lookup"><span data-stu-id="00d5c-299">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



 

 





