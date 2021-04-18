---
title: DSA-Signature-Attribut
description: Der DSA-Signature eines Objekts ist die Aufruf-ID des letzten Verzeichnisses, um das Objekt zu ändern.
ms.assetid: 7ae65f15-b0c9-4d73-8a65-92c23d0a239b
ms.tgt_platform: multiple
keywords:
- AD-Schema für DSA-Signature-Attribut
- AD-Schema des DSASignature-Attributs
topic_type:
- apiref
api_name:
- DSA-Signature
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfed9e2cb871f3418c8bdbf4401d03c1e78492b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344280"
---
# <a name="dsa-signature-attribute"></a><span data-ttu-id="96ead-105">DSA-Signature-Attribut</span><span class="sxs-lookup"><span data-stu-id="96ead-105">DSA-Signature attribute</span></span>

<span data-ttu-id="96ead-106">Der DSA-Signature eines Objekts ist die Aufruf-ID des letzten Verzeichnisses, um das Objekt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="96ead-106">The DSA-Signature of an object is the Invocation-ID of the last directory to modify the object.</span></span>



| <span data-ttu-id="96ead-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96ead-107">Entry</span></span> | <span data-ttu-id="96ead-108">Wert</span><span class="sxs-lookup"><span data-stu-id="96ead-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="96ead-109">CN</span><span class="sxs-lookup"><span data-stu-id="96ead-109">CN</span></span>                | <span data-ttu-id="96ead-110">DSA-Signature</span><span class="sxs-lookup"><span data-stu-id="96ead-110">DSA-Signature</span></span>                                         |
| <span data-ttu-id="96ead-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="96ead-111">Ldap-Display-Name</span></span> | <span data-ttu-id="96ead-112">DSASignature</span><span class="sxs-lookup"><span data-stu-id="96ead-112">dSASignature</span></span>                                          |
| <span data-ttu-id="96ead-113">Size</span><span class="sxs-lookup"><span data-stu-id="96ead-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="96ead-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="96ead-114">Update Privilege</span></span>  | <span data-ttu-id="96ead-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="96ead-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="96ead-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="96ead-116">Update Frequency</span></span>  | <span data-ttu-id="96ead-117">Jedes Mal, wenn ein Objekt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="96ead-117">Whenever an object is modified.</span></span>                       |
| <span data-ttu-id="96ead-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="96ead-118">Attribute-Id</span></span>      | <span data-ttu-id="96ead-119">1.2.840.113556.1.2.74</span><span class="sxs-lookup"><span data-stu-id="96ead-119">1.2.840.113556.1.2.74</span></span>                                 |
| <span data-ttu-id="96ead-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="96ead-120">System-Id-Guid</span></span>    | <span data-ttu-id="96ead-121">167757bc-47b3-11d1-a9c3-0000-C1</span><span class="sxs-lookup"><span data-stu-id="96ead-121">167757bc-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="96ead-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="96ead-122">Syntax</span></span>            | [<span data-ttu-id="96ead-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="96ead-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="96ead-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="96ead-124">Implementations</span></span>

-   [<span data-ttu-id="96ead-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="96ead-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="96ead-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="96ead-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="96ead-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="96ead-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="96ead-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="96ead-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="96ead-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="96ead-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="96ead-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="96ead-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="96ead-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="96ead-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="96ead-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="96ead-132">Windows 2000 Server</span></span>



| <span data-ttu-id="96ead-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96ead-133">Entry</span></span> | <span data-ttu-id="96ead-134">Wert</span><span class="sxs-lookup"><span data-stu-id="96ead-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="96ead-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96ead-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="96ead-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96ead-136">MAPI-Id</span></span>                | <span data-ttu-id="96ead-137">0x8077</span><span class="sxs-lookup"><span data-stu-id="96ead-137">0x8077</span></span>                          |
| <span data-ttu-id="96ead-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="96ead-138">System-Only</span></span>            | <span data-ttu-id="96ead-139">False</span><span class="sxs-lookup"><span data-stu-id="96ead-139">False</span></span>                           |
| <span data-ttu-id="96ead-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96ead-140">Is-Single-Valued</span></span>       | <span data-ttu-id="96ead-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="96ead-141">True</span></span>                            |
| <span data-ttu-id="96ead-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96ead-142">Is Indexed</span></span>             | <span data-ttu-id="96ead-143">False</span><span class="sxs-lookup"><span data-stu-id="96ead-143">False</span></span>                           |
| <span data-ttu-id="96ead-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96ead-144">In Global Catalog</span></span>      | <span data-ttu-id="96ead-145">False</span><span class="sxs-lookup"><span data-stu-id="96ead-145">False</span></span>                           |
| <span data-ttu-id="96ead-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96ead-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="96ead-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96ead-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="96ead-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96ead-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="96ead-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96ead-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="96ead-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96ead-150">Search-Flags</span></span>           | <span data-ttu-id="96ead-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96ead-151">0x00000000</span></span>                      |
| <span data-ttu-id="96ead-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96ead-152">System-Flags</span></span>           | <span data-ttu-id="96ead-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96ead-153">0x00000010</span></span>                      |
| <span data-ttu-id="96ead-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96ead-154">Classes used in</span></span>        | [<span data-ttu-id="96ead-155">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="96ead-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="96ead-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="96ead-156">Windows Server 2003</span></span>



| <span data-ttu-id="96ead-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96ead-157">Entry</span></span> | <span data-ttu-id="96ead-158">Wert</span><span class="sxs-lookup"><span data-stu-id="96ead-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="96ead-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96ead-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="96ead-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96ead-160">MAPI-Id</span></span>                | <span data-ttu-id="96ead-161">0x8077</span><span class="sxs-lookup"><span data-stu-id="96ead-161">0x8077</span></span>                          |
| <span data-ttu-id="96ead-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="96ead-162">System-Only</span></span>            | <span data-ttu-id="96ead-163">False</span><span class="sxs-lookup"><span data-stu-id="96ead-163">False</span></span>                           |
| <span data-ttu-id="96ead-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96ead-164">Is-Single-Valued</span></span>       | <span data-ttu-id="96ead-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="96ead-165">True</span></span>                            |
| <span data-ttu-id="96ead-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96ead-166">Is Indexed</span></span>             | <span data-ttu-id="96ead-167">False</span><span class="sxs-lookup"><span data-stu-id="96ead-167">False</span></span>                           |
| <span data-ttu-id="96ead-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96ead-168">In Global Catalog</span></span>      | <span data-ttu-id="96ead-169">False</span><span class="sxs-lookup"><span data-stu-id="96ead-169">False</span></span>                           |
| <span data-ttu-id="96ead-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96ead-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="96ead-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96ead-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="96ead-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96ead-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="96ead-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96ead-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="96ead-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96ead-174">Search-Flags</span></span>           | <span data-ttu-id="96ead-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96ead-175">0x00000000</span></span>                      |
| <span data-ttu-id="96ead-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96ead-176">System-Flags</span></span>           | <span data-ttu-id="96ead-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96ead-177">0x00000010</span></span>                      |
| <span data-ttu-id="96ead-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96ead-178">Classes used in</span></span>        | [<span data-ttu-id="96ead-179">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="96ead-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="96ead-180">Adam</span><span class="sxs-lookup"><span data-stu-id="96ead-180">ADAM</span></span>



| <span data-ttu-id="96ead-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96ead-181">Entry</span></span> | <span data-ttu-id="96ead-182">Wert</span><span class="sxs-lookup"><span data-stu-id="96ead-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="96ead-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96ead-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="96ead-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96ead-184">MAPI-Id</span></span>                | <span data-ttu-id="96ead-185">0x8077</span><span class="sxs-lookup"><span data-stu-id="96ead-185">0x8077</span></span>                          |
| <span data-ttu-id="96ead-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="96ead-186">System-Only</span></span>            | <span data-ttu-id="96ead-187">False</span><span class="sxs-lookup"><span data-stu-id="96ead-187">False</span></span>                           |
| <span data-ttu-id="96ead-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96ead-188">Is-Single-Valued</span></span>       | <span data-ttu-id="96ead-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="96ead-189">True</span></span>                            |
| <span data-ttu-id="96ead-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96ead-190">Is Indexed</span></span>             | <span data-ttu-id="96ead-191">False</span><span class="sxs-lookup"><span data-stu-id="96ead-191">False</span></span>                           |
| <span data-ttu-id="96ead-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96ead-192">In Global Catalog</span></span>      | <span data-ttu-id="96ead-193">False</span><span class="sxs-lookup"><span data-stu-id="96ead-193">False</span></span>                           |
| <span data-ttu-id="96ead-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96ead-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="96ead-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96ead-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="96ead-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96ead-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="96ead-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96ead-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="96ead-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96ead-198">Search-Flags</span></span>           | <span data-ttu-id="96ead-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96ead-199">0x00000000</span></span>                      |
| <span data-ttu-id="96ead-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96ead-200">System-Flags</span></span>           | <span data-ttu-id="96ead-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96ead-201">0x00000010</span></span>                      |
| <span data-ttu-id="96ead-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96ead-202">Classes used in</span></span>        | [<span data-ttu-id="96ead-203">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="96ead-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="96ead-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="96ead-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="96ead-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96ead-205">Entry</span></span> | <span data-ttu-id="96ead-206">Wert</span><span class="sxs-lookup"><span data-stu-id="96ead-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="96ead-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96ead-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="96ead-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96ead-208">MAPI-Id</span></span>                | <span data-ttu-id="96ead-209">0x8077</span><span class="sxs-lookup"><span data-stu-id="96ead-209">0x8077</span></span>                          |
| <span data-ttu-id="96ead-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="96ead-210">System-Only</span></span>            | <span data-ttu-id="96ead-211">False</span><span class="sxs-lookup"><span data-stu-id="96ead-211">False</span></span>                           |
| <span data-ttu-id="96ead-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96ead-212">Is-Single-Valued</span></span>       | <span data-ttu-id="96ead-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="96ead-213">True</span></span>                            |
| <span data-ttu-id="96ead-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96ead-214">Is Indexed</span></span>             | <span data-ttu-id="96ead-215">False</span><span class="sxs-lookup"><span data-stu-id="96ead-215">False</span></span>                           |
| <span data-ttu-id="96ead-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96ead-216">In Global Catalog</span></span>      | <span data-ttu-id="96ead-217">False</span><span class="sxs-lookup"><span data-stu-id="96ead-217">False</span></span>                           |
| <span data-ttu-id="96ead-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96ead-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="96ead-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96ead-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="96ead-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96ead-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="96ead-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96ead-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="96ead-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96ead-222">Search-Flags</span></span>           | <span data-ttu-id="96ead-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96ead-223">0x00000000</span></span>                      |
| <span data-ttu-id="96ead-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96ead-224">System-Flags</span></span>           | <span data-ttu-id="96ead-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96ead-225">0x00000010</span></span>                      |
| <span data-ttu-id="96ead-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96ead-226">Classes used in</span></span>        | [<span data-ttu-id="96ead-227">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="96ead-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="96ead-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96ead-228">Windows Server 2008</span></span>



| <span data-ttu-id="96ead-229">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96ead-229">Entry</span></span> | <span data-ttu-id="96ead-230">Wert</span><span class="sxs-lookup"><span data-stu-id="96ead-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="96ead-231">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96ead-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="96ead-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96ead-232">MAPI-Id</span></span>                | <span data-ttu-id="96ead-233">0x8077</span><span class="sxs-lookup"><span data-stu-id="96ead-233">0x8077</span></span>                          |
| <span data-ttu-id="96ead-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="96ead-234">System-Only</span></span>            | <span data-ttu-id="96ead-235">False</span><span class="sxs-lookup"><span data-stu-id="96ead-235">False</span></span>                           |
| <span data-ttu-id="96ead-236">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96ead-236">Is-Single-Valued</span></span>       | <span data-ttu-id="96ead-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="96ead-237">True</span></span>                            |
| <span data-ttu-id="96ead-238">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96ead-238">Is Indexed</span></span>             | <span data-ttu-id="96ead-239">False</span><span class="sxs-lookup"><span data-stu-id="96ead-239">False</span></span>                           |
| <span data-ttu-id="96ead-240">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96ead-240">In Global Catalog</span></span>      | <span data-ttu-id="96ead-241">False</span><span class="sxs-lookup"><span data-stu-id="96ead-241">False</span></span>                           |
| <span data-ttu-id="96ead-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96ead-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="96ead-243">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96ead-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="96ead-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96ead-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="96ead-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96ead-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="96ead-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96ead-246">Search-Flags</span></span>           | <span data-ttu-id="96ead-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96ead-247">0x00000000</span></span>                      |
| <span data-ttu-id="96ead-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96ead-248">System-Flags</span></span>           | <span data-ttu-id="96ead-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96ead-249">0x00000010</span></span>                      |
| <span data-ttu-id="96ead-250">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96ead-250">Classes used in</span></span>        | [<span data-ttu-id="96ead-251">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="96ead-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="96ead-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="96ead-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="96ead-253">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96ead-253">Entry</span></span> | <span data-ttu-id="96ead-254">Wert</span><span class="sxs-lookup"><span data-stu-id="96ead-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="96ead-255">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96ead-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="96ead-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96ead-256">MAPI-Id</span></span>                | <span data-ttu-id="96ead-257">0x8077</span><span class="sxs-lookup"><span data-stu-id="96ead-257">0x8077</span></span>                          |
| <span data-ttu-id="96ead-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="96ead-258">System-Only</span></span>            | <span data-ttu-id="96ead-259">False</span><span class="sxs-lookup"><span data-stu-id="96ead-259">False</span></span>                           |
| <span data-ttu-id="96ead-260">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96ead-260">Is-Single-Valued</span></span>       | <span data-ttu-id="96ead-261">Richtig</span><span class="sxs-lookup"><span data-stu-id="96ead-261">True</span></span>                            |
| <span data-ttu-id="96ead-262">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96ead-262">Is Indexed</span></span>             | <span data-ttu-id="96ead-263">False</span><span class="sxs-lookup"><span data-stu-id="96ead-263">False</span></span>                           |
| <span data-ttu-id="96ead-264">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96ead-264">In Global Catalog</span></span>      | <span data-ttu-id="96ead-265">False</span><span class="sxs-lookup"><span data-stu-id="96ead-265">False</span></span>                           |
| <span data-ttu-id="96ead-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96ead-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="96ead-267">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96ead-267">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="96ead-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96ead-268">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="96ead-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96ead-269">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="96ead-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96ead-270">Search-Flags</span></span>           | <span data-ttu-id="96ead-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96ead-271">0x00000000</span></span>                      |
| <span data-ttu-id="96ead-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96ead-272">System-Flags</span></span>           | <span data-ttu-id="96ead-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96ead-273">0x00000010</span></span>                      |
| <span data-ttu-id="96ead-274">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96ead-274">Classes used in</span></span>        | [<span data-ttu-id="96ead-275">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="96ead-275">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="96ead-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="96ead-276">Windows Server 2012</span></span>



| <span data-ttu-id="96ead-277">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96ead-277">Entry</span></span> | <span data-ttu-id="96ead-278">Wert</span><span class="sxs-lookup"><span data-stu-id="96ead-278">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="96ead-279">Link-ID</span><span class="sxs-lookup"><span data-stu-id="96ead-279">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="96ead-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96ead-280">MAPI-Id</span></span>                | <span data-ttu-id="96ead-281">0x8077</span><span class="sxs-lookup"><span data-stu-id="96ead-281">0x8077</span></span>                          |
| <span data-ttu-id="96ead-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="96ead-282">System-Only</span></span>            | <span data-ttu-id="96ead-283">False</span><span class="sxs-lookup"><span data-stu-id="96ead-283">False</span></span>                           |
| <span data-ttu-id="96ead-284">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="96ead-284">Is-Single-Valued</span></span>       | <span data-ttu-id="96ead-285">Richtig</span><span class="sxs-lookup"><span data-stu-id="96ead-285">True</span></span>                            |
| <span data-ttu-id="96ead-286">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="96ead-286">Is Indexed</span></span>             | <span data-ttu-id="96ead-287">False</span><span class="sxs-lookup"><span data-stu-id="96ead-287">False</span></span>                           |
| <span data-ttu-id="96ead-288">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="96ead-288">In Global Catalog</span></span>      | <span data-ttu-id="96ead-289">False</span><span class="sxs-lookup"><span data-stu-id="96ead-289">False</span></span>                           |
| <span data-ttu-id="96ead-290">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96ead-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="96ead-291">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="96ead-291">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="96ead-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96ead-292">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="96ead-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96ead-293">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="96ead-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96ead-294">Search-Flags</span></span>           | <span data-ttu-id="96ead-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96ead-295">0x00000000</span></span>                      |
| <span data-ttu-id="96ead-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96ead-296">System-Flags</span></span>           | <span data-ttu-id="96ead-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96ead-297">0x00000010</span></span>                      |
| <span data-ttu-id="96ead-298">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="96ead-298">Classes used in</span></span>        | [<span data-ttu-id="96ead-299">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="96ead-299">**Top**</span></span>](c-top.md)<br/> |



 

 





