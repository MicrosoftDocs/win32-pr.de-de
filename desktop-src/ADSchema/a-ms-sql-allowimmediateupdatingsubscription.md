---
title: MS-SQL-zugswimmediateupdatingabonnement-Attribut
description: True, wenn die Veröffentlichung synchronisierte Abonnements zum Aktualisieren von Transaktionen zulässt.
ms.assetid: 7efa4b8f-77ad-4f68-9852-7dac9f922d95
ms.tgt_platform: multiple
keywords:
- MS-SQL-zugswimmediateupdatingabonnement-Attribut, AD-Schema
- MS-SQL-zugswimmediateupdatingabonnement-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- MS-SQL-AllowImmediateUpdatingSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed7970aa4b4f26a7221ea9a0c3d4e279ddc5db1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519516"
---
# <a name="ms-sql-allowimmediateupdatingsubscription-attribute"></a><span data-ttu-id="db9b5-105">MS-SQL-zugswimmediateupdatingabonnement-Attribut</span><span class="sxs-lookup"><span data-stu-id="db9b5-105">MS-SQL-AllowImmediateUpdatingSubscription attribute</span></span>

<span data-ttu-id="db9b5-106">True, wenn die Veröffentlichung synchronisierte Abonnements zum Aktualisieren von Transaktionen zulässt.</span><span class="sxs-lookup"><span data-stu-id="db9b5-106">True if the publication allows synchronized transaction updating subscriptions.</span></span>



| <span data-ttu-id="db9b5-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db9b5-107">Entry</span></span> | <span data-ttu-id="db9b5-108">Wert</span><span class="sxs-lookup"><span data-stu-id="db9b5-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="db9b5-109">CN</span><span class="sxs-lookup"><span data-stu-id="db9b5-109">CN</span></span>                | <span data-ttu-id="db9b5-110">MS-SQL-zugswimmediateupdatingabonnement</span><span class="sxs-lookup"><span data-stu-id="db9b5-110">MS-SQL-AllowImmediateUpdatingSubscription</span></span> |
| <span data-ttu-id="db9b5-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="db9b5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="db9b5-112">MS-SQL-zugswimmediateupdatingabonnement</span><span class="sxs-lookup"><span data-stu-id="db9b5-112">mS-SQL-AllowImmediateUpdatingSubscription</span></span> |
| <span data-ttu-id="db9b5-113">Size</span><span class="sxs-lookup"><span data-stu-id="db9b5-113">Size</span></span>              | <span data-ttu-id="db9b5-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="db9b5-114">4 bytes</span></span>                                   |
| <span data-ttu-id="db9b5-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="db9b5-115">Update Privilege</span></span>  | <span data-ttu-id="db9b5-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="db9b5-116">This value is set by the system.</span></span>          |
| <span data-ttu-id="db9b5-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="db9b5-117">Update Frequency</span></span>  | <span data-ttu-id="db9b5-118">Wenn die Replikation eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="db9b5-118">When replication is setup.</span></span>                |
| <span data-ttu-id="db9b5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="db9b5-119">Attribute-Id</span></span>      | <span data-ttu-id="db9b5-120">1.2.840.113556.1.4.1404</span><span class="sxs-lookup"><span data-stu-id="db9b5-120">1.2.840.113556.1.4.1404</span></span>                   |
| <span data-ttu-id="db9b5-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="db9b5-121">System-Id-Guid</span></span>    | <span data-ttu-id="db9b5-122">c4186b6e-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="db9b5-122">c4186b6e-d34b-11d2-999a-0000f87a57d4</span></span>      |
| <span data-ttu-id="db9b5-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="db9b5-123">Syntax</span></span>            | [<span data-ttu-id="db9b5-124">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="db9b5-124">**Boolean**</span></span>](s-boolean.md)              |



## <a name="implementations"></a><span data-ttu-id="db9b5-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="db9b5-125">Implementations</span></span>

-   [<span data-ttu-id="db9b5-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="db9b5-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="db9b5-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="db9b5-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="db9b5-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="db9b5-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="db9b5-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="db9b5-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="db9b5-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="db9b5-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="db9b5-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="db9b5-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="db9b5-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="db9b5-132">Windows 2000 Server</span></span>



| <span data-ttu-id="db9b5-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db9b5-133">Entry</span></span> | <span data-ttu-id="db9b5-134">Wert</span><span class="sxs-lookup"><span data-stu-id="db9b5-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="db9b5-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db9b5-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="db9b5-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db9b5-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="db9b5-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="db9b5-137">System-Only</span></span>            | <span data-ttu-id="db9b5-138">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-138">False</span></span>                                                               |
| <span data-ttu-id="db9b5-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db9b5-139">Is-Single-Valued</span></span>       | <span data-ttu-id="db9b5-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="db9b5-140">True</span></span>                                                                |
| <span data-ttu-id="db9b5-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db9b5-141">Is Indexed</span></span>             | <span data-ttu-id="db9b5-142">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-142">False</span></span>                                                               |
| <span data-ttu-id="db9b5-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db9b5-143">In Global Catalog</span></span>      | <span data-ttu-id="db9b5-144">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-144">False</span></span>                                                               |
| <span data-ttu-id="db9b5-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db9b5-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="db9b5-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db9b5-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="db9b5-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db9b5-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="db9b5-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db9b5-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="db9b5-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db9b5-149">Search-Flags</span></span>           | <span data-ttu-id="db9b5-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db9b5-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="db9b5-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db9b5-151">System-Flags</span></span>           | <span data-ttu-id="db9b5-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db9b5-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="db9b5-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db9b5-153">Classes used in</span></span>        | [<span data-ttu-id="db9b5-154">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="db9b5-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="db9b5-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="db9b5-155">Windows Server 2003</span></span>



| <span data-ttu-id="db9b5-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db9b5-156">Entry</span></span> | <span data-ttu-id="db9b5-157">Wert</span><span class="sxs-lookup"><span data-stu-id="db9b5-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="db9b5-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db9b5-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="db9b5-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db9b5-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="db9b5-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="db9b5-160">System-Only</span></span>            | <span data-ttu-id="db9b5-161">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-161">False</span></span>                                                               |
| <span data-ttu-id="db9b5-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db9b5-162">Is-Single-Valued</span></span>       | <span data-ttu-id="db9b5-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="db9b5-163">True</span></span>                                                                |
| <span data-ttu-id="db9b5-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db9b5-164">Is Indexed</span></span>             | <span data-ttu-id="db9b5-165">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-165">False</span></span>                                                               |
| <span data-ttu-id="db9b5-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db9b5-166">In Global Catalog</span></span>      | <span data-ttu-id="db9b5-167">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-167">False</span></span>                                                               |
| <span data-ttu-id="db9b5-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db9b5-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="db9b5-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db9b5-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="db9b5-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db9b5-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="db9b5-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db9b5-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="db9b5-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db9b5-172">Search-Flags</span></span>           | <span data-ttu-id="db9b5-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db9b5-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="db9b5-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db9b5-174">System-Flags</span></span>           | <span data-ttu-id="db9b5-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db9b5-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="db9b5-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db9b5-176">Classes used in</span></span>        | [<span data-ttu-id="db9b5-177">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="db9b5-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="db9b5-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="db9b5-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="db9b5-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db9b5-179">Entry</span></span> | <span data-ttu-id="db9b5-180">Wert</span><span class="sxs-lookup"><span data-stu-id="db9b5-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="db9b5-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db9b5-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="db9b5-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db9b5-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="db9b5-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="db9b5-183">System-Only</span></span>            | <span data-ttu-id="db9b5-184">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-184">False</span></span>                                                               |
| <span data-ttu-id="db9b5-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db9b5-185">Is-Single-Valued</span></span>       | <span data-ttu-id="db9b5-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="db9b5-186">True</span></span>                                                                |
| <span data-ttu-id="db9b5-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db9b5-187">Is Indexed</span></span>             | <span data-ttu-id="db9b5-188">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-188">False</span></span>                                                               |
| <span data-ttu-id="db9b5-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db9b5-189">In Global Catalog</span></span>      | <span data-ttu-id="db9b5-190">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-190">False</span></span>                                                               |
| <span data-ttu-id="db9b5-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db9b5-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="db9b5-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db9b5-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="db9b5-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db9b5-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="db9b5-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db9b5-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="db9b5-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db9b5-195">Search-Flags</span></span>           | <span data-ttu-id="db9b5-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db9b5-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="db9b5-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db9b5-197">System-Flags</span></span>           | <span data-ttu-id="db9b5-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db9b5-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="db9b5-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db9b5-199">Classes used in</span></span>        | [<span data-ttu-id="db9b5-200">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="db9b5-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="db9b5-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db9b5-201">Windows Server 2008</span></span>



| <span data-ttu-id="db9b5-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db9b5-202">Entry</span></span> | <span data-ttu-id="db9b5-203">Wert</span><span class="sxs-lookup"><span data-stu-id="db9b5-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="db9b5-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db9b5-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="db9b5-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db9b5-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="db9b5-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="db9b5-206">System-Only</span></span>            | <span data-ttu-id="db9b5-207">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-207">False</span></span>                                                               |
| <span data-ttu-id="db9b5-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db9b5-208">Is-Single-Valued</span></span>       | <span data-ttu-id="db9b5-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="db9b5-209">True</span></span>                                                                |
| <span data-ttu-id="db9b5-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db9b5-210">Is Indexed</span></span>             | <span data-ttu-id="db9b5-211">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-211">False</span></span>                                                               |
| <span data-ttu-id="db9b5-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db9b5-212">In Global Catalog</span></span>      | <span data-ttu-id="db9b5-213">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-213">False</span></span>                                                               |
| <span data-ttu-id="db9b5-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db9b5-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="db9b5-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db9b5-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="db9b5-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db9b5-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="db9b5-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db9b5-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="db9b5-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db9b5-218">Search-Flags</span></span>           | <span data-ttu-id="db9b5-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db9b5-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="db9b5-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db9b5-220">System-Flags</span></span>           | <span data-ttu-id="db9b5-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db9b5-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="db9b5-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db9b5-222">Classes used in</span></span>        | [<span data-ttu-id="db9b5-223">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="db9b5-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="db9b5-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="db9b5-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="db9b5-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db9b5-225">Entry</span></span> | <span data-ttu-id="db9b5-226">Wert</span><span class="sxs-lookup"><span data-stu-id="db9b5-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="db9b5-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db9b5-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="db9b5-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db9b5-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="db9b5-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="db9b5-229">System-Only</span></span>            | <span data-ttu-id="db9b5-230">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-230">False</span></span>                                                               |
| <span data-ttu-id="db9b5-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db9b5-231">Is-Single-Valued</span></span>       | <span data-ttu-id="db9b5-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="db9b5-232">True</span></span>                                                                |
| <span data-ttu-id="db9b5-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db9b5-233">Is Indexed</span></span>             | <span data-ttu-id="db9b5-234">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-234">False</span></span>                                                               |
| <span data-ttu-id="db9b5-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db9b5-235">In Global Catalog</span></span>      | <span data-ttu-id="db9b5-236">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-236">False</span></span>                                                               |
| <span data-ttu-id="db9b5-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db9b5-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="db9b5-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db9b5-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="db9b5-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db9b5-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="db9b5-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db9b5-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="db9b5-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db9b5-241">Search-Flags</span></span>           | <span data-ttu-id="db9b5-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db9b5-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="db9b5-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db9b5-243">System-Flags</span></span>           | <span data-ttu-id="db9b5-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db9b5-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="db9b5-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db9b5-245">Classes used in</span></span>        | [<span data-ttu-id="db9b5-246">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="db9b5-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="db9b5-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="db9b5-247">Windows Server 2012</span></span>



| <span data-ttu-id="db9b5-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db9b5-248">Entry</span></span> | <span data-ttu-id="db9b5-249">Wert</span><span class="sxs-lookup"><span data-stu-id="db9b5-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="db9b5-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="db9b5-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="db9b5-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db9b5-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="db9b5-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="db9b5-252">System-Only</span></span>            | <span data-ttu-id="db9b5-253">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-253">False</span></span>                                                               |
| <span data-ttu-id="db9b5-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="db9b5-254">Is-Single-Valued</span></span>       | <span data-ttu-id="db9b5-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="db9b5-255">True</span></span>                                                                |
| <span data-ttu-id="db9b5-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="db9b5-256">Is Indexed</span></span>             | <span data-ttu-id="db9b5-257">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-257">False</span></span>                                                               |
| <span data-ttu-id="db9b5-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="db9b5-258">In Global Catalog</span></span>      | <span data-ttu-id="db9b5-259">False</span><span class="sxs-lookup"><span data-stu-id="db9b5-259">False</span></span>                                                               |
| <span data-ttu-id="db9b5-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db9b5-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="db9b5-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="db9b5-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="db9b5-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db9b5-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="db9b5-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db9b5-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="db9b5-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db9b5-264">Search-Flags</span></span>           | <span data-ttu-id="db9b5-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db9b5-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="db9b5-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db9b5-266">System-Flags</span></span>           | <span data-ttu-id="db9b5-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db9b5-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="db9b5-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="db9b5-268">Classes used in</span></span>        | [<span data-ttu-id="db9b5-269">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="db9b5-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





