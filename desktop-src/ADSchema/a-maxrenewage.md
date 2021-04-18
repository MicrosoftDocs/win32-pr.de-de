---
title: Max-Renew-Age-Attribut
description: Dieses Attribut bestimmt den Zeitraum (in Tagen), in dem das Ticket Erteilungs Ticket (TGT) eines Benutzers für die Kerberos-Authentifizierung erneuert werden kann. Die Standardeinstellung ist 7 Tage im Standard-Domänen Gruppenrichtlinie Objekt (GPO).
ms.assetid: 9e4023d1-b88b-44c9-802b-03387614211d
ms.tgt_platform: multiple
keywords:
- Max-Renew-Age-Attribut AD-Schema
- maxverlänage-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Max-Renew-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0068beff1f7d7af1ab66f01f7236dcc4b0116c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344119"
---
# <a name="max-renew-age-attribute"></a><span data-ttu-id="0040b-106">Max-Renew-Age-Attribut</span><span class="sxs-lookup"><span data-stu-id="0040b-106">Max-Renew-Age attribute</span></span>

<span data-ttu-id="0040b-107">Dieses Attribut bestimmt den Zeitraum (in Tagen), in dem das Ticket Erteilungs Ticket (TGT) eines Benutzers für die Kerberos-Authentifizierung erneuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0040b-107">This attribute determines the time period, in days, during which a user's ticket-granting ticket (TGT) can be renewed for purposes of Kerberos authentication.</span></span> <span data-ttu-id="0040b-108">Die Standardeinstellung ist 7 Tage im Standard-Domänen Gruppenrichtlinie Objekt (GPO).</span><span class="sxs-lookup"><span data-stu-id="0040b-108">The default setting is 7 days in the Default Domain Group Policy object (GPO).</span></span>



| <span data-ttu-id="0040b-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0040b-109">Entry</span></span> | <span data-ttu-id="0040b-110">Wert</span><span class="sxs-lookup"><span data-stu-id="0040b-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0040b-111">CN</span><span class="sxs-lookup"><span data-stu-id="0040b-111">CN</span></span>                | <span data-ttu-id="0040b-112">Max-Renew-Alter</span><span class="sxs-lookup"><span data-stu-id="0040b-112">Max-Renew-Age</span></span>                        |
| <span data-ttu-id="0040b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0040b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="0040b-114">maxverlänage</span><span class="sxs-lookup"><span data-stu-id="0040b-114">maxRenewAge</span></span>                          |
| <span data-ttu-id="0040b-115">Size</span><span class="sxs-lookup"><span data-stu-id="0040b-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="0040b-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0040b-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="0040b-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="0040b-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="0040b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0040b-118">Attribute-Id</span></span>      | <span data-ttu-id="0040b-119">1.2.840.113556.1.4.75</span><span class="sxs-lookup"><span data-stu-id="0040b-119">1.2.840.113556.1.4.75</span></span>                |
| <span data-ttu-id="0040b-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0040b-120">System-Id-Guid</span></span>    | <span data-ttu-id="0040b-121">bf9679bc-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0040b-121">bf9679bc-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="0040b-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0040b-122">Syntax</span></span>            | [<span data-ttu-id="0040b-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="0040b-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="0040b-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="0040b-124">Implementations</span></span>

-   [<span data-ttu-id="0040b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0040b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0040b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0040b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0040b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0040b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0040b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0040b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0040b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0040b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0040b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0040b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0040b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0040b-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0040b-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0040b-132">Entry</span></span> | <span data-ttu-id="0040b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="0040b-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="0040b-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0040b-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="0040b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0040b-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="0040b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0040b-136">System-Only</span></span>            | <span data-ttu-id="0040b-137">False</span><span class="sxs-lookup"><span data-stu-id="0040b-137">False</span></span>                                              |
| <span data-ttu-id="0040b-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0040b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0040b-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="0040b-139">True</span></span>                                               |
| <span data-ttu-id="0040b-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0040b-140">Is Indexed</span></span>             | <span data-ttu-id="0040b-141">False</span><span class="sxs-lookup"><span data-stu-id="0040b-141">False</span></span>                                              |
| <span data-ttu-id="0040b-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0040b-142">In Global Catalog</span></span>      | <span data-ttu-id="0040b-143">False</span><span class="sxs-lookup"><span data-stu-id="0040b-143">False</span></span>                                              |
| <span data-ttu-id="0040b-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0040b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0040b-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0040b-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="0040b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0040b-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="0040b-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0040b-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="0040b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0040b-148">Search-Flags</span></span>           | <span data-ttu-id="0040b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0040b-149">0x00000000</span></span>                                         |
| <span data-ttu-id="0040b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0040b-150">System-Flags</span></span>           | <span data-ttu-id="0040b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0040b-151">0x00000010</span></span>                                         |
| <span data-ttu-id="0040b-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0040b-152">Classes used in</span></span>        | [<span data-ttu-id="0040b-153">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="0040b-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0040b-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0040b-154">Windows Server 2003</span></span>



| <span data-ttu-id="0040b-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0040b-155">Entry</span></span> | <span data-ttu-id="0040b-156">Wert</span><span class="sxs-lookup"><span data-stu-id="0040b-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="0040b-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0040b-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="0040b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0040b-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="0040b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="0040b-159">System-Only</span></span>            | <span data-ttu-id="0040b-160">False</span><span class="sxs-lookup"><span data-stu-id="0040b-160">False</span></span>                                              |
| <span data-ttu-id="0040b-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0040b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="0040b-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="0040b-162">True</span></span>                                               |
| <span data-ttu-id="0040b-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0040b-163">Is Indexed</span></span>             | <span data-ttu-id="0040b-164">False</span><span class="sxs-lookup"><span data-stu-id="0040b-164">False</span></span>                                              |
| <span data-ttu-id="0040b-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0040b-165">In Global Catalog</span></span>      | <span data-ttu-id="0040b-166">False</span><span class="sxs-lookup"><span data-stu-id="0040b-166">False</span></span>                                              |
| <span data-ttu-id="0040b-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0040b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="0040b-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0040b-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="0040b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0040b-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="0040b-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0040b-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="0040b-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0040b-171">Search-Flags</span></span>           | <span data-ttu-id="0040b-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0040b-172">0x00000000</span></span>                                         |
| <span data-ttu-id="0040b-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0040b-173">System-Flags</span></span>           | <span data-ttu-id="0040b-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0040b-174">0x00000010</span></span>                                         |
| <span data-ttu-id="0040b-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0040b-175">Classes used in</span></span>        | [<span data-ttu-id="0040b-176">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="0040b-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0040b-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0040b-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0040b-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0040b-178">Entry</span></span> | <span data-ttu-id="0040b-179">Wert</span><span class="sxs-lookup"><span data-stu-id="0040b-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="0040b-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0040b-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="0040b-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0040b-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="0040b-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="0040b-182">System-Only</span></span>            | <span data-ttu-id="0040b-183">False</span><span class="sxs-lookup"><span data-stu-id="0040b-183">False</span></span>                                              |
| <span data-ttu-id="0040b-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0040b-184">Is-Single-Valued</span></span>       | <span data-ttu-id="0040b-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="0040b-185">True</span></span>                                               |
| <span data-ttu-id="0040b-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0040b-186">Is Indexed</span></span>             | <span data-ttu-id="0040b-187">False</span><span class="sxs-lookup"><span data-stu-id="0040b-187">False</span></span>                                              |
| <span data-ttu-id="0040b-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0040b-188">In Global Catalog</span></span>      | <span data-ttu-id="0040b-189">False</span><span class="sxs-lookup"><span data-stu-id="0040b-189">False</span></span>                                              |
| <span data-ttu-id="0040b-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0040b-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="0040b-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0040b-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="0040b-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0040b-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="0040b-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0040b-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="0040b-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0040b-194">Search-Flags</span></span>           | <span data-ttu-id="0040b-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0040b-195">0x00000000</span></span>                                         |
| <span data-ttu-id="0040b-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0040b-196">System-Flags</span></span>           | <span data-ttu-id="0040b-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0040b-197">0x00000010</span></span>                                         |
| <span data-ttu-id="0040b-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0040b-198">Classes used in</span></span>        | [<span data-ttu-id="0040b-199">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="0040b-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0040b-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0040b-200">Windows Server 2008</span></span>



| <span data-ttu-id="0040b-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0040b-201">Entry</span></span> | <span data-ttu-id="0040b-202">Wert</span><span class="sxs-lookup"><span data-stu-id="0040b-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="0040b-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0040b-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="0040b-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0040b-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="0040b-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="0040b-205">System-Only</span></span>            | <span data-ttu-id="0040b-206">False</span><span class="sxs-lookup"><span data-stu-id="0040b-206">False</span></span>                                              |
| <span data-ttu-id="0040b-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0040b-207">Is-Single-Valued</span></span>       | <span data-ttu-id="0040b-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="0040b-208">True</span></span>                                               |
| <span data-ttu-id="0040b-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0040b-209">Is Indexed</span></span>             | <span data-ttu-id="0040b-210">False</span><span class="sxs-lookup"><span data-stu-id="0040b-210">False</span></span>                                              |
| <span data-ttu-id="0040b-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0040b-211">In Global Catalog</span></span>      | <span data-ttu-id="0040b-212">False</span><span class="sxs-lookup"><span data-stu-id="0040b-212">False</span></span>                                              |
| <span data-ttu-id="0040b-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0040b-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="0040b-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0040b-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="0040b-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0040b-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="0040b-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0040b-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="0040b-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0040b-217">Search-Flags</span></span>           | <span data-ttu-id="0040b-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0040b-218">0x00000000</span></span>                                         |
| <span data-ttu-id="0040b-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0040b-219">System-Flags</span></span>           | <span data-ttu-id="0040b-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0040b-220">0x00000010</span></span>                                         |
| <span data-ttu-id="0040b-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0040b-221">Classes used in</span></span>        | [<span data-ttu-id="0040b-222">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="0040b-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0040b-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0040b-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0040b-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0040b-224">Entry</span></span> | <span data-ttu-id="0040b-225">Wert</span><span class="sxs-lookup"><span data-stu-id="0040b-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="0040b-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0040b-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="0040b-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0040b-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="0040b-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="0040b-228">System-Only</span></span>            | <span data-ttu-id="0040b-229">False</span><span class="sxs-lookup"><span data-stu-id="0040b-229">False</span></span>                                              |
| <span data-ttu-id="0040b-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0040b-230">Is-Single-Valued</span></span>       | <span data-ttu-id="0040b-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="0040b-231">True</span></span>                                               |
| <span data-ttu-id="0040b-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0040b-232">Is Indexed</span></span>             | <span data-ttu-id="0040b-233">False</span><span class="sxs-lookup"><span data-stu-id="0040b-233">False</span></span>                                              |
| <span data-ttu-id="0040b-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0040b-234">In Global Catalog</span></span>      | <span data-ttu-id="0040b-235">False</span><span class="sxs-lookup"><span data-stu-id="0040b-235">False</span></span>                                              |
| <span data-ttu-id="0040b-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0040b-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="0040b-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0040b-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="0040b-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0040b-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="0040b-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0040b-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="0040b-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0040b-240">Search-Flags</span></span>           | <span data-ttu-id="0040b-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0040b-241">0x00000000</span></span>                                         |
| <span data-ttu-id="0040b-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0040b-242">System-Flags</span></span>           | <span data-ttu-id="0040b-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0040b-243">0x00000010</span></span>                                         |
| <span data-ttu-id="0040b-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0040b-244">Classes used in</span></span>        | [<span data-ttu-id="0040b-245">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="0040b-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0040b-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0040b-246">Windows Server 2012</span></span>



| <span data-ttu-id="0040b-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0040b-247">Entry</span></span> | <span data-ttu-id="0040b-248">Wert</span><span class="sxs-lookup"><span data-stu-id="0040b-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="0040b-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0040b-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="0040b-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0040b-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="0040b-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="0040b-251">System-Only</span></span>            | <span data-ttu-id="0040b-252">False</span><span class="sxs-lookup"><span data-stu-id="0040b-252">False</span></span>                                              |
| <span data-ttu-id="0040b-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0040b-253">Is-Single-Valued</span></span>       | <span data-ttu-id="0040b-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="0040b-254">True</span></span>                                               |
| <span data-ttu-id="0040b-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0040b-255">Is Indexed</span></span>             | <span data-ttu-id="0040b-256">False</span><span class="sxs-lookup"><span data-stu-id="0040b-256">False</span></span>                                              |
| <span data-ttu-id="0040b-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0040b-257">In Global Catalog</span></span>      | <span data-ttu-id="0040b-258">False</span><span class="sxs-lookup"><span data-stu-id="0040b-258">False</span></span>                                              |
| <span data-ttu-id="0040b-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0040b-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="0040b-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0040b-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="0040b-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0040b-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="0040b-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0040b-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="0040b-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0040b-263">Search-Flags</span></span>           | <span data-ttu-id="0040b-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0040b-264">0x00000000</span></span>                                         |
| <span data-ttu-id="0040b-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0040b-265">System-Flags</span></span>           | <span data-ttu-id="0040b-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0040b-266">0x00000010</span></span>                                         |
| <span data-ttu-id="0040b-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0040b-267">Classes used in</span></span>        | [<span data-ttu-id="0040b-268">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="0040b-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





