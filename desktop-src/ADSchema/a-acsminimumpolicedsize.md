---
title: ACS-minimal-Richtlinien Attribut
description: Das ACS-minimal-Richtwert-Attribut ist nur für die interne Verwendung vorgesehen.
ms.assetid: 27b4273a-a625-430b-baa0-a6037e2aac1e
ms.tgt_platform: multiple
keywords:
- AD-Schema für ACS-minimal-Richtlinien Größe
- acsminimumpolicedsize-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ACS-Minimum-Policed-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3de4bb2b33a45ab7d10bad72ba286d1695b980a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106343535"
---
# <a name="acs-minimum-policed-size-attribute"></a><span data-ttu-id="3e02f-105">ACS-minimal-Richtlinien Attribut</span><span class="sxs-lookup"><span data-stu-id="3e02f-105">ACS-Minimum-Policed-Size attribute</span></span>

<span data-ttu-id="3e02f-106">Das **ACS-minimal-Richtwert** -Attribut ist nur für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="3e02f-106">The **ACS-Minimum-Policed-Size** attribute is for internal use only.</span></span> <span data-ttu-id="3e02f-107">Basierend auf RFC2210.</span><span class="sxs-lookup"><span data-stu-id="3e02f-107">Based on RFC2210.</span></span>



| <span data-ttu-id="3e02f-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e02f-108">Entry</span></span> | <span data-ttu-id="3e02f-109">Wert</span><span class="sxs-lookup"><span data-stu-id="3e02f-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="3e02f-110">CN</span><span class="sxs-lookup"><span data-stu-id="3e02f-110">CN</span></span>                | <span data-ttu-id="3e02f-111">ACS-minimal-Richtlinien Größe</span><span class="sxs-lookup"><span data-stu-id="3e02f-111">ACS-Minimum-Policed-Size</span></span>             |
| <span data-ttu-id="3e02f-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3e02f-112">Ldap-Display-Name</span></span> | <span data-ttu-id="3e02f-113">acsminimumpolicedsize</span><span class="sxs-lookup"><span data-stu-id="3e02f-113">aCSMinimumPolicedSize</span></span>                |
| <span data-ttu-id="3e02f-114">Size</span><span class="sxs-lookup"><span data-stu-id="3e02f-114">Size</span></span>              | <span data-ttu-id="3e02f-115">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="3e02f-115">8 bytes</span></span>                              |
| <span data-ttu-id="3e02f-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="3e02f-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="3e02f-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="3e02f-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="3e02f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3e02f-118">Attribute-Id</span></span>      | <span data-ttu-id="3e02f-119">1.2.840.113556.1.4.1315</span><span class="sxs-lookup"><span data-stu-id="3e02f-119">1.2.840.113556.1.4.1315</span></span>              |
| <span data-ttu-id="3e02f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3e02f-120">System-Id-Guid</span></span>    | <span data-ttu-id="3e02f-121">8d0e7195-3b90-11d2-90cc-00c04f d91ab1</span><span class="sxs-lookup"><span data-stu-id="3e02f-121">8d0e7195-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="3e02f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e02f-122">Syntax</span></span>            | [<span data-ttu-id="3e02f-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="3e02f-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="3e02f-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="3e02f-124">Implementations</span></span>

-   [<span data-ttu-id="3e02f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3e02f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3e02f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3e02f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3e02f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3e02f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3e02f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3e02f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3e02f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3e02f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3e02f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3e02f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3e02f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3e02f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="3e02f-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e02f-132">Entry</span></span> | <span data-ttu-id="3e02f-133">Wert</span><span class="sxs-lookup"><span data-stu-id="3e02f-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3e02f-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3e02f-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e02f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e02f-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e02f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e02f-136">System-Only</span></span>            | <span data-ttu-id="3e02f-137">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-137">False</span></span>                                        |
| <span data-ttu-id="3e02f-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3e02f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="3e02f-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="3e02f-139">True</span></span>                                         |
| <span data-ttu-id="3e02f-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3e02f-140">Is Indexed</span></span>             | <span data-ttu-id="3e02f-141">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-141">False</span></span>                                        |
| <span data-ttu-id="3e02f-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3e02f-142">In Global Catalog</span></span>      | <span data-ttu-id="3e02f-143">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-143">False</span></span>                                        |
| <span data-ttu-id="3e02f-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e02f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e02f-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3e02f-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3e02f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e02f-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3e02f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e02f-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3e02f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e02f-148">Search-Flags</span></span>           | <span data-ttu-id="3e02f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e02f-149">0x00000000</span></span>                                   |
| <span data-ttu-id="3e02f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e02f-150">System-Flags</span></span>           | <span data-ttu-id="3e02f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e02f-151">0x00000010</span></span>                                   |
| <span data-ttu-id="3e02f-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3e02f-152">Classes used in</span></span>        | [<span data-ttu-id="3e02f-153">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="3e02f-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3e02f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3e02f-154">Windows Server 2003</span></span>



| <span data-ttu-id="3e02f-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e02f-155">Entry</span></span> | <span data-ttu-id="3e02f-156">Wert</span><span class="sxs-lookup"><span data-stu-id="3e02f-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3e02f-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3e02f-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e02f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e02f-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e02f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e02f-159">System-Only</span></span>            | <span data-ttu-id="3e02f-160">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-160">False</span></span>                                        |
| <span data-ttu-id="3e02f-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3e02f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="3e02f-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="3e02f-162">True</span></span>                                         |
| <span data-ttu-id="3e02f-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3e02f-163">Is Indexed</span></span>             | <span data-ttu-id="3e02f-164">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-164">False</span></span>                                        |
| <span data-ttu-id="3e02f-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3e02f-165">In Global Catalog</span></span>      | <span data-ttu-id="3e02f-166">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-166">False</span></span>                                        |
| <span data-ttu-id="3e02f-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e02f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e02f-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3e02f-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3e02f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e02f-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3e02f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e02f-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3e02f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e02f-171">Search-Flags</span></span>           | <span data-ttu-id="3e02f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e02f-172">0x00000000</span></span>                                   |
| <span data-ttu-id="3e02f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e02f-173">System-Flags</span></span>           | <span data-ttu-id="3e02f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e02f-174">0x00000010</span></span>                                   |
| <span data-ttu-id="3e02f-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3e02f-175">Classes used in</span></span>        | [<span data-ttu-id="3e02f-176">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="3e02f-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3e02f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3e02f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3e02f-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e02f-178">Entry</span></span> | <span data-ttu-id="3e02f-179">Wert</span><span class="sxs-lookup"><span data-stu-id="3e02f-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3e02f-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3e02f-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e02f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e02f-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e02f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e02f-182">System-Only</span></span>            | <span data-ttu-id="3e02f-183">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-183">False</span></span>                                        |
| <span data-ttu-id="3e02f-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3e02f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="3e02f-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="3e02f-185">True</span></span>                                         |
| <span data-ttu-id="3e02f-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3e02f-186">Is Indexed</span></span>             | <span data-ttu-id="3e02f-187">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-187">False</span></span>                                        |
| <span data-ttu-id="3e02f-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3e02f-188">In Global Catalog</span></span>      | <span data-ttu-id="3e02f-189">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-189">False</span></span>                                        |
| <span data-ttu-id="3e02f-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e02f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e02f-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3e02f-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3e02f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e02f-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3e02f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e02f-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3e02f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e02f-194">Search-Flags</span></span>           | <span data-ttu-id="3e02f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e02f-195">0x00000000</span></span>                                   |
| <span data-ttu-id="3e02f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e02f-196">System-Flags</span></span>           | <span data-ttu-id="3e02f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e02f-197">0x00000010</span></span>                                   |
| <span data-ttu-id="3e02f-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3e02f-198">Classes used in</span></span>        | [<span data-ttu-id="3e02f-199">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="3e02f-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3e02f-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e02f-200">Windows Server 2008</span></span>



| <span data-ttu-id="3e02f-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e02f-201">Entry</span></span> | <span data-ttu-id="3e02f-202">Wert</span><span class="sxs-lookup"><span data-stu-id="3e02f-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3e02f-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3e02f-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e02f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e02f-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e02f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e02f-205">System-Only</span></span>            | <span data-ttu-id="3e02f-206">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-206">False</span></span>                                        |
| <span data-ttu-id="3e02f-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3e02f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="3e02f-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="3e02f-208">True</span></span>                                         |
| <span data-ttu-id="3e02f-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3e02f-209">Is Indexed</span></span>             | <span data-ttu-id="3e02f-210">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-210">False</span></span>                                        |
| <span data-ttu-id="3e02f-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3e02f-211">In Global Catalog</span></span>      | <span data-ttu-id="3e02f-212">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-212">False</span></span>                                        |
| <span data-ttu-id="3e02f-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e02f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e02f-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3e02f-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3e02f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e02f-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3e02f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e02f-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3e02f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e02f-217">Search-Flags</span></span>           | <span data-ttu-id="3e02f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e02f-218">0x00000000</span></span>                                   |
| <span data-ttu-id="3e02f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e02f-219">System-Flags</span></span>           | <span data-ttu-id="3e02f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e02f-220">0x00000010</span></span>                                   |
| <span data-ttu-id="3e02f-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3e02f-221">Classes used in</span></span>        | [<span data-ttu-id="3e02f-222">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="3e02f-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3e02f-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3e02f-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3e02f-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e02f-224">Entry</span></span> | <span data-ttu-id="3e02f-225">Wert</span><span class="sxs-lookup"><span data-stu-id="3e02f-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3e02f-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3e02f-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e02f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e02f-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e02f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e02f-228">System-Only</span></span>            | <span data-ttu-id="3e02f-229">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-229">False</span></span>                                        |
| <span data-ttu-id="3e02f-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3e02f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="3e02f-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="3e02f-231">True</span></span>                                         |
| <span data-ttu-id="3e02f-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3e02f-232">Is Indexed</span></span>             | <span data-ttu-id="3e02f-233">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-233">False</span></span>                                        |
| <span data-ttu-id="3e02f-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3e02f-234">In Global Catalog</span></span>      | <span data-ttu-id="3e02f-235">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-235">False</span></span>                                        |
| <span data-ttu-id="3e02f-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e02f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e02f-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3e02f-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3e02f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e02f-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3e02f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e02f-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3e02f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e02f-240">Search-Flags</span></span>           | <span data-ttu-id="3e02f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e02f-241">0x00000000</span></span>                                   |
| <span data-ttu-id="3e02f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e02f-242">System-Flags</span></span>           | <span data-ttu-id="3e02f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e02f-243">0x00000010</span></span>                                   |
| <span data-ttu-id="3e02f-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3e02f-244">Classes used in</span></span>        | [<span data-ttu-id="3e02f-245">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="3e02f-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3e02f-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e02f-246">Windows Server 2012</span></span>



| <span data-ttu-id="3e02f-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e02f-247">Entry</span></span> | <span data-ttu-id="3e02f-248">Wert</span><span class="sxs-lookup"><span data-stu-id="3e02f-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3e02f-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3e02f-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e02f-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e02f-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e02f-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e02f-251">System-Only</span></span>            | <span data-ttu-id="3e02f-252">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-252">False</span></span>                                        |
| <span data-ttu-id="3e02f-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3e02f-253">Is-Single-Valued</span></span>       | <span data-ttu-id="3e02f-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="3e02f-254">True</span></span>                                         |
| <span data-ttu-id="3e02f-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3e02f-255">Is Indexed</span></span>             | <span data-ttu-id="3e02f-256">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-256">False</span></span>                                        |
| <span data-ttu-id="3e02f-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3e02f-257">In Global Catalog</span></span>      | <span data-ttu-id="3e02f-258">False</span><span class="sxs-lookup"><span data-stu-id="3e02f-258">False</span></span>                                        |
| <span data-ttu-id="3e02f-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e02f-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e02f-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3e02f-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3e02f-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e02f-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3e02f-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e02f-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3e02f-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e02f-263">Search-Flags</span></span>           | <span data-ttu-id="3e02f-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e02f-264">0x00000000</span></span>                                   |
| <span data-ttu-id="3e02f-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e02f-265">System-Flags</span></span>           | <span data-ttu-id="3e02f-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e02f-266">0x00000010</span></span>                                   |
| <span data-ttu-id="3e02f-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3e02f-267">Classes used in</span></span>        | [<span data-ttu-id="3e02f-268">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="3e02f-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





