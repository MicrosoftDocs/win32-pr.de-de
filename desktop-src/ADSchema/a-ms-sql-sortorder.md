---
title: MS-SQL-sortor-Attribut
description: Die Sortierreihenfolge für die aktuelle Instanz von SQL Server.
ms.assetid: cd58cb56-19aa-4ee6-b241-1198b3e9e097
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-SQL-SortOrder-Attributs
- AD-Schema des MS-SQL-SortOrder-Attributs
topic_type:
- apiref
api_name:
- MS-SQL-SortOrder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940dafa4cc9bfce15ae1a5df472720e6e779f19e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344118"
---
# <a name="ms-sql-sortorder-attribute"></a><span data-ttu-id="db4c0-105">MS-SQL-sortor-Attribut</span><span class="sxs-lookup"><span data-stu-id="db4c0-105">MS-SQL-SortOrder attribute</span></span>

<span data-ttu-id="db4c0-106">Die Sortierreihenfolge für die aktuelle Instanz von SQL Server.</span><span class="sxs-lookup"><span data-stu-id="db4c0-106">The sort order for the current instance of SQL Server.</span></span>



| <span data-ttu-id="db4c0-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db4c0-107">Entry</span></span> | <span data-ttu-id="db4c0-108">Wert</span><span class="sxs-lookup"><span data-stu-id="db4c0-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="db4c0-109">CN</span><span class="sxs-lookup"><span data-stu-id="db4c0-109">CN</span></span>                | <span data-ttu-id="db4c0-110">MS-SQL-sortor</span><span class="sxs-lookup"><span data-stu-id="db4c0-110">MS-SQL-SortOrder</span></span>                            |
| <span data-ttu-id="db4c0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="db4c0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="db4c0-112">MS-SQL-sortor</span><span class="sxs-lookup"><span data-stu-id="db4c0-112">mS-SQL-SortOrder</span></span>                            |
| <span data-ttu-id="db4c0-113">Size</span><span class="sxs-lookup"><span data-stu-id="db4c0-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="db4c0-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="db4c0-114">Update Privilege</span></span>  | <span data-ttu-id="db4c0-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="db4c0-115">Domain administrator</span></span>                        |
| <span data-ttu-id="db4c0-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="db4c0-116">Update Frequency</span></span>  | <span data-ttu-id="db4c0-117">Beim System Setup.</span><span class="sxs-lookup"><span data-stu-id="db4c0-117">At system setup.</span></span>                            |
| <span data-ttu-id="db4c0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="db4c0-118">Attribute-Id</span></span>      | <span data-ttu-id="db4c0-119">1.2.840.113556.1.4.1371</span><span class="sxs-lookup"><span data-stu-id="db4c0-119">1.2.840.113556.1.4.1371</span></span>                     |
| <span data-ttu-id="db4c0-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="db4c0-120">System-Id-Guid</span></span>    | <span data-ttu-id="db4c0-121">6ddc42c0-CCEE-11d2-9993-0000f 87a57d4</span><span class="sxs-lookup"><span data-stu-id="db4c0-121">6ddc42c0-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="db4c0-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="db4c0-122">Syntax</span></span>            | [<span data-ttu-id="db4c0-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="db4c0-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="db4c0-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="db4c0-124">Implementations</span></span>

-   [<span data-ttu-id="db4c0-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="db4c0-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="db4c0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="db4c0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="db4c0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="db4c0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="db4c0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="db4c0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="db4c0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="db4c0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="db4c0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="db4c0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="db4c0-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="db4c0-131">Windows 2000 Server</span></span>



| <span data-ttu-id="db4c0-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db4c0-132">Entry</span></span> | <span data-ttu-id="db4c0-133">Wert</span><span class="sxs-lookup"><span data-stu-id="db4c0-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="db4c0-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db4c0-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="db4c0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db4c0-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="db4c0-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="db4c0-136">System-Only</span></span>            | <span data-ttu-id="db4c0-137">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-137">False</span></span>                                                     |
| <span data-ttu-id="db4c0-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db4c0-138">Is-Single-Valued</span></span>       | <span data-ttu-id="db4c0-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="db4c0-139">True</span></span>                                                      |
| <span data-ttu-id="db4c0-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db4c0-140">Is Indexed</span></span>             | <span data-ttu-id="db4c0-141">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-141">False</span></span>                                                     |
| <span data-ttu-id="db4c0-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db4c0-142">In Global Catalog</span></span>      | <span data-ttu-id="db4c0-143">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-143">False</span></span>                                                     |
| <span data-ttu-id="db4c0-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db4c0-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="db4c0-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db4c0-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="db4c0-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db4c0-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="db4c0-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db4c0-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="db4c0-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db4c0-148">Search-Flags</span></span>           | <span data-ttu-id="db4c0-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db4c0-149">0x00000000</span></span>                                                |
| <span data-ttu-id="db4c0-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db4c0-150">System-Flags</span></span>           | <span data-ttu-id="db4c0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db4c0-151">0x00000010</span></span>                                                |
| <span data-ttu-id="db4c0-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db4c0-152">Classes used in</span></span>        | [<span data-ttu-id="db4c0-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="db4c0-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="db4c0-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="db4c0-154">Windows Server 2003</span></span>



| <span data-ttu-id="db4c0-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db4c0-155">Entry</span></span> | <span data-ttu-id="db4c0-156">Wert</span><span class="sxs-lookup"><span data-stu-id="db4c0-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="db4c0-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db4c0-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="db4c0-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db4c0-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="db4c0-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="db4c0-159">System-Only</span></span>            | <span data-ttu-id="db4c0-160">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-160">False</span></span>                                                     |
| <span data-ttu-id="db4c0-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db4c0-161">Is-Single-Valued</span></span>       | <span data-ttu-id="db4c0-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="db4c0-162">True</span></span>                                                      |
| <span data-ttu-id="db4c0-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db4c0-163">Is Indexed</span></span>             | <span data-ttu-id="db4c0-164">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-164">False</span></span>                                                     |
| <span data-ttu-id="db4c0-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db4c0-165">In Global Catalog</span></span>      | <span data-ttu-id="db4c0-166">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-166">False</span></span>                                                     |
| <span data-ttu-id="db4c0-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db4c0-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="db4c0-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db4c0-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="db4c0-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db4c0-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="db4c0-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db4c0-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="db4c0-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db4c0-171">Search-Flags</span></span>           | <span data-ttu-id="db4c0-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db4c0-172">0x00000000</span></span>                                                |
| <span data-ttu-id="db4c0-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db4c0-173">System-Flags</span></span>           | <span data-ttu-id="db4c0-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db4c0-174">0x00000010</span></span>                                                |
| <span data-ttu-id="db4c0-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db4c0-175">Classes used in</span></span>        | [<span data-ttu-id="db4c0-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="db4c0-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="db4c0-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="db4c0-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="db4c0-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db4c0-178">Entry</span></span> | <span data-ttu-id="db4c0-179">Wert</span><span class="sxs-lookup"><span data-stu-id="db4c0-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="db4c0-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db4c0-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="db4c0-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db4c0-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="db4c0-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="db4c0-182">System-Only</span></span>            | <span data-ttu-id="db4c0-183">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-183">False</span></span>                                                     |
| <span data-ttu-id="db4c0-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db4c0-184">Is-Single-Valued</span></span>       | <span data-ttu-id="db4c0-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="db4c0-185">True</span></span>                                                      |
| <span data-ttu-id="db4c0-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db4c0-186">Is Indexed</span></span>             | <span data-ttu-id="db4c0-187">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-187">False</span></span>                                                     |
| <span data-ttu-id="db4c0-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db4c0-188">In Global Catalog</span></span>      | <span data-ttu-id="db4c0-189">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-189">False</span></span>                                                     |
| <span data-ttu-id="db4c0-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db4c0-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="db4c0-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db4c0-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="db4c0-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db4c0-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="db4c0-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db4c0-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="db4c0-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db4c0-194">Search-Flags</span></span>           | <span data-ttu-id="db4c0-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db4c0-195">0x00000000</span></span>                                                |
| <span data-ttu-id="db4c0-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db4c0-196">System-Flags</span></span>           | <span data-ttu-id="db4c0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db4c0-197">0x00000010</span></span>                                                |
| <span data-ttu-id="db4c0-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db4c0-198">Classes used in</span></span>        | [<span data-ttu-id="db4c0-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="db4c0-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="db4c0-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db4c0-200">Windows Server 2008</span></span>



| <span data-ttu-id="db4c0-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db4c0-201">Entry</span></span> | <span data-ttu-id="db4c0-202">Wert</span><span class="sxs-lookup"><span data-stu-id="db4c0-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="db4c0-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db4c0-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="db4c0-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db4c0-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="db4c0-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="db4c0-205">System-Only</span></span>            | <span data-ttu-id="db4c0-206">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-206">False</span></span>                                                     |
| <span data-ttu-id="db4c0-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db4c0-207">Is-Single-Valued</span></span>       | <span data-ttu-id="db4c0-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="db4c0-208">True</span></span>                                                      |
| <span data-ttu-id="db4c0-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db4c0-209">Is Indexed</span></span>             | <span data-ttu-id="db4c0-210">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-210">False</span></span>                                                     |
| <span data-ttu-id="db4c0-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db4c0-211">In Global Catalog</span></span>      | <span data-ttu-id="db4c0-212">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-212">False</span></span>                                                     |
| <span data-ttu-id="db4c0-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db4c0-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="db4c0-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db4c0-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="db4c0-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db4c0-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="db4c0-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db4c0-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="db4c0-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db4c0-217">Search-Flags</span></span>           | <span data-ttu-id="db4c0-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db4c0-218">0x00000000</span></span>                                                |
| <span data-ttu-id="db4c0-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db4c0-219">System-Flags</span></span>           | <span data-ttu-id="db4c0-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db4c0-220">0x00000010</span></span>                                                |
| <span data-ttu-id="db4c0-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db4c0-221">Classes used in</span></span>        | [<span data-ttu-id="db4c0-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="db4c0-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="db4c0-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="db4c0-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="db4c0-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db4c0-224">Entry</span></span> | <span data-ttu-id="db4c0-225">Wert</span><span class="sxs-lookup"><span data-stu-id="db4c0-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="db4c0-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db4c0-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="db4c0-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db4c0-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="db4c0-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="db4c0-228">System-Only</span></span>            | <span data-ttu-id="db4c0-229">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-229">False</span></span>                                                     |
| <span data-ttu-id="db4c0-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db4c0-230">Is-Single-Valued</span></span>       | <span data-ttu-id="db4c0-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="db4c0-231">True</span></span>                                                      |
| <span data-ttu-id="db4c0-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db4c0-232">Is Indexed</span></span>             | <span data-ttu-id="db4c0-233">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-233">False</span></span>                                                     |
| <span data-ttu-id="db4c0-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db4c0-234">In Global Catalog</span></span>      | <span data-ttu-id="db4c0-235">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-235">False</span></span>                                                     |
| <span data-ttu-id="db4c0-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db4c0-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="db4c0-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db4c0-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="db4c0-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db4c0-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="db4c0-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db4c0-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="db4c0-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db4c0-240">Search-Flags</span></span>           | <span data-ttu-id="db4c0-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db4c0-241">0x00000000</span></span>                                                |
| <span data-ttu-id="db4c0-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db4c0-242">System-Flags</span></span>           | <span data-ttu-id="db4c0-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db4c0-243">0x00000010</span></span>                                                |
| <span data-ttu-id="db4c0-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db4c0-244">Classes used in</span></span>        | [<span data-ttu-id="db4c0-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="db4c0-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="db4c0-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="db4c0-246">Windows Server 2012</span></span>



| <span data-ttu-id="db4c0-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db4c0-247">Entry</span></span> | <span data-ttu-id="db4c0-248">Wert</span><span class="sxs-lookup"><span data-stu-id="db4c0-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="db4c0-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db4c0-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="db4c0-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db4c0-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="db4c0-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="db4c0-251">System-Only</span></span>            | <span data-ttu-id="db4c0-252">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-252">False</span></span>                                                     |
| <span data-ttu-id="db4c0-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db4c0-253">Is-Single-Valued</span></span>       | <span data-ttu-id="db4c0-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="db4c0-254">True</span></span>                                                      |
| <span data-ttu-id="db4c0-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db4c0-255">Is Indexed</span></span>             | <span data-ttu-id="db4c0-256">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-256">False</span></span>                                                     |
| <span data-ttu-id="db4c0-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db4c0-257">In Global Catalog</span></span>      | <span data-ttu-id="db4c0-258">False</span><span class="sxs-lookup"><span data-stu-id="db4c0-258">False</span></span>                                                     |
| <span data-ttu-id="db4c0-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db4c0-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="db4c0-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db4c0-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="db4c0-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db4c0-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="db4c0-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db4c0-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="db4c0-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db4c0-263">Search-Flags</span></span>           | <span data-ttu-id="db4c0-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db4c0-264">0x00000000</span></span>                                                |
| <span data-ttu-id="db4c0-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db4c0-265">System-Flags</span></span>           | <span data-ttu-id="db4c0-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db4c0-266">0x00000010</span></span>                                                |
| <span data-ttu-id="db4c0-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db4c0-267">Classes used in</span></span>        | [<span data-ttu-id="db4c0-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="db4c0-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





