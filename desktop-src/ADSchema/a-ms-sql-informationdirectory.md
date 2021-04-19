---
title: MS-SQL-informationdirectory-Attribut
description: Das Informations Verzeichnis für die aktuelle Instanz von SQL Server.
ms.assetid: fec29b94-b136-4862-8615-7190b3b45ec3
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-SQL-informationdirectory-Attributs
- AD-Schema des MS-SQL-informationdirectory-Attributs
topic_type:
- apiref
api_name:
- MS-SQL-InformationDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a5ca19d6c746e6e5874e82010fcbca367c1157
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346582"
---
# <a name="ms-sql-informationdirectory-attribute"></a><span data-ttu-id="04db5-105">MS-SQL-informationdirectory-Attribut</span><span class="sxs-lookup"><span data-stu-id="04db5-105">MS-SQL-InformationDirectory attribute</span></span>

<span data-ttu-id="04db5-106">Das Informations Verzeichnis für die aktuelle Instanz von SQL Server.</span><span class="sxs-lookup"><span data-stu-id="04db5-106">The informational directory for the current instance of SQL Server.</span></span>



| <span data-ttu-id="04db5-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04db5-107">Entry</span></span> | <span data-ttu-id="04db5-108">Wert</span><span class="sxs-lookup"><span data-stu-id="04db5-108">Value</span></span> |
|-------------------|------------------------------------------|
| <span data-ttu-id="04db5-109">CN</span><span class="sxs-lookup"><span data-stu-id="04db5-109">CN</span></span>                | <span data-ttu-id="04db5-110">MS-SQL-informationdirectory</span><span class="sxs-lookup"><span data-stu-id="04db5-110">MS-SQL-InformationDirectory</span></span>              |
| <span data-ttu-id="04db5-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="04db5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="04db5-112">MS-SQL-informationdirectory</span><span class="sxs-lookup"><span data-stu-id="04db5-112">mS-SQL-InformationDirectory</span></span>              |
| <span data-ttu-id="04db5-113">Size</span><span class="sxs-lookup"><span data-stu-id="04db5-113">Size</span></span>              | \-                                       |
| <span data-ttu-id="04db5-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="04db5-114">Update Privilege</span></span>  | <span data-ttu-id="04db5-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="04db5-115">Domain administrator</span></span>                     |
| <span data-ttu-id="04db5-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="04db5-116">Update Frequency</span></span>  | <span data-ttu-id="04db5-117">Beim Systemstart oder beim Aktualisieren von AD.</span><span class="sxs-lookup"><span data-stu-id="04db5-117">At system startup or when AD is updated.</span></span> |
| <span data-ttu-id="04db5-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="04db5-118">Attribute-Id</span></span>      | <span data-ttu-id="04db5-119">1.2.840.113556.1.4.1392</span><span class="sxs-lookup"><span data-stu-id="04db5-119">1.2.840.113556.1.4.1392</span></span>                  |
| <span data-ttu-id="04db5-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="04db5-120">System-Id-Guid</span></span>    | <span data-ttu-id="04db5-121">d0aedb2e-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="04db5-121">d0aedb2e-ccee-11d2-9993-0000f87a57d4</span></span>     |
| <span data-ttu-id="04db5-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="04db5-122">Syntax</span></span>            | [<span data-ttu-id="04db5-123">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="04db5-123">**Boolean**</span></span>](s-boolean.md)             |



## <a name="implementations"></a><span data-ttu-id="04db5-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="04db5-124">Implementations</span></span>

-   [<span data-ttu-id="04db5-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="04db5-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="04db5-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="04db5-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="04db5-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="04db5-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="04db5-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="04db5-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="04db5-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="04db5-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="04db5-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="04db5-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="04db5-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04db5-131">Windows 2000 Server</span></span>



| <span data-ttu-id="04db5-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04db5-132">Entry</span></span> | <span data-ttu-id="04db5-133">Wert</span><span class="sxs-lookup"><span data-stu-id="04db5-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="04db5-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04db5-134">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="04db5-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04db5-135">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="04db5-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="04db5-136">System-Only</span></span>            | <span data-ttu-id="04db5-137">False</span><span class="sxs-lookup"><span data-stu-id="04db5-137">False</span></span>                                                             |
| <span data-ttu-id="04db5-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04db5-138">Is-Single-Valued</span></span>       | <span data-ttu-id="04db5-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="04db5-139">True</span></span>                                                              |
| <span data-ttu-id="04db5-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04db5-140">Is Indexed</span></span>             | <span data-ttu-id="04db5-141">False</span><span class="sxs-lookup"><span data-stu-id="04db5-141">False</span></span>                                                             |
| <span data-ttu-id="04db5-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04db5-142">In Global Catalog</span></span>      | <span data-ttu-id="04db5-143">False</span><span class="sxs-lookup"><span data-stu-id="04db5-143">False</span></span>                                                             |
| <span data-ttu-id="04db5-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04db5-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="04db5-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04db5-145">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="04db5-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04db5-146">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="04db5-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04db5-147">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="04db5-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04db5-148">Search-Flags</span></span>           | <span data-ttu-id="04db5-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04db5-149">0x00000000</span></span>                                                        |
| <span data-ttu-id="04db5-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04db5-150">System-Flags</span></span>           | <span data-ttu-id="04db5-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04db5-151">0x00000010</span></span>                                                        |
| <span data-ttu-id="04db5-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04db5-152">Classes used in</span></span>        | [<span data-ttu-id="04db5-153">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="04db5-153">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="04db5-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="04db5-154">Windows Server 2003</span></span>



| <span data-ttu-id="04db5-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04db5-155">Entry</span></span> | <span data-ttu-id="04db5-156">Wert</span><span class="sxs-lookup"><span data-stu-id="04db5-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="04db5-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04db5-157">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="04db5-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04db5-158">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="04db5-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="04db5-159">System-Only</span></span>            | <span data-ttu-id="04db5-160">False</span><span class="sxs-lookup"><span data-stu-id="04db5-160">False</span></span>                                                             |
| <span data-ttu-id="04db5-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04db5-161">Is-Single-Valued</span></span>       | <span data-ttu-id="04db5-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="04db5-162">True</span></span>                                                              |
| <span data-ttu-id="04db5-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04db5-163">Is Indexed</span></span>             | <span data-ttu-id="04db5-164">False</span><span class="sxs-lookup"><span data-stu-id="04db5-164">False</span></span>                                                             |
| <span data-ttu-id="04db5-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04db5-165">In Global Catalog</span></span>      | <span data-ttu-id="04db5-166">False</span><span class="sxs-lookup"><span data-stu-id="04db5-166">False</span></span>                                                             |
| <span data-ttu-id="04db5-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04db5-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="04db5-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04db5-168">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="04db5-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04db5-169">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="04db5-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04db5-170">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="04db5-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04db5-171">Search-Flags</span></span>           | <span data-ttu-id="04db5-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04db5-172">0x00000000</span></span>                                                        |
| <span data-ttu-id="04db5-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04db5-173">System-Flags</span></span>           | <span data-ttu-id="04db5-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04db5-174">0x00000010</span></span>                                                        |
| <span data-ttu-id="04db5-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04db5-175">Classes used in</span></span>        | [<span data-ttu-id="04db5-176">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="04db5-176">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="04db5-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="04db5-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="04db5-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04db5-178">Entry</span></span> | <span data-ttu-id="04db5-179">Wert</span><span class="sxs-lookup"><span data-stu-id="04db5-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="04db5-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04db5-180">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="04db5-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04db5-181">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="04db5-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="04db5-182">System-Only</span></span>            | <span data-ttu-id="04db5-183">False</span><span class="sxs-lookup"><span data-stu-id="04db5-183">False</span></span>                                                             |
| <span data-ttu-id="04db5-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04db5-184">Is-Single-Valued</span></span>       | <span data-ttu-id="04db5-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="04db5-185">True</span></span>                                                              |
| <span data-ttu-id="04db5-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04db5-186">Is Indexed</span></span>             | <span data-ttu-id="04db5-187">False</span><span class="sxs-lookup"><span data-stu-id="04db5-187">False</span></span>                                                             |
| <span data-ttu-id="04db5-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04db5-188">In Global Catalog</span></span>      | <span data-ttu-id="04db5-189">False</span><span class="sxs-lookup"><span data-stu-id="04db5-189">False</span></span>                                                             |
| <span data-ttu-id="04db5-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04db5-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="04db5-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04db5-191">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="04db5-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04db5-192">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="04db5-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04db5-193">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="04db5-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04db5-194">Search-Flags</span></span>           | <span data-ttu-id="04db5-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04db5-195">0x00000000</span></span>                                                        |
| <span data-ttu-id="04db5-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04db5-196">System-Flags</span></span>           | <span data-ttu-id="04db5-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04db5-197">0x00000010</span></span>                                                        |
| <span data-ttu-id="04db5-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04db5-198">Classes used in</span></span>        | [<span data-ttu-id="04db5-199">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="04db5-199">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="04db5-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04db5-200">Windows Server 2008</span></span>



| <span data-ttu-id="04db5-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04db5-201">Entry</span></span> | <span data-ttu-id="04db5-202">Wert</span><span class="sxs-lookup"><span data-stu-id="04db5-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="04db5-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04db5-203">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="04db5-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04db5-204">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="04db5-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="04db5-205">System-Only</span></span>            | <span data-ttu-id="04db5-206">False</span><span class="sxs-lookup"><span data-stu-id="04db5-206">False</span></span>                                                             |
| <span data-ttu-id="04db5-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04db5-207">Is-Single-Valued</span></span>       | <span data-ttu-id="04db5-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="04db5-208">True</span></span>                                                              |
| <span data-ttu-id="04db5-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04db5-209">Is Indexed</span></span>             | <span data-ttu-id="04db5-210">False</span><span class="sxs-lookup"><span data-stu-id="04db5-210">False</span></span>                                                             |
| <span data-ttu-id="04db5-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04db5-211">In Global Catalog</span></span>      | <span data-ttu-id="04db5-212">False</span><span class="sxs-lookup"><span data-stu-id="04db5-212">False</span></span>                                                             |
| <span data-ttu-id="04db5-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04db5-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="04db5-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04db5-214">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="04db5-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04db5-215">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="04db5-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04db5-216">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="04db5-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04db5-217">Search-Flags</span></span>           | <span data-ttu-id="04db5-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04db5-218">0x00000000</span></span>                                                        |
| <span data-ttu-id="04db5-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04db5-219">System-Flags</span></span>           | <span data-ttu-id="04db5-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04db5-220">0x00000010</span></span>                                                        |
| <span data-ttu-id="04db5-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04db5-221">Classes used in</span></span>        | [<span data-ttu-id="04db5-222">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="04db5-222">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="04db5-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="04db5-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="04db5-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04db5-224">Entry</span></span> | <span data-ttu-id="04db5-225">Wert</span><span class="sxs-lookup"><span data-stu-id="04db5-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="04db5-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04db5-226">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="04db5-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04db5-227">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="04db5-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="04db5-228">System-Only</span></span>            | <span data-ttu-id="04db5-229">False</span><span class="sxs-lookup"><span data-stu-id="04db5-229">False</span></span>                                                             |
| <span data-ttu-id="04db5-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04db5-230">Is-Single-Valued</span></span>       | <span data-ttu-id="04db5-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="04db5-231">True</span></span>                                                              |
| <span data-ttu-id="04db5-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04db5-232">Is Indexed</span></span>             | <span data-ttu-id="04db5-233">False</span><span class="sxs-lookup"><span data-stu-id="04db5-233">False</span></span>                                                             |
| <span data-ttu-id="04db5-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04db5-234">In Global Catalog</span></span>      | <span data-ttu-id="04db5-235">False</span><span class="sxs-lookup"><span data-stu-id="04db5-235">False</span></span>                                                             |
| <span data-ttu-id="04db5-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04db5-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="04db5-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04db5-237">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="04db5-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04db5-238">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="04db5-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04db5-239">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="04db5-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04db5-240">Search-Flags</span></span>           | <span data-ttu-id="04db5-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04db5-241">0x00000000</span></span>                                                        |
| <span data-ttu-id="04db5-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04db5-242">System-Flags</span></span>           | <span data-ttu-id="04db5-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04db5-243">0x00000010</span></span>                                                        |
| <span data-ttu-id="04db5-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04db5-244">Classes used in</span></span>        | [<span data-ttu-id="04db5-245">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="04db5-245">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="04db5-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04db5-246">Windows Server 2012</span></span>



| <span data-ttu-id="04db5-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04db5-247">Entry</span></span> | <span data-ttu-id="04db5-248">Wert</span><span class="sxs-lookup"><span data-stu-id="04db5-248">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="04db5-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04db5-249">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="04db5-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04db5-250">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="04db5-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="04db5-251">System-Only</span></span>            | <span data-ttu-id="04db5-252">False</span><span class="sxs-lookup"><span data-stu-id="04db5-252">False</span></span>                                                             |
| <span data-ttu-id="04db5-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04db5-253">Is-Single-Valued</span></span>       | <span data-ttu-id="04db5-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="04db5-254">True</span></span>                                                              |
| <span data-ttu-id="04db5-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04db5-255">Is Indexed</span></span>             | <span data-ttu-id="04db5-256">False</span><span class="sxs-lookup"><span data-stu-id="04db5-256">False</span></span>                                                             |
| <span data-ttu-id="04db5-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04db5-257">In Global Catalog</span></span>      | <span data-ttu-id="04db5-258">False</span><span class="sxs-lookup"><span data-stu-id="04db5-258">False</span></span>                                                             |
| <span data-ttu-id="04db5-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04db5-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="04db5-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04db5-260">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="04db5-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04db5-261">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="04db5-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04db5-262">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="04db5-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04db5-263">Search-Flags</span></span>           | <span data-ttu-id="04db5-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04db5-264">0x00000000</span></span>                                                        |
| <span data-ttu-id="04db5-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04db5-265">System-Flags</span></span>           | <span data-ttu-id="04db5-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04db5-266">0x00000010</span></span>                                                        |
| <span data-ttu-id="04db5-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04db5-267">Classes used in</span></span>        | [<span data-ttu-id="04db5-268">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="04db5-268">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



 

 





