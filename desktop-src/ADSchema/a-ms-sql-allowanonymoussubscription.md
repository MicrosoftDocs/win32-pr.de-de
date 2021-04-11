---
title: MS-SQL-zubezeichnungs Abonnement-Attribut
description: True, wenn die Veröffentlichung anonymen Abonnenten das Abonnieren ermöglicht.
ms.assetid: d4ac86ce-d3c5-493e-8212-e9250671a522
ms.tgt_platform: multiple
keywords:
- Schema des MS-SQL-zubezeichnungs Abonnements-Attributs
- Schema des MS-SQL-zubezeichnungs Abonnements-Attributs
topic_type:
- apiref
api_name:
- MS-SQL-AllowAnonymousSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23de7f731ffaca310a39d81d4af80a5b0a23a84
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123062"
---
# <a name="ms-sql-allowanonymoussubscription-attribute"></a><span data-ttu-id="48894-105">MS-SQL-zubezeichnungs Abonnement-Attribut</span><span class="sxs-lookup"><span data-stu-id="48894-105">MS-SQL-AllowAnonymousSubscription attribute</span></span>

<span data-ttu-id="48894-106">True, wenn die Veröffentlichung anonymen Abonnenten das Abonnieren ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="48894-106">True if the publication allows anonymous subscribers to subscribe to it.</span></span>



| <span data-ttu-id="48894-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="48894-107">Entry</span></span> | <span data-ttu-id="48894-108">Wert</span><span class="sxs-lookup"><span data-stu-id="48894-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="48894-109">CN</span><span class="sxs-lookup"><span data-stu-id="48894-109">CN</span></span>                | <span data-ttu-id="48894-110">MS-SQL-zuverteilungsabonnement</span><span class="sxs-lookup"><span data-stu-id="48894-110">MS-SQL-AllowAnonymousSubscription</span></span>    |
| <span data-ttu-id="48894-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="48894-111">Ldap-Display-Name</span></span> | <span data-ttu-id="48894-112">MS-SQL-zuverteilungsabonnement</span><span class="sxs-lookup"><span data-stu-id="48894-112">mS-SQL-AllowAnonymousSubscription</span></span>    |
| <span data-ttu-id="48894-113">Size</span><span class="sxs-lookup"><span data-stu-id="48894-113">Size</span></span>              | <span data-ttu-id="48894-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="48894-114">4 bytes</span></span>                              |
| <span data-ttu-id="48894-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="48894-115">Update Privilege</span></span>  | <span data-ttu-id="48894-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="48894-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="48894-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="48894-117">Update Frequency</span></span>  | <span data-ttu-id="48894-118">Wenn die Replikation eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="48894-118">When replication is setup.</span></span>           |
| <span data-ttu-id="48894-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="48894-119">Attribute-Id</span></span>      | <span data-ttu-id="48894-120">1.2.840.113556.1.4.1394</span><span class="sxs-lookup"><span data-stu-id="48894-120">1.2.840.113556.1.4.1394</span></span>              |
| <span data-ttu-id="48894-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="48894-121">System-Id-Guid</span></span>    | <span data-ttu-id="48894-122">db77be4a-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="48894-122">db77be4a-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="48894-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="48894-123">Syntax</span></span>            | [<span data-ttu-id="48894-124">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="48894-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="48894-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="48894-125">Implementations</span></span>

-   [<span data-ttu-id="48894-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="48894-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="48894-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="48894-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="48894-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="48894-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="48894-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="48894-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="48894-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="48894-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="48894-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="48894-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="48894-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="48894-132">Windows 2000 Server</span></span>



| <span data-ttu-id="48894-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="48894-133">Entry</span></span> | <span data-ttu-id="48894-134">Wert</span><span class="sxs-lookup"><span data-stu-id="48894-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="48894-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="48894-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="48894-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48894-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="48894-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="48894-137">System-Only</span></span>            | <span data-ttu-id="48894-138">False</span><span class="sxs-lookup"><span data-stu-id="48894-138">False</span></span>                                                               |
| <span data-ttu-id="48894-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="48894-139">Is-Single-Valued</span></span>       | <span data-ttu-id="48894-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="48894-140">True</span></span>                                                                |
| <span data-ttu-id="48894-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="48894-141">Is Indexed</span></span>             | <span data-ttu-id="48894-142">False</span><span class="sxs-lookup"><span data-stu-id="48894-142">False</span></span>                                                               |
| <span data-ttu-id="48894-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="48894-143">In Global Catalog</span></span>      | <span data-ttu-id="48894-144">False</span><span class="sxs-lookup"><span data-stu-id="48894-144">False</span></span>                                                               |
| <span data-ttu-id="48894-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48894-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="48894-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="48894-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="48894-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48894-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="48894-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48894-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="48894-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48894-149">Search-Flags</span></span>           | <span data-ttu-id="48894-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48894-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="48894-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48894-151">System-Flags</span></span>           | <span data-ttu-id="48894-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48894-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="48894-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="48894-153">Classes used in</span></span>        | [<span data-ttu-id="48894-154">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="48894-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="48894-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="48894-155">Windows Server 2003</span></span>



| <span data-ttu-id="48894-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="48894-156">Entry</span></span> | <span data-ttu-id="48894-157">Wert</span><span class="sxs-lookup"><span data-stu-id="48894-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="48894-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="48894-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="48894-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48894-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="48894-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="48894-160">System-Only</span></span>            | <span data-ttu-id="48894-161">False</span><span class="sxs-lookup"><span data-stu-id="48894-161">False</span></span>                                                               |
| <span data-ttu-id="48894-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="48894-162">Is-Single-Valued</span></span>       | <span data-ttu-id="48894-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="48894-163">True</span></span>                                                                |
| <span data-ttu-id="48894-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="48894-164">Is Indexed</span></span>             | <span data-ttu-id="48894-165">False</span><span class="sxs-lookup"><span data-stu-id="48894-165">False</span></span>                                                               |
| <span data-ttu-id="48894-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="48894-166">In Global Catalog</span></span>      | <span data-ttu-id="48894-167">False</span><span class="sxs-lookup"><span data-stu-id="48894-167">False</span></span>                                                               |
| <span data-ttu-id="48894-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48894-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="48894-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="48894-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="48894-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48894-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="48894-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48894-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="48894-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48894-172">Search-Flags</span></span>           | <span data-ttu-id="48894-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48894-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="48894-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48894-174">System-Flags</span></span>           | <span data-ttu-id="48894-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48894-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="48894-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="48894-176">Classes used in</span></span>        | [<span data-ttu-id="48894-177">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="48894-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="48894-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="48894-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="48894-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="48894-179">Entry</span></span> | <span data-ttu-id="48894-180">Wert</span><span class="sxs-lookup"><span data-stu-id="48894-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="48894-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="48894-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="48894-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48894-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="48894-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="48894-183">System-Only</span></span>            | <span data-ttu-id="48894-184">False</span><span class="sxs-lookup"><span data-stu-id="48894-184">False</span></span>                                                               |
| <span data-ttu-id="48894-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="48894-185">Is-Single-Valued</span></span>       | <span data-ttu-id="48894-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="48894-186">True</span></span>                                                                |
| <span data-ttu-id="48894-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="48894-187">Is Indexed</span></span>             | <span data-ttu-id="48894-188">False</span><span class="sxs-lookup"><span data-stu-id="48894-188">False</span></span>                                                               |
| <span data-ttu-id="48894-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="48894-189">In Global Catalog</span></span>      | <span data-ttu-id="48894-190">False</span><span class="sxs-lookup"><span data-stu-id="48894-190">False</span></span>                                                               |
| <span data-ttu-id="48894-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48894-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="48894-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="48894-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="48894-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48894-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="48894-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48894-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="48894-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48894-195">Search-Flags</span></span>           | <span data-ttu-id="48894-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48894-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="48894-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48894-197">System-Flags</span></span>           | <span data-ttu-id="48894-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48894-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="48894-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="48894-199">Classes used in</span></span>        | [<span data-ttu-id="48894-200">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="48894-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="48894-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48894-201">Windows Server 2008</span></span>



| <span data-ttu-id="48894-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="48894-202">Entry</span></span> | <span data-ttu-id="48894-203">Wert</span><span class="sxs-lookup"><span data-stu-id="48894-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="48894-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="48894-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="48894-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48894-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="48894-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="48894-206">System-Only</span></span>            | <span data-ttu-id="48894-207">False</span><span class="sxs-lookup"><span data-stu-id="48894-207">False</span></span>                                                               |
| <span data-ttu-id="48894-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="48894-208">Is-Single-Valued</span></span>       | <span data-ttu-id="48894-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="48894-209">True</span></span>                                                                |
| <span data-ttu-id="48894-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="48894-210">Is Indexed</span></span>             | <span data-ttu-id="48894-211">False</span><span class="sxs-lookup"><span data-stu-id="48894-211">False</span></span>                                                               |
| <span data-ttu-id="48894-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="48894-212">In Global Catalog</span></span>      | <span data-ttu-id="48894-213">False</span><span class="sxs-lookup"><span data-stu-id="48894-213">False</span></span>                                                               |
| <span data-ttu-id="48894-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48894-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="48894-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="48894-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="48894-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48894-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="48894-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48894-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="48894-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48894-218">Search-Flags</span></span>           | <span data-ttu-id="48894-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48894-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="48894-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48894-220">System-Flags</span></span>           | <span data-ttu-id="48894-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48894-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="48894-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="48894-222">Classes used in</span></span>        | [<span data-ttu-id="48894-223">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="48894-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="48894-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="48894-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="48894-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="48894-225">Entry</span></span> | <span data-ttu-id="48894-226">Wert</span><span class="sxs-lookup"><span data-stu-id="48894-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="48894-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="48894-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="48894-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48894-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="48894-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="48894-229">System-Only</span></span>            | <span data-ttu-id="48894-230">False</span><span class="sxs-lookup"><span data-stu-id="48894-230">False</span></span>                                                               |
| <span data-ttu-id="48894-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="48894-231">Is-Single-Valued</span></span>       | <span data-ttu-id="48894-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="48894-232">True</span></span>                                                                |
| <span data-ttu-id="48894-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="48894-233">Is Indexed</span></span>             | <span data-ttu-id="48894-234">False</span><span class="sxs-lookup"><span data-stu-id="48894-234">False</span></span>                                                               |
| <span data-ttu-id="48894-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="48894-235">In Global Catalog</span></span>      | <span data-ttu-id="48894-236">False</span><span class="sxs-lookup"><span data-stu-id="48894-236">False</span></span>                                                               |
| <span data-ttu-id="48894-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48894-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="48894-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="48894-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="48894-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48894-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="48894-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48894-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="48894-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48894-241">Search-Flags</span></span>           | <span data-ttu-id="48894-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48894-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="48894-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48894-243">System-Flags</span></span>           | <span data-ttu-id="48894-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48894-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="48894-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="48894-245">Classes used in</span></span>        | [<span data-ttu-id="48894-246">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="48894-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="48894-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="48894-247">Windows Server 2012</span></span>



| <span data-ttu-id="48894-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="48894-248">Entry</span></span> | <span data-ttu-id="48894-249">Wert</span><span class="sxs-lookup"><span data-stu-id="48894-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="48894-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="48894-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="48894-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48894-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="48894-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="48894-252">System-Only</span></span>            | <span data-ttu-id="48894-253">False</span><span class="sxs-lookup"><span data-stu-id="48894-253">False</span></span>                                                               |
| <span data-ttu-id="48894-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="48894-254">Is-Single-Valued</span></span>       | <span data-ttu-id="48894-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="48894-255">True</span></span>                                                                |
| <span data-ttu-id="48894-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="48894-256">Is Indexed</span></span>             | <span data-ttu-id="48894-257">False</span><span class="sxs-lookup"><span data-stu-id="48894-257">False</span></span>                                                               |
| <span data-ttu-id="48894-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="48894-258">In Global Catalog</span></span>      | <span data-ttu-id="48894-259">False</span><span class="sxs-lookup"><span data-stu-id="48894-259">False</span></span>                                                               |
| <span data-ttu-id="48894-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48894-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="48894-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="48894-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="48894-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48894-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="48894-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48894-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="48894-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48894-264">Search-Flags</span></span>           | <span data-ttu-id="48894-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48894-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="48894-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48894-266">System-Flags</span></span>           | <span data-ttu-id="48894-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48894-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="48894-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="48894-268">Classes used in</span></span>        | [<span data-ttu-id="48894-269">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="48894-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





