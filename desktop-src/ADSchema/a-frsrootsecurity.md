---
title: FRS-root-Security-Attribut
description: Die Sicherheits Beschreibung des Replikat Gruppen Stamms für die Datei Replikation.
ms.assetid: 1db92f68-465a-4d93-ad4d-706ef4761ddc
ms.tgt_platform: multiple
keywords:
- AD-Schema des FRS-root-Security-Attributs
- Schema des frsrootsecurity-Attributs
topic_type:
- apiref
api_name:
- FRS-Root-Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a84059902998b120ad38215257fdddcb1c21ea6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344279"
---
# <a name="frs-root-security-attribute"></a><span data-ttu-id="39091-105">FRS-root-Security-Attribut</span><span class="sxs-lookup"><span data-stu-id="39091-105">FRS-Root-Security attribute</span></span>

<span data-ttu-id="39091-106">Die Sicherheits Beschreibung des Replikat Gruppen Stamms für die Datei Replikation.</span><span class="sxs-lookup"><span data-stu-id="39091-106">The security descriptor of replica set root for file replication.</span></span>



| <span data-ttu-id="39091-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39091-107">Entry</span></span> | <span data-ttu-id="39091-108">Wert</span><span class="sxs-lookup"><span data-stu-id="39091-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="39091-109">CN</span><span class="sxs-lookup"><span data-stu-id="39091-109">CN</span></span>                | <span data-ttu-id="39091-110">FRS-root-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="39091-110">FRS-Root-Security</span></span>                                   |
| <span data-ttu-id="39091-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="39091-111">Ldap-Display-Name</span></span> | <span data-ttu-id="39091-112">frsrootsecurity</span><span class="sxs-lookup"><span data-stu-id="39091-112">fRSRootSecurity</span></span>                                     |
| <span data-ttu-id="39091-113">Size</span><span class="sxs-lookup"><span data-stu-id="39091-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="39091-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="39091-114">Update Privilege</span></span>  | \-                                                  |
| <span data-ttu-id="39091-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="39091-115">Update Frequency</span></span>  | \-                                                  |
| <span data-ttu-id="39091-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="39091-116">Attribute-Id</span></span>      | <span data-ttu-id="39091-117">1.2.840.113556.1.4.535</span><span class="sxs-lookup"><span data-stu-id="39091-117">1.2.840.113556.1.4.535</span></span>                              |
| <span data-ttu-id="39091-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="39091-118">System-Id-Guid</span></span>    | <span data-ttu-id="39091-119">5245801f-ca6a-11D0-AFFF -0000f 80367c1</span><span class="sxs-lookup"><span data-stu-id="39091-119">5245801f-ca6a-11d0-afff-0000f80367c1</span></span>                |
| <span data-ttu-id="39091-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="39091-120">Syntax</span></span>            | [<span data-ttu-id="39091-121">**String(NT-Sec-Desc)**</span><span class="sxs-lookup"><span data-stu-id="39091-121">**String(NT-Sec-Desc)**</span></span>](s-string-nt-sec-desc.md) |



## <a name="implementations"></a><span data-ttu-id="39091-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="39091-122">Implementations</span></span>

-   [<span data-ttu-id="39091-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="39091-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="39091-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="39091-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="39091-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="39091-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="39091-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="39091-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="39091-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="39091-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="39091-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="39091-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="39091-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="39091-129">Windows 2000 Server</span></span>



| <span data-ttu-id="39091-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39091-130">Entry</span></span> | <span data-ttu-id="39091-131">Wert</span><span class="sxs-lookup"><span data-stu-id="39091-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39091-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39091-132">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="39091-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39091-133">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="39091-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="39091-134">System-Only</span></span>            | <span data-ttu-id="39091-135">False</span><span class="sxs-lookup"><span data-stu-id="39091-135">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39091-136">Is-Single-Valued</span></span>       | <span data-ttu-id="39091-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="39091-137">True</span></span>                                                                                                       |
| <span data-ttu-id="39091-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39091-138">Is Indexed</span></span>             | <span data-ttu-id="39091-139">False</span><span class="sxs-lookup"><span data-stu-id="39091-139">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39091-140">In Global Catalog</span></span>      | <span data-ttu-id="39091-141">False</span><span class="sxs-lookup"><span data-stu-id="39091-141">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39091-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="39091-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39091-143">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="39091-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39091-144">Range-Lower</span></span>            | <span data-ttu-id="39091-145">0</span><span class="sxs-lookup"><span data-stu-id="39091-145">0</span></span>                                                                                                          |
| <span data-ttu-id="39091-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39091-146">Range-Upper</span></span>            | <span data-ttu-id="39091-147">65.535</span><span class="sxs-lookup"><span data-stu-id="39091-147">65535</span></span>                                                                                                      |
| <span data-ttu-id="39091-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39091-148">Search-Flags</span></span>           | <span data-ttu-id="39091-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39091-149">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="39091-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39091-150">System-Flags</span></span>           | <span data-ttu-id="39091-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39091-151">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="39091-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39091-152">Classes used in</span></span>        | [<span data-ttu-id="39091-153">**NTFRS-Mitglied**</span><span class="sxs-lookup"><span data-stu-id="39091-153">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="39091-154">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="39091-154">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="39091-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="39091-155">Windows Server 2003</span></span>



| <span data-ttu-id="39091-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39091-156">Entry</span></span> | <span data-ttu-id="39091-157">Wert</span><span class="sxs-lookup"><span data-stu-id="39091-157">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39091-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39091-158">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="39091-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39091-159">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="39091-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="39091-160">System-Only</span></span>            | <span data-ttu-id="39091-161">False</span><span class="sxs-lookup"><span data-stu-id="39091-161">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39091-162">Is-Single-Valued</span></span>       | <span data-ttu-id="39091-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="39091-163">True</span></span>                                                                                                       |
| <span data-ttu-id="39091-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39091-164">Is Indexed</span></span>             | <span data-ttu-id="39091-165">False</span><span class="sxs-lookup"><span data-stu-id="39091-165">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39091-166">In Global Catalog</span></span>      | <span data-ttu-id="39091-167">False</span><span class="sxs-lookup"><span data-stu-id="39091-167">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39091-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="39091-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39091-169">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="39091-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39091-170">Range-Lower</span></span>            | <span data-ttu-id="39091-171">0</span><span class="sxs-lookup"><span data-stu-id="39091-171">0</span></span>                                                                                                          |
| <span data-ttu-id="39091-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39091-172">Range-Upper</span></span>            | <span data-ttu-id="39091-173">65.535</span><span class="sxs-lookup"><span data-stu-id="39091-173">65535</span></span>                                                                                                      |
| <span data-ttu-id="39091-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39091-174">Search-Flags</span></span>           | <span data-ttu-id="39091-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39091-175">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="39091-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39091-176">System-Flags</span></span>           | <span data-ttu-id="39091-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39091-177">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="39091-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39091-178">Classes used in</span></span>        | [<span data-ttu-id="39091-179">**NTFRS-Mitglied**</span><span class="sxs-lookup"><span data-stu-id="39091-179">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="39091-180">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="39091-180">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="39091-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="39091-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="39091-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39091-182">Entry</span></span> | <span data-ttu-id="39091-183">Wert</span><span class="sxs-lookup"><span data-stu-id="39091-183">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39091-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39091-184">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="39091-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39091-185">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="39091-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="39091-186">System-Only</span></span>            | <span data-ttu-id="39091-187">False</span><span class="sxs-lookup"><span data-stu-id="39091-187">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39091-188">Is-Single-Valued</span></span>       | <span data-ttu-id="39091-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="39091-189">True</span></span>                                                                                                       |
| <span data-ttu-id="39091-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39091-190">Is Indexed</span></span>             | <span data-ttu-id="39091-191">False</span><span class="sxs-lookup"><span data-stu-id="39091-191">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39091-192">In Global Catalog</span></span>      | <span data-ttu-id="39091-193">False</span><span class="sxs-lookup"><span data-stu-id="39091-193">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39091-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="39091-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39091-195">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="39091-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39091-196">Range-Lower</span></span>            | <span data-ttu-id="39091-197">0</span><span class="sxs-lookup"><span data-stu-id="39091-197">0</span></span>                                                                                                          |
| <span data-ttu-id="39091-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39091-198">Range-Upper</span></span>            | <span data-ttu-id="39091-199">65.535</span><span class="sxs-lookup"><span data-stu-id="39091-199">65535</span></span>                                                                                                      |
| <span data-ttu-id="39091-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39091-200">Search-Flags</span></span>           | <span data-ttu-id="39091-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39091-201">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="39091-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39091-202">System-Flags</span></span>           | <span data-ttu-id="39091-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39091-203">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="39091-204">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39091-204">Classes used in</span></span>        | [<span data-ttu-id="39091-205">**NTFRS-Mitglied**</span><span class="sxs-lookup"><span data-stu-id="39091-205">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="39091-206">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="39091-206">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="39091-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39091-207">Windows Server 2008</span></span>



| <span data-ttu-id="39091-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39091-208">Entry</span></span> | <span data-ttu-id="39091-209">Wert</span><span class="sxs-lookup"><span data-stu-id="39091-209">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39091-210">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39091-210">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="39091-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39091-211">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="39091-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="39091-212">System-Only</span></span>            | <span data-ttu-id="39091-213">False</span><span class="sxs-lookup"><span data-stu-id="39091-213">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-214">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39091-214">Is-Single-Valued</span></span>       | <span data-ttu-id="39091-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="39091-215">True</span></span>                                                                                                       |
| <span data-ttu-id="39091-216">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39091-216">Is Indexed</span></span>             | <span data-ttu-id="39091-217">False</span><span class="sxs-lookup"><span data-stu-id="39091-217">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-218">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39091-218">In Global Catalog</span></span>      | <span data-ttu-id="39091-219">False</span><span class="sxs-lookup"><span data-stu-id="39091-219">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39091-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="39091-221">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39091-221">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="39091-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39091-222">Range-Lower</span></span>            | <span data-ttu-id="39091-223">0</span><span class="sxs-lookup"><span data-stu-id="39091-223">0</span></span>                                                                                                          |
| <span data-ttu-id="39091-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39091-224">Range-Upper</span></span>            | <span data-ttu-id="39091-225">65.535</span><span class="sxs-lookup"><span data-stu-id="39091-225">65535</span></span>                                                                                                      |
| <span data-ttu-id="39091-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39091-226">Search-Flags</span></span>           | <span data-ttu-id="39091-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39091-227">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="39091-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39091-228">System-Flags</span></span>           | <span data-ttu-id="39091-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39091-229">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="39091-230">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39091-230">Classes used in</span></span>        | [<span data-ttu-id="39091-231">**NTFRS-Mitglied**</span><span class="sxs-lookup"><span data-stu-id="39091-231">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="39091-232">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="39091-232">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="39091-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39091-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="39091-234">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39091-234">Entry</span></span> | <span data-ttu-id="39091-235">Wert</span><span class="sxs-lookup"><span data-stu-id="39091-235">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39091-236">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39091-236">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="39091-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39091-237">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="39091-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="39091-238">System-Only</span></span>            | <span data-ttu-id="39091-239">False</span><span class="sxs-lookup"><span data-stu-id="39091-239">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-240">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39091-240">Is-Single-Valued</span></span>       | <span data-ttu-id="39091-241">Richtig</span><span class="sxs-lookup"><span data-stu-id="39091-241">True</span></span>                                                                                                       |
| <span data-ttu-id="39091-242">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39091-242">Is Indexed</span></span>             | <span data-ttu-id="39091-243">False</span><span class="sxs-lookup"><span data-stu-id="39091-243">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-244">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39091-244">In Global Catalog</span></span>      | <span data-ttu-id="39091-245">False</span><span class="sxs-lookup"><span data-stu-id="39091-245">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-246">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39091-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="39091-247">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39091-247">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="39091-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39091-248">Range-Lower</span></span>            | <span data-ttu-id="39091-249">0</span><span class="sxs-lookup"><span data-stu-id="39091-249">0</span></span>                                                                                                          |
| <span data-ttu-id="39091-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39091-250">Range-Upper</span></span>            | <span data-ttu-id="39091-251">65.535</span><span class="sxs-lookup"><span data-stu-id="39091-251">65535</span></span>                                                                                                      |
| <span data-ttu-id="39091-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39091-252">Search-Flags</span></span>           | <span data-ttu-id="39091-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39091-253">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="39091-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39091-254">System-Flags</span></span>           | <span data-ttu-id="39091-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39091-255">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="39091-256">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39091-256">Classes used in</span></span>        | [<span data-ttu-id="39091-257">**NTFRS-Mitglied**</span><span class="sxs-lookup"><span data-stu-id="39091-257">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="39091-258">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="39091-258">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="39091-259">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="39091-259">Windows Server 2012</span></span>



| <span data-ttu-id="39091-260">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39091-260">Entry</span></span> | <span data-ttu-id="39091-261">Wert</span><span class="sxs-lookup"><span data-stu-id="39091-261">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39091-262">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39091-262">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="39091-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39091-263">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="39091-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="39091-264">System-Only</span></span>            | <span data-ttu-id="39091-265">False</span><span class="sxs-lookup"><span data-stu-id="39091-265">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-266">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39091-266">Is-Single-Valued</span></span>       | <span data-ttu-id="39091-267">Richtig</span><span class="sxs-lookup"><span data-stu-id="39091-267">True</span></span>                                                                                                       |
| <span data-ttu-id="39091-268">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39091-268">Is Indexed</span></span>             | <span data-ttu-id="39091-269">False</span><span class="sxs-lookup"><span data-stu-id="39091-269">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-270">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39091-270">In Global Catalog</span></span>      | <span data-ttu-id="39091-271">False</span><span class="sxs-lookup"><span data-stu-id="39091-271">False</span></span>                                                                                                      |
| <span data-ttu-id="39091-272">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39091-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="39091-273">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39091-273">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="39091-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39091-274">Range-Lower</span></span>            | <span data-ttu-id="39091-275">0</span><span class="sxs-lookup"><span data-stu-id="39091-275">0</span></span>                                                                                                          |
| <span data-ttu-id="39091-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39091-276">Range-Upper</span></span>            | <span data-ttu-id="39091-277">65.535</span><span class="sxs-lookup"><span data-stu-id="39091-277">65535</span></span>                                                                                                      |
| <span data-ttu-id="39091-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39091-278">Search-Flags</span></span>           | <span data-ttu-id="39091-279">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39091-279">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="39091-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39091-280">System-Flags</span></span>           | <span data-ttu-id="39091-281">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39091-281">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="39091-282">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39091-282">Classes used in</span></span>        | [<span data-ttu-id="39091-283">**NTFRS-Mitglied**</span><span class="sxs-lookup"><span data-stu-id="39091-283">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="39091-284">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="39091-284">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





