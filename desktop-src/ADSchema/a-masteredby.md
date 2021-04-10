---
title: Mastered-By-Attribut
description: Rückwärts Verknüpfung für das Attribut "-Master-NCS". Der Distinguished Name für die NTDS-Einstellungs Objekte.
ms.assetid: bd14998c-1691-4167-83c4-3c1ec1181b7f
ms.tgt_platform: multiple
keywords:
- AD-Schema für Mastered-By-Attribut
- masteredby-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Mastered-By
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85cf02f78363e1e8db06bddfb2c389cc78077090
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107223"
---
# <a name="mastered-by-attribute"></a><span data-ttu-id="5601a-106">Mastered-By-Attribut</span><span class="sxs-lookup"><span data-stu-id="5601a-106">Mastered-By attribute</span></span>

<span data-ttu-id="5601a-107">Rückwärts Verknüpfung für das Attribut "-Master-NCS".</span><span class="sxs-lookup"><span data-stu-id="5601a-107">Backward link for Has-Master-NCs attribute.</span></span> <span data-ttu-id="5601a-108">Der Distinguished Name für die NTDS-Einstellungs Objekte.</span><span class="sxs-lookup"><span data-stu-id="5601a-108">The distinguished name for its NTDS Settings objects.</span></span>



| <span data-ttu-id="5601a-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5601a-109">Entry</span></span> | <span data-ttu-id="5601a-110">Wert</span><span class="sxs-lookup"><span data-stu-id="5601a-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="5601a-111">CN</span><span class="sxs-lookup"><span data-stu-id="5601a-111">CN</span></span>                | <span data-ttu-id="5601a-112">Mastered-By</span><span class="sxs-lookup"><span data-stu-id="5601a-112">Mastered-By</span></span>                             |
| <span data-ttu-id="5601a-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5601a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5601a-114">masteredby</span><span class="sxs-lookup"><span data-stu-id="5601a-114">masteredBy</span></span>                              |
| <span data-ttu-id="5601a-115">Size</span><span class="sxs-lookup"><span data-stu-id="5601a-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="5601a-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5601a-116">Update Privilege</span></span>  | <span data-ttu-id="5601a-117">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5601a-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="5601a-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="5601a-118">Update Frequency</span></span>  | <span data-ttu-id="5601a-119">Wenn der namens Kontext erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5601a-119">When the Naming Context is created.</span></span>     |
| <span data-ttu-id="5601a-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5601a-120">Attribute-Id</span></span>      | <span data-ttu-id="5601a-121">1.2.840.113556.1.4.1409</span><span class="sxs-lookup"><span data-stu-id="5601a-121">1.2.840.113556.1.4.1409</span></span>                 |
| <span data-ttu-id="5601a-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5601a-122">System-Id-Guid</span></span>    | <span data-ttu-id="5601a-123">e48e64e0-12c9-11d3-9102-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="5601a-123">e48e64e0-12c9-11d3-9102-00c04fd91ab1</span></span>    |
| <span data-ttu-id="5601a-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="5601a-124">Syntax</span></span>            | [<span data-ttu-id="5601a-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="5601a-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="5601a-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="5601a-126">Implementations</span></span>

-   [<span data-ttu-id="5601a-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5601a-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5601a-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5601a-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5601a-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="5601a-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="5601a-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5601a-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5601a-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5601a-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5601a-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5601a-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5601a-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5601a-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5601a-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5601a-134">Windows 2000 Server</span></span>



| <span data-ttu-id="5601a-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5601a-135">Entry</span></span> | <span data-ttu-id="5601a-136">Wert</span><span class="sxs-lookup"><span data-stu-id="5601a-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5601a-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5601a-137">Link-Id</span></span>                | <span data-ttu-id="5601a-138">77</span><span class="sxs-lookup"><span data-stu-id="5601a-138">77</span></span>                              |
| <span data-ttu-id="5601a-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5601a-139">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5601a-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="5601a-140">System-Only</span></span>            | <span data-ttu-id="5601a-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="5601a-141">True</span></span>                            |
| <span data-ttu-id="5601a-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5601a-142">Is-Single-Valued</span></span>       | <span data-ttu-id="5601a-143">False</span><span class="sxs-lookup"><span data-stu-id="5601a-143">False</span></span>                           |
| <span data-ttu-id="5601a-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5601a-144">Is Indexed</span></span>             | <span data-ttu-id="5601a-145">False</span><span class="sxs-lookup"><span data-stu-id="5601a-145">False</span></span>                           |
| <span data-ttu-id="5601a-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5601a-146">In Global Catalog</span></span>      | <span data-ttu-id="5601a-147">False</span><span class="sxs-lookup"><span data-stu-id="5601a-147">False</span></span>                           |
| <span data-ttu-id="5601a-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5601a-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="5601a-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5601a-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5601a-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5601a-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5601a-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5601a-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5601a-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5601a-152">Search-Flags</span></span>           | <span data-ttu-id="5601a-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5601a-153">0x00000000</span></span>                      |
| <span data-ttu-id="5601a-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5601a-154">System-Flags</span></span>           | <span data-ttu-id="5601a-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5601a-155">0x00000010</span></span>                      |
| <span data-ttu-id="5601a-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5601a-156">Classes used in</span></span>        | [<span data-ttu-id="5601a-157">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="5601a-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5601a-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5601a-158">Windows Server 2003</span></span>



| <span data-ttu-id="5601a-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5601a-159">Entry</span></span> | <span data-ttu-id="5601a-160">Wert</span><span class="sxs-lookup"><span data-stu-id="5601a-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5601a-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5601a-161">Link-Id</span></span>                | <span data-ttu-id="5601a-162">77</span><span class="sxs-lookup"><span data-stu-id="5601a-162">77</span></span>                              |
| <span data-ttu-id="5601a-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5601a-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5601a-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="5601a-164">System-Only</span></span>            | <span data-ttu-id="5601a-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="5601a-165">True</span></span>                            |
| <span data-ttu-id="5601a-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5601a-166">Is-Single-Valued</span></span>       | <span data-ttu-id="5601a-167">False</span><span class="sxs-lookup"><span data-stu-id="5601a-167">False</span></span>                           |
| <span data-ttu-id="5601a-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5601a-168">Is Indexed</span></span>             | <span data-ttu-id="5601a-169">False</span><span class="sxs-lookup"><span data-stu-id="5601a-169">False</span></span>                           |
| <span data-ttu-id="5601a-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5601a-170">In Global Catalog</span></span>      | <span data-ttu-id="5601a-171">False</span><span class="sxs-lookup"><span data-stu-id="5601a-171">False</span></span>                           |
| <span data-ttu-id="5601a-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5601a-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="5601a-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5601a-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5601a-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5601a-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5601a-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5601a-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5601a-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5601a-176">Search-Flags</span></span>           | <span data-ttu-id="5601a-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5601a-177">0x00000000</span></span>                      |
| <span data-ttu-id="5601a-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5601a-178">System-Flags</span></span>           | <span data-ttu-id="5601a-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5601a-179">0x00000010</span></span>                      |
| <span data-ttu-id="5601a-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5601a-180">Classes used in</span></span>        | [<span data-ttu-id="5601a-181">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="5601a-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="5601a-182">Adam</span><span class="sxs-lookup"><span data-stu-id="5601a-182">ADAM</span></span>



| <span data-ttu-id="5601a-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5601a-183">Entry</span></span> | <span data-ttu-id="5601a-184">Wert</span><span class="sxs-lookup"><span data-stu-id="5601a-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5601a-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5601a-185">Link-Id</span></span>                | <span data-ttu-id="5601a-186">77</span><span class="sxs-lookup"><span data-stu-id="5601a-186">77</span></span>                              |
| <span data-ttu-id="5601a-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5601a-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5601a-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="5601a-188">System-Only</span></span>            | <span data-ttu-id="5601a-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="5601a-189">True</span></span>                            |
| <span data-ttu-id="5601a-190">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5601a-190">Is-Single-Valued</span></span>       | <span data-ttu-id="5601a-191">False</span><span class="sxs-lookup"><span data-stu-id="5601a-191">False</span></span>                           |
| <span data-ttu-id="5601a-192">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5601a-192">Is Indexed</span></span>             | <span data-ttu-id="5601a-193">False</span><span class="sxs-lookup"><span data-stu-id="5601a-193">False</span></span>                           |
| <span data-ttu-id="5601a-194">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5601a-194">In Global Catalog</span></span>      | <span data-ttu-id="5601a-195">False</span><span class="sxs-lookup"><span data-stu-id="5601a-195">False</span></span>                           |
| <span data-ttu-id="5601a-196">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5601a-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="5601a-197">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5601a-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5601a-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5601a-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5601a-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5601a-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5601a-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5601a-200">Search-Flags</span></span>           | <span data-ttu-id="5601a-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5601a-201">0x00000000</span></span>                      |
| <span data-ttu-id="5601a-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5601a-202">System-Flags</span></span>           | <span data-ttu-id="5601a-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5601a-203">0x00000010</span></span>                      |
| <span data-ttu-id="5601a-204">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5601a-204">Classes used in</span></span>        | [<span data-ttu-id="5601a-205">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="5601a-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5601a-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5601a-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5601a-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5601a-207">Entry</span></span> | <span data-ttu-id="5601a-208">Wert</span><span class="sxs-lookup"><span data-stu-id="5601a-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5601a-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5601a-209">Link-Id</span></span>                | <span data-ttu-id="5601a-210">77</span><span class="sxs-lookup"><span data-stu-id="5601a-210">77</span></span>                              |
| <span data-ttu-id="5601a-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5601a-211">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5601a-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="5601a-212">System-Only</span></span>            | <span data-ttu-id="5601a-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="5601a-213">True</span></span>                            |
| <span data-ttu-id="5601a-214">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5601a-214">Is-Single-Valued</span></span>       | <span data-ttu-id="5601a-215">False</span><span class="sxs-lookup"><span data-stu-id="5601a-215">False</span></span>                           |
| <span data-ttu-id="5601a-216">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5601a-216">Is Indexed</span></span>             | <span data-ttu-id="5601a-217">False</span><span class="sxs-lookup"><span data-stu-id="5601a-217">False</span></span>                           |
| <span data-ttu-id="5601a-218">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5601a-218">In Global Catalog</span></span>      | <span data-ttu-id="5601a-219">False</span><span class="sxs-lookup"><span data-stu-id="5601a-219">False</span></span>                           |
| <span data-ttu-id="5601a-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5601a-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="5601a-221">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5601a-221">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5601a-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5601a-222">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5601a-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5601a-223">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5601a-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5601a-224">Search-Flags</span></span>           | <span data-ttu-id="5601a-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5601a-225">0x00000000</span></span>                      |
| <span data-ttu-id="5601a-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5601a-226">System-Flags</span></span>           | <span data-ttu-id="5601a-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5601a-227">0x00000010</span></span>                      |
| <span data-ttu-id="5601a-228">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5601a-228">Classes used in</span></span>        | [<span data-ttu-id="5601a-229">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="5601a-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5601a-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5601a-230">Windows Server 2008</span></span>



| <span data-ttu-id="5601a-231">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5601a-231">Entry</span></span> | <span data-ttu-id="5601a-232">Wert</span><span class="sxs-lookup"><span data-stu-id="5601a-232">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5601a-233">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5601a-233">Link-Id</span></span>                | <span data-ttu-id="5601a-234">77</span><span class="sxs-lookup"><span data-stu-id="5601a-234">77</span></span>                              |
| <span data-ttu-id="5601a-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5601a-235">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5601a-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="5601a-236">System-Only</span></span>            | <span data-ttu-id="5601a-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="5601a-237">True</span></span>                            |
| <span data-ttu-id="5601a-238">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5601a-238">Is-Single-Valued</span></span>       | <span data-ttu-id="5601a-239">False</span><span class="sxs-lookup"><span data-stu-id="5601a-239">False</span></span>                           |
| <span data-ttu-id="5601a-240">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5601a-240">Is Indexed</span></span>             | <span data-ttu-id="5601a-241">False</span><span class="sxs-lookup"><span data-stu-id="5601a-241">False</span></span>                           |
| <span data-ttu-id="5601a-242">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5601a-242">In Global Catalog</span></span>      | <span data-ttu-id="5601a-243">False</span><span class="sxs-lookup"><span data-stu-id="5601a-243">False</span></span>                           |
| <span data-ttu-id="5601a-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5601a-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="5601a-245">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5601a-245">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5601a-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5601a-246">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5601a-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5601a-247">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5601a-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5601a-248">Search-Flags</span></span>           | <span data-ttu-id="5601a-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5601a-249">0x00000000</span></span>                      |
| <span data-ttu-id="5601a-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5601a-250">System-Flags</span></span>           | <span data-ttu-id="5601a-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5601a-251">0x00000010</span></span>                      |
| <span data-ttu-id="5601a-252">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5601a-252">Classes used in</span></span>        | [<span data-ttu-id="5601a-253">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="5601a-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5601a-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5601a-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5601a-255">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5601a-255">Entry</span></span> | <span data-ttu-id="5601a-256">Wert</span><span class="sxs-lookup"><span data-stu-id="5601a-256">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5601a-257">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5601a-257">Link-Id</span></span>                | <span data-ttu-id="5601a-258">77</span><span class="sxs-lookup"><span data-stu-id="5601a-258">77</span></span>                              |
| <span data-ttu-id="5601a-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5601a-259">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5601a-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="5601a-260">System-Only</span></span>            | <span data-ttu-id="5601a-261">Richtig</span><span class="sxs-lookup"><span data-stu-id="5601a-261">True</span></span>                            |
| <span data-ttu-id="5601a-262">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5601a-262">Is-Single-Valued</span></span>       | <span data-ttu-id="5601a-263">False</span><span class="sxs-lookup"><span data-stu-id="5601a-263">False</span></span>                           |
| <span data-ttu-id="5601a-264">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5601a-264">Is Indexed</span></span>             | <span data-ttu-id="5601a-265">False</span><span class="sxs-lookup"><span data-stu-id="5601a-265">False</span></span>                           |
| <span data-ttu-id="5601a-266">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5601a-266">In Global Catalog</span></span>      | <span data-ttu-id="5601a-267">False</span><span class="sxs-lookup"><span data-stu-id="5601a-267">False</span></span>                           |
| <span data-ttu-id="5601a-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5601a-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="5601a-269">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5601a-269">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5601a-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5601a-270">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5601a-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5601a-271">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5601a-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5601a-272">Search-Flags</span></span>           | <span data-ttu-id="5601a-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5601a-273">0x00000000</span></span>                      |
| <span data-ttu-id="5601a-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5601a-274">System-Flags</span></span>           | <span data-ttu-id="5601a-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5601a-275">0x00000010</span></span>                      |
| <span data-ttu-id="5601a-276">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5601a-276">Classes used in</span></span>        | [<span data-ttu-id="5601a-277">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="5601a-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5601a-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5601a-278">Windows Server 2012</span></span>



| <span data-ttu-id="5601a-279">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5601a-279">Entry</span></span> | <span data-ttu-id="5601a-280">Wert</span><span class="sxs-lookup"><span data-stu-id="5601a-280">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5601a-281">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5601a-281">Link-Id</span></span>                | <span data-ttu-id="5601a-282">77</span><span class="sxs-lookup"><span data-stu-id="5601a-282">77</span></span>                              |
| <span data-ttu-id="5601a-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5601a-283">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5601a-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="5601a-284">System-Only</span></span>            | <span data-ttu-id="5601a-285">Richtig</span><span class="sxs-lookup"><span data-stu-id="5601a-285">True</span></span>                            |
| <span data-ttu-id="5601a-286">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5601a-286">Is-Single-Valued</span></span>       | <span data-ttu-id="5601a-287">False</span><span class="sxs-lookup"><span data-stu-id="5601a-287">False</span></span>                           |
| <span data-ttu-id="5601a-288">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5601a-288">Is Indexed</span></span>             | <span data-ttu-id="5601a-289">False</span><span class="sxs-lookup"><span data-stu-id="5601a-289">False</span></span>                           |
| <span data-ttu-id="5601a-290">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5601a-290">In Global Catalog</span></span>      | <span data-ttu-id="5601a-291">False</span><span class="sxs-lookup"><span data-stu-id="5601a-291">False</span></span>                           |
| <span data-ttu-id="5601a-292">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5601a-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="5601a-293">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5601a-293">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5601a-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5601a-294">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5601a-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5601a-295">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5601a-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5601a-296">Search-Flags</span></span>           | <span data-ttu-id="5601a-297">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5601a-297">0x00000000</span></span>                      |
| <span data-ttu-id="5601a-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5601a-298">System-Flags</span></span>           | <span data-ttu-id="5601a-299">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5601a-299">0x00000010</span></span>                      |
| <span data-ttu-id="5601a-300">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5601a-300">Classes used in</span></span>        | [<span data-ttu-id="5601a-301">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="5601a-301">**Top**</span></span>](c-top.md)<br/> |



 

 





