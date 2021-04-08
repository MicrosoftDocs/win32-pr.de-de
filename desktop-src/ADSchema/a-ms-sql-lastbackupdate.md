---
title: MS-SQL-lastbackupdate-Attribut
description: Das letzte Datum, an dem die Datenbank gesichert wurde.
ms.assetid: 09bd6c2a-85fe-46af-8569-5bc3cbc8411d
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-SQL-lastbackupdate-Attributs
- AD-Schema des MS-SQL-lastbackupdate-Attributs
topic_type:
- apiref
api_name:
- MS-SQL-LastBackupDate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d91cadf953ab51185882c73d4d999a5ccb3fed9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957660"
---
# <a name="ms-sql-lastbackupdate-attribute"></a><span data-ttu-id="7454c-105">MS-SQL-lastbackupdate-Attribut</span><span class="sxs-lookup"><span data-stu-id="7454c-105">MS-SQL-LastBackupDate attribute</span></span>

<span data-ttu-id="7454c-106">Das letzte Datum, an dem die Datenbank gesichert wurde.</span><span class="sxs-lookup"><span data-stu-id="7454c-106">The last date that the database was backed up.</span></span>



| <span data-ttu-id="7454c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7454c-107">Entry</span></span> | <span data-ttu-id="7454c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="7454c-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="7454c-109">CN</span><span class="sxs-lookup"><span data-stu-id="7454c-109">CN</span></span>                | <span data-ttu-id="7454c-110">MS-SQL-lastbackupdate</span><span class="sxs-lookup"><span data-stu-id="7454c-110">MS-SQL-LastBackupDate</span></span>                       |
| <span data-ttu-id="7454c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7454c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7454c-112">MS-SQL-lastbackupdate</span><span class="sxs-lookup"><span data-stu-id="7454c-112">mS-SQL-LastBackupDate</span></span>                       |
| <span data-ttu-id="7454c-113">Size</span><span class="sxs-lookup"><span data-stu-id="7454c-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="7454c-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="7454c-114">Update Privilege</span></span>  | <span data-ttu-id="7454c-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7454c-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="7454c-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="7454c-116">Update Frequency</span></span>  | <span data-ttu-id="7454c-117">Wenn die Datenbank gesichert wird.</span><span class="sxs-lookup"><span data-stu-id="7454c-117">When the database is backed up.</span></span>             |
| <span data-ttu-id="7454c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7454c-118">Attribute-Id</span></span>      | <span data-ttu-id="7454c-119">1.2.840.113556.1.4.1398</span><span class="sxs-lookup"><span data-stu-id="7454c-119">1.2.840.113556.1.4.1398</span></span>                     |
| <span data-ttu-id="7454c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7454c-120">System-Id-Guid</span></span>    | <span data-ttu-id="7454c-121">f2b6abca-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="7454c-121">f2b6abca-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="7454c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="7454c-122">Syntax</span></span>            | [<span data-ttu-id="7454c-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7454c-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="7454c-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="7454c-124">Implementations</span></span>

-   [<span data-ttu-id="7454c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7454c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7454c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7454c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7454c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7454c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7454c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7454c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7454c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7454c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7454c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7454c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7454c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7454c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7454c-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7454c-132">Entry</span></span> | <span data-ttu-id="7454c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="7454c-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7454c-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7454c-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7454c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7454c-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7454c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7454c-136">System-Only</span></span>            | <span data-ttu-id="7454c-137">False</span><span class="sxs-lookup"><span data-stu-id="7454c-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7454c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7454c-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="7454c-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="7454c-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7454c-140">Is Indexed</span></span>             | <span data-ttu-id="7454c-141">False</span><span class="sxs-lookup"><span data-stu-id="7454c-141">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7454c-142">In Global Catalog</span></span>      | <span data-ttu-id="7454c-143">False</span><span class="sxs-lookup"><span data-stu-id="7454c-143">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7454c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7454c-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7454c-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7454c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7454c-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7454c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7454c-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7454c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7454c-148">Search-Flags</span></span>           | <span data-ttu-id="7454c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7454c-149">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="7454c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7454c-150">System-Flags</span></span>           | <span data-ttu-id="7454c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7454c-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7454c-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7454c-152">Classes used in</span></span>        | [<span data-ttu-id="7454c-153">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="7454c-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="7454c-154">**MS-SQL-olapdatabase**</span><span class="sxs-lookup"><span data-stu-id="7454c-154">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7454c-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7454c-155">Windows Server 2003</span></span>



| <span data-ttu-id="7454c-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7454c-156">Entry</span></span> | <span data-ttu-id="7454c-157">Wert</span><span class="sxs-lookup"><span data-stu-id="7454c-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7454c-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7454c-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7454c-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7454c-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7454c-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="7454c-160">System-Only</span></span>            | <span data-ttu-id="7454c-161">False</span><span class="sxs-lookup"><span data-stu-id="7454c-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7454c-162">Is-Single-Valued</span></span>       | <span data-ttu-id="7454c-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="7454c-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="7454c-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7454c-164">Is Indexed</span></span>             | <span data-ttu-id="7454c-165">False</span><span class="sxs-lookup"><span data-stu-id="7454c-165">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7454c-166">In Global Catalog</span></span>      | <span data-ttu-id="7454c-167">False</span><span class="sxs-lookup"><span data-stu-id="7454c-167">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7454c-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="7454c-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7454c-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7454c-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7454c-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7454c-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7454c-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7454c-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7454c-172">Search-Flags</span></span>           | <span data-ttu-id="7454c-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7454c-173">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="7454c-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7454c-174">System-Flags</span></span>           | <span data-ttu-id="7454c-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7454c-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7454c-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7454c-176">Classes used in</span></span>        | [<span data-ttu-id="7454c-177">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="7454c-177">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="7454c-178">**MS-SQL-olapdatabase**</span><span class="sxs-lookup"><span data-stu-id="7454c-178">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7454c-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7454c-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7454c-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7454c-180">Entry</span></span> | <span data-ttu-id="7454c-181">Wert</span><span class="sxs-lookup"><span data-stu-id="7454c-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7454c-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7454c-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7454c-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7454c-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7454c-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="7454c-184">System-Only</span></span>            | <span data-ttu-id="7454c-185">False</span><span class="sxs-lookup"><span data-stu-id="7454c-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7454c-186">Is-Single-Valued</span></span>       | <span data-ttu-id="7454c-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="7454c-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="7454c-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7454c-188">Is Indexed</span></span>             | <span data-ttu-id="7454c-189">False</span><span class="sxs-lookup"><span data-stu-id="7454c-189">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7454c-190">In Global Catalog</span></span>      | <span data-ttu-id="7454c-191">False</span><span class="sxs-lookup"><span data-stu-id="7454c-191">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7454c-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="7454c-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7454c-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7454c-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7454c-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7454c-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7454c-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7454c-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7454c-196">Search-Flags</span></span>           | <span data-ttu-id="7454c-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7454c-197">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="7454c-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7454c-198">System-Flags</span></span>           | <span data-ttu-id="7454c-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7454c-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7454c-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7454c-200">Classes used in</span></span>        | [<span data-ttu-id="7454c-201">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="7454c-201">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="7454c-202">**MS-SQL-olapdatabase**</span><span class="sxs-lookup"><span data-stu-id="7454c-202">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7454c-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7454c-203">Windows Server 2008</span></span>



| <span data-ttu-id="7454c-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7454c-204">Entry</span></span> | <span data-ttu-id="7454c-205">Wert</span><span class="sxs-lookup"><span data-stu-id="7454c-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7454c-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7454c-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7454c-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7454c-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7454c-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="7454c-208">System-Only</span></span>            | <span data-ttu-id="7454c-209">False</span><span class="sxs-lookup"><span data-stu-id="7454c-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7454c-210">Is-Single-Valued</span></span>       | <span data-ttu-id="7454c-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="7454c-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="7454c-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7454c-212">Is Indexed</span></span>             | <span data-ttu-id="7454c-213">False</span><span class="sxs-lookup"><span data-stu-id="7454c-213">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7454c-214">In Global Catalog</span></span>      | <span data-ttu-id="7454c-215">False</span><span class="sxs-lookup"><span data-stu-id="7454c-215">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7454c-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="7454c-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7454c-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7454c-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7454c-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7454c-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7454c-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7454c-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7454c-220">Search-Flags</span></span>           | <span data-ttu-id="7454c-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7454c-221">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="7454c-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7454c-222">System-Flags</span></span>           | <span data-ttu-id="7454c-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7454c-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7454c-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7454c-224">Classes used in</span></span>        | [<span data-ttu-id="7454c-225">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="7454c-225">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="7454c-226">**MS-SQL-olapdatabase**</span><span class="sxs-lookup"><span data-stu-id="7454c-226">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7454c-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7454c-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7454c-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7454c-228">Entry</span></span> | <span data-ttu-id="7454c-229">Wert</span><span class="sxs-lookup"><span data-stu-id="7454c-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7454c-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7454c-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7454c-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7454c-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7454c-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="7454c-232">System-Only</span></span>            | <span data-ttu-id="7454c-233">False</span><span class="sxs-lookup"><span data-stu-id="7454c-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7454c-234">Is-Single-Valued</span></span>       | <span data-ttu-id="7454c-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="7454c-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="7454c-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7454c-236">Is Indexed</span></span>             | <span data-ttu-id="7454c-237">False</span><span class="sxs-lookup"><span data-stu-id="7454c-237">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7454c-238">In Global Catalog</span></span>      | <span data-ttu-id="7454c-239">False</span><span class="sxs-lookup"><span data-stu-id="7454c-239">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7454c-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="7454c-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7454c-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7454c-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7454c-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7454c-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7454c-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7454c-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7454c-244">Search-Flags</span></span>           | <span data-ttu-id="7454c-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7454c-245">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="7454c-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7454c-246">System-Flags</span></span>           | <span data-ttu-id="7454c-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7454c-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7454c-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7454c-248">Classes used in</span></span>        | [<span data-ttu-id="7454c-249">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="7454c-249">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="7454c-250">**MS-SQL-olapdatabase**</span><span class="sxs-lookup"><span data-stu-id="7454c-250">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7454c-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7454c-251">Windows Server 2012</span></span>



| <span data-ttu-id="7454c-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7454c-252">Entry</span></span> | <span data-ttu-id="7454c-253">Wert</span><span class="sxs-lookup"><span data-stu-id="7454c-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7454c-254">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7454c-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7454c-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7454c-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7454c-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="7454c-256">System-Only</span></span>            | <span data-ttu-id="7454c-257">False</span><span class="sxs-lookup"><span data-stu-id="7454c-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-258">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7454c-258">Is-Single-Valued</span></span>       | <span data-ttu-id="7454c-259">Richtig</span><span class="sxs-lookup"><span data-stu-id="7454c-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="7454c-260">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7454c-260">Is Indexed</span></span>             | <span data-ttu-id="7454c-261">False</span><span class="sxs-lookup"><span data-stu-id="7454c-261">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-262">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7454c-262">In Global Catalog</span></span>      | <span data-ttu-id="7454c-263">False</span><span class="sxs-lookup"><span data-stu-id="7454c-263">False</span></span>                                                                                                                         |
| <span data-ttu-id="7454c-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7454c-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="7454c-265">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7454c-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7454c-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7454c-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7454c-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7454c-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7454c-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7454c-268">Search-Flags</span></span>           | <span data-ttu-id="7454c-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7454c-269">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="7454c-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7454c-270">System-Flags</span></span>           | <span data-ttu-id="7454c-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7454c-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7454c-272">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7454c-272">Classes used in</span></span>        | [<span data-ttu-id="7454c-273">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="7454c-273">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="7454c-274">**MS-SQL-olapdatabase**</span><span class="sxs-lookup"><span data-stu-id="7454c-274">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



 

 





