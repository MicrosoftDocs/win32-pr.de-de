---
title: Attribut für ungültiges Kennwort
description: Das letzte Datum, an dem der Anmeldeversuch bei diesem Konto erfolgt ist, wurde mit einem ungültigen Kennwort erstellt.
ms.assetid: 8e8c5b73-b42d-4a62-89af-c0ff2fe106d8
ms.tgt_platform: multiple
keywords:
- AD-Schema für ungültiges Kenn Wort Attribut
- badpasswordtime-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Bad-Password-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47df09d0ff2d82a9180c43721aa09e5363884e24
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480471"
---
# <a name="bad-password-time-attribute"></a><span data-ttu-id="59cf0-105">Attribut für ungültiges Kennwort</span><span class="sxs-lookup"><span data-stu-id="59cf0-105">Bad-Password-Time attribute</span></span>

<span data-ttu-id="59cf0-106">Das letzte Datum, an dem der Anmeldeversuch bei diesem Konto erfolgt ist, wurde mit einem ungültigen Kennwort erstellt.</span><span class="sxs-lookup"><span data-stu-id="59cf0-106">The last time and date that an attempt to log on to this account was made with a password that is not valid.</span></span> <span data-ttu-id="59cf0-107">Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601 (UTC) darstellt.</span><span class="sxs-lookup"><span data-stu-id="59cf0-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="59cf0-108">Der Wert 0 (null) bedeutet, dass das letzte Mal, dass ein falsches Kennwort verwendet wurde, unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="59cf0-108">A value of zero means that the last time a incorrect password was used is unknown.</span></span>



| <span data-ttu-id="59cf0-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="59cf0-109">Entry</span></span> | <span data-ttu-id="59cf0-110">Wert</span><span class="sxs-lookup"><span data-stu-id="59cf0-110">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="59cf0-111">CN</span><span class="sxs-lookup"><span data-stu-id="59cf0-111">CN</span></span>                | <span data-ttu-id="59cf0-112">Ungültige Kenn Wort Zeit</span><span class="sxs-lookup"><span data-stu-id="59cf0-112">Bad-Password-Time</span></span>                         |
| <span data-ttu-id="59cf0-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="59cf0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="59cf0-114">badPasswordTime</span><span class="sxs-lookup"><span data-stu-id="59cf0-114">badPasswordTime</span></span>                           |
| <span data-ttu-id="59cf0-115">Size</span><span class="sxs-lookup"><span data-stu-id="59cf0-115">Size</span></span>              | <span data-ttu-id="59cf0-116">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="59cf0-116">8 bytes</span></span>                                   |
| <span data-ttu-id="59cf0-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="59cf0-117">Update Privilege</span></span>  | <span data-ttu-id="59cf0-118">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="59cf0-118">This value is set by the system.</span></span>          |
| <span data-ttu-id="59cf0-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="59cf0-119">Update Frequency</span></span>  | <span data-ttu-id="59cf0-120">Jedes Mal, wenn der Benutzer ein ungültiges Kennwort eingibt.</span><span class="sxs-lookup"><span data-stu-id="59cf0-120">Each time the user enters a bad password.</span></span> |
| <span data-ttu-id="59cf0-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="59cf0-121">Attribute-Id</span></span>      | <span data-ttu-id="59cf0-122">1.2.840.113556.1.4.49</span><span class="sxs-lookup"><span data-stu-id="59cf0-122">1.2.840.113556.1.4.49</span></span>                     |
| <span data-ttu-id="59cf0-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="59cf0-123">System-Id-Guid</span></span>    | <span data-ttu-id="59cf0-124">bf96792d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="59cf0-124">bf96792d-0de6-11d0-a285-00aa003049e2</span></span>      |
| <span data-ttu-id="59cf0-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="59cf0-125">Syntax</span></span>            | [<span data-ttu-id="59cf0-126">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="59cf0-126">**Interval**</span></span>](s-interval.md)            |



## <a name="implementations"></a><span data-ttu-id="59cf0-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="59cf0-127">Implementations</span></span>

-   [<span data-ttu-id="59cf0-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="59cf0-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="59cf0-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="59cf0-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="59cf0-130">**Adam**</span><span class="sxs-lookup"><span data-stu-id="59cf0-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="59cf0-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="59cf0-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="59cf0-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="59cf0-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="59cf0-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="59cf0-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="59cf0-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="59cf0-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="59cf0-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="59cf0-135">Windows 2000 Server</span></span>



| <span data-ttu-id="59cf0-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="59cf0-136">Entry</span></span> | <span data-ttu-id="59cf0-137">Wert</span><span class="sxs-lookup"><span data-stu-id="59cf0-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="59cf0-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="59cf0-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="59cf0-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59cf0-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="59cf0-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="59cf0-140">System-Only</span></span>            | <span data-ttu-id="59cf0-141">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-141">False</span></span>                             |
| <span data-ttu-id="59cf0-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="59cf0-142">Is-Single-Valued</span></span>       | <span data-ttu-id="59cf0-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="59cf0-143">True</span></span>                              |
| <span data-ttu-id="59cf0-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="59cf0-144">Is Indexed</span></span>             | <span data-ttu-id="59cf0-145">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-145">False</span></span>                             |
| <span data-ttu-id="59cf0-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="59cf0-146">In Global Catalog</span></span>      | <span data-ttu-id="59cf0-147">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-147">False</span></span>                             |
| <span data-ttu-id="59cf0-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="59cf0-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="59cf0-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="59cf0-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="59cf0-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59cf0-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="59cf0-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59cf0-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="59cf0-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59cf0-152">Search-Flags</span></span>           | <span data-ttu-id="59cf0-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59cf0-153">0x00000000</span></span>                        |
| <span data-ttu-id="59cf0-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59cf0-154">System-Flags</span></span>           | <span data-ttu-id="59cf0-155">0x00000011</span><span class="sxs-lookup"><span data-stu-id="59cf0-155">0x00000011</span></span>                        |
| <span data-ttu-id="59cf0-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="59cf0-156">Classes used in</span></span>        | [<span data-ttu-id="59cf0-157">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="59cf0-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="59cf0-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="59cf0-158">Windows Server 2003</span></span>



| <span data-ttu-id="59cf0-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="59cf0-159">Entry</span></span> | <span data-ttu-id="59cf0-160">Wert</span><span class="sxs-lookup"><span data-stu-id="59cf0-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="59cf0-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="59cf0-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="59cf0-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59cf0-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="59cf0-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="59cf0-163">System-Only</span></span>            | <span data-ttu-id="59cf0-164">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-164">False</span></span>                             |
| <span data-ttu-id="59cf0-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="59cf0-165">Is-Single-Valued</span></span>       | <span data-ttu-id="59cf0-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="59cf0-166">True</span></span>                              |
| <span data-ttu-id="59cf0-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="59cf0-167">Is Indexed</span></span>             | <span data-ttu-id="59cf0-168">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-168">False</span></span>                             |
| <span data-ttu-id="59cf0-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="59cf0-169">In Global Catalog</span></span>      | <span data-ttu-id="59cf0-170">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-170">False</span></span>                             |
| <span data-ttu-id="59cf0-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="59cf0-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="59cf0-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="59cf0-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="59cf0-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59cf0-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="59cf0-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59cf0-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="59cf0-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59cf0-175">Search-Flags</span></span>           | <span data-ttu-id="59cf0-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59cf0-176">0x00000000</span></span>                        |
| <span data-ttu-id="59cf0-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59cf0-177">System-Flags</span></span>           | <span data-ttu-id="59cf0-178">0x00000011</span><span class="sxs-lookup"><span data-stu-id="59cf0-178">0x00000011</span></span>                        |
| <span data-ttu-id="59cf0-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="59cf0-179">Classes used in</span></span>        | [<span data-ttu-id="59cf0-180">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="59cf0-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="59cf0-181">Adam</span><span class="sxs-lookup"><span data-stu-id="59cf0-181">ADAM</span></span>



| <span data-ttu-id="59cf0-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="59cf0-182">Entry</span></span> | <span data-ttu-id="59cf0-183">Wert</span><span class="sxs-lookup"><span data-stu-id="59cf0-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="59cf0-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="59cf0-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="59cf0-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59cf0-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="59cf0-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="59cf0-186">System-Only</span></span>            | <span data-ttu-id="59cf0-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="59cf0-187">True</span></span>                                                              |
| <span data-ttu-id="59cf0-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="59cf0-188">Is-Single-Valued</span></span>       | <span data-ttu-id="59cf0-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="59cf0-189">True</span></span>                                                              |
| <span data-ttu-id="59cf0-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="59cf0-190">Is Indexed</span></span>             | <span data-ttu-id="59cf0-191">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-191">False</span></span>                                                             |
| <span data-ttu-id="59cf0-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="59cf0-192">In Global Catalog</span></span>      | <span data-ttu-id="59cf0-193">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-193">False</span></span>                                                             |
| <span data-ttu-id="59cf0-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="59cf0-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="59cf0-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="59cf0-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="59cf0-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59cf0-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="59cf0-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59cf0-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="59cf0-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59cf0-198">Search-Flags</span></span>           | <span data-ttu-id="59cf0-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59cf0-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="59cf0-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59cf0-200">System-Flags</span></span>           | <span data-ttu-id="59cf0-201">0x00000011</span><span class="sxs-lookup"><span data-stu-id="59cf0-201">0x00000011</span></span>                                                        |
| <span data-ttu-id="59cf0-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="59cf0-202">Classes used in</span></span>        | [<span data-ttu-id="59cf0-203">**ms-DS-Bindable-Objekt**</span><span class="sxs-lookup"><span data-stu-id="59cf0-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="59cf0-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="59cf0-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="59cf0-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="59cf0-205">Entry</span></span> | <span data-ttu-id="59cf0-206">Wert</span><span class="sxs-lookup"><span data-stu-id="59cf0-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="59cf0-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="59cf0-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="59cf0-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59cf0-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="59cf0-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="59cf0-209">System-Only</span></span>            | <span data-ttu-id="59cf0-210">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-210">False</span></span>                             |
| <span data-ttu-id="59cf0-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="59cf0-211">Is-Single-Valued</span></span>       | <span data-ttu-id="59cf0-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="59cf0-212">True</span></span>                              |
| <span data-ttu-id="59cf0-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="59cf0-213">Is Indexed</span></span>             | <span data-ttu-id="59cf0-214">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-214">False</span></span>                             |
| <span data-ttu-id="59cf0-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="59cf0-215">In Global Catalog</span></span>      | <span data-ttu-id="59cf0-216">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-216">False</span></span>                             |
| <span data-ttu-id="59cf0-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="59cf0-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="59cf0-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="59cf0-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="59cf0-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59cf0-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="59cf0-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59cf0-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="59cf0-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59cf0-221">Search-Flags</span></span>           | <span data-ttu-id="59cf0-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59cf0-222">0x00000000</span></span>                        |
| <span data-ttu-id="59cf0-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59cf0-223">System-Flags</span></span>           | <span data-ttu-id="59cf0-224">0x00000011</span><span class="sxs-lookup"><span data-stu-id="59cf0-224">0x00000011</span></span>                        |
| <span data-ttu-id="59cf0-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="59cf0-225">Classes used in</span></span>        | [<span data-ttu-id="59cf0-226">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="59cf0-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="59cf0-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59cf0-227">Windows Server 2008</span></span>



| <span data-ttu-id="59cf0-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="59cf0-228">Entry</span></span> | <span data-ttu-id="59cf0-229">Wert</span><span class="sxs-lookup"><span data-stu-id="59cf0-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="59cf0-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="59cf0-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="59cf0-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59cf0-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="59cf0-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="59cf0-232">System-Only</span></span>            | <span data-ttu-id="59cf0-233">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-233">False</span></span>                             |
| <span data-ttu-id="59cf0-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="59cf0-234">Is-Single-Valued</span></span>       | <span data-ttu-id="59cf0-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="59cf0-235">True</span></span>                              |
| <span data-ttu-id="59cf0-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="59cf0-236">Is Indexed</span></span>             | <span data-ttu-id="59cf0-237">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-237">False</span></span>                             |
| <span data-ttu-id="59cf0-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="59cf0-238">In Global Catalog</span></span>      | <span data-ttu-id="59cf0-239">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-239">False</span></span>                             |
| <span data-ttu-id="59cf0-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="59cf0-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="59cf0-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="59cf0-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="59cf0-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59cf0-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="59cf0-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59cf0-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="59cf0-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59cf0-244">Search-Flags</span></span>           | <span data-ttu-id="59cf0-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59cf0-245">0x00000000</span></span>                        |
| <span data-ttu-id="59cf0-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59cf0-246">System-Flags</span></span>           | <span data-ttu-id="59cf0-247">0x00000011</span><span class="sxs-lookup"><span data-stu-id="59cf0-247">0x00000011</span></span>                        |
| <span data-ttu-id="59cf0-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="59cf0-248">Classes used in</span></span>        | [<span data-ttu-id="59cf0-249">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="59cf0-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="59cf0-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="59cf0-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="59cf0-251">Eingabe</span><span class="sxs-lookup"><span data-stu-id="59cf0-251">Entry</span></span> | <span data-ttu-id="59cf0-252">Wert</span><span class="sxs-lookup"><span data-stu-id="59cf0-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="59cf0-253">Link-ID</span><span class="sxs-lookup"><span data-stu-id="59cf0-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="59cf0-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59cf0-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="59cf0-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="59cf0-255">System-Only</span></span>            | <span data-ttu-id="59cf0-256">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-256">False</span></span>                             |
| <span data-ttu-id="59cf0-257">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="59cf0-257">Is-Single-Valued</span></span>       | <span data-ttu-id="59cf0-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="59cf0-258">True</span></span>                              |
| <span data-ttu-id="59cf0-259">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="59cf0-259">Is Indexed</span></span>             | <span data-ttu-id="59cf0-260">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-260">False</span></span>                             |
| <span data-ttu-id="59cf0-261">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="59cf0-261">In Global Catalog</span></span>      | <span data-ttu-id="59cf0-262">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-262">False</span></span>                             |
| <span data-ttu-id="59cf0-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="59cf0-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="59cf0-264">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="59cf0-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="59cf0-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59cf0-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="59cf0-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59cf0-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="59cf0-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59cf0-267">Search-Flags</span></span>           | <span data-ttu-id="59cf0-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59cf0-268">0x00000000</span></span>                        |
| <span data-ttu-id="59cf0-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59cf0-269">System-Flags</span></span>           | <span data-ttu-id="59cf0-270">0x00000011</span><span class="sxs-lookup"><span data-stu-id="59cf0-270">0x00000011</span></span>                        |
| <span data-ttu-id="59cf0-271">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="59cf0-271">Classes used in</span></span>        | [<span data-ttu-id="59cf0-272">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="59cf0-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="59cf0-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="59cf0-273">Windows Server 2012</span></span>



| <span data-ttu-id="59cf0-274">Eingabe</span><span class="sxs-lookup"><span data-stu-id="59cf0-274">Entry</span></span> | <span data-ttu-id="59cf0-275">Wert</span><span class="sxs-lookup"><span data-stu-id="59cf0-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="59cf0-276">Link-ID</span><span class="sxs-lookup"><span data-stu-id="59cf0-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="59cf0-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59cf0-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="59cf0-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="59cf0-278">System-Only</span></span>            | <span data-ttu-id="59cf0-279">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-279">False</span></span>                             |
| <span data-ttu-id="59cf0-280">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="59cf0-280">Is-Single-Valued</span></span>       | <span data-ttu-id="59cf0-281">Richtig</span><span class="sxs-lookup"><span data-stu-id="59cf0-281">True</span></span>                              |
| <span data-ttu-id="59cf0-282">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="59cf0-282">Is Indexed</span></span>             | <span data-ttu-id="59cf0-283">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-283">False</span></span>                             |
| <span data-ttu-id="59cf0-284">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="59cf0-284">In Global Catalog</span></span>      | <span data-ttu-id="59cf0-285">False</span><span class="sxs-lookup"><span data-stu-id="59cf0-285">False</span></span>                             |
| <span data-ttu-id="59cf0-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="59cf0-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="59cf0-287">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="59cf0-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="59cf0-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59cf0-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="59cf0-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59cf0-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="59cf0-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59cf0-290">Search-Flags</span></span>           | <span data-ttu-id="59cf0-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59cf0-291">0x00000000</span></span>                        |
| <span data-ttu-id="59cf0-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59cf0-292">System-Flags</span></span>           | <span data-ttu-id="59cf0-293">0x00000011</span><span class="sxs-lookup"><span data-stu-id="59cf0-293">0x00000011</span></span>                        |
| <span data-ttu-id="59cf0-294">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="59cf0-294">Classes used in</span></span>        | [<span data-ttu-id="59cf0-295">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="59cf0-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="59cf0-296">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59cf0-296">Remarks</span></span>

<span data-ttu-id="59cf0-297">Der hohe Teil dieser großen Ganzzahl entspricht dem **dwHighDateTime** -Member der [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Struktur, und der niedrige Teil entspricht dem **dwLowDateTime** -Member der **FILETIME** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="59cf0-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="59cf0-298">Dieses Attribut wird nicht repliziert und auf jedem Domänen Controller in der Domäne separat verwaltet.</span><span class="sxs-lookup"><span data-stu-id="59cf0-298">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="59cf0-299">Um einen exakten Wert für die letzte ungültige Kenn Wort Zeit des Benutzers in der Domäne zu erhalten, muss jeder Domänen Controller in der Domäne abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="59cf0-299">To get an accurate value for the user's last bad password time in the domain, each domain controller in the domain must be queried.</span></span> <span data-ttu-id="59cf0-300">Der größte Wert, der abgerufen wird, stellt die echte ungültige Kenn Wort Zeit dar.</span><span class="sxs-lookup"><span data-stu-id="59cf0-300">The largest value that is obtained represents the true bad password time.</span></span>

 

