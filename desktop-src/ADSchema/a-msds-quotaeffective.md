---
title: ms-DS-Quota-effektives Attribut
description: Das effektive Kontingent für einen Sicherheits Prinzipal, der aus den zugewiesenen Kontingenten für eine Verzeichnis Partition berechnet wird.
ms.assetid: 22422499-9b56-4d74-a30e-63917abacdd1
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-Quota-effektives Attribut
- AD-Schema des msDS-quotaeffective-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Quota-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe610c87c356431883cecded5eda3e0a9c42297
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480362"
---
# <a name="ms-ds-quota-effective-attribute"></a><span data-ttu-id="bce43-105">ms-DS-Quota-effektives Attribut</span><span class="sxs-lookup"><span data-stu-id="bce43-105">ms-DS-Quota-Effective attribute</span></span>

<span data-ttu-id="bce43-106">Das effektive Kontingent für einen Sicherheits Prinzipal, der aus den zugewiesenen Kontingenten für eine Verzeichnis Partition berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="bce43-106">The effective quota for a security principal computed from the assigned quotas for a directory partition.</span></span>



| <span data-ttu-id="bce43-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bce43-107">Entry</span></span> | <span data-ttu-id="bce43-108">Wert</span><span class="sxs-lookup"><span data-stu-id="bce43-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="bce43-109">CN</span><span class="sxs-lookup"><span data-stu-id="bce43-109">CN</span></span>                | <span data-ttu-id="bce43-110">ms-DS-Kontingent-effektiv</span><span class="sxs-lookup"><span data-stu-id="bce43-110">ms-DS-Quota-Effective</span></span>                |
| <span data-ttu-id="bce43-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bce43-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bce43-112">MSDS-quotaeffective</span><span class="sxs-lookup"><span data-stu-id="bce43-112">msDS-QuotaEffective</span></span>                  |
| <span data-ttu-id="bce43-113">Size</span><span class="sxs-lookup"><span data-stu-id="bce43-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="bce43-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="bce43-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="bce43-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="bce43-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="bce43-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bce43-116">Attribute-Id</span></span>      | <span data-ttu-id="bce43-117">1.2.840.113556.1.4.1848</span><span class="sxs-lookup"><span data-stu-id="bce43-117">1.2.840.113556.1.4.1848</span></span>              |
| <span data-ttu-id="bce43-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bce43-118">System-Id-Guid</span></span>    | <span data-ttu-id="bce43-119">6655b152-101C-48b4-B347-e1lbc60157</span><span class="sxs-lookup"><span data-stu-id="bce43-119">6655b152-101c-48b4-b347-e1fcebc60157</span></span> |
| <span data-ttu-id="bce43-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="bce43-120">Syntax</span></span>            | [<span data-ttu-id="bce43-121">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="bce43-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="bce43-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="bce43-122">Implementations</span></span>

-   [<span data-ttu-id="bce43-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bce43-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bce43-124">**Adam**</span><span class="sxs-lookup"><span data-stu-id="bce43-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bce43-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bce43-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bce43-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bce43-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bce43-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bce43-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bce43-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bce43-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="bce43-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bce43-129">Windows Server 2003</span></span>



| <span data-ttu-id="bce43-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bce43-130">Entry</span></span> | <span data-ttu-id="bce43-131">Wert</span><span class="sxs-lookup"><span data-stu-id="bce43-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="bce43-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bce43-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bce43-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bce43-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bce43-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="bce43-134">System-Only</span></span>            | <span data-ttu-id="bce43-135">False</span><span class="sxs-lookup"><span data-stu-id="bce43-135">False</span></span>                                                             |
| <span data-ttu-id="bce43-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bce43-136">Is-Single-Valued</span></span>       | <span data-ttu-id="bce43-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="bce43-137">True</span></span>                                                              |
| <span data-ttu-id="bce43-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bce43-138">Is Indexed</span></span>             | <span data-ttu-id="bce43-139">False</span><span class="sxs-lookup"><span data-stu-id="bce43-139">False</span></span>                                                             |
| <span data-ttu-id="bce43-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bce43-140">In Global Catalog</span></span>      | <span data-ttu-id="bce43-141">False</span><span class="sxs-lookup"><span data-stu-id="bce43-141">False</span></span>                                                             |
| <span data-ttu-id="bce43-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bce43-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="bce43-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bce43-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="bce43-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bce43-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="bce43-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bce43-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="bce43-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bce43-146">Search-Flags</span></span>           | <span data-ttu-id="bce43-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bce43-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="bce43-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bce43-148">System-Flags</span></span>           | <span data-ttu-id="bce43-149">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bce43-149">0x00000014</span></span>                                                        |
| <span data-ttu-id="bce43-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bce43-150">Classes used in</span></span>        | [<span data-ttu-id="bce43-151">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="bce43-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bce43-152">Adam</span><span class="sxs-lookup"><span data-stu-id="bce43-152">ADAM</span></span>



| <span data-ttu-id="bce43-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bce43-153">Entry</span></span> | <span data-ttu-id="bce43-154">Wert</span><span class="sxs-lookup"><span data-stu-id="bce43-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="bce43-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bce43-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bce43-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bce43-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bce43-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="bce43-157">System-Only</span></span>            | <span data-ttu-id="bce43-158">False</span><span class="sxs-lookup"><span data-stu-id="bce43-158">False</span></span>                                                             |
| <span data-ttu-id="bce43-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bce43-159">Is-Single-Valued</span></span>       | <span data-ttu-id="bce43-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="bce43-160">True</span></span>                                                              |
| <span data-ttu-id="bce43-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bce43-161">Is Indexed</span></span>             | <span data-ttu-id="bce43-162">False</span><span class="sxs-lookup"><span data-stu-id="bce43-162">False</span></span>                                                             |
| <span data-ttu-id="bce43-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bce43-163">In Global Catalog</span></span>      | <span data-ttu-id="bce43-164">False</span><span class="sxs-lookup"><span data-stu-id="bce43-164">False</span></span>                                                             |
| <span data-ttu-id="bce43-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bce43-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="bce43-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bce43-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="bce43-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bce43-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="bce43-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bce43-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="bce43-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bce43-169">Search-Flags</span></span>           | <span data-ttu-id="bce43-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bce43-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="bce43-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bce43-171">System-Flags</span></span>           | <span data-ttu-id="bce43-172">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bce43-172">0x00000014</span></span>                                                        |
| <span data-ttu-id="bce43-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bce43-173">Classes used in</span></span>        | [<span data-ttu-id="bce43-174">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="bce43-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bce43-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bce43-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bce43-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bce43-176">Entry</span></span> | <span data-ttu-id="bce43-177">Wert</span><span class="sxs-lookup"><span data-stu-id="bce43-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="bce43-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bce43-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bce43-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bce43-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bce43-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="bce43-180">System-Only</span></span>            | <span data-ttu-id="bce43-181">False</span><span class="sxs-lookup"><span data-stu-id="bce43-181">False</span></span>                                                             |
| <span data-ttu-id="bce43-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bce43-182">Is-Single-Valued</span></span>       | <span data-ttu-id="bce43-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="bce43-183">True</span></span>                                                              |
| <span data-ttu-id="bce43-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bce43-184">Is Indexed</span></span>             | <span data-ttu-id="bce43-185">False</span><span class="sxs-lookup"><span data-stu-id="bce43-185">False</span></span>                                                             |
| <span data-ttu-id="bce43-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bce43-186">In Global Catalog</span></span>      | <span data-ttu-id="bce43-187">False</span><span class="sxs-lookup"><span data-stu-id="bce43-187">False</span></span>                                                             |
| <span data-ttu-id="bce43-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bce43-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="bce43-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bce43-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="bce43-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bce43-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="bce43-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bce43-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="bce43-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bce43-192">Search-Flags</span></span>           | <span data-ttu-id="bce43-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bce43-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="bce43-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bce43-194">System-Flags</span></span>           | <span data-ttu-id="bce43-195">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bce43-195">0x00000014</span></span>                                                        |
| <span data-ttu-id="bce43-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bce43-196">Classes used in</span></span>        | [<span data-ttu-id="bce43-197">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="bce43-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bce43-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bce43-198">Windows Server 2008</span></span>



| <span data-ttu-id="bce43-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bce43-199">Entry</span></span> | <span data-ttu-id="bce43-200">Wert</span><span class="sxs-lookup"><span data-stu-id="bce43-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="bce43-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bce43-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bce43-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bce43-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bce43-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="bce43-203">System-Only</span></span>            | <span data-ttu-id="bce43-204">False</span><span class="sxs-lookup"><span data-stu-id="bce43-204">False</span></span>                                                             |
| <span data-ttu-id="bce43-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bce43-205">Is-Single-Valued</span></span>       | <span data-ttu-id="bce43-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="bce43-206">True</span></span>                                                              |
| <span data-ttu-id="bce43-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bce43-207">Is Indexed</span></span>             | <span data-ttu-id="bce43-208">False</span><span class="sxs-lookup"><span data-stu-id="bce43-208">False</span></span>                                                             |
| <span data-ttu-id="bce43-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bce43-209">In Global Catalog</span></span>      | <span data-ttu-id="bce43-210">False</span><span class="sxs-lookup"><span data-stu-id="bce43-210">False</span></span>                                                             |
| <span data-ttu-id="bce43-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bce43-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="bce43-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bce43-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="bce43-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bce43-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="bce43-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bce43-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="bce43-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bce43-215">Search-Flags</span></span>           | <span data-ttu-id="bce43-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bce43-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="bce43-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bce43-217">System-Flags</span></span>           | <span data-ttu-id="bce43-218">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bce43-218">0x00000014</span></span>                                                        |
| <span data-ttu-id="bce43-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bce43-219">Classes used in</span></span>        | [<span data-ttu-id="bce43-220">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="bce43-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bce43-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bce43-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bce43-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bce43-222">Entry</span></span> | <span data-ttu-id="bce43-223">Wert</span><span class="sxs-lookup"><span data-stu-id="bce43-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="bce43-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bce43-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bce43-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bce43-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bce43-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="bce43-226">System-Only</span></span>            | <span data-ttu-id="bce43-227">False</span><span class="sxs-lookup"><span data-stu-id="bce43-227">False</span></span>                                                             |
| <span data-ttu-id="bce43-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bce43-228">Is-Single-Valued</span></span>       | <span data-ttu-id="bce43-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="bce43-229">True</span></span>                                                              |
| <span data-ttu-id="bce43-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bce43-230">Is Indexed</span></span>             | <span data-ttu-id="bce43-231">False</span><span class="sxs-lookup"><span data-stu-id="bce43-231">False</span></span>                                                             |
| <span data-ttu-id="bce43-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bce43-232">In Global Catalog</span></span>      | <span data-ttu-id="bce43-233">False</span><span class="sxs-lookup"><span data-stu-id="bce43-233">False</span></span>                                                             |
| <span data-ttu-id="bce43-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bce43-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="bce43-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bce43-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="bce43-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bce43-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="bce43-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bce43-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="bce43-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bce43-238">Search-Flags</span></span>           | <span data-ttu-id="bce43-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bce43-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="bce43-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bce43-240">System-Flags</span></span>           | <span data-ttu-id="bce43-241">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bce43-241">0x00000014</span></span>                                                        |
| <span data-ttu-id="bce43-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bce43-242">Classes used in</span></span>        | [<span data-ttu-id="bce43-243">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="bce43-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bce43-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bce43-244">Windows Server 2012</span></span>



| <span data-ttu-id="bce43-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bce43-245">Entry</span></span> | <span data-ttu-id="bce43-246">Wert</span><span class="sxs-lookup"><span data-stu-id="bce43-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="bce43-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bce43-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bce43-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bce43-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bce43-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="bce43-249">System-Only</span></span>            | <span data-ttu-id="bce43-250">False</span><span class="sxs-lookup"><span data-stu-id="bce43-250">False</span></span>                                                             |
| <span data-ttu-id="bce43-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bce43-251">Is-Single-Valued</span></span>       | <span data-ttu-id="bce43-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="bce43-252">True</span></span>                                                              |
| <span data-ttu-id="bce43-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bce43-253">Is Indexed</span></span>             | <span data-ttu-id="bce43-254">False</span><span class="sxs-lookup"><span data-stu-id="bce43-254">False</span></span>                                                             |
| <span data-ttu-id="bce43-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bce43-255">In Global Catalog</span></span>      | <span data-ttu-id="bce43-256">False</span><span class="sxs-lookup"><span data-stu-id="bce43-256">False</span></span>                                                             |
| <span data-ttu-id="bce43-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bce43-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="bce43-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bce43-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="bce43-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bce43-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="bce43-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bce43-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="bce43-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bce43-261">Search-Flags</span></span>           | <span data-ttu-id="bce43-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bce43-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="bce43-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bce43-263">System-Flags</span></span>           | <span data-ttu-id="bce43-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="bce43-264">0x00000014</span></span>                                                        |
| <span data-ttu-id="bce43-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bce43-265">Classes used in</span></span>        | [<span data-ttu-id="bce43-266">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="bce43-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





