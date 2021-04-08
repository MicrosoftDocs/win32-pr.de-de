---
title: Object-Guid-Attribut
description: Der eindeutige Bezeichner für ein-Objekt.
ms.assetid: fc2d65a3-7472-41ef-9780-d1a7ec965804
ms.tgt_platform: multiple
keywords:
- AD-Schema für Object-Guid-Attribut
- objectGUID-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Object-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07e3715c38b629869296e6f8df5dbebd9a515d1b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859795"
---
# <a name="object-guid-attribute"></a><span data-ttu-id="b8bac-105">Object-Guid-Attribut</span><span class="sxs-lookup"><span data-stu-id="b8bac-105">Object-Guid attribute</span></span>

<span data-ttu-id="b8bac-106">Der eindeutige Bezeichner für ein-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b8bac-106">The unique identifier for an object.</span></span>



| <span data-ttu-id="b8bac-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b8bac-107">Entry</span></span> | <span data-ttu-id="b8bac-108">Wert</span><span class="sxs-lookup"><span data-stu-id="b8bac-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b8bac-109">CN</span><span class="sxs-lookup"><span data-stu-id="b8bac-109">CN</span></span>                | <span data-ttu-id="b8bac-110">Object-Guid</span><span class="sxs-lookup"><span data-stu-id="b8bac-110">Object-Guid</span></span>                                                         |
| <span data-ttu-id="b8bac-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b8bac-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b8bac-112">objectGUID</span><span class="sxs-lookup"><span data-stu-id="b8bac-112">objectGUID</span></span>                                                          |
| <span data-ttu-id="b8bac-113">Size</span><span class="sxs-lookup"><span data-stu-id="b8bac-113">Size</span></span>              | <span data-ttu-id="b8bac-114">16 Bytes</span><span class="sxs-lookup"><span data-stu-id="b8bac-114">16 bytes</span></span>                                                            |
| <span data-ttu-id="b8bac-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b8bac-115">Update Privilege</span></span>  | <span data-ttu-id="b8bac-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b8bac-116">This value is set by the system.</span></span>                                    |
| <span data-ttu-id="b8bac-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b8bac-117">Update Frequency</span></span>  | <span data-ttu-id="b8bac-118">Dieser Wert wird festgelegt, wenn das Objekt erstellt wird, und kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b8bac-118">This value is set when the object is created and cannot be changed.</span></span> |
| <span data-ttu-id="b8bac-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b8bac-119">Attribute-Id</span></span>      | <span data-ttu-id="b8bac-120">1.2.840.113556.1.4.2</span><span class="sxs-lookup"><span data-stu-id="b8bac-120">1.2.840.113556.1.4.2</span></span>                                                |
| <span data-ttu-id="b8bac-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b8bac-121">System-Id-Guid</span></span>    | <span data-ttu-id="b8bac-122">bf9679e7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b8bac-122">bf9679e7-0de6-11d0-a285-00aa003049e2</span></span>                                |
| <span data-ttu-id="b8bac-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8bac-123">Syntax</span></span>            | [<span data-ttu-id="b8bac-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="b8bac-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)               |



## <a name="implementations"></a><span data-ttu-id="b8bac-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b8bac-125">Implementations</span></span>

-   [<span data-ttu-id="b8bac-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b8bac-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b8bac-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b8bac-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b8bac-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="b8bac-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b8bac-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b8bac-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b8bac-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b8bac-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b8bac-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b8bac-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b8bac-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b8bac-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b8bac-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b8bac-133">Windows 2000 Server</span></span>



| <span data-ttu-id="b8bac-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b8bac-134">Entry</span></span> | <span data-ttu-id="b8bac-135">Wert</span><span class="sxs-lookup"><span data-stu-id="b8bac-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8bac-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b8bac-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8bac-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8bac-137">MAPI-Id</span></span>                | <span data-ttu-id="b8bac-138">0x8c6d</span><span class="sxs-lookup"><span data-stu-id="b8bac-138">0x8C6D</span></span>                          |
| <span data-ttu-id="b8bac-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8bac-139">System-Only</span></span>            | <span data-ttu-id="b8bac-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-140">True</span></span>                            |
| <span data-ttu-id="b8bac-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b8bac-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b8bac-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-142">True</span></span>                            |
| <span data-ttu-id="b8bac-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b8bac-143">Is Indexed</span></span>             | <span data-ttu-id="b8bac-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-144">True</span></span>                            |
| <span data-ttu-id="b8bac-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b8bac-145">In Global Catalog</span></span>      | <span data-ttu-id="b8bac-146">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-146">True</span></span>                            |
| <span data-ttu-id="b8bac-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8bac-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8bac-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b8bac-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8bac-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8bac-149">Range-Lower</span></span>            | <span data-ttu-id="b8bac-150">16</span><span class="sxs-lookup"><span data-stu-id="b8bac-150">16</span></span>                              |
| <span data-ttu-id="b8bac-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8bac-151">Range-Upper</span></span>            | <span data-ttu-id="b8bac-152">16</span><span class="sxs-lookup"><span data-stu-id="b8bac-152">16</span></span>                              |
| <span data-ttu-id="b8bac-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bac-153">Search-Flags</span></span>           | <span data-ttu-id="b8bac-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b8bac-154">0x00000009</span></span>                      |
| <span data-ttu-id="b8bac-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bac-155">System-Flags</span></span>           | <span data-ttu-id="b8bac-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8bac-156">0x00000013</span></span>                      |
| <span data-ttu-id="b8bac-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b8bac-157">Classes used in</span></span>        | [<span data-ttu-id="b8bac-158">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b8bac-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b8bac-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8bac-159">Windows Server 2003</span></span>



| <span data-ttu-id="b8bac-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b8bac-160">Entry</span></span> | <span data-ttu-id="b8bac-161">Wert</span><span class="sxs-lookup"><span data-stu-id="b8bac-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8bac-162">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b8bac-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8bac-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8bac-163">MAPI-Id</span></span>                | <span data-ttu-id="b8bac-164">0x8c6d</span><span class="sxs-lookup"><span data-stu-id="b8bac-164">0x8C6D</span></span>                          |
| <span data-ttu-id="b8bac-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8bac-165">System-Only</span></span>            | <span data-ttu-id="b8bac-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-166">True</span></span>                            |
| <span data-ttu-id="b8bac-167">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b8bac-167">Is-Single-Valued</span></span>       | <span data-ttu-id="b8bac-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-168">True</span></span>                            |
| <span data-ttu-id="b8bac-169">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b8bac-169">Is Indexed</span></span>             | <span data-ttu-id="b8bac-170">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-170">True</span></span>                            |
| <span data-ttu-id="b8bac-171">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b8bac-171">In Global Catalog</span></span>      | <span data-ttu-id="b8bac-172">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-172">True</span></span>                            |
| <span data-ttu-id="b8bac-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8bac-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8bac-174">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b8bac-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8bac-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8bac-175">Range-Lower</span></span>            | <span data-ttu-id="b8bac-176">16</span><span class="sxs-lookup"><span data-stu-id="b8bac-176">16</span></span>                              |
| <span data-ttu-id="b8bac-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8bac-177">Range-Upper</span></span>            | <span data-ttu-id="b8bac-178">16</span><span class="sxs-lookup"><span data-stu-id="b8bac-178">16</span></span>                              |
| <span data-ttu-id="b8bac-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bac-179">Search-Flags</span></span>           | <span data-ttu-id="b8bac-180">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b8bac-180">0x00000009</span></span>                      |
| <span data-ttu-id="b8bac-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bac-181">System-Flags</span></span>           | <span data-ttu-id="b8bac-182">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8bac-182">0x00000013</span></span>                      |
| <span data-ttu-id="b8bac-183">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b8bac-183">Classes used in</span></span>        | [<span data-ttu-id="b8bac-184">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b8bac-184">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b8bac-185">Adam</span><span class="sxs-lookup"><span data-stu-id="b8bac-185">ADAM</span></span>



| <span data-ttu-id="b8bac-186">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b8bac-186">Entry</span></span> | <span data-ttu-id="b8bac-187">Wert</span><span class="sxs-lookup"><span data-stu-id="b8bac-187">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8bac-188">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b8bac-188">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8bac-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8bac-189">MAPI-Id</span></span>                | <span data-ttu-id="b8bac-190">0x8c6d</span><span class="sxs-lookup"><span data-stu-id="b8bac-190">0x8C6D</span></span>                          |
| <span data-ttu-id="b8bac-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8bac-191">System-Only</span></span>            | <span data-ttu-id="b8bac-192">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-192">True</span></span>                            |
| <span data-ttu-id="b8bac-193">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b8bac-193">Is-Single-Valued</span></span>       | <span data-ttu-id="b8bac-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-194">True</span></span>                            |
| <span data-ttu-id="b8bac-195">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b8bac-195">Is Indexed</span></span>             | <span data-ttu-id="b8bac-196">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-196">True</span></span>                            |
| <span data-ttu-id="b8bac-197">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b8bac-197">In Global Catalog</span></span>      | <span data-ttu-id="b8bac-198">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-198">True</span></span>                            |
| <span data-ttu-id="b8bac-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8bac-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8bac-200">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b8bac-200">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8bac-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8bac-201">Range-Lower</span></span>            | <span data-ttu-id="b8bac-202">16</span><span class="sxs-lookup"><span data-stu-id="b8bac-202">16</span></span>                              |
| <span data-ttu-id="b8bac-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8bac-203">Range-Upper</span></span>            | <span data-ttu-id="b8bac-204">16</span><span class="sxs-lookup"><span data-stu-id="b8bac-204">16</span></span>                              |
| <span data-ttu-id="b8bac-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bac-205">Search-Flags</span></span>           | <span data-ttu-id="b8bac-206">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b8bac-206">0x00000009</span></span>                      |
| <span data-ttu-id="b8bac-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bac-207">System-Flags</span></span>           | <span data-ttu-id="b8bac-208">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8bac-208">0x00000013</span></span>                      |
| <span data-ttu-id="b8bac-209">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b8bac-209">Classes used in</span></span>        | [<span data-ttu-id="b8bac-210">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b8bac-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b8bac-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b8bac-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b8bac-212">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b8bac-212">Entry</span></span> | <span data-ttu-id="b8bac-213">Wert</span><span class="sxs-lookup"><span data-stu-id="b8bac-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8bac-214">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b8bac-214">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8bac-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8bac-215">MAPI-Id</span></span>                | <span data-ttu-id="b8bac-216">0x8c6d</span><span class="sxs-lookup"><span data-stu-id="b8bac-216">0x8C6D</span></span>                          |
| <span data-ttu-id="b8bac-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8bac-217">System-Only</span></span>            | <span data-ttu-id="b8bac-218">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-218">True</span></span>                            |
| <span data-ttu-id="b8bac-219">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b8bac-219">Is-Single-Valued</span></span>       | <span data-ttu-id="b8bac-220">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-220">True</span></span>                            |
| <span data-ttu-id="b8bac-221">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b8bac-221">Is Indexed</span></span>             | <span data-ttu-id="b8bac-222">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-222">True</span></span>                            |
| <span data-ttu-id="b8bac-223">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b8bac-223">In Global Catalog</span></span>      | <span data-ttu-id="b8bac-224">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-224">True</span></span>                            |
| <span data-ttu-id="b8bac-225">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8bac-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8bac-226">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b8bac-226">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8bac-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8bac-227">Range-Lower</span></span>            | <span data-ttu-id="b8bac-228">16</span><span class="sxs-lookup"><span data-stu-id="b8bac-228">16</span></span>                              |
| <span data-ttu-id="b8bac-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8bac-229">Range-Upper</span></span>            | <span data-ttu-id="b8bac-230">16</span><span class="sxs-lookup"><span data-stu-id="b8bac-230">16</span></span>                              |
| <span data-ttu-id="b8bac-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bac-231">Search-Flags</span></span>           | <span data-ttu-id="b8bac-232">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b8bac-232">0x00000009</span></span>                      |
| <span data-ttu-id="b8bac-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bac-233">System-Flags</span></span>           | <span data-ttu-id="b8bac-234">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8bac-234">0x00000013</span></span>                      |
| <span data-ttu-id="b8bac-235">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b8bac-235">Classes used in</span></span>        | [<span data-ttu-id="b8bac-236">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b8bac-236">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b8bac-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8bac-237">Windows Server 2008</span></span>



| <span data-ttu-id="b8bac-238">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b8bac-238">Entry</span></span> | <span data-ttu-id="b8bac-239">Wert</span><span class="sxs-lookup"><span data-stu-id="b8bac-239">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8bac-240">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b8bac-240">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8bac-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8bac-241">MAPI-Id</span></span>                | <span data-ttu-id="b8bac-242">0x8c6d</span><span class="sxs-lookup"><span data-stu-id="b8bac-242">0x8C6D</span></span>                          |
| <span data-ttu-id="b8bac-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8bac-243">System-Only</span></span>            | <span data-ttu-id="b8bac-244">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-244">True</span></span>                            |
| <span data-ttu-id="b8bac-245">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b8bac-245">Is-Single-Valued</span></span>       | <span data-ttu-id="b8bac-246">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-246">True</span></span>                            |
| <span data-ttu-id="b8bac-247">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b8bac-247">Is Indexed</span></span>             | <span data-ttu-id="b8bac-248">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-248">True</span></span>                            |
| <span data-ttu-id="b8bac-249">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b8bac-249">In Global Catalog</span></span>      | <span data-ttu-id="b8bac-250">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-250">True</span></span>                            |
| <span data-ttu-id="b8bac-251">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8bac-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8bac-252">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b8bac-252">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8bac-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8bac-253">Range-Lower</span></span>            | <span data-ttu-id="b8bac-254">16</span><span class="sxs-lookup"><span data-stu-id="b8bac-254">16</span></span>                              |
| <span data-ttu-id="b8bac-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8bac-255">Range-Upper</span></span>            | <span data-ttu-id="b8bac-256">16</span><span class="sxs-lookup"><span data-stu-id="b8bac-256">16</span></span>                              |
| <span data-ttu-id="b8bac-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bac-257">Search-Flags</span></span>           | <span data-ttu-id="b8bac-258">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b8bac-258">0x00000009</span></span>                      |
| <span data-ttu-id="b8bac-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bac-259">System-Flags</span></span>           | <span data-ttu-id="b8bac-260">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8bac-260">0x00000013</span></span>                      |
| <span data-ttu-id="b8bac-261">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b8bac-261">Classes used in</span></span>        | [<span data-ttu-id="b8bac-262">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b8bac-262">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b8bac-263">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8bac-263">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b8bac-264">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b8bac-264">Entry</span></span> | <span data-ttu-id="b8bac-265">Wert</span><span class="sxs-lookup"><span data-stu-id="b8bac-265">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8bac-266">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b8bac-266">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8bac-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8bac-267">MAPI-Id</span></span>                | <span data-ttu-id="b8bac-268">0x8c6d</span><span class="sxs-lookup"><span data-stu-id="b8bac-268">0x8C6D</span></span>                          |
| <span data-ttu-id="b8bac-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8bac-269">System-Only</span></span>            | <span data-ttu-id="b8bac-270">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-270">True</span></span>                            |
| <span data-ttu-id="b8bac-271">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b8bac-271">Is-Single-Valued</span></span>       | <span data-ttu-id="b8bac-272">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-272">True</span></span>                            |
| <span data-ttu-id="b8bac-273">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b8bac-273">Is Indexed</span></span>             | <span data-ttu-id="b8bac-274">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-274">True</span></span>                            |
| <span data-ttu-id="b8bac-275">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b8bac-275">In Global Catalog</span></span>      | <span data-ttu-id="b8bac-276">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-276">True</span></span>                            |
| <span data-ttu-id="b8bac-277">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8bac-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8bac-278">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b8bac-278">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8bac-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8bac-279">Range-Lower</span></span>            | <span data-ttu-id="b8bac-280">16</span><span class="sxs-lookup"><span data-stu-id="b8bac-280">16</span></span>                              |
| <span data-ttu-id="b8bac-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8bac-281">Range-Upper</span></span>            | <span data-ttu-id="b8bac-282">16</span><span class="sxs-lookup"><span data-stu-id="b8bac-282">16</span></span>                              |
| <span data-ttu-id="b8bac-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bac-283">Search-Flags</span></span>           | <span data-ttu-id="b8bac-284">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b8bac-284">0x00000009</span></span>                      |
| <span data-ttu-id="b8bac-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bac-285">System-Flags</span></span>           | <span data-ttu-id="b8bac-286">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8bac-286">0x00000013</span></span>                      |
| <span data-ttu-id="b8bac-287">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b8bac-287">Classes used in</span></span>        | [<span data-ttu-id="b8bac-288">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b8bac-288">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b8bac-289">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8bac-289">Windows Server 2012</span></span>



| <span data-ttu-id="b8bac-290">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b8bac-290">Entry</span></span> | <span data-ttu-id="b8bac-291">Wert</span><span class="sxs-lookup"><span data-stu-id="b8bac-291">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8bac-292">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b8bac-292">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8bac-293">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8bac-293">MAPI-Id</span></span>                | <span data-ttu-id="b8bac-294">0x8c6d</span><span class="sxs-lookup"><span data-stu-id="b8bac-294">0x8C6D</span></span>                          |
| <span data-ttu-id="b8bac-295">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8bac-295">System-Only</span></span>            | <span data-ttu-id="b8bac-296">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-296">True</span></span>                            |
| <span data-ttu-id="b8bac-297">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b8bac-297">Is-Single-Valued</span></span>       | <span data-ttu-id="b8bac-298">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-298">True</span></span>                            |
| <span data-ttu-id="b8bac-299">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b8bac-299">Is Indexed</span></span>             | <span data-ttu-id="b8bac-300">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-300">True</span></span>                            |
| <span data-ttu-id="b8bac-301">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b8bac-301">In Global Catalog</span></span>      | <span data-ttu-id="b8bac-302">Richtig</span><span class="sxs-lookup"><span data-stu-id="b8bac-302">True</span></span>                            |
| <span data-ttu-id="b8bac-303">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8bac-303">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8bac-304">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b8bac-304">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8bac-305">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8bac-305">Range-Lower</span></span>            | <span data-ttu-id="b8bac-306">16</span><span class="sxs-lookup"><span data-stu-id="b8bac-306">16</span></span>                              |
| <span data-ttu-id="b8bac-307">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8bac-307">Range-Upper</span></span>            | <span data-ttu-id="b8bac-308">16</span><span class="sxs-lookup"><span data-stu-id="b8bac-308">16</span></span>                              |
| <span data-ttu-id="b8bac-309">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bac-309">Search-Flags</span></span>           | <span data-ttu-id="b8bac-310">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b8bac-310">0x00000009</span></span>                      |
| <span data-ttu-id="b8bac-311">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bac-311">System-Flags</span></span>           | <span data-ttu-id="b8bac-312">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8bac-312">0x00000013</span></span>                      |
| <span data-ttu-id="b8bac-313">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b8bac-313">Classes used in</span></span>        | [<span data-ttu-id="b8bac-314">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b8bac-314">**Top**</span></span>](c-top.md)<br/> |



 

 





