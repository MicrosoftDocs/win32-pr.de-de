---
title: Reps-To-Attribut
description: Listet die Server auf, über die das Verzeichnis über Änderungen und Server benachrichtigt wird, an die das Verzeichnisänderungen an der Anforderung für den definierten Namens Kontext sendet.
ms.assetid: d7fd5a57-a0e1-4c69-9b9a-1cdad87610b1
ms.tgt_platform: multiple
keywords:
- AD-Schema für Reps-To-Attribut
- AD-Schema für repsto-Attribut
topic_type:
- apiref
api_name:
- Reps-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd5c39d19eb12bb801d7ca7fb9b22ed665d59d10
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957588"
---
# <a name="reps-to-attribute"></a><span data-ttu-id="c410e-105">Reps-To-Attribut</span><span class="sxs-lookup"><span data-stu-id="c410e-105">Reps-To attribute</span></span>

<span data-ttu-id="c410e-106">Listet die Server auf, über die das Verzeichnis über Änderungen und Server benachrichtigt wird, an die das Verzeichnisänderungen an der Anforderung für den definierten Namens Kontext sendet.</span><span class="sxs-lookup"><span data-stu-id="c410e-106">Lists the servers that the directory will notify of changes and servers to which the directory will send changes on Request for the defined naming context.</span></span>



| <span data-ttu-id="c410e-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c410e-107">Entry</span></span> | <span data-ttu-id="c410e-108">Wert</span><span class="sxs-lookup"><span data-stu-id="c410e-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="c410e-109">CN</span><span class="sxs-lookup"><span data-stu-id="c410e-109">CN</span></span>                | <span data-ttu-id="c410e-110">Reps-To</span><span class="sxs-lookup"><span data-stu-id="c410e-110">Reps-To</span></span>                                               |
| <span data-ttu-id="c410e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c410e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c410e-112">repsto</span><span class="sxs-lookup"><span data-stu-id="c410e-112">repsTo</span></span>                                                |
| <span data-ttu-id="c410e-113">Size</span><span class="sxs-lookup"><span data-stu-id="c410e-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="c410e-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c410e-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="c410e-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="c410e-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="c410e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c410e-116">Attribute-Id</span></span>      | <span data-ttu-id="c410e-117">1.2.840.113556.1.2.83</span><span class="sxs-lookup"><span data-stu-id="c410e-117">1.2.840.113556.1.2.83</span></span>                                 |
| <span data-ttu-id="c410e-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c410e-118">System-Id-Guid</span></span>    | <span data-ttu-id="c410e-119">bf967a1e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c410e-119">bf967a1e-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="c410e-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="c410e-120">Syntax</span></span>            | [<span data-ttu-id="c410e-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="c410e-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="c410e-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="c410e-122">Implementations</span></span>

-   [<span data-ttu-id="c410e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c410e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c410e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c410e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c410e-125">**Adam**</span><span class="sxs-lookup"><span data-stu-id="c410e-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c410e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c410e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c410e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c410e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c410e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c410e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c410e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c410e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c410e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c410e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="c410e-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c410e-131">Entry</span></span> | <span data-ttu-id="c410e-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c410e-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c410e-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c410e-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c410e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c410e-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c410e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c410e-135">System-Only</span></span>            | <span data-ttu-id="c410e-136">Richtig</span><span class="sxs-lookup"><span data-stu-id="c410e-136">True</span></span>                            |
| <span data-ttu-id="c410e-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c410e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c410e-138">False</span><span class="sxs-lookup"><span data-stu-id="c410e-138">False</span></span>                           |
| <span data-ttu-id="c410e-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c410e-139">Is Indexed</span></span>             | <span data-ttu-id="c410e-140">False</span><span class="sxs-lookup"><span data-stu-id="c410e-140">False</span></span>                           |
| <span data-ttu-id="c410e-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c410e-141">In Global Catalog</span></span>      | <span data-ttu-id="c410e-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="c410e-142">True</span></span>                            |
| <span data-ttu-id="c410e-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c410e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c410e-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c410e-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c410e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c410e-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c410e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c410e-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c410e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c410e-147">Search-Flags</span></span>           | <span data-ttu-id="c410e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c410e-148">0x00000000</span></span>                      |
| <span data-ttu-id="c410e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c410e-149">System-Flags</span></span>           | <span data-ttu-id="c410e-150">0x00000013</span><span class="sxs-lookup"><span data-stu-id="c410e-150">0x00000013</span></span>                      |
| <span data-ttu-id="c410e-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c410e-151">Classes used in</span></span>        | [<span data-ttu-id="c410e-152">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c410e-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c410e-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c410e-153">Windows Server 2003</span></span>



| <span data-ttu-id="c410e-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c410e-154">Entry</span></span> | <span data-ttu-id="c410e-155">Wert</span><span class="sxs-lookup"><span data-stu-id="c410e-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c410e-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c410e-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c410e-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c410e-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c410e-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c410e-158">System-Only</span></span>            | <span data-ttu-id="c410e-159">Richtig</span><span class="sxs-lookup"><span data-stu-id="c410e-159">True</span></span>                            |
| <span data-ttu-id="c410e-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c410e-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c410e-161">False</span><span class="sxs-lookup"><span data-stu-id="c410e-161">False</span></span>                           |
| <span data-ttu-id="c410e-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c410e-162">Is Indexed</span></span>             | <span data-ttu-id="c410e-163">False</span><span class="sxs-lookup"><span data-stu-id="c410e-163">False</span></span>                           |
| <span data-ttu-id="c410e-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c410e-164">In Global Catalog</span></span>      | <span data-ttu-id="c410e-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="c410e-165">True</span></span>                            |
| <span data-ttu-id="c410e-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c410e-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c410e-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c410e-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c410e-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c410e-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c410e-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c410e-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c410e-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c410e-170">Search-Flags</span></span>           | <span data-ttu-id="c410e-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c410e-171">0x00000000</span></span>                      |
| <span data-ttu-id="c410e-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c410e-172">System-Flags</span></span>           | <span data-ttu-id="c410e-173">0x00000013</span><span class="sxs-lookup"><span data-stu-id="c410e-173">0x00000013</span></span>                      |
| <span data-ttu-id="c410e-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c410e-174">Classes used in</span></span>        | [<span data-ttu-id="c410e-175">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c410e-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c410e-176">Adam</span><span class="sxs-lookup"><span data-stu-id="c410e-176">ADAM</span></span>



| <span data-ttu-id="c410e-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c410e-177">Entry</span></span> | <span data-ttu-id="c410e-178">Wert</span><span class="sxs-lookup"><span data-stu-id="c410e-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c410e-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c410e-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c410e-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c410e-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c410e-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="c410e-181">System-Only</span></span>            | <span data-ttu-id="c410e-182">Richtig</span><span class="sxs-lookup"><span data-stu-id="c410e-182">True</span></span>                            |
| <span data-ttu-id="c410e-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c410e-183">Is-Single-Valued</span></span>       | <span data-ttu-id="c410e-184">False</span><span class="sxs-lookup"><span data-stu-id="c410e-184">False</span></span>                           |
| <span data-ttu-id="c410e-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c410e-185">Is Indexed</span></span>             | <span data-ttu-id="c410e-186">False</span><span class="sxs-lookup"><span data-stu-id="c410e-186">False</span></span>                           |
| <span data-ttu-id="c410e-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c410e-187">In Global Catalog</span></span>      | <span data-ttu-id="c410e-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="c410e-188">True</span></span>                            |
| <span data-ttu-id="c410e-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c410e-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="c410e-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c410e-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c410e-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c410e-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c410e-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c410e-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c410e-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c410e-193">Search-Flags</span></span>           | <span data-ttu-id="c410e-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c410e-194">0x00000000</span></span>                      |
| <span data-ttu-id="c410e-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c410e-195">System-Flags</span></span>           | <span data-ttu-id="c410e-196">0x00000013</span><span class="sxs-lookup"><span data-stu-id="c410e-196">0x00000013</span></span>                      |
| <span data-ttu-id="c410e-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c410e-197">Classes used in</span></span>        | [<span data-ttu-id="c410e-198">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c410e-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c410e-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c410e-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c410e-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c410e-200">Entry</span></span> | <span data-ttu-id="c410e-201">Wert</span><span class="sxs-lookup"><span data-stu-id="c410e-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c410e-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c410e-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c410e-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c410e-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c410e-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="c410e-204">System-Only</span></span>            | <span data-ttu-id="c410e-205">Richtig</span><span class="sxs-lookup"><span data-stu-id="c410e-205">True</span></span>                            |
| <span data-ttu-id="c410e-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c410e-206">Is-Single-Valued</span></span>       | <span data-ttu-id="c410e-207">False</span><span class="sxs-lookup"><span data-stu-id="c410e-207">False</span></span>                           |
| <span data-ttu-id="c410e-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c410e-208">Is Indexed</span></span>             | <span data-ttu-id="c410e-209">False</span><span class="sxs-lookup"><span data-stu-id="c410e-209">False</span></span>                           |
| <span data-ttu-id="c410e-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c410e-210">In Global Catalog</span></span>      | <span data-ttu-id="c410e-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="c410e-211">True</span></span>                            |
| <span data-ttu-id="c410e-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c410e-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="c410e-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c410e-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c410e-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c410e-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c410e-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c410e-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c410e-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c410e-216">Search-Flags</span></span>           | <span data-ttu-id="c410e-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c410e-217">0x00000000</span></span>                      |
| <span data-ttu-id="c410e-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c410e-218">System-Flags</span></span>           | <span data-ttu-id="c410e-219">0x00000013</span><span class="sxs-lookup"><span data-stu-id="c410e-219">0x00000013</span></span>                      |
| <span data-ttu-id="c410e-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c410e-220">Classes used in</span></span>        | [<span data-ttu-id="c410e-221">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c410e-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c410e-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c410e-222">Windows Server 2008</span></span>



| <span data-ttu-id="c410e-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c410e-223">Entry</span></span> | <span data-ttu-id="c410e-224">Wert</span><span class="sxs-lookup"><span data-stu-id="c410e-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c410e-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c410e-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c410e-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c410e-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c410e-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="c410e-227">System-Only</span></span>            | <span data-ttu-id="c410e-228">Richtig</span><span class="sxs-lookup"><span data-stu-id="c410e-228">True</span></span>                            |
| <span data-ttu-id="c410e-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c410e-229">Is-Single-Valued</span></span>       | <span data-ttu-id="c410e-230">False</span><span class="sxs-lookup"><span data-stu-id="c410e-230">False</span></span>                           |
| <span data-ttu-id="c410e-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c410e-231">Is Indexed</span></span>             | <span data-ttu-id="c410e-232">False</span><span class="sxs-lookup"><span data-stu-id="c410e-232">False</span></span>                           |
| <span data-ttu-id="c410e-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c410e-233">In Global Catalog</span></span>      | <span data-ttu-id="c410e-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="c410e-234">True</span></span>                            |
| <span data-ttu-id="c410e-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c410e-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="c410e-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c410e-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c410e-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c410e-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c410e-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c410e-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c410e-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c410e-239">Search-Flags</span></span>           | <span data-ttu-id="c410e-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c410e-240">0x00000000</span></span>                      |
| <span data-ttu-id="c410e-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c410e-241">System-Flags</span></span>           | <span data-ttu-id="c410e-242">0x00000013</span><span class="sxs-lookup"><span data-stu-id="c410e-242">0x00000013</span></span>                      |
| <span data-ttu-id="c410e-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c410e-243">Classes used in</span></span>        | [<span data-ttu-id="c410e-244">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c410e-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c410e-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c410e-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c410e-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c410e-246">Entry</span></span> | <span data-ttu-id="c410e-247">Wert</span><span class="sxs-lookup"><span data-stu-id="c410e-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c410e-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c410e-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c410e-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c410e-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c410e-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="c410e-250">System-Only</span></span>            | <span data-ttu-id="c410e-251">Richtig</span><span class="sxs-lookup"><span data-stu-id="c410e-251">True</span></span>                            |
| <span data-ttu-id="c410e-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c410e-252">Is-Single-Valued</span></span>       | <span data-ttu-id="c410e-253">False</span><span class="sxs-lookup"><span data-stu-id="c410e-253">False</span></span>                           |
| <span data-ttu-id="c410e-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c410e-254">Is Indexed</span></span>             | <span data-ttu-id="c410e-255">False</span><span class="sxs-lookup"><span data-stu-id="c410e-255">False</span></span>                           |
| <span data-ttu-id="c410e-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c410e-256">In Global Catalog</span></span>      | <span data-ttu-id="c410e-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="c410e-257">True</span></span>                            |
| <span data-ttu-id="c410e-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c410e-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="c410e-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c410e-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c410e-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c410e-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c410e-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c410e-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c410e-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c410e-262">Search-Flags</span></span>           | <span data-ttu-id="c410e-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c410e-263">0x00000000</span></span>                      |
| <span data-ttu-id="c410e-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c410e-264">System-Flags</span></span>           | <span data-ttu-id="c410e-265">0x00000013</span><span class="sxs-lookup"><span data-stu-id="c410e-265">0x00000013</span></span>                      |
| <span data-ttu-id="c410e-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c410e-266">Classes used in</span></span>        | [<span data-ttu-id="c410e-267">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c410e-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c410e-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c410e-268">Windows Server 2012</span></span>



| <span data-ttu-id="c410e-269">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c410e-269">Entry</span></span> | <span data-ttu-id="c410e-270">Wert</span><span class="sxs-lookup"><span data-stu-id="c410e-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c410e-271">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c410e-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c410e-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c410e-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c410e-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="c410e-273">System-Only</span></span>            | <span data-ttu-id="c410e-274">Richtig</span><span class="sxs-lookup"><span data-stu-id="c410e-274">True</span></span>                            |
| <span data-ttu-id="c410e-275">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c410e-275">Is-Single-Valued</span></span>       | <span data-ttu-id="c410e-276">False</span><span class="sxs-lookup"><span data-stu-id="c410e-276">False</span></span>                           |
| <span data-ttu-id="c410e-277">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c410e-277">Is Indexed</span></span>             | <span data-ttu-id="c410e-278">False</span><span class="sxs-lookup"><span data-stu-id="c410e-278">False</span></span>                           |
| <span data-ttu-id="c410e-279">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c410e-279">In Global Catalog</span></span>      | <span data-ttu-id="c410e-280">Richtig</span><span class="sxs-lookup"><span data-stu-id="c410e-280">True</span></span>                            |
| <span data-ttu-id="c410e-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c410e-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="c410e-282">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c410e-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c410e-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c410e-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c410e-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c410e-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c410e-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c410e-285">Search-Flags</span></span>           | <span data-ttu-id="c410e-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c410e-286">0x00000000</span></span>                      |
| <span data-ttu-id="c410e-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c410e-287">System-Flags</span></span>           | <span data-ttu-id="c410e-288">0x00000013</span><span class="sxs-lookup"><span data-stu-id="c410e-288">0x00000013</span></span>                      |
| <span data-ttu-id="c410e-289">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c410e-289">Classes used in</span></span>        | [<span data-ttu-id="c410e-290">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c410e-290">**Top**</span></span>](c-top.md)<br/> |



 

 





