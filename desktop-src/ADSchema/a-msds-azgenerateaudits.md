---
title: ms-DS-AZ-Generate-überwachungattribut
description: Ein boolesches Feld, das angibt, ob Lauf Zeit Überwachungen aktiviert werden müssen (einschließlich Überwachungen für Zugriffs Überprüfungen usw.).
ms.assetid: 23578f6a-7e7f-4871-9503-73f2ce598173
ms.tgt_platform: multiple
keywords:
- "\"ms-DS-AZ-Generate-Überwachungen\"-Attribut AD-Schema"
- AD-Schema für das msDS-azgenerateüberwachungattribut
topic_type:
- apiref
api_name:
- ms-DS-Az-Generate-Audits
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645bdfd2f822139072391d401ecedfedee8680b8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859858"
---
# <a name="ms-ds-az-generate-audits-attribute"></a><span data-ttu-id="0190b-105">ms-DS-AZ-Generate-überwachungattribut</span><span class="sxs-lookup"><span data-stu-id="0190b-105">ms-DS-Az-Generate-Audits attribute</span></span>

<span data-ttu-id="0190b-106">Ein boolesches Feld, das angibt, ob Lauf Zeit Überwachungen aktiviert werden müssen (einschließlich Überwachungen für Zugriffs Überprüfungen usw.).</span><span class="sxs-lookup"><span data-stu-id="0190b-106">A Boolean field that indicates whether runtime audits need to be turned on (include audits for access checks, and so on).</span></span>



| <span data-ttu-id="0190b-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0190b-107">Entry</span></span> | <span data-ttu-id="0190b-108">Wert</span><span class="sxs-lookup"><span data-stu-id="0190b-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="0190b-109">CN</span><span class="sxs-lookup"><span data-stu-id="0190b-109">CN</span></span>                | <span data-ttu-id="0190b-110">ms-DS-AZ-Generate-Überwachungen</span><span class="sxs-lookup"><span data-stu-id="0190b-110">ms-DS-Az-Generate-Audits</span></span>                |
| <span data-ttu-id="0190b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0190b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0190b-112">MSDS-azgenerateüberwachungen</span><span class="sxs-lookup"><span data-stu-id="0190b-112">msDS-AzGenerateAudits</span></span>                   |
| <span data-ttu-id="0190b-113">Size</span><span class="sxs-lookup"><span data-stu-id="0190b-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="0190b-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0190b-114">Update Privilege</span></span>  | <span data-ttu-id="0190b-115">Azrollen-Administrator</span><span class="sxs-lookup"><span data-stu-id="0190b-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="0190b-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="0190b-116">Update Frequency</span></span>  | <span data-ttu-id="0190b-117">Während der Initialisierung oder Richtlinien Änderung.</span><span class="sxs-lookup"><span data-stu-id="0190b-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="0190b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0190b-118">Attribute-Id</span></span>      | <span data-ttu-id="0190b-119">1.2.840.113556.1.4.1805</span><span class="sxs-lookup"><span data-stu-id="0190b-119">1.2.840.113556.1.4.1805</span></span>                 |
| <span data-ttu-id="0190b-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0190b-120">System-Id-Guid</span></span>    | <span data-ttu-id="0190b-121">f90abab0-186c-4418-bb85-88447c87222a</span><span class="sxs-lookup"><span data-stu-id="0190b-121">f90abab0-186c-4418-bb85-88447c87222a</span></span>    |
| <span data-ttu-id="0190b-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0190b-122">Syntax</span></span>            | [<span data-ttu-id="0190b-123">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="0190b-123">**Boolean**</span></span>](s-boolean.md)            |



## <a name="implementations"></a><span data-ttu-id="0190b-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="0190b-124">Implementations</span></span>

-   [<span data-ttu-id="0190b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0190b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0190b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0190b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0190b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0190b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0190b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0190b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0190b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0190b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="0190b-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0190b-130">Windows Server 2003</span></span>



| <span data-ttu-id="0190b-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0190b-131">Entry</span></span> | <span data-ttu-id="0190b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="0190b-132">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0190b-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0190b-133">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="0190b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0190b-134">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="0190b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="0190b-135">System-Only</span></span>            | <span data-ttu-id="0190b-136">False</span><span class="sxs-lookup"><span data-stu-id="0190b-136">False</span></span>                                                                                                                              |
| <span data-ttu-id="0190b-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0190b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="0190b-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="0190b-138">True</span></span>                                                                                                                               |
| <span data-ttu-id="0190b-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0190b-139">Is Indexed</span></span>             | <span data-ttu-id="0190b-140">False</span><span class="sxs-lookup"><span data-stu-id="0190b-140">False</span></span>                                                                                                                              |
| <span data-ttu-id="0190b-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0190b-141">In Global Catalog</span></span>      | <span data-ttu-id="0190b-142">False</span><span class="sxs-lookup"><span data-stu-id="0190b-142">False</span></span>                                                                                                                              |
| <span data-ttu-id="0190b-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0190b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="0190b-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0190b-144">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="0190b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0190b-145">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="0190b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0190b-146">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="0190b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0190b-147">Search-Flags</span></span>           | <span data-ttu-id="0190b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0190b-148">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="0190b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0190b-149">System-Flags</span></span>           | <span data-ttu-id="0190b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0190b-150">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="0190b-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0190b-151">Classes used in</span></span>        | [<span data-ttu-id="0190b-152">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="0190b-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="0190b-153">**ms-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="0190b-153">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0190b-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0190b-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0190b-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0190b-155">Entry</span></span> | <span data-ttu-id="0190b-156">Wert</span><span class="sxs-lookup"><span data-stu-id="0190b-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0190b-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0190b-157">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="0190b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0190b-158">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="0190b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="0190b-159">System-Only</span></span>            | <span data-ttu-id="0190b-160">False</span><span class="sxs-lookup"><span data-stu-id="0190b-160">False</span></span>                                                                                                                              |
| <span data-ttu-id="0190b-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0190b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="0190b-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="0190b-162">True</span></span>                                                                                                                               |
| <span data-ttu-id="0190b-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0190b-163">Is Indexed</span></span>             | <span data-ttu-id="0190b-164">False</span><span class="sxs-lookup"><span data-stu-id="0190b-164">False</span></span>                                                                                                                              |
| <span data-ttu-id="0190b-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0190b-165">In Global Catalog</span></span>      | <span data-ttu-id="0190b-166">False</span><span class="sxs-lookup"><span data-stu-id="0190b-166">False</span></span>                                                                                                                              |
| <span data-ttu-id="0190b-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0190b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="0190b-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0190b-168">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="0190b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0190b-169">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="0190b-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0190b-170">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="0190b-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0190b-171">Search-Flags</span></span>           | <span data-ttu-id="0190b-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0190b-172">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="0190b-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0190b-173">System-Flags</span></span>           | <span data-ttu-id="0190b-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0190b-174">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="0190b-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0190b-175">Classes used in</span></span>        | [<span data-ttu-id="0190b-176">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="0190b-176">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="0190b-177">**ms-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="0190b-177">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0190b-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0190b-178">Windows Server 2008</span></span>



| <span data-ttu-id="0190b-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0190b-179">Entry</span></span> | <span data-ttu-id="0190b-180">Wert</span><span class="sxs-lookup"><span data-stu-id="0190b-180">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0190b-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0190b-181">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="0190b-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0190b-182">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="0190b-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="0190b-183">System-Only</span></span>            | <span data-ttu-id="0190b-184">False</span><span class="sxs-lookup"><span data-stu-id="0190b-184">False</span></span>                                                                                                                              |
| <span data-ttu-id="0190b-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0190b-185">Is-Single-Valued</span></span>       | <span data-ttu-id="0190b-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="0190b-186">True</span></span>                                                                                                                               |
| <span data-ttu-id="0190b-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0190b-187">Is Indexed</span></span>             | <span data-ttu-id="0190b-188">False</span><span class="sxs-lookup"><span data-stu-id="0190b-188">False</span></span>                                                                                                                              |
| <span data-ttu-id="0190b-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0190b-189">In Global Catalog</span></span>      | <span data-ttu-id="0190b-190">False</span><span class="sxs-lookup"><span data-stu-id="0190b-190">False</span></span>                                                                                                                              |
| <span data-ttu-id="0190b-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0190b-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="0190b-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0190b-192">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="0190b-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0190b-193">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="0190b-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0190b-194">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="0190b-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0190b-195">Search-Flags</span></span>           | <span data-ttu-id="0190b-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0190b-196">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="0190b-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0190b-197">System-Flags</span></span>           | <span data-ttu-id="0190b-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0190b-198">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="0190b-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0190b-199">Classes used in</span></span>        | [<span data-ttu-id="0190b-200">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="0190b-200">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="0190b-201">**ms-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="0190b-201">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0190b-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0190b-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0190b-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0190b-203">Entry</span></span> | <span data-ttu-id="0190b-204">Wert</span><span class="sxs-lookup"><span data-stu-id="0190b-204">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0190b-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0190b-205">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="0190b-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0190b-206">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="0190b-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="0190b-207">System-Only</span></span>            | <span data-ttu-id="0190b-208">False</span><span class="sxs-lookup"><span data-stu-id="0190b-208">False</span></span>                                                                                                                              |
| <span data-ttu-id="0190b-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0190b-209">Is-Single-Valued</span></span>       | <span data-ttu-id="0190b-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="0190b-210">True</span></span>                                                                                                                               |
| <span data-ttu-id="0190b-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0190b-211">Is Indexed</span></span>             | <span data-ttu-id="0190b-212">False</span><span class="sxs-lookup"><span data-stu-id="0190b-212">False</span></span>                                                                                                                              |
| <span data-ttu-id="0190b-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0190b-213">In Global Catalog</span></span>      | <span data-ttu-id="0190b-214">False</span><span class="sxs-lookup"><span data-stu-id="0190b-214">False</span></span>                                                                                                                              |
| <span data-ttu-id="0190b-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0190b-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="0190b-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0190b-216">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="0190b-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0190b-217">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="0190b-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0190b-218">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="0190b-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0190b-219">Search-Flags</span></span>           | <span data-ttu-id="0190b-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0190b-220">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="0190b-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0190b-221">System-Flags</span></span>           | <span data-ttu-id="0190b-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0190b-222">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="0190b-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0190b-223">Classes used in</span></span>        | [<span data-ttu-id="0190b-224">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="0190b-224">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="0190b-225">**ms-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="0190b-225">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0190b-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0190b-226">Windows Server 2012</span></span>



| <span data-ttu-id="0190b-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0190b-227">Entry</span></span> | <span data-ttu-id="0190b-228">Wert</span><span class="sxs-lookup"><span data-stu-id="0190b-228">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0190b-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0190b-229">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="0190b-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0190b-230">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="0190b-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="0190b-231">System-Only</span></span>            | <span data-ttu-id="0190b-232">False</span><span class="sxs-lookup"><span data-stu-id="0190b-232">False</span></span>                                                                                                                              |
| <span data-ttu-id="0190b-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0190b-233">Is-Single-Valued</span></span>       | <span data-ttu-id="0190b-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="0190b-234">True</span></span>                                                                                                                               |
| <span data-ttu-id="0190b-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0190b-235">Is Indexed</span></span>             | <span data-ttu-id="0190b-236">False</span><span class="sxs-lookup"><span data-stu-id="0190b-236">False</span></span>                                                                                                                              |
| <span data-ttu-id="0190b-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0190b-237">In Global Catalog</span></span>      | <span data-ttu-id="0190b-238">False</span><span class="sxs-lookup"><span data-stu-id="0190b-238">False</span></span>                                                                                                                              |
| <span data-ttu-id="0190b-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0190b-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="0190b-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0190b-240">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="0190b-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0190b-241">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="0190b-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0190b-242">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="0190b-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0190b-243">Search-Flags</span></span>           | <span data-ttu-id="0190b-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0190b-244">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="0190b-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0190b-245">System-Flags</span></span>           | <span data-ttu-id="0190b-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0190b-246">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="0190b-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0190b-247">Classes used in</span></span>        | [<span data-ttu-id="0190b-248">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="0190b-248">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="0190b-249">**ms-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="0190b-249">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



 

 





