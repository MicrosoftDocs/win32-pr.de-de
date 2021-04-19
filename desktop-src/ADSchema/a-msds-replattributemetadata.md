---
title: ms-DS-repl-Attribute-Meta-Data-Attribut
description: Eine Liste von Metadaten für jedes replizierte Attribut. Die Metadaten zeigen an, wer das Attribut zuletzt geändert hat.
ms.assetid: 07cfd323-eb90-4715-9307-583cf7e9f63e
ms.tgt_platform: multiple
keywords:
- "\"ms-DS-repl-Attribute-Meta-Data\"-Attribut AD-Schema"
- adschema des msDS-ReplAttributeMetaData-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Repl-Attribute-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edc991ead7104d8b9b4c023882d39adf1d53446
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342512"
---
# <a name="ms-ds-repl-attribute-meta-data-attribute"></a><span data-ttu-id="b1c63-106">ms-DS-repl-Attribute-Meta-Data-Attribut</span><span class="sxs-lookup"><span data-stu-id="b1c63-106">ms-DS-Repl-Attribute-Meta-Data attribute</span></span>

<span data-ttu-id="b1c63-107">Eine Liste von Metadaten für jedes replizierte Attribut.</span><span class="sxs-lookup"><span data-stu-id="b1c63-107">A list of metadata for each replicated attribute.</span></span> <span data-ttu-id="b1c63-108">Die Metadaten zeigen an, wer das Attribut zuletzt geändert hat.</span><span class="sxs-lookup"><span data-stu-id="b1c63-108">The metadata indicates who changed the attribute last.</span></span>



| <span data-ttu-id="b1c63-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b1c63-109">Entry</span></span> | <span data-ttu-id="b1c63-110">Wert</span><span class="sxs-lookup"><span data-stu-id="b1c63-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b1c63-111">CN</span><span class="sxs-lookup"><span data-stu-id="b1c63-111">CN</span></span>                | <span data-ttu-id="b1c63-112">ms-DS-repl-Attribute-Meta-Data</span><span class="sxs-lookup"><span data-stu-id="b1c63-112">ms-DS-Repl-Attribute-Meta-Data</span></span>              |
| <span data-ttu-id="b1c63-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b1c63-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b1c63-114">msDS-ReplAttributeMetaData</span><span class="sxs-lookup"><span data-stu-id="b1c63-114">msDS-ReplAttributeMetaData</span></span>                  |
| <span data-ttu-id="b1c63-115">Size</span><span class="sxs-lookup"><span data-stu-id="b1c63-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="b1c63-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b1c63-116">Update Privilege</span></span>  | <span data-ttu-id="b1c63-117">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1c63-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="b1c63-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b1c63-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b1c63-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b1c63-119">Attribute-Id</span></span>      | <span data-ttu-id="b1c63-120">1.2.840.113556.1.4.1707</span><span class="sxs-lookup"><span data-stu-id="b1c63-120">1.2.840.113556.1.4.1707</span></span>                     |
| <span data-ttu-id="b1c63-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b1c63-121">System-Id-Guid</span></span>    | <span data-ttu-id="b1c63-122">d7c53242-724e-4c39-9d4c-2df8c9d66c7a</span><span class="sxs-lookup"><span data-stu-id="b1c63-122">d7c53242-724e-4c39-9d4c-2df8c9d66c7a</span></span>        |
| <span data-ttu-id="b1c63-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1c63-123">Syntax</span></span>            | [<span data-ttu-id="b1c63-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b1c63-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b1c63-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b1c63-125">Implementations</span></span>

-   [<span data-ttu-id="b1c63-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b1c63-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b1c63-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="b1c63-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b1c63-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b1c63-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b1c63-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b1c63-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b1c63-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b1c63-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b1c63-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b1c63-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b1c63-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1c63-132">Windows Server 2003</span></span>



| <span data-ttu-id="b1c63-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b1c63-133">Entry</span></span> | <span data-ttu-id="b1c63-134">Wert</span><span class="sxs-lookup"><span data-stu-id="b1c63-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1c63-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b1c63-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1c63-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1c63-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b1c63-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1c63-137">System-Only</span></span>            | <span data-ttu-id="b1c63-138">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-138">False</span></span>                           |
| <span data-ttu-id="b1c63-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b1c63-139">Is-Single-Valued</span></span>       | <span data-ttu-id="b1c63-140">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-140">False</span></span>                           |
| <span data-ttu-id="b1c63-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b1c63-141">Is Indexed</span></span>             | <span data-ttu-id="b1c63-142">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-142">False</span></span>                           |
| <span data-ttu-id="b1c63-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b1c63-143">In Global Catalog</span></span>      | <span data-ttu-id="b1c63-144">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-144">False</span></span>                           |
| <span data-ttu-id="b1c63-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1c63-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1c63-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b1c63-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1c63-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1c63-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1c63-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1c63-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1c63-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1c63-149">Search-Flags</span></span>           | <span data-ttu-id="b1c63-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1c63-150">0x00000000</span></span>                      |
| <span data-ttu-id="b1c63-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1c63-151">System-Flags</span></span>           | <span data-ttu-id="b1c63-152">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b1c63-152">0x00000014</span></span>                      |
| <span data-ttu-id="b1c63-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b1c63-153">Classes used in</span></span>        | [<span data-ttu-id="b1c63-154">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b1c63-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b1c63-155">Adam</span><span class="sxs-lookup"><span data-stu-id="b1c63-155">ADAM</span></span>



| <span data-ttu-id="b1c63-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b1c63-156">Entry</span></span> | <span data-ttu-id="b1c63-157">Wert</span><span class="sxs-lookup"><span data-stu-id="b1c63-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1c63-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b1c63-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1c63-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1c63-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b1c63-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1c63-160">System-Only</span></span>            | <span data-ttu-id="b1c63-161">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-161">False</span></span>                           |
| <span data-ttu-id="b1c63-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b1c63-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b1c63-163">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-163">False</span></span>                           |
| <span data-ttu-id="b1c63-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b1c63-164">Is Indexed</span></span>             | <span data-ttu-id="b1c63-165">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-165">False</span></span>                           |
| <span data-ttu-id="b1c63-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b1c63-166">In Global Catalog</span></span>      | <span data-ttu-id="b1c63-167">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-167">False</span></span>                           |
| <span data-ttu-id="b1c63-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1c63-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1c63-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b1c63-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1c63-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1c63-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1c63-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1c63-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1c63-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1c63-172">Search-Flags</span></span>           | <span data-ttu-id="b1c63-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1c63-173">0x00000000</span></span>                      |
| <span data-ttu-id="b1c63-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1c63-174">System-Flags</span></span>           | <span data-ttu-id="b1c63-175">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b1c63-175">0x00000014</span></span>                      |
| <span data-ttu-id="b1c63-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b1c63-176">Classes used in</span></span>        | [<span data-ttu-id="b1c63-177">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b1c63-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b1c63-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b1c63-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b1c63-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b1c63-179">Entry</span></span> | <span data-ttu-id="b1c63-180">Wert</span><span class="sxs-lookup"><span data-stu-id="b1c63-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1c63-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b1c63-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1c63-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1c63-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b1c63-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1c63-183">System-Only</span></span>            | <span data-ttu-id="b1c63-184">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-184">False</span></span>                           |
| <span data-ttu-id="b1c63-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b1c63-185">Is-Single-Valued</span></span>       | <span data-ttu-id="b1c63-186">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-186">False</span></span>                           |
| <span data-ttu-id="b1c63-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b1c63-187">Is Indexed</span></span>             | <span data-ttu-id="b1c63-188">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-188">False</span></span>                           |
| <span data-ttu-id="b1c63-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b1c63-189">In Global Catalog</span></span>      | <span data-ttu-id="b1c63-190">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-190">False</span></span>                           |
| <span data-ttu-id="b1c63-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1c63-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1c63-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b1c63-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1c63-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1c63-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1c63-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1c63-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1c63-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1c63-195">Search-Flags</span></span>           | <span data-ttu-id="b1c63-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1c63-196">0x00000000</span></span>                      |
| <span data-ttu-id="b1c63-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1c63-197">System-Flags</span></span>           | <span data-ttu-id="b1c63-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b1c63-198">0x00000014</span></span>                      |
| <span data-ttu-id="b1c63-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b1c63-199">Classes used in</span></span>        | [<span data-ttu-id="b1c63-200">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b1c63-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b1c63-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1c63-201">Windows Server 2008</span></span>



| <span data-ttu-id="b1c63-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b1c63-202">Entry</span></span> | <span data-ttu-id="b1c63-203">Wert</span><span class="sxs-lookup"><span data-stu-id="b1c63-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1c63-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b1c63-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1c63-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1c63-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b1c63-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1c63-206">System-Only</span></span>            | <span data-ttu-id="b1c63-207">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-207">False</span></span>                           |
| <span data-ttu-id="b1c63-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b1c63-208">Is-Single-Valued</span></span>       | <span data-ttu-id="b1c63-209">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-209">False</span></span>                           |
| <span data-ttu-id="b1c63-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b1c63-210">Is Indexed</span></span>             | <span data-ttu-id="b1c63-211">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-211">False</span></span>                           |
| <span data-ttu-id="b1c63-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b1c63-212">In Global Catalog</span></span>      | <span data-ttu-id="b1c63-213">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-213">False</span></span>                           |
| <span data-ttu-id="b1c63-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1c63-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1c63-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b1c63-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1c63-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1c63-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1c63-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1c63-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1c63-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1c63-218">Search-Flags</span></span>           | <span data-ttu-id="b1c63-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1c63-219">0x00000000</span></span>                      |
| <span data-ttu-id="b1c63-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1c63-220">System-Flags</span></span>           | <span data-ttu-id="b1c63-221">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b1c63-221">0x00000014</span></span>                      |
| <span data-ttu-id="b1c63-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b1c63-222">Classes used in</span></span>        | [<span data-ttu-id="b1c63-223">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b1c63-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b1c63-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b1c63-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b1c63-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b1c63-225">Entry</span></span> | <span data-ttu-id="b1c63-226">Wert</span><span class="sxs-lookup"><span data-stu-id="b1c63-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1c63-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b1c63-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1c63-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1c63-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b1c63-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1c63-229">System-Only</span></span>            | <span data-ttu-id="b1c63-230">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-230">False</span></span>                           |
| <span data-ttu-id="b1c63-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b1c63-231">Is-Single-Valued</span></span>       | <span data-ttu-id="b1c63-232">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-232">False</span></span>                           |
| <span data-ttu-id="b1c63-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b1c63-233">Is Indexed</span></span>             | <span data-ttu-id="b1c63-234">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-234">False</span></span>                           |
| <span data-ttu-id="b1c63-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b1c63-235">In Global Catalog</span></span>      | <span data-ttu-id="b1c63-236">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-236">False</span></span>                           |
| <span data-ttu-id="b1c63-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1c63-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1c63-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b1c63-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1c63-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1c63-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1c63-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1c63-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1c63-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1c63-241">Search-Flags</span></span>           | <span data-ttu-id="b1c63-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1c63-242">0x00000000</span></span>                      |
| <span data-ttu-id="b1c63-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1c63-243">System-Flags</span></span>           | <span data-ttu-id="b1c63-244">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b1c63-244">0x00000014</span></span>                      |
| <span data-ttu-id="b1c63-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b1c63-245">Classes used in</span></span>        | [<span data-ttu-id="b1c63-246">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b1c63-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b1c63-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1c63-247">Windows Server 2012</span></span>



| <span data-ttu-id="b1c63-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b1c63-248">Entry</span></span> | <span data-ttu-id="b1c63-249">Wert</span><span class="sxs-lookup"><span data-stu-id="b1c63-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1c63-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b1c63-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1c63-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1c63-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b1c63-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1c63-252">System-Only</span></span>            | <span data-ttu-id="b1c63-253">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-253">False</span></span>                           |
| <span data-ttu-id="b1c63-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b1c63-254">Is-Single-Valued</span></span>       | <span data-ttu-id="b1c63-255">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-255">False</span></span>                           |
| <span data-ttu-id="b1c63-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b1c63-256">Is Indexed</span></span>             | <span data-ttu-id="b1c63-257">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-257">False</span></span>                           |
| <span data-ttu-id="b1c63-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b1c63-258">In Global Catalog</span></span>      | <span data-ttu-id="b1c63-259">False</span><span class="sxs-lookup"><span data-stu-id="b1c63-259">False</span></span>                           |
| <span data-ttu-id="b1c63-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1c63-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1c63-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b1c63-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1c63-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1c63-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1c63-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1c63-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1c63-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1c63-264">Search-Flags</span></span>           | <span data-ttu-id="b1c63-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1c63-265">0x00000000</span></span>                      |
| <span data-ttu-id="b1c63-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1c63-266">System-Flags</span></span>           | <span data-ttu-id="b1c63-267">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b1c63-267">0x00000014</span></span>                      |
| <span data-ttu-id="b1c63-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b1c63-268">Classes used in</span></span>        | [<span data-ttu-id="b1c63-269">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="b1c63-269">**Top**</span></span>](c-top.md)<br/> |



 

 





