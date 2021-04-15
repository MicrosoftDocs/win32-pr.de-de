---
title: Schema-Info-Attribut
description: Ein interner binärer Wert, der verwendet wird, um Schema Änderungen zwischen DCS zu erkennen und einen Schema-NC-Replikations Durchlauf vor der Replikation anderer NC- Wird zum Auflösen von Verknüpfungen verwendet, wenn das Schema FSMO übernommen wird und eine Änderung an mehr als einem DC vorgenommen wird.
ms.assetid: 416cef3f-211b-439d-b177-267806c6a5d2
ms.tgt_platform: multiple
keywords:
- AD-Schema für Schema-Info-Attribut
- Schema des Schema Info-Attributs AD
topic_type:
- apiref
api_name:
- Schema-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca55fc8ad3f53709b3819a7333e3470a1ac35cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104520023"
---
# <a name="schema-info-attribute"></a><span data-ttu-id="f6fb4-106">Schema-Info-Attribut</span><span class="sxs-lookup"><span data-stu-id="f6fb4-106">Schema-Info attribute</span></span>

<span data-ttu-id="f6fb4-107">Ein interner binärer Wert, der verwendet wird, um Schema Änderungen zwischen DCS zu erkennen und einen Schema-NC-Replikations Durchlauf vor der Replikation anderer NC-</span><span class="sxs-lookup"><span data-stu-id="f6fb4-107">An internal binary value used to detect schema changes between DCs and force a schema NC replication cycle before replicating any other NC.</span></span> <span data-ttu-id="f6fb4-108">Wird zum Auflösen von Verknüpfungen verwendet, wenn das Schema FSMO übernommen wird und eine Änderung an mehr als einem DC vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="f6fb4-108">Used to resolve ties when the schema FSMO is seized and a change is made on more than one DC.</span></span>



| <span data-ttu-id="f6fb4-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f6fb4-109">Entry</span></span> | <span data-ttu-id="f6fb4-110">Wert</span><span class="sxs-lookup"><span data-stu-id="f6fb4-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="f6fb4-111">CN</span><span class="sxs-lookup"><span data-stu-id="f6fb4-111">CN</span></span>                | <span data-ttu-id="f6fb4-112">Schema-Info</span><span class="sxs-lookup"><span data-stu-id="f6fb4-112">Schema-Info</span></span>                                           |
| <span data-ttu-id="f6fb4-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f6fb4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f6fb4-114">Schema Info</span><span class="sxs-lookup"><span data-stu-id="f6fb4-114">schemaInfo</span></span>                                            |
| <span data-ttu-id="f6fb4-115">Size</span><span class="sxs-lookup"><span data-stu-id="f6fb4-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="f6fb4-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f6fb4-116">Update Privilege</span></span>  | <span data-ttu-id="f6fb4-117">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f6fb4-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="f6fb4-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f6fb4-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="f6fb4-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f6fb4-119">Attribute-Id</span></span>      | <span data-ttu-id="f6fb4-120">1.2.840.113556.1.4.1358</span><span class="sxs-lookup"><span data-stu-id="f6fb4-120">1.2.840.113556.1.4.1358</span></span>                               |
| <span data-ttu-id="f6fb4-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f6fb4-121">System-Id-Guid</span></span>    | <span data-ttu-id="f6fb4-122">f9fb64ae-93b4-11d2-9945-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="f6fb4-122">f9fb64ae-93b4-11d2-9945-0000f87a57d4</span></span>                  |
| <span data-ttu-id="f6fb4-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6fb4-123">Syntax</span></span>            | [<span data-ttu-id="f6fb4-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="f6fb4-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="f6fb4-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f6fb4-125">Implementations</span></span>

-   [<span data-ttu-id="f6fb4-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f6fb4-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f6fb4-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f6fb4-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f6fb4-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="f6fb4-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f6fb4-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f6fb4-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f6fb4-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f6fb4-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f6fb4-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f6fb4-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f6fb4-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f6fb4-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f6fb4-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f6fb4-133">Windows 2000 Server</span></span>



| <span data-ttu-id="f6fb4-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f6fb4-134">Entry</span></span> | <span data-ttu-id="f6fb4-135">Wert</span><span class="sxs-lookup"><span data-stu-id="f6fb4-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f6fb4-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f6fb4-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f6fb4-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6fb4-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f6fb4-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6fb4-138">System-Only</span></span>            | <span data-ttu-id="f6fb4-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="f6fb4-139">True</span></span>                            |
| <span data-ttu-id="f6fb4-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f6fb4-140">Is-Single-Valued</span></span>       | <span data-ttu-id="f6fb4-141">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-141">False</span></span>                           |
| <span data-ttu-id="f6fb4-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f6fb4-142">Is Indexed</span></span>             | <span data-ttu-id="f6fb4-143">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-143">False</span></span>                           |
| <span data-ttu-id="f6fb4-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f6fb4-144">In Global Catalog</span></span>      | <span data-ttu-id="f6fb4-145">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-145">False</span></span>                           |
| <span data-ttu-id="f6fb4-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f6fb4-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6fb4-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f6fb4-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f6fb4-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6fb4-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f6fb4-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6fb4-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f6fb4-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6fb4-150">Search-Flags</span></span>           | <span data-ttu-id="f6fb4-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6fb4-151">0x00000000</span></span>                      |
| <span data-ttu-id="f6fb4-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6fb4-152">System-Flags</span></span>           | <span data-ttu-id="f6fb4-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6fb4-153">0x00000010</span></span>                      |
| <span data-ttu-id="f6fb4-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f6fb4-154">Classes used in</span></span>        | [<span data-ttu-id="f6fb4-155">**DMD**</span><span class="sxs-lookup"><span data-stu-id="f6fb4-155">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f6fb4-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f6fb4-156">Windows Server 2003</span></span>



| <span data-ttu-id="f6fb4-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f6fb4-157">Entry</span></span> | <span data-ttu-id="f6fb4-158">Wert</span><span class="sxs-lookup"><span data-stu-id="f6fb4-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f6fb4-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f6fb4-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f6fb4-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6fb4-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f6fb4-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6fb4-161">System-Only</span></span>            | <span data-ttu-id="f6fb4-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="f6fb4-162">True</span></span>                            |
| <span data-ttu-id="f6fb4-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f6fb4-163">Is-Single-Valued</span></span>       | <span data-ttu-id="f6fb4-164">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-164">False</span></span>                           |
| <span data-ttu-id="f6fb4-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f6fb4-165">Is Indexed</span></span>             | <span data-ttu-id="f6fb4-166">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-166">False</span></span>                           |
| <span data-ttu-id="f6fb4-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f6fb4-167">In Global Catalog</span></span>      | <span data-ttu-id="f6fb4-168">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-168">False</span></span>                           |
| <span data-ttu-id="f6fb4-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f6fb4-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6fb4-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f6fb4-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f6fb4-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6fb4-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f6fb4-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6fb4-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f6fb4-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6fb4-173">Search-Flags</span></span>           | <span data-ttu-id="f6fb4-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6fb4-174">0x00000000</span></span>                      |
| <span data-ttu-id="f6fb4-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6fb4-175">System-Flags</span></span>           | <span data-ttu-id="f6fb4-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6fb4-176">0x00000010</span></span>                      |
| <span data-ttu-id="f6fb4-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f6fb4-177">Classes used in</span></span>        | [<span data-ttu-id="f6fb4-178">**DMD**</span><span class="sxs-lookup"><span data-stu-id="f6fb4-178">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f6fb4-179">Adam</span><span class="sxs-lookup"><span data-stu-id="f6fb4-179">ADAM</span></span>



| <span data-ttu-id="f6fb4-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f6fb4-180">Entry</span></span> | <span data-ttu-id="f6fb4-181">Wert</span><span class="sxs-lookup"><span data-stu-id="f6fb4-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f6fb4-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f6fb4-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f6fb4-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6fb4-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f6fb4-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6fb4-184">System-Only</span></span>            | <span data-ttu-id="f6fb4-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="f6fb4-185">True</span></span>                            |
| <span data-ttu-id="f6fb4-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f6fb4-186">Is-Single-Valued</span></span>       | <span data-ttu-id="f6fb4-187">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-187">False</span></span>                           |
| <span data-ttu-id="f6fb4-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f6fb4-188">Is Indexed</span></span>             | <span data-ttu-id="f6fb4-189">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-189">False</span></span>                           |
| <span data-ttu-id="f6fb4-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f6fb4-190">In Global Catalog</span></span>      | <span data-ttu-id="f6fb4-191">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-191">False</span></span>                           |
| <span data-ttu-id="f6fb4-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f6fb4-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6fb4-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f6fb4-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f6fb4-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6fb4-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f6fb4-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6fb4-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f6fb4-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6fb4-196">Search-Flags</span></span>           | <span data-ttu-id="f6fb4-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6fb4-197">0x00000000</span></span>                      |
| <span data-ttu-id="f6fb4-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6fb4-198">System-Flags</span></span>           | <span data-ttu-id="f6fb4-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6fb4-199">0x00000010</span></span>                      |
| <span data-ttu-id="f6fb4-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f6fb4-200">Classes used in</span></span>        | [<span data-ttu-id="f6fb4-201">**DMD**</span><span class="sxs-lookup"><span data-stu-id="f6fb4-201">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f6fb4-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f6fb4-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f6fb4-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f6fb4-203">Entry</span></span> | <span data-ttu-id="f6fb4-204">Wert</span><span class="sxs-lookup"><span data-stu-id="f6fb4-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f6fb4-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f6fb4-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f6fb4-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6fb4-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f6fb4-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6fb4-207">System-Only</span></span>            | <span data-ttu-id="f6fb4-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="f6fb4-208">True</span></span>                            |
| <span data-ttu-id="f6fb4-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f6fb4-209">Is-Single-Valued</span></span>       | <span data-ttu-id="f6fb4-210">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-210">False</span></span>                           |
| <span data-ttu-id="f6fb4-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f6fb4-211">Is Indexed</span></span>             | <span data-ttu-id="f6fb4-212">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-212">False</span></span>                           |
| <span data-ttu-id="f6fb4-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f6fb4-213">In Global Catalog</span></span>      | <span data-ttu-id="f6fb4-214">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-214">False</span></span>                           |
| <span data-ttu-id="f6fb4-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f6fb4-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6fb4-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f6fb4-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f6fb4-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6fb4-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f6fb4-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6fb4-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f6fb4-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6fb4-219">Search-Flags</span></span>           | <span data-ttu-id="f6fb4-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6fb4-220">0x00000000</span></span>                      |
| <span data-ttu-id="f6fb4-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6fb4-221">System-Flags</span></span>           | <span data-ttu-id="f6fb4-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6fb4-222">0x00000010</span></span>                      |
| <span data-ttu-id="f6fb4-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f6fb4-223">Classes used in</span></span>        | [<span data-ttu-id="f6fb4-224">**DMD**</span><span class="sxs-lookup"><span data-stu-id="f6fb4-224">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f6fb4-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6fb4-225">Windows Server 2008</span></span>



| <span data-ttu-id="f6fb4-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f6fb4-226">Entry</span></span> | <span data-ttu-id="f6fb4-227">Wert</span><span class="sxs-lookup"><span data-stu-id="f6fb4-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f6fb4-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f6fb4-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f6fb4-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6fb4-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f6fb4-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6fb4-230">System-Only</span></span>            | <span data-ttu-id="f6fb4-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="f6fb4-231">True</span></span>                            |
| <span data-ttu-id="f6fb4-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f6fb4-232">Is-Single-Valued</span></span>       | <span data-ttu-id="f6fb4-233">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-233">False</span></span>                           |
| <span data-ttu-id="f6fb4-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f6fb4-234">Is Indexed</span></span>             | <span data-ttu-id="f6fb4-235">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-235">False</span></span>                           |
| <span data-ttu-id="f6fb4-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f6fb4-236">In Global Catalog</span></span>      | <span data-ttu-id="f6fb4-237">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-237">False</span></span>                           |
| <span data-ttu-id="f6fb4-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f6fb4-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6fb4-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f6fb4-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f6fb4-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6fb4-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f6fb4-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6fb4-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f6fb4-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6fb4-242">Search-Flags</span></span>           | <span data-ttu-id="f6fb4-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6fb4-243">0x00000000</span></span>                      |
| <span data-ttu-id="f6fb4-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6fb4-244">System-Flags</span></span>           | <span data-ttu-id="f6fb4-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6fb4-245">0x00000010</span></span>                      |
| <span data-ttu-id="f6fb4-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f6fb4-246">Classes used in</span></span>        | [<span data-ttu-id="f6fb4-247">**DMD**</span><span class="sxs-lookup"><span data-stu-id="f6fb4-247">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f6fb4-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f6fb4-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f6fb4-249">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f6fb4-249">Entry</span></span> | <span data-ttu-id="f6fb4-250">Wert</span><span class="sxs-lookup"><span data-stu-id="f6fb4-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f6fb4-251">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f6fb4-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f6fb4-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6fb4-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f6fb4-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6fb4-253">System-Only</span></span>            | <span data-ttu-id="f6fb4-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="f6fb4-254">True</span></span>                            |
| <span data-ttu-id="f6fb4-255">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f6fb4-255">Is-Single-Valued</span></span>       | <span data-ttu-id="f6fb4-256">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-256">False</span></span>                           |
| <span data-ttu-id="f6fb4-257">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f6fb4-257">Is Indexed</span></span>             | <span data-ttu-id="f6fb4-258">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-258">False</span></span>                           |
| <span data-ttu-id="f6fb4-259">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f6fb4-259">In Global Catalog</span></span>      | <span data-ttu-id="f6fb4-260">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-260">False</span></span>                           |
| <span data-ttu-id="f6fb4-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f6fb4-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6fb4-262">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f6fb4-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f6fb4-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6fb4-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f6fb4-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6fb4-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f6fb4-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6fb4-265">Search-Flags</span></span>           | <span data-ttu-id="f6fb4-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6fb4-266">0x00000000</span></span>                      |
| <span data-ttu-id="f6fb4-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6fb4-267">System-Flags</span></span>           | <span data-ttu-id="f6fb4-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6fb4-268">0x00000010</span></span>                      |
| <span data-ttu-id="f6fb4-269">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f6fb4-269">Classes used in</span></span>        | [<span data-ttu-id="f6fb4-270">**DMD**</span><span class="sxs-lookup"><span data-stu-id="f6fb4-270">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f6fb4-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f6fb4-271">Windows Server 2012</span></span>



| <span data-ttu-id="f6fb4-272">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f6fb4-272">Entry</span></span> | <span data-ttu-id="f6fb4-273">Wert</span><span class="sxs-lookup"><span data-stu-id="f6fb4-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f6fb4-274">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f6fb4-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f6fb4-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6fb4-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f6fb4-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6fb4-276">System-Only</span></span>            | <span data-ttu-id="f6fb4-277">Richtig</span><span class="sxs-lookup"><span data-stu-id="f6fb4-277">True</span></span>                            |
| <span data-ttu-id="f6fb4-278">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f6fb4-278">Is-Single-Valued</span></span>       | <span data-ttu-id="f6fb4-279">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-279">False</span></span>                           |
| <span data-ttu-id="f6fb4-280">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f6fb4-280">Is Indexed</span></span>             | <span data-ttu-id="f6fb4-281">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-281">False</span></span>                           |
| <span data-ttu-id="f6fb4-282">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f6fb4-282">In Global Catalog</span></span>      | <span data-ttu-id="f6fb4-283">False</span><span class="sxs-lookup"><span data-stu-id="f6fb4-283">False</span></span>                           |
| <span data-ttu-id="f6fb4-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f6fb4-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6fb4-285">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f6fb4-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f6fb4-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6fb4-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f6fb4-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6fb4-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f6fb4-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6fb4-288">Search-Flags</span></span>           | <span data-ttu-id="f6fb4-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6fb4-289">0x00000000</span></span>                      |
| <span data-ttu-id="f6fb4-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6fb4-290">System-Flags</span></span>           | <span data-ttu-id="f6fb4-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6fb4-291">0x00000010</span></span>                      |
| <span data-ttu-id="f6fb4-292">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f6fb4-292">Classes used in</span></span>        | [<span data-ttu-id="f6fb4-293">**DMD**</span><span class="sxs-lookup"><span data-stu-id="f6fb4-293">**DMD**</span></span>](c-dmd.md)<br/> |



 

 





