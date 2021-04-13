---
title: Owner-Attribut
description: Der Distinguished Name eines Objekts, das den Besitz eines Objekts besitzt.
ms.assetid: 37b0e8eb-fe33-494a-9e1f-264cf9211344
ms.tgt_platform: multiple
keywords:
- AD-Schema für Besitzer Attribut
- AD-Schema für Besitzer Attribut
topic_type:
- apiref
api_name:
- Owner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d416158fea3fd0e3dfbda1cd60b2543d3df16248
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104520055"
---
# <a name="owner-attribute"></a><span data-ttu-id="7eeb6-105">Owner-Attribut</span><span class="sxs-lookup"><span data-stu-id="7eeb6-105">Owner attribute</span></span>

<span data-ttu-id="7eeb6-106">Der Distinguished Name eines Objekts, das den Besitz eines Objekts besitzt.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-106">The distinguished name of an object that has ownership of an object.</span></span>



| <span data-ttu-id="7eeb6-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7eeb6-107">Entry</span></span> | <span data-ttu-id="7eeb6-108">Wert</span><span class="sxs-lookup"><span data-stu-id="7eeb6-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="7eeb6-109">CN</span><span class="sxs-lookup"><span data-stu-id="7eeb6-109">CN</span></span>                | <span data-ttu-id="7eeb6-110">Besitzer</span><span class="sxs-lookup"><span data-stu-id="7eeb6-110">Owner</span></span>                                   |
| <span data-ttu-id="7eeb6-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7eeb6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7eeb6-112">owner</span><span class="sxs-lookup"><span data-stu-id="7eeb6-112">owner</span></span>                                   |
| <span data-ttu-id="7eeb6-113">Size</span><span class="sxs-lookup"><span data-stu-id="7eeb6-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="7eeb6-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="7eeb6-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="7eeb6-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="7eeb6-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="7eeb6-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7eeb6-116">Attribute-Id</span></span>      | <span data-ttu-id="7eeb6-117">2.5.4.32</span><span class="sxs-lookup"><span data-stu-id="7eeb6-117">2.5.4.32</span></span>                                |
| <span data-ttu-id="7eeb6-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7eeb6-118">System-Id-Guid</span></span>    | <span data-ttu-id="7eeb6-119">bf9679f3-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7eeb6-119">bf9679f3-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="7eeb6-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="7eeb6-120">Syntax</span></span>            | [<span data-ttu-id="7eeb6-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="7eeb6-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="7eeb6-122">Implementations</span></span>

-   [<span data-ttu-id="7eeb6-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7eeb6-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7eeb6-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7eeb6-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7eeb6-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7eeb6-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7eeb6-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7eeb6-129">Windows 2000 Server</span></span>



| <span data-ttu-id="7eeb6-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7eeb6-130">Entry</span></span> | <span data-ttu-id="7eeb6-131">Wert</span><span class="sxs-lookup"><span data-stu-id="7eeb6-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eeb6-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7eeb6-132">Link-Id</span></span>                | <span data-ttu-id="7eeb6-133">44</span><span class="sxs-lookup"><span data-stu-id="7eeb6-133">44</span></span>                                                                                        |
| <span data-ttu-id="7eeb6-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7eeb6-134">MAPI-Id</span></span>                | \-                                                                                        |
| <span data-ttu-id="7eeb6-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7eeb6-135">System-Only</span></span>            | <span data-ttu-id="7eeb6-136">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-136">False</span></span>                                                                                     |
| <span data-ttu-id="7eeb6-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7eeb6-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7eeb6-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="7eeb6-138">True</span></span>                                                                                      |
| <span data-ttu-id="7eeb6-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7eeb6-139">Is Indexed</span></span>             | <span data-ttu-id="7eeb6-140">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-140">False</span></span>                                                                                     |
| <span data-ttu-id="7eeb6-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7eeb6-141">In Global Catalog</span></span>      | <span data-ttu-id="7eeb6-142">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-142">False</span></span>                                                                                     |
| <span data-ttu-id="7eeb6-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7eeb6-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7eeb6-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7eeb6-144">O:BAG:BAD:S:</span></span>                                                                              |
| <span data-ttu-id="7eeb6-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7eeb6-145">Range-Lower</span></span>            | \-                                                                                        |
| <span data-ttu-id="7eeb6-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7eeb6-146">Range-Upper</span></span>            | \-                                                                                        |
| <span data-ttu-id="7eeb6-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7eeb6-147">Search-Flags</span></span>           | <span data-ttu-id="7eeb6-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7eeb6-148">0x00000000</span></span>                                                                                |
| <span data-ttu-id="7eeb6-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7eeb6-149">System-Flags</span></span>           | <span data-ttu-id="7eeb6-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7eeb6-150">0x00000010</span></span>                                                                                |
| <span data-ttu-id="7eeb6-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7eeb6-151">Classes used in</span></span>        | [<span data-ttu-id="7eeb6-152">**Schutz**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-152">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="7eeb6-153">**Gruppe von Namen**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-153">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7eeb6-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7eeb6-154">Windows Server 2003</span></span>



| <span data-ttu-id="7eeb6-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7eeb6-155">Entry</span></span> | <span data-ttu-id="7eeb6-156">Wert</span><span class="sxs-lookup"><span data-stu-id="7eeb6-156">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eeb6-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7eeb6-157">Link-Id</span></span>                | <span data-ttu-id="7eeb6-158">44</span><span class="sxs-lookup"><span data-stu-id="7eeb6-158">44</span></span>                                                                                                                                                      |
| <span data-ttu-id="7eeb6-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7eeb6-159">MAPI-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="7eeb6-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="7eeb6-160">System-Only</span></span>            | <span data-ttu-id="7eeb6-161">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-161">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="7eeb6-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7eeb6-162">Is-Single-Valued</span></span>       | <span data-ttu-id="7eeb6-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="7eeb6-163">True</span></span>                                                                                                                                                    |
| <span data-ttu-id="7eeb6-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7eeb6-164">Is Indexed</span></span>             | <span data-ttu-id="7eeb6-165">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-165">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="7eeb6-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7eeb6-166">In Global Catalog</span></span>      | <span data-ttu-id="7eeb6-167">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-167">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="7eeb6-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7eeb6-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="7eeb6-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7eeb6-169">O:BAG:BAD:S:</span></span>                                                                                                                                            |
| <span data-ttu-id="7eeb6-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7eeb6-170">Range-Lower</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="7eeb6-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7eeb6-171">Range-Upper</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="7eeb6-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7eeb6-172">Search-Flags</span></span>           | <span data-ttu-id="7eeb6-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7eeb6-173">0x00000000</span></span>                                                                                                                                              |
| <span data-ttu-id="7eeb6-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7eeb6-174">System-Flags</span></span>           | <span data-ttu-id="7eeb6-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7eeb6-175">0x00000010</span></span>                                                                                                                                              |
| <span data-ttu-id="7eeb6-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7eeb6-176">Classes used in</span></span>        | [<span data-ttu-id="7eeb6-177">**Schutz**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-177">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="7eeb6-178">**Gruppe von Namen**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-178">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="7eeb6-179">**groupof uniquumames**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-179">**groupOfUniqueNames**</span></span>](c-groupofuniquenames.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7eeb6-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7eeb6-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7eeb6-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7eeb6-181">Entry</span></span> | <span data-ttu-id="7eeb6-182">Wert</span><span class="sxs-lookup"><span data-stu-id="7eeb6-182">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eeb6-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7eeb6-183">Link-Id</span></span>                | <span data-ttu-id="7eeb6-184">44</span><span class="sxs-lookup"><span data-stu-id="7eeb6-184">44</span></span>                                                                                                                                                      |
| <span data-ttu-id="7eeb6-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7eeb6-185">MAPI-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="7eeb6-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="7eeb6-186">System-Only</span></span>            | <span data-ttu-id="7eeb6-187">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-187">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="7eeb6-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7eeb6-188">Is-Single-Valued</span></span>       | <span data-ttu-id="7eeb6-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="7eeb6-189">True</span></span>                                                                                                                                                    |
| <span data-ttu-id="7eeb6-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7eeb6-190">Is Indexed</span></span>             | <span data-ttu-id="7eeb6-191">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-191">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="7eeb6-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7eeb6-192">In Global Catalog</span></span>      | <span data-ttu-id="7eeb6-193">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-193">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="7eeb6-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7eeb6-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="7eeb6-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7eeb6-195">O:BAG:BAD:S:</span></span>                                                                                                                                            |
| <span data-ttu-id="7eeb6-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7eeb6-196">Range-Lower</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="7eeb6-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7eeb6-197">Range-Upper</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="7eeb6-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7eeb6-198">Search-Flags</span></span>           | <span data-ttu-id="7eeb6-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7eeb6-199">0x00000000</span></span>                                                                                                                                              |
| <span data-ttu-id="7eeb6-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7eeb6-200">System-Flags</span></span>           | <span data-ttu-id="7eeb6-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7eeb6-201">0x00000010</span></span>                                                                                                                                              |
| <span data-ttu-id="7eeb6-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7eeb6-202">Classes used in</span></span>        | [<span data-ttu-id="7eeb6-203">**Schutz**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-203">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="7eeb6-204">**Gruppe von Namen**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-204">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="7eeb6-205">**groupof uniquumames**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-205">**groupOfUniqueNames**</span></span>](c-groupofuniquenames.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7eeb6-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7eeb6-206">Windows Server 2008</span></span>



| <span data-ttu-id="7eeb6-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7eeb6-207">Entry</span></span> | <span data-ttu-id="7eeb6-208">Wert</span><span class="sxs-lookup"><span data-stu-id="7eeb6-208">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eeb6-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7eeb6-209">Link-Id</span></span>                | <span data-ttu-id="7eeb6-210">44</span><span class="sxs-lookup"><span data-stu-id="7eeb6-210">44</span></span>                                                                                                                                                      |
| <span data-ttu-id="7eeb6-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7eeb6-211">MAPI-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="7eeb6-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="7eeb6-212">System-Only</span></span>            | <span data-ttu-id="7eeb6-213">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-213">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="7eeb6-214">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7eeb6-214">Is-Single-Valued</span></span>       | <span data-ttu-id="7eeb6-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="7eeb6-215">True</span></span>                                                                                                                                                    |
| <span data-ttu-id="7eeb6-216">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7eeb6-216">Is Indexed</span></span>             | <span data-ttu-id="7eeb6-217">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-217">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="7eeb6-218">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7eeb6-218">In Global Catalog</span></span>      | <span data-ttu-id="7eeb6-219">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-219">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="7eeb6-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7eeb6-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="7eeb6-221">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7eeb6-221">O:BAG:BAD:S:</span></span>                                                                                                                                            |
| <span data-ttu-id="7eeb6-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7eeb6-222">Range-Lower</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="7eeb6-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7eeb6-223">Range-Upper</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="7eeb6-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7eeb6-224">Search-Flags</span></span>           | <span data-ttu-id="7eeb6-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7eeb6-225">0x00000000</span></span>                                                                                                                                              |
| <span data-ttu-id="7eeb6-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7eeb6-226">System-Flags</span></span>           | <span data-ttu-id="7eeb6-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7eeb6-227">0x00000010</span></span>                                                                                                                                              |
| <span data-ttu-id="7eeb6-228">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7eeb6-228">Classes used in</span></span>        | [<span data-ttu-id="7eeb6-229">**Schutz**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-229">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="7eeb6-230">**Gruppe von Namen**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-230">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="7eeb6-231">**groupof uniquumames**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-231">**groupOfUniqueNames**</span></span>](c-groupofuniquenames.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7eeb6-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7eeb6-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7eeb6-233">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7eeb6-233">Entry</span></span> | <span data-ttu-id="7eeb6-234">Wert</span><span class="sxs-lookup"><span data-stu-id="7eeb6-234">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eeb6-235">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7eeb6-235">Link-Id</span></span>                | <span data-ttu-id="7eeb6-236">44</span><span class="sxs-lookup"><span data-stu-id="7eeb6-236">44</span></span>                                                                                                                                                      |
| <span data-ttu-id="7eeb6-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7eeb6-237">MAPI-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="7eeb6-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="7eeb6-238">System-Only</span></span>            | <span data-ttu-id="7eeb6-239">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-239">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="7eeb6-240">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7eeb6-240">Is-Single-Valued</span></span>       | <span data-ttu-id="7eeb6-241">Richtig</span><span class="sxs-lookup"><span data-stu-id="7eeb6-241">True</span></span>                                                                                                                                                    |
| <span data-ttu-id="7eeb6-242">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7eeb6-242">Is Indexed</span></span>             | <span data-ttu-id="7eeb6-243">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-243">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="7eeb6-244">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7eeb6-244">In Global Catalog</span></span>      | <span data-ttu-id="7eeb6-245">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-245">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="7eeb6-246">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7eeb6-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="7eeb6-247">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7eeb6-247">O:BAG:BAD:S:</span></span>                                                                                                                                            |
| <span data-ttu-id="7eeb6-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7eeb6-248">Range-Lower</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="7eeb6-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7eeb6-249">Range-Upper</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="7eeb6-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7eeb6-250">Search-Flags</span></span>           | <span data-ttu-id="7eeb6-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7eeb6-251">0x00000000</span></span>                                                                                                                                              |
| <span data-ttu-id="7eeb6-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7eeb6-252">System-Flags</span></span>           | <span data-ttu-id="7eeb6-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7eeb6-253">0x00000010</span></span>                                                                                                                                              |
| <span data-ttu-id="7eeb6-254">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7eeb6-254">Classes used in</span></span>        | [<span data-ttu-id="7eeb6-255">**Schutz**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-255">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="7eeb6-256">**Gruppe von Namen**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-256">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="7eeb6-257">**groupof uniquumames**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-257">**groupOfUniqueNames**</span></span>](c-groupofuniquenames.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7eeb6-258">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7eeb6-258">Windows Server 2012</span></span>



| <span data-ttu-id="7eeb6-259">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7eeb6-259">Entry</span></span> | <span data-ttu-id="7eeb6-260">Wert</span><span class="sxs-lookup"><span data-stu-id="7eeb6-260">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eeb6-261">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7eeb6-261">Link-Id</span></span>                | <span data-ttu-id="7eeb6-262">44</span><span class="sxs-lookup"><span data-stu-id="7eeb6-262">44</span></span>                                                                                                                                                      |
| <span data-ttu-id="7eeb6-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7eeb6-263">MAPI-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="7eeb6-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="7eeb6-264">System-Only</span></span>            | <span data-ttu-id="7eeb6-265">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-265">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="7eeb6-266">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7eeb6-266">Is-Single-Valued</span></span>       | <span data-ttu-id="7eeb6-267">Richtig</span><span class="sxs-lookup"><span data-stu-id="7eeb6-267">True</span></span>                                                                                                                                                    |
| <span data-ttu-id="7eeb6-268">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7eeb6-268">Is Indexed</span></span>             | <span data-ttu-id="7eeb6-269">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-269">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="7eeb6-270">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7eeb6-270">In Global Catalog</span></span>      | <span data-ttu-id="7eeb6-271">False</span><span class="sxs-lookup"><span data-stu-id="7eeb6-271">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="7eeb6-272">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7eeb6-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="7eeb6-273">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7eeb6-273">O:BAG:BAD:S:</span></span>                                                                                                                                            |
| <span data-ttu-id="7eeb6-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7eeb6-274">Range-Lower</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="7eeb6-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7eeb6-275">Range-Upper</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="7eeb6-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7eeb6-276">Search-Flags</span></span>           | <span data-ttu-id="7eeb6-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7eeb6-277">0x00000000</span></span>                                                                                                                                              |
| <span data-ttu-id="7eeb6-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7eeb6-278">System-Flags</span></span>           | <span data-ttu-id="7eeb6-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7eeb6-279">0x00000010</span></span>                                                                                                                                              |
| <span data-ttu-id="7eeb6-280">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7eeb6-280">Classes used in</span></span>        | [<span data-ttu-id="7eeb6-281">**Schutz**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-281">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="7eeb6-282">**Gruppe von Namen**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-282">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="7eeb6-283">**groupof uniquumames**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-283">**groupOfUniqueNames**</span></span>](c-groupofuniquenames.md)<br/> |



 

 





