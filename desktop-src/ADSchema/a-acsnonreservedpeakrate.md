---
title: ACS-nicht reserviertes Attribut mit Spitzen Raten
description: Das Attribut "ACS-Non-reserved-Peak-Rate" ist nur für die interne Verwendung vorgesehen.
ms.assetid: 4080839c-d99e-4527-8c81-6d23ab0d3d70
ms.tgt_platform: multiple
keywords:
- AD-Schema für ACS-nicht reservierte Spitzen Raten Attribute
- acsnonreservedpeer Rate-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Peak-Rate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea3d2075e90648388a9a1277dbbe768a3fc616f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107325"
---
# <a name="acs-non-reserved-peak-rate-attribute"></a><span data-ttu-id="ade0a-105">ACS-nicht reserviertes Attribut mit Spitzen Raten</span><span class="sxs-lookup"><span data-stu-id="ade0a-105">ACS-Non-Reserved-Peak-Rate attribute</span></span>

<span data-ttu-id="ade0a-106">Das Attribut " **ACS-Non-reserved-Peak-Rate** " ist nur für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="ade0a-106">The **ACS-Non-Reserved-Peak-Rate** attribute is for internal use only.</span></span> <span data-ttu-id="ade0a-107">Basierend auf RFC2814.</span><span class="sxs-lookup"><span data-stu-id="ade0a-107">Based on RFC2814.</span></span>



| <span data-ttu-id="ade0a-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ade0a-108">Entry</span></span> | <span data-ttu-id="ade0a-109">Wert</span><span class="sxs-lookup"><span data-stu-id="ade0a-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ade0a-110">CN</span><span class="sxs-lookup"><span data-stu-id="ade0a-110">CN</span></span>                | <span data-ttu-id="ade0a-111">ACS-nicht reservierte Spitzen Rate</span><span class="sxs-lookup"><span data-stu-id="ade0a-111">ACS-Non-Reserved-Peak-Rate</span></span>           |
| <span data-ttu-id="ade0a-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ade0a-112">Ldap-Display-Name</span></span> | <span data-ttu-id="ade0a-113">acsnonreservedpeer-Rate</span><span class="sxs-lookup"><span data-stu-id="ade0a-113">aCSNonReservedPeakRate</span></span>               |
| <span data-ttu-id="ade0a-114">Size</span><span class="sxs-lookup"><span data-stu-id="ade0a-114">Size</span></span>              | <span data-ttu-id="ade0a-115">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="ade0a-115">8 bytes</span></span>                              |
| <span data-ttu-id="ade0a-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ade0a-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ade0a-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="ade0a-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ade0a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ade0a-118">Attribute-Id</span></span>      | <span data-ttu-id="ade0a-119">1.2.840.113556.1.4.1318</span><span class="sxs-lookup"><span data-stu-id="ade0a-119">1.2.840.113556.1.4.1318</span></span>              |
| <span data-ttu-id="ade0a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ade0a-120">System-Id-Guid</span></span>    | <span data-ttu-id="ade0a-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="ade0a-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="ade0a-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="ade0a-122">Syntax</span></span>            | [<span data-ttu-id="ade0a-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="ade0a-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="ade0a-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ade0a-124">Implementations</span></span>

-   [<span data-ttu-id="ade0a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ade0a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ade0a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ade0a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ade0a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ade0a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ade0a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ade0a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ade0a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ade0a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ade0a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ade0a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ade0a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ade0a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ade0a-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ade0a-132">Entry</span></span> | <span data-ttu-id="ade0a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="ade0a-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ade0a-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ade0a-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ade0a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ade0a-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ade0a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ade0a-136">System-Only</span></span>            | <span data-ttu-id="ade0a-137">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-137">False</span></span>                                        |
| <span data-ttu-id="ade0a-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ade0a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ade0a-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="ade0a-139">True</span></span>                                         |
| <span data-ttu-id="ade0a-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ade0a-140">Is Indexed</span></span>             | <span data-ttu-id="ade0a-141">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-141">False</span></span>                                        |
| <span data-ttu-id="ade0a-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ade0a-142">In Global Catalog</span></span>      | <span data-ttu-id="ade0a-143">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-143">False</span></span>                                        |
| <span data-ttu-id="ade0a-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ade0a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ade0a-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ade0a-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ade0a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ade0a-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ade0a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ade0a-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ade0a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ade0a-148">Search-Flags</span></span>           | <span data-ttu-id="ade0a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ade0a-149">0x00000000</span></span>                                   |
| <span data-ttu-id="ade0a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ade0a-150">System-Flags</span></span>           | <span data-ttu-id="ade0a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ade0a-151">0x00000010</span></span>                                   |
| <span data-ttu-id="ade0a-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ade0a-152">Classes used in</span></span>        | [<span data-ttu-id="ade0a-153">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="ade0a-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ade0a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ade0a-154">Windows Server 2003</span></span>



| <span data-ttu-id="ade0a-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ade0a-155">Entry</span></span> | <span data-ttu-id="ade0a-156">Wert</span><span class="sxs-lookup"><span data-stu-id="ade0a-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ade0a-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ade0a-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ade0a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ade0a-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ade0a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ade0a-159">System-Only</span></span>            | <span data-ttu-id="ade0a-160">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-160">False</span></span>                                        |
| <span data-ttu-id="ade0a-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ade0a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ade0a-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="ade0a-162">True</span></span>                                         |
| <span data-ttu-id="ade0a-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ade0a-163">Is Indexed</span></span>             | <span data-ttu-id="ade0a-164">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-164">False</span></span>                                        |
| <span data-ttu-id="ade0a-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ade0a-165">In Global Catalog</span></span>      | <span data-ttu-id="ade0a-166">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-166">False</span></span>                                        |
| <span data-ttu-id="ade0a-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ade0a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ade0a-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ade0a-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ade0a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ade0a-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ade0a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ade0a-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ade0a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ade0a-171">Search-Flags</span></span>           | <span data-ttu-id="ade0a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ade0a-172">0x00000000</span></span>                                   |
| <span data-ttu-id="ade0a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ade0a-173">System-Flags</span></span>           | <span data-ttu-id="ade0a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ade0a-174">0x00000010</span></span>                                   |
| <span data-ttu-id="ade0a-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ade0a-175">Classes used in</span></span>        | [<span data-ttu-id="ade0a-176">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="ade0a-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ade0a-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ade0a-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ade0a-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ade0a-178">Entry</span></span> | <span data-ttu-id="ade0a-179">Wert</span><span class="sxs-lookup"><span data-stu-id="ade0a-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ade0a-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ade0a-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ade0a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ade0a-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ade0a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ade0a-182">System-Only</span></span>            | <span data-ttu-id="ade0a-183">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-183">False</span></span>                                        |
| <span data-ttu-id="ade0a-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ade0a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ade0a-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="ade0a-185">True</span></span>                                         |
| <span data-ttu-id="ade0a-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ade0a-186">Is Indexed</span></span>             | <span data-ttu-id="ade0a-187">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-187">False</span></span>                                        |
| <span data-ttu-id="ade0a-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ade0a-188">In Global Catalog</span></span>      | <span data-ttu-id="ade0a-189">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-189">False</span></span>                                        |
| <span data-ttu-id="ade0a-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ade0a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ade0a-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ade0a-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ade0a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ade0a-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ade0a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ade0a-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ade0a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ade0a-194">Search-Flags</span></span>           | <span data-ttu-id="ade0a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ade0a-195">0x00000000</span></span>                                   |
| <span data-ttu-id="ade0a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ade0a-196">System-Flags</span></span>           | <span data-ttu-id="ade0a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ade0a-197">0x00000010</span></span>                                   |
| <span data-ttu-id="ade0a-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ade0a-198">Classes used in</span></span>        | [<span data-ttu-id="ade0a-199">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="ade0a-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ade0a-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ade0a-200">Windows Server 2008</span></span>



| <span data-ttu-id="ade0a-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ade0a-201">Entry</span></span> | <span data-ttu-id="ade0a-202">Wert</span><span class="sxs-lookup"><span data-stu-id="ade0a-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ade0a-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ade0a-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ade0a-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ade0a-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ade0a-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ade0a-205">System-Only</span></span>            | <span data-ttu-id="ade0a-206">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-206">False</span></span>                                        |
| <span data-ttu-id="ade0a-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ade0a-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ade0a-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="ade0a-208">True</span></span>                                         |
| <span data-ttu-id="ade0a-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ade0a-209">Is Indexed</span></span>             | <span data-ttu-id="ade0a-210">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-210">False</span></span>                                        |
| <span data-ttu-id="ade0a-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ade0a-211">In Global Catalog</span></span>      | <span data-ttu-id="ade0a-212">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-212">False</span></span>                                        |
| <span data-ttu-id="ade0a-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ade0a-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ade0a-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ade0a-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ade0a-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ade0a-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ade0a-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ade0a-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ade0a-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ade0a-217">Search-Flags</span></span>           | <span data-ttu-id="ade0a-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ade0a-218">0x00000000</span></span>                                   |
| <span data-ttu-id="ade0a-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ade0a-219">System-Flags</span></span>           | <span data-ttu-id="ade0a-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ade0a-220">0x00000010</span></span>                                   |
| <span data-ttu-id="ade0a-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ade0a-221">Classes used in</span></span>        | [<span data-ttu-id="ade0a-222">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="ade0a-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ade0a-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ade0a-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ade0a-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ade0a-224">Entry</span></span> | <span data-ttu-id="ade0a-225">Wert</span><span class="sxs-lookup"><span data-stu-id="ade0a-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ade0a-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ade0a-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ade0a-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ade0a-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ade0a-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ade0a-228">System-Only</span></span>            | <span data-ttu-id="ade0a-229">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-229">False</span></span>                                        |
| <span data-ttu-id="ade0a-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ade0a-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ade0a-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="ade0a-231">True</span></span>                                         |
| <span data-ttu-id="ade0a-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ade0a-232">Is Indexed</span></span>             | <span data-ttu-id="ade0a-233">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-233">False</span></span>                                        |
| <span data-ttu-id="ade0a-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ade0a-234">In Global Catalog</span></span>      | <span data-ttu-id="ade0a-235">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-235">False</span></span>                                        |
| <span data-ttu-id="ade0a-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ade0a-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ade0a-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ade0a-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ade0a-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ade0a-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ade0a-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ade0a-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ade0a-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ade0a-240">Search-Flags</span></span>           | <span data-ttu-id="ade0a-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ade0a-241">0x00000000</span></span>                                   |
| <span data-ttu-id="ade0a-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ade0a-242">System-Flags</span></span>           | <span data-ttu-id="ade0a-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ade0a-243">0x00000010</span></span>                                   |
| <span data-ttu-id="ade0a-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ade0a-244">Classes used in</span></span>        | [<span data-ttu-id="ade0a-245">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="ade0a-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ade0a-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ade0a-246">Windows Server 2012</span></span>



| <span data-ttu-id="ade0a-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ade0a-247">Entry</span></span> | <span data-ttu-id="ade0a-248">Wert</span><span class="sxs-lookup"><span data-stu-id="ade0a-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ade0a-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ade0a-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ade0a-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ade0a-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ade0a-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="ade0a-251">System-Only</span></span>            | <span data-ttu-id="ade0a-252">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-252">False</span></span>                                        |
| <span data-ttu-id="ade0a-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ade0a-253">Is-Single-Valued</span></span>       | <span data-ttu-id="ade0a-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="ade0a-254">True</span></span>                                         |
| <span data-ttu-id="ade0a-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ade0a-255">Is Indexed</span></span>             | <span data-ttu-id="ade0a-256">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-256">False</span></span>                                        |
| <span data-ttu-id="ade0a-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ade0a-257">In Global Catalog</span></span>      | <span data-ttu-id="ade0a-258">False</span><span class="sxs-lookup"><span data-stu-id="ade0a-258">False</span></span>                                        |
| <span data-ttu-id="ade0a-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ade0a-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="ade0a-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ade0a-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ade0a-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ade0a-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ade0a-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ade0a-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ade0a-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ade0a-263">Search-Flags</span></span>           | <span data-ttu-id="ade0a-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ade0a-264">0x00000000</span></span>                                   |
| <span data-ttu-id="ade0a-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ade0a-265">System-Flags</span></span>           | <span data-ttu-id="ade0a-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ade0a-266">0x00000010</span></span>                                   |
| <span data-ttu-id="ade0a-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ade0a-267">Classes used in</span></span>        | [<span data-ttu-id="ade0a-268">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="ade0a-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





