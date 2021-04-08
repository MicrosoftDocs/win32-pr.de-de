---
title: MSMQ-Site-Gates-Attribut
description: Die Liste der DNS für MSMQ-Routing Server, über die der gesamte Datenverkehr Zwischenstand Orten weitergeleitet werden muss.
ms.assetid: 4c00553e-6439-4fad-974c-3bfbb61d8f2d
ms.tgt_platform: multiple
keywords:
- AD-Schema des MSMQ-Site-Gates-Attributs
- AD-Schema des msmqsitegates-Attributs
topic_type:
- apiref
api_name:
- MSMQ-Site-Gates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b970c979bb34ef0854755e042b6d36457c999be0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859646"
---
# <a name="msmq-site-gates-attribute"></a><span data-ttu-id="da8c6-105">MSMQ-Site-Gates-Attribut</span><span class="sxs-lookup"><span data-stu-id="da8c6-105">MSMQ-Site-Gates attribute</span></span>

<span data-ttu-id="da8c6-106">Die Liste der DNS für MSMQ-Routing Server, über die der gesamte Datenverkehr Zwischenstand Orten weitergeleitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="da8c6-106">The list of DNs for MSMQ routing servers, through which all traffic between sites must be routed.</span></span>



| <span data-ttu-id="da8c6-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da8c6-107">Entry</span></span> | <span data-ttu-id="da8c6-108">Wert</span><span class="sxs-lookup"><span data-stu-id="da8c6-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="da8c6-109">CN</span><span class="sxs-lookup"><span data-stu-id="da8c6-109">CN</span></span>                | <span data-ttu-id="da8c6-110">MSMQ-Site-Gates</span><span class="sxs-lookup"><span data-stu-id="da8c6-110">MSMQ-Site-Gates</span></span>                         |
| <span data-ttu-id="da8c6-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="da8c6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="da8c6-112">msmqsitegates</span><span class="sxs-lookup"><span data-stu-id="da8c6-112">mSMQSiteGates</span></span>                           |
| <span data-ttu-id="da8c6-113">Size</span><span class="sxs-lookup"><span data-stu-id="da8c6-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="da8c6-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="da8c6-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="da8c6-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="da8c6-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="da8c6-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="da8c6-116">Attribute-Id</span></span>      | <span data-ttu-id="da8c6-117">1.2.840.113556.1.4.945</span><span class="sxs-lookup"><span data-stu-id="da8c6-117">1.2.840.113556.1.4.945</span></span>                  |
| <span data-ttu-id="da8c6-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="da8c6-118">System-Id-Guid</span></span>    | <span data-ttu-id="da8c6-119">9a0dc339-C100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="da8c6-119">9a0dc339-c100-11d1-bbc5-0080c76670c0</span></span>    |
| <span data-ttu-id="da8c6-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="da8c6-120">Syntax</span></span>            | [<span data-ttu-id="da8c6-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="da8c6-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="da8c6-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="da8c6-122">Implementations</span></span>

-   [<span data-ttu-id="da8c6-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="da8c6-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="da8c6-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="da8c6-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="da8c6-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="da8c6-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="da8c6-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="da8c6-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="da8c6-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="da8c6-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="da8c6-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="da8c6-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="da8c6-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="da8c6-129">Windows 2000 Server</span></span>



| <span data-ttu-id="da8c6-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da8c6-130">Entry</span></span> | <span data-ttu-id="da8c6-131">Wert</span><span class="sxs-lookup"><span data-stu-id="da8c6-131">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="da8c6-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da8c6-132">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="da8c6-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da8c6-133">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="da8c6-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="da8c6-134">System-Only</span></span>            | <span data-ttu-id="da8c6-135">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-135">False</span></span>                                               |
| <span data-ttu-id="da8c6-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da8c6-136">Is-Single-Valued</span></span>       | <span data-ttu-id="da8c6-137">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-137">False</span></span>                                               |
| <span data-ttu-id="da8c6-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da8c6-138">Is Indexed</span></span>             | <span data-ttu-id="da8c6-139">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-139">False</span></span>                                               |
| <span data-ttu-id="da8c6-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da8c6-140">In Global Catalog</span></span>      | <span data-ttu-id="da8c6-141">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-141">False</span></span>                                               |
| <span data-ttu-id="da8c6-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da8c6-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="da8c6-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da8c6-143">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="da8c6-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da8c6-144">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="da8c6-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da8c6-145">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="da8c6-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da8c6-146">Search-Flags</span></span>           | <span data-ttu-id="da8c6-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da8c6-147">0x00000000</span></span>                                          |
| <span data-ttu-id="da8c6-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da8c6-148">System-Flags</span></span>           | <span data-ttu-id="da8c6-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da8c6-149">0x00000010</span></span>                                          |
| <span data-ttu-id="da8c6-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da8c6-150">Classes used in</span></span>        | [<span data-ttu-id="da8c6-151">**MSMQ-Site-Link**</span><span class="sxs-lookup"><span data-stu-id="da8c6-151">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="da8c6-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="da8c6-152">Windows Server 2003</span></span>



| <span data-ttu-id="da8c6-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da8c6-153">Entry</span></span> | <span data-ttu-id="da8c6-154">Wert</span><span class="sxs-lookup"><span data-stu-id="da8c6-154">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="da8c6-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da8c6-155">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="da8c6-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da8c6-156">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="da8c6-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="da8c6-157">System-Only</span></span>            | <span data-ttu-id="da8c6-158">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-158">False</span></span>                                               |
| <span data-ttu-id="da8c6-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da8c6-159">Is-Single-Valued</span></span>       | <span data-ttu-id="da8c6-160">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-160">False</span></span>                                               |
| <span data-ttu-id="da8c6-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da8c6-161">Is Indexed</span></span>             | <span data-ttu-id="da8c6-162">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-162">False</span></span>                                               |
| <span data-ttu-id="da8c6-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da8c6-163">In Global Catalog</span></span>      | <span data-ttu-id="da8c6-164">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-164">False</span></span>                                               |
| <span data-ttu-id="da8c6-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da8c6-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="da8c6-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da8c6-166">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="da8c6-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da8c6-167">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="da8c6-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da8c6-168">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="da8c6-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da8c6-169">Search-Flags</span></span>           | <span data-ttu-id="da8c6-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da8c6-170">0x00000000</span></span>                                          |
| <span data-ttu-id="da8c6-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da8c6-171">System-Flags</span></span>           | <span data-ttu-id="da8c6-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da8c6-172">0x00000010</span></span>                                          |
| <span data-ttu-id="da8c6-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da8c6-173">Classes used in</span></span>        | [<span data-ttu-id="da8c6-174">**MSMQ-Site-Link**</span><span class="sxs-lookup"><span data-stu-id="da8c6-174">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="da8c6-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="da8c6-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="da8c6-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da8c6-176">Entry</span></span> | <span data-ttu-id="da8c6-177">Wert</span><span class="sxs-lookup"><span data-stu-id="da8c6-177">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="da8c6-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da8c6-178">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="da8c6-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da8c6-179">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="da8c6-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="da8c6-180">System-Only</span></span>            | <span data-ttu-id="da8c6-181">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-181">False</span></span>                                               |
| <span data-ttu-id="da8c6-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da8c6-182">Is-Single-Valued</span></span>       | <span data-ttu-id="da8c6-183">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-183">False</span></span>                                               |
| <span data-ttu-id="da8c6-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da8c6-184">Is Indexed</span></span>             | <span data-ttu-id="da8c6-185">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-185">False</span></span>                                               |
| <span data-ttu-id="da8c6-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da8c6-186">In Global Catalog</span></span>      | <span data-ttu-id="da8c6-187">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-187">False</span></span>                                               |
| <span data-ttu-id="da8c6-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da8c6-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="da8c6-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da8c6-189">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="da8c6-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da8c6-190">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="da8c6-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da8c6-191">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="da8c6-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da8c6-192">Search-Flags</span></span>           | <span data-ttu-id="da8c6-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da8c6-193">0x00000000</span></span>                                          |
| <span data-ttu-id="da8c6-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da8c6-194">System-Flags</span></span>           | <span data-ttu-id="da8c6-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da8c6-195">0x00000010</span></span>                                          |
| <span data-ttu-id="da8c6-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da8c6-196">Classes used in</span></span>        | [<span data-ttu-id="da8c6-197">**MSMQ-Site-Link**</span><span class="sxs-lookup"><span data-stu-id="da8c6-197">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="da8c6-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da8c6-198">Windows Server 2008</span></span>



| <span data-ttu-id="da8c6-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da8c6-199">Entry</span></span> | <span data-ttu-id="da8c6-200">Wert</span><span class="sxs-lookup"><span data-stu-id="da8c6-200">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="da8c6-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da8c6-201">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="da8c6-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da8c6-202">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="da8c6-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="da8c6-203">System-Only</span></span>            | <span data-ttu-id="da8c6-204">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-204">False</span></span>                                               |
| <span data-ttu-id="da8c6-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da8c6-205">Is-Single-Valued</span></span>       | <span data-ttu-id="da8c6-206">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-206">False</span></span>                                               |
| <span data-ttu-id="da8c6-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da8c6-207">Is Indexed</span></span>             | <span data-ttu-id="da8c6-208">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-208">False</span></span>                                               |
| <span data-ttu-id="da8c6-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da8c6-209">In Global Catalog</span></span>      | <span data-ttu-id="da8c6-210">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-210">False</span></span>                                               |
| <span data-ttu-id="da8c6-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da8c6-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="da8c6-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da8c6-212">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="da8c6-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da8c6-213">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="da8c6-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da8c6-214">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="da8c6-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da8c6-215">Search-Flags</span></span>           | <span data-ttu-id="da8c6-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da8c6-216">0x00000000</span></span>                                          |
| <span data-ttu-id="da8c6-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da8c6-217">System-Flags</span></span>           | <span data-ttu-id="da8c6-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da8c6-218">0x00000010</span></span>                                          |
| <span data-ttu-id="da8c6-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da8c6-219">Classes used in</span></span>        | [<span data-ttu-id="da8c6-220">**MSMQ-Site-Link**</span><span class="sxs-lookup"><span data-stu-id="da8c6-220">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="da8c6-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="da8c6-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="da8c6-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da8c6-222">Entry</span></span> | <span data-ttu-id="da8c6-223">Wert</span><span class="sxs-lookup"><span data-stu-id="da8c6-223">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="da8c6-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da8c6-224">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="da8c6-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da8c6-225">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="da8c6-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="da8c6-226">System-Only</span></span>            | <span data-ttu-id="da8c6-227">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-227">False</span></span>                                               |
| <span data-ttu-id="da8c6-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da8c6-228">Is-Single-Valued</span></span>       | <span data-ttu-id="da8c6-229">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-229">False</span></span>                                               |
| <span data-ttu-id="da8c6-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da8c6-230">Is Indexed</span></span>             | <span data-ttu-id="da8c6-231">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-231">False</span></span>                                               |
| <span data-ttu-id="da8c6-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da8c6-232">In Global Catalog</span></span>      | <span data-ttu-id="da8c6-233">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-233">False</span></span>                                               |
| <span data-ttu-id="da8c6-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da8c6-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="da8c6-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da8c6-235">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="da8c6-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da8c6-236">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="da8c6-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da8c6-237">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="da8c6-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da8c6-238">Search-Flags</span></span>           | <span data-ttu-id="da8c6-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da8c6-239">0x00000000</span></span>                                          |
| <span data-ttu-id="da8c6-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da8c6-240">System-Flags</span></span>           | <span data-ttu-id="da8c6-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da8c6-241">0x00000010</span></span>                                          |
| <span data-ttu-id="da8c6-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da8c6-242">Classes used in</span></span>        | [<span data-ttu-id="da8c6-243">**MSMQ-Site-Link**</span><span class="sxs-lookup"><span data-stu-id="da8c6-243">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="da8c6-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="da8c6-244">Windows Server 2012</span></span>



| <span data-ttu-id="da8c6-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da8c6-245">Entry</span></span> | <span data-ttu-id="da8c6-246">Wert</span><span class="sxs-lookup"><span data-stu-id="da8c6-246">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="da8c6-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da8c6-247">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="da8c6-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da8c6-248">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="da8c6-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="da8c6-249">System-Only</span></span>            | <span data-ttu-id="da8c6-250">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-250">False</span></span>                                               |
| <span data-ttu-id="da8c6-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da8c6-251">Is-Single-Valued</span></span>       | <span data-ttu-id="da8c6-252">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-252">False</span></span>                                               |
| <span data-ttu-id="da8c6-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da8c6-253">Is Indexed</span></span>             | <span data-ttu-id="da8c6-254">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-254">False</span></span>                                               |
| <span data-ttu-id="da8c6-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da8c6-255">In Global Catalog</span></span>      | <span data-ttu-id="da8c6-256">False</span><span class="sxs-lookup"><span data-stu-id="da8c6-256">False</span></span>                                               |
| <span data-ttu-id="da8c6-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da8c6-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="da8c6-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da8c6-258">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="da8c6-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da8c6-259">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="da8c6-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da8c6-260">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="da8c6-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da8c6-261">Search-Flags</span></span>           | <span data-ttu-id="da8c6-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da8c6-262">0x00000000</span></span>                                          |
| <span data-ttu-id="da8c6-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da8c6-263">System-Flags</span></span>           | <span data-ttu-id="da8c6-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da8c6-264">0x00000010</span></span>                                          |
| <span data-ttu-id="da8c6-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da8c6-265">Classes used in</span></span>        | [<span data-ttu-id="da8c6-266">**MSMQ-Site-Link**</span><span class="sxs-lookup"><span data-stu-id="da8c6-266">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



 

 





