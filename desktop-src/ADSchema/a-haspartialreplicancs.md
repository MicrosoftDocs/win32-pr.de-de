---
title: Has-Partial-Replica-NCS-Attribut
description: Gleich geordnetes Element von "-Master-NCS". "Has-Partial-Replica-NCS" gibt den Distinguished Name für alle anderen NCS der Domäne wieder, die in einen globalen Katalog repliziert wurden.
ms.assetid: 2501bbb3-74b5-4604-b0c0-8653fc092e1c
ms.tgt_platform: multiple
keywords:
- Has-Partial-Replica-NCS-Attribut AD-Schema
- haspartialreplicancs-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Has-Partial-Replica-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f284df094c909b01b88a4853ed7c4a41dee9f31a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744217"
---
# <a name="has-partial-replica-ncs-attribute"></a><span data-ttu-id="6c9c7-106">Has-Partial-Replica-NCS-Attribut</span><span class="sxs-lookup"><span data-stu-id="6c9c7-106">Has-Partial-Replica-NCs attribute</span></span>

<span data-ttu-id="6c9c7-107">Gleich geordnetes Element von "-Master-NCS".</span><span class="sxs-lookup"><span data-stu-id="6c9c7-107">Sibling to Has-Master-NCs.</span></span> <span data-ttu-id="6c9c7-108">"Has-Partial-Replica-NCS" gibt den Distinguished Name für alle anderen NCS der Domäne wieder, die in einen globalen Katalog repliziert wurden.</span><span class="sxs-lookup"><span data-stu-id="6c9c7-108">Has-Partial-Replica-NCs reflects the distinguished name for all other-domain NCs that have been replicated into a global catalog.</span></span>



| <span data-ttu-id="6c9c7-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c9c7-109">Entry</span></span> | <span data-ttu-id="6c9c7-110">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9c7-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="6c9c7-111">CN</span><span class="sxs-lookup"><span data-stu-id="6c9c7-111">CN</span></span>                | <span data-ttu-id="6c9c7-112">Has-Partial-Replica-NCS</span><span class="sxs-lookup"><span data-stu-id="6c9c7-112">Has-Partial-Replica-NCs</span></span>                 |
| <span data-ttu-id="6c9c7-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6c9c7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6c9c7-114">haspartialreplicancs</span><span class="sxs-lookup"><span data-stu-id="6c9c7-114">hasPartialReplicaNCs</span></span>                    |
| <span data-ttu-id="6c9c7-115">Size</span><span class="sxs-lookup"><span data-stu-id="6c9c7-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="6c9c7-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="6c9c7-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="6c9c7-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="6c9c7-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="6c9c7-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6c9c7-118">Attribute-Id</span></span>      | <span data-ttu-id="6c9c7-119">1.2.840.113556.1.2.15</span><span class="sxs-lookup"><span data-stu-id="6c9c7-119">1.2.840.113556.1.2.15</span></span>                   |
| <span data-ttu-id="6c9c7-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6c9c7-120">System-Id-Guid</span></span>    | <span data-ttu-id="6c9c7-121">bf967981-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6c9c7-121">bf967981-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="6c9c7-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c9c7-122">Syntax</span></span>            | [<span data-ttu-id="6c9c7-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="6c9c7-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="6c9c7-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="6c9c7-124">Implementations</span></span>

-   [<span data-ttu-id="6c9c7-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6c9c7-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6c9c7-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6c9c7-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6c9c7-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="6c9c7-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6c9c7-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6c9c7-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6c9c7-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6c9c7-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6c9c7-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6c9c7-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6c9c7-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6c9c7-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6c9c7-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c9c7-132">Windows 2000 Server</span></span>



| <span data-ttu-id="6c9c7-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c9c7-133">Entry</span></span> | <span data-ttu-id="6c9c7-134">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9c7-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="6c9c7-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c9c7-135">Link-Id</span></span>                | <span data-ttu-id="6c9c7-136">74</span><span class="sxs-lookup"><span data-stu-id="6c9c7-136">74</span></span>                                       |
| <span data-ttu-id="6c9c7-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c9c7-137">MAPI-Id</span></span>                | <span data-ttu-id="6c9c7-138">0x80b5</span><span class="sxs-lookup"><span data-stu-id="6c9c7-138">0x80B5</span></span>                                   |
| <span data-ttu-id="6c9c7-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c9c7-139">System-Only</span></span>            | <span data-ttu-id="6c9c7-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="6c9c7-140">True</span></span>                                     |
| <span data-ttu-id="6c9c7-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c9c7-141">Is-Single-Valued</span></span>       | <span data-ttu-id="6c9c7-142">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-142">False</span></span>                                    |
| <span data-ttu-id="6c9c7-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c9c7-143">Is Indexed</span></span>             | <span data-ttu-id="6c9c7-144">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-144">False</span></span>                                    |
| <span data-ttu-id="6c9c7-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c9c7-145">In Global Catalog</span></span>      | <span data-ttu-id="6c9c7-146">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-146">False</span></span>                                    |
| <span data-ttu-id="6c9c7-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c9c7-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c9c7-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c9c7-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="6c9c7-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c9c7-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="6c9c7-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c9c7-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="6c9c7-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9c7-151">Search-Flags</span></span>           | <span data-ttu-id="6c9c7-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c9c7-152">0x00000000</span></span>                               |
| <span data-ttu-id="6c9c7-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9c7-153">System-Flags</span></span>           | <span data-ttu-id="6c9c7-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c9c7-154">0x00000010</span></span>                               |
| <span data-ttu-id="6c9c7-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c9c7-155">Classes used in</span></span>        | [<span data-ttu-id="6c9c7-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="6c9c7-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6c9c7-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c9c7-157">Windows Server 2003</span></span>



| <span data-ttu-id="6c9c7-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c9c7-158">Entry</span></span> | <span data-ttu-id="6c9c7-159">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9c7-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="6c9c7-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c9c7-160">Link-Id</span></span>                | <span data-ttu-id="6c9c7-161">74</span><span class="sxs-lookup"><span data-stu-id="6c9c7-161">74</span></span>                                       |
| <span data-ttu-id="6c9c7-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c9c7-162">MAPI-Id</span></span>                | <span data-ttu-id="6c9c7-163">0x80b5</span><span class="sxs-lookup"><span data-stu-id="6c9c7-163">0x80B5</span></span>                                   |
| <span data-ttu-id="6c9c7-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c9c7-164">System-Only</span></span>            | <span data-ttu-id="6c9c7-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="6c9c7-165">True</span></span>                                     |
| <span data-ttu-id="6c9c7-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c9c7-166">Is-Single-Valued</span></span>       | <span data-ttu-id="6c9c7-167">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-167">False</span></span>                                    |
| <span data-ttu-id="6c9c7-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c9c7-168">Is Indexed</span></span>             | <span data-ttu-id="6c9c7-169">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-169">False</span></span>                                    |
| <span data-ttu-id="6c9c7-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c9c7-170">In Global Catalog</span></span>      | <span data-ttu-id="6c9c7-171">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-171">False</span></span>                                    |
| <span data-ttu-id="6c9c7-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c9c7-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c9c7-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c9c7-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="6c9c7-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c9c7-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="6c9c7-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c9c7-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="6c9c7-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9c7-176">Search-Flags</span></span>           | <span data-ttu-id="6c9c7-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c9c7-177">0x00000000</span></span>                               |
| <span data-ttu-id="6c9c7-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9c7-178">System-Flags</span></span>           | <span data-ttu-id="6c9c7-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c9c7-179">0x00000010</span></span>                               |
| <span data-ttu-id="6c9c7-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c9c7-180">Classes used in</span></span>        | [<span data-ttu-id="6c9c7-181">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="6c9c7-181">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6c9c7-182">Adam</span><span class="sxs-lookup"><span data-stu-id="6c9c7-182">ADAM</span></span>



| <span data-ttu-id="6c9c7-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c9c7-183">Entry</span></span> | <span data-ttu-id="6c9c7-184">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9c7-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="6c9c7-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c9c7-185">Link-Id</span></span>                | <span data-ttu-id="6c9c7-186">74</span><span class="sxs-lookup"><span data-stu-id="6c9c7-186">74</span></span>                                       |
| <span data-ttu-id="6c9c7-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c9c7-187">MAPI-Id</span></span>                | <span data-ttu-id="6c9c7-188">0x80b5</span><span class="sxs-lookup"><span data-stu-id="6c9c7-188">0x80B5</span></span>                                   |
| <span data-ttu-id="6c9c7-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c9c7-189">System-Only</span></span>            | <span data-ttu-id="6c9c7-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="6c9c7-190">True</span></span>                                     |
| <span data-ttu-id="6c9c7-191">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c9c7-191">Is-Single-Valued</span></span>       | <span data-ttu-id="6c9c7-192">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-192">False</span></span>                                    |
| <span data-ttu-id="6c9c7-193">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c9c7-193">Is Indexed</span></span>             | <span data-ttu-id="6c9c7-194">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-194">False</span></span>                                    |
| <span data-ttu-id="6c9c7-195">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c9c7-195">In Global Catalog</span></span>      | <span data-ttu-id="6c9c7-196">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-196">False</span></span>                                    |
| <span data-ttu-id="6c9c7-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c9c7-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c9c7-198">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c9c7-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="6c9c7-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c9c7-199">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="6c9c7-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c9c7-200">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="6c9c7-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9c7-201">Search-Flags</span></span>           | <span data-ttu-id="6c9c7-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c9c7-202">0x00000000</span></span>                               |
| <span data-ttu-id="6c9c7-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9c7-203">System-Flags</span></span>           | <span data-ttu-id="6c9c7-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c9c7-204">0x00000010</span></span>                               |
| <span data-ttu-id="6c9c7-205">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c9c7-205">Classes used in</span></span>        | [<span data-ttu-id="6c9c7-206">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="6c9c7-206">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6c9c7-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6c9c7-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6c9c7-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c9c7-208">Entry</span></span> | <span data-ttu-id="6c9c7-209">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9c7-209">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="6c9c7-210">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c9c7-210">Link-Id</span></span>                | <span data-ttu-id="6c9c7-211">74</span><span class="sxs-lookup"><span data-stu-id="6c9c7-211">74</span></span>                                       |
| <span data-ttu-id="6c9c7-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c9c7-212">MAPI-Id</span></span>                | <span data-ttu-id="6c9c7-213">0x80b5</span><span class="sxs-lookup"><span data-stu-id="6c9c7-213">0x80B5</span></span>                                   |
| <span data-ttu-id="6c9c7-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c9c7-214">System-Only</span></span>            | <span data-ttu-id="6c9c7-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="6c9c7-215">True</span></span>                                     |
| <span data-ttu-id="6c9c7-216">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c9c7-216">Is-Single-Valued</span></span>       | <span data-ttu-id="6c9c7-217">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-217">False</span></span>                                    |
| <span data-ttu-id="6c9c7-218">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c9c7-218">Is Indexed</span></span>             | <span data-ttu-id="6c9c7-219">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-219">False</span></span>                                    |
| <span data-ttu-id="6c9c7-220">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c9c7-220">In Global Catalog</span></span>      | <span data-ttu-id="6c9c7-221">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-221">False</span></span>                                    |
| <span data-ttu-id="6c9c7-222">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c9c7-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c9c7-223">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c9c7-223">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="6c9c7-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c9c7-224">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="6c9c7-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c9c7-225">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="6c9c7-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9c7-226">Search-Flags</span></span>           | <span data-ttu-id="6c9c7-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c9c7-227">0x00000000</span></span>                               |
| <span data-ttu-id="6c9c7-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9c7-228">System-Flags</span></span>           | <span data-ttu-id="6c9c7-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c9c7-229">0x00000010</span></span>                               |
| <span data-ttu-id="6c9c7-230">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c9c7-230">Classes used in</span></span>        | [<span data-ttu-id="6c9c7-231">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="6c9c7-231">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6c9c7-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c9c7-232">Windows Server 2008</span></span>



| <span data-ttu-id="6c9c7-233">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c9c7-233">Entry</span></span> | <span data-ttu-id="6c9c7-234">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9c7-234">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="6c9c7-235">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c9c7-235">Link-Id</span></span>                | <span data-ttu-id="6c9c7-236">74</span><span class="sxs-lookup"><span data-stu-id="6c9c7-236">74</span></span>                                       |
| <span data-ttu-id="6c9c7-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c9c7-237">MAPI-Id</span></span>                | <span data-ttu-id="6c9c7-238">0x80b5</span><span class="sxs-lookup"><span data-stu-id="6c9c7-238">0x80B5</span></span>                                   |
| <span data-ttu-id="6c9c7-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c9c7-239">System-Only</span></span>            | <span data-ttu-id="6c9c7-240">Richtig</span><span class="sxs-lookup"><span data-stu-id="6c9c7-240">True</span></span>                                     |
| <span data-ttu-id="6c9c7-241">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c9c7-241">Is-Single-Valued</span></span>       | <span data-ttu-id="6c9c7-242">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-242">False</span></span>                                    |
| <span data-ttu-id="6c9c7-243">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c9c7-243">Is Indexed</span></span>             | <span data-ttu-id="6c9c7-244">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-244">False</span></span>                                    |
| <span data-ttu-id="6c9c7-245">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c9c7-245">In Global Catalog</span></span>      | <span data-ttu-id="6c9c7-246">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-246">False</span></span>                                    |
| <span data-ttu-id="6c9c7-247">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c9c7-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c9c7-248">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c9c7-248">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="6c9c7-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c9c7-249">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="6c9c7-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c9c7-250">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="6c9c7-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9c7-251">Search-Flags</span></span>           | <span data-ttu-id="6c9c7-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c9c7-252">0x00000000</span></span>                               |
| <span data-ttu-id="6c9c7-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9c7-253">System-Flags</span></span>           | <span data-ttu-id="6c9c7-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c9c7-254">0x00000010</span></span>                               |
| <span data-ttu-id="6c9c7-255">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c9c7-255">Classes used in</span></span>        | [<span data-ttu-id="6c9c7-256">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="6c9c7-256">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6c9c7-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6c9c7-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6c9c7-258">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c9c7-258">Entry</span></span> | <span data-ttu-id="6c9c7-259">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9c7-259">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="6c9c7-260">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c9c7-260">Link-Id</span></span>                | <span data-ttu-id="6c9c7-261">74</span><span class="sxs-lookup"><span data-stu-id="6c9c7-261">74</span></span>                                       |
| <span data-ttu-id="6c9c7-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c9c7-262">MAPI-Id</span></span>                | <span data-ttu-id="6c9c7-263">0x80b5</span><span class="sxs-lookup"><span data-stu-id="6c9c7-263">0x80B5</span></span>                                   |
| <span data-ttu-id="6c9c7-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c9c7-264">System-Only</span></span>            | <span data-ttu-id="6c9c7-265">Richtig</span><span class="sxs-lookup"><span data-stu-id="6c9c7-265">True</span></span>                                     |
| <span data-ttu-id="6c9c7-266">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c9c7-266">Is-Single-Valued</span></span>       | <span data-ttu-id="6c9c7-267">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-267">False</span></span>                                    |
| <span data-ttu-id="6c9c7-268">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c9c7-268">Is Indexed</span></span>             | <span data-ttu-id="6c9c7-269">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-269">False</span></span>                                    |
| <span data-ttu-id="6c9c7-270">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c9c7-270">In Global Catalog</span></span>      | <span data-ttu-id="6c9c7-271">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-271">False</span></span>                                    |
| <span data-ttu-id="6c9c7-272">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c9c7-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c9c7-273">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c9c7-273">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="6c9c7-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c9c7-274">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="6c9c7-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c9c7-275">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="6c9c7-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9c7-276">Search-Flags</span></span>           | <span data-ttu-id="6c9c7-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c9c7-277">0x00000000</span></span>                               |
| <span data-ttu-id="6c9c7-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9c7-278">System-Flags</span></span>           | <span data-ttu-id="6c9c7-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c9c7-279">0x00000010</span></span>                               |
| <span data-ttu-id="6c9c7-280">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c9c7-280">Classes used in</span></span>        | [<span data-ttu-id="6c9c7-281">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="6c9c7-281">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6c9c7-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6c9c7-282">Windows Server 2012</span></span>



| <span data-ttu-id="6c9c7-283">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c9c7-283">Entry</span></span> | <span data-ttu-id="6c9c7-284">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9c7-284">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="6c9c7-285">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c9c7-285">Link-Id</span></span>                | <span data-ttu-id="6c9c7-286">74</span><span class="sxs-lookup"><span data-stu-id="6c9c7-286">74</span></span>                                       |
| <span data-ttu-id="6c9c7-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c9c7-287">MAPI-Id</span></span>                | <span data-ttu-id="6c9c7-288">0x80b5</span><span class="sxs-lookup"><span data-stu-id="6c9c7-288">0x80B5</span></span>                                   |
| <span data-ttu-id="6c9c7-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c9c7-289">System-Only</span></span>            | <span data-ttu-id="6c9c7-290">Richtig</span><span class="sxs-lookup"><span data-stu-id="6c9c7-290">True</span></span>                                     |
| <span data-ttu-id="6c9c7-291">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c9c7-291">Is-Single-Valued</span></span>       | <span data-ttu-id="6c9c7-292">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-292">False</span></span>                                    |
| <span data-ttu-id="6c9c7-293">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c9c7-293">Is Indexed</span></span>             | <span data-ttu-id="6c9c7-294">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-294">False</span></span>                                    |
| <span data-ttu-id="6c9c7-295">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c9c7-295">In Global Catalog</span></span>      | <span data-ttu-id="6c9c7-296">False</span><span class="sxs-lookup"><span data-stu-id="6c9c7-296">False</span></span>                                    |
| <span data-ttu-id="6c9c7-297">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c9c7-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c9c7-298">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c9c7-298">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="6c9c7-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c9c7-299">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="6c9c7-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c9c7-300">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="6c9c7-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9c7-301">Search-Flags</span></span>           | <span data-ttu-id="6c9c7-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c9c7-302">0x00000000</span></span>                               |
| <span data-ttu-id="6c9c7-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9c7-303">System-Flags</span></span>           | <span data-ttu-id="6c9c7-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c9c7-304">0x00000010</span></span>                               |
| <span data-ttu-id="6c9c7-305">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c9c7-305">Classes used in</span></span>        | [<span data-ttu-id="6c9c7-306">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="6c9c7-306">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





