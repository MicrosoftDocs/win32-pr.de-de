---
title: Account-Expires-Attribut
description: Das Datum, an dem das Konto abläuft.
ms.assetid: 8c3c565e-77fe-4e8b-970a-8396fc6b45aa
ms.tgt_platform: multiple
keywords:
- AD-Schema für Account-Expires-Attribut
- AccountExpires-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Account-Expires
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb5041c544f96f79ad4c3172d776ebe909b1983
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346798"
---
# <a name="account-expires-attribute"></a><span data-ttu-id="f89c7-105">Account-Expires-Attribut</span><span class="sxs-lookup"><span data-stu-id="f89c7-105">Account-Expires attribute</span></span>

<span data-ttu-id="f89c7-106">Das Datum, an dem das Konto abläuft.</span><span class="sxs-lookup"><span data-stu-id="f89c7-106">The date when the account expires.</span></span> <span data-ttu-id="f89c7-107">Dieser Wert stellt die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601 (UTC) dar.</span><span class="sxs-lookup"><span data-stu-id="f89c7-107">This value represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="f89c7-108">Der Wert 0 oder 0x7FFFFFFFFFFFFFFF (9223372036854775807) gibt an, dass das Konto nie abläuft.</span><span class="sxs-lookup"><span data-stu-id="f89c7-108">A value of 0 or 0x7FFFFFFFFFFFFFFF (9223372036854775807) indicates that the account never expires.</span></span>



| <span data-ttu-id="f89c7-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f89c7-109">Entry</span></span> | <span data-ttu-id="f89c7-110">Wert</span><span class="sxs-lookup"><span data-stu-id="f89c7-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="f89c7-111">CN</span><span class="sxs-lookup"><span data-stu-id="f89c7-111">CN</span></span>                | <span data-ttu-id="f89c7-112">Account-Expires</span><span class="sxs-lookup"><span data-stu-id="f89c7-112">Account-Expires</span></span>                                                        |
| <span data-ttu-id="f89c7-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f89c7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f89c7-114">AccountExpires</span><span class="sxs-lookup"><span data-stu-id="f89c7-114">accountExpires</span></span>                                                         |
| <span data-ttu-id="f89c7-115">Size</span><span class="sxs-lookup"><span data-stu-id="f89c7-115">Size</span></span>              | <span data-ttu-id="f89c7-116">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="f89c7-116">8 bytes</span></span>                                                                |
| <span data-ttu-id="f89c7-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f89c7-117">Update Privilege</span></span>  | <span data-ttu-id="f89c7-118">Der Domänen Administrator legt dieses Attribut fest.</span><span class="sxs-lookup"><span data-stu-id="f89c7-118">The domain administrator sets this attribute.</span></span>                          |
| <span data-ttu-id="f89c7-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f89c7-119">Update Frequency</span></span>  | <span data-ttu-id="f89c7-120">Wenn das vorherige Ablaufdatum abläuft und aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="f89c7-120">Whenever the previous expiration date expires and needs to be updated.</span></span> |
| <span data-ttu-id="f89c7-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f89c7-121">Attribute-Id</span></span>      | <span data-ttu-id="f89c7-122">1.2.840.113556.1.4.159</span><span class="sxs-lookup"><span data-stu-id="f89c7-122">1.2.840.113556.1.4.159</span></span>                                                 |
| <span data-ttu-id="f89c7-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f89c7-123">System-Id-Guid</span></span>    | <span data-ttu-id="f89c7-124">bf967915-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f89c7-124">bf967915-0de6-11d0-a285-00aa003049e2</span></span>                                   |
| <span data-ttu-id="f89c7-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="f89c7-125">Syntax</span></span>            | [<span data-ttu-id="f89c7-126">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="f89c7-126">**Interval**</span></span>](s-interval.md)                                         |



## <a name="implementations"></a><span data-ttu-id="f89c7-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f89c7-127">Implementations</span></span>

-   [<span data-ttu-id="f89c7-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f89c7-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f89c7-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f89c7-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f89c7-130">**Adam**</span><span class="sxs-lookup"><span data-stu-id="f89c7-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f89c7-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f89c7-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f89c7-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f89c7-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f89c7-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f89c7-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f89c7-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f89c7-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f89c7-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f89c7-135">Windows 2000 Server</span></span>



| <span data-ttu-id="f89c7-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f89c7-136">Entry</span></span> | <span data-ttu-id="f89c7-137">Wert</span><span class="sxs-lookup"><span data-stu-id="f89c7-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f89c7-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f89c7-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f89c7-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f89c7-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f89c7-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="f89c7-140">System-Only</span></span>            | <span data-ttu-id="f89c7-141">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-141">False</span></span>                             |
| <span data-ttu-id="f89c7-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f89c7-142">Is-Single-Valued</span></span>       | <span data-ttu-id="f89c7-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="f89c7-143">True</span></span>                              |
| <span data-ttu-id="f89c7-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f89c7-144">Is Indexed</span></span>             | <span data-ttu-id="f89c7-145">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-145">False</span></span>                             |
| <span data-ttu-id="f89c7-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f89c7-146">In Global Catalog</span></span>      | <span data-ttu-id="f89c7-147">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-147">False</span></span>                             |
| <span data-ttu-id="f89c7-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f89c7-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="f89c7-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f89c7-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f89c7-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f89c7-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f89c7-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f89c7-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f89c7-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f89c7-152">Search-Flags</span></span>           | <span data-ttu-id="f89c7-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f89c7-153">0x00000010</span></span>                        |
| <span data-ttu-id="f89c7-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f89c7-154">System-Flags</span></span>           | <span data-ttu-id="f89c7-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f89c7-155">0x00000010</span></span>                        |
| <span data-ttu-id="f89c7-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f89c7-156">Classes used in</span></span>        | [<span data-ttu-id="f89c7-157">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="f89c7-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f89c7-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f89c7-158">Windows Server 2003</span></span>



| <span data-ttu-id="f89c7-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f89c7-159">Entry</span></span> | <span data-ttu-id="f89c7-160">Wert</span><span class="sxs-lookup"><span data-stu-id="f89c7-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f89c7-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f89c7-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f89c7-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f89c7-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f89c7-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="f89c7-163">System-Only</span></span>            | <span data-ttu-id="f89c7-164">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-164">False</span></span>                             |
| <span data-ttu-id="f89c7-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f89c7-165">Is-Single-Valued</span></span>       | <span data-ttu-id="f89c7-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="f89c7-166">True</span></span>                              |
| <span data-ttu-id="f89c7-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f89c7-167">Is Indexed</span></span>             | <span data-ttu-id="f89c7-168">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-168">False</span></span>                             |
| <span data-ttu-id="f89c7-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f89c7-169">In Global Catalog</span></span>      | <span data-ttu-id="f89c7-170">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-170">False</span></span>                             |
| <span data-ttu-id="f89c7-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f89c7-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="f89c7-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f89c7-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f89c7-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f89c7-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f89c7-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f89c7-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f89c7-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f89c7-175">Search-Flags</span></span>           | <span data-ttu-id="f89c7-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f89c7-176">0x00000010</span></span>                        |
| <span data-ttu-id="f89c7-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f89c7-177">System-Flags</span></span>           | <span data-ttu-id="f89c7-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f89c7-178">0x00000010</span></span>                        |
| <span data-ttu-id="f89c7-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f89c7-179">Classes used in</span></span>        | [<span data-ttu-id="f89c7-180">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="f89c7-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f89c7-181">Adam</span><span class="sxs-lookup"><span data-stu-id="f89c7-181">ADAM</span></span>



| <span data-ttu-id="f89c7-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f89c7-182">Entry</span></span> | <span data-ttu-id="f89c7-183">Wert</span><span class="sxs-lookup"><span data-stu-id="f89c7-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f89c7-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f89c7-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f89c7-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f89c7-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f89c7-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="f89c7-186">System-Only</span></span>            | <span data-ttu-id="f89c7-187">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-187">False</span></span>                                                             |
| <span data-ttu-id="f89c7-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f89c7-188">Is-Single-Valued</span></span>       | <span data-ttu-id="f89c7-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="f89c7-189">True</span></span>                                                              |
| <span data-ttu-id="f89c7-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f89c7-190">Is Indexed</span></span>             | <span data-ttu-id="f89c7-191">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-191">False</span></span>                                                             |
| <span data-ttu-id="f89c7-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f89c7-192">In Global Catalog</span></span>      | <span data-ttu-id="f89c7-193">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-193">False</span></span>                                                             |
| <span data-ttu-id="f89c7-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f89c7-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="f89c7-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f89c7-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f89c7-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f89c7-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f89c7-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f89c7-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f89c7-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f89c7-198">Search-Flags</span></span>           | <span data-ttu-id="f89c7-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f89c7-199">0x00000010</span></span>                                                        |
| <span data-ttu-id="f89c7-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f89c7-200">System-Flags</span></span>           | <span data-ttu-id="f89c7-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f89c7-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="f89c7-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f89c7-202">Classes used in</span></span>        | [<span data-ttu-id="f89c7-203">**ms-DS-Bindable-Objekt**</span><span class="sxs-lookup"><span data-stu-id="f89c7-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f89c7-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f89c7-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f89c7-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f89c7-205">Entry</span></span> | <span data-ttu-id="f89c7-206">Wert</span><span class="sxs-lookup"><span data-stu-id="f89c7-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f89c7-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f89c7-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f89c7-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f89c7-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f89c7-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="f89c7-209">System-Only</span></span>            | <span data-ttu-id="f89c7-210">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-210">False</span></span>                             |
| <span data-ttu-id="f89c7-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f89c7-211">Is-Single-Valued</span></span>       | <span data-ttu-id="f89c7-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="f89c7-212">True</span></span>                              |
| <span data-ttu-id="f89c7-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f89c7-213">Is Indexed</span></span>             | <span data-ttu-id="f89c7-214">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-214">False</span></span>                             |
| <span data-ttu-id="f89c7-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f89c7-215">In Global Catalog</span></span>      | <span data-ttu-id="f89c7-216">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-216">False</span></span>                             |
| <span data-ttu-id="f89c7-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f89c7-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="f89c7-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f89c7-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f89c7-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f89c7-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f89c7-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f89c7-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f89c7-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f89c7-221">Search-Flags</span></span>           | <span data-ttu-id="f89c7-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f89c7-222">0x00000010</span></span>                        |
| <span data-ttu-id="f89c7-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f89c7-223">System-Flags</span></span>           | <span data-ttu-id="f89c7-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f89c7-224">0x00000010</span></span>                        |
| <span data-ttu-id="f89c7-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f89c7-225">Classes used in</span></span>        | [<span data-ttu-id="f89c7-226">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="f89c7-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f89c7-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f89c7-227">Windows Server 2008</span></span>



| <span data-ttu-id="f89c7-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f89c7-228">Entry</span></span> | <span data-ttu-id="f89c7-229">Wert</span><span class="sxs-lookup"><span data-stu-id="f89c7-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f89c7-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f89c7-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f89c7-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f89c7-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f89c7-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="f89c7-232">System-Only</span></span>            | <span data-ttu-id="f89c7-233">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-233">False</span></span>                             |
| <span data-ttu-id="f89c7-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f89c7-234">Is-Single-Valued</span></span>       | <span data-ttu-id="f89c7-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="f89c7-235">True</span></span>                              |
| <span data-ttu-id="f89c7-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f89c7-236">Is Indexed</span></span>             | <span data-ttu-id="f89c7-237">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-237">False</span></span>                             |
| <span data-ttu-id="f89c7-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f89c7-238">In Global Catalog</span></span>      | <span data-ttu-id="f89c7-239">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-239">False</span></span>                             |
| <span data-ttu-id="f89c7-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f89c7-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="f89c7-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f89c7-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f89c7-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f89c7-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f89c7-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f89c7-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f89c7-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f89c7-244">Search-Flags</span></span>           | <span data-ttu-id="f89c7-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f89c7-245">0x00000010</span></span>                        |
| <span data-ttu-id="f89c7-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f89c7-246">System-Flags</span></span>           | <span data-ttu-id="f89c7-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f89c7-247">0x00000010</span></span>                        |
| <span data-ttu-id="f89c7-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f89c7-248">Classes used in</span></span>        | [<span data-ttu-id="f89c7-249">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="f89c7-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f89c7-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f89c7-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f89c7-251">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f89c7-251">Entry</span></span> | <span data-ttu-id="f89c7-252">Wert</span><span class="sxs-lookup"><span data-stu-id="f89c7-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f89c7-253">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f89c7-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f89c7-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f89c7-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f89c7-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="f89c7-255">System-Only</span></span>            | <span data-ttu-id="f89c7-256">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-256">False</span></span>                             |
| <span data-ttu-id="f89c7-257">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f89c7-257">Is-Single-Valued</span></span>       | <span data-ttu-id="f89c7-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="f89c7-258">True</span></span>                              |
| <span data-ttu-id="f89c7-259">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f89c7-259">Is Indexed</span></span>             | <span data-ttu-id="f89c7-260">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-260">False</span></span>                             |
| <span data-ttu-id="f89c7-261">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f89c7-261">In Global Catalog</span></span>      | <span data-ttu-id="f89c7-262">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-262">False</span></span>                             |
| <span data-ttu-id="f89c7-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f89c7-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="f89c7-264">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f89c7-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f89c7-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f89c7-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f89c7-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f89c7-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f89c7-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f89c7-267">Search-Flags</span></span>           | <span data-ttu-id="f89c7-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f89c7-268">0x00000010</span></span>                        |
| <span data-ttu-id="f89c7-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f89c7-269">System-Flags</span></span>           | <span data-ttu-id="f89c7-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f89c7-270">0x00000010</span></span>                        |
| <span data-ttu-id="f89c7-271">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f89c7-271">Classes used in</span></span>        | [<span data-ttu-id="f89c7-272">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="f89c7-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f89c7-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f89c7-273">Windows Server 2012</span></span>



| <span data-ttu-id="f89c7-274">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f89c7-274">Entry</span></span> | <span data-ttu-id="f89c7-275">Wert</span><span class="sxs-lookup"><span data-stu-id="f89c7-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f89c7-276">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f89c7-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f89c7-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f89c7-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f89c7-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="f89c7-278">System-Only</span></span>            | <span data-ttu-id="f89c7-279">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-279">False</span></span>                             |
| <span data-ttu-id="f89c7-280">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f89c7-280">Is-Single-Valued</span></span>       | <span data-ttu-id="f89c7-281">Richtig</span><span class="sxs-lookup"><span data-stu-id="f89c7-281">True</span></span>                              |
| <span data-ttu-id="f89c7-282">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f89c7-282">Is Indexed</span></span>             | <span data-ttu-id="f89c7-283">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-283">False</span></span>                             |
| <span data-ttu-id="f89c7-284">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f89c7-284">In Global Catalog</span></span>      | <span data-ttu-id="f89c7-285">False</span><span class="sxs-lookup"><span data-stu-id="f89c7-285">False</span></span>                             |
| <span data-ttu-id="f89c7-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f89c7-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="f89c7-287">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f89c7-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f89c7-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f89c7-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f89c7-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f89c7-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f89c7-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f89c7-290">Search-Flags</span></span>           | <span data-ttu-id="f89c7-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f89c7-291">0x00000010</span></span>                        |
| <span data-ttu-id="f89c7-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f89c7-292">System-Flags</span></span>           | <span data-ttu-id="f89c7-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f89c7-293">0x00000010</span></span>                        |
| <span data-ttu-id="f89c7-294">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f89c7-294">Classes used in</span></span>        | [<span data-ttu-id="f89c7-295">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="f89c7-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f89c7-296">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f89c7-296">Remarks</span></span>

<span data-ttu-id="f89c7-297">Der hohe Teil dieser großen Ganzzahl entspricht dem **dwHighDateTime** -Member der [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Struktur, und der niedrige Teil entspricht dem **dwLowDateTime** -Member der **FILETIME** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f89c7-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

 

