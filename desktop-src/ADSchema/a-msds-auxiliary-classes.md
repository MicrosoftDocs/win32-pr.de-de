---
title: ms-DS-hilfclasses-Attribut
description: Dieses Attribut listet die Erweiterungs Klassen auf, die dynamisch an ein-Objekt angefügt wurden. Dieses Attribut ist keiner Klasse zugeordnet. Sie wird automatisch vom System aufgefüllt.
ms.assetid: bf41f15d-9af9-43de-8425-33d50880c3fa
ms.tgt_platform: multiple
keywords:
- AD-Schema für das Attribut "ms-DS-hilfclasses"
- AD-Schema für MSDS-hilfclasses-Attribut
topic_type:
- apiref
api_name:
- ms-DS-Auxiliary-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24608d0626ae4bcd6adb70a646d95121615c29e5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859699"
---
# <a name="ms-ds-auxiliary-classes-attribute"></a><span data-ttu-id="b1486-107">ms-DS-hilfclasses-Attribut</span><span class="sxs-lookup"><span data-stu-id="b1486-107">ms-DS-Auxiliary-Classes attribute</span></span>

<span data-ttu-id="b1486-108">Dieses Attribut listet die Erweiterungs Klassen auf, die dynamisch an ein-Objekt angefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="b1486-108">This attribute lists the auxiliary classes that have been dynamically attached to an object.</span></span> <span data-ttu-id="b1486-109">Dieses Attribut ist keiner Klasse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b1486-109">This attribute is not associated with a class.</span></span> <span data-ttu-id="b1486-110">Sie wird automatisch vom System aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="b1486-110">It is automatically populated by the system.</span></span>



| <span data-ttu-id="b1486-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b1486-111">Entry</span></span> | <span data-ttu-id="b1486-112">Wert</span><span class="sxs-lookup"><span data-stu-id="b1486-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b1486-113">CN</span><span class="sxs-lookup"><span data-stu-id="b1486-113">CN</span></span>                | <span data-ttu-id="b1486-114">ms-DS-Hilfsklassen</span><span class="sxs-lookup"><span data-stu-id="b1486-114">ms-DS-Auxiliary-Classes</span></span>                                         |
| <span data-ttu-id="b1486-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b1486-115">Ldap-Display-Name</span></span> | <span data-ttu-id="b1486-116">MSDS-Hilfssysteme</span><span class="sxs-lookup"><span data-stu-id="b1486-116">msDS-Auxiliary-Classes</span></span>                                          |
| <span data-ttu-id="b1486-117">Size</span><span class="sxs-lookup"><span data-stu-id="b1486-117">Size</span></span>              | \-                                                              |
| <span data-ttu-id="b1486-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b1486-118">Update Privilege</span></span>  | <span data-ttu-id="b1486-119">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1486-119">This value is set by the system.</span></span>                                |
| <span data-ttu-id="b1486-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b1486-120">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="b1486-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b1486-121">Attribute-Id</span></span>      | <span data-ttu-id="b1486-122">1.2.840.113556.1.4.1458</span><span class="sxs-lookup"><span data-stu-id="b1486-122">1.2.840.113556.1.4.1458</span></span>                                         |
| <span data-ttu-id="b1486-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b1486-123">System-Id-Guid</span></span>    | <span data-ttu-id="b1486-124">c4af1073-ee50-4be0-b8c0-89a41fe99abe</span><span class="sxs-lookup"><span data-stu-id="b1486-124">c4af1073-ee50-4be0-b8c0-89a41fe99abe</span></span>                            |
| <span data-ttu-id="b1486-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1486-125">Syntax</span></span>            | [<span data-ttu-id="b1486-126">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="b1486-126">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="b1486-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b1486-127">Implementations</span></span>

-   [<span data-ttu-id="b1486-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b1486-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b1486-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="b1486-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b1486-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b1486-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b1486-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b1486-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b1486-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b1486-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b1486-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b1486-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b1486-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1486-134">Windows Server 2003</span></span>



| <span data-ttu-id="b1486-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b1486-135">Entry</span></span> | <span data-ttu-id="b1486-136">Wert</span><span class="sxs-lookup"><span data-stu-id="b1486-136">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b1486-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b1486-137">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b1486-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1486-138">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b1486-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1486-139">System-Only</span></span>            | <span data-ttu-id="b1486-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="b1486-140">True</span></span>         |
| <span data-ttu-id="b1486-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b1486-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b1486-142">False</span><span class="sxs-lookup"><span data-stu-id="b1486-142">False</span></span>        |
| <span data-ttu-id="b1486-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b1486-143">Is Indexed</span></span>             | <span data-ttu-id="b1486-144">False</span><span class="sxs-lookup"><span data-stu-id="b1486-144">False</span></span>        |
| <span data-ttu-id="b1486-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b1486-145">In Global Catalog</span></span>      | <span data-ttu-id="b1486-146">False</span><span class="sxs-lookup"><span data-stu-id="b1486-146">False</span></span>        |
| <span data-ttu-id="b1486-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1486-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1486-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b1486-148">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b1486-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1486-149">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b1486-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1486-150">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b1486-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1486-151">Search-Flags</span></span>           | <span data-ttu-id="b1486-152">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b1486-152">0x00000008</span></span>   |
| <span data-ttu-id="b1486-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1486-153">System-Flags</span></span>           | <span data-ttu-id="b1486-154">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b1486-154">0x00000014</span></span>   |
| <span data-ttu-id="b1486-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b1486-155">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="b1486-156">Adam</span><span class="sxs-lookup"><span data-stu-id="b1486-156">ADAM</span></span>



| <span data-ttu-id="b1486-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b1486-157">Entry</span></span> | <span data-ttu-id="b1486-158">Wert</span><span class="sxs-lookup"><span data-stu-id="b1486-158">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b1486-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b1486-159">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b1486-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1486-160">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b1486-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1486-161">System-Only</span></span>            | <span data-ttu-id="b1486-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="b1486-162">True</span></span>         |
| <span data-ttu-id="b1486-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b1486-163">Is-Single-Valued</span></span>       | <span data-ttu-id="b1486-164">False</span><span class="sxs-lookup"><span data-stu-id="b1486-164">False</span></span>        |
| <span data-ttu-id="b1486-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b1486-165">Is Indexed</span></span>             | <span data-ttu-id="b1486-166">False</span><span class="sxs-lookup"><span data-stu-id="b1486-166">False</span></span>        |
| <span data-ttu-id="b1486-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b1486-167">In Global Catalog</span></span>      | <span data-ttu-id="b1486-168">False</span><span class="sxs-lookup"><span data-stu-id="b1486-168">False</span></span>        |
| <span data-ttu-id="b1486-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1486-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1486-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b1486-170">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b1486-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1486-171">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b1486-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1486-172">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b1486-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1486-173">Search-Flags</span></span>           | <span data-ttu-id="b1486-174">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b1486-174">0x00000008</span></span>   |
| <span data-ttu-id="b1486-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1486-175">System-Flags</span></span>           | <span data-ttu-id="b1486-176">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b1486-176">0x00000014</span></span>   |
| <span data-ttu-id="b1486-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b1486-177">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b1486-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b1486-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b1486-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b1486-179">Entry</span></span> | <span data-ttu-id="b1486-180">Wert</span><span class="sxs-lookup"><span data-stu-id="b1486-180">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b1486-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b1486-181">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b1486-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1486-182">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b1486-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1486-183">System-Only</span></span>            | <span data-ttu-id="b1486-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="b1486-184">True</span></span>         |
| <span data-ttu-id="b1486-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b1486-185">Is-Single-Valued</span></span>       | <span data-ttu-id="b1486-186">False</span><span class="sxs-lookup"><span data-stu-id="b1486-186">False</span></span>        |
| <span data-ttu-id="b1486-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b1486-187">Is Indexed</span></span>             | <span data-ttu-id="b1486-188">False</span><span class="sxs-lookup"><span data-stu-id="b1486-188">False</span></span>        |
| <span data-ttu-id="b1486-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b1486-189">In Global Catalog</span></span>      | <span data-ttu-id="b1486-190">False</span><span class="sxs-lookup"><span data-stu-id="b1486-190">False</span></span>        |
| <span data-ttu-id="b1486-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1486-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1486-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b1486-192">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b1486-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1486-193">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b1486-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1486-194">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b1486-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1486-195">Search-Flags</span></span>           | <span data-ttu-id="b1486-196">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b1486-196">0x00000008</span></span>   |
| <span data-ttu-id="b1486-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1486-197">System-Flags</span></span>           | <span data-ttu-id="b1486-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b1486-198">0x00000014</span></span>   |
| <span data-ttu-id="b1486-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b1486-199">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="b1486-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1486-200">Windows Server 2008</span></span>



| <span data-ttu-id="b1486-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b1486-201">Entry</span></span> | <span data-ttu-id="b1486-202">Wert</span><span class="sxs-lookup"><span data-stu-id="b1486-202">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b1486-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b1486-203">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b1486-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1486-204">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b1486-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1486-205">System-Only</span></span>            | <span data-ttu-id="b1486-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="b1486-206">True</span></span>         |
| <span data-ttu-id="b1486-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b1486-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b1486-208">False</span><span class="sxs-lookup"><span data-stu-id="b1486-208">False</span></span>        |
| <span data-ttu-id="b1486-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b1486-209">Is Indexed</span></span>             | <span data-ttu-id="b1486-210">False</span><span class="sxs-lookup"><span data-stu-id="b1486-210">False</span></span>        |
| <span data-ttu-id="b1486-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b1486-211">In Global Catalog</span></span>      | <span data-ttu-id="b1486-212">False</span><span class="sxs-lookup"><span data-stu-id="b1486-212">False</span></span>        |
| <span data-ttu-id="b1486-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1486-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1486-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b1486-214">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b1486-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1486-215">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b1486-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1486-216">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b1486-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1486-217">Search-Flags</span></span>           | <span data-ttu-id="b1486-218">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b1486-218">0x00000008</span></span>   |
| <span data-ttu-id="b1486-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1486-219">System-Flags</span></span>           | <span data-ttu-id="b1486-220">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b1486-220">0x00000014</span></span>   |
| <span data-ttu-id="b1486-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b1486-221">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b1486-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b1486-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b1486-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b1486-223">Entry</span></span> | <span data-ttu-id="b1486-224">Wert</span><span class="sxs-lookup"><span data-stu-id="b1486-224">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b1486-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b1486-225">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b1486-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1486-226">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b1486-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1486-227">System-Only</span></span>            | <span data-ttu-id="b1486-228">Richtig</span><span class="sxs-lookup"><span data-stu-id="b1486-228">True</span></span>         |
| <span data-ttu-id="b1486-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b1486-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b1486-230">False</span><span class="sxs-lookup"><span data-stu-id="b1486-230">False</span></span>        |
| <span data-ttu-id="b1486-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b1486-231">Is Indexed</span></span>             | <span data-ttu-id="b1486-232">False</span><span class="sxs-lookup"><span data-stu-id="b1486-232">False</span></span>        |
| <span data-ttu-id="b1486-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b1486-233">In Global Catalog</span></span>      | <span data-ttu-id="b1486-234">False</span><span class="sxs-lookup"><span data-stu-id="b1486-234">False</span></span>        |
| <span data-ttu-id="b1486-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1486-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1486-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b1486-236">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b1486-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1486-237">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b1486-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1486-238">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b1486-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1486-239">Search-Flags</span></span>           | <span data-ttu-id="b1486-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b1486-240">0x00000008</span></span>   |
| <span data-ttu-id="b1486-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1486-241">System-Flags</span></span>           | <span data-ttu-id="b1486-242">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b1486-242">0x00000014</span></span>   |
| <span data-ttu-id="b1486-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b1486-243">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="b1486-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1486-244">Windows Server 2012</span></span>



| <span data-ttu-id="b1486-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b1486-245">Entry</span></span> | <span data-ttu-id="b1486-246">Wert</span><span class="sxs-lookup"><span data-stu-id="b1486-246">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b1486-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b1486-247">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b1486-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1486-248">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b1486-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1486-249">System-Only</span></span>            | <span data-ttu-id="b1486-250">Richtig</span><span class="sxs-lookup"><span data-stu-id="b1486-250">True</span></span>         |
| <span data-ttu-id="b1486-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b1486-251">Is-Single-Valued</span></span>       | <span data-ttu-id="b1486-252">False</span><span class="sxs-lookup"><span data-stu-id="b1486-252">False</span></span>        |
| <span data-ttu-id="b1486-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b1486-253">Is Indexed</span></span>             | <span data-ttu-id="b1486-254">False</span><span class="sxs-lookup"><span data-stu-id="b1486-254">False</span></span>        |
| <span data-ttu-id="b1486-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b1486-255">In Global Catalog</span></span>      | <span data-ttu-id="b1486-256">False</span><span class="sxs-lookup"><span data-stu-id="b1486-256">False</span></span>        |
| <span data-ttu-id="b1486-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1486-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1486-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b1486-258">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b1486-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1486-259">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b1486-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1486-260">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b1486-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1486-261">Search-Flags</span></span>           | <span data-ttu-id="b1486-262">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b1486-262">0x00000008</span></span>   |
| <span data-ttu-id="b1486-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1486-263">System-Flags</span></span>           | <span data-ttu-id="b1486-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b1486-264">0x00000014</span></span>   |
| <span data-ttu-id="b1486-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b1486-265">Classes used in</span></span>        | \-           |



 

 




