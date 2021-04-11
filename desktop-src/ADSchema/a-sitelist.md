---
title: Site-List-Attribut
description: Liste der mit diesem Link Objekt verbundenen Websites.
ms.assetid: c27dece1-513d-450e-b777-6fc7172d970a
ms.tgt_platform: multiple
keywords:
- AD-Schema für Site-List-Attribut
- sitelist-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Site-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3be0fcdc67fc07693a1354e589f67b7efe3f00a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107517"
---
# <a name="site-list-attribute"></a><span data-ttu-id="71e6b-105">Site-List-Attribut</span><span class="sxs-lookup"><span data-stu-id="71e6b-105">Site-List attribute</span></span>

<span data-ttu-id="71e6b-106">Liste der mit diesem Link Objekt verbundenen Websites.</span><span class="sxs-lookup"><span data-stu-id="71e6b-106">List of sites connected to this link object.</span></span>



| <span data-ttu-id="71e6b-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="71e6b-107">Entry</span></span> | <span data-ttu-id="71e6b-108">Wert</span><span class="sxs-lookup"><span data-stu-id="71e6b-108">Value</span></span> |
|-------------------|----------------------------------------------|
| <span data-ttu-id="71e6b-109">CN</span><span class="sxs-lookup"><span data-stu-id="71e6b-109">CN</span></span>                | <span data-ttu-id="71e6b-110">Site-List</span><span class="sxs-lookup"><span data-stu-id="71e6b-110">Site-List</span></span>                                    |
| <span data-ttu-id="71e6b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="71e6b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="71e6b-112">sitelist</span><span class="sxs-lookup"><span data-stu-id="71e6b-112">siteList</span></span>                                     |
| <span data-ttu-id="71e6b-113">Size</span><span class="sxs-lookup"><span data-stu-id="71e6b-113">Size</span></span>              | \-                                           |
| <span data-ttu-id="71e6b-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="71e6b-114">Update Privilege</span></span>  | <span data-ttu-id="71e6b-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="71e6b-115">Domain administrator</span></span>                         |
| <span data-ttu-id="71e6b-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="71e6b-116">Update Frequency</span></span>  | <span data-ttu-id="71e6b-117">Jedes Mal, wenn eine Site hinzugefügt oder daraus entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="71e6b-117">Whenever a site is added to or removed from.</span></span> |
| <span data-ttu-id="71e6b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="71e6b-118">Attribute-Id</span></span>      | <span data-ttu-id="71e6b-119">1.2.840.113556.1.4.821</span><span class="sxs-lookup"><span data-stu-id="71e6b-119">1.2.840.113556.1.4.821</span></span>                       |
| <span data-ttu-id="71e6b-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="71e6b-120">System-Id-Guid</span></span>    | <span data-ttu-id="71e6b-121">d50c2cdc-8951-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="71e6b-121">d50c2cdc-8951-11d1-aebc-0000f80367c1</span></span>         |
| <span data-ttu-id="71e6b-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="71e6b-122">Syntax</span></span>            | [<span data-ttu-id="71e6b-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="71e6b-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)      |



## <a name="implementations"></a><span data-ttu-id="71e6b-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="71e6b-124">Implementations</span></span>

-   [<span data-ttu-id="71e6b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="71e6b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="71e6b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="71e6b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="71e6b-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="71e6b-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="71e6b-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="71e6b-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="71e6b-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="71e6b-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="71e6b-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="71e6b-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="71e6b-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="71e6b-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="71e6b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="71e6b-132">Windows 2000 Server</span></span>



| <span data-ttu-id="71e6b-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="71e6b-133">Entry</span></span> | <span data-ttu-id="71e6b-134">Wert</span><span class="sxs-lookup"><span data-stu-id="71e6b-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="71e6b-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="71e6b-135">Link-Id</span></span>                | <span data-ttu-id="71e6b-136">144</span><span class="sxs-lookup"><span data-stu-id="71e6b-136">144</span></span>                                        |
| <span data-ttu-id="71e6b-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71e6b-137">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="71e6b-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="71e6b-138">System-Only</span></span>            | <span data-ttu-id="71e6b-139">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-139">False</span></span>                                      |
| <span data-ttu-id="71e6b-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="71e6b-140">Is-Single-Valued</span></span>       | <span data-ttu-id="71e6b-141">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-141">False</span></span>                                      |
| <span data-ttu-id="71e6b-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="71e6b-142">Is Indexed</span></span>             | <span data-ttu-id="71e6b-143">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-143">False</span></span>                                      |
| <span data-ttu-id="71e6b-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="71e6b-144">In Global Catalog</span></span>      | <span data-ttu-id="71e6b-145">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-145">False</span></span>                                      |
| <span data-ttu-id="71e6b-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71e6b-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="71e6b-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="71e6b-147">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="71e6b-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71e6b-148">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="71e6b-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71e6b-149">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="71e6b-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71e6b-150">Search-Flags</span></span>           | <span data-ttu-id="71e6b-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71e6b-151">0x00000000</span></span>                                 |
| <span data-ttu-id="71e6b-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71e6b-152">System-Flags</span></span>           | <span data-ttu-id="71e6b-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71e6b-153">0x00000010</span></span>                                 |
| <span data-ttu-id="71e6b-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="71e6b-154">Classes used in</span></span>        | [<span data-ttu-id="71e6b-155">**Standort Link**</span><span class="sxs-lookup"><span data-stu-id="71e6b-155">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="71e6b-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="71e6b-156">Windows Server 2003</span></span>



| <span data-ttu-id="71e6b-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="71e6b-157">Entry</span></span> | <span data-ttu-id="71e6b-158">Wert</span><span class="sxs-lookup"><span data-stu-id="71e6b-158">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="71e6b-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="71e6b-159">Link-Id</span></span>                | <span data-ttu-id="71e6b-160">144</span><span class="sxs-lookup"><span data-stu-id="71e6b-160">144</span></span>                                        |
| <span data-ttu-id="71e6b-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71e6b-161">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="71e6b-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="71e6b-162">System-Only</span></span>            | <span data-ttu-id="71e6b-163">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-163">False</span></span>                                      |
| <span data-ttu-id="71e6b-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="71e6b-164">Is-Single-Valued</span></span>       | <span data-ttu-id="71e6b-165">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-165">False</span></span>                                      |
| <span data-ttu-id="71e6b-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="71e6b-166">Is Indexed</span></span>             | <span data-ttu-id="71e6b-167">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-167">False</span></span>                                      |
| <span data-ttu-id="71e6b-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="71e6b-168">In Global Catalog</span></span>      | <span data-ttu-id="71e6b-169">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-169">False</span></span>                                      |
| <span data-ttu-id="71e6b-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71e6b-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="71e6b-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="71e6b-171">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="71e6b-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71e6b-172">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="71e6b-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71e6b-173">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="71e6b-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71e6b-174">Search-Flags</span></span>           | <span data-ttu-id="71e6b-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71e6b-175">0x00000000</span></span>                                 |
| <span data-ttu-id="71e6b-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71e6b-176">System-Flags</span></span>           | <span data-ttu-id="71e6b-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71e6b-177">0x00000010</span></span>                                 |
| <span data-ttu-id="71e6b-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="71e6b-178">Classes used in</span></span>        | [<span data-ttu-id="71e6b-179">**Standort Link**</span><span class="sxs-lookup"><span data-stu-id="71e6b-179">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="adam"></a><span data-ttu-id="71e6b-180">Adam</span><span class="sxs-lookup"><span data-stu-id="71e6b-180">ADAM</span></span>



| <span data-ttu-id="71e6b-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="71e6b-181">Entry</span></span> | <span data-ttu-id="71e6b-182">Wert</span><span class="sxs-lookup"><span data-stu-id="71e6b-182">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="71e6b-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="71e6b-183">Link-Id</span></span>                | <span data-ttu-id="71e6b-184">144</span><span class="sxs-lookup"><span data-stu-id="71e6b-184">144</span></span>                                        |
| <span data-ttu-id="71e6b-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71e6b-185">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="71e6b-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="71e6b-186">System-Only</span></span>            | <span data-ttu-id="71e6b-187">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-187">False</span></span>                                      |
| <span data-ttu-id="71e6b-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="71e6b-188">Is-Single-Valued</span></span>       | <span data-ttu-id="71e6b-189">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-189">False</span></span>                                      |
| <span data-ttu-id="71e6b-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="71e6b-190">Is Indexed</span></span>             | <span data-ttu-id="71e6b-191">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-191">False</span></span>                                      |
| <span data-ttu-id="71e6b-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="71e6b-192">In Global Catalog</span></span>      | <span data-ttu-id="71e6b-193">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-193">False</span></span>                                      |
| <span data-ttu-id="71e6b-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71e6b-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="71e6b-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="71e6b-195">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="71e6b-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71e6b-196">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="71e6b-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71e6b-197">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="71e6b-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71e6b-198">Search-Flags</span></span>           | <span data-ttu-id="71e6b-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71e6b-199">0x00000000</span></span>                                 |
| <span data-ttu-id="71e6b-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71e6b-200">System-Flags</span></span>           | <span data-ttu-id="71e6b-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71e6b-201">0x00000010</span></span>                                 |
| <span data-ttu-id="71e6b-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="71e6b-202">Classes used in</span></span>        | [<span data-ttu-id="71e6b-203">**Standort Link**</span><span class="sxs-lookup"><span data-stu-id="71e6b-203">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="71e6b-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="71e6b-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="71e6b-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="71e6b-205">Entry</span></span> | <span data-ttu-id="71e6b-206">Wert</span><span class="sxs-lookup"><span data-stu-id="71e6b-206">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="71e6b-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="71e6b-207">Link-Id</span></span>                | <span data-ttu-id="71e6b-208">144</span><span class="sxs-lookup"><span data-stu-id="71e6b-208">144</span></span>                                        |
| <span data-ttu-id="71e6b-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71e6b-209">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="71e6b-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="71e6b-210">System-Only</span></span>            | <span data-ttu-id="71e6b-211">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-211">False</span></span>                                      |
| <span data-ttu-id="71e6b-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="71e6b-212">Is-Single-Valued</span></span>       | <span data-ttu-id="71e6b-213">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-213">False</span></span>                                      |
| <span data-ttu-id="71e6b-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="71e6b-214">Is Indexed</span></span>             | <span data-ttu-id="71e6b-215">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-215">False</span></span>                                      |
| <span data-ttu-id="71e6b-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="71e6b-216">In Global Catalog</span></span>      | <span data-ttu-id="71e6b-217">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-217">False</span></span>                                      |
| <span data-ttu-id="71e6b-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71e6b-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="71e6b-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="71e6b-219">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="71e6b-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71e6b-220">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="71e6b-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71e6b-221">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="71e6b-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71e6b-222">Search-Flags</span></span>           | <span data-ttu-id="71e6b-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71e6b-223">0x00000000</span></span>                                 |
| <span data-ttu-id="71e6b-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71e6b-224">System-Flags</span></span>           | <span data-ttu-id="71e6b-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71e6b-225">0x00000010</span></span>                                 |
| <span data-ttu-id="71e6b-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="71e6b-226">Classes used in</span></span>        | [<span data-ttu-id="71e6b-227">**Standort Link**</span><span class="sxs-lookup"><span data-stu-id="71e6b-227">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="71e6b-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71e6b-228">Windows Server 2008</span></span>



| <span data-ttu-id="71e6b-229">Eingabe</span><span class="sxs-lookup"><span data-stu-id="71e6b-229">Entry</span></span> | <span data-ttu-id="71e6b-230">Wert</span><span class="sxs-lookup"><span data-stu-id="71e6b-230">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="71e6b-231">Link-ID</span><span class="sxs-lookup"><span data-stu-id="71e6b-231">Link-Id</span></span>                | <span data-ttu-id="71e6b-232">144</span><span class="sxs-lookup"><span data-stu-id="71e6b-232">144</span></span>                                        |
| <span data-ttu-id="71e6b-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71e6b-233">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="71e6b-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="71e6b-234">System-Only</span></span>            | <span data-ttu-id="71e6b-235">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-235">False</span></span>                                      |
| <span data-ttu-id="71e6b-236">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="71e6b-236">Is-Single-Valued</span></span>       | <span data-ttu-id="71e6b-237">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-237">False</span></span>                                      |
| <span data-ttu-id="71e6b-238">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="71e6b-238">Is Indexed</span></span>             | <span data-ttu-id="71e6b-239">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-239">False</span></span>                                      |
| <span data-ttu-id="71e6b-240">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="71e6b-240">In Global Catalog</span></span>      | <span data-ttu-id="71e6b-241">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-241">False</span></span>                                      |
| <span data-ttu-id="71e6b-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71e6b-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="71e6b-243">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="71e6b-243">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="71e6b-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71e6b-244">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="71e6b-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71e6b-245">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="71e6b-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71e6b-246">Search-Flags</span></span>           | <span data-ttu-id="71e6b-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71e6b-247">0x00000000</span></span>                                 |
| <span data-ttu-id="71e6b-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71e6b-248">System-Flags</span></span>           | <span data-ttu-id="71e6b-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71e6b-249">0x00000010</span></span>                                 |
| <span data-ttu-id="71e6b-250">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="71e6b-250">Classes used in</span></span>        | [<span data-ttu-id="71e6b-251">**Standort Link**</span><span class="sxs-lookup"><span data-stu-id="71e6b-251">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="71e6b-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="71e6b-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="71e6b-253">Eingabe</span><span class="sxs-lookup"><span data-stu-id="71e6b-253">Entry</span></span> | <span data-ttu-id="71e6b-254">Wert</span><span class="sxs-lookup"><span data-stu-id="71e6b-254">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="71e6b-255">Link-ID</span><span class="sxs-lookup"><span data-stu-id="71e6b-255">Link-Id</span></span>                | <span data-ttu-id="71e6b-256">144</span><span class="sxs-lookup"><span data-stu-id="71e6b-256">144</span></span>                                        |
| <span data-ttu-id="71e6b-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71e6b-257">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="71e6b-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="71e6b-258">System-Only</span></span>            | <span data-ttu-id="71e6b-259">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-259">False</span></span>                                      |
| <span data-ttu-id="71e6b-260">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="71e6b-260">Is-Single-Valued</span></span>       | <span data-ttu-id="71e6b-261">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-261">False</span></span>                                      |
| <span data-ttu-id="71e6b-262">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="71e6b-262">Is Indexed</span></span>             | <span data-ttu-id="71e6b-263">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-263">False</span></span>                                      |
| <span data-ttu-id="71e6b-264">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="71e6b-264">In Global Catalog</span></span>      | <span data-ttu-id="71e6b-265">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-265">False</span></span>                                      |
| <span data-ttu-id="71e6b-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71e6b-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="71e6b-267">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="71e6b-267">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="71e6b-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71e6b-268">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="71e6b-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71e6b-269">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="71e6b-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71e6b-270">Search-Flags</span></span>           | <span data-ttu-id="71e6b-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71e6b-271">0x00000000</span></span>                                 |
| <span data-ttu-id="71e6b-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71e6b-272">System-Flags</span></span>           | <span data-ttu-id="71e6b-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71e6b-273">0x00000010</span></span>                                 |
| <span data-ttu-id="71e6b-274">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="71e6b-274">Classes used in</span></span>        | [<span data-ttu-id="71e6b-275">**Standort Link**</span><span class="sxs-lookup"><span data-stu-id="71e6b-275">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="71e6b-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="71e6b-276">Windows Server 2012</span></span>



| <span data-ttu-id="71e6b-277">Eingabe</span><span class="sxs-lookup"><span data-stu-id="71e6b-277">Entry</span></span> | <span data-ttu-id="71e6b-278">Wert</span><span class="sxs-lookup"><span data-stu-id="71e6b-278">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="71e6b-279">Link-ID</span><span class="sxs-lookup"><span data-stu-id="71e6b-279">Link-Id</span></span>                | <span data-ttu-id="71e6b-280">144</span><span class="sxs-lookup"><span data-stu-id="71e6b-280">144</span></span>                                        |
| <span data-ttu-id="71e6b-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71e6b-281">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="71e6b-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="71e6b-282">System-Only</span></span>            | <span data-ttu-id="71e6b-283">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-283">False</span></span>                                      |
| <span data-ttu-id="71e6b-284">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="71e6b-284">Is-Single-Valued</span></span>       | <span data-ttu-id="71e6b-285">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-285">False</span></span>                                      |
| <span data-ttu-id="71e6b-286">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="71e6b-286">Is Indexed</span></span>             | <span data-ttu-id="71e6b-287">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-287">False</span></span>                                      |
| <span data-ttu-id="71e6b-288">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="71e6b-288">In Global Catalog</span></span>      | <span data-ttu-id="71e6b-289">False</span><span class="sxs-lookup"><span data-stu-id="71e6b-289">False</span></span>                                      |
| <span data-ttu-id="71e6b-290">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71e6b-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="71e6b-291">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="71e6b-291">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="71e6b-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71e6b-292">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="71e6b-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71e6b-293">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="71e6b-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71e6b-294">Search-Flags</span></span>           | <span data-ttu-id="71e6b-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71e6b-295">0x00000000</span></span>                                 |
| <span data-ttu-id="71e6b-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71e6b-296">System-Flags</span></span>           | <span data-ttu-id="71e6b-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71e6b-297">0x00000010</span></span>                                 |
| <span data-ttu-id="71e6b-298">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="71e6b-298">Classes used in</span></span>        | [<span data-ttu-id="71e6b-299">**Standort Link**</span><span class="sxs-lookup"><span data-stu-id="71e6b-299">**Site-Link**</span></span>](c-sitelink.md)<br/> |



 

 





