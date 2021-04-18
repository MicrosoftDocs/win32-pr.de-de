---
title: Managed-Objects-Attribut
description: Enthält die Liste der Objekte, die vom Benutzer verwaltet werden. Die aufgelisteten Objekte sind solche, deren Eigenschaft ManagedBy auf diesen Benutzer festgelegt ist. Jedes Element in der Liste ist ein verknüpfter Verweis auf das verwaltete Objekt.
ms.assetid: 59b76431-03a5-4839-8800-ef03d26b66cc
ms.tgt_platform: multiple
keywords:
- AD-Schema für Managed-Objects-Attribut
- managedobjects-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Managed-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c7bc489d11c99f8790426a531e09a20f133476
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106343497"
---
# <a name="managed-objects-attribute"></a><span data-ttu-id="4e7a2-107">Managed-Objects-Attribut</span><span class="sxs-lookup"><span data-stu-id="4e7a2-107">Managed-Objects attribute</span></span>

<span data-ttu-id="4e7a2-108">Enthält die Liste der Objekte, die vom Benutzer verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="4e7a2-108">Contains the list of objects that are managed by the user.</span></span> <span data-ttu-id="4e7a2-109">Die aufgelisteten Objekte sind solche, deren Eigenschaft ManagedBy auf diesen Benutzer festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4e7a2-109">The objects listed are those that have the property managedBy property set to this user.</span></span> <span data-ttu-id="4e7a2-110">Jedes Element in der Liste ist ein verknüpfter Verweis auf das verwaltete Objekt.</span><span class="sxs-lookup"><span data-stu-id="4e7a2-110">Each item in the list is a linked reference to the managed object.</span></span>



| <span data-ttu-id="4e7a2-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4e7a2-111">Entry</span></span> | <span data-ttu-id="4e7a2-112">Wert</span><span class="sxs-lookup"><span data-stu-id="4e7a2-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4e7a2-113">CN</span><span class="sxs-lookup"><span data-stu-id="4e7a2-113">CN</span></span>                | <span data-ttu-id="4e7a2-114">Managed-Objects</span><span class="sxs-lookup"><span data-stu-id="4e7a2-114">Managed-Objects</span></span>                                                                    |
| <span data-ttu-id="4e7a2-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4e7a2-115">Ldap-Display-Name</span></span> | <span data-ttu-id="4e7a2-116">managedObjects</span><span class="sxs-lookup"><span data-stu-id="4e7a2-116">managedObjects</span></span>                                                                     |
| <span data-ttu-id="4e7a2-117">Size</span><span class="sxs-lookup"><span data-stu-id="4e7a2-117">Size</span></span>              | \-                                                                                 |
| <span data-ttu-id="4e7a2-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="4e7a2-118">Update Privilege</span></span>  | <span data-ttu-id="4e7a2-119">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4e7a2-119">This value is set by the system.</span></span>                                                   |
| <span data-ttu-id="4e7a2-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="4e7a2-120">Update Frequency</span></span>  | <span data-ttu-id="4e7a2-121">Wenn der Benutzerdaten Satz erstellt wird und die verwalteten Objekte geändert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="4e7a2-121">When the users record is created and whenever the managed objects needs to change.</span></span> |
| <span data-ttu-id="4e7a2-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4e7a2-122">Attribute-Id</span></span>      | <span data-ttu-id="4e7a2-123">1.2.840.113556.1.4.654</span><span class="sxs-lookup"><span data-stu-id="4e7a2-123">1.2.840.113556.1.4.654</span></span>                                                             |
| <span data-ttu-id="4e7a2-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4e7a2-124">System-Id-Guid</span></span>    | <span data-ttu-id="4e7a2-125">0296c124-40DA-11d1-a9c0-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="4e7a2-125">0296c124-40da-11d1-a9c0-0000f80367c1</span></span>                                               |
| <span data-ttu-id="4e7a2-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e7a2-126">Syntax</span></span>            | [<span data-ttu-id="4e7a2-127">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="4e7a2-127">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                                            |



## <a name="implementations"></a><span data-ttu-id="4e7a2-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="4e7a2-128">Implementations</span></span>

-   [<span data-ttu-id="4e7a2-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4e7a2-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4e7a2-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4e7a2-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4e7a2-131">**Adam**</span><span class="sxs-lookup"><span data-stu-id="4e7a2-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4e7a2-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4e7a2-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4e7a2-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4e7a2-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4e7a2-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4e7a2-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4e7a2-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4e7a2-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4e7a2-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4e7a2-136">Windows 2000 Server</span></span>



| <span data-ttu-id="4e7a2-137">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4e7a2-137">Entry</span></span> | <span data-ttu-id="4e7a2-138">Wert</span><span class="sxs-lookup"><span data-stu-id="4e7a2-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4e7a2-139">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4e7a2-139">Link-Id</span></span>                | <span data-ttu-id="4e7a2-140">73</span><span class="sxs-lookup"><span data-stu-id="4e7a2-140">73</span></span>                              |
| <span data-ttu-id="4e7a2-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e7a2-141">MAPI-Id</span></span>                | <span data-ttu-id="4e7a2-142">0x8024</span><span class="sxs-lookup"><span data-stu-id="4e7a2-142">0x8024</span></span>                          |
| <span data-ttu-id="4e7a2-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e7a2-143">System-Only</span></span>            | <span data-ttu-id="4e7a2-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="4e7a2-144">True</span></span>                            |
| <span data-ttu-id="4e7a2-145">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4e7a2-145">Is-Single-Valued</span></span>       | <span data-ttu-id="4e7a2-146">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-146">False</span></span>                           |
| <span data-ttu-id="4e7a2-147">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4e7a2-147">Is Indexed</span></span>             | <span data-ttu-id="4e7a2-148">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-148">False</span></span>                           |
| <span data-ttu-id="4e7a2-149">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4e7a2-149">In Global Catalog</span></span>      | <span data-ttu-id="4e7a2-150">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-150">False</span></span>                           |
| <span data-ttu-id="4e7a2-151">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4e7a2-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e7a2-152">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4e7a2-152">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4e7a2-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e7a2-153">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4e7a2-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e7a2-154">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4e7a2-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e7a2-155">Search-Flags</span></span>           | <span data-ttu-id="4e7a2-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e7a2-156">0x00000000</span></span>                      |
| <span data-ttu-id="4e7a2-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e7a2-157">System-Flags</span></span>           | <span data-ttu-id="4e7a2-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e7a2-158">0x00000010</span></span>                      |
| <span data-ttu-id="4e7a2-159">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4e7a2-159">Classes used in</span></span>        | [<span data-ttu-id="4e7a2-160">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="4e7a2-160">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4e7a2-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4e7a2-161">Windows Server 2003</span></span>



| <span data-ttu-id="4e7a2-162">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4e7a2-162">Entry</span></span> | <span data-ttu-id="4e7a2-163">Wert</span><span class="sxs-lookup"><span data-stu-id="4e7a2-163">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4e7a2-164">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4e7a2-164">Link-Id</span></span>                | <span data-ttu-id="4e7a2-165">73</span><span class="sxs-lookup"><span data-stu-id="4e7a2-165">73</span></span>                              |
| <span data-ttu-id="4e7a2-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e7a2-166">MAPI-Id</span></span>                | <span data-ttu-id="4e7a2-167">0x8024</span><span class="sxs-lookup"><span data-stu-id="4e7a2-167">0x8024</span></span>                          |
| <span data-ttu-id="4e7a2-168">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e7a2-168">System-Only</span></span>            | <span data-ttu-id="4e7a2-169">Richtig</span><span class="sxs-lookup"><span data-stu-id="4e7a2-169">True</span></span>                            |
| <span data-ttu-id="4e7a2-170">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4e7a2-170">Is-Single-Valued</span></span>       | <span data-ttu-id="4e7a2-171">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-171">False</span></span>                           |
| <span data-ttu-id="4e7a2-172">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4e7a2-172">Is Indexed</span></span>             | <span data-ttu-id="4e7a2-173">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-173">False</span></span>                           |
| <span data-ttu-id="4e7a2-174">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4e7a2-174">In Global Catalog</span></span>      | <span data-ttu-id="4e7a2-175">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-175">False</span></span>                           |
| <span data-ttu-id="4e7a2-176">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4e7a2-176">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e7a2-177">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4e7a2-177">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4e7a2-178">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e7a2-178">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4e7a2-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e7a2-179">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4e7a2-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e7a2-180">Search-Flags</span></span>           | <span data-ttu-id="4e7a2-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e7a2-181">0x00000000</span></span>                      |
| <span data-ttu-id="4e7a2-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e7a2-182">System-Flags</span></span>           | <span data-ttu-id="4e7a2-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e7a2-183">0x00000010</span></span>                      |
| <span data-ttu-id="4e7a2-184">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4e7a2-184">Classes used in</span></span>        | [<span data-ttu-id="4e7a2-185">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="4e7a2-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4e7a2-186">Adam</span><span class="sxs-lookup"><span data-stu-id="4e7a2-186">ADAM</span></span>



| <span data-ttu-id="4e7a2-187">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4e7a2-187">Entry</span></span> | <span data-ttu-id="4e7a2-188">Wert</span><span class="sxs-lookup"><span data-stu-id="4e7a2-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4e7a2-189">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4e7a2-189">Link-Id</span></span>                | <span data-ttu-id="4e7a2-190">73</span><span class="sxs-lookup"><span data-stu-id="4e7a2-190">73</span></span>                              |
| <span data-ttu-id="4e7a2-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e7a2-191">MAPI-Id</span></span>                | <span data-ttu-id="4e7a2-192">0x8024</span><span class="sxs-lookup"><span data-stu-id="4e7a2-192">0x8024</span></span>                          |
| <span data-ttu-id="4e7a2-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e7a2-193">System-Only</span></span>            | <span data-ttu-id="4e7a2-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="4e7a2-194">True</span></span>                            |
| <span data-ttu-id="4e7a2-195">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4e7a2-195">Is-Single-Valued</span></span>       | <span data-ttu-id="4e7a2-196">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-196">False</span></span>                           |
| <span data-ttu-id="4e7a2-197">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4e7a2-197">Is Indexed</span></span>             | <span data-ttu-id="4e7a2-198">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-198">False</span></span>                           |
| <span data-ttu-id="4e7a2-199">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4e7a2-199">In Global Catalog</span></span>      | <span data-ttu-id="4e7a2-200">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-200">False</span></span>                           |
| <span data-ttu-id="4e7a2-201">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4e7a2-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e7a2-202">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4e7a2-202">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4e7a2-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e7a2-203">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4e7a2-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e7a2-204">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4e7a2-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e7a2-205">Search-Flags</span></span>           | <span data-ttu-id="4e7a2-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e7a2-206">0x00000000</span></span>                      |
| <span data-ttu-id="4e7a2-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e7a2-207">System-Flags</span></span>           | <span data-ttu-id="4e7a2-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e7a2-208">0x00000010</span></span>                      |
| <span data-ttu-id="4e7a2-209">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4e7a2-209">Classes used in</span></span>        | [<span data-ttu-id="4e7a2-210">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="4e7a2-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4e7a2-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4e7a2-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4e7a2-212">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4e7a2-212">Entry</span></span> | <span data-ttu-id="4e7a2-213">Wert</span><span class="sxs-lookup"><span data-stu-id="4e7a2-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4e7a2-214">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4e7a2-214">Link-Id</span></span>                | <span data-ttu-id="4e7a2-215">73</span><span class="sxs-lookup"><span data-stu-id="4e7a2-215">73</span></span>                              |
| <span data-ttu-id="4e7a2-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e7a2-216">MAPI-Id</span></span>                | <span data-ttu-id="4e7a2-217">0x8024</span><span class="sxs-lookup"><span data-stu-id="4e7a2-217">0x8024</span></span>                          |
| <span data-ttu-id="4e7a2-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e7a2-218">System-Only</span></span>            | <span data-ttu-id="4e7a2-219">Richtig</span><span class="sxs-lookup"><span data-stu-id="4e7a2-219">True</span></span>                            |
| <span data-ttu-id="4e7a2-220">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4e7a2-220">Is-Single-Valued</span></span>       | <span data-ttu-id="4e7a2-221">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-221">False</span></span>                           |
| <span data-ttu-id="4e7a2-222">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4e7a2-222">Is Indexed</span></span>             | <span data-ttu-id="4e7a2-223">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-223">False</span></span>                           |
| <span data-ttu-id="4e7a2-224">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4e7a2-224">In Global Catalog</span></span>      | <span data-ttu-id="4e7a2-225">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-225">False</span></span>                           |
| <span data-ttu-id="4e7a2-226">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4e7a2-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e7a2-227">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4e7a2-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4e7a2-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e7a2-228">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4e7a2-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e7a2-229">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4e7a2-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e7a2-230">Search-Flags</span></span>           | <span data-ttu-id="4e7a2-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e7a2-231">0x00000000</span></span>                      |
| <span data-ttu-id="4e7a2-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e7a2-232">System-Flags</span></span>           | <span data-ttu-id="4e7a2-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e7a2-233">0x00000010</span></span>                      |
| <span data-ttu-id="4e7a2-234">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4e7a2-234">Classes used in</span></span>        | [<span data-ttu-id="4e7a2-235">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="4e7a2-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4e7a2-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e7a2-236">Windows Server 2008</span></span>



| <span data-ttu-id="4e7a2-237">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4e7a2-237">Entry</span></span> | <span data-ttu-id="4e7a2-238">Wert</span><span class="sxs-lookup"><span data-stu-id="4e7a2-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4e7a2-239">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4e7a2-239">Link-Id</span></span>                | <span data-ttu-id="4e7a2-240">73</span><span class="sxs-lookup"><span data-stu-id="4e7a2-240">73</span></span>                              |
| <span data-ttu-id="4e7a2-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e7a2-241">MAPI-Id</span></span>                | <span data-ttu-id="4e7a2-242">0x8024</span><span class="sxs-lookup"><span data-stu-id="4e7a2-242">0x8024</span></span>                          |
| <span data-ttu-id="4e7a2-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e7a2-243">System-Only</span></span>            | <span data-ttu-id="4e7a2-244">Richtig</span><span class="sxs-lookup"><span data-stu-id="4e7a2-244">True</span></span>                            |
| <span data-ttu-id="4e7a2-245">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4e7a2-245">Is-Single-Valued</span></span>       | <span data-ttu-id="4e7a2-246">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-246">False</span></span>                           |
| <span data-ttu-id="4e7a2-247">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4e7a2-247">Is Indexed</span></span>             | <span data-ttu-id="4e7a2-248">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-248">False</span></span>                           |
| <span data-ttu-id="4e7a2-249">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4e7a2-249">In Global Catalog</span></span>      | <span data-ttu-id="4e7a2-250">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-250">False</span></span>                           |
| <span data-ttu-id="4e7a2-251">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4e7a2-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e7a2-252">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4e7a2-252">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4e7a2-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e7a2-253">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4e7a2-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e7a2-254">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4e7a2-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e7a2-255">Search-Flags</span></span>           | <span data-ttu-id="4e7a2-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e7a2-256">0x00000000</span></span>                      |
| <span data-ttu-id="4e7a2-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e7a2-257">System-Flags</span></span>           | <span data-ttu-id="4e7a2-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e7a2-258">0x00000010</span></span>                      |
| <span data-ttu-id="4e7a2-259">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4e7a2-259">Classes used in</span></span>        | [<span data-ttu-id="4e7a2-260">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="4e7a2-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4e7a2-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4e7a2-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4e7a2-262">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4e7a2-262">Entry</span></span> | <span data-ttu-id="4e7a2-263">Wert</span><span class="sxs-lookup"><span data-stu-id="4e7a2-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4e7a2-264">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4e7a2-264">Link-Id</span></span>                | <span data-ttu-id="4e7a2-265">73</span><span class="sxs-lookup"><span data-stu-id="4e7a2-265">73</span></span>                              |
| <span data-ttu-id="4e7a2-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e7a2-266">MAPI-Id</span></span>                | <span data-ttu-id="4e7a2-267">0x8024</span><span class="sxs-lookup"><span data-stu-id="4e7a2-267">0x8024</span></span>                          |
| <span data-ttu-id="4e7a2-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e7a2-268">System-Only</span></span>            | <span data-ttu-id="4e7a2-269">Richtig</span><span class="sxs-lookup"><span data-stu-id="4e7a2-269">True</span></span>                            |
| <span data-ttu-id="4e7a2-270">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4e7a2-270">Is-Single-Valued</span></span>       | <span data-ttu-id="4e7a2-271">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-271">False</span></span>                           |
| <span data-ttu-id="4e7a2-272">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4e7a2-272">Is Indexed</span></span>             | <span data-ttu-id="4e7a2-273">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-273">False</span></span>                           |
| <span data-ttu-id="4e7a2-274">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4e7a2-274">In Global Catalog</span></span>      | <span data-ttu-id="4e7a2-275">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-275">False</span></span>                           |
| <span data-ttu-id="4e7a2-276">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4e7a2-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e7a2-277">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4e7a2-277">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4e7a2-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e7a2-278">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4e7a2-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e7a2-279">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4e7a2-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e7a2-280">Search-Flags</span></span>           | <span data-ttu-id="4e7a2-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e7a2-281">0x00000000</span></span>                      |
| <span data-ttu-id="4e7a2-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e7a2-282">System-Flags</span></span>           | <span data-ttu-id="4e7a2-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e7a2-283">0x00000010</span></span>                      |
| <span data-ttu-id="4e7a2-284">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4e7a2-284">Classes used in</span></span>        | [<span data-ttu-id="4e7a2-285">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="4e7a2-285">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4e7a2-286">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4e7a2-286">Windows Server 2012</span></span>



| <span data-ttu-id="4e7a2-287">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4e7a2-287">Entry</span></span> | <span data-ttu-id="4e7a2-288">Wert</span><span class="sxs-lookup"><span data-stu-id="4e7a2-288">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4e7a2-289">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4e7a2-289">Link-Id</span></span>                | <span data-ttu-id="4e7a2-290">73</span><span class="sxs-lookup"><span data-stu-id="4e7a2-290">73</span></span>                              |
| <span data-ttu-id="4e7a2-291">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e7a2-291">MAPI-Id</span></span>                | <span data-ttu-id="4e7a2-292">0x8024</span><span class="sxs-lookup"><span data-stu-id="4e7a2-292">0x8024</span></span>                          |
| <span data-ttu-id="4e7a2-293">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e7a2-293">System-Only</span></span>            | <span data-ttu-id="4e7a2-294">Richtig</span><span class="sxs-lookup"><span data-stu-id="4e7a2-294">True</span></span>                            |
| <span data-ttu-id="4e7a2-295">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4e7a2-295">Is-Single-Valued</span></span>       | <span data-ttu-id="4e7a2-296">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-296">False</span></span>                           |
| <span data-ttu-id="4e7a2-297">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4e7a2-297">Is Indexed</span></span>             | <span data-ttu-id="4e7a2-298">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-298">False</span></span>                           |
| <span data-ttu-id="4e7a2-299">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4e7a2-299">In Global Catalog</span></span>      | <span data-ttu-id="4e7a2-300">False</span><span class="sxs-lookup"><span data-stu-id="4e7a2-300">False</span></span>                           |
| <span data-ttu-id="4e7a2-301">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4e7a2-301">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e7a2-302">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4e7a2-302">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4e7a2-303">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e7a2-303">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4e7a2-304">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e7a2-304">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4e7a2-305">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e7a2-305">Search-Flags</span></span>           | <span data-ttu-id="4e7a2-306">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e7a2-306">0x00000000</span></span>                      |
| <span data-ttu-id="4e7a2-307">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e7a2-307">System-Flags</span></span>           | <span data-ttu-id="4e7a2-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e7a2-308">0x00000010</span></span>                      |
| <span data-ttu-id="4e7a2-309">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4e7a2-309">Classes used in</span></span>        | [<span data-ttu-id="4e7a2-310">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="4e7a2-310">**Top**</span></span>](c-top.md)<br/> |



 

 





