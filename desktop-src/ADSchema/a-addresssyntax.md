---
title: Address-Syntax-Attribut
description: Eine Grammatik zum Codieren der Anzeige Tabellen Eigenschaften als Zeichenfolge.
ms.assetid: 809981da-8572-4a9f-a4c3-06cff95c8bdc
ms.tgt_platform: multiple
keywords:
- AD-Schema für Address-Syntax-Attribut
- addresssyntax-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Address-Syntax
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db7ae0a0d5a4672168329b546dd53c19697eec4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342898"
---
# <a name="address-syntax-attribute"></a><span data-ttu-id="27d7a-105">Address-Syntax-Attribut</span><span class="sxs-lookup"><span data-stu-id="27d7a-105">Address-Syntax attribute</span></span>

<span data-ttu-id="27d7a-106">Eine Grammatik zum Codieren der Anzeige Tabellen Eigenschaften als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="27d7a-106">A grammar for encoding the display table properties as a string.</span></span>



| <span data-ttu-id="27d7a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="27d7a-107">Entry</span></span> | <span data-ttu-id="27d7a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="27d7a-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="27d7a-109">CN</span><span class="sxs-lookup"><span data-stu-id="27d7a-109">CN</span></span>                | <span data-ttu-id="27d7a-110">Address-Syntax</span><span class="sxs-lookup"><span data-stu-id="27d7a-110">Address-Syntax</span></span>                                        |
| <span data-ttu-id="27d7a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="27d7a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="27d7a-112">addresssyntax</span><span class="sxs-lookup"><span data-stu-id="27d7a-112">addressSyntax</span></span>                                         |
| <span data-ttu-id="27d7a-113">Size</span><span class="sxs-lookup"><span data-stu-id="27d7a-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="27d7a-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="27d7a-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="27d7a-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="27d7a-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="27d7a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="27d7a-116">Attribute-Id</span></span>      | <span data-ttu-id="27d7a-117">1.2.840.113556.1.2.255</span><span class="sxs-lookup"><span data-stu-id="27d7a-117">1.2.840.113556.1.2.255</span></span>                                |
| <span data-ttu-id="27d7a-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="27d7a-118">System-Id-Guid</span></span>    | <span data-ttu-id="27d7a-119">5F d42463-1262-11D0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="27d7a-119">5fd42463-1262-11d0-a060-00aa006c33ed</span></span>                  |
| <span data-ttu-id="27d7a-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="27d7a-120">Syntax</span></span>            | [<span data-ttu-id="27d7a-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="27d7a-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="27d7a-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="27d7a-122">Implementations</span></span>

-   [<span data-ttu-id="27d7a-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="27d7a-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="27d7a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="27d7a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="27d7a-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="27d7a-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="27d7a-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="27d7a-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="27d7a-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="27d7a-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="27d7a-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="27d7a-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="27d7a-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27d7a-129">Windows 2000 Server</span></span>



| <span data-ttu-id="27d7a-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="27d7a-130">Entry</span></span> | <span data-ttu-id="27d7a-131">Wert</span><span class="sxs-lookup"><span data-stu-id="27d7a-131">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="27d7a-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="27d7a-132">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="27d7a-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d7a-133">MAPI-Id</span></span>                | <span data-ttu-id="27d7a-134">0x8018</span><span class="sxs-lookup"><span data-stu-id="27d7a-134">0x8018</span></span>                                                   |
| <span data-ttu-id="27d7a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d7a-135">System-Only</span></span>            | <span data-ttu-id="27d7a-136">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-136">False</span></span>                                                    |
| <span data-ttu-id="27d7a-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="27d7a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="27d7a-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="27d7a-138">True</span></span>                                                     |
| <span data-ttu-id="27d7a-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="27d7a-139">Is Indexed</span></span>             | <span data-ttu-id="27d7a-140">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-140">False</span></span>                                                    |
| <span data-ttu-id="27d7a-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="27d7a-141">In Global Catalog</span></span>      | <span data-ttu-id="27d7a-142">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-142">False</span></span>                                                    |
| <span data-ttu-id="27d7a-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27d7a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d7a-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="27d7a-144">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="27d7a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d7a-145">Range-Lower</span></span>            | <span data-ttu-id="27d7a-146">1</span><span class="sxs-lookup"><span data-stu-id="27d7a-146">1</span></span>                                                        |
| <span data-ttu-id="27d7a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d7a-147">Range-Upper</span></span>            | <span data-ttu-id="27d7a-148">4096</span><span class="sxs-lookup"><span data-stu-id="27d7a-148">4096</span></span>                                                     |
| <span data-ttu-id="27d7a-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d7a-149">Search-Flags</span></span>           | <span data-ttu-id="27d7a-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d7a-150">0x00000000</span></span>                                               |
| <span data-ttu-id="27d7a-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d7a-151">System-Flags</span></span>           | <span data-ttu-id="27d7a-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27d7a-152">0x00000010</span></span>                                               |
| <span data-ttu-id="27d7a-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="27d7a-153">Classes used in</span></span>        | [<span data-ttu-id="27d7a-154">**Address-Template**</span><span class="sxs-lookup"><span data-stu-id="27d7a-154">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="27d7a-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27d7a-155">Windows Server 2003</span></span>



| <span data-ttu-id="27d7a-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="27d7a-156">Entry</span></span> | <span data-ttu-id="27d7a-157">Wert</span><span class="sxs-lookup"><span data-stu-id="27d7a-157">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="27d7a-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="27d7a-158">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="27d7a-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d7a-159">MAPI-Id</span></span>                | <span data-ttu-id="27d7a-160">0x8018</span><span class="sxs-lookup"><span data-stu-id="27d7a-160">0x8018</span></span>                                                   |
| <span data-ttu-id="27d7a-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d7a-161">System-Only</span></span>            | <span data-ttu-id="27d7a-162">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-162">False</span></span>                                                    |
| <span data-ttu-id="27d7a-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="27d7a-163">Is-Single-Valued</span></span>       | <span data-ttu-id="27d7a-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="27d7a-164">True</span></span>                                                     |
| <span data-ttu-id="27d7a-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="27d7a-165">Is Indexed</span></span>             | <span data-ttu-id="27d7a-166">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-166">False</span></span>                                                    |
| <span data-ttu-id="27d7a-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="27d7a-167">In Global Catalog</span></span>      | <span data-ttu-id="27d7a-168">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-168">False</span></span>                                                    |
| <span data-ttu-id="27d7a-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27d7a-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d7a-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="27d7a-170">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="27d7a-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d7a-171">Range-Lower</span></span>            | <span data-ttu-id="27d7a-172">1</span><span class="sxs-lookup"><span data-stu-id="27d7a-172">1</span></span>                                                        |
| <span data-ttu-id="27d7a-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d7a-173">Range-Upper</span></span>            | <span data-ttu-id="27d7a-174">4096</span><span class="sxs-lookup"><span data-stu-id="27d7a-174">4096</span></span>                                                     |
| <span data-ttu-id="27d7a-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d7a-175">Search-Flags</span></span>           | <span data-ttu-id="27d7a-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d7a-176">0x00000000</span></span>                                               |
| <span data-ttu-id="27d7a-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d7a-177">System-Flags</span></span>           | <span data-ttu-id="27d7a-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27d7a-178">0x00000010</span></span>                                               |
| <span data-ttu-id="27d7a-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="27d7a-179">Classes used in</span></span>        | [<span data-ttu-id="27d7a-180">**Address-Template**</span><span class="sxs-lookup"><span data-stu-id="27d7a-180">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="27d7a-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="27d7a-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="27d7a-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="27d7a-182">Entry</span></span> | <span data-ttu-id="27d7a-183">Wert</span><span class="sxs-lookup"><span data-stu-id="27d7a-183">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="27d7a-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="27d7a-184">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="27d7a-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d7a-185">MAPI-Id</span></span>                | <span data-ttu-id="27d7a-186">0x8018</span><span class="sxs-lookup"><span data-stu-id="27d7a-186">0x8018</span></span>                                                   |
| <span data-ttu-id="27d7a-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d7a-187">System-Only</span></span>            | <span data-ttu-id="27d7a-188">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-188">False</span></span>                                                    |
| <span data-ttu-id="27d7a-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="27d7a-189">Is-Single-Valued</span></span>       | <span data-ttu-id="27d7a-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="27d7a-190">True</span></span>                                                     |
| <span data-ttu-id="27d7a-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="27d7a-191">Is Indexed</span></span>             | <span data-ttu-id="27d7a-192">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-192">False</span></span>                                                    |
| <span data-ttu-id="27d7a-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="27d7a-193">In Global Catalog</span></span>      | <span data-ttu-id="27d7a-194">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-194">False</span></span>                                                    |
| <span data-ttu-id="27d7a-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27d7a-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d7a-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="27d7a-196">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="27d7a-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d7a-197">Range-Lower</span></span>            | <span data-ttu-id="27d7a-198">1</span><span class="sxs-lookup"><span data-stu-id="27d7a-198">1</span></span>                                                        |
| <span data-ttu-id="27d7a-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d7a-199">Range-Upper</span></span>            | <span data-ttu-id="27d7a-200">4096</span><span class="sxs-lookup"><span data-stu-id="27d7a-200">4096</span></span>                                                     |
| <span data-ttu-id="27d7a-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d7a-201">Search-Flags</span></span>           | <span data-ttu-id="27d7a-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d7a-202">0x00000000</span></span>                                               |
| <span data-ttu-id="27d7a-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d7a-203">System-Flags</span></span>           | <span data-ttu-id="27d7a-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27d7a-204">0x00000010</span></span>                                               |
| <span data-ttu-id="27d7a-205">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="27d7a-205">Classes used in</span></span>        | [<span data-ttu-id="27d7a-206">**Address-Template**</span><span class="sxs-lookup"><span data-stu-id="27d7a-206">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="27d7a-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27d7a-207">Windows Server 2008</span></span>



| <span data-ttu-id="27d7a-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="27d7a-208">Entry</span></span> | <span data-ttu-id="27d7a-209">Wert</span><span class="sxs-lookup"><span data-stu-id="27d7a-209">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="27d7a-210">Link-ID</span><span class="sxs-lookup"><span data-stu-id="27d7a-210">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="27d7a-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d7a-211">MAPI-Id</span></span>                | <span data-ttu-id="27d7a-212">0x8018</span><span class="sxs-lookup"><span data-stu-id="27d7a-212">0x8018</span></span>                                                   |
| <span data-ttu-id="27d7a-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d7a-213">System-Only</span></span>            | <span data-ttu-id="27d7a-214">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-214">False</span></span>                                                    |
| <span data-ttu-id="27d7a-215">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="27d7a-215">Is-Single-Valued</span></span>       | <span data-ttu-id="27d7a-216">Richtig</span><span class="sxs-lookup"><span data-stu-id="27d7a-216">True</span></span>                                                     |
| <span data-ttu-id="27d7a-217">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="27d7a-217">Is Indexed</span></span>             | <span data-ttu-id="27d7a-218">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-218">False</span></span>                                                    |
| <span data-ttu-id="27d7a-219">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="27d7a-219">In Global Catalog</span></span>      | <span data-ttu-id="27d7a-220">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-220">False</span></span>                                                    |
| <span data-ttu-id="27d7a-221">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27d7a-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d7a-222">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="27d7a-222">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="27d7a-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d7a-223">Range-Lower</span></span>            | <span data-ttu-id="27d7a-224">1</span><span class="sxs-lookup"><span data-stu-id="27d7a-224">1</span></span>                                                        |
| <span data-ttu-id="27d7a-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d7a-225">Range-Upper</span></span>            | <span data-ttu-id="27d7a-226">4096</span><span class="sxs-lookup"><span data-stu-id="27d7a-226">4096</span></span>                                                     |
| <span data-ttu-id="27d7a-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d7a-227">Search-Flags</span></span>           | <span data-ttu-id="27d7a-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d7a-228">0x00000000</span></span>                                               |
| <span data-ttu-id="27d7a-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d7a-229">System-Flags</span></span>           | <span data-ttu-id="27d7a-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27d7a-230">0x00000010</span></span>                                               |
| <span data-ttu-id="27d7a-231">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="27d7a-231">Classes used in</span></span>        | [<span data-ttu-id="27d7a-232">**Address-Template**</span><span class="sxs-lookup"><span data-stu-id="27d7a-232">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="27d7a-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="27d7a-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="27d7a-234">Eingabe</span><span class="sxs-lookup"><span data-stu-id="27d7a-234">Entry</span></span> | <span data-ttu-id="27d7a-235">Wert</span><span class="sxs-lookup"><span data-stu-id="27d7a-235">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="27d7a-236">Link-ID</span><span class="sxs-lookup"><span data-stu-id="27d7a-236">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="27d7a-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d7a-237">MAPI-Id</span></span>                | <span data-ttu-id="27d7a-238">0x8018</span><span class="sxs-lookup"><span data-stu-id="27d7a-238">0x8018</span></span>                                                   |
| <span data-ttu-id="27d7a-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d7a-239">System-Only</span></span>            | <span data-ttu-id="27d7a-240">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-240">False</span></span>                                                    |
| <span data-ttu-id="27d7a-241">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="27d7a-241">Is-Single-Valued</span></span>       | <span data-ttu-id="27d7a-242">Richtig</span><span class="sxs-lookup"><span data-stu-id="27d7a-242">True</span></span>                                                     |
| <span data-ttu-id="27d7a-243">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="27d7a-243">Is Indexed</span></span>             | <span data-ttu-id="27d7a-244">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-244">False</span></span>                                                    |
| <span data-ttu-id="27d7a-245">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="27d7a-245">In Global Catalog</span></span>      | <span data-ttu-id="27d7a-246">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-246">False</span></span>                                                    |
| <span data-ttu-id="27d7a-247">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27d7a-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d7a-248">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="27d7a-248">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="27d7a-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d7a-249">Range-Lower</span></span>            | <span data-ttu-id="27d7a-250">1</span><span class="sxs-lookup"><span data-stu-id="27d7a-250">1</span></span>                                                        |
| <span data-ttu-id="27d7a-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d7a-251">Range-Upper</span></span>            | <span data-ttu-id="27d7a-252">4096</span><span class="sxs-lookup"><span data-stu-id="27d7a-252">4096</span></span>                                                     |
| <span data-ttu-id="27d7a-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d7a-253">Search-Flags</span></span>           | <span data-ttu-id="27d7a-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d7a-254">0x00000000</span></span>                                               |
| <span data-ttu-id="27d7a-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d7a-255">System-Flags</span></span>           | <span data-ttu-id="27d7a-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27d7a-256">0x00000010</span></span>                                               |
| <span data-ttu-id="27d7a-257">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="27d7a-257">Classes used in</span></span>        | [<span data-ttu-id="27d7a-258">**Address-Template**</span><span class="sxs-lookup"><span data-stu-id="27d7a-258">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="27d7a-259">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27d7a-259">Windows Server 2012</span></span>



| <span data-ttu-id="27d7a-260">Eingabe</span><span class="sxs-lookup"><span data-stu-id="27d7a-260">Entry</span></span> | <span data-ttu-id="27d7a-261">Wert</span><span class="sxs-lookup"><span data-stu-id="27d7a-261">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="27d7a-262">Link-ID</span><span class="sxs-lookup"><span data-stu-id="27d7a-262">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="27d7a-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d7a-263">MAPI-Id</span></span>                | <span data-ttu-id="27d7a-264">0x8018</span><span class="sxs-lookup"><span data-stu-id="27d7a-264">0x8018</span></span>                                                   |
| <span data-ttu-id="27d7a-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d7a-265">System-Only</span></span>            | <span data-ttu-id="27d7a-266">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-266">False</span></span>                                                    |
| <span data-ttu-id="27d7a-267">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="27d7a-267">Is-Single-Valued</span></span>       | <span data-ttu-id="27d7a-268">Richtig</span><span class="sxs-lookup"><span data-stu-id="27d7a-268">True</span></span>                                                     |
| <span data-ttu-id="27d7a-269">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="27d7a-269">Is Indexed</span></span>             | <span data-ttu-id="27d7a-270">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-270">False</span></span>                                                    |
| <span data-ttu-id="27d7a-271">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="27d7a-271">In Global Catalog</span></span>      | <span data-ttu-id="27d7a-272">False</span><span class="sxs-lookup"><span data-stu-id="27d7a-272">False</span></span>                                                    |
| <span data-ttu-id="27d7a-273">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27d7a-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d7a-274">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="27d7a-274">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="27d7a-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d7a-275">Range-Lower</span></span>            | <span data-ttu-id="27d7a-276">1</span><span class="sxs-lookup"><span data-stu-id="27d7a-276">1</span></span>                                                        |
| <span data-ttu-id="27d7a-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d7a-277">Range-Upper</span></span>            | <span data-ttu-id="27d7a-278">4096</span><span class="sxs-lookup"><span data-stu-id="27d7a-278">4096</span></span>                                                     |
| <span data-ttu-id="27d7a-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d7a-279">Search-Flags</span></span>           | <span data-ttu-id="27d7a-280">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d7a-280">0x00000000</span></span>                                               |
| <span data-ttu-id="27d7a-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d7a-281">System-Flags</span></span>           | <span data-ttu-id="27d7a-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27d7a-282">0x00000010</span></span>                                               |
| <span data-ttu-id="27d7a-283">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="27d7a-283">Classes used in</span></span>        | [<span data-ttu-id="27d7a-284">**Address-Template**</span><span class="sxs-lookup"><span data-stu-id="27d7a-284">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



 

 





