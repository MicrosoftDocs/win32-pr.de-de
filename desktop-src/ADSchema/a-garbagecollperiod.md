---
title: Garbage-Coll-period-Attribut
description: Dieses Attribut befindet sich im CN-Verzeichnisdienst, CN Windows NT, CN Services, CN Configuration,... Objekt. Sie stellt die Zeit in Stunden zwischen den Ausführungen der DS Garbage Collection dar.
ms.assetid: 982a75f9-04b5-489e-99b3-a9fd3fb280c8
ms.tgt_platform: multiple
keywords:
- AD-Schema für das Garbage Coll-period-Attribut
- garbageCollPeriod-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Garbage-Coll-Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64890df97cf4c131ad0dcdbed8cb80bf20b66a83
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106345352"
---
# <a name="garbage-coll-period-attribute"></a><span data-ttu-id="47890-106">Garbage-Coll-period-Attribut</span><span class="sxs-lookup"><span data-stu-id="47890-106">Garbage-Coll-Period attribute</span></span>

<span data-ttu-id="47890-107">Dieses Attribut befindet sich im Verzeichnisdienst CN = Verzeichnisdienst, CN = Windows NT, CN = Services, CN = Configuration,... Objekt.</span><span class="sxs-lookup"><span data-stu-id="47890-107">This attribute is located on the CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,... object.</span></span> <span data-ttu-id="47890-108">Sie stellt die Zeit in Stunden zwischen den Ausführungen der DS Garbage Collection dar.</span><span class="sxs-lookup"><span data-stu-id="47890-108">It represents the time, in hours, between DS garbage collection runs.</span></span>



| <span data-ttu-id="47890-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47890-109">Entry</span></span> | <span data-ttu-id="47890-110">Wert</span><span class="sxs-lookup"><span data-stu-id="47890-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="47890-111">CN</span><span class="sxs-lookup"><span data-stu-id="47890-111">CN</span></span>                | <span data-ttu-id="47890-112">Garbage Koll-Zeitraum</span><span class="sxs-lookup"><span data-stu-id="47890-112">Garbage-Coll-Period</span></span>                  |
| <span data-ttu-id="47890-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="47890-113">Ldap-Display-Name</span></span> | <span data-ttu-id="47890-114">garbageCollPeriod</span><span class="sxs-lookup"><span data-stu-id="47890-114">garbageCollPeriod</span></span>                    |
| <span data-ttu-id="47890-115">Size</span><span class="sxs-lookup"><span data-stu-id="47890-115">Size</span></span>              | <span data-ttu-id="47890-116">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="47890-116">4 bytes</span></span>                              |
| <span data-ttu-id="47890-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="47890-117">Update Privilege</span></span>  | <span data-ttu-id="47890-118">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="47890-118">Domain administrator</span></span>                 |
| <span data-ttu-id="47890-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="47890-119">Update Frequency</span></span>  | <span data-ttu-id="47890-120">Sehr selten.</span><span class="sxs-lookup"><span data-stu-id="47890-120">Very rare.</span></span>                           |
| <span data-ttu-id="47890-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="47890-121">Attribute-Id</span></span>      | <span data-ttu-id="47890-122">1.2.840.113556.1.2.301</span><span class="sxs-lookup"><span data-stu-id="47890-122">1.2.840.113556.1.2.301</span></span>               |
| <span data-ttu-id="47890-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="47890-123">System-Id-Guid</span></span>    | <span data-ttu-id="47890-124">5F d424a1-1262-11D0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="47890-124">5fd424a1-1262-11d0-a060-00aa006c33ed</span></span> |
| <span data-ttu-id="47890-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="47890-125">Syntax</span></span>            | [<span data-ttu-id="47890-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="47890-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="47890-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="47890-127">Implementations</span></span>

-   [<span data-ttu-id="47890-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="47890-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="47890-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="47890-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="47890-130">**Adam**</span><span class="sxs-lookup"><span data-stu-id="47890-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="47890-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="47890-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="47890-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="47890-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="47890-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="47890-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="47890-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="47890-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="47890-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="47890-135">Windows 2000 Server</span></span>



| <span data-ttu-id="47890-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47890-136">Entry</span></span> | <span data-ttu-id="47890-137">Wert</span><span class="sxs-lookup"><span data-stu-id="47890-137">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47890-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="47890-138">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="47890-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47890-139">MAPI-Id</span></span>                | <span data-ttu-id="47890-140">0x80af</span><span class="sxs-lookup"><span data-stu-id="47890-140">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="47890-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="47890-141">System-Only</span></span>            | <span data-ttu-id="47890-142">False</span><span class="sxs-lookup"><span data-stu-id="47890-142">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-143">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="47890-143">Is-Single-Valued</span></span>       | <span data-ttu-id="47890-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="47890-144">True</span></span>                                                                                                  |
| <span data-ttu-id="47890-145">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="47890-145">Is Indexed</span></span>             | <span data-ttu-id="47890-146">False</span><span class="sxs-lookup"><span data-stu-id="47890-146">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-147">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="47890-147">In Global Catalog</span></span>      | <span data-ttu-id="47890-148">False</span><span class="sxs-lookup"><span data-stu-id="47890-148">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47890-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="47890-150">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="47890-150">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="47890-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47890-151">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="47890-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47890-152">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="47890-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47890-153">Search-Flags</span></span>           | <span data-ttu-id="47890-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47890-154">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="47890-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47890-155">System-Flags</span></span>           | <span data-ttu-id="47890-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="47890-156">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="47890-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="47890-157">Classes used in</span></span>        | [<span data-ttu-id="47890-158">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="47890-158">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="47890-159">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="47890-159">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="47890-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="47890-160">Windows Server 2003</span></span>



| <span data-ttu-id="47890-161">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47890-161">Entry</span></span> | <span data-ttu-id="47890-162">Wert</span><span class="sxs-lookup"><span data-stu-id="47890-162">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47890-163">Link-ID</span><span class="sxs-lookup"><span data-stu-id="47890-163">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="47890-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47890-164">MAPI-Id</span></span>                | <span data-ttu-id="47890-165">0x80af</span><span class="sxs-lookup"><span data-stu-id="47890-165">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="47890-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="47890-166">System-Only</span></span>            | <span data-ttu-id="47890-167">False</span><span class="sxs-lookup"><span data-stu-id="47890-167">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-168">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="47890-168">Is-Single-Valued</span></span>       | <span data-ttu-id="47890-169">Richtig</span><span class="sxs-lookup"><span data-stu-id="47890-169">True</span></span>                                                                                                  |
| <span data-ttu-id="47890-170">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="47890-170">Is Indexed</span></span>             | <span data-ttu-id="47890-171">False</span><span class="sxs-lookup"><span data-stu-id="47890-171">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-172">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="47890-172">In Global Catalog</span></span>      | <span data-ttu-id="47890-173">False</span><span class="sxs-lookup"><span data-stu-id="47890-173">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47890-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="47890-175">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="47890-175">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="47890-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47890-176">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="47890-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47890-177">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="47890-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47890-178">Search-Flags</span></span>           | <span data-ttu-id="47890-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47890-179">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="47890-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47890-180">System-Flags</span></span>           | <span data-ttu-id="47890-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="47890-181">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="47890-182">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="47890-182">Classes used in</span></span>        | [<span data-ttu-id="47890-183">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="47890-183">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="47890-184">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="47890-184">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="47890-185">Adam</span><span class="sxs-lookup"><span data-stu-id="47890-185">ADAM</span></span>



| <span data-ttu-id="47890-186">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47890-186">Entry</span></span> | <span data-ttu-id="47890-187">Wert</span><span class="sxs-lookup"><span data-stu-id="47890-187">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="47890-188">Link-ID</span><span class="sxs-lookup"><span data-stu-id="47890-188">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="47890-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47890-189">MAPI-Id</span></span>                | <span data-ttu-id="47890-190">0x80af</span><span class="sxs-lookup"><span data-stu-id="47890-190">0x80AF</span></span>                                           |
| <span data-ttu-id="47890-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="47890-191">System-Only</span></span>            | <span data-ttu-id="47890-192">False</span><span class="sxs-lookup"><span data-stu-id="47890-192">False</span></span>                                            |
| <span data-ttu-id="47890-193">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="47890-193">Is-Single-Valued</span></span>       | <span data-ttu-id="47890-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="47890-194">True</span></span>                                             |
| <span data-ttu-id="47890-195">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="47890-195">Is Indexed</span></span>             | <span data-ttu-id="47890-196">False</span><span class="sxs-lookup"><span data-stu-id="47890-196">False</span></span>                                            |
| <span data-ttu-id="47890-197">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="47890-197">In Global Catalog</span></span>      | <span data-ttu-id="47890-198">False</span><span class="sxs-lookup"><span data-stu-id="47890-198">False</span></span>                                            |
| <span data-ttu-id="47890-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47890-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="47890-200">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="47890-200">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="47890-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47890-201">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="47890-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47890-202">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="47890-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47890-203">Search-Flags</span></span>           | <span data-ttu-id="47890-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47890-204">0x00000000</span></span>                                       |
| <span data-ttu-id="47890-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47890-205">System-Flags</span></span>           | <span data-ttu-id="47890-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="47890-206">0x00000010</span></span>                                       |
| <span data-ttu-id="47890-207">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="47890-207">Classes used in</span></span>        | [<span data-ttu-id="47890-208">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="47890-208">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="47890-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="47890-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="47890-210">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47890-210">Entry</span></span> | <span data-ttu-id="47890-211">Wert</span><span class="sxs-lookup"><span data-stu-id="47890-211">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47890-212">Link-ID</span><span class="sxs-lookup"><span data-stu-id="47890-212">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="47890-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47890-213">MAPI-Id</span></span>                | <span data-ttu-id="47890-214">0x80af</span><span class="sxs-lookup"><span data-stu-id="47890-214">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="47890-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="47890-215">System-Only</span></span>            | <span data-ttu-id="47890-216">False</span><span class="sxs-lookup"><span data-stu-id="47890-216">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-217">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="47890-217">Is-Single-Valued</span></span>       | <span data-ttu-id="47890-218">Richtig</span><span class="sxs-lookup"><span data-stu-id="47890-218">True</span></span>                                                                                                  |
| <span data-ttu-id="47890-219">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="47890-219">Is Indexed</span></span>             | <span data-ttu-id="47890-220">False</span><span class="sxs-lookup"><span data-stu-id="47890-220">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-221">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="47890-221">In Global Catalog</span></span>      | <span data-ttu-id="47890-222">False</span><span class="sxs-lookup"><span data-stu-id="47890-222">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47890-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="47890-224">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="47890-224">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="47890-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47890-225">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="47890-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47890-226">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="47890-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47890-227">Search-Flags</span></span>           | <span data-ttu-id="47890-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47890-228">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="47890-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47890-229">System-Flags</span></span>           | <span data-ttu-id="47890-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="47890-230">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="47890-231">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="47890-231">Classes used in</span></span>        | [<span data-ttu-id="47890-232">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="47890-232">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="47890-233">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="47890-233">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="47890-234">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47890-234">Windows Server 2008</span></span>



| <span data-ttu-id="47890-235">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47890-235">Entry</span></span> | <span data-ttu-id="47890-236">Wert</span><span class="sxs-lookup"><span data-stu-id="47890-236">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47890-237">Link-ID</span><span class="sxs-lookup"><span data-stu-id="47890-237">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="47890-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47890-238">MAPI-Id</span></span>                | <span data-ttu-id="47890-239">0x80af</span><span class="sxs-lookup"><span data-stu-id="47890-239">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="47890-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="47890-240">System-Only</span></span>            | <span data-ttu-id="47890-241">False</span><span class="sxs-lookup"><span data-stu-id="47890-241">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-242">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="47890-242">Is-Single-Valued</span></span>       | <span data-ttu-id="47890-243">Richtig</span><span class="sxs-lookup"><span data-stu-id="47890-243">True</span></span>                                                                                                  |
| <span data-ttu-id="47890-244">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="47890-244">Is Indexed</span></span>             | <span data-ttu-id="47890-245">False</span><span class="sxs-lookup"><span data-stu-id="47890-245">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-246">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="47890-246">In Global Catalog</span></span>      | <span data-ttu-id="47890-247">False</span><span class="sxs-lookup"><span data-stu-id="47890-247">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-248">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47890-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="47890-249">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="47890-249">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="47890-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47890-250">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="47890-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47890-251">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="47890-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47890-252">Search-Flags</span></span>           | <span data-ttu-id="47890-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47890-253">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="47890-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47890-254">System-Flags</span></span>           | <span data-ttu-id="47890-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="47890-255">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="47890-256">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="47890-256">Classes used in</span></span>        | [<span data-ttu-id="47890-257">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="47890-257">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="47890-258">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="47890-258">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="47890-259">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="47890-259">Windows Server 2008 R2</span></span>



| <span data-ttu-id="47890-260">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47890-260">Entry</span></span> | <span data-ttu-id="47890-261">Wert</span><span class="sxs-lookup"><span data-stu-id="47890-261">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47890-262">Link-ID</span><span class="sxs-lookup"><span data-stu-id="47890-262">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="47890-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47890-263">MAPI-Id</span></span>                | <span data-ttu-id="47890-264">0x80af</span><span class="sxs-lookup"><span data-stu-id="47890-264">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="47890-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="47890-265">System-Only</span></span>            | <span data-ttu-id="47890-266">False</span><span class="sxs-lookup"><span data-stu-id="47890-266">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-267">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="47890-267">Is-Single-Valued</span></span>       | <span data-ttu-id="47890-268">Richtig</span><span class="sxs-lookup"><span data-stu-id="47890-268">True</span></span>                                                                                                  |
| <span data-ttu-id="47890-269">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="47890-269">Is Indexed</span></span>             | <span data-ttu-id="47890-270">False</span><span class="sxs-lookup"><span data-stu-id="47890-270">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-271">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="47890-271">In Global Catalog</span></span>      | <span data-ttu-id="47890-272">False</span><span class="sxs-lookup"><span data-stu-id="47890-272">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-273">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47890-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="47890-274">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="47890-274">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="47890-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47890-275">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="47890-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47890-276">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="47890-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47890-277">Search-Flags</span></span>           | <span data-ttu-id="47890-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47890-278">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="47890-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47890-279">System-Flags</span></span>           | <span data-ttu-id="47890-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="47890-280">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="47890-281">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="47890-281">Classes used in</span></span>        | [<span data-ttu-id="47890-282">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="47890-282">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="47890-283">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="47890-283">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="47890-284">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="47890-284">Windows Server 2012</span></span>



| <span data-ttu-id="47890-285">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47890-285">Entry</span></span> | <span data-ttu-id="47890-286">Wert</span><span class="sxs-lookup"><span data-stu-id="47890-286">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47890-287">Link-ID</span><span class="sxs-lookup"><span data-stu-id="47890-287">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="47890-288">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47890-288">MAPI-Id</span></span>                | <span data-ttu-id="47890-289">0x80af</span><span class="sxs-lookup"><span data-stu-id="47890-289">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="47890-290">System-Only</span><span class="sxs-lookup"><span data-stu-id="47890-290">System-Only</span></span>            | <span data-ttu-id="47890-291">False</span><span class="sxs-lookup"><span data-stu-id="47890-291">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-292">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="47890-292">Is-Single-Valued</span></span>       | <span data-ttu-id="47890-293">Richtig</span><span class="sxs-lookup"><span data-stu-id="47890-293">True</span></span>                                                                                                  |
| <span data-ttu-id="47890-294">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="47890-294">Is Indexed</span></span>             | <span data-ttu-id="47890-295">False</span><span class="sxs-lookup"><span data-stu-id="47890-295">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-296">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="47890-296">In Global Catalog</span></span>      | <span data-ttu-id="47890-297">False</span><span class="sxs-lookup"><span data-stu-id="47890-297">False</span></span>                                                                                                 |
| <span data-ttu-id="47890-298">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47890-298">NT-Security-Descriptor</span></span> | <span data-ttu-id="47890-299">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="47890-299">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="47890-300">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47890-300">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="47890-301">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47890-301">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="47890-302">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47890-302">Search-Flags</span></span>           | <span data-ttu-id="47890-303">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47890-303">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="47890-304">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47890-304">System-Flags</span></span>           | <span data-ttu-id="47890-305">0x00000010</span><span class="sxs-lookup"><span data-stu-id="47890-305">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="47890-306">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="47890-306">Classes used in</span></span>        | [<span data-ttu-id="47890-307">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="47890-307">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="47890-308">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="47890-308">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





