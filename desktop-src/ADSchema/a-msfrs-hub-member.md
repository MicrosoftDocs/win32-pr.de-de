---
title: MS-FRS-Hub-Member-Attribut
description: Das MS-FRS-Hub-Member-Attribut wird verwendet, um die bevorzugten NTFRS-topologieeinstellungen aufzuzeichnen.
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-FRS-Hub-Member-Attribut
- AD-Schema für msfrs-Hub-Member-Attribut
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a211c5951ac589d00c4b8c92c031c80b2d1415
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342909"
---
# <a name="ms-frs-hub-member-attribute"></a><span data-ttu-id="c1e6a-105">MS-FRS-Hub-Member-Attribut</span><span class="sxs-lookup"><span data-stu-id="c1e6a-105">ms-FRS-Hub-Member attribute</span></span>

<span data-ttu-id="c1e6a-106">Das **MS-FRS-Hub-Member-** Attribut wird verwendet, um die bevorzugten NTFRS-topologieeinstellungen aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="c1e6a-106">The **ms-FRS-Hub-Member** attribute is used to record the preferred NTFRS topology settings.</span></span> <span data-ttu-id="c1e6a-107">Wenn ein FRS-Element einer Replikat Gruppe hinzugefügt oder gelöscht wird, werden diese Attribute referenziert, und es werden entsprechende Anpassungen an den Verbindungen zwischen dem Rest der FRS-Mitglieder in der Replikat Gruppe vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="c1e6a-107">When an FRS member gets added or deleted to a replica set, these attributes are referred and appropriate adjustments are made to the connections between the rest of the FRS members in the replica set.</span></span>



| <span data-ttu-id="c1e6a-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c1e6a-108">Entry</span></span> | <span data-ttu-id="c1e6a-109">Wert</span><span class="sxs-lookup"><span data-stu-id="c1e6a-109">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c1e6a-110">CN</span><span class="sxs-lookup"><span data-stu-id="c1e6a-110">CN</span></span>                | <span data-ttu-id="c1e6a-111">MS-FRS-Hub-Member</span><span class="sxs-lookup"><span data-stu-id="c1e6a-111">ms-FRS-Hub-Member</span></span>                                                  |
| <span data-ttu-id="c1e6a-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c1e6a-112">Ldap-Display-Name</span></span> | <span data-ttu-id="c1e6a-113">msfrs-Hub-Member</span><span class="sxs-lookup"><span data-stu-id="c1e6a-113">msFRS-Hub-Member</span></span>                                                   |
| <span data-ttu-id="c1e6a-114">Size</span><span class="sxs-lookup"><span data-stu-id="c1e6a-114">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="c1e6a-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c1e6a-115">Update Privilege</span></span>  | <span data-ttu-id="c1e6a-116">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="c1e6a-116">Domain administrator</span></span>                                               |
| <span data-ttu-id="c1e6a-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="c1e6a-117">Update Frequency</span></span>  | <span data-ttu-id="c1e6a-118">Wenn die Replikat Gruppe erstellt oder die bevorzugte Topologie geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c1e6a-118">When the replica set is created or the preferred topology changes.</span></span> |
| <span data-ttu-id="c1e6a-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c1e6a-119">Attribute-Id</span></span>      | <span data-ttu-id="c1e6a-120">1.2.840.113556.1.4.1693</span><span class="sxs-lookup"><span data-stu-id="c1e6a-120">1.2.840.113556.1.4.1693</span></span>                                            |
| <span data-ttu-id="c1e6a-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c1e6a-121">System-Id-Guid</span></span>    | <span data-ttu-id="c1e6a-122">5643ff81-35b6-4ca9-9512-baf0bd0a2772</span><span class="sxs-lookup"><span data-stu-id="c1e6a-122">5643ff81-35b6-4ca9-9512-baf0bd0a2772</span></span>                               |
| <span data-ttu-id="c1e6a-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1e6a-123">Syntax</span></span>            | [<span data-ttu-id="c1e6a-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c1e6a-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                            |



## <a name="implementations"></a><span data-ttu-id="c1e6a-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="c1e6a-125">Implementations</span></span>

-   [<span data-ttu-id="c1e6a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c1e6a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c1e6a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c1e6a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c1e6a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c1e6a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c1e6a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c1e6a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c1e6a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c1e6a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c1e6a-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c1e6a-131">Windows Server 2003</span></span>



| <span data-ttu-id="c1e6a-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c1e6a-132">Entry</span></span> | <span data-ttu-id="c1e6a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="c1e6a-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c1e6a-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c1e6a-134">Link-Id</span></span>                | <span data-ttu-id="c1e6a-135">1046</span><span class="sxs-lookup"><span data-stu-id="c1e6a-135">1046</span></span>                                                      |
| <span data-ttu-id="c1e6a-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1e6a-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c1e6a-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1e6a-137">System-Only</span></span>            | <span data-ttu-id="c1e6a-138">False</span><span class="sxs-lookup"><span data-stu-id="c1e6a-138">False</span></span>                                                     |
| <span data-ttu-id="c1e6a-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c1e6a-139">Is-Single-Valued</span></span>       | <span data-ttu-id="c1e6a-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="c1e6a-140">True</span></span>                                                      |
| <span data-ttu-id="c1e6a-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c1e6a-141">Is Indexed</span></span>             | <span data-ttu-id="c1e6a-142">False</span><span class="sxs-lookup"><span data-stu-id="c1e6a-142">False</span></span>                                                     |
| <span data-ttu-id="c1e6a-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c1e6a-143">In Global Catalog</span></span>      | <span data-ttu-id="c1e6a-144">False</span><span class="sxs-lookup"><span data-stu-id="c1e6a-144">False</span></span>                                                     |
| <span data-ttu-id="c1e6a-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c1e6a-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1e6a-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c1e6a-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c1e6a-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1e6a-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c1e6a-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1e6a-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c1e6a-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e6a-149">Search-Flags</span></span>           | <span data-ttu-id="c1e6a-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1e6a-150">0x00000000</span></span>                                                |
| <span data-ttu-id="c1e6a-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e6a-151">System-Flags</span></span>           | <span data-ttu-id="c1e6a-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1e6a-152">0x00000000</span></span>                                                |
| <span data-ttu-id="c1e6a-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c1e6a-153">Classes used in</span></span>        | [<span data-ttu-id="c1e6a-154">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="c1e6a-154">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c1e6a-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c1e6a-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c1e6a-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c1e6a-156">Entry</span></span> | <span data-ttu-id="c1e6a-157">Wert</span><span class="sxs-lookup"><span data-stu-id="c1e6a-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c1e6a-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c1e6a-158">Link-Id</span></span>                | <span data-ttu-id="c1e6a-159">1046</span><span class="sxs-lookup"><span data-stu-id="c1e6a-159">1046</span></span>                                                      |
| <span data-ttu-id="c1e6a-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1e6a-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c1e6a-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1e6a-161">System-Only</span></span>            | <span data-ttu-id="c1e6a-162">False</span><span class="sxs-lookup"><span data-stu-id="c1e6a-162">False</span></span>                                                     |
| <span data-ttu-id="c1e6a-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c1e6a-163">Is-Single-Valued</span></span>       | <span data-ttu-id="c1e6a-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="c1e6a-164">True</span></span>                                                      |
| <span data-ttu-id="c1e6a-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c1e6a-165">Is Indexed</span></span>             | <span data-ttu-id="c1e6a-166">False</span><span class="sxs-lookup"><span data-stu-id="c1e6a-166">False</span></span>                                                     |
| <span data-ttu-id="c1e6a-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c1e6a-167">In Global Catalog</span></span>      | <span data-ttu-id="c1e6a-168">False</span><span class="sxs-lookup"><span data-stu-id="c1e6a-168">False</span></span>                                                     |
| <span data-ttu-id="c1e6a-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c1e6a-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1e6a-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c1e6a-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c1e6a-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1e6a-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c1e6a-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1e6a-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c1e6a-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e6a-173">Search-Flags</span></span>           | <span data-ttu-id="c1e6a-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1e6a-174">0x00000000</span></span>                                                |
| <span data-ttu-id="c1e6a-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e6a-175">System-Flags</span></span>           | <span data-ttu-id="c1e6a-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1e6a-176">0x00000000</span></span>                                                |
| <span data-ttu-id="c1e6a-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c1e6a-177">Classes used in</span></span>        | [<span data-ttu-id="c1e6a-178">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="c1e6a-178">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c1e6a-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1e6a-179">Windows Server 2008</span></span>



| <span data-ttu-id="c1e6a-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c1e6a-180">Entry</span></span> | <span data-ttu-id="c1e6a-181">Wert</span><span class="sxs-lookup"><span data-stu-id="c1e6a-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c1e6a-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c1e6a-182">Link-Id</span></span>                | <span data-ttu-id="c1e6a-183">1046</span><span class="sxs-lookup"><span data-stu-id="c1e6a-183">1046</span></span>                                                      |
| <span data-ttu-id="c1e6a-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1e6a-184">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c1e6a-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1e6a-185">System-Only</span></span>            | <span data-ttu-id="c1e6a-186">False</span><span class="sxs-lookup"><span data-stu-id="c1e6a-186">False</span></span>                                                     |
| <span data-ttu-id="c1e6a-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c1e6a-187">Is-Single-Valued</span></span>       | <span data-ttu-id="c1e6a-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="c1e6a-188">True</span></span>                                                      |
| <span data-ttu-id="c1e6a-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c1e6a-189">Is Indexed</span></span>             | <span data-ttu-id="c1e6a-190">False</span><span class="sxs-lookup"><span data-stu-id="c1e6a-190">False</span></span>                                                     |
| <span data-ttu-id="c1e6a-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c1e6a-191">In Global Catalog</span></span>      | <span data-ttu-id="c1e6a-192">False</span><span class="sxs-lookup"><span data-stu-id="c1e6a-192">False</span></span>                                                     |
| <span data-ttu-id="c1e6a-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c1e6a-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1e6a-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c1e6a-194">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c1e6a-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1e6a-195">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c1e6a-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1e6a-196">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c1e6a-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e6a-197">Search-Flags</span></span>           | <span data-ttu-id="c1e6a-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1e6a-198">0x00000000</span></span>                                                |
| <span data-ttu-id="c1e6a-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e6a-199">System-Flags</span></span>           | <span data-ttu-id="c1e6a-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1e6a-200">0x00000000</span></span>                                                |
| <span data-ttu-id="c1e6a-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c1e6a-201">Classes used in</span></span>        | [<span data-ttu-id="c1e6a-202">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="c1e6a-202">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c1e6a-203">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1e6a-203">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c1e6a-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c1e6a-204">Entry</span></span> | <span data-ttu-id="c1e6a-205">Wert</span><span class="sxs-lookup"><span data-stu-id="c1e6a-205">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c1e6a-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c1e6a-206">Link-Id</span></span>                | <span data-ttu-id="c1e6a-207">1046</span><span class="sxs-lookup"><span data-stu-id="c1e6a-207">1046</span></span>                                                      |
| <span data-ttu-id="c1e6a-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1e6a-208">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c1e6a-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1e6a-209">System-Only</span></span>            | <span data-ttu-id="c1e6a-210">False</span><span class="sxs-lookup"><span data-stu-id="c1e6a-210">False</span></span>                                                     |
| <span data-ttu-id="c1e6a-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c1e6a-211">Is-Single-Valued</span></span>       | <span data-ttu-id="c1e6a-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="c1e6a-212">True</span></span>                                                      |
| <span data-ttu-id="c1e6a-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c1e6a-213">Is Indexed</span></span>             | <span data-ttu-id="c1e6a-214">False</span><span class="sxs-lookup"><span data-stu-id="c1e6a-214">False</span></span>                                                     |
| <span data-ttu-id="c1e6a-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c1e6a-215">In Global Catalog</span></span>      | <span data-ttu-id="c1e6a-216">False</span><span class="sxs-lookup"><span data-stu-id="c1e6a-216">False</span></span>                                                     |
| <span data-ttu-id="c1e6a-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c1e6a-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1e6a-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c1e6a-218">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c1e6a-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1e6a-219">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c1e6a-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1e6a-220">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c1e6a-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e6a-221">Search-Flags</span></span>           | <span data-ttu-id="c1e6a-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1e6a-222">0x00000000</span></span>                                                |
| <span data-ttu-id="c1e6a-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e6a-223">System-Flags</span></span>           | <span data-ttu-id="c1e6a-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1e6a-224">0x00000000</span></span>                                                |
| <span data-ttu-id="c1e6a-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c1e6a-225">Classes used in</span></span>        | [<span data-ttu-id="c1e6a-226">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="c1e6a-226">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c1e6a-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c1e6a-227">Windows Server 2012</span></span>



| <span data-ttu-id="c1e6a-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c1e6a-228">Entry</span></span> | <span data-ttu-id="c1e6a-229">Wert</span><span class="sxs-lookup"><span data-stu-id="c1e6a-229">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c1e6a-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c1e6a-230">Link-Id</span></span>                | <span data-ttu-id="c1e6a-231">1046</span><span class="sxs-lookup"><span data-stu-id="c1e6a-231">1046</span></span>                                                      |
| <span data-ttu-id="c1e6a-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1e6a-232">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c1e6a-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1e6a-233">System-Only</span></span>            | <span data-ttu-id="c1e6a-234">False</span><span class="sxs-lookup"><span data-stu-id="c1e6a-234">False</span></span>                                                     |
| <span data-ttu-id="c1e6a-235">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c1e6a-235">Is-Single-Valued</span></span>       | <span data-ttu-id="c1e6a-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="c1e6a-236">True</span></span>                                                      |
| <span data-ttu-id="c1e6a-237">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c1e6a-237">Is Indexed</span></span>             | <span data-ttu-id="c1e6a-238">False</span><span class="sxs-lookup"><span data-stu-id="c1e6a-238">False</span></span>                                                     |
| <span data-ttu-id="c1e6a-239">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c1e6a-239">In Global Catalog</span></span>      | <span data-ttu-id="c1e6a-240">False</span><span class="sxs-lookup"><span data-stu-id="c1e6a-240">False</span></span>                                                     |
| <span data-ttu-id="c1e6a-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c1e6a-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1e6a-242">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c1e6a-242">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c1e6a-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1e6a-243">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c1e6a-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1e6a-244">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c1e6a-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e6a-245">Search-Flags</span></span>           | <span data-ttu-id="c1e6a-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1e6a-246">0x00000000</span></span>                                                |
| <span data-ttu-id="c1e6a-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e6a-247">System-Flags</span></span>           | <span data-ttu-id="c1e6a-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1e6a-248">0x00000000</span></span>                                                |
| <span data-ttu-id="c1e6a-249">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c1e6a-249">Classes used in</span></span>        | [<span data-ttu-id="c1e6a-250">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="c1e6a-250">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c1e6a-251">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1e6a-251">Remarks</span></span>

<span data-ttu-id="c1e6a-252">Dies ist der voll qualifizierte Distinguished Name eines [**NTFRS-Member-**](c-ntfrsmember.md) Objekts.</span><span class="sxs-lookup"><span data-stu-id="c1e6a-252">This is the fully qualified distinguished name of an [**NTFRS-Member**](c-ntfrsmember.md) object.</span></span> <span data-ttu-id="c1e6a-253">Der Distinguished Name hat das Format "CN = *<computerGuid>* , CN = *<Dfs Link Name>* , CN = *<Dfs Root name>* , CN = DFS Volumes, CN = File Replication Service, CN = System, DC =..."</span><span class="sxs-lookup"><span data-stu-id="c1e6a-253">The distinguished name is in the format of "CN=*<computerGuid>*, CN=*<Dfs Link Name>*, CN=*<Dfs Root name>*, CN=DFS Volumes, CN=File Replication Service,CN=System, DC=..."</span></span>

 

 





