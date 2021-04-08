---
title: ACS-Maximum-SDU-size-Attribut
description: Das ACS-Maximum-SDU-size-Attribut ist nur für die interne Verwendung vorgesehen.
ms.assetid: 60dc8b92-888f-4eaf-8c7a-70d1ee12b490
ms.tgt_platform: multiple
keywords:
- AD-Schema für das ACS-Maximum-SDU-size-Attribut
- acsmaximumsdusize-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ACS-Maximum-SDU-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c9fa6260b3e0370f8a3d6e0ddfdab206d41db02
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744424"
---
# <a name="acs-maximum-sdu-size-attribute"></a><span data-ttu-id="0876c-105">ACS-Maximum-SDU-size-Attribut</span><span class="sxs-lookup"><span data-stu-id="0876c-105">ACS-Maximum-SDU-Size attribute</span></span>

<span data-ttu-id="0876c-106">Das **ACS-Maximum-SDU-size-** Attribut ist nur für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="0876c-106">The **ACS-Maximum-SDU-Size** attribute is for internal use only.</span></span> <span data-ttu-id="0876c-107">Basierend auf RFC2210.</span><span class="sxs-lookup"><span data-stu-id="0876c-107">Based on RFC2210.</span></span>



| <span data-ttu-id="0876c-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0876c-108">Entry</span></span> | <span data-ttu-id="0876c-109">Wert</span><span class="sxs-lookup"><span data-stu-id="0876c-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0876c-110">CN</span><span class="sxs-lookup"><span data-stu-id="0876c-110">CN</span></span>                | <span data-ttu-id="0876c-111">ACS-Maximum-SDU-size</span><span class="sxs-lookup"><span data-stu-id="0876c-111">ACS-Maximum-SDU-Size</span></span>                 |
| <span data-ttu-id="0876c-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0876c-112">Ldap-Display-Name</span></span> | <span data-ttu-id="0876c-113">acsmaximumsdusize</span><span class="sxs-lookup"><span data-stu-id="0876c-113">aCSMaximumSDUSize</span></span>                    |
| <span data-ttu-id="0876c-114">Size</span><span class="sxs-lookup"><span data-stu-id="0876c-114">Size</span></span>              | <span data-ttu-id="0876c-115">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="0876c-115">8 bytes</span></span>                              |
| <span data-ttu-id="0876c-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0876c-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="0876c-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="0876c-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="0876c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0876c-118">Attribute-Id</span></span>      | <span data-ttu-id="0876c-119">1.2.840.113556.1.4.1314</span><span class="sxs-lookup"><span data-stu-id="0876c-119">1.2.840.113556.1.4.1314</span></span>              |
| <span data-ttu-id="0876c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0876c-120">System-Id-Guid</span></span>    | <span data-ttu-id="0876c-121">87a2d8f 9-3b90-11d2-90cc-00c04f d91ab1</span><span class="sxs-lookup"><span data-stu-id="0876c-121">87a2d8f9-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="0876c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0876c-122">Syntax</span></span>            | [<span data-ttu-id="0876c-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="0876c-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="0876c-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="0876c-124">Implementations</span></span>

-   [<span data-ttu-id="0876c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0876c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0876c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0876c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0876c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0876c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0876c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0876c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0876c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0876c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0876c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0876c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0876c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0876c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0876c-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0876c-132">Entry</span></span> | <span data-ttu-id="0876c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="0876c-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0876c-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0876c-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0876c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0876c-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0876c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0876c-136">System-Only</span></span>            | <span data-ttu-id="0876c-137">False</span><span class="sxs-lookup"><span data-stu-id="0876c-137">False</span></span>                                        |
| <span data-ttu-id="0876c-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0876c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0876c-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="0876c-139">True</span></span>                                         |
| <span data-ttu-id="0876c-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0876c-140">Is Indexed</span></span>             | <span data-ttu-id="0876c-141">False</span><span class="sxs-lookup"><span data-stu-id="0876c-141">False</span></span>                                        |
| <span data-ttu-id="0876c-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0876c-142">In Global Catalog</span></span>      | <span data-ttu-id="0876c-143">False</span><span class="sxs-lookup"><span data-stu-id="0876c-143">False</span></span>                                        |
| <span data-ttu-id="0876c-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0876c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0876c-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0876c-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0876c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0876c-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0876c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0876c-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0876c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0876c-148">Search-Flags</span></span>           | <span data-ttu-id="0876c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0876c-149">0x00000000</span></span>                                   |
| <span data-ttu-id="0876c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0876c-150">System-Flags</span></span>           | <span data-ttu-id="0876c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0876c-151">0x00000010</span></span>                                   |
| <span data-ttu-id="0876c-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0876c-152">Classes used in</span></span>        | [<span data-ttu-id="0876c-153">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="0876c-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0876c-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0876c-154">Windows Server 2003</span></span>



| <span data-ttu-id="0876c-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0876c-155">Entry</span></span> | <span data-ttu-id="0876c-156">Wert</span><span class="sxs-lookup"><span data-stu-id="0876c-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0876c-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0876c-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0876c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0876c-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0876c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="0876c-159">System-Only</span></span>            | <span data-ttu-id="0876c-160">False</span><span class="sxs-lookup"><span data-stu-id="0876c-160">False</span></span>                                        |
| <span data-ttu-id="0876c-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0876c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="0876c-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="0876c-162">True</span></span>                                         |
| <span data-ttu-id="0876c-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0876c-163">Is Indexed</span></span>             | <span data-ttu-id="0876c-164">False</span><span class="sxs-lookup"><span data-stu-id="0876c-164">False</span></span>                                        |
| <span data-ttu-id="0876c-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0876c-165">In Global Catalog</span></span>      | <span data-ttu-id="0876c-166">False</span><span class="sxs-lookup"><span data-stu-id="0876c-166">False</span></span>                                        |
| <span data-ttu-id="0876c-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0876c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="0876c-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0876c-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0876c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0876c-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0876c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0876c-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0876c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0876c-171">Search-Flags</span></span>           | <span data-ttu-id="0876c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0876c-172">0x00000000</span></span>                                   |
| <span data-ttu-id="0876c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0876c-173">System-Flags</span></span>           | <span data-ttu-id="0876c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0876c-174">0x00000010</span></span>                                   |
| <span data-ttu-id="0876c-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0876c-175">Classes used in</span></span>        | [<span data-ttu-id="0876c-176">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="0876c-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0876c-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0876c-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0876c-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0876c-178">Entry</span></span> | <span data-ttu-id="0876c-179">Wert</span><span class="sxs-lookup"><span data-stu-id="0876c-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0876c-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0876c-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0876c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0876c-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0876c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="0876c-182">System-Only</span></span>            | <span data-ttu-id="0876c-183">False</span><span class="sxs-lookup"><span data-stu-id="0876c-183">False</span></span>                                        |
| <span data-ttu-id="0876c-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0876c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="0876c-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="0876c-185">True</span></span>                                         |
| <span data-ttu-id="0876c-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0876c-186">Is Indexed</span></span>             | <span data-ttu-id="0876c-187">False</span><span class="sxs-lookup"><span data-stu-id="0876c-187">False</span></span>                                        |
| <span data-ttu-id="0876c-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0876c-188">In Global Catalog</span></span>      | <span data-ttu-id="0876c-189">False</span><span class="sxs-lookup"><span data-stu-id="0876c-189">False</span></span>                                        |
| <span data-ttu-id="0876c-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0876c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="0876c-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0876c-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0876c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0876c-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0876c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0876c-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0876c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0876c-194">Search-Flags</span></span>           | <span data-ttu-id="0876c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0876c-195">0x00000000</span></span>                                   |
| <span data-ttu-id="0876c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0876c-196">System-Flags</span></span>           | <span data-ttu-id="0876c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0876c-197">0x00000010</span></span>                                   |
| <span data-ttu-id="0876c-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0876c-198">Classes used in</span></span>        | [<span data-ttu-id="0876c-199">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="0876c-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0876c-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0876c-200">Windows Server 2008</span></span>



| <span data-ttu-id="0876c-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0876c-201">Entry</span></span> | <span data-ttu-id="0876c-202">Wert</span><span class="sxs-lookup"><span data-stu-id="0876c-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0876c-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0876c-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0876c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0876c-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0876c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="0876c-205">System-Only</span></span>            | <span data-ttu-id="0876c-206">False</span><span class="sxs-lookup"><span data-stu-id="0876c-206">False</span></span>                                        |
| <span data-ttu-id="0876c-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0876c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="0876c-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="0876c-208">True</span></span>                                         |
| <span data-ttu-id="0876c-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0876c-209">Is Indexed</span></span>             | <span data-ttu-id="0876c-210">False</span><span class="sxs-lookup"><span data-stu-id="0876c-210">False</span></span>                                        |
| <span data-ttu-id="0876c-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0876c-211">In Global Catalog</span></span>      | <span data-ttu-id="0876c-212">False</span><span class="sxs-lookup"><span data-stu-id="0876c-212">False</span></span>                                        |
| <span data-ttu-id="0876c-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0876c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="0876c-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0876c-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0876c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0876c-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0876c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0876c-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0876c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0876c-217">Search-Flags</span></span>           | <span data-ttu-id="0876c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0876c-218">0x00000000</span></span>                                   |
| <span data-ttu-id="0876c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0876c-219">System-Flags</span></span>           | <span data-ttu-id="0876c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0876c-220">0x00000010</span></span>                                   |
| <span data-ttu-id="0876c-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0876c-221">Classes used in</span></span>        | [<span data-ttu-id="0876c-222">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="0876c-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0876c-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0876c-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0876c-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0876c-224">Entry</span></span> | <span data-ttu-id="0876c-225">Wert</span><span class="sxs-lookup"><span data-stu-id="0876c-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0876c-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0876c-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0876c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0876c-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0876c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="0876c-228">System-Only</span></span>            | <span data-ttu-id="0876c-229">False</span><span class="sxs-lookup"><span data-stu-id="0876c-229">False</span></span>                                        |
| <span data-ttu-id="0876c-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0876c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="0876c-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="0876c-231">True</span></span>                                         |
| <span data-ttu-id="0876c-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0876c-232">Is Indexed</span></span>             | <span data-ttu-id="0876c-233">False</span><span class="sxs-lookup"><span data-stu-id="0876c-233">False</span></span>                                        |
| <span data-ttu-id="0876c-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0876c-234">In Global Catalog</span></span>      | <span data-ttu-id="0876c-235">False</span><span class="sxs-lookup"><span data-stu-id="0876c-235">False</span></span>                                        |
| <span data-ttu-id="0876c-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0876c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="0876c-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0876c-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0876c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0876c-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0876c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0876c-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0876c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0876c-240">Search-Flags</span></span>           | <span data-ttu-id="0876c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0876c-241">0x00000000</span></span>                                   |
| <span data-ttu-id="0876c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0876c-242">System-Flags</span></span>           | <span data-ttu-id="0876c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0876c-243">0x00000010</span></span>                                   |
| <span data-ttu-id="0876c-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0876c-244">Classes used in</span></span>        | [<span data-ttu-id="0876c-245">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="0876c-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0876c-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0876c-246">Windows Server 2012</span></span>



| <span data-ttu-id="0876c-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0876c-247">Entry</span></span> | <span data-ttu-id="0876c-248">Wert</span><span class="sxs-lookup"><span data-stu-id="0876c-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0876c-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0876c-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0876c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0876c-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0876c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="0876c-251">System-Only</span></span>            | <span data-ttu-id="0876c-252">False</span><span class="sxs-lookup"><span data-stu-id="0876c-252">False</span></span>                                        |
| <span data-ttu-id="0876c-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0876c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="0876c-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="0876c-254">True</span></span>                                         |
| <span data-ttu-id="0876c-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0876c-255">Is Indexed</span></span>             | <span data-ttu-id="0876c-256">False</span><span class="sxs-lookup"><span data-stu-id="0876c-256">False</span></span>                                        |
| <span data-ttu-id="0876c-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0876c-257">In Global Catalog</span></span>      | <span data-ttu-id="0876c-258">False</span><span class="sxs-lookup"><span data-stu-id="0876c-258">False</span></span>                                        |
| <span data-ttu-id="0876c-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0876c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="0876c-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0876c-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0876c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0876c-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0876c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0876c-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0876c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0876c-263">Search-Flags</span></span>           | <span data-ttu-id="0876c-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0876c-264">0x00000000</span></span>                                   |
| <span data-ttu-id="0876c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0876c-265">System-Flags</span></span>           | <span data-ttu-id="0876c-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0876c-266">0x00000010</span></span>                                   |
| <span data-ttu-id="0876c-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0876c-267">Classes used in</span></span>        | [<span data-ttu-id="0876c-268">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="0876c-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





