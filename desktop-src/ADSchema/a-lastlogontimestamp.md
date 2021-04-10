---
title: Last-Logon-Timestamp-Attribut
description: Dies ist der Zeitpunkt, zu dem sich der Benutzer zuletzt bei der Domäne angemeldet hat.
ms.assetid: 6c94bccb-1e0a-421c-a00c-5f6e6389690f
ms.tgt_platform: multiple
keywords:
- AD-Schema des Last-Logon-Timestamp-Attributs
- AD-Schema des lastLogonTimestamp-Attributs
topic_type:
- apiref
api_name:
- Last-Logon-Timestamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6d7668891d008e1b16b7dc148462498e9210b4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107240"
---
# <a name="last-logon-timestamp-attribute"></a><span data-ttu-id="1cd73-105">Last-Logon-Timestamp-Attribut</span><span class="sxs-lookup"><span data-stu-id="1cd73-105">Last-Logon-Timestamp attribute</span></span>

<span data-ttu-id="1cd73-106">Dies ist der Zeitpunkt, zu dem sich der Benutzer zuletzt bei der Domäne angemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="1cd73-106">This is the time that the user last logged into the domain.</span></span> <span data-ttu-id="1cd73-107">Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601 (UTC) darstellt.</span><span class="sxs-lookup"><span data-stu-id="1cd73-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="1cd73-108">Jedes Mal, wenn sich ein Benutzer anmeldet, wird der Wert dieses Attributs vom DC gelesen.</span><span class="sxs-lookup"><span data-stu-id="1cd73-108">Whenever a user logs on, the value of this attribute is read from the DC.</span></span> <span data-ttu-id="1cd73-109">Wenn der Wert älter ist \[ `current_time - msDS-LogonTimeSyncInterval` \] , wird der Wert aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1cd73-109">If the value is older \[ `current_time - msDS-LogonTimeSyncInterval` \], the value is updated.</span></span> <span data-ttu-id="1cd73-110">Das erste Update nach der Erhöhung der Domänen Funktionsebene wird als 14 Tage minus zufälliger Prozentsatz von 5 Tagen berechnet.</span><span class="sxs-lookup"><span data-stu-id="1cd73-110">The initial update after the raise of the domain functional level is calculated as 14 days minus random percentage of 5 days.</span></span>



| <span data-ttu-id="1cd73-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1cd73-111">Entry</span></span> | <span data-ttu-id="1cd73-112">Wert</span><span class="sxs-lookup"><span data-stu-id="1cd73-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cd73-113">CN</span><span class="sxs-lookup"><span data-stu-id="1cd73-113">CN</span></span>                | <span data-ttu-id="1cd73-114">Zeitstempel der letzten Anmeldung</span><span class="sxs-lookup"><span data-stu-id="1cd73-114">Last-Logon-Timestamp</span></span>                                                                                                   |
| <span data-ttu-id="1cd73-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1cd73-115">Ldap-Display-Name</span></span> | <span data-ttu-id="1cd73-116">lastLogonTimestamp</span><span class="sxs-lookup"><span data-stu-id="1cd73-116">lastLogonTimestamp</span></span>                                                                                                     |
| <span data-ttu-id="1cd73-117">Size</span><span class="sxs-lookup"><span data-stu-id="1cd73-117">Size</span></span>              | \-                                                                                                                     |
| <span data-ttu-id="1cd73-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="1cd73-118">Update Privilege</span></span>  | <span data-ttu-id="1cd73-119">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1cd73-119">This value is set by the system.</span></span>                                                                                       |
| <span data-ttu-id="1cd73-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="1cd73-120">Update Frequency</span></span>  | <span data-ttu-id="1cd73-121">Wenn sich der Benutzer anmeldet und dieser Wert älter als die aktuelle Zeit abzüglich des Werts von MSDS-logontimesyncinterval ist.</span><span class="sxs-lookup"><span data-stu-id="1cd73-121">When the user logs on, and if this value is older than the current time minus the value of msDS-LogonTimeSyncInterval.</span></span> |
| <span data-ttu-id="1cd73-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1cd73-122">Attribute-Id</span></span>      | <span data-ttu-id="1cd73-123">1.2.840.113556.1.4.1696</span><span class="sxs-lookup"><span data-stu-id="1cd73-123">1.2.840.113556.1.4.1696</span></span>                                                                                                |
| <span data-ttu-id="1cd73-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1cd73-124">System-Id-Guid</span></span>    | <span data-ttu-id="1cd73-125">c0e20a04-0e5a-4ff3-9482-5efeaecd7060</span><span class="sxs-lookup"><span data-stu-id="1cd73-125">c0e20a04-0e5a-4ff3-9482-5efeaecd7060</span></span>                                                                                   |
| <span data-ttu-id="1cd73-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cd73-126">Syntax</span></span>            | [<span data-ttu-id="1cd73-127">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="1cd73-127">**Interval**</span></span>](s-interval.md)                                                                                         |



## <a name="implementations"></a><span data-ttu-id="1cd73-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="1cd73-128">Implementations</span></span>

-   [<span data-ttu-id="1cd73-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1cd73-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1cd73-130">**Adam**</span><span class="sxs-lookup"><span data-stu-id="1cd73-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1cd73-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1cd73-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1cd73-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1cd73-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1cd73-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1cd73-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1cd73-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1cd73-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="1cd73-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1cd73-135">Windows Server 2003</span></span>



| <span data-ttu-id="1cd73-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1cd73-136">Entry</span></span> | <span data-ttu-id="1cd73-137">Wert</span><span class="sxs-lookup"><span data-stu-id="1cd73-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1cd73-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1cd73-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1cd73-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cd73-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1cd73-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cd73-140">System-Only</span></span>            | <span data-ttu-id="1cd73-141">False</span><span class="sxs-lookup"><span data-stu-id="1cd73-141">False</span></span>                             |
| <span data-ttu-id="1cd73-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1cd73-142">Is-Single-Valued</span></span>       | <span data-ttu-id="1cd73-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="1cd73-143">True</span></span>                              |
| <span data-ttu-id="1cd73-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1cd73-144">Is Indexed</span></span>             | <span data-ttu-id="1cd73-145">False</span><span class="sxs-lookup"><span data-stu-id="1cd73-145">False</span></span>                             |
| <span data-ttu-id="1cd73-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1cd73-146">In Global Catalog</span></span>      | <span data-ttu-id="1cd73-147">False</span><span class="sxs-lookup"><span data-stu-id="1cd73-147">False</span></span>                             |
| <span data-ttu-id="1cd73-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1cd73-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cd73-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1cd73-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1cd73-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cd73-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1cd73-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cd73-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1cd73-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd73-152">Search-Flags</span></span>           | <span data-ttu-id="1cd73-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cd73-153">0x00000000</span></span>                        |
| <span data-ttu-id="1cd73-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd73-154">System-Flags</span></span>           | <span data-ttu-id="1cd73-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cd73-155">0x00000010</span></span>                        |
| <span data-ttu-id="1cd73-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1cd73-156">Classes used in</span></span>        | [<span data-ttu-id="1cd73-157">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="1cd73-157">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1cd73-158">Adam</span><span class="sxs-lookup"><span data-stu-id="1cd73-158">ADAM</span></span>



| <span data-ttu-id="1cd73-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1cd73-159">Entry</span></span> | <span data-ttu-id="1cd73-160">Wert</span><span class="sxs-lookup"><span data-stu-id="1cd73-160">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="1cd73-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1cd73-161">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1cd73-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cd73-162">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1cd73-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cd73-163">System-Only</span></span>            | <span data-ttu-id="1cd73-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="1cd73-164">True</span></span>                                                              |
| <span data-ttu-id="1cd73-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1cd73-165">Is-Single-Valued</span></span>       | <span data-ttu-id="1cd73-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="1cd73-166">True</span></span>                                                              |
| <span data-ttu-id="1cd73-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1cd73-167">Is Indexed</span></span>             | <span data-ttu-id="1cd73-168">False</span><span class="sxs-lookup"><span data-stu-id="1cd73-168">False</span></span>                                                             |
| <span data-ttu-id="1cd73-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1cd73-169">In Global Catalog</span></span>      | <span data-ttu-id="1cd73-170">False</span><span class="sxs-lookup"><span data-stu-id="1cd73-170">False</span></span>                                                             |
| <span data-ttu-id="1cd73-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1cd73-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cd73-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1cd73-172">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="1cd73-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cd73-173">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="1cd73-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cd73-174">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="1cd73-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd73-175">Search-Flags</span></span>           | <span data-ttu-id="1cd73-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cd73-176">0x00000000</span></span>                                                        |
| <span data-ttu-id="1cd73-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd73-177">System-Flags</span></span>           | <span data-ttu-id="1cd73-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cd73-178">0x00000010</span></span>                                                        |
| <span data-ttu-id="1cd73-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1cd73-179">Classes used in</span></span>        | [<span data-ttu-id="1cd73-180">**ms-DS-Bindable-Objekt**</span><span class="sxs-lookup"><span data-stu-id="1cd73-180">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1cd73-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1cd73-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1cd73-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1cd73-182">Entry</span></span> | <span data-ttu-id="1cd73-183">Wert</span><span class="sxs-lookup"><span data-stu-id="1cd73-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1cd73-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1cd73-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1cd73-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cd73-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1cd73-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cd73-186">System-Only</span></span>            | <span data-ttu-id="1cd73-187">False</span><span class="sxs-lookup"><span data-stu-id="1cd73-187">False</span></span>                             |
| <span data-ttu-id="1cd73-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1cd73-188">Is-Single-Valued</span></span>       | <span data-ttu-id="1cd73-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="1cd73-189">True</span></span>                              |
| <span data-ttu-id="1cd73-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1cd73-190">Is Indexed</span></span>             | <span data-ttu-id="1cd73-191">False</span><span class="sxs-lookup"><span data-stu-id="1cd73-191">False</span></span>                             |
| <span data-ttu-id="1cd73-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1cd73-192">In Global Catalog</span></span>      | <span data-ttu-id="1cd73-193">False</span><span class="sxs-lookup"><span data-stu-id="1cd73-193">False</span></span>                             |
| <span data-ttu-id="1cd73-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1cd73-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cd73-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1cd73-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1cd73-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cd73-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1cd73-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cd73-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1cd73-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd73-198">Search-Flags</span></span>           | <span data-ttu-id="1cd73-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cd73-199">0x00000000</span></span>                        |
| <span data-ttu-id="1cd73-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd73-200">System-Flags</span></span>           | <span data-ttu-id="1cd73-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cd73-201">0x00000010</span></span>                        |
| <span data-ttu-id="1cd73-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1cd73-202">Classes used in</span></span>        | [<span data-ttu-id="1cd73-203">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="1cd73-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1cd73-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1cd73-204">Windows Server 2008</span></span>



| <span data-ttu-id="1cd73-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1cd73-205">Entry</span></span> | <span data-ttu-id="1cd73-206">Wert</span><span class="sxs-lookup"><span data-stu-id="1cd73-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1cd73-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1cd73-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1cd73-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cd73-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1cd73-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cd73-209">System-Only</span></span>            | <span data-ttu-id="1cd73-210">False</span><span class="sxs-lookup"><span data-stu-id="1cd73-210">False</span></span>                             |
| <span data-ttu-id="1cd73-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1cd73-211">Is-Single-Valued</span></span>       | <span data-ttu-id="1cd73-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="1cd73-212">True</span></span>                              |
| <span data-ttu-id="1cd73-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1cd73-213">Is Indexed</span></span>             | <span data-ttu-id="1cd73-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="1cd73-214">True</span></span>                              |
| <span data-ttu-id="1cd73-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1cd73-215">In Global Catalog</span></span>      | <span data-ttu-id="1cd73-216">Richtig</span><span class="sxs-lookup"><span data-stu-id="1cd73-216">True</span></span>                              |
| <span data-ttu-id="1cd73-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1cd73-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cd73-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1cd73-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1cd73-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cd73-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1cd73-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cd73-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1cd73-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd73-221">Search-Flags</span></span>           | <span data-ttu-id="1cd73-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1cd73-222">0x00000001</span></span>                        |
| <span data-ttu-id="1cd73-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd73-223">System-Flags</span></span>           | <span data-ttu-id="1cd73-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cd73-224">0x00000010</span></span>                        |
| <span data-ttu-id="1cd73-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1cd73-225">Classes used in</span></span>        | [<span data-ttu-id="1cd73-226">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="1cd73-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1cd73-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1cd73-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1cd73-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1cd73-228">Entry</span></span> | <span data-ttu-id="1cd73-229">Wert</span><span class="sxs-lookup"><span data-stu-id="1cd73-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1cd73-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1cd73-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1cd73-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cd73-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1cd73-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cd73-232">System-Only</span></span>            | <span data-ttu-id="1cd73-233">False</span><span class="sxs-lookup"><span data-stu-id="1cd73-233">False</span></span>                             |
| <span data-ttu-id="1cd73-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1cd73-234">Is-Single-Valued</span></span>       | <span data-ttu-id="1cd73-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="1cd73-235">True</span></span>                              |
| <span data-ttu-id="1cd73-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1cd73-236">Is Indexed</span></span>             | <span data-ttu-id="1cd73-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="1cd73-237">True</span></span>                              |
| <span data-ttu-id="1cd73-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1cd73-238">In Global Catalog</span></span>      | <span data-ttu-id="1cd73-239">Richtig</span><span class="sxs-lookup"><span data-stu-id="1cd73-239">True</span></span>                              |
| <span data-ttu-id="1cd73-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1cd73-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cd73-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1cd73-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1cd73-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cd73-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1cd73-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cd73-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1cd73-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd73-244">Search-Flags</span></span>           | <span data-ttu-id="1cd73-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1cd73-245">0x00000001</span></span>                        |
| <span data-ttu-id="1cd73-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd73-246">System-Flags</span></span>           | <span data-ttu-id="1cd73-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cd73-247">0x00000010</span></span>                        |
| <span data-ttu-id="1cd73-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1cd73-248">Classes used in</span></span>        | [<span data-ttu-id="1cd73-249">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="1cd73-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1cd73-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1cd73-250">Windows Server 2012</span></span>



| <span data-ttu-id="1cd73-251">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1cd73-251">Entry</span></span> | <span data-ttu-id="1cd73-252">Wert</span><span class="sxs-lookup"><span data-stu-id="1cd73-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1cd73-253">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1cd73-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1cd73-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cd73-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1cd73-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cd73-255">System-Only</span></span>            | <span data-ttu-id="1cd73-256">False</span><span class="sxs-lookup"><span data-stu-id="1cd73-256">False</span></span>                             |
| <span data-ttu-id="1cd73-257">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1cd73-257">Is-Single-Valued</span></span>       | <span data-ttu-id="1cd73-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="1cd73-258">True</span></span>                              |
| <span data-ttu-id="1cd73-259">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1cd73-259">Is Indexed</span></span>             | <span data-ttu-id="1cd73-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="1cd73-260">True</span></span>                              |
| <span data-ttu-id="1cd73-261">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1cd73-261">In Global Catalog</span></span>      | <span data-ttu-id="1cd73-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="1cd73-262">True</span></span>                              |
| <span data-ttu-id="1cd73-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1cd73-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cd73-264">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1cd73-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1cd73-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cd73-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1cd73-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cd73-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1cd73-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd73-267">Search-Flags</span></span>           | <span data-ttu-id="1cd73-268">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1cd73-268">0x00000001</span></span>                        |
| <span data-ttu-id="1cd73-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cd73-269">System-Flags</span></span>           | <span data-ttu-id="1cd73-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cd73-270">0x00000010</span></span>                        |
| <span data-ttu-id="1cd73-271">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1cd73-271">Classes used in</span></span>        | [<span data-ttu-id="1cd73-272">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="1cd73-272">**User**</span></span>](c-user.md)<br/> |



 

 





