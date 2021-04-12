---
title: Revision-Attribut
description: Die Revisions Ebene für eine Sicherheits Beschreibung oder eine andere Änderung. Wird nur in den SAM-Server-und DS-UI-Settings-Objekten verwendet.
ms.assetid: 480de80f-3e76-4a62-a4a7-29a67f910a62
ms.tgt_platform: multiple
keywords:
- AD-Schema für Revisions Attribut
- AD-Schema für Revisions Attribut
topic_type:
- apiref
api_name:
- Revision
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8948bd865db776c52ac021d296792a6f7d0720dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519671"
---
# <a name="revision-attribute"></a><span data-ttu-id="39648-106">Revision-Attribut</span><span class="sxs-lookup"><span data-stu-id="39648-106">Revision attribute</span></span>

<span data-ttu-id="39648-107">Die Revisions Ebene für eine Sicherheits Beschreibung oder eine andere Änderung.</span><span class="sxs-lookup"><span data-stu-id="39648-107">The revision level for a security descriptor or other change.</span></span> <span data-ttu-id="39648-108">Wird nur in den SAM-Server-und DS-UI-Settings-Objekten verwendet.</span><span class="sxs-lookup"><span data-stu-id="39648-108">Only used in the sam-server and ds-ui-settings objects.</span></span>



| <span data-ttu-id="39648-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39648-109">Entry</span></span> | <span data-ttu-id="39648-110">Wert</span><span class="sxs-lookup"><span data-stu-id="39648-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="39648-111">CN</span><span class="sxs-lookup"><span data-stu-id="39648-111">CN</span></span>                | <span data-ttu-id="39648-112">Revision</span><span class="sxs-lookup"><span data-stu-id="39648-112">Revision</span></span>                             |
| <span data-ttu-id="39648-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="39648-113">Ldap-Display-Name</span></span> | <span data-ttu-id="39648-114">revision</span><span class="sxs-lookup"><span data-stu-id="39648-114">revision</span></span>                             |
| <span data-ttu-id="39648-115">Size</span><span class="sxs-lookup"><span data-stu-id="39648-115">Size</span></span>              | <span data-ttu-id="39648-116">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="39648-116">4 bytes</span></span>                              |
| <span data-ttu-id="39648-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="39648-117">Update Privilege</span></span>  | <span data-ttu-id="39648-118">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="39648-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="39648-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="39648-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="39648-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="39648-120">Attribute-Id</span></span>      | <span data-ttu-id="39648-121">1.2.840.113556.1.4.145</span><span class="sxs-lookup"><span data-stu-id="39648-121">1.2.840.113556.1.4.145</span></span>               |
| <span data-ttu-id="39648-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="39648-122">System-Id-Guid</span></span>    | <span data-ttu-id="39648-123">bf967a21-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="39648-123">bf967a21-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="39648-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="39648-124">Syntax</span></span>            | [<span data-ttu-id="39648-125">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="39648-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="39648-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="39648-126">Implementations</span></span>

-   [<span data-ttu-id="39648-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="39648-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="39648-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="39648-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="39648-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="39648-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="39648-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="39648-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="39648-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="39648-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="39648-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="39648-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="39648-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="39648-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="39648-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="39648-134">Windows 2000 Server</span></span>



| <span data-ttu-id="39648-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39648-135">Entry</span></span> | <span data-ttu-id="39648-136">Wert</span><span class="sxs-lookup"><span data-stu-id="39648-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39648-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39648-137">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="39648-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39648-138">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="39648-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="39648-139">System-Only</span></span>            | <span data-ttu-id="39648-140">False</span><span class="sxs-lookup"><span data-stu-id="39648-140">False</span></span>                                                                                 |
| <span data-ttu-id="39648-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39648-141">Is-Single-Valued</span></span>       | <span data-ttu-id="39648-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="39648-142">True</span></span>                                                                                  |
| <span data-ttu-id="39648-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39648-143">Is Indexed</span></span>             | <span data-ttu-id="39648-144">False</span><span class="sxs-lookup"><span data-stu-id="39648-144">False</span></span>                                                                                 |
| <span data-ttu-id="39648-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39648-145">In Global Catalog</span></span>      | <span data-ttu-id="39648-146">False</span><span class="sxs-lookup"><span data-stu-id="39648-146">False</span></span>                                                                                 |
| <span data-ttu-id="39648-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39648-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="39648-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39648-148">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="39648-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39648-149">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="39648-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39648-150">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="39648-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39648-151">Search-Flags</span></span>           | <span data-ttu-id="39648-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39648-152">0x00000000</span></span>                                                                            |
| <span data-ttu-id="39648-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39648-153">System-Flags</span></span>           | <span data-ttu-id="39648-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39648-154">0x00000010</span></span>                                                                            |
| <span data-ttu-id="39648-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39648-155">Classes used in</span></span>        | [<span data-ttu-id="39648-156">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="39648-156">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="39648-157">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="39648-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="39648-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="39648-158">Windows Server 2003</span></span>



| <span data-ttu-id="39648-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39648-159">Entry</span></span> | <span data-ttu-id="39648-160">Wert</span><span class="sxs-lookup"><span data-stu-id="39648-160">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39648-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39648-161">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="39648-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39648-162">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="39648-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="39648-163">System-Only</span></span>            | <span data-ttu-id="39648-164">False</span><span class="sxs-lookup"><span data-stu-id="39648-164">False</span></span>                                                                                 |
| <span data-ttu-id="39648-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39648-165">Is-Single-Valued</span></span>       | <span data-ttu-id="39648-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="39648-166">True</span></span>                                                                                  |
| <span data-ttu-id="39648-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39648-167">Is Indexed</span></span>             | <span data-ttu-id="39648-168">False</span><span class="sxs-lookup"><span data-stu-id="39648-168">False</span></span>                                                                                 |
| <span data-ttu-id="39648-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39648-169">In Global Catalog</span></span>      | <span data-ttu-id="39648-170">False</span><span class="sxs-lookup"><span data-stu-id="39648-170">False</span></span>                                                                                 |
| <span data-ttu-id="39648-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39648-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="39648-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39648-172">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="39648-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39648-173">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="39648-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39648-174">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="39648-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39648-175">Search-Flags</span></span>           | <span data-ttu-id="39648-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39648-176">0x00000000</span></span>                                                                            |
| <span data-ttu-id="39648-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39648-177">System-Flags</span></span>           | <span data-ttu-id="39648-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39648-178">0x00000010</span></span>                                                                            |
| <span data-ttu-id="39648-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39648-179">Classes used in</span></span>        | [<span data-ttu-id="39648-180">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="39648-180">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="39648-181">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="39648-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="39648-182">Adam</span><span class="sxs-lookup"><span data-stu-id="39648-182">ADAM</span></span>



| <span data-ttu-id="39648-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39648-183">Entry</span></span> | <span data-ttu-id="39648-184">Wert</span><span class="sxs-lookup"><span data-stu-id="39648-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="39648-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39648-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="39648-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39648-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="39648-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="39648-187">System-Only</span></span>            | <span data-ttu-id="39648-188">False</span><span class="sxs-lookup"><span data-stu-id="39648-188">False</span></span>                           |
| <span data-ttu-id="39648-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39648-189">Is-Single-Valued</span></span>       | <span data-ttu-id="39648-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="39648-190">True</span></span>                            |
| <span data-ttu-id="39648-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39648-191">Is Indexed</span></span>             | <span data-ttu-id="39648-192">False</span><span class="sxs-lookup"><span data-stu-id="39648-192">False</span></span>                           |
| <span data-ttu-id="39648-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39648-193">In Global Catalog</span></span>      | <span data-ttu-id="39648-194">False</span><span class="sxs-lookup"><span data-stu-id="39648-194">False</span></span>                           |
| <span data-ttu-id="39648-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39648-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="39648-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39648-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="39648-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39648-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="39648-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39648-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="39648-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39648-199">Search-Flags</span></span>           | <span data-ttu-id="39648-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39648-200">0x00000000</span></span>                      |
| <span data-ttu-id="39648-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39648-201">System-Flags</span></span>           | <span data-ttu-id="39648-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39648-202">0x00000010</span></span>                      |
| <span data-ttu-id="39648-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39648-203">Classes used in</span></span>        | [<span data-ttu-id="39648-204">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="39648-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="39648-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="39648-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="39648-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39648-206">Entry</span></span> | <span data-ttu-id="39648-207">Wert</span><span class="sxs-lookup"><span data-stu-id="39648-207">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39648-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39648-208">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="39648-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39648-209">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="39648-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="39648-210">System-Only</span></span>            | <span data-ttu-id="39648-211">False</span><span class="sxs-lookup"><span data-stu-id="39648-211">False</span></span>                                                                                 |
| <span data-ttu-id="39648-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39648-212">Is-Single-Valued</span></span>       | <span data-ttu-id="39648-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="39648-213">True</span></span>                                                                                  |
| <span data-ttu-id="39648-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39648-214">Is Indexed</span></span>             | <span data-ttu-id="39648-215">False</span><span class="sxs-lookup"><span data-stu-id="39648-215">False</span></span>                                                                                 |
| <span data-ttu-id="39648-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39648-216">In Global Catalog</span></span>      | <span data-ttu-id="39648-217">False</span><span class="sxs-lookup"><span data-stu-id="39648-217">False</span></span>                                                                                 |
| <span data-ttu-id="39648-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39648-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="39648-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39648-219">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="39648-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39648-220">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="39648-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39648-221">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="39648-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39648-222">Search-Flags</span></span>           | <span data-ttu-id="39648-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39648-223">0x00000000</span></span>                                                                            |
| <span data-ttu-id="39648-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39648-224">System-Flags</span></span>           | <span data-ttu-id="39648-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39648-225">0x00000010</span></span>                                                                            |
| <span data-ttu-id="39648-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39648-226">Classes used in</span></span>        | [<span data-ttu-id="39648-227">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="39648-227">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="39648-228">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="39648-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="39648-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39648-229">Windows Server 2008</span></span>



| <span data-ttu-id="39648-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39648-230">Entry</span></span> | <span data-ttu-id="39648-231">Wert</span><span class="sxs-lookup"><span data-stu-id="39648-231">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39648-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39648-232">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="39648-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39648-233">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="39648-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="39648-234">System-Only</span></span>            | <span data-ttu-id="39648-235">False</span><span class="sxs-lookup"><span data-stu-id="39648-235">False</span></span>                                                                                 |
| <span data-ttu-id="39648-236">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39648-236">Is-Single-Valued</span></span>       | <span data-ttu-id="39648-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="39648-237">True</span></span>                                                                                  |
| <span data-ttu-id="39648-238">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39648-238">Is Indexed</span></span>             | <span data-ttu-id="39648-239">False</span><span class="sxs-lookup"><span data-stu-id="39648-239">False</span></span>                                                                                 |
| <span data-ttu-id="39648-240">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39648-240">In Global Catalog</span></span>      | <span data-ttu-id="39648-241">False</span><span class="sxs-lookup"><span data-stu-id="39648-241">False</span></span>                                                                                 |
| <span data-ttu-id="39648-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39648-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="39648-243">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39648-243">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="39648-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39648-244">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="39648-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39648-245">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="39648-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39648-246">Search-Flags</span></span>           | <span data-ttu-id="39648-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39648-247">0x00000000</span></span>                                                                            |
| <span data-ttu-id="39648-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39648-248">System-Flags</span></span>           | <span data-ttu-id="39648-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39648-249">0x00000010</span></span>                                                                            |
| <span data-ttu-id="39648-250">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39648-250">Classes used in</span></span>        | [<span data-ttu-id="39648-251">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="39648-251">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="39648-252">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="39648-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="39648-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39648-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="39648-254">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39648-254">Entry</span></span> | <span data-ttu-id="39648-255">Wert</span><span class="sxs-lookup"><span data-stu-id="39648-255">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39648-256">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39648-256">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="39648-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39648-257">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="39648-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="39648-258">System-Only</span></span>            | <span data-ttu-id="39648-259">False</span><span class="sxs-lookup"><span data-stu-id="39648-259">False</span></span>                                                                                 |
| <span data-ttu-id="39648-260">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39648-260">Is-Single-Valued</span></span>       | <span data-ttu-id="39648-261">Richtig</span><span class="sxs-lookup"><span data-stu-id="39648-261">True</span></span>                                                                                  |
| <span data-ttu-id="39648-262">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39648-262">Is Indexed</span></span>             | <span data-ttu-id="39648-263">False</span><span class="sxs-lookup"><span data-stu-id="39648-263">False</span></span>                                                                                 |
| <span data-ttu-id="39648-264">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39648-264">In Global Catalog</span></span>      | <span data-ttu-id="39648-265">False</span><span class="sxs-lookup"><span data-stu-id="39648-265">False</span></span>                                                                                 |
| <span data-ttu-id="39648-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39648-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="39648-267">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39648-267">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="39648-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39648-268">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="39648-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39648-269">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="39648-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39648-270">Search-Flags</span></span>           | <span data-ttu-id="39648-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39648-271">0x00000000</span></span>                                                                            |
| <span data-ttu-id="39648-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39648-272">System-Flags</span></span>           | <span data-ttu-id="39648-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39648-273">0x00000010</span></span>                                                                            |
| <span data-ttu-id="39648-274">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39648-274">Classes used in</span></span>        | [<span data-ttu-id="39648-275">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="39648-275">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="39648-276">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="39648-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="39648-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="39648-277">Windows Server 2012</span></span>



| <span data-ttu-id="39648-278">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39648-278">Entry</span></span> | <span data-ttu-id="39648-279">Wert</span><span class="sxs-lookup"><span data-stu-id="39648-279">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39648-280">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39648-280">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="39648-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39648-281">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="39648-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="39648-282">System-Only</span></span>            | <span data-ttu-id="39648-283">False</span><span class="sxs-lookup"><span data-stu-id="39648-283">False</span></span>                                                                                 |
| <span data-ttu-id="39648-284">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39648-284">Is-Single-Valued</span></span>       | <span data-ttu-id="39648-285">Richtig</span><span class="sxs-lookup"><span data-stu-id="39648-285">True</span></span>                                                                                  |
| <span data-ttu-id="39648-286">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39648-286">Is Indexed</span></span>             | <span data-ttu-id="39648-287">False</span><span class="sxs-lookup"><span data-stu-id="39648-287">False</span></span>                                                                                 |
| <span data-ttu-id="39648-288">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39648-288">In Global Catalog</span></span>      | <span data-ttu-id="39648-289">False</span><span class="sxs-lookup"><span data-stu-id="39648-289">False</span></span>                                                                                 |
| <span data-ttu-id="39648-290">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39648-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="39648-291">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39648-291">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="39648-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39648-292">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="39648-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39648-293">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="39648-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39648-294">Search-Flags</span></span>           | <span data-ttu-id="39648-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39648-295">0x00000000</span></span>                                                                            |
| <span data-ttu-id="39648-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39648-296">System-Flags</span></span>           | <span data-ttu-id="39648-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39648-297">0x00000010</span></span>                                                                            |
| <span data-ttu-id="39648-298">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39648-298">Classes used in</span></span>        | [<span data-ttu-id="39648-299">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="39648-299">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="39648-300">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="39648-300">**Top**</span></span>](c-top.md)<br/> |



 

 





