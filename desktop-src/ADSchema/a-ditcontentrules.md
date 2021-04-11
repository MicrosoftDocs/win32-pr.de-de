---
title: DIT-Content-Rules-Attribut
description: Hiermit wird der zulässige Inhalt von Einträgen einer bestimmten strukturellen Objektklasse mithilfe der Identifizierung eines optionalen Satzes von hilfsobjektklassen und obligatorischen, optionalen und ausgelösten Attributen angegeben.
ms.assetid: 75550f5c-efbf-4cd9-8619-a69d2b462f13
ms.tgt_platform: multiple
keywords:
- AD-Schema für dit-Content-Rules-Attribut
- ditcontentrules-Attribut AD-Schema
topic_type:
- apiref
api_name:
- DIT-Content-Rules
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399529237cb7a9f2c4bf1803255f546184ad47f3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123085"
---
# <a name="dit-content-rules-attribute"></a><span data-ttu-id="5882c-105">DIT-Content-Rules-Attribut</span><span class="sxs-lookup"><span data-stu-id="5882c-105">DIT-Content-Rules attribute</span></span>

<span data-ttu-id="5882c-106">Hiermit wird der zulässige Inhalt von Einträgen einer bestimmten strukturellen Objektklasse mithilfe der Identifizierung eines optionalen Satzes von hilfsobjektklassen und obligatorischen, optionalen und ausgelösten Attributen angegeben.</span><span class="sxs-lookup"><span data-stu-id="5882c-106">This specifies the permissible content of entries of a particular structural object class by using the identification of an optional set of auxiliary object classes, and mandatory, optional, and precluded attributes.</span></span> <span data-ttu-id="5882c-107">Kollektive Attribute sind in dit-Content-Rules enthalten, wie in RFC 2251 definiert.</span><span class="sxs-lookup"><span data-stu-id="5882c-107">Collective attributes are included in DIT-Content-Rules as defined in RFC 2251.</span></span>



| <span data-ttu-id="5882c-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5882c-108">Entry</span></span> | <span data-ttu-id="5882c-109">Wert</span><span class="sxs-lookup"><span data-stu-id="5882c-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5882c-110">CN</span><span class="sxs-lookup"><span data-stu-id="5882c-110">CN</span></span>                | <span data-ttu-id="5882c-111">DIT-Content-Rules</span><span class="sxs-lookup"><span data-stu-id="5882c-111">DIT-Content-Rules</span></span>                           |
| <span data-ttu-id="5882c-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5882c-112">Ldap-Display-Name</span></span> | <span data-ttu-id="5882c-113">ditcontentrules</span><span class="sxs-lookup"><span data-stu-id="5882c-113">dITContentRules</span></span>                             |
| <span data-ttu-id="5882c-114">Size</span><span class="sxs-lookup"><span data-stu-id="5882c-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="5882c-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5882c-115">Update Privilege</span></span>  | <span data-ttu-id="5882c-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5882c-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="5882c-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="5882c-117">Update Frequency</span></span>  | <span data-ttu-id="5882c-118">Immer dann, wenn eine neue Klasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5882c-118">Whenever a new class is created.</span></span>            |
| <span data-ttu-id="5882c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5882c-119">Attribute-Id</span></span>      | <span data-ttu-id="5882c-120">2.5.21.2</span><span class="sxs-lookup"><span data-stu-id="5882c-120">2.5.21.2</span></span>                                    |
| <span data-ttu-id="5882c-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5882c-121">System-Id-Guid</span></span>    | <span data-ttu-id="5882c-122">9a7ad946-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="5882c-122">9a7ad946-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="5882c-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="5882c-123">Syntax</span></span>            | [<span data-ttu-id="5882c-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5882c-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5882c-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="5882c-125">Implementations</span></span>

-   [<span data-ttu-id="5882c-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5882c-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5882c-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5882c-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5882c-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="5882c-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="5882c-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5882c-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5882c-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5882c-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5882c-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5882c-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5882c-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5882c-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5882c-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5882c-133">Windows 2000 Server</span></span>



| <span data-ttu-id="5882c-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5882c-134">Entry</span></span> | <span data-ttu-id="5882c-135">Wert</span><span class="sxs-lookup"><span data-stu-id="5882c-135">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="5882c-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5882c-136">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="5882c-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5882c-137">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="5882c-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="5882c-138">System-Only</span></span>            | <span data-ttu-id="5882c-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="5882c-139">True</span></span>                                        |
| <span data-ttu-id="5882c-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5882c-140">Is-Single-Valued</span></span>       | <span data-ttu-id="5882c-141">False</span><span class="sxs-lookup"><span data-stu-id="5882c-141">False</span></span>                                       |
| <span data-ttu-id="5882c-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5882c-142">Is Indexed</span></span>             | <span data-ttu-id="5882c-143">False</span><span class="sxs-lookup"><span data-stu-id="5882c-143">False</span></span>                                       |
| <span data-ttu-id="5882c-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5882c-144">In Global Catalog</span></span>      | <span data-ttu-id="5882c-145">False</span><span class="sxs-lookup"><span data-stu-id="5882c-145">False</span></span>                                       |
| <span data-ttu-id="5882c-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5882c-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="5882c-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5882c-147">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="5882c-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5882c-148">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="5882c-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5882c-149">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="5882c-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5882c-150">Search-Flags</span></span>           | <span data-ttu-id="5882c-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5882c-151">0x00000000</span></span>                                  |
| <span data-ttu-id="5882c-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5882c-152">System-Flags</span></span>           | <span data-ttu-id="5882c-153">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5882c-153">0x08000014</span></span>                                  |
| <span data-ttu-id="5882c-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5882c-154">Classes used in</span></span>        | [<span data-ttu-id="5882c-155">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="5882c-155">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5882c-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5882c-156">Windows Server 2003</span></span>



| <span data-ttu-id="5882c-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5882c-157">Entry</span></span> | <span data-ttu-id="5882c-158">Wert</span><span class="sxs-lookup"><span data-stu-id="5882c-158">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="5882c-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5882c-159">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="5882c-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5882c-160">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="5882c-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="5882c-161">System-Only</span></span>            | <span data-ttu-id="5882c-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="5882c-162">True</span></span>                                        |
| <span data-ttu-id="5882c-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5882c-163">Is-Single-Valued</span></span>       | <span data-ttu-id="5882c-164">False</span><span class="sxs-lookup"><span data-stu-id="5882c-164">False</span></span>                                       |
| <span data-ttu-id="5882c-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5882c-165">Is Indexed</span></span>             | <span data-ttu-id="5882c-166">False</span><span class="sxs-lookup"><span data-stu-id="5882c-166">False</span></span>                                       |
| <span data-ttu-id="5882c-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5882c-167">In Global Catalog</span></span>      | <span data-ttu-id="5882c-168">False</span><span class="sxs-lookup"><span data-stu-id="5882c-168">False</span></span>                                       |
| <span data-ttu-id="5882c-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5882c-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="5882c-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5882c-170">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="5882c-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5882c-171">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="5882c-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5882c-172">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="5882c-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5882c-173">Search-Flags</span></span>           | <span data-ttu-id="5882c-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5882c-174">0x00000000</span></span>                                  |
| <span data-ttu-id="5882c-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5882c-175">System-Flags</span></span>           | <span data-ttu-id="5882c-176">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5882c-176">0x08000014</span></span>                                  |
| <span data-ttu-id="5882c-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5882c-177">Classes used in</span></span>        | [<span data-ttu-id="5882c-178">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="5882c-178">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="5882c-179">Adam</span><span class="sxs-lookup"><span data-stu-id="5882c-179">ADAM</span></span>



| <span data-ttu-id="5882c-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5882c-180">Entry</span></span> | <span data-ttu-id="5882c-181">Wert</span><span class="sxs-lookup"><span data-stu-id="5882c-181">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="5882c-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5882c-182">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="5882c-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5882c-183">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="5882c-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="5882c-184">System-Only</span></span>            | <span data-ttu-id="5882c-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="5882c-185">True</span></span>                                        |
| <span data-ttu-id="5882c-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5882c-186">Is-Single-Valued</span></span>       | <span data-ttu-id="5882c-187">False</span><span class="sxs-lookup"><span data-stu-id="5882c-187">False</span></span>                                       |
| <span data-ttu-id="5882c-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5882c-188">Is Indexed</span></span>             | <span data-ttu-id="5882c-189">False</span><span class="sxs-lookup"><span data-stu-id="5882c-189">False</span></span>                                       |
| <span data-ttu-id="5882c-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5882c-190">In Global Catalog</span></span>      | <span data-ttu-id="5882c-191">False</span><span class="sxs-lookup"><span data-stu-id="5882c-191">False</span></span>                                       |
| <span data-ttu-id="5882c-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5882c-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="5882c-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5882c-193">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="5882c-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5882c-194">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="5882c-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5882c-195">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="5882c-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5882c-196">Search-Flags</span></span>           | <span data-ttu-id="5882c-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5882c-197">0x00000000</span></span>                                  |
| <span data-ttu-id="5882c-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5882c-198">System-Flags</span></span>           | <span data-ttu-id="5882c-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5882c-199">0x08000014</span></span>                                  |
| <span data-ttu-id="5882c-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5882c-200">Classes used in</span></span>        | [<span data-ttu-id="5882c-201">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="5882c-201">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5882c-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5882c-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5882c-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5882c-203">Entry</span></span> | <span data-ttu-id="5882c-204">Wert</span><span class="sxs-lookup"><span data-stu-id="5882c-204">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="5882c-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5882c-205">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="5882c-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5882c-206">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="5882c-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="5882c-207">System-Only</span></span>            | <span data-ttu-id="5882c-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="5882c-208">True</span></span>                                        |
| <span data-ttu-id="5882c-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5882c-209">Is-Single-Valued</span></span>       | <span data-ttu-id="5882c-210">False</span><span class="sxs-lookup"><span data-stu-id="5882c-210">False</span></span>                                       |
| <span data-ttu-id="5882c-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5882c-211">Is Indexed</span></span>             | <span data-ttu-id="5882c-212">False</span><span class="sxs-lookup"><span data-stu-id="5882c-212">False</span></span>                                       |
| <span data-ttu-id="5882c-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5882c-213">In Global Catalog</span></span>      | <span data-ttu-id="5882c-214">False</span><span class="sxs-lookup"><span data-stu-id="5882c-214">False</span></span>                                       |
| <span data-ttu-id="5882c-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5882c-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="5882c-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5882c-216">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="5882c-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5882c-217">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="5882c-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5882c-218">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="5882c-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5882c-219">Search-Flags</span></span>           | <span data-ttu-id="5882c-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5882c-220">0x00000000</span></span>                                  |
| <span data-ttu-id="5882c-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5882c-221">System-Flags</span></span>           | <span data-ttu-id="5882c-222">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5882c-222">0x08000014</span></span>                                  |
| <span data-ttu-id="5882c-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5882c-223">Classes used in</span></span>        | [<span data-ttu-id="5882c-224">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="5882c-224">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5882c-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5882c-225">Windows Server 2008</span></span>



| <span data-ttu-id="5882c-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5882c-226">Entry</span></span> | <span data-ttu-id="5882c-227">Wert</span><span class="sxs-lookup"><span data-stu-id="5882c-227">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="5882c-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5882c-228">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="5882c-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5882c-229">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="5882c-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="5882c-230">System-Only</span></span>            | <span data-ttu-id="5882c-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="5882c-231">True</span></span>                                        |
| <span data-ttu-id="5882c-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5882c-232">Is-Single-Valued</span></span>       | <span data-ttu-id="5882c-233">False</span><span class="sxs-lookup"><span data-stu-id="5882c-233">False</span></span>                                       |
| <span data-ttu-id="5882c-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5882c-234">Is Indexed</span></span>             | <span data-ttu-id="5882c-235">False</span><span class="sxs-lookup"><span data-stu-id="5882c-235">False</span></span>                                       |
| <span data-ttu-id="5882c-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5882c-236">In Global Catalog</span></span>      | <span data-ttu-id="5882c-237">False</span><span class="sxs-lookup"><span data-stu-id="5882c-237">False</span></span>                                       |
| <span data-ttu-id="5882c-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5882c-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="5882c-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5882c-239">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="5882c-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5882c-240">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="5882c-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5882c-241">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="5882c-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5882c-242">Search-Flags</span></span>           | <span data-ttu-id="5882c-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5882c-243">0x00000000</span></span>                                  |
| <span data-ttu-id="5882c-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5882c-244">System-Flags</span></span>           | <span data-ttu-id="5882c-245">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5882c-245">0x08000014</span></span>                                  |
| <span data-ttu-id="5882c-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5882c-246">Classes used in</span></span>        | [<span data-ttu-id="5882c-247">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="5882c-247">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5882c-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5882c-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5882c-249">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5882c-249">Entry</span></span> | <span data-ttu-id="5882c-250">Wert</span><span class="sxs-lookup"><span data-stu-id="5882c-250">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="5882c-251">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5882c-251">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="5882c-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5882c-252">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="5882c-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="5882c-253">System-Only</span></span>            | <span data-ttu-id="5882c-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="5882c-254">True</span></span>                                        |
| <span data-ttu-id="5882c-255">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5882c-255">Is-Single-Valued</span></span>       | <span data-ttu-id="5882c-256">False</span><span class="sxs-lookup"><span data-stu-id="5882c-256">False</span></span>                                       |
| <span data-ttu-id="5882c-257">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5882c-257">Is Indexed</span></span>             | <span data-ttu-id="5882c-258">False</span><span class="sxs-lookup"><span data-stu-id="5882c-258">False</span></span>                                       |
| <span data-ttu-id="5882c-259">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5882c-259">In Global Catalog</span></span>      | <span data-ttu-id="5882c-260">False</span><span class="sxs-lookup"><span data-stu-id="5882c-260">False</span></span>                                       |
| <span data-ttu-id="5882c-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5882c-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="5882c-262">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5882c-262">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="5882c-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5882c-263">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="5882c-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5882c-264">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="5882c-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5882c-265">Search-Flags</span></span>           | <span data-ttu-id="5882c-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5882c-266">0x00000000</span></span>                                  |
| <span data-ttu-id="5882c-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5882c-267">System-Flags</span></span>           | <span data-ttu-id="5882c-268">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5882c-268">0x08000014</span></span>                                  |
| <span data-ttu-id="5882c-269">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5882c-269">Classes used in</span></span>        | [<span data-ttu-id="5882c-270">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="5882c-270">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5882c-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5882c-271">Windows Server 2012</span></span>



| <span data-ttu-id="5882c-272">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5882c-272">Entry</span></span> | <span data-ttu-id="5882c-273">Wert</span><span class="sxs-lookup"><span data-stu-id="5882c-273">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="5882c-274">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5882c-274">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="5882c-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5882c-275">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="5882c-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="5882c-276">System-Only</span></span>            | <span data-ttu-id="5882c-277">Richtig</span><span class="sxs-lookup"><span data-stu-id="5882c-277">True</span></span>                                        |
| <span data-ttu-id="5882c-278">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5882c-278">Is-Single-Valued</span></span>       | <span data-ttu-id="5882c-279">False</span><span class="sxs-lookup"><span data-stu-id="5882c-279">False</span></span>                                       |
| <span data-ttu-id="5882c-280">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5882c-280">Is Indexed</span></span>             | <span data-ttu-id="5882c-281">False</span><span class="sxs-lookup"><span data-stu-id="5882c-281">False</span></span>                                       |
| <span data-ttu-id="5882c-282">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5882c-282">In Global Catalog</span></span>      | <span data-ttu-id="5882c-283">False</span><span class="sxs-lookup"><span data-stu-id="5882c-283">False</span></span>                                       |
| <span data-ttu-id="5882c-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5882c-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="5882c-285">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5882c-285">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="5882c-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5882c-286">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="5882c-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5882c-287">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="5882c-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5882c-288">Search-Flags</span></span>           | <span data-ttu-id="5882c-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5882c-289">0x00000000</span></span>                                  |
| <span data-ttu-id="5882c-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5882c-290">System-Flags</span></span>           | <span data-ttu-id="5882c-291">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5882c-291">0x08000014</span></span>                                  |
| <span data-ttu-id="5882c-292">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5882c-292">Classes used in</span></span>        | [<span data-ttu-id="5882c-293">**Unter Schema**</span><span class="sxs-lookup"><span data-stu-id="5882c-293">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





