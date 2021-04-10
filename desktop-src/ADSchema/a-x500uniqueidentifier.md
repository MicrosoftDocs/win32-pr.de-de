---
title: x500uniqueIdentifier-Attribut
description: Wird verwendet, um zwischen Objekten zu unterscheiden, wenn ein definierter Name wieder verwendet wurde. Dabei handelt es sich um einen anderen Attributtyp als die Typen "UID" und "uniqueidentifier".
ms.assetid: 72975f85-2e0a-4b4e-8fc2-8eeb2d744563
ms.tgt_platform: multiple
keywords:
- x500uniqueIdentifier-Attribut AD-Schema
topic_type:
- apiref
api_name:
- x500uniqueIdentifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b6be2dd1beca51dbc3ad2de2caa8ef6afb11a5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122617"
---
# <a name="x500uniqueidentifier-attribute"></a><span data-ttu-id="e475f-105">x500uniqueIdentifier-Attribut</span><span class="sxs-lookup"><span data-stu-id="e475f-105">x500uniqueIdentifier attribute</span></span>

<span data-ttu-id="e475f-106">Wird verwendet, um zwischen Objekten zu unterscheiden, wenn ein definierter Name wieder verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e475f-106">Used to distinguish between objects when a distinguished name has been reused.</span></span> <span data-ttu-id="e475f-107">Dabei handelt es sich um einen anderen Attributtyp als die Typen "UID" und "uniqueidentifier".</span><span class="sxs-lookup"><span data-stu-id="e475f-107">This is a different attribute type from both the uid and uniqueIdentifier types.</span></span>



| <span data-ttu-id="e475f-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e475f-108">Entry</span></span> | <span data-ttu-id="e475f-109">Wert</span><span class="sxs-lookup"><span data-stu-id="e475f-109">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="e475f-110">CN</span><span class="sxs-lookup"><span data-stu-id="e475f-110">CN</span></span>                | <span data-ttu-id="e475f-111">x500uniqueIdentifier</span><span class="sxs-lookup"><span data-stu-id="e475f-111">x500uniqueIdentifier</span></span>                                  |
| <span data-ttu-id="e475f-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e475f-112">Ldap-Display-Name</span></span> | <span data-ttu-id="e475f-113">x500uniqueIdentifier</span><span class="sxs-lookup"><span data-stu-id="e475f-113">x500uniqueIdentifier</span></span>                                  |
| <span data-ttu-id="e475f-114">Size</span><span class="sxs-lookup"><span data-stu-id="e475f-114">Size</span></span>              | \-                                                    |
| <span data-ttu-id="e475f-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e475f-115">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="e475f-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="e475f-116">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="e475f-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e475f-117">Attribute-Id</span></span>      | <span data-ttu-id="e475f-118">2.5.4.45</span><span class="sxs-lookup"><span data-stu-id="e475f-118">2.5.4.45</span></span>                                              |
| <span data-ttu-id="e475f-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e475f-119">System-Id-Guid</span></span>    | <span data-ttu-id="e475f-120">d07da11f-8a3d-42b6-b0aa-76c962be719a</span><span class="sxs-lookup"><span data-stu-id="e475f-120">d07da11f-8a3d-42b6-b0aa-76c962be719a</span></span>                  |
| <span data-ttu-id="e475f-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="e475f-121">Syntax</span></span>            | [<span data-ttu-id="e475f-122">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="e475f-122">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="e475f-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="e475f-123">Implementations</span></span>

-   [<span data-ttu-id="e475f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e475f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e475f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e475f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e475f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e475f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e475f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e475f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e475f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e475f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e475f-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e475f-129">Windows Server 2003</span></span>



| <span data-ttu-id="e475f-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e475f-130">Entry</span></span> | <span data-ttu-id="e475f-131">Wert</span><span class="sxs-lookup"><span data-stu-id="e475f-131">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e475f-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e475f-132">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="e475f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e475f-133">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="e475f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="e475f-134">System-Only</span></span>            | <span data-ttu-id="e475f-135">False</span><span class="sxs-lookup"><span data-stu-id="e475f-135">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e475f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="e475f-137">False</span><span class="sxs-lookup"><span data-stu-id="e475f-137">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e475f-138">Is Indexed</span></span>             | <span data-ttu-id="e475f-139">False</span><span class="sxs-lookup"><span data-stu-id="e475f-139">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e475f-140">In Global Catalog</span></span>      | <span data-ttu-id="e475f-141">False</span><span class="sxs-lookup"><span data-stu-id="e475f-141">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e475f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="e475f-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e475f-143">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="e475f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e475f-144">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="e475f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e475f-145">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="e475f-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e475f-146">Search-Flags</span></span>           | <span data-ttu-id="e475f-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e475f-147">0x00000000</span></span>                                                                            |
| <span data-ttu-id="e475f-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e475f-148">System-Flags</span></span>           | <span data-ttu-id="e475f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e475f-149">0x00000000</span></span>                                                                            |
| <span data-ttu-id="e475f-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e475f-150">Classes used in</span></span>        | [<span data-ttu-id="e475f-151">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e475f-151">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="e475f-152">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="e475f-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e475f-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e475f-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e475f-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e475f-154">Entry</span></span> | <span data-ttu-id="e475f-155">Wert</span><span class="sxs-lookup"><span data-stu-id="e475f-155">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e475f-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e475f-156">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="e475f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e475f-157">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="e475f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e475f-158">System-Only</span></span>            | <span data-ttu-id="e475f-159">False</span><span class="sxs-lookup"><span data-stu-id="e475f-159">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e475f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e475f-161">False</span><span class="sxs-lookup"><span data-stu-id="e475f-161">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e475f-162">Is Indexed</span></span>             | <span data-ttu-id="e475f-163">False</span><span class="sxs-lookup"><span data-stu-id="e475f-163">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e475f-164">In Global Catalog</span></span>      | <span data-ttu-id="e475f-165">False</span><span class="sxs-lookup"><span data-stu-id="e475f-165">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e475f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e475f-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e475f-167">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="e475f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e475f-168">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="e475f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e475f-169">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="e475f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e475f-170">Search-Flags</span></span>           | <span data-ttu-id="e475f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e475f-171">0x00000000</span></span>                                                                            |
| <span data-ttu-id="e475f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e475f-172">System-Flags</span></span>           | <span data-ttu-id="e475f-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e475f-173">0x00000000</span></span>                                                                            |
| <span data-ttu-id="e475f-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e475f-174">Classes used in</span></span>        | [<span data-ttu-id="e475f-175">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e475f-175">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="e475f-176">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="e475f-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e475f-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e475f-177">Windows Server 2008</span></span>



| <span data-ttu-id="e475f-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e475f-178">Entry</span></span> | <span data-ttu-id="e475f-179">Wert</span><span class="sxs-lookup"><span data-stu-id="e475f-179">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e475f-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e475f-180">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="e475f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e475f-181">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="e475f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e475f-182">System-Only</span></span>            | <span data-ttu-id="e475f-183">False</span><span class="sxs-lookup"><span data-stu-id="e475f-183">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e475f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e475f-185">False</span><span class="sxs-lookup"><span data-stu-id="e475f-185">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e475f-186">Is Indexed</span></span>             | <span data-ttu-id="e475f-187">False</span><span class="sxs-lookup"><span data-stu-id="e475f-187">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e475f-188">In Global Catalog</span></span>      | <span data-ttu-id="e475f-189">False</span><span class="sxs-lookup"><span data-stu-id="e475f-189">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e475f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e475f-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e475f-191">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="e475f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e475f-192">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="e475f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e475f-193">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="e475f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e475f-194">Search-Flags</span></span>           | <span data-ttu-id="e475f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e475f-195">0x00000000</span></span>                                                                            |
| <span data-ttu-id="e475f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e475f-196">System-Flags</span></span>           | <span data-ttu-id="e475f-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e475f-197">0x00000000</span></span>                                                                            |
| <span data-ttu-id="e475f-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e475f-198">Classes used in</span></span>        | [<span data-ttu-id="e475f-199">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e475f-199">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="e475f-200">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="e475f-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e475f-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e475f-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e475f-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e475f-202">Entry</span></span> | <span data-ttu-id="e475f-203">Wert</span><span class="sxs-lookup"><span data-stu-id="e475f-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e475f-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e475f-204">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="e475f-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e475f-205">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="e475f-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="e475f-206">System-Only</span></span>            | <span data-ttu-id="e475f-207">False</span><span class="sxs-lookup"><span data-stu-id="e475f-207">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e475f-208">Is-Single-Valued</span></span>       | <span data-ttu-id="e475f-209">False</span><span class="sxs-lookup"><span data-stu-id="e475f-209">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e475f-210">Is Indexed</span></span>             | <span data-ttu-id="e475f-211">False</span><span class="sxs-lookup"><span data-stu-id="e475f-211">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e475f-212">In Global Catalog</span></span>      | <span data-ttu-id="e475f-213">False</span><span class="sxs-lookup"><span data-stu-id="e475f-213">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e475f-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="e475f-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e475f-215">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="e475f-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e475f-216">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="e475f-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e475f-217">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="e475f-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e475f-218">Search-Flags</span></span>           | <span data-ttu-id="e475f-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e475f-219">0x00000000</span></span>                                                                            |
| <span data-ttu-id="e475f-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e475f-220">System-Flags</span></span>           | <span data-ttu-id="e475f-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e475f-221">0x00000000</span></span>                                                                            |
| <span data-ttu-id="e475f-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e475f-222">Classes used in</span></span>        | [<span data-ttu-id="e475f-223">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e475f-223">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="e475f-224">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="e475f-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e475f-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e475f-225">Windows Server 2012</span></span>



| <span data-ttu-id="e475f-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e475f-226">Entry</span></span> | <span data-ttu-id="e475f-227">Wert</span><span class="sxs-lookup"><span data-stu-id="e475f-227">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e475f-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e475f-228">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="e475f-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e475f-229">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="e475f-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="e475f-230">System-Only</span></span>            | <span data-ttu-id="e475f-231">False</span><span class="sxs-lookup"><span data-stu-id="e475f-231">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e475f-232">Is-Single-Valued</span></span>       | <span data-ttu-id="e475f-233">False</span><span class="sxs-lookup"><span data-stu-id="e475f-233">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e475f-234">Is Indexed</span></span>             | <span data-ttu-id="e475f-235">False</span><span class="sxs-lookup"><span data-stu-id="e475f-235">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e475f-236">In Global Catalog</span></span>      | <span data-ttu-id="e475f-237">False</span><span class="sxs-lookup"><span data-stu-id="e475f-237">False</span></span>                                                                                 |
| <span data-ttu-id="e475f-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e475f-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="e475f-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e475f-239">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="e475f-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e475f-240">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="e475f-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e475f-241">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="e475f-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e475f-242">Search-Flags</span></span>           | <span data-ttu-id="e475f-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e475f-243">0x00000000</span></span>                                                                            |
| <span data-ttu-id="e475f-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e475f-244">System-Flags</span></span>           | <span data-ttu-id="e475f-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e475f-245">0x00000000</span></span>                                                                            |
| <span data-ttu-id="e475f-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e475f-246">Classes used in</span></span>        | [<span data-ttu-id="e475f-247">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e475f-247">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="e475f-248">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="e475f-248">**User**</span></span>](c-user.md)<br/> |



 

 





