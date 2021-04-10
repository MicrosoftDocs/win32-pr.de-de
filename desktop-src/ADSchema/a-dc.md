---
title: Domain-Component-Attribut
description: Das Benennungs Attribut für Domänen-und DNS-Objekte. Wird normalerweise als Domänen Controller Domänen Name angezeigt.
ms.assetid: 1d674af1-ed2f-4266-9704-8c6ed5a9bdd8
ms.tgt_platform: multiple
keywords:
- AD-Schema für Domain-Component-Attribut
- AD-Schema für DC-Attribut
topic_type:
- apiref
api_name:
- Domain-Component
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97a6958d51c6e0e29f70685b2624fb194d42e05
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107150"
---
# <a name="domain-component-attribute"></a><span data-ttu-id="47490-106">Domain-Component-Attribut</span><span class="sxs-lookup"><span data-stu-id="47490-106">Domain-Component attribute</span></span>

<span data-ttu-id="47490-107">Das Benennungs Attribut für Domänen-und DNS-Objekte.</span><span class="sxs-lookup"><span data-stu-id="47490-107">The naming attribute for Domain and DNS objects.</span></span> <span data-ttu-id="47490-108">Wird normalerweise als DC = Domänen Name angezeigt.</span><span class="sxs-lookup"><span data-stu-id="47490-108">Usually displayed as dc=DomainName.</span></span>



| <span data-ttu-id="47490-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47490-109">Entry</span></span> | <span data-ttu-id="47490-110">Wert</span><span class="sxs-lookup"><span data-stu-id="47490-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="47490-111">CN</span><span class="sxs-lookup"><span data-stu-id="47490-111">CN</span></span>                | <span data-ttu-id="47490-112">Domain-Component</span><span class="sxs-lookup"><span data-stu-id="47490-112">Domain-Component</span></span>                            |
| <span data-ttu-id="47490-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="47490-113">Ldap-Display-Name</span></span> | <span data-ttu-id="47490-114">dc</span><span class="sxs-lookup"><span data-stu-id="47490-114">dc</span></span>                                          |
| <span data-ttu-id="47490-115">Size</span><span class="sxs-lookup"><span data-stu-id="47490-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="47490-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="47490-116">Update Privilege</span></span>  | <span data-ttu-id="47490-117">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="47490-117">Domain administrator</span></span>                        |
| <span data-ttu-id="47490-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="47490-118">Update Frequency</span></span>  | <span data-ttu-id="47490-119">Wenn die Domäne erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="47490-119">When the domain is created.</span></span>                 |
| <span data-ttu-id="47490-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="47490-120">Attribute-Id</span></span>      | <span data-ttu-id="47490-121">0.9.2342.19200300.100.1.25</span><span class="sxs-lookup"><span data-stu-id="47490-121">0.9.2342.19200300.100.1.25</span></span>                  |
| <span data-ttu-id="47490-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="47490-122">System-Id-Guid</span></span>    | <span data-ttu-id="47490-123">19195a55-6da0-11D0-afd3-00c04f 930c9</span><span class="sxs-lookup"><span data-stu-id="47490-123">19195a55-6da0-11d0-afd3-00c04fd930c9</span></span>        |
| <span data-ttu-id="47490-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="47490-124">Syntax</span></span>            | [<span data-ttu-id="47490-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="47490-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="47490-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="47490-126">Implementations</span></span>

-   [<span data-ttu-id="47490-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="47490-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="47490-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="47490-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="47490-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="47490-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="47490-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="47490-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="47490-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="47490-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="47490-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="47490-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="47490-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="47490-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="47490-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="47490-134">Windows 2000 Server</span></span>



| <span data-ttu-id="47490-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47490-135">Entry</span></span> | <span data-ttu-id="47490-136">Wert</span><span class="sxs-lookup"><span data-stu-id="47490-136">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47490-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="47490-137">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="47490-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47490-138">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="47490-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="47490-139">System-Only</span></span>            | <span data-ttu-id="47490-140">False</span><span class="sxs-lookup"><span data-stu-id="47490-140">False</span></span>                                                                                                                   |
| <span data-ttu-id="47490-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="47490-141">Is-Single-Valued</span></span>       | <span data-ttu-id="47490-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="47490-142">True</span></span>                                                                                                                    |
| <span data-ttu-id="47490-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="47490-143">Is Indexed</span></span>             | <span data-ttu-id="47490-144">False</span><span class="sxs-lookup"><span data-stu-id="47490-144">False</span></span>                                                                                                                   |
| <span data-ttu-id="47490-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="47490-145">In Global Catalog</span></span>      | <span data-ttu-id="47490-146">Richtig</span><span class="sxs-lookup"><span data-stu-id="47490-146">True</span></span>                                                                                                                    |
| <span data-ttu-id="47490-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47490-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="47490-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="47490-148">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="47490-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47490-149">Range-Lower</span></span>            | <span data-ttu-id="47490-150">1</span><span class="sxs-lookup"><span data-stu-id="47490-150">1</span></span>                                                                                                                       |
| <span data-ttu-id="47490-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47490-151">Range-Upper</span></span>            | <span data-ttu-id="47490-152">255</span><span class="sxs-lookup"><span data-stu-id="47490-152">255</span></span>                                                                                                                     |
| <span data-ttu-id="47490-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47490-153">Search-Flags</span></span>           | <span data-ttu-id="47490-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47490-154">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="47490-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47490-155">System-Flags</span></span>           | <span data-ttu-id="47490-156">0x00000012</span><span class="sxs-lookup"><span data-stu-id="47490-156">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="47490-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="47490-157">Classes used in</span></span>        | [<span data-ttu-id="47490-158">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="47490-158">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="47490-159">**DNS-Zone**</span><span class="sxs-lookup"><span data-stu-id="47490-159">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="47490-160">**Domain**</span><span class="sxs-lookup"><span data-stu-id="47490-160">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="47490-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="47490-161">Windows Server 2003</span></span>



| <span data-ttu-id="47490-162">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47490-162">Entry</span></span> | <span data-ttu-id="47490-163">Wert</span><span class="sxs-lookup"><span data-stu-id="47490-163">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47490-164">Link-ID</span><span class="sxs-lookup"><span data-stu-id="47490-164">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="47490-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47490-165">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="47490-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="47490-166">System-Only</span></span>            | <span data-ttu-id="47490-167">False</span><span class="sxs-lookup"><span data-stu-id="47490-167">False</span></span>                                                                                                                   |
| <span data-ttu-id="47490-168">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="47490-168">Is-Single-Valued</span></span>       | <span data-ttu-id="47490-169">Richtig</span><span class="sxs-lookup"><span data-stu-id="47490-169">True</span></span>                                                                                                                    |
| <span data-ttu-id="47490-170">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="47490-170">Is Indexed</span></span>             | <span data-ttu-id="47490-171">False</span><span class="sxs-lookup"><span data-stu-id="47490-171">False</span></span>                                                                                                                   |
| <span data-ttu-id="47490-172">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="47490-172">In Global Catalog</span></span>      | <span data-ttu-id="47490-173">Richtig</span><span class="sxs-lookup"><span data-stu-id="47490-173">True</span></span>                                                                                                                    |
| <span data-ttu-id="47490-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47490-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="47490-175">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="47490-175">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="47490-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47490-176">Range-Lower</span></span>            | <span data-ttu-id="47490-177">1</span><span class="sxs-lookup"><span data-stu-id="47490-177">1</span></span>                                                                                                                       |
| <span data-ttu-id="47490-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47490-178">Range-Upper</span></span>            | <span data-ttu-id="47490-179">255</span><span class="sxs-lookup"><span data-stu-id="47490-179">255</span></span>                                                                                                                     |
| <span data-ttu-id="47490-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47490-180">Search-Flags</span></span>           | <span data-ttu-id="47490-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47490-181">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="47490-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47490-182">System-Flags</span></span>           | <span data-ttu-id="47490-183">0x00000012</span><span class="sxs-lookup"><span data-stu-id="47490-183">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="47490-184">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="47490-184">Classes used in</span></span>        | [<span data-ttu-id="47490-185">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="47490-185">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="47490-186">**DNS-Zone**</span><span class="sxs-lookup"><span data-stu-id="47490-186">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="47490-187">**Domain**</span><span class="sxs-lookup"><span data-stu-id="47490-187">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="adam"></a><span data-ttu-id="47490-188">Adam</span><span class="sxs-lookup"><span data-stu-id="47490-188">ADAM</span></span>



| <span data-ttu-id="47490-189">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47490-189">Entry</span></span> | <span data-ttu-id="47490-190">Wert</span><span class="sxs-lookup"><span data-stu-id="47490-190">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="47490-191">Link-ID</span><span class="sxs-lookup"><span data-stu-id="47490-191">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="47490-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47490-192">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="47490-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="47490-193">System-Only</span></span>            | <span data-ttu-id="47490-194">False</span><span class="sxs-lookup"><span data-stu-id="47490-194">False</span></span>                                 |
| <span data-ttu-id="47490-195">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="47490-195">Is-Single-Valued</span></span>       | <span data-ttu-id="47490-196">Richtig</span><span class="sxs-lookup"><span data-stu-id="47490-196">True</span></span>                                  |
| <span data-ttu-id="47490-197">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="47490-197">Is Indexed</span></span>             | <span data-ttu-id="47490-198">False</span><span class="sxs-lookup"><span data-stu-id="47490-198">False</span></span>                                 |
| <span data-ttu-id="47490-199">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="47490-199">In Global Catalog</span></span>      | <span data-ttu-id="47490-200">Richtig</span><span class="sxs-lookup"><span data-stu-id="47490-200">True</span></span>                                  |
| <span data-ttu-id="47490-201">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47490-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="47490-202">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="47490-202">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="47490-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47490-203">Range-Lower</span></span>            | <span data-ttu-id="47490-204">1</span><span class="sxs-lookup"><span data-stu-id="47490-204">1</span></span>                                     |
| <span data-ttu-id="47490-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47490-205">Range-Upper</span></span>            | <span data-ttu-id="47490-206">255</span><span class="sxs-lookup"><span data-stu-id="47490-206">255</span></span>                                   |
| <span data-ttu-id="47490-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47490-207">Search-Flags</span></span>           | <span data-ttu-id="47490-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47490-208">0x00000000</span></span>                            |
| <span data-ttu-id="47490-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47490-209">System-Flags</span></span>           | <span data-ttu-id="47490-210">0x00000012</span><span class="sxs-lookup"><span data-stu-id="47490-210">0x00000012</span></span>                            |
| <span data-ttu-id="47490-211">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="47490-211">Classes used in</span></span>        | [<span data-ttu-id="47490-212">**Domain**</span><span class="sxs-lookup"><span data-stu-id="47490-212">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="47490-213">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="47490-213">Windows Server 2003 R2</span></span>



| <span data-ttu-id="47490-214">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47490-214">Entry</span></span> | <span data-ttu-id="47490-215">Wert</span><span class="sxs-lookup"><span data-stu-id="47490-215">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47490-216">Link-ID</span><span class="sxs-lookup"><span data-stu-id="47490-216">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="47490-217">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47490-217">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="47490-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="47490-218">System-Only</span></span>            | <span data-ttu-id="47490-219">False</span><span class="sxs-lookup"><span data-stu-id="47490-219">False</span></span>                                                                                                                   |
| <span data-ttu-id="47490-220">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="47490-220">Is-Single-Valued</span></span>       | <span data-ttu-id="47490-221">Richtig</span><span class="sxs-lookup"><span data-stu-id="47490-221">True</span></span>                                                                                                                    |
| <span data-ttu-id="47490-222">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="47490-222">Is Indexed</span></span>             | <span data-ttu-id="47490-223">False</span><span class="sxs-lookup"><span data-stu-id="47490-223">False</span></span>                                                                                                                   |
| <span data-ttu-id="47490-224">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="47490-224">In Global Catalog</span></span>      | <span data-ttu-id="47490-225">Richtig</span><span class="sxs-lookup"><span data-stu-id="47490-225">True</span></span>                                                                                                                    |
| <span data-ttu-id="47490-226">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47490-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="47490-227">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="47490-227">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="47490-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47490-228">Range-Lower</span></span>            | <span data-ttu-id="47490-229">1</span><span class="sxs-lookup"><span data-stu-id="47490-229">1</span></span>                                                                                                                       |
| <span data-ttu-id="47490-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47490-230">Range-Upper</span></span>            | <span data-ttu-id="47490-231">255</span><span class="sxs-lookup"><span data-stu-id="47490-231">255</span></span>                                                                                                                     |
| <span data-ttu-id="47490-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47490-232">Search-Flags</span></span>           | <span data-ttu-id="47490-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47490-233">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="47490-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47490-234">System-Flags</span></span>           | <span data-ttu-id="47490-235">0x00000012</span><span class="sxs-lookup"><span data-stu-id="47490-235">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="47490-236">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="47490-236">Classes used in</span></span>        | [<span data-ttu-id="47490-237">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="47490-237">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="47490-238">**DNS-Zone**</span><span class="sxs-lookup"><span data-stu-id="47490-238">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="47490-239">**Domain**</span><span class="sxs-lookup"><span data-stu-id="47490-239">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="47490-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47490-240">Windows Server 2008</span></span>



| <span data-ttu-id="47490-241">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47490-241">Entry</span></span> | <span data-ttu-id="47490-242">Wert</span><span class="sxs-lookup"><span data-stu-id="47490-242">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47490-243">Link-ID</span><span class="sxs-lookup"><span data-stu-id="47490-243">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="47490-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47490-244">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="47490-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="47490-245">System-Only</span></span>            | <span data-ttu-id="47490-246">False</span><span class="sxs-lookup"><span data-stu-id="47490-246">False</span></span>                                                                                                                   |
| <span data-ttu-id="47490-247">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="47490-247">Is-Single-Valued</span></span>       | <span data-ttu-id="47490-248">Richtig</span><span class="sxs-lookup"><span data-stu-id="47490-248">True</span></span>                                                                                                                    |
| <span data-ttu-id="47490-249">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="47490-249">Is Indexed</span></span>             | <span data-ttu-id="47490-250">False</span><span class="sxs-lookup"><span data-stu-id="47490-250">False</span></span>                                                                                                                   |
| <span data-ttu-id="47490-251">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="47490-251">In Global Catalog</span></span>      | <span data-ttu-id="47490-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="47490-252">True</span></span>                                                                                                                    |
| <span data-ttu-id="47490-253">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47490-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="47490-254">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="47490-254">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="47490-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47490-255">Range-Lower</span></span>            | <span data-ttu-id="47490-256">1</span><span class="sxs-lookup"><span data-stu-id="47490-256">1</span></span>                                                                                                                       |
| <span data-ttu-id="47490-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47490-257">Range-Upper</span></span>            | <span data-ttu-id="47490-258">255</span><span class="sxs-lookup"><span data-stu-id="47490-258">255</span></span>                                                                                                                     |
| <span data-ttu-id="47490-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47490-259">Search-Flags</span></span>           | <span data-ttu-id="47490-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47490-260">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="47490-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47490-261">System-Flags</span></span>           | <span data-ttu-id="47490-262">0x00000012</span><span class="sxs-lookup"><span data-stu-id="47490-262">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="47490-263">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="47490-263">Classes used in</span></span>        | [<span data-ttu-id="47490-264">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="47490-264">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="47490-265">**DNS-Zone**</span><span class="sxs-lookup"><span data-stu-id="47490-265">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="47490-266">**Domain**</span><span class="sxs-lookup"><span data-stu-id="47490-266">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="47490-267">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="47490-267">Windows Server 2008 R2</span></span>



| <span data-ttu-id="47490-268">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47490-268">Entry</span></span> | <span data-ttu-id="47490-269">Wert</span><span class="sxs-lookup"><span data-stu-id="47490-269">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47490-270">Link-ID</span><span class="sxs-lookup"><span data-stu-id="47490-270">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="47490-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47490-271">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="47490-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="47490-272">System-Only</span></span>            | <span data-ttu-id="47490-273">False</span><span class="sxs-lookup"><span data-stu-id="47490-273">False</span></span>                                                                                                                   |
| <span data-ttu-id="47490-274">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="47490-274">Is-Single-Valued</span></span>       | <span data-ttu-id="47490-275">Richtig</span><span class="sxs-lookup"><span data-stu-id="47490-275">True</span></span>                                                                                                                    |
| <span data-ttu-id="47490-276">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="47490-276">Is Indexed</span></span>             | <span data-ttu-id="47490-277">False</span><span class="sxs-lookup"><span data-stu-id="47490-277">False</span></span>                                                                                                                   |
| <span data-ttu-id="47490-278">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="47490-278">In Global Catalog</span></span>      | <span data-ttu-id="47490-279">Richtig</span><span class="sxs-lookup"><span data-stu-id="47490-279">True</span></span>                                                                                                                    |
| <span data-ttu-id="47490-280">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47490-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="47490-281">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="47490-281">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="47490-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47490-282">Range-Lower</span></span>            | <span data-ttu-id="47490-283">1</span><span class="sxs-lookup"><span data-stu-id="47490-283">1</span></span>                                                                                                                       |
| <span data-ttu-id="47490-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47490-284">Range-Upper</span></span>            | <span data-ttu-id="47490-285">255</span><span class="sxs-lookup"><span data-stu-id="47490-285">255</span></span>                                                                                                                     |
| <span data-ttu-id="47490-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47490-286">Search-Flags</span></span>           | <span data-ttu-id="47490-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47490-287">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="47490-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47490-288">System-Flags</span></span>           | <span data-ttu-id="47490-289">0x00000012</span><span class="sxs-lookup"><span data-stu-id="47490-289">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="47490-290">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="47490-290">Classes used in</span></span>        | [<span data-ttu-id="47490-291">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="47490-291">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="47490-292">**DNS-Zone**</span><span class="sxs-lookup"><span data-stu-id="47490-292">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="47490-293">**Domain**</span><span class="sxs-lookup"><span data-stu-id="47490-293">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="47490-294">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="47490-294">Windows Server 2012</span></span>



| <span data-ttu-id="47490-295">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47490-295">Entry</span></span> | <span data-ttu-id="47490-296">Wert</span><span class="sxs-lookup"><span data-stu-id="47490-296">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47490-297">Link-ID</span><span class="sxs-lookup"><span data-stu-id="47490-297">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="47490-298">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47490-298">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="47490-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="47490-299">System-Only</span></span>            | <span data-ttu-id="47490-300">False</span><span class="sxs-lookup"><span data-stu-id="47490-300">False</span></span>                                                                                                                   |
| <span data-ttu-id="47490-301">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="47490-301">Is-Single-Valued</span></span>       | <span data-ttu-id="47490-302">Richtig</span><span class="sxs-lookup"><span data-stu-id="47490-302">True</span></span>                                                                                                                    |
| <span data-ttu-id="47490-303">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="47490-303">Is Indexed</span></span>             | <span data-ttu-id="47490-304">False</span><span class="sxs-lookup"><span data-stu-id="47490-304">False</span></span>                                                                                                                   |
| <span data-ttu-id="47490-305">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="47490-305">In Global Catalog</span></span>      | <span data-ttu-id="47490-306">Richtig</span><span class="sxs-lookup"><span data-stu-id="47490-306">True</span></span>                                                                                                                    |
| <span data-ttu-id="47490-307">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47490-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="47490-308">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="47490-308">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="47490-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47490-309">Range-Lower</span></span>            | <span data-ttu-id="47490-310">1</span><span class="sxs-lookup"><span data-stu-id="47490-310">1</span></span>                                                                                                                       |
| <span data-ttu-id="47490-311">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47490-311">Range-Upper</span></span>            | <span data-ttu-id="47490-312">255</span><span class="sxs-lookup"><span data-stu-id="47490-312">255</span></span>                                                                                                                     |
| <span data-ttu-id="47490-313">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47490-313">Search-Flags</span></span>           | <span data-ttu-id="47490-314">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47490-314">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="47490-315">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47490-315">System-Flags</span></span>           | <span data-ttu-id="47490-316">0x00000012</span><span class="sxs-lookup"><span data-stu-id="47490-316">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="47490-317">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="47490-317">Classes used in</span></span>        | [<span data-ttu-id="47490-318">**DNS-Knoten**</span><span class="sxs-lookup"><span data-stu-id="47490-318">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="47490-319">**DNS-Zone**</span><span class="sxs-lookup"><span data-stu-id="47490-319">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="47490-320">**Domain**</span><span class="sxs-lookup"><span data-stu-id="47490-320">**Domain**</span></span>](c-domain.md)<br/> |



 

 





