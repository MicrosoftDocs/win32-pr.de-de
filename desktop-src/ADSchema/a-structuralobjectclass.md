---
title: Strukturgeschütztes Objektklassen Attribut
description: Dieses konstruierte Attribut speichert eine Liste der Klassen, die in einer Klassenhierarchie enthalten sind, einschließlich abstrakter Klassen. Diese Liste enthält dynamisch verknüpfte Hilfsklassen.
ms.assetid: f7311cb9-4816-4caa-9cae-cbcd61b93d27
ms.tgt_platform: multiple
keywords:
- Struktur-Objektklassen Attribut AD-Schema
- StructuralObjectClass-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Structural-Object-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdcc236c0c65aa365400894dd6ccfb845af04b55
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106343912"
---
# <a name="structural-object-class-attribute"></a><span data-ttu-id="7da6e-106">Strukturgeschütztes Objektklassen Attribut</span><span class="sxs-lookup"><span data-stu-id="7da6e-106">Structural-Object-Class attribute</span></span>

<span data-ttu-id="7da6e-107">Dieses konstruierte Attribut speichert eine Liste der Klassen, die in einer Klassenhierarchie enthalten sind, einschließlich abstrakter Klassen.</span><span class="sxs-lookup"><span data-stu-id="7da6e-107">This constructed attribute stores a list of classes contained in a class hierarchy, including abstract classes.</span></span> <span data-ttu-id="7da6e-108">Diese Liste enthält dynamisch verknüpfte Hilfsklassen.</span><span class="sxs-lookup"><span data-stu-id="7da6e-108">This list does contain dynamically linked auxiliary classes.</span></span>



| <span data-ttu-id="7da6e-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7da6e-109">Entry</span></span> | <span data-ttu-id="7da6e-110">Wert</span><span class="sxs-lookup"><span data-stu-id="7da6e-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="7da6e-111">CN</span><span class="sxs-lookup"><span data-stu-id="7da6e-111">CN</span></span>                | <span data-ttu-id="7da6e-112">Struktur-Objekt-Klasse</span><span class="sxs-lookup"><span data-stu-id="7da6e-112">Structural-Object-Class</span></span>                                         |
| <span data-ttu-id="7da6e-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7da6e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="7da6e-114">StructuralObjectClass</span><span class="sxs-lookup"><span data-stu-id="7da6e-114">structuralObjectClass</span></span>                                           |
| <span data-ttu-id="7da6e-115">Size</span><span class="sxs-lookup"><span data-stu-id="7da6e-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="7da6e-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="7da6e-116">Update Privilege</span></span>  | <span data-ttu-id="7da6e-117">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7da6e-117">This value is set by the system.</span></span>                                |
| <span data-ttu-id="7da6e-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="7da6e-118">Update Frequency</span></span>  | <span data-ttu-id="7da6e-119">Bei der Klassen Erstellung.</span><span class="sxs-lookup"><span data-stu-id="7da6e-119">At class creation.</span></span>                                              |
| <span data-ttu-id="7da6e-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7da6e-120">Attribute-Id</span></span>      | <span data-ttu-id="7da6e-121">2.5.21.9</span><span class="sxs-lookup"><span data-stu-id="7da6e-121">2.5.21.9</span></span>                                                        |
| <span data-ttu-id="7da6e-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7da6e-122">System-Id-Guid</span></span>    | <span data-ttu-id="7da6e-123">3860949b38-9950-81ecb6bc2982</span><span class="sxs-lookup"><span data-stu-id="7da6e-123">3860949f-f6a8-4b38-9950-81ecb6bc2982</span></span>                            |
| <span data-ttu-id="7da6e-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="7da6e-124">Syntax</span></span>            | [<span data-ttu-id="7da6e-125">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="7da6e-125">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="7da6e-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="7da6e-126">Implementations</span></span>

-   [<span data-ttu-id="7da6e-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7da6e-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7da6e-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="7da6e-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7da6e-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7da6e-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7da6e-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7da6e-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7da6e-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7da6e-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7da6e-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7da6e-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7da6e-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7da6e-133">Windows Server 2003</span></span>



| <span data-ttu-id="7da6e-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7da6e-134">Entry</span></span> | <span data-ttu-id="7da6e-135">Wert</span><span class="sxs-lookup"><span data-stu-id="7da6e-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7da6e-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7da6e-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7da6e-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7da6e-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7da6e-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="7da6e-138">System-Only</span></span>            | <span data-ttu-id="7da6e-139">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-139">False</span></span>                           |
| <span data-ttu-id="7da6e-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7da6e-140">Is-Single-Valued</span></span>       | <span data-ttu-id="7da6e-141">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-141">False</span></span>                           |
| <span data-ttu-id="7da6e-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7da6e-142">Is Indexed</span></span>             | <span data-ttu-id="7da6e-143">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-143">False</span></span>                           |
| <span data-ttu-id="7da6e-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7da6e-144">In Global Catalog</span></span>      | <span data-ttu-id="7da6e-145">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-145">False</span></span>                           |
| <span data-ttu-id="7da6e-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7da6e-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="7da6e-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7da6e-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7da6e-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7da6e-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7da6e-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7da6e-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7da6e-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7da6e-150">Search-Flags</span></span>           | <span data-ttu-id="7da6e-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7da6e-151">0x00000000</span></span>                      |
| <span data-ttu-id="7da6e-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7da6e-152">System-Flags</span></span>           | <span data-ttu-id="7da6e-153">0x00000014</span><span class="sxs-lookup"><span data-stu-id="7da6e-153">0x00000014</span></span>                      |
| <span data-ttu-id="7da6e-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7da6e-154">Classes used in</span></span>        | [<span data-ttu-id="7da6e-155">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="7da6e-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7da6e-156">Adam</span><span class="sxs-lookup"><span data-stu-id="7da6e-156">ADAM</span></span>



| <span data-ttu-id="7da6e-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7da6e-157">Entry</span></span> | <span data-ttu-id="7da6e-158">Wert</span><span class="sxs-lookup"><span data-stu-id="7da6e-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7da6e-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7da6e-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7da6e-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7da6e-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7da6e-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="7da6e-161">System-Only</span></span>            | <span data-ttu-id="7da6e-162">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-162">False</span></span>                           |
| <span data-ttu-id="7da6e-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7da6e-163">Is-Single-Valued</span></span>       | <span data-ttu-id="7da6e-164">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-164">False</span></span>                           |
| <span data-ttu-id="7da6e-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7da6e-165">Is Indexed</span></span>             | <span data-ttu-id="7da6e-166">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-166">False</span></span>                           |
| <span data-ttu-id="7da6e-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7da6e-167">In Global Catalog</span></span>      | <span data-ttu-id="7da6e-168">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-168">False</span></span>                           |
| <span data-ttu-id="7da6e-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7da6e-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="7da6e-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7da6e-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7da6e-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7da6e-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7da6e-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7da6e-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7da6e-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7da6e-173">Search-Flags</span></span>           | <span data-ttu-id="7da6e-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7da6e-174">0x00000000</span></span>                      |
| <span data-ttu-id="7da6e-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7da6e-175">System-Flags</span></span>           | <span data-ttu-id="7da6e-176">0x00000014</span><span class="sxs-lookup"><span data-stu-id="7da6e-176">0x00000014</span></span>                      |
| <span data-ttu-id="7da6e-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7da6e-177">Classes used in</span></span>        | [<span data-ttu-id="7da6e-178">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="7da6e-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7da6e-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7da6e-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7da6e-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7da6e-180">Entry</span></span> | <span data-ttu-id="7da6e-181">Wert</span><span class="sxs-lookup"><span data-stu-id="7da6e-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7da6e-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7da6e-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7da6e-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7da6e-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7da6e-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="7da6e-184">System-Only</span></span>            | <span data-ttu-id="7da6e-185">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-185">False</span></span>                           |
| <span data-ttu-id="7da6e-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7da6e-186">Is-Single-Valued</span></span>       | <span data-ttu-id="7da6e-187">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-187">False</span></span>                           |
| <span data-ttu-id="7da6e-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7da6e-188">Is Indexed</span></span>             | <span data-ttu-id="7da6e-189">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-189">False</span></span>                           |
| <span data-ttu-id="7da6e-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7da6e-190">In Global Catalog</span></span>      | <span data-ttu-id="7da6e-191">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-191">False</span></span>                           |
| <span data-ttu-id="7da6e-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7da6e-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="7da6e-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7da6e-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7da6e-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7da6e-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7da6e-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7da6e-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7da6e-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7da6e-196">Search-Flags</span></span>           | <span data-ttu-id="7da6e-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7da6e-197">0x00000000</span></span>                      |
| <span data-ttu-id="7da6e-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7da6e-198">System-Flags</span></span>           | <span data-ttu-id="7da6e-199">0x00000014</span><span class="sxs-lookup"><span data-stu-id="7da6e-199">0x00000014</span></span>                      |
| <span data-ttu-id="7da6e-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7da6e-200">Classes used in</span></span>        | [<span data-ttu-id="7da6e-201">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="7da6e-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7da6e-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7da6e-202">Windows Server 2008</span></span>



| <span data-ttu-id="7da6e-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7da6e-203">Entry</span></span> | <span data-ttu-id="7da6e-204">Wert</span><span class="sxs-lookup"><span data-stu-id="7da6e-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7da6e-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7da6e-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7da6e-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7da6e-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7da6e-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="7da6e-207">System-Only</span></span>            | <span data-ttu-id="7da6e-208">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-208">False</span></span>                           |
| <span data-ttu-id="7da6e-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7da6e-209">Is-Single-Valued</span></span>       | <span data-ttu-id="7da6e-210">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-210">False</span></span>                           |
| <span data-ttu-id="7da6e-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7da6e-211">Is Indexed</span></span>             | <span data-ttu-id="7da6e-212">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-212">False</span></span>                           |
| <span data-ttu-id="7da6e-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7da6e-213">In Global Catalog</span></span>      | <span data-ttu-id="7da6e-214">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-214">False</span></span>                           |
| <span data-ttu-id="7da6e-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7da6e-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="7da6e-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7da6e-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7da6e-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7da6e-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7da6e-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7da6e-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7da6e-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7da6e-219">Search-Flags</span></span>           | <span data-ttu-id="7da6e-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7da6e-220">0x00000000</span></span>                      |
| <span data-ttu-id="7da6e-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7da6e-221">System-Flags</span></span>           | <span data-ttu-id="7da6e-222">0x00000014</span><span class="sxs-lookup"><span data-stu-id="7da6e-222">0x00000014</span></span>                      |
| <span data-ttu-id="7da6e-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7da6e-223">Classes used in</span></span>        | [<span data-ttu-id="7da6e-224">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="7da6e-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7da6e-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7da6e-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7da6e-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7da6e-226">Entry</span></span> | <span data-ttu-id="7da6e-227">Wert</span><span class="sxs-lookup"><span data-stu-id="7da6e-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7da6e-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7da6e-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7da6e-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7da6e-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7da6e-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="7da6e-230">System-Only</span></span>            | <span data-ttu-id="7da6e-231">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-231">False</span></span>                           |
| <span data-ttu-id="7da6e-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7da6e-232">Is-Single-Valued</span></span>       | <span data-ttu-id="7da6e-233">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-233">False</span></span>                           |
| <span data-ttu-id="7da6e-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7da6e-234">Is Indexed</span></span>             | <span data-ttu-id="7da6e-235">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-235">False</span></span>                           |
| <span data-ttu-id="7da6e-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7da6e-236">In Global Catalog</span></span>      | <span data-ttu-id="7da6e-237">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-237">False</span></span>                           |
| <span data-ttu-id="7da6e-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7da6e-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="7da6e-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7da6e-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7da6e-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7da6e-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7da6e-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7da6e-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7da6e-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7da6e-242">Search-Flags</span></span>           | <span data-ttu-id="7da6e-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7da6e-243">0x00000000</span></span>                      |
| <span data-ttu-id="7da6e-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7da6e-244">System-Flags</span></span>           | <span data-ttu-id="7da6e-245">0x00000014</span><span class="sxs-lookup"><span data-stu-id="7da6e-245">0x00000014</span></span>                      |
| <span data-ttu-id="7da6e-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7da6e-246">Classes used in</span></span>        | [<span data-ttu-id="7da6e-247">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="7da6e-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7da6e-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7da6e-248">Windows Server 2012</span></span>



| <span data-ttu-id="7da6e-249">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7da6e-249">Entry</span></span> | <span data-ttu-id="7da6e-250">Wert</span><span class="sxs-lookup"><span data-stu-id="7da6e-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7da6e-251">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7da6e-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7da6e-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7da6e-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7da6e-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="7da6e-253">System-Only</span></span>            | <span data-ttu-id="7da6e-254">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-254">False</span></span>                           |
| <span data-ttu-id="7da6e-255">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7da6e-255">Is-Single-Valued</span></span>       | <span data-ttu-id="7da6e-256">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-256">False</span></span>                           |
| <span data-ttu-id="7da6e-257">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7da6e-257">Is Indexed</span></span>             | <span data-ttu-id="7da6e-258">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-258">False</span></span>                           |
| <span data-ttu-id="7da6e-259">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7da6e-259">In Global Catalog</span></span>      | <span data-ttu-id="7da6e-260">False</span><span class="sxs-lookup"><span data-stu-id="7da6e-260">False</span></span>                           |
| <span data-ttu-id="7da6e-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7da6e-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="7da6e-262">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7da6e-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7da6e-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7da6e-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7da6e-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7da6e-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7da6e-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7da6e-265">Search-Flags</span></span>           | <span data-ttu-id="7da6e-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7da6e-266">0x00000000</span></span>                      |
| <span data-ttu-id="7da6e-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7da6e-267">System-Flags</span></span>           | <span data-ttu-id="7da6e-268">0x00000014</span><span class="sxs-lookup"><span data-stu-id="7da6e-268">0x00000014</span></span>                      |
| <span data-ttu-id="7da6e-269">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7da6e-269">Classes used in</span></span>        | [<span data-ttu-id="7da6e-270">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="7da6e-270">**Top**</span></span>](c-top.md)<br/> |



 

 





