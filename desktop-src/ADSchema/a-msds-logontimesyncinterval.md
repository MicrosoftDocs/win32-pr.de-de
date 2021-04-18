---
title: ms-DS-Logon-Time-Sync-Interval-Attribut
description: Dieses Attribut steuert die Granularität (in Tagen), mit der der Zeitpunkt der letzten Anmeldung für einen Benutzer oder Computer, der im lastLogonTimestamp-Attribut aufgezeichnet wurde, auf alle DCS in einer Domäne repliziert wird.
ms.assetid: f1f9f1f8-df60-44b5-965d-631c4dd4ef84
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-Logon-Time-Sync-Interval-Attribut
- AD-Schema des msDS-logontimesyncinterval-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Logon-Time-Sync-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dbf23ca77bda9dac76f02986be1c05c80559199
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104520167"
---
# <a name="ms-ds-logon-time-sync-interval-attribute"></a><span data-ttu-id="aaec0-105">ms-DS-Logon-Time-Sync-Interval-Attribut</span><span class="sxs-lookup"><span data-stu-id="aaec0-105">ms-DS-Logon-Time-Sync-Interval attribute</span></span>

<span data-ttu-id="aaec0-106">Dieses Attribut steuert die Granularität (in Tagen), mit der der Zeitpunkt der letzten Anmeldung für einen Benutzer oder Computer, der im lastLogonTimestamp-Attribut aufgezeichnet wurde, auf alle DCS in einer Domäne repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="aaec0-106">This attribute controls the granularity, in days, with which the last logon time for a user or computer, recorded in the lastLogonTimestamp attribute, is replicated to all DCs in a domain.</span></span>



| <span data-ttu-id="aaec0-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aaec0-107">Entry</span></span> | <span data-ttu-id="aaec0-108">Wert</span><span class="sxs-lookup"><span data-stu-id="aaec0-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaec0-109">CN</span><span class="sxs-lookup"><span data-stu-id="aaec0-109">CN</span></span>                | <span data-ttu-id="aaec0-110">ms-DS-Logon-Time-Sync-Interval</span><span class="sxs-lookup"><span data-stu-id="aaec0-110">ms-DS-Logon-Time-Sync-Interval</span></span>                                                                             |
| <span data-ttu-id="aaec0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="aaec0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="aaec0-112">MSDS-logontimesyncinterval</span><span class="sxs-lookup"><span data-stu-id="aaec0-112">msDS-LogonTimeSyncInterval</span></span>                                                                                 |
| <span data-ttu-id="aaec0-113">Size</span><span class="sxs-lookup"><span data-stu-id="aaec0-113">Size</span></span>              | <span data-ttu-id="aaec0-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="aaec0-114">4 bytes</span></span>                                                                                                    |
| <span data-ttu-id="aaec0-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="aaec0-115">Update Privilege</span></span>  | <span data-ttu-id="aaec0-116">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="aaec0-116">Domain administrator</span></span>                                                                                       |
| <span data-ttu-id="aaec0-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="aaec0-117">Update Frequency</span></span>  | <span data-ttu-id="aaec0-118">Da es sich hierbei um eine Richtlinien Einstellung handelt, wird Sie nur dann aktualisiert, wenn eine Änderung der Domänen weiten Richtlinie gewünscht wird.</span><span class="sxs-lookup"><span data-stu-id="aaec0-118">Rarely, since this is a policy setting, it is updated only when a change in domain-wide policy is desired.</span></span> |
| <span data-ttu-id="aaec0-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="aaec0-119">Attribute-Id</span></span>      | <span data-ttu-id="aaec0-120">1.2.840.113556.1.4.1784</span><span class="sxs-lookup"><span data-stu-id="aaec0-120">1.2.840.113556.1.4.1784</span></span>                                                                                    |
| <span data-ttu-id="aaec0-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="aaec0-121">System-Id-Guid</span></span>    | <span data-ttu-id="aaec0-122">ad7940f8-e43a-4a42-83bc-d688e59ea605</span><span class="sxs-lookup"><span data-stu-id="aaec0-122">ad7940f8-e43a-4a42-83bc-d688e59ea605</span></span>                                                                       |
| <span data-ttu-id="aaec0-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="aaec0-123">Syntax</span></span>            | [<span data-ttu-id="aaec0-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="aaec0-124">**Enumeration**</span></span>](s-enumeration.md)                                                                       |



## <a name="implementations"></a><span data-ttu-id="aaec0-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="aaec0-125">Implementations</span></span>

-   [<span data-ttu-id="aaec0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="aaec0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="aaec0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="aaec0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="aaec0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="aaec0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="aaec0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="aaec0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="aaec0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="aaec0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="aaec0-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aaec0-131">Windows Server 2003</span></span>



| <span data-ttu-id="aaec0-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aaec0-132">Entry</span></span> | <span data-ttu-id="aaec0-133">Wert</span><span class="sxs-lookup"><span data-stu-id="aaec0-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="aaec0-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aaec0-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="aaec0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aaec0-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="aaec0-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="aaec0-136">System-Only</span></span>            | <span data-ttu-id="aaec0-137">False</span><span class="sxs-lookup"><span data-stu-id="aaec0-137">False</span></span>                                        |
| <span data-ttu-id="aaec0-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aaec0-138">Is-Single-Valued</span></span>       | <span data-ttu-id="aaec0-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="aaec0-139">True</span></span>                                         |
| <span data-ttu-id="aaec0-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aaec0-140">Is Indexed</span></span>             | <span data-ttu-id="aaec0-141">False</span><span class="sxs-lookup"><span data-stu-id="aaec0-141">False</span></span>                                        |
| <span data-ttu-id="aaec0-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aaec0-142">In Global Catalog</span></span>      | <span data-ttu-id="aaec0-143">False</span><span class="sxs-lookup"><span data-stu-id="aaec0-143">False</span></span>                                        |
| <span data-ttu-id="aaec0-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aaec0-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="aaec0-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aaec0-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="aaec0-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aaec0-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="aaec0-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aaec0-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="aaec0-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aaec0-148">Search-Flags</span></span>           | <span data-ttu-id="aaec0-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aaec0-149">0x00000000</span></span>                                   |
| <span data-ttu-id="aaec0-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aaec0-150">System-Flags</span></span>           | <span data-ttu-id="aaec0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aaec0-151">0x00000010</span></span>                                   |
| <span data-ttu-id="aaec0-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aaec0-152">Classes used in</span></span>        | [<span data-ttu-id="aaec0-153">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="aaec0-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="aaec0-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="aaec0-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="aaec0-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aaec0-155">Entry</span></span> | <span data-ttu-id="aaec0-156">Wert</span><span class="sxs-lookup"><span data-stu-id="aaec0-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="aaec0-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aaec0-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="aaec0-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aaec0-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="aaec0-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="aaec0-159">System-Only</span></span>            | <span data-ttu-id="aaec0-160">False</span><span class="sxs-lookup"><span data-stu-id="aaec0-160">False</span></span>                                        |
| <span data-ttu-id="aaec0-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aaec0-161">Is-Single-Valued</span></span>       | <span data-ttu-id="aaec0-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="aaec0-162">True</span></span>                                         |
| <span data-ttu-id="aaec0-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aaec0-163">Is Indexed</span></span>             | <span data-ttu-id="aaec0-164">False</span><span class="sxs-lookup"><span data-stu-id="aaec0-164">False</span></span>                                        |
| <span data-ttu-id="aaec0-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aaec0-165">In Global Catalog</span></span>      | <span data-ttu-id="aaec0-166">False</span><span class="sxs-lookup"><span data-stu-id="aaec0-166">False</span></span>                                        |
| <span data-ttu-id="aaec0-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aaec0-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="aaec0-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aaec0-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="aaec0-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aaec0-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="aaec0-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aaec0-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="aaec0-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aaec0-171">Search-Flags</span></span>           | <span data-ttu-id="aaec0-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aaec0-172">0x00000000</span></span>                                   |
| <span data-ttu-id="aaec0-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aaec0-173">System-Flags</span></span>           | <span data-ttu-id="aaec0-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aaec0-174">0x00000010</span></span>                                   |
| <span data-ttu-id="aaec0-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aaec0-175">Classes used in</span></span>        | [<span data-ttu-id="aaec0-176">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="aaec0-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="aaec0-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aaec0-177">Windows Server 2008</span></span>



| <span data-ttu-id="aaec0-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aaec0-178">Entry</span></span> | <span data-ttu-id="aaec0-179">Wert</span><span class="sxs-lookup"><span data-stu-id="aaec0-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="aaec0-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aaec0-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="aaec0-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aaec0-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="aaec0-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="aaec0-182">System-Only</span></span>            | <span data-ttu-id="aaec0-183">False</span><span class="sxs-lookup"><span data-stu-id="aaec0-183">False</span></span>                                        |
| <span data-ttu-id="aaec0-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aaec0-184">Is-Single-Valued</span></span>       | <span data-ttu-id="aaec0-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="aaec0-185">True</span></span>                                         |
| <span data-ttu-id="aaec0-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aaec0-186">Is Indexed</span></span>             | <span data-ttu-id="aaec0-187">False</span><span class="sxs-lookup"><span data-stu-id="aaec0-187">False</span></span>                                        |
| <span data-ttu-id="aaec0-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aaec0-188">In Global Catalog</span></span>      | <span data-ttu-id="aaec0-189">False</span><span class="sxs-lookup"><span data-stu-id="aaec0-189">False</span></span>                                        |
| <span data-ttu-id="aaec0-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aaec0-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="aaec0-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aaec0-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="aaec0-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aaec0-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="aaec0-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aaec0-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="aaec0-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aaec0-194">Search-Flags</span></span>           | <span data-ttu-id="aaec0-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aaec0-195">0x00000000</span></span>                                   |
| <span data-ttu-id="aaec0-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aaec0-196">System-Flags</span></span>           | <span data-ttu-id="aaec0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aaec0-197">0x00000010</span></span>                                   |
| <span data-ttu-id="aaec0-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aaec0-198">Classes used in</span></span>        | [<span data-ttu-id="aaec0-199">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="aaec0-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="aaec0-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aaec0-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="aaec0-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aaec0-201">Entry</span></span> | <span data-ttu-id="aaec0-202">Wert</span><span class="sxs-lookup"><span data-stu-id="aaec0-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="aaec0-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aaec0-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="aaec0-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aaec0-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="aaec0-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="aaec0-205">System-Only</span></span>            | <span data-ttu-id="aaec0-206">False</span><span class="sxs-lookup"><span data-stu-id="aaec0-206">False</span></span>                                        |
| <span data-ttu-id="aaec0-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aaec0-207">Is-Single-Valued</span></span>       | <span data-ttu-id="aaec0-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="aaec0-208">True</span></span>                                         |
| <span data-ttu-id="aaec0-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aaec0-209">Is Indexed</span></span>             | <span data-ttu-id="aaec0-210">False</span><span class="sxs-lookup"><span data-stu-id="aaec0-210">False</span></span>                                        |
| <span data-ttu-id="aaec0-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aaec0-211">In Global Catalog</span></span>      | <span data-ttu-id="aaec0-212">False</span><span class="sxs-lookup"><span data-stu-id="aaec0-212">False</span></span>                                        |
| <span data-ttu-id="aaec0-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aaec0-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="aaec0-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aaec0-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="aaec0-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aaec0-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="aaec0-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aaec0-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="aaec0-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aaec0-217">Search-Flags</span></span>           | <span data-ttu-id="aaec0-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aaec0-218">0x00000000</span></span>                                   |
| <span data-ttu-id="aaec0-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aaec0-219">System-Flags</span></span>           | <span data-ttu-id="aaec0-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aaec0-220">0x00000010</span></span>                                   |
| <span data-ttu-id="aaec0-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aaec0-221">Classes used in</span></span>        | [<span data-ttu-id="aaec0-222">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="aaec0-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="aaec0-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aaec0-223">Windows Server 2012</span></span>



| <span data-ttu-id="aaec0-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aaec0-224">Entry</span></span> | <span data-ttu-id="aaec0-225">Wert</span><span class="sxs-lookup"><span data-stu-id="aaec0-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="aaec0-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aaec0-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="aaec0-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aaec0-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="aaec0-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="aaec0-228">System-Only</span></span>            | <span data-ttu-id="aaec0-229">False</span><span class="sxs-lookup"><span data-stu-id="aaec0-229">False</span></span>                                        |
| <span data-ttu-id="aaec0-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aaec0-230">Is-Single-Valued</span></span>       | <span data-ttu-id="aaec0-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="aaec0-231">True</span></span>                                         |
| <span data-ttu-id="aaec0-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aaec0-232">Is Indexed</span></span>             | <span data-ttu-id="aaec0-233">False</span><span class="sxs-lookup"><span data-stu-id="aaec0-233">False</span></span>                                        |
| <span data-ttu-id="aaec0-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aaec0-234">In Global Catalog</span></span>      | <span data-ttu-id="aaec0-235">False</span><span class="sxs-lookup"><span data-stu-id="aaec0-235">False</span></span>                                        |
| <span data-ttu-id="aaec0-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aaec0-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="aaec0-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aaec0-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="aaec0-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aaec0-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="aaec0-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aaec0-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="aaec0-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aaec0-240">Search-Flags</span></span>           | <span data-ttu-id="aaec0-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aaec0-241">0x00000000</span></span>                                   |
| <span data-ttu-id="aaec0-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aaec0-242">System-Flags</span></span>           | <span data-ttu-id="aaec0-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aaec0-243">0x00000010</span></span>                                   |
| <span data-ttu-id="aaec0-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aaec0-244">Classes used in</span></span>        | [<span data-ttu-id="aaec0-245">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="aaec0-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





