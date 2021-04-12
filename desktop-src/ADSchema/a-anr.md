---
title: ANR-Attribut
description: Mehrdeutiges namens Auflösungs Attribut, das bei der Auswahl zwischen Objekten verwendet werden soll.
ms.assetid: 9057dc7e-f669-4821-86b0-703ff7e5b120
ms.tgt_platform: multiple
keywords:
- AD-Schema für ANR-Attribut
- AD-Schema für ANR-Attribut
topic_type:
- apiref
api_name:
- ANR
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28efc6d6871eb737f9c1953fbdb5ad5798f7fd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480487"
---
# <a name="anr-attribute"></a><span data-ttu-id="7fd82-105">ANR-Attribut</span><span class="sxs-lookup"><span data-stu-id="7fd82-105">ANR attribute</span></span>

<span data-ttu-id="7fd82-106">Mehrdeutiges namens Auflösungs Attribut, das bei der Auswahl zwischen Objekten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7fd82-106">Ambiguous name resolution attribute to be used when choosing between objects.</span></span>



| <span data-ttu-id="7fd82-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7fd82-107">Entry</span></span> | <span data-ttu-id="7fd82-108">Wert</span><span class="sxs-lookup"><span data-stu-id="7fd82-108">Value</span></span> |
|-------------------|-------------------------------------------------------------------|
| <span data-ttu-id="7fd82-109">CN</span><span class="sxs-lookup"><span data-stu-id="7fd82-109">CN</span></span>                | <span data-ttu-id="7fd82-110">ANR</span><span class="sxs-lookup"><span data-stu-id="7fd82-110">ANR</span></span>                                                               |
| <span data-ttu-id="7fd82-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7fd82-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7fd82-112">aNR</span><span class="sxs-lookup"><span data-stu-id="7fd82-112">aNR</span></span>                                                               |
| <span data-ttu-id="7fd82-113">Size</span><span class="sxs-lookup"><span data-stu-id="7fd82-113">Size</span></span>              | \-                                                                |
| <span data-ttu-id="7fd82-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="7fd82-114">Update Privilege</span></span>  | <span data-ttu-id="7fd82-115">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="7fd82-115">Schema administrator</span></span>                                              |
| <span data-ttu-id="7fd82-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="7fd82-116">Update Frequency</span></span>  | <span data-ttu-id="7fd82-117">Wenn ein Attribut hinzugefügt oder aus der ANR-Liste entfernt werden muss.</span><span class="sxs-lookup"><span data-stu-id="7fd82-117">When an attribute needs to be added or removed from the ANR list.</span></span> |
| <span data-ttu-id="7fd82-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7fd82-118">Attribute-Id</span></span>      | <span data-ttu-id="7fd82-119">1.2.840.113556.1.4.1208</span><span class="sxs-lookup"><span data-stu-id="7fd82-119">1.2.840.113556.1.4.1208</span></span>                                           |
| <span data-ttu-id="7fd82-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7fd82-120">System-Id-Guid</span></span>    | <span data-ttu-id="7fd82-121">45b01500-c419-11d1-bbc9-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="7fd82-121">45b01500-c419-11d1-bbc9-0080c76670c0</span></span>                              |
| <span data-ttu-id="7fd82-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fd82-122">Syntax</span></span>            | [<span data-ttu-id="7fd82-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7fd82-123">**String(Unicode)**</span></span>](s-string-unicode.md)                       |



## <a name="implementations"></a><span data-ttu-id="7fd82-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="7fd82-124">Implementations</span></span>

-   [<span data-ttu-id="7fd82-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7fd82-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7fd82-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7fd82-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7fd82-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="7fd82-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7fd82-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7fd82-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7fd82-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7fd82-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7fd82-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7fd82-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7fd82-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7fd82-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7fd82-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7fd82-132">Windows 2000 Server</span></span>



| <span data-ttu-id="7fd82-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7fd82-133">Entry</span></span> | <span data-ttu-id="7fd82-134">Wert</span><span class="sxs-lookup"><span data-stu-id="7fd82-134">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="7fd82-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7fd82-135">Link-Id</span></span>                | \-           |
| <span data-ttu-id="7fd82-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fd82-136">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="7fd82-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fd82-137">System-Only</span></span>            | <span data-ttu-id="7fd82-138">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-138">False</span></span>        |
| <span data-ttu-id="7fd82-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7fd82-139">Is-Single-Valued</span></span>       | <span data-ttu-id="7fd82-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="7fd82-140">True</span></span>         |
| <span data-ttu-id="7fd82-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7fd82-141">Is Indexed</span></span>             | <span data-ttu-id="7fd82-142">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-142">False</span></span>        |
| <span data-ttu-id="7fd82-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7fd82-143">In Global Catalog</span></span>      | <span data-ttu-id="7fd82-144">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-144">False</span></span>        |
| <span data-ttu-id="7fd82-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7fd82-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fd82-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7fd82-146">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="7fd82-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fd82-147">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="7fd82-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fd82-148">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="7fd82-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd82-149">Search-Flags</span></span>           | <span data-ttu-id="7fd82-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7fd82-150">0x00000000</span></span>   |
| <span data-ttu-id="7fd82-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd82-151">System-Flags</span></span>           | <span data-ttu-id="7fd82-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7fd82-152">0x08000014</span></span>   |
| <span data-ttu-id="7fd82-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7fd82-153">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="7fd82-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7fd82-154">Windows Server 2003</span></span>



| <span data-ttu-id="7fd82-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7fd82-155">Entry</span></span> | <span data-ttu-id="7fd82-156">Wert</span><span class="sxs-lookup"><span data-stu-id="7fd82-156">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="7fd82-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7fd82-157">Link-Id</span></span>                | \-           |
| <span data-ttu-id="7fd82-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fd82-158">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="7fd82-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fd82-159">System-Only</span></span>            | <span data-ttu-id="7fd82-160">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-160">False</span></span>        |
| <span data-ttu-id="7fd82-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7fd82-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7fd82-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="7fd82-162">True</span></span>         |
| <span data-ttu-id="7fd82-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7fd82-163">Is Indexed</span></span>             | <span data-ttu-id="7fd82-164">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-164">False</span></span>        |
| <span data-ttu-id="7fd82-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7fd82-165">In Global Catalog</span></span>      | <span data-ttu-id="7fd82-166">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-166">False</span></span>        |
| <span data-ttu-id="7fd82-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7fd82-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fd82-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7fd82-168">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="7fd82-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fd82-169">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="7fd82-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fd82-170">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="7fd82-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd82-171">Search-Flags</span></span>           | <span data-ttu-id="7fd82-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7fd82-172">0x00000000</span></span>   |
| <span data-ttu-id="7fd82-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd82-173">System-Flags</span></span>           | <span data-ttu-id="7fd82-174">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7fd82-174">0x08000014</span></span>   |
| <span data-ttu-id="7fd82-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7fd82-175">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="7fd82-176">Adam</span><span class="sxs-lookup"><span data-stu-id="7fd82-176">ADAM</span></span>



| <span data-ttu-id="7fd82-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7fd82-177">Entry</span></span> | <span data-ttu-id="7fd82-178">Wert</span><span class="sxs-lookup"><span data-stu-id="7fd82-178">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="7fd82-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7fd82-179">Link-Id</span></span>                | \-           |
| <span data-ttu-id="7fd82-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fd82-180">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="7fd82-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fd82-181">System-Only</span></span>            | <span data-ttu-id="7fd82-182">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-182">False</span></span>        |
| <span data-ttu-id="7fd82-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7fd82-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7fd82-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="7fd82-184">True</span></span>         |
| <span data-ttu-id="7fd82-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7fd82-185">Is Indexed</span></span>             | <span data-ttu-id="7fd82-186">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-186">False</span></span>        |
| <span data-ttu-id="7fd82-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7fd82-187">In Global Catalog</span></span>      | <span data-ttu-id="7fd82-188">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-188">False</span></span>        |
| <span data-ttu-id="7fd82-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7fd82-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fd82-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7fd82-190">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="7fd82-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fd82-191">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="7fd82-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fd82-192">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="7fd82-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd82-193">Search-Flags</span></span>           | <span data-ttu-id="7fd82-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7fd82-194">0x00000000</span></span>   |
| <span data-ttu-id="7fd82-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd82-195">System-Flags</span></span>           | <span data-ttu-id="7fd82-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7fd82-196">0x08000014</span></span>   |
| <span data-ttu-id="7fd82-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7fd82-197">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7fd82-198">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7fd82-198">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7fd82-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7fd82-199">Entry</span></span> | <span data-ttu-id="7fd82-200">Wert</span><span class="sxs-lookup"><span data-stu-id="7fd82-200">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="7fd82-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7fd82-201">Link-Id</span></span>                | \-           |
| <span data-ttu-id="7fd82-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fd82-202">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="7fd82-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fd82-203">System-Only</span></span>            | <span data-ttu-id="7fd82-204">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-204">False</span></span>        |
| <span data-ttu-id="7fd82-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7fd82-205">Is-Single-Valued</span></span>       | <span data-ttu-id="7fd82-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="7fd82-206">True</span></span>         |
| <span data-ttu-id="7fd82-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7fd82-207">Is Indexed</span></span>             | <span data-ttu-id="7fd82-208">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-208">False</span></span>        |
| <span data-ttu-id="7fd82-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7fd82-209">In Global Catalog</span></span>      | <span data-ttu-id="7fd82-210">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-210">False</span></span>        |
| <span data-ttu-id="7fd82-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7fd82-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fd82-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7fd82-212">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="7fd82-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fd82-213">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="7fd82-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fd82-214">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="7fd82-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd82-215">Search-Flags</span></span>           | <span data-ttu-id="7fd82-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7fd82-216">0x00000000</span></span>   |
| <span data-ttu-id="7fd82-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd82-217">System-Flags</span></span>           | <span data-ttu-id="7fd82-218">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7fd82-218">0x08000014</span></span>   |
| <span data-ttu-id="7fd82-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7fd82-219">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="7fd82-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fd82-220">Windows Server 2008</span></span>



| <span data-ttu-id="7fd82-221">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7fd82-221">Entry</span></span> | <span data-ttu-id="7fd82-222">Wert</span><span class="sxs-lookup"><span data-stu-id="7fd82-222">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="7fd82-223">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7fd82-223">Link-Id</span></span>                | \-           |
| <span data-ttu-id="7fd82-224">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fd82-224">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="7fd82-225">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fd82-225">System-Only</span></span>            | <span data-ttu-id="7fd82-226">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-226">False</span></span>        |
| <span data-ttu-id="7fd82-227">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7fd82-227">Is-Single-Valued</span></span>       | <span data-ttu-id="7fd82-228">Richtig</span><span class="sxs-lookup"><span data-stu-id="7fd82-228">True</span></span>         |
| <span data-ttu-id="7fd82-229">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7fd82-229">Is Indexed</span></span>             | <span data-ttu-id="7fd82-230">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-230">False</span></span>        |
| <span data-ttu-id="7fd82-231">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7fd82-231">In Global Catalog</span></span>      | <span data-ttu-id="7fd82-232">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-232">False</span></span>        |
| <span data-ttu-id="7fd82-233">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7fd82-233">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fd82-234">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7fd82-234">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="7fd82-235">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fd82-235">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="7fd82-236">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fd82-236">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="7fd82-237">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd82-237">Search-Flags</span></span>           | <span data-ttu-id="7fd82-238">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7fd82-238">0x00000000</span></span>   |
| <span data-ttu-id="7fd82-239">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd82-239">System-Flags</span></span>           | <span data-ttu-id="7fd82-240">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7fd82-240">0x08000014</span></span>   |
| <span data-ttu-id="7fd82-241">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7fd82-241">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7fd82-242">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7fd82-242">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7fd82-243">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7fd82-243">Entry</span></span> | <span data-ttu-id="7fd82-244">Wert</span><span class="sxs-lookup"><span data-stu-id="7fd82-244">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="7fd82-245">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7fd82-245">Link-Id</span></span>                | \-           |
| <span data-ttu-id="7fd82-246">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fd82-246">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="7fd82-247">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fd82-247">System-Only</span></span>            | <span data-ttu-id="7fd82-248">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-248">False</span></span>        |
| <span data-ttu-id="7fd82-249">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7fd82-249">Is-Single-Valued</span></span>       | <span data-ttu-id="7fd82-250">Richtig</span><span class="sxs-lookup"><span data-stu-id="7fd82-250">True</span></span>         |
| <span data-ttu-id="7fd82-251">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7fd82-251">Is Indexed</span></span>             | <span data-ttu-id="7fd82-252">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-252">False</span></span>        |
| <span data-ttu-id="7fd82-253">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7fd82-253">In Global Catalog</span></span>      | <span data-ttu-id="7fd82-254">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-254">False</span></span>        |
| <span data-ttu-id="7fd82-255">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7fd82-255">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fd82-256">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7fd82-256">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="7fd82-257">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fd82-257">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="7fd82-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fd82-258">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="7fd82-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd82-259">Search-Flags</span></span>           | <span data-ttu-id="7fd82-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7fd82-260">0x00000000</span></span>   |
| <span data-ttu-id="7fd82-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd82-261">System-Flags</span></span>           | <span data-ttu-id="7fd82-262">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7fd82-262">0x08000014</span></span>   |
| <span data-ttu-id="7fd82-263">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7fd82-263">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="7fd82-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7fd82-264">Windows Server 2012</span></span>



| <span data-ttu-id="7fd82-265">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7fd82-265">Entry</span></span> | <span data-ttu-id="7fd82-266">Wert</span><span class="sxs-lookup"><span data-stu-id="7fd82-266">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="7fd82-267">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7fd82-267">Link-Id</span></span>                | \-           |
| <span data-ttu-id="7fd82-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fd82-268">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="7fd82-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fd82-269">System-Only</span></span>            | <span data-ttu-id="7fd82-270">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-270">False</span></span>        |
| <span data-ttu-id="7fd82-271">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7fd82-271">Is-Single-Valued</span></span>       | <span data-ttu-id="7fd82-272">Richtig</span><span class="sxs-lookup"><span data-stu-id="7fd82-272">True</span></span>         |
| <span data-ttu-id="7fd82-273">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7fd82-273">Is Indexed</span></span>             | <span data-ttu-id="7fd82-274">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-274">False</span></span>        |
| <span data-ttu-id="7fd82-275">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7fd82-275">In Global Catalog</span></span>      | <span data-ttu-id="7fd82-276">False</span><span class="sxs-lookup"><span data-stu-id="7fd82-276">False</span></span>        |
| <span data-ttu-id="7fd82-277">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7fd82-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fd82-278">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7fd82-278">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="7fd82-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fd82-279">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="7fd82-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fd82-280">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="7fd82-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd82-281">Search-Flags</span></span>           | <span data-ttu-id="7fd82-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7fd82-282">0x00000000</span></span>   |
| <span data-ttu-id="7fd82-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd82-283">System-Flags</span></span>           | <span data-ttu-id="7fd82-284">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7fd82-284">0x08000014</span></span>   |
| <span data-ttu-id="7fd82-285">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7fd82-285">Classes used in</span></span>        | \-           |



 

 




