---
title: Dns-Root-Attribut
description: Der oberste DNS-Domänen Name, der einer Domäne/Verzeichnis Partition zugewiesen ist.
ms.assetid: 0b33daad-b5c5-4126-86fa-abd3e0006c5f
ms.tgt_platform: multiple
keywords:
- AD-Schema für Dns-Root-Attribut
- dnsRoot-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Dns-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2c2fd2c39e8f0015d7641eccd27279b3478ec4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344525"
---
# <a name="dns-root-attribute"></a><span data-ttu-id="9bdf2-105">Dns-Root-Attribut</span><span class="sxs-lookup"><span data-stu-id="9bdf2-105">Dns-Root attribute</span></span>

<span data-ttu-id="9bdf2-106">Der oberste DNS-Domänen Name, der einer Domäne/Verzeichnis Partition zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9bdf2-106">The uppermost DNS domain name assigned to a domain/directory partition.</span></span> <span data-ttu-id="9bdf2-107">Dies wird für ein CrossRef-Objekt festgelegt und wird unter anderem für die Verweis Generierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9bdf2-107">This is set on a crossRef object and is used, among other things, for referral generation.</span></span> <span data-ttu-id="9bdf2-108">Beim Durchsuchen einer gesamten Domänen Struktur muss die Suche beim Dns-Root-Objekt initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="9bdf2-108">When searching through an entire domain tree, the search must be initiated at the Dns-Root object.</span></span> <span data-ttu-id="9bdf2-109">Dieses Attribut kann mehr wertig sein. in diesem Fall werden mehrere Verweise generiert.</span><span class="sxs-lookup"><span data-stu-id="9bdf2-109">This attribute can be multi-valued, in which case multiple referrals are generated.</span></span>



| <span data-ttu-id="9bdf2-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9bdf2-110">Entry</span></span> | <span data-ttu-id="9bdf2-111">Wert</span><span class="sxs-lookup"><span data-stu-id="9bdf2-111">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9bdf2-112">CN</span><span class="sxs-lookup"><span data-stu-id="9bdf2-112">CN</span></span>                | <span data-ttu-id="9bdf2-113">Dns-Root</span><span class="sxs-lookup"><span data-stu-id="9bdf2-113">Dns-Root</span></span>                                    |
| <span data-ttu-id="9bdf2-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9bdf2-114">Ldap-Display-Name</span></span> | <span data-ttu-id="9bdf2-115">dnsRoot</span><span class="sxs-lookup"><span data-stu-id="9bdf2-115">dnsRoot</span></span>                                     |
| <span data-ttu-id="9bdf2-116">Size</span><span class="sxs-lookup"><span data-stu-id="9bdf2-116">Size</span></span>              | \-                                          |
| <span data-ttu-id="9bdf2-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="9bdf2-117">Update Privilege</span></span>  | <span data-ttu-id="9bdf2-118">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9bdf2-118">This value is set by the system.</span></span>            |
| <span data-ttu-id="9bdf2-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="9bdf2-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="9bdf2-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9bdf2-120">Attribute-Id</span></span>      | <span data-ttu-id="9bdf2-121">1.2.840.113556.1.4.28</span><span class="sxs-lookup"><span data-stu-id="9bdf2-121">1.2.840.113556.1.4.28</span></span>                       |
| <span data-ttu-id="9bdf2-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9bdf2-122">System-Id-Guid</span></span>    | <span data-ttu-id="9bdf2-123">bf967959-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9bdf2-123">bf967959-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="9bdf2-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bdf2-124">Syntax</span></span>            | [<span data-ttu-id="9bdf2-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9bdf2-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9bdf2-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="9bdf2-126">Implementations</span></span>

-   [<span data-ttu-id="9bdf2-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9bdf2-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9bdf2-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9bdf2-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9bdf2-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="9bdf2-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9bdf2-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9bdf2-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9bdf2-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9bdf2-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9bdf2-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9bdf2-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9bdf2-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9bdf2-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9bdf2-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9bdf2-134">Windows 2000 Server</span></span>



| <span data-ttu-id="9bdf2-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9bdf2-135">Entry</span></span> | <span data-ttu-id="9bdf2-136">Wert</span><span class="sxs-lookup"><span data-stu-id="9bdf2-136">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="9bdf2-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9bdf2-137">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="9bdf2-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9bdf2-138">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="9bdf2-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="9bdf2-139">System-Only</span></span>            | <span data-ttu-id="9bdf2-140">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-140">False</span></span>                                      |
| <span data-ttu-id="9bdf2-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9bdf2-141">Is-Single-Valued</span></span>       | <span data-ttu-id="9bdf2-142">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-142">False</span></span>                                      |
| <span data-ttu-id="9bdf2-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9bdf2-143">Is Indexed</span></span>             | <span data-ttu-id="9bdf2-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="9bdf2-144">True</span></span>                                       |
| <span data-ttu-id="9bdf2-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9bdf2-145">In Global Catalog</span></span>      | <span data-ttu-id="9bdf2-146">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-146">False</span></span>                                      |
| <span data-ttu-id="9bdf2-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9bdf2-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="9bdf2-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9bdf2-148">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="9bdf2-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9bdf2-149">Range-Lower</span></span>            | <span data-ttu-id="9bdf2-150">1</span><span class="sxs-lookup"><span data-stu-id="9bdf2-150">1</span></span>                                          |
| <span data-ttu-id="9bdf2-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9bdf2-151">Range-Upper</span></span>            | <span data-ttu-id="9bdf2-152">255</span><span class="sxs-lookup"><span data-stu-id="9bdf2-152">255</span></span>                                        |
| <span data-ttu-id="9bdf2-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9bdf2-153">Search-Flags</span></span>           | <span data-ttu-id="9bdf2-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9bdf2-154">0x00000001</span></span>                                 |
| <span data-ttu-id="9bdf2-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9bdf2-155">System-Flags</span></span>           | <span data-ttu-id="9bdf2-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9bdf2-156">0x00000010</span></span>                                 |
| <span data-ttu-id="9bdf2-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9bdf2-157">Classes used in</span></span>        | [<span data-ttu-id="9bdf2-158">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="9bdf2-158">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9bdf2-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9bdf2-159">Windows Server 2003</span></span>



| <span data-ttu-id="9bdf2-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9bdf2-160">Entry</span></span> | <span data-ttu-id="9bdf2-161">Wert</span><span class="sxs-lookup"><span data-stu-id="9bdf2-161">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="9bdf2-162">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9bdf2-162">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="9bdf2-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9bdf2-163">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="9bdf2-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="9bdf2-164">System-Only</span></span>            | <span data-ttu-id="9bdf2-165">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-165">False</span></span>                                      |
| <span data-ttu-id="9bdf2-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9bdf2-166">Is-Single-Valued</span></span>       | <span data-ttu-id="9bdf2-167">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-167">False</span></span>                                      |
| <span data-ttu-id="9bdf2-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9bdf2-168">Is Indexed</span></span>             | <span data-ttu-id="9bdf2-169">Richtig</span><span class="sxs-lookup"><span data-stu-id="9bdf2-169">True</span></span>                                       |
| <span data-ttu-id="9bdf2-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9bdf2-170">In Global Catalog</span></span>      | <span data-ttu-id="9bdf2-171">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-171">False</span></span>                                      |
| <span data-ttu-id="9bdf2-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9bdf2-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="9bdf2-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9bdf2-173">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="9bdf2-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9bdf2-174">Range-Lower</span></span>            | <span data-ttu-id="9bdf2-175">1</span><span class="sxs-lookup"><span data-stu-id="9bdf2-175">1</span></span>                                          |
| <span data-ttu-id="9bdf2-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9bdf2-176">Range-Upper</span></span>            | <span data-ttu-id="9bdf2-177">255</span><span class="sxs-lookup"><span data-stu-id="9bdf2-177">255</span></span>                                        |
| <span data-ttu-id="9bdf2-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9bdf2-178">Search-Flags</span></span>           | <span data-ttu-id="9bdf2-179">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9bdf2-179">0x00000001</span></span>                                 |
| <span data-ttu-id="9bdf2-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9bdf2-180">System-Flags</span></span>           | <span data-ttu-id="9bdf2-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9bdf2-181">0x00000010</span></span>                                 |
| <span data-ttu-id="9bdf2-182">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9bdf2-182">Classes used in</span></span>        | [<span data-ttu-id="9bdf2-183">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="9bdf2-183">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9bdf2-184">Adam</span><span class="sxs-lookup"><span data-stu-id="9bdf2-184">ADAM</span></span>



| <span data-ttu-id="9bdf2-185">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9bdf2-185">Entry</span></span> | <span data-ttu-id="9bdf2-186">Wert</span><span class="sxs-lookup"><span data-stu-id="9bdf2-186">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="9bdf2-187">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9bdf2-187">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="9bdf2-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9bdf2-188">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="9bdf2-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="9bdf2-189">System-Only</span></span>            | <span data-ttu-id="9bdf2-190">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-190">False</span></span>                                      |
| <span data-ttu-id="9bdf2-191">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9bdf2-191">Is-Single-Valued</span></span>       | <span data-ttu-id="9bdf2-192">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-192">False</span></span>                                      |
| <span data-ttu-id="9bdf2-193">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9bdf2-193">Is Indexed</span></span>             | <span data-ttu-id="9bdf2-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="9bdf2-194">True</span></span>                                       |
| <span data-ttu-id="9bdf2-195">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9bdf2-195">In Global Catalog</span></span>      | <span data-ttu-id="9bdf2-196">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-196">False</span></span>                                      |
| <span data-ttu-id="9bdf2-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9bdf2-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="9bdf2-198">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9bdf2-198">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="9bdf2-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9bdf2-199">Range-Lower</span></span>            | <span data-ttu-id="9bdf2-200">1</span><span class="sxs-lookup"><span data-stu-id="9bdf2-200">1</span></span>                                          |
| <span data-ttu-id="9bdf2-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9bdf2-201">Range-Upper</span></span>            | <span data-ttu-id="9bdf2-202">255</span><span class="sxs-lookup"><span data-stu-id="9bdf2-202">255</span></span>                                        |
| <span data-ttu-id="9bdf2-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9bdf2-203">Search-Flags</span></span>           | <span data-ttu-id="9bdf2-204">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9bdf2-204">0x00000001</span></span>                                 |
| <span data-ttu-id="9bdf2-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9bdf2-205">System-Flags</span></span>           | <span data-ttu-id="9bdf2-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9bdf2-206">0x00000010</span></span>                                 |
| <span data-ttu-id="9bdf2-207">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9bdf2-207">Classes used in</span></span>        | [<span data-ttu-id="9bdf2-208">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="9bdf2-208">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9bdf2-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9bdf2-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9bdf2-210">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9bdf2-210">Entry</span></span> | <span data-ttu-id="9bdf2-211">Wert</span><span class="sxs-lookup"><span data-stu-id="9bdf2-211">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="9bdf2-212">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9bdf2-212">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="9bdf2-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9bdf2-213">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="9bdf2-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="9bdf2-214">System-Only</span></span>            | <span data-ttu-id="9bdf2-215">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-215">False</span></span>                                      |
| <span data-ttu-id="9bdf2-216">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9bdf2-216">Is-Single-Valued</span></span>       | <span data-ttu-id="9bdf2-217">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-217">False</span></span>                                      |
| <span data-ttu-id="9bdf2-218">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9bdf2-218">Is Indexed</span></span>             | <span data-ttu-id="9bdf2-219">Richtig</span><span class="sxs-lookup"><span data-stu-id="9bdf2-219">True</span></span>                                       |
| <span data-ttu-id="9bdf2-220">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9bdf2-220">In Global Catalog</span></span>      | <span data-ttu-id="9bdf2-221">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-221">False</span></span>                                      |
| <span data-ttu-id="9bdf2-222">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9bdf2-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="9bdf2-223">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9bdf2-223">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="9bdf2-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9bdf2-224">Range-Lower</span></span>            | <span data-ttu-id="9bdf2-225">1</span><span class="sxs-lookup"><span data-stu-id="9bdf2-225">1</span></span>                                          |
| <span data-ttu-id="9bdf2-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9bdf2-226">Range-Upper</span></span>            | <span data-ttu-id="9bdf2-227">255</span><span class="sxs-lookup"><span data-stu-id="9bdf2-227">255</span></span>                                        |
| <span data-ttu-id="9bdf2-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9bdf2-228">Search-Flags</span></span>           | <span data-ttu-id="9bdf2-229">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9bdf2-229">0x00000001</span></span>                                 |
| <span data-ttu-id="9bdf2-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9bdf2-230">System-Flags</span></span>           | <span data-ttu-id="9bdf2-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9bdf2-231">0x00000010</span></span>                                 |
| <span data-ttu-id="9bdf2-232">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9bdf2-232">Classes used in</span></span>        | [<span data-ttu-id="9bdf2-233">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="9bdf2-233">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9bdf2-234">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9bdf2-234">Windows Server 2008</span></span>



| <span data-ttu-id="9bdf2-235">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9bdf2-235">Entry</span></span> | <span data-ttu-id="9bdf2-236">Wert</span><span class="sxs-lookup"><span data-stu-id="9bdf2-236">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="9bdf2-237">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9bdf2-237">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="9bdf2-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9bdf2-238">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="9bdf2-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="9bdf2-239">System-Only</span></span>            | <span data-ttu-id="9bdf2-240">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-240">False</span></span>                                      |
| <span data-ttu-id="9bdf2-241">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9bdf2-241">Is-Single-Valued</span></span>       | <span data-ttu-id="9bdf2-242">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-242">False</span></span>                                      |
| <span data-ttu-id="9bdf2-243">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9bdf2-243">Is Indexed</span></span>             | <span data-ttu-id="9bdf2-244">Richtig</span><span class="sxs-lookup"><span data-stu-id="9bdf2-244">True</span></span>                                       |
| <span data-ttu-id="9bdf2-245">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9bdf2-245">In Global Catalog</span></span>      | <span data-ttu-id="9bdf2-246">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-246">False</span></span>                                      |
| <span data-ttu-id="9bdf2-247">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9bdf2-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="9bdf2-248">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9bdf2-248">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="9bdf2-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9bdf2-249">Range-Lower</span></span>            | <span data-ttu-id="9bdf2-250">1</span><span class="sxs-lookup"><span data-stu-id="9bdf2-250">1</span></span>                                          |
| <span data-ttu-id="9bdf2-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9bdf2-251">Range-Upper</span></span>            | <span data-ttu-id="9bdf2-252">255</span><span class="sxs-lookup"><span data-stu-id="9bdf2-252">255</span></span>                                        |
| <span data-ttu-id="9bdf2-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9bdf2-253">Search-Flags</span></span>           | <span data-ttu-id="9bdf2-254">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9bdf2-254">0x00000001</span></span>                                 |
| <span data-ttu-id="9bdf2-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9bdf2-255">System-Flags</span></span>           | <span data-ttu-id="9bdf2-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9bdf2-256">0x00000010</span></span>                                 |
| <span data-ttu-id="9bdf2-257">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9bdf2-257">Classes used in</span></span>        | [<span data-ttu-id="9bdf2-258">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="9bdf2-258">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9bdf2-259">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9bdf2-259">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9bdf2-260">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9bdf2-260">Entry</span></span> | <span data-ttu-id="9bdf2-261">Wert</span><span class="sxs-lookup"><span data-stu-id="9bdf2-261">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="9bdf2-262">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9bdf2-262">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="9bdf2-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9bdf2-263">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="9bdf2-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="9bdf2-264">System-Only</span></span>            | <span data-ttu-id="9bdf2-265">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-265">False</span></span>                                      |
| <span data-ttu-id="9bdf2-266">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9bdf2-266">Is-Single-Valued</span></span>       | <span data-ttu-id="9bdf2-267">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-267">False</span></span>                                      |
| <span data-ttu-id="9bdf2-268">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9bdf2-268">Is Indexed</span></span>             | <span data-ttu-id="9bdf2-269">Richtig</span><span class="sxs-lookup"><span data-stu-id="9bdf2-269">True</span></span>                                       |
| <span data-ttu-id="9bdf2-270">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9bdf2-270">In Global Catalog</span></span>      | <span data-ttu-id="9bdf2-271">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-271">False</span></span>                                      |
| <span data-ttu-id="9bdf2-272">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9bdf2-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="9bdf2-273">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9bdf2-273">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="9bdf2-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9bdf2-274">Range-Lower</span></span>            | <span data-ttu-id="9bdf2-275">1</span><span class="sxs-lookup"><span data-stu-id="9bdf2-275">1</span></span>                                          |
| <span data-ttu-id="9bdf2-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9bdf2-276">Range-Upper</span></span>            | <span data-ttu-id="9bdf2-277">255</span><span class="sxs-lookup"><span data-stu-id="9bdf2-277">255</span></span>                                        |
| <span data-ttu-id="9bdf2-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9bdf2-278">Search-Flags</span></span>           | <span data-ttu-id="9bdf2-279">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9bdf2-279">0x00000001</span></span>                                 |
| <span data-ttu-id="9bdf2-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9bdf2-280">System-Flags</span></span>           | <span data-ttu-id="9bdf2-281">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9bdf2-281">0x00000010</span></span>                                 |
| <span data-ttu-id="9bdf2-282">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9bdf2-282">Classes used in</span></span>        | [<span data-ttu-id="9bdf2-283">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="9bdf2-283">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9bdf2-284">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9bdf2-284">Windows Server 2012</span></span>



| <span data-ttu-id="9bdf2-285">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9bdf2-285">Entry</span></span> | <span data-ttu-id="9bdf2-286">Wert</span><span class="sxs-lookup"><span data-stu-id="9bdf2-286">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="9bdf2-287">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9bdf2-287">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="9bdf2-288">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9bdf2-288">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="9bdf2-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="9bdf2-289">System-Only</span></span>            | <span data-ttu-id="9bdf2-290">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-290">False</span></span>                                      |
| <span data-ttu-id="9bdf2-291">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9bdf2-291">Is-Single-Valued</span></span>       | <span data-ttu-id="9bdf2-292">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-292">False</span></span>                                      |
| <span data-ttu-id="9bdf2-293">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9bdf2-293">Is Indexed</span></span>             | <span data-ttu-id="9bdf2-294">Richtig</span><span class="sxs-lookup"><span data-stu-id="9bdf2-294">True</span></span>                                       |
| <span data-ttu-id="9bdf2-295">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9bdf2-295">In Global Catalog</span></span>      | <span data-ttu-id="9bdf2-296">False</span><span class="sxs-lookup"><span data-stu-id="9bdf2-296">False</span></span>                                      |
| <span data-ttu-id="9bdf2-297">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9bdf2-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="9bdf2-298">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9bdf2-298">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="9bdf2-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9bdf2-299">Range-Lower</span></span>            | <span data-ttu-id="9bdf2-300">1</span><span class="sxs-lookup"><span data-stu-id="9bdf2-300">1</span></span>                                          |
| <span data-ttu-id="9bdf2-301">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9bdf2-301">Range-Upper</span></span>            | <span data-ttu-id="9bdf2-302">255</span><span class="sxs-lookup"><span data-stu-id="9bdf2-302">255</span></span>                                        |
| <span data-ttu-id="9bdf2-303">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9bdf2-303">Search-Flags</span></span>           | <span data-ttu-id="9bdf2-304">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9bdf2-304">0x00000001</span></span>                                 |
| <span data-ttu-id="9bdf2-305">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9bdf2-305">System-Flags</span></span>           | <span data-ttu-id="9bdf2-306">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9bdf2-306">0x00000010</span></span>                                 |
| <span data-ttu-id="9bdf2-307">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9bdf2-307">Classes used in</span></span>        | [<span data-ttu-id="9bdf2-308">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="9bdf2-308">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





