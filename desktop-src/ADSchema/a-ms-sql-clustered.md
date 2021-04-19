---
title: MS-SQL-CLUSTERED-Attribut
description: True, wenn der Server gruppiert ist.
ms.assetid: 066609a4-fdf1-422b-9b26-445f617c99d4
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-SQL-CLUSTERED-Attribut
- AD-Schema für MS-SQL-CLUSTERED-Attribut
topic_type:
- apiref
api_name:
- MS-SQL-Clustered
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4ba701168f3dff5b3809818a6df987855a08e3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342690"
---
# <a name="ms-sql-clustered-attribute"></a><span data-ttu-id="a2c59-105">MS-SQL-CLUSTERED-Attribut</span><span class="sxs-lookup"><span data-stu-id="a2c59-105">MS-SQL-Clustered attribute</span></span>

<span data-ttu-id="a2c59-106">True, wenn der Server gruppiert ist.</span><span class="sxs-lookup"><span data-stu-id="a2c59-106">True if the server is clustered.</span></span>



| <span data-ttu-id="a2c59-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a2c59-107">Entry</span></span> | <span data-ttu-id="a2c59-108">Wert</span><span class="sxs-lookup"><span data-stu-id="a2c59-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a2c59-109">CN</span><span class="sxs-lookup"><span data-stu-id="a2c59-109">CN</span></span>                | <span data-ttu-id="a2c59-110">MS-SQL-gruppiert</span><span class="sxs-lookup"><span data-stu-id="a2c59-110">MS-SQL-Clustered</span></span>                     |
| <span data-ttu-id="a2c59-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a2c59-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a2c59-112">MS-SQL-gruppiert</span><span class="sxs-lookup"><span data-stu-id="a2c59-112">mS-SQL-Clustered</span></span>                     |
| <span data-ttu-id="a2c59-113">Size</span><span class="sxs-lookup"><span data-stu-id="a2c59-113">Size</span></span>              | <span data-ttu-id="a2c59-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="a2c59-114">4 bytes</span></span>                              |
| <span data-ttu-id="a2c59-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a2c59-115">Update Privilege</span></span>  | <span data-ttu-id="a2c59-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a2c59-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="a2c59-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="a2c59-117">Update Frequency</span></span>  | <span data-ttu-id="a2c59-118">Beim Systemstart.</span><span class="sxs-lookup"><span data-stu-id="a2c59-118">At system startup.</span></span>                   |
| <span data-ttu-id="a2c59-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a2c59-119">Attribute-Id</span></span>      | <span data-ttu-id="a2c59-120">1.2.840.113556.1.4.1373</span><span class="sxs-lookup"><span data-stu-id="a2c59-120">1.2.840.113556.1.4.1373</span></span>              |
| <span data-ttu-id="a2c59-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a2c59-121">System-Id-Guid</span></span>    | <span data-ttu-id="a2c59-122">7778bd90ccee-11d2-9993-0000f 87a57d4</span><span class="sxs-lookup"><span data-stu-id="a2c59-122">7778bd90-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="a2c59-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2c59-123">Syntax</span></span>            | [<span data-ttu-id="a2c59-124">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="a2c59-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="a2c59-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="a2c59-125">Implementations</span></span>

-   [<span data-ttu-id="a2c59-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a2c59-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a2c59-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a2c59-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a2c59-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a2c59-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a2c59-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a2c59-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a2c59-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a2c59-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a2c59-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a2c59-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a2c59-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a2c59-132">Windows 2000 Server</span></span>



| <span data-ttu-id="a2c59-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a2c59-133">Entry</span></span> | <span data-ttu-id="a2c59-134">Wert</span><span class="sxs-lookup"><span data-stu-id="a2c59-134">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a2c59-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a2c59-135">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a2c59-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2c59-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a2c59-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2c59-137">System-Only</span></span>            | <span data-ttu-id="a2c59-138">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-138">False</span></span>                                                     |
| <span data-ttu-id="a2c59-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a2c59-139">Is-Single-Valued</span></span>       | <span data-ttu-id="a2c59-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="a2c59-140">True</span></span>                                                      |
| <span data-ttu-id="a2c59-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a2c59-141">Is Indexed</span></span>             | <span data-ttu-id="a2c59-142">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-142">False</span></span>                                                     |
| <span data-ttu-id="a2c59-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a2c59-143">In Global Catalog</span></span>      | <span data-ttu-id="a2c59-144">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-144">False</span></span>                                                     |
| <span data-ttu-id="a2c59-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2c59-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2c59-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a2c59-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a2c59-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2c59-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a2c59-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2c59-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a2c59-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c59-149">Search-Flags</span></span>           | <span data-ttu-id="a2c59-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2c59-150">0x00000000</span></span>                                                |
| <span data-ttu-id="a2c59-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c59-151">System-Flags</span></span>           | <span data-ttu-id="a2c59-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2c59-152">0x00000010</span></span>                                                |
| <span data-ttu-id="a2c59-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a2c59-153">Classes used in</span></span>        | [<span data-ttu-id="a2c59-154">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a2c59-154">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a2c59-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a2c59-155">Windows Server 2003</span></span>



| <span data-ttu-id="a2c59-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a2c59-156">Entry</span></span> | <span data-ttu-id="a2c59-157">Wert</span><span class="sxs-lookup"><span data-stu-id="a2c59-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a2c59-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a2c59-158">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a2c59-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2c59-159">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a2c59-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2c59-160">System-Only</span></span>            | <span data-ttu-id="a2c59-161">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-161">False</span></span>                                                     |
| <span data-ttu-id="a2c59-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a2c59-162">Is-Single-Valued</span></span>       | <span data-ttu-id="a2c59-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="a2c59-163">True</span></span>                                                      |
| <span data-ttu-id="a2c59-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a2c59-164">Is Indexed</span></span>             | <span data-ttu-id="a2c59-165">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-165">False</span></span>                                                     |
| <span data-ttu-id="a2c59-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a2c59-166">In Global Catalog</span></span>      | <span data-ttu-id="a2c59-167">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-167">False</span></span>                                                     |
| <span data-ttu-id="a2c59-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2c59-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2c59-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a2c59-169">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a2c59-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2c59-170">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a2c59-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2c59-171">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a2c59-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c59-172">Search-Flags</span></span>           | <span data-ttu-id="a2c59-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2c59-173">0x00000000</span></span>                                                |
| <span data-ttu-id="a2c59-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c59-174">System-Flags</span></span>           | <span data-ttu-id="a2c59-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2c59-175">0x00000010</span></span>                                                |
| <span data-ttu-id="a2c59-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a2c59-176">Classes used in</span></span>        | [<span data-ttu-id="a2c59-177">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a2c59-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a2c59-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a2c59-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a2c59-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a2c59-179">Entry</span></span> | <span data-ttu-id="a2c59-180">Wert</span><span class="sxs-lookup"><span data-stu-id="a2c59-180">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a2c59-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a2c59-181">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a2c59-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2c59-182">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a2c59-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2c59-183">System-Only</span></span>            | <span data-ttu-id="a2c59-184">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-184">False</span></span>                                                     |
| <span data-ttu-id="a2c59-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a2c59-185">Is-Single-Valued</span></span>       | <span data-ttu-id="a2c59-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="a2c59-186">True</span></span>                                                      |
| <span data-ttu-id="a2c59-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a2c59-187">Is Indexed</span></span>             | <span data-ttu-id="a2c59-188">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-188">False</span></span>                                                     |
| <span data-ttu-id="a2c59-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a2c59-189">In Global Catalog</span></span>      | <span data-ttu-id="a2c59-190">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-190">False</span></span>                                                     |
| <span data-ttu-id="a2c59-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2c59-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2c59-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a2c59-192">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a2c59-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2c59-193">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a2c59-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2c59-194">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a2c59-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c59-195">Search-Flags</span></span>           | <span data-ttu-id="a2c59-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2c59-196">0x00000000</span></span>                                                |
| <span data-ttu-id="a2c59-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c59-197">System-Flags</span></span>           | <span data-ttu-id="a2c59-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2c59-198">0x00000010</span></span>                                                |
| <span data-ttu-id="a2c59-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a2c59-199">Classes used in</span></span>        | [<span data-ttu-id="a2c59-200">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a2c59-200">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a2c59-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2c59-201">Windows Server 2008</span></span>



| <span data-ttu-id="a2c59-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a2c59-202">Entry</span></span> | <span data-ttu-id="a2c59-203">Wert</span><span class="sxs-lookup"><span data-stu-id="a2c59-203">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a2c59-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a2c59-204">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a2c59-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2c59-205">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a2c59-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2c59-206">System-Only</span></span>            | <span data-ttu-id="a2c59-207">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-207">False</span></span>                                                     |
| <span data-ttu-id="a2c59-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a2c59-208">Is-Single-Valued</span></span>       | <span data-ttu-id="a2c59-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="a2c59-209">True</span></span>                                                      |
| <span data-ttu-id="a2c59-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a2c59-210">Is Indexed</span></span>             | <span data-ttu-id="a2c59-211">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-211">False</span></span>                                                     |
| <span data-ttu-id="a2c59-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a2c59-212">In Global Catalog</span></span>      | <span data-ttu-id="a2c59-213">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-213">False</span></span>                                                     |
| <span data-ttu-id="a2c59-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2c59-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2c59-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a2c59-215">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a2c59-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2c59-216">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a2c59-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2c59-217">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a2c59-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c59-218">Search-Flags</span></span>           | <span data-ttu-id="a2c59-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2c59-219">0x00000000</span></span>                                                |
| <span data-ttu-id="a2c59-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c59-220">System-Flags</span></span>           | <span data-ttu-id="a2c59-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2c59-221">0x00000010</span></span>                                                |
| <span data-ttu-id="a2c59-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a2c59-222">Classes used in</span></span>        | [<span data-ttu-id="a2c59-223">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a2c59-223">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a2c59-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a2c59-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a2c59-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a2c59-225">Entry</span></span> | <span data-ttu-id="a2c59-226">Wert</span><span class="sxs-lookup"><span data-stu-id="a2c59-226">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a2c59-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a2c59-227">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a2c59-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2c59-228">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a2c59-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2c59-229">System-Only</span></span>            | <span data-ttu-id="a2c59-230">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-230">False</span></span>                                                     |
| <span data-ttu-id="a2c59-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a2c59-231">Is-Single-Valued</span></span>       | <span data-ttu-id="a2c59-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="a2c59-232">True</span></span>                                                      |
| <span data-ttu-id="a2c59-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a2c59-233">Is Indexed</span></span>             | <span data-ttu-id="a2c59-234">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-234">False</span></span>                                                     |
| <span data-ttu-id="a2c59-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a2c59-235">In Global Catalog</span></span>      | <span data-ttu-id="a2c59-236">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-236">False</span></span>                                                     |
| <span data-ttu-id="a2c59-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2c59-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2c59-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a2c59-238">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a2c59-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2c59-239">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a2c59-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2c59-240">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a2c59-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c59-241">Search-Flags</span></span>           | <span data-ttu-id="a2c59-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2c59-242">0x00000000</span></span>                                                |
| <span data-ttu-id="a2c59-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c59-243">System-Flags</span></span>           | <span data-ttu-id="a2c59-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2c59-244">0x00000010</span></span>                                                |
| <span data-ttu-id="a2c59-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a2c59-245">Classes used in</span></span>        | [<span data-ttu-id="a2c59-246">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a2c59-246">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a2c59-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2c59-247">Windows Server 2012</span></span>



| <span data-ttu-id="a2c59-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a2c59-248">Entry</span></span> | <span data-ttu-id="a2c59-249">Wert</span><span class="sxs-lookup"><span data-stu-id="a2c59-249">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a2c59-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a2c59-250">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a2c59-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2c59-251">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a2c59-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2c59-252">System-Only</span></span>            | <span data-ttu-id="a2c59-253">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-253">False</span></span>                                                     |
| <span data-ttu-id="a2c59-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a2c59-254">Is-Single-Valued</span></span>       | <span data-ttu-id="a2c59-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="a2c59-255">True</span></span>                                                      |
| <span data-ttu-id="a2c59-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a2c59-256">Is Indexed</span></span>             | <span data-ttu-id="a2c59-257">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-257">False</span></span>                                                     |
| <span data-ttu-id="a2c59-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a2c59-258">In Global Catalog</span></span>      | <span data-ttu-id="a2c59-259">False</span><span class="sxs-lookup"><span data-stu-id="a2c59-259">False</span></span>                                                     |
| <span data-ttu-id="a2c59-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2c59-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2c59-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a2c59-261">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a2c59-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2c59-262">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a2c59-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2c59-263">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a2c59-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c59-264">Search-Flags</span></span>           | <span data-ttu-id="a2c59-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2c59-265">0x00000000</span></span>                                                |
| <span data-ttu-id="a2c59-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2c59-266">System-Flags</span></span>           | <span data-ttu-id="a2c59-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2c59-267">0x00000010</span></span>                                                |
| <span data-ttu-id="a2c59-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a2c59-268">Classes used in</span></span>        | [<span data-ttu-id="a2c59-269">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a2c59-269">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





