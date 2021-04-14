---
title: ms-DS-AZ-Script-Timeout-Attribut
description: Die maximale Zeit in Millisekunden, die auf das Abschließen der Überwachung einer bestimmten Richtlinie durch ein Skript gewartet werden soll.
ms.assetid: 166d87a3-8768-42d9-9041-21f272059fbf
ms.tgt_platform: multiple
keywords:
- "\"ms-DS-AZ-Script-Timeout\"-Attribut AD-Schema"
- AD-Schema des msDS-azscripttimeout-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Az-Script-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67de4230c3f4710a3eefe6edab896d4fcadcb91
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392313"
---
# <a name="ms-ds-az-script-timeout-attribute"></a><span data-ttu-id="29fe2-105">ms-DS-AZ-Script-Timeout-Attribut</span><span class="sxs-lookup"><span data-stu-id="29fe2-105">ms-DS-Az-Script-Timeout attribute</span></span>

<span data-ttu-id="29fe2-106">Die maximale Zeit in Millisekunden, die auf das Abschließen der Überwachung einer bestimmten Richtlinie durch ein Skript gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="29fe2-106">The maximum time, in milliseconds, to wait for a script to finish auditing a specific policy.</span></span>



| <span data-ttu-id="29fe2-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="29fe2-107">Entry</span></span> | <span data-ttu-id="29fe2-108">Wert</span><span class="sxs-lookup"><span data-stu-id="29fe2-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="29fe2-109">CN</span><span class="sxs-lookup"><span data-stu-id="29fe2-109">CN</span></span>                | <span data-ttu-id="29fe2-110">ms-DS-AZ-Script-Timeout</span><span class="sxs-lookup"><span data-stu-id="29fe2-110">ms-DS-Az-Script-Timeout</span></span>                 |
| <span data-ttu-id="29fe2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="29fe2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="29fe2-112">MSDS-azscripttimeout</span><span class="sxs-lookup"><span data-stu-id="29fe2-112">msDS-AzScriptTimeout</span></span>                    |
| <span data-ttu-id="29fe2-113">Size</span><span class="sxs-lookup"><span data-stu-id="29fe2-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="29fe2-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="29fe2-114">Update Privilege</span></span>  | <span data-ttu-id="29fe2-115">Azrollen-Administrator</span><span class="sxs-lookup"><span data-stu-id="29fe2-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="29fe2-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="29fe2-116">Update Frequency</span></span>  | <span data-ttu-id="29fe2-117">Während der Initialisierung oder Richtlinien Änderung.</span><span class="sxs-lookup"><span data-stu-id="29fe2-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="29fe2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="29fe2-118">Attribute-Id</span></span>      | <span data-ttu-id="29fe2-119">1.2.840.113556.1.4.1797</span><span class="sxs-lookup"><span data-stu-id="29fe2-119">1.2.840.113556.1.4.1797</span></span>                 |
| <span data-ttu-id="29fe2-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="29fe2-120">System-Id-Guid</span></span>    | <span data-ttu-id="29fe2-121">87d0b41-2c8b-41b6-b972-11b-bbd50d6b0</span><span class="sxs-lookup"><span data-stu-id="29fe2-121">87d0fb41-2c8b-41f6-b972-11fdfd50d6b0</span></span>    |
| <span data-ttu-id="29fe2-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="29fe2-122">Syntax</span></span>            | [<span data-ttu-id="29fe2-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="29fe2-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="29fe2-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="29fe2-124">Implementations</span></span>

-   [<span data-ttu-id="29fe2-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="29fe2-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="29fe2-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="29fe2-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="29fe2-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="29fe2-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="29fe2-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="29fe2-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="29fe2-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="29fe2-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="29fe2-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="29fe2-130">Windows Server 2003</span></span>



| <span data-ttu-id="29fe2-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="29fe2-131">Entry</span></span> | <span data-ttu-id="29fe2-132">Wert</span><span class="sxs-lookup"><span data-stu-id="29fe2-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="29fe2-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="29fe2-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="29fe2-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29fe2-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="29fe2-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="29fe2-135">System-Only</span></span>            | <span data-ttu-id="29fe2-136">False</span><span class="sxs-lookup"><span data-stu-id="29fe2-136">False</span></span>                                                              |
| <span data-ttu-id="29fe2-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="29fe2-137">Is-Single-Valued</span></span>       | <span data-ttu-id="29fe2-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="29fe2-138">True</span></span>                                                               |
| <span data-ttu-id="29fe2-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="29fe2-139">Is Indexed</span></span>             | <span data-ttu-id="29fe2-140">False</span><span class="sxs-lookup"><span data-stu-id="29fe2-140">False</span></span>                                                              |
| <span data-ttu-id="29fe2-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="29fe2-141">In Global Catalog</span></span>      | <span data-ttu-id="29fe2-142">False</span><span class="sxs-lookup"><span data-stu-id="29fe2-142">False</span></span>                                                              |
| <span data-ttu-id="29fe2-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="29fe2-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="29fe2-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="29fe2-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="29fe2-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29fe2-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="29fe2-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29fe2-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="29fe2-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29fe2-147">Search-Flags</span></span>           | <span data-ttu-id="29fe2-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29fe2-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="29fe2-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29fe2-149">System-Flags</span></span>           | <span data-ttu-id="29fe2-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29fe2-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="29fe2-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="29fe2-151">Classes used in</span></span>        | [<span data-ttu-id="29fe2-152">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="29fe2-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="29fe2-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="29fe2-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="29fe2-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="29fe2-154">Entry</span></span> | <span data-ttu-id="29fe2-155">Wert</span><span class="sxs-lookup"><span data-stu-id="29fe2-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="29fe2-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="29fe2-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="29fe2-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29fe2-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="29fe2-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="29fe2-158">System-Only</span></span>            | <span data-ttu-id="29fe2-159">False</span><span class="sxs-lookup"><span data-stu-id="29fe2-159">False</span></span>                                                              |
| <span data-ttu-id="29fe2-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="29fe2-160">Is-Single-Valued</span></span>       | <span data-ttu-id="29fe2-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="29fe2-161">True</span></span>                                                               |
| <span data-ttu-id="29fe2-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="29fe2-162">Is Indexed</span></span>             | <span data-ttu-id="29fe2-163">False</span><span class="sxs-lookup"><span data-stu-id="29fe2-163">False</span></span>                                                              |
| <span data-ttu-id="29fe2-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="29fe2-164">In Global Catalog</span></span>      | <span data-ttu-id="29fe2-165">False</span><span class="sxs-lookup"><span data-stu-id="29fe2-165">False</span></span>                                                              |
| <span data-ttu-id="29fe2-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="29fe2-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="29fe2-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="29fe2-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="29fe2-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29fe2-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="29fe2-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29fe2-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="29fe2-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29fe2-170">Search-Flags</span></span>           | <span data-ttu-id="29fe2-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29fe2-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="29fe2-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29fe2-172">System-Flags</span></span>           | <span data-ttu-id="29fe2-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29fe2-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="29fe2-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="29fe2-174">Classes used in</span></span>        | [<span data-ttu-id="29fe2-175">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="29fe2-175">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="29fe2-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29fe2-176">Windows Server 2008</span></span>



| <span data-ttu-id="29fe2-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="29fe2-177">Entry</span></span> | <span data-ttu-id="29fe2-178">Wert</span><span class="sxs-lookup"><span data-stu-id="29fe2-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="29fe2-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="29fe2-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="29fe2-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29fe2-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="29fe2-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="29fe2-181">System-Only</span></span>            | <span data-ttu-id="29fe2-182">False</span><span class="sxs-lookup"><span data-stu-id="29fe2-182">False</span></span>                                                              |
| <span data-ttu-id="29fe2-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="29fe2-183">Is-Single-Valued</span></span>       | <span data-ttu-id="29fe2-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="29fe2-184">True</span></span>                                                               |
| <span data-ttu-id="29fe2-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="29fe2-185">Is Indexed</span></span>             | <span data-ttu-id="29fe2-186">False</span><span class="sxs-lookup"><span data-stu-id="29fe2-186">False</span></span>                                                              |
| <span data-ttu-id="29fe2-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="29fe2-187">In Global Catalog</span></span>      | <span data-ttu-id="29fe2-188">False</span><span class="sxs-lookup"><span data-stu-id="29fe2-188">False</span></span>                                                              |
| <span data-ttu-id="29fe2-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="29fe2-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="29fe2-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="29fe2-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="29fe2-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29fe2-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="29fe2-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29fe2-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="29fe2-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29fe2-193">Search-Flags</span></span>           | <span data-ttu-id="29fe2-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29fe2-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="29fe2-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29fe2-195">System-Flags</span></span>           | <span data-ttu-id="29fe2-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29fe2-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="29fe2-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="29fe2-197">Classes used in</span></span>        | [<span data-ttu-id="29fe2-198">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="29fe2-198">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="29fe2-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="29fe2-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="29fe2-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="29fe2-200">Entry</span></span> | <span data-ttu-id="29fe2-201">Wert</span><span class="sxs-lookup"><span data-stu-id="29fe2-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="29fe2-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="29fe2-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="29fe2-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29fe2-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="29fe2-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="29fe2-204">System-Only</span></span>            | <span data-ttu-id="29fe2-205">False</span><span class="sxs-lookup"><span data-stu-id="29fe2-205">False</span></span>                                                              |
| <span data-ttu-id="29fe2-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="29fe2-206">Is-Single-Valued</span></span>       | <span data-ttu-id="29fe2-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="29fe2-207">True</span></span>                                                               |
| <span data-ttu-id="29fe2-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="29fe2-208">Is Indexed</span></span>             | <span data-ttu-id="29fe2-209">False</span><span class="sxs-lookup"><span data-stu-id="29fe2-209">False</span></span>                                                              |
| <span data-ttu-id="29fe2-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="29fe2-210">In Global Catalog</span></span>      | <span data-ttu-id="29fe2-211">False</span><span class="sxs-lookup"><span data-stu-id="29fe2-211">False</span></span>                                                              |
| <span data-ttu-id="29fe2-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="29fe2-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="29fe2-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="29fe2-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="29fe2-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29fe2-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="29fe2-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29fe2-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="29fe2-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29fe2-216">Search-Flags</span></span>           | <span data-ttu-id="29fe2-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29fe2-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="29fe2-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29fe2-218">System-Flags</span></span>           | <span data-ttu-id="29fe2-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29fe2-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="29fe2-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="29fe2-220">Classes used in</span></span>        | [<span data-ttu-id="29fe2-221">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="29fe2-221">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="29fe2-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29fe2-222">Windows Server 2012</span></span>



| <span data-ttu-id="29fe2-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="29fe2-223">Entry</span></span> | <span data-ttu-id="29fe2-224">Wert</span><span class="sxs-lookup"><span data-stu-id="29fe2-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="29fe2-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="29fe2-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="29fe2-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29fe2-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="29fe2-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="29fe2-227">System-Only</span></span>            | <span data-ttu-id="29fe2-228">False</span><span class="sxs-lookup"><span data-stu-id="29fe2-228">False</span></span>                                                              |
| <span data-ttu-id="29fe2-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="29fe2-229">Is-Single-Valued</span></span>       | <span data-ttu-id="29fe2-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="29fe2-230">True</span></span>                                                               |
| <span data-ttu-id="29fe2-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="29fe2-231">Is Indexed</span></span>             | <span data-ttu-id="29fe2-232">False</span><span class="sxs-lookup"><span data-stu-id="29fe2-232">False</span></span>                                                              |
| <span data-ttu-id="29fe2-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="29fe2-233">In Global Catalog</span></span>      | <span data-ttu-id="29fe2-234">False</span><span class="sxs-lookup"><span data-stu-id="29fe2-234">False</span></span>                                                              |
| <span data-ttu-id="29fe2-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="29fe2-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="29fe2-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="29fe2-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="29fe2-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29fe2-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="29fe2-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29fe2-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="29fe2-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29fe2-239">Search-Flags</span></span>           | <span data-ttu-id="29fe2-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29fe2-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="29fe2-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29fe2-241">System-Flags</span></span>           | <span data-ttu-id="29fe2-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29fe2-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="29fe2-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="29fe2-243">Classes used in</span></span>        | [<span data-ttu-id="29fe2-244">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="29fe2-244">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



 

 





