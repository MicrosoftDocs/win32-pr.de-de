---
title: MS-SQL-NamedPipe-Attribut
description: Die Named Pipe Verbindung.
ms.assetid: d18c911d-06ed-4d08-b584-7b2748620770
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-SQL-NamedPipe-Attributs
- AD-Schema des MS-SQL-NamedPipe-Attributs
topic_type:
- apiref
api_name:
- MS-SQL-NamedPipe
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33e231be0561ae8c0e885911cb92954d6ff0d20d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392250"
---
# <a name="ms-sql-namedpipe-attribute"></a><span data-ttu-id="b3a18-105">MS-SQL-NamedPipe-Attribut</span><span class="sxs-lookup"><span data-stu-id="b3a18-105">MS-SQL-NamedPipe attribute</span></span>

<span data-ttu-id="b3a18-106">Die Named Pipe Verbindung.</span><span class="sxs-lookup"><span data-stu-id="b3a18-106">The named pipe connection.</span></span>



| <span data-ttu-id="b3a18-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3a18-107">Entry</span></span> | <span data-ttu-id="b3a18-108">Wert</span><span class="sxs-lookup"><span data-stu-id="b3a18-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b3a18-109">CN</span><span class="sxs-lookup"><span data-stu-id="b3a18-109">CN</span></span>                | <span data-ttu-id="b3a18-110">MS-SQL-NamedPipe</span><span class="sxs-lookup"><span data-stu-id="b3a18-110">MS-SQL-NamedPipe</span></span>                            |
| <span data-ttu-id="b3a18-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b3a18-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b3a18-112">MS-SQL-NamedPipe</span><span class="sxs-lookup"><span data-stu-id="b3a18-112">mS-SQL-NamedPipe</span></span>                            |
| <span data-ttu-id="b3a18-113">Size</span><span class="sxs-lookup"><span data-stu-id="b3a18-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="b3a18-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b3a18-114">Update Privilege</span></span>  | <span data-ttu-id="b3a18-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b3a18-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="b3a18-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b3a18-116">Update Frequency</span></span>  | <span data-ttu-id="b3a18-117">Beim Systemstart.</span><span class="sxs-lookup"><span data-stu-id="b3a18-117">At system startup.</span></span>                          |
| <span data-ttu-id="b3a18-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b3a18-118">Attribute-Id</span></span>      | <span data-ttu-id="b3a18-119">1.2.840.113556.1.4.1374</span><span class="sxs-lookup"><span data-stu-id="b3a18-119">1.2.840.113556.1.4.1374</span></span>                     |
| <span data-ttu-id="b3a18-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b3a18-120">System-Id-Guid</span></span>    | <span data-ttu-id="b3a18-121">7b91c840-CCEE-11d2-9993-0000f 87a57d4</span><span class="sxs-lookup"><span data-stu-id="b3a18-121">7b91c840-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="b3a18-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3a18-122">Syntax</span></span>            | [<span data-ttu-id="b3a18-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b3a18-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b3a18-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b3a18-124">Implementations</span></span>

-   [<span data-ttu-id="b3a18-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b3a18-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b3a18-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b3a18-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b3a18-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b3a18-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b3a18-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b3a18-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b3a18-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b3a18-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b3a18-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b3a18-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b3a18-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b3a18-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b3a18-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3a18-132">Entry</span></span> | <span data-ttu-id="b3a18-133">Wert</span><span class="sxs-lookup"><span data-stu-id="b3a18-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b3a18-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b3a18-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b3a18-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3a18-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b3a18-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3a18-136">System-Only</span></span>            | <span data-ttu-id="b3a18-137">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-137">False</span></span>                                                     |
| <span data-ttu-id="b3a18-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b3a18-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b3a18-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3a18-139">True</span></span>                                                      |
| <span data-ttu-id="b3a18-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b3a18-140">Is Indexed</span></span>             | <span data-ttu-id="b3a18-141">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-141">False</span></span>                                                     |
| <span data-ttu-id="b3a18-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b3a18-142">In Global Catalog</span></span>      | <span data-ttu-id="b3a18-143">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-143">False</span></span>                                                     |
| <span data-ttu-id="b3a18-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b3a18-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3a18-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b3a18-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b3a18-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3a18-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b3a18-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3a18-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b3a18-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3a18-148">Search-Flags</span></span>           | <span data-ttu-id="b3a18-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3a18-149">0x00000000</span></span>                                                |
| <span data-ttu-id="b3a18-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3a18-150">System-Flags</span></span>           | <span data-ttu-id="b3a18-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3a18-151">0x00000010</span></span>                                                |
| <span data-ttu-id="b3a18-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b3a18-152">Classes used in</span></span>        | [<span data-ttu-id="b3a18-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b3a18-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b3a18-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b3a18-154">Windows Server 2003</span></span>



| <span data-ttu-id="b3a18-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3a18-155">Entry</span></span> | <span data-ttu-id="b3a18-156">Wert</span><span class="sxs-lookup"><span data-stu-id="b3a18-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b3a18-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b3a18-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b3a18-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3a18-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b3a18-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3a18-159">System-Only</span></span>            | <span data-ttu-id="b3a18-160">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-160">False</span></span>                                                     |
| <span data-ttu-id="b3a18-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b3a18-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b3a18-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3a18-162">True</span></span>                                                      |
| <span data-ttu-id="b3a18-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b3a18-163">Is Indexed</span></span>             | <span data-ttu-id="b3a18-164">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-164">False</span></span>                                                     |
| <span data-ttu-id="b3a18-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b3a18-165">In Global Catalog</span></span>      | <span data-ttu-id="b3a18-166">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-166">False</span></span>                                                     |
| <span data-ttu-id="b3a18-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b3a18-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3a18-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b3a18-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b3a18-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3a18-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b3a18-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3a18-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b3a18-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3a18-171">Search-Flags</span></span>           | <span data-ttu-id="b3a18-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3a18-172">0x00000000</span></span>                                                |
| <span data-ttu-id="b3a18-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3a18-173">System-Flags</span></span>           | <span data-ttu-id="b3a18-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3a18-174">0x00000010</span></span>                                                |
| <span data-ttu-id="b3a18-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b3a18-175">Classes used in</span></span>        | [<span data-ttu-id="b3a18-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b3a18-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b3a18-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b3a18-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b3a18-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3a18-178">Entry</span></span> | <span data-ttu-id="b3a18-179">Wert</span><span class="sxs-lookup"><span data-stu-id="b3a18-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b3a18-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b3a18-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b3a18-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3a18-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b3a18-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3a18-182">System-Only</span></span>            | <span data-ttu-id="b3a18-183">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-183">False</span></span>                                                     |
| <span data-ttu-id="b3a18-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b3a18-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b3a18-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3a18-185">True</span></span>                                                      |
| <span data-ttu-id="b3a18-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b3a18-186">Is Indexed</span></span>             | <span data-ttu-id="b3a18-187">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-187">False</span></span>                                                     |
| <span data-ttu-id="b3a18-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b3a18-188">In Global Catalog</span></span>      | <span data-ttu-id="b3a18-189">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-189">False</span></span>                                                     |
| <span data-ttu-id="b3a18-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b3a18-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3a18-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b3a18-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b3a18-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3a18-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b3a18-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3a18-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b3a18-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3a18-194">Search-Flags</span></span>           | <span data-ttu-id="b3a18-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3a18-195">0x00000000</span></span>                                                |
| <span data-ttu-id="b3a18-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3a18-196">System-Flags</span></span>           | <span data-ttu-id="b3a18-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3a18-197">0x00000010</span></span>                                                |
| <span data-ttu-id="b3a18-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b3a18-198">Classes used in</span></span>        | [<span data-ttu-id="b3a18-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b3a18-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b3a18-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3a18-200">Windows Server 2008</span></span>



| <span data-ttu-id="b3a18-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3a18-201">Entry</span></span> | <span data-ttu-id="b3a18-202">Wert</span><span class="sxs-lookup"><span data-stu-id="b3a18-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b3a18-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b3a18-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b3a18-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3a18-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b3a18-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3a18-205">System-Only</span></span>            | <span data-ttu-id="b3a18-206">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-206">False</span></span>                                                     |
| <span data-ttu-id="b3a18-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b3a18-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b3a18-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3a18-208">True</span></span>                                                      |
| <span data-ttu-id="b3a18-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b3a18-209">Is Indexed</span></span>             | <span data-ttu-id="b3a18-210">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-210">False</span></span>                                                     |
| <span data-ttu-id="b3a18-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b3a18-211">In Global Catalog</span></span>      | <span data-ttu-id="b3a18-212">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-212">False</span></span>                                                     |
| <span data-ttu-id="b3a18-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b3a18-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3a18-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b3a18-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b3a18-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3a18-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b3a18-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3a18-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b3a18-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3a18-217">Search-Flags</span></span>           | <span data-ttu-id="b3a18-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3a18-218">0x00000000</span></span>                                                |
| <span data-ttu-id="b3a18-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3a18-219">System-Flags</span></span>           | <span data-ttu-id="b3a18-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3a18-220">0x00000010</span></span>                                                |
| <span data-ttu-id="b3a18-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b3a18-221">Classes used in</span></span>        | [<span data-ttu-id="b3a18-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b3a18-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b3a18-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b3a18-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b3a18-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3a18-224">Entry</span></span> | <span data-ttu-id="b3a18-225">Wert</span><span class="sxs-lookup"><span data-stu-id="b3a18-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b3a18-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b3a18-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b3a18-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3a18-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b3a18-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3a18-228">System-Only</span></span>            | <span data-ttu-id="b3a18-229">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-229">False</span></span>                                                     |
| <span data-ttu-id="b3a18-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b3a18-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b3a18-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3a18-231">True</span></span>                                                      |
| <span data-ttu-id="b3a18-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b3a18-232">Is Indexed</span></span>             | <span data-ttu-id="b3a18-233">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-233">False</span></span>                                                     |
| <span data-ttu-id="b3a18-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b3a18-234">In Global Catalog</span></span>      | <span data-ttu-id="b3a18-235">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-235">False</span></span>                                                     |
| <span data-ttu-id="b3a18-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b3a18-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3a18-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b3a18-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b3a18-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3a18-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b3a18-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3a18-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b3a18-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3a18-240">Search-Flags</span></span>           | <span data-ttu-id="b3a18-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3a18-241">0x00000000</span></span>                                                |
| <span data-ttu-id="b3a18-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3a18-242">System-Flags</span></span>           | <span data-ttu-id="b3a18-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3a18-243">0x00000010</span></span>                                                |
| <span data-ttu-id="b3a18-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b3a18-244">Classes used in</span></span>        | [<span data-ttu-id="b3a18-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b3a18-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b3a18-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b3a18-246">Windows Server 2012</span></span>



| <span data-ttu-id="b3a18-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3a18-247">Entry</span></span> | <span data-ttu-id="b3a18-248">Wert</span><span class="sxs-lookup"><span data-stu-id="b3a18-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b3a18-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b3a18-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b3a18-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3a18-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b3a18-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3a18-251">System-Only</span></span>            | <span data-ttu-id="b3a18-252">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-252">False</span></span>                                                     |
| <span data-ttu-id="b3a18-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b3a18-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b3a18-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="b3a18-254">True</span></span>                                                      |
| <span data-ttu-id="b3a18-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b3a18-255">Is Indexed</span></span>             | <span data-ttu-id="b3a18-256">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-256">False</span></span>                                                     |
| <span data-ttu-id="b3a18-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b3a18-257">In Global Catalog</span></span>      | <span data-ttu-id="b3a18-258">False</span><span class="sxs-lookup"><span data-stu-id="b3a18-258">False</span></span>                                                     |
| <span data-ttu-id="b3a18-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b3a18-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3a18-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b3a18-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b3a18-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3a18-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b3a18-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3a18-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b3a18-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3a18-263">Search-Flags</span></span>           | <span data-ttu-id="b3a18-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3a18-264">0x00000000</span></span>                                                |
| <span data-ttu-id="b3a18-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3a18-265">System-Flags</span></span>           | <span data-ttu-id="b3a18-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3a18-266">0x00000010</span></span>                                                |
| <span data-ttu-id="b3a18-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b3a18-267">Classes used in</span></span>        | [<span data-ttu-id="b3a18-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="b3a18-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





