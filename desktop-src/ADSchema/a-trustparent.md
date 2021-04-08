---
title: Trust-Parent-Attribut
description: Das übergeordnete Element in der Kerberos-Vertrauens Hierarchie.
ms.assetid: 738cf509-42a2-40b6-a525-6df34c02d0f0
ms.tgt_platform: multiple
keywords:
- AD-Schema für Trust-Parent-Attribut
- Trust Parent-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Trust-Parent
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d8be971c7597b14daf7a694e41c9d67714e5f0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744873"
---
# <a name="trust-parent-attribute"></a><span data-ttu-id="34aea-105">Trust-Parent-Attribut</span><span class="sxs-lookup"><span data-stu-id="34aea-105">Trust-Parent attribute</span></span>

<span data-ttu-id="34aea-106">Das übergeordnete Element in der Kerberos-Vertrauens Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="34aea-106">The parent in KERBEROS trust hierarchy.</span></span>



| <span data-ttu-id="34aea-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34aea-107">Entry</span></span> | <span data-ttu-id="34aea-108">Wert</span><span class="sxs-lookup"><span data-stu-id="34aea-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="34aea-109">CN</span><span class="sxs-lookup"><span data-stu-id="34aea-109">CN</span></span>                | <span data-ttu-id="34aea-110">Trust-Parent</span><span class="sxs-lookup"><span data-stu-id="34aea-110">Trust-Parent</span></span>                            |
| <span data-ttu-id="34aea-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="34aea-111">Ldap-Display-Name</span></span> | <span data-ttu-id="34aea-112">Trust Parent</span><span class="sxs-lookup"><span data-stu-id="34aea-112">trustParent</span></span>                             |
| <span data-ttu-id="34aea-113">Size</span><span class="sxs-lookup"><span data-stu-id="34aea-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="34aea-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="34aea-114">Update Privilege</span></span>  | <span data-ttu-id="34aea-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="34aea-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="34aea-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="34aea-116">Update Frequency</span></span>  | <span data-ttu-id="34aea-117">Wenn eine untergeordnete Domäne erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="34aea-117">When a child domain is created.</span></span>         |
| <span data-ttu-id="34aea-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="34aea-118">Attribute-Id</span></span>      | <span data-ttu-id="34aea-119">1.2.840.113556.1.4.471</span><span class="sxs-lookup"><span data-stu-id="34aea-119">1.2.840.113556.1.4.471</span></span>                  |
| <span data-ttu-id="34aea-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="34aea-120">System-Id-Guid</span></span>    | <span data-ttu-id="34aea-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="34aea-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span></span>    |
| <span data-ttu-id="34aea-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="34aea-122">Syntax</span></span>            | [<span data-ttu-id="34aea-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="34aea-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="34aea-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="34aea-124">Implementations</span></span>

-   [<span data-ttu-id="34aea-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="34aea-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="34aea-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="34aea-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="34aea-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="34aea-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="34aea-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="34aea-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="34aea-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="34aea-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="34aea-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="34aea-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="34aea-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="34aea-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="34aea-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="34aea-132">Windows 2000 Server</span></span>



| <span data-ttu-id="34aea-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34aea-133">Entry</span></span> | <span data-ttu-id="34aea-134">Wert</span><span class="sxs-lookup"><span data-stu-id="34aea-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="34aea-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="34aea-135">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="34aea-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34aea-136">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="34aea-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="34aea-137">System-Only</span></span>            | <span data-ttu-id="34aea-138">False</span><span class="sxs-lookup"><span data-stu-id="34aea-138">False</span></span>                                      |
| <span data-ttu-id="34aea-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="34aea-139">Is-Single-Valued</span></span>       | <span data-ttu-id="34aea-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="34aea-140">True</span></span>                                       |
| <span data-ttu-id="34aea-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="34aea-141">Is Indexed</span></span>             | <span data-ttu-id="34aea-142">False</span><span class="sxs-lookup"><span data-stu-id="34aea-142">False</span></span>                                      |
| <span data-ttu-id="34aea-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="34aea-143">In Global Catalog</span></span>      | <span data-ttu-id="34aea-144">False</span><span class="sxs-lookup"><span data-stu-id="34aea-144">False</span></span>                                      |
| <span data-ttu-id="34aea-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34aea-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="34aea-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="34aea-146">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="34aea-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34aea-147">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="34aea-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34aea-148">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="34aea-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34aea-149">Search-Flags</span></span>           | <span data-ttu-id="34aea-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34aea-150">0x00000000</span></span>                                 |
| <span data-ttu-id="34aea-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34aea-151">System-Flags</span></span>           | <span data-ttu-id="34aea-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34aea-152">0x00000010</span></span>                                 |
| <span data-ttu-id="34aea-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="34aea-153">Classes used in</span></span>        | [<span data-ttu-id="34aea-154">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="34aea-154">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="34aea-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34aea-155">Windows Server 2003</span></span>



| <span data-ttu-id="34aea-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34aea-156">Entry</span></span> | <span data-ttu-id="34aea-157">Wert</span><span class="sxs-lookup"><span data-stu-id="34aea-157">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="34aea-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="34aea-158">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="34aea-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34aea-159">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="34aea-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="34aea-160">System-Only</span></span>            | <span data-ttu-id="34aea-161">False</span><span class="sxs-lookup"><span data-stu-id="34aea-161">False</span></span>                                      |
| <span data-ttu-id="34aea-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="34aea-162">Is-Single-Valued</span></span>       | <span data-ttu-id="34aea-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="34aea-163">True</span></span>                                       |
| <span data-ttu-id="34aea-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="34aea-164">Is Indexed</span></span>             | <span data-ttu-id="34aea-165">False</span><span class="sxs-lookup"><span data-stu-id="34aea-165">False</span></span>                                      |
| <span data-ttu-id="34aea-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="34aea-166">In Global Catalog</span></span>      | <span data-ttu-id="34aea-167">False</span><span class="sxs-lookup"><span data-stu-id="34aea-167">False</span></span>                                      |
| <span data-ttu-id="34aea-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34aea-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="34aea-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="34aea-169">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="34aea-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34aea-170">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="34aea-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34aea-171">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="34aea-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34aea-172">Search-Flags</span></span>           | <span data-ttu-id="34aea-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34aea-173">0x00000000</span></span>                                 |
| <span data-ttu-id="34aea-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34aea-174">System-Flags</span></span>           | <span data-ttu-id="34aea-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34aea-175">0x00000010</span></span>                                 |
| <span data-ttu-id="34aea-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="34aea-176">Classes used in</span></span>        | [<span data-ttu-id="34aea-177">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="34aea-177">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="34aea-178">Adam</span><span class="sxs-lookup"><span data-stu-id="34aea-178">ADAM</span></span>



| <span data-ttu-id="34aea-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34aea-179">Entry</span></span> | <span data-ttu-id="34aea-180">Wert</span><span class="sxs-lookup"><span data-stu-id="34aea-180">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="34aea-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="34aea-181">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="34aea-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34aea-182">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="34aea-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="34aea-183">System-Only</span></span>            | <span data-ttu-id="34aea-184">False</span><span class="sxs-lookup"><span data-stu-id="34aea-184">False</span></span>                                      |
| <span data-ttu-id="34aea-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="34aea-185">Is-Single-Valued</span></span>       | <span data-ttu-id="34aea-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="34aea-186">True</span></span>                                       |
| <span data-ttu-id="34aea-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="34aea-187">Is Indexed</span></span>             | <span data-ttu-id="34aea-188">False</span><span class="sxs-lookup"><span data-stu-id="34aea-188">False</span></span>                                      |
| <span data-ttu-id="34aea-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="34aea-189">In Global Catalog</span></span>      | <span data-ttu-id="34aea-190">False</span><span class="sxs-lookup"><span data-stu-id="34aea-190">False</span></span>                                      |
| <span data-ttu-id="34aea-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34aea-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="34aea-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="34aea-192">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="34aea-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34aea-193">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="34aea-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34aea-194">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="34aea-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34aea-195">Search-Flags</span></span>           | <span data-ttu-id="34aea-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34aea-196">0x00000000</span></span>                                 |
| <span data-ttu-id="34aea-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34aea-197">System-Flags</span></span>           | <span data-ttu-id="34aea-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34aea-198">0x00000010</span></span>                                 |
| <span data-ttu-id="34aea-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="34aea-199">Classes used in</span></span>        | [<span data-ttu-id="34aea-200">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="34aea-200">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="34aea-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="34aea-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="34aea-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34aea-202">Entry</span></span> | <span data-ttu-id="34aea-203">Wert</span><span class="sxs-lookup"><span data-stu-id="34aea-203">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="34aea-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="34aea-204">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="34aea-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34aea-205">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="34aea-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="34aea-206">System-Only</span></span>            | <span data-ttu-id="34aea-207">False</span><span class="sxs-lookup"><span data-stu-id="34aea-207">False</span></span>                                      |
| <span data-ttu-id="34aea-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="34aea-208">Is-Single-Valued</span></span>       | <span data-ttu-id="34aea-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="34aea-209">True</span></span>                                       |
| <span data-ttu-id="34aea-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="34aea-210">Is Indexed</span></span>             | <span data-ttu-id="34aea-211">False</span><span class="sxs-lookup"><span data-stu-id="34aea-211">False</span></span>                                      |
| <span data-ttu-id="34aea-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="34aea-212">In Global Catalog</span></span>      | <span data-ttu-id="34aea-213">False</span><span class="sxs-lookup"><span data-stu-id="34aea-213">False</span></span>                                      |
| <span data-ttu-id="34aea-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34aea-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="34aea-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="34aea-215">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="34aea-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34aea-216">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="34aea-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34aea-217">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="34aea-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34aea-218">Search-Flags</span></span>           | <span data-ttu-id="34aea-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34aea-219">0x00000000</span></span>                                 |
| <span data-ttu-id="34aea-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34aea-220">System-Flags</span></span>           | <span data-ttu-id="34aea-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34aea-221">0x00000010</span></span>                                 |
| <span data-ttu-id="34aea-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="34aea-222">Classes used in</span></span>        | [<span data-ttu-id="34aea-223">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="34aea-223">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="34aea-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34aea-224">Windows Server 2008</span></span>



| <span data-ttu-id="34aea-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34aea-225">Entry</span></span> | <span data-ttu-id="34aea-226">Wert</span><span class="sxs-lookup"><span data-stu-id="34aea-226">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="34aea-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="34aea-227">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="34aea-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34aea-228">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="34aea-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="34aea-229">System-Only</span></span>            | <span data-ttu-id="34aea-230">False</span><span class="sxs-lookup"><span data-stu-id="34aea-230">False</span></span>                                      |
| <span data-ttu-id="34aea-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="34aea-231">Is-Single-Valued</span></span>       | <span data-ttu-id="34aea-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="34aea-232">True</span></span>                                       |
| <span data-ttu-id="34aea-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="34aea-233">Is Indexed</span></span>             | <span data-ttu-id="34aea-234">False</span><span class="sxs-lookup"><span data-stu-id="34aea-234">False</span></span>                                      |
| <span data-ttu-id="34aea-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="34aea-235">In Global Catalog</span></span>      | <span data-ttu-id="34aea-236">False</span><span class="sxs-lookup"><span data-stu-id="34aea-236">False</span></span>                                      |
| <span data-ttu-id="34aea-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34aea-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="34aea-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="34aea-238">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="34aea-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34aea-239">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="34aea-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34aea-240">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="34aea-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34aea-241">Search-Flags</span></span>           | <span data-ttu-id="34aea-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34aea-242">0x00000000</span></span>                                 |
| <span data-ttu-id="34aea-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34aea-243">System-Flags</span></span>           | <span data-ttu-id="34aea-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34aea-244">0x00000010</span></span>                                 |
| <span data-ttu-id="34aea-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="34aea-245">Classes used in</span></span>        | [<span data-ttu-id="34aea-246">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="34aea-246">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="34aea-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="34aea-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="34aea-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34aea-248">Entry</span></span> | <span data-ttu-id="34aea-249">Wert</span><span class="sxs-lookup"><span data-stu-id="34aea-249">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="34aea-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="34aea-250">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="34aea-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34aea-251">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="34aea-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="34aea-252">System-Only</span></span>            | <span data-ttu-id="34aea-253">False</span><span class="sxs-lookup"><span data-stu-id="34aea-253">False</span></span>                                      |
| <span data-ttu-id="34aea-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="34aea-254">Is-Single-Valued</span></span>       | <span data-ttu-id="34aea-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="34aea-255">True</span></span>                                       |
| <span data-ttu-id="34aea-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="34aea-256">Is Indexed</span></span>             | <span data-ttu-id="34aea-257">False</span><span class="sxs-lookup"><span data-stu-id="34aea-257">False</span></span>                                      |
| <span data-ttu-id="34aea-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="34aea-258">In Global Catalog</span></span>      | <span data-ttu-id="34aea-259">False</span><span class="sxs-lookup"><span data-stu-id="34aea-259">False</span></span>                                      |
| <span data-ttu-id="34aea-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34aea-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="34aea-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="34aea-261">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="34aea-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34aea-262">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="34aea-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34aea-263">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="34aea-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34aea-264">Search-Flags</span></span>           | <span data-ttu-id="34aea-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34aea-265">0x00000000</span></span>                                 |
| <span data-ttu-id="34aea-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34aea-266">System-Flags</span></span>           | <span data-ttu-id="34aea-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34aea-267">0x00000010</span></span>                                 |
| <span data-ttu-id="34aea-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="34aea-268">Classes used in</span></span>        | [<span data-ttu-id="34aea-269">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="34aea-269">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="34aea-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="34aea-270">Windows Server 2012</span></span>



| <span data-ttu-id="34aea-271">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34aea-271">Entry</span></span> | <span data-ttu-id="34aea-272">Wert</span><span class="sxs-lookup"><span data-stu-id="34aea-272">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="34aea-273">Link-ID</span><span class="sxs-lookup"><span data-stu-id="34aea-273">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="34aea-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34aea-274">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="34aea-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="34aea-275">System-Only</span></span>            | <span data-ttu-id="34aea-276">False</span><span class="sxs-lookup"><span data-stu-id="34aea-276">False</span></span>                                      |
| <span data-ttu-id="34aea-277">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="34aea-277">Is-Single-Valued</span></span>       | <span data-ttu-id="34aea-278">Richtig</span><span class="sxs-lookup"><span data-stu-id="34aea-278">True</span></span>                                       |
| <span data-ttu-id="34aea-279">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="34aea-279">Is Indexed</span></span>             | <span data-ttu-id="34aea-280">False</span><span class="sxs-lookup"><span data-stu-id="34aea-280">False</span></span>                                      |
| <span data-ttu-id="34aea-281">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="34aea-281">In Global Catalog</span></span>      | <span data-ttu-id="34aea-282">False</span><span class="sxs-lookup"><span data-stu-id="34aea-282">False</span></span>                                      |
| <span data-ttu-id="34aea-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34aea-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="34aea-284">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="34aea-284">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="34aea-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34aea-285">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="34aea-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34aea-286">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="34aea-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34aea-287">Search-Flags</span></span>           | <span data-ttu-id="34aea-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34aea-288">0x00000000</span></span>                                 |
| <span data-ttu-id="34aea-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34aea-289">System-Flags</span></span>           | <span data-ttu-id="34aea-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34aea-290">0x00000010</span></span>                                 |
| <span data-ttu-id="34aea-291">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="34aea-291">Classes used in</span></span>        | [<span data-ttu-id="34aea-292">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="34aea-292">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





