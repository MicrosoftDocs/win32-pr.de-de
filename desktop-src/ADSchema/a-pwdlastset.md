---
title: PWD-letztes Set-Attribut
description: Das Datum und die Uhrzeit der letzten Änderung des Kennworts für dieses Konto.
ms.assetid: 06ca5cd5-a285-488a-9db0-c698b82a847d
ms.tgt_platform: multiple
keywords:
- PWD-letztes Set-Attribut AD-Schema
- AD-Schema des pwdLastSet-Attributs
topic_type:
- apiref
api_name:
- Pwd-Last-Set
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc49fbbf768d2ca873f6f35f61022cc9182830b1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344757"
---
# <a name="pwd-last-set-attribute"></a><span data-ttu-id="1024c-105">PWD-letztes Set-Attribut</span><span class="sxs-lookup"><span data-stu-id="1024c-105">Pwd-Last-Set attribute</span></span>

<span data-ttu-id="1024c-106">Das Datum und die Uhrzeit der letzten Änderung des Kennworts für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="1024c-106">The date and time that the password for this account was last changed.</span></span> <span data-ttu-id="1024c-107">Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von 100 Nanosekunden-Intervallen seit dem 1. Januar 1601 (UTC) darstellt.</span><span class="sxs-lookup"><span data-stu-id="1024c-107">This value is stored as a large integer that represents the number of 100 nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="1024c-108">Wenn dieser Wert auf 0 festgelegt ist und das Attribut " [**User-Account-Control**](a-useraccountcontrol.md) " nicht das Kennwort " **UF \_ 't \_ expire \_ passwd** " enthält, muss der Benutzer das Kennwort bei der nächsten Anmeldung festlegen.</span><span class="sxs-lookup"><span data-stu-id="1024c-108">If this value is set to 0 and the [**User-Account-Control**](a-useraccountcontrol.md) attribute does not contain the **UF\_DONT\_EXPIRE\_PASSWD** flag, then the user must set the password at the next logon.</span></span>



| <span data-ttu-id="1024c-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1024c-109">Entry</span></span> | <span data-ttu-id="1024c-110">Wert</span><span class="sxs-lookup"><span data-stu-id="1024c-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1024c-111">CN</span><span class="sxs-lookup"><span data-stu-id="1024c-111">CN</span></span>                | <span data-ttu-id="1024c-112">PWD-letztes Set</span><span class="sxs-lookup"><span data-stu-id="1024c-112">Pwd-Last-Set</span></span>                         |
| <span data-ttu-id="1024c-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1024c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1024c-114">pwdLastSet</span><span class="sxs-lookup"><span data-stu-id="1024c-114">pwdLastSet</span></span>                           |
| <span data-ttu-id="1024c-115">Size</span><span class="sxs-lookup"><span data-stu-id="1024c-115">Size</span></span>              | <span data-ttu-id="1024c-116">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="1024c-116">8 bytes</span></span>                              |
| <span data-ttu-id="1024c-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="1024c-117">Update Privilege</span></span>  | <span data-ttu-id="1024c-118">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1024c-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="1024c-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="1024c-119">Update Frequency</span></span>  | <span data-ttu-id="1024c-120">Jedes Mal, wenn das Kennwort geändert wird.</span><span class="sxs-lookup"><span data-stu-id="1024c-120">Each time the password is changed.</span></span>   |
| <span data-ttu-id="1024c-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1024c-121">Attribute-Id</span></span>      | <span data-ttu-id="1024c-122">1.2.840.113556.1.4.96</span><span class="sxs-lookup"><span data-stu-id="1024c-122">1.2.840.113556.1.4.96</span></span>                |
| <span data-ttu-id="1024c-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1024c-123">System-Id-Guid</span></span>    | <span data-ttu-id="1024c-124">bf967a0a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1024c-124">bf967a0a-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="1024c-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="1024c-125">Syntax</span></span>            | [<span data-ttu-id="1024c-126">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="1024c-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="1024c-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="1024c-127">Implementations</span></span>

-   [<span data-ttu-id="1024c-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1024c-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1024c-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1024c-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1024c-130">**Adam**</span><span class="sxs-lookup"><span data-stu-id="1024c-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1024c-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1024c-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1024c-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1024c-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1024c-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1024c-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1024c-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1024c-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1024c-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1024c-135">Windows 2000 Server</span></span>



| <span data-ttu-id="1024c-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1024c-136">Entry</span></span> | <span data-ttu-id="1024c-137">Wert</span><span class="sxs-lookup"><span data-stu-id="1024c-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1024c-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1024c-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1024c-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1024c-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1024c-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="1024c-140">System-Only</span></span>            | <span data-ttu-id="1024c-141">False</span><span class="sxs-lookup"><span data-stu-id="1024c-141">False</span></span>                             |
| <span data-ttu-id="1024c-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1024c-142">Is-Single-Valued</span></span>       | <span data-ttu-id="1024c-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="1024c-143">True</span></span>                              |
| <span data-ttu-id="1024c-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1024c-144">Is Indexed</span></span>             | <span data-ttu-id="1024c-145">False</span><span class="sxs-lookup"><span data-stu-id="1024c-145">False</span></span>                             |
| <span data-ttu-id="1024c-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1024c-146">In Global Catalog</span></span>      | <span data-ttu-id="1024c-147">False</span><span class="sxs-lookup"><span data-stu-id="1024c-147">False</span></span>                             |
| <span data-ttu-id="1024c-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1024c-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="1024c-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1024c-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1024c-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1024c-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1024c-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1024c-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1024c-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1024c-152">Search-Flags</span></span>           | <span data-ttu-id="1024c-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1024c-153">0x00000000</span></span>                        |
| <span data-ttu-id="1024c-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1024c-154">System-Flags</span></span>           | <span data-ttu-id="1024c-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1024c-155">0x00000010</span></span>                        |
| <span data-ttu-id="1024c-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1024c-156">Classes used in</span></span>        | [<span data-ttu-id="1024c-157">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="1024c-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1024c-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1024c-158">Windows Server 2003</span></span>



| <span data-ttu-id="1024c-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1024c-159">Entry</span></span> | <span data-ttu-id="1024c-160">Wert</span><span class="sxs-lookup"><span data-stu-id="1024c-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1024c-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1024c-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1024c-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1024c-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1024c-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="1024c-163">System-Only</span></span>            | <span data-ttu-id="1024c-164">False</span><span class="sxs-lookup"><span data-stu-id="1024c-164">False</span></span>                             |
| <span data-ttu-id="1024c-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1024c-165">Is-Single-Valued</span></span>       | <span data-ttu-id="1024c-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="1024c-166">True</span></span>                              |
| <span data-ttu-id="1024c-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1024c-167">Is Indexed</span></span>             | <span data-ttu-id="1024c-168">False</span><span class="sxs-lookup"><span data-stu-id="1024c-168">False</span></span>                             |
| <span data-ttu-id="1024c-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1024c-169">In Global Catalog</span></span>      | <span data-ttu-id="1024c-170">False</span><span class="sxs-lookup"><span data-stu-id="1024c-170">False</span></span>                             |
| <span data-ttu-id="1024c-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1024c-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="1024c-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1024c-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1024c-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1024c-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1024c-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1024c-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1024c-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1024c-175">Search-Flags</span></span>           | <span data-ttu-id="1024c-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1024c-176">0x00000000</span></span>                        |
| <span data-ttu-id="1024c-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1024c-177">System-Flags</span></span>           | <span data-ttu-id="1024c-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1024c-178">0x00000010</span></span>                        |
| <span data-ttu-id="1024c-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1024c-179">Classes used in</span></span>        | [<span data-ttu-id="1024c-180">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="1024c-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1024c-181">Adam</span><span class="sxs-lookup"><span data-stu-id="1024c-181">ADAM</span></span>



| <span data-ttu-id="1024c-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1024c-182">Entry</span></span> | <span data-ttu-id="1024c-183">Wert</span><span class="sxs-lookup"><span data-stu-id="1024c-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="1024c-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1024c-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1024c-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1024c-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1024c-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="1024c-186">System-Only</span></span>            | <span data-ttu-id="1024c-187">False</span><span class="sxs-lookup"><span data-stu-id="1024c-187">False</span></span>                                                             |
| <span data-ttu-id="1024c-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1024c-188">Is-Single-Valued</span></span>       | <span data-ttu-id="1024c-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="1024c-189">True</span></span>                                                              |
| <span data-ttu-id="1024c-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1024c-190">Is Indexed</span></span>             | <span data-ttu-id="1024c-191">False</span><span class="sxs-lookup"><span data-stu-id="1024c-191">False</span></span>                                                             |
| <span data-ttu-id="1024c-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1024c-192">In Global Catalog</span></span>      | <span data-ttu-id="1024c-193">False</span><span class="sxs-lookup"><span data-stu-id="1024c-193">False</span></span>                                                             |
| <span data-ttu-id="1024c-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1024c-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="1024c-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1024c-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="1024c-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1024c-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="1024c-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1024c-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="1024c-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1024c-198">Search-Flags</span></span>           | <span data-ttu-id="1024c-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1024c-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="1024c-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1024c-200">System-Flags</span></span>           | <span data-ttu-id="1024c-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1024c-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="1024c-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1024c-202">Classes used in</span></span>        | [<span data-ttu-id="1024c-203">**ms-DS-Bindable-Objekt**</span><span class="sxs-lookup"><span data-stu-id="1024c-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1024c-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1024c-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1024c-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1024c-205">Entry</span></span> | <span data-ttu-id="1024c-206">Wert</span><span class="sxs-lookup"><span data-stu-id="1024c-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1024c-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1024c-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1024c-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1024c-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1024c-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="1024c-209">System-Only</span></span>            | <span data-ttu-id="1024c-210">False</span><span class="sxs-lookup"><span data-stu-id="1024c-210">False</span></span>                             |
| <span data-ttu-id="1024c-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1024c-211">Is-Single-Valued</span></span>       | <span data-ttu-id="1024c-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="1024c-212">True</span></span>                              |
| <span data-ttu-id="1024c-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1024c-213">Is Indexed</span></span>             | <span data-ttu-id="1024c-214">False</span><span class="sxs-lookup"><span data-stu-id="1024c-214">False</span></span>                             |
| <span data-ttu-id="1024c-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1024c-215">In Global Catalog</span></span>      | <span data-ttu-id="1024c-216">False</span><span class="sxs-lookup"><span data-stu-id="1024c-216">False</span></span>                             |
| <span data-ttu-id="1024c-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1024c-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="1024c-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1024c-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1024c-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1024c-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1024c-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1024c-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1024c-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1024c-221">Search-Flags</span></span>           | <span data-ttu-id="1024c-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1024c-222">0x00000000</span></span>                        |
| <span data-ttu-id="1024c-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1024c-223">System-Flags</span></span>           | <span data-ttu-id="1024c-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1024c-224">0x00000010</span></span>                        |
| <span data-ttu-id="1024c-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1024c-225">Classes used in</span></span>        | [<span data-ttu-id="1024c-226">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="1024c-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1024c-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1024c-227">Windows Server 2008</span></span>



| <span data-ttu-id="1024c-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1024c-228">Entry</span></span> | <span data-ttu-id="1024c-229">Wert</span><span class="sxs-lookup"><span data-stu-id="1024c-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1024c-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1024c-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1024c-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1024c-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1024c-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="1024c-232">System-Only</span></span>            | <span data-ttu-id="1024c-233">False</span><span class="sxs-lookup"><span data-stu-id="1024c-233">False</span></span>                             |
| <span data-ttu-id="1024c-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1024c-234">Is-Single-Valued</span></span>       | <span data-ttu-id="1024c-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="1024c-235">True</span></span>                              |
| <span data-ttu-id="1024c-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1024c-236">Is Indexed</span></span>             | <span data-ttu-id="1024c-237">False</span><span class="sxs-lookup"><span data-stu-id="1024c-237">False</span></span>                             |
| <span data-ttu-id="1024c-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1024c-238">In Global Catalog</span></span>      | <span data-ttu-id="1024c-239">False</span><span class="sxs-lookup"><span data-stu-id="1024c-239">False</span></span>                             |
| <span data-ttu-id="1024c-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1024c-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="1024c-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1024c-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1024c-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1024c-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1024c-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1024c-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1024c-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1024c-244">Search-Flags</span></span>           | <span data-ttu-id="1024c-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1024c-245">0x00000000</span></span>                        |
| <span data-ttu-id="1024c-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1024c-246">System-Flags</span></span>           | <span data-ttu-id="1024c-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1024c-247">0x00000010</span></span>                        |
| <span data-ttu-id="1024c-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1024c-248">Classes used in</span></span>        | [<span data-ttu-id="1024c-249">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="1024c-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1024c-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1024c-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1024c-251">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1024c-251">Entry</span></span> | <span data-ttu-id="1024c-252">Wert</span><span class="sxs-lookup"><span data-stu-id="1024c-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1024c-253">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1024c-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1024c-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1024c-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1024c-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="1024c-255">System-Only</span></span>            | <span data-ttu-id="1024c-256">False</span><span class="sxs-lookup"><span data-stu-id="1024c-256">False</span></span>                             |
| <span data-ttu-id="1024c-257">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1024c-257">Is-Single-Valued</span></span>       | <span data-ttu-id="1024c-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="1024c-258">True</span></span>                              |
| <span data-ttu-id="1024c-259">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1024c-259">Is Indexed</span></span>             | <span data-ttu-id="1024c-260">False</span><span class="sxs-lookup"><span data-stu-id="1024c-260">False</span></span>                             |
| <span data-ttu-id="1024c-261">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1024c-261">In Global Catalog</span></span>      | <span data-ttu-id="1024c-262">False</span><span class="sxs-lookup"><span data-stu-id="1024c-262">False</span></span>                             |
| <span data-ttu-id="1024c-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1024c-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="1024c-264">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1024c-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1024c-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1024c-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1024c-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1024c-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1024c-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1024c-267">Search-Flags</span></span>           | <span data-ttu-id="1024c-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1024c-268">0x00000000</span></span>                        |
| <span data-ttu-id="1024c-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1024c-269">System-Flags</span></span>           | <span data-ttu-id="1024c-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1024c-270">0x00000010</span></span>                        |
| <span data-ttu-id="1024c-271">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1024c-271">Classes used in</span></span>        | [<span data-ttu-id="1024c-272">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="1024c-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1024c-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1024c-273">Windows Server 2012</span></span>



| <span data-ttu-id="1024c-274">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1024c-274">Entry</span></span> | <span data-ttu-id="1024c-275">Wert</span><span class="sxs-lookup"><span data-stu-id="1024c-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1024c-276">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1024c-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1024c-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1024c-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1024c-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="1024c-278">System-Only</span></span>            | <span data-ttu-id="1024c-279">False</span><span class="sxs-lookup"><span data-stu-id="1024c-279">False</span></span>                             |
| <span data-ttu-id="1024c-280">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1024c-280">Is-Single-Valued</span></span>       | <span data-ttu-id="1024c-281">Richtig</span><span class="sxs-lookup"><span data-stu-id="1024c-281">True</span></span>                              |
| <span data-ttu-id="1024c-282">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1024c-282">Is Indexed</span></span>             | <span data-ttu-id="1024c-283">False</span><span class="sxs-lookup"><span data-stu-id="1024c-283">False</span></span>                             |
| <span data-ttu-id="1024c-284">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1024c-284">In Global Catalog</span></span>      | <span data-ttu-id="1024c-285">False</span><span class="sxs-lookup"><span data-stu-id="1024c-285">False</span></span>                             |
| <span data-ttu-id="1024c-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1024c-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="1024c-287">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1024c-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1024c-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1024c-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1024c-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1024c-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1024c-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1024c-290">Search-Flags</span></span>           | <span data-ttu-id="1024c-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1024c-291">0x00000000</span></span>                        |
| <span data-ttu-id="1024c-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1024c-292">System-Flags</span></span>           | <span data-ttu-id="1024c-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1024c-293">0x00000010</span></span>                        |
| <span data-ttu-id="1024c-294">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1024c-294">Classes used in</span></span>        | [<span data-ttu-id="1024c-295">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="1024c-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="1024c-296">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1024c-296">Remarks</span></span>

<span data-ttu-id="1024c-297">Der hohe Teil dieser großen Ganzzahl entspricht dem **dwHighDateTime** -Member der [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Struktur, und der niedrige Teil entspricht dem **dwLowDateTime** -Member der **FILETIME** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1024c-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

## <a name="see-also"></a><span data-ttu-id="1024c-298">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1024c-298">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1024c-299">**Benutzerkontensteuerung**</span><span class="sxs-lookup"><span data-stu-id="1024c-299">**User-Account-Control**</span></span>](a-useraccountcontrol.md)
</dt> </dl>

 

