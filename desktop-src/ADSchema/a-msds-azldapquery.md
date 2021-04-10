---
title: ms-DS-AZ-LDAP-Query-Attribut
description: Eine Zeichenfolge, die die LDAP-Abfrage definiert (maximale Länge 4096), mit der die Mitgliedschaft eines Benutzer Objekts zur Gruppe bestimmt wird.
ms.assetid: e24d4c50-2153-49a6-8aef-4872ccaab13e
ms.tgt_platform: multiple
keywords:
- "\"ms-DS-AZ-LDAP-Query\"-Attribut AD-Schema"
- AD-Schema des msDS-azldapquery-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Az-LDAP-Query
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1f6c21d5ed28a9d2419b16c6ce7986f3250488
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107841"
---
# <a name="ms-ds-az-ldap-query-attribute"></a><span data-ttu-id="457bc-105">ms-DS-AZ-LDAP-Query-Attribut</span><span class="sxs-lookup"><span data-stu-id="457bc-105">ms-DS-Az-LDAP-Query attribute</span></span>

<span data-ttu-id="457bc-106">Eine Zeichenfolge, die die LDAP-Abfrage definiert (maximale Länge 4096), mit der die Mitgliedschaft eines Benutzer Objekts zur Gruppe bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="457bc-106">A string that defines the LDAP query (max length 4096) which determines the membership of a user object to the group.</span></span>



| <span data-ttu-id="457bc-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="457bc-107">Entry</span></span> | <span data-ttu-id="457bc-108">Wert</span><span class="sxs-lookup"><span data-stu-id="457bc-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="457bc-109">CN</span><span class="sxs-lookup"><span data-stu-id="457bc-109">CN</span></span>                | <span data-ttu-id="457bc-110">ms-DS-AZ-LDAP-Query</span><span class="sxs-lookup"><span data-stu-id="457bc-110">ms-DS-Az-LDAP-Query</span></span>                         |
| <span data-ttu-id="457bc-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="457bc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="457bc-112">MSDS-azldapquery</span><span class="sxs-lookup"><span data-stu-id="457bc-112">msDS-AzLDAPQuery</span></span>                            |
| <span data-ttu-id="457bc-113">Size</span><span class="sxs-lookup"><span data-stu-id="457bc-113">Size</span></span>              | <span data-ttu-id="457bc-114">4096 Zeichen</span><span class="sxs-lookup"><span data-stu-id="457bc-114">4096 characters</span></span>                             |
| <span data-ttu-id="457bc-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="457bc-115">Update Privilege</span></span>  | <span data-ttu-id="457bc-116">Azrollen-Administrator</span><span class="sxs-lookup"><span data-stu-id="457bc-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="457bc-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="457bc-117">Update Frequency</span></span>  | <span data-ttu-id="457bc-118">Während der Initialisierung oder Richtlinien Änderung.</span><span class="sxs-lookup"><span data-stu-id="457bc-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="457bc-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="457bc-119">Attribute-Id</span></span>      | <span data-ttu-id="457bc-120">1.2.840.113556.1.4.1792</span><span class="sxs-lookup"><span data-stu-id="457bc-120">1.2.840.113556.1.4.1792</span></span>                     |
| <span data-ttu-id="457bc-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="457bc-121">System-Id-Guid</span></span>    | <span data-ttu-id="457bc-122">5e53368b-fc94-45c8-9d7d-DAF 31ee7112d</span><span class="sxs-lookup"><span data-stu-id="457bc-122">5e53368b-fc94-45c8-9d7d-daf31ee7112d</span></span>        |
| <span data-ttu-id="457bc-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="457bc-123">Syntax</span></span>            | [<span data-ttu-id="457bc-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="457bc-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="457bc-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="457bc-125">Implementations</span></span>

-   [<span data-ttu-id="457bc-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="457bc-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="457bc-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="457bc-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="457bc-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="457bc-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="457bc-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="457bc-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="457bc-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="457bc-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="457bc-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="457bc-131">Windows Server 2003</span></span>



| <span data-ttu-id="457bc-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="457bc-132">Entry</span></span> | <span data-ttu-id="457bc-133">Wert</span><span class="sxs-lookup"><span data-stu-id="457bc-133">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="457bc-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="457bc-134">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="457bc-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="457bc-135">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="457bc-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="457bc-136">System-Only</span></span>            | <span data-ttu-id="457bc-137">False</span><span class="sxs-lookup"><span data-stu-id="457bc-137">False</span></span>                               |
| <span data-ttu-id="457bc-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="457bc-138">Is-Single-Valued</span></span>       | <span data-ttu-id="457bc-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="457bc-139">True</span></span>                                |
| <span data-ttu-id="457bc-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="457bc-140">Is Indexed</span></span>             | <span data-ttu-id="457bc-141">False</span><span class="sxs-lookup"><span data-stu-id="457bc-141">False</span></span>                               |
| <span data-ttu-id="457bc-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="457bc-142">In Global Catalog</span></span>      | <span data-ttu-id="457bc-143">False</span><span class="sxs-lookup"><span data-stu-id="457bc-143">False</span></span>                               |
| <span data-ttu-id="457bc-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="457bc-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="457bc-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="457bc-145">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="457bc-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="457bc-146">Range-Lower</span></span>            | <span data-ttu-id="457bc-147">0</span><span class="sxs-lookup"><span data-stu-id="457bc-147">0</span></span>                                   |
| <span data-ttu-id="457bc-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="457bc-148">Range-Upper</span></span>            | <span data-ttu-id="457bc-149">4096</span><span class="sxs-lookup"><span data-stu-id="457bc-149">4096</span></span>                                |
| <span data-ttu-id="457bc-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="457bc-150">Search-Flags</span></span>           | <span data-ttu-id="457bc-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="457bc-151">0x00000000</span></span>                          |
| <span data-ttu-id="457bc-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="457bc-152">System-Flags</span></span>           | <span data-ttu-id="457bc-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="457bc-153">0x00000010</span></span>                          |
| <span data-ttu-id="457bc-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="457bc-154">Classes used in</span></span>        | [<span data-ttu-id="457bc-155">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="457bc-155">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="457bc-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="457bc-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="457bc-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="457bc-157">Entry</span></span> | <span data-ttu-id="457bc-158">Wert</span><span class="sxs-lookup"><span data-stu-id="457bc-158">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="457bc-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="457bc-159">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="457bc-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="457bc-160">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="457bc-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="457bc-161">System-Only</span></span>            | <span data-ttu-id="457bc-162">False</span><span class="sxs-lookup"><span data-stu-id="457bc-162">False</span></span>                               |
| <span data-ttu-id="457bc-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="457bc-163">Is-Single-Valued</span></span>       | <span data-ttu-id="457bc-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="457bc-164">True</span></span>                                |
| <span data-ttu-id="457bc-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="457bc-165">Is Indexed</span></span>             | <span data-ttu-id="457bc-166">False</span><span class="sxs-lookup"><span data-stu-id="457bc-166">False</span></span>                               |
| <span data-ttu-id="457bc-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="457bc-167">In Global Catalog</span></span>      | <span data-ttu-id="457bc-168">False</span><span class="sxs-lookup"><span data-stu-id="457bc-168">False</span></span>                               |
| <span data-ttu-id="457bc-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="457bc-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="457bc-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="457bc-170">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="457bc-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="457bc-171">Range-Lower</span></span>            | <span data-ttu-id="457bc-172">0</span><span class="sxs-lookup"><span data-stu-id="457bc-172">0</span></span>                                   |
| <span data-ttu-id="457bc-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="457bc-173">Range-Upper</span></span>            | <span data-ttu-id="457bc-174">4096</span><span class="sxs-lookup"><span data-stu-id="457bc-174">4096</span></span>                                |
| <span data-ttu-id="457bc-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="457bc-175">Search-Flags</span></span>           | <span data-ttu-id="457bc-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="457bc-176">0x00000000</span></span>                          |
| <span data-ttu-id="457bc-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="457bc-177">System-Flags</span></span>           | <span data-ttu-id="457bc-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="457bc-178">0x00000010</span></span>                          |
| <span data-ttu-id="457bc-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="457bc-179">Classes used in</span></span>        | [<span data-ttu-id="457bc-180">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="457bc-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="457bc-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="457bc-181">Windows Server 2008</span></span>



| <span data-ttu-id="457bc-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="457bc-182">Entry</span></span> | <span data-ttu-id="457bc-183">Wert</span><span class="sxs-lookup"><span data-stu-id="457bc-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="457bc-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="457bc-184">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="457bc-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="457bc-185">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="457bc-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="457bc-186">System-Only</span></span>            | <span data-ttu-id="457bc-187">False</span><span class="sxs-lookup"><span data-stu-id="457bc-187">False</span></span>                               |
| <span data-ttu-id="457bc-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="457bc-188">Is-Single-Valued</span></span>       | <span data-ttu-id="457bc-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="457bc-189">True</span></span>                                |
| <span data-ttu-id="457bc-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="457bc-190">Is Indexed</span></span>             | <span data-ttu-id="457bc-191">False</span><span class="sxs-lookup"><span data-stu-id="457bc-191">False</span></span>                               |
| <span data-ttu-id="457bc-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="457bc-192">In Global Catalog</span></span>      | <span data-ttu-id="457bc-193">False</span><span class="sxs-lookup"><span data-stu-id="457bc-193">False</span></span>                               |
| <span data-ttu-id="457bc-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="457bc-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="457bc-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="457bc-195">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="457bc-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="457bc-196">Range-Lower</span></span>            | <span data-ttu-id="457bc-197">0</span><span class="sxs-lookup"><span data-stu-id="457bc-197">0</span></span>                                   |
| <span data-ttu-id="457bc-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="457bc-198">Range-Upper</span></span>            | <span data-ttu-id="457bc-199">4096</span><span class="sxs-lookup"><span data-stu-id="457bc-199">4096</span></span>                                |
| <span data-ttu-id="457bc-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="457bc-200">Search-Flags</span></span>           | <span data-ttu-id="457bc-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="457bc-201">0x00000000</span></span>                          |
| <span data-ttu-id="457bc-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="457bc-202">System-Flags</span></span>           | <span data-ttu-id="457bc-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="457bc-203">0x00000010</span></span>                          |
| <span data-ttu-id="457bc-204">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="457bc-204">Classes used in</span></span>        | [<span data-ttu-id="457bc-205">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="457bc-205">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="457bc-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="457bc-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="457bc-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="457bc-207">Entry</span></span> | <span data-ttu-id="457bc-208">Wert</span><span class="sxs-lookup"><span data-stu-id="457bc-208">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="457bc-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="457bc-209">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="457bc-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="457bc-210">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="457bc-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="457bc-211">System-Only</span></span>            | <span data-ttu-id="457bc-212">False</span><span class="sxs-lookup"><span data-stu-id="457bc-212">False</span></span>                               |
| <span data-ttu-id="457bc-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="457bc-213">Is-Single-Valued</span></span>       | <span data-ttu-id="457bc-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="457bc-214">True</span></span>                                |
| <span data-ttu-id="457bc-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="457bc-215">Is Indexed</span></span>             | <span data-ttu-id="457bc-216">False</span><span class="sxs-lookup"><span data-stu-id="457bc-216">False</span></span>                               |
| <span data-ttu-id="457bc-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="457bc-217">In Global Catalog</span></span>      | <span data-ttu-id="457bc-218">False</span><span class="sxs-lookup"><span data-stu-id="457bc-218">False</span></span>                               |
| <span data-ttu-id="457bc-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="457bc-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="457bc-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="457bc-220">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="457bc-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="457bc-221">Range-Lower</span></span>            | <span data-ttu-id="457bc-222">0</span><span class="sxs-lookup"><span data-stu-id="457bc-222">0</span></span>                                   |
| <span data-ttu-id="457bc-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="457bc-223">Range-Upper</span></span>            | <span data-ttu-id="457bc-224">4096</span><span class="sxs-lookup"><span data-stu-id="457bc-224">4096</span></span>                                |
| <span data-ttu-id="457bc-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="457bc-225">Search-Flags</span></span>           | <span data-ttu-id="457bc-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="457bc-226">0x00000000</span></span>                          |
| <span data-ttu-id="457bc-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="457bc-227">System-Flags</span></span>           | <span data-ttu-id="457bc-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="457bc-228">0x00000010</span></span>                          |
| <span data-ttu-id="457bc-229">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="457bc-229">Classes used in</span></span>        | [<span data-ttu-id="457bc-230">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="457bc-230">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="457bc-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="457bc-231">Windows Server 2012</span></span>



| <span data-ttu-id="457bc-232">Eingabe</span><span class="sxs-lookup"><span data-stu-id="457bc-232">Entry</span></span> | <span data-ttu-id="457bc-233">Wert</span><span class="sxs-lookup"><span data-stu-id="457bc-233">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="457bc-234">Link-ID</span><span class="sxs-lookup"><span data-stu-id="457bc-234">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="457bc-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="457bc-235">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="457bc-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="457bc-236">System-Only</span></span>            | <span data-ttu-id="457bc-237">False</span><span class="sxs-lookup"><span data-stu-id="457bc-237">False</span></span>                               |
| <span data-ttu-id="457bc-238">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="457bc-238">Is-Single-Valued</span></span>       | <span data-ttu-id="457bc-239">Richtig</span><span class="sxs-lookup"><span data-stu-id="457bc-239">True</span></span>                                |
| <span data-ttu-id="457bc-240">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="457bc-240">Is Indexed</span></span>             | <span data-ttu-id="457bc-241">False</span><span class="sxs-lookup"><span data-stu-id="457bc-241">False</span></span>                               |
| <span data-ttu-id="457bc-242">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="457bc-242">In Global Catalog</span></span>      | <span data-ttu-id="457bc-243">False</span><span class="sxs-lookup"><span data-stu-id="457bc-243">False</span></span>                               |
| <span data-ttu-id="457bc-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="457bc-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="457bc-245">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="457bc-245">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="457bc-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="457bc-246">Range-Lower</span></span>            | <span data-ttu-id="457bc-247">0</span><span class="sxs-lookup"><span data-stu-id="457bc-247">0</span></span>                                   |
| <span data-ttu-id="457bc-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="457bc-248">Range-Upper</span></span>            | <span data-ttu-id="457bc-249">4096</span><span class="sxs-lookup"><span data-stu-id="457bc-249">4096</span></span>                                |
| <span data-ttu-id="457bc-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="457bc-250">Search-Flags</span></span>           | <span data-ttu-id="457bc-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="457bc-251">0x00000000</span></span>                          |
| <span data-ttu-id="457bc-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="457bc-252">System-Flags</span></span>           | <span data-ttu-id="457bc-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="457bc-253">0x00000010</span></span>                          |
| <span data-ttu-id="457bc-254">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="457bc-254">Classes used in</span></span>        | [<span data-ttu-id="457bc-255">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="457bc-255">**Group**</span></span>](c-group.md)<br/> |



 

 





