---
title: ms-DS-Top-Quota-Usage-Attribut
description: Die Liste der obersten Kontingent Benutzer, die sich zurzeit in der Verzeichnis Datenbank befinden, geordnet nach absteigender Kontingent Auslastung.
ms.assetid: c52db8c8-233c-495f-b3fe-edbe1d723677
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-Top-Quota-Usage-Attribut
- AD-Schema des msDS-topquotausage-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Top-Quota-Usage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db787c0360eff64c726ec680c9fd2a18da1e8d1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342527"
---
# <a name="ms-ds-top-quota-usage-attribute"></a><span data-ttu-id="af881-105">ms-DS-Top-Quota-Usage-Attribut</span><span class="sxs-lookup"><span data-stu-id="af881-105">ms-DS-Top-Quota-Usage attribute</span></span>

<span data-ttu-id="af881-106">Die Liste der obersten Kontingent Benutzer, die sich zurzeit in der Verzeichnis Datenbank befinden, geordnet nach absteigender Kontingent Auslastung.</span><span class="sxs-lookup"><span data-stu-id="af881-106">The list of top quota users currently in the directory database, ordered by decreasing quota usage.</span></span>



| <span data-ttu-id="af881-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="af881-107">Entry</span></span> | <span data-ttu-id="af881-108">Wert</span><span class="sxs-lookup"><span data-stu-id="af881-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="af881-109">CN</span><span class="sxs-lookup"><span data-stu-id="af881-109">CN</span></span>                | <span data-ttu-id="af881-110">ms-DS-Top-Quota-Usage</span><span class="sxs-lookup"><span data-stu-id="af881-110">ms-DS-Top-Quota-Usage</span></span>                       |
| <span data-ttu-id="af881-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="af881-111">Ldap-Display-Name</span></span> | <span data-ttu-id="af881-112">MSDS-topquotausage</span><span class="sxs-lookup"><span data-stu-id="af881-112">msDS-TopQuotaUsage</span></span>                          |
| <span data-ttu-id="af881-113">Size</span><span class="sxs-lookup"><span data-stu-id="af881-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="af881-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="af881-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="af881-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="af881-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="af881-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="af881-116">Attribute-Id</span></span>      | <span data-ttu-id="af881-117">1.2.840.113556.1.4.1850</span><span class="sxs-lookup"><span data-stu-id="af881-117">1.2.840.113556.1.4.1850</span></span>                     |
| <span data-ttu-id="af881-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="af881-118">System-Id-Guid</span></span>    | <span data-ttu-id="af881-119">7b7cce4f-f1f5-4bb6-b7eb-23504af19e75</span><span class="sxs-lookup"><span data-stu-id="af881-119">7b7cce4f-f1f5-4bb6-b7eb-23504af19e75</span></span>        |
| <span data-ttu-id="af881-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="af881-120">Syntax</span></span>            | [<span data-ttu-id="af881-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="af881-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="af881-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="af881-122">Implementations</span></span>

-   [<span data-ttu-id="af881-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="af881-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="af881-124">**Adam**</span><span class="sxs-lookup"><span data-stu-id="af881-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="af881-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="af881-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="af881-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="af881-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="af881-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="af881-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="af881-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="af881-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="af881-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af881-129">Windows Server 2003</span></span>



| <span data-ttu-id="af881-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="af881-130">Entry</span></span> | <span data-ttu-id="af881-131">Wert</span><span class="sxs-lookup"><span data-stu-id="af881-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="af881-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="af881-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="af881-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af881-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="af881-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="af881-134">System-Only</span></span>            | <span data-ttu-id="af881-135">False</span><span class="sxs-lookup"><span data-stu-id="af881-135">False</span></span>                                                             |
| <span data-ttu-id="af881-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="af881-136">Is-Single-Valued</span></span>       | <span data-ttu-id="af881-137">False</span><span class="sxs-lookup"><span data-stu-id="af881-137">False</span></span>                                                             |
| <span data-ttu-id="af881-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="af881-138">Is Indexed</span></span>             | <span data-ttu-id="af881-139">False</span><span class="sxs-lookup"><span data-stu-id="af881-139">False</span></span>                                                             |
| <span data-ttu-id="af881-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="af881-140">In Global Catalog</span></span>      | <span data-ttu-id="af881-141">False</span><span class="sxs-lookup"><span data-stu-id="af881-141">False</span></span>                                                             |
| <span data-ttu-id="af881-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="af881-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="af881-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="af881-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="af881-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af881-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="af881-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af881-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="af881-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af881-146">Search-Flags</span></span>           | <span data-ttu-id="af881-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af881-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="af881-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af881-148">System-Flags</span></span>           | <span data-ttu-id="af881-149">0x00000014</span><span class="sxs-lookup"><span data-stu-id="af881-149">0x00000014</span></span>                                                        |
| <span data-ttu-id="af881-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="af881-150">Classes used in</span></span>        | [<span data-ttu-id="af881-151">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="af881-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="af881-152">Adam</span><span class="sxs-lookup"><span data-stu-id="af881-152">ADAM</span></span>



| <span data-ttu-id="af881-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="af881-153">Entry</span></span> | <span data-ttu-id="af881-154">Wert</span><span class="sxs-lookup"><span data-stu-id="af881-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="af881-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="af881-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="af881-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af881-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="af881-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="af881-157">System-Only</span></span>            | <span data-ttu-id="af881-158">False</span><span class="sxs-lookup"><span data-stu-id="af881-158">False</span></span>                                                             |
| <span data-ttu-id="af881-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="af881-159">Is-Single-Valued</span></span>       | <span data-ttu-id="af881-160">False</span><span class="sxs-lookup"><span data-stu-id="af881-160">False</span></span>                                                             |
| <span data-ttu-id="af881-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="af881-161">Is Indexed</span></span>             | <span data-ttu-id="af881-162">False</span><span class="sxs-lookup"><span data-stu-id="af881-162">False</span></span>                                                             |
| <span data-ttu-id="af881-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="af881-163">In Global Catalog</span></span>      | <span data-ttu-id="af881-164">False</span><span class="sxs-lookup"><span data-stu-id="af881-164">False</span></span>                                                             |
| <span data-ttu-id="af881-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="af881-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="af881-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="af881-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="af881-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af881-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="af881-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af881-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="af881-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af881-169">Search-Flags</span></span>           | <span data-ttu-id="af881-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af881-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="af881-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af881-171">System-Flags</span></span>           | <span data-ttu-id="af881-172">0x00000014</span><span class="sxs-lookup"><span data-stu-id="af881-172">0x00000014</span></span>                                                        |
| <span data-ttu-id="af881-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="af881-173">Classes used in</span></span>        | [<span data-ttu-id="af881-174">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="af881-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="af881-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="af881-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="af881-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="af881-176">Entry</span></span> | <span data-ttu-id="af881-177">Wert</span><span class="sxs-lookup"><span data-stu-id="af881-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="af881-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="af881-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="af881-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af881-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="af881-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="af881-180">System-Only</span></span>            | <span data-ttu-id="af881-181">False</span><span class="sxs-lookup"><span data-stu-id="af881-181">False</span></span>                                                             |
| <span data-ttu-id="af881-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="af881-182">Is-Single-Valued</span></span>       | <span data-ttu-id="af881-183">False</span><span class="sxs-lookup"><span data-stu-id="af881-183">False</span></span>                                                             |
| <span data-ttu-id="af881-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="af881-184">Is Indexed</span></span>             | <span data-ttu-id="af881-185">False</span><span class="sxs-lookup"><span data-stu-id="af881-185">False</span></span>                                                             |
| <span data-ttu-id="af881-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="af881-186">In Global Catalog</span></span>      | <span data-ttu-id="af881-187">False</span><span class="sxs-lookup"><span data-stu-id="af881-187">False</span></span>                                                             |
| <span data-ttu-id="af881-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="af881-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="af881-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="af881-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="af881-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af881-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="af881-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af881-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="af881-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af881-192">Search-Flags</span></span>           | <span data-ttu-id="af881-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af881-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="af881-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af881-194">System-Flags</span></span>           | <span data-ttu-id="af881-195">0x00000014</span><span class="sxs-lookup"><span data-stu-id="af881-195">0x00000014</span></span>                                                        |
| <span data-ttu-id="af881-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="af881-196">Classes used in</span></span>        | [<span data-ttu-id="af881-197">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="af881-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="af881-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af881-198">Windows Server 2008</span></span>



| <span data-ttu-id="af881-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="af881-199">Entry</span></span> | <span data-ttu-id="af881-200">Wert</span><span class="sxs-lookup"><span data-stu-id="af881-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="af881-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="af881-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="af881-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af881-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="af881-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="af881-203">System-Only</span></span>            | <span data-ttu-id="af881-204">False</span><span class="sxs-lookup"><span data-stu-id="af881-204">False</span></span>                                                             |
| <span data-ttu-id="af881-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="af881-205">Is-Single-Valued</span></span>       | <span data-ttu-id="af881-206">False</span><span class="sxs-lookup"><span data-stu-id="af881-206">False</span></span>                                                             |
| <span data-ttu-id="af881-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="af881-207">Is Indexed</span></span>             | <span data-ttu-id="af881-208">False</span><span class="sxs-lookup"><span data-stu-id="af881-208">False</span></span>                                                             |
| <span data-ttu-id="af881-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="af881-209">In Global Catalog</span></span>      | <span data-ttu-id="af881-210">False</span><span class="sxs-lookup"><span data-stu-id="af881-210">False</span></span>                                                             |
| <span data-ttu-id="af881-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="af881-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="af881-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="af881-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="af881-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af881-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="af881-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af881-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="af881-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af881-215">Search-Flags</span></span>           | <span data-ttu-id="af881-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af881-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="af881-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af881-217">System-Flags</span></span>           | <span data-ttu-id="af881-218">0x00000014</span><span class="sxs-lookup"><span data-stu-id="af881-218">0x00000014</span></span>                                                        |
| <span data-ttu-id="af881-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="af881-219">Classes used in</span></span>        | [<span data-ttu-id="af881-220">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="af881-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="af881-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="af881-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="af881-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="af881-222">Entry</span></span> | <span data-ttu-id="af881-223">Wert</span><span class="sxs-lookup"><span data-stu-id="af881-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="af881-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="af881-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="af881-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af881-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="af881-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="af881-226">System-Only</span></span>            | <span data-ttu-id="af881-227">False</span><span class="sxs-lookup"><span data-stu-id="af881-227">False</span></span>                                                             |
| <span data-ttu-id="af881-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="af881-228">Is-Single-Valued</span></span>       | <span data-ttu-id="af881-229">False</span><span class="sxs-lookup"><span data-stu-id="af881-229">False</span></span>                                                             |
| <span data-ttu-id="af881-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="af881-230">Is Indexed</span></span>             | <span data-ttu-id="af881-231">False</span><span class="sxs-lookup"><span data-stu-id="af881-231">False</span></span>                                                             |
| <span data-ttu-id="af881-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="af881-232">In Global Catalog</span></span>      | <span data-ttu-id="af881-233">False</span><span class="sxs-lookup"><span data-stu-id="af881-233">False</span></span>                                                             |
| <span data-ttu-id="af881-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="af881-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="af881-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="af881-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="af881-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af881-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="af881-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af881-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="af881-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af881-238">Search-Flags</span></span>           | <span data-ttu-id="af881-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af881-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="af881-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af881-240">System-Flags</span></span>           | <span data-ttu-id="af881-241">0x00000014</span><span class="sxs-lookup"><span data-stu-id="af881-241">0x00000014</span></span>                                                        |
| <span data-ttu-id="af881-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="af881-242">Classes used in</span></span>        | [<span data-ttu-id="af881-243">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="af881-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="af881-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="af881-244">Windows Server 2012</span></span>



| <span data-ttu-id="af881-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="af881-245">Entry</span></span> | <span data-ttu-id="af881-246">Wert</span><span class="sxs-lookup"><span data-stu-id="af881-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="af881-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="af881-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="af881-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af881-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="af881-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="af881-249">System-Only</span></span>            | <span data-ttu-id="af881-250">False</span><span class="sxs-lookup"><span data-stu-id="af881-250">False</span></span>                                                             |
| <span data-ttu-id="af881-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="af881-251">Is-Single-Valued</span></span>       | <span data-ttu-id="af881-252">False</span><span class="sxs-lookup"><span data-stu-id="af881-252">False</span></span>                                                             |
| <span data-ttu-id="af881-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="af881-253">Is Indexed</span></span>             | <span data-ttu-id="af881-254">False</span><span class="sxs-lookup"><span data-stu-id="af881-254">False</span></span>                                                             |
| <span data-ttu-id="af881-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="af881-255">In Global Catalog</span></span>      | <span data-ttu-id="af881-256">False</span><span class="sxs-lookup"><span data-stu-id="af881-256">False</span></span>                                                             |
| <span data-ttu-id="af881-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="af881-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="af881-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="af881-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="af881-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af881-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="af881-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af881-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="af881-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af881-261">Search-Flags</span></span>           | <span data-ttu-id="af881-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af881-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="af881-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af881-263">System-Flags</span></span>           | <span data-ttu-id="af881-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="af881-264">0x00000014</span></span>                                                        |
| <span data-ttu-id="af881-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="af881-265">Classes used in</span></span>        | [<span data-ttu-id="af881-266">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="af881-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





