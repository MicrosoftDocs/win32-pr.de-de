---
title: MS-SQL-Version-Attribut
description: Die Version der aktuellen Instanz von SQL Server.
ms.assetid: 0003892c-906d-429b-bc98-bbc441b2d58b
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-SQL-Version-Attribut
- AD-Schema für MS-SQL-Version-Attribut
topic_type:
- apiref
api_name:
- MS-SQL-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446a436a30311f5696d8ed63334b0cf796eb2767
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859879"
---
# <a name="ms-sql-version-attribute"></a><span data-ttu-id="f51e9-105">MS-SQL-Version-Attribut</span><span class="sxs-lookup"><span data-stu-id="f51e9-105">MS-SQL-Version attribute</span></span>

<span data-ttu-id="f51e9-106">Die Version der aktuellen Instanz von SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f51e9-106">The version for the current instance of SQL Server.</span></span>



| <span data-ttu-id="f51e9-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f51e9-107">Entry</span></span> | <span data-ttu-id="f51e9-108">Wert</span><span class="sxs-lookup"><span data-stu-id="f51e9-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f51e9-109">CN</span><span class="sxs-lookup"><span data-stu-id="f51e9-109">CN</span></span>                | <span data-ttu-id="f51e9-110">MS-SQL-Version</span><span class="sxs-lookup"><span data-stu-id="f51e9-110">MS-SQL-Version</span></span>                              |
| <span data-ttu-id="f51e9-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f51e9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f51e9-112">MS-SQL-Version</span><span class="sxs-lookup"><span data-stu-id="f51e9-112">mS-SQL-Version</span></span>                              |
| <span data-ttu-id="f51e9-113">Size</span><span class="sxs-lookup"><span data-stu-id="f51e9-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="f51e9-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f51e9-114">Update Privilege</span></span>  | <span data-ttu-id="f51e9-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f51e9-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="f51e9-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f51e9-116">Update Frequency</span></span>  | <span data-ttu-id="f51e9-117">Beim System Setup.</span><span class="sxs-lookup"><span data-stu-id="f51e9-117">At system setup.</span></span>                            |
| <span data-ttu-id="f51e9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f51e9-118">Attribute-Id</span></span>      | <span data-ttu-id="f51e9-119">1.2.840.113556.1.4.1388</span><span class="sxs-lookup"><span data-stu-id="f51e9-119">1.2.840.113556.1.4.1388</span></span>                     |
| <span data-ttu-id="f51e9-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f51e9-120">System-Id-Guid</span></span>    | <span data-ttu-id="f51e9-121">c07cc1d0-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="f51e9-121">c07cc1d0-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="f51e9-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="f51e9-122">Syntax</span></span>            | [<span data-ttu-id="f51e9-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f51e9-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f51e9-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f51e9-124">Implementations</span></span>

-   [<span data-ttu-id="f51e9-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f51e9-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f51e9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f51e9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f51e9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f51e9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f51e9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f51e9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f51e9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f51e9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f51e9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f51e9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f51e9-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f51e9-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f51e9-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f51e9-132">Entry</span></span> | <span data-ttu-id="f51e9-133">Wert</span><span class="sxs-lookup"><span data-stu-id="f51e9-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f51e9-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f51e9-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f51e9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f51e9-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f51e9-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f51e9-136">System-Only</span></span>            | <span data-ttu-id="f51e9-137">False</span><span class="sxs-lookup"><span data-stu-id="f51e9-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="f51e9-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f51e9-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f51e9-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f51e9-140">Is Indexed</span></span>             | <span data-ttu-id="f51e9-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-141">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f51e9-142">In Global Catalog</span></span>      | <span data-ttu-id="f51e9-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-143">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f51e9-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f51e9-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f51e9-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="f51e9-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f51e9-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f51e9-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f51e9-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f51e9-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f51e9-148">Search-Flags</span></span>           | <span data-ttu-id="f51e9-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f51e9-149">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="f51e9-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f51e9-150">System-Flags</span></span>           | <span data-ttu-id="f51e9-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f51e9-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="f51e9-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f51e9-152">Classes used in</span></span>        | [<span data-ttu-id="f51e9-153">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="f51e9-153">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="f51e9-154">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="f51e9-154">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f51e9-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f51e9-155">Windows Server 2003</span></span>



| <span data-ttu-id="f51e9-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f51e9-156">Entry</span></span> | <span data-ttu-id="f51e9-157">Wert</span><span class="sxs-lookup"><span data-stu-id="f51e9-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f51e9-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f51e9-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f51e9-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f51e9-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f51e9-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="f51e9-160">System-Only</span></span>            | <span data-ttu-id="f51e9-161">False</span><span class="sxs-lookup"><span data-stu-id="f51e9-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="f51e9-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f51e9-162">Is-Single-Valued</span></span>       | <span data-ttu-id="f51e9-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f51e9-164">Is Indexed</span></span>             | <span data-ttu-id="f51e9-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-165">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f51e9-166">In Global Catalog</span></span>      | <span data-ttu-id="f51e9-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-167">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f51e9-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="f51e9-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f51e9-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="f51e9-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f51e9-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f51e9-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f51e9-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f51e9-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f51e9-172">Search-Flags</span></span>           | <span data-ttu-id="f51e9-173">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f51e9-173">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="f51e9-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f51e9-174">System-Flags</span></span>           | <span data-ttu-id="f51e9-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f51e9-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="f51e9-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f51e9-176">Classes used in</span></span>        | [<span data-ttu-id="f51e9-177">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="f51e9-177">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="f51e9-178">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="f51e9-178">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f51e9-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f51e9-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f51e9-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f51e9-180">Entry</span></span> | <span data-ttu-id="f51e9-181">Wert</span><span class="sxs-lookup"><span data-stu-id="f51e9-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f51e9-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f51e9-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f51e9-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f51e9-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f51e9-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="f51e9-184">System-Only</span></span>            | <span data-ttu-id="f51e9-185">False</span><span class="sxs-lookup"><span data-stu-id="f51e9-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="f51e9-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f51e9-186">Is-Single-Valued</span></span>       | <span data-ttu-id="f51e9-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f51e9-188">Is Indexed</span></span>             | <span data-ttu-id="f51e9-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-189">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f51e9-190">In Global Catalog</span></span>      | <span data-ttu-id="f51e9-191">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-191">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f51e9-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="f51e9-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f51e9-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="f51e9-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f51e9-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f51e9-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f51e9-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f51e9-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f51e9-196">Search-Flags</span></span>           | <span data-ttu-id="f51e9-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f51e9-197">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="f51e9-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f51e9-198">System-Flags</span></span>           | <span data-ttu-id="f51e9-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f51e9-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="f51e9-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f51e9-200">Classes used in</span></span>        | [<span data-ttu-id="f51e9-201">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="f51e9-201">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="f51e9-202">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="f51e9-202">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f51e9-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f51e9-203">Windows Server 2008</span></span>



| <span data-ttu-id="f51e9-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f51e9-204">Entry</span></span> | <span data-ttu-id="f51e9-205">Wert</span><span class="sxs-lookup"><span data-stu-id="f51e9-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f51e9-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f51e9-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f51e9-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f51e9-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f51e9-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="f51e9-208">System-Only</span></span>            | <span data-ttu-id="f51e9-209">False</span><span class="sxs-lookup"><span data-stu-id="f51e9-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="f51e9-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f51e9-210">Is-Single-Valued</span></span>       | <span data-ttu-id="f51e9-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f51e9-212">Is Indexed</span></span>             | <span data-ttu-id="f51e9-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-213">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f51e9-214">In Global Catalog</span></span>      | <span data-ttu-id="f51e9-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-215">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f51e9-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="f51e9-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f51e9-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="f51e9-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f51e9-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f51e9-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f51e9-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f51e9-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f51e9-220">Search-Flags</span></span>           | <span data-ttu-id="f51e9-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f51e9-221">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="f51e9-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f51e9-222">System-Flags</span></span>           | <span data-ttu-id="f51e9-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f51e9-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="f51e9-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f51e9-224">Classes used in</span></span>        | [<span data-ttu-id="f51e9-225">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="f51e9-225">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="f51e9-226">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="f51e9-226">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f51e9-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f51e9-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f51e9-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f51e9-228">Entry</span></span> | <span data-ttu-id="f51e9-229">Wert</span><span class="sxs-lookup"><span data-stu-id="f51e9-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f51e9-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f51e9-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f51e9-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f51e9-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f51e9-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="f51e9-232">System-Only</span></span>            | <span data-ttu-id="f51e9-233">False</span><span class="sxs-lookup"><span data-stu-id="f51e9-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="f51e9-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f51e9-234">Is-Single-Valued</span></span>       | <span data-ttu-id="f51e9-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f51e9-236">Is Indexed</span></span>             | <span data-ttu-id="f51e9-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-237">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f51e9-238">In Global Catalog</span></span>      | <span data-ttu-id="f51e9-239">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-239">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f51e9-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="f51e9-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f51e9-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="f51e9-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f51e9-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f51e9-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f51e9-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f51e9-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f51e9-244">Search-Flags</span></span>           | <span data-ttu-id="f51e9-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f51e9-245">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="f51e9-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f51e9-246">System-Flags</span></span>           | <span data-ttu-id="f51e9-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f51e9-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="f51e9-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f51e9-248">Classes used in</span></span>        | [<span data-ttu-id="f51e9-249">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="f51e9-249">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="f51e9-250">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="f51e9-250">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f51e9-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f51e9-251">Windows Server 2012</span></span>



| <span data-ttu-id="f51e9-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f51e9-252">Entry</span></span> | <span data-ttu-id="f51e9-253">Wert</span><span class="sxs-lookup"><span data-stu-id="f51e9-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f51e9-254">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f51e9-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f51e9-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f51e9-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f51e9-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="f51e9-256">System-Only</span></span>            | <span data-ttu-id="f51e9-257">False</span><span class="sxs-lookup"><span data-stu-id="f51e9-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="f51e9-258">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f51e9-258">Is-Single-Valued</span></span>       | <span data-ttu-id="f51e9-259">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-260">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f51e9-260">Is Indexed</span></span>             | <span data-ttu-id="f51e9-261">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-261">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-262">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f51e9-262">In Global Catalog</span></span>      | <span data-ttu-id="f51e9-263">Richtig</span><span class="sxs-lookup"><span data-stu-id="f51e9-263">True</span></span>                                                                                                                          |
| <span data-ttu-id="f51e9-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f51e9-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="f51e9-265">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f51e9-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="f51e9-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f51e9-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f51e9-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f51e9-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f51e9-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f51e9-268">Search-Flags</span></span>           | <span data-ttu-id="f51e9-269">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f51e9-269">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="f51e9-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f51e9-270">System-Flags</span></span>           | <span data-ttu-id="f51e9-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f51e9-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="f51e9-272">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f51e9-272">Classes used in</span></span>        | [<span data-ttu-id="f51e9-273">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="f51e9-273">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="f51e9-274">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="f51e9-274">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



 

 





