---
title: Invocation-Id-Attribut
description: Dient zum eindeutigen Identifizieren der einzelnen Microsoft Exchange Server-Verzeichnisse in der Organisation.
ms.assetid: c069a57c-b9d0-49e9-8096-39b43f378573
ms.tgt_platform: multiple
keywords:
- AD-Schema für Invocation-Id-Attribut
- AD-Schema für invocationID-Attribut
topic_type:
- apiref
api_name:
- Invocation-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611589c466013ad46c0920a2da1e2250cf596214
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107030"
---
# <a name="invocation-id-attribute"></a><span data-ttu-id="ffe7f-105">Invocation-Id-Attribut</span><span class="sxs-lookup"><span data-stu-id="ffe7f-105">Invocation-Id attribute</span></span>

<span data-ttu-id="ffe7f-106">Dient zum eindeutigen Identifizieren der einzelnen Microsoft Exchange Server-Verzeichnisse in der Organisation.</span><span class="sxs-lookup"><span data-stu-id="ffe7f-106">Used to uniquely identify each Microsoft Exchange Server directory in the organization.</span></span>



| <span data-ttu-id="ffe7f-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ffe7f-107">Entry</span></span> | <span data-ttu-id="ffe7f-108">Wert</span><span class="sxs-lookup"><span data-stu-id="ffe7f-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="ffe7f-109">CN</span><span class="sxs-lookup"><span data-stu-id="ffe7f-109">CN</span></span>                | <span data-ttu-id="ffe7f-110">Invocation-Id</span><span class="sxs-lookup"><span data-stu-id="ffe7f-110">Invocation-Id</span></span>                                         |
| <span data-ttu-id="ffe7f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ffe7f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ffe7f-112">invocationId</span><span class="sxs-lookup"><span data-stu-id="ffe7f-112">invocationId</span></span>                                          |
| <span data-ttu-id="ffe7f-113">Size</span><span class="sxs-lookup"><span data-stu-id="ffe7f-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="ffe7f-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ffe7f-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="ffe7f-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="ffe7f-115">Update Frequency</span></span>  | <span data-ttu-id="ffe7f-116">Wenn der Exchange-Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ffe7f-116">When the Exchange Server is installed.</span></span>                |
| <span data-ttu-id="ffe7f-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ffe7f-117">Attribute-Id</span></span>      | <span data-ttu-id="ffe7f-118">1.2.840.113556.1.2.115</span><span class="sxs-lookup"><span data-stu-id="ffe7f-118">1.2.840.113556.1.2.115</span></span>                                |
| <span data-ttu-id="ffe7f-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ffe7f-119">System-Id-Guid</span></span>    | <span data-ttu-id="ffe7f-120">bf96798e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ffe7f-120">bf96798e-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="ffe7f-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffe7f-121">Syntax</span></span>            | [<span data-ttu-id="ffe7f-122">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="ffe7f-122">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="ffe7f-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ffe7f-123">Implementations</span></span>

-   [<span data-ttu-id="ffe7f-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ffe7f-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ffe7f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ffe7f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ffe7f-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="ffe7f-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ffe7f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ffe7f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ffe7f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ffe7f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ffe7f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ffe7f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ffe7f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ffe7f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ffe7f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ffe7f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ffe7f-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ffe7f-132">Entry</span></span> | <span data-ttu-id="ffe7f-133">Wert</span><span class="sxs-lookup"><span data-stu-id="ffe7f-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ffe7f-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ffe7f-134">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="ffe7f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffe7f-135">MAPI-Id</span></span>                | <span data-ttu-id="ffe7f-136">0x80bf</span><span class="sxs-lookup"><span data-stu-id="ffe7f-136">0x80BF</span></span>                                   |
| <span data-ttu-id="ffe7f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffe7f-137">System-Only</span></span>            | <span data-ttu-id="ffe7f-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-138">True</span></span>                                     |
| <span data-ttu-id="ffe7f-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ffe7f-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-140">True</span></span>                                     |
| <span data-ttu-id="ffe7f-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ffe7f-141">Is Indexed</span></span>             | <span data-ttu-id="ffe7f-142">False</span><span class="sxs-lookup"><span data-stu-id="ffe7f-142">False</span></span>                                    |
| <span data-ttu-id="ffe7f-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ffe7f-143">In Global Catalog</span></span>      | <span data-ttu-id="ffe7f-144">False</span><span class="sxs-lookup"><span data-stu-id="ffe7f-144">False</span></span>                                    |
| <span data-ttu-id="ffe7f-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ffe7f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffe7f-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ffe7f-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ffe7f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffe7f-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ffe7f-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffe7f-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ffe7f-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffe7f-149">Search-Flags</span></span>           | <span data-ttu-id="ffe7f-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffe7f-150">0x00000000</span></span>                               |
| <span data-ttu-id="ffe7f-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffe7f-151">System-Flags</span></span>           | <span data-ttu-id="ffe7f-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffe7f-152">0x00000010</span></span>                               |
| <span data-ttu-id="ffe7f-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ffe7f-153">Classes used in</span></span>        | [<span data-ttu-id="ffe7f-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ffe7f-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ffe7f-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ffe7f-155">Windows Server 2003</span></span>



| <span data-ttu-id="ffe7f-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ffe7f-156">Entry</span></span> | <span data-ttu-id="ffe7f-157">Wert</span><span class="sxs-lookup"><span data-stu-id="ffe7f-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ffe7f-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ffe7f-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="ffe7f-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffe7f-159">MAPI-Id</span></span>                | <span data-ttu-id="ffe7f-160">0x80bf</span><span class="sxs-lookup"><span data-stu-id="ffe7f-160">0x80BF</span></span>                                   |
| <span data-ttu-id="ffe7f-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffe7f-161">System-Only</span></span>            | <span data-ttu-id="ffe7f-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-162">True</span></span>                                     |
| <span data-ttu-id="ffe7f-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-163">Is-Single-Valued</span></span>       | <span data-ttu-id="ffe7f-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-164">True</span></span>                                     |
| <span data-ttu-id="ffe7f-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ffe7f-165">Is Indexed</span></span>             | <span data-ttu-id="ffe7f-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-166">True</span></span>                                     |
| <span data-ttu-id="ffe7f-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ffe7f-167">In Global Catalog</span></span>      | <span data-ttu-id="ffe7f-168">False</span><span class="sxs-lookup"><span data-stu-id="ffe7f-168">False</span></span>                                    |
| <span data-ttu-id="ffe7f-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ffe7f-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffe7f-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ffe7f-170">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ffe7f-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffe7f-171">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ffe7f-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffe7f-172">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ffe7f-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffe7f-173">Search-Flags</span></span>           | <span data-ttu-id="ffe7f-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ffe7f-174">0x00000001</span></span>                               |
| <span data-ttu-id="ffe7f-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffe7f-175">System-Flags</span></span>           | <span data-ttu-id="ffe7f-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffe7f-176">0x00000010</span></span>                               |
| <span data-ttu-id="ffe7f-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ffe7f-177">Classes used in</span></span>        | [<span data-ttu-id="ffe7f-178">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ffe7f-178">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ffe7f-179">Adam</span><span class="sxs-lookup"><span data-stu-id="ffe7f-179">ADAM</span></span>



| <span data-ttu-id="ffe7f-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ffe7f-180">Entry</span></span> | <span data-ttu-id="ffe7f-181">Wert</span><span class="sxs-lookup"><span data-stu-id="ffe7f-181">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ffe7f-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ffe7f-182">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="ffe7f-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffe7f-183">MAPI-Id</span></span>                | <span data-ttu-id="ffe7f-184">0x80bf</span><span class="sxs-lookup"><span data-stu-id="ffe7f-184">0x80BF</span></span>                                   |
| <span data-ttu-id="ffe7f-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffe7f-185">System-Only</span></span>            | <span data-ttu-id="ffe7f-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-186">True</span></span>                                     |
| <span data-ttu-id="ffe7f-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-187">Is-Single-Valued</span></span>       | <span data-ttu-id="ffe7f-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-188">True</span></span>                                     |
| <span data-ttu-id="ffe7f-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ffe7f-189">Is Indexed</span></span>             | <span data-ttu-id="ffe7f-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-190">True</span></span>                                     |
| <span data-ttu-id="ffe7f-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ffe7f-191">In Global Catalog</span></span>      | <span data-ttu-id="ffe7f-192">False</span><span class="sxs-lookup"><span data-stu-id="ffe7f-192">False</span></span>                                    |
| <span data-ttu-id="ffe7f-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ffe7f-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffe7f-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ffe7f-194">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ffe7f-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffe7f-195">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ffe7f-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffe7f-196">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ffe7f-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffe7f-197">Search-Flags</span></span>           | <span data-ttu-id="ffe7f-198">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ffe7f-198">0x00000001</span></span>                               |
| <span data-ttu-id="ffe7f-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffe7f-199">System-Flags</span></span>           | <span data-ttu-id="ffe7f-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffe7f-200">0x00000010</span></span>                               |
| <span data-ttu-id="ffe7f-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ffe7f-201">Classes used in</span></span>        | [<span data-ttu-id="ffe7f-202">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ffe7f-202">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ffe7f-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ffe7f-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ffe7f-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ffe7f-204">Entry</span></span> | <span data-ttu-id="ffe7f-205">Wert</span><span class="sxs-lookup"><span data-stu-id="ffe7f-205">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ffe7f-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ffe7f-206">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="ffe7f-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffe7f-207">MAPI-Id</span></span>                | <span data-ttu-id="ffe7f-208">0x80bf</span><span class="sxs-lookup"><span data-stu-id="ffe7f-208">0x80BF</span></span>                                   |
| <span data-ttu-id="ffe7f-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffe7f-209">System-Only</span></span>            | <span data-ttu-id="ffe7f-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-210">True</span></span>                                     |
| <span data-ttu-id="ffe7f-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-211">Is-Single-Valued</span></span>       | <span data-ttu-id="ffe7f-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-212">True</span></span>                                     |
| <span data-ttu-id="ffe7f-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ffe7f-213">Is Indexed</span></span>             | <span data-ttu-id="ffe7f-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-214">True</span></span>                                     |
| <span data-ttu-id="ffe7f-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ffe7f-215">In Global Catalog</span></span>      | <span data-ttu-id="ffe7f-216">False</span><span class="sxs-lookup"><span data-stu-id="ffe7f-216">False</span></span>                                    |
| <span data-ttu-id="ffe7f-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ffe7f-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffe7f-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ffe7f-218">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ffe7f-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffe7f-219">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ffe7f-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffe7f-220">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ffe7f-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffe7f-221">Search-Flags</span></span>           | <span data-ttu-id="ffe7f-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ffe7f-222">0x00000001</span></span>                               |
| <span data-ttu-id="ffe7f-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffe7f-223">System-Flags</span></span>           | <span data-ttu-id="ffe7f-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffe7f-224">0x00000010</span></span>                               |
| <span data-ttu-id="ffe7f-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ffe7f-225">Classes used in</span></span>        | [<span data-ttu-id="ffe7f-226">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ffe7f-226">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ffe7f-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffe7f-227">Windows Server 2008</span></span>



| <span data-ttu-id="ffe7f-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ffe7f-228">Entry</span></span> | <span data-ttu-id="ffe7f-229">Wert</span><span class="sxs-lookup"><span data-stu-id="ffe7f-229">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ffe7f-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ffe7f-230">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="ffe7f-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffe7f-231">MAPI-Id</span></span>                | <span data-ttu-id="ffe7f-232">0x80bf</span><span class="sxs-lookup"><span data-stu-id="ffe7f-232">0x80BF</span></span>                                   |
| <span data-ttu-id="ffe7f-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffe7f-233">System-Only</span></span>            | <span data-ttu-id="ffe7f-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-234">True</span></span>                                     |
| <span data-ttu-id="ffe7f-235">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-235">Is-Single-Valued</span></span>       | <span data-ttu-id="ffe7f-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-236">True</span></span>                                     |
| <span data-ttu-id="ffe7f-237">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ffe7f-237">Is Indexed</span></span>             | <span data-ttu-id="ffe7f-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-238">True</span></span>                                     |
| <span data-ttu-id="ffe7f-239">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ffe7f-239">In Global Catalog</span></span>      | <span data-ttu-id="ffe7f-240">False</span><span class="sxs-lookup"><span data-stu-id="ffe7f-240">False</span></span>                                    |
| <span data-ttu-id="ffe7f-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ffe7f-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffe7f-242">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ffe7f-242">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ffe7f-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffe7f-243">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ffe7f-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffe7f-244">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ffe7f-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffe7f-245">Search-Flags</span></span>           | <span data-ttu-id="ffe7f-246">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ffe7f-246">0x00000001</span></span>                               |
| <span data-ttu-id="ffe7f-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffe7f-247">System-Flags</span></span>           | <span data-ttu-id="ffe7f-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffe7f-248">0x00000010</span></span>                               |
| <span data-ttu-id="ffe7f-249">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ffe7f-249">Classes used in</span></span>        | [<span data-ttu-id="ffe7f-250">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ffe7f-250">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ffe7f-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ffe7f-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ffe7f-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ffe7f-252">Entry</span></span> | <span data-ttu-id="ffe7f-253">Wert</span><span class="sxs-lookup"><span data-stu-id="ffe7f-253">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ffe7f-254">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ffe7f-254">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="ffe7f-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffe7f-255">MAPI-Id</span></span>                | <span data-ttu-id="ffe7f-256">0x80bf</span><span class="sxs-lookup"><span data-stu-id="ffe7f-256">0x80BF</span></span>                                   |
| <span data-ttu-id="ffe7f-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffe7f-257">System-Only</span></span>            | <span data-ttu-id="ffe7f-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-258">True</span></span>                                     |
| <span data-ttu-id="ffe7f-259">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-259">Is-Single-Valued</span></span>       | <span data-ttu-id="ffe7f-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-260">True</span></span>                                     |
| <span data-ttu-id="ffe7f-261">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ffe7f-261">Is Indexed</span></span>             | <span data-ttu-id="ffe7f-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-262">True</span></span>                                     |
| <span data-ttu-id="ffe7f-263">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ffe7f-263">In Global Catalog</span></span>      | <span data-ttu-id="ffe7f-264">False</span><span class="sxs-lookup"><span data-stu-id="ffe7f-264">False</span></span>                                    |
| <span data-ttu-id="ffe7f-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ffe7f-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffe7f-266">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ffe7f-266">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ffe7f-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffe7f-267">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ffe7f-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffe7f-268">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ffe7f-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffe7f-269">Search-Flags</span></span>           | <span data-ttu-id="ffe7f-270">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ffe7f-270">0x00000001</span></span>                               |
| <span data-ttu-id="ffe7f-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffe7f-271">System-Flags</span></span>           | <span data-ttu-id="ffe7f-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffe7f-272">0x00000010</span></span>                               |
| <span data-ttu-id="ffe7f-273">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ffe7f-273">Classes used in</span></span>        | [<span data-ttu-id="ffe7f-274">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ffe7f-274">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ffe7f-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ffe7f-275">Windows Server 2012</span></span>



| <span data-ttu-id="ffe7f-276">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ffe7f-276">Entry</span></span> | <span data-ttu-id="ffe7f-277">Wert</span><span class="sxs-lookup"><span data-stu-id="ffe7f-277">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="ffe7f-278">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ffe7f-278">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="ffe7f-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffe7f-279">MAPI-Id</span></span>                | <span data-ttu-id="ffe7f-280">0x80bf</span><span class="sxs-lookup"><span data-stu-id="ffe7f-280">0x80BF</span></span>                                   |
| <span data-ttu-id="ffe7f-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffe7f-281">System-Only</span></span>            | <span data-ttu-id="ffe7f-282">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-282">True</span></span>                                     |
| <span data-ttu-id="ffe7f-283">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-283">Is-Single-Valued</span></span>       | <span data-ttu-id="ffe7f-284">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-284">True</span></span>                                     |
| <span data-ttu-id="ffe7f-285">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ffe7f-285">Is Indexed</span></span>             | <span data-ttu-id="ffe7f-286">Richtig</span><span class="sxs-lookup"><span data-stu-id="ffe7f-286">True</span></span>                                     |
| <span data-ttu-id="ffe7f-287">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ffe7f-287">In Global Catalog</span></span>      | <span data-ttu-id="ffe7f-288">False</span><span class="sxs-lookup"><span data-stu-id="ffe7f-288">False</span></span>                                    |
| <span data-ttu-id="ffe7f-289">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ffe7f-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffe7f-290">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ffe7f-290">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="ffe7f-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffe7f-291">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="ffe7f-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffe7f-292">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="ffe7f-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffe7f-293">Search-Flags</span></span>           | <span data-ttu-id="ffe7f-294">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ffe7f-294">0x00000001</span></span>                               |
| <span data-ttu-id="ffe7f-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffe7f-295">System-Flags</span></span>           | <span data-ttu-id="ffe7f-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffe7f-296">0x00000010</span></span>                               |
| <span data-ttu-id="ffe7f-297">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ffe7f-297">Classes used in</span></span>        | [<span data-ttu-id="ffe7f-298">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="ffe7f-298">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





