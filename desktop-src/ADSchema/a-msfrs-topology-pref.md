---
title: MS-FRS-Topology-Pref-Attribut
description: Das MS-FRS-Topologie-Pref-Attribut wird verwendet, um die bevorzugten NTFRS-topologieeinstellungen aufzuzeichnen.
ms.assetid: 2804ad8a-bec8-491b-84ea-bdff1c8635d0
ms.tgt_platform: multiple
keywords:
- MS-FRS-Topology-Pref-Attribut AD-Schema
- msfrs-Topology-Pref-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-FRS-Topology-Pref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de417b03385e51d6a97fd68097f81bcc0cb6b9db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744665"
---
# <a name="ms-frs-topology-pref-attribute"></a><span data-ttu-id="d250f-105">MS-FRS-Topology-Pref-Attribut</span><span class="sxs-lookup"><span data-stu-id="d250f-105">ms-FRS-Topology-Pref attribute</span></span>

<span data-ttu-id="d250f-106">Das **MS-FRS-Topologie-Pref-** Attribut wird verwendet, um die bevorzugten NTFRS-topologieeinstellungen aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="d250f-106">The **ms-FRS-Topology-Pref** attribute is used to record the preferred NTFRS topology settings.</span></span> <span data-ttu-id="d250f-107">Wenn ein FRS-Mitglied der Replikat Gruppe hinzugefügt oder gelöscht wird, werden diese Attribute und Anpassungen an den Verbindungen zwischen den restlichen FRS-Mitgliedern in der Replikat Gruppe vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="d250f-107">When an FRS member gets added or deleted to the replica set, these attributes are referred, and adjustments made to the connections between the rest of the FRS members in the replica set.</span></span>

<span data-ttu-id="d250f-108">Gültige Werte für dieses Attribut sind wie folgt.</span><span class="sxs-lookup"><span data-stu-id="d250f-108">Valid values for this attribute are as follows.</span></span>

| <span data-ttu-id="d250f-109">Wert</span><span class="sxs-lookup"><span data-stu-id="d250f-109">Value</span></span> | <span data-ttu-id="d250f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d250f-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="d250f-111">1</span><span class="sxs-lookup"><span data-stu-id="d250f-111">1</span></span>     | <span data-ttu-id="d250f-112">FRS \_ rstopologypref- \_ Ring</span><span class="sxs-lookup"><span data-stu-id="d250f-112">FRS\_RSTOPOLOGYPREF\_RING</span></span><br/>     |
| <span data-ttu-id="d250f-113">2</span><span class="sxs-lookup"><span data-stu-id="d250f-113">2</span></span>     | <span data-ttu-id="d250f-114">FRS \_ rstopologypref \_ hubgesprochen</span><span class="sxs-lookup"><span data-stu-id="d250f-114">FRS\_RSTOPOLOGYPREF\_HUBSPOKE</span></span><br/> |
| <span data-ttu-id="d250f-115">3</span><span class="sxs-lookup"><span data-stu-id="d250f-115">3</span></span>     | <span data-ttu-id="d250f-116">FRS \_ rstopologypref \_ FullMesh</span><span class="sxs-lookup"><span data-stu-id="d250f-116">FRS\_RSTOPOLOGYPREF\_FULLMESH</span></span><br/> |
| <span data-ttu-id="d250f-117">4</span><span class="sxs-lookup"><span data-stu-id="d250f-117">4</span></span>     | <span data-ttu-id="d250f-118">FRS \_ rstopologypref \_ Benutzer definiert</span><span class="sxs-lookup"><span data-stu-id="d250f-118">FRS\_RSTOPOLOGYPREF\_CUSTOM</span></span><br/>   |



 



| <span data-ttu-id="d250f-119">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d250f-119">Entry</span></span> | <span data-ttu-id="d250f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d250f-120">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d250f-121">CN</span><span class="sxs-lookup"><span data-stu-id="d250f-121">CN</span></span>                | <span data-ttu-id="d250f-122">MS-FRS-Topology-Pref</span><span class="sxs-lookup"><span data-stu-id="d250f-122">ms-FRS-Topology-Pref</span></span>                                               |
| <span data-ttu-id="d250f-123">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d250f-123">Ldap-Display-Name</span></span> | <span data-ttu-id="d250f-124">msfrs-Topology-Pref</span><span class="sxs-lookup"><span data-stu-id="d250f-124">msFRS-Topology-Pref</span></span>                                                |
| <span data-ttu-id="d250f-125">Size</span><span class="sxs-lookup"><span data-stu-id="d250f-125">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="d250f-126">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d250f-126">Update Privilege</span></span>  | <span data-ttu-id="d250f-127">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="d250f-127">Domain administrator</span></span>                                               |
| <span data-ttu-id="d250f-128">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="d250f-128">Update Frequency</span></span>  | <span data-ttu-id="d250f-129">Wenn die Replikat Gruppe erstellt oder die bevorzugte Topologie geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d250f-129">When the replica set is created or the preferred topology changes.</span></span> |
| <span data-ttu-id="d250f-130">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d250f-130">Attribute-Id</span></span>      | <span data-ttu-id="d250f-131">1.2.840.113556.1.4.1692</span><span class="sxs-lookup"><span data-stu-id="d250f-131">1.2.840.113556.1.4.1692</span></span>                                            |
| <span data-ttu-id="d250f-132">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d250f-132">System-Id-Guid</span></span>    | <span data-ttu-id="d250f-133">92aa27e0-5c50-402d-9ec1-ee847def9788</span><span class="sxs-lookup"><span data-stu-id="d250f-133">92aa27e0-5c50-402d-9ec1-ee847def9788</span></span>                               |
| <span data-ttu-id="d250f-134">Syntax</span><span class="sxs-lookup"><span data-stu-id="d250f-134">Syntax</span></span>            | [<span data-ttu-id="d250f-135">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d250f-135">**String(Unicode)**</span></span>](s-string-unicode.md)                        |



## <a name="implementations"></a><span data-ttu-id="d250f-136">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="d250f-136">Implementations</span></span>

-   [<span data-ttu-id="d250f-137">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d250f-137">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d250f-138">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d250f-138">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d250f-139">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d250f-139">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d250f-140">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d250f-140">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d250f-141">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d250f-141">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d250f-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d250f-142">Windows Server 2003</span></span>



| <span data-ttu-id="d250f-143">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d250f-143">Entry</span></span> | <span data-ttu-id="d250f-144">Wert</span><span class="sxs-lookup"><span data-stu-id="d250f-144">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d250f-145">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d250f-145">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d250f-146">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d250f-146">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d250f-147">System-Only</span><span class="sxs-lookup"><span data-stu-id="d250f-147">System-Only</span></span>            | <span data-ttu-id="d250f-148">False</span><span class="sxs-lookup"><span data-stu-id="d250f-148">False</span></span>                                                     |
| <span data-ttu-id="d250f-149">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d250f-149">Is-Single-Valued</span></span>       | <span data-ttu-id="d250f-150">Richtig</span><span class="sxs-lookup"><span data-stu-id="d250f-150">True</span></span>                                                      |
| <span data-ttu-id="d250f-151">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d250f-151">Is Indexed</span></span>             | <span data-ttu-id="d250f-152">False</span><span class="sxs-lookup"><span data-stu-id="d250f-152">False</span></span>                                                     |
| <span data-ttu-id="d250f-153">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d250f-153">In Global Catalog</span></span>      | <span data-ttu-id="d250f-154">False</span><span class="sxs-lookup"><span data-stu-id="d250f-154">False</span></span>                                                     |
| <span data-ttu-id="d250f-155">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d250f-155">NT-Security-Descriptor</span></span> | <span data-ttu-id="d250f-156">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d250f-156">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d250f-157">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d250f-157">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d250f-158">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d250f-158">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d250f-159">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d250f-159">Search-Flags</span></span>           | <span data-ttu-id="d250f-160">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d250f-160">0x00000000</span></span>                                                |
| <span data-ttu-id="d250f-161">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d250f-161">System-Flags</span></span>           | <span data-ttu-id="d250f-162">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d250f-162">0x00000000</span></span>                                                |
| <span data-ttu-id="d250f-163">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d250f-163">Classes used in</span></span>        | [<span data-ttu-id="d250f-164">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="d250f-164">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d250f-165">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d250f-165">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d250f-166">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d250f-166">Entry</span></span> | <span data-ttu-id="d250f-167">Wert</span><span class="sxs-lookup"><span data-stu-id="d250f-167">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d250f-168">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d250f-168">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d250f-169">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d250f-169">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d250f-170">System-Only</span><span class="sxs-lookup"><span data-stu-id="d250f-170">System-Only</span></span>            | <span data-ttu-id="d250f-171">False</span><span class="sxs-lookup"><span data-stu-id="d250f-171">False</span></span>                                                     |
| <span data-ttu-id="d250f-172">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d250f-172">Is-Single-Valued</span></span>       | <span data-ttu-id="d250f-173">Richtig</span><span class="sxs-lookup"><span data-stu-id="d250f-173">True</span></span>                                                      |
| <span data-ttu-id="d250f-174">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d250f-174">Is Indexed</span></span>             | <span data-ttu-id="d250f-175">False</span><span class="sxs-lookup"><span data-stu-id="d250f-175">False</span></span>                                                     |
| <span data-ttu-id="d250f-176">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d250f-176">In Global Catalog</span></span>      | <span data-ttu-id="d250f-177">False</span><span class="sxs-lookup"><span data-stu-id="d250f-177">False</span></span>                                                     |
| <span data-ttu-id="d250f-178">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d250f-178">NT-Security-Descriptor</span></span> | <span data-ttu-id="d250f-179">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d250f-179">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d250f-180">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d250f-180">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d250f-181">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d250f-181">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d250f-182">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d250f-182">Search-Flags</span></span>           | <span data-ttu-id="d250f-183">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d250f-183">0x00000000</span></span>                                                |
| <span data-ttu-id="d250f-184">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d250f-184">System-Flags</span></span>           | <span data-ttu-id="d250f-185">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d250f-185">0x00000000</span></span>                                                |
| <span data-ttu-id="d250f-186">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d250f-186">Classes used in</span></span>        | [<span data-ttu-id="d250f-187">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="d250f-187">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d250f-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d250f-188">Windows Server 2008</span></span>



| <span data-ttu-id="d250f-189">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d250f-189">Entry</span></span> | <span data-ttu-id="d250f-190">Wert</span><span class="sxs-lookup"><span data-stu-id="d250f-190">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d250f-191">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d250f-191">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d250f-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d250f-192">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d250f-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="d250f-193">System-Only</span></span>            | <span data-ttu-id="d250f-194">False</span><span class="sxs-lookup"><span data-stu-id="d250f-194">False</span></span>                                                     |
| <span data-ttu-id="d250f-195">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d250f-195">Is-Single-Valued</span></span>       | <span data-ttu-id="d250f-196">Richtig</span><span class="sxs-lookup"><span data-stu-id="d250f-196">True</span></span>                                                      |
| <span data-ttu-id="d250f-197">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d250f-197">Is Indexed</span></span>             | <span data-ttu-id="d250f-198">False</span><span class="sxs-lookup"><span data-stu-id="d250f-198">False</span></span>                                                     |
| <span data-ttu-id="d250f-199">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d250f-199">In Global Catalog</span></span>      | <span data-ttu-id="d250f-200">False</span><span class="sxs-lookup"><span data-stu-id="d250f-200">False</span></span>                                                     |
| <span data-ttu-id="d250f-201">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d250f-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="d250f-202">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d250f-202">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d250f-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d250f-203">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d250f-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d250f-204">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d250f-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d250f-205">Search-Flags</span></span>           | <span data-ttu-id="d250f-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d250f-206">0x00000000</span></span>                                                |
| <span data-ttu-id="d250f-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d250f-207">System-Flags</span></span>           | <span data-ttu-id="d250f-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d250f-208">0x00000000</span></span>                                                |
| <span data-ttu-id="d250f-209">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d250f-209">Classes used in</span></span>        | [<span data-ttu-id="d250f-210">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="d250f-210">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d250f-211">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d250f-211">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d250f-212">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d250f-212">Entry</span></span> | <span data-ttu-id="d250f-213">Wert</span><span class="sxs-lookup"><span data-stu-id="d250f-213">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d250f-214">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d250f-214">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d250f-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d250f-215">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d250f-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="d250f-216">System-Only</span></span>            | <span data-ttu-id="d250f-217">False</span><span class="sxs-lookup"><span data-stu-id="d250f-217">False</span></span>                                                     |
| <span data-ttu-id="d250f-218">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d250f-218">Is-Single-Valued</span></span>       | <span data-ttu-id="d250f-219">Richtig</span><span class="sxs-lookup"><span data-stu-id="d250f-219">True</span></span>                                                      |
| <span data-ttu-id="d250f-220">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d250f-220">Is Indexed</span></span>             | <span data-ttu-id="d250f-221">False</span><span class="sxs-lookup"><span data-stu-id="d250f-221">False</span></span>                                                     |
| <span data-ttu-id="d250f-222">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d250f-222">In Global Catalog</span></span>      | <span data-ttu-id="d250f-223">False</span><span class="sxs-lookup"><span data-stu-id="d250f-223">False</span></span>                                                     |
| <span data-ttu-id="d250f-224">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d250f-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="d250f-225">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d250f-225">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d250f-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d250f-226">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d250f-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d250f-227">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d250f-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d250f-228">Search-Flags</span></span>           | <span data-ttu-id="d250f-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d250f-229">0x00000000</span></span>                                                |
| <span data-ttu-id="d250f-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d250f-230">System-Flags</span></span>           | <span data-ttu-id="d250f-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d250f-231">0x00000000</span></span>                                                |
| <span data-ttu-id="d250f-232">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d250f-232">Classes used in</span></span>        | [<span data-ttu-id="d250f-233">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="d250f-233">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d250f-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d250f-234">Windows Server 2012</span></span>



| <span data-ttu-id="d250f-235">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d250f-235">Entry</span></span> | <span data-ttu-id="d250f-236">Wert</span><span class="sxs-lookup"><span data-stu-id="d250f-236">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d250f-237">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d250f-237">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d250f-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d250f-238">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d250f-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="d250f-239">System-Only</span></span>            | <span data-ttu-id="d250f-240">False</span><span class="sxs-lookup"><span data-stu-id="d250f-240">False</span></span>                                                     |
| <span data-ttu-id="d250f-241">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d250f-241">Is-Single-Valued</span></span>       | <span data-ttu-id="d250f-242">Richtig</span><span class="sxs-lookup"><span data-stu-id="d250f-242">True</span></span>                                                      |
| <span data-ttu-id="d250f-243">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d250f-243">Is Indexed</span></span>             | <span data-ttu-id="d250f-244">False</span><span class="sxs-lookup"><span data-stu-id="d250f-244">False</span></span>                                                     |
| <span data-ttu-id="d250f-245">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d250f-245">In Global Catalog</span></span>      | <span data-ttu-id="d250f-246">False</span><span class="sxs-lookup"><span data-stu-id="d250f-246">False</span></span>                                                     |
| <span data-ttu-id="d250f-247">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d250f-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="d250f-248">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d250f-248">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d250f-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d250f-249">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d250f-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d250f-250">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d250f-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d250f-251">Search-Flags</span></span>           | <span data-ttu-id="d250f-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d250f-252">0x00000000</span></span>                                                |
| <span data-ttu-id="d250f-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d250f-253">System-Flags</span></span>           | <span data-ttu-id="d250f-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d250f-254">0x00000000</span></span>                                                |
| <span data-ttu-id="d250f-255">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d250f-255">Classes used in</span></span>        | [<span data-ttu-id="d250f-256">**NTFRS-Replikat Satz**</span><span class="sxs-lookup"><span data-stu-id="d250f-256">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





