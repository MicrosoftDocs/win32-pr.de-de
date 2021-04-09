---
title: Last-Logon-Attribut
description: Der Zeitpunkt, an dem sich der Benutzer zuletzt angemeldet hat.
ms.assetid: 271f4f38-90f9-4add-a3ed-413c224e1fae
ms.tgt_platform: multiple
keywords:
- AD-Schema für Last-Logon-Attribut
- adschema des lastLogon-Attributs
topic_type:
- apiref
api_name:
- Last-Logon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae01ffabf2d4862c030607b997a4d9057b934f8f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859725"
---
# <a name="last-logon-attribute"></a><span data-ttu-id="4a70f-105">Last-Logon-Attribut</span><span class="sxs-lookup"><span data-stu-id="4a70f-105">Last-Logon attribute</span></span>

<span data-ttu-id="4a70f-106">Der Zeitpunkt, an dem sich der Benutzer zuletzt angemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="4a70f-106">The last time the user logged on.</span></span> <span data-ttu-id="4a70f-107">Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601 (UTC) darstellt.</span><span class="sxs-lookup"><span data-stu-id="4a70f-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="4a70f-108">Der Wert 0 (null) bedeutet, dass die Uhrzeit der letzten Anmeldung unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="4a70f-108">A value of zero means that the last logon time is unknown.</span></span>



| <span data-ttu-id="4a70f-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a70f-109">Entry</span></span> | <span data-ttu-id="4a70f-110">Wert</span><span class="sxs-lookup"><span data-stu-id="4a70f-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4a70f-111">CN</span><span class="sxs-lookup"><span data-stu-id="4a70f-111">CN</span></span>                | <span data-ttu-id="4a70f-112">Last-Logon</span><span class="sxs-lookup"><span data-stu-id="4a70f-112">Last-Logon</span></span>                           |
| <span data-ttu-id="4a70f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4a70f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4a70f-114">lastLogon</span><span class="sxs-lookup"><span data-stu-id="4a70f-114">lastLogon</span></span>                            |
| <span data-ttu-id="4a70f-115">Size</span><span class="sxs-lookup"><span data-stu-id="4a70f-115">Size</span></span>              | <span data-ttu-id="4a70f-116">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="4a70f-116">8 bytes</span></span>                              |
| <span data-ttu-id="4a70f-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="4a70f-117">Update Privilege</span></span>  | <span data-ttu-id="4a70f-118">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a70f-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="4a70f-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="4a70f-119">Update Frequency</span></span>  | <span data-ttu-id="4a70f-120">Jedes Mal, wenn sich der Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="4a70f-120">Each time the user logs on.</span></span>          |
| <span data-ttu-id="4a70f-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4a70f-121">Attribute-Id</span></span>      | <span data-ttu-id="4a70f-122">1.2.840.113556.1.4.52</span><span class="sxs-lookup"><span data-stu-id="4a70f-122">1.2.840.113556.1.4.52</span></span>                |
| <span data-ttu-id="4a70f-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4a70f-123">System-Id-Guid</span></span>    | <span data-ttu-id="4a70f-124">bf967997-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="4a70f-124">bf967997-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="4a70f-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a70f-125">Syntax</span></span>            | [<span data-ttu-id="4a70f-126">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="4a70f-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="4a70f-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="4a70f-127">Implementations</span></span>

-   [<span data-ttu-id="4a70f-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4a70f-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4a70f-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4a70f-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4a70f-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4a70f-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4a70f-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4a70f-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4a70f-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4a70f-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4a70f-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4a70f-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4a70f-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4a70f-134">Windows 2000 Server</span></span>



| <span data-ttu-id="4a70f-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a70f-135">Entry</span></span> | <span data-ttu-id="4a70f-136">Wert</span><span class="sxs-lookup"><span data-stu-id="4a70f-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4a70f-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a70f-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4a70f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a70f-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4a70f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a70f-139">System-Only</span></span>            | <span data-ttu-id="4a70f-140">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-140">False</span></span>                             |
| <span data-ttu-id="4a70f-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a70f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="4a70f-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a70f-142">True</span></span>                              |
| <span data-ttu-id="4a70f-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a70f-143">Is Indexed</span></span>             | <span data-ttu-id="4a70f-144">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-144">False</span></span>                             |
| <span data-ttu-id="4a70f-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a70f-145">In Global Catalog</span></span>      | <span data-ttu-id="4a70f-146">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-146">False</span></span>                             |
| <span data-ttu-id="4a70f-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a70f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a70f-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a70f-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4a70f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a70f-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4a70f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a70f-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4a70f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a70f-151">Search-Flags</span></span>           | <span data-ttu-id="4a70f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a70f-152">0x00000000</span></span>                        |
| <span data-ttu-id="4a70f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a70f-153">System-Flags</span></span>           | <span data-ttu-id="4a70f-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="4a70f-154">0x00000011</span></span>                        |
| <span data-ttu-id="4a70f-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a70f-155">Classes used in</span></span>        | [<span data-ttu-id="4a70f-156">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="4a70f-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4a70f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4a70f-157">Windows Server 2003</span></span>



| <span data-ttu-id="4a70f-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a70f-158">Entry</span></span> | <span data-ttu-id="4a70f-159">Wert</span><span class="sxs-lookup"><span data-stu-id="4a70f-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4a70f-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a70f-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4a70f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a70f-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4a70f-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a70f-162">System-Only</span></span>            | <span data-ttu-id="4a70f-163">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-163">False</span></span>                             |
| <span data-ttu-id="4a70f-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a70f-164">Is-Single-Valued</span></span>       | <span data-ttu-id="4a70f-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a70f-165">True</span></span>                              |
| <span data-ttu-id="4a70f-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a70f-166">Is Indexed</span></span>             | <span data-ttu-id="4a70f-167">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-167">False</span></span>                             |
| <span data-ttu-id="4a70f-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a70f-168">In Global Catalog</span></span>      | <span data-ttu-id="4a70f-169">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-169">False</span></span>                             |
| <span data-ttu-id="4a70f-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a70f-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a70f-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a70f-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4a70f-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a70f-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4a70f-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a70f-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4a70f-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a70f-174">Search-Flags</span></span>           | <span data-ttu-id="4a70f-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a70f-175">0x00000000</span></span>                        |
| <span data-ttu-id="4a70f-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a70f-176">System-Flags</span></span>           | <span data-ttu-id="4a70f-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="4a70f-177">0x00000011</span></span>                        |
| <span data-ttu-id="4a70f-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a70f-178">Classes used in</span></span>        | [<span data-ttu-id="4a70f-179">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="4a70f-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4a70f-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4a70f-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4a70f-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a70f-181">Entry</span></span> | <span data-ttu-id="4a70f-182">Wert</span><span class="sxs-lookup"><span data-stu-id="4a70f-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4a70f-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a70f-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4a70f-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a70f-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4a70f-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a70f-185">System-Only</span></span>            | <span data-ttu-id="4a70f-186">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-186">False</span></span>                             |
| <span data-ttu-id="4a70f-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a70f-187">Is-Single-Valued</span></span>       | <span data-ttu-id="4a70f-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a70f-188">True</span></span>                              |
| <span data-ttu-id="4a70f-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a70f-189">Is Indexed</span></span>             | <span data-ttu-id="4a70f-190">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-190">False</span></span>                             |
| <span data-ttu-id="4a70f-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a70f-191">In Global Catalog</span></span>      | <span data-ttu-id="4a70f-192">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-192">False</span></span>                             |
| <span data-ttu-id="4a70f-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a70f-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a70f-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a70f-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4a70f-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a70f-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4a70f-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a70f-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4a70f-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a70f-197">Search-Flags</span></span>           | <span data-ttu-id="4a70f-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a70f-198">0x00000000</span></span>                        |
| <span data-ttu-id="4a70f-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a70f-199">System-Flags</span></span>           | <span data-ttu-id="4a70f-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="4a70f-200">0x00000011</span></span>                        |
| <span data-ttu-id="4a70f-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a70f-201">Classes used in</span></span>        | [<span data-ttu-id="4a70f-202">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="4a70f-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4a70f-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a70f-203">Windows Server 2008</span></span>



| <span data-ttu-id="4a70f-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a70f-204">Entry</span></span> | <span data-ttu-id="4a70f-205">Wert</span><span class="sxs-lookup"><span data-stu-id="4a70f-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4a70f-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a70f-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4a70f-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a70f-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4a70f-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a70f-208">System-Only</span></span>            | <span data-ttu-id="4a70f-209">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-209">False</span></span>                             |
| <span data-ttu-id="4a70f-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a70f-210">Is-Single-Valued</span></span>       | <span data-ttu-id="4a70f-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a70f-211">True</span></span>                              |
| <span data-ttu-id="4a70f-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a70f-212">Is Indexed</span></span>             | <span data-ttu-id="4a70f-213">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-213">False</span></span>                             |
| <span data-ttu-id="4a70f-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a70f-214">In Global Catalog</span></span>      | <span data-ttu-id="4a70f-215">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-215">False</span></span>                             |
| <span data-ttu-id="4a70f-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a70f-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a70f-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a70f-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4a70f-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a70f-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4a70f-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a70f-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4a70f-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a70f-220">Search-Flags</span></span>           | <span data-ttu-id="4a70f-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a70f-221">0x00000000</span></span>                        |
| <span data-ttu-id="4a70f-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a70f-222">System-Flags</span></span>           | <span data-ttu-id="4a70f-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="4a70f-223">0x00000011</span></span>                        |
| <span data-ttu-id="4a70f-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a70f-224">Classes used in</span></span>        | [<span data-ttu-id="4a70f-225">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="4a70f-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4a70f-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4a70f-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4a70f-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a70f-227">Entry</span></span> | <span data-ttu-id="4a70f-228">Wert</span><span class="sxs-lookup"><span data-stu-id="4a70f-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4a70f-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a70f-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4a70f-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a70f-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4a70f-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a70f-231">System-Only</span></span>            | <span data-ttu-id="4a70f-232">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-232">False</span></span>                             |
| <span data-ttu-id="4a70f-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a70f-233">Is-Single-Valued</span></span>       | <span data-ttu-id="4a70f-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a70f-234">True</span></span>                              |
| <span data-ttu-id="4a70f-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a70f-235">Is Indexed</span></span>             | <span data-ttu-id="4a70f-236">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-236">False</span></span>                             |
| <span data-ttu-id="4a70f-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a70f-237">In Global Catalog</span></span>      | <span data-ttu-id="4a70f-238">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-238">False</span></span>                             |
| <span data-ttu-id="4a70f-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a70f-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a70f-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a70f-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4a70f-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a70f-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4a70f-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a70f-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4a70f-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a70f-243">Search-Flags</span></span>           | <span data-ttu-id="4a70f-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a70f-244">0x00000000</span></span>                        |
| <span data-ttu-id="4a70f-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a70f-245">System-Flags</span></span>           | <span data-ttu-id="4a70f-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="4a70f-246">0x00000011</span></span>                        |
| <span data-ttu-id="4a70f-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a70f-247">Classes used in</span></span>        | [<span data-ttu-id="4a70f-248">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="4a70f-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4a70f-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4a70f-249">Windows Server 2012</span></span>



| <span data-ttu-id="4a70f-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a70f-250">Entry</span></span> | <span data-ttu-id="4a70f-251">Wert</span><span class="sxs-lookup"><span data-stu-id="4a70f-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4a70f-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4a70f-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4a70f-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a70f-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4a70f-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a70f-254">System-Only</span></span>            | <span data-ttu-id="4a70f-255">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-255">False</span></span>                             |
| <span data-ttu-id="4a70f-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4a70f-256">Is-Single-Valued</span></span>       | <span data-ttu-id="4a70f-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="4a70f-257">True</span></span>                              |
| <span data-ttu-id="4a70f-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4a70f-258">Is Indexed</span></span>             | <span data-ttu-id="4a70f-259">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-259">False</span></span>                             |
| <span data-ttu-id="4a70f-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4a70f-260">In Global Catalog</span></span>      | <span data-ttu-id="4a70f-261">False</span><span class="sxs-lookup"><span data-stu-id="4a70f-261">False</span></span>                             |
| <span data-ttu-id="4a70f-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a70f-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a70f-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4a70f-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4a70f-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a70f-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4a70f-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a70f-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4a70f-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a70f-266">Search-Flags</span></span>           | <span data-ttu-id="4a70f-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a70f-267">0x00000000</span></span>                        |
| <span data-ttu-id="4a70f-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a70f-268">System-Flags</span></span>           | <span data-ttu-id="4a70f-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="4a70f-269">0x00000011</span></span>                        |
| <span data-ttu-id="4a70f-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4a70f-270">Classes used in</span></span>        | [<span data-ttu-id="4a70f-271">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="4a70f-271">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="4a70f-272">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a70f-272">Remarks</span></span>

<span data-ttu-id="4a70f-273">Der hohe Teil dieser großen Ganzzahl entspricht dem **dwHighDateTime** -Member der [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Struktur, und der niedrige Teil entspricht dem **dwLowDateTime** -Member der **FILETIME** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a70f-273">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="4a70f-274">Dieses Attribut wird nicht repliziert und auf jedem Domänen Controller in der Domäne separat verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4a70f-274">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="4a70f-275">Um einen exakten Wert für die letzte Anmeldung des Benutzers in der Domäne zu erhalten, muss das Attribut der **letzten Anmeldung** für den Benutzer von jedem Domänen Controller in der Domäne abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4a70f-275">To get an accurate value for the user's last logon in the domain, the **Last-Logon** attribute for the user must be retrieved from every domain controller in the domain.</span></span> <span data-ttu-id="4a70f-276">Der größte Wert, der abgerufen wird, ist die tatsächliche Uhrzeit der letzten Anmeldung für diesen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="4a70f-276">The largest value that is retrieved is the true last logon time for that user.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a70f-277">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a70f-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a70f-278">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="4a70f-278">**FILETIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> </dl>

 

