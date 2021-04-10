---
title: Min-Ticket-Age-Attribut
description: Dieses Attribut bestimmt den minimalen Zeitraum (in Stunden), für den das Ticket Erteilungs Ticket (TGT) eines Benutzers für die Kerberos-Authentifizierung verwendet werden kann, bevor eine Anforderung zum Erneuern des Tickets erteilt werden kann.
ms.assetid: 91a6a8f2-4d8d-4929-8e8d-ffdaa8b05cbe
ms.tgt_platform: multiple
keywords:
- "\"Min-Ticket-Age\"-Attribut AD-Schema"
- Schema des minticketage-Attributs AD
topic_type:
- apiref
api_name:
- Min-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc43277bb3750ee0e759baa4348e85ef826ce010
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107199"
---
# <a name="min-ticket-age-attribute"></a><span data-ttu-id="985bb-105">Min-Ticket-Age-Attribut</span><span class="sxs-lookup"><span data-stu-id="985bb-105">Min-Ticket-Age attribute</span></span>

<span data-ttu-id="985bb-106">Dieses Attribut bestimmt den minimalen Zeitraum (in Stunden), für den das Ticket Erteilungs Ticket (TGT) eines Benutzers für die Kerberos-Authentifizierung verwendet werden kann, bevor eine Anforderung zum Erneuern des Tickets erteilt werden kann.</span><span class="sxs-lookup"><span data-stu-id="985bb-106">This attribute determines the minimum time period, in hours, that a user's ticket-granting ticket (TGT) can be used for Kerberos authentication before a request can be made to renew the ticket.</span></span>



| <span data-ttu-id="985bb-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="985bb-107">Entry</span></span> | <span data-ttu-id="985bb-108">Wert</span><span class="sxs-lookup"><span data-stu-id="985bb-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="985bb-109">CN</span><span class="sxs-lookup"><span data-stu-id="985bb-109">CN</span></span>                | <span data-ttu-id="985bb-110">Min. Ticket-Alter</span><span class="sxs-lookup"><span data-stu-id="985bb-110">Min-Ticket-Age</span></span>                       |
| <span data-ttu-id="985bb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="985bb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="985bb-112">minticketage</span><span class="sxs-lookup"><span data-stu-id="985bb-112">minTicketAge</span></span>                         |
| <span data-ttu-id="985bb-113">Size</span><span class="sxs-lookup"><span data-stu-id="985bb-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="985bb-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="985bb-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="985bb-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="985bb-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="985bb-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="985bb-116">Attribute-Id</span></span>      | <span data-ttu-id="985bb-117">1.2.840.113556.1.4.80</span><span class="sxs-lookup"><span data-stu-id="985bb-117">1.2.840.113556.1.4.80</span></span>                |
| <span data-ttu-id="985bb-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="985bb-118">System-Id-Guid</span></span>    | <span data-ttu-id="985bb-119">bf9679c4-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="985bb-119">bf9679c4-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="985bb-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="985bb-120">Syntax</span></span>            | [<span data-ttu-id="985bb-121">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="985bb-121">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="985bb-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="985bb-122">Implementations</span></span>

-   [<span data-ttu-id="985bb-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="985bb-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="985bb-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="985bb-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="985bb-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="985bb-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="985bb-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="985bb-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="985bb-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="985bb-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="985bb-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="985bb-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="985bb-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="985bb-129">Windows 2000 Server</span></span>



| <span data-ttu-id="985bb-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="985bb-130">Entry</span></span> | <span data-ttu-id="985bb-131">Wert</span><span class="sxs-lookup"><span data-stu-id="985bb-131">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="985bb-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="985bb-132">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="985bb-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="985bb-133">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="985bb-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="985bb-134">System-Only</span></span>            | <span data-ttu-id="985bb-135">False</span><span class="sxs-lookup"><span data-stu-id="985bb-135">False</span></span>                                              |
| <span data-ttu-id="985bb-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="985bb-136">Is-Single-Valued</span></span>       | <span data-ttu-id="985bb-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="985bb-137">True</span></span>                                               |
| <span data-ttu-id="985bb-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="985bb-138">Is Indexed</span></span>             | <span data-ttu-id="985bb-139">False</span><span class="sxs-lookup"><span data-stu-id="985bb-139">False</span></span>                                              |
| <span data-ttu-id="985bb-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="985bb-140">In Global Catalog</span></span>      | <span data-ttu-id="985bb-141">False</span><span class="sxs-lookup"><span data-stu-id="985bb-141">False</span></span>                                              |
| <span data-ttu-id="985bb-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="985bb-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="985bb-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="985bb-143">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="985bb-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="985bb-144">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="985bb-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="985bb-145">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="985bb-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="985bb-146">Search-Flags</span></span>           | <span data-ttu-id="985bb-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="985bb-147">0x00000000</span></span>                                         |
| <span data-ttu-id="985bb-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="985bb-148">System-Flags</span></span>           | <span data-ttu-id="985bb-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="985bb-149">0x00000010</span></span>                                         |
| <span data-ttu-id="985bb-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="985bb-150">Classes used in</span></span>        | [<span data-ttu-id="985bb-151">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="985bb-151">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="985bb-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="985bb-152">Windows Server 2003</span></span>



| <span data-ttu-id="985bb-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="985bb-153">Entry</span></span> | <span data-ttu-id="985bb-154">Wert</span><span class="sxs-lookup"><span data-stu-id="985bb-154">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="985bb-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="985bb-155">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="985bb-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="985bb-156">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="985bb-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="985bb-157">System-Only</span></span>            | <span data-ttu-id="985bb-158">False</span><span class="sxs-lookup"><span data-stu-id="985bb-158">False</span></span>                                              |
| <span data-ttu-id="985bb-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="985bb-159">Is-Single-Valued</span></span>       | <span data-ttu-id="985bb-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="985bb-160">True</span></span>                                               |
| <span data-ttu-id="985bb-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="985bb-161">Is Indexed</span></span>             | <span data-ttu-id="985bb-162">False</span><span class="sxs-lookup"><span data-stu-id="985bb-162">False</span></span>                                              |
| <span data-ttu-id="985bb-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="985bb-163">In Global Catalog</span></span>      | <span data-ttu-id="985bb-164">False</span><span class="sxs-lookup"><span data-stu-id="985bb-164">False</span></span>                                              |
| <span data-ttu-id="985bb-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="985bb-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="985bb-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="985bb-166">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="985bb-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="985bb-167">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="985bb-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="985bb-168">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="985bb-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="985bb-169">Search-Flags</span></span>           | <span data-ttu-id="985bb-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="985bb-170">0x00000000</span></span>                                         |
| <span data-ttu-id="985bb-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="985bb-171">System-Flags</span></span>           | <span data-ttu-id="985bb-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="985bb-172">0x00000010</span></span>                                         |
| <span data-ttu-id="985bb-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="985bb-173">Classes used in</span></span>        | [<span data-ttu-id="985bb-174">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="985bb-174">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="985bb-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="985bb-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="985bb-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="985bb-176">Entry</span></span> | <span data-ttu-id="985bb-177">Wert</span><span class="sxs-lookup"><span data-stu-id="985bb-177">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="985bb-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="985bb-178">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="985bb-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="985bb-179">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="985bb-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="985bb-180">System-Only</span></span>            | <span data-ttu-id="985bb-181">False</span><span class="sxs-lookup"><span data-stu-id="985bb-181">False</span></span>                                              |
| <span data-ttu-id="985bb-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="985bb-182">Is-Single-Valued</span></span>       | <span data-ttu-id="985bb-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="985bb-183">True</span></span>                                               |
| <span data-ttu-id="985bb-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="985bb-184">Is Indexed</span></span>             | <span data-ttu-id="985bb-185">False</span><span class="sxs-lookup"><span data-stu-id="985bb-185">False</span></span>                                              |
| <span data-ttu-id="985bb-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="985bb-186">In Global Catalog</span></span>      | <span data-ttu-id="985bb-187">False</span><span class="sxs-lookup"><span data-stu-id="985bb-187">False</span></span>                                              |
| <span data-ttu-id="985bb-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="985bb-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="985bb-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="985bb-189">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="985bb-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="985bb-190">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="985bb-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="985bb-191">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="985bb-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="985bb-192">Search-Flags</span></span>           | <span data-ttu-id="985bb-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="985bb-193">0x00000000</span></span>                                         |
| <span data-ttu-id="985bb-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="985bb-194">System-Flags</span></span>           | <span data-ttu-id="985bb-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="985bb-195">0x00000010</span></span>                                         |
| <span data-ttu-id="985bb-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="985bb-196">Classes used in</span></span>        | [<span data-ttu-id="985bb-197">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="985bb-197">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="985bb-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="985bb-198">Windows Server 2008</span></span>



| <span data-ttu-id="985bb-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="985bb-199">Entry</span></span> | <span data-ttu-id="985bb-200">Wert</span><span class="sxs-lookup"><span data-stu-id="985bb-200">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="985bb-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="985bb-201">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="985bb-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="985bb-202">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="985bb-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="985bb-203">System-Only</span></span>            | <span data-ttu-id="985bb-204">False</span><span class="sxs-lookup"><span data-stu-id="985bb-204">False</span></span>                                              |
| <span data-ttu-id="985bb-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="985bb-205">Is-Single-Valued</span></span>       | <span data-ttu-id="985bb-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="985bb-206">True</span></span>                                               |
| <span data-ttu-id="985bb-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="985bb-207">Is Indexed</span></span>             | <span data-ttu-id="985bb-208">False</span><span class="sxs-lookup"><span data-stu-id="985bb-208">False</span></span>                                              |
| <span data-ttu-id="985bb-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="985bb-209">In Global Catalog</span></span>      | <span data-ttu-id="985bb-210">False</span><span class="sxs-lookup"><span data-stu-id="985bb-210">False</span></span>                                              |
| <span data-ttu-id="985bb-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="985bb-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="985bb-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="985bb-212">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="985bb-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="985bb-213">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="985bb-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="985bb-214">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="985bb-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="985bb-215">Search-Flags</span></span>           | <span data-ttu-id="985bb-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="985bb-216">0x00000000</span></span>                                         |
| <span data-ttu-id="985bb-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="985bb-217">System-Flags</span></span>           | <span data-ttu-id="985bb-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="985bb-218">0x00000010</span></span>                                         |
| <span data-ttu-id="985bb-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="985bb-219">Classes used in</span></span>        | [<span data-ttu-id="985bb-220">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="985bb-220">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="985bb-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="985bb-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="985bb-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="985bb-222">Entry</span></span> | <span data-ttu-id="985bb-223">Wert</span><span class="sxs-lookup"><span data-stu-id="985bb-223">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="985bb-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="985bb-224">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="985bb-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="985bb-225">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="985bb-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="985bb-226">System-Only</span></span>            | <span data-ttu-id="985bb-227">False</span><span class="sxs-lookup"><span data-stu-id="985bb-227">False</span></span>                                              |
| <span data-ttu-id="985bb-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="985bb-228">Is-Single-Valued</span></span>       | <span data-ttu-id="985bb-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="985bb-229">True</span></span>                                               |
| <span data-ttu-id="985bb-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="985bb-230">Is Indexed</span></span>             | <span data-ttu-id="985bb-231">False</span><span class="sxs-lookup"><span data-stu-id="985bb-231">False</span></span>                                              |
| <span data-ttu-id="985bb-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="985bb-232">In Global Catalog</span></span>      | <span data-ttu-id="985bb-233">False</span><span class="sxs-lookup"><span data-stu-id="985bb-233">False</span></span>                                              |
| <span data-ttu-id="985bb-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="985bb-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="985bb-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="985bb-235">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="985bb-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="985bb-236">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="985bb-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="985bb-237">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="985bb-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="985bb-238">Search-Flags</span></span>           | <span data-ttu-id="985bb-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="985bb-239">0x00000000</span></span>                                         |
| <span data-ttu-id="985bb-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="985bb-240">System-Flags</span></span>           | <span data-ttu-id="985bb-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="985bb-241">0x00000010</span></span>                                         |
| <span data-ttu-id="985bb-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="985bb-242">Classes used in</span></span>        | [<span data-ttu-id="985bb-243">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="985bb-243">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="985bb-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="985bb-244">Windows Server 2012</span></span>



| <span data-ttu-id="985bb-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="985bb-245">Entry</span></span> | <span data-ttu-id="985bb-246">Wert</span><span class="sxs-lookup"><span data-stu-id="985bb-246">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="985bb-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="985bb-247">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="985bb-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="985bb-248">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="985bb-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="985bb-249">System-Only</span></span>            | <span data-ttu-id="985bb-250">False</span><span class="sxs-lookup"><span data-stu-id="985bb-250">False</span></span>                                              |
| <span data-ttu-id="985bb-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="985bb-251">Is-Single-Valued</span></span>       | <span data-ttu-id="985bb-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="985bb-252">True</span></span>                                               |
| <span data-ttu-id="985bb-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="985bb-253">Is Indexed</span></span>             | <span data-ttu-id="985bb-254">False</span><span class="sxs-lookup"><span data-stu-id="985bb-254">False</span></span>                                              |
| <span data-ttu-id="985bb-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="985bb-255">In Global Catalog</span></span>      | <span data-ttu-id="985bb-256">False</span><span class="sxs-lookup"><span data-stu-id="985bb-256">False</span></span>                                              |
| <span data-ttu-id="985bb-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="985bb-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="985bb-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="985bb-258">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="985bb-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="985bb-259">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="985bb-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="985bb-260">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="985bb-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="985bb-261">Search-Flags</span></span>           | <span data-ttu-id="985bb-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="985bb-262">0x00000000</span></span>                                         |
| <span data-ttu-id="985bb-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="985bb-263">System-Flags</span></span>           | <span data-ttu-id="985bb-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="985bb-264">0x00000010</span></span>                                         |
| <span data-ttu-id="985bb-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="985bb-265">Classes used in</span></span>        | [<span data-ttu-id="985bb-266">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="985bb-266">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





