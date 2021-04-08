---
title: Max-Ticket-Age-Attribut
description: Dieses Attribut bestimmt den maximalen Zeitraum (in Stunden), den das Ticket Erteilungs Ticket (TGT) eines Benutzers für die Kerberos-Authentifizierung verwendet werden kann.
ms.assetid: 54ab0f2b-31eb-45d7-9a43-e70dc78136b5
ms.tgt_platform: multiple
keywords:
- "\"Max-Ticket-Age\"-Attribut AD-Schema"
- Schema des maxticketage-Attributs AD
topic_type:
- apiref
api_name:
- Max-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d68bca2f8dd87d37be7215e26f549424cd32b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744345"
---
# <a name="max-ticket-age-attribute"></a><span data-ttu-id="48d90-105">Max-Ticket-Age-Attribut</span><span class="sxs-lookup"><span data-stu-id="48d90-105">Max-Ticket-Age attribute</span></span>

<span data-ttu-id="48d90-106">Dieses Attribut bestimmt den maximalen Zeitraum (in Stunden), den das Ticket Erteilungs Ticket (TGT) eines Benutzers für die Kerberos-Authentifizierung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="48d90-106">This attribute determines the maximum amount of time, in hours, that a user's ticket-granting ticket (TGT) can be used for the purpose of Kerberos authentication.</span></span> <span data-ttu-id="48d90-107">Wenn das TGT eines Benutzers abläuft, muss ein neues angefordert werden, oder das vorhandene muss erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="48d90-107">When a user's TGT expires, a new one must be requested, or the existing one must be renewed.</span></span> <span data-ttu-id="48d90-108">Standardmäßig ist diese Einstellung im Standard-Domänen Gruppenrichtlinie Objekt (GPO) auf 10 Stunden festgelegt.</span><span class="sxs-lookup"><span data-stu-id="48d90-108">By default, this setting is set to 10 hours in the Default Domain Group Policy object (GPO).</span></span>



| <span data-ttu-id="48d90-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="48d90-109">Entry</span></span> | <span data-ttu-id="48d90-110">Wert</span><span class="sxs-lookup"><span data-stu-id="48d90-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="48d90-111">CN</span><span class="sxs-lookup"><span data-stu-id="48d90-111">CN</span></span>                | <span data-ttu-id="48d90-112">Max-Ticket-Age</span><span class="sxs-lookup"><span data-stu-id="48d90-112">Max-Ticket-Age</span></span>                       |
| <span data-ttu-id="48d90-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="48d90-113">Ldap-Display-Name</span></span> | <span data-ttu-id="48d90-114">maxticketage</span><span class="sxs-lookup"><span data-stu-id="48d90-114">maxTicketAge</span></span>                         |
| <span data-ttu-id="48d90-115">Size</span><span class="sxs-lookup"><span data-stu-id="48d90-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="48d90-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="48d90-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="48d90-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="48d90-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="48d90-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="48d90-118">Attribute-Id</span></span>      | <span data-ttu-id="48d90-119">1.2.840.113556.1.4.77</span><span class="sxs-lookup"><span data-stu-id="48d90-119">1.2.840.113556.1.4.77</span></span>                |
| <span data-ttu-id="48d90-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="48d90-120">System-Id-Guid</span></span>    | <span data-ttu-id="48d90-121">bf9679be-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="48d90-121">bf9679be-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="48d90-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="48d90-122">Syntax</span></span>            | [<span data-ttu-id="48d90-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="48d90-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="48d90-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="48d90-124">Implementations</span></span>

-   [<span data-ttu-id="48d90-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="48d90-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="48d90-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="48d90-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="48d90-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="48d90-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="48d90-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="48d90-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="48d90-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="48d90-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="48d90-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="48d90-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="48d90-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="48d90-131">Windows 2000 Server</span></span>



| <span data-ttu-id="48d90-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="48d90-132">Entry</span></span> | <span data-ttu-id="48d90-133">Wert</span><span class="sxs-lookup"><span data-stu-id="48d90-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="48d90-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="48d90-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="48d90-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48d90-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="48d90-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="48d90-136">System-Only</span></span>            | <span data-ttu-id="48d90-137">False</span><span class="sxs-lookup"><span data-stu-id="48d90-137">False</span></span>                                              |
| <span data-ttu-id="48d90-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="48d90-138">Is-Single-Valued</span></span>       | <span data-ttu-id="48d90-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="48d90-139">True</span></span>                                               |
| <span data-ttu-id="48d90-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="48d90-140">Is Indexed</span></span>             | <span data-ttu-id="48d90-141">False</span><span class="sxs-lookup"><span data-stu-id="48d90-141">False</span></span>                                              |
| <span data-ttu-id="48d90-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="48d90-142">In Global Catalog</span></span>      | <span data-ttu-id="48d90-143">False</span><span class="sxs-lookup"><span data-stu-id="48d90-143">False</span></span>                                              |
| <span data-ttu-id="48d90-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48d90-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="48d90-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="48d90-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="48d90-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48d90-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="48d90-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48d90-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="48d90-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48d90-148">Search-Flags</span></span>           | <span data-ttu-id="48d90-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48d90-149">0x00000000</span></span>                                         |
| <span data-ttu-id="48d90-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48d90-150">System-Flags</span></span>           | <span data-ttu-id="48d90-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48d90-151">0x00000010</span></span>                                         |
| <span data-ttu-id="48d90-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="48d90-152">Classes used in</span></span>        | [<span data-ttu-id="48d90-153">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="48d90-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="48d90-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="48d90-154">Windows Server 2003</span></span>



| <span data-ttu-id="48d90-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="48d90-155">Entry</span></span> | <span data-ttu-id="48d90-156">Wert</span><span class="sxs-lookup"><span data-stu-id="48d90-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="48d90-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="48d90-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="48d90-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48d90-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="48d90-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="48d90-159">System-Only</span></span>            | <span data-ttu-id="48d90-160">False</span><span class="sxs-lookup"><span data-stu-id="48d90-160">False</span></span>                                              |
| <span data-ttu-id="48d90-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="48d90-161">Is-Single-Valued</span></span>       | <span data-ttu-id="48d90-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="48d90-162">True</span></span>                                               |
| <span data-ttu-id="48d90-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="48d90-163">Is Indexed</span></span>             | <span data-ttu-id="48d90-164">False</span><span class="sxs-lookup"><span data-stu-id="48d90-164">False</span></span>                                              |
| <span data-ttu-id="48d90-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="48d90-165">In Global Catalog</span></span>      | <span data-ttu-id="48d90-166">False</span><span class="sxs-lookup"><span data-stu-id="48d90-166">False</span></span>                                              |
| <span data-ttu-id="48d90-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48d90-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="48d90-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="48d90-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="48d90-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48d90-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="48d90-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48d90-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="48d90-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48d90-171">Search-Flags</span></span>           | <span data-ttu-id="48d90-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48d90-172">0x00000000</span></span>                                         |
| <span data-ttu-id="48d90-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48d90-173">System-Flags</span></span>           | <span data-ttu-id="48d90-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48d90-174">0x00000010</span></span>                                         |
| <span data-ttu-id="48d90-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="48d90-175">Classes used in</span></span>        | [<span data-ttu-id="48d90-176">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="48d90-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="48d90-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="48d90-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="48d90-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="48d90-178">Entry</span></span> | <span data-ttu-id="48d90-179">Wert</span><span class="sxs-lookup"><span data-stu-id="48d90-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="48d90-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="48d90-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="48d90-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48d90-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="48d90-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="48d90-182">System-Only</span></span>            | <span data-ttu-id="48d90-183">False</span><span class="sxs-lookup"><span data-stu-id="48d90-183">False</span></span>                                              |
| <span data-ttu-id="48d90-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="48d90-184">Is-Single-Valued</span></span>       | <span data-ttu-id="48d90-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="48d90-185">True</span></span>                                               |
| <span data-ttu-id="48d90-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="48d90-186">Is Indexed</span></span>             | <span data-ttu-id="48d90-187">False</span><span class="sxs-lookup"><span data-stu-id="48d90-187">False</span></span>                                              |
| <span data-ttu-id="48d90-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="48d90-188">In Global Catalog</span></span>      | <span data-ttu-id="48d90-189">False</span><span class="sxs-lookup"><span data-stu-id="48d90-189">False</span></span>                                              |
| <span data-ttu-id="48d90-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48d90-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="48d90-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="48d90-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="48d90-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48d90-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="48d90-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48d90-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="48d90-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48d90-194">Search-Flags</span></span>           | <span data-ttu-id="48d90-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48d90-195">0x00000000</span></span>                                         |
| <span data-ttu-id="48d90-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48d90-196">System-Flags</span></span>           | <span data-ttu-id="48d90-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48d90-197">0x00000010</span></span>                                         |
| <span data-ttu-id="48d90-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="48d90-198">Classes used in</span></span>        | [<span data-ttu-id="48d90-199">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="48d90-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="48d90-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48d90-200">Windows Server 2008</span></span>



| <span data-ttu-id="48d90-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="48d90-201">Entry</span></span> | <span data-ttu-id="48d90-202">Wert</span><span class="sxs-lookup"><span data-stu-id="48d90-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="48d90-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="48d90-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="48d90-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48d90-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="48d90-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="48d90-205">System-Only</span></span>            | <span data-ttu-id="48d90-206">False</span><span class="sxs-lookup"><span data-stu-id="48d90-206">False</span></span>                                              |
| <span data-ttu-id="48d90-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="48d90-207">Is-Single-Valued</span></span>       | <span data-ttu-id="48d90-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="48d90-208">True</span></span>                                               |
| <span data-ttu-id="48d90-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="48d90-209">Is Indexed</span></span>             | <span data-ttu-id="48d90-210">False</span><span class="sxs-lookup"><span data-stu-id="48d90-210">False</span></span>                                              |
| <span data-ttu-id="48d90-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="48d90-211">In Global Catalog</span></span>      | <span data-ttu-id="48d90-212">False</span><span class="sxs-lookup"><span data-stu-id="48d90-212">False</span></span>                                              |
| <span data-ttu-id="48d90-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48d90-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="48d90-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="48d90-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="48d90-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48d90-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="48d90-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48d90-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="48d90-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48d90-217">Search-Flags</span></span>           | <span data-ttu-id="48d90-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48d90-218">0x00000000</span></span>                                         |
| <span data-ttu-id="48d90-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48d90-219">System-Flags</span></span>           | <span data-ttu-id="48d90-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48d90-220">0x00000010</span></span>                                         |
| <span data-ttu-id="48d90-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="48d90-221">Classes used in</span></span>        | [<span data-ttu-id="48d90-222">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="48d90-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="48d90-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="48d90-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="48d90-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="48d90-224">Entry</span></span> | <span data-ttu-id="48d90-225">Wert</span><span class="sxs-lookup"><span data-stu-id="48d90-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="48d90-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="48d90-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="48d90-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48d90-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="48d90-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="48d90-228">System-Only</span></span>            | <span data-ttu-id="48d90-229">False</span><span class="sxs-lookup"><span data-stu-id="48d90-229">False</span></span>                                              |
| <span data-ttu-id="48d90-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="48d90-230">Is-Single-Valued</span></span>       | <span data-ttu-id="48d90-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="48d90-231">True</span></span>                                               |
| <span data-ttu-id="48d90-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="48d90-232">Is Indexed</span></span>             | <span data-ttu-id="48d90-233">False</span><span class="sxs-lookup"><span data-stu-id="48d90-233">False</span></span>                                              |
| <span data-ttu-id="48d90-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="48d90-234">In Global Catalog</span></span>      | <span data-ttu-id="48d90-235">False</span><span class="sxs-lookup"><span data-stu-id="48d90-235">False</span></span>                                              |
| <span data-ttu-id="48d90-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48d90-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="48d90-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="48d90-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="48d90-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48d90-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="48d90-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48d90-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="48d90-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48d90-240">Search-Flags</span></span>           | <span data-ttu-id="48d90-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48d90-241">0x00000000</span></span>                                         |
| <span data-ttu-id="48d90-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48d90-242">System-Flags</span></span>           | <span data-ttu-id="48d90-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48d90-243">0x00000010</span></span>                                         |
| <span data-ttu-id="48d90-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="48d90-244">Classes used in</span></span>        | [<span data-ttu-id="48d90-245">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="48d90-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="48d90-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="48d90-246">Windows Server 2012</span></span>



| <span data-ttu-id="48d90-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="48d90-247">Entry</span></span> | <span data-ttu-id="48d90-248">Wert</span><span class="sxs-lookup"><span data-stu-id="48d90-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="48d90-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="48d90-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="48d90-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48d90-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="48d90-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="48d90-251">System-Only</span></span>            | <span data-ttu-id="48d90-252">False</span><span class="sxs-lookup"><span data-stu-id="48d90-252">False</span></span>                                              |
| <span data-ttu-id="48d90-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="48d90-253">Is-Single-Valued</span></span>       | <span data-ttu-id="48d90-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="48d90-254">True</span></span>                                               |
| <span data-ttu-id="48d90-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="48d90-255">Is Indexed</span></span>             | <span data-ttu-id="48d90-256">False</span><span class="sxs-lookup"><span data-stu-id="48d90-256">False</span></span>                                              |
| <span data-ttu-id="48d90-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="48d90-257">In Global Catalog</span></span>      | <span data-ttu-id="48d90-258">False</span><span class="sxs-lookup"><span data-stu-id="48d90-258">False</span></span>                                              |
| <span data-ttu-id="48d90-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48d90-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="48d90-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="48d90-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="48d90-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48d90-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="48d90-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48d90-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="48d90-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48d90-263">Search-Flags</span></span>           | <span data-ttu-id="48d90-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48d90-264">0x00000000</span></span>                                         |
| <span data-ttu-id="48d90-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48d90-265">System-Flags</span></span>           | <span data-ttu-id="48d90-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48d90-266">0x00000010</span></span>                                         |
| <span data-ttu-id="48d90-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="48d90-267">Classes used in</span></span>        | [<span data-ttu-id="48d90-268">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="48d90-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





