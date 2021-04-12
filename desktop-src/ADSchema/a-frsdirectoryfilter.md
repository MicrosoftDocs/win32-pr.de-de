---
title: FRS-Directory-Filter-Attribut
description: Die Liste der Verzeichnisse, die von der Datei Replikation ausgeschlossen sind, z. b. Temp oder obj.
ms.assetid: 3ce37a96-0cb2-46bf-aad1-80fc1304855d
ms.tgt_platform: multiple
keywords:
- AD-Schema für das FRS-Verzeichnis-Filter-Attribut
- Schema des fRSDirectoryFilter-Attributs
topic_type:
- apiref
api_name:
- FRS-Directory-Filter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b547cd431d7f51af698a137b7edd7dd299a3ec2f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479698"
---
# <a name="frs-directory-filter-attribute"></a><span data-ttu-id="e31b1-105">FRS-Directory-Filter-Attribut</span><span class="sxs-lookup"><span data-stu-id="e31b1-105">FRS-Directory-Filter attribute</span></span>

<span data-ttu-id="e31b1-106">Die Liste der Verzeichnisse, die von der Datei Replikation ausgeschlossen sind, z. b. Temp oder obj.</span><span class="sxs-lookup"><span data-stu-id="e31b1-106">The list of directories excluded from file replication, for example, temp, or obj.</span></span>



| <span data-ttu-id="e31b1-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e31b1-107">Entry</span></span> | <span data-ttu-id="e31b1-108">Wert</span><span class="sxs-lookup"><span data-stu-id="e31b1-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e31b1-109">CN</span><span class="sxs-lookup"><span data-stu-id="e31b1-109">CN</span></span>                | <span data-ttu-id="e31b1-110">FRS-Verzeichnis-Filter</span><span class="sxs-lookup"><span data-stu-id="e31b1-110">FRS-Directory-Filter</span></span>                        |
| <span data-ttu-id="e31b1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e31b1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e31b1-112">frsdirecteryfilter</span><span class="sxs-lookup"><span data-stu-id="e31b1-112">fRSDirectoryFilter</span></span>                          |
| <span data-ttu-id="e31b1-113">Size</span><span class="sxs-lookup"><span data-stu-id="e31b1-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="e31b1-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e31b1-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="e31b1-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="e31b1-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="e31b1-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e31b1-116">Attribute-Id</span></span>      | <span data-ttu-id="e31b1-117">1.2.840.113556.1.4.484</span><span class="sxs-lookup"><span data-stu-id="e31b1-117">1.2.840.113556.1.4.484</span></span>                      |
| <span data-ttu-id="e31b1-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e31b1-118">System-Id-Guid</span></span>    | <span data-ttu-id="e31b1-119">1be8f171-a9ff-11D0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="e31b1-119">1be8f171-a9ff-11d0-afe2-00c04fd930c9</span></span>        |
| <span data-ttu-id="e31b1-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="e31b1-120">Syntax</span></span>            | [<span data-ttu-id="e31b1-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e31b1-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e31b1-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="e31b1-122">Implementations</span></span>

-   [<span data-ttu-id="e31b1-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e31b1-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e31b1-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e31b1-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e31b1-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e31b1-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e31b1-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e31b1-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e31b1-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e31b1-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e31b1-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e31b1-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e31b1-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e31b1-129">Windows 2000 Server</span></span>



| <span data-ttu-id="e31b1-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e31b1-130">Entry</span></span> | <span data-ttu-id="e31b1-131">Wert</span><span class="sxs-lookup"><span data-stu-id="e31b1-131">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e31b1-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e31b1-132">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e31b1-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e31b1-133">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e31b1-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="e31b1-134">System-Only</span></span>            | <span data-ttu-id="e31b1-135">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-135">False</span></span>                                                     |
| <span data-ttu-id="e31b1-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e31b1-136">Is-Single-Valued</span></span>       | <span data-ttu-id="e31b1-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="e31b1-137">True</span></span>                                                      |
| <span data-ttu-id="e31b1-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e31b1-138">Is Indexed</span></span>             | <span data-ttu-id="e31b1-139">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-139">False</span></span>                                                     |
| <span data-ttu-id="e31b1-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e31b1-140">In Global Catalog</span></span>      | <span data-ttu-id="e31b1-141">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-141">False</span></span>                                                     |
| <span data-ttu-id="e31b1-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e31b1-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="e31b1-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e31b1-143">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e31b1-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e31b1-144">Range-Lower</span></span>            | <span data-ttu-id="e31b1-145">0</span><span class="sxs-lookup"><span data-stu-id="e31b1-145">0</span></span>                                                         |
| <span data-ttu-id="e31b1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e31b1-146">Range-Upper</span></span>            | <span data-ttu-id="e31b1-147">2048</span><span class="sxs-lookup"><span data-stu-id="e31b1-147">2048</span></span>                                                      |
| <span data-ttu-id="e31b1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e31b1-148">Search-Flags</span></span>           | <span data-ttu-id="e31b1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e31b1-149">0x00000000</span></span>                                                |
| <span data-ttu-id="e31b1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e31b1-150">System-Flags</span></span>           | <span data-ttu-id="e31b1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e31b1-151">0x00000010</span></span>                                                |
| <span data-ttu-id="e31b1-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e31b1-152">Classes used in</span></span>        | [<span data-ttu-id="e31b1-153">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="e31b1-153">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e31b1-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e31b1-154">Windows Server 2003</span></span>



| <span data-ttu-id="e31b1-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e31b1-155">Entry</span></span> | <span data-ttu-id="e31b1-156">Wert</span><span class="sxs-lookup"><span data-stu-id="e31b1-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e31b1-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e31b1-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e31b1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e31b1-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e31b1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e31b1-159">System-Only</span></span>            | <span data-ttu-id="e31b1-160">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-160">False</span></span>                                                     |
| <span data-ttu-id="e31b1-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e31b1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e31b1-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="e31b1-162">True</span></span>                                                      |
| <span data-ttu-id="e31b1-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e31b1-163">Is Indexed</span></span>             | <span data-ttu-id="e31b1-164">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-164">False</span></span>                                                     |
| <span data-ttu-id="e31b1-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e31b1-165">In Global Catalog</span></span>      | <span data-ttu-id="e31b1-166">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-166">False</span></span>                                                     |
| <span data-ttu-id="e31b1-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e31b1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e31b1-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e31b1-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e31b1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e31b1-169">Range-Lower</span></span>            | <span data-ttu-id="e31b1-170">0</span><span class="sxs-lookup"><span data-stu-id="e31b1-170">0</span></span>                                                         |
| <span data-ttu-id="e31b1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e31b1-171">Range-Upper</span></span>            | <span data-ttu-id="e31b1-172">2048</span><span class="sxs-lookup"><span data-stu-id="e31b1-172">2048</span></span>                                                      |
| <span data-ttu-id="e31b1-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e31b1-173">Search-Flags</span></span>           | <span data-ttu-id="e31b1-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e31b1-174">0x00000000</span></span>                                                |
| <span data-ttu-id="e31b1-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e31b1-175">System-Flags</span></span>           | <span data-ttu-id="e31b1-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e31b1-176">0x00000010</span></span>                                                |
| <span data-ttu-id="e31b1-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e31b1-177">Classes used in</span></span>        | [<span data-ttu-id="e31b1-178">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="e31b1-178">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e31b1-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e31b1-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e31b1-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e31b1-180">Entry</span></span> | <span data-ttu-id="e31b1-181">Wert</span><span class="sxs-lookup"><span data-stu-id="e31b1-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e31b1-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e31b1-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e31b1-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e31b1-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e31b1-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="e31b1-184">System-Only</span></span>            | <span data-ttu-id="e31b1-185">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-185">False</span></span>                                                     |
| <span data-ttu-id="e31b1-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e31b1-186">Is-Single-Valued</span></span>       | <span data-ttu-id="e31b1-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="e31b1-187">True</span></span>                                                      |
| <span data-ttu-id="e31b1-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e31b1-188">Is Indexed</span></span>             | <span data-ttu-id="e31b1-189">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-189">False</span></span>                                                     |
| <span data-ttu-id="e31b1-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e31b1-190">In Global Catalog</span></span>      | <span data-ttu-id="e31b1-191">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-191">False</span></span>                                                     |
| <span data-ttu-id="e31b1-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e31b1-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="e31b1-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e31b1-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e31b1-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e31b1-194">Range-Lower</span></span>            | <span data-ttu-id="e31b1-195">0</span><span class="sxs-lookup"><span data-stu-id="e31b1-195">0</span></span>                                                         |
| <span data-ttu-id="e31b1-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e31b1-196">Range-Upper</span></span>            | <span data-ttu-id="e31b1-197">2048</span><span class="sxs-lookup"><span data-stu-id="e31b1-197">2048</span></span>                                                      |
| <span data-ttu-id="e31b1-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e31b1-198">Search-Flags</span></span>           | <span data-ttu-id="e31b1-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e31b1-199">0x00000000</span></span>                                                |
| <span data-ttu-id="e31b1-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e31b1-200">System-Flags</span></span>           | <span data-ttu-id="e31b1-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e31b1-201">0x00000010</span></span>                                                |
| <span data-ttu-id="e31b1-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e31b1-202">Classes used in</span></span>        | [<span data-ttu-id="e31b1-203">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="e31b1-203">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e31b1-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e31b1-204">Windows Server 2008</span></span>



| <span data-ttu-id="e31b1-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e31b1-205">Entry</span></span> | <span data-ttu-id="e31b1-206">Wert</span><span class="sxs-lookup"><span data-stu-id="e31b1-206">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e31b1-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e31b1-207">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e31b1-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e31b1-208">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e31b1-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="e31b1-209">System-Only</span></span>            | <span data-ttu-id="e31b1-210">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-210">False</span></span>                                                     |
| <span data-ttu-id="e31b1-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e31b1-211">Is-Single-Valued</span></span>       | <span data-ttu-id="e31b1-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="e31b1-212">True</span></span>                                                      |
| <span data-ttu-id="e31b1-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e31b1-213">Is Indexed</span></span>             | <span data-ttu-id="e31b1-214">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-214">False</span></span>                                                     |
| <span data-ttu-id="e31b1-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e31b1-215">In Global Catalog</span></span>      | <span data-ttu-id="e31b1-216">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-216">False</span></span>                                                     |
| <span data-ttu-id="e31b1-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e31b1-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="e31b1-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e31b1-218">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e31b1-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e31b1-219">Range-Lower</span></span>            | <span data-ttu-id="e31b1-220">0</span><span class="sxs-lookup"><span data-stu-id="e31b1-220">0</span></span>                                                         |
| <span data-ttu-id="e31b1-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e31b1-221">Range-Upper</span></span>            | <span data-ttu-id="e31b1-222">2048</span><span class="sxs-lookup"><span data-stu-id="e31b1-222">2048</span></span>                                                      |
| <span data-ttu-id="e31b1-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e31b1-223">Search-Flags</span></span>           | <span data-ttu-id="e31b1-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e31b1-224">0x00000000</span></span>                                                |
| <span data-ttu-id="e31b1-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e31b1-225">System-Flags</span></span>           | <span data-ttu-id="e31b1-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e31b1-226">0x00000010</span></span>                                                |
| <span data-ttu-id="e31b1-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e31b1-227">Classes used in</span></span>        | [<span data-ttu-id="e31b1-228">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="e31b1-228">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e31b1-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e31b1-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e31b1-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e31b1-230">Entry</span></span> | <span data-ttu-id="e31b1-231">Wert</span><span class="sxs-lookup"><span data-stu-id="e31b1-231">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e31b1-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e31b1-232">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e31b1-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e31b1-233">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e31b1-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="e31b1-234">System-Only</span></span>            | <span data-ttu-id="e31b1-235">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-235">False</span></span>                                                     |
| <span data-ttu-id="e31b1-236">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e31b1-236">Is-Single-Valued</span></span>       | <span data-ttu-id="e31b1-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="e31b1-237">True</span></span>                                                      |
| <span data-ttu-id="e31b1-238">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e31b1-238">Is Indexed</span></span>             | <span data-ttu-id="e31b1-239">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-239">False</span></span>                                                     |
| <span data-ttu-id="e31b1-240">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e31b1-240">In Global Catalog</span></span>      | <span data-ttu-id="e31b1-241">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-241">False</span></span>                                                     |
| <span data-ttu-id="e31b1-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e31b1-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="e31b1-243">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e31b1-243">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e31b1-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e31b1-244">Range-Lower</span></span>            | <span data-ttu-id="e31b1-245">0</span><span class="sxs-lookup"><span data-stu-id="e31b1-245">0</span></span>                                                         |
| <span data-ttu-id="e31b1-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e31b1-246">Range-Upper</span></span>            | <span data-ttu-id="e31b1-247">2048</span><span class="sxs-lookup"><span data-stu-id="e31b1-247">2048</span></span>                                                      |
| <span data-ttu-id="e31b1-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e31b1-248">Search-Flags</span></span>           | <span data-ttu-id="e31b1-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e31b1-249">0x00000000</span></span>                                                |
| <span data-ttu-id="e31b1-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e31b1-250">System-Flags</span></span>           | <span data-ttu-id="e31b1-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e31b1-251">0x00000010</span></span>                                                |
| <span data-ttu-id="e31b1-252">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e31b1-252">Classes used in</span></span>        | [<span data-ttu-id="e31b1-253">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="e31b1-253">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e31b1-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e31b1-254">Windows Server 2012</span></span>



| <span data-ttu-id="e31b1-255">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e31b1-255">Entry</span></span> | <span data-ttu-id="e31b1-256">Wert</span><span class="sxs-lookup"><span data-stu-id="e31b1-256">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e31b1-257">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e31b1-257">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e31b1-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e31b1-258">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e31b1-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="e31b1-259">System-Only</span></span>            | <span data-ttu-id="e31b1-260">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-260">False</span></span>                                                     |
| <span data-ttu-id="e31b1-261">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e31b1-261">Is-Single-Valued</span></span>       | <span data-ttu-id="e31b1-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="e31b1-262">True</span></span>                                                      |
| <span data-ttu-id="e31b1-263">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e31b1-263">Is Indexed</span></span>             | <span data-ttu-id="e31b1-264">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-264">False</span></span>                                                     |
| <span data-ttu-id="e31b1-265">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e31b1-265">In Global Catalog</span></span>      | <span data-ttu-id="e31b1-266">False</span><span class="sxs-lookup"><span data-stu-id="e31b1-266">False</span></span>                                                     |
| <span data-ttu-id="e31b1-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e31b1-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="e31b1-268">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e31b1-268">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e31b1-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e31b1-269">Range-Lower</span></span>            | <span data-ttu-id="e31b1-270">0</span><span class="sxs-lookup"><span data-stu-id="e31b1-270">0</span></span>                                                         |
| <span data-ttu-id="e31b1-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e31b1-271">Range-Upper</span></span>            | <span data-ttu-id="e31b1-272">2048</span><span class="sxs-lookup"><span data-stu-id="e31b1-272">2048</span></span>                                                      |
| <span data-ttu-id="e31b1-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e31b1-273">Search-Flags</span></span>           | <span data-ttu-id="e31b1-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e31b1-274">0x00000000</span></span>                                                |
| <span data-ttu-id="e31b1-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e31b1-275">System-Flags</span></span>           | <span data-ttu-id="e31b1-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e31b1-276">0x00000010</span></span>                                                |
| <span data-ttu-id="e31b1-277">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e31b1-277">Classes used in</span></span>        | [<span data-ttu-id="e31b1-278">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="e31b1-278">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





