---
title: ms-DS-Quota-Treuhänder-Attribut
description: Die SID des Sicherheits Prinzipals, für den das Kontingent zugewiesen wird.
ms.assetid: 4da8f731-0a8f-4d8a-a4e7-81ed881a30b5
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-Quota-Treuhänder-Attribut
- AD-Schema des msDS-quotatrustee-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Quota-Trustee
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7733e74c2f5d381aa6f52ea58bb03c377fab7cbe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344292"
---
# <a name="ms-ds-quota-trustee-attribute"></a><span data-ttu-id="57ea2-105">ms-DS-Quota-Treuhänder-Attribut</span><span class="sxs-lookup"><span data-stu-id="57ea2-105">ms-DS-Quota-Trustee attribute</span></span>

<span data-ttu-id="57ea2-106">Die SID des Sicherheits Prinzipals, für den das Kontingent zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="57ea2-106">The SID of the security principal for which the quota is being assigned.</span></span>



| <span data-ttu-id="57ea2-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="57ea2-107">Entry</span></span> | <span data-ttu-id="57ea2-108">Wert</span><span class="sxs-lookup"><span data-stu-id="57ea2-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="57ea2-109">CN</span><span class="sxs-lookup"><span data-stu-id="57ea2-109">CN</span></span>                | <span data-ttu-id="57ea2-110">ms-DS-Kontingent-Treuhänder</span><span class="sxs-lookup"><span data-stu-id="57ea2-110">ms-DS-Quota-Trustee</span></span>                  |
| <span data-ttu-id="57ea2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="57ea2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="57ea2-112">MSDS-quotatrustee</span><span class="sxs-lookup"><span data-stu-id="57ea2-112">msDS-QuotaTrustee</span></span>                    |
| <span data-ttu-id="57ea2-113">Size</span><span class="sxs-lookup"><span data-stu-id="57ea2-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="57ea2-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="57ea2-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="57ea2-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="57ea2-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="57ea2-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="57ea2-116">Attribute-Id</span></span>      | <span data-ttu-id="57ea2-117">1.2.840.113556.1.4.1844</span><span class="sxs-lookup"><span data-stu-id="57ea2-117">1.2.840.113556.1.4.1844</span></span>              |
| <span data-ttu-id="57ea2-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="57ea2-118">System-Id-Guid</span></span>    | <span data-ttu-id="57ea2-119">16378906-4ea5-49be-a8d1-bfd41dff4f65</span><span class="sxs-lookup"><span data-stu-id="57ea2-119">16378906-4ea5-49be-a8d1-bfd41dff4f65</span></span> |
| <span data-ttu-id="57ea2-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="57ea2-120">Syntax</span></span>            | [<span data-ttu-id="57ea2-121">**Zeichenfolge (SID)**</span><span class="sxs-lookup"><span data-stu-id="57ea2-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="57ea2-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="57ea2-122">Implementations</span></span>

-   [<span data-ttu-id="57ea2-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="57ea2-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="57ea2-124">**Adam**</span><span class="sxs-lookup"><span data-stu-id="57ea2-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="57ea2-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="57ea2-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="57ea2-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="57ea2-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="57ea2-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="57ea2-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="57ea2-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="57ea2-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="57ea2-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="57ea2-129">Windows Server 2003</span></span>



| <span data-ttu-id="57ea2-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="57ea2-130">Entry</span></span> | <span data-ttu-id="57ea2-131">Wert</span><span class="sxs-lookup"><span data-stu-id="57ea2-131">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="57ea2-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="57ea2-132">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="57ea2-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57ea2-133">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="57ea2-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="57ea2-134">System-Only</span></span>            | <span data-ttu-id="57ea2-135">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-135">False</span></span>                                                         |
| <span data-ttu-id="57ea2-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="57ea2-136">Is-Single-Valued</span></span>       | <span data-ttu-id="57ea2-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="57ea2-137">True</span></span>                                                          |
| <span data-ttu-id="57ea2-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="57ea2-138">Is Indexed</span></span>             | <span data-ttu-id="57ea2-139">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-139">False</span></span>                                                         |
| <span data-ttu-id="57ea2-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="57ea2-140">In Global Catalog</span></span>      | <span data-ttu-id="57ea2-141">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-141">False</span></span>                                                         |
| <span data-ttu-id="57ea2-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="57ea2-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="57ea2-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="57ea2-143">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="57ea2-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57ea2-144">Range-Lower</span></span>            | <span data-ttu-id="57ea2-145">0</span><span class="sxs-lookup"><span data-stu-id="57ea2-145">0</span></span>                                                             |
| <span data-ttu-id="57ea2-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57ea2-146">Range-Upper</span></span>            | <span data-ttu-id="57ea2-147">28</span><span class="sxs-lookup"><span data-stu-id="57ea2-147">28</span></span>                                                            |
| <span data-ttu-id="57ea2-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57ea2-148">Search-Flags</span></span>           | <span data-ttu-id="57ea2-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57ea2-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="57ea2-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57ea2-150">System-Flags</span></span>           | <span data-ttu-id="57ea2-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57ea2-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="57ea2-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="57ea2-152">Classes used in</span></span>        | [<span data-ttu-id="57ea2-153">**ms-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="57ea2-153">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="adam"></a><span data-ttu-id="57ea2-154">Adam</span><span class="sxs-lookup"><span data-stu-id="57ea2-154">ADAM</span></span>



| <span data-ttu-id="57ea2-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="57ea2-155">Entry</span></span> | <span data-ttu-id="57ea2-156">Wert</span><span class="sxs-lookup"><span data-stu-id="57ea2-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="57ea2-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="57ea2-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="57ea2-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57ea2-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="57ea2-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="57ea2-159">System-Only</span></span>            | <span data-ttu-id="57ea2-160">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-160">False</span></span>                                                         |
| <span data-ttu-id="57ea2-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="57ea2-161">Is-Single-Valued</span></span>       | <span data-ttu-id="57ea2-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="57ea2-162">True</span></span>                                                          |
| <span data-ttu-id="57ea2-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="57ea2-163">Is Indexed</span></span>             | <span data-ttu-id="57ea2-164">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-164">False</span></span>                                                         |
| <span data-ttu-id="57ea2-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="57ea2-165">In Global Catalog</span></span>      | <span data-ttu-id="57ea2-166">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-166">False</span></span>                                                         |
| <span data-ttu-id="57ea2-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="57ea2-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="57ea2-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="57ea2-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="57ea2-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57ea2-169">Range-Lower</span></span>            | <span data-ttu-id="57ea2-170">0</span><span class="sxs-lookup"><span data-stu-id="57ea2-170">0</span></span>                                                             |
| <span data-ttu-id="57ea2-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57ea2-171">Range-Upper</span></span>            | <span data-ttu-id="57ea2-172">28</span><span class="sxs-lookup"><span data-stu-id="57ea2-172">28</span></span>                                                            |
| <span data-ttu-id="57ea2-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57ea2-173">Search-Flags</span></span>           | <span data-ttu-id="57ea2-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57ea2-174">0x00000000</span></span>                                                    |
| <span data-ttu-id="57ea2-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57ea2-175">System-Flags</span></span>           | <span data-ttu-id="57ea2-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57ea2-176">0x00000010</span></span>                                                    |
| <span data-ttu-id="57ea2-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="57ea2-177">Classes used in</span></span>        | [<span data-ttu-id="57ea2-178">**ms-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="57ea2-178">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="57ea2-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="57ea2-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="57ea2-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="57ea2-180">Entry</span></span> | <span data-ttu-id="57ea2-181">Wert</span><span class="sxs-lookup"><span data-stu-id="57ea2-181">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="57ea2-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="57ea2-182">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="57ea2-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57ea2-183">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="57ea2-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="57ea2-184">System-Only</span></span>            | <span data-ttu-id="57ea2-185">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-185">False</span></span>                                                         |
| <span data-ttu-id="57ea2-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="57ea2-186">Is-Single-Valued</span></span>       | <span data-ttu-id="57ea2-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="57ea2-187">True</span></span>                                                          |
| <span data-ttu-id="57ea2-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="57ea2-188">Is Indexed</span></span>             | <span data-ttu-id="57ea2-189">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-189">False</span></span>                                                         |
| <span data-ttu-id="57ea2-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="57ea2-190">In Global Catalog</span></span>      | <span data-ttu-id="57ea2-191">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-191">False</span></span>                                                         |
| <span data-ttu-id="57ea2-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="57ea2-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="57ea2-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="57ea2-193">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="57ea2-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57ea2-194">Range-Lower</span></span>            | <span data-ttu-id="57ea2-195">0</span><span class="sxs-lookup"><span data-stu-id="57ea2-195">0</span></span>                                                             |
| <span data-ttu-id="57ea2-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57ea2-196">Range-Upper</span></span>            | <span data-ttu-id="57ea2-197">28</span><span class="sxs-lookup"><span data-stu-id="57ea2-197">28</span></span>                                                            |
| <span data-ttu-id="57ea2-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57ea2-198">Search-Flags</span></span>           | <span data-ttu-id="57ea2-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57ea2-199">0x00000000</span></span>                                                    |
| <span data-ttu-id="57ea2-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57ea2-200">System-Flags</span></span>           | <span data-ttu-id="57ea2-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57ea2-201">0x00000010</span></span>                                                    |
| <span data-ttu-id="57ea2-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="57ea2-202">Classes used in</span></span>        | [<span data-ttu-id="57ea2-203">**ms-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="57ea2-203">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="57ea2-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57ea2-204">Windows Server 2008</span></span>



| <span data-ttu-id="57ea2-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="57ea2-205">Entry</span></span> | <span data-ttu-id="57ea2-206">Wert</span><span class="sxs-lookup"><span data-stu-id="57ea2-206">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="57ea2-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="57ea2-207">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="57ea2-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57ea2-208">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="57ea2-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="57ea2-209">System-Only</span></span>            | <span data-ttu-id="57ea2-210">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-210">False</span></span>                                                         |
| <span data-ttu-id="57ea2-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="57ea2-211">Is-Single-Valued</span></span>       | <span data-ttu-id="57ea2-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="57ea2-212">True</span></span>                                                          |
| <span data-ttu-id="57ea2-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="57ea2-213">Is Indexed</span></span>             | <span data-ttu-id="57ea2-214">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-214">False</span></span>                                                         |
| <span data-ttu-id="57ea2-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="57ea2-215">In Global Catalog</span></span>      | <span data-ttu-id="57ea2-216">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-216">False</span></span>                                                         |
| <span data-ttu-id="57ea2-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="57ea2-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="57ea2-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="57ea2-218">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="57ea2-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57ea2-219">Range-Lower</span></span>            | <span data-ttu-id="57ea2-220">0</span><span class="sxs-lookup"><span data-stu-id="57ea2-220">0</span></span>                                                             |
| <span data-ttu-id="57ea2-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57ea2-221">Range-Upper</span></span>            | <span data-ttu-id="57ea2-222">28</span><span class="sxs-lookup"><span data-stu-id="57ea2-222">28</span></span>                                                            |
| <span data-ttu-id="57ea2-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57ea2-223">Search-Flags</span></span>           | <span data-ttu-id="57ea2-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57ea2-224">0x00000000</span></span>                                                    |
| <span data-ttu-id="57ea2-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57ea2-225">System-Flags</span></span>           | <span data-ttu-id="57ea2-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57ea2-226">0x00000010</span></span>                                                    |
| <span data-ttu-id="57ea2-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="57ea2-227">Classes used in</span></span>        | [<span data-ttu-id="57ea2-228">**ms-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="57ea2-228">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="57ea2-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="57ea2-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="57ea2-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="57ea2-230">Entry</span></span> | <span data-ttu-id="57ea2-231">Wert</span><span class="sxs-lookup"><span data-stu-id="57ea2-231">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="57ea2-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="57ea2-232">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="57ea2-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57ea2-233">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="57ea2-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="57ea2-234">System-Only</span></span>            | <span data-ttu-id="57ea2-235">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-235">False</span></span>                                                         |
| <span data-ttu-id="57ea2-236">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="57ea2-236">Is-Single-Valued</span></span>       | <span data-ttu-id="57ea2-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="57ea2-237">True</span></span>                                                          |
| <span data-ttu-id="57ea2-238">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="57ea2-238">Is Indexed</span></span>             | <span data-ttu-id="57ea2-239">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-239">False</span></span>                                                         |
| <span data-ttu-id="57ea2-240">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="57ea2-240">In Global Catalog</span></span>      | <span data-ttu-id="57ea2-241">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-241">False</span></span>                                                         |
| <span data-ttu-id="57ea2-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="57ea2-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="57ea2-243">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="57ea2-243">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="57ea2-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57ea2-244">Range-Lower</span></span>            | <span data-ttu-id="57ea2-245">0</span><span class="sxs-lookup"><span data-stu-id="57ea2-245">0</span></span>                                                             |
| <span data-ttu-id="57ea2-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57ea2-246">Range-Upper</span></span>            | <span data-ttu-id="57ea2-247">28</span><span class="sxs-lookup"><span data-stu-id="57ea2-247">28</span></span>                                                            |
| <span data-ttu-id="57ea2-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57ea2-248">Search-Flags</span></span>           | <span data-ttu-id="57ea2-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57ea2-249">0x00000000</span></span>                                                    |
| <span data-ttu-id="57ea2-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57ea2-250">System-Flags</span></span>           | <span data-ttu-id="57ea2-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57ea2-251">0x00000010</span></span>                                                    |
| <span data-ttu-id="57ea2-252">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="57ea2-252">Classes used in</span></span>        | [<span data-ttu-id="57ea2-253">**ms-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="57ea2-253">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="57ea2-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="57ea2-254">Windows Server 2012</span></span>



| <span data-ttu-id="57ea2-255">Eingabe</span><span class="sxs-lookup"><span data-stu-id="57ea2-255">Entry</span></span> | <span data-ttu-id="57ea2-256">Wert</span><span class="sxs-lookup"><span data-stu-id="57ea2-256">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="57ea2-257">Link-ID</span><span class="sxs-lookup"><span data-stu-id="57ea2-257">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="57ea2-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57ea2-258">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="57ea2-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="57ea2-259">System-Only</span></span>            | <span data-ttu-id="57ea2-260">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-260">False</span></span>                                                         |
| <span data-ttu-id="57ea2-261">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="57ea2-261">Is-Single-Valued</span></span>       | <span data-ttu-id="57ea2-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="57ea2-262">True</span></span>                                                          |
| <span data-ttu-id="57ea2-263">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="57ea2-263">Is Indexed</span></span>             | <span data-ttu-id="57ea2-264">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-264">False</span></span>                                                         |
| <span data-ttu-id="57ea2-265">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="57ea2-265">In Global Catalog</span></span>      | <span data-ttu-id="57ea2-266">False</span><span class="sxs-lookup"><span data-stu-id="57ea2-266">False</span></span>                                                         |
| <span data-ttu-id="57ea2-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="57ea2-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="57ea2-268">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="57ea2-268">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="57ea2-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57ea2-269">Range-Lower</span></span>            | <span data-ttu-id="57ea2-270">0</span><span class="sxs-lookup"><span data-stu-id="57ea2-270">0</span></span>                                                             |
| <span data-ttu-id="57ea2-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57ea2-271">Range-Upper</span></span>            | <span data-ttu-id="57ea2-272">28</span><span class="sxs-lookup"><span data-stu-id="57ea2-272">28</span></span>                                                            |
| <span data-ttu-id="57ea2-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57ea2-273">Search-Flags</span></span>           | <span data-ttu-id="57ea2-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57ea2-274">0x00000000</span></span>                                                    |
| <span data-ttu-id="57ea2-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57ea2-275">System-Flags</span></span>           | <span data-ttu-id="57ea2-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57ea2-276">0x00000010</span></span>                                                    |
| <span data-ttu-id="57ea2-277">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="57ea2-277">Classes used in</span></span>        | [<span data-ttu-id="57ea2-278">**ms-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="57ea2-278">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



 

 





