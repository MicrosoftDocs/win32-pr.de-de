---
title: MS-SQL-Type-Attribut
description: Der Replikationstyp, der von diesem SQL Server verwendet wird.
ms.assetid: 8e7fa9ab-9a25-4ee3-9134-68af698a5fb8
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-SQL-Type-Attributs
- AD-Schema des MS-SQL-Type-Attributs
topic_type:
- apiref
api_name:
- MS-SQL-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057b85b0c522a891cc31cde699fd062897c54818
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859880"
---
# <a name="ms-sql-type-attribute"></a><span data-ttu-id="d3305-105">MS-SQL-Type-Attribut</span><span class="sxs-lookup"><span data-stu-id="d3305-105">MS-SQL-Type attribute</span></span>

<span data-ttu-id="d3305-106">Der Replikationstyp, der von diesem SQL Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3305-106">The replication type used by this SQL server.</span></span> <span data-ttu-id="d3305-107">Die folgenden Werte sind die möglichen Werte für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="d3305-107">The following values are the possible values for this attribute.</span></span>



| <span data-ttu-id="d3305-108">Wert</span><span class="sxs-lookup"><span data-stu-id="d3305-108">Value</span></span>        | <span data-ttu-id="d3305-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3305-109">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="d3305-110">0</span><span class="sxs-lookup"><span data-stu-id="d3305-110">0</span></span><br/> | <span data-ttu-id="d3305-111">Transaktionsreplikation.</span><span class="sxs-lookup"><span data-stu-id="d3305-111">Transactional replication.</span></span><br/> |
| <span data-ttu-id="d3305-112">1</span><span class="sxs-lookup"><span data-stu-id="d3305-112">1</span></span><br/> | <span data-ttu-id="d3305-113">Momentaufnahmereplikation.</span><span class="sxs-lookup"><span data-stu-id="d3305-113">Snapshot replication.</span></span><br/>      |
| <span data-ttu-id="d3305-114">2</span><span class="sxs-lookup"><span data-stu-id="d3305-114">2</span></span><br/> | <span data-ttu-id="d3305-115">Mergereplikation.</span><span class="sxs-lookup"><span data-stu-id="d3305-115">Merge replication.</span></span><br/>         |



 



| <span data-ttu-id="d3305-116">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3305-116">Entry</span></span> | <span data-ttu-id="d3305-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d3305-117">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d3305-118">CN</span><span class="sxs-lookup"><span data-stu-id="d3305-118">CN</span></span>                | <span data-ttu-id="d3305-119">MS-SQL-Type</span><span class="sxs-lookup"><span data-stu-id="d3305-119">MS-SQL-Type</span></span>                                 |
| <span data-ttu-id="d3305-120">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d3305-120">Ldap-Display-Name</span></span> | <span data-ttu-id="d3305-121">MS-SQL-Type</span><span class="sxs-lookup"><span data-stu-id="d3305-121">mS-SQL-Type</span></span>                                 |
| <span data-ttu-id="d3305-122">Size</span><span class="sxs-lookup"><span data-stu-id="d3305-122">Size</span></span>              | \-                                          |
| <span data-ttu-id="d3305-123">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d3305-123">Update Privilege</span></span>  | <span data-ttu-id="d3305-124">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="d3305-124">Domain administrator</span></span>                        |
| <span data-ttu-id="d3305-125">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="d3305-125">Update Frequency</span></span>  | <span data-ttu-id="d3305-126">Wenn die Replikation eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="d3305-126">When replication is set up.</span></span>                 |
| <span data-ttu-id="d3305-127">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d3305-127">Attribute-Id</span></span>      | <span data-ttu-id="d3305-128">1.2.840.113556.1.4.1391</span><span class="sxs-lookup"><span data-stu-id="d3305-128">1.2.840.113556.1.4.1391</span></span>                     |
| <span data-ttu-id="d3305-129">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d3305-129">System-Id-Guid</span></span>    | <span data-ttu-id="d3305-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="d3305-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="d3305-131">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3305-131">Syntax</span></span>            | [<span data-ttu-id="d3305-132">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d3305-132">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d3305-133">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="d3305-133">Implementations</span></span>

-   [<span data-ttu-id="d3305-134">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d3305-134">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d3305-135">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d3305-135">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d3305-136">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d3305-136">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d3305-137">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d3305-137">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d3305-138">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d3305-138">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d3305-139">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d3305-139">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d3305-140">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d3305-140">Windows 2000 Server</span></span>



| <span data-ttu-id="d3305-141">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3305-141">Entry</span></span> | <span data-ttu-id="d3305-142">Wert</span><span class="sxs-lookup"><span data-stu-id="d3305-142">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3305-143">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3305-143">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="d3305-144">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3305-144">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="d3305-145">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3305-145">System-Only</span></span>            | <span data-ttu-id="d3305-146">False</span><span class="sxs-lookup"><span data-stu-id="d3305-146">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-147">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3305-147">Is-Single-Valued</span></span>       | <span data-ttu-id="d3305-148">Richtig</span><span class="sxs-lookup"><span data-stu-id="d3305-148">True</span></span>                                                                                                                                |
| <span data-ttu-id="d3305-149">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3305-149">Is Indexed</span></span>             | <span data-ttu-id="d3305-150">False</span><span class="sxs-lookup"><span data-stu-id="d3305-150">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-151">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3305-151">In Global Catalog</span></span>      | <span data-ttu-id="d3305-152">False</span><span class="sxs-lookup"><span data-stu-id="d3305-152">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-153">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3305-153">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3305-154">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3305-154">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="d3305-155">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3305-155">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="d3305-156">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3305-156">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="d3305-157">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3305-157">Search-Flags</span></span>           | <span data-ttu-id="d3305-158">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3305-158">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="d3305-159">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3305-159">System-Flags</span></span>           | <span data-ttu-id="d3305-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3305-160">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="d3305-161">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3305-161">Classes used in</span></span>        | [<span data-ttu-id="d3305-162">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="d3305-162">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="d3305-163">**MS-SQL-olapdatabase**</span><span class="sxs-lookup"><span data-stu-id="d3305-163">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d3305-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d3305-164">Windows Server 2003</span></span>



| <span data-ttu-id="d3305-165">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3305-165">Entry</span></span> | <span data-ttu-id="d3305-166">Wert</span><span class="sxs-lookup"><span data-stu-id="d3305-166">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3305-167">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3305-167">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="d3305-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3305-168">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="d3305-169">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3305-169">System-Only</span></span>            | <span data-ttu-id="d3305-170">False</span><span class="sxs-lookup"><span data-stu-id="d3305-170">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-171">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3305-171">Is-Single-Valued</span></span>       | <span data-ttu-id="d3305-172">Richtig</span><span class="sxs-lookup"><span data-stu-id="d3305-172">True</span></span>                                                                                                                                |
| <span data-ttu-id="d3305-173">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3305-173">Is Indexed</span></span>             | <span data-ttu-id="d3305-174">False</span><span class="sxs-lookup"><span data-stu-id="d3305-174">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-175">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3305-175">In Global Catalog</span></span>      | <span data-ttu-id="d3305-176">False</span><span class="sxs-lookup"><span data-stu-id="d3305-176">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-177">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3305-177">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3305-178">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3305-178">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="d3305-179">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3305-179">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="d3305-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3305-180">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="d3305-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3305-181">Search-Flags</span></span>           | <span data-ttu-id="d3305-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3305-182">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="d3305-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3305-183">System-Flags</span></span>           | <span data-ttu-id="d3305-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3305-184">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="d3305-185">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3305-185">Classes used in</span></span>        | [<span data-ttu-id="d3305-186">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="d3305-186">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="d3305-187">**MS-SQL-olapdatabase**</span><span class="sxs-lookup"><span data-stu-id="d3305-187">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d3305-188">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d3305-188">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d3305-189">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3305-189">Entry</span></span> | <span data-ttu-id="d3305-190">Wert</span><span class="sxs-lookup"><span data-stu-id="d3305-190">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3305-191">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3305-191">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="d3305-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3305-192">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="d3305-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3305-193">System-Only</span></span>            | <span data-ttu-id="d3305-194">False</span><span class="sxs-lookup"><span data-stu-id="d3305-194">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-195">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3305-195">Is-Single-Valued</span></span>       | <span data-ttu-id="d3305-196">Richtig</span><span class="sxs-lookup"><span data-stu-id="d3305-196">True</span></span>                                                                                                                                |
| <span data-ttu-id="d3305-197">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3305-197">Is Indexed</span></span>             | <span data-ttu-id="d3305-198">False</span><span class="sxs-lookup"><span data-stu-id="d3305-198">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-199">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3305-199">In Global Catalog</span></span>      | <span data-ttu-id="d3305-200">False</span><span class="sxs-lookup"><span data-stu-id="d3305-200">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-201">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3305-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3305-202">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3305-202">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="d3305-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3305-203">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="d3305-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3305-204">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="d3305-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3305-205">Search-Flags</span></span>           | <span data-ttu-id="d3305-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3305-206">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="d3305-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3305-207">System-Flags</span></span>           | <span data-ttu-id="d3305-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3305-208">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="d3305-209">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3305-209">Classes used in</span></span>        | [<span data-ttu-id="d3305-210">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="d3305-210">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="d3305-211">**MS-SQL-olapdatabase**</span><span class="sxs-lookup"><span data-stu-id="d3305-211">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d3305-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3305-212">Windows Server 2008</span></span>



| <span data-ttu-id="d3305-213">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3305-213">Entry</span></span> | <span data-ttu-id="d3305-214">Wert</span><span class="sxs-lookup"><span data-stu-id="d3305-214">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3305-215">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3305-215">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="d3305-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3305-216">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="d3305-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3305-217">System-Only</span></span>            | <span data-ttu-id="d3305-218">False</span><span class="sxs-lookup"><span data-stu-id="d3305-218">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-219">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3305-219">Is-Single-Valued</span></span>       | <span data-ttu-id="d3305-220">Richtig</span><span class="sxs-lookup"><span data-stu-id="d3305-220">True</span></span>                                                                                                                                |
| <span data-ttu-id="d3305-221">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3305-221">Is Indexed</span></span>             | <span data-ttu-id="d3305-222">False</span><span class="sxs-lookup"><span data-stu-id="d3305-222">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-223">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3305-223">In Global Catalog</span></span>      | <span data-ttu-id="d3305-224">False</span><span class="sxs-lookup"><span data-stu-id="d3305-224">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-225">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3305-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3305-226">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3305-226">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="d3305-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3305-227">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="d3305-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3305-228">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="d3305-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3305-229">Search-Flags</span></span>           | <span data-ttu-id="d3305-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3305-230">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="d3305-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3305-231">System-Flags</span></span>           | <span data-ttu-id="d3305-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3305-232">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="d3305-233">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3305-233">Classes used in</span></span>        | [<span data-ttu-id="d3305-234">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="d3305-234">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="d3305-235">**MS-SQL-olapdatabase**</span><span class="sxs-lookup"><span data-stu-id="d3305-235">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d3305-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d3305-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d3305-237">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3305-237">Entry</span></span> | <span data-ttu-id="d3305-238">Wert</span><span class="sxs-lookup"><span data-stu-id="d3305-238">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3305-239">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3305-239">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="d3305-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3305-240">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="d3305-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3305-241">System-Only</span></span>            | <span data-ttu-id="d3305-242">False</span><span class="sxs-lookup"><span data-stu-id="d3305-242">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-243">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3305-243">Is-Single-Valued</span></span>       | <span data-ttu-id="d3305-244">Richtig</span><span class="sxs-lookup"><span data-stu-id="d3305-244">True</span></span>                                                                                                                                |
| <span data-ttu-id="d3305-245">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3305-245">Is Indexed</span></span>             | <span data-ttu-id="d3305-246">False</span><span class="sxs-lookup"><span data-stu-id="d3305-246">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-247">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3305-247">In Global Catalog</span></span>      | <span data-ttu-id="d3305-248">False</span><span class="sxs-lookup"><span data-stu-id="d3305-248">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-249">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3305-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3305-250">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3305-250">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="d3305-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3305-251">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="d3305-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3305-252">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="d3305-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3305-253">Search-Flags</span></span>           | <span data-ttu-id="d3305-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3305-254">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="d3305-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3305-255">System-Flags</span></span>           | <span data-ttu-id="d3305-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3305-256">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="d3305-257">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3305-257">Classes used in</span></span>        | [<span data-ttu-id="d3305-258">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="d3305-258">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="d3305-259">**MS-SQL-olapdatabase**</span><span class="sxs-lookup"><span data-stu-id="d3305-259">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d3305-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d3305-260">Windows Server 2012</span></span>



| <span data-ttu-id="d3305-261">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3305-261">Entry</span></span> | <span data-ttu-id="d3305-262">Wert</span><span class="sxs-lookup"><span data-stu-id="d3305-262">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3305-263">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3305-263">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="d3305-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3305-264">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="d3305-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3305-265">System-Only</span></span>            | <span data-ttu-id="d3305-266">False</span><span class="sxs-lookup"><span data-stu-id="d3305-266">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-267">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3305-267">Is-Single-Valued</span></span>       | <span data-ttu-id="d3305-268">Richtig</span><span class="sxs-lookup"><span data-stu-id="d3305-268">True</span></span>                                                                                                                                |
| <span data-ttu-id="d3305-269">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3305-269">Is Indexed</span></span>             | <span data-ttu-id="d3305-270">False</span><span class="sxs-lookup"><span data-stu-id="d3305-270">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-271">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3305-271">In Global Catalog</span></span>      | <span data-ttu-id="d3305-272">False</span><span class="sxs-lookup"><span data-stu-id="d3305-272">False</span></span>                                                                                                                               |
| <span data-ttu-id="d3305-273">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3305-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3305-274">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3305-274">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="d3305-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3305-275">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="d3305-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3305-276">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="d3305-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3305-277">Search-Flags</span></span>           | <span data-ttu-id="d3305-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3305-278">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="d3305-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3305-279">System-Flags</span></span>           | <span data-ttu-id="d3305-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3305-280">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="d3305-281">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3305-281">Classes used in</span></span>        | [<span data-ttu-id="d3305-282">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="d3305-282">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="d3305-283">**MS-SQL-olapdatabase**</span><span class="sxs-lookup"><span data-stu-id="d3305-283">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



 

 





