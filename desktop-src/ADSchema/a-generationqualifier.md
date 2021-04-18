---
title: Generation-Qualifier-Attribut
description: 'Gibt eine Person-Generierung an. Beispiel: Jr. oder II.'
ms.assetid: 6b882114-3273-43ff-8df3-5b23c98a2dae
ms.tgt_platform: multiple
keywords:
- AD-Schema für Generation-Qualifier-Attribut
- generationqualifier-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Generation-Qualifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc29fdc6bc32273113c5daab2482465535dee145
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106340042"
---
# <a name="generation-qualifier-attribute"></a><span data-ttu-id="244c5-106">Generation-Qualifier-Attribut</span><span class="sxs-lookup"><span data-stu-id="244c5-106">Generation-Qualifier attribute</span></span>

<span data-ttu-id="244c5-107">Gibt eine Person-Generierung an.</span><span class="sxs-lookup"><span data-stu-id="244c5-107">Indicates a person generation.</span></span> <span data-ttu-id="244c5-108">Beispiel: Jr. oder II.</span><span class="sxs-lookup"><span data-stu-id="244c5-108">For example, Jr. or II.</span></span>



| <span data-ttu-id="244c5-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="244c5-109">Entry</span></span> | <span data-ttu-id="244c5-110">Wert</span><span class="sxs-lookup"><span data-stu-id="244c5-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="244c5-111">CN</span><span class="sxs-lookup"><span data-stu-id="244c5-111">CN</span></span>                | <span data-ttu-id="244c5-112">Generation-Qualifier</span><span class="sxs-lookup"><span data-stu-id="244c5-112">Generation-Qualifier</span></span>                        |
| <span data-ttu-id="244c5-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="244c5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="244c5-114">generationqualifizierer</span><span class="sxs-lookup"><span data-stu-id="244c5-114">generationQualifier</span></span>                         |
| <span data-ttu-id="244c5-115">Size</span><span class="sxs-lookup"><span data-stu-id="244c5-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="244c5-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="244c5-116">Update Privilege</span></span>  | <span data-ttu-id="244c5-117">Domänenadministrator</span><span class="sxs-lookup"><span data-stu-id="244c5-117">Domain Administrator</span></span>                        |
| <span data-ttu-id="244c5-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="244c5-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="244c5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="244c5-119">Attribute-Id</span></span>      | <span data-ttu-id="244c5-120">2.5.4.44</span><span class="sxs-lookup"><span data-stu-id="244c5-120">2.5.4.44</span></span>                                    |
| <span data-ttu-id="244c5-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="244c5-121">System-Id-Guid</span></span>    | <span data-ttu-id="244c5-122">16775804-47F 3-11d1-a9c3-0000 C1</span><span class="sxs-lookup"><span data-stu-id="244c5-122">16775804-47f3-11d1-a9c3-0000f80367c1</span></span>        |
| <span data-ttu-id="244c5-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="244c5-123">Syntax</span></span>            | [<span data-ttu-id="244c5-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="244c5-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="244c5-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="244c5-125">Implementations</span></span>

-   [<span data-ttu-id="244c5-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="244c5-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="244c5-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="244c5-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="244c5-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="244c5-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="244c5-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="244c5-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="244c5-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="244c5-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="244c5-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="244c5-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="244c5-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="244c5-132">Windows 2000 Server</span></span>



| <span data-ttu-id="244c5-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="244c5-133">Entry</span></span> | <span data-ttu-id="244c5-134">Wert</span><span class="sxs-lookup"><span data-stu-id="244c5-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="244c5-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="244c5-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="244c5-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="244c5-136">MAPI-Id</span></span>                | <span data-ttu-id="244c5-137">0x8c53</span><span class="sxs-lookup"><span data-stu-id="244c5-137">0x8C53</span></span>                                                             |
| <span data-ttu-id="244c5-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="244c5-138">System-Only</span></span>            | <span data-ttu-id="244c5-139">False</span><span class="sxs-lookup"><span data-stu-id="244c5-139">False</span></span>                                                              |
| <span data-ttu-id="244c5-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="244c5-140">Is-Single-Valued</span></span>       | <span data-ttu-id="244c5-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="244c5-141">True</span></span>                                                               |
| <span data-ttu-id="244c5-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="244c5-142">Is Indexed</span></span>             | <span data-ttu-id="244c5-143">False</span><span class="sxs-lookup"><span data-stu-id="244c5-143">False</span></span>                                                              |
| <span data-ttu-id="244c5-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="244c5-144">In Global Catalog</span></span>      | <span data-ttu-id="244c5-145">False</span><span class="sxs-lookup"><span data-stu-id="244c5-145">False</span></span>                                                              |
| <span data-ttu-id="244c5-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="244c5-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="244c5-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="244c5-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="244c5-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="244c5-148">Range-Lower</span></span>            | <span data-ttu-id="244c5-149">1</span><span class="sxs-lookup"><span data-stu-id="244c5-149">1</span></span>                                                                  |
| <span data-ttu-id="244c5-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="244c5-150">Range-Upper</span></span>            | <span data-ttu-id="244c5-151">64</span><span class="sxs-lookup"><span data-stu-id="244c5-151">64</span></span>                                                                 |
| <span data-ttu-id="244c5-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="244c5-152">Search-Flags</span></span>           | <span data-ttu-id="244c5-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="244c5-153">0x00000000</span></span>                                                         |
| <span data-ttu-id="244c5-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="244c5-154">System-Flags</span></span>           | <span data-ttu-id="244c5-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="244c5-155">0x00000010</span></span>                                                         |
| <span data-ttu-id="244c5-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="244c5-156">Classes used in</span></span>        | [<span data-ttu-id="244c5-157">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="244c5-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="244c5-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="244c5-158">Windows Server 2003</span></span>



| <span data-ttu-id="244c5-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="244c5-159">Entry</span></span> | <span data-ttu-id="244c5-160">Wert</span><span class="sxs-lookup"><span data-stu-id="244c5-160">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="244c5-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="244c5-161">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="244c5-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="244c5-162">MAPI-Id</span></span>                | <span data-ttu-id="244c5-163">0x8c53</span><span class="sxs-lookup"><span data-stu-id="244c5-163">0x8C53</span></span>                                                             |
| <span data-ttu-id="244c5-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="244c5-164">System-Only</span></span>            | <span data-ttu-id="244c5-165">False</span><span class="sxs-lookup"><span data-stu-id="244c5-165">False</span></span>                                                              |
| <span data-ttu-id="244c5-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="244c5-166">Is-Single-Valued</span></span>       | <span data-ttu-id="244c5-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="244c5-167">True</span></span>                                                               |
| <span data-ttu-id="244c5-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="244c5-168">Is Indexed</span></span>             | <span data-ttu-id="244c5-169">False</span><span class="sxs-lookup"><span data-stu-id="244c5-169">False</span></span>                                                              |
| <span data-ttu-id="244c5-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="244c5-170">In Global Catalog</span></span>      | <span data-ttu-id="244c5-171">False</span><span class="sxs-lookup"><span data-stu-id="244c5-171">False</span></span>                                                              |
| <span data-ttu-id="244c5-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="244c5-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="244c5-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="244c5-173">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="244c5-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="244c5-174">Range-Lower</span></span>            | <span data-ttu-id="244c5-175">1</span><span class="sxs-lookup"><span data-stu-id="244c5-175">1</span></span>                                                                  |
| <span data-ttu-id="244c5-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="244c5-176">Range-Upper</span></span>            | <span data-ttu-id="244c5-177">64</span><span class="sxs-lookup"><span data-stu-id="244c5-177">64</span></span>                                                                 |
| <span data-ttu-id="244c5-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="244c5-178">Search-Flags</span></span>           | <span data-ttu-id="244c5-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="244c5-179">0x00000000</span></span>                                                         |
| <span data-ttu-id="244c5-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="244c5-180">System-Flags</span></span>           | <span data-ttu-id="244c5-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="244c5-181">0x00000010</span></span>                                                         |
| <span data-ttu-id="244c5-182">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="244c5-182">Classes used in</span></span>        | [<span data-ttu-id="244c5-183">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="244c5-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="244c5-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="244c5-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="244c5-185">Eingabe</span><span class="sxs-lookup"><span data-stu-id="244c5-185">Entry</span></span> | <span data-ttu-id="244c5-186">Wert</span><span class="sxs-lookup"><span data-stu-id="244c5-186">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="244c5-187">Link-ID</span><span class="sxs-lookup"><span data-stu-id="244c5-187">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="244c5-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="244c5-188">MAPI-Id</span></span>                | <span data-ttu-id="244c5-189">0x8c53</span><span class="sxs-lookup"><span data-stu-id="244c5-189">0x8C53</span></span>                                                             |
| <span data-ttu-id="244c5-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="244c5-190">System-Only</span></span>            | <span data-ttu-id="244c5-191">False</span><span class="sxs-lookup"><span data-stu-id="244c5-191">False</span></span>                                                              |
| <span data-ttu-id="244c5-192">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="244c5-192">Is-Single-Valued</span></span>       | <span data-ttu-id="244c5-193">Richtig</span><span class="sxs-lookup"><span data-stu-id="244c5-193">True</span></span>                                                               |
| <span data-ttu-id="244c5-194">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="244c5-194">Is Indexed</span></span>             | <span data-ttu-id="244c5-195">False</span><span class="sxs-lookup"><span data-stu-id="244c5-195">False</span></span>                                                              |
| <span data-ttu-id="244c5-196">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="244c5-196">In Global Catalog</span></span>      | <span data-ttu-id="244c5-197">False</span><span class="sxs-lookup"><span data-stu-id="244c5-197">False</span></span>                                                              |
| <span data-ttu-id="244c5-198">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="244c5-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="244c5-199">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="244c5-199">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="244c5-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="244c5-200">Range-Lower</span></span>            | <span data-ttu-id="244c5-201">1</span><span class="sxs-lookup"><span data-stu-id="244c5-201">1</span></span>                                                                  |
| <span data-ttu-id="244c5-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="244c5-202">Range-Upper</span></span>            | <span data-ttu-id="244c5-203">64</span><span class="sxs-lookup"><span data-stu-id="244c5-203">64</span></span>                                                                 |
| <span data-ttu-id="244c5-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="244c5-204">Search-Flags</span></span>           | <span data-ttu-id="244c5-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="244c5-205">0x00000000</span></span>                                                         |
| <span data-ttu-id="244c5-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="244c5-206">System-Flags</span></span>           | <span data-ttu-id="244c5-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="244c5-207">0x00000010</span></span>                                                         |
| <span data-ttu-id="244c5-208">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="244c5-208">Classes used in</span></span>        | [<span data-ttu-id="244c5-209">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="244c5-209">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="244c5-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="244c5-210">Windows Server 2008</span></span>



| <span data-ttu-id="244c5-211">Eingabe</span><span class="sxs-lookup"><span data-stu-id="244c5-211">Entry</span></span> | <span data-ttu-id="244c5-212">Wert</span><span class="sxs-lookup"><span data-stu-id="244c5-212">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="244c5-213">Link-ID</span><span class="sxs-lookup"><span data-stu-id="244c5-213">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="244c5-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="244c5-214">MAPI-Id</span></span>                | <span data-ttu-id="244c5-215">0x8c53</span><span class="sxs-lookup"><span data-stu-id="244c5-215">0x8C53</span></span>                                                             |
| <span data-ttu-id="244c5-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="244c5-216">System-Only</span></span>            | <span data-ttu-id="244c5-217">False</span><span class="sxs-lookup"><span data-stu-id="244c5-217">False</span></span>                                                              |
| <span data-ttu-id="244c5-218">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="244c5-218">Is-Single-Valued</span></span>       | <span data-ttu-id="244c5-219">Richtig</span><span class="sxs-lookup"><span data-stu-id="244c5-219">True</span></span>                                                               |
| <span data-ttu-id="244c5-220">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="244c5-220">Is Indexed</span></span>             | <span data-ttu-id="244c5-221">False</span><span class="sxs-lookup"><span data-stu-id="244c5-221">False</span></span>                                                              |
| <span data-ttu-id="244c5-222">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="244c5-222">In Global Catalog</span></span>      | <span data-ttu-id="244c5-223">False</span><span class="sxs-lookup"><span data-stu-id="244c5-223">False</span></span>                                                              |
| <span data-ttu-id="244c5-224">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="244c5-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="244c5-225">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="244c5-225">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="244c5-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="244c5-226">Range-Lower</span></span>            | <span data-ttu-id="244c5-227">1</span><span class="sxs-lookup"><span data-stu-id="244c5-227">1</span></span>                                                                  |
| <span data-ttu-id="244c5-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="244c5-228">Range-Upper</span></span>            | <span data-ttu-id="244c5-229">64</span><span class="sxs-lookup"><span data-stu-id="244c5-229">64</span></span>                                                                 |
| <span data-ttu-id="244c5-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="244c5-230">Search-Flags</span></span>           | <span data-ttu-id="244c5-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="244c5-231">0x00000000</span></span>                                                         |
| <span data-ttu-id="244c5-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="244c5-232">System-Flags</span></span>           | <span data-ttu-id="244c5-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="244c5-233">0x00000010</span></span>                                                         |
| <span data-ttu-id="244c5-234">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="244c5-234">Classes used in</span></span>        | [<span data-ttu-id="244c5-235">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="244c5-235">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="244c5-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="244c5-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="244c5-237">Eingabe</span><span class="sxs-lookup"><span data-stu-id="244c5-237">Entry</span></span> | <span data-ttu-id="244c5-238">Wert</span><span class="sxs-lookup"><span data-stu-id="244c5-238">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="244c5-239">Link-ID</span><span class="sxs-lookup"><span data-stu-id="244c5-239">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="244c5-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="244c5-240">MAPI-Id</span></span>                | <span data-ttu-id="244c5-241">0x8c53</span><span class="sxs-lookup"><span data-stu-id="244c5-241">0x8C53</span></span>                                                             |
| <span data-ttu-id="244c5-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="244c5-242">System-Only</span></span>            | <span data-ttu-id="244c5-243">False</span><span class="sxs-lookup"><span data-stu-id="244c5-243">False</span></span>                                                              |
| <span data-ttu-id="244c5-244">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="244c5-244">Is-Single-Valued</span></span>       | <span data-ttu-id="244c5-245">Richtig</span><span class="sxs-lookup"><span data-stu-id="244c5-245">True</span></span>                                                               |
| <span data-ttu-id="244c5-246">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="244c5-246">Is Indexed</span></span>             | <span data-ttu-id="244c5-247">False</span><span class="sxs-lookup"><span data-stu-id="244c5-247">False</span></span>                                                              |
| <span data-ttu-id="244c5-248">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="244c5-248">In Global Catalog</span></span>      | <span data-ttu-id="244c5-249">False</span><span class="sxs-lookup"><span data-stu-id="244c5-249">False</span></span>                                                              |
| <span data-ttu-id="244c5-250">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="244c5-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="244c5-251">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="244c5-251">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="244c5-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="244c5-252">Range-Lower</span></span>            | <span data-ttu-id="244c5-253">1</span><span class="sxs-lookup"><span data-stu-id="244c5-253">1</span></span>                                                                  |
| <span data-ttu-id="244c5-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="244c5-254">Range-Upper</span></span>            | <span data-ttu-id="244c5-255">64</span><span class="sxs-lookup"><span data-stu-id="244c5-255">64</span></span>                                                                 |
| <span data-ttu-id="244c5-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="244c5-256">Search-Flags</span></span>           | <span data-ttu-id="244c5-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="244c5-257">0x00000000</span></span>                                                         |
| <span data-ttu-id="244c5-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="244c5-258">System-Flags</span></span>           | <span data-ttu-id="244c5-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="244c5-259">0x00000010</span></span>                                                         |
| <span data-ttu-id="244c5-260">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="244c5-260">Classes used in</span></span>        | [<span data-ttu-id="244c5-261">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="244c5-261">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="244c5-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="244c5-262">Windows Server 2012</span></span>



| <span data-ttu-id="244c5-263">Eingabe</span><span class="sxs-lookup"><span data-stu-id="244c5-263">Entry</span></span> | <span data-ttu-id="244c5-264">Wert</span><span class="sxs-lookup"><span data-stu-id="244c5-264">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="244c5-265">Link-ID</span><span class="sxs-lookup"><span data-stu-id="244c5-265">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="244c5-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="244c5-266">MAPI-Id</span></span>                | <span data-ttu-id="244c5-267">0x8c53</span><span class="sxs-lookup"><span data-stu-id="244c5-267">0x8C53</span></span>                                                             |
| <span data-ttu-id="244c5-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="244c5-268">System-Only</span></span>            | <span data-ttu-id="244c5-269">False</span><span class="sxs-lookup"><span data-stu-id="244c5-269">False</span></span>                                                              |
| <span data-ttu-id="244c5-270">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="244c5-270">Is-Single-Valued</span></span>       | <span data-ttu-id="244c5-271">Richtig</span><span class="sxs-lookup"><span data-stu-id="244c5-271">True</span></span>                                                               |
| <span data-ttu-id="244c5-272">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="244c5-272">Is Indexed</span></span>             | <span data-ttu-id="244c5-273">False</span><span class="sxs-lookup"><span data-stu-id="244c5-273">False</span></span>                                                              |
| <span data-ttu-id="244c5-274">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="244c5-274">In Global Catalog</span></span>      | <span data-ttu-id="244c5-275">False</span><span class="sxs-lookup"><span data-stu-id="244c5-275">False</span></span>                                                              |
| <span data-ttu-id="244c5-276">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="244c5-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="244c5-277">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="244c5-277">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="244c5-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="244c5-278">Range-Lower</span></span>            | <span data-ttu-id="244c5-279">1</span><span class="sxs-lookup"><span data-stu-id="244c5-279">1</span></span>                                                                  |
| <span data-ttu-id="244c5-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="244c5-280">Range-Upper</span></span>            | <span data-ttu-id="244c5-281">64</span><span class="sxs-lookup"><span data-stu-id="244c5-281">64</span></span>                                                                 |
| <span data-ttu-id="244c5-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="244c5-282">Search-Flags</span></span>           | <span data-ttu-id="244c5-283">0x00000000</span><span class="sxs-lookup"><span data-stu-id="244c5-283">0x00000000</span></span>                                                         |
| <span data-ttu-id="244c5-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="244c5-284">System-Flags</span></span>           | <span data-ttu-id="244c5-285">0x00000010</span><span class="sxs-lookup"><span data-stu-id="244c5-285">0x00000010</span></span>                                                         |
| <span data-ttu-id="244c5-286">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="244c5-286">Classes used in</span></span>        | [<span data-ttu-id="244c5-287">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="244c5-287">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





