---
title: FRS-File-Filter-Attribut
description: Eine Liste der Dateinamen Erweiterungen, die von der Datei Replikation ausgeschlossen werden.
ms.assetid: 094a393a-9e1a-4da8-a38a-161102f164fd
ms.tgt_platform: multiple
keywords:
- AD-Schema für FRS-File-Filter-Attribut
- Schema des fRSFileFilter-Attributs
topic_type:
- apiref
api_name:
- FRS-File-Filter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234cf7d6e56e84c2ed9578fc56036e581a2f0ad2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106345950"
---
# <a name="frs-file-filter-attribute"></a><span data-ttu-id="3502b-105">FRS-File-Filter-Attribut</span><span class="sxs-lookup"><span data-stu-id="3502b-105">FRS-File-Filter attribute</span></span>

<span data-ttu-id="3502b-106">Eine Liste der Dateinamen Erweiterungen, die von der Datei Replikation ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="3502b-106">A list of file name extensions excluded from file replication.</span></span>



| <span data-ttu-id="3502b-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3502b-107">Entry</span></span> | <span data-ttu-id="3502b-108">Wert</span><span class="sxs-lookup"><span data-stu-id="3502b-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="3502b-109">CN</span><span class="sxs-lookup"><span data-stu-id="3502b-109">CN</span></span>                | <span data-ttu-id="3502b-110">FRS-File-Filter</span><span class="sxs-lookup"><span data-stu-id="3502b-110">FRS-File-Filter</span></span>                             |
| <span data-ttu-id="3502b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3502b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3502b-112">fRSFileFilter</span><span class="sxs-lookup"><span data-stu-id="3502b-112">fRSFileFilter</span></span>                               |
| <span data-ttu-id="3502b-113">Size</span><span class="sxs-lookup"><span data-stu-id="3502b-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="3502b-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="3502b-114">Update Privilege</span></span>  | <span data-ttu-id="3502b-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="3502b-115">Domain administrator</span></span>                        |
| <span data-ttu-id="3502b-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="3502b-116">Update Frequency</span></span>  | <span data-ttu-id="3502b-117">Wenn die Replikation eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="3502b-117">When replication is setup.</span></span>                  |
| <span data-ttu-id="3502b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3502b-118">Attribute-Id</span></span>      | <span data-ttu-id="3502b-119">1.2.840.113556.1.4.483</span><span class="sxs-lookup"><span data-stu-id="3502b-119">1.2.840.113556.1.4.483</span></span>                      |
| <span data-ttu-id="3502b-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3502b-120">System-Id-Guid</span></span>    | <span data-ttu-id="3502b-121">1be8f170-a9ff-11D0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="3502b-121">1be8f170-a9ff-11d0-afe2-00c04fd930c9</span></span>        |
| <span data-ttu-id="3502b-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="3502b-122">Syntax</span></span>            | [<span data-ttu-id="3502b-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3502b-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="3502b-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="3502b-124">Implementations</span></span>

-   [<span data-ttu-id="3502b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3502b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3502b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3502b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3502b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3502b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3502b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3502b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3502b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3502b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3502b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3502b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3502b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3502b-131">Windows 2000 Server</span></span>



| <span data-ttu-id="3502b-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3502b-132">Entry</span></span> | <span data-ttu-id="3502b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="3502b-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3502b-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3502b-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3502b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3502b-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3502b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="3502b-136">System-Only</span></span>            | <span data-ttu-id="3502b-137">False</span><span class="sxs-lookup"><span data-stu-id="3502b-137">False</span></span>                                                     |
| <span data-ttu-id="3502b-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3502b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="3502b-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="3502b-139">True</span></span>                                                      |
| <span data-ttu-id="3502b-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3502b-140">Is Indexed</span></span>             | <span data-ttu-id="3502b-141">False</span><span class="sxs-lookup"><span data-stu-id="3502b-141">False</span></span>                                                     |
| <span data-ttu-id="3502b-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3502b-142">In Global Catalog</span></span>      | <span data-ttu-id="3502b-143">False</span><span class="sxs-lookup"><span data-stu-id="3502b-143">False</span></span>                                                     |
| <span data-ttu-id="3502b-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3502b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="3502b-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3502b-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3502b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3502b-146">Range-Lower</span></span>            | <span data-ttu-id="3502b-147">0</span><span class="sxs-lookup"><span data-stu-id="3502b-147">0</span></span>                                                         |
| <span data-ttu-id="3502b-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3502b-148">Range-Upper</span></span>            | <span data-ttu-id="3502b-149">2048</span><span class="sxs-lookup"><span data-stu-id="3502b-149">2048</span></span>                                                      |
| <span data-ttu-id="3502b-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3502b-150">Search-Flags</span></span>           | <span data-ttu-id="3502b-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3502b-151">0x00000000</span></span>                                                |
| <span data-ttu-id="3502b-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3502b-152">System-Flags</span></span>           | <span data-ttu-id="3502b-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3502b-153">0x00000010</span></span>                                                |
| <span data-ttu-id="3502b-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3502b-154">Classes used in</span></span>        | [<span data-ttu-id="3502b-155">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="3502b-155">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3502b-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3502b-156">Windows Server 2003</span></span>



| <span data-ttu-id="3502b-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3502b-157">Entry</span></span> | <span data-ttu-id="3502b-158">Wert</span><span class="sxs-lookup"><span data-stu-id="3502b-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3502b-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3502b-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3502b-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3502b-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3502b-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="3502b-161">System-Only</span></span>            | <span data-ttu-id="3502b-162">False</span><span class="sxs-lookup"><span data-stu-id="3502b-162">False</span></span>                                                     |
| <span data-ttu-id="3502b-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3502b-163">Is-Single-Valued</span></span>       | <span data-ttu-id="3502b-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="3502b-164">True</span></span>                                                      |
| <span data-ttu-id="3502b-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3502b-165">Is Indexed</span></span>             | <span data-ttu-id="3502b-166">False</span><span class="sxs-lookup"><span data-stu-id="3502b-166">False</span></span>                                                     |
| <span data-ttu-id="3502b-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3502b-167">In Global Catalog</span></span>      | <span data-ttu-id="3502b-168">False</span><span class="sxs-lookup"><span data-stu-id="3502b-168">False</span></span>                                                     |
| <span data-ttu-id="3502b-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3502b-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="3502b-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3502b-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3502b-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3502b-171">Range-Lower</span></span>            | <span data-ttu-id="3502b-172">0</span><span class="sxs-lookup"><span data-stu-id="3502b-172">0</span></span>                                                         |
| <span data-ttu-id="3502b-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3502b-173">Range-Upper</span></span>            | <span data-ttu-id="3502b-174">2048</span><span class="sxs-lookup"><span data-stu-id="3502b-174">2048</span></span>                                                      |
| <span data-ttu-id="3502b-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3502b-175">Search-Flags</span></span>           | <span data-ttu-id="3502b-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3502b-176">0x00000000</span></span>                                                |
| <span data-ttu-id="3502b-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3502b-177">System-Flags</span></span>           | <span data-ttu-id="3502b-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3502b-178">0x00000010</span></span>                                                |
| <span data-ttu-id="3502b-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3502b-179">Classes used in</span></span>        | [<span data-ttu-id="3502b-180">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="3502b-180">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3502b-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3502b-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3502b-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3502b-182">Entry</span></span> | <span data-ttu-id="3502b-183">Wert</span><span class="sxs-lookup"><span data-stu-id="3502b-183">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3502b-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3502b-184">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3502b-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3502b-185">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3502b-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="3502b-186">System-Only</span></span>            | <span data-ttu-id="3502b-187">False</span><span class="sxs-lookup"><span data-stu-id="3502b-187">False</span></span>                                                     |
| <span data-ttu-id="3502b-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3502b-188">Is-Single-Valued</span></span>       | <span data-ttu-id="3502b-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="3502b-189">True</span></span>                                                      |
| <span data-ttu-id="3502b-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3502b-190">Is Indexed</span></span>             | <span data-ttu-id="3502b-191">False</span><span class="sxs-lookup"><span data-stu-id="3502b-191">False</span></span>                                                     |
| <span data-ttu-id="3502b-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3502b-192">In Global Catalog</span></span>      | <span data-ttu-id="3502b-193">False</span><span class="sxs-lookup"><span data-stu-id="3502b-193">False</span></span>                                                     |
| <span data-ttu-id="3502b-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3502b-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="3502b-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3502b-195">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3502b-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3502b-196">Range-Lower</span></span>            | <span data-ttu-id="3502b-197">0</span><span class="sxs-lookup"><span data-stu-id="3502b-197">0</span></span>                                                         |
| <span data-ttu-id="3502b-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3502b-198">Range-Upper</span></span>            | <span data-ttu-id="3502b-199">2048</span><span class="sxs-lookup"><span data-stu-id="3502b-199">2048</span></span>                                                      |
| <span data-ttu-id="3502b-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3502b-200">Search-Flags</span></span>           | <span data-ttu-id="3502b-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3502b-201">0x00000000</span></span>                                                |
| <span data-ttu-id="3502b-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3502b-202">System-Flags</span></span>           | <span data-ttu-id="3502b-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3502b-203">0x00000010</span></span>                                                |
| <span data-ttu-id="3502b-204">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3502b-204">Classes used in</span></span>        | [<span data-ttu-id="3502b-205">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="3502b-205">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3502b-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3502b-206">Windows Server 2008</span></span>



| <span data-ttu-id="3502b-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3502b-207">Entry</span></span> | <span data-ttu-id="3502b-208">Wert</span><span class="sxs-lookup"><span data-stu-id="3502b-208">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3502b-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3502b-209">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3502b-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3502b-210">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3502b-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="3502b-211">System-Only</span></span>            | <span data-ttu-id="3502b-212">False</span><span class="sxs-lookup"><span data-stu-id="3502b-212">False</span></span>                                                     |
| <span data-ttu-id="3502b-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3502b-213">Is-Single-Valued</span></span>       | <span data-ttu-id="3502b-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="3502b-214">True</span></span>                                                      |
| <span data-ttu-id="3502b-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3502b-215">Is Indexed</span></span>             | <span data-ttu-id="3502b-216">False</span><span class="sxs-lookup"><span data-stu-id="3502b-216">False</span></span>                                                     |
| <span data-ttu-id="3502b-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3502b-217">In Global Catalog</span></span>      | <span data-ttu-id="3502b-218">False</span><span class="sxs-lookup"><span data-stu-id="3502b-218">False</span></span>                                                     |
| <span data-ttu-id="3502b-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3502b-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="3502b-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3502b-220">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3502b-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3502b-221">Range-Lower</span></span>            | <span data-ttu-id="3502b-222">0</span><span class="sxs-lookup"><span data-stu-id="3502b-222">0</span></span>                                                         |
| <span data-ttu-id="3502b-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3502b-223">Range-Upper</span></span>            | <span data-ttu-id="3502b-224">2048</span><span class="sxs-lookup"><span data-stu-id="3502b-224">2048</span></span>                                                      |
| <span data-ttu-id="3502b-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3502b-225">Search-Flags</span></span>           | <span data-ttu-id="3502b-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3502b-226">0x00000000</span></span>                                                |
| <span data-ttu-id="3502b-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3502b-227">System-Flags</span></span>           | <span data-ttu-id="3502b-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3502b-228">0x00000010</span></span>                                                |
| <span data-ttu-id="3502b-229">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3502b-229">Classes used in</span></span>        | [<span data-ttu-id="3502b-230">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="3502b-230">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3502b-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3502b-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3502b-232">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3502b-232">Entry</span></span> | <span data-ttu-id="3502b-233">Wert</span><span class="sxs-lookup"><span data-stu-id="3502b-233">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3502b-234">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3502b-234">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3502b-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3502b-235">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3502b-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="3502b-236">System-Only</span></span>            | <span data-ttu-id="3502b-237">False</span><span class="sxs-lookup"><span data-stu-id="3502b-237">False</span></span>                                                     |
| <span data-ttu-id="3502b-238">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3502b-238">Is-Single-Valued</span></span>       | <span data-ttu-id="3502b-239">Richtig</span><span class="sxs-lookup"><span data-stu-id="3502b-239">True</span></span>                                                      |
| <span data-ttu-id="3502b-240">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3502b-240">Is Indexed</span></span>             | <span data-ttu-id="3502b-241">False</span><span class="sxs-lookup"><span data-stu-id="3502b-241">False</span></span>                                                     |
| <span data-ttu-id="3502b-242">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3502b-242">In Global Catalog</span></span>      | <span data-ttu-id="3502b-243">False</span><span class="sxs-lookup"><span data-stu-id="3502b-243">False</span></span>                                                     |
| <span data-ttu-id="3502b-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3502b-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="3502b-245">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3502b-245">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3502b-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3502b-246">Range-Lower</span></span>            | <span data-ttu-id="3502b-247">0</span><span class="sxs-lookup"><span data-stu-id="3502b-247">0</span></span>                                                         |
| <span data-ttu-id="3502b-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3502b-248">Range-Upper</span></span>            | <span data-ttu-id="3502b-249">2048</span><span class="sxs-lookup"><span data-stu-id="3502b-249">2048</span></span>                                                      |
| <span data-ttu-id="3502b-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3502b-250">Search-Flags</span></span>           | <span data-ttu-id="3502b-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3502b-251">0x00000000</span></span>                                                |
| <span data-ttu-id="3502b-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3502b-252">System-Flags</span></span>           | <span data-ttu-id="3502b-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3502b-253">0x00000010</span></span>                                                |
| <span data-ttu-id="3502b-254">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3502b-254">Classes used in</span></span>        | [<span data-ttu-id="3502b-255">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="3502b-255">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3502b-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3502b-256">Windows Server 2012</span></span>



| <span data-ttu-id="3502b-257">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3502b-257">Entry</span></span> | <span data-ttu-id="3502b-258">Wert</span><span class="sxs-lookup"><span data-stu-id="3502b-258">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3502b-259">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3502b-259">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3502b-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3502b-260">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3502b-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="3502b-261">System-Only</span></span>            | <span data-ttu-id="3502b-262">False</span><span class="sxs-lookup"><span data-stu-id="3502b-262">False</span></span>                                                     |
| <span data-ttu-id="3502b-263">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3502b-263">Is-Single-Valued</span></span>       | <span data-ttu-id="3502b-264">Richtig</span><span class="sxs-lookup"><span data-stu-id="3502b-264">True</span></span>                                                      |
| <span data-ttu-id="3502b-265">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3502b-265">Is Indexed</span></span>             | <span data-ttu-id="3502b-266">False</span><span class="sxs-lookup"><span data-stu-id="3502b-266">False</span></span>                                                     |
| <span data-ttu-id="3502b-267">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3502b-267">In Global Catalog</span></span>      | <span data-ttu-id="3502b-268">False</span><span class="sxs-lookup"><span data-stu-id="3502b-268">False</span></span>                                                     |
| <span data-ttu-id="3502b-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3502b-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="3502b-270">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3502b-270">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3502b-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3502b-271">Range-Lower</span></span>            | <span data-ttu-id="3502b-272">0</span><span class="sxs-lookup"><span data-stu-id="3502b-272">0</span></span>                                                         |
| <span data-ttu-id="3502b-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3502b-273">Range-Upper</span></span>            | <span data-ttu-id="3502b-274">2048</span><span class="sxs-lookup"><span data-stu-id="3502b-274">2048</span></span>                                                      |
| <span data-ttu-id="3502b-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3502b-275">Search-Flags</span></span>           | <span data-ttu-id="3502b-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3502b-276">0x00000000</span></span>                                                |
| <span data-ttu-id="3502b-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3502b-277">System-Flags</span></span>           | <span data-ttu-id="3502b-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3502b-278">0x00000010</span></span>                                                |
| <span data-ttu-id="3502b-279">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3502b-279">Classes used in</span></span>        | [<span data-ttu-id="3502b-280">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="3502b-280">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





