---
title: MS-SQL-thirdparty-Attribut
description: Dieses Attribut gibt an, ob die Veröffentlichungsdaten aus einer anderen Datenquelle als SQL Server. Wenn Sie von einer anderen Quelle aus ist, wird Sie auf "true" festgelegt.
ms.assetid: 84d93b9f-0acc-47da-9f1b-44d8468ad53e
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-SQL-thirdparty-Attributs
- AD-Schema des MS-SQL-thirdparty-Attributs
topic_type:
- apiref
api_name:
- MS-SQL-ThirdParty
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc2b60f9589990f6357ee3c4cd24215e8af21df
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744297"
---
# <a name="ms-sql-thirdparty-attribute"></a><span data-ttu-id="88ed2-106">MS-SQL-thirdparty-Attribut</span><span class="sxs-lookup"><span data-stu-id="88ed2-106">MS-SQL-ThirdParty attribute</span></span>

<span data-ttu-id="88ed2-107">Dieses Attribut gibt an, ob die Veröffentlichungsdaten aus einer anderen Datenquelle als SQL Server.</span><span class="sxs-lookup"><span data-stu-id="88ed2-107">This attribute indicates whether the publication data is from a data source other than SQL Server.</span></span> <span data-ttu-id="88ed2-108">Wenn Sie von einer anderen Quelle aus ist, wird Sie auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="88ed2-108">If it is from another source, then it is set to **TRUE**.</span></span>



| <span data-ttu-id="88ed2-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88ed2-109">Entry</span></span> | <span data-ttu-id="88ed2-110">Wert</span><span class="sxs-lookup"><span data-stu-id="88ed2-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="88ed2-111">CN</span><span class="sxs-lookup"><span data-stu-id="88ed2-111">CN</span></span>                | <span data-ttu-id="88ed2-112">MS-SQL-thirdparty</span><span class="sxs-lookup"><span data-stu-id="88ed2-112">MS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="88ed2-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="88ed2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="88ed2-114">MS-SQL-thirdparty</span><span class="sxs-lookup"><span data-stu-id="88ed2-114">mS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="88ed2-115">Size</span><span class="sxs-lookup"><span data-stu-id="88ed2-115">Size</span></span>              | <span data-ttu-id="88ed2-116">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="88ed2-116">4 bytes</span></span>                              |
| <span data-ttu-id="88ed2-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="88ed2-117">Update Privilege</span></span>  | <span data-ttu-id="88ed2-118">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="88ed2-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="88ed2-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="88ed2-119">Update Frequency</span></span>  | <span data-ttu-id="88ed2-120">Wenn die Replikation eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="88ed2-120">When replication is setup.</span></span>           |
| <span data-ttu-id="88ed2-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="88ed2-121">Attribute-Id</span></span>      | <span data-ttu-id="88ed2-122">1.2.840.113556.1.4.1407</span><span class="sxs-lookup"><span data-stu-id="88ed2-122">1.2.840.113556.1.4.1407</span></span>              |
| <span data-ttu-id="88ed2-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="88ed2-123">System-Id-Guid</span></span>    | <span data-ttu-id="88ed2-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="88ed2-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span></span> |
| <span data-ttu-id="88ed2-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="88ed2-125">Syntax</span></span>            | [<span data-ttu-id="88ed2-126">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="88ed2-126">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="88ed2-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="88ed2-127">Implementations</span></span>

-   [<span data-ttu-id="88ed2-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="88ed2-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="88ed2-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="88ed2-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="88ed2-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="88ed2-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="88ed2-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="88ed2-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="88ed2-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="88ed2-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="88ed2-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="88ed2-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="88ed2-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="88ed2-134">Windows 2000 Server</span></span>



| <span data-ttu-id="88ed2-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88ed2-135">Entry</span></span> | <span data-ttu-id="88ed2-136">Wert</span><span class="sxs-lookup"><span data-stu-id="88ed2-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88ed2-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="88ed2-137">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88ed2-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88ed2-138">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88ed2-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="88ed2-139">System-Only</span></span>            | <span data-ttu-id="88ed2-140">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-140">False</span></span>                                                               |
| <span data-ttu-id="88ed2-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="88ed2-141">Is-Single-Valued</span></span>       | <span data-ttu-id="88ed2-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="88ed2-142">True</span></span>                                                                |
| <span data-ttu-id="88ed2-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="88ed2-143">Is Indexed</span></span>             | <span data-ttu-id="88ed2-144">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-144">False</span></span>                                                               |
| <span data-ttu-id="88ed2-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="88ed2-145">In Global Catalog</span></span>      | <span data-ttu-id="88ed2-146">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-146">False</span></span>                                                               |
| <span data-ttu-id="88ed2-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="88ed2-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="88ed2-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="88ed2-148">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="88ed2-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88ed2-149">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="88ed2-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88ed2-150">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="88ed2-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88ed2-151">Search-Flags</span></span>           | <span data-ttu-id="88ed2-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88ed2-152">0x00000000</span></span>                                                          |
| <span data-ttu-id="88ed2-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88ed2-153">System-Flags</span></span>           | <span data-ttu-id="88ed2-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88ed2-154">0x00000010</span></span>                                                          |
| <span data-ttu-id="88ed2-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="88ed2-155">Classes used in</span></span>        | [<span data-ttu-id="88ed2-156">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="88ed2-156">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="88ed2-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="88ed2-157">Windows Server 2003</span></span>



| <span data-ttu-id="88ed2-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88ed2-158">Entry</span></span> | <span data-ttu-id="88ed2-159">Wert</span><span class="sxs-lookup"><span data-stu-id="88ed2-159">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88ed2-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="88ed2-160">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88ed2-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88ed2-161">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88ed2-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="88ed2-162">System-Only</span></span>            | <span data-ttu-id="88ed2-163">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-163">False</span></span>                                                               |
| <span data-ttu-id="88ed2-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="88ed2-164">Is-Single-Valued</span></span>       | <span data-ttu-id="88ed2-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="88ed2-165">True</span></span>                                                                |
| <span data-ttu-id="88ed2-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="88ed2-166">Is Indexed</span></span>             | <span data-ttu-id="88ed2-167">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-167">False</span></span>                                                               |
| <span data-ttu-id="88ed2-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="88ed2-168">In Global Catalog</span></span>      | <span data-ttu-id="88ed2-169">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-169">False</span></span>                                                               |
| <span data-ttu-id="88ed2-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="88ed2-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="88ed2-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="88ed2-171">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="88ed2-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88ed2-172">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="88ed2-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88ed2-173">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="88ed2-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88ed2-174">Search-Flags</span></span>           | <span data-ttu-id="88ed2-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88ed2-175">0x00000000</span></span>                                                          |
| <span data-ttu-id="88ed2-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88ed2-176">System-Flags</span></span>           | <span data-ttu-id="88ed2-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88ed2-177">0x00000010</span></span>                                                          |
| <span data-ttu-id="88ed2-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="88ed2-178">Classes used in</span></span>        | [<span data-ttu-id="88ed2-179">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="88ed2-179">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="88ed2-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="88ed2-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="88ed2-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88ed2-181">Entry</span></span> | <span data-ttu-id="88ed2-182">Wert</span><span class="sxs-lookup"><span data-stu-id="88ed2-182">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88ed2-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="88ed2-183">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88ed2-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88ed2-184">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88ed2-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="88ed2-185">System-Only</span></span>            | <span data-ttu-id="88ed2-186">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-186">False</span></span>                                                               |
| <span data-ttu-id="88ed2-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="88ed2-187">Is-Single-Valued</span></span>       | <span data-ttu-id="88ed2-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="88ed2-188">True</span></span>                                                                |
| <span data-ttu-id="88ed2-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="88ed2-189">Is Indexed</span></span>             | <span data-ttu-id="88ed2-190">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-190">False</span></span>                                                               |
| <span data-ttu-id="88ed2-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="88ed2-191">In Global Catalog</span></span>      | <span data-ttu-id="88ed2-192">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-192">False</span></span>                                                               |
| <span data-ttu-id="88ed2-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="88ed2-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="88ed2-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="88ed2-194">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="88ed2-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88ed2-195">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="88ed2-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88ed2-196">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="88ed2-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88ed2-197">Search-Flags</span></span>           | <span data-ttu-id="88ed2-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88ed2-198">0x00000000</span></span>                                                          |
| <span data-ttu-id="88ed2-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88ed2-199">System-Flags</span></span>           | <span data-ttu-id="88ed2-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88ed2-200">0x00000010</span></span>                                                          |
| <span data-ttu-id="88ed2-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="88ed2-201">Classes used in</span></span>        | [<span data-ttu-id="88ed2-202">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="88ed2-202">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="88ed2-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88ed2-203">Windows Server 2008</span></span>



| <span data-ttu-id="88ed2-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88ed2-204">Entry</span></span> | <span data-ttu-id="88ed2-205">Wert</span><span class="sxs-lookup"><span data-stu-id="88ed2-205">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88ed2-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="88ed2-206">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88ed2-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88ed2-207">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88ed2-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="88ed2-208">System-Only</span></span>            | <span data-ttu-id="88ed2-209">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-209">False</span></span>                                                               |
| <span data-ttu-id="88ed2-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="88ed2-210">Is-Single-Valued</span></span>       | <span data-ttu-id="88ed2-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="88ed2-211">True</span></span>                                                                |
| <span data-ttu-id="88ed2-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="88ed2-212">Is Indexed</span></span>             | <span data-ttu-id="88ed2-213">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-213">False</span></span>                                                               |
| <span data-ttu-id="88ed2-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="88ed2-214">In Global Catalog</span></span>      | <span data-ttu-id="88ed2-215">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-215">False</span></span>                                                               |
| <span data-ttu-id="88ed2-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="88ed2-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="88ed2-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="88ed2-217">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="88ed2-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88ed2-218">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="88ed2-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88ed2-219">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="88ed2-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88ed2-220">Search-Flags</span></span>           | <span data-ttu-id="88ed2-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88ed2-221">0x00000000</span></span>                                                          |
| <span data-ttu-id="88ed2-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88ed2-222">System-Flags</span></span>           | <span data-ttu-id="88ed2-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88ed2-223">0x00000010</span></span>                                                          |
| <span data-ttu-id="88ed2-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="88ed2-224">Classes used in</span></span>        | [<span data-ttu-id="88ed2-225">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="88ed2-225">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="88ed2-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="88ed2-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="88ed2-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88ed2-227">Entry</span></span> | <span data-ttu-id="88ed2-228">Wert</span><span class="sxs-lookup"><span data-stu-id="88ed2-228">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88ed2-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="88ed2-229">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88ed2-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88ed2-230">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88ed2-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="88ed2-231">System-Only</span></span>            | <span data-ttu-id="88ed2-232">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-232">False</span></span>                                                               |
| <span data-ttu-id="88ed2-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="88ed2-233">Is-Single-Valued</span></span>       | <span data-ttu-id="88ed2-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="88ed2-234">True</span></span>                                                                |
| <span data-ttu-id="88ed2-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="88ed2-235">Is Indexed</span></span>             | <span data-ttu-id="88ed2-236">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-236">False</span></span>                                                               |
| <span data-ttu-id="88ed2-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="88ed2-237">In Global Catalog</span></span>      | <span data-ttu-id="88ed2-238">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-238">False</span></span>                                                               |
| <span data-ttu-id="88ed2-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="88ed2-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="88ed2-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="88ed2-240">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="88ed2-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88ed2-241">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="88ed2-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88ed2-242">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="88ed2-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88ed2-243">Search-Flags</span></span>           | <span data-ttu-id="88ed2-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88ed2-244">0x00000000</span></span>                                                          |
| <span data-ttu-id="88ed2-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88ed2-245">System-Flags</span></span>           | <span data-ttu-id="88ed2-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88ed2-246">0x00000010</span></span>                                                          |
| <span data-ttu-id="88ed2-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="88ed2-247">Classes used in</span></span>        | [<span data-ttu-id="88ed2-248">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="88ed2-248">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="88ed2-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88ed2-249">Windows Server 2012</span></span>



| <span data-ttu-id="88ed2-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88ed2-250">Entry</span></span> | <span data-ttu-id="88ed2-251">Wert</span><span class="sxs-lookup"><span data-stu-id="88ed2-251">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88ed2-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="88ed2-252">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88ed2-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88ed2-253">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88ed2-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="88ed2-254">System-Only</span></span>            | <span data-ttu-id="88ed2-255">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-255">False</span></span>                                                               |
| <span data-ttu-id="88ed2-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="88ed2-256">Is-Single-Valued</span></span>       | <span data-ttu-id="88ed2-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="88ed2-257">True</span></span>                                                                |
| <span data-ttu-id="88ed2-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="88ed2-258">Is Indexed</span></span>             | <span data-ttu-id="88ed2-259">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-259">False</span></span>                                                               |
| <span data-ttu-id="88ed2-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="88ed2-260">In Global Catalog</span></span>      | <span data-ttu-id="88ed2-261">False</span><span class="sxs-lookup"><span data-stu-id="88ed2-261">False</span></span>                                                               |
| <span data-ttu-id="88ed2-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="88ed2-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="88ed2-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="88ed2-263">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="88ed2-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88ed2-264">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="88ed2-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88ed2-265">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="88ed2-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88ed2-266">Search-Flags</span></span>           | <span data-ttu-id="88ed2-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88ed2-267">0x00000000</span></span>                                                          |
| <span data-ttu-id="88ed2-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88ed2-268">System-Flags</span></span>           | <span data-ttu-id="88ed2-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88ed2-269">0x00000010</span></span>                                                          |
| <span data-ttu-id="88ed2-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="88ed2-270">Classes used in</span></span>        | [<span data-ttu-id="88ed2-271">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="88ed2-271">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





