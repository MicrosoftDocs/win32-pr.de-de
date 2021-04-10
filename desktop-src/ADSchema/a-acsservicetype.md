---
title: ACS-Service Type-Attribut
description: Der ACS-Diensttyp. Kontrollierte Auslastung oder garantierte Bandbreite.
ms.assetid: 3de23f2b-16dc-48c0-a8c5-e3130cd84ba8
ms.tgt_platform: multiple
keywords:
- AD-Schema des ACS-Service Type-Attributs
- acsservicetype-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ACS-Service-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b7dc97c17e9f7b38fa2f6f0ea863099bbef838a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107313"
---
# <a name="acs-service-type-attribute"></a><span data-ttu-id="e3c93-106">ACS-Service Type-Attribut</span><span class="sxs-lookup"><span data-stu-id="e3c93-106">ACS-Service-Type attribute</span></span>

<span data-ttu-id="e3c93-107">Der ACS-Diensttyp.</span><span class="sxs-lookup"><span data-stu-id="e3c93-107">The ACS service type.</span></span> <span data-ttu-id="e3c93-108">Kontrollierte Auslastung oder garantierte Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="e3c93-108">Controlled load or guaranteed bandwidth.</span></span>



| <span data-ttu-id="e3c93-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e3c93-109">Entry</span></span> | <span data-ttu-id="e3c93-110">Wert</span><span class="sxs-lookup"><span data-stu-id="e3c93-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e3c93-111">CN</span><span class="sxs-lookup"><span data-stu-id="e3c93-111">CN</span></span>                | <span data-ttu-id="e3c93-112">ACS-Diensttyp</span><span class="sxs-lookup"><span data-stu-id="e3c93-112">ACS-Service-Type</span></span>                     |
| <span data-ttu-id="e3c93-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e3c93-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e3c93-114">acsservicetype</span><span class="sxs-lookup"><span data-stu-id="e3c93-114">aCSServiceType</span></span>                       |
| <span data-ttu-id="e3c93-115">Size</span><span class="sxs-lookup"><span data-stu-id="e3c93-115">Size</span></span>              | <span data-ttu-id="e3c93-116">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="e3c93-116">4 bytes</span></span>                              |
| <span data-ttu-id="e3c93-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e3c93-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e3c93-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="e3c93-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e3c93-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e3c93-119">Attribute-Id</span></span>      | <span data-ttu-id="e3c93-120">1.2.840.113556.1.4.762</span><span class="sxs-lookup"><span data-stu-id="e3c93-120">1.2.840.113556.1.4.762</span></span>               |
| <span data-ttu-id="e3c93-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e3c93-121">System-Id-Guid</span></span>    | <span data-ttu-id="e3c93-122">7F 56127b-5301-11d1-a9c5-0000 C1</span><span class="sxs-lookup"><span data-stu-id="e3c93-122">7f56127f-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="e3c93-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3c93-123">Syntax</span></span>            | [<span data-ttu-id="e3c93-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="e3c93-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="e3c93-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="e3c93-125">Implementations</span></span>

-   [<span data-ttu-id="e3c93-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e3c93-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e3c93-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e3c93-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e3c93-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e3c93-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e3c93-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e3c93-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e3c93-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e3c93-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e3c93-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e3c93-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e3c93-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e3c93-132">Windows 2000 Server</span></span>



| <span data-ttu-id="e3c93-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e3c93-133">Entry</span></span> | <span data-ttu-id="e3c93-134">Wert</span><span class="sxs-lookup"><span data-stu-id="e3c93-134">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c93-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e3c93-135">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e3c93-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c93-136">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e3c93-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c93-137">System-Only</span></span>            | <span data-ttu-id="e3c93-138">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-138">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e3c93-139">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c93-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="e3c93-140">True</span></span>                                                                                                       |
| <span data-ttu-id="e3c93-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e3c93-141">Is Indexed</span></span>             | <span data-ttu-id="e3c93-142">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-142">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e3c93-143">In Global Catalog</span></span>      | <span data-ttu-id="e3c93-144">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-144">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e3c93-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c93-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e3c93-146">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e3c93-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c93-147">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e3c93-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c93-148">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e3c93-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c93-149">Search-Flags</span></span>           | <span data-ttu-id="e3c93-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c93-150">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e3c93-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c93-151">System-Flags</span></span>           | <span data-ttu-id="e3c93-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c93-152">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e3c93-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e3c93-153">Classes used in</span></span>        | [<span data-ttu-id="e3c93-154">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="e3c93-154">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="e3c93-155">**ACS-Ressourcen Limits**</span><span class="sxs-lookup"><span data-stu-id="e3c93-155">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e3c93-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e3c93-156">Windows Server 2003</span></span>



| <span data-ttu-id="e3c93-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e3c93-157">Entry</span></span> | <span data-ttu-id="e3c93-158">Wert</span><span class="sxs-lookup"><span data-stu-id="e3c93-158">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c93-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e3c93-159">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e3c93-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c93-160">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e3c93-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c93-161">System-Only</span></span>            | <span data-ttu-id="e3c93-162">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-162">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e3c93-163">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c93-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="e3c93-164">True</span></span>                                                                                                       |
| <span data-ttu-id="e3c93-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e3c93-165">Is Indexed</span></span>             | <span data-ttu-id="e3c93-166">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-166">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e3c93-167">In Global Catalog</span></span>      | <span data-ttu-id="e3c93-168">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-168">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e3c93-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c93-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e3c93-170">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e3c93-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c93-171">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e3c93-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c93-172">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e3c93-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c93-173">Search-Flags</span></span>           | <span data-ttu-id="e3c93-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c93-174">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e3c93-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c93-175">System-Flags</span></span>           | <span data-ttu-id="e3c93-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c93-176">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e3c93-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e3c93-177">Classes used in</span></span>        | [<span data-ttu-id="e3c93-178">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="e3c93-178">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="e3c93-179">**ACS-Ressourcen Limits**</span><span class="sxs-lookup"><span data-stu-id="e3c93-179">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e3c93-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e3c93-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e3c93-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e3c93-181">Entry</span></span> | <span data-ttu-id="e3c93-182">Wert</span><span class="sxs-lookup"><span data-stu-id="e3c93-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c93-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e3c93-183">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e3c93-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c93-184">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e3c93-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c93-185">System-Only</span></span>            | <span data-ttu-id="e3c93-186">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-186">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e3c93-187">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c93-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="e3c93-188">True</span></span>                                                                                                       |
| <span data-ttu-id="e3c93-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e3c93-189">Is Indexed</span></span>             | <span data-ttu-id="e3c93-190">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-190">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e3c93-191">In Global Catalog</span></span>      | <span data-ttu-id="e3c93-192">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-192">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e3c93-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c93-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e3c93-194">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e3c93-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c93-195">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e3c93-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c93-196">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e3c93-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c93-197">Search-Flags</span></span>           | <span data-ttu-id="e3c93-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c93-198">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e3c93-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c93-199">System-Flags</span></span>           | <span data-ttu-id="e3c93-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c93-200">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e3c93-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e3c93-201">Classes used in</span></span>        | [<span data-ttu-id="e3c93-202">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="e3c93-202">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="e3c93-203">**ACS-Ressourcen Limits**</span><span class="sxs-lookup"><span data-stu-id="e3c93-203">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e3c93-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3c93-204">Windows Server 2008</span></span>



| <span data-ttu-id="e3c93-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e3c93-205">Entry</span></span> | <span data-ttu-id="e3c93-206">Wert</span><span class="sxs-lookup"><span data-stu-id="e3c93-206">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c93-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e3c93-207">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e3c93-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c93-208">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e3c93-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c93-209">System-Only</span></span>            | <span data-ttu-id="e3c93-210">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-210">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e3c93-211">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c93-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="e3c93-212">True</span></span>                                                                                                       |
| <span data-ttu-id="e3c93-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e3c93-213">Is Indexed</span></span>             | <span data-ttu-id="e3c93-214">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-214">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e3c93-215">In Global Catalog</span></span>      | <span data-ttu-id="e3c93-216">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-216">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e3c93-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c93-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e3c93-218">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e3c93-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c93-219">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e3c93-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c93-220">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e3c93-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c93-221">Search-Flags</span></span>           | <span data-ttu-id="e3c93-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c93-222">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e3c93-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c93-223">System-Flags</span></span>           | <span data-ttu-id="e3c93-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c93-224">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e3c93-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e3c93-225">Classes used in</span></span>        | [<span data-ttu-id="e3c93-226">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="e3c93-226">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="e3c93-227">**ACS-Ressourcen Limits**</span><span class="sxs-lookup"><span data-stu-id="e3c93-227">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e3c93-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e3c93-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e3c93-229">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e3c93-229">Entry</span></span> | <span data-ttu-id="e3c93-230">Wert</span><span class="sxs-lookup"><span data-stu-id="e3c93-230">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c93-231">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e3c93-231">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e3c93-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c93-232">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e3c93-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c93-233">System-Only</span></span>            | <span data-ttu-id="e3c93-234">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-234">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-235">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e3c93-235">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c93-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="e3c93-236">True</span></span>                                                                                                       |
| <span data-ttu-id="e3c93-237">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e3c93-237">Is Indexed</span></span>             | <span data-ttu-id="e3c93-238">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-238">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-239">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e3c93-239">In Global Catalog</span></span>      | <span data-ttu-id="e3c93-240">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-240">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e3c93-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c93-242">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e3c93-242">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e3c93-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c93-243">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e3c93-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c93-244">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e3c93-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c93-245">Search-Flags</span></span>           | <span data-ttu-id="e3c93-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c93-246">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e3c93-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c93-247">System-Flags</span></span>           | <span data-ttu-id="e3c93-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c93-248">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e3c93-249">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e3c93-249">Classes used in</span></span>        | [<span data-ttu-id="e3c93-250">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="e3c93-250">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="e3c93-251">**ACS-Ressourcen Limits**</span><span class="sxs-lookup"><span data-stu-id="e3c93-251">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e3c93-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e3c93-252">Windows Server 2012</span></span>



| <span data-ttu-id="e3c93-253">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e3c93-253">Entry</span></span> | <span data-ttu-id="e3c93-254">Wert</span><span class="sxs-lookup"><span data-stu-id="e3c93-254">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c93-255">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e3c93-255">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e3c93-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c93-256">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e3c93-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c93-257">System-Only</span></span>            | <span data-ttu-id="e3c93-258">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-258">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-259">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e3c93-259">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c93-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="e3c93-260">True</span></span>                                                                                                       |
| <span data-ttu-id="e3c93-261">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e3c93-261">Is Indexed</span></span>             | <span data-ttu-id="e3c93-262">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-262">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-263">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e3c93-263">In Global Catalog</span></span>      | <span data-ttu-id="e3c93-264">False</span><span class="sxs-lookup"><span data-stu-id="e3c93-264">False</span></span>                                                                                                      |
| <span data-ttu-id="e3c93-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e3c93-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c93-266">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e3c93-266">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e3c93-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c93-267">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e3c93-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c93-268">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e3c93-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c93-269">Search-Flags</span></span>           | <span data-ttu-id="e3c93-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c93-270">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e3c93-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c93-271">System-Flags</span></span>           | <span data-ttu-id="e3c93-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c93-272">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e3c93-273">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e3c93-273">Classes used in</span></span>        | [<span data-ttu-id="e3c93-274">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="e3c93-274">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="e3c93-275">**ACS-Ressourcen Limits**</span><span class="sxs-lookup"><span data-stu-id="e3c93-275">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



 

 





