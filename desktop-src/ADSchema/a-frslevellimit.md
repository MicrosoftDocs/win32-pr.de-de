---
title: FRS-Limit (Attribut)
description: Die Tiefe der Verzeichnisstruktur für die Replikation bei der Datei Replikation begrenzen.
ms.assetid: e2916cbd-1ce7-4ff7-82a2-5fbdae3c6a1b
ms.tgt_platform: multiple
keywords:
- AD-Schema der FRS-Ebene-Limit
- frslevellimit-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- FRS-Level-Limit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c587565eb10014ef638a2320dd9229d8409ba06
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342682"
---
# <a name="frs-level-limit-attribute"></a><span data-ttu-id="1f75f-105">FRS-Limit (Attribut)</span><span class="sxs-lookup"><span data-stu-id="1f75f-105">FRS-Level-Limit attribute</span></span>

<span data-ttu-id="1f75f-106">Die Tiefe der Verzeichnisstruktur für die Replikation bei der Datei Replikation begrenzen.</span><span class="sxs-lookup"><span data-stu-id="1f75f-106">Limit depth of directory tree to replicate for file replication.</span></span>



| <span data-ttu-id="1f75f-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1f75f-107">Entry</span></span> | <span data-ttu-id="1f75f-108">Wert</span><span class="sxs-lookup"><span data-stu-id="1f75f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1f75f-109">CN</span><span class="sxs-lookup"><span data-stu-id="1f75f-109">CN</span></span>                | <span data-ttu-id="1f75f-110">Limit für FRS-Ebene</span><span class="sxs-lookup"><span data-stu-id="1f75f-110">FRS-Level-Limit</span></span>                      |
| <span data-ttu-id="1f75f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1f75f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1f75f-112">frslevellimit</span><span class="sxs-lookup"><span data-stu-id="1f75f-112">fRSLevelLimit</span></span>                        |
| <span data-ttu-id="1f75f-113">Size</span><span class="sxs-lookup"><span data-stu-id="1f75f-113">Size</span></span>              | <span data-ttu-id="1f75f-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="1f75f-114">4 bytes</span></span>                              |
| <span data-ttu-id="1f75f-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="1f75f-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="1f75f-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="1f75f-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="1f75f-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1f75f-117">Attribute-Id</span></span>      | <span data-ttu-id="1f75f-118">1.2.840.113556.1.4.534</span><span class="sxs-lookup"><span data-stu-id="1f75f-118">1.2.840.113556.1.4.534</span></span>               |
| <span data-ttu-id="1f75f-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1f75f-119">System-Id-Guid</span></span>    | <span data-ttu-id="1f75f-120">5245801e-ca6a-11D0-AFFF -0000f 80367c1</span><span class="sxs-lookup"><span data-stu-id="1f75f-120">5245801e-ca6a-11d0-afff-0000f80367c1</span></span> |
| <span data-ttu-id="1f75f-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f75f-121">Syntax</span></span>            | [<span data-ttu-id="1f75f-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="1f75f-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="1f75f-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="1f75f-123">Implementations</span></span>

-   [<span data-ttu-id="1f75f-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1f75f-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1f75f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1f75f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1f75f-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1f75f-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1f75f-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1f75f-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1f75f-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1f75f-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1f75f-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1f75f-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1f75f-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1f75f-130">Windows 2000 Server</span></span>



| <span data-ttu-id="1f75f-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1f75f-131">Entry</span></span> | <span data-ttu-id="1f75f-132">Wert</span><span class="sxs-lookup"><span data-stu-id="1f75f-132">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1f75f-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1f75f-133">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1f75f-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f75f-134">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1f75f-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f75f-135">System-Only</span></span>            | <span data-ttu-id="1f75f-136">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-136">False</span></span>                                                     |
| <span data-ttu-id="1f75f-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1f75f-137">Is-Single-Valued</span></span>       | <span data-ttu-id="1f75f-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="1f75f-138">True</span></span>                                                      |
| <span data-ttu-id="1f75f-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1f75f-139">Is Indexed</span></span>             | <span data-ttu-id="1f75f-140">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-140">False</span></span>                                                     |
| <span data-ttu-id="1f75f-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1f75f-141">In Global Catalog</span></span>      | <span data-ttu-id="1f75f-142">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-142">False</span></span>                                                     |
| <span data-ttu-id="1f75f-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1f75f-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f75f-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1f75f-144">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1f75f-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f75f-145">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1f75f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f75f-146">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1f75f-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f75f-147">Search-Flags</span></span>           | <span data-ttu-id="1f75f-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f75f-148">0x00000000</span></span>                                                |
| <span data-ttu-id="1f75f-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f75f-149">System-Flags</span></span>           | <span data-ttu-id="1f75f-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f75f-150">0x00000010</span></span>                                                |
| <span data-ttu-id="1f75f-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1f75f-151">Classes used in</span></span>        | [<span data-ttu-id="1f75f-152">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="1f75f-152">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1f75f-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1f75f-153">Windows Server 2003</span></span>



| <span data-ttu-id="1f75f-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1f75f-154">Entry</span></span> | <span data-ttu-id="1f75f-155">Wert</span><span class="sxs-lookup"><span data-stu-id="1f75f-155">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1f75f-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1f75f-156">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1f75f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f75f-157">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1f75f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f75f-158">System-Only</span></span>            | <span data-ttu-id="1f75f-159">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-159">False</span></span>                                                     |
| <span data-ttu-id="1f75f-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1f75f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="1f75f-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="1f75f-161">True</span></span>                                                      |
| <span data-ttu-id="1f75f-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1f75f-162">Is Indexed</span></span>             | <span data-ttu-id="1f75f-163">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-163">False</span></span>                                                     |
| <span data-ttu-id="1f75f-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1f75f-164">In Global Catalog</span></span>      | <span data-ttu-id="1f75f-165">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-165">False</span></span>                                                     |
| <span data-ttu-id="1f75f-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1f75f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f75f-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1f75f-167">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1f75f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f75f-168">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1f75f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f75f-169">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1f75f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f75f-170">Search-Flags</span></span>           | <span data-ttu-id="1f75f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f75f-171">0x00000000</span></span>                                                |
| <span data-ttu-id="1f75f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f75f-172">System-Flags</span></span>           | <span data-ttu-id="1f75f-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f75f-173">0x00000010</span></span>                                                |
| <span data-ttu-id="1f75f-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1f75f-174">Classes used in</span></span>        | [<span data-ttu-id="1f75f-175">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="1f75f-175">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1f75f-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1f75f-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1f75f-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1f75f-177">Entry</span></span> | <span data-ttu-id="1f75f-178">Wert</span><span class="sxs-lookup"><span data-stu-id="1f75f-178">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1f75f-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1f75f-179">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1f75f-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f75f-180">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1f75f-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f75f-181">System-Only</span></span>            | <span data-ttu-id="1f75f-182">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-182">False</span></span>                                                     |
| <span data-ttu-id="1f75f-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1f75f-183">Is-Single-Valued</span></span>       | <span data-ttu-id="1f75f-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="1f75f-184">True</span></span>                                                      |
| <span data-ttu-id="1f75f-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1f75f-185">Is Indexed</span></span>             | <span data-ttu-id="1f75f-186">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-186">False</span></span>                                                     |
| <span data-ttu-id="1f75f-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1f75f-187">In Global Catalog</span></span>      | <span data-ttu-id="1f75f-188">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-188">False</span></span>                                                     |
| <span data-ttu-id="1f75f-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1f75f-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f75f-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1f75f-190">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1f75f-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f75f-191">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1f75f-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f75f-192">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1f75f-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f75f-193">Search-Flags</span></span>           | <span data-ttu-id="1f75f-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f75f-194">0x00000000</span></span>                                                |
| <span data-ttu-id="1f75f-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f75f-195">System-Flags</span></span>           | <span data-ttu-id="1f75f-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f75f-196">0x00000010</span></span>                                                |
| <span data-ttu-id="1f75f-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1f75f-197">Classes used in</span></span>        | [<span data-ttu-id="1f75f-198">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="1f75f-198">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1f75f-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f75f-199">Windows Server 2008</span></span>



| <span data-ttu-id="1f75f-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1f75f-200">Entry</span></span> | <span data-ttu-id="1f75f-201">Wert</span><span class="sxs-lookup"><span data-stu-id="1f75f-201">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1f75f-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1f75f-202">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1f75f-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f75f-203">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1f75f-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f75f-204">System-Only</span></span>            | <span data-ttu-id="1f75f-205">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-205">False</span></span>                                                     |
| <span data-ttu-id="1f75f-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1f75f-206">Is-Single-Valued</span></span>       | <span data-ttu-id="1f75f-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="1f75f-207">True</span></span>                                                      |
| <span data-ttu-id="1f75f-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1f75f-208">Is Indexed</span></span>             | <span data-ttu-id="1f75f-209">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-209">False</span></span>                                                     |
| <span data-ttu-id="1f75f-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1f75f-210">In Global Catalog</span></span>      | <span data-ttu-id="1f75f-211">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-211">False</span></span>                                                     |
| <span data-ttu-id="1f75f-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1f75f-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f75f-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1f75f-213">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1f75f-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f75f-214">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1f75f-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f75f-215">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1f75f-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f75f-216">Search-Flags</span></span>           | <span data-ttu-id="1f75f-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f75f-217">0x00000000</span></span>                                                |
| <span data-ttu-id="1f75f-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f75f-218">System-Flags</span></span>           | <span data-ttu-id="1f75f-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f75f-219">0x00000010</span></span>                                                |
| <span data-ttu-id="1f75f-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1f75f-220">Classes used in</span></span>        | [<span data-ttu-id="1f75f-221">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="1f75f-221">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1f75f-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1f75f-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1f75f-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1f75f-223">Entry</span></span> | <span data-ttu-id="1f75f-224">Wert</span><span class="sxs-lookup"><span data-stu-id="1f75f-224">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1f75f-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1f75f-225">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1f75f-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f75f-226">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1f75f-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f75f-227">System-Only</span></span>            | <span data-ttu-id="1f75f-228">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-228">False</span></span>                                                     |
| <span data-ttu-id="1f75f-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1f75f-229">Is-Single-Valued</span></span>       | <span data-ttu-id="1f75f-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="1f75f-230">True</span></span>                                                      |
| <span data-ttu-id="1f75f-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1f75f-231">Is Indexed</span></span>             | <span data-ttu-id="1f75f-232">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-232">False</span></span>                                                     |
| <span data-ttu-id="1f75f-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1f75f-233">In Global Catalog</span></span>      | <span data-ttu-id="1f75f-234">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-234">False</span></span>                                                     |
| <span data-ttu-id="1f75f-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1f75f-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f75f-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1f75f-236">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1f75f-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f75f-237">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1f75f-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f75f-238">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1f75f-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f75f-239">Search-Flags</span></span>           | <span data-ttu-id="1f75f-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f75f-240">0x00000000</span></span>                                                |
| <span data-ttu-id="1f75f-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f75f-241">System-Flags</span></span>           | <span data-ttu-id="1f75f-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f75f-242">0x00000010</span></span>                                                |
| <span data-ttu-id="1f75f-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1f75f-243">Classes used in</span></span>        | [<span data-ttu-id="1f75f-244">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="1f75f-244">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1f75f-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1f75f-245">Windows Server 2012</span></span>



| <span data-ttu-id="1f75f-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1f75f-246">Entry</span></span> | <span data-ttu-id="1f75f-247">Wert</span><span class="sxs-lookup"><span data-stu-id="1f75f-247">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1f75f-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1f75f-248">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1f75f-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f75f-249">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1f75f-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f75f-250">System-Only</span></span>            | <span data-ttu-id="1f75f-251">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-251">False</span></span>                                                     |
| <span data-ttu-id="1f75f-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1f75f-252">Is-Single-Valued</span></span>       | <span data-ttu-id="1f75f-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="1f75f-253">True</span></span>                                                      |
| <span data-ttu-id="1f75f-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1f75f-254">Is Indexed</span></span>             | <span data-ttu-id="1f75f-255">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-255">False</span></span>                                                     |
| <span data-ttu-id="1f75f-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1f75f-256">In Global Catalog</span></span>      | <span data-ttu-id="1f75f-257">False</span><span class="sxs-lookup"><span data-stu-id="1f75f-257">False</span></span>                                                     |
| <span data-ttu-id="1f75f-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1f75f-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f75f-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1f75f-259">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1f75f-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f75f-260">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1f75f-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f75f-261">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1f75f-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f75f-262">Search-Flags</span></span>           | <span data-ttu-id="1f75f-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f75f-263">0x00000000</span></span>                                                |
| <span data-ttu-id="1f75f-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f75f-264">System-Flags</span></span>           | <span data-ttu-id="1f75f-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f75f-265">0x00000010</span></span>                                                |
| <span data-ttu-id="1f75f-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1f75f-266">Classes used in</span></span>        | [<span data-ttu-id="1f75f-267">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="1f75f-267">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





