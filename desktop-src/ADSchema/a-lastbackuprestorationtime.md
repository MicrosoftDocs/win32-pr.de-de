---
title: Letztes Backup-Wiederherstellungszeit Attribut
description: Zeitpunkt der letzten Systemwiederherstellung.
ms.assetid: 44850c16-3f17-4883-9a54-3e82ca7d63da
ms.tgt_platform: multiple
keywords:
- AD-Schema für die letzte Sicherung-Wiederherstellungszeit des Attributs
- lastbackuprestorationtime-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Last-Backup-Restoration-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9220d06a4cdd562599611d2ad19cf09fa279ef3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104041036"
---
# <a name="last-backup-restoration-time-attribute"></a><span data-ttu-id="165ce-105">Letztes Backup-Wiederherstellungszeit Attribut</span><span class="sxs-lookup"><span data-stu-id="165ce-105">Last-Backup-Restoration-Time attribute</span></span>

<span data-ttu-id="165ce-106">Zeitpunkt der letzten Systemwiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="165ce-106">When the last system restore occurred.</span></span>



| <span data-ttu-id="165ce-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="165ce-107">Entry</span></span> | <span data-ttu-id="165ce-108">Wert</span><span class="sxs-lookup"><span data-stu-id="165ce-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="165ce-109">CN</span><span class="sxs-lookup"><span data-stu-id="165ce-109">CN</span></span>                | <span data-ttu-id="165ce-110">Letzte Sicherung-Wiederherstellungszeit</span><span class="sxs-lookup"><span data-stu-id="165ce-110">Last-Backup-Restoration-Time</span></span>         |
| <span data-ttu-id="165ce-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="165ce-111">Ldap-Display-Name</span></span> | <span data-ttu-id="165ce-112">lastbackuprestorationtime</span><span class="sxs-lookup"><span data-stu-id="165ce-112">lastBackupRestorationTime</span></span>            |
| <span data-ttu-id="165ce-113">Size</span><span class="sxs-lookup"><span data-stu-id="165ce-113">Size</span></span>              | <span data-ttu-id="165ce-114">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="165ce-114">8 bytes</span></span>                              |
| <span data-ttu-id="165ce-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="165ce-115">Update Privilege</span></span>  | <span data-ttu-id="165ce-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="165ce-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="165ce-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="165ce-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="165ce-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="165ce-118">Attribute-Id</span></span>      | <span data-ttu-id="165ce-119">1.2.840.113556.1.4.519</span><span class="sxs-lookup"><span data-stu-id="165ce-119">1.2.840.113556.1.4.519</span></span>               |
| <span data-ttu-id="165ce-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="165ce-120">System-Id-Guid</span></span>    | <span data-ttu-id="165ce-121">1fbb0be8-BA63-11D0-Afef-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="165ce-121">1fbb0be8-ba63-11d0-afef-0000f80367c1</span></span> |
| <span data-ttu-id="165ce-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="165ce-122">Syntax</span></span>            | [<span data-ttu-id="165ce-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="165ce-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="165ce-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="165ce-124">Implementations</span></span>

-   [<span data-ttu-id="165ce-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="165ce-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="165ce-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="165ce-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="165ce-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="165ce-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="165ce-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="165ce-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="165ce-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="165ce-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="165ce-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="165ce-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="165ce-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="165ce-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="165ce-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="165ce-132">Windows 2000 Server</span></span>



| <span data-ttu-id="165ce-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="165ce-133">Entry</span></span> | <span data-ttu-id="165ce-134">Wert</span><span class="sxs-lookup"><span data-stu-id="165ce-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="165ce-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="165ce-135">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="165ce-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="165ce-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="165ce-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="165ce-137">System-Only</span></span>            | <span data-ttu-id="165ce-138">False</span><span class="sxs-lookup"><span data-stu-id="165ce-138">False</span></span>                                    |
| <span data-ttu-id="165ce-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="165ce-139">Is-Single-Valued</span></span>       | <span data-ttu-id="165ce-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="165ce-140">True</span></span>                                     |
| <span data-ttu-id="165ce-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="165ce-141">Is Indexed</span></span>             | <span data-ttu-id="165ce-142">False</span><span class="sxs-lookup"><span data-stu-id="165ce-142">False</span></span>                                    |
| <span data-ttu-id="165ce-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="165ce-143">In Global Catalog</span></span>      | <span data-ttu-id="165ce-144">False</span><span class="sxs-lookup"><span data-stu-id="165ce-144">False</span></span>                                    |
| <span data-ttu-id="165ce-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="165ce-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="165ce-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="165ce-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="165ce-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="165ce-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="165ce-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="165ce-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="165ce-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="165ce-149">Search-Flags</span></span>           | <span data-ttu-id="165ce-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="165ce-150">0x00000000</span></span>                               |
| <span data-ttu-id="165ce-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="165ce-151">System-Flags</span></span>           | <span data-ttu-id="165ce-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="165ce-152">0x00000010</span></span>                               |
| <span data-ttu-id="165ce-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="165ce-153">Classes used in</span></span>        | [<span data-ttu-id="165ce-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="165ce-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="165ce-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="165ce-155">Windows Server 2003</span></span>



| <span data-ttu-id="165ce-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="165ce-156">Entry</span></span> | <span data-ttu-id="165ce-157">Wert</span><span class="sxs-lookup"><span data-stu-id="165ce-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="165ce-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="165ce-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="165ce-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="165ce-159">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="165ce-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="165ce-160">System-Only</span></span>            | <span data-ttu-id="165ce-161">False</span><span class="sxs-lookup"><span data-stu-id="165ce-161">False</span></span>                                    |
| <span data-ttu-id="165ce-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="165ce-162">Is-Single-Valued</span></span>       | <span data-ttu-id="165ce-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="165ce-163">True</span></span>                                     |
| <span data-ttu-id="165ce-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="165ce-164">Is Indexed</span></span>             | <span data-ttu-id="165ce-165">False</span><span class="sxs-lookup"><span data-stu-id="165ce-165">False</span></span>                                    |
| <span data-ttu-id="165ce-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="165ce-166">In Global Catalog</span></span>      | <span data-ttu-id="165ce-167">False</span><span class="sxs-lookup"><span data-stu-id="165ce-167">False</span></span>                                    |
| <span data-ttu-id="165ce-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="165ce-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="165ce-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="165ce-169">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="165ce-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="165ce-170">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="165ce-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="165ce-171">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="165ce-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="165ce-172">Search-Flags</span></span>           | <span data-ttu-id="165ce-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="165ce-173">0x00000000</span></span>                               |
| <span data-ttu-id="165ce-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="165ce-174">System-Flags</span></span>           | <span data-ttu-id="165ce-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="165ce-175">0x00000010</span></span>                               |
| <span data-ttu-id="165ce-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="165ce-176">Classes used in</span></span>        | [<span data-ttu-id="165ce-177">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="165ce-177">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="165ce-178">Adam</span><span class="sxs-lookup"><span data-stu-id="165ce-178">ADAM</span></span>



| <span data-ttu-id="165ce-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="165ce-179">Entry</span></span> | <span data-ttu-id="165ce-180">Wert</span><span class="sxs-lookup"><span data-stu-id="165ce-180">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="165ce-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="165ce-181">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="165ce-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="165ce-182">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="165ce-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="165ce-183">System-Only</span></span>            | <span data-ttu-id="165ce-184">False</span><span class="sxs-lookup"><span data-stu-id="165ce-184">False</span></span>                                    |
| <span data-ttu-id="165ce-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="165ce-185">Is-Single-Valued</span></span>       | <span data-ttu-id="165ce-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="165ce-186">True</span></span>                                     |
| <span data-ttu-id="165ce-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="165ce-187">Is Indexed</span></span>             | <span data-ttu-id="165ce-188">False</span><span class="sxs-lookup"><span data-stu-id="165ce-188">False</span></span>                                    |
| <span data-ttu-id="165ce-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="165ce-189">In Global Catalog</span></span>      | <span data-ttu-id="165ce-190">False</span><span class="sxs-lookup"><span data-stu-id="165ce-190">False</span></span>                                    |
| <span data-ttu-id="165ce-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="165ce-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="165ce-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="165ce-192">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="165ce-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="165ce-193">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="165ce-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="165ce-194">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="165ce-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="165ce-195">Search-Flags</span></span>           | <span data-ttu-id="165ce-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="165ce-196">0x00000000</span></span>                               |
| <span data-ttu-id="165ce-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="165ce-197">System-Flags</span></span>           | <span data-ttu-id="165ce-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="165ce-198">0x00000010</span></span>                               |
| <span data-ttu-id="165ce-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="165ce-199">Classes used in</span></span>        | [<span data-ttu-id="165ce-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="165ce-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="165ce-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="165ce-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="165ce-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="165ce-202">Entry</span></span> | <span data-ttu-id="165ce-203">Wert</span><span class="sxs-lookup"><span data-stu-id="165ce-203">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="165ce-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="165ce-204">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="165ce-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="165ce-205">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="165ce-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="165ce-206">System-Only</span></span>            | <span data-ttu-id="165ce-207">False</span><span class="sxs-lookup"><span data-stu-id="165ce-207">False</span></span>                                    |
| <span data-ttu-id="165ce-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="165ce-208">Is-Single-Valued</span></span>       | <span data-ttu-id="165ce-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="165ce-209">True</span></span>                                     |
| <span data-ttu-id="165ce-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="165ce-210">Is Indexed</span></span>             | <span data-ttu-id="165ce-211">False</span><span class="sxs-lookup"><span data-stu-id="165ce-211">False</span></span>                                    |
| <span data-ttu-id="165ce-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="165ce-212">In Global Catalog</span></span>      | <span data-ttu-id="165ce-213">False</span><span class="sxs-lookup"><span data-stu-id="165ce-213">False</span></span>                                    |
| <span data-ttu-id="165ce-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="165ce-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="165ce-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="165ce-215">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="165ce-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="165ce-216">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="165ce-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="165ce-217">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="165ce-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="165ce-218">Search-Flags</span></span>           | <span data-ttu-id="165ce-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="165ce-219">0x00000000</span></span>                               |
| <span data-ttu-id="165ce-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="165ce-220">System-Flags</span></span>           | <span data-ttu-id="165ce-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="165ce-221">0x00000010</span></span>                               |
| <span data-ttu-id="165ce-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="165ce-222">Classes used in</span></span>        | [<span data-ttu-id="165ce-223">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="165ce-223">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="165ce-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="165ce-224">Windows Server 2008</span></span>



| <span data-ttu-id="165ce-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="165ce-225">Entry</span></span> | <span data-ttu-id="165ce-226">Wert</span><span class="sxs-lookup"><span data-stu-id="165ce-226">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="165ce-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="165ce-227">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="165ce-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="165ce-228">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="165ce-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="165ce-229">System-Only</span></span>            | <span data-ttu-id="165ce-230">False</span><span class="sxs-lookup"><span data-stu-id="165ce-230">False</span></span>                                    |
| <span data-ttu-id="165ce-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="165ce-231">Is-Single-Valued</span></span>       | <span data-ttu-id="165ce-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="165ce-232">True</span></span>                                     |
| <span data-ttu-id="165ce-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="165ce-233">Is Indexed</span></span>             | <span data-ttu-id="165ce-234">False</span><span class="sxs-lookup"><span data-stu-id="165ce-234">False</span></span>                                    |
| <span data-ttu-id="165ce-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="165ce-235">In Global Catalog</span></span>      | <span data-ttu-id="165ce-236">False</span><span class="sxs-lookup"><span data-stu-id="165ce-236">False</span></span>                                    |
| <span data-ttu-id="165ce-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="165ce-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="165ce-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="165ce-238">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="165ce-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="165ce-239">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="165ce-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="165ce-240">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="165ce-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="165ce-241">Search-Flags</span></span>           | <span data-ttu-id="165ce-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="165ce-242">0x00000000</span></span>                               |
| <span data-ttu-id="165ce-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="165ce-243">System-Flags</span></span>           | <span data-ttu-id="165ce-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="165ce-244">0x00000010</span></span>                               |
| <span data-ttu-id="165ce-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="165ce-245">Classes used in</span></span>        | [<span data-ttu-id="165ce-246">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="165ce-246">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="165ce-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="165ce-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="165ce-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="165ce-248">Entry</span></span> | <span data-ttu-id="165ce-249">Wert</span><span class="sxs-lookup"><span data-stu-id="165ce-249">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="165ce-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="165ce-250">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="165ce-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="165ce-251">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="165ce-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="165ce-252">System-Only</span></span>            | <span data-ttu-id="165ce-253">False</span><span class="sxs-lookup"><span data-stu-id="165ce-253">False</span></span>                                    |
| <span data-ttu-id="165ce-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="165ce-254">Is-Single-Valued</span></span>       | <span data-ttu-id="165ce-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="165ce-255">True</span></span>                                     |
| <span data-ttu-id="165ce-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="165ce-256">Is Indexed</span></span>             | <span data-ttu-id="165ce-257">False</span><span class="sxs-lookup"><span data-stu-id="165ce-257">False</span></span>                                    |
| <span data-ttu-id="165ce-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="165ce-258">In Global Catalog</span></span>      | <span data-ttu-id="165ce-259">False</span><span class="sxs-lookup"><span data-stu-id="165ce-259">False</span></span>                                    |
| <span data-ttu-id="165ce-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="165ce-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="165ce-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="165ce-261">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="165ce-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="165ce-262">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="165ce-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="165ce-263">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="165ce-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="165ce-264">Search-Flags</span></span>           | <span data-ttu-id="165ce-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="165ce-265">0x00000000</span></span>                               |
| <span data-ttu-id="165ce-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="165ce-266">System-Flags</span></span>           | <span data-ttu-id="165ce-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="165ce-267">0x00000010</span></span>                               |
| <span data-ttu-id="165ce-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="165ce-268">Classes used in</span></span>        | [<span data-ttu-id="165ce-269">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="165ce-269">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="165ce-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="165ce-270">Windows Server 2012</span></span>



| <span data-ttu-id="165ce-271">Eingabe</span><span class="sxs-lookup"><span data-stu-id="165ce-271">Entry</span></span> | <span data-ttu-id="165ce-272">Wert</span><span class="sxs-lookup"><span data-stu-id="165ce-272">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="165ce-273">Link-ID</span><span class="sxs-lookup"><span data-stu-id="165ce-273">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="165ce-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="165ce-274">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="165ce-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="165ce-275">System-Only</span></span>            | <span data-ttu-id="165ce-276">False</span><span class="sxs-lookup"><span data-stu-id="165ce-276">False</span></span>                                    |
| <span data-ttu-id="165ce-277">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="165ce-277">Is-Single-Valued</span></span>       | <span data-ttu-id="165ce-278">Richtig</span><span class="sxs-lookup"><span data-stu-id="165ce-278">True</span></span>                                     |
| <span data-ttu-id="165ce-279">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="165ce-279">Is Indexed</span></span>             | <span data-ttu-id="165ce-280">False</span><span class="sxs-lookup"><span data-stu-id="165ce-280">False</span></span>                                    |
| <span data-ttu-id="165ce-281">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="165ce-281">In Global Catalog</span></span>      | <span data-ttu-id="165ce-282">False</span><span class="sxs-lookup"><span data-stu-id="165ce-282">False</span></span>                                    |
| <span data-ttu-id="165ce-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="165ce-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="165ce-284">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="165ce-284">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="165ce-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="165ce-285">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="165ce-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="165ce-286">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="165ce-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="165ce-287">Search-Flags</span></span>           | <span data-ttu-id="165ce-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="165ce-288">0x00000000</span></span>                               |
| <span data-ttu-id="165ce-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="165ce-289">System-Flags</span></span>           | <span data-ttu-id="165ce-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="165ce-290">0x00000010</span></span>                               |
| <span data-ttu-id="165ce-291">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="165ce-291">Classes used in</span></span>        | [<span data-ttu-id="165ce-292">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="165ce-292">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





