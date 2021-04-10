---
title: ACS-DSBM-Deadtime-Attribut
description: Dieses Attribut enthält das Wahlzeit Intervall (dsbmdeadinterval) für eine Domäne.
ms.assetid: c3a0780c-1786-4631-b870-77146de87f18
ms.tgt_platform: multiple
keywords:
- AD-Schema des ACS-DSBM-Deadtime-Attributs
- acsdsbmdeadtime-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ACS-DSBM-DeadTime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8b1c980175dc985c3a718d15323be0b8d1b411
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107342"
---
# <a name="acs-dsbm-deadtime-attribute"></a><span data-ttu-id="64c87-105">ACS-DSBM-Deadtime-Attribut</span><span class="sxs-lookup"><span data-stu-id="64c87-105">ACS-DSBM-DeadTime attribute</span></span>

<span data-ttu-id="64c87-106">Dieses Attribut enthält das Wahlzeit Intervall (dsbmdeadinterval) für eine Domäne.</span><span class="sxs-lookup"><span data-stu-id="64c87-106">This attribute contains the election dead time interval (DSBMDeadInterval) for a domain.</span></span> <span data-ttu-id="64c87-107">Wenn das designierte Subnetz-Bandbreiten-Manager \_ \_ während dieses Intervalls keine I am DSBM-Ankündigung sendet, wählt die anderen subnetzbandbreiten-Manager (sbms) in der Domäne einen neuen DSBM aus.</span><span class="sxs-lookup"><span data-stu-id="64c87-107">If the Designated Subnet Bandwidth Manager does not send out an I\_AM\_DSBM advertisement during this interval, then the other Subnet Bandwidth Managers (SBMs) in the domain elect a new DSBM.</span></span>



| <span data-ttu-id="64c87-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64c87-108">Entry</span></span> | <span data-ttu-id="64c87-109">Wert</span><span class="sxs-lookup"><span data-stu-id="64c87-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="64c87-110">CN</span><span class="sxs-lookup"><span data-stu-id="64c87-110">CN</span></span>                | <span data-ttu-id="64c87-111">ACS-DSBM-Deadtime</span><span class="sxs-lookup"><span data-stu-id="64c87-111">ACS-DSBM-DeadTime</span></span>                    |
| <span data-ttu-id="64c87-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="64c87-112">Ldap-Display-Name</span></span> | <span data-ttu-id="64c87-113">acsdsbmdeadtime</span><span class="sxs-lookup"><span data-stu-id="64c87-113">aCSDSBMDeadTime</span></span>                      |
| <span data-ttu-id="64c87-114">Size</span><span class="sxs-lookup"><span data-stu-id="64c87-114">Size</span></span>              | <span data-ttu-id="64c87-115">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="64c87-115">4 bytes</span></span>                              |
| <span data-ttu-id="64c87-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="64c87-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="64c87-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="64c87-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="64c87-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="64c87-118">Attribute-Id</span></span>      | <span data-ttu-id="64c87-119">1.2.840.113556.1.4.778</span><span class="sxs-lookup"><span data-stu-id="64c87-119">1.2.840.113556.1.4.778</span></span>               |
| <span data-ttu-id="64c87-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="64c87-120">System-Id-Guid</span></span>    | <span data-ttu-id="64c87-121">1cb355a0-56d0-11d1-a9c6-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="64c87-121">1cb355a0-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="64c87-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="64c87-122">Syntax</span></span>            | [<span data-ttu-id="64c87-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="64c87-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="64c87-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="64c87-124">Implementations</span></span>

-   [<span data-ttu-id="64c87-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="64c87-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="64c87-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="64c87-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="64c87-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="64c87-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="64c87-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="64c87-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="64c87-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="64c87-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="64c87-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="64c87-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="64c87-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="64c87-131">Windows 2000 Server</span></span>



| <span data-ttu-id="64c87-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64c87-132">Entry</span></span> | <span data-ttu-id="64c87-133">Wert</span><span class="sxs-lookup"><span data-stu-id="64c87-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64c87-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64c87-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64c87-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64c87-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64c87-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="64c87-136">System-Only</span></span>            | <span data-ttu-id="64c87-137">False</span><span class="sxs-lookup"><span data-stu-id="64c87-137">False</span></span>                                        |
| <span data-ttu-id="64c87-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64c87-138">Is-Single-Valued</span></span>       | <span data-ttu-id="64c87-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="64c87-139">True</span></span>                                         |
| <span data-ttu-id="64c87-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64c87-140">Is Indexed</span></span>             | <span data-ttu-id="64c87-141">False</span><span class="sxs-lookup"><span data-stu-id="64c87-141">False</span></span>                                        |
| <span data-ttu-id="64c87-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64c87-142">In Global Catalog</span></span>      | <span data-ttu-id="64c87-143">False</span><span class="sxs-lookup"><span data-stu-id="64c87-143">False</span></span>                                        |
| <span data-ttu-id="64c87-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64c87-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="64c87-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64c87-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64c87-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64c87-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64c87-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64c87-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64c87-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64c87-148">Search-Flags</span></span>           | <span data-ttu-id="64c87-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c87-149">0x00000000</span></span>                                   |
| <span data-ttu-id="64c87-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64c87-150">System-Flags</span></span>           | <span data-ttu-id="64c87-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64c87-151">0x00000010</span></span>                                   |
| <span data-ttu-id="64c87-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64c87-152">Classes used in</span></span>        | [<span data-ttu-id="64c87-153">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="64c87-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="64c87-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="64c87-154">Windows Server 2003</span></span>



| <span data-ttu-id="64c87-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64c87-155">Entry</span></span> | <span data-ttu-id="64c87-156">Wert</span><span class="sxs-lookup"><span data-stu-id="64c87-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64c87-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64c87-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64c87-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64c87-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64c87-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="64c87-159">System-Only</span></span>            | <span data-ttu-id="64c87-160">False</span><span class="sxs-lookup"><span data-stu-id="64c87-160">False</span></span>                                        |
| <span data-ttu-id="64c87-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64c87-161">Is-Single-Valued</span></span>       | <span data-ttu-id="64c87-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="64c87-162">True</span></span>                                         |
| <span data-ttu-id="64c87-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64c87-163">Is Indexed</span></span>             | <span data-ttu-id="64c87-164">False</span><span class="sxs-lookup"><span data-stu-id="64c87-164">False</span></span>                                        |
| <span data-ttu-id="64c87-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64c87-165">In Global Catalog</span></span>      | <span data-ttu-id="64c87-166">False</span><span class="sxs-lookup"><span data-stu-id="64c87-166">False</span></span>                                        |
| <span data-ttu-id="64c87-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64c87-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="64c87-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64c87-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64c87-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64c87-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64c87-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64c87-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64c87-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64c87-171">Search-Flags</span></span>           | <span data-ttu-id="64c87-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c87-172">0x00000000</span></span>                                   |
| <span data-ttu-id="64c87-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64c87-173">System-Flags</span></span>           | <span data-ttu-id="64c87-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64c87-174">0x00000010</span></span>                                   |
| <span data-ttu-id="64c87-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64c87-175">Classes used in</span></span>        | [<span data-ttu-id="64c87-176">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="64c87-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="64c87-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="64c87-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="64c87-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64c87-178">Entry</span></span> | <span data-ttu-id="64c87-179">Wert</span><span class="sxs-lookup"><span data-stu-id="64c87-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64c87-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64c87-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64c87-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64c87-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64c87-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="64c87-182">System-Only</span></span>            | <span data-ttu-id="64c87-183">False</span><span class="sxs-lookup"><span data-stu-id="64c87-183">False</span></span>                                        |
| <span data-ttu-id="64c87-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64c87-184">Is-Single-Valued</span></span>       | <span data-ttu-id="64c87-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="64c87-185">True</span></span>                                         |
| <span data-ttu-id="64c87-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64c87-186">Is Indexed</span></span>             | <span data-ttu-id="64c87-187">False</span><span class="sxs-lookup"><span data-stu-id="64c87-187">False</span></span>                                        |
| <span data-ttu-id="64c87-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64c87-188">In Global Catalog</span></span>      | <span data-ttu-id="64c87-189">False</span><span class="sxs-lookup"><span data-stu-id="64c87-189">False</span></span>                                        |
| <span data-ttu-id="64c87-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64c87-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="64c87-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64c87-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64c87-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64c87-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64c87-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64c87-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64c87-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64c87-194">Search-Flags</span></span>           | <span data-ttu-id="64c87-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c87-195">0x00000000</span></span>                                   |
| <span data-ttu-id="64c87-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64c87-196">System-Flags</span></span>           | <span data-ttu-id="64c87-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64c87-197">0x00000010</span></span>                                   |
| <span data-ttu-id="64c87-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64c87-198">Classes used in</span></span>        | [<span data-ttu-id="64c87-199">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="64c87-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="64c87-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64c87-200">Windows Server 2008</span></span>



| <span data-ttu-id="64c87-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64c87-201">Entry</span></span> | <span data-ttu-id="64c87-202">Wert</span><span class="sxs-lookup"><span data-stu-id="64c87-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64c87-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64c87-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64c87-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64c87-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64c87-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="64c87-205">System-Only</span></span>            | <span data-ttu-id="64c87-206">False</span><span class="sxs-lookup"><span data-stu-id="64c87-206">False</span></span>                                        |
| <span data-ttu-id="64c87-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64c87-207">Is-Single-Valued</span></span>       | <span data-ttu-id="64c87-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="64c87-208">True</span></span>                                         |
| <span data-ttu-id="64c87-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64c87-209">Is Indexed</span></span>             | <span data-ttu-id="64c87-210">False</span><span class="sxs-lookup"><span data-stu-id="64c87-210">False</span></span>                                        |
| <span data-ttu-id="64c87-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64c87-211">In Global Catalog</span></span>      | <span data-ttu-id="64c87-212">False</span><span class="sxs-lookup"><span data-stu-id="64c87-212">False</span></span>                                        |
| <span data-ttu-id="64c87-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64c87-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="64c87-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64c87-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64c87-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64c87-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64c87-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64c87-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64c87-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64c87-217">Search-Flags</span></span>           | <span data-ttu-id="64c87-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c87-218">0x00000000</span></span>                                   |
| <span data-ttu-id="64c87-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64c87-219">System-Flags</span></span>           | <span data-ttu-id="64c87-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64c87-220">0x00000010</span></span>                                   |
| <span data-ttu-id="64c87-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64c87-221">Classes used in</span></span>        | [<span data-ttu-id="64c87-222">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="64c87-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="64c87-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="64c87-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="64c87-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64c87-224">Entry</span></span> | <span data-ttu-id="64c87-225">Wert</span><span class="sxs-lookup"><span data-stu-id="64c87-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64c87-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64c87-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64c87-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64c87-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64c87-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="64c87-228">System-Only</span></span>            | <span data-ttu-id="64c87-229">False</span><span class="sxs-lookup"><span data-stu-id="64c87-229">False</span></span>                                        |
| <span data-ttu-id="64c87-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64c87-230">Is-Single-Valued</span></span>       | <span data-ttu-id="64c87-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="64c87-231">True</span></span>                                         |
| <span data-ttu-id="64c87-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64c87-232">Is Indexed</span></span>             | <span data-ttu-id="64c87-233">False</span><span class="sxs-lookup"><span data-stu-id="64c87-233">False</span></span>                                        |
| <span data-ttu-id="64c87-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64c87-234">In Global Catalog</span></span>      | <span data-ttu-id="64c87-235">False</span><span class="sxs-lookup"><span data-stu-id="64c87-235">False</span></span>                                        |
| <span data-ttu-id="64c87-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64c87-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="64c87-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64c87-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64c87-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64c87-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64c87-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64c87-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64c87-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64c87-240">Search-Flags</span></span>           | <span data-ttu-id="64c87-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c87-241">0x00000000</span></span>                                   |
| <span data-ttu-id="64c87-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64c87-242">System-Flags</span></span>           | <span data-ttu-id="64c87-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64c87-243">0x00000010</span></span>                                   |
| <span data-ttu-id="64c87-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64c87-244">Classes used in</span></span>        | [<span data-ttu-id="64c87-245">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="64c87-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="64c87-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="64c87-246">Windows Server 2012</span></span>



| <span data-ttu-id="64c87-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64c87-247">Entry</span></span> | <span data-ttu-id="64c87-248">Wert</span><span class="sxs-lookup"><span data-stu-id="64c87-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64c87-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="64c87-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64c87-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64c87-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64c87-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="64c87-251">System-Only</span></span>            | <span data-ttu-id="64c87-252">False</span><span class="sxs-lookup"><span data-stu-id="64c87-252">False</span></span>                                        |
| <span data-ttu-id="64c87-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="64c87-253">Is-Single-Valued</span></span>       | <span data-ttu-id="64c87-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="64c87-254">True</span></span>                                         |
| <span data-ttu-id="64c87-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="64c87-255">Is Indexed</span></span>             | <span data-ttu-id="64c87-256">False</span><span class="sxs-lookup"><span data-stu-id="64c87-256">False</span></span>                                        |
| <span data-ttu-id="64c87-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="64c87-257">In Global Catalog</span></span>      | <span data-ttu-id="64c87-258">False</span><span class="sxs-lookup"><span data-stu-id="64c87-258">False</span></span>                                        |
| <span data-ttu-id="64c87-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64c87-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="64c87-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="64c87-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64c87-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64c87-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64c87-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64c87-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64c87-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64c87-263">Search-Flags</span></span>           | <span data-ttu-id="64c87-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c87-264">0x00000000</span></span>                                   |
| <span data-ttu-id="64c87-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64c87-265">System-Flags</span></span>           | <span data-ttu-id="64c87-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64c87-266">0x00000010</span></span>                                   |
| <span data-ttu-id="64c87-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="64c87-267">Classes used in</span></span>        | [<span data-ttu-id="64c87-268">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="64c87-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





