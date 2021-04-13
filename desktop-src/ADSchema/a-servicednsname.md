---
title: Dienst-DNS-Name-Attribut
description: Der DNS-Name für die Suche nach einem Server, auf dem dieser Dienst ausgeführt wird.
ms.assetid: b2852276-30f5-4c2a-9f72-9df0d7c0c994
ms.tgt_platform: multiple
keywords:
- AD-Schema für Dienst-DNS-Name-Attribut
- servicednsname-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Service-DNS-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b881587a1358a6e7a3a814efb80af122ac5669
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519999"
---
# <a name="service-dns-name-attribute"></a><span data-ttu-id="544ae-105">Dienst-DNS-Name-Attribut</span><span class="sxs-lookup"><span data-stu-id="544ae-105">Service-DNS-Name attribute</span></span>

<span data-ttu-id="544ae-106">Der DNS-Name für die Suche nach einem Server, auf dem dieser Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="544ae-106">The DNS name to look up to find a server running this service.</span></span>



| <span data-ttu-id="544ae-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="544ae-107">Entry</span></span> | <span data-ttu-id="544ae-108">Wert</span><span class="sxs-lookup"><span data-stu-id="544ae-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="544ae-109">CN</span><span class="sxs-lookup"><span data-stu-id="544ae-109">CN</span></span>                | <span data-ttu-id="544ae-110">Dienst-DNS-Name</span><span class="sxs-lookup"><span data-stu-id="544ae-110">Service-DNS-Name</span></span>                            |
| <span data-ttu-id="544ae-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="544ae-111">Ldap-Display-Name</span></span> | <span data-ttu-id="544ae-112">serviceDNSName</span><span class="sxs-lookup"><span data-stu-id="544ae-112">serviceDNSName</span></span>                              |
| <span data-ttu-id="544ae-113">Size</span><span class="sxs-lookup"><span data-stu-id="544ae-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="544ae-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="544ae-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="544ae-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="544ae-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="544ae-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="544ae-116">Attribute-Id</span></span>      | <span data-ttu-id="544ae-117">1.2.840.113556.1.4.657</span><span class="sxs-lookup"><span data-stu-id="544ae-117">1.2.840.113556.1.4.657</span></span>                      |
| <span data-ttu-id="544ae-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="544ae-118">System-Id-Guid</span></span>    | <span data-ttu-id="544ae-119">28630eb8-41d5-11d1-a9c1-0000 C1</span><span class="sxs-lookup"><span data-stu-id="544ae-119">28630eb8-41d5-11d1-a9c1-0000f80367c1</span></span>        |
| <span data-ttu-id="544ae-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="544ae-120">Syntax</span></span>            | [<span data-ttu-id="544ae-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="544ae-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="544ae-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="544ae-122">Implementations</span></span>

-   [<span data-ttu-id="544ae-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="544ae-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="544ae-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="544ae-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="544ae-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="544ae-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="544ae-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="544ae-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="544ae-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="544ae-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="544ae-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="544ae-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="544ae-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="544ae-129">Windows 2000 Server</span></span>



| <span data-ttu-id="544ae-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="544ae-130">Entry</span></span> | <span data-ttu-id="544ae-131">Wert</span><span class="sxs-lookup"><span data-stu-id="544ae-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="544ae-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="544ae-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="544ae-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="544ae-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="544ae-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="544ae-134">System-Only</span></span>            | <span data-ttu-id="544ae-135">False</span><span class="sxs-lookup"><span data-stu-id="544ae-135">False</span></span>                                                                   |
| <span data-ttu-id="544ae-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="544ae-136">Is-Single-Valued</span></span>       | <span data-ttu-id="544ae-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="544ae-137">True</span></span>                                                                    |
| <span data-ttu-id="544ae-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="544ae-138">Is Indexed</span></span>             | <span data-ttu-id="544ae-139">False</span><span class="sxs-lookup"><span data-stu-id="544ae-139">False</span></span>                                                                   |
| <span data-ttu-id="544ae-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="544ae-140">In Global Catalog</span></span>      | <span data-ttu-id="544ae-141">False</span><span class="sxs-lookup"><span data-stu-id="544ae-141">False</span></span>                                                                   |
| <span data-ttu-id="544ae-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="544ae-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="544ae-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="544ae-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="544ae-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="544ae-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="544ae-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="544ae-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="544ae-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="544ae-146">Search-Flags</span></span>           | <span data-ttu-id="544ae-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="544ae-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="544ae-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="544ae-148">System-Flags</span></span>           | <span data-ttu-id="544ae-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="544ae-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="544ae-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="544ae-150">Classes used in</span></span>        | [<span data-ttu-id="544ae-151">**Dienst-Verbindungspunkt**</span><span class="sxs-lookup"><span data-stu-id="544ae-151">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="544ae-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="544ae-152">Windows Server 2003</span></span>



| <span data-ttu-id="544ae-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="544ae-153">Entry</span></span> | <span data-ttu-id="544ae-154">Wert</span><span class="sxs-lookup"><span data-stu-id="544ae-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="544ae-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="544ae-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="544ae-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="544ae-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="544ae-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="544ae-157">System-Only</span></span>            | <span data-ttu-id="544ae-158">False</span><span class="sxs-lookup"><span data-stu-id="544ae-158">False</span></span>                                                                   |
| <span data-ttu-id="544ae-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="544ae-159">Is-Single-Valued</span></span>       | <span data-ttu-id="544ae-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="544ae-160">True</span></span>                                                                    |
| <span data-ttu-id="544ae-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="544ae-161">Is Indexed</span></span>             | <span data-ttu-id="544ae-162">False</span><span class="sxs-lookup"><span data-stu-id="544ae-162">False</span></span>                                                                   |
| <span data-ttu-id="544ae-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="544ae-163">In Global Catalog</span></span>      | <span data-ttu-id="544ae-164">False</span><span class="sxs-lookup"><span data-stu-id="544ae-164">False</span></span>                                                                   |
| <span data-ttu-id="544ae-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="544ae-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="544ae-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="544ae-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="544ae-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="544ae-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="544ae-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="544ae-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="544ae-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="544ae-169">Search-Flags</span></span>           | <span data-ttu-id="544ae-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="544ae-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="544ae-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="544ae-171">System-Flags</span></span>           | <span data-ttu-id="544ae-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="544ae-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="544ae-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="544ae-173">Classes used in</span></span>        | [<span data-ttu-id="544ae-174">**Dienst-Verbindungspunkt**</span><span class="sxs-lookup"><span data-stu-id="544ae-174">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="544ae-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="544ae-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="544ae-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="544ae-176">Entry</span></span> | <span data-ttu-id="544ae-177">Wert</span><span class="sxs-lookup"><span data-stu-id="544ae-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="544ae-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="544ae-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="544ae-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="544ae-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="544ae-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="544ae-180">System-Only</span></span>            | <span data-ttu-id="544ae-181">False</span><span class="sxs-lookup"><span data-stu-id="544ae-181">False</span></span>                                                                   |
| <span data-ttu-id="544ae-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="544ae-182">Is-Single-Valued</span></span>       | <span data-ttu-id="544ae-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="544ae-183">True</span></span>                                                                    |
| <span data-ttu-id="544ae-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="544ae-184">Is Indexed</span></span>             | <span data-ttu-id="544ae-185">False</span><span class="sxs-lookup"><span data-stu-id="544ae-185">False</span></span>                                                                   |
| <span data-ttu-id="544ae-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="544ae-186">In Global Catalog</span></span>      | <span data-ttu-id="544ae-187">False</span><span class="sxs-lookup"><span data-stu-id="544ae-187">False</span></span>                                                                   |
| <span data-ttu-id="544ae-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="544ae-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="544ae-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="544ae-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="544ae-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="544ae-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="544ae-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="544ae-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="544ae-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="544ae-192">Search-Flags</span></span>           | <span data-ttu-id="544ae-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="544ae-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="544ae-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="544ae-194">System-Flags</span></span>           | <span data-ttu-id="544ae-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="544ae-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="544ae-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="544ae-196">Classes used in</span></span>        | [<span data-ttu-id="544ae-197">**Dienst-Verbindungspunkt**</span><span class="sxs-lookup"><span data-stu-id="544ae-197">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="544ae-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="544ae-198">Windows Server 2008</span></span>



| <span data-ttu-id="544ae-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="544ae-199">Entry</span></span> | <span data-ttu-id="544ae-200">Wert</span><span class="sxs-lookup"><span data-stu-id="544ae-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="544ae-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="544ae-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="544ae-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="544ae-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="544ae-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="544ae-203">System-Only</span></span>            | <span data-ttu-id="544ae-204">False</span><span class="sxs-lookup"><span data-stu-id="544ae-204">False</span></span>                                                                   |
| <span data-ttu-id="544ae-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="544ae-205">Is-Single-Valued</span></span>       | <span data-ttu-id="544ae-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="544ae-206">True</span></span>                                                                    |
| <span data-ttu-id="544ae-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="544ae-207">Is Indexed</span></span>             | <span data-ttu-id="544ae-208">False</span><span class="sxs-lookup"><span data-stu-id="544ae-208">False</span></span>                                                                   |
| <span data-ttu-id="544ae-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="544ae-209">In Global Catalog</span></span>      | <span data-ttu-id="544ae-210">False</span><span class="sxs-lookup"><span data-stu-id="544ae-210">False</span></span>                                                                   |
| <span data-ttu-id="544ae-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="544ae-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="544ae-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="544ae-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="544ae-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="544ae-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="544ae-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="544ae-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="544ae-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="544ae-215">Search-Flags</span></span>           | <span data-ttu-id="544ae-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="544ae-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="544ae-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="544ae-217">System-Flags</span></span>           | <span data-ttu-id="544ae-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="544ae-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="544ae-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="544ae-219">Classes used in</span></span>        | [<span data-ttu-id="544ae-220">**Dienst-Verbindungspunkt**</span><span class="sxs-lookup"><span data-stu-id="544ae-220">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="544ae-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="544ae-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="544ae-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="544ae-222">Entry</span></span> | <span data-ttu-id="544ae-223">Wert</span><span class="sxs-lookup"><span data-stu-id="544ae-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="544ae-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="544ae-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="544ae-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="544ae-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="544ae-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="544ae-226">System-Only</span></span>            | <span data-ttu-id="544ae-227">False</span><span class="sxs-lookup"><span data-stu-id="544ae-227">False</span></span>                                                                   |
| <span data-ttu-id="544ae-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="544ae-228">Is-Single-Valued</span></span>       | <span data-ttu-id="544ae-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="544ae-229">True</span></span>                                                                    |
| <span data-ttu-id="544ae-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="544ae-230">Is Indexed</span></span>             | <span data-ttu-id="544ae-231">False</span><span class="sxs-lookup"><span data-stu-id="544ae-231">False</span></span>                                                                   |
| <span data-ttu-id="544ae-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="544ae-232">In Global Catalog</span></span>      | <span data-ttu-id="544ae-233">False</span><span class="sxs-lookup"><span data-stu-id="544ae-233">False</span></span>                                                                   |
| <span data-ttu-id="544ae-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="544ae-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="544ae-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="544ae-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="544ae-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="544ae-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="544ae-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="544ae-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="544ae-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="544ae-238">Search-Flags</span></span>           | <span data-ttu-id="544ae-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="544ae-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="544ae-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="544ae-240">System-Flags</span></span>           | <span data-ttu-id="544ae-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="544ae-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="544ae-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="544ae-242">Classes used in</span></span>        | [<span data-ttu-id="544ae-243">**Dienst-Verbindungspunkt**</span><span class="sxs-lookup"><span data-stu-id="544ae-243">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="544ae-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="544ae-244">Windows Server 2012</span></span>



| <span data-ttu-id="544ae-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="544ae-245">Entry</span></span> | <span data-ttu-id="544ae-246">Wert</span><span class="sxs-lookup"><span data-stu-id="544ae-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="544ae-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="544ae-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="544ae-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="544ae-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="544ae-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="544ae-249">System-Only</span></span>            | <span data-ttu-id="544ae-250">False</span><span class="sxs-lookup"><span data-stu-id="544ae-250">False</span></span>                                                                   |
| <span data-ttu-id="544ae-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="544ae-251">Is-Single-Valued</span></span>       | <span data-ttu-id="544ae-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="544ae-252">True</span></span>                                                                    |
| <span data-ttu-id="544ae-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="544ae-253">Is Indexed</span></span>             | <span data-ttu-id="544ae-254">False</span><span class="sxs-lookup"><span data-stu-id="544ae-254">False</span></span>                                                                   |
| <span data-ttu-id="544ae-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="544ae-255">In Global Catalog</span></span>      | <span data-ttu-id="544ae-256">False</span><span class="sxs-lookup"><span data-stu-id="544ae-256">False</span></span>                                                                   |
| <span data-ttu-id="544ae-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="544ae-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="544ae-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="544ae-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="544ae-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="544ae-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="544ae-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="544ae-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="544ae-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="544ae-261">Search-Flags</span></span>           | <span data-ttu-id="544ae-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="544ae-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="544ae-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="544ae-263">System-Flags</span></span>           | <span data-ttu-id="544ae-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="544ae-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="544ae-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="544ae-265">Classes used in</span></span>        | [<span data-ttu-id="544ae-266">**Dienst-Verbindungspunkt**</span><span class="sxs-lookup"><span data-stu-id="544ae-266">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



 

 





