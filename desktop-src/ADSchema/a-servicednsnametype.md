---
title: Dienst-DNS-Name-Type-Attribut
description: Typ des DNS-Einsatzes, der für diesen Dienst gesucht werden soll. Beispielsweise ein-oder-SRV.
ms.assetid: 9a1ab2ae-b63f-4c70-b0df-de97c482bc5a
ms.tgt_platform: multiple
keywords:
- AD-Schema des Dienst-DNS-Name-Type-Attributs
- serviceDNSNameType-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Service-DNS-Name-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369bf644cac226788332cb4a2935973a5d5ffeae
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859569"
---
# <a name="service-dns-name-type-attribute"></a><span data-ttu-id="bafda-106">Dienst-DNS-Name-Type-Attribut</span><span class="sxs-lookup"><span data-stu-id="bafda-106">Service-DNS-Name-Type attribute</span></span>

<span data-ttu-id="bafda-107">Typ des DNS-Einsatzes, der für diesen Dienst gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="bafda-107">Type of DNS Record to look up for this service.</span></span> <span data-ttu-id="bafda-108">Beispielsweise ein-oder-SRV.</span><span class="sxs-lookup"><span data-stu-id="bafda-108">For example, A or SRV.</span></span>



| <span data-ttu-id="bafda-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bafda-109">Entry</span></span> | <span data-ttu-id="bafda-110">Wert</span><span class="sxs-lookup"><span data-stu-id="bafda-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="bafda-111">CN</span><span class="sxs-lookup"><span data-stu-id="bafda-111">CN</span></span>                | <span data-ttu-id="bafda-112">Dienst-DNS-Name-Type</span><span class="sxs-lookup"><span data-stu-id="bafda-112">Service-DNS-Name-Type</span></span>                       |
| <span data-ttu-id="bafda-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bafda-113">Ldap-Display-Name</span></span> | <span data-ttu-id="bafda-114">serviceDNSNameType</span><span class="sxs-lookup"><span data-stu-id="bafda-114">serviceDNSNameType</span></span>                          |
| <span data-ttu-id="bafda-115">Size</span><span class="sxs-lookup"><span data-stu-id="bafda-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="bafda-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="bafda-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="bafda-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="bafda-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="bafda-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bafda-118">Attribute-Id</span></span>      | <span data-ttu-id="bafda-119">1.2.840.113556.1.4.659</span><span class="sxs-lookup"><span data-stu-id="bafda-119">1.2.840.113556.1.4.659</span></span>                      |
| <span data-ttu-id="bafda-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bafda-120">System-Id-Guid</span></span>    | <span data-ttu-id="bafda-121">28630eba-41d5-11d1-a9c1-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="bafda-121">28630eba-41d5-11d1-a9c1-0000f80367c1</span></span>        |
| <span data-ttu-id="bafda-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="bafda-122">Syntax</span></span>            | [<span data-ttu-id="bafda-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bafda-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="bafda-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="bafda-124">Implementations</span></span>

-   [<span data-ttu-id="bafda-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bafda-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bafda-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bafda-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bafda-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bafda-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bafda-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bafda-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bafda-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bafda-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bafda-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bafda-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bafda-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bafda-131">Windows 2000 Server</span></span>



| <span data-ttu-id="bafda-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bafda-132">Entry</span></span> | <span data-ttu-id="bafda-133">Wert</span><span class="sxs-lookup"><span data-stu-id="bafda-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bafda-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bafda-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bafda-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bafda-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bafda-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="bafda-136">System-Only</span></span>            | <span data-ttu-id="bafda-137">False</span><span class="sxs-lookup"><span data-stu-id="bafda-137">False</span></span>                                                                   |
| <span data-ttu-id="bafda-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bafda-138">Is-Single-Valued</span></span>       | <span data-ttu-id="bafda-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="bafda-139">True</span></span>                                                                    |
| <span data-ttu-id="bafda-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bafda-140">Is Indexed</span></span>             | <span data-ttu-id="bafda-141">False</span><span class="sxs-lookup"><span data-stu-id="bafda-141">False</span></span>                                                                   |
| <span data-ttu-id="bafda-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bafda-142">In Global Catalog</span></span>      | <span data-ttu-id="bafda-143">False</span><span class="sxs-lookup"><span data-stu-id="bafda-143">False</span></span>                                                                   |
| <span data-ttu-id="bafda-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bafda-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="bafda-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bafda-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="bafda-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bafda-146">Range-Lower</span></span>            | <span data-ttu-id="bafda-147">1</span><span class="sxs-lookup"><span data-stu-id="bafda-147">1</span></span>                                                                       |
| <span data-ttu-id="bafda-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bafda-148">Range-Upper</span></span>            | <span data-ttu-id="bafda-149">256</span><span class="sxs-lookup"><span data-stu-id="bafda-149">256</span></span>                                                                     |
| <span data-ttu-id="bafda-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bafda-150">Search-Flags</span></span>           | <span data-ttu-id="bafda-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bafda-151">0x00000000</span></span>                                                              |
| <span data-ttu-id="bafda-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bafda-152">System-Flags</span></span>           | <span data-ttu-id="bafda-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bafda-153">0x00000010</span></span>                                                              |
| <span data-ttu-id="bafda-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bafda-154">Classes used in</span></span>        | [<span data-ttu-id="bafda-155">**Dienst-Verbindungspunkt**</span><span class="sxs-lookup"><span data-stu-id="bafda-155">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bafda-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bafda-156">Windows Server 2003</span></span>



| <span data-ttu-id="bafda-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bafda-157">Entry</span></span> | <span data-ttu-id="bafda-158">Wert</span><span class="sxs-lookup"><span data-stu-id="bafda-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bafda-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bafda-159">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bafda-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bafda-160">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bafda-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="bafda-161">System-Only</span></span>            | <span data-ttu-id="bafda-162">False</span><span class="sxs-lookup"><span data-stu-id="bafda-162">False</span></span>                                                                   |
| <span data-ttu-id="bafda-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bafda-163">Is-Single-Valued</span></span>       | <span data-ttu-id="bafda-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="bafda-164">True</span></span>                                                                    |
| <span data-ttu-id="bafda-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bafda-165">Is Indexed</span></span>             | <span data-ttu-id="bafda-166">False</span><span class="sxs-lookup"><span data-stu-id="bafda-166">False</span></span>                                                                   |
| <span data-ttu-id="bafda-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bafda-167">In Global Catalog</span></span>      | <span data-ttu-id="bafda-168">False</span><span class="sxs-lookup"><span data-stu-id="bafda-168">False</span></span>                                                                   |
| <span data-ttu-id="bafda-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bafda-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="bafda-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bafda-170">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="bafda-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bafda-171">Range-Lower</span></span>            | <span data-ttu-id="bafda-172">1</span><span class="sxs-lookup"><span data-stu-id="bafda-172">1</span></span>                                                                       |
| <span data-ttu-id="bafda-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bafda-173">Range-Upper</span></span>            | <span data-ttu-id="bafda-174">256</span><span class="sxs-lookup"><span data-stu-id="bafda-174">256</span></span>                                                                     |
| <span data-ttu-id="bafda-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bafda-175">Search-Flags</span></span>           | <span data-ttu-id="bafda-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bafda-176">0x00000000</span></span>                                                              |
| <span data-ttu-id="bafda-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bafda-177">System-Flags</span></span>           | <span data-ttu-id="bafda-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bafda-178">0x00000010</span></span>                                                              |
| <span data-ttu-id="bafda-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bafda-179">Classes used in</span></span>        | [<span data-ttu-id="bafda-180">**Dienst-Verbindungspunkt**</span><span class="sxs-lookup"><span data-stu-id="bafda-180">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bafda-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bafda-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bafda-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bafda-182">Entry</span></span> | <span data-ttu-id="bafda-183">Wert</span><span class="sxs-lookup"><span data-stu-id="bafda-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bafda-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bafda-184">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bafda-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bafda-185">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bafda-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="bafda-186">System-Only</span></span>            | <span data-ttu-id="bafda-187">False</span><span class="sxs-lookup"><span data-stu-id="bafda-187">False</span></span>                                                                   |
| <span data-ttu-id="bafda-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bafda-188">Is-Single-Valued</span></span>       | <span data-ttu-id="bafda-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="bafda-189">True</span></span>                                                                    |
| <span data-ttu-id="bafda-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bafda-190">Is Indexed</span></span>             | <span data-ttu-id="bafda-191">False</span><span class="sxs-lookup"><span data-stu-id="bafda-191">False</span></span>                                                                   |
| <span data-ttu-id="bafda-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bafda-192">In Global Catalog</span></span>      | <span data-ttu-id="bafda-193">False</span><span class="sxs-lookup"><span data-stu-id="bafda-193">False</span></span>                                                                   |
| <span data-ttu-id="bafda-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bafda-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="bafda-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bafda-195">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="bafda-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bafda-196">Range-Lower</span></span>            | <span data-ttu-id="bafda-197">1</span><span class="sxs-lookup"><span data-stu-id="bafda-197">1</span></span>                                                                       |
| <span data-ttu-id="bafda-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bafda-198">Range-Upper</span></span>            | <span data-ttu-id="bafda-199">256</span><span class="sxs-lookup"><span data-stu-id="bafda-199">256</span></span>                                                                     |
| <span data-ttu-id="bafda-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bafda-200">Search-Flags</span></span>           | <span data-ttu-id="bafda-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bafda-201">0x00000000</span></span>                                                              |
| <span data-ttu-id="bafda-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bafda-202">System-Flags</span></span>           | <span data-ttu-id="bafda-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bafda-203">0x00000010</span></span>                                                              |
| <span data-ttu-id="bafda-204">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bafda-204">Classes used in</span></span>        | [<span data-ttu-id="bafda-205">**Dienst-Verbindungspunkt**</span><span class="sxs-lookup"><span data-stu-id="bafda-205">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bafda-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bafda-206">Windows Server 2008</span></span>



| <span data-ttu-id="bafda-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bafda-207">Entry</span></span> | <span data-ttu-id="bafda-208">Wert</span><span class="sxs-lookup"><span data-stu-id="bafda-208">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bafda-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bafda-209">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bafda-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bafda-210">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bafda-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="bafda-211">System-Only</span></span>            | <span data-ttu-id="bafda-212">False</span><span class="sxs-lookup"><span data-stu-id="bafda-212">False</span></span>                                                                   |
| <span data-ttu-id="bafda-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bafda-213">Is-Single-Valued</span></span>       | <span data-ttu-id="bafda-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="bafda-214">True</span></span>                                                                    |
| <span data-ttu-id="bafda-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bafda-215">Is Indexed</span></span>             | <span data-ttu-id="bafda-216">False</span><span class="sxs-lookup"><span data-stu-id="bafda-216">False</span></span>                                                                   |
| <span data-ttu-id="bafda-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bafda-217">In Global Catalog</span></span>      | <span data-ttu-id="bafda-218">False</span><span class="sxs-lookup"><span data-stu-id="bafda-218">False</span></span>                                                                   |
| <span data-ttu-id="bafda-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bafda-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="bafda-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bafda-220">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="bafda-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bafda-221">Range-Lower</span></span>            | <span data-ttu-id="bafda-222">1</span><span class="sxs-lookup"><span data-stu-id="bafda-222">1</span></span>                                                                       |
| <span data-ttu-id="bafda-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bafda-223">Range-Upper</span></span>            | <span data-ttu-id="bafda-224">256</span><span class="sxs-lookup"><span data-stu-id="bafda-224">256</span></span>                                                                     |
| <span data-ttu-id="bafda-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bafda-225">Search-Flags</span></span>           | <span data-ttu-id="bafda-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bafda-226">0x00000000</span></span>                                                              |
| <span data-ttu-id="bafda-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bafda-227">System-Flags</span></span>           | <span data-ttu-id="bafda-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bafda-228">0x00000010</span></span>                                                              |
| <span data-ttu-id="bafda-229">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bafda-229">Classes used in</span></span>        | [<span data-ttu-id="bafda-230">**Dienst-Verbindungspunkt**</span><span class="sxs-lookup"><span data-stu-id="bafda-230">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bafda-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bafda-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bafda-232">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bafda-232">Entry</span></span> | <span data-ttu-id="bafda-233">Wert</span><span class="sxs-lookup"><span data-stu-id="bafda-233">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bafda-234">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bafda-234">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bafda-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bafda-235">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bafda-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="bafda-236">System-Only</span></span>            | <span data-ttu-id="bafda-237">False</span><span class="sxs-lookup"><span data-stu-id="bafda-237">False</span></span>                                                                   |
| <span data-ttu-id="bafda-238">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bafda-238">Is-Single-Valued</span></span>       | <span data-ttu-id="bafda-239">Richtig</span><span class="sxs-lookup"><span data-stu-id="bafda-239">True</span></span>                                                                    |
| <span data-ttu-id="bafda-240">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bafda-240">Is Indexed</span></span>             | <span data-ttu-id="bafda-241">False</span><span class="sxs-lookup"><span data-stu-id="bafda-241">False</span></span>                                                                   |
| <span data-ttu-id="bafda-242">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bafda-242">In Global Catalog</span></span>      | <span data-ttu-id="bafda-243">False</span><span class="sxs-lookup"><span data-stu-id="bafda-243">False</span></span>                                                                   |
| <span data-ttu-id="bafda-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bafda-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="bafda-245">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bafda-245">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="bafda-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bafda-246">Range-Lower</span></span>            | <span data-ttu-id="bafda-247">1</span><span class="sxs-lookup"><span data-stu-id="bafda-247">1</span></span>                                                                       |
| <span data-ttu-id="bafda-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bafda-248">Range-Upper</span></span>            | <span data-ttu-id="bafda-249">256</span><span class="sxs-lookup"><span data-stu-id="bafda-249">256</span></span>                                                                     |
| <span data-ttu-id="bafda-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bafda-250">Search-Flags</span></span>           | <span data-ttu-id="bafda-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bafda-251">0x00000000</span></span>                                                              |
| <span data-ttu-id="bafda-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bafda-252">System-Flags</span></span>           | <span data-ttu-id="bafda-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bafda-253">0x00000010</span></span>                                                              |
| <span data-ttu-id="bafda-254">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bafda-254">Classes used in</span></span>        | [<span data-ttu-id="bafda-255">**Dienst-Verbindungspunkt**</span><span class="sxs-lookup"><span data-stu-id="bafda-255">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bafda-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bafda-256">Windows Server 2012</span></span>



| <span data-ttu-id="bafda-257">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bafda-257">Entry</span></span> | <span data-ttu-id="bafda-258">Wert</span><span class="sxs-lookup"><span data-stu-id="bafda-258">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bafda-259">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bafda-259">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bafda-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bafda-260">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="bafda-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="bafda-261">System-Only</span></span>            | <span data-ttu-id="bafda-262">False</span><span class="sxs-lookup"><span data-stu-id="bafda-262">False</span></span>                                                                   |
| <span data-ttu-id="bafda-263">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bafda-263">Is-Single-Valued</span></span>       | <span data-ttu-id="bafda-264">Richtig</span><span class="sxs-lookup"><span data-stu-id="bafda-264">True</span></span>                                                                    |
| <span data-ttu-id="bafda-265">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bafda-265">Is Indexed</span></span>             | <span data-ttu-id="bafda-266">False</span><span class="sxs-lookup"><span data-stu-id="bafda-266">False</span></span>                                                                   |
| <span data-ttu-id="bafda-267">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bafda-267">In Global Catalog</span></span>      | <span data-ttu-id="bafda-268">False</span><span class="sxs-lookup"><span data-stu-id="bafda-268">False</span></span>                                                                   |
| <span data-ttu-id="bafda-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bafda-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="bafda-270">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bafda-270">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="bafda-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bafda-271">Range-Lower</span></span>            | <span data-ttu-id="bafda-272">1</span><span class="sxs-lookup"><span data-stu-id="bafda-272">1</span></span>                                                                       |
| <span data-ttu-id="bafda-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bafda-273">Range-Upper</span></span>            | <span data-ttu-id="bafda-274">256</span><span class="sxs-lookup"><span data-stu-id="bafda-274">256</span></span>                                                                     |
| <span data-ttu-id="bafda-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bafda-275">Search-Flags</span></span>           | <span data-ttu-id="bafda-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bafda-276">0x00000000</span></span>                                                              |
| <span data-ttu-id="bafda-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bafda-277">System-Flags</span></span>           | <span data-ttu-id="bafda-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bafda-278">0x00000010</span></span>                                                              |
| <span data-ttu-id="bafda-279">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bafda-279">Classes used in</span></span>        | [<span data-ttu-id="bafda-280">**Dienst-Verbindungspunkt**</span><span class="sxs-lookup"><span data-stu-id="bafda-280">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



 

 





