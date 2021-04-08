---
title: Attribut "tsmo-Role-Owner"
description: Flexibler Single-Master Vorgang der Distinguished Name des Domänen Controllers, auf dem das Schema geändert werden kann.
ms.assetid: 8eb28524-4bbf-453c-89ab-864ef94b0781
ms.tgt_platform: multiple
keywords:
- Schema für die Active Directory-Rollen Besitzer
- AD-Schema des fSMORoleOwner-Attributs
topic_type:
- apiref
api_name:
- FSMO-Role-Owner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d4439e5ee10fba11db831024d6b1958b75cd81
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859736"
---
# <a name="fsmo-role-owner-attribute"></a><span data-ttu-id="e07fa-105">Attribut "tsmo-Role-Owner"</span><span class="sxs-lookup"><span data-stu-id="e07fa-105">FSMO-Role-Owner attribute</span></span>

<span data-ttu-id="e07fa-106">Flexibler Single-Master Vorgang: der Distinguished Name des Domänen Controllers, auf dem das Schema geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e07fa-106">Flexible Single-Master Operation: The distinguished name of the DC where the schema can be modified.</span></span>



| <span data-ttu-id="e07fa-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e07fa-107">Entry</span></span> | <span data-ttu-id="e07fa-108">Wert</span><span class="sxs-lookup"><span data-stu-id="e07fa-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="e07fa-109">CN</span><span class="sxs-lookup"><span data-stu-id="e07fa-109">CN</span></span>                | <span data-ttu-id="e07fa-110">"F"-Rollen Besitzer</span><span class="sxs-lookup"><span data-stu-id="e07fa-110">FSMO-Role-Owner</span></span>                         |
| <span data-ttu-id="e07fa-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e07fa-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e07fa-112">fSMORoleOwner</span><span class="sxs-lookup"><span data-stu-id="e07fa-112">fSMORoleOwner</span></span>                           |
| <span data-ttu-id="e07fa-113">Size</span><span class="sxs-lookup"><span data-stu-id="e07fa-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="e07fa-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e07fa-114">Update Privilege</span></span>  | <span data-ttu-id="e07fa-115">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="e07fa-115">Schema administrator</span></span>                    |
| <span data-ttu-id="e07fa-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="e07fa-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="e07fa-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e07fa-117">Attribute-Id</span></span>      | <span data-ttu-id="e07fa-118">1.2.840.113556.1.4.369</span><span class="sxs-lookup"><span data-stu-id="e07fa-118">1.2.840.113556.1.4.369</span></span>                  |
| <span data-ttu-id="e07fa-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e07fa-119">System-Id-Guid</span></span>    | <span data-ttu-id="e07fa-120">66171887-8F -11D0-AFDA-00c04f-930c9</span><span class="sxs-lookup"><span data-stu-id="e07fa-120">66171887-8f3c-11d0-afda-00c04fd930c9</span></span>    |
| <span data-ttu-id="e07fa-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="e07fa-121">Syntax</span></span>            | [<span data-ttu-id="e07fa-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="e07fa-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="e07fa-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="e07fa-123">Implementations</span></span>

-   [<span data-ttu-id="e07fa-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e07fa-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e07fa-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e07fa-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e07fa-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="e07fa-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e07fa-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e07fa-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e07fa-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e07fa-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e07fa-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e07fa-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e07fa-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e07fa-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e07fa-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e07fa-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e07fa-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e07fa-132">Entry</span></span> | <span data-ttu-id="e07fa-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e07fa-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e07fa-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e07fa-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e07fa-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e07fa-135">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e07fa-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e07fa-136">System-Only</span></span>            | <span data-ttu-id="e07fa-137">False</span><span class="sxs-lookup"><span data-stu-id="e07fa-137">False</span></span>                           |
| <span data-ttu-id="e07fa-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e07fa-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e07fa-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="e07fa-139">True</span></span>                            |
| <span data-ttu-id="e07fa-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e07fa-140">Is Indexed</span></span>             | <span data-ttu-id="e07fa-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="e07fa-141">True</span></span>                            |
| <span data-ttu-id="e07fa-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e07fa-142">In Global Catalog</span></span>      | <span data-ttu-id="e07fa-143">False</span><span class="sxs-lookup"><span data-stu-id="e07fa-143">False</span></span>                           |
| <span data-ttu-id="e07fa-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e07fa-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e07fa-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e07fa-145">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e07fa-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e07fa-146">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e07fa-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e07fa-147">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e07fa-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e07fa-148">Search-Flags</span></span>           | <span data-ttu-id="e07fa-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e07fa-149">0x00000001</span></span>                      |
| <span data-ttu-id="e07fa-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e07fa-150">System-Flags</span></span>           | <span data-ttu-id="e07fa-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e07fa-151">0x00000010</span></span>                      |
| <span data-ttu-id="e07fa-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e07fa-152">Classes used in</span></span>        | [<span data-ttu-id="e07fa-153">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="e07fa-153">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e07fa-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e07fa-154">Windows Server 2003</span></span>



| <span data-ttu-id="e07fa-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e07fa-155">Entry</span></span> | <span data-ttu-id="e07fa-156">Wert</span><span class="sxs-lookup"><span data-stu-id="e07fa-156">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e07fa-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e07fa-157">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e07fa-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e07fa-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e07fa-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e07fa-159">System-Only</span></span>            | <span data-ttu-id="e07fa-160">False</span><span class="sxs-lookup"><span data-stu-id="e07fa-160">False</span></span>                           |
| <span data-ttu-id="e07fa-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e07fa-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e07fa-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="e07fa-162">True</span></span>                            |
| <span data-ttu-id="e07fa-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e07fa-163">Is Indexed</span></span>             | <span data-ttu-id="e07fa-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="e07fa-164">True</span></span>                            |
| <span data-ttu-id="e07fa-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e07fa-165">In Global Catalog</span></span>      | <span data-ttu-id="e07fa-166">False</span><span class="sxs-lookup"><span data-stu-id="e07fa-166">False</span></span>                           |
| <span data-ttu-id="e07fa-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e07fa-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e07fa-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e07fa-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e07fa-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e07fa-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e07fa-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e07fa-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e07fa-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e07fa-171">Search-Flags</span></span>           | <span data-ttu-id="e07fa-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e07fa-172">0x00000001</span></span>                      |
| <span data-ttu-id="e07fa-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e07fa-173">System-Flags</span></span>           | <span data-ttu-id="e07fa-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e07fa-174">0x00000010</span></span>                      |
| <span data-ttu-id="e07fa-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e07fa-175">Classes used in</span></span>        | [<span data-ttu-id="e07fa-176">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="e07fa-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e07fa-177">Adam</span><span class="sxs-lookup"><span data-stu-id="e07fa-177">ADAM</span></span>



| <span data-ttu-id="e07fa-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e07fa-178">Entry</span></span> | <span data-ttu-id="e07fa-179">Wert</span><span class="sxs-lookup"><span data-stu-id="e07fa-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e07fa-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e07fa-180">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e07fa-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e07fa-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e07fa-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e07fa-182">System-Only</span></span>            | <span data-ttu-id="e07fa-183">False</span><span class="sxs-lookup"><span data-stu-id="e07fa-183">False</span></span>                           |
| <span data-ttu-id="e07fa-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e07fa-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e07fa-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="e07fa-185">True</span></span>                            |
| <span data-ttu-id="e07fa-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e07fa-186">Is Indexed</span></span>             | <span data-ttu-id="e07fa-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="e07fa-187">True</span></span>                            |
| <span data-ttu-id="e07fa-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e07fa-188">In Global Catalog</span></span>      | <span data-ttu-id="e07fa-189">False</span><span class="sxs-lookup"><span data-stu-id="e07fa-189">False</span></span>                           |
| <span data-ttu-id="e07fa-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e07fa-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e07fa-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e07fa-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e07fa-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e07fa-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e07fa-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e07fa-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e07fa-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e07fa-194">Search-Flags</span></span>           | <span data-ttu-id="e07fa-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e07fa-195">0x00000001</span></span>                      |
| <span data-ttu-id="e07fa-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e07fa-196">System-Flags</span></span>           | <span data-ttu-id="e07fa-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e07fa-197">0x00000010</span></span>                      |
| <span data-ttu-id="e07fa-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e07fa-198">Classes used in</span></span>        | [<span data-ttu-id="e07fa-199">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="e07fa-199">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e07fa-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e07fa-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e07fa-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e07fa-201">Entry</span></span> | <span data-ttu-id="e07fa-202">Wert</span><span class="sxs-lookup"><span data-stu-id="e07fa-202">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e07fa-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e07fa-203">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e07fa-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e07fa-204">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e07fa-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e07fa-205">System-Only</span></span>            | <span data-ttu-id="e07fa-206">False</span><span class="sxs-lookup"><span data-stu-id="e07fa-206">False</span></span>                           |
| <span data-ttu-id="e07fa-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e07fa-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e07fa-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="e07fa-208">True</span></span>                            |
| <span data-ttu-id="e07fa-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e07fa-209">Is Indexed</span></span>             | <span data-ttu-id="e07fa-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="e07fa-210">True</span></span>                            |
| <span data-ttu-id="e07fa-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e07fa-211">In Global Catalog</span></span>      | <span data-ttu-id="e07fa-212">False</span><span class="sxs-lookup"><span data-stu-id="e07fa-212">False</span></span>                           |
| <span data-ttu-id="e07fa-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e07fa-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e07fa-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e07fa-214">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e07fa-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e07fa-215">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e07fa-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e07fa-216">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e07fa-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e07fa-217">Search-Flags</span></span>           | <span data-ttu-id="e07fa-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e07fa-218">0x00000001</span></span>                      |
| <span data-ttu-id="e07fa-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e07fa-219">System-Flags</span></span>           | <span data-ttu-id="e07fa-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e07fa-220">0x00000010</span></span>                      |
| <span data-ttu-id="e07fa-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e07fa-221">Classes used in</span></span>        | [<span data-ttu-id="e07fa-222">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="e07fa-222">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e07fa-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e07fa-223">Windows Server 2008</span></span>



| <span data-ttu-id="e07fa-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e07fa-224">Entry</span></span> | <span data-ttu-id="e07fa-225">Wert</span><span class="sxs-lookup"><span data-stu-id="e07fa-225">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e07fa-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e07fa-226">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e07fa-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e07fa-227">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e07fa-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e07fa-228">System-Only</span></span>            | <span data-ttu-id="e07fa-229">False</span><span class="sxs-lookup"><span data-stu-id="e07fa-229">False</span></span>                           |
| <span data-ttu-id="e07fa-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e07fa-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e07fa-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="e07fa-231">True</span></span>                            |
| <span data-ttu-id="e07fa-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e07fa-232">Is Indexed</span></span>             | <span data-ttu-id="e07fa-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="e07fa-233">True</span></span>                            |
| <span data-ttu-id="e07fa-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e07fa-234">In Global Catalog</span></span>      | <span data-ttu-id="e07fa-235">False</span><span class="sxs-lookup"><span data-stu-id="e07fa-235">False</span></span>                           |
| <span data-ttu-id="e07fa-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e07fa-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e07fa-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e07fa-237">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e07fa-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e07fa-238">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e07fa-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e07fa-239">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e07fa-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e07fa-240">Search-Flags</span></span>           | <span data-ttu-id="e07fa-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e07fa-241">0x00000001</span></span>                      |
| <span data-ttu-id="e07fa-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e07fa-242">System-Flags</span></span>           | <span data-ttu-id="e07fa-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e07fa-243">0x00000010</span></span>                      |
| <span data-ttu-id="e07fa-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e07fa-244">Classes used in</span></span>        | [<span data-ttu-id="e07fa-245">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="e07fa-245">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e07fa-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e07fa-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e07fa-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e07fa-247">Entry</span></span> | <span data-ttu-id="e07fa-248">Wert</span><span class="sxs-lookup"><span data-stu-id="e07fa-248">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e07fa-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e07fa-249">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e07fa-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e07fa-250">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e07fa-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e07fa-251">System-Only</span></span>            | <span data-ttu-id="e07fa-252">False</span><span class="sxs-lookup"><span data-stu-id="e07fa-252">False</span></span>                           |
| <span data-ttu-id="e07fa-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e07fa-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e07fa-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="e07fa-254">True</span></span>                            |
| <span data-ttu-id="e07fa-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e07fa-255">Is Indexed</span></span>             | <span data-ttu-id="e07fa-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="e07fa-256">True</span></span>                            |
| <span data-ttu-id="e07fa-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e07fa-257">In Global Catalog</span></span>      | <span data-ttu-id="e07fa-258">False</span><span class="sxs-lookup"><span data-stu-id="e07fa-258">False</span></span>                           |
| <span data-ttu-id="e07fa-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e07fa-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e07fa-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e07fa-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e07fa-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e07fa-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e07fa-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e07fa-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e07fa-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e07fa-263">Search-Flags</span></span>           | <span data-ttu-id="e07fa-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e07fa-264">0x00000001</span></span>                      |
| <span data-ttu-id="e07fa-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e07fa-265">System-Flags</span></span>           | <span data-ttu-id="e07fa-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e07fa-266">0x00000010</span></span>                      |
| <span data-ttu-id="e07fa-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e07fa-267">Classes used in</span></span>        | [<span data-ttu-id="e07fa-268">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="e07fa-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e07fa-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e07fa-269">Windows Server 2012</span></span>



| <span data-ttu-id="e07fa-270">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e07fa-270">Entry</span></span> | <span data-ttu-id="e07fa-271">Wert</span><span class="sxs-lookup"><span data-stu-id="e07fa-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e07fa-272">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e07fa-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e07fa-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e07fa-273">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e07fa-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="e07fa-274">System-Only</span></span>            | <span data-ttu-id="e07fa-275">False</span><span class="sxs-lookup"><span data-stu-id="e07fa-275">False</span></span>                           |
| <span data-ttu-id="e07fa-276">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e07fa-276">Is-Single-Valued</span></span>       | <span data-ttu-id="e07fa-277">Richtig</span><span class="sxs-lookup"><span data-stu-id="e07fa-277">True</span></span>                            |
| <span data-ttu-id="e07fa-278">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e07fa-278">Is Indexed</span></span>             | <span data-ttu-id="e07fa-279">Richtig</span><span class="sxs-lookup"><span data-stu-id="e07fa-279">True</span></span>                            |
| <span data-ttu-id="e07fa-280">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e07fa-280">In Global Catalog</span></span>      | <span data-ttu-id="e07fa-281">False</span><span class="sxs-lookup"><span data-stu-id="e07fa-281">False</span></span>                           |
| <span data-ttu-id="e07fa-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e07fa-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="e07fa-283">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e07fa-283">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e07fa-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e07fa-284">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e07fa-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e07fa-285">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e07fa-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e07fa-286">Search-Flags</span></span>           | <span data-ttu-id="e07fa-287">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e07fa-287">0x00000001</span></span>                      |
| <span data-ttu-id="e07fa-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e07fa-288">System-Flags</span></span>           | <span data-ttu-id="e07fa-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e07fa-289">0x00000010</span></span>                      |
| <span data-ttu-id="e07fa-290">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e07fa-290">Classes used in</span></span>        | [<span data-ttu-id="e07fa-291">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="e07fa-291">**Top**</span></span>](c-top.md)<br/> |



 

 





