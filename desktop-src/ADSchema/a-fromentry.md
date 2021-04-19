---
title: From-Entry-Attribut
description: Dies ist ein konstruiertes Attribut, das true ist, wenn das Objekt beschreibbar ist, und false, wenn es schreibgeschützt ist, z. b. eine GC-Replikat Instanz.
ms.assetid: b43e979d-15f9-4425-8a58-c9ed71bab1e4
ms.tgt_platform: multiple
keywords:
- AD-Schema für From-Entry-Attribut
- Schema des fromentry-Attributs AD
topic_type:
- apiref
api_name:
- From-Entry
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c5f5e45e2897b917ad442f1b1b5d77246fa079c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342692"
---
# <a name="from-entry-attribute"></a><span data-ttu-id="fe5f2-105">From-Entry-Attribut</span><span class="sxs-lookup"><span data-stu-id="fe5f2-105">From-Entry attribute</span></span>

<span data-ttu-id="fe5f2-106">Dies ist ein konstruiertes Attribut, das **true** ist, wenn das Objekt beschreibbar ist, und **false** , wenn es schreibgeschützt ist, z. b. eine GC-Replikat Instanz.</span><span class="sxs-lookup"><span data-stu-id="fe5f2-106">This is a constructed attribute that is **TRUE** if the object is writable and **FALSE** if it is read-only, for example, a GC replica instance.</span></span>



| <span data-ttu-id="fe5f2-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fe5f2-107">Entry</span></span> | <span data-ttu-id="fe5f2-108">Wert</span><span class="sxs-lookup"><span data-stu-id="fe5f2-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="fe5f2-109">CN</span><span class="sxs-lookup"><span data-stu-id="fe5f2-109">CN</span></span>                | <span data-ttu-id="fe5f2-110">From-Entry</span><span class="sxs-lookup"><span data-stu-id="fe5f2-110">From-Entry</span></span>                           |
| <span data-ttu-id="fe5f2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fe5f2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fe5f2-112">fromentry</span><span class="sxs-lookup"><span data-stu-id="fe5f2-112">fromEntry</span></span>                            |
| <span data-ttu-id="fe5f2-113">Size</span><span class="sxs-lookup"><span data-stu-id="fe5f2-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="fe5f2-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="fe5f2-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="fe5f2-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="fe5f2-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="fe5f2-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fe5f2-116">Attribute-Id</span></span>      | <span data-ttu-id="fe5f2-117">1.2.840.113556.1.4.910</span><span class="sxs-lookup"><span data-stu-id="fe5f2-117">1.2.840.113556.1.4.910</span></span>               |
| <span data-ttu-id="fe5f2-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fe5f2-118">System-Id-Guid</span></span>    | <span data-ttu-id="fe5f2-119">9a7ad949-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="fe5f2-119">9a7ad949-ca53-11d1-bbd0-0080c76670c0</span></span> |
| <span data-ttu-id="fe5f2-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe5f2-120">Syntax</span></span>            | [<span data-ttu-id="fe5f2-121">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="fe5f2-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="fe5f2-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="fe5f2-122">Implementations</span></span>

-   [<span data-ttu-id="fe5f2-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fe5f2-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fe5f2-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fe5f2-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fe5f2-125">**Adam**</span><span class="sxs-lookup"><span data-stu-id="fe5f2-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="fe5f2-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fe5f2-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fe5f2-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fe5f2-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fe5f2-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fe5f2-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fe5f2-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fe5f2-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fe5f2-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fe5f2-130">Windows 2000 Server</span></span>



| <span data-ttu-id="fe5f2-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fe5f2-131">Entry</span></span> | <span data-ttu-id="fe5f2-132">Wert</span><span class="sxs-lookup"><span data-stu-id="fe5f2-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fe5f2-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fe5f2-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fe5f2-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe5f2-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fe5f2-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe5f2-135">System-Only</span></span>            | <span data-ttu-id="fe5f2-136">Richtig</span><span class="sxs-lookup"><span data-stu-id="fe5f2-136">True</span></span>                            |
| <span data-ttu-id="fe5f2-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fe5f2-137">Is-Single-Valued</span></span>       | <span data-ttu-id="fe5f2-138">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-138">False</span></span>                           |
| <span data-ttu-id="fe5f2-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fe5f2-139">Is Indexed</span></span>             | <span data-ttu-id="fe5f2-140">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-140">False</span></span>                           |
| <span data-ttu-id="fe5f2-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fe5f2-141">In Global Catalog</span></span>      | <span data-ttu-id="fe5f2-142">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-142">False</span></span>                           |
| <span data-ttu-id="fe5f2-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fe5f2-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe5f2-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fe5f2-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fe5f2-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe5f2-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fe5f2-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe5f2-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fe5f2-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe5f2-147">Search-Flags</span></span>           | <span data-ttu-id="fe5f2-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe5f2-148">0x00000000</span></span>                      |
| <span data-ttu-id="fe5f2-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe5f2-149">System-Flags</span></span>           | <span data-ttu-id="fe5f2-150">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fe5f2-150">0x08000014</span></span>                      |
| <span data-ttu-id="fe5f2-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fe5f2-151">Classes used in</span></span>        | [<span data-ttu-id="fe5f2-152">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="fe5f2-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fe5f2-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe5f2-153">Windows Server 2003</span></span>



| <span data-ttu-id="fe5f2-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fe5f2-154">Entry</span></span> | <span data-ttu-id="fe5f2-155">Wert</span><span class="sxs-lookup"><span data-stu-id="fe5f2-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fe5f2-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fe5f2-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fe5f2-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe5f2-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fe5f2-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe5f2-158">System-Only</span></span>            | <span data-ttu-id="fe5f2-159">Richtig</span><span class="sxs-lookup"><span data-stu-id="fe5f2-159">True</span></span>                            |
| <span data-ttu-id="fe5f2-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fe5f2-160">Is-Single-Valued</span></span>       | <span data-ttu-id="fe5f2-161">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-161">False</span></span>                           |
| <span data-ttu-id="fe5f2-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fe5f2-162">Is Indexed</span></span>             | <span data-ttu-id="fe5f2-163">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-163">False</span></span>                           |
| <span data-ttu-id="fe5f2-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fe5f2-164">In Global Catalog</span></span>      | <span data-ttu-id="fe5f2-165">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-165">False</span></span>                           |
| <span data-ttu-id="fe5f2-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fe5f2-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe5f2-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fe5f2-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fe5f2-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe5f2-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fe5f2-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe5f2-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fe5f2-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe5f2-170">Search-Flags</span></span>           | <span data-ttu-id="fe5f2-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe5f2-171">0x00000000</span></span>                      |
| <span data-ttu-id="fe5f2-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe5f2-172">System-Flags</span></span>           | <span data-ttu-id="fe5f2-173">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fe5f2-173">0x08000014</span></span>                      |
| <span data-ttu-id="fe5f2-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fe5f2-174">Classes used in</span></span>        | [<span data-ttu-id="fe5f2-175">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="fe5f2-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="fe5f2-176">Adam</span><span class="sxs-lookup"><span data-stu-id="fe5f2-176">ADAM</span></span>



| <span data-ttu-id="fe5f2-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fe5f2-177">Entry</span></span> | <span data-ttu-id="fe5f2-178">Wert</span><span class="sxs-lookup"><span data-stu-id="fe5f2-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fe5f2-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fe5f2-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fe5f2-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe5f2-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fe5f2-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe5f2-181">System-Only</span></span>            | <span data-ttu-id="fe5f2-182">Richtig</span><span class="sxs-lookup"><span data-stu-id="fe5f2-182">True</span></span>                            |
| <span data-ttu-id="fe5f2-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fe5f2-183">Is-Single-Valued</span></span>       | <span data-ttu-id="fe5f2-184">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-184">False</span></span>                           |
| <span data-ttu-id="fe5f2-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fe5f2-185">Is Indexed</span></span>             | <span data-ttu-id="fe5f2-186">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-186">False</span></span>                           |
| <span data-ttu-id="fe5f2-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fe5f2-187">In Global Catalog</span></span>      | <span data-ttu-id="fe5f2-188">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-188">False</span></span>                           |
| <span data-ttu-id="fe5f2-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fe5f2-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe5f2-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fe5f2-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fe5f2-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe5f2-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fe5f2-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe5f2-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fe5f2-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe5f2-193">Search-Flags</span></span>           | <span data-ttu-id="fe5f2-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe5f2-194">0x00000000</span></span>                      |
| <span data-ttu-id="fe5f2-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe5f2-195">System-Flags</span></span>           | <span data-ttu-id="fe5f2-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fe5f2-196">0x08000014</span></span>                      |
| <span data-ttu-id="fe5f2-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fe5f2-197">Classes used in</span></span>        | [<span data-ttu-id="fe5f2-198">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="fe5f2-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fe5f2-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fe5f2-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fe5f2-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fe5f2-200">Entry</span></span> | <span data-ttu-id="fe5f2-201">Wert</span><span class="sxs-lookup"><span data-stu-id="fe5f2-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fe5f2-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fe5f2-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fe5f2-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe5f2-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fe5f2-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe5f2-204">System-Only</span></span>            | <span data-ttu-id="fe5f2-205">Richtig</span><span class="sxs-lookup"><span data-stu-id="fe5f2-205">True</span></span>                            |
| <span data-ttu-id="fe5f2-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fe5f2-206">Is-Single-Valued</span></span>       | <span data-ttu-id="fe5f2-207">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-207">False</span></span>                           |
| <span data-ttu-id="fe5f2-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fe5f2-208">Is Indexed</span></span>             | <span data-ttu-id="fe5f2-209">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-209">False</span></span>                           |
| <span data-ttu-id="fe5f2-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fe5f2-210">In Global Catalog</span></span>      | <span data-ttu-id="fe5f2-211">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-211">False</span></span>                           |
| <span data-ttu-id="fe5f2-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fe5f2-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe5f2-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fe5f2-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fe5f2-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe5f2-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fe5f2-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe5f2-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fe5f2-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe5f2-216">Search-Flags</span></span>           | <span data-ttu-id="fe5f2-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe5f2-217">0x00000000</span></span>                      |
| <span data-ttu-id="fe5f2-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe5f2-218">System-Flags</span></span>           | <span data-ttu-id="fe5f2-219">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fe5f2-219">0x08000014</span></span>                      |
| <span data-ttu-id="fe5f2-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fe5f2-220">Classes used in</span></span>        | [<span data-ttu-id="fe5f2-221">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="fe5f2-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fe5f2-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe5f2-222">Windows Server 2008</span></span>



| <span data-ttu-id="fe5f2-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fe5f2-223">Entry</span></span> | <span data-ttu-id="fe5f2-224">Wert</span><span class="sxs-lookup"><span data-stu-id="fe5f2-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fe5f2-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fe5f2-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fe5f2-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe5f2-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fe5f2-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe5f2-227">System-Only</span></span>            | <span data-ttu-id="fe5f2-228">Richtig</span><span class="sxs-lookup"><span data-stu-id="fe5f2-228">True</span></span>                            |
| <span data-ttu-id="fe5f2-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fe5f2-229">Is-Single-Valued</span></span>       | <span data-ttu-id="fe5f2-230">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-230">False</span></span>                           |
| <span data-ttu-id="fe5f2-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fe5f2-231">Is Indexed</span></span>             | <span data-ttu-id="fe5f2-232">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-232">False</span></span>                           |
| <span data-ttu-id="fe5f2-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fe5f2-233">In Global Catalog</span></span>      | <span data-ttu-id="fe5f2-234">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-234">False</span></span>                           |
| <span data-ttu-id="fe5f2-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fe5f2-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe5f2-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fe5f2-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fe5f2-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe5f2-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fe5f2-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe5f2-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fe5f2-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe5f2-239">Search-Flags</span></span>           | <span data-ttu-id="fe5f2-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe5f2-240">0x00000000</span></span>                      |
| <span data-ttu-id="fe5f2-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe5f2-241">System-Flags</span></span>           | <span data-ttu-id="fe5f2-242">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fe5f2-242">0x08000014</span></span>                      |
| <span data-ttu-id="fe5f2-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fe5f2-243">Classes used in</span></span>        | [<span data-ttu-id="fe5f2-244">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="fe5f2-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fe5f2-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fe5f2-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fe5f2-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fe5f2-246">Entry</span></span> | <span data-ttu-id="fe5f2-247">Wert</span><span class="sxs-lookup"><span data-stu-id="fe5f2-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fe5f2-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fe5f2-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fe5f2-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe5f2-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fe5f2-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe5f2-250">System-Only</span></span>            | <span data-ttu-id="fe5f2-251">Richtig</span><span class="sxs-lookup"><span data-stu-id="fe5f2-251">True</span></span>                            |
| <span data-ttu-id="fe5f2-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fe5f2-252">Is-Single-Valued</span></span>       | <span data-ttu-id="fe5f2-253">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-253">False</span></span>                           |
| <span data-ttu-id="fe5f2-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fe5f2-254">Is Indexed</span></span>             | <span data-ttu-id="fe5f2-255">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-255">False</span></span>                           |
| <span data-ttu-id="fe5f2-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fe5f2-256">In Global Catalog</span></span>      | <span data-ttu-id="fe5f2-257">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-257">False</span></span>                           |
| <span data-ttu-id="fe5f2-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fe5f2-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe5f2-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fe5f2-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fe5f2-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe5f2-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fe5f2-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe5f2-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fe5f2-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe5f2-262">Search-Flags</span></span>           | <span data-ttu-id="fe5f2-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe5f2-263">0x00000000</span></span>                      |
| <span data-ttu-id="fe5f2-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe5f2-264">System-Flags</span></span>           | <span data-ttu-id="fe5f2-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fe5f2-265">0x08000014</span></span>                      |
| <span data-ttu-id="fe5f2-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fe5f2-266">Classes used in</span></span>        | [<span data-ttu-id="fe5f2-267">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="fe5f2-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fe5f2-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fe5f2-268">Windows Server 2012</span></span>



| <span data-ttu-id="fe5f2-269">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fe5f2-269">Entry</span></span> | <span data-ttu-id="fe5f2-270">Wert</span><span class="sxs-lookup"><span data-stu-id="fe5f2-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fe5f2-271">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fe5f2-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fe5f2-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe5f2-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fe5f2-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe5f2-273">System-Only</span></span>            | <span data-ttu-id="fe5f2-274">Richtig</span><span class="sxs-lookup"><span data-stu-id="fe5f2-274">True</span></span>                            |
| <span data-ttu-id="fe5f2-275">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fe5f2-275">Is-Single-Valued</span></span>       | <span data-ttu-id="fe5f2-276">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-276">False</span></span>                           |
| <span data-ttu-id="fe5f2-277">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fe5f2-277">Is Indexed</span></span>             | <span data-ttu-id="fe5f2-278">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-278">False</span></span>                           |
| <span data-ttu-id="fe5f2-279">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fe5f2-279">In Global Catalog</span></span>      | <span data-ttu-id="fe5f2-280">False</span><span class="sxs-lookup"><span data-stu-id="fe5f2-280">False</span></span>                           |
| <span data-ttu-id="fe5f2-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fe5f2-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe5f2-282">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fe5f2-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fe5f2-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe5f2-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fe5f2-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe5f2-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fe5f2-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe5f2-285">Search-Flags</span></span>           | <span data-ttu-id="fe5f2-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe5f2-286">0x00000000</span></span>                      |
| <span data-ttu-id="fe5f2-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe5f2-287">System-Flags</span></span>           | <span data-ttu-id="fe5f2-288">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fe5f2-288">0x08000014</span></span>                      |
| <span data-ttu-id="fe5f2-289">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fe5f2-289">Classes used in</span></span>        | [<span data-ttu-id="fe5f2-290">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="fe5f2-290">**Top**</span></span>](c-top.md)<br/> |



 

 





