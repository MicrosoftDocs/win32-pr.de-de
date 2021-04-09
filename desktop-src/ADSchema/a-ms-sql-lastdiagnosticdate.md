---
title: MS-SQL-lastdiagnosticdate-Attribut
description: Das letzte Datum, an dem DBCC CHECKDB ausgeführt wurde.
ms.assetid: 7060e111-e4cb-4c5a-bce1-32712cbea00e
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-SQL-lastdiagnosticdate-Attributs
- AD-Schema des MS-SQL-lastdiagnosticdate-Attributs
topic_type:
- apiref
api_name:
- MS-SQL-LastDiagnosticDate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f25b8322a9f83b96c0ab4883478e6c0ffa2f3b49
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744320"
---
# <a name="ms-sql-lastdiagnosticdate-attribute"></a><span data-ttu-id="812ff-105">MS-SQL-lastdiagnosticdate-Attribut</span><span class="sxs-lookup"><span data-stu-id="812ff-105">MS-SQL-LastDiagnosticDate attribute</span></span>

<span data-ttu-id="812ff-106">Das letzte Datum, an dem DBCC CHECKDB ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="812ff-106">The last date that DBCC checkdb was run.</span></span>



| <span data-ttu-id="812ff-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="812ff-107">Entry</span></span> | <span data-ttu-id="812ff-108">Wert</span><span class="sxs-lookup"><span data-stu-id="812ff-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="812ff-109">CN</span><span class="sxs-lookup"><span data-stu-id="812ff-109">CN</span></span>                | <span data-ttu-id="812ff-110">MS-SQL-lastdiagnosticdate</span><span class="sxs-lookup"><span data-stu-id="812ff-110">MS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="812ff-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="812ff-111">Ldap-Display-Name</span></span> | <span data-ttu-id="812ff-112">MS-SQL-lastdiagnosticdate</span><span class="sxs-lookup"><span data-stu-id="812ff-112">mS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="812ff-113">Size</span><span class="sxs-lookup"><span data-stu-id="812ff-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="812ff-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="812ff-114">Update Privilege</span></span>  | <span data-ttu-id="812ff-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="812ff-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="812ff-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="812ff-116">Update Frequency</span></span>  | <span data-ttu-id="812ff-117">Wenn DBCC CHECKDB ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="812ff-117">When DBCC checkdb is run.</span></span>                   |
| <span data-ttu-id="812ff-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="812ff-118">Attribute-Id</span></span>      | <span data-ttu-id="812ff-119">1.2.840.113556.1.4.1399</span><span class="sxs-lookup"><span data-stu-id="812ff-119">1.2.840.113556.1.4.1399</span></span>                     |
| <span data-ttu-id="812ff-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="812ff-120">System-Id-Guid</span></span>    | <span data-ttu-id="812ff-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="812ff-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="812ff-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="812ff-122">Syntax</span></span>            | [<span data-ttu-id="812ff-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="812ff-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="812ff-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="812ff-124">Implementations</span></span>

-   [<span data-ttu-id="812ff-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="812ff-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="812ff-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="812ff-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="812ff-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="812ff-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="812ff-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="812ff-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="812ff-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="812ff-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="812ff-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="812ff-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="812ff-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="812ff-131">Windows 2000 Server</span></span>



| <span data-ttu-id="812ff-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="812ff-132">Entry</span></span> | <span data-ttu-id="812ff-133">Wert</span><span class="sxs-lookup"><span data-stu-id="812ff-133">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="812ff-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="812ff-134">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="812ff-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="812ff-135">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="812ff-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="812ff-136">System-Only</span></span>            | <span data-ttu-id="812ff-137">False</span><span class="sxs-lookup"><span data-stu-id="812ff-137">False</span></span>                                                         |
| <span data-ttu-id="812ff-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="812ff-138">Is-Single-Valued</span></span>       | <span data-ttu-id="812ff-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="812ff-139">True</span></span>                                                          |
| <span data-ttu-id="812ff-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="812ff-140">Is Indexed</span></span>             | <span data-ttu-id="812ff-141">False</span><span class="sxs-lookup"><span data-stu-id="812ff-141">False</span></span>                                                         |
| <span data-ttu-id="812ff-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="812ff-142">In Global Catalog</span></span>      | <span data-ttu-id="812ff-143">False</span><span class="sxs-lookup"><span data-stu-id="812ff-143">False</span></span>                                                         |
| <span data-ttu-id="812ff-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="812ff-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="812ff-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="812ff-145">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="812ff-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="812ff-146">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="812ff-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="812ff-147">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="812ff-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="812ff-148">Search-Flags</span></span>           | <span data-ttu-id="812ff-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="812ff-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="812ff-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="812ff-150">System-Flags</span></span>           | <span data-ttu-id="812ff-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="812ff-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="812ff-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="812ff-152">Classes used in</span></span>        | [<span data-ttu-id="812ff-153">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="812ff-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="812ff-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="812ff-154">Windows Server 2003</span></span>



| <span data-ttu-id="812ff-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="812ff-155">Entry</span></span> | <span data-ttu-id="812ff-156">Wert</span><span class="sxs-lookup"><span data-stu-id="812ff-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="812ff-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="812ff-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="812ff-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="812ff-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="812ff-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="812ff-159">System-Only</span></span>            | <span data-ttu-id="812ff-160">False</span><span class="sxs-lookup"><span data-stu-id="812ff-160">False</span></span>                                                         |
| <span data-ttu-id="812ff-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="812ff-161">Is-Single-Valued</span></span>       | <span data-ttu-id="812ff-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="812ff-162">True</span></span>                                                          |
| <span data-ttu-id="812ff-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="812ff-163">Is Indexed</span></span>             | <span data-ttu-id="812ff-164">False</span><span class="sxs-lookup"><span data-stu-id="812ff-164">False</span></span>                                                         |
| <span data-ttu-id="812ff-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="812ff-165">In Global Catalog</span></span>      | <span data-ttu-id="812ff-166">False</span><span class="sxs-lookup"><span data-stu-id="812ff-166">False</span></span>                                                         |
| <span data-ttu-id="812ff-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="812ff-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="812ff-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="812ff-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="812ff-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="812ff-169">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="812ff-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="812ff-170">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="812ff-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="812ff-171">Search-Flags</span></span>           | <span data-ttu-id="812ff-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="812ff-172">0x00000000</span></span>                                                    |
| <span data-ttu-id="812ff-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="812ff-173">System-Flags</span></span>           | <span data-ttu-id="812ff-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="812ff-174">0x00000010</span></span>                                                    |
| <span data-ttu-id="812ff-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="812ff-175">Classes used in</span></span>        | [<span data-ttu-id="812ff-176">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="812ff-176">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="812ff-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="812ff-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="812ff-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="812ff-178">Entry</span></span> | <span data-ttu-id="812ff-179">Wert</span><span class="sxs-lookup"><span data-stu-id="812ff-179">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="812ff-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="812ff-180">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="812ff-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="812ff-181">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="812ff-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="812ff-182">System-Only</span></span>            | <span data-ttu-id="812ff-183">False</span><span class="sxs-lookup"><span data-stu-id="812ff-183">False</span></span>                                                         |
| <span data-ttu-id="812ff-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="812ff-184">Is-Single-Valued</span></span>       | <span data-ttu-id="812ff-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="812ff-185">True</span></span>                                                          |
| <span data-ttu-id="812ff-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="812ff-186">Is Indexed</span></span>             | <span data-ttu-id="812ff-187">False</span><span class="sxs-lookup"><span data-stu-id="812ff-187">False</span></span>                                                         |
| <span data-ttu-id="812ff-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="812ff-188">In Global Catalog</span></span>      | <span data-ttu-id="812ff-189">False</span><span class="sxs-lookup"><span data-stu-id="812ff-189">False</span></span>                                                         |
| <span data-ttu-id="812ff-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="812ff-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="812ff-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="812ff-191">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="812ff-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="812ff-192">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="812ff-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="812ff-193">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="812ff-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="812ff-194">Search-Flags</span></span>           | <span data-ttu-id="812ff-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="812ff-195">0x00000000</span></span>                                                    |
| <span data-ttu-id="812ff-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="812ff-196">System-Flags</span></span>           | <span data-ttu-id="812ff-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="812ff-197">0x00000010</span></span>                                                    |
| <span data-ttu-id="812ff-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="812ff-198">Classes used in</span></span>        | [<span data-ttu-id="812ff-199">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="812ff-199">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="812ff-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="812ff-200">Windows Server 2008</span></span>



| <span data-ttu-id="812ff-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="812ff-201">Entry</span></span> | <span data-ttu-id="812ff-202">Wert</span><span class="sxs-lookup"><span data-stu-id="812ff-202">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="812ff-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="812ff-203">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="812ff-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="812ff-204">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="812ff-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="812ff-205">System-Only</span></span>            | <span data-ttu-id="812ff-206">False</span><span class="sxs-lookup"><span data-stu-id="812ff-206">False</span></span>                                                         |
| <span data-ttu-id="812ff-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="812ff-207">Is-Single-Valued</span></span>       | <span data-ttu-id="812ff-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="812ff-208">True</span></span>                                                          |
| <span data-ttu-id="812ff-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="812ff-209">Is Indexed</span></span>             | <span data-ttu-id="812ff-210">False</span><span class="sxs-lookup"><span data-stu-id="812ff-210">False</span></span>                                                         |
| <span data-ttu-id="812ff-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="812ff-211">In Global Catalog</span></span>      | <span data-ttu-id="812ff-212">False</span><span class="sxs-lookup"><span data-stu-id="812ff-212">False</span></span>                                                         |
| <span data-ttu-id="812ff-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="812ff-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="812ff-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="812ff-214">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="812ff-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="812ff-215">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="812ff-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="812ff-216">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="812ff-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="812ff-217">Search-Flags</span></span>           | <span data-ttu-id="812ff-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="812ff-218">0x00000000</span></span>                                                    |
| <span data-ttu-id="812ff-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="812ff-219">System-Flags</span></span>           | <span data-ttu-id="812ff-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="812ff-220">0x00000010</span></span>                                                    |
| <span data-ttu-id="812ff-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="812ff-221">Classes used in</span></span>        | [<span data-ttu-id="812ff-222">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="812ff-222">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="812ff-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="812ff-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="812ff-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="812ff-224">Entry</span></span> | <span data-ttu-id="812ff-225">Wert</span><span class="sxs-lookup"><span data-stu-id="812ff-225">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="812ff-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="812ff-226">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="812ff-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="812ff-227">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="812ff-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="812ff-228">System-Only</span></span>            | <span data-ttu-id="812ff-229">False</span><span class="sxs-lookup"><span data-stu-id="812ff-229">False</span></span>                                                         |
| <span data-ttu-id="812ff-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="812ff-230">Is-Single-Valued</span></span>       | <span data-ttu-id="812ff-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="812ff-231">True</span></span>                                                          |
| <span data-ttu-id="812ff-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="812ff-232">Is Indexed</span></span>             | <span data-ttu-id="812ff-233">False</span><span class="sxs-lookup"><span data-stu-id="812ff-233">False</span></span>                                                         |
| <span data-ttu-id="812ff-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="812ff-234">In Global Catalog</span></span>      | <span data-ttu-id="812ff-235">False</span><span class="sxs-lookup"><span data-stu-id="812ff-235">False</span></span>                                                         |
| <span data-ttu-id="812ff-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="812ff-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="812ff-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="812ff-237">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="812ff-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="812ff-238">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="812ff-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="812ff-239">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="812ff-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="812ff-240">Search-Flags</span></span>           | <span data-ttu-id="812ff-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="812ff-241">0x00000000</span></span>                                                    |
| <span data-ttu-id="812ff-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="812ff-242">System-Flags</span></span>           | <span data-ttu-id="812ff-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="812ff-243">0x00000010</span></span>                                                    |
| <span data-ttu-id="812ff-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="812ff-244">Classes used in</span></span>        | [<span data-ttu-id="812ff-245">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="812ff-245">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="812ff-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="812ff-246">Windows Server 2012</span></span>



| <span data-ttu-id="812ff-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="812ff-247">Entry</span></span> | <span data-ttu-id="812ff-248">Wert</span><span class="sxs-lookup"><span data-stu-id="812ff-248">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="812ff-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="812ff-249">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="812ff-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="812ff-250">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="812ff-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="812ff-251">System-Only</span></span>            | <span data-ttu-id="812ff-252">False</span><span class="sxs-lookup"><span data-stu-id="812ff-252">False</span></span>                                                         |
| <span data-ttu-id="812ff-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="812ff-253">Is-Single-Valued</span></span>       | <span data-ttu-id="812ff-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="812ff-254">True</span></span>                                                          |
| <span data-ttu-id="812ff-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="812ff-255">Is Indexed</span></span>             | <span data-ttu-id="812ff-256">False</span><span class="sxs-lookup"><span data-stu-id="812ff-256">False</span></span>                                                         |
| <span data-ttu-id="812ff-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="812ff-257">In Global Catalog</span></span>      | <span data-ttu-id="812ff-258">False</span><span class="sxs-lookup"><span data-stu-id="812ff-258">False</span></span>                                                         |
| <span data-ttu-id="812ff-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="812ff-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="812ff-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="812ff-260">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="812ff-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="812ff-261">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="812ff-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="812ff-262">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="812ff-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="812ff-263">Search-Flags</span></span>           | <span data-ttu-id="812ff-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="812ff-264">0x00000000</span></span>                                                    |
| <span data-ttu-id="812ff-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="812ff-265">System-Flags</span></span>           | <span data-ttu-id="812ff-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="812ff-266">0x00000010</span></span>                                                    |
| <span data-ttu-id="812ff-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="812ff-267">Classes used in</span></span>        | [<span data-ttu-id="812ff-268">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="812ff-268">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



 

 





