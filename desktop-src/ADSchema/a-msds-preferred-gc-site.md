---
title: ms-DS-Preferred-GC-Site-Attribut
description: Das Attribut "ms-DS-Preferred-GC-Site" wird vom Sicherheits Konten-Manager für die Gruppen Erweiterung während der tokenbewertung verwendet.
ms.assetid: f42d3787-4063-4804-a7b5-4798516ad47e
ms.tgt_platform: multiple
keywords:
- ms-DS-Preferred-GC-Site-Attribut AD-Schema
- "\"msDS-Preferred-GC-Site Attribute ad Schema\""
topic_type:
- apiref
api_name:
- ms-DS-Preferred-GC-Site
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172e12758ba0b365fa195cb4e1384c161cea3d14
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104213771"
---
# <a name="ms-ds-preferred-gc-site-attribute"></a><span data-ttu-id="df3ef-105">ms-DS-Preferred-GC-Site-Attribut</span><span class="sxs-lookup"><span data-stu-id="df3ef-105">ms-DS-Preferred-GC-Site attribute</span></span>

<span data-ttu-id="df3ef-106">Das Attribut " **ms-DS-Preferred-GC-Site** " wird vom Sicherheits Konten-Manager für die Gruppen Erweiterung während der tokenbewertung verwendet.</span><span class="sxs-lookup"><span data-stu-id="df3ef-106">The **ms-DS-Preferred-GC-Site** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="df3ef-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="df3ef-107">Entry</span></span> | <span data-ttu-id="df3ef-108">Wert</span><span class="sxs-lookup"><span data-stu-id="df3ef-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="df3ef-109">CN</span><span class="sxs-lookup"><span data-stu-id="df3ef-109">CN</span></span>                | <span data-ttu-id="df3ef-110">ms-DS-bevorzugt-GC-Site</span><span class="sxs-lookup"><span data-stu-id="df3ef-110">ms-DS-Preferred-GC-Site</span></span>                 |
| <span data-ttu-id="df3ef-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="df3ef-111">Ldap-Display-Name</span></span> | <span data-ttu-id="df3ef-112">MSDS-bevorzugt-GC-Site</span><span class="sxs-lookup"><span data-stu-id="df3ef-112">msDS-Preferred-GC-Site</span></span>                  |
| <span data-ttu-id="df3ef-113">Size</span><span class="sxs-lookup"><span data-stu-id="df3ef-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="df3ef-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="df3ef-114">Update Privilege</span></span>  | <span data-ttu-id="df3ef-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="df3ef-115">Domain administrator</span></span>                    |
| <span data-ttu-id="df3ef-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="df3ef-116">Update Frequency</span></span>  | <span data-ttu-id="df3ef-117">Nach Ermessen des Administrators.</span><span class="sxs-lookup"><span data-stu-id="df3ef-117">At the administrator's discretion.</span></span>      |
| <span data-ttu-id="df3ef-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="df3ef-118">Attribute-Id</span></span>      | <span data-ttu-id="df3ef-119">1.2.840.113556.1.4.1444</span><span class="sxs-lookup"><span data-stu-id="df3ef-119">1.2.840.113556.1.4.1444</span></span>                 |
| <span data-ttu-id="df3ef-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="df3ef-120">System-Id-Guid</span></span>    | <span data-ttu-id="df3ef-121">d921b50a-0ab2-42cd-87f6-09cf83a91854</span><span class="sxs-lookup"><span data-stu-id="df3ef-121">d921b50a-0ab2-42cd-87f6-09cf83a91854</span></span>    |
| <span data-ttu-id="df3ef-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="df3ef-122">Syntax</span></span>            | [<span data-ttu-id="df3ef-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="df3ef-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="df3ef-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="df3ef-124">Implementations</span></span>

-   [<span data-ttu-id="df3ef-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="df3ef-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="df3ef-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="df3ef-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="df3ef-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="df3ef-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="df3ef-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="df3ef-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="df3ef-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="df3ef-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="df3ef-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="df3ef-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="df3ef-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="df3ef-131">Windows Server 2003</span></span>



| <span data-ttu-id="df3ef-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="df3ef-132">Entry</span></span> | <span data-ttu-id="df3ef-133">Wert</span><span class="sxs-lookup"><span data-stu-id="df3ef-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="df3ef-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="df3ef-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="df3ef-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df3ef-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="df3ef-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="df3ef-136">System-Only</span></span>            | <span data-ttu-id="df3ef-137">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-137">False</span></span>                                                       |
| <span data-ttu-id="df3ef-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="df3ef-138">Is-Single-Valued</span></span>       | <span data-ttu-id="df3ef-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="df3ef-139">True</span></span>                                                        |
| <span data-ttu-id="df3ef-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="df3ef-140">Is Indexed</span></span>             | <span data-ttu-id="df3ef-141">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-141">False</span></span>                                                       |
| <span data-ttu-id="df3ef-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="df3ef-142">In Global Catalog</span></span>      | <span data-ttu-id="df3ef-143">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-143">False</span></span>                                                       |
| <span data-ttu-id="df3ef-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df3ef-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="df3ef-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="df3ef-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="df3ef-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df3ef-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="df3ef-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df3ef-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="df3ef-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df3ef-148">Search-Flags</span></span>           | <span data-ttu-id="df3ef-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df3ef-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="df3ef-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df3ef-150">System-Flags</span></span>           | <span data-ttu-id="df3ef-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df3ef-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="df3ef-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="df3ef-152">Classes used in</span></span>        | [<span data-ttu-id="df3ef-153">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="df3ef-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="df3ef-154">Adam</span><span class="sxs-lookup"><span data-stu-id="df3ef-154">ADAM</span></span>



| <span data-ttu-id="df3ef-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="df3ef-155">Entry</span></span> | <span data-ttu-id="df3ef-156">Wert</span><span class="sxs-lookup"><span data-stu-id="df3ef-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="df3ef-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="df3ef-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="df3ef-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df3ef-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="df3ef-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="df3ef-159">System-Only</span></span>            | <span data-ttu-id="df3ef-160">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-160">False</span></span>                                                       |
| <span data-ttu-id="df3ef-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="df3ef-161">Is-Single-Valued</span></span>       | <span data-ttu-id="df3ef-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="df3ef-162">True</span></span>                                                        |
| <span data-ttu-id="df3ef-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="df3ef-163">Is Indexed</span></span>             | <span data-ttu-id="df3ef-164">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-164">False</span></span>                                                       |
| <span data-ttu-id="df3ef-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="df3ef-165">In Global Catalog</span></span>      | <span data-ttu-id="df3ef-166">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-166">False</span></span>                                                       |
| <span data-ttu-id="df3ef-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df3ef-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="df3ef-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="df3ef-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="df3ef-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df3ef-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="df3ef-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df3ef-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="df3ef-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df3ef-171">Search-Flags</span></span>           | <span data-ttu-id="df3ef-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df3ef-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="df3ef-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df3ef-173">System-Flags</span></span>           | <span data-ttu-id="df3ef-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df3ef-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="df3ef-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="df3ef-175">Classes used in</span></span>        | [<span data-ttu-id="df3ef-176">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="df3ef-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="df3ef-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="df3ef-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="df3ef-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="df3ef-178">Entry</span></span> | <span data-ttu-id="df3ef-179">Wert</span><span class="sxs-lookup"><span data-stu-id="df3ef-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="df3ef-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="df3ef-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="df3ef-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df3ef-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="df3ef-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="df3ef-182">System-Only</span></span>            | <span data-ttu-id="df3ef-183">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-183">False</span></span>                                                       |
| <span data-ttu-id="df3ef-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="df3ef-184">Is-Single-Valued</span></span>       | <span data-ttu-id="df3ef-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="df3ef-185">True</span></span>                                                        |
| <span data-ttu-id="df3ef-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="df3ef-186">Is Indexed</span></span>             | <span data-ttu-id="df3ef-187">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-187">False</span></span>                                                       |
| <span data-ttu-id="df3ef-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="df3ef-188">In Global Catalog</span></span>      | <span data-ttu-id="df3ef-189">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-189">False</span></span>                                                       |
| <span data-ttu-id="df3ef-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df3ef-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="df3ef-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="df3ef-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="df3ef-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df3ef-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="df3ef-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df3ef-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="df3ef-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df3ef-194">Search-Flags</span></span>           | <span data-ttu-id="df3ef-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df3ef-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="df3ef-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df3ef-196">System-Flags</span></span>           | <span data-ttu-id="df3ef-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df3ef-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="df3ef-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="df3ef-198">Classes used in</span></span>        | [<span data-ttu-id="df3ef-199">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="df3ef-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="df3ef-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df3ef-200">Windows Server 2008</span></span>



| <span data-ttu-id="df3ef-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="df3ef-201">Entry</span></span> | <span data-ttu-id="df3ef-202">Wert</span><span class="sxs-lookup"><span data-stu-id="df3ef-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="df3ef-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="df3ef-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="df3ef-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df3ef-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="df3ef-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="df3ef-205">System-Only</span></span>            | <span data-ttu-id="df3ef-206">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-206">False</span></span>                                                       |
| <span data-ttu-id="df3ef-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="df3ef-207">Is-Single-Valued</span></span>       | <span data-ttu-id="df3ef-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="df3ef-208">True</span></span>                                                        |
| <span data-ttu-id="df3ef-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="df3ef-209">Is Indexed</span></span>             | <span data-ttu-id="df3ef-210">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-210">False</span></span>                                                       |
| <span data-ttu-id="df3ef-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="df3ef-211">In Global Catalog</span></span>      | <span data-ttu-id="df3ef-212">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-212">False</span></span>                                                       |
| <span data-ttu-id="df3ef-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df3ef-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="df3ef-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="df3ef-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="df3ef-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df3ef-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="df3ef-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df3ef-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="df3ef-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df3ef-217">Search-Flags</span></span>           | <span data-ttu-id="df3ef-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df3ef-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="df3ef-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df3ef-219">System-Flags</span></span>           | <span data-ttu-id="df3ef-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df3ef-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="df3ef-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="df3ef-221">Classes used in</span></span>        | [<span data-ttu-id="df3ef-222">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="df3ef-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="df3ef-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="df3ef-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="df3ef-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="df3ef-224">Entry</span></span> | <span data-ttu-id="df3ef-225">Wert</span><span class="sxs-lookup"><span data-stu-id="df3ef-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="df3ef-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="df3ef-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="df3ef-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df3ef-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="df3ef-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="df3ef-228">System-Only</span></span>            | <span data-ttu-id="df3ef-229">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-229">False</span></span>                                                       |
| <span data-ttu-id="df3ef-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="df3ef-230">Is-Single-Valued</span></span>       | <span data-ttu-id="df3ef-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="df3ef-231">True</span></span>                                                        |
| <span data-ttu-id="df3ef-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="df3ef-232">Is Indexed</span></span>             | <span data-ttu-id="df3ef-233">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-233">False</span></span>                                                       |
| <span data-ttu-id="df3ef-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="df3ef-234">In Global Catalog</span></span>      | <span data-ttu-id="df3ef-235">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-235">False</span></span>                                                       |
| <span data-ttu-id="df3ef-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df3ef-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="df3ef-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="df3ef-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="df3ef-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df3ef-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="df3ef-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df3ef-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="df3ef-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df3ef-240">Search-Flags</span></span>           | <span data-ttu-id="df3ef-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df3ef-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="df3ef-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df3ef-242">System-Flags</span></span>           | <span data-ttu-id="df3ef-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df3ef-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="df3ef-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="df3ef-244">Classes used in</span></span>        | [<span data-ttu-id="df3ef-245">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="df3ef-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="df3ef-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="df3ef-246">Windows Server 2012</span></span>



| <span data-ttu-id="df3ef-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="df3ef-247">Entry</span></span> | <span data-ttu-id="df3ef-248">Wert</span><span class="sxs-lookup"><span data-stu-id="df3ef-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="df3ef-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="df3ef-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="df3ef-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df3ef-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="df3ef-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="df3ef-251">System-Only</span></span>            | <span data-ttu-id="df3ef-252">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-252">False</span></span>                                                       |
| <span data-ttu-id="df3ef-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="df3ef-253">Is-Single-Valued</span></span>       | <span data-ttu-id="df3ef-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="df3ef-254">True</span></span>                                                        |
| <span data-ttu-id="df3ef-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="df3ef-255">Is Indexed</span></span>             | <span data-ttu-id="df3ef-256">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-256">False</span></span>                                                       |
| <span data-ttu-id="df3ef-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="df3ef-257">In Global Catalog</span></span>      | <span data-ttu-id="df3ef-258">False</span><span class="sxs-lookup"><span data-stu-id="df3ef-258">False</span></span>                                                       |
| <span data-ttu-id="df3ef-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df3ef-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="df3ef-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="df3ef-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="df3ef-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df3ef-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="df3ef-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df3ef-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="df3ef-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df3ef-263">Search-Flags</span></span>           | <span data-ttu-id="df3ef-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df3ef-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="df3ef-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df3ef-265">System-Flags</span></span>           | <span data-ttu-id="df3ef-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df3ef-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="df3ef-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="df3ef-267">Classes used in</span></span>        | [<span data-ttu-id="df3ef-268">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="df3ef-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





