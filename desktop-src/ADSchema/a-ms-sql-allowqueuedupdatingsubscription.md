---
title: MS-SQL-allowqueuedupdatingabonnement-Attribut
description: True, um Transaktionen in der Warteschlange zuzulassen, wenn Abonnements aktualisiert werden.
ms.assetid: 132c107f-8586-48db-b70c-027c619aadf7
ms.tgt_platform: multiple
keywords:
- "\"MS-SQL-allowqueuedupdatingabonnement\"-Attribut, AD-Schema"
- "\"MS-SQL-allowqueuedupdatingabonnement\"-Attribut, AD-Schema"
topic_type:
- apiref
api_name:
- MS-SQL-AllowQueuedUpdatingSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2056a04b6e0f155c156cde06975e96eb13f61eb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859462"
---
# <a name="ms-sql-allowqueuedupdatingsubscription-attribute"></a><span data-ttu-id="03e15-105">MS-SQL-allowqueuedupdatingabonnement-Attribut</span><span class="sxs-lookup"><span data-stu-id="03e15-105">MS-SQL-AllowQueuedUpdatingSubscription attribute</span></span>

<span data-ttu-id="03e15-106">True, um Transaktionen in der Warteschlange zuzulassen, wenn Abonnements aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="03e15-106">True to allow queued transactions when updating subscriptions.</span></span>



| <span data-ttu-id="03e15-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="03e15-107">Entry</span></span> | <span data-ttu-id="03e15-108">Wert</span><span class="sxs-lookup"><span data-stu-id="03e15-108">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="03e15-109">CN</span><span class="sxs-lookup"><span data-stu-id="03e15-109">CN</span></span>                | <span data-ttu-id="03e15-110">MS-SQL-allowqueuedupdatingabonnement</span><span class="sxs-lookup"><span data-stu-id="03e15-110">MS-SQL-AllowQueuedUpdatingSubscription</span></span> |
| <span data-ttu-id="03e15-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="03e15-111">Ldap-Display-Name</span></span> | <span data-ttu-id="03e15-112">MS-SQL-allowqueuedupdatingabonnement</span><span class="sxs-lookup"><span data-stu-id="03e15-112">mS-SQL-AllowQueuedUpdatingSubscription</span></span> |
| <span data-ttu-id="03e15-113">Size</span><span class="sxs-lookup"><span data-stu-id="03e15-113">Size</span></span>              | <span data-ttu-id="03e15-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="03e15-114">4 bytes</span></span>                                |
| <span data-ttu-id="03e15-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="03e15-115">Update Privilege</span></span>  | <span data-ttu-id="03e15-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="03e15-116">This value is set by the system.</span></span>       |
| <span data-ttu-id="03e15-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="03e15-117">Update Frequency</span></span>  | <span data-ttu-id="03e15-118">Wenn die Replikation eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="03e15-118">When replication is setup.</span></span>             |
| <span data-ttu-id="03e15-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="03e15-119">Attribute-Id</span></span>      | <span data-ttu-id="03e15-120">1.2.840.113556.1.4.1405</span><span class="sxs-lookup"><span data-stu-id="03e15-120">1.2.840.113556.1.4.1405</span></span>                |
| <span data-ttu-id="03e15-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="03e15-121">System-Id-Guid</span></span>    | <span data-ttu-id="03e15-122">c458ca80-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="03e15-122">c458ca80-d34b-11d2-999a-0000f87a57d4</span></span>   |
| <span data-ttu-id="03e15-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="03e15-123">Syntax</span></span>            | [<span data-ttu-id="03e15-124">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="03e15-124">**Boolean**</span></span>](s-boolean.md)           |



## <a name="implementations"></a><span data-ttu-id="03e15-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="03e15-125">Implementations</span></span>

-   [<span data-ttu-id="03e15-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="03e15-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="03e15-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="03e15-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="03e15-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="03e15-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="03e15-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="03e15-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="03e15-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="03e15-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="03e15-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="03e15-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="03e15-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="03e15-132">Windows 2000 Server</span></span>



| <span data-ttu-id="03e15-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="03e15-133">Entry</span></span> | <span data-ttu-id="03e15-134">Wert</span><span class="sxs-lookup"><span data-stu-id="03e15-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="03e15-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="03e15-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03e15-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03e15-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03e15-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="03e15-137">System-Only</span></span>            | <span data-ttu-id="03e15-138">False</span><span class="sxs-lookup"><span data-stu-id="03e15-138">False</span></span>                                                               |
| <span data-ttu-id="03e15-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="03e15-139">Is-Single-Valued</span></span>       | <span data-ttu-id="03e15-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="03e15-140">True</span></span>                                                                |
| <span data-ttu-id="03e15-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="03e15-141">Is Indexed</span></span>             | <span data-ttu-id="03e15-142">False</span><span class="sxs-lookup"><span data-stu-id="03e15-142">False</span></span>                                                               |
| <span data-ttu-id="03e15-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="03e15-143">In Global Catalog</span></span>      | <span data-ttu-id="03e15-144">False</span><span class="sxs-lookup"><span data-stu-id="03e15-144">False</span></span>                                                               |
| <span data-ttu-id="03e15-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="03e15-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="03e15-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="03e15-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="03e15-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03e15-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="03e15-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03e15-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="03e15-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03e15-149">Search-Flags</span></span>           | <span data-ttu-id="03e15-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03e15-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="03e15-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03e15-151">System-Flags</span></span>           | <span data-ttu-id="03e15-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03e15-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="03e15-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="03e15-153">Classes used in</span></span>        | [<span data-ttu-id="03e15-154">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="03e15-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="03e15-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="03e15-155">Windows Server 2003</span></span>



| <span data-ttu-id="03e15-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="03e15-156">Entry</span></span> | <span data-ttu-id="03e15-157">Wert</span><span class="sxs-lookup"><span data-stu-id="03e15-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="03e15-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="03e15-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03e15-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03e15-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03e15-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="03e15-160">System-Only</span></span>            | <span data-ttu-id="03e15-161">False</span><span class="sxs-lookup"><span data-stu-id="03e15-161">False</span></span>                                                               |
| <span data-ttu-id="03e15-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="03e15-162">Is-Single-Valued</span></span>       | <span data-ttu-id="03e15-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="03e15-163">True</span></span>                                                                |
| <span data-ttu-id="03e15-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="03e15-164">Is Indexed</span></span>             | <span data-ttu-id="03e15-165">False</span><span class="sxs-lookup"><span data-stu-id="03e15-165">False</span></span>                                                               |
| <span data-ttu-id="03e15-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="03e15-166">In Global Catalog</span></span>      | <span data-ttu-id="03e15-167">False</span><span class="sxs-lookup"><span data-stu-id="03e15-167">False</span></span>                                                               |
| <span data-ttu-id="03e15-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="03e15-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="03e15-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="03e15-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="03e15-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03e15-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="03e15-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03e15-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="03e15-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03e15-172">Search-Flags</span></span>           | <span data-ttu-id="03e15-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03e15-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="03e15-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03e15-174">System-Flags</span></span>           | <span data-ttu-id="03e15-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03e15-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="03e15-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="03e15-176">Classes used in</span></span>        | [<span data-ttu-id="03e15-177">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="03e15-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="03e15-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="03e15-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="03e15-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="03e15-179">Entry</span></span> | <span data-ttu-id="03e15-180">Wert</span><span class="sxs-lookup"><span data-stu-id="03e15-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="03e15-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="03e15-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03e15-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03e15-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03e15-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="03e15-183">System-Only</span></span>            | <span data-ttu-id="03e15-184">False</span><span class="sxs-lookup"><span data-stu-id="03e15-184">False</span></span>                                                               |
| <span data-ttu-id="03e15-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="03e15-185">Is-Single-Valued</span></span>       | <span data-ttu-id="03e15-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="03e15-186">True</span></span>                                                                |
| <span data-ttu-id="03e15-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="03e15-187">Is Indexed</span></span>             | <span data-ttu-id="03e15-188">False</span><span class="sxs-lookup"><span data-stu-id="03e15-188">False</span></span>                                                               |
| <span data-ttu-id="03e15-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="03e15-189">In Global Catalog</span></span>      | <span data-ttu-id="03e15-190">False</span><span class="sxs-lookup"><span data-stu-id="03e15-190">False</span></span>                                                               |
| <span data-ttu-id="03e15-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="03e15-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="03e15-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="03e15-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="03e15-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03e15-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="03e15-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03e15-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="03e15-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03e15-195">Search-Flags</span></span>           | <span data-ttu-id="03e15-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03e15-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="03e15-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03e15-197">System-Flags</span></span>           | <span data-ttu-id="03e15-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03e15-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="03e15-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="03e15-199">Classes used in</span></span>        | [<span data-ttu-id="03e15-200">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="03e15-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="03e15-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03e15-201">Windows Server 2008</span></span>



| <span data-ttu-id="03e15-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="03e15-202">Entry</span></span> | <span data-ttu-id="03e15-203">Wert</span><span class="sxs-lookup"><span data-stu-id="03e15-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="03e15-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="03e15-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03e15-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03e15-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03e15-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="03e15-206">System-Only</span></span>            | <span data-ttu-id="03e15-207">False</span><span class="sxs-lookup"><span data-stu-id="03e15-207">False</span></span>                                                               |
| <span data-ttu-id="03e15-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="03e15-208">Is-Single-Valued</span></span>       | <span data-ttu-id="03e15-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="03e15-209">True</span></span>                                                                |
| <span data-ttu-id="03e15-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="03e15-210">Is Indexed</span></span>             | <span data-ttu-id="03e15-211">False</span><span class="sxs-lookup"><span data-stu-id="03e15-211">False</span></span>                                                               |
| <span data-ttu-id="03e15-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="03e15-212">In Global Catalog</span></span>      | <span data-ttu-id="03e15-213">False</span><span class="sxs-lookup"><span data-stu-id="03e15-213">False</span></span>                                                               |
| <span data-ttu-id="03e15-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="03e15-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="03e15-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="03e15-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="03e15-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03e15-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="03e15-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03e15-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="03e15-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03e15-218">Search-Flags</span></span>           | <span data-ttu-id="03e15-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03e15-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="03e15-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03e15-220">System-Flags</span></span>           | <span data-ttu-id="03e15-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03e15-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="03e15-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="03e15-222">Classes used in</span></span>        | [<span data-ttu-id="03e15-223">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="03e15-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="03e15-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="03e15-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="03e15-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="03e15-225">Entry</span></span> | <span data-ttu-id="03e15-226">Wert</span><span class="sxs-lookup"><span data-stu-id="03e15-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="03e15-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="03e15-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03e15-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03e15-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03e15-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="03e15-229">System-Only</span></span>            | <span data-ttu-id="03e15-230">False</span><span class="sxs-lookup"><span data-stu-id="03e15-230">False</span></span>                                                               |
| <span data-ttu-id="03e15-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="03e15-231">Is-Single-Valued</span></span>       | <span data-ttu-id="03e15-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="03e15-232">True</span></span>                                                                |
| <span data-ttu-id="03e15-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="03e15-233">Is Indexed</span></span>             | <span data-ttu-id="03e15-234">False</span><span class="sxs-lookup"><span data-stu-id="03e15-234">False</span></span>                                                               |
| <span data-ttu-id="03e15-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="03e15-235">In Global Catalog</span></span>      | <span data-ttu-id="03e15-236">False</span><span class="sxs-lookup"><span data-stu-id="03e15-236">False</span></span>                                                               |
| <span data-ttu-id="03e15-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="03e15-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="03e15-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="03e15-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="03e15-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03e15-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="03e15-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03e15-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="03e15-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03e15-241">Search-Flags</span></span>           | <span data-ttu-id="03e15-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03e15-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="03e15-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03e15-243">System-Flags</span></span>           | <span data-ttu-id="03e15-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03e15-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="03e15-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="03e15-245">Classes used in</span></span>        | [<span data-ttu-id="03e15-246">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="03e15-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="03e15-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="03e15-247">Windows Server 2012</span></span>



| <span data-ttu-id="03e15-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="03e15-248">Entry</span></span> | <span data-ttu-id="03e15-249">Wert</span><span class="sxs-lookup"><span data-stu-id="03e15-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="03e15-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="03e15-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03e15-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03e15-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03e15-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="03e15-252">System-Only</span></span>            | <span data-ttu-id="03e15-253">False</span><span class="sxs-lookup"><span data-stu-id="03e15-253">False</span></span>                                                               |
| <span data-ttu-id="03e15-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="03e15-254">Is-Single-Valued</span></span>       | <span data-ttu-id="03e15-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="03e15-255">True</span></span>                                                                |
| <span data-ttu-id="03e15-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="03e15-256">Is Indexed</span></span>             | <span data-ttu-id="03e15-257">False</span><span class="sxs-lookup"><span data-stu-id="03e15-257">False</span></span>                                                               |
| <span data-ttu-id="03e15-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="03e15-258">In Global Catalog</span></span>      | <span data-ttu-id="03e15-259">False</span><span class="sxs-lookup"><span data-stu-id="03e15-259">False</span></span>                                                               |
| <span data-ttu-id="03e15-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="03e15-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="03e15-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="03e15-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="03e15-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03e15-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="03e15-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03e15-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="03e15-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03e15-264">Search-Flags</span></span>           | <span data-ttu-id="03e15-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03e15-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="03e15-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03e15-266">System-Flags</span></span>           | <span data-ttu-id="03e15-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03e15-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="03e15-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="03e15-268">Classes used in</span></span>        | [<span data-ttu-id="03e15-269">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="03e15-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





