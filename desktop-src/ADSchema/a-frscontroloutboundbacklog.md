---
title: FRS-Control-Outbound-Rückstand-Attribut
description: Warn-/fehlerlevelpaar für ausgehenden Rückstand (Anzahl der Dateien).
ms.assetid: d35b4605-c336-4ed0-af8c-da5c9534e5c2
ms.tgt_platform: multiple
keywords:
- AD-Schema für FRS-Control-Outbound-Rückstand
- Schema des frscontroloutboundrückstand-Attributs
topic_type:
- apiref
api_name:
- FRS-Control-Outbound-Backlog
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b3201f782735658a53dcb0e802106c86267df4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744361"
---
# <a name="frs-control-outbound-backlog-attribute"></a><span data-ttu-id="aeaa4-105">FRS-Control-Outbound-Rückstand-Attribut</span><span class="sxs-lookup"><span data-stu-id="aeaa4-105">FRS-Control-Outbound-Backlog attribute</span></span>

<span data-ttu-id="aeaa4-106">Warn-/fehlerlevelpaar für ausgehenden Rückstand (Anzahl der Dateien).</span><span class="sxs-lookup"><span data-stu-id="aeaa4-106">Warning/Error level pair for outbound backlog (number of files).</span></span>



| <span data-ttu-id="aeaa4-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aeaa4-107">Entry</span></span> | <span data-ttu-id="aeaa4-108">Wert</span><span class="sxs-lookup"><span data-stu-id="aeaa4-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="aeaa4-109">CN</span><span class="sxs-lookup"><span data-stu-id="aeaa4-109">CN</span></span>                | <span data-ttu-id="aeaa4-110">FRS-Control-Outbound-Rückstand</span><span class="sxs-lookup"><span data-stu-id="aeaa4-110">FRS-Control-Outbound-Backlog</span></span>                |
| <span data-ttu-id="aeaa4-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="aeaa4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="aeaa4-112">frscontroloutboundrückstand</span><span class="sxs-lookup"><span data-stu-id="aeaa4-112">fRSControlOutboundBacklog</span></span>                   |
| <span data-ttu-id="aeaa4-113">Size</span><span class="sxs-lookup"><span data-stu-id="aeaa4-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="aeaa4-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="aeaa4-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="aeaa4-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="aeaa4-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="aeaa4-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="aeaa4-116">Attribute-Id</span></span>      | <span data-ttu-id="aeaa4-117">1.2.840.113556.1.4.873</span><span class="sxs-lookup"><span data-stu-id="aeaa4-117">1.2.840.113556.1.4.873</span></span>                      |
| <span data-ttu-id="aeaa4-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="aeaa4-118">System-Id-Guid</span></span>    | <span data-ttu-id="aeaa4-119">2a13257c-9373-11d1-AEbc-0000e80367c1</span><span class="sxs-lookup"><span data-stu-id="aeaa4-119">2a13257c-9373-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="aeaa4-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="aeaa4-120">Syntax</span></span>            | [<span data-ttu-id="aeaa4-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="aeaa4-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="aeaa4-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="aeaa4-122">Implementations</span></span>

-   [<span data-ttu-id="aeaa4-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="aeaa4-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="aeaa4-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="aeaa4-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="aeaa4-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="aeaa4-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="aeaa4-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="aeaa4-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="aeaa4-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="aeaa4-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="aeaa4-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="aeaa4-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="aeaa4-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aeaa4-129">Windows 2000 Server</span></span>



| <span data-ttu-id="aeaa4-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aeaa4-130">Entry</span></span> | <span data-ttu-id="aeaa4-131">Wert</span><span class="sxs-lookup"><span data-stu-id="aeaa4-131">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="aeaa4-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aeaa4-132">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="aeaa4-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aeaa4-133">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="aeaa4-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="aeaa4-134">System-Only</span></span>            | <span data-ttu-id="aeaa4-135">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-135">False</span></span>                                            |
| <span data-ttu-id="aeaa4-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aeaa4-136">Is-Single-Valued</span></span>       | <span data-ttu-id="aeaa4-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="aeaa4-137">True</span></span>                                             |
| <span data-ttu-id="aeaa4-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aeaa4-138">Is Indexed</span></span>             | <span data-ttu-id="aeaa4-139">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-139">False</span></span>                                            |
| <span data-ttu-id="aeaa4-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aeaa4-140">In Global Catalog</span></span>      | <span data-ttu-id="aeaa4-141">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-141">False</span></span>                                            |
| <span data-ttu-id="aeaa4-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aeaa4-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="aeaa4-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aeaa4-143">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="aeaa4-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aeaa4-144">Range-Lower</span></span>            | <span data-ttu-id="aeaa4-145">0</span><span class="sxs-lookup"><span data-stu-id="aeaa4-145">0</span></span>                                                |
| <span data-ttu-id="aeaa4-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aeaa4-146">Range-Upper</span></span>            | <span data-ttu-id="aeaa4-147">32</span><span class="sxs-lookup"><span data-stu-id="aeaa4-147">32</span></span>                                               |
| <span data-ttu-id="aeaa4-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aeaa4-148">Search-Flags</span></span>           | <span data-ttu-id="aeaa4-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aeaa4-149">0x00000000</span></span>                                       |
| <span data-ttu-id="aeaa4-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aeaa4-150">System-Flags</span></span>           | <span data-ttu-id="aeaa4-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aeaa4-151">0x00000010</span></span>                                       |
| <span data-ttu-id="aeaa4-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aeaa4-152">Classes used in</span></span>        | [<span data-ttu-id="aeaa4-153">**NTFRS-Mitglied**</span><span class="sxs-lookup"><span data-stu-id="aeaa4-153">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="aeaa4-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aeaa4-154">Windows Server 2003</span></span>



| <span data-ttu-id="aeaa4-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aeaa4-155">Entry</span></span> | <span data-ttu-id="aeaa4-156">Wert</span><span class="sxs-lookup"><span data-stu-id="aeaa4-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="aeaa4-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aeaa4-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="aeaa4-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aeaa4-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="aeaa4-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="aeaa4-159">System-Only</span></span>            | <span data-ttu-id="aeaa4-160">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-160">False</span></span>                                            |
| <span data-ttu-id="aeaa4-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aeaa4-161">Is-Single-Valued</span></span>       | <span data-ttu-id="aeaa4-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="aeaa4-162">True</span></span>                                             |
| <span data-ttu-id="aeaa4-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aeaa4-163">Is Indexed</span></span>             | <span data-ttu-id="aeaa4-164">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-164">False</span></span>                                            |
| <span data-ttu-id="aeaa4-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aeaa4-165">In Global Catalog</span></span>      | <span data-ttu-id="aeaa4-166">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-166">False</span></span>                                            |
| <span data-ttu-id="aeaa4-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aeaa4-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="aeaa4-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aeaa4-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="aeaa4-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aeaa4-169">Range-Lower</span></span>            | <span data-ttu-id="aeaa4-170">0</span><span class="sxs-lookup"><span data-stu-id="aeaa4-170">0</span></span>                                                |
| <span data-ttu-id="aeaa4-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aeaa4-171">Range-Upper</span></span>            | <span data-ttu-id="aeaa4-172">32</span><span class="sxs-lookup"><span data-stu-id="aeaa4-172">32</span></span>                                               |
| <span data-ttu-id="aeaa4-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aeaa4-173">Search-Flags</span></span>           | <span data-ttu-id="aeaa4-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aeaa4-174">0x00000000</span></span>                                       |
| <span data-ttu-id="aeaa4-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aeaa4-175">System-Flags</span></span>           | <span data-ttu-id="aeaa4-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aeaa4-176">0x00000010</span></span>                                       |
| <span data-ttu-id="aeaa4-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aeaa4-177">Classes used in</span></span>        | [<span data-ttu-id="aeaa4-178">**NTFRS-Mitglied**</span><span class="sxs-lookup"><span data-stu-id="aeaa4-178">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="aeaa4-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="aeaa4-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="aeaa4-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aeaa4-180">Entry</span></span> | <span data-ttu-id="aeaa4-181">Wert</span><span class="sxs-lookup"><span data-stu-id="aeaa4-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="aeaa4-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aeaa4-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="aeaa4-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aeaa4-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="aeaa4-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="aeaa4-184">System-Only</span></span>            | <span data-ttu-id="aeaa4-185">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-185">False</span></span>                                            |
| <span data-ttu-id="aeaa4-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aeaa4-186">Is-Single-Valued</span></span>       | <span data-ttu-id="aeaa4-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="aeaa4-187">True</span></span>                                             |
| <span data-ttu-id="aeaa4-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aeaa4-188">Is Indexed</span></span>             | <span data-ttu-id="aeaa4-189">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-189">False</span></span>                                            |
| <span data-ttu-id="aeaa4-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aeaa4-190">In Global Catalog</span></span>      | <span data-ttu-id="aeaa4-191">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-191">False</span></span>                                            |
| <span data-ttu-id="aeaa4-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aeaa4-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="aeaa4-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aeaa4-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="aeaa4-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aeaa4-194">Range-Lower</span></span>            | <span data-ttu-id="aeaa4-195">0</span><span class="sxs-lookup"><span data-stu-id="aeaa4-195">0</span></span>                                                |
| <span data-ttu-id="aeaa4-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aeaa4-196">Range-Upper</span></span>            | <span data-ttu-id="aeaa4-197">32</span><span class="sxs-lookup"><span data-stu-id="aeaa4-197">32</span></span>                                               |
| <span data-ttu-id="aeaa4-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aeaa4-198">Search-Flags</span></span>           | <span data-ttu-id="aeaa4-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aeaa4-199">0x00000000</span></span>                                       |
| <span data-ttu-id="aeaa4-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aeaa4-200">System-Flags</span></span>           | <span data-ttu-id="aeaa4-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aeaa4-201">0x00000010</span></span>                                       |
| <span data-ttu-id="aeaa4-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aeaa4-202">Classes used in</span></span>        | [<span data-ttu-id="aeaa4-203">**NTFRS-Mitglied**</span><span class="sxs-lookup"><span data-stu-id="aeaa4-203">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="aeaa4-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aeaa4-204">Windows Server 2008</span></span>



| <span data-ttu-id="aeaa4-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aeaa4-205">Entry</span></span> | <span data-ttu-id="aeaa4-206">Wert</span><span class="sxs-lookup"><span data-stu-id="aeaa4-206">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="aeaa4-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aeaa4-207">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="aeaa4-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aeaa4-208">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="aeaa4-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="aeaa4-209">System-Only</span></span>            | <span data-ttu-id="aeaa4-210">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-210">False</span></span>                                            |
| <span data-ttu-id="aeaa4-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aeaa4-211">Is-Single-Valued</span></span>       | <span data-ttu-id="aeaa4-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="aeaa4-212">True</span></span>                                             |
| <span data-ttu-id="aeaa4-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aeaa4-213">Is Indexed</span></span>             | <span data-ttu-id="aeaa4-214">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-214">False</span></span>                                            |
| <span data-ttu-id="aeaa4-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aeaa4-215">In Global Catalog</span></span>      | <span data-ttu-id="aeaa4-216">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-216">False</span></span>                                            |
| <span data-ttu-id="aeaa4-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aeaa4-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="aeaa4-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aeaa4-218">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="aeaa4-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aeaa4-219">Range-Lower</span></span>            | <span data-ttu-id="aeaa4-220">0</span><span class="sxs-lookup"><span data-stu-id="aeaa4-220">0</span></span>                                                |
| <span data-ttu-id="aeaa4-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aeaa4-221">Range-Upper</span></span>            | <span data-ttu-id="aeaa4-222">32</span><span class="sxs-lookup"><span data-stu-id="aeaa4-222">32</span></span>                                               |
| <span data-ttu-id="aeaa4-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aeaa4-223">Search-Flags</span></span>           | <span data-ttu-id="aeaa4-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aeaa4-224">0x00000000</span></span>                                       |
| <span data-ttu-id="aeaa4-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aeaa4-225">System-Flags</span></span>           | <span data-ttu-id="aeaa4-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aeaa4-226">0x00000010</span></span>                                       |
| <span data-ttu-id="aeaa4-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aeaa4-227">Classes used in</span></span>        | [<span data-ttu-id="aeaa4-228">**NTFRS-Mitglied**</span><span class="sxs-lookup"><span data-stu-id="aeaa4-228">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="aeaa4-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aeaa4-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="aeaa4-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aeaa4-230">Entry</span></span> | <span data-ttu-id="aeaa4-231">Wert</span><span class="sxs-lookup"><span data-stu-id="aeaa4-231">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="aeaa4-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aeaa4-232">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="aeaa4-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aeaa4-233">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="aeaa4-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="aeaa4-234">System-Only</span></span>            | <span data-ttu-id="aeaa4-235">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-235">False</span></span>                                            |
| <span data-ttu-id="aeaa4-236">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aeaa4-236">Is-Single-Valued</span></span>       | <span data-ttu-id="aeaa4-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="aeaa4-237">True</span></span>                                             |
| <span data-ttu-id="aeaa4-238">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aeaa4-238">Is Indexed</span></span>             | <span data-ttu-id="aeaa4-239">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-239">False</span></span>                                            |
| <span data-ttu-id="aeaa4-240">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aeaa4-240">In Global Catalog</span></span>      | <span data-ttu-id="aeaa4-241">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-241">False</span></span>                                            |
| <span data-ttu-id="aeaa4-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aeaa4-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="aeaa4-243">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aeaa4-243">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="aeaa4-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aeaa4-244">Range-Lower</span></span>            | <span data-ttu-id="aeaa4-245">0</span><span class="sxs-lookup"><span data-stu-id="aeaa4-245">0</span></span>                                                |
| <span data-ttu-id="aeaa4-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aeaa4-246">Range-Upper</span></span>            | <span data-ttu-id="aeaa4-247">32</span><span class="sxs-lookup"><span data-stu-id="aeaa4-247">32</span></span>                                               |
| <span data-ttu-id="aeaa4-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aeaa4-248">Search-Flags</span></span>           | <span data-ttu-id="aeaa4-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aeaa4-249">0x00000000</span></span>                                       |
| <span data-ttu-id="aeaa4-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aeaa4-250">System-Flags</span></span>           | <span data-ttu-id="aeaa4-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aeaa4-251">0x00000010</span></span>                                       |
| <span data-ttu-id="aeaa4-252">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aeaa4-252">Classes used in</span></span>        | [<span data-ttu-id="aeaa4-253">**NTFRS-Mitglied**</span><span class="sxs-lookup"><span data-stu-id="aeaa4-253">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="aeaa4-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aeaa4-254">Windows Server 2012</span></span>



| <span data-ttu-id="aeaa4-255">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aeaa4-255">Entry</span></span> | <span data-ttu-id="aeaa4-256">Wert</span><span class="sxs-lookup"><span data-stu-id="aeaa4-256">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="aeaa4-257">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aeaa4-257">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="aeaa4-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aeaa4-258">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="aeaa4-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="aeaa4-259">System-Only</span></span>            | <span data-ttu-id="aeaa4-260">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-260">False</span></span>                                            |
| <span data-ttu-id="aeaa4-261">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aeaa4-261">Is-Single-Valued</span></span>       | <span data-ttu-id="aeaa4-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="aeaa4-262">True</span></span>                                             |
| <span data-ttu-id="aeaa4-263">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aeaa4-263">Is Indexed</span></span>             | <span data-ttu-id="aeaa4-264">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-264">False</span></span>                                            |
| <span data-ttu-id="aeaa4-265">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aeaa4-265">In Global Catalog</span></span>      | <span data-ttu-id="aeaa4-266">False</span><span class="sxs-lookup"><span data-stu-id="aeaa4-266">False</span></span>                                            |
| <span data-ttu-id="aeaa4-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aeaa4-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="aeaa4-268">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aeaa4-268">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="aeaa4-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aeaa4-269">Range-Lower</span></span>            | <span data-ttu-id="aeaa4-270">0</span><span class="sxs-lookup"><span data-stu-id="aeaa4-270">0</span></span>                                                |
| <span data-ttu-id="aeaa4-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aeaa4-271">Range-Upper</span></span>            | <span data-ttu-id="aeaa4-272">32</span><span class="sxs-lookup"><span data-stu-id="aeaa4-272">32</span></span>                                               |
| <span data-ttu-id="aeaa4-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aeaa4-273">Search-Flags</span></span>           | <span data-ttu-id="aeaa4-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aeaa4-274">0x00000000</span></span>                                       |
| <span data-ttu-id="aeaa4-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aeaa4-275">System-Flags</span></span>           | <span data-ttu-id="aeaa4-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aeaa4-276">0x00000010</span></span>                                       |
| <span data-ttu-id="aeaa4-277">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aeaa4-277">Classes used in</span></span>        | [<span data-ttu-id="aeaa4-278">**NTFRS-Mitglied**</span><span class="sxs-lookup"><span data-stu-id="aeaa4-278">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> |



 

 





