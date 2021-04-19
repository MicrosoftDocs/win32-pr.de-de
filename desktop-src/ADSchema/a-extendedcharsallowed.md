---
title: Extended-chars-Allowed-Attribut
description: Gibt an, ob im Wert dieses Attributs erweiterte Zeichen zulässig sind. Gilt nur für IA5-, numerische, druckbare und Teletex-Zeichen folgen Attribute.
ms.assetid: aeacb5ef-9af2-498b-ae53-b3095de0d0c6
ms.tgt_platform: multiple
keywords:
- AD-Schema für erweiterte c#-Attribute
- extendedcharsallowed-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Extended-Chars-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e26194232387f27f3177f13edeab90efc97a4bb3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346142"
---
# <a name="extended-chars-allowed-attribute"></a><span data-ttu-id="14cc0-106">Extended-chars-Allowed-Attribut</span><span class="sxs-lookup"><span data-stu-id="14cc0-106">Extended-Chars-Allowed attribute</span></span>

<span data-ttu-id="14cc0-107">Gibt an, ob im Wert dieses Attributs erweiterte Zeichen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="14cc0-107">Indicates whether extended characters are allowed in the value of this attribute.</span></span> <span data-ttu-id="14cc0-108">Gilt nur für IA5-, numerische, druckbare und Teletex-Zeichen folgen Attribute.</span><span class="sxs-lookup"><span data-stu-id="14cc0-108">Only applies to IA5, Numeric, Printable, and Teletex string attributes.</span></span>



| <span data-ttu-id="14cc0-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14cc0-109">Entry</span></span> | <span data-ttu-id="14cc0-110">Wert</span><span class="sxs-lookup"><span data-stu-id="14cc0-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="14cc0-111">CN</span><span class="sxs-lookup"><span data-stu-id="14cc0-111">CN</span></span>                | <span data-ttu-id="14cc0-112">Extended-chars-Allowed</span><span class="sxs-lookup"><span data-stu-id="14cc0-112">Extended-Chars-Allowed</span></span>               |
| <span data-ttu-id="14cc0-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="14cc0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="14cc0-114">extendedcharsallowed</span><span class="sxs-lookup"><span data-stu-id="14cc0-114">extendedCharsAllowed</span></span>                 |
| <span data-ttu-id="14cc0-115">Size</span><span class="sxs-lookup"><span data-stu-id="14cc0-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="14cc0-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="14cc0-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="14cc0-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="14cc0-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="14cc0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="14cc0-118">Attribute-Id</span></span>      | <span data-ttu-id="14cc0-119">1.2.840.113556.1.2.380</span><span class="sxs-lookup"><span data-stu-id="14cc0-119">1.2.840.113556.1.2.380</span></span>               |
| <span data-ttu-id="14cc0-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="14cc0-120">System-Id-Guid</span></span>    | <span data-ttu-id="14cc0-121">bf967966-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="14cc0-121">bf967966-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="14cc0-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="14cc0-122">Syntax</span></span>            | [<span data-ttu-id="14cc0-123">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="14cc0-123">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="14cc0-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="14cc0-124">Implementations</span></span>

-   [<span data-ttu-id="14cc0-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="14cc0-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="14cc0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="14cc0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="14cc0-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="14cc0-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="14cc0-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="14cc0-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="14cc0-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="14cc0-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="14cc0-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="14cc0-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="14cc0-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="14cc0-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="14cc0-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14cc0-132">Windows 2000 Server</span></span>



| <span data-ttu-id="14cc0-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14cc0-133">Entry</span></span> | <span data-ttu-id="14cc0-134">Wert</span><span class="sxs-lookup"><span data-stu-id="14cc0-134">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="14cc0-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="14cc0-135">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="14cc0-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14cc0-136">MAPI-Id</span></span>                | <span data-ttu-id="14cc0-137">0x80a7</span><span class="sxs-lookup"><span data-stu-id="14cc0-137">0x80A7</span></span>                                                   |
| <span data-ttu-id="14cc0-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="14cc0-138">System-Only</span></span>            | <span data-ttu-id="14cc0-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="14cc0-139">True</span></span>                                                     |
| <span data-ttu-id="14cc0-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="14cc0-140">Is-Single-Valued</span></span>       | <span data-ttu-id="14cc0-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="14cc0-141">True</span></span>                                                     |
| <span data-ttu-id="14cc0-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="14cc0-142">Is Indexed</span></span>             | <span data-ttu-id="14cc0-143">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-143">False</span></span>                                                    |
| <span data-ttu-id="14cc0-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="14cc0-144">In Global Catalog</span></span>      | <span data-ttu-id="14cc0-145">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-145">False</span></span>                                                    |
| <span data-ttu-id="14cc0-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="14cc0-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="14cc0-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="14cc0-147">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="14cc0-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14cc0-148">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="14cc0-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14cc0-149">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="14cc0-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14cc0-150">Search-Flags</span></span>           | <span data-ttu-id="14cc0-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14cc0-151">0x00000000</span></span>                                               |
| <span data-ttu-id="14cc0-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14cc0-152">System-Flags</span></span>           | <span data-ttu-id="14cc0-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14cc0-153">0x00000010</span></span>                                               |
| <span data-ttu-id="14cc0-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="14cc0-154">Classes used in</span></span>        | [<span data-ttu-id="14cc0-155">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="14cc0-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="14cc0-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="14cc0-156">Windows Server 2003</span></span>



| <span data-ttu-id="14cc0-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14cc0-157">Entry</span></span> | <span data-ttu-id="14cc0-158">Wert</span><span class="sxs-lookup"><span data-stu-id="14cc0-158">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="14cc0-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="14cc0-159">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="14cc0-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14cc0-160">MAPI-Id</span></span>                | <span data-ttu-id="14cc0-161">0x80a7</span><span class="sxs-lookup"><span data-stu-id="14cc0-161">0x80A7</span></span>                                                   |
| <span data-ttu-id="14cc0-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="14cc0-162">System-Only</span></span>            | <span data-ttu-id="14cc0-163">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-163">False</span></span>                                                    |
| <span data-ttu-id="14cc0-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="14cc0-164">Is-Single-Valued</span></span>       | <span data-ttu-id="14cc0-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="14cc0-165">True</span></span>                                                     |
| <span data-ttu-id="14cc0-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="14cc0-166">Is Indexed</span></span>             | <span data-ttu-id="14cc0-167">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-167">False</span></span>                                                    |
| <span data-ttu-id="14cc0-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="14cc0-168">In Global Catalog</span></span>      | <span data-ttu-id="14cc0-169">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-169">False</span></span>                                                    |
| <span data-ttu-id="14cc0-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="14cc0-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="14cc0-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="14cc0-171">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="14cc0-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14cc0-172">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="14cc0-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14cc0-173">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="14cc0-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14cc0-174">Search-Flags</span></span>           | <span data-ttu-id="14cc0-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14cc0-175">0x00000000</span></span>                                               |
| <span data-ttu-id="14cc0-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14cc0-176">System-Flags</span></span>           | <span data-ttu-id="14cc0-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14cc0-177">0x00000010</span></span>                                               |
| <span data-ttu-id="14cc0-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="14cc0-178">Classes used in</span></span>        | [<span data-ttu-id="14cc0-179">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="14cc0-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="14cc0-180">Adam</span><span class="sxs-lookup"><span data-stu-id="14cc0-180">ADAM</span></span>



| <span data-ttu-id="14cc0-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14cc0-181">Entry</span></span> | <span data-ttu-id="14cc0-182">Wert</span><span class="sxs-lookup"><span data-stu-id="14cc0-182">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="14cc0-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="14cc0-183">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="14cc0-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14cc0-184">MAPI-Id</span></span>                | <span data-ttu-id="14cc0-185">0x80a7</span><span class="sxs-lookup"><span data-stu-id="14cc0-185">0x80A7</span></span>                                                   |
| <span data-ttu-id="14cc0-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="14cc0-186">System-Only</span></span>            | <span data-ttu-id="14cc0-187">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-187">False</span></span>                                                    |
| <span data-ttu-id="14cc0-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="14cc0-188">Is-Single-Valued</span></span>       | <span data-ttu-id="14cc0-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="14cc0-189">True</span></span>                                                     |
| <span data-ttu-id="14cc0-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="14cc0-190">Is Indexed</span></span>             | <span data-ttu-id="14cc0-191">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-191">False</span></span>                                                    |
| <span data-ttu-id="14cc0-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="14cc0-192">In Global Catalog</span></span>      | <span data-ttu-id="14cc0-193">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-193">False</span></span>                                                    |
| <span data-ttu-id="14cc0-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="14cc0-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="14cc0-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="14cc0-195">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="14cc0-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14cc0-196">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="14cc0-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14cc0-197">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="14cc0-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14cc0-198">Search-Flags</span></span>           | <span data-ttu-id="14cc0-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14cc0-199">0x00000000</span></span>                                               |
| <span data-ttu-id="14cc0-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14cc0-200">System-Flags</span></span>           | <span data-ttu-id="14cc0-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14cc0-201">0x00000010</span></span>                                               |
| <span data-ttu-id="14cc0-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="14cc0-202">Classes used in</span></span>        | [<span data-ttu-id="14cc0-203">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="14cc0-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="14cc0-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="14cc0-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="14cc0-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14cc0-205">Entry</span></span> | <span data-ttu-id="14cc0-206">Wert</span><span class="sxs-lookup"><span data-stu-id="14cc0-206">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="14cc0-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="14cc0-207">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="14cc0-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14cc0-208">MAPI-Id</span></span>                | <span data-ttu-id="14cc0-209">0x80a7</span><span class="sxs-lookup"><span data-stu-id="14cc0-209">0x80A7</span></span>                                                   |
| <span data-ttu-id="14cc0-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="14cc0-210">System-Only</span></span>            | <span data-ttu-id="14cc0-211">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-211">False</span></span>                                                    |
| <span data-ttu-id="14cc0-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="14cc0-212">Is-Single-Valued</span></span>       | <span data-ttu-id="14cc0-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="14cc0-213">True</span></span>                                                     |
| <span data-ttu-id="14cc0-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="14cc0-214">Is Indexed</span></span>             | <span data-ttu-id="14cc0-215">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-215">False</span></span>                                                    |
| <span data-ttu-id="14cc0-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="14cc0-216">In Global Catalog</span></span>      | <span data-ttu-id="14cc0-217">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-217">False</span></span>                                                    |
| <span data-ttu-id="14cc0-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="14cc0-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="14cc0-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="14cc0-219">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="14cc0-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14cc0-220">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="14cc0-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14cc0-221">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="14cc0-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14cc0-222">Search-Flags</span></span>           | <span data-ttu-id="14cc0-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14cc0-223">0x00000000</span></span>                                               |
| <span data-ttu-id="14cc0-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14cc0-224">System-Flags</span></span>           | <span data-ttu-id="14cc0-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14cc0-225">0x00000010</span></span>                                               |
| <span data-ttu-id="14cc0-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="14cc0-226">Classes used in</span></span>        | [<span data-ttu-id="14cc0-227">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="14cc0-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="14cc0-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14cc0-228">Windows Server 2008</span></span>



| <span data-ttu-id="14cc0-229">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14cc0-229">Entry</span></span> | <span data-ttu-id="14cc0-230">Wert</span><span class="sxs-lookup"><span data-stu-id="14cc0-230">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="14cc0-231">Link-ID</span><span class="sxs-lookup"><span data-stu-id="14cc0-231">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="14cc0-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14cc0-232">MAPI-Id</span></span>                | <span data-ttu-id="14cc0-233">0x80a7</span><span class="sxs-lookup"><span data-stu-id="14cc0-233">0x80A7</span></span>                                                   |
| <span data-ttu-id="14cc0-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="14cc0-234">System-Only</span></span>            | <span data-ttu-id="14cc0-235">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-235">False</span></span>                                                    |
| <span data-ttu-id="14cc0-236">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="14cc0-236">Is-Single-Valued</span></span>       | <span data-ttu-id="14cc0-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="14cc0-237">True</span></span>                                                     |
| <span data-ttu-id="14cc0-238">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="14cc0-238">Is Indexed</span></span>             | <span data-ttu-id="14cc0-239">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-239">False</span></span>                                                    |
| <span data-ttu-id="14cc0-240">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="14cc0-240">In Global Catalog</span></span>      | <span data-ttu-id="14cc0-241">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-241">False</span></span>                                                    |
| <span data-ttu-id="14cc0-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="14cc0-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="14cc0-243">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="14cc0-243">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="14cc0-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14cc0-244">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="14cc0-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14cc0-245">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="14cc0-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14cc0-246">Search-Flags</span></span>           | <span data-ttu-id="14cc0-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14cc0-247">0x00000000</span></span>                                               |
| <span data-ttu-id="14cc0-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14cc0-248">System-Flags</span></span>           | <span data-ttu-id="14cc0-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14cc0-249">0x00000010</span></span>                                               |
| <span data-ttu-id="14cc0-250">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="14cc0-250">Classes used in</span></span>        | [<span data-ttu-id="14cc0-251">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="14cc0-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="14cc0-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="14cc0-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="14cc0-253">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14cc0-253">Entry</span></span> | <span data-ttu-id="14cc0-254">Wert</span><span class="sxs-lookup"><span data-stu-id="14cc0-254">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="14cc0-255">Link-ID</span><span class="sxs-lookup"><span data-stu-id="14cc0-255">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="14cc0-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14cc0-256">MAPI-Id</span></span>                | <span data-ttu-id="14cc0-257">0x80a7</span><span class="sxs-lookup"><span data-stu-id="14cc0-257">0x80A7</span></span>                                                   |
| <span data-ttu-id="14cc0-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="14cc0-258">System-Only</span></span>            | <span data-ttu-id="14cc0-259">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-259">False</span></span>                                                    |
| <span data-ttu-id="14cc0-260">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="14cc0-260">Is-Single-Valued</span></span>       | <span data-ttu-id="14cc0-261">Richtig</span><span class="sxs-lookup"><span data-stu-id="14cc0-261">True</span></span>                                                     |
| <span data-ttu-id="14cc0-262">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="14cc0-262">Is Indexed</span></span>             | <span data-ttu-id="14cc0-263">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-263">False</span></span>                                                    |
| <span data-ttu-id="14cc0-264">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="14cc0-264">In Global Catalog</span></span>      | <span data-ttu-id="14cc0-265">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-265">False</span></span>                                                    |
| <span data-ttu-id="14cc0-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="14cc0-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="14cc0-267">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="14cc0-267">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="14cc0-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14cc0-268">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="14cc0-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14cc0-269">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="14cc0-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14cc0-270">Search-Flags</span></span>           | <span data-ttu-id="14cc0-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14cc0-271">0x00000000</span></span>                                               |
| <span data-ttu-id="14cc0-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14cc0-272">System-Flags</span></span>           | <span data-ttu-id="14cc0-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14cc0-273">0x00000010</span></span>                                               |
| <span data-ttu-id="14cc0-274">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="14cc0-274">Classes used in</span></span>        | [<span data-ttu-id="14cc0-275">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="14cc0-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="14cc0-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14cc0-276">Windows Server 2012</span></span>



| <span data-ttu-id="14cc0-277">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14cc0-277">Entry</span></span> | <span data-ttu-id="14cc0-278">Wert</span><span class="sxs-lookup"><span data-stu-id="14cc0-278">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="14cc0-279">Link-ID</span><span class="sxs-lookup"><span data-stu-id="14cc0-279">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="14cc0-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14cc0-280">MAPI-Id</span></span>                | <span data-ttu-id="14cc0-281">0x80a7</span><span class="sxs-lookup"><span data-stu-id="14cc0-281">0x80A7</span></span>                                                   |
| <span data-ttu-id="14cc0-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="14cc0-282">System-Only</span></span>            | <span data-ttu-id="14cc0-283">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-283">False</span></span>                                                    |
| <span data-ttu-id="14cc0-284">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="14cc0-284">Is-Single-Valued</span></span>       | <span data-ttu-id="14cc0-285">Richtig</span><span class="sxs-lookup"><span data-stu-id="14cc0-285">True</span></span>                                                     |
| <span data-ttu-id="14cc0-286">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="14cc0-286">Is Indexed</span></span>             | <span data-ttu-id="14cc0-287">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-287">False</span></span>                                                    |
| <span data-ttu-id="14cc0-288">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="14cc0-288">In Global Catalog</span></span>      | <span data-ttu-id="14cc0-289">False</span><span class="sxs-lookup"><span data-stu-id="14cc0-289">False</span></span>                                                    |
| <span data-ttu-id="14cc0-290">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="14cc0-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="14cc0-291">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="14cc0-291">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="14cc0-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14cc0-292">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="14cc0-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14cc0-293">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="14cc0-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14cc0-294">Search-Flags</span></span>           | <span data-ttu-id="14cc0-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14cc0-295">0x00000000</span></span>                                               |
| <span data-ttu-id="14cc0-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14cc0-296">System-Flags</span></span>           | <span data-ttu-id="14cc0-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14cc0-297">0x00000010</span></span>                                               |
| <span data-ttu-id="14cc0-298">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="14cc0-298">Classes used in</span></span>        | [<span data-ttu-id="14cc0-299">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="14cc0-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





