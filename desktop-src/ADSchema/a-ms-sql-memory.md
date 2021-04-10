---
title: MS-SQL-Memory-Attribut
description: Die Menge des Arbeitsspeichers auf dem Computer.
ms.assetid: 36d69b8a-669b-4488-a75e-3b0af7f9845a
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-SQL-Memory-Attributs
- AD-Schema des MS-SQL-Memory-Attributs
topic_type:
- apiref
api_name:
- MS-SQL-Memory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d7f6b96f2a591e05df8bf325b028172ef713dc5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123044"
---
# <a name="ms-sql-memory-attribute"></a><span data-ttu-id="d4892-105">MS-SQL-Memory-Attribut</span><span class="sxs-lookup"><span data-stu-id="d4892-105">MS-SQL-Memory attribute</span></span>

<span data-ttu-id="d4892-106">Die Menge des Arbeitsspeichers auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="d4892-106">The amount of memory on the computer.</span></span>



| <span data-ttu-id="d4892-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d4892-107">Entry</span></span> | <span data-ttu-id="d4892-108">Wert</span><span class="sxs-lookup"><span data-stu-id="d4892-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d4892-109">CN</span><span class="sxs-lookup"><span data-stu-id="d4892-109">CN</span></span>                | <span data-ttu-id="d4892-110">MS-SQL-Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="d4892-110">MS-SQL-Memory</span></span>                        |
| <span data-ttu-id="d4892-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d4892-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d4892-112">MS-SQL-Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="d4892-112">mS-SQL-Memory</span></span>                        |
| <span data-ttu-id="d4892-113">Size</span><span class="sxs-lookup"><span data-stu-id="d4892-113">Size</span></span>              | <span data-ttu-id="d4892-114">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="d4892-114">8 bytes</span></span>                              |
| <span data-ttu-id="d4892-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d4892-115">Update Privilege</span></span>  | <span data-ttu-id="d4892-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d4892-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="d4892-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="d4892-117">Update Frequency</span></span>  | <span data-ttu-id="d4892-118">Beim Systemstart.</span><span class="sxs-lookup"><span data-stu-id="d4892-118">At system startup.</span></span>                   |
| <span data-ttu-id="d4892-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d4892-119">Attribute-Id</span></span>      | <span data-ttu-id="d4892-120">1.2.840.113556.1.4.1367</span><span class="sxs-lookup"><span data-stu-id="d4892-120">1.2.840.113556.1.4.1367</span></span>              |
| <span data-ttu-id="d4892-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d4892-121">System-Id-Guid</span></span>    | <span data-ttu-id="d4892-122">5b5d448c-CCEE-11d2-9993-0000f 87a57d4</span><span class="sxs-lookup"><span data-stu-id="d4892-122">5b5d448c-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="d4892-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4892-123">Syntax</span></span>            | [<span data-ttu-id="d4892-124">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="d4892-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="d4892-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="d4892-125">Implementations</span></span>

-   [<span data-ttu-id="d4892-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d4892-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d4892-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d4892-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d4892-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d4892-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d4892-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d4892-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d4892-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d4892-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d4892-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d4892-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d4892-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d4892-132">Windows 2000 Server</span></span>



| <span data-ttu-id="d4892-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d4892-133">Entry</span></span> | <span data-ttu-id="d4892-134">Wert</span><span class="sxs-lookup"><span data-stu-id="d4892-134">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d4892-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d4892-135">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d4892-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4892-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d4892-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4892-137">System-Only</span></span>            | <span data-ttu-id="d4892-138">False</span><span class="sxs-lookup"><span data-stu-id="d4892-138">False</span></span>                                                     |
| <span data-ttu-id="d4892-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d4892-139">Is-Single-Valued</span></span>       | <span data-ttu-id="d4892-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="d4892-140">True</span></span>                                                      |
| <span data-ttu-id="d4892-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d4892-141">Is Indexed</span></span>             | <span data-ttu-id="d4892-142">False</span><span class="sxs-lookup"><span data-stu-id="d4892-142">False</span></span>                                                     |
| <span data-ttu-id="d4892-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d4892-143">In Global Catalog</span></span>      | <span data-ttu-id="d4892-144">False</span><span class="sxs-lookup"><span data-stu-id="d4892-144">False</span></span>                                                     |
| <span data-ttu-id="d4892-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d4892-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4892-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d4892-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d4892-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4892-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d4892-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4892-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d4892-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4892-149">Search-Flags</span></span>           | <span data-ttu-id="d4892-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4892-150">0x00000000</span></span>                                                |
| <span data-ttu-id="d4892-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4892-151">System-Flags</span></span>           | <span data-ttu-id="d4892-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4892-152">0x00000010</span></span>                                                |
| <span data-ttu-id="d4892-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d4892-153">Classes used in</span></span>        | [<span data-ttu-id="d4892-154">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d4892-154">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d4892-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d4892-155">Windows Server 2003</span></span>



| <span data-ttu-id="d4892-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d4892-156">Entry</span></span> | <span data-ttu-id="d4892-157">Wert</span><span class="sxs-lookup"><span data-stu-id="d4892-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d4892-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d4892-158">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d4892-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4892-159">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d4892-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4892-160">System-Only</span></span>            | <span data-ttu-id="d4892-161">False</span><span class="sxs-lookup"><span data-stu-id="d4892-161">False</span></span>                                                     |
| <span data-ttu-id="d4892-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d4892-162">Is-Single-Valued</span></span>       | <span data-ttu-id="d4892-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="d4892-163">True</span></span>                                                      |
| <span data-ttu-id="d4892-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d4892-164">Is Indexed</span></span>             | <span data-ttu-id="d4892-165">False</span><span class="sxs-lookup"><span data-stu-id="d4892-165">False</span></span>                                                     |
| <span data-ttu-id="d4892-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d4892-166">In Global Catalog</span></span>      | <span data-ttu-id="d4892-167">False</span><span class="sxs-lookup"><span data-stu-id="d4892-167">False</span></span>                                                     |
| <span data-ttu-id="d4892-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d4892-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4892-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d4892-169">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d4892-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4892-170">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d4892-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4892-171">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d4892-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4892-172">Search-Flags</span></span>           | <span data-ttu-id="d4892-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4892-173">0x00000000</span></span>                                                |
| <span data-ttu-id="d4892-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4892-174">System-Flags</span></span>           | <span data-ttu-id="d4892-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4892-175">0x00000010</span></span>                                                |
| <span data-ttu-id="d4892-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d4892-176">Classes used in</span></span>        | [<span data-ttu-id="d4892-177">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d4892-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d4892-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d4892-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d4892-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d4892-179">Entry</span></span> | <span data-ttu-id="d4892-180">Wert</span><span class="sxs-lookup"><span data-stu-id="d4892-180">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d4892-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d4892-181">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d4892-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4892-182">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d4892-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4892-183">System-Only</span></span>            | <span data-ttu-id="d4892-184">False</span><span class="sxs-lookup"><span data-stu-id="d4892-184">False</span></span>                                                     |
| <span data-ttu-id="d4892-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d4892-185">Is-Single-Valued</span></span>       | <span data-ttu-id="d4892-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="d4892-186">True</span></span>                                                      |
| <span data-ttu-id="d4892-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d4892-187">Is Indexed</span></span>             | <span data-ttu-id="d4892-188">False</span><span class="sxs-lookup"><span data-stu-id="d4892-188">False</span></span>                                                     |
| <span data-ttu-id="d4892-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d4892-189">In Global Catalog</span></span>      | <span data-ttu-id="d4892-190">False</span><span class="sxs-lookup"><span data-stu-id="d4892-190">False</span></span>                                                     |
| <span data-ttu-id="d4892-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d4892-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4892-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d4892-192">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d4892-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4892-193">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d4892-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4892-194">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d4892-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4892-195">Search-Flags</span></span>           | <span data-ttu-id="d4892-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4892-196">0x00000000</span></span>                                                |
| <span data-ttu-id="d4892-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4892-197">System-Flags</span></span>           | <span data-ttu-id="d4892-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4892-198">0x00000010</span></span>                                                |
| <span data-ttu-id="d4892-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d4892-199">Classes used in</span></span>        | [<span data-ttu-id="d4892-200">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d4892-200">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d4892-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4892-201">Windows Server 2008</span></span>



| <span data-ttu-id="d4892-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d4892-202">Entry</span></span> | <span data-ttu-id="d4892-203">Wert</span><span class="sxs-lookup"><span data-stu-id="d4892-203">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d4892-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d4892-204">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d4892-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4892-205">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d4892-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4892-206">System-Only</span></span>            | <span data-ttu-id="d4892-207">False</span><span class="sxs-lookup"><span data-stu-id="d4892-207">False</span></span>                                                     |
| <span data-ttu-id="d4892-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d4892-208">Is-Single-Valued</span></span>       | <span data-ttu-id="d4892-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="d4892-209">True</span></span>                                                      |
| <span data-ttu-id="d4892-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d4892-210">Is Indexed</span></span>             | <span data-ttu-id="d4892-211">False</span><span class="sxs-lookup"><span data-stu-id="d4892-211">False</span></span>                                                     |
| <span data-ttu-id="d4892-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d4892-212">In Global Catalog</span></span>      | <span data-ttu-id="d4892-213">False</span><span class="sxs-lookup"><span data-stu-id="d4892-213">False</span></span>                                                     |
| <span data-ttu-id="d4892-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d4892-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4892-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d4892-215">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d4892-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4892-216">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d4892-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4892-217">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d4892-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4892-218">Search-Flags</span></span>           | <span data-ttu-id="d4892-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4892-219">0x00000000</span></span>                                                |
| <span data-ttu-id="d4892-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4892-220">System-Flags</span></span>           | <span data-ttu-id="d4892-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4892-221">0x00000010</span></span>                                                |
| <span data-ttu-id="d4892-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d4892-222">Classes used in</span></span>        | [<span data-ttu-id="d4892-223">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d4892-223">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d4892-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d4892-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d4892-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d4892-225">Entry</span></span> | <span data-ttu-id="d4892-226">Wert</span><span class="sxs-lookup"><span data-stu-id="d4892-226">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d4892-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d4892-227">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d4892-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4892-228">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d4892-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4892-229">System-Only</span></span>            | <span data-ttu-id="d4892-230">False</span><span class="sxs-lookup"><span data-stu-id="d4892-230">False</span></span>                                                     |
| <span data-ttu-id="d4892-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d4892-231">Is-Single-Valued</span></span>       | <span data-ttu-id="d4892-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="d4892-232">True</span></span>                                                      |
| <span data-ttu-id="d4892-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d4892-233">Is Indexed</span></span>             | <span data-ttu-id="d4892-234">False</span><span class="sxs-lookup"><span data-stu-id="d4892-234">False</span></span>                                                     |
| <span data-ttu-id="d4892-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d4892-235">In Global Catalog</span></span>      | <span data-ttu-id="d4892-236">False</span><span class="sxs-lookup"><span data-stu-id="d4892-236">False</span></span>                                                     |
| <span data-ttu-id="d4892-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d4892-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4892-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d4892-238">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d4892-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4892-239">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d4892-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4892-240">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d4892-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4892-241">Search-Flags</span></span>           | <span data-ttu-id="d4892-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4892-242">0x00000000</span></span>                                                |
| <span data-ttu-id="d4892-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4892-243">System-Flags</span></span>           | <span data-ttu-id="d4892-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4892-244">0x00000010</span></span>                                                |
| <span data-ttu-id="d4892-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d4892-245">Classes used in</span></span>        | [<span data-ttu-id="d4892-246">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d4892-246">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d4892-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d4892-247">Windows Server 2012</span></span>



| <span data-ttu-id="d4892-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d4892-248">Entry</span></span> | <span data-ttu-id="d4892-249">Wert</span><span class="sxs-lookup"><span data-stu-id="d4892-249">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d4892-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d4892-250">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d4892-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4892-251">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d4892-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4892-252">System-Only</span></span>            | <span data-ttu-id="d4892-253">False</span><span class="sxs-lookup"><span data-stu-id="d4892-253">False</span></span>                                                     |
| <span data-ttu-id="d4892-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d4892-254">Is-Single-Valued</span></span>       | <span data-ttu-id="d4892-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="d4892-255">True</span></span>                                                      |
| <span data-ttu-id="d4892-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d4892-256">Is Indexed</span></span>             | <span data-ttu-id="d4892-257">False</span><span class="sxs-lookup"><span data-stu-id="d4892-257">False</span></span>                                                     |
| <span data-ttu-id="d4892-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d4892-258">In Global Catalog</span></span>      | <span data-ttu-id="d4892-259">False</span><span class="sxs-lookup"><span data-stu-id="d4892-259">False</span></span>                                                     |
| <span data-ttu-id="d4892-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d4892-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4892-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d4892-261">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d4892-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4892-262">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d4892-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4892-263">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d4892-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4892-264">Search-Flags</span></span>           | <span data-ttu-id="d4892-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4892-265">0x00000000</span></span>                                                |
| <span data-ttu-id="d4892-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4892-266">System-Flags</span></span>           | <span data-ttu-id="d4892-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4892-267">0x00000010</span></span>                                                |
| <span data-ttu-id="d4892-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d4892-268">Classes used in</span></span>        | [<span data-ttu-id="d4892-269">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d4892-269">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





