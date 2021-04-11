---
title: ACS-DSBM-priority-Attribut
description: Diese Attribute enthalten die Priorität für diesen subnetzbandbreiten-Manager (SBM).
ms.assetid: 08dd49d2-a2fa-4707-8302-25566680b91d
ms.tgt_platform: multiple
keywords:
- AD-Schema des ACS-DSBM-Priority-Attributs
- acsdsbmpriority-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ACS-DSBM-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd32c9e9cca95dbd5f52569de0b61e886033d13
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123235"
---
# <a name="acs-dsbm-priority-attribute"></a><span data-ttu-id="f8ad0-105">ACS-DSBM-priority-Attribut</span><span class="sxs-lookup"><span data-stu-id="f8ad0-105">ACS-DSBM-Priority attribute</span></span>

<span data-ttu-id="f8ad0-106">Diese Attribute enthalten die Priorität für diesen subnetzbandbreiten-Manager (SBM).</span><span class="sxs-lookup"><span data-stu-id="f8ad0-106">This attributes contains the priority for this Subnet Bandwidth Manager (SBM).</span></span> <span data-ttu-id="f8ad0-107">Wenn ein neuer benannter subnetzbandbreiten-Manager (DSBM) ausgewählt werden muss, wird dieser Wert als Teil einer Nachricht zum Bereitstellen von DSBM an andere sbms in der Domäne gesendet \_ .</span><span class="sxs-lookup"><span data-stu-id="f8ad0-107">When a new Designated Subnet Bandwidth Manager (DSBM) needs to be elected, this value is sent to other SBMs in the domain as part of a DSBM\_willing message.</span></span> <span data-ttu-id="f8ad0-108">Der SBM mit der höchsten Priorität wird als neue DSBM gewählt.</span><span class="sxs-lookup"><span data-stu-id="f8ad0-108">The SBM with the highest priority is elected as the new DSBM.</span></span>



| <span data-ttu-id="f8ad0-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f8ad0-109">Entry</span></span> | <span data-ttu-id="f8ad0-110">Wert</span><span class="sxs-lookup"><span data-stu-id="f8ad0-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f8ad0-111">CN</span><span class="sxs-lookup"><span data-stu-id="f8ad0-111">CN</span></span>                | <span data-ttu-id="f8ad0-112">ACS-DSBM-Priorität</span><span class="sxs-lookup"><span data-stu-id="f8ad0-112">ACS-DSBM-Priority</span></span>                    |
| <span data-ttu-id="f8ad0-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f8ad0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f8ad0-114">acsdsbmpriority</span><span class="sxs-lookup"><span data-stu-id="f8ad0-114">aCSDSBMPriority</span></span>                      |
| <span data-ttu-id="f8ad0-115">Size</span><span class="sxs-lookup"><span data-stu-id="f8ad0-115">Size</span></span>              | <span data-ttu-id="f8ad0-116">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="f8ad0-116">4 bytes</span></span>                              |
| <span data-ttu-id="f8ad0-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f8ad0-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f8ad0-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f8ad0-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f8ad0-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f8ad0-119">Attribute-Id</span></span>      | <span data-ttu-id="f8ad0-120">1.2.840.113556.1.4.776</span><span class="sxs-lookup"><span data-stu-id="f8ad0-120">1.2.840.113556.1.4.776</span></span>               |
| <span data-ttu-id="f8ad0-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f8ad0-121">System-Id-Guid</span></span>    | <span data-ttu-id="f8ad0-122">1cb3559e-56d0-11d1-a9c6-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="f8ad0-122">1cb3559e-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="f8ad0-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8ad0-123">Syntax</span></span>            | [<span data-ttu-id="f8ad0-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="f8ad0-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="f8ad0-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f8ad0-125">Implementations</span></span>

-   [<span data-ttu-id="f8ad0-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f8ad0-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f8ad0-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f8ad0-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f8ad0-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f8ad0-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f8ad0-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f8ad0-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f8ad0-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f8ad0-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f8ad0-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f8ad0-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f8ad0-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f8ad0-132">Windows 2000 Server</span></span>



| <span data-ttu-id="f8ad0-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f8ad0-133">Entry</span></span> | <span data-ttu-id="f8ad0-134">Wert</span><span class="sxs-lookup"><span data-stu-id="f8ad0-134">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f8ad0-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f8ad0-135">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f8ad0-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8ad0-136">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f8ad0-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8ad0-137">System-Only</span></span>            | <span data-ttu-id="f8ad0-138">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-138">False</span></span>                                        |
| <span data-ttu-id="f8ad0-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f8ad0-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f8ad0-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="f8ad0-140">True</span></span>                                         |
| <span data-ttu-id="f8ad0-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f8ad0-141">Is Indexed</span></span>             | <span data-ttu-id="f8ad0-142">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-142">False</span></span>                                        |
| <span data-ttu-id="f8ad0-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f8ad0-143">In Global Catalog</span></span>      | <span data-ttu-id="f8ad0-144">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-144">False</span></span>                                        |
| <span data-ttu-id="f8ad0-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8ad0-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8ad0-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f8ad0-146">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f8ad0-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8ad0-147">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f8ad0-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8ad0-148">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f8ad0-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ad0-149">Search-Flags</span></span>           | <span data-ttu-id="f8ad0-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8ad0-150">0x00000000</span></span>                                   |
| <span data-ttu-id="f8ad0-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ad0-151">System-Flags</span></span>           | <span data-ttu-id="f8ad0-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8ad0-152">0x00000010</span></span>                                   |
| <span data-ttu-id="f8ad0-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f8ad0-153">Classes used in</span></span>        | [<span data-ttu-id="f8ad0-154">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="f8ad0-154">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f8ad0-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f8ad0-155">Windows Server 2003</span></span>



| <span data-ttu-id="f8ad0-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f8ad0-156">Entry</span></span> | <span data-ttu-id="f8ad0-157">Wert</span><span class="sxs-lookup"><span data-stu-id="f8ad0-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f8ad0-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f8ad0-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f8ad0-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8ad0-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f8ad0-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8ad0-160">System-Only</span></span>            | <span data-ttu-id="f8ad0-161">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-161">False</span></span>                                        |
| <span data-ttu-id="f8ad0-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f8ad0-162">Is-Single-Valued</span></span>       | <span data-ttu-id="f8ad0-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="f8ad0-163">True</span></span>                                         |
| <span data-ttu-id="f8ad0-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f8ad0-164">Is Indexed</span></span>             | <span data-ttu-id="f8ad0-165">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-165">False</span></span>                                        |
| <span data-ttu-id="f8ad0-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f8ad0-166">In Global Catalog</span></span>      | <span data-ttu-id="f8ad0-167">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-167">False</span></span>                                        |
| <span data-ttu-id="f8ad0-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8ad0-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8ad0-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f8ad0-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f8ad0-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8ad0-170">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f8ad0-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8ad0-171">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f8ad0-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ad0-172">Search-Flags</span></span>           | <span data-ttu-id="f8ad0-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8ad0-173">0x00000000</span></span>                                   |
| <span data-ttu-id="f8ad0-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ad0-174">System-Flags</span></span>           | <span data-ttu-id="f8ad0-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8ad0-175">0x00000010</span></span>                                   |
| <span data-ttu-id="f8ad0-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f8ad0-176">Classes used in</span></span>        | [<span data-ttu-id="f8ad0-177">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="f8ad0-177">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f8ad0-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f8ad0-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f8ad0-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f8ad0-179">Entry</span></span> | <span data-ttu-id="f8ad0-180">Wert</span><span class="sxs-lookup"><span data-stu-id="f8ad0-180">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f8ad0-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f8ad0-181">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f8ad0-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8ad0-182">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f8ad0-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8ad0-183">System-Only</span></span>            | <span data-ttu-id="f8ad0-184">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-184">False</span></span>                                        |
| <span data-ttu-id="f8ad0-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f8ad0-185">Is-Single-Valued</span></span>       | <span data-ttu-id="f8ad0-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="f8ad0-186">True</span></span>                                         |
| <span data-ttu-id="f8ad0-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f8ad0-187">Is Indexed</span></span>             | <span data-ttu-id="f8ad0-188">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-188">False</span></span>                                        |
| <span data-ttu-id="f8ad0-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f8ad0-189">In Global Catalog</span></span>      | <span data-ttu-id="f8ad0-190">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-190">False</span></span>                                        |
| <span data-ttu-id="f8ad0-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8ad0-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8ad0-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f8ad0-192">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f8ad0-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8ad0-193">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f8ad0-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8ad0-194">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f8ad0-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ad0-195">Search-Flags</span></span>           | <span data-ttu-id="f8ad0-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8ad0-196">0x00000000</span></span>                                   |
| <span data-ttu-id="f8ad0-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ad0-197">System-Flags</span></span>           | <span data-ttu-id="f8ad0-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8ad0-198">0x00000010</span></span>                                   |
| <span data-ttu-id="f8ad0-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f8ad0-199">Classes used in</span></span>        | [<span data-ttu-id="f8ad0-200">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="f8ad0-200">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f8ad0-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8ad0-201">Windows Server 2008</span></span>



| <span data-ttu-id="f8ad0-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f8ad0-202">Entry</span></span> | <span data-ttu-id="f8ad0-203">Wert</span><span class="sxs-lookup"><span data-stu-id="f8ad0-203">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f8ad0-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f8ad0-204">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f8ad0-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8ad0-205">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f8ad0-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8ad0-206">System-Only</span></span>            | <span data-ttu-id="f8ad0-207">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-207">False</span></span>                                        |
| <span data-ttu-id="f8ad0-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f8ad0-208">Is-Single-Valued</span></span>       | <span data-ttu-id="f8ad0-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="f8ad0-209">True</span></span>                                         |
| <span data-ttu-id="f8ad0-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f8ad0-210">Is Indexed</span></span>             | <span data-ttu-id="f8ad0-211">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-211">False</span></span>                                        |
| <span data-ttu-id="f8ad0-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f8ad0-212">In Global Catalog</span></span>      | <span data-ttu-id="f8ad0-213">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-213">False</span></span>                                        |
| <span data-ttu-id="f8ad0-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8ad0-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8ad0-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f8ad0-215">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f8ad0-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8ad0-216">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f8ad0-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8ad0-217">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f8ad0-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ad0-218">Search-Flags</span></span>           | <span data-ttu-id="f8ad0-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8ad0-219">0x00000000</span></span>                                   |
| <span data-ttu-id="f8ad0-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ad0-220">System-Flags</span></span>           | <span data-ttu-id="f8ad0-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8ad0-221">0x00000010</span></span>                                   |
| <span data-ttu-id="f8ad0-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f8ad0-222">Classes used in</span></span>        | [<span data-ttu-id="f8ad0-223">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="f8ad0-223">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f8ad0-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f8ad0-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f8ad0-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f8ad0-225">Entry</span></span> | <span data-ttu-id="f8ad0-226">Wert</span><span class="sxs-lookup"><span data-stu-id="f8ad0-226">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f8ad0-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f8ad0-227">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f8ad0-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8ad0-228">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f8ad0-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8ad0-229">System-Only</span></span>            | <span data-ttu-id="f8ad0-230">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-230">False</span></span>                                        |
| <span data-ttu-id="f8ad0-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f8ad0-231">Is-Single-Valued</span></span>       | <span data-ttu-id="f8ad0-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="f8ad0-232">True</span></span>                                         |
| <span data-ttu-id="f8ad0-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f8ad0-233">Is Indexed</span></span>             | <span data-ttu-id="f8ad0-234">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-234">False</span></span>                                        |
| <span data-ttu-id="f8ad0-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f8ad0-235">In Global Catalog</span></span>      | <span data-ttu-id="f8ad0-236">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-236">False</span></span>                                        |
| <span data-ttu-id="f8ad0-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8ad0-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8ad0-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f8ad0-238">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f8ad0-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8ad0-239">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f8ad0-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8ad0-240">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f8ad0-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ad0-241">Search-Flags</span></span>           | <span data-ttu-id="f8ad0-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8ad0-242">0x00000000</span></span>                                   |
| <span data-ttu-id="f8ad0-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ad0-243">System-Flags</span></span>           | <span data-ttu-id="f8ad0-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8ad0-244">0x00000010</span></span>                                   |
| <span data-ttu-id="f8ad0-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f8ad0-245">Classes used in</span></span>        | [<span data-ttu-id="f8ad0-246">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="f8ad0-246">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f8ad0-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f8ad0-247">Windows Server 2012</span></span>



| <span data-ttu-id="f8ad0-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f8ad0-248">Entry</span></span> | <span data-ttu-id="f8ad0-249">Wert</span><span class="sxs-lookup"><span data-stu-id="f8ad0-249">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f8ad0-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f8ad0-250">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f8ad0-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8ad0-251">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f8ad0-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8ad0-252">System-Only</span></span>            | <span data-ttu-id="f8ad0-253">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-253">False</span></span>                                        |
| <span data-ttu-id="f8ad0-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f8ad0-254">Is-Single-Valued</span></span>       | <span data-ttu-id="f8ad0-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="f8ad0-255">True</span></span>                                         |
| <span data-ttu-id="f8ad0-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f8ad0-256">Is Indexed</span></span>             | <span data-ttu-id="f8ad0-257">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-257">False</span></span>                                        |
| <span data-ttu-id="f8ad0-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f8ad0-258">In Global Catalog</span></span>      | <span data-ttu-id="f8ad0-259">False</span><span class="sxs-lookup"><span data-stu-id="f8ad0-259">False</span></span>                                        |
| <span data-ttu-id="f8ad0-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8ad0-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8ad0-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f8ad0-261">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f8ad0-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8ad0-262">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f8ad0-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8ad0-263">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f8ad0-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ad0-264">Search-Flags</span></span>           | <span data-ttu-id="f8ad0-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8ad0-265">0x00000000</span></span>                                   |
| <span data-ttu-id="f8ad0-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ad0-266">System-Flags</span></span>           | <span data-ttu-id="f8ad0-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8ad0-267">0x00000010</span></span>                                   |
| <span data-ttu-id="f8ad0-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f8ad0-268">Classes used in</span></span>        | [<span data-ttu-id="f8ad0-269">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="f8ad0-269">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





