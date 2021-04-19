---
title: meetingendtime-Attribut
description: Das Datum und die Uhrzeit, zu der die Besprechung enden soll.
ms.assetid: b2eb0dac-11fe-4bc4-9271-f481dd4afd27
ms.tgt_platform: multiple
keywords:
- AD-Schema für das meetingendtime-Attribut
topic_type:
- apiref
api_name:
- meetingEndTime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f0387f7b6dc9c57e12621d98bd4504020e4b0b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346352"
---
# <a name="meetingendtime-attribute"></a><span data-ttu-id="c72e7-104">meetingendtime-Attribut</span><span class="sxs-lookup"><span data-stu-id="c72e7-104">meetingEndTime attribute</span></span>

<span data-ttu-id="c72e7-105">Das Datum und die Uhrzeit, zu der die Besprechung enden soll.</span><span class="sxs-lookup"><span data-stu-id="c72e7-105">The date and time that the meeting is to end.</span></span>



| <span data-ttu-id="c72e7-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c72e7-106">Entry</span></span> | <span data-ttu-id="c72e7-107">Wert</span><span class="sxs-lookup"><span data-stu-id="c72e7-107">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c72e7-108">CN</span><span class="sxs-lookup"><span data-stu-id="c72e7-108">CN</span></span>                | <span data-ttu-id="c72e7-109">meetingendtime</span><span class="sxs-lookup"><span data-stu-id="c72e7-109">meetingEndTime</span></span>                                                                   |
| <span data-ttu-id="c72e7-110">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c72e7-110">Ldap-Display-Name</span></span> | <span data-ttu-id="c72e7-111">meetingendtime</span><span class="sxs-lookup"><span data-stu-id="c72e7-111">meetingEndTime</span></span>                                                                   |
| <span data-ttu-id="c72e7-112">Size</span><span class="sxs-lookup"><span data-stu-id="c72e7-112">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="c72e7-113">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c72e7-113">Update Privilege</span></span>  | <span data-ttu-id="c72e7-114">Jeder kann dieses Objekt basierend auf der Sicherheit des Objekts, das erstellt wird, aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c72e7-114">Anyone may update this object based on the security of the object being created.</span></span> |
| <span data-ttu-id="c72e7-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="c72e7-115">Update Frequency</span></span>  | \-                                                                               |
| <span data-ttu-id="c72e7-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c72e7-116">Attribute-Id</span></span>      | <span data-ttu-id="c72e7-117">1.2.840.113556.1.4.588</span><span class="sxs-lookup"><span data-stu-id="c72e7-117">1.2.840.113556.1.4.588</span></span>                                                           |
| <span data-ttu-id="c72e7-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c72e7-118">System-Id-Guid</span></span>    | <span data-ttu-id="c72e7-119">11b6cc91-48C4-11d1-a9c3-0000t80367c1</span><span class="sxs-lookup"><span data-stu-id="c72e7-119">11b6cc91-48c4-11d1-a9c3-0000f80367c1</span></span>                                             |
| <span data-ttu-id="c72e7-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="c72e7-120">Syntax</span></span>            | [<span data-ttu-id="c72e7-121">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="c72e7-121">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md)                    |



## <a name="implementations"></a><span data-ttu-id="c72e7-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="c72e7-122">Implementations</span></span>

-   [<span data-ttu-id="c72e7-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c72e7-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c72e7-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c72e7-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c72e7-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c72e7-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c72e7-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c72e7-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c72e7-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c72e7-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c72e7-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c72e7-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c72e7-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c72e7-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c72e7-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c72e7-130">Entry</span></span> | <span data-ttu-id="c72e7-131">Wert</span><span class="sxs-lookup"><span data-stu-id="c72e7-131">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="c72e7-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c72e7-132">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="c72e7-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c72e7-133">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="c72e7-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c72e7-134">System-Only</span></span>            | <span data-ttu-id="c72e7-135">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-135">False</span></span>                                   |
| <span data-ttu-id="c72e7-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c72e7-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c72e7-137">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-137">False</span></span>                                   |
| <span data-ttu-id="c72e7-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c72e7-138">Is Indexed</span></span>             | <span data-ttu-id="c72e7-139">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-139">False</span></span>                                   |
| <span data-ttu-id="c72e7-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c72e7-140">In Global Catalog</span></span>      | <span data-ttu-id="c72e7-141">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-141">False</span></span>                                   |
| <span data-ttu-id="c72e7-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c72e7-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c72e7-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c72e7-143">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="c72e7-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c72e7-144">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="c72e7-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c72e7-145">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="c72e7-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c72e7-146">Search-Flags</span></span>           | <span data-ttu-id="c72e7-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c72e7-147">0x00000000</span></span>                              |
| <span data-ttu-id="c72e7-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c72e7-148">System-Flags</span></span>           | <span data-ttu-id="c72e7-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c72e7-149">0x00000010</span></span>                              |
| <span data-ttu-id="c72e7-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c72e7-150">Classes used in</span></span>        | [<span data-ttu-id="c72e7-151">**Freuen**</span><span class="sxs-lookup"><span data-stu-id="c72e7-151">**Meeting**</span></span>](c-meeting.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c72e7-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c72e7-152">Windows Server 2003</span></span>



| <span data-ttu-id="c72e7-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c72e7-153">Entry</span></span> | <span data-ttu-id="c72e7-154">Wert</span><span class="sxs-lookup"><span data-stu-id="c72e7-154">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="c72e7-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c72e7-155">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="c72e7-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c72e7-156">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="c72e7-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="c72e7-157">System-Only</span></span>            | <span data-ttu-id="c72e7-158">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-158">False</span></span>                                   |
| <span data-ttu-id="c72e7-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c72e7-159">Is-Single-Valued</span></span>       | <span data-ttu-id="c72e7-160">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-160">False</span></span>                                   |
| <span data-ttu-id="c72e7-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c72e7-161">Is Indexed</span></span>             | <span data-ttu-id="c72e7-162">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-162">False</span></span>                                   |
| <span data-ttu-id="c72e7-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c72e7-163">In Global Catalog</span></span>      | <span data-ttu-id="c72e7-164">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-164">False</span></span>                                   |
| <span data-ttu-id="c72e7-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c72e7-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="c72e7-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c72e7-166">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="c72e7-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c72e7-167">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="c72e7-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c72e7-168">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="c72e7-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c72e7-169">Search-Flags</span></span>           | <span data-ttu-id="c72e7-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c72e7-170">0x00000000</span></span>                              |
| <span data-ttu-id="c72e7-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c72e7-171">System-Flags</span></span>           | <span data-ttu-id="c72e7-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c72e7-172">0x00000010</span></span>                              |
| <span data-ttu-id="c72e7-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c72e7-173">Classes used in</span></span>        | [<span data-ttu-id="c72e7-174">**Freuen**</span><span class="sxs-lookup"><span data-stu-id="c72e7-174">**Meeting**</span></span>](c-meeting.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c72e7-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c72e7-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c72e7-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c72e7-176">Entry</span></span> | <span data-ttu-id="c72e7-177">Wert</span><span class="sxs-lookup"><span data-stu-id="c72e7-177">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="c72e7-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c72e7-178">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="c72e7-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c72e7-179">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="c72e7-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="c72e7-180">System-Only</span></span>            | <span data-ttu-id="c72e7-181">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-181">False</span></span>                                   |
| <span data-ttu-id="c72e7-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c72e7-182">Is-Single-Valued</span></span>       | <span data-ttu-id="c72e7-183">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-183">False</span></span>                                   |
| <span data-ttu-id="c72e7-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c72e7-184">Is Indexed</span></span>             | <span data-ttu-id="c72e7-185">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-185">False</span></span>                                   |
| <span data-ttu-id="c72e7-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c72e7-186">In Global Catalog</span></span>      | <span data-ttu-id="c72e7-187">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-187">False</span></span>                                   |
| <span data-ttu-id="c72e7-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c72e7-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="c72e7-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c72e7-189">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="c72e7-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c72e7-190">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="c72e7-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c72e7-191">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="c72e7-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c72e7-192">Search-Flags</span></span>           | <span data-ttu-id="c72e7-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c72e7-193">0x00000000</span></span>                              |
| <span data-ttu-id="c72e7-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c72e7-194">System-Flags</span></span>           | <span data-ttu-id="c72e7-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c72e7-195">0x00000010</span></span>                              |
| <span data-ttu-id="c72e7-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c72e7-196">Classes used in</span></span>        | [<span data-ttu-id="c72e7-197">**Freuen**</span><span class="sxs-lookup"><span data-stu-id="c72e7-197">**Meeting**</span></span>](c-meeting.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c72e7-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c72e7-198">Windows Server 2008</span></span>



| <span data-ttu-id="c72e7-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c72e7-199">Entry</span></span> | <span data-ttu-id="c72e7-200">Wert</span><span class="sxs-lookup"><span data-stu-id="c72e7-200">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="c72e7-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c72e7-201">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="c72e7-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c72e7-202">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="c72e7-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="c72e7-203">System-Only</span></span>            | <span data-ttu-id="c72e7-204">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-204">False</span></span>                                   |
| <span data-ttu-id="c72e7-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c72e7-205">Is-Single-Valued</span></span>       | <span data-ttu-id="c72e7-206">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-206">False</span></span>                                   |
| <span data-ttu-id="c72e7-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c72e7-207">Is Indexed</span></span>             | <span data-ttu-id="c72e7-208">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-208">False</span></span>                                   |
| <span data-ttu-id="c72e7-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c72e7-209">In Global Catalog</span></span>      | <span data-ttu-id="c72e7-210">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-210">False</span></span>                                   |
| <span data-ttu-id="c72e7-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c72e7-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="c72e7-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c72e7-212">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="c72e7-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c72e7-213">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="c72e7-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c72e7-214">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="c72e7-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c72e7-215">Search-Flags</span></span>           | <span data-ttu-id="c72e7-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c72e7-216">0x00000000</span></span>                              |
| <span data-ttu-id="c72e7-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c72e7-217">System-Flags</span></span>           | <span data-ttu-id="c72e7-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c72e7-218">0x00000010</span></span>                              |
| <span data-ttu-id="c72e7-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c72e7-219">Classes used in</span></span>        | [<span data-ttu-id="c72e7-220">**Freuen**</span><span class="sxs-lookup"><span data-stu-id="c72e7-220">**Meeting**</span></span>](c-meeting.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c72e7-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c72e7-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c72e7-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c72e7-222">Entry</span></span> | <span data-ttu-id="c72e7-223">Wert</span><span class="sxs-lookup"><span data-stu-id="c72e7-223">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="c72e7-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c72e7-224">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="c72e7-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c72e7-225">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="c72e7-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="c72e7-226">System-Only</span></span>            | <span data-ttu-id="c72e7-227">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-227">False</span></span>                                   |
| <span data-ttu-id="c72e7-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c72e7-228">Is-Single-Valued</span></span>       | <span data-ttu-id="c72e7-229">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-229">False</span></span>                                   |
| <span data-ttu-id="c72e7-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c72e7-230">Is Indexed</span></span>             | <span data-ttu-id="c72e7-231">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-231">False</span></span>                                   |
| <span data-ttu-id="c72e7-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c72e7-232">In Global Catalog</span></span>      | <span data-ttu-id="c72e7-233">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-233">False</span></span>                                   |
| <span data-ttu-id="c72e7-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c72e7-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="c72e7-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c72e7-235">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="c72e7-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c72e7-236">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="c72e7-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c72e7-237">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="c72e7-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c72e7-238">Search-Flags</span></span>           | <span data-ttu-id="c72e7-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c72e7-239">0x00000000</span></span>                              |
| <span data-ttu-id="c72e7-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c72e7-240">System-Flags</span></span>           | <span data-ttu-id="c72e7-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c72e7-241">0x00000010</span></span>                              |
| <span data-ttu-id="c72e7-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c72e7-242">Classes used in</span></span>        | [<span data-ttu-id="c72e7-243">**Freuen**</span><span class="sxs-lookup"><span data-stu-id="c72e7-243">**Meeting**</span></span>](c-meeting.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c72e7-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c72e7-244">Windows Server 2012</span></span>



| <span data-ttu-id="c72e7-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c72e7-245">Entry</span></span> | <span data-ttu-id="c72e7-246">Wert</span><span class="sxs-lookup"><span data-stu-id="c72e7-246">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="c72e7-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c72e7-247">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="c72e7-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c72e7-248">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="c72e7-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="c72e7-249">System-Only</span></span>            | <span data-ttu-id="c72e7-250">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-250">False</span></span>                                   |
| <span data-ttu-id="c72e7-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c72e7-251">Is-Single-Valued</span></span>       | <span data-ttu-id="c72e7-252">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-252">False</span></span>                                   |
| <span data-ttu-id="c72e7-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c72e7-253">Is Indexed</span></span>             | <span data-ttu-id="c72e7-254">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-254">False</span></span>                                   |
| <span data-ttu-id="c72e7-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c72e7-255">In Global Catalog</span></span>      | <span data-ttu-id="c72e7-256">False</span><span class="sxs-lookup"><span data-stu-id="c72e7-256">False</span></span>                                   |
| <span data-ttu-id="c72e7-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c72e7-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="c72e7-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c72e7-258">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="c72e7-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c72e7-259">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="c72e7-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c72e7-260">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="c72e7-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c72e7-261">Search-Flags</span></span>           | <span data-ttu-id="c72e7-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c72e7-262">0x00000000</span></span>                              |
| <span data-ttu-id="c72e7-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c72e7-263">System-Flags</span></span>           | <span data-ttu-id="c72e7-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c72e7-264">0x00000010</span></span>                              |
| <span data-ttu-id="c72e7-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c72e7-265">Classes used in</span></span>        | [<span data-ttu-id="c72e7-266">**Freuen**</span><span class="sxs-lookup"><span data-stu-id="c72e7-266">**Meeting**</span></span>](c-meeting.md)<br/> |



 

 





