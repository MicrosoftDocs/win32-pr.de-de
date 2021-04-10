---
title: Object-Class-Attribut
description: Die Liste der Klassen, von denen diese Klasse abgeleitet ist.
ms.assetid: def98723-2d8a-49ea-84f8-afe6ff9cdfd9
ms.tgt_platform: multiple
keywords:
- AD-Schema für Object-Class-Attribut
- AD-Schema für objectClass-Attribut
topic_type:
- apiref
api_name:
- Object-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851d48bcbcc40640af3ee555c343feaab05edf6b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122749"
---
# <a name="object-class-attribute"></a><span data-ttu-id="a1a08-105">Object-Class-Attribut</span><span class="sxs-lookup"><span data-stu-id="a1a08-105">Object-Class attribute</span></span>

<span data-ttu-id="a1a08-106">Die Liste der Klassen, von denen diese Klasse abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="a1a08-106">The list of classes from which this class is derived.</span></span>



| <span data-ttu-id="a1a08-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a1a08-107">Entry</span></span> | <span data-ttu-id="a1a08-108">Wert</span><span class="sxs-lookup"><span data-stu-id="a1a08-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="a1a08-109">CN</span><span class="sxs-lookup"><span data-stu-id="a1a08-109">CN</span></span>                | <span data-ttu-id="a1a08-110">Object-Class</span><span class="sxs-lookup"><span data-stu-id="a1a08-110">Object-Class</span></span>                                                    |
| <span data-ttu-id="a1a08-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a1a08-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a1a08-112">objectClass</span><span class="sxs-lookup"><span data-stu-id="a1a08-112">objectClass</span></span>                                                     |
| <span data-ttu-id="a1a08-113">Size</span><span class="sxs-lookup"><span data-stu-id="a1a08-113">Size</span></span>              | <span data-ttu-id="a1a08-114">Im Durchschnitt ungefähr 20 Bytes.</span><span class="sxs-lookup"><span data-stu-id="a1a08-114">About 20 bytes on average.</span></span>                                      |
| <span data-ttu-id="a1a08-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a1a08-115">Update Privilege</span></span>  | <span data-ttu-id="a1a08-116">Dieser Wert wird vom Designer des-Objekts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a1a08-116">The designer of the object would set this value.</span></span>                |
| <span data-ttu-id="a1a08-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="a1a08-117">Update Frequency</span></span>  | <span data-ttu-id="a1a08-118">Dieser Wert sollte sich nie ändern.</span><span class="sxs-lookup"><span data-stu-id="a1a08-118">This value should never change.</span></span>                                 |
| <span data-ttu-id="a1a08-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a1a08-119">Attribute-Id</span></span>      | <span data-ttu-id="a1a08-120">2.5.4.0</span><span class="sxs-lookup"><span data-stu-id="a1a08-120">2.5.4.0</span></span>                                                         |
| <span data-ttu-id="a1a08-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a1a08-121">System-Id-Guid</span></span>    | <span data-ttu-id="a1a08-122">bf9679e5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a1a08-122">bf9679e5-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="a1a08-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1a08-123">Syntax</span></span>            | [<span data-ttu-id="a1a08-124">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="a1a08-124">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="a1a08-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="a1a08-125">Implementations</span></span>

-   [<span data-ttu-id="a1a08-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a1a08-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a1a08-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a1a08-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a1a08-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="a1a08-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a1a08-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a1a08-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a1a08-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a1a08-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a1a08-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a1a08-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a1a08-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a1a08-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a1a08-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a1a08-133">Windows 2000 Server</span></span>



| <span data-ttu-id="a1a08-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a1a08-134">Entry</span></span> | <span data-ttu-id="a1a08-135">Wert</span><span class="sxs-lookup"><span data-stu-id="a1a08-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a1a08-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a1a08-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a1a08-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1a08-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a1a08-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1a08-138">System-Only</span></span>            | <span data-ttu-id="a1a08-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="a1a08-139">True</span></span>                            |
| <span data-ttu-id="a1a08-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a1a08-140">Is-Single-Valued</span></span>       | <span data-ttu-id="a1a08-141">False</span><span class="sxs-lookup"><span data-stu-id="a1a08-141">False</span></span>                           |
| <span data-ttu-id="a1a08-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a1a08-142">Is Indexed</span></span>             | <span data-ttu-id="a1a08-143">False</span><span class="sxs-lookup"><span data-stu-id="a1a08-143">False</span></span>                           |
| <span data-ttu-id="a1a08-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a1a08-144">In Global Catalog</span></span>      | <span data-ttu-id="a1a08-145">Richtig</span><span class="sxs-lookup"><span data-stu-id="a1a08-145">True</span></span>                            |
| <span data-ttu-id="a1a08-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1a08-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1a08-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a1a08-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a1a08-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1a08-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a1a08-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1a08-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a1a08-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a08-150">Search-Flags</span></span>           | <span data-ttu-id="a1a08-151">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a1a08-151">0x00000008</span></span>                      |
| <span data-ttu-id="a1a08-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a08-152">System-Flags</span></span>           | <span data-ttu-id="a1a08-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a1a08-153">0x00000012</span></span>                      |
| <span data-ttu-id="a1a08-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a1a08-154">Classes used in</span></span>        | [<span data-ttu-id="a1a08-155">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a1a08-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a1a08-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a1a08-156">Windows Server 2003</span></span>



| <span data-ttu-id="a1a08-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a1a08-157">Entry</span></span> | <span data-ttu-id="a1a08-158">Wert</span><span class="sxs-lookup"><span data-stu-id="a1a08-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a1a08-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a1a08-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a1a08-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1a08-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a1a08-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1a08-161">System-Only</span></span>            | <span data-ttu-id="a1a08-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="a1a08-162">True</span></span>                            |
| <span data-ttu-id="a1a08-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a1a08-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a1a08-164">False</span><span class="sxs-lookup"><span data-stu-id="a1a08-164">False</span></span>                           |
| <span data-ttu-id="a1a08-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a1a08-165">Is Indexed</span></span>             | <span data-ttu-id="a1a08-166">False</span><span class="sxs-lookup"><span data-stu-id="a1a08-166">False</span></span>                           |
| <span data-ttu-id="a1a08-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a1a08-167">In Global Catalog</span></span>      | <span data-ttu-id="a1a08-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="a1a08-168">True</span></span>                            |
| <span data-ttu-id="a1a08-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1a08-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1a08-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a1a08-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a1a08-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1a08-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a1a08-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1a08-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a1a08-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a08-173">Search-Flags</span></span>           | <span data-ttu-id="a1a08-174">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a1a08-174">0x00000008</span></span>                      |
| <span data-ttu-id="a1a08-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a08-175">System-Flags</span></span>           | <span data-ttu-id="a1a08-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a1a08-176">0x00000012</span></span>                      |
| <span data-ttu-id="a1a08-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a1a08-177">Classes used in</span></span>        | [<span data-ttu-id="a1a08-178">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a1a08-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a1a08-179">Adam</span><span class="sxs-lookup"><span data-stu-id="a1a08-179">ADAM</span></span>



| <span data-ttu-id="a1a08-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a1a08-180">Entry</span></span> | <span data-ttu-id="a1a08-181">Wert</span><span class="sxs-lookup"><span data-stu-id="a1a08-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a1a08-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a1a08-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a1a08-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1a08-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a1a08-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1a08-184">System-Only</span></span>            | <span data-ttu-id="a1a08-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="a1a08-185">True</span></span>                            |
| <span data-ttu-id="a1a08-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a1a08-186">Is-Single-Valued</span></span>       | <span data-ttu-id="a1a08-187">False</span><span class="sxs-lookup"><span data-stu-id="a1a08-187">False</span></span>                           |
| <span data-ttu-id="a1a08-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a1a08-188">Is Indexed</span></span>             | <span data-ttu-id="a1a08-189">False</span><span class="sxs-lookup"><span data-stu-id="a1a08-189">False</span></span>                           |
| <span data-ttu-id="a1a08-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a1a08-190">In Global Catalog</span></span>      | <span data-ttu-id="a1a08-191">Richtig</span><span class="sxs-lookup"><span data-stu-id="a1a08-191">True</span></span>                            |
| <span data-ttu-id="a1a08-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1a08-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1a08-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a1a08-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a1a08-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1a08-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a1a08-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1a08-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a1a08-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a08-196">Search-Flags</span></span>           | <span data-ttu-id="a1a08-197">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a1a08-197">0x00000008</span></span>                      |
| <span data-ttu-id="a1a08-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a08-198">System-Flags</span></span>           | <span data-ttu-id="a1a08-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a1a08-199">0x00000012</span></span>                      |
| <span data-ttu-id="a1a08-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a1a08-200">Classes used in</span></span>        | [<span data-ttu-id="a1a08-201">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a1a08-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a1a08-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a1a08-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a1a08-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a1a08-203">Entry</span></span> | <span data-ttu-id="a1a08-204">Wert</span><span class="sxs-lookup"><span data-stu-id="a1a08-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a1a08-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a1a08-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a1a08-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1a08-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a1a08-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1a08-207">System-Only</span></span>            | <span data-ttu-id="a1a08-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="a1a08-208">True</span></span>                            |
| <span data-ttu-id="a1a08-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a1a08-209">Is-Single-Valued</span></span>       | <span data-ttu-id="a1a08-210">False</span><span class="sxs-lookup"><span data-stu-id="a1a08-210">False</span></span>                           |
| <span data-ttu-id="a1a08-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a1a08-211">Is Indexed</span></span>             | <span data-ttu-id="a1a08-212">False</span><span class="sxs-lookup"><span data-stu-id="a1a08-212">False</span></span>                           |
| <span data-ttu-id="a1a08-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a1a08-213">In Global Catalog</span></span>      | <span data-ttu-id="a1a08-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="a1a08-214">True</span></span>                            |
| <span data-ttu-id="a1a08-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1a08-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1a08-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a1a08-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a1a08-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1a08-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a1a08-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1a08-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a1a08-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a08-219">Search-Flags</span></span>           | <span data-ttu-id="a1a08-220">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a1a08-220">0x00000008</span></span>                      |
| <span data-ttu-id="a1a08-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a08-221">System-Flags</span></span>           | <span data-ttu-id="a1a08-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a1a08-222">0x00000012</span></span>                      |
| <span data-ttu-id="a1a08-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a1a08-223">Classes used in</span></span>        | [<span data-ttu-id="a1a08-224">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a1a08-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a1a08-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1a08-225">Windows Server 2008</span></span>



| <span data-ttu-id="a1a08-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a1a08-226">Entry</span></span> | <span data-ttu-id="a1a08-227">Wert</span><span class="sxs-lookup"><span data-stu-id="a1a08-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a1a08-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a1a08-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a1a08-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1a08-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a1a08-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1a08-230">System-Only</span></span>            | <span data-ttu-id="a1a08-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="a1a08-231">True</span></span>                            |
| <span data-ttu-id="a1a08-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a1a08-232">Is-Single-Valued</span></span>       | <span data-ttu-id="a1a08-233">False</span><span class="sxs-lookup"><span data-stu-id="a1a08-233">False</span></span>                           |
| <span data-ttu-id="a1a08-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a1a08-234">Is Indexed</span></span>             | <span data-ttu-id="a1a08-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="a1a08-235">True</span></span>                            |
| <span data-ttu-id="a1a08-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a1a08-236">In Global Catalog</span></span>      | <span data-ttu-id="a1a08-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="a1a08-237">True</span></span>                            |
| <span data-ttu-id="a1a08-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1a08-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1a08-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a1a08-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a1a08-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1a08-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a1a08-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1a08-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a1a08-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a08-242">Search-Flags</span></span>           | <span data-ttu-id="a1a08-243">0x00000009</span><span class="sxs-lookup"><span data-stu-id="a1a08-243">0x00000009</span></span>                      |
| <span data-ttu-id="a1a08-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a08-244">System-Flags</span></span>           | <span data-ttu-id="a1a08-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a1a08-245">0x00000012</span></span>                      |
| <span data-ttu-id="a1a08-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a1a08-246">Classes used in</span></span>        | [<span data-ttu-id="a1a08-247">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a1a08-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a1a08-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a1a08-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a1a08-249">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a1a08-249">Entry</span></span> | <span data-ttu-id="a1a08-250">Wert</span><span class="sxs-lookup"><span data-stu-id="a1a08-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a1a08-251">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a1a08-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a1a08-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1a08-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a1a08-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1a08-253">System-Only</span></span>            | <span data-ttu-id="a1a08-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="a1a08-254">True</span></span>                            |
| <span data-ttu-id="a1a08-255">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a1a08-255">Is-Single-Valued</span></span>       | <span data-ttu-id="a1a08-256">False</span><span class="sxs-lookup"><span data-stu-id="a1a08-256">False</span></span>                           |
| <span data-ttu-id="a1a08-257">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a1a08-257">Is Indexed</span></span>             | <span data-ttu-id="a1a08-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="a1a08-258">True</span></span>                            |
| <span data-ttu-id="a1a08-259">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a1a08-259">In Global Catalog</span></span>      | <span data-ttu-id="a1a08-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="a1a08-260">True</span></span>                            |
| <span data-ttu-id="a1a08-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1a08-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1a08-262">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a1a08-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a1a08-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1a08-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a1a08-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1a08-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a1a08-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a08-265">Search-Flags</span></span>           | <span data-ttu-id="a1a08-266">0x00000009</span><span class="sxs-lookup"><span data-stu-id="a1a08-266">0x00000009</span></span>                      |
| <span data-ttu-id="a1a08-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a08-267">System-Flags</span></span>           | <span data-ttu-id="a1a08-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a1a08-268">0x00000012</span></span>                      |
| <span data-ttu-id="a1a08-269">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a1a08-269">Classes used in</span></span>        | [<span data-ttu-id="a1a08-270">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a1a08-270">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a1a08-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a1a08-271">Windows Server 2012</span></span>



| <span data-ttu-id="a1a08-272">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a1a08-272">Entry</span></span> | <span data-ttu-id="a1a08-273">Wert</span><span class="sxs-lookup"><span data-stu-id="a1a08-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a1a08-274">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a1a08-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a1a08-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1a08-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a1a08-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1a08-276">System-Only</span></span>            | <span data-ttu-id="a1a08-277">Richtig</span><span class="sxs-lookup"><span data-stu-id="a1a08-277">True</span></span>                            |
| <span data-ttu-id="a1a08-278">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a1a08-278">Is-Single-Valued</span></span>       | <span data-ttu-id="a1a08-279">False</span><span class="sxs-lookup"><span data-stu-id="a1a08-279">False</span></span>                           |
| <span data-ttu-id="a1a08-280">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a1a08-280">Is Indexed</span></span>             | <span data-ttu-id="a1a08-281">Richtig</span><span class="sxs-lookup"><span data-stu-id="a1a08-281">True</span></span>                            |
| <span data-ttu-id="a1a08-282">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a1a08-282">In Global Catalog</span></span>      | <span data-ttu-id="a1a08-283">Richtig</span><span class="sxs-lookup"><span data-stu-id="a1a08-283">True</span></span>                            |
| <span data-ttu-id="a1a08-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1a08-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1a08-285">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a1a08-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a1a08-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1a08-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a1a08-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1a08-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a1a08-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a08-288">Search-Flags</span></span>           | <span data-ttu-id="a1a08-289">0x00000009</span><span class="sxs-lookup"><span data-stu-id="a1a08-289">0x00000009</span></span>                      |
| <span data-ttu-id="a1a08-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1a08-290">System-Flags</span></span>           | <span data-ttu-id="a1a08-291">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a1a08-291">0x00000012</span></span>                      |
| <span data-ttu-id="a1a08-292">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a1a08-292">Classes used in</span></span>        | [<span data-ttu-id="a1a08-293">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a1a08-293">**Top**</span></span>](c-top.md)<br/> |



 

 





