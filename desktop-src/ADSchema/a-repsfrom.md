---
title: Reps-From-Attribut
description: Listet die Server auf, von denen das Verzeichnisänderungen für den definierten Namens Kontext annimmt.
ms.assetid: 2e18410b-d383-4838-aeaf-dd479be5f44d
ms.tgt_platform: multiple
keywords:
- AD-Schema für Reps-From-Attribut
- AD-Schema des repsfrom-Attributs
topic_type:
- apiref
api_name:
- Reps-From
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc6981b71b6ec251eb27af0e7570fe1558d1ff20
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106340033"
---
# <a name="reps-from-attribute"></a><span data-ttu-id="a8daf-105">Reps-From-Attribut</span><span class="sxs-lookup"><span data-stu-id="a8daf-105">Reps-From attribute</span></span>

<span data-ttu-id="a8daf-106">Listet die Server auf, von denen das Verzeichnisänderungen für den definierten Namens Kontext annimmt.</span><span class="sxs-lookup"><span data-stu-id="a8daf-106">Lists the servers from which the directory will accept changes for the defined naming context.</span></span>



| <span data-ttu-id="a8daf-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8daf-107">Entry</span></span> | <span data-ttu-id="a8daf-108">Wert</span><span class="sxs-lookup"><span data-stu-id="a8daf-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="a8daf-109">CN</span><span class="sxs-lookup"><span data-stu-id="a8daf-109">CN</span></span>                | <span data-ttu-id="a8daf-110">Reps-From</span><span class="sxs-lookup"><span data-stu-id="a8daf-110">Reps-From</span></span>                                             |
| <span data-ttu-id="a8daf-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a8daf-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a8daf-112">repsfrom</span><span class="sxs-lookup"><span data-stu-id="a8daf-112">repsFrom</span></span>                                              |
| <span data-ttu-id="a8daf-113">Size</span><span class="sxs-lookup"><span data-stu-id="a8daf-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="a8daf-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a8daf-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="a8daf-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="a8daf-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="a8daf-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a8daf-116">Attribute-Id</span></span>      | <span data-ttu-id="a8daf-117">1.2.840.113556.1.2.91</span><span class="sxs-lookup"><span data-stu-id="a8daf-117">1.2.840.113556.1.2.91</span></span>                                 |
| <span data-ttu-id="a8daf-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a8daf-118">System-Id-Guid</span></span>    | <span data-ttu-id="a8daf-119">bf967a1d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a8daf-119">bf967a1d-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="a8daf-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8daf-120">Syntax</span></span>            | [<span data-ttu-id="a8daf-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="a8daf-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="a8daf-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="a8daf-122">Implementations</span></span>

-   [<span data-ttu-id="a8daf-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a8daf-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a8daf-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a8daf-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a8daf-125">**Adam**</span><span class="sxs-lookup"><span data-stu-id="a8daf-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a8daf-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a8daf-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a8daf-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a8daf-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a8daf-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a8daf-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a8daf-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a8daf-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a8daf-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a8daf-130">Windows 2000 Server</span></span>



| <span data-ttu-id="a8daf-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8daf-131">Entry</span></span> | <span data-ttu-id="a8daf-132">Wert</span><span class="sxs-lookup"><span data-stu-id="a8daf-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a8daf-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8daf-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a8daf-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8daf-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a8daf-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8daf-135">System-Only</span></span>            | <span data-ttu-id="a8daf-136">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8daf-136">True</span></span>                            |
| <span data-ttu-id="a8daf-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8daf-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a8daf-138">False</span><span class="sxs-lookup"><span data-stu-id="a8daf-138">False</span></span>                           |
| <span data-ttu-id="a8daf-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8daf-139">Is Indexed</span></span>             | <span data-ttu-id="a8daf-140">False</span><span class="sxs-lookup"><span data-stu-id="a8daf-140">False</span></span>                           |
| <span data-ttu-id="a8daf-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8daf-141">In Global Catalog</span></span>      | <span data-ttu-id="a8daf-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8daf-142">True</span></span>                            |
| <span data-ttu-id="a8daf-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8daf-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8daf-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8daf-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a8daf-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8daf-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a8daf-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8daf-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a8daf-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8daf-147">Search-Flags</span></span>           | <span data-ttu-id="a8daf-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8daf-148">0x00000000</span></span>                      |
| <span data-ttu-id="a8daf-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8daf-149">System-Flags</span></span>           | <span data-ttu-id="a8daf-150">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a8daf-150">0x00000013</span></span>                      |
| <span data-ttu-id="a8daf-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8daf-151">Classes used in</span></span>        | [<span data-ttu-id="a8daf-152">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a8daf-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a8daf-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8daf-153">Windows Server 2003</span></span>



| <span data-ttu-id="a8daf-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8daf-154">Entry</span></span> | <span data-ttu-id="a8daf-155">Wert</span><span class="sxs-lookup"><span data-stu-id="a8daf-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a8daf-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8daf-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a8daf-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8daf-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a8daf-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8daf-158">System-Only</span></span>            | <span data-ttu-id="a8daf-159">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8daf-159">True</span></span>                            |
| <span data-ttu-id="a8daf-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8daf-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a8daf-161">False</span><span class="sxs-lookup"><span data-stu-id="a8daf-161">False</span></span>                           |
| <span data-ttu-id="a8daf-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8daf-162">Is Indexed</span></span>             | <span data-ttu-id="a8daf-163">False</span><span class="sxs-lookup"><span data-stu-id="a8daf-163">False</span></span>                           |
| <span data-ttu-id="a8daf-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8daf-164">In Global Catalog</span></span>      | <span data-ttu-id="a8daf-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8daf-165">True</span></span>                            |
| <span data-ttu-id="a8daf-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8daf-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8daf-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8daf-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a8daf-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8daf-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a8daf-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8daf-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a8daf-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8daf-170">Search-Flags</span></span>           | <span data-ttu-id="a8daf-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8daf-171">0x00000000</span></span>                      |
| <span data-ttu-id="a8daf-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8daf-172">System-Flags</span></span>           | <span data-ttu-id="a8daf-173">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a8daf-173">0x00000013</span></span>                      |
| <span data-ttu-id="a8daf-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8daf-174">Classes used in</span></span>        | [<span data-ttu-id="a8daf-175">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a8daf-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a8daf-176">Adam</span><span class="sxs-lookup"><span data-stu-id="a8daf-176">ADAM</span></span>



| <span data-ttu-id="a8daf-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8daf-177">Entry</span></span> | <span data-ttu-id="a8daf-178">Wert</span><span class="sxs-lookup"><span data-stu-id="a8daf-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a8daf-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8daf-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a8daf-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8daf-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a8daf-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8daf-181">System-Only</span></span>            | <span data-ttu-id="a8daf-182">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8daf-182">True</span></span>                            |
| <span data-ttu-id="a8daf-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8daf-183">Is-Single-Valued</span></span>       | <span data-ttu-id="a8daf-184">False</span><span class="sxs-lookup"><span data-stu-id="a8daf-184">False</span></span>                           |
| <span data-ttu-id="a8daf-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8daf-185">Is Indexed</span></span>             | <span data-ttu-id="a8daf-186">False</span><span class="sxs-lookup"><span data-stu-id="a8daf-186">False</span></span>                           |
| <span data-ttu-id="a8daf-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8daf-187">In Global Catalog</span></span>      | <span data-ttu-id="a8daf-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8daf-188">True</span></span>                            |
| <span data-ttu-id="a8daf-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8daf-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8daf-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8daf-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a8daf-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8daf-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a8daf-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8daf-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a8daf-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8daf-193">Search-Flags</span></span>           | <span data-ttu-id="a8daf-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8daf-194">0x00000000</span></span>                      |
| <span data-ttu-id="a8daf-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8daf-195">System-Flags</span></span>           | <span data-ttu-id="a8daf-196">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a8daf-196">0x00000013</span></span>                      |
| <span data-ttu-id="a8daf-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8daf-197">Classes used in</span></span>        | [<span data-ttu-id="a8daf-198">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a8daf-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a8daf-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a8daf-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a8daf-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8daf-200">Entry</span></span> | <span data-ttu-id="a8daf-201">Wert</span><span class="sxs-lookup"><span data-stu-id="a8daf-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a8daf-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8daf-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a8daf-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8daf-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a8daf-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8daf-204">System-Only</span></span>            | <span data-ttu-id="a8daf-205">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8daf-205">True</span></span>                            |
| <span data-ttu-id="a8daf-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8daf-206">Is-Single-Valued</span></span>       | <span data-ttu-id="a8daf-207">False</span><span class="sxs-lookup"><span data-stu-id="a8daf-207">False</span></span>                           |
| <span data-ttu-id="a8daf-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8daf-208">Is Indexed</span></span>             | <span data-ttu-id="a8daf-209">False</span><span class="sxs-lookup"><span data-stu-id="a8daf-209">False</span></span>                           |
| <span data-ttu-id="a8daf-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8daf-210">In Global Catalog</span></span>      | <span data-ttu-id="a8daf-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8daf-211">True</span></span>                            |
| <span data-ttu-id="a8daf-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8daf-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8daf-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8daf-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a8daf-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8daf-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a8daf-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8daf-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a8daf-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8daf-216">Search-Flags</span></span>           | <span data-ttu-id="a8daf-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8daf-217">0x00000000</span></span>                      |
| <span data-ttu-id="a8daf-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8daf-218">System-Flags</span></span>           | <span data-ttu-id="a8daf-219">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a8daf-219">0x00000013</span></span>                      |
| <span data-ttu-id="a8daf-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8daf-220">Classes used in</span></span>        | [<span data-ttu-id="a8daf-221">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a8daf-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a8daf-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8daf-222">Windows Server 2008</span></span>



| <span data-ttu-id="a8daf-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8daf-223">Entry</span></span> | <span data-ttu-id="a8daf-224">Wert</span><span class="sxs-lookup"><span data-stu-id="a8daf-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a8daf-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8daf-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a8daf-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8daf-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a8daf-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8daf-227">System-Only</span></span>            | <span data-ttu-id="a8daf-228">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8daf-228">True</span></span>                            |
| <span data-ttu-id="a8daf-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8daf-229">Is-Single-Valued</span></span>       | <span data-ttu-id="a8daf-230">False</span><span class="sxs-lookup"><span data-stu-id="a8daf-230">False</span></span>                           |
| <span data-ttu-id="a8daf-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8daf-231">Is Indexed</span></span>             | <span data-ttu-id="a8daf-232">False</span><span class="sxs-lookup"><span data-stu-id="a8daf-232">False</span></span>                           |
| <span data-ttu-id="a8daf-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8daf-233">In Global Catalog</span></span>      | <span data-ttu-id="a8daf-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8daf-234">True</span></span>                            |
| <span data-ttu-id="a8daf-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8daf-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8daf-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8daf-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a8daf-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8daf-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a8daf-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8daf-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a8daf-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8daf-239">Search-Flags</span></span>           | <span data-ttu-id="a8daf-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8daf-240">0x00000000</span></span>                      |
| <span data-ttu-id="a8daf-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8daf-241">System-Flags</span></span>           | <span data-ttu-id="a8daf-242">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a8daf-242">0x00000013</span></span>                      |
| <span data-ttu-id="a8daf-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8daf-243">Classes used in</span></span>        | [<span data-ttu-id="a8daf-244">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a8daf-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a8daf-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a8daf-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a8daf-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8daf-246">Entry</span></span> | <span data-ttu-id="a8daf-247">Wert</span><span class="sxs-lookup"><span data-stu-id="a8daf-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a8daf-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8daf-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a8daf-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8daf-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a8daf-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8daf-250">System-Only</span></span>            | <span data-ttu-id="a8daf-251">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8daf-251">True</span></span>                            |
| <span data-ttu-id="a8daf-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8daf-252">Is-Single-Valued</span></span>       | <span data-ttu-id="a8daf-253">False</span><span class="sxs-lookup"><span data-stu-id="a8daf-253">False</span></span>                           |
| <span data-ttu-id="a8daf-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8daf-254">Is Indexed</span></span>             | <span data-ttu-id="a8daf-255">False</span><span class="sxs-lookup"><span data-stu-id="a8daf-255">False</span></span>                           |
| <span data-ttu-id="a8daf-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8daf-256">In Global Catalog</span></span>      | <span data-ttu-id="a8daf-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8daf-257">True</span></span>                            |
| <span data-ttu-id="a8daf-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8daf-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8daf-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8daf-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a8daf-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8daf-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a8daf-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8daf-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a8daf-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8daf-262">Search-Flags</span></span>           | <span data-ttu-id="a8daf-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8daf-263">0x00000000</span></span>                      |
| <span data-ttu-id="a8daf-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8daf-264">System-Flags</span></span>           | <span data-ttu-id="a8daf-265">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a8daf-265">0x00000013</span></span>                      |
| <span data-ttu-id="a8daf-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8daf-266">Classes used in</span></span>        | [<span data-ttu-id="a8daf-267">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a8daf-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a8daf-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a8daf-268">Windows Server 2012</span></span>



| <span data-ttu-id="a8daf-269">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8daf-269">Entry</span></span> | <span data-ttu-id="a8daf-270">Wert</span><span class="sxs-lookup"><span data-stu-id="a8daf-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a8daf-271">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8daf-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a8daf-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8daf-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a8daf-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8daf-273">System-Only</span></span>            | <span data-ttu-id="a8daf-274">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8daf-274">True</span></span>                            |
| <span data-ttu-id="a8daf-275">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8daf-275">Is-Single-Valued</span></span>       | <span data-ttu-id="a8daf-276">False</span><span class="sxs-lookup"><span data-stu-id="a8daf-276">False</span></span>                           |
| <span data-ttu-id="a8daf-277">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8daf-277">Is Indexed</span></span>             | <span data-ttu-id="a8daf-278">False</span><span class="sxs-lookup"><span data-stu-id="a8daf-278">False</span></span>                           |
| <span data-ttu-id="a8daf-279">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8daf-279">In Global Catalog</span></span>      | <span data-ttu-id="a8daf-280">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8daf-280">True</span></span>                            |
| <span data-ttu-id="a8daf-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8daf-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8daf-282">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8daf-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a8daf-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8daf-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a8daf-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8daf-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a8daf-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8daf-285">Search-Flags</span></span>           | <span data-ttu-id="a8daf-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8daf-286">0x00000000</span></span>                      |
| <span data-ttu-id="a8daf-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8daf-287">System-Flags</span></span>           | <span data-ttu-id="a8daf-288">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a8daf-288">0x00000013</span></span>                      |
| <span data-ttu-id="a8daf-289">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8daf-289">Classes used in</span></span>        | [<span data-ttu-id="a8daf-290">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a8daf-290">**Top**</span></span>](c-top.md)<br/> |



 

 





