---
title: ms-DS-AZ-Domain-Timeout-Attribut
description: Zeit (in Millisekunden), nach der erkannt wird, dass eine Domäne nicht erreichbar ist und bevor der DC erneut versucht wird.
ms.assetid: b2523faa-7cf1-4325-a3fa-70c5f568adaa
ms.tgt_platform: multiple
keywords:
- "\"ms-DS-AZ-Domain-Timeout\"-Attribut AD-Schema"
- AD-Schema des msDS-azdomaintimeout-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Az-Domain-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce6f457977de1124438fa4b54e4a84d1cb6d54e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859696"
---
# <a name="ms-ds-az-domain-timeout-attribute"></a><span data-ttu-id="88eb6-105">ms-DS-AZ-Domain-Timeout-Attribut</span><span class="sxs-lookup"><span data-stu-id="88eb6-105">ms-DS-Az-Domain-Timeout attribute</span></span>

<span data-ttu-id="88eb6-106">Zeit (in Millisekunden), nach der erkannt wird, dass eine Domäne nicht erreichbar ist und bevor der DC erneut versucht wird.</span><span class="sxs-lookup"><span data-stu-id="88eb6-106">Time, in milliseconds, after a domain is detected to be unreachable and before the DC is tried again.</span></span>



| <span data-ttu-id="88eb6-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88eb6-107">Entry</span></span> | <span data-ttu-id="88eb6-108">Wert</span><span class="sxs-lookup"><span data-stu-id="88eb6-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="88eb6-109">CN</span><span class="sxs-lookup"><span data-stu-id="88eb6-109">CN</span></span>                | <span data-ttu-id="88eb6-110">ms-DS-AZ-Domain-Timeout</span><span class="sxs-lookup"><span data-stu-id="88eb6-110">ms-DS-Az-Domain-Timeout</span></span>                 |
| <span data-ttu-id="88eb6-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="88eb6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="88eb6-112">MSDS-azdomaintimeout</span><span class="sxs-lookup"><span data-stu-id="88eb6-112">msDS-AzDomainTimeout</span></span>                    |
| <span data-ttu-id="88eb6-113">Size</span><span class="sxs-lookup"><span data-stu-id="88eb6-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="88eb6-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="88eb6-114">Update Privilege</span></span>  | <span data-ttu-id="88eb6-115">Azrollen-Administrator</span><span class="sxs-lookup"><span data-stu-id="88eb6-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="88eb6-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="88eb6-116">Update Frequency</span></span>  | <span data-ttu-id="88eb6-117">Während der Initialisierung oder Richtlinien Änderung.</span><span class="sxs-lookup"><span data-stu-id="88eb6-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="88eb6-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="88eb6-118">Attribute-Id</span></span>      | <span data-ttu-id="88eb6-119">1.2.840.113556.1.4.1795</span><span class="sxs-lookup"><span data-stu-id="88eb6-119">1.2.840.113556.1.4.1795</span></span>                 |
| <span data-ttu-id="88eb6-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="88eb6-120">System-Id-Guid</span></span>    | <span data-ttu-id="88eb6-121">6448l56a-ca70-4e2e-b0af-d20e4ce653d0</span><span class="sxs-lookup"><span data-stu-id="88eb6-121">6448f56a-ca70-4e2e-b0af-d20e4ce653d0</span></span>    |
| <span data-ttu-id="88eb6-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="88eb6-122">Syntax</span></span>            | [<span data-ttu-id="88eb6-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="88eb6-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="88eb6-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="88eb6-124">Implementations</span></span>

-   [<span data-ttu-id="88eb6-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="88eb6-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="88eb6-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="88eb6-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="88eb6-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="88eb6-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="88eb6-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="88eb6-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="88eb6-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="88eb6-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="88eb6-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="88eb6-130">Windows Server 2003</span></span>



| <span data-ttu-id="88eb6-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88eb6-131">Entry</span></span> | <span data-ttu-id="88eb6-132">Wert</span><span class="sxs-lookup"><span data-stu-id="88eb6-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="88eb6-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="88eb6-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="88eb6-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88eb6-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="88eb6-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="88eb6-135">System-Only</span></span>            | <span data-ttu-id="88eb6-136">False</span><span class="sxs-lookup"><span data-stu-id="88eb6-136">False</span></span>                                                              |
| <span data-ttu-id="88eb6-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="88eb6-137">Is-Single-Valued</span></span>       | <span data-ttu-id="88eb6-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="88eb6-138">True</span></span>                                                               |
| <span data-ttu-id="88eb6-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="88eb6-139">Is Indexed</span></span>             | <span data-ttu-id="88eb6-140">False</span><span class="sxs-lookup"><span data-stu-id="88eb6-140">False</span></span>                                                              |
| <span data-ttu-id="88eb6-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="88eb6-141">In Global Catalog</span></span>      | <span data-ttu-id="88eb6-142">False</span><span class="sxs-lookup"><span data-stu-id="88eb6-142">False</span></span>                                                              |
| <span data-ttu-id="88eb6-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="88eb6-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="88eb6-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="88eb6-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="88eb6-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88eb6-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="88eb6-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88eb6-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="88eb6-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88eb6-147">Search-Flags</span></span>           | <span data-ttu-id="88eb6-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88eb6-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="88eb6-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88eb6-149">System-Flags</span></span>           | <span data-ttu-id="88eb6-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88eb6-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="88eb6-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="88eb6-151">Classes used in</span></span>        | [<span data-ttu-id="88eb6-152">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="88eb6-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="88eb6-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="88eb6-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="88eb6-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88eb6-154">Entry</span></span> | <span data-ttu-id="88eb6-155">Wert</span><span class="sxs-lookup"><span data-stu-id="88eb6-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="88eb6-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="88eb6-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="88eb6-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88eb6-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="88eb6-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="88eb6-158">System-Only</span></span>            | <span data-ttu-id="88eb6-159">False</span><span class="sxs-lookup"><span data-stu-id="88eb6-159">False</span></span>                                                              |
| <span data-ttu-id="88eb6-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="88eb6-160">Is-Single-Valued</span></span>       | <span data-ttu-id="88eb6-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="88eb6-161">True</span></span>                                                               |
| <span data-ttu-id="88eb6-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="88eb6-162">Is Indexed</span></span>             | <span data-ttu-id="88eb6-163">False</span><span class="sxs-lookup"><span data-stu-id="88eb6-163">False</span></span>                                                              |
| <span data-ttu-id="88eb6-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="88eb6-164">In Global Catalog</span></span>      | <span data-ttu-id="88eb6-165">False</span><span class="sxs-lookup"><span data-stu-id="88eb6-165">False</span></span>                                                              |
| <span data-ttu-id="88eb6-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="88eb6-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="88eb6-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="88eb6-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="88eb6-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88eb6-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="88eb6-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88eb6-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="88eb6-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88eb6-170">Search-Flags</span></span>           | <span data-ttu-id="88eb6-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88eb6-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="88eb6-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88eb6-172">System-Flags</span></span>           | <span data-ttu-id="88eb6-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88eb6-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="88eb6-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="88eb6-174">Classes used in</span></span>        | [<span data-ttu-id="88eb6-175">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="88eb6-175">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="88eb6-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88eb6-176">Windows Server 2008</span></span>



| <span data-ttu-id="88eb6-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88eb6-177">Entry</span></span> | <span data-ttu-id="88eb6-178">Wert</span><span class="sxs-lookup"><span data-stu-id="88eb6-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="88eb6-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="88eb6-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="88eb6-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88eb6-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="88eb6-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="88eb6-181">System-Only</span></span>            | <span data-ttu-id="88eb6-182">False</span><span class="sxs-lookup"><span data-stu-id="88eb6-182">False</span></span>                                                              |
| <span data-ttu-id="88eb6-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="88eb6-183">Is-Single-Valued</span></span>       | <span data-ttu-id="88eb6-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="88eb6-184">True</span></span>                                                               |
| <span data-ttu-id="88eb6-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="88eb6-185">Is Indexed</span></span>             | <span data-ttu-id="88eb6-186">False</span><span class="sxs-lookup"><span data-stu-id="88eb6-186">False</span></span>                                                              |
| <span data-ttu-id="88eb6-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="88eb6-187">In Global Catalog</span></span>      | <span data-ttu-id="88eb6-188">False</span><span class="sxs-lookup"><span data-stu-id="88eb6-188">False</span></span>                                                              |
| <span data-ttu-id="88eb6-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="88eb6-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="88eb6-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="88eb6-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="88eb6-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88eb6-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="88eb6-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88eb6-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="88eb6-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88eb6-193">Search-Flags</span></span>           | <span data-ttu-id="88eb6-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88eb6-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="88eb6-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88eb6-195">System-Flags</span></span>           | <span data-ttu-id="88eb6-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88eb6-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="88eb6-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="88eb6-197">Classes used in</span></span>        | [<span data-ttu-id="88eb6-198">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="88eb6-198">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="88eb6-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="88eb6-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="88eb6-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88eb6-200">Entry</span></span> | <span data-ttu-id="88eb6-201">Wert</span><span class="sxs-lookup"><span data-stu-id="88eb6-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="88eb6-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="88eb6-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="88eb6-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88eb6-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="88eb6-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="88eb6-204">System-Only</span></span>            | <span data-ttu-id="88eb6-205">False</span><span class="sxs-lookup"><span data-stu-id="88eb6-205">False</span></span>                                                              |
| <span data-ttu-id="88eb6-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="88eb6-206">Is-Single-Valued</span></span>       | <span data-ttu-id="88eb6-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="88eb6-207">True</span></span>                                                               |
| <span data-ttu-id="88eb6-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="88eb6-208">Is Indexed</span></span>             | <span data-ttu-id="88eb6-209">False</span><span class="sxs-lookup"><span data-stu-id="88eb6-209">False</span></span>                                                              |
| <span data-ttu-id="88eb6-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="88eb6-210">In Global Catalog</span></span>      | <span data-ttu-id="88eb6-211">False</span><span class="sxs-lookup"><span data-stu-id="88eb6-211">False</span></span>                                                              |
| <span data-ttu-id="88eb6-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="88eb6-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="88eb6-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="88eb6-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="88eb6-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88eb6-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="88eb6-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88eb6-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="88eb6-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88eb6-216">Search-Flags</span></span>           | <span data-ttu-id="88eb6-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88eb6-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="88eb6-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88eb6-218">System-Flags</span></span>           | <span data-ttu-id="88eb6-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88eb6-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="88eb6-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="88eb6-220">Classes used in</span></span>        | [<span data-ttu-id="88eb6-221">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="88eb6-221">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="88eb6-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88eb6-222">Windows Server 2012</span></span>



| <span data-ttu-id="88eb6-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88eb6-223">Entry</span></span> | <span data-ttu-id="88eb6-224">Wert</span><span class="sxs-lookup"><span data-stu-id="88eb6-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="88eb6-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="88eb6-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="88eb6-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88eb6-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="88eb6-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="88eb6-227">System-Only</span></span>            | <span data-ttu-id="88eb6-228">False</span><span class="sxs-lookup"><span data-stu-id="88eb6-228">False</span></span>                                                              |
| <span data-ttu-id="88eb6-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="88eb6-229">Is-Single-Valued</span></span>       | <span data-ttu-id="88eb6-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="88eb6-230">True</span></span>                                                               |
| <span data-ttu-id="88eb6-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="88eb6-231">Is Indexed</span></span>             | <span data-ttu-id="88eb6-232">False</span><span class="sxs-lookup"><span data-stu-id="88eb6-232">False</span></span>                                                              |
| <span data-ttu-id="88eb6-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="88eb6-233">In Global Catalog</span></span>      | <span data-ttu-id="88eb6-234">False</span><span class="sxs-lookup"><span data-stu-id="88eb6-234">False</span></span>                                                              |
| <span data-ttu-id="88eb6-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="88eb6-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="88eb6-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="88eb6-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="88eb6-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88eb6-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="88eb6-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88eb6-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="88eb6-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88eb6-239">Search-Flags</span></span>           | <span data-ttu-id="88eb6-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88eb6-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="88eb6-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88eb6-241">System-Flags</span></span>           | <span data-ttu-id="88eb6-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88eb6-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="88eb6-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="88eb6-243">Classes used in</span></span>        | [<span data-ttu-id="88eb6-244">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="88eb6-244">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



 

 





