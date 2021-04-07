---
title: MS-SQL-RegisteredOwner-Attribut
description: Der registrierte Besitzer für die aktuelle Instanz von SQL Server.
ms.assetid: d07712e8-021d-40db-91ba-0fef7e89bb0f
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-SQL-RegisteredOwner-Attributs
- AD-Schema des MS-SQL-RegisteredOwner-Attributs
topic_type:
- apiref
api_name:
- MS-SQL-RegisteredOwner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e201494afffdfea59b75bc1901a474469871351
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103745201"
---
# <a name="ms-sql-registeredowner-attribute"></a><span data-ttu-id="0f7b3-105">MS-SQL-RegisteredOwner-Attribut</span><span class="sxs-lookup"><span data-stu-id="0f7b3-105">MS-SQL-RegisteredOwner attribute</span></span>

<span data-ttu-id="0f7b3-106">Der registrierte Besitzer für die aktuelle Instanz von SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0f7b3-106">The registered owner for the current instance of SQL Server.</span></span>



| <span data-ttu-id="0f7b3-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0f7b3-107">Entry</span></span> | <span data-ttu-id="0f7b3-108">Wert</span><span class="sxs-lookup"><span data-stu-id="0f7b3-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="0f7b3-109">CN</span><span class="sxs-lookup"><span data-stu-id="0f7b3-109">CN</span></span>                | <span data-ttu-id="0f7b3-110">MS-SQL-RegisteredOwner</span><span class="sxs-lookup"><span data-stu-id="0f7b3-110">MS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="0f7b3-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0f7b3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0f7b3-112">MS-SQL-RegisteredOwner</span><span class="sxs-lookup"><span data-stu-id="0f7b3-112">mS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="0f7b3-113">Size</span><span class="sxs-lookup"><span data-stu-id="0f7b3-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="0f7b3-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0f7b3-114">Update Privilege</span></span>  | <span data-ttu-id="0f7b3-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="0f7b3-115">Domain administrator</span></span>                        |
| <span data-ttu-id="0f7b3-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="0f7b3-116">Update Frequency</span></span>  | <span data-ttu-id="0f7b3-117">Beim System Setup.</span><span class="sxs-lookup"><span data-stu-id="0f7b3-117">At system setup.</span></span>                            |
| <span data-ttu-id="0f7b3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0f7b3-118">Attribute-Id</span></span>      | <span data-ttu-id="0f7b3-119">1.2.840.113556.1.4.1364</span><span class="sxs-lookup"><span data-stu-id="0f7b3-119">1.2.840.113556.1.4.1364</span></span>                     |
| <span data-ttu-id="0f7b3-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0f7b3-120">System-Id-Guid</span></span>    | <span data-ttu-id="0f7b3-121">48f & D44 EA-CCEE-11d2-9993-0000f 87a57d4</span><span class="sxs-lookup"><span data-stu-id="0f7b3-121">48fd44ea-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="0f7b3-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f7b3-122">Syntax</span></span>            | [<span data-ttu-id="0f7b3-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="0f7b3-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="0f7b3-124">Implementations</span></span>

-   [<span data-ttu-id="0f7b3-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0f7b3-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0f7b3-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0f7b3-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0f7b3-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0f7b3-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0f7b3-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0f7b3-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0f7b3-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0f7b3-132">Entry</span></span> | <span data-ttu-id="0f7b3-133">Wert</span><span class="sxs-lookup"><span data-stu-id="0f7b3-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7b3-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0f7b3-134">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f7b3-135">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f7b3-136">System-Only</span></span>            | <span data-ttu-id="0f7b3-137">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-137">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0f7b3-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0f7b3-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f7b3-139">True</span></span>                                                                                                                  |
| <span data-ttu-id="0f7b3-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0f7b3-140">Is Indexed</span></span>             | <span data-ttu-id="0f7b3-141">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-141">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0f7b3-142">In Global Catalog</span></span>      | <span data-ttu-id="0f7b3-143">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-143">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f7b3-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f7b3-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0f7b3-145">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="0f7b3-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f7b3-146">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f7b3-147">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f7b3-148">Search-Flags</span></span>           | <span data-ttu-id="0f7b3-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f7b3-149">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="0f7b3-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f7b3-150">System-Flags</span></span>           | <span data-ttu-id="0f7b3-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f7b3-151">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="0f7b3-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0f7b3-152">Classes used in</span></span>        | [<span data-ttu-id="0f7b3-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="0f7b3-154">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-154">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0f7b3-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0f7b3-155">Windows Server 2003</span></span>



| <span data-ttu-id="0f7b3-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0f7b3-156">Entry</span></span> | <span data-ttu-id="0f7b3-157">Wert</span><span class="sxs-lookup"><span data-stu-id="0f7b3-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7b3-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0f7b3-158">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f7b3-159">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f7b3-160">System-Only</span></span>            | <span data-ttu-id="0f7b3-161">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-161">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0f7b3-162">Is-Single-Valued</span></span>       | <span data-ttu-id="0f7b3-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f7b3-163">True</span></span>                                                                                                                  |
| <span data-ttu-id="0f7b3-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0f7b3-164">Is Indexed</span></span>             | <span data-ttu-id="0f7b3-165">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-165">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0f7b3-166">In Global Catalog</span></span>      | <span data-ttu-id="0f7b3-167">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-167">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f7b3-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f7b3-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0f7b3-169">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="0f7b3-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f7b3-170">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f7b3-171">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f7b3-172">Search-Flags</span></span>           | <span data-ttu-id="0f7b3-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f7b3-173">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="0f7b3-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f7b3-174">System-Flags</span></span>           | <span data-ttu-id="0f7b3-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f7b3-175">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="0f7b3-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0f7b3-176">Classes used in</span></span>        | [<span data-ttu-id="0f7b3-177">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="0f7b3-178">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-178">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0f7b3-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0f7b3-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0f7b3-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0f7b3-180">Entry</span></span> | <span data-ttu-id="0f7b3-181">Wert</span><span class="sxs-lookup"><span data-stu-id="0f7b3-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7b3-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0f7b3-182">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f7b3-183">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f7b3-184">System-Only</span></span>            | <span data-ttu-id="0f7b3-185">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-185">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0f7b3-186">Is-Single-Valued</span></span>       | <span data-ttu-id="0f7b3-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f7b3-187">True</span></span>                                                                                                                  |
| <span data-ttu-id="0f7b3-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0f7b3-188">Is Indexed</span></span>             | <span data-ttu-id="0f7b3-189">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-189">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0f7b3-190">In Global Catalog</span></span>      | <span data-ttu-id="0f7b3-191">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-191">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f7b3-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f7b3-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0f7b3-193">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="0f7b3-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f7b3-194">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f7b3-195">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f7b3-196">Search-Flags</span></span>           | <span data-ttu-id="0f7b3-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f7b3-197">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="0f7b3-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f7b3-198">System-Flags</span></span>           | <span data-ttu-id="0f7b3-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f7b3-199">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="0f7b3-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0f7b3-200">Classes used in</span></span>        | [<span data-ttu-id="0f7b3-201">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-201">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="0f7b3-202">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-202">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0f7b3-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f7b3-203">Windows Server 2008</span></span>



| <span data-ttu-id="0f7b3-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0f7b3-204">Entry</span></span> | <span data-ttu-id="0f7b3-205">Wert</span><span class="sxs-lookup"><span data-stu-id="0f7b3-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7b3-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0f7b3-206">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f7b3-207">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f7b3-208">System-Only</span></span>            | <span data-ttu-id="0f7b3-209">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-209">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0f7b3-210">Is-Single-Valued</span></span>       | <span data-ttu-id="0f7b3-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f7b3-211">True</span></span>                                                                                                                  |
| <span data-ttu-id="0f7b3-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0f7b3-212">Is Indexed</span></span>             | <span data-ttu-id="0f7b3-213">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-213">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0f7b3-214">In Global Catalog</span></span>      | <span data-ttu-id="0f7b3-215">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-215">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f7b3-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f7b3-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0f7b3-217">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="0f7b3-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f7b3-218">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f7b3-219">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f7b3-220">Search-Flags</span></span>           | <span data-ttu-id="0f7b3-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f7b3-221">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="0f7b3-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f7b3-222">System-Flags</span></span>           | <span data-ttu-id="0f7b3-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f7b3-223">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="0f7b3-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0f7b3-224">Classes used in</span></span>        | [<span data-ttu-id="0f7b3-225">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-225">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="0f7b3-226">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-226">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0f7b3-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0f7b3-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0f7b3-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0f7b3-228">Entry</span></span> | <span data-ttu-id="0f7b3-229">Wert</span><span class="sxs-lookup"><span data-stu-id="0f7b3-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7b3-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0f7b3-230">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f7b3-231">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f7b3-232">System-Only</span></span>            | <span data-ttu-id="0f7b3-233">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-233">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0f7b3-234">Is-Single-Valued</span></span>       | <span data-ttu-id="0f7b3-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f7b3-235">True</span></span>                                                                                                                  |
| <span data-ttu-id="0f7b3-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0f7b3-236">Is Indexed</span></span>             | <span data-ttu-id="0f7b3-237">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-237">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0f7b3-238">In Global Catalog</span></span>      | <span data-ttu-id="0f7b3-239">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-239">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f7b3-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f7b3-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0f7b3-241">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="0f7b3-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f7b3-242">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f7b3-243">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f7b3-244">Search-Flags</span></span>           | <span data-ttu-id="0f7b3-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f7b3-245">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="0f7b3-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f7b3-246">System-Flags</span></span>           | <span data-ttu-id="0f7b3-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f7b3-247">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="0f7b3-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0f7b3-248">Classes used in</span></span>        | [<span data-ttu-id="0f7b3-249">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-249">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="0f7b3-250">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-250">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0f7b3-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0f7b3-251">Windows Server 2012</span></span>



| <span data-ttu-id="0f7b3-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0f7b3-252">Entry</span></span> | <span data-ttu-id="0f7b3-253">Wert</span><span class="sxs-lookup"><span data-stu-id="0f7b3-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7b3-254">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0f7b3-254">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f7b3-255">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f7b3-256">System-Only</span></span>            | <span data-ttu-id="0f7b3-257">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-257">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-258">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0f7b3-258">Is-Single-Valued</span></span>       | <span data-ttu-id="0f7b3-259">Richtig</span><span class="sxs-lookup"><span data-stu-id="0f7b3-259">True</span></span>                                                                                                                  |
| <span data-ttu-id="0f7b3-260">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0f7b3-260">Is Indexed</span></span>             | <span data-ttu-id="0f7b3-261">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-261">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-262">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0f7b3-262">In Global Catalog</span></span>      | <span data-ttu-id="0f7b3-263">False</span><span class="sxs-lookup"><span data-stu-id="0f7b3-263">False</span></span>                                                                                                                 |
| <span data-ttu-id="0f7b3-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f7b3-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f7b3-265">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0f7b3-265">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="0f7b3-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f7b3-266">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f7b3-267">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="0f7b3-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f7b3-268">Search-Flags</span></span>           | <span data-ttu-id="0f7b3-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f7b3-269">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="0f7b3-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f7b3-270">System-Flags</span></span>           | <span data-ttu-id="0f7b3-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f7b3-271">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="0f7b3-272">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0f7b3-272">Classes used in</span></span>        | [<span data-ttu-id="0f7b3-273">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-273">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="0f7b3-274">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="0f7b3-274">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



 

 





