---
title: Is-Deleted-Attribut
description: Wenn true, wurde dieses Objekt zum Löschen markiert und kann nicht instanziiert werden. Nachdem der Tombstone-Zeitraum abgelaufen ist, wird er aus dem System entfernt.
ms.assetid: 549b5161-5d2f-47d7-8192-4480334ef13d
ms.tgt_platform: multiple
keywords:
- AD-Schema für Is-Deleted-Attribut
- AD-Schema für isDeleted-Attribut
topic_type:
- apiref
api_name:
- Is-Deleted
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b30dec5ed139da60853324b82cc6e0f55fcc70
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342679"
---
# <a name="is-deleted-attribute"></a><span data-ttu-id="94b2d-106">Is-Deleted-Attribut</span><span class="sxs-lookup"><span data-stu-id="94b2d-106">Is-Deleted attribute</span></span>

<span data-ttu-id="94b2d-107">Wenn **true**, wurde dieses Objekt zum Löschen markiert und kann nicht instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="94b2d-107">If **TRUE**, this object has been marked for deletion and cannot be instantiated.</span></span> <span data-ttu-id="94b2d-108">Nachdem der Tombstone-Zeitraum abgelaufen ist, wird er aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="94b2d-108">After the tombstone period has expired, it will be removed from the system.</span></span>



| <span data-ttu-id="94b2d-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="94b2d-109">Entry</span></span> | <span data-ttu-id="94b2d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="94b2d-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="94b2d-111">CN</span><span class="sxs-lookup"><span data-stu-id="94b2d-111">CN</span></span>                | <span data-ttu-id="94b2d-112">Is-Deleted</span><span class="sxs-lookup"><span data-stu-id="94b2d-112">Is-Deleted</span></span>                           |
| <span data-ttu-id="94b2d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="94b2d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="94b2d-114">isDeleted</span><span class="sxs-lookup"><span data-stu-id="94b2d-114">isDeleted</span></span>                            |
| <span data-ttu-id="94b2d-115">Size</span><span class="sxs-lookup"><span data-stu-id="94b2d-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="94b2d-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="94b2d-116">Update Privilege</span></span>  | <span data-ttu-id="94b2d-117">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="94b2d-117">Domain administrator</span></span>                 |
| <span data-ttu-id="94b2d-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="94b2d-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="94b2d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="94b2d-119">Attribute-Id</span></span>      | <span data-ttu-id="94b2d-120">1.2.840.113556.1.2.48</span><span class="sxs-lookup"><span data-stu-id="94b2d-120">1.2.840.113556.1.2.48</span></span>                |
| <span data-ttu-id="94b2d-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="94b2d-121">System-Id-Guid</span></span>    | <span data-ttu-id="94b2d-122">bf96798f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="94b2d-122">bf96798f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="94b2d-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="94b2d-123">Syntax</span></span>            | [<span data-ttu-id="94b2d-124">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="94b2d-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="94b2d-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="94b2d-125">Implementations</span></span>

-   [<span data-ttu-id="94b2d-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="94b2d-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="94b2d-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="94b2d-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="94b2d-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="94b2d-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="94b2d-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="94b2d-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="94b2d-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="94b2d-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="94b2d-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="94b2d-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="94b2d-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="94b2d-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="94b2d-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="94b2d-133">Windows 2000 Server</span></span>



| <span data-ttu-id="94b2d-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="94b2d-134">Entry</span></span> | <span data-ttu-id="94b2d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="94b2d-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="94b2d-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="94b2d-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="94b2d-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="94b2d-137">MAPI-Id</span></span>                | <span data-ttu-id="94b2d-138">0x80c0</span><span class="sxs-lookup"><span data-stu-id="94b2d-138">0x80C0</span></span>                          |
| <span data-ttu-id="94b2d-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="94b2d-139">System-Only</span></span>            | <span data-ttu-id="94b2d-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-140">True</span></span>                            |
| <span data-ttu-id="94b2d-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="94b2d-141">Is-Single-Valued</span></span>       | <span data-ttu-id="94b2d-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-142">True</span></span>                            |
| <span data-ttu-id="94b2d-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="94b2d-143">Is Indexed</span></span>             | <span data-ttu-id="94b2d-144">False</span><span class="sxs-lookup"><span data-stu-id="94b2d-144">False</span></span>                           |
| <span data-ttu-id="94b2d-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="94b2d-145">In Global Catalog</span></span>      | <span data-ttu-id="94b2d-146">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-146">True</span></span>                            |
| <span data-ttu-id="94b2d-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="94b2d-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="94b2d-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="94b2d-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="94b2d-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="94b2d-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="94b2d-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="94b2d-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="94b2d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="94b2d-151">Search-Flags</span></span>           | <span data-ttu-id="94b2d-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="94b2d-152">0x00000000</span></span>                      |
| <span data-ttu-id="94b2d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="94b2d-153">System-Flags</span></span>           | <span data-ttu-id="94b2d-154">0x00000012</span><span class="sxs-lookup"><span data-stu-id="94b2d-154">0x00000012</span></span>                      |
| <span data-ttu-id="94b2d-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="94b2d-155">Classes used in</span></span>        | [<span data-ttu-id="94b2d-156">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="94b2d-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="94b2d-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="94b2d-157">Windows Server 2003</span></span>



| <span data-ttu-id="94b2d-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="94b2d-158">Entry</span></span> | <span data-ttu-id="94b2d-159">Wert</span><span class="sxs-lookup"><span data-stu-id="94b2d-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="94b2d-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="94b2d-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="94b2d-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="94b2d-161">MAPI-Id</span></span>                | <span data-ttu-id="94b2d-162">0x80c0</span><span class="sxs-lookup"><span data-stu-id="94b2d-162">0x80C0</span></span>                          |
| <span data-ttu-id="94b2d-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="94b2d-163">System-Only</span></span>            | <span data-ttu-id="94b2d-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-164">True</span></span>                            |
| <span data-ttu-id="94b2d-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="94b2d-165">Is-Single-Valued</span></span>       | <span data-ttu-id="94b2d-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-166">True</span></span>                            |
| <span data-ttu-id="94b2d-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="94b2d-167">Is Indexed</span></span>             | <span data-ttu-id="94b2d-168">False</span><span class="sxs-lookup"><span data-stu-id="94b2d-168">False</span></span>                           |
| <span data-ttu-id="94b2d-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="94b2d-169">In Global Catalog</span></span>      | <span data-ttu-id="94b2d-170">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-170">True</span></span>                            |
| <span data-ttu-id="94b2d-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="94b2d-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="94b2d-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="94b2d-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="94b2d-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="94b2d-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="94b2d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="94b2d-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="94b2d-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="94b2d-175">Search-Flags</span></span>           | <span data-ttu-id="94b2d-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="94b2d-176">0x00000000</span></span>                      |
| <span data-ttu-id="94b2d-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="94b2d-177">System-Flags</span></span>           | <span data-ttu-id="94b2d-178">0x00000012</span><span class="sxs-lookup"><span data-stu-id="94b2d-178">0x00000012</span></span>                      |
| <span data-ttu-id="94b2d-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="94b2d-179">Classes used in</span></span>        | [<span data-ttu-id="94b2d-180">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="94b2d-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="94b2d-181">Adam</span><span class="sxs-lookup"><span data-stu-id="94b2d-181">ADAM</span></span>



| <span data-ttu-id="94b2d-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="94b2d-182">Entry</span></span> | <span data-ttu-id="94b2d-183">Wert</span><span class="sxs-lookup"><span data-stu-id="94b2d-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="94b2d-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="94b2d-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="94b2d-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="94b2d-185">MAPI-Id</span></span>                | <span data-ttu-id="94b2d-186">0x80c0</span><span class="sxs-lookup"><span data-stu-id="94b2d-186">0x80C0</span></span>                          |
| <span data-ttu-id="94b2d-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="94b2d-187">System-Only</span></span>            | <span data-ttu-id="94b2d-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-188">True</span></span>                            |
| <span data-ttu-id="94b2d-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="94b2d-189">Is-Single-Valued</span></span>       | <span data-ttu-id="94b2d-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-190">True</span></span>                            |
| <span data-ttu-id="94b2d-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="94b2d-191">Is Indexed</span></span>             | <span data-ttu-id="94b2d-192">False</span><span class="sxs-lookup"><span data-stu-id="94b2d-192">False</span></span>                           |
| <span data-ttu-id="94b2d-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="94b2d-193">In Global Catalog</span></span>      | <span data-ttu-id="94b2d-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-194">True</span></span>                            |
| <span data-ttu-id="94b2d-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="94b2d-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="94b2d-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="94b2d-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="94b2d-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="94b2d-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="94b2d-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="94b2d-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="94b2d-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="94b2d-199">Search-Flags</span></span>           | <span data-ttu-id="94b2d-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="94b2d-200">0x00000000</span></span>                      |
| <span data-ttu-id="94b2d-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="94b2d-201">System-Flags</span></span>           | <span data-ttu-id="94b2d-202">0x00000012</span><span class="sxs-lookup"><span data-stu-id="94b2d-202">0x00000012</span></span>                      |
| <span data-ttu-id="94b2d-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="94b2d-203">Classes used in</span></span>        | [<span data-ttu-id="94b2d-204">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="94b2d-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="94b2d-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="94b2d-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="94b2d-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="94b2d-206">Entry</span></span> | <span data-ttu-id="94b2d-207">Wert</span><span class="sxs-lookup"><span data-stu-id="94b2d-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="94b2d-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="94b2d-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="94b2d-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="94b2d-209">MAPI-Id</span></span>                | <span data-ttu-id="94b2d-210">0x80c0</span><span class="sxs-lookup"><span data-stu-id="94b2d-210">0x80C0</span></span>                          |
| <span data-ttu-id="94b2d-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="94b2d-211">System-Only</span></span>            | <span data-ttu-id="94b2d-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-212">True</span></span>                            |
| <span data-ttu-id="94b2d-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="94b2d-213">Is-Single-Valued</span></span>       | <span data-ttu-id="94b2d-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-214">True</span></span>                            |
| <span data-ttu-id="94b2d-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="94b2d-215">Is Indexed</span></span>             | <span data-ttu-id="94b2d-216">False</span><span class="sxs-lookup"><span data-stu-id="94b2d-216">False</span></span>                           |
| <span data-ttu-id="94b2d-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="94b2d-217">In Global Catalog</span></span>      | <span data-ttu-id="94b2d-218">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-218">True</span></span>                            |
| <span data-ttu-id="94b2d-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="94b2d-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="94b2d-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="94b2d-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="94b2d-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="94b2d-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="94b2d-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="94b2d-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="94b2d-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="94b2d-223">Search-Flags</span></span>           | <span data-ttu-id="94b2d-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="94b2d-224">0x00000000</span></span>                      |
| <span data-ttu-id="94b2d-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="94b2d-225">System-Flags</span></span>           | <span data-ttu-id="94b2d-226">0x00000012</span><span class="sxs-lookup"><span data-stu-id="94b2d-226">0x00000012</span></span>                      |
| <span data-ttu-id="94b2d-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="94b2d-227">Classes used in</span></span>        | [<span data-ttu-id="94b2d-228">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="94b2d-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="94b2d-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94b2d-229">Windows Server 2008</span></span>



| <span data-ttu-id="94b2d-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="94b2d-230">Entry</span></span> | <span data-ttu-id="94b2d-231">Wert</span><span class="sxs-lookup"><span data-stu-id="94b2d-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="94b2d-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="94b2d-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="94b2d-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="94b2d-233">MAPI-Id</span></span>                | <span data-ttu-id="94b2d-234">0x80c0</span><span class="sxs-lookup"><span data-stu-id="94b2d-234">0x80C0</span></span>                          |
| <span data-ttu-id="94b2d-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="94b2d-235">System-Only</span></span>            | <span data-ttu-id="94b2d-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-236">True</span></span>                            |
| <span data-ttu-id="94b2d-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="94b2d-237">Is-Single-Valued</span></span>       | <span data-ttu-id="94b2d-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-238">True</span></span>                            |
| <span data-ttu-id="94b2d-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="94b2d-239">Is Indexed</span></span>             | <span data-ttu-id="94b2d-240">False</span><span class="sxs-lookup"><span data-stu-id="94b2d-240">False</span></span>                           |
| <span data-ttu-id="94b2d-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="94b2d-241">In Global Catalog</span></span>      | <span data-ttu-id="94b2d-242">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-242">True</span></span>                            |
| <span data-ttu-id="94b2d-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="94b2d-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="94b2d-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="94b2d-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="94b2d-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="94b2d-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="94b2d-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="94b2d-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="94b2d-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="94b2d-247">Search-Flags</span></span>           | <span data-ttu-id="94b2d-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="94b2d-248">0x00000000</span></span>                      |
| <span data-ttu-id="94b2d-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="94b2d-249">System-Flags</span></span>           | <span data-ttu-id="94b2d-250">0x00000012</span><span class="sxs-lookup"><span data-stu-id="94b2d-250">0x00000012</span></span>                      |
| <span data-ttu-id="94b2d-251">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="94b2d-251">Classes used in</span></span>        | [<span data-ttu-id="94b2d-252">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="94b2d-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="94b2d-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="94b2d-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="94b2d-254">Eingabe</span><span class="sxs-lookup"><span data-stu-id="94b2d-254">Entry</span></span> | <span data-ttu-id="94b2d-255">Wert</span><span class="sxs-lookup"><span data-stu-id="94b2d-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="94b2d-256">Link-ID</span><span class="sxs-lookup"><span data-stu-id="94b2d-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="94b2d-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="94b2d-257">MAPI-Id</span></span>                | <span data-ttu-id="94b2d-258">0x80c0</span><span class="sxs-lookup"><span data-stu-id="94b2d-258">0x80C0</span></span>                          |
| <span data-ttu-id="94b2d-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="94b2d-259">System-Only</span></span>            | <span data-ttu-id="94b2d-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-260">True</span></span>                            |
| <span data-ttu-id="94b2d-261">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="94b2d-261">Is-Single-Valued</span></span>       | <span data-ttu-id="94b2d-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-262">True</span></span>                            |
| <span data-ttu-id="94b2d-263">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="94b2d-263">Is Indexed</span></span>             | <span data-ttu-id="94b2d-264">False</span><span class="sxs-lookup"><span data-stu-id="94b2d-264">False</span></span>                           |
| <span data-ttu-id="94b2d-265">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="94b2d-265">In Global Catalog</span></span>      | <span data-ttu-id="94b2d-266">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-266">True</span></span>                            |
| <span data-ttu-id="94b2d-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="94b2d-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="94b2d-268">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="94b2d-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="94b2d-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="94b2d-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="94b2d-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="94b2d-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="94b2d-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="94b2d-271">Search-Flags</span></span>           | <span data-ttu-id="94b2d-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="94b2d-272">0x00000000</span></span>                      |
| <span data-ttu-id="94b2d-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="94b2d-273">System-Flags</span></span>           | <span data-ttu-id="94b2d-274">0x00000012</span><span class="sxs-lookup"><span data-stu-id="94b2d-274">0x00000012</span></span>                      |
| <span data-ttu-id="94b2d-275">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="94b2d-275">Classes used in</span></span>        | [<span data-ttu-id="94b2d-276">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="94b2d-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="94b2d-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="94b2d-277">Windows Server 2012</span></span>



| <span data-ttu-id="94b2d-278">Eingabe</span><span class="sxs-lookup"><span data-stu-id="94b2d-278">Entry</span></span> | <span data-ttu-id="94b2d-279">Wert</span><span class="sxs-lookup"><span data-stu-id="94b2d-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="94b2d-280">Link-ID</span><span class="sxs-lookup"><span data-stu-id="94b2d-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="94b2d-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="94b2d-281">MAPI-Id</span></span>                | <span data-ttu-id="94b2d-282">0x80c0</span><span class="sxs-lookup"><span data-stu-id="94b2d-282">0x80C0</span></span>                          |
| <span data-ttu-id="94b2d-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="94b2d-283">System-Only</span></span>            | <span data-ttu-id="94b2d-284">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-284">True</span></span>                            |
| <span data-ttu-id="94b2d-285">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="94b2d-285">Is-Single-Valued</span></span>       | <span data-ttu-id="94b2d-286">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-286">True</span></span>                            |
| <span data-ttu-id="94b2d-287">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="94b2d-287">Is Indexed</span></span>             | <span data-ttu-id="94b2d-288">False</span><span class="sxs-lookup"><span data-stu-id="94b2d-288">False</span></span>                           |
| <span data-ttu-id="94b2d-289">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="94b2d-289">In Global Catalog</span></span>      | <span data-ttu-id="94b2d-290">Richtig</span><span class="sxs-lookup"><span data-stu-id="94b2d-290">True</span></span>                            |
| <span data-ttu-id="94b2d-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="94b2d-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="94b2d-292">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="94b2d-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="94b2d-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="94b2d-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="94b2d-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="94b2d-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="94b2d-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="94b2d-295">Search-Flags</span></span>           | <span data-ttu-id="94b2d-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="94b2d-296">0x00000000</span></span>                      |
| <span data-ttu-id="94b2d-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="94b2d-297">System-Flags</span></span>           | <span data-ttu-id="94b2d-298">0x00000012</span><span class="sxs-lookup"><span data-stu-id="94b2d-298">0x00000012</span></span>                      |
| <span data-ttu-id="94b2d-299">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="94b2d-299">Classes used in</span></span>        | [<span data-ttu-id="94b2d-300">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="94b2d-300">**Top**</span></span>](c-top.md)<br/> |



 

 





