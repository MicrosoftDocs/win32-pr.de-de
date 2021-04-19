---
title: MS-SQL-ServiceAccount-Attribut
description: Eine benutzerdefinierte Zeichenfolge. Der Standardwert ist auf ServiceAccount festgelegt.
ms.assetid: 0db095c8-8492-45c0-b509-d4082cec2c13
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-SQL-ServiceAccount-Attributs
- AD-Schema des MS-SQL-ServiceAccount-Attributs
topic_type:
- apiref
api_name:
- MS-SQL-ServiceAccount
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab96de3d56dedd3178e579e100f00b77df4edb7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342894"
---
# <a name="ms-sql-serviceaccount-attribute"></a><span data-ttu-id="55e64-106">MS-SQL-ServiceAccount-Attribut</span><span class="sxs-lookup"><span data-stu-id="55e64-106">MS-SQL-ServiceAccount attribute</span></span>

<span data-ttu-id="55e64-107">Eine benutzerdefinierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="55e64-107">A user defined string.</span></span> <span data-ttu-id="55e64-108">Der Standardwert ist auf ServiceAccount festgelegt.</span><span class="sxs-lookup"><span data-stu-id="55e64-108">The default is set to ServiceAccount.</span></span>



| <span data-ttu-id="55e64-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="55e64-109">Entry</span></span> | <span data-ttu-id="55e64-110">Wert</span><span class="sxs-lookup"><span data-stu-id="55e64-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="55e64-111">CN</span><span class="sxs-lookup"><span data-stu-id="55e64-111">CN</span></span>                | <span data-ttu-id="55e64-112">MS-SQL-ServiceAccount</span><span class="sxs-lookup"><span data-stu-id="55e64-112">MS-SQL-ServiceAccount</span></span>                       |
| <span data-ttu-id="55e64-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="55e64-113">Ldap-Display-Name</span></span> | <span data-ttu-id="55e64-114">MS-SQL-ServiceAccount</span><span class="sxs-lookup"><span data-stu-id="55e64-114">mS-SQL-ServiceAccount</span></span>                       |
| <span data-ttu-id="55e64-115">Size</span><span class="sxs-lookup"><span data-stu-id="55e64-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="55e64-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="55e64-116">Update Privilege</span></span>  | <span data-ttu-id="55e64-117">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="55e64-117">Domain administrator</span></span>                        |
| <span data-ttu-id="55e64-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="55e64-118">Update Frequency</span></span>  | <span data-ttu-id="55e64-119">Beim System Setup.</span><span class="sxs-lookup"><span data-stu-id="55e64-119">At system setup.</span></span>                            |
| <span data-ttu-id="55e64-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="55e64-120">Attribute-Id</span></span>      | <span data-ttu-id="55e64-121">1.2.840.113556.1.4.1369</span><span class="sxs-lookup"><span data-stu-id="55e64-121">1.2.840.113556.1.4.1369</span></span>                     |
| <span data-ttu-id="55e64-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="55e64-122">System-Id-Guid</span></span>    | <span data-ttu-id="55e64-123">64933a3e-CCEE-11d2-9993-0000f 87a57d4</span><span class="sxs-lookup"><span data-stu-id="55e64-123">64933a3e-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="55e64-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="55e64-124">Syntax</span></span>            | [<span data-ttu-id="55e64-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="55e64-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="55e64-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="55e64-126">Implementations</span></span>

-   [<span data-ttu-id="55e64-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="55e64-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="55e64-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="55e64-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="55e64-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="55e64-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="55e64-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="55e64-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="55e64-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="55e64-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="55e64-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="55e64-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="55e64-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="55e64-133">Windows 2000 Server</span></span>



| <span data-ttu-id="55e64-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="55e64-134">Entry</span></span> | <span data-ttu-id="55e64-135">Wert</span><span class="sxs-lookup"><span data-stu-id="55e64-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55e64-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="55e64-136">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="55e64-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55e64-137">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="55e64-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="55e64-138">System-Only</span></span>            | <span data-ttu-id="55e64-139">False</span><span class="sxs-lookup"><span data-stu-id="55e64-139">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="55e64-140">Is-Single-Valued</span></span>       | <span data-ttu-id="55e64-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="55e64-141">True</span></span>                                                                                                                  |
| <span data-ttu-id="55e64-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="55e64-142">Is Indexed</span></span>             | <span data-ttu-id="55e64-143">False</span><span class="sxs-lookup"><span data-stu-id="55e64-143">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="55e64-144">In Global Catalog</span></span>      | <span data-ttu-id="55e64-145">False</span><span class="sxs-lookup"><span data-stu-id="55e64-145">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="55e64-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="55e64-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="55e64-147">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="55e64-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55e64-148">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="55e64-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55e64-149">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="55e64-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55e64-150">Search-Flags</span></span>           | <span data-ttu-id="55e64-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55e64-151">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="55e64-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55e64-152">System-Flags</span></span>           | <span data-ttu-id="55e64-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e64-153">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="55e64-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="55e64-154">Classes used in</span></span>        | [<span data-ttu-id="55e64-155">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="55e64-155">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="55e64-156">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="55e64-156">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="55e64-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="55e64-157">Windows Server 2003</span></span>



| <span data-ttu-id="55e64-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="55e64-158">Entry</span></span> | <span data-ttu-id="55e64-159">Wert</span><span class="sxs-lookup"><span data-stu-id="55e64-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55e64-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="55e64-160">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="55e64-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55e64-161">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="55e64-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="55e64-162">System-Only</span></span>            | <span data-ttu-id="55e64-163">False</span><span class="sxs-lookup"><span data-stu-id="55e64-163">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="55e64-164">Is-Single-Valued</span></span>       | <span data-ttu-id="55e64-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="55e64-165">True</span></span>                                                                                                                  |
| <span data-ttu-id="55e64-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="55e64-166">Is Indexed</span></span>             | <span data-ttu-id="55e64-167">False</span><span class="sxs-lookup"><span data-stu-id="55e64-167">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="55e64-168">In Global Catalog</span></span>      | <span data-ttu-id="55e64-169">False</span><span class="sxs-lookup"><span data-stu-id="55e64-169">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="55e64-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="55e64-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="55e64-171">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="55e64-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55e64-172">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="55e64-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55e64-173">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="55e64-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55e64-174">Search-Flags</span></span>           | <span data-ttu-id="55e64-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55e64-175">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="55e64-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55e64-176">System-Flags</span></span>           | <span data-ttu-id="55e64-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e64-177">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="55e64-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="55e64-178">Classes used in</span></span>        | [<span data-ttu-id="55e64-179">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="55e64-179">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="55e64-180">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="55e64-180">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="55e64-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="55e64-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="55e64-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="55e64-182">Entry</span></span> | <span data-ttu-id="55e64-183">Wert</span><span class="sxs-lookup"><span data-stu-id="55e64-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55e64-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="55e64-184">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="55e64-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55e64-185">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="55e64-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="55e64-186">System-Only</span></span>            | <span data-ttu-id="55e64-187">False</span><span class="sxs-lookup"><span data-stu-id="55e64-187">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="55e64-188">Is-Single-Valued</span></span>       | <span data-ttu-id="55e64-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="55e64-189">True</span></span>                                                                                                                  |
| <span data-ttu-id="55e64-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="55e64-190">Is Indexed</span></span>             | <span data-ttu-id="55e64-191">False</span><span class="sxs-lookup"><span data-stu-id="55e64-191">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="55e64-192">In Global Catalog</span></span>      | <span data-ttu-id="55e64-193">False</span><span class="sxs-lookup"><span data-stu-id="55e64-193">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="55e64-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="55e64-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="55e64-195">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="55e64-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55e64-196">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="55e64-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55e64-197">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="55e64-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55e64-198">Search-Flags</span></span>           | <span data-ttu-id="55e64-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55e64-199">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="55e64-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55e64-200">System-Flags</span></span>           | <span data-ttu-id="55e64-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e64-201">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="55e64-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="55e64-202">Classes used in</span></span>        | [<span data-ttu-id="55e64-203">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="55e64-203">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="55e64-204">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="55e64-204">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="55e64-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55e64-205">Windows Server 2008</span></span>



| <span data-ttu-id="55e64-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="55e64-206">Entry</span></span> | <span data-ttu-id="55e64-207">Wert</span><span class="sxs-lookup"><span data-stu-id="55e64-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55e64-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="55e64-208">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="55e64-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55e64-209">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="55e64-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="55e64-210">System-Only</span></span>            | <span data-ttu-id="55e64-211">False</span><span class="sxs-lookup"><span data-stu-id="55e64-211">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="55e64-212">Is-Single-Valued</span></span>       | <span data-ttu-id="55e64-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="55e64-213">True</span></span>                                                                                                                  |
| <span data-ttu-id="55e64-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="55e64-214">Is Indexed</span></span>             | <span data-ttu-id="55e64-215">False</span><span class="sxs-lookup"><span data-stu-id="55e64-215">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="55e64-216">In Global Catalog</span></span>      | <span data-ttu-id="55e64-217">False</span><span class="sxs-lookup"><span data-stu-id="55e64-217">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="55e64-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="55e64-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="55e64-219">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="55e64-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55e64-220">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="55e64-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55e64-221">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="55e64-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55e64-222">Search-Flags</span></span>           | <span data-ttu-id="55e64-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55e64-223">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="55e64-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55e64-224">System-Flags</span></span>           | <span data-ttu-id="55e64-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e64-225">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="55e64-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="55e64-226">Classes used in</span></span>        | [<span data-ttu-id="55e64-227">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="55e64-227">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="55e64-228">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="55e64-228">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="55e64-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="55e64-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="55e64-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="55e64-230">Entry</span></span> | <span data-ttu-id="55e64-231">Wert</span><span class="sxs-lookup"><span data-stu-id="55e64-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55e64-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="55e64-232">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="55e64-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55e64-233">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="55e64-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="55e64-234">System-Only</span></span>            | <span data-ttu-id="55e64-235">False</span><span class="sxs-lookup"><span data-stu-id="55e64-235">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-236">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="55e64-236">Is-Single-Valued</span></span>       | <span data-ttu-id="55e64-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="55e64-237">True</span></span>                                                                                                                  |
| <span data-ttu-id="55e64-238">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="55e64-238">Is Indexed</span></span>             | <span data-ttu-id="55e64-239">False</span><span class="sxs-lookup"><span data-stu-id="55e64-239">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-240">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="55e64-240">In Global Catalog</span></span>      | <span data-ttu-id="55e64-241">False</span><span class="sxs-lookup"><span data-stu-id="55e64-241">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="55e64-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="55e64-243">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="55e64-243">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="55e64-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55e64-244">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="55e64-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55e64-245">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="55e64-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55e64-246">Search-Flags</span></span>           | <span data-ttu-id="55e64-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55e64-247">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="55e64-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55e64-248">System-Flags</span></span>           | <span data-ttu-id="55e64-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e64-249">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="55e64-250">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="55e64-250">Classes used in</span></span>        | [<span data-ttu-id="55e64-251">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="55e64-251">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="55e64-252">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="55e64-252">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="55e64-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="55e64-253">Windows Server 2012</span></span>



| <span data-ttu-id="55e64-254">Eingabe</span><span class="sxs-lookup"><span data-stu-id="55e64-254">Entry</span></span> | <span data-ttu-id="55e64-255">Wert</span><span class="sxs-lookup"><span data-stu-id="55e64-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55e64-256">Link-ID</span><span class="sxs-lookup"><span data-stu-id="55e64-256">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="55e64-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55e64-257">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="55e64-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="55e64-258">System-Only</span></span>            | <span data-ttu-id="55e64-259">False</span><span class="sxs-lookup"><span data-stu-id="55e64-259">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-260">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="55e64-260">Is-Single-Valued</span></span>       | <span data-ttu-id="55e64-261">Richtig</span><span class="sxs-lookup"><span data-stu-id="55e64-261">True</span></span>                                                                                                                  |
| <span data-ttu-id="55e64-262">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="55e64-262">Is Indexed</span></span>             | <span data-ttu-id="55e64-263">False</span><span class="sxs-lookup"><span data-stu-id="55e64-263">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-264">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="55e64-264">In Global Catalog</span></span>      | <span data-ttu-id="55e64-265">False</span><span class="sxs-lookup"><span data-stu-id="55e64-265">False</span></span>                                                                                                                 |
| <span data-ttu-id="55e64-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="55e64-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="55e64-267">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="55e64-267">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="55e64-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55e64-268">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="55e64-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55e64-269">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="55e64-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55e64-270">Search-Flags</span></span>           | <span data-ttu-id="55e64-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55e64-271">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="55e64-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55e64-272">System-Flags</span></span>           | <span data-ttu-id="55e64-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e64-273">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="55e64-274">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="55e64-274">Classes used in</span></span>        | [<span data-ttu-id="55e64-275">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="55e64-275">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="55e64-276">**MS-SQL-olapserver**</span><span class="sxs-lookup"><span data-stu-id="55e64-276">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



 

 





