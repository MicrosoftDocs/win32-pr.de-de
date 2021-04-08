---
title: Trust-Attributes-Attribut
description: Dieses Attribut speichert die Vertrauens Attribute für eine vertrauenswürdige Domäne.
ms.assetid: c85b98a6-4d09-4eb2-821b-58ef558b3460
ms.tgt_platform: multiple
keywords:
- AD-Schema für Trust-Attributes-Attribut
- trustatutributes-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Trust-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81dc06f73fbda5dab7ce8d2a07bfc90323d2b29
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744881"
---
# <a name="trust-attributes-attribute"></a><span data-ttu-id="f8070-105">Trust-Attributes-Attribut</span><span class="sxs-lookup"><span data-stu-id="f8070-105">Trust-Attributes attribute</span></span>

<span data-ttu-id="f8070-106">Dieses Attribut speichert die Vertrauens Attribute für eine vertrauenswürdige Domäne.</span><span class="sxs-lookup"><span data-stu-id="f8070-106">This attribute stores the trust attributes for a trusted domain.</span></span> <span data-ttu-id="f8070-107">Folgende Attributwerte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="f8070-107">Possible attribute values are as follows:</span></span>

-   <span data-ttu-id="f8070-108">\_ \_ Nicht \_ transitives Vertrauens Attribut deaktivieren Transitivität.</span><span class="sxs-lookup"><span data-stu-id="f8070-108">TRUST\_ATTRIBUTE\_NON\_TRANSITIVE Disable transitivity.</span></span>
-   <span data-ttu-id="f8070-109">\_ \_ \_ Die übergeordnete Vertrauensstellung der Trust-Attribut Struktur ist auf das übergeordnete Element der Organisationsstruktur</span><span class="sxs-lookup"><span data-stu-id="f8070-109">TRUST\_ATTRIBUTE\_TREE\_PARENT Trust is set to the organization tree parent.</span></span>
-   <span data-ttu-id="f8070-110">Vertrauensstellung des vertrauenswürdigen \_ Attribut \_ Baums \_ auf einen anderen Struktur Stamm in der Gesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="f8070-110">TRUST\_ATTRIBUTE\_TREE\_ROOT Trust set to another tree root in the forest.</span></span>
-   <span data-ttu-id="f8070-111">Vertrauens \_ Attribut \_ komplexer Darstellung \_ nur vertrauenswürdiger Link ist nur für den komplexer Darstellung-Client gültig.</span><span class="sxs-lookup"><span data-stu-id="f8070-111">TRUST\_ATTRIBUTE\_UPLEVEL\_ONLY Trusted link valid only for uplevel client.</span></span>



| <span data-ttu-id="f8070-112">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f8070-112">Entry</span></span> | <span data-ttu-id="f8070-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f8070-113">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f8070-114">CN</span><span class="sxs-lookup"><span data-stu-id="f8070-114">CN</span></span>                | <span data-ttu-id="f8070-115">Trust-Attributes</span><span class="sxs-lookup"><span data-stu-id="f8070-115">Trust-Attributes</span></span>                     |
| <span data-ttu-id="f8070-116">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f8070-116">Ldap-Display-Name</span></span> | <span data-ttu-id="f8070-117">trustatus Tributes</span><span class="sxs-lookup"><span data-stu-id="f8070-117">trustAttributes</span></span>                      |
| <span data-ttu-id="f8070-118">Size</span><span class="sxs-lookup"><span data-stu-id="f8070-118">Size</span></span>              | \-                                   |
| <span data-ttu-id="f8070-119">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f8070-119">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f8070-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f8070-120">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f8070-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f8070-121">Attribute-Id</span></span>      | <span data-ttu-id="f8070-122">1.2.840.113556.1.4.470</span><span class="sxs-lookup"><span data-stu-id="f8070-122">1.2.840.113556.1.4.470</span></span>               |
| <span data-ttu-id="f8070-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f8070-123">System-Id-Guid</span></span>    | <span data-ttu-id="f8070-124">80a67e5a-9F 22-11D0-AFDD-00c04f-930c9</span><span class="sxs-lookup"><span data-stu-id="f8070-124">80a67e5a-9f22-11d0-afdd-00c04fd930c9</span></span> |
| <span data-ttu-id="f8070-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8070-125">Syntax</span></span>            | [<span data-ttu-id="f8070-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="f8070-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="f8070-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f8070-127">Implementations</span></span>

-   [<span data-ttu-id="f8070-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f8070-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f8070-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f8070-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f8070-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f8070-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f8070-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f8070-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f8070-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f8070-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f8070-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f8070-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f8070-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f8070-134">Windows 2000 Server</span></span>



| <span data-ttu-id="f8070-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f8070-135">Entry</span></span> | <span data-ttu-id="f8070-136">Wert</span><span class="sxs-lookup"><span data-stu-id="f8070-136">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f8070-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f8070-137">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f8070-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8070-138">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f8070-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8070-139">System-Only</span></span>            | <span data-ttu-id="f8070-140">False</span><span class="sxs-lookup"><span data-stu-id="f8070-140">False</span></span>                                                |
| <span data-ttu-id="f8070-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f8070-141">Is-Single-Valued</span></span>       | <span data-ttu-id="f8070-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="f8070-142">True</span></span>                                                 |
| <span data-ttu-id="f8070-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f8070-143">Is Indexed</span></span>             | <span data-ttu-id="f8070-144">False</span><span class="sxs-lookup"><span data-stu-id="f8070-144">False</span></span>                                                |
| <span data-ttu-id="f8070-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f8070-145">In Global Catalog</span></span>      | <span data-ttu-id="f8070-146">False</span><span class="sxs-lookup"><span data-stu-id="f8070-146">False</span></span>                                                |
| <span data-ttu-id="f8070-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8070-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8070-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f8070-148">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f8070-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8070-149">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f8070-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8070-150">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f8070-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8070-151">Search-Flags</span></span>           | <span data-ttu-id="f8070-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8070-152">0x00000000</span></span>                                           |
| <span data-ttu-id="f8070-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8070-153">System-Flags</span></span>           | <span data-ttu-id="f8070-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8070-154">0x00000010</span></span>                                           |
| <span data-ttu-id="f8070-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f8070-155">Classes used in</span></span>        | [<span data-ttu-id="f8070-156">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="f8070-156">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f8070-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f8070-157">Windows Server 2003</span></span>



| <span data-ttu-id="f8070-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f8070-158">Entry</span></span> | <span data-ttu-id="f8070-159">Wert</span><span class="sxs-lookup"><span data-stu-id="f8070-159">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f8070-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f8070-160">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f8070-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8070-161">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f8070-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8070-162">System-Only</span></span>            | <span data-ttu-id="f8070-163">False</span><span class="sxs-lookup"><span data-stu-id="f8070-163">False</span></span>                                                |
| <span data-ttu-id="f8070-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f8070-164">Is-Single-Valued</span></span>       | <span data-ttu-id="f8070-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="f8070-165">True</span></span>                                                 |
| <span data-ttu-id="f8070-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f8070-166">Is Indexed</span></span>             | <span data-ttu-id="f8070-167">False</span><span class="sxs-lookup"><span data-stu-id="f8070-167">False</span></span>                                                |
| <span data-ttu-id="f8070-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f8070-168">In Global Catalog</span></span>      | <span data-ttu-id="f8070-169">Richtig</span><span class="sxs-lookup"><span data-stu-id="f8070-169">True</span></span>                                                 |
| <span data-ttu-id="f8070-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8070-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8070-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f8070-171">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f8070-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8070-172">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f8070-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8070-173">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f8070-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8070-174">Search-Flags</span></span>           | <span data-ttu-id="f8070-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8070-175">0x00000000</span></span>                                           |
| <span data-ttu-id="f8070-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8070-176">System-Flags</span></span>           | <span data-ttu-id="f8070-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8070-177">0x00000010</span></span>                                           |
| <span data-ttu-id="f8070-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f8070-178">Classes used in</span></span>        | [<span data-ttu-id="f8070-179">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="f8070-179">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f8070-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f8070-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f8070-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f8070-181">Entry</span></span> | <span data-ttu-id="f8070-182">Wert</span><span class="sxs-lookup"><span data-stu-id="f8070-182">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f8070-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f8070-183">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f8070-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8070-184">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f8070-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8070-185">System-Only</span></span>            | <span data-ttu-id="f8070-186">False</span><span class="sxs-lookup"><span data-stu-id="f8070-186">False</span></span>                                                |
| <span data-ttu-id="f8070-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f8070-187">Is-Single-Valued</span></span>       | <span data-ttu-id="f8070-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="f8070-188">True</span></span>                                                 |
| <span data-ttu-id="f8070-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f8070-189">Is Indexed</span></span>             | <span data-ttu-id="f8070-190">False</span><span class="sxs-lookup"><span data-stu-id="f8070-190">False</span></span>                                                |
| <span data-ttu-id="f8070-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f8070-191">In Global Catalog</span></span>      | <span data-ttu-id="f8070-192">Richtig</span><span class="sxs-lookup"><span data-stu-id="f8070-192">True</span></span>                                                 |
| <span data-ttu-id="f8070-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8070-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8070-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f8070-194">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f8070-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8070-195">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f8070-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8070-196">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f8070-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8070-197">Search-Flags</span></span>           | <span data-ttu-id="f8070-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8070-198">0x00000000</span></span>                                           |
| <span data-ttu-id="f8070-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8070-199">System-Flags</span></span>           | <span data-ttu-id="f8070-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8070-200">0x00000010</span></span>                                           |
| <span data-ttu-id="f8070-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f8070-201">Classes used in</span></span>        | [<span data-ttu-id="f8070-202">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="f8070-202">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f8070-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8070-203">Windows Server 2008</span></span>



| <span data-ttu-id="f8070-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f8070-204">Entry</span></span> | <span data-ttu-id="f8070-205">Wert</span><span class="sxs-lookup"><span data-stu-id="f8070-205">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f8070-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f8070-206">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f8070-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8070-207">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f8070-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8070-208">System-Only</span></span>            | <span data-ttu-id="f8070-209">False</span><span class="sxs-lookup"><span data-stu-id="f8070-209">False</span></span>                                                |
| <span data-ttu-id="f8070-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f8070-210">Is-Single-Valued</span></span>       | <span data-ttu-id="f8070-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="f8070-211">True</span></span>                                                 |
| <span data-ttu-id="f8070-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f8070-212">Is Indexed</span></span>             | <span data-ttu-id="f8070-213">False</span><span class="sxs-lookup"><span data-stu-id="f8070-213">False</span></span>                                                |
| <span data-ttu-id="f8070-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f8070-214">In Global Catalog</span></span>      | <span data-ttu-id="f8070-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="f8070-215">True</span></span>                                                 |
| <span data-ttu-id="f8070-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8070-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8070-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f8070-217">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f8070-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8070-218">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f8070-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8070-219">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f8070-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8070-220">Search-Flags</span></span>           | <span data-ttu-id="f8070-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8070-221">0x00000000</span></span>                                           |
| <span data-ttu-id="f8070-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8070-222">System-Flags</span></span>           | <span data-ttu-id="f8070-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8070-223">0x00000010</span></span>                                           |
| <span data-ttu-id="f8070-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f8070-224">Classes used in</span></span>        | [<span data-ttu-id="f8070-225">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="f8070-225">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f8070-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f8070-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f8070-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f8070-227">Entry</span></span> | <span data-ttu-id="f8070-228">Wert</span><span class="sxs-lookup"><span data-stu-id="f8070-228">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f8070-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f8070-229">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f8070-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8070-230">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f8070-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8070-231">System-Only</span></span>            | <span data-ttu-id="f8070-232">False</span><span class="sxs-lookup"><span data-stu-id="f8070-232">False</span></span>                                                |
| <span data-ttu-id="f8070-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f8070-233">Is-Single-Valued</span></span>       | <span data-ttu-id="f8070-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="f8070-234">True</span></span>                                                 |
| <span data-ttu-id="f8070-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f8070-235">Is Indexed</span></span>             | <span data-ttu-id="f8070-236">False</span><span class="sxs-lookup"><span data-stu-id="f8070-236">False</span></span>                                                |
| <span data-ttu-id="f8070-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f8070-237">In Global Catalog</span></span>      | <span data-ttu-id="f8070-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="f8070-238">True</span></span>                                                 |
| <span data-ttu-id="f8070-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8070-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8070-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f8070-240">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f8070-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8070-241">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f8070-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8070-242">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f8070-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8070-243">Search-Flags</span></span>           | <span data-ttu-id="f8070-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8070-244">0x00000000</span></span>                                           |
| <span data-ttu-id="f8070-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8070-245">System-Flags</span></span>           | <span data-ttu-id="f8070-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8070-246">0x00000010</span></span>                                           |
| <span data-ttu-id="f8070-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f8070-247">Classes used in</span></span>        | [<span data-ttu-id="f8070-248">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="f8070-248">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f8070-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f8070-249">Windows Server 2012</span></span>



| <span data-ttu-id="f8070-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f8070-250">Entry</span></span> | <span data-ttu-id="f8070-251">Wert</span><span class="sxs-lookup"><span data-stu-id="f8070-251">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f8070-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f8070-252">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f8070-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8070-253">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f8070-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8070-254">System-Only</span></span>            | <span data-ttu-id="f8070-255">False</span><span class="sxs-lookup"><span data-stu-id="f8070-255">False</span></span>                                                |
| <span data-ttu-id="f8070-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f8070-256">Is-Single-Valued</span></span>       | <span data-ttu-id="f8070-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="f8070-257">True</span></span>                                                 |
| <span data-ttu-id="f8070-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f8070-258">Is Indexed</span></span>             | <span data-ttu-id="f8070-259">False</span><span class="sxs-lookup"><span data-stu-id="f8070-259">False</span></span>                                                |
| <span data-ttu-id="f8070-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f8070-260">In Global Catalog</span></span>      | <span data-ttu-id="f8070-261">Richtig</span><span class="sxs-lookup"><span data-stu-id="f8070-261">True</span></span>                                                 |
| <span data-ttu-id="f8070-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8070-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8070-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f8070-263">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f8070-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8070-264">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f8070-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8070-265">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f8070-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8070-266">Search-Flags</span></span>           | <span data-ttu-id="f8070-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8070-267">0x00000000</span></span>                                           |
| <span data-ttu-id="f8070-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8070-268">System-Flags</span></span>           | <span data-ttu-id="f8070-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8070-269">0x00000010</span></span>                                           |
| <span data-ttu-id="f8070-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f8070-270">Classes used in</span></span>        | [<span data-ttu-id="f8070-271">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="f8070-271">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





