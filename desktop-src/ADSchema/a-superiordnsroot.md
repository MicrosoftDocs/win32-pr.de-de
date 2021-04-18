---
title: Superior-DNS-Root-Attribut
description: Hierbei handelt es sich um ein System Attribut, das für die Verweis Generierung verwendet wird.
ms.assetid: 421f8315-26e2-457d-ae76-868b7fc6551a
ms.tgt_platform: multiple
keywords:
- AD-Schema für das übergeordnete DNS-Root-Attribut
- "\"superiordnsroot\"-Attribut AD-Schema"
topic_type:
- apiref
api_name:
- Superior-DNS-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6561839cf5137968adbac628ad6046b8b86dab85
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344138"
---
# <a name="superior-dns-root-attribute"></a><span data-ttu-id="b5b0a-105">Superior-DNS-Root-Attribut</span><span class="sxs-lookup"><span data-stu-id="b5b0a-105">Superior-DNS-Root attribute</span></span>

<span data-ttu-id="b5b0a-106">Hierbei handelt es sich um ein System Attribut, das für die Verweis Generierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-106">This is a system attribute that is used for referrals generation.</span></span>



| <span data-ttu-id="b5b0a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5b0a-107">Entry</span></span> | <span data-ttu-id="b5b0a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="b5b0a-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b5b0a-109">CN</span><span class="sxs-lookup"><span data-stu-id="b5b0a-109">CN</span></span>                | <span data-ttu-id="b5b0a-110">Superior-DNS-Root</span><span class="sxs-lookup"><span data-stu-id="b5b0a-110">Superior-DNS-Root</span></span>                           |
| <span data-ttu-id="b5b0a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b5b0a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b5b0a-112">superiordnsroot</span><span class="sxs-lookup"><span data-stu-id="b5b0a-112">superiorDNSRoot</span></span>                             |
| <span data-ttu-id="b5b0a-113">Size</span><span class="sxs-lookup"><span data-stu-id="b5b0a-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="b5b0a-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b5b0a-114">Update Privilege</span></span>  | <span data-ttu-id="b5b0a-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="b5b0a-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b5b0a-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b5b0a-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b5b0a-117">Attribute-Id</span></span>      | <span data-ttu-id="b5b0a-118">1.2.840.113556.1.4.532</span><span class="sxs-lookup"><span data-stu-id="b5b0a-118">1.2.840.113556.1.4.532</span></span>                      |
| <span data-ttu-id="b5b0a-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b5b0a-119">System-Id-Guid</span></span>    | <span data-ttu-id="b5b0a-120">5245801d-ca6a-11D0-AFFF -0000f 80367c1</span><span class="sxs-lookup"><span data-stu-id="b5b0a-120">5245801d-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="b5b0a-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5b0a-121">Syntax</span></span>            | [<span data-ttu-id="b5b0a-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b5b0a-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b5b0a-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b5b0a-123">Implementations</span></span>

-   [<span data-ttu-id="b5b0a-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b5b0a-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b5b0a-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b5b0a-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b5b0a-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="b5b0a-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b5b0a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b5b0a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b5b0a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b5b0a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b5b0a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b5b0a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b5b0a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b5b0a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b5b0a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b5b0a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b5b0a-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5b0a-132">Entry</span></span> | <span data-ttu-id="b5b0a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="b5b0a-133">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="b5b0a-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b5b0a-134">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="b5b0a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5b0a-135">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="b5b0a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5b0a-136">System-Only</span></span>            | <span data-ttu-id="b5b0a-137">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-137">False</span></span>                                      |
| <span data-ttu-id="b5b0a-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b5b0a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b5b0a-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="b5b0a-139">True</span></span>                                       |
| <span data-ttu-id="b5b0a-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b5b0a-140">Is Indexed</span></span>             | <span data-ttu-id="b5b0a-141">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-141">False</span></span>                                      |
| <span data-ttu-id="b5b0a-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b5b0a-142">In Global Catalog</span></span>      | <span data-ttu-id="b5b0a-143">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-143">False</span></span>                                      |
| <span data-ttu-id="b5b0a-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b5b0a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5b0a-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b5b0a-145">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="b5b0a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5b0a-146">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="b5b0a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5b0a-147">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="b5b0a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5b0a-148">Search-Flags</span></span>           | <span data-ttu-id="b5b0a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5b0a-149">0x00000000</span></span>                                 |
| <span data-ttu-id="b5b0a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5b0a-150">System-Flags</span></span>           | <span data-ttu-id="b5b0a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5b0a-151">0x00000010</span></span>                                 |
| <span data-ttu-id="b5b0a-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b5b0a-152">Classes used in</span></span>        | [<span data-ttu-id="b5b0a-153">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="b5b0a-153">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b5b0a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b5b0a-154">Windows Server 2003</span></span>



| <span data-ttu-id="b5b0a-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5b0a-155">Entry</span></span> | <span data-ttu-id="b5b0a-156">Wert</span><span class="sxs-lookup"><span data-stu-id="b5b0a-156">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="b5b0a-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b5b0a-157">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="b5b0a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5b0a-158">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="b5b0a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5b0a-159">System-Only</span></span>            | <span data-ttu-id="b5b0a-160">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-160">False</span></span>                                      |
| <span data-ttu-id="b5b0a-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b5b0a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b5b0a-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="b5b0a-162">True</span></span>                                       |
| <span data-ttu-id="b5b0a-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b5b0a-163">Is Indexed</span></span>             | <span data-ttu-id="b5b0a-164">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-164">False</span></span>                                      |
| <span data-ttu-id="b5b0a-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b5b0a-165">In Global Catalog</span></span>      | <span data-ttu-id="b5b0a-166">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-166">False</span></span>                                      |
| <span data-ttu-id="b5b0a-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b5b0a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5b0a-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b5b0a-168">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="b5b0a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5b0a-169">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="b5b0a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5b0a-170">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="b5b0a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5b0a-171">Search-Flags</span></span>           | <span data-ttu-id="b5b0a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5b0a-172">0x00000000</span></span>                                 |
| <span data-ttu-id="b5b0a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5b0a-173">System-Flags</span></span>           | <span data-ttu-id="b5b0a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5b0a-174">0x00000010</span></span>                                 |
| <span data-ttu-id="b5b0a-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b5b0a-175">Classes used in</span></span>        | [<span data-ttu-id="b5b0a-176">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="b5b0a-176">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b5b0a-177">Adam</span><span class="sxs-lookup"><span data-stu-id="b5b0a-177">ADAM</span></span>



| <span data-ttu-id="b5b0a-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5b0a-178">Entry</span></span> | <span data-ttu-id="b5b0a-179">Wert</span><span class="sxs-lookup"><span data-stu-id="b5b0a-179">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="b5b0a-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b5b0a-180">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="b5b0a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5b0a-181">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="b5b0a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5b0a-182">System-Only</span></span>            | <span data-ttu-id="b5b0a-183">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-183">False</span></span>                                      |
| <span data-ttu-id="b5b0a-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b5b0a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b5b0a-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="b5b0a-185">True</span></span>                                       |
| <span data-ttu-id="b5b0a-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b5b0a-186">Is Indexed</span></span>             | <span data-ttu-id="b5b0a-187">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-187">False</span></span>                                      |
| <span data-ttu-id="b5b0a-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b5b0a-188">In Global Catalog</span></span>      | <span data-ttu-id="b5b0a-189">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-189">False</span></span>                                      |
| <span data-ttu-id="b5b0a-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b5b0a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5b0a-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b5b0a-191">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="b5b0a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5b0a-192">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="b5b0a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5b0a-193">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="b5b0a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5b0a-194">Search-Flags</span></span>           | <span data-ttu-id="b5b0a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5b0a-195">0x00000000</span></span>                                 |
| <span data-ttu-id="b5b0a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5b0a-196">System-Flags</span></span>           | <span data-ttu-id="b5b0a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5b0a-197">0x00000010</span></span>                                 |
| <span data-ttu-id="b5b0a-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b5b0a-198">Classes used in</span></span>        | [<span data-ttu-id="b5b0a-199">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="b5b0a-199">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b5b0a-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b5b0a-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b5b0a-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5b0a-201">Entry</span></span> | <span data-ttu-id="b5b0a-202">Wert</span><span class="sxs-lookup"><span data-stu-id="b5b0a-202">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="b5b0a-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b5b0a-203">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="b5b0a-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5b0a-204">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="b5b0a-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5b0a-205">System-Only</span></span>            | <span data-ttu-id="b5b0a-206">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-206">False</span></span>                                      |
| <span data-ttu-id="b5b0a-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b5b0a-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b5b0a-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="b5b0a-208">True</span></span>                                       |
| <span data-ttu-id="b5b0a-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b5b0a-209">Is Indexed</span></span>             | <span data-ttu-id="b5b0a-210">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-210">False</span></span>                                      |
| <span data-ttu-id="b5b0a-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b5b0a-211">In Global Catalog</span></span>      | <span data-ttu-id="b5b0a-212">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-212">False</span></span>                                      |
| <span data-ttu-id="b5b0a-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b5b0a-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5b0a-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b5b0a-214">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="b5b0a-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5b0a-215">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="b5b0a-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5b0a-216">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="b5b0a-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5b0a-217">Search-Flags</span></span>           | <span data-ttu-id="b5b0a-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5b0a-218">0x00000000</span></span>                                 |
| <span data-ttu-id="b5b0a-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5b0a-219">System-Flags</span></span>           | <span data-ttu-id="b5b0a-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5b0a-220">0x00000010</span></span>                                 |
| <span data-ttu-id="b5b0a-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b5b0a-221">Classes used in</span></span>        | [<span data-ttu-id="b5b0a-222">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="b5b0a-222">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b5b0a-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5b0a-223">Windows Server 2008</span></span>



| <span data-ttu-id="b5b0a-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5b0a-224">Entry</span></span> | <span data-ttu-id="b5b0a-225">Wert</span><span class="sxs-lookup"><span data-stu-id="b5b0a-225">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="b5b0a-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b5b0a-226">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="b5b0a-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5b0a-227">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="b5b0a-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5b0a-228">System-Only</span></span>            | <span data-ttu-id="b5b0a-229">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-229">False</span></span>                                      |
| <span data-ttu-id="b5b0a-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b5b0a-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b5b0a-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="b5b0a-231">True</span></span>                                       |
| <span data-ttu-id="b5b0a-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b5b0a-232">Is Indexed</span></span>             | <span data-ttu-id="b5b0a-233">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-233">False</span></span>                                      |
| <span data-ttu-id="b5b0a-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b5b0a-234">In Global Catalog</span></span>      | <span data-ttu-id="b5b0a-235">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-235">False</span></span>                                      |
| <span data-ttu-id="b5b0a-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b5b0a-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5b0a-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b5b0a-237">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="b5b0a-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5b0a-238">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="b5b0a-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5b0a-239">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="b5b0a-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5b0a-240">Search-Flags</span></span>           | <span data-ttu-id="b5b0a-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5b0a-241">0x00000000</span></span>                                 |
| <span data-ttu-id="b5b0a-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5b0a-242">System-Flags</span></span>           | <span data-ttu-id="b5b0a-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5b0a-243">0x00000010</span></span>                                 |
| <span data-ttu-id="b5b0a-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b5b0a-244">Classes used in</span></span>        | [<span data-ttu-id="b5b0a-245">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="b5b0a-245">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b5b0a-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b5b0a-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b5b0a-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5b0a-247">Entry</span></span> | <span data-ttu-id="b5b0a-248">Wert</span><span class="sxs-lookup"><span data-stu-id="b5b0a-248">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="b5b0a-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b5b0a-249">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="b5b0a-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5b0a-250">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="b5b0a-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5b0a-251">System-Only</span></span>            | <span data-ttu-id="b5b0a-252">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-252">False</span></span>                                      |
| <span data-ttu-id="b5b0a-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b5b0a-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b5b0a-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="b5b0a-254">True</span></span>                                       |
| <span data-ttu-id="b5b0a-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b5b0a-255">Is Indexed</span></span>             | <span data-ttu-id="b5b0a-256">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-256">False</span></span>                                      |
| <span data-ttu-id="b5b0a-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b5b0a-257">In Global Catalog</span></span>      | <span data-ttu-id="b5b0a-258">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-258">False</span></span>                                      |
| <span data-ttu-id="b5b0a-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b5b0a-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5b0a-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b5b0a-260">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="b5b0a-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5b0a-261">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="b5b0a-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5b0a-262">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="b5b0a-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5b0a-263">Search-Flags</span></span>           | <span data-ttu-id="b5b0a-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5b0a-264">0x00000000</span></span>                                 |
| <span data-ttu-id="b5b0a-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5b0a-265">System-Flags</span></span>           | <span data-ttu-id="b5b0a-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5b0a-266">0x00000010</span></span>                                 |
| <span data-ttu-id="b5b0a-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b5b0a-267">Classes used in</span></span>        | [<span data-ttu-id="b5b0a-268">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="b5b0a-268">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b5b0a-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b5b0a-269">Windows Server 2012</span></span>



| <span data-ttu-id="b5b0a-270">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5b0a-270">Entry</span></span> | <span data-ttu-id="b5b0a-271">Wert</span><span class="sxs-lookup"><span data-stu-id="b5b0a-271">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="b5b0a-272">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b5b0a-272">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="b5b0a-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5b0a-273">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="b5b0a-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5b0a-274">System-Only</span></span>            | <span data-ttu-id="b5b0a-275">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-275">False</span></span>                                      |
| <span data-ttu-id="b5b0a-276">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b5b0a-276">Is-Single-Valued</span></span>       | <span data-ttu-id="b5b0a-277">Richtig</span><span class="sxs-lookup"><span data-stu-id="b5b0a-277">True</span></span>                                       |
| <span data-ttu-id="b5b0a-278">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b5b0a-278">Is Indexed</span></span>             | <span data-ttu-id="b5b0a-279">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-279">False</span></span>                                      |
| <span data-ttu-id="b5b0a-280">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b5b0a-280">In Global Catalog</span></span>      | <span data-ttu-id="b5b0a-281">False</span><span class="sxs-lookup"><span data-stu-id="b5b0a-281">False</span></span>                                      |
| <span data-ttu-id="b5b0a-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b5b0a-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5b0a-283">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b5b0a-283">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="b5b0a-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5b0a-284">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="b5b0a-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5b0a-285">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="b5b0a-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5b0a-286">Search-Flags</span></span>           | <span data-ttu-id="b5b0a-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5b0a-287">0x00000000</span></span>                                 |
| <span data-ttu-id="b5b0a-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5b0a-288">System-Flags</span></span>           | <span data-ttu-id="b5b0a-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5b0a-289">0x00000010</span></span>                                 |
| <span data-ttu-id="b5b0a-290">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b5b0a-290">Classes used in</span></span>        | [<span data-ttu-id="b5b0a-291">**Kreuz Verweis**</span><span class="sxs-lookup"><span data-stu-id="b5b0a-291">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





