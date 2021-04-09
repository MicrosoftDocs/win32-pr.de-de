---
title: Tombstone-Lifetime-Attribut
description: Die Anzahl der Tage, bevor ein gelöschtes Objekt aus den Verzeichnisdiensten entfernt wird.
ms.assetid: 58898097-912b-4fe6-b6ea-91f49aaa2b1b
ms.tgt_platform: multiple
keywords:
- AD-Schema für Tombstone-Lifetime-Attribut
- tombstoneLifetime-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Tombstone-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb2bd0b7b970270c626437ee65288fd07bf48272
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859747"
---
# <a name="tombstone-lifetime-attribute"></a><span data-ttu-id="945de-105">Tombstone-Lifetime-Attribut</span><span class="sxs-lookup"><span data-stu-id="945de-105">Tombstone-Lifetime attribute</span></span>

<span data-ttu-id="945de-106">Die Anzahl der Tage, bevor ein gelöschtes Objekt aus den Verzeichnisdiensten entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="945de-106">The number of days before a deleted object is removed from the directory services.</span></span> <span data-ttu-id="945de-107">Dies hilft beim Entfernen von Objekten von replizierten Servern und verhindert, dass Wiederherstellungen ein gelöschtes Objekt erneut einführen.</span><span class="sxs-lookup"><span data-stu-id="945de-107">This assists in removing objects from replicated servers and preventing restores from reintroducing a deleted object.</span></span> <span data-ttu-id="945de-108">Dieser Wert befindet sich im Verzeichnisdienst Objekt in der Konfigurations-NIC.</span><span class="sxs-lookup"><span data-stu-id="945de-108">This value is in the Directory Service object in the configuration NIC.</span></span>



| <span data-ttu-id="945de-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="945de-109">Entry</span></span> | <span data-ttu-id="945de-110">Wert</span><span class="sxs-lookup"><span data-stu-id="945de-110">Value</span></span> |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="945de-111">CN</span><span class="sxs-lookup"><span data-stu-id="945de-111">CN</span></span>                | <span data-ttu-id="945de-112">Tombstone-Lifetime</span><span class="sxs-lookup"><span data-stu-id="945de-112">Tombstone-Lifetime</span></span>                                        |
| <span data-ttu-id="945de-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="945de-113">Ldap-Display-Name</span></span> | <span data-ttu-id="945de-114">tombstoneLifetime</span><span class="sxs-lookup"><span data-stu-id="945de-114">tombstoneLifetime</span></span>                                         |
| <span data-ttu-id="945de-115">Size</span><span class="sxs-lookup"><span data-stu-id="945de-115">Size</span></span>              | <span data-ttu-id="945de-116">4 Bytes.</span><span class="sxs-lookup"><span data-stu-id="945de-116">4 bytes.</span></span> <span data-ttu-id="945de-117">Der Standardwert ist 60 Tage, wenn kein Wert eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="945de-117">The default is 60 days when no value is entered.</span></span> |
| <span data-ttu-id="945de-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="945de-118">Update Privilege</span></span>  | \-                                                        |
| <span data-ttu-id="945de-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="945de-119">Update Frequency</span></span>  | \-                                                        |
| <span data-ttu-id="945de-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="945de-120">Attribute-Id</span></span>      | <span data-ttu-id="945de-121">1.2.840.113556.1.2.54</span><span class="sxs-lookup"><span data-stu-id="945de-121">1.2.840.113556.1.2.54</span></span>                                     |
| <span data-ttu-id="945de-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="945de-122">System-Id-Guid</span></span>    | <span data-ttu-id="945de-123">16c3a860-1273-11D0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="945de-123">16c3a860-1273-11d0-a060-00aa006c33ed</span></span>                      |
| <span data-ttu-id="945de-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="945de-124">Syntax</span></span>            | [<span data-ttu-id="945de-125">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="945de-125">**Enumeration**</span></span>](s-enumeration.md)                      |



## <a name="implementations"></a><span data-ttu-id="945de-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="945de-126">Implementations</span></span>

-   [<span data-ttu-id="945de-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="945de-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="945de-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="945de-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="945de-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="945de-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="945de-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="945de-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="945de-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="945de-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="945de-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="945de-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="945de-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="945de-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="945de-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="945de-134">Windows 2000 Server</span></span>



| <span data-ttu-id="945de-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="945de-135">Entry</span></span> | <span data-ttu-id="945de-136">Wert</span><span class="sxs-lookup"><span data-stu-id="945de-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="945de-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="945de-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="945de-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="945de-138">MAPI-Id</span></span>                | <span data-ttu-id="945de-139">0x8145</span><span class="sxs-lookup"><span data-stu-id="945de-139">0x8145</span></span>                                           |
| <span data-ttu-id="945de-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="945de-140">System-Only</span></span>            | <span data-ttu-id="945de-141">False</span><span class="sxs-lookup"><span data-stu-id="945de-141">False</span></span>                                            |
| <span data-ttu-id="945de-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="945de-142">Is-Single-Valued</span></span>       | <span data-ttu-id="945de-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="945de-143">True</span></span>                                             |
| <span data-ttu-id="945de-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="945de-144">Is Indexed</span></span>             | <span data-ttu-id="945de-145">False</span><span class="sxs-lookup"><span data-stu-id="945de-145">False</span></span>                                            |
| <span data-ttu-id="945de-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="945de-146">In Global Catalog</span></span>      | <span data-ttu-id="945de-147">False</span><span class="sxs-lookup"><span data-stu-id="945de-147">False</span></span>                                            |
| <span data-ttu-id="945de-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="945de-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="945de-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="945de-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="945de-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="945de-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="945de-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="945de-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="945de-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="945de-152">Search-Flags</span></span>           | <span data-ttu-id="945de-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="945de-153">0x00000000</span></span>                                       |
| <span data-ttu-id="945de-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="945de-154">System-Flags</span></span>           | <span data-ttu-id="945de-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="945de-155">0x00000010</span></span>                                       |
| <span data-ttu-id="945de-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="945de-156">Classes used in</span></span>        | [<span data-ttu-id="945de-157">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="945de-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="945de-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="945de-158">Windows Server 2003</span></span>



| <span data-ttu-id="945de-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="945de-159">Entry</span></span> | <span data-ttu-id="945de-160">Wert</span><span class="sxs-lookup"><span data-stu-id="945de-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="945de-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="945de-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="945de-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="945de-162">MAPI-Id</span></span>                | <span data-ttu-id="945de-163">0x8145</span><span class="sxs-lookup"><span data-stu-id="945de-163">0x8145</span></span>                                           |
| <span data-ttu-id="945de-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="945de-164">System-Only</span></span>            | <span data-ttu-id="945de-165">False</span><span class="sxs-lookup"><span data-stu-id="945de-165">False</span></span>                                            |
| <span data-ttu-id="945de-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="945de-166">Is-Single-Valued</span></span>       | <span data-ttu-id="945de-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="945de-167">True</span></span>                                             |
| <span data-ttu-id="945de-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="945de-168">Is Indexed</span></span>             | <span data-ttu-id="945de-169">False</span><span class="sxs-lookup"><span data-stu-id="945de-169">False</span></span>                                            |
| <span data-ttu-id="945de-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="945de-170">In Global Catalog</span></span>      | <span data-ttu-id="945de-171">False</span><span class="sxs-lookup"><span data-stu-id="945de-171">False</span></span>                                            |
| <span data-ttu-id="945de-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="945de-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="945de-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="945de-173">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="945de-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="945de-174">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="945de-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="945de-175">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="945de-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="945de-176">Search-Flags</span></span>           | <span data-ttu-id="945de-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="945de-177">0x00000000</span></span>                                       |
| <span data-ttu-id="945de-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="945de-178">System-Flags</span></span>           | <span data-ttu-id="945de-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="945de-179">0x00000010</span></span>                                       |
| <span data-ttu-id="945de-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="945de-180">Classes used in</span></span>        | [<span data-ttu-id="945de-181">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="945de-181">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="945de-182">Adam</span><span class="sxs-lookup"><span data-stu-id="945de-182">ADAM</span></span>



| <span data-ttu-id="945de-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="945de-183">Entry</span></span> | <span data-ttu-id="945de-184">Wert</span><span class="sxs-lookup"><span data-stu-id="945de-184">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="945de-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="945de-185">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="945de-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="945de-186">MAPI-Id</span></span>                | <span data-ttu-id="945de-187">0x8145</span><span class="sxs-lookup"><span data-stu-id="945de-187">0x8145</span></span>                                           |
| <span data-ttu-id="945de-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="945de-188">System-Only</span></span>            | <span data-ttu-id="945de-189">False</span><span class="sxs-lookup"><span data-stu-id="945de-189">False</span></span>                                            |
| <span data-ttu-id="945de-190">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="945de-190">Is-Single-Valued</span></span>       | <span data-ttu-id="945de-191">Richtig</span><span class="sxs-lookup"><span data-stu-id="945de-191">True</span></span>                                             |
| <span data-ttu-id="945de-192">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="945de-192">Is Indexed</span></span>             | <span data-ttu-id="945de-193">False</span><span class="sxs-lookup"><span data-stu-id="945de-193">False</span></span>                                            |
| <span data-ttu-id="945de-194">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="945de-194">In Global Catalog</span></span>      | <span data-ttu-id="945de-195">False</span><span class="sxs-lookup"><span data-stu-id="945de-195">False</span></span>                                            |
| <span data-ttu-id="945de-196">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="945de-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="945de-197">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="945de-197">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="945de-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="945de-198">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="945de-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="945de-199">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="945de-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="945de-200">Search-Flags</span></span>           | <span data-ttu-id="945de-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="945de-201">0x00000000</span></span>                                       |
| <span data-ttu-id="945de-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="945de-202">System-Flags</span></span>           | <span data-ttu-id="945de-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="945de-203">0x00000010</span></span>                                       |
| <span data-ttu-id="945de-204">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="945de-204">Classes used in</span></span>        | [<span data-ttu-id="945de-205">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="945de-205">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="945de-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="945de-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="945de-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="945de-207">Entry</span></span> | <span data-ttu-id="945de-208">Wert</span><span class="sxs-lookup"><span data-stu-id="945de-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="945de-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="945de-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="945de-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="945de-210">MAPI-Id</span></span>                | <span data-ttu-id="945de-211">0x8145</span><span class="sxs-lookup"><span data-stu-id="945de-211">0x8145</span></span>                                           |
| <span data-ttu-id="945de-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="945de-212">System-Only</span></span>            | <span data-ttu-id="945de-213">False</span><span class="sxs-lookup"><span data-stu-id="945de-213">False</span></span>                                            |
| <span data-ttu-id="945de-214">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="945de-214">Is-Single-Valued</span></span>       | <span data-ttu-id="945de-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="945de-215">True</span></span>                                             |
| <span data-ttu-id="945de-216">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="945de-216">Is Indexed</span></span>             | <span data-ttu-id="945de-217">False</span><span class="sxs-lookup"><span data-stu-id="945de-217">False</span></span>                                            |
| <span data-ttu-id="945de-218">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="945de-218">In Global Catalog</span></span>      | <span data-ttu-id="945de-219">False</span><span class="sxs-lookup"><span data-stu-id="945de-219">False</span></span>                                            |
| <span data-ttu-id="945de-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="945de-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="945de-221">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="945de-221">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="945de-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="945de-222">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="945de-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="945de-223">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="945de-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="945de-224">Search-Flags</span></span>           | <span data-ttu-id="945de-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="945de-225">0x00000000</span></span>                                       |
| <span data-ttu-id="945de-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="945de-226">System-Flags</span></span>           | <span data-ttu-id="945de-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="945de-227">0x00000010</span></span>                                       |
| <span data-ttu-id="945de-228">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="945de-228">Classes used in</span></span>        | [<span data-ttu-id="945de-229">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="945de-229">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="945de-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="945de-230">Windows Server 2008</span></span>



| <span data-ttu-id="945de-231">Eingabe</span><span class="sxs-lookup"><span data-stu-id="945de-231">Entry</span></span> | <span data-ttu-id="945de-232">Wert</span><span class="sxs-lookup"><span data-stu-id="945de-232">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="945de-233">Link-ID</span><span class="sxs-lookup"><span data-stu-id="945de-233">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="945de-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="945de-234">MAPI-Id</span></span>                | <span data-ttu-id="945de-235">0x8145</span><span class="sxs-lookup"><span data-stu-id="945de-235">0x8145</span></span>                                           |
| <span data-ttu-id="945de-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="945de-236">System-Only</span></span>            | <span data-ttu-id="945de-237">False</span><span class="sxs-lookup"><span data-stu-id="945de-237">False</span></span>                                            |
| <span data-ttu-id="945de-238">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="945de-238">Is-Single-Valued</span></span>       | <span data-ttu-id="945de-239">Richtig</span><span class="sxs-lookup"><span data-stu-id="945de-239">True</span></span>                                             |
| <span data-ttu-id="945de-240">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="945de-240">Is Indexed</span></span>             | <span data-ttu-id="945de-241">False</span><span class="sxs-lookup"><span data-stu-id="945de-241">False</span></span>                                            |
| <span data-ttu-id="945de-242">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="945de-242">In Global Catalog</span></span>      | <span data-ttu-id="945de-243">False</span><span class="sxs-lookup"><span data-stu-id="945de-243">False</span></span>                                            |
| <span data-ttu-id="945de-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="945de-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="945de-245">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="945de-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="945de-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="945de-246">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="945de-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="945de-247">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="945de-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="945de-248">Search-Flags</span></span>           | <span data-ttu-id="945de-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="945de-249">0x00000000</span></span>                                       |
| <span data-ttu-id="945de-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="945de-250">System-Flags</span></span>           | <span data-ttu-id="945de-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="945de-251">0x00000010</span></span>                                       |
| <span data-ttu-id="945de-252">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="945de-252">Classes used in</span></span>        | [<span data-ttu-id="945de-253">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="945de-253">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="945de-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="945de-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="945de-255">Eingabe</span><span class="sxs-lookup"><span data-stu-id="945de-255">Entry</span></span> | <span data-ttu-id="945de-256">Wert</span><span class="sxs-lookup"><span data-stu-id="945de-256">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="945de-257">Link-ID</span><span class="sxs-lookup"><span data-stu-id="945de-257">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="945de-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="945de-258">MAPI-Id</span></span>                | <span data-ttu-id="945de-259">0x8145</span><span class="sxs-lookup"><span data-stu-id="945de-259">0x8145</span></span>                                           |
| <span data-ttu-id="945de-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="945de-260">System-Only</span></span>            | <span data-ttu-id="945de-261">False</span><span class="sxs-lookup"><span data-stu-id="945de-261">False</span></span>                                            |
| <span data-ttu-id="945de-262">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="945de-262">Is-Single-Valued</span></span>       | <span data-ttu-id="945de-263">Richtig</span><span class="sxs-lookup"><span data-stu-id="945de-263">True</span></span>                                             |
| <span data-ttu-id="945de-264">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="945de-264">Is Indexed</span></span>             | <span data-ttu-id="945de-265">False</span><span class="sxs-lookup"><span data-stu-id="945de-265">False</span></span>                                            |
| <span data-ttu-id="945de-266">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="945de-266">In Global Catalog</span></span>      | <span data-ttu-id="945de-267">False</span><span class="sxs-lookup"><span data-stu-id="945de-267">False</span></span>                                            |
| <span data-ttu-id="945de-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="945de-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="945de-269">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="945de-269">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="945de-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="945de-270">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="945de-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="945de-271">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="945de-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="945de-272">Search-Flags</span></span>           | <span data-ttu-id="945de-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="945de-273">0x00000000</span></span>                                       |
| <span data-ttu-id="945de-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="945de-274">System-Flags</span></span>           | <span data-ttu-id="945de-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="945de-275">0x00000010</span></span>                                       |
| <span data-ttu-id="945de-276">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="945de-276">Classes used in</span></span>        | [<span data-ttu-id="945de-277">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="945de-277">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="945de-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="945de-278">Windows Server 2012</span></span>



| <span data-ttu-id="945de-279">Eingabe</span><span class="sxs-lookup"><span data-stu-id="945de-279">Entry</span></span> | <span data-ttu-id="945de-280">Wert</span><span class="sxs-lookup"><span data-stu-id="945de-280">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="945de-281">Link-ID</span><span class="sxs-lookup"><span data-stu-id="945de-281">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="945de-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="945de-282">MAPI-Id</span></span>                | <span data-ttu-id="945de-283">0x8145</span><span class="sxs-lookup"><span data-stu-id="945de-283">0x8145</span></span>                                           |
| <span data-ttu-id="945de-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="945de-284">System-Only</span></span>            | <span data-ttu-id="945de-285">False</span><span class="sxs-lookup"><span data-stu-id="945de-285">False</span></span>                                            |
| <span data-ttu-id="945de-286">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="945de-286">Is-Single-Valued</span></span>       | <span data-ttu-id="945de-287">Richtig</span><span class="sxs-lookup"><span data-stu-id="945de-287">True</span></span>                                             |
| <span data-ttu-id="945de-288">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="945de-288">Is Indexed</span></span>             | <span data-ttu-id="945de-289">False</span><span class="sxs-lookup"><span data-stu-id="945de-289">False</span></span>                                            |
| <span data-ttu-id="945de-290">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="945de-290">In Global Catalog</span></span>      | <span data-ttu-id="945de-291">False</span><span class="sxs-lookup"><span data-stu-id="945de-291">False</span></span>                                            |
| <span data-ttu-id="945de-292">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="945de-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="945de-293">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="945de-293">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="945de-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="945de-294">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="945de-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="945de-295">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="945de-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="945de-296">Search-Flags</span></span>           | <span data-ttu-id="945de-297">0x00000000</span><span class="sxs-lookup"><span data-stu-id="945de-297">0x00000000</span></span>                                       |
| <span data-ttu-id="945de-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="945de-298">System-Flags</span></span>           | <span data-ttu-id="945de-299">0x00000010</span><span class="sxs-lookup"><span data-stu-id="945de-299">0x00000010</span></span>                                       |
| <span data-ttu-id="945de-300">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="945de-300">Classes used in</span></span>        | [<span data-ttu-id="945de-301">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="945de-301">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





