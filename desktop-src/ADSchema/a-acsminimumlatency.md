---
title: ACS-Attribut mit minimaler Latenzzeit
description: Das Attribut "ACS-minimaler Latenz" ist nur für die interne Verwendung vorgesehen.
ms.assetid: ec2cca55-9e31-49da-98aa-aa2f6664ea90
ms.tgt_platform: multiple
keywords:
- AD-Schema des ACS-Attributs mit minimaler Latenz
- acsminimumlatency-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- ACS-Minimum-Latency
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab7e9e6d5a9ccf626cdf8849ffe0e29504b4a0b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104041050"
---
# <a name="acs-minimum-latency-attribute"></a><span data-ttu-id="cbb23-105">ACS-Attribut mit minimaler Latenzzeit</span><span class="sxs-lookup"><span data-stu-id="cbb23-105">ACS-Minimum-Latency attribute</span></span>

<span data-ttu-id="cbb23-106">Das Attribut " **ACS-minimaler Latenz** " ist nur für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="cbb23-106">The **ACS-Minimum-Latency** attribute is for internal use only.</span></span> <span data-ttu-id="cbb23-107">Basierend auf RFC2210.</span><span class="sxs-lookup"><span data-stu-id="cbb23-107">Based on RFC2210.</span></span>



| <span data-ttu-id="cbb23-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cbb23-108">Entry</span></span> | <span data-ttu-id="cbb23-109">Wert</span><span class="sxs-lookup"><span data-stu-id="cbb23-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="cbb23-110">CN</span><span class="sxs-lookup"><span data-stu-id="cbb23-110">CN</span></span>                | <span data-ttu-id="cbb23-111">ACS-minimale Latenzzeit</span><span class="sxs-lookup"><span data-stu-id="cbb23-111">ACS-Minimum-Latency</span></span>                  |
| <span data-ttu-id="cbb23-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cbb23-112">Ldap-Display-Name</span></span> | <span data-ttu-id="cbb23-113">acsminimumlatency</span><span class="sxs-lookup"><span data-stu-id="cbb23-113">aCSMinimumLatency</span></span>                    |
| <span data-ttu-id="cbb23-114">Size</span><span class="sxs-lookup"><span data-stu-id="cbb23-114">Size</span></span>              | <span data-ttu-id="cbb23-115">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="cbb23-115">8 bytes</span></span>                              |
| <span data-ttu-id="cbb23-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="cbb23-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="cbb23-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="cbb23-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="cbb23-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cbb23-118">Attribute-Id</span></span>      | <span data-ttu-id="cbb23-119">1.2.840.113556.1.4.1316</span><span class="sxs-lookup"><span data-stu-id="cbb23-119">1.2.840.113556.1.4.1316</span></span>              |
| <span data-ttu-id="cbb23-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cbb23-120">System-Id-Guid</span></span>    | <span data-ttu-id="cbb23-121">9517fef b-3b90-11d2-90cc-00c04f d91ab1</span><span class="sxs-lookup"><span data-stu-id="cbb23-121">9517fefb-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="cbb23-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbb23-122">Syntax</span></span>            | [<span data-ttu-id="cbb23-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="cbb23-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="cbb23-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="cbb23-124">Implementations</span></span>

-   [<span data-ttu-id="cbb23-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cbb23-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cbb23-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cbb23-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cbb23-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cbb23-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cbb23-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cbb23-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cbb23-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cbb23-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cbb23-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cbb23-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cbb23-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cbb23-131">Windows 2000 Server</span></span>



| <span data-ttu-id="cbb23-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cbb23-132">Entry</span></span> | <span data-ttu-id="cbb23-133">Wert</span><span class="sxs-lookup"><span data-stu-id="cbb23-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cbb23-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cbb23-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cbb23-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cbb23-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cbb23-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="cbb23-136">System-Only</span></span>            | <span data-ttu-id="cbb23-137">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-137">False</span></span>                                        |
| <span data-ttu-id="cbb23-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cbb23-138">Is-Single-Valued</span></span>       | <span data-ttu-id="cbb23-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="cbb23-139">True</span></span>                                         |
| <span data-ttu-id="cbb23-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cbb23-140">Is Indexed</span></span>             | <span data-ttu-id="cbb23-141">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-141">False</span></span>                                        |
| <span data-ttu-id="cbb23-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cbb23-142">In Global Catalog</span></span>      | <span data-ttu-id="cbb23-143">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-143">False</span></span>                                        |
| <span data-ttu-id="cbb23-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cbb23-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="cbb23-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cbb23-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cbb23-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cbb23-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cbb23-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cbb23-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cbb23-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb23-148">Search-Flags</span></span>           | <span data-ttu-id="cbb23-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbb23-149">0x00000000</span></span>                                   |
| <span data-ttu-id="cbb23-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb23-150">System-Flags</span></span>           | <span data-ttu-id="cbb23-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cbb23-151">0x00000010</span></span>                                   |
| <span data-ttu-id="cbb23-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cbb23-152">Classes used in</span></span>        | [<span data-ttu-id="cbb23-153">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="cbb23-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cbb23-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cbb23-154">Windows Server 2003</span></span>



| <span data-ttu-id="cbb23-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cbb23-155">Entry</span></span> | <span data-ttu-id="cbb23-156">Wert</span><span class="sxs-lookup"><span data-stu-id="cbb23-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cbb23-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cbb23-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cbb23-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cbb23-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cbb23-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="cbb23-159">System-Only</span></span>            | <span data-ttu-id="cbb23-160">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-160">False</span></span>                                        |
| <span data-ttu-id="cbb23-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cbb23-161">Is-Single-Valued</span></span>       | <span data-ttu-id="cbb23-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="cbb23-162">True</span></span>                                         |
| <span data-ttu-id="cbb23-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cbb23-163">Is Indexed</span></span>             | <span data-ttu-id="cbb23-164">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-164">False</span></span>                                        |
| <span data-ttu-id="cbb23-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cbb23-165">In Global Catalog</span></span>      | <span data-ttu-id="cbb23-166">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-166">False</span></span>                                        |
| <span data-ttu-id="cbb23-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cbb23-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="cbb23-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cbb23-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cbb23-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cbb23-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cbb23-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cbb23-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cbb23-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb23-171">Search-Flags</span></span>           | <span data-ttu-id="cbb23-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbb23-172">0x00000000</span></span>                                   |
| <span data-ttu-id="cbb23-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb23-173">System-Flags</span></span>           | <span data-ttu-id="cbb23-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cbb23-174">0x00000010</span></span>                                   |
| <span data-ttu-id="cbb23-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cbb23-175">Classes used in</span></span>        | [<span data-ttu-id="cbb23-176">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="cbb23-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cbb23-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cbb23-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cbb23-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cbb23-178">Entry</span></span> | <span data-ttu-id="cbb23-179">Wert</span><span class="sxs-lookup"><span data-stu-id="cbb23-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cbb23-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cbb23-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cbb23-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cbb23-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cbb23-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="cbb23-182">System-Only</span></span>            | <span data-ttu-id="cbb23-183">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-183">False</span></span>                                        |
| <span data-ttu-id="cbb23-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cbb23-184">Is-Single-Valued</span></span>       | <span data-ttu-id="cbb23-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="cbb23-185">True</span></span>                                         |
| <span data-ttu-id="cbb23-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cbb23-186">Is Indexed</span></span>             | <span data-ttu-id="cbb23-187">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-187">False</span></span>                                        |
| <span data-ttu-id="cbb23-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cbb23-188">In Global Catalog</span></span>      | <span data-ttu-id="cbb23-189">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-189">False</span></span>                                        |
| <span data-ttu-id="cbb23-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cbb23-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="cbb23-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cbb23-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cbb23-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cbb23-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cbb23-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cbb23-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cbb23-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb23-194">Search-Flags</span></span>           | <span data-ttu-id="cbb23-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbb23-195">0x00000000</span></span>                                   |
| <span data-ttu-id="cbb23-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb23-196">System-Flags</span></span>           | <span data-ttu-id="cbb23-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cbb23-197">0x00000010</span></span>                                   |
| <span data-ttu-id="cbb23-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cbb23-198">Classes used in</span></span>        | [<span data-ttu-id="cbb23-199">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="cbb23-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cbb23-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbb23-200">Windows Server 2008</span></span>



| <span data-ttu-id="cbb23-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cbb23-201">Entry</span></span> | <span data-ttu-id="cbb23-202">Wert</span><span class="sxs-lookup"><span data-stu-id="cbb23-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cbb23-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cbb23-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cbb23-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cbb23-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cbb23-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="cbb23-205">System-Only</span></span>            | <span data-ttu-id="cbb23-206">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-206">False</span></span>                                        |
| <span data-ttu-id="cbb23-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cbb23-207">Is-Single-Valued</span></span>       | <span data-ttu-id="cbb23-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="cbb23-208">True</span></span>                                         |
| <span data-ttu-id="cbb23-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cbb23-209">Is Indexed</span></span>             | <span data-ttu-id="cbb23-210">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-210">False</span></span>                                        |
| <span data-ttu-id="cbb23-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cbb23-211">In Global Catalog</span></span>      | <span data-ttu-id="cbb23-212">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-212">False</span></span>                                        |
| <span data-ttu-id="cbb23-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cbb23-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="cbb23-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cbb23-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cbb23-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cbb23-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cbb23-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cbb23-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cbb23-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb23-217">Search-Flags</span></span>           | <span data-ttu-id="cbb23-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbb23-218">0x00000000</span></span>                                   |
| <span data-ttu-id="cbb23-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb23-219">System-Flags</span></span>           | <span data-ttu-id="cbb23-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cbb23-220">0x00000010</span></span>                                   |
| <span data-ttu-id="cbb23-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cbb23-221">Classes used in</span></span>        | [<span data-ttu-id="cbb23-222">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="cbb23-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cbb23-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cbb23-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cbb23-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cbb23-224">Entry</span></span> | <span data-ttu-id="cbb23-225">Wert</span><span class="sxs-lookup"><span data-stu-id="cbb23-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cbb23-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cbb23-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cbb23-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cbb23-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cbb23-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="cbb23-228">System-Only</span></span>            | <span data-ttu-id="cbb23-229">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-229">False</span></span>                                        |
| <span data-ttu-id="cbb23-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cbb23-230">Is-Single-Valued</span></span>       | <span data-ttu-id="cbb23-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="cbb23-231">True</span></span>                                         |
| <span data-ttu-id="cbb23-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cbb23-232">Is Indexed</span></span>             | <span data-ttu-id="cbb23-233">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-233">False</span></span>                                        |
| <span data-ttu-id="cbb23-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cbb23-234">In Global Catalog</span></span>      | <span data-ttu-id="cbb23-235">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-235">False</span></span>                                        |
| <span data-ttu-id="cbb23-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cbb23-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="cbb23-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cbb23-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cbb23-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cbb23-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cbb23-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cbb23-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cbb23-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb23-240">Search-Flags</span></span>           | <span data-ttu-id="cbb23-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbb23-241">0x00000000</span></span>                                   |
| <span data-ttu-id="cbb23-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb23-242">System-Flags</span></span>           | <span data-ttu-id="cbb23-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cbb23-243">0x00000010</span></span>                                   |
| <span data-ttu-id="cbb23-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cbb23-244">Classes used in</span></span>        | [<span data-ttu-id="cbb23-245">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="cbb23-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cbb23-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cbb23-246">Windows Server 2012</span></span>



| <span data-ttu-id="cbb23-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cbb23-247">Entry</span></span> | <span data-ttu-id="cbb23-248">Wert</span><span class="sxs-lookup"><span data-stu-id="cbb23-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cbb23-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cbb23-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cbb23-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cbb23-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cbb23-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="cbb23-251">System-Only</span></span>            | <span data-ttu-id="cbb23-252">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-252">False</span></span>                                        |
| <span data-ttu-id="cbb23-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cbb23-253">Is-Single-Valued</span></span>       | <span data-ttu-id="cbb23-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="cbb23-254">True</span></span>                                         |
| <span data-ttu-id="cbb23-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cbb23-255">Is Indexed</span></span>             | <span data-ttu-id="cbb23-256">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-256">False</span></span>                                        |
| <span data-ttu-id="cbb23-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cbb23-257">In Global Catalog</span></span>      | <span data-ttu-id="cbb23-258">False</span><span class="sxs-lookup"><span data-stu-id="cbb23-258">False</span></span>                                        |
| <span data-ttu-id="cbb23-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cbb23-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="cbb23-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cbb23-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cbb23-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cbb23-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cbb23-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cbb23-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cbb23-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb23-263">Search-Flags</span></span>           | <span data-ttu-id="cbb23-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbb23-264">0x00000000</span></span>                                   |
| <span data-ttu-id="cbb23-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb23-265">System-Flags</span></span>           | <span data-ttu-id="cbb23-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cbb23-266">0x00000010</span></span>                                   |
| <span data-ttu-id="cbb23-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cbb23-267">Classes used in</span></span>        | [<span data-ttu-id="cbb23-268">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="cbb23-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





