---
title: MS-SQL-Attributset-Attribut
description: Der Zeichensatz für die aktuelle Instanz von SQL Server.
ms.assetid: 5c45058f-e883-455c-8e18-415ddae149f8
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-SQL-Attributset-Attributs
- AD-Schema des MS-SQL-Attributset-Attributs
topic_type:
- apiref
api_name:
- MS-SQL-CharacterSet
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f2f3718c9e47393498e42c4091283ea768d5072
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859887"
---
# <a name="ms-sql-characterset-attribute"></a><span data-ttu-id="3f897-105">MS-SQL-Attributset-Attribut</span><span class="sxs-lookup"><span data-stu-id="3f897-105">MS-SQL-CharacterSet attribute</span></span>

<span data-ttu-id="3f897-106">Der Zeichensatz für die aktuelle Instanz von SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3f897-106">The character set for the current instance of SQL Server.</span></span>



| <span data-ttu-id="3f897-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3f897-107">Entry</span></span> | <span data-ttu-id="3f897-108">Wert</span><span class="sxs-lookup"><span data-stu-id="3f897-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="3f897-109">CN</span><span class="sxs-lookup"><span data-stu-id="3f897-109">CN</span></span>                | <span data-ttu-id="3f897-110">MS-SQL-Merkmal Satz</span><span class="sxs-lookup"><span data-stu-id="3f897-110">MS-SQL-CharacterSet</span></span>                  |
| <span data-ttu-id="3f897-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3f897-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3f897-112">MS-SQL-Merkmal Satz</span><span class="sxs-lookup"><span data-stu-id="3f897-112">mS-SQL-CharacterSet</span></span>                  |
| <span data-ttu-id="3f897-113">Size</span><span class="sxs-lookup"><span data-stu-id="3f897-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="3f897-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="3f897-114">Update Privilege</span></span>  | <span data-ttu-id="3f897-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3f897-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="3f897-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="3f897-116">Update Frequency</span></span>  | <span data-ttu-id="3f897-117">Beim Systemstart.</span><span class="sxs-lookup"><span data-stu-id="3f897-117">At system startup.</span></span>                   |
| <span data-ttu-id="3f897-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3f897-118">Attribute-Id</span></span>      | <span data-ttu-id="3f897-119">1.2.840.113556.1.4.1370</span><span class="sxs-lookup"><span data-stu-id="3f897-119">1.2.840.113556.1.4.1370</span></span>              |
| <span data-ttu-id="3f897-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3f897-120">System-Id-Guid</span></span>    | <span data-ttu-id="3f897-121">696177a6-CCEE-11d2-9993-0000f 87a57d4</span><span class="sxs-lookup"><span data-stu-id="3f897-121">696177a6-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="3f897-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f897-122">Syntax</span></span>            | [<span data-ttu-id="3f897-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="3f897-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="3f897-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="3f897-124">Implementations</span></span>

-   [<span data-ttu-id="3f897-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3f897-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3f897-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3f897-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3f897-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3f897-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3f897-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3f897-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3f897-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3f897-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3f897-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3f897-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3f897-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3f897-131">Windows 2000 Server</span></span>



| <span data-ttu-id="3f897-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3f897-132">Entry</span></span> | <span data-ttu-id="3f897-133">Wert</span><span class="sxs-lookup"><span data-stu-id="3f897-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3f897-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3f897-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3f897-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f897-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3f897-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f897-136">System-Only</span></span>            | <span data-ttu-id="3f897-137">False</span><span class="sxs-lookup"><span data-stu-id="3f897-137">False</span></span>                                                     |
| <span data-ttu-id="3f897-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3f897-138">Is-Single-Valued</span></span>       | <span data-ttu-id="3f897-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="3f897-139">True</span></span>                                                      |
| <span data-ttu-id="3f897-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3f897-140">Is Indexed</span></span>             | <span data-ttu-id="3f897-141">False</span><span class="sxs-lookup"><span data-stu-id="3f897-141">False</span></span>                                                     |
| <span data-ttu-id="3f897-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3f897-142">In Global Catalog</span></span>      | <span data-ttu-id="3f897-143">False</span><span class="sxs-lookup"><span data-stu-id="3f897-143">False</span></span>                                                     |
| <span data-ttu-id="3f897-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f897-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f897-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3f897-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3f897-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f897-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="3f897-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f897-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="3f897-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f897-148">Search-Flags</span></span>           | <span data-ttu-id="3f897-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f897-149">0x00000000</span></span>                                                |
| <span data-ttu-id="3f897-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f897-150">System-Flags</span></span>           | <span data-ttu-id="3f897-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f897-151">0x00000010</span></span>                                                |
| <span data-ttu-id="3f897-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3f897-152">Classes used in</span></span>        | [<span data-ttu-id="3f897-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="3f897-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3f897-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3f897-154">Windows Server 2003</span></span>



| <span data-ttu-id="3f897-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3f897-155">Entry</span></span> | <span data-ttu-id="3f897-156">Wert</span><span class="sxs-lookup"><span data-stu-id="3f897-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3f897-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3f897-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3f897-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f897-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3f897-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f897-159">System-Only</span></span>            | <span data-ttu-id="3f897-160">False</span><span class="sxs-lookup"><span data-stu-id="3f897-160">False</span></span>                                                     |
| <span data-ttu-id="3f897-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3f897-161">Is-Single-Valued</span></span>       | <span data-ttu-id="3f897-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="3f897-162">True</span></span>                                                      |
| <span data-ttu-id="3f897-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3f897-163">Is Indexed</span></span>             | <span data-ttu-id="3f897-164">False</span><span class="sxs-lookup"><span data-stu-id="3f897-164">False</span></span>                                                     |
| <span data-ttu-id="3f897-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3f897-165">In Global Catalog</span></span>      | <span data-ttu-id="3f897-166">False</span><span class="sxs-lookup"><span data-stu-id="3f897-166">False</span></span>                                                     |
| <span data-ttu-id="3f897-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f897-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f897-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3f897-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3f897-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f897-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="3f897-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f897-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="3f897-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f897-171">Search-Flags</span></span>           | <span data-ttu-id="3f897-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f897-172">0x00000000</span></span>                                                |
| <span data-ttu-id="3f897-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f897-173">System-Flags</span></span>           | <span data-ttu-id="3f897-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f897-174">0x00000010</span></span>                                                |
| <span data-ttu-id="3f897-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3f897-175">Classes used in</span></span>        | [<span data-ttu-id="3f897-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="3f897-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3f897-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3f897-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3f897-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3f897-178">Entry</span></span> | <span data-ttu-id="3f897-179">Wert</span><span class="sxs-lookup"><span data-stu-id="3f897-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3f897-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3f897-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3f897-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f897-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3f897-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f897-182">System-Only</span></span>            | <span data-ttu-id="3f897-183">False</span><span class="sxs-lookup"><span data-stu-id="3f897-183">False</span></span>                                                     |
| <span data-ttu-id="3f897-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3f897-184">Is-Single-Valued</span></span>       | <span data-ttu-id="3f897-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="3f897-185">True</span></span>                                                      |
| <span data-ttu-id="3f897-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3f897-186">Is Indexed</span></span>             | <span data-ttu-id="3f897-187">False</span><span class="sxs-lookup"><span data-stu-id="3f897-187">False</span></span>                                                     |
| <span data-ttu-id="3f897-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3f897-188">In Global Catalog</span></span>      | <span data-ttu-id="3f897-189">False</span><span class="sxs-lookup"><span data-stu-id="3f897-189">False</span></span>                                                     |
| <span data-ttu-id="3f897-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f897-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f897-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3f897-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3f897-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f897-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="3f897-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f897-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="3f897-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f897-194">Search-Flags</span></span>           | <span data-ttu-id="3f897-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f897-195">0x00000000</span></span>                                                |
| <span data-ttu-id="3f897-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f897-196">System-Flags</span></span>           | <span data-ttu-id="3f897-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f897-197">0x00000010</span></span>                                                |
| <span data-ttu-id="3f897-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3f897-198">Classes used in</span></span>        | [<span data-ttu-id="3f897-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="3f897-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3f897-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f897-200">Windows Server 2008</span></span>



| <span data-ttu-id="3f897-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3f897-201">Entry</span></span> | <span data-ttu-id="3f897-202">Wert</span><span class="sxs-lookup"><span data-stu-id="3f897-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3f897-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3f897-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3f897-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f897-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3f897-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f897-205">System-Only</span></span>            | <span data-ttu-id="3f897-206">False</span><span class="sxs-lookup"><span data-stu-id="3f897-206">False</span></span>                                                     |
| <span data-ttu-id="3f897-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3f897-207">Is-Single-Valued</span></span>       | <span data-ttu-id="3f897-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="3f897-208">True</span></span>                                                      |
| <span data-ttu-id="3f897-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3f897-209">Is Indexed</span></span>             | <span data-ttu-id="3f897-210">False</span><span class="sxs-lookup"><span data-stu-id="3f897-210">False</span></span>                                                     |
| <span data-ttu-id="3f897-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3f897-211">In Global Catalog</span></span>      | <span data-ttu-id="3f897-212">False</span><span class="sxs-lookup"><span data-stu-id="3f897-212">False</span></span>                                                     |
| <span data-ttu-id="3f897-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f897-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f897-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3f897-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3f897-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f897-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="3f897-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f897-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="3f897-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f897-217">Search-Flags</span></span>           | <span data-ttu-id="3f897-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f897-218">0x00000000</span></span>                                                |
| <span data-ttu-id="3f897-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f897-219">System-Flags</span></span>           | <span data-ttu-id="3f897-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f897-220">0x00000010</span></span>                                                |
| <span data-ttu-id="3f897-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3f897-221">Classes used in</span></span>        | [<span data-ttu-id="3f897-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="3f897-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3f897-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3f897-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3f897-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3f897-224">Entry</span></span> | <span data-ttu-id="3f897-225">Wert</span><span class="sxs-lookup"><span data-stu-id="3f897-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3f897-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3f897-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3f897-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f897-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3f897-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f897-228">System-Only</span></span>            | <span data-ttu-id="3f897-229">False</span><span class="sxs-lookup"><span data-stu-id="3f897-229">False</span></span>                                                     |
| <span data-ttu-id="3f897-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3f897-230">Is-Single-Valued</span></span>       | <span data-ttu-id="3f897-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="3f897-231">True</span></span>                                                      |
| <span data-ttu-id="3f897-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3f897-232">Is Indexed</span></span>             | <span data-ttu-id="3f897-233">False</span><span class="sxs-lookup"><span data-stu-id="3f897-233">False</span></span>                                                     |
| <span data-ttu-id="3f897-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3f897-234">In Global Catalog</span></span>      | <span data-ttu-id="3f897-235">False</span><span class="sxs-lookup"><span data-stu-id="3f897-235">False</span></span>                                                     |
| <span data-ttu-id="3f897-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f897-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f897-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3f897-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3f897-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f897-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="3f897-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f897-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="3f897-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f897-240">Search-Flags</span></span>           | <span data-ttu-id="3f897-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f897-241">0x00000000</span></span>                                                |
| <span data-ttu-id="3f897-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f897-242">System-Flags</span></span>           | <span data-ttu-id="3f897-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f897-243">0x00000010</span></span>                                                |
| <span data-ttu-id="3f897-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3f897-244">Classes used in</span></span>        | [<span data-ttu-id="3f897-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="3f897-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3f897-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3f897-246">Windows Server 2012</span></span>



| <span data-ttu-id="3f897-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3f897-247">Entry</span></span> | <span data-ttu-id="3f897-248">Wert</span><span class="sxs-lookup"><span data-stu-id="3f897-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3f897-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3f897-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3f897-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f897-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3f897-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f897-251">System-Only</span></span>            | <span data-ttu-id="3f897-252">False</span><span class="sxs-lookup"><span data-stu-id="3f897-252">False</span></span>                                                     |
| <span data-ttu-id="3f897-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3f897-253">Is-Single-Valued</span></span>       | <span data-ttu-id="3f897-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="3f897-254">True</span></span>                                                      |
| <span data-ttu-id="3f897-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3f897-255">Is Indexed</span></span>             | <span data-ttu-id="3f897-256">False</span><span class="sxs-lookup"><span data-stu-id="3f897-256">False</span></span>                                                     |
| <span data-ttu-id="3f897-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3f897-257">In Global Catalog</span></span>      | <span data-ttu-id="3f897-258">False</span><span class="sxs-lookup"><span data-stu-id="3f897-258">False</span></span>                                                     |
| <span data-ttu-id="3f897-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f897-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f897-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3f897-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3f897-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f897-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="3f897-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f897-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="3f897-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f897-263">Search-Flags</span></span>           | <span data-ttu-id="3f897-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f897-264">0x00000000</span></span>                                                |
| <span data-ttu-id="3f897-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f897-265">System-Flags</span></span>           | <span data-ttu-id="3f897-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f897-266">0x00000010</span></span>                                                |
| <span data-ttu-id="3f897-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3f897-267">Classes used in</span></span>        | [<span data-ttu-id="3f897-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="3f897-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





