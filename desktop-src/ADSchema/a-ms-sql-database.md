---
title: MS-SQL-Database-Attribut
description: Der Name der SQL Server Datenbank, die an der Replikation beteiligt ist.
ms.assetid: 624705d9-df3f-458e-98f4-fb8da073efd6
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-SQL-Database-Attribut
- AD-Schema für MS-SQL-Database-Attribut
topic_type:
- apiref
api_name:
- MS-SQL-Database
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae6c448213bee18fede3cc8a77cabf607c3b2ee3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859459"
---
# <a name="ms-sql-database-attribute"></a><span data-ttu-id="8ade7-105">MS-SQL-Database-Attribut</span><span class="sxs-lookup"><span data-stu-id="8ade7-105">MS-SQL-Database attribute</span></span>

<span data-ttu-id="8ade7-106">Der Name der SQL Server Datenbank, die an der Replikation beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="8ade7-106">The name of the SQL Server database involved in replication.</span></span>



| <span data-ttu-id="8ade7-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8ade7-107">Entry</span></span> | <span data-ttu-id="8ade7-108">Wert</span><span class="sxs-lookup"><span data-stu-id="8ade7-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="8ade7-109">CN</span><span class="sxs-lookup"><span data-stu-id="8ade7-109">CN</span></span>                | <span data-ttu-id="8ade7-110">MS-SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="8ade7-110">MS-SQL-Database</span></span>                             |
| <span data-ttu-id="8ade7-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8ade7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8ade7-112">MS-SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="8ade7-112">mS-SQL-Database</span></span>                             |
| <span data-ttu-id="8ade7-113">Size</span><span class="sxs-lookup"><span data-stu-id="8ade7-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="8ade7-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="8ade7-114">Update Privilege</span></span>  | <span data-ttu-id="8ade7-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="8ade7-115">Domain administrator</span></span>                        |
| <span data-ttu-id="8ade7-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="8ade7-116">Update Frequency</span></span>  | <span data-ttu-id="8ade7-117">Wenn die Replikation eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="8ade7-117">When replication is setup.</span></span>                  |
| <span data-ttu-id="8ade7-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8ade7-118">Attribute-Id</span></span>      | <span data-ttu-id="8ade7-119">1.2.840.113556.1.4.1393</span><span class="sxs-lookup"><span data-stu-id="8ade7-119">1.2.840.113556.1.4.1393</span></span>                     |
| <span data-ttu-id="8ade7-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8ade7-120">System-Id-Guid</span></span>    | <span data-ttu-id="8ade7-121">d5a0dbdc-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="8ade7-121">d5a0dbdc-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="8ade7-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ade7-122">Syntax</span></span>            | [<span data-ttu-id="8ade7-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="8ade7-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="8ade7-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="8ade7-124">Implementations</span></span>

-   [<span data-ttu-id="8ade7-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8ade7-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8ade7-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8ade7-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8ade7-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8ade7-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8ade7-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8ade7-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8ade7-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8ade7-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8ade7-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8ade7-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8ade7-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8ade7-131">Windows 2000 Server</span></span>



| <span data-ttu-id="8ade7-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8ade7-132">Entry</span></span> | <span data-ttu-id="8ade7-133">Wert</span><span class="sxs-lookup"><span data-stu-id="8ade7-133">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8ade7-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8ade7-134">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8ade7-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ade7-135">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8ade7-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ade7-136">System-Only</span></span>            | <span data-ttu-id="8ade7-137">False</span><span class="sxs-lookup"><span data-stu-id="8ade7-137">False</span></span>                                                               |
| <span data-ttu-id="8ade7-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8ade7-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8ade7-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-139">True</span></span>                                                                |
| <span data-ttu-id="8ade7-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8ade7-140">Is Indexed</span></span>             | <span data-ttu-id="8ade7-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-141">True</span></span>                                                                |
| <span data-ttu-id="8ade7-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8ade7-142">In Global Catalog</span></span>      | <span data-ttu-id="8ade7-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-143">True</span></span>                                                                |
| <span data-ttu-id="8ade7-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8ade7-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ade7-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8ade7-145">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8ade7-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ade7-146">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8ade7-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ade7-147">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8ade7-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ade7-148">Search-Flags</span></span>           | <span data-ttu-id="8ade7-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8ade7-149">0x00000001</span></span>                                                          |
| <span data-ttu-id="8ade7-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ade7-150">System-Flags</span></span>           | <span data-ttu-id="8ade7-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ade7-151">0x00000010</span></span>                                                          |
| <span data-ttu-id="8ade7-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8ade7-152">Classes used in</span></span>        | [<span data-ttu-id="8ade7-153">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="8ade7-153">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8ade7-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8ade7-154">Windows Server 2003</span></span>



| <span data-ttu-id="8ade7-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8ade7-155">Entry</span></span> | <span data-ttu-id="8ade7-156">Wert</span><span class="sxs-lookup"><span data-stu-id="8ade7-156">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8ade7-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8ade7-157">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8ade7-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ade7-158">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8ade7-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ade7-159">System-Only</span></span>            | <span data-ttu-id="8ade7-160">False</span><span class="sxs-lookup"><span data-stu-id="8ade7-160">False</span></span>                                                               |
| <span data-ttu-id="8ade7-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8ade7-161">Is-Single-Valued</span></span>       | <span data-ttu-id="8ade7-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-162">True</span></span>                                                                |
| <span data-ttu-id="8ade7-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8ade7-163">Is Indexed</span></span>             | <span data-ttu-id="8ade7-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-164">True</span></span>                                                                |
| <span data-ttu-id="8ade7-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8ade7-165">In Global Catalog</span></span>      | <span data-ttu-id="8ade7-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-166">True</span></span>                                                                |
| <span data-ttu-id="8ade7-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8ade7-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ade7-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8ade7-168">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8ade7-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ade7-169">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8ade7-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ade7-170">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8ade7-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ade7-171">Search-Flags</span></span>           | <span data-ttu-id="8ade7-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8ade7-172">0x00000001</span></span>                                                          |
| <span data-ttu-id="8ade7-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ade7-173">System-Flags</span></span>           | <span data-ttu-id="8ade7-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ade7-174">0x00000010</span></span>                                                          |
| <span data-ttu-id="8ade7-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8ade7-175">Classes used in</span></span>        | [<span data-ttu-id="8ade7-176">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="8ade7-176">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8ade7-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8ade7-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8ade7-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8ade7-178">Entry</span></span> | <span data-ttu-id="8ade7-179">Wert</span><span class="sxs-lookup"><span data-stu-id="8ade7-179">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8ade7-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8ade7-180">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8ade7-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ade7-181">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8ade7-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ade7-182">System-Only</span></span>            | <span data-ttu-id="8ade7-183">False</span><span class="sxs-lookup"><span data-stu-id="8ade7-183">False</span></span>                                                               |
| <span data-ttu-id="8ade7-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8ade7-184">Is-Single-Valued</span></span>       | <span data-ttu-id="8ade7-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-185">True</span></span>                                                                |
| <span data-ttu-id="8ade7-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8ade7-186">Is Indexed</span></span>             | <span data-ttu-id="8ade7-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-187">True</span></span>                                                                |
| <span data-ttu-id="8ade7-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8ade7-188">In Global Catalog</span></span>      | <span data-ttu-id="8ade7-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-189">True</span></span>                                                                |
| <span data-ttu-id="8ade7-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8ade7-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ade7-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8ade7-191">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8ade7-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ade7-192">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8ade7-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ade7-193">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8ade7-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ade7-194">Search-Flags</span></span>           | <span data-ttu-id="8ade7-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8ade7-195">0x00000001</span></span>                                                          |
| <span data-ttu-id="8ade7-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ade7-196">System-Flags</span></span>           | <span data-ttu-id="8ade7-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ade7-197">0x00000010</span></span>                                                          |
| <span data-ttu-id="8ade7-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8ade7-198">Classes used in</span></span>        | [<span data-ttu-id="8ade7-199">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="8ade7-199">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8ade7-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ade7-200">Windows Server 2008</span></span>



| <span data-ttu-id="8ade7-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8ade7-201">Entry</span></span> | <span data-ttu-id="8ade7-202">Wert</span><span class="sxs-lookup"><span data-stu-id="8ade7-202">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8ade7-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8ade7-203">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8ade7-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ade7-204">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8ade7-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ade7-205">System-Only</span></span>            | <span data-ttu-id="8ade7-206">False</span><span class="sxs-lookup"><span data-stu-id="8ade7-206">False</span></span>                                                               |
| <span data-ttu-id="8ade7-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8ade7-207">Is-Single-Valued</span></span>       | <span data-ttu-id="8ade7-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-208">True</span></span>                                                                |
| <span data-ttu-id="8ade7-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8ade7-209">Is Indexed</span></span>             | <span data-ttu-id="8ade7-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-210">True</span></span>                                                                |
| <span data-ttu-id="8ade7-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8ade7-211">In Global Catalog</span></span>      | <span data-ttu-id="8ade7-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-212">True</span></span>                                                                |
| <span data-ttu-id="8ade7-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8ade7-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ade7-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8ade7-214">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8ade7-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ade7-215">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8ade7-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ade7-216">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8ade7-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ade7-217">Search-Flags</span></span>           | <span data-ttu-id="8ade7-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8ade7-218">0x00000001</span></span>                                                          |
| <span data-ttu-id="8ade7-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ade7-219">System-Flags</span></span>           | <span data-ttu-id="8ade7-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ade7-220">0x00000010</span></span>                                                          |
| <span data-ttu-id="8ade7-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8ade7-221">Classes used in</span></span>        | [<span data-ttu-id="8ade7-222">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="8ade7-222">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8ade7-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8ade7-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8ade7-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8ade7-224">Entry</span></span> | <span data-ttu-id="8ade7-225">Wert</span><span class="sxs-lookup"><span data-stu-id="8ade7-225">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8ade7-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8ade7-226">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8ade7-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ade7-227">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8ade7-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ade7-228">System-Only</span></span>            | <span data-ttu-id="8ade7-229">False</span><span class="sxs-lookup"><span data-stu-id="8ade7-229">False</span></span>                                                               |
| <span data-ttu-id="8ade7-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8ade7-230">Is-Single-Valued</span></span>       | <span data-ttu-id="8ade7-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-231">True</span></span>                                                                |
| <span data-ttu-id="8ade7-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8ade7-232">Is Indexed</span></span>             | <span data-ttu-id="8ade7-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-233">True</span></span>                                                                |
| <span data-ttu-id="8ade7-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8ade7-234">In Global Catalog</span></span>      | <span data-ttu-id="8ade7-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-235">True</span></span>                                                                |
| <span data-ttu-id="8ade7-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8ade7-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ade7-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8ade7-237">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8ade7-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ade7-238">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8ade7-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ade7-239">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8ade7-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ade7-240">Search-Flags</span></span>           | <span data-ttu-id="8ade7-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8ade7-241">0x00000001</span></span>                                                          |
| <span data-ttu-id="8ade7-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ade7-242">System-Flags</span></span>           | <span data-ttu-id="8ade7-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ade7-243">0x00000010</span></span>                                                          |
| <span data-ttu-id="8ade7-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8ade7-244">Classes used in</span></span>        | [<span data-ttu-id="8ade7-245">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="8ade7-245">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8ade7-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8ade7-246">Windows Server 2012</span></span>



| <span data-ttu-id="8ade7-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8ade7-247">Entry</span></span> | <span data-ttu-id="8ade7-248">Wert</span><span class="sxs-lookup"><span data-stu-id="8ade7-248">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8ade7-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8ade7-249">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8ade7-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ade7-250">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8ade7-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ade7-251">System-Only</span></span>            | <span data-ttu-id="8ade7-252">False</span><span class="sxs-lookup"><span data-stu-id="8ade7-252">False</span></span>                                                               |
| <span data-ttu-id="8ade7-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8ade7-253">Is-Single-Valued</span></span>       | <span data-ttu-id="8ade7-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-254">True</span></span>                                                                |
| <span data-ttu-id="8ade7-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8ade7-255">Is Indexed</span></span>             | <span data-ttu-id="8ade7-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-256">True</span></span>                                                                |
| <span data-ttu-id="8ade7-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8ade7-257">In Global Catalog</span></span>      | <span data-ttu-id="8ade7-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ade7-258">True</span></span>                                                                |
| <span data-ttu-id="8ade7-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8ade7-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ade7-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8ade7-260">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8ade7-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ade7-261">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8ade7-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ade7-262">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8ade7-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ade7-263">Search-Flags</span></span>           | <span data-ttu-id="8ade7-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8ade7-264">0x00000001</span></span>                                                          |
| <span data-ttu-id="8ade7-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ade7-265">System-Flags</span></span>           | <span data-ttu-id="8ade7-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ade7-266">0x00000010</span></span>                                                          |
| <span data-ttu-id="8ade7-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8ade7-267">Classes used in</span></span>        | [<span data-ttu-id="8ade7-268">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="8ade7-268">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





