---
title: MS-SQL-allowknownpullabonnementattribut
description: True, wenn die Veröffentlichung registrierten Abonnenten das Abonnieren ermöglicht.
ms.assetid: be3b618e-bdf5-4bb4-ac4d-51dc97e73408
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-SQL-allowknownpullabonnementattributs
- AD-Schema des MS-SQL-allowknownpullabonnementattributs
topic_type:
- apiref
api_name:
- MS-SQL-AllowKnownPullSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d07789bf68f470db69219765628ebc82b2014428
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859888"
---
# <a name="ms-sql-allowknownpullsubscription-attribute"></a><span data-ttu-id="362f5-105">MS-SQL-allowknownpullabonnementattribut</span><span class="sxs-lookup"><span data-stu-id="362f5-105">MS-SQL-AllowKnownPullSubscription attribute</span></span>

<span data-ttu-id="362f5-106">True, wenn die Veröffentlichung registrierten Abonnenten das Abonnieren ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="362f5-106">True if the publication allows registered subscribers to subscribe.</span></span>



| <span data-ttu-id="362f5-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="362f5-107">Entry</span></span> | <span data-ttu-id="362f5-108">Wert</span><span class="sxs-lookup"><span data-stu-id="362f5-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="362f5-109">CN</span><span class="sxs-lookup"><span data-stu-id="362f5-109">CN</span></span>                | <span data-ttu-id="362f5-110">MS-SQL-allowknownpullabonnement</span><span class="sxs-lookup"><span data-stu-id="362f5-110">MS-SQL-AllowKnownPullSubscription</span></span>    |
| <span data-ttu-id="362f5-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="362f5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="362f5-112">MS-SQL-allowknownpullabonnement</span><span class="sxs-lookup"><span data-stu-id="362f5-112">mS-SQL-AllowKnownPullSubscription</span></span>    |
| <span data-ttu-id="362f5-113">Size</span><span class="sxs-lookup"><span data-stu-id="362f5-113">Size</span></span>              | <span data-ttu-id="362f5-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="362f5-114">4 bytes</span></span>                              |
| <span data-ttu-id="362f5-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="362f5-115">Update Privilege</span></span>  | <span data-ttu-id="362f5-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="362f5-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="362f5-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="362f5-117">Update Frequency</span></span>  | <span data-ttu-id="362f5-118">Wenn die Replikation eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="362f5-118">When replication is setup.</span></span>           |
| <span data-ttu-id="362f5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="362f5-119">Attribute-Id</span></span>      | <span data-ttu-id="362f5-120">1.2.840.113556.1.4.1403</span><span class="sxs-lookup"><span data-stu-id="362f5-120">1.2.840.113556.1.4.1403</span></span>              |
| <span data-ttu-id="362f5-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="362f5-121">System-Id-Guid</span></span>    | <span data-ttu-id="362f5-122">c3bb7054-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="362f5-122">c3bb7054-d34b-11d2-999a-0000f87a57d4</span></span> |
| <span data-ttu-id="362f5-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="362f5-123">Syntax</span></span>            | [<span data-ttu-id="362f5-124">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="362f5-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="362f5-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="362f5-125">Implementations</span></span>

-   [<span data-ttu-id="362f5-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="362f5-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="362f5-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="362f5-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="362f5-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="362f5-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="362f5-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="362f5-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="362f5-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="362f5-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="362f5-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="362f5-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="362f5-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="362f5-132">Windows 2000 Server</span></span>



| <span data-ttu-id="362f5-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="362f5-133">Entry</span></span> | <span data-ttu-id="362f5-134">Wert</span><span class="sxs-lookup"><span data-stu-id="362f5-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="362f5-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="362f5-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="362f5-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="362f5-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="362f5-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="362f5-137">System-Only</span></span>            | <span data-ttu-id="362f5-138">False</span><span class="sxs-lookup"><span data-stu-id="362f5-138">False</span></span>                                                               |
| <span data-ttu-id="362f5-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="362f5-139">Is-Single-Valued</span></span>       | <span data-ttu-id="362f5-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="362f5-140">True</span></span>                                                                |
| <span data-ttu-id="362f5-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="362f5-141">Is Indexed</span></span>             | <span data-ttu-id="362f5-142">False</span><span class="sxs-lookup"><span data-stu-id="362f5-142">False</span></span>                                                               |
| <span data-ttu-id="362f5-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="362f5-143">In Global Catalog</span></span>      | <span data-ttu-id="362f5-144">False</span><span class="sxs-lookup"><span data-stu-id="362f5-144">False</span></span>                                                               |
| <span data-ttu-id="362f5-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="362f5-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="362f5-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="362f5-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="362f5-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="362f5-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="362f5-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="362f5-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="362f5-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="362f5-149">Search-Flags</span></span>           | <span data-ttu-id="362f5-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="362f5-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="362f5-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="362f5-151">System-Flags</span></span>           | <span data-ttu-id="362f5-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="362f5-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="362f5-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="362f5-153">Classes used in</span></span>        | [<span data-ttu-id="362f5-154">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="362f5-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="362f5-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="362f5-155">Windows Server 2003</span></span>



| <span data-ttu-id="362f5-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="362f5-156">Entry</span></span> | <span data-ttu-id="362f5-157">Wert</span><span class="sxs-lookup"><span data-stu-id="362f5-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="362f5-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="362f5-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="362f5-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="362f5-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="362f5-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="362f5-160">System-Only</span></span>            | <span data-ttu-id="362f5-161">False</span><span class="sxs-lookup"><span data-stu-id="362f5-161">False</span></span>                                                               |
| <span data-ttu-id="362f5-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="362f5-162">Is-Single-Valued</span></span>       | <span data-ttu-id="362f5-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="362f5-163">True</span></span>                                                                |
| <span data-ttu-id="362f5-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="362f5-164">Is Indexed</span></span>             | <span data-ttu-id="362f5-165">False</span><span class="sxs-lookup"><span data-stu-id="362f5-165">False</span></span>                                                               |
| <span data-ttu-id="362f5-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="362f5-166">In Global Catalog</span></span>      | <span data-ttu-id="362f5-167">False</span><span class="sxs-lookup"><span data-stu-id="362f5-167">False</span></span>                                                               |
| <span data-ttu-id="362f5-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="362f5-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="362f5-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="362f5-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="362f5-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="362f5-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="362f5-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="362f5-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="362f5-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="362f5-172">Search-Flags</span></span>           | <span data-ttu-id="362f5-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="362f5-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="362f5-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="362f5-174">System-Flags</span></span>           | <span data-ttu-id="362f5-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="362f5-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="362f5-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="362f5-176">Classes used in</span></span>        | [<span data-ttu-id="362f5-177">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="362f5-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="362f5-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="362f5-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="362f5-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="362f5-179">Entry</span></span> | <span data-ttu-id="362f5-180">Wert</span><span class="sxs-lookup"><span data-stu-id="362f5-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="362f5-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="362f5-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="362f5-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="362f5-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="362f5-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="362f5-183">System-Only</span></span>            | <span data-ttu-id="362f5-184">False</span><span class="sxs-lookup"><span data-stu-id="362f5-184">False</span></span>                                                               |
| <span data-ttu-id="362f5-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="362f5-185">Is-Single-Valued</span></span>       | <span data-ttu-id="362f5-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="362f5-186">True</span></span>                                                                |
| <span data-ttu-id="362f5-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="362f5-187">Is Indexed</span></span>             | <span data-ttu-id="362f5-188">False</span><span class="sxs-lookup"><span data-stu-id="362f5-188">False</span></span>                                                               |
| <span data-ttu-id="362f5-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="362f5-189">In Global Catalog</span></span>      | <span data-ttu-id="362f5-190">False</span><span class="sxs-lookup"><span data-stu-id="362f5-190">False</span></span>                                                               |
| <span data-ttu-id="362f5-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="362f5-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="362f5-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="362f5-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="362f5-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="362f5-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="362f5-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="362f5-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="362f5-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="362f5-195">Search-Flags</span></span>           | <span data-ttu-id="362f5-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="362f5-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="362f5-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="362f5-197">System-Flags</span></span>           | <span data-ttu-id="362f5-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="362f5-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="362f5-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="362f5-199">Classes used in</span></span>        | [<span data-ttu-id="362f5-200">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="362f5-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="362f5-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="362f5-201">Windows Server 2008</span></span>



| <span data-ttu-id="362f5-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="362f5-202">Entry</span></span> | <span data-ttu-id="362f5-203">Wert</span><span class="sxs-lookup"><span data-stu-id="362f5-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="362f5-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="362f5-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="362f5-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="362f5-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="362f5-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="362f5-206">System-Only</span></span>            | <span data-ttu-id="362f5-207">False</span><span class="sxs-lookup"><span data-stu-id="362f5-207">False</span></span>                                                               |
| <span data-ttu-id="362f5-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="362f5-208">Is-Single-Valued</span></span>       | <span data-ttu-id="362f5-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="362f5-209">True</span></span>                                                                |
| <span data-ttu-id="362f5-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="362f5-210">Is Indexed</span></span>             | <span data-ttu-id="362f5-211">False</span><span class="sxs-lookup"><span data-stu-id="362f5-211">False</span></span>                                                               |
| <span data-ttu-id="362f5-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="362f5-212">In Global Catalog</span></span>      | <span data-ttu-id="362f5-213">False</span><span class="sxs-lookup"><span data-stu-id="362f5-213">False</span></span>                                                               |
| <span data-ttu-id="362f5-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="362f5-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="362f5-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="362f5-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="362f5-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="362f5-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="362f5-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="362f5-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="362f5-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="362f5-218">Search-Flags</span></span>           | <span data-ttu-id="362f5-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="362f5-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="362f5-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="362f5-220">System-Flags</span></span>           | <span data-ttu-id="362f5-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="362f5-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="362f5-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="362f5-222">Classes used in</span></span>        | [<span data-ttu-id="362f5-223">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="362f5-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="362f5-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="362f5-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="362f5-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="362f5-225">Entry</span></span> | <span data-ttu-id="362f5-226">Wert</span><span class="sxs-lookup"><span data-stu-id="362f5-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="362f5-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="362f5-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="362f5-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="362f5-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="362f5-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="362f5-229">System-Only</span></span>            | <span data-ttu-id="362f5-230">False</span><span class="sxs-lookup"><span data-stu-id="362f5-230">False</span></span>                                                               |
| <span data-ttu-id="362f5-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="362f5-231">Is-Single-Valued</span></span>       | <span data-ttu-id="362f5-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="362f5-232">True</span></span>                                                                |
| <span data-ttu-id="362f5-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="362f5-233">Is Indexed</span></span>             | <span data-ttu-id="362f5-234">False</span><span class="sxs-lookup"><span data-stu-id="362f5-234">False</span></span>                                                               |
| <span data-ttu-id="362f5-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="362f5-235">In Global Catalog</span></span>      | <span data-ttu-id="362f5-236">False</span><span class="sxs-lookup"><span data-stu-id="362f5-236">False</span></span>                                                               |
| <span data-ttu-id="362f5-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="362f5-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="362f5-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="362f5-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="362f5-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="362f5-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="362f5-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="362f5-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="362f5-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="362f5-241">Search-Flags</span></span>           | <span data-ttu-id="362f5-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="362f5-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="362f5-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="362f5-243">System-Flags</span></span>           | <span data-ttu-id="362f5-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="362f5-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="362f5-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="362f5-245">Classes used in</span></span>        | [<span data-ttu-id="362f5-246">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="362f5-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="362f5-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="362f5-247">Windows Server 2012</span></span>



| <span data-ttu-id="362f5-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="362f5-248">Entry</span></span> | <span data-ttu-id="362f5-249">Wert</span><span class="sxs-lookup"><span data-stu-id="362f5-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="362f5-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="362f5-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="362f5-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="362f5-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="362f5-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="362f5-252">System-Only</span></span>            | <span data-ttu-id="362f5-253">False</span><span class="sxs-lookup"><span data-stu-id="362f5-253">False</span></span>                                                               |
| <span data-ttu-id="362f5-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="362f5-254">Is-Single-Valued</span></span>       | <span data-ttu-id="362f5-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="362f5-255">True</span></span>                                                                |
| <span data-ttu-id="362f5-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="362f5-256">Is Indexed</span></span>             | <span data-ttu-id="362f5-257">False</span><span class="sxs-lookup"><span data-stu-id="362f5-257">False</span></span>                                                               |
| <span data-ttu-id="362f5-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="362f5-258">In Global Catalog</span></span>      | <span data-ttu-id="362f5-259">False</span><span class="sxs-lookup"><span data-stu-id="362f5-259">False</span></span>                                                               |
| <span data-ttu-id="362f5-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="362f5-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="362f5-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="362f5-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="362f5-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="362f5-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="362f5-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="362f5-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="362f5-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="362f5-264">Search-Flags</span></span>           | <span data-ttu-id="362f5-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="362f5-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="362f5-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="362f5-266">System-Flags</span></span>           | <span data-ttu-id="362f5-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="362f5-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="362f5-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="362f5-268">Classes used in</span></span>        | [<span data-ttu-id="362f5-269">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="362f5-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





