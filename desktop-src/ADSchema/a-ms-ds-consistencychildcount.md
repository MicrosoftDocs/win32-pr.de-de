---
title: MS-DS-Konsistenz-Child-count-Attribut
description: Dieses Attribut wird verwendet, um die Konsistenz zwischen dem Verzeichnis und einem anderen Objekt, einer Datenbank oder einer Anwendung zu überprüfen, indem die Anzahl der untergeordneten Objekte verglichen wird.
ms.assetid: f7d6e8f0-963b-45a9-86af-8e51d6de32bb
ms.tgt_platform: multiple
keywords:
- AD-Schema für das Attribut "ms-DS-Konsistenz-Child-count"
- AD-Schema für ms-DS-ConsistencyChildCount-Attribut
topic_type:
- apiref
api_name:
- MS-DS-Consistency-Child-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b9c46d1c4519550a91d92d0a82f726a20572490
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107192"
---
# <a name="ms-ds-consistency-child-count-attribute"></a><span data-ttu-id="f25ce-105">MS-DS-Konsistenz-Child-count-Attribut</span><span class="sxs-lookup"><span data-stu-id="f25ce-105">MS-DS-Consistency-Child-Count attribute</span></span>

<span data-ttu-id="f25ce-106">Dieses Attribut wird verwendet, um die Konsistenz zwischen dem Verzeichnis und einem anderen Objekt, einer Datenbank oder einer Anwendung zu überprüfen, indem die Anzahl der untergeordneten Objekte verglichen wird.</span><span class="sxs-lookup"><span data-stu-id="f25ce-106">This attribute is used to check consistency between the directory and another object, database, or application, by comparing a count of child objects.</span></span>



| <span data-ttu-id="f25ce-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f25ce-107">Entry</span></span> | <span data-ttu-id="f25ce-108">Wert</span><span class="sxs-lookup"><span data-stu-id="f25ce-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f25ce-109">CN</span><span class="sxs-lookup"><span data-stu-id="f25ce-109">CN</span></span>                | <span data-ttu-id="f25ce-110">MS-DS-Konsistenz-untergeordnet-Anzahl</span><span class="sxs-lookup"><span data-stu-id="f25ce-110">MS-DS-Consistency-Child-Count</span></span>        |
| <span data-ttu-id="f25ce-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f25ce-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f25ce-112">mS-DS-ConsistencyChildCount</span><span class="sxs-lookup"><span data-stu-id="f25ce-112">mS-DS-ConsistencyChildCount</span></span>          |
| <span data-ttu-id="f25ce-113">Size</span><span class="sxs-lookup"><span data-stu-id="f25ce-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="f25ce-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f25ce-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f25ce-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f25ce-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f25ce-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f25ce-116">Attribute-Id</span></span>      | <span data-ttu-id="f25ce-117">1.2.840.113556.1.4.1361</span><span class="sxs-lookup"><span data-stu-id="f25ce-117">1.2.840.113556.1.4.1361</span></span>              |
| <span data-ttu-id="f25ce-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f25ce-118">System-Id-Guid</span></span>    | <span data-ttu-id="f25ce-119">178b7bc2-b63a-11d2-90e1-00c04f d91ab1</span><span class="sxs-lookup"><span data-stu-id="f25ce-119">178b7bc2-b63a-11d2-90e1-00c04fd91ab1</span></span> |
| <span data-ttu-id="f25ce-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="f25ce-120">Syntax</span></span>            | [<span data-ttu-id="f25ce-121">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="f25ce-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="f25ce-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f25ce-122">Implementations</span></span>

-   [<span data-ttu-id="f25ce-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f25ce-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f25ce-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f25ce-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f25ce-125">**Adam**</span><span class="sxs-lookup"><span data-stu-id="f25ce-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f25ce-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f25ce-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f25ce-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f25ce-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f25ce-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f25ce-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f25ce-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f25ce-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f25ce-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f25ce-130">Windows 2000 Server</span></span>



| <span data-ttu-id="f25ce-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f25ce-131">Entry</span></span> | <span data-ttu-id="f25ce-132">Wert</span><span class="sxs-lookup"><span data-stu-id="f25ce-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f25ce-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f25ce-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f25ce-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f25ce-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f25ce-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="f25ce-135">System-Only</span></span>            | <span data-ttu-id="f25ce-136">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-136">False</span></span>                           |
| <span data-ttu-id="f25ce-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f25ce-137">Is-Single-Valued</span></span>       | <span data-ttu-id="f25ce-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="f25ce-138">True</span></span>                            |
| <span data-ttu-id="f25ce-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f25ce-139">Is Indexed</span></span>             | <span data-ttu-id="f25ce-140">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-140">False</span></span>                           |
| <span data-ttu-id="f25ce-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f25ce-141">In Global Catalog</span></span>      | <span data-ttu-id="f25ce-142">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-142">False</span></span>                           |
| <span data-ttu-id="f25ce-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f25ce-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="f25ce-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f25ce-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f25ce-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f25ce-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f25ce-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f25ce-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f25ce-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f25ce-147">Search-Flags</span></span>           | <span data-ttu-id="f25ce-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f25ce-148">0x00000000</span></span>                      |
| <span data-ttu-id="f25ce-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f25ce-149">System-Flags</span></span>           | <span data-ttu-id="f25ce-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f25ce-150">0x00000010</span></span>                      |
| <span data-ttu-id="f25ce-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f25ce-151">Classes used in</span></span>        | [<span data-ttu-id="f25ce-152">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f25ce-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f25ce-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f25ce-153">Windows Server 2003</span></span>



| <span data-ttu-id="f25ce-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f25ce-154">Entry</span></span> | <span data-ttu-id="f25ce-155">Wert</span><span class="sxs-lookup"><span data-stu-id="f25ce-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f25ce-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f25ce-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f25ce-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f25ce-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f25ce-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="f25ce-158">System-Only</span></span>            | <span data-ttu-id="f25ce-159">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-159">False</span></span>                           |
| <span data-ttu-id="f25ce-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f25ce-160">Is-Single-Valued</span></span>       | <span data-ttu-id="f25ce-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="f25ce-161">True</span></span>                            |
| <span data-ttu-id="f25ce-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f25ce-162">Is Indexed</span></span>             | <span data-ttu-id="f25ce-163">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-163">False</span></span>                           |
| <span data-ttu-id="f25ce-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f25ce-164">In Global Catalog</span></span>      | <span data-ttu-id="f25ce-165">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-165">False</span></span>                           |
| <span data-ttu-id="f25ce-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f25ce-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="f25ce-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f25ce-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f25ce-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f25ce-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f25ce-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f25ce-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f25ce-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f25ce-170">Search-Flags</span></span>           | <span data-ttu-id="f25ce-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f25ce-171">0x00000000</span></span>                      |
| <span data-ttu-id="f25ce-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f25ce-172">System-Flags</span></span>           | <span data-ttu-id="f25ce-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f25ce-173">0x00000010</span></span>                      |
| <span data-ttu-id="f25ce-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f25ce-174">Classes used in</span></span>        | [<span data-ttu-id="f25ce-175">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f25ce-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f25ce-176">Adam</span><span class="sxs-lookup"><span data-stu-id="f25ce-176">ADAM</span></span>



| <span data-ttu-id="f25ce-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f25ce-177">Entry</span></span> | <span data-ttu-id="f25ce-178">Wert</span><span class="sxs-lookup"><span data-stu-id="f25ce-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f25ce-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f25ce-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f25ce-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f25ce-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f25ce-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="f25ce-181">System-Only</span></span>            | <span data-ttu-id="f25ce-182">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-182">False</span></span>                           |
| <span data-ttu-id="f25ce-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f25ce-183">Is-Single-Valued</span></span>       | <span data-ttu-id="f25ce-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="f25ce-184">True</span></span>                            |
| <span data-ttu-id="f25ce-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f25ce-185">Is Indexed</span></span>             | <span data-ttu-id="f25ce-186">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-186">False</span></span>                           |
| <span data-ttu-id="f25ce-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f25ce-187">In Global Catalog</span></span>      | <span data-ttu-id="f25ce-188">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-188">False</span></span>                           |
| <span data-ttu-id="f25ce-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f25ce-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="f25ce-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f25ce-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f25ce-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f25ce-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f25ce-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f25ce-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f25ce-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f25ce-193">Search-Flags</span></span>           | <span data-ttu-id="f25ce-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f25ce-194">0x00000000</span></span>                      |
| <span data-ttu-id="f25ce-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f25ce-195">System-Flags</span></span>           | <span data-ttu-id="f25ce-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f25ce-196">0x00000010</span></span>                      |
| <span data-ttu-id="f25ce-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f25ce-197">Classes used in</span></span>        | [<span data-ttu-id="f25ce-198">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f25ce-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f25ce-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f25ce-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f25ce-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f25ce-200">Entry</span></span> | <span data-ttu-id="f25ce-201">Wert</span><span class="sxs-lookup"><span data-stu-id="f25ce-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f25ce-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f25ce-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f25ce-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f25ce-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f25ce-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="f25ce-204">System-Only</span></span>            | <span data-ttu-id="f25ce-205">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-205">False</span></span>                           |
| <span data-ttu-id="f25ce-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f25ce-206">Is-Single-Valued</span></span>       | <span data-ttu-id="f25ce-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="f25ce-207">True</span></span>                            |
| <span data-ttu-id="f25ce-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f25ce-208">Is Indexed</span></span>             | <span data-ttu-id="f25ce-209">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-209">False</span></span>                           |
| <span data-ttu-id="f25ce-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f25ce-210">In Global Catalog</span></span>      | <span data-ttu-id="f25ce-211">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-211">False</span></span>                           |
| <span data-ttu-id="f25ce-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f25ce-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="f25ce-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f25ce-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f25ce-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f25ce-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f25ce-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f25ce-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f25ce-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f25ce-216">Search-Flags</span></span>           | <span data-ttu-id="f25ce-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f25ce-217">0x00000000</span></span>                      |
| <span data-ttu-id="f25ce-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f25ce-218">System-Flags</span></span>           | <span data-ttu-id="f25ce-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f25ce-219">0x00000010</span></span>                      |
| <span data-ttu-id="f25ce-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f25ce-220">Classes used in</span></span>        | [<span data-ttu-id="f25ce-221">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f25ce-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f25ce-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f25ce-222">Windows Server 2008</span></span>



| <span data-ttu-id="f25ce-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f25ce-223">Entry</span></span> | <span data-ttu-id="f25ce-224">Wert</span><span class="sxs-lookup"><span data-stu-id="f25ce-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f25ce-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f25ce-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f25ce-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f25ce-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f25ce-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="f25ce-227">System-Only</span></span>            | <span data-ttu-id="f25ce-228">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-228">False</span></span>                           |
| <span data-ttu-id="f25ce-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f25ce-229">Is-Single-Valued</span></span>       | <span data-ttu-id="f25ce-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="f25ce-230">True</span></span>                            |
| <span data-ttu-id="f25ce-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f25ce-231">Is Indexed</span></span>             | <span data-ttu-id="f25ce-232">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-232">False</span></span>                           |
| <span data-ttu-id="f25ce-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f25ce-233">In Global Catalog</span></span>      | <span data-ttu-id="f25ce-234">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-234">False</span></span>                           |
| <span data-ttu-id="f25ce-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f25ce-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="f25ce-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f25ce-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f25ce-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f25ce-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f25ce-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f25ce-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f25ce-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f25ce-239">Search-Flags</span></span>           | <span data-ttu-id="f25ce-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f25ce-240">0x00000000</span></span>                      |
| <span data-ttu-id="f25ce-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f25ce-241">System-Flags</span></span>           | <span data-ttu-id="f25ce-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f25ce-242">0x00000010</span></span>                      |
| <span data-ttu-id="f25ce-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f25ce-243">Classes used in</span></span>        | [<span data-ttu-id="f25ce-244">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f25ce-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f25ce-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f25ce-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f25ce-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f25ce-246">Entry</span></span> | <span data-ttu-id="f25ce-247">Wert</span><span class="sxs-lookup"><span data-stu-id="f25ce-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f25ce-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f25ce-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f25ce-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f25ce-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f25ce-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="f25ce-250">System-Only</span></span>            | <span data-ttu-id="f25ce-251">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-251">False</span></span>                           |
| <span data-ttu-id="f25ce-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f25ce-252">Is-Single-Valued</span></span>       | <span data-ttu-id="f25ce-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="f25ce-253">True</span></span>                            |
| <span data-ttu-id="f25ce-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f25ce-254">Is Indexed</span></span>             | <span data-ttu-id="f25ce-255">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-255">False</span></span>                           |
| <span data-ttu-id="f25ce-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f25ce-256">In Global Catalog</span></span>      | <span data-ttu-id="f25ce-257">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-257">False</span></span>                           |
| <span data-ttu-id="f25ce-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f25ce-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="f25ce-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f25ce-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f25ce-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f25ce-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f25ce-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f25ce-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f25ce-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f25ce-262">Search-Flags</span></span>           | <span data-ttu-id="f25ce-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f25ce-263">0x00000000</span></span>                      |
| <span data-ttu-id="f25ce-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f25ce-264">System-Flags</span></span>           | <span data-ttu-id="f25ce-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f25ce-265">0x00000010</span></span>                      |
| <span data-ttu-id="f25ce-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f25ce-266">Classes used in</span></span>        | [<span data-ttu-id="f25ce-267">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f25ce-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f25ce-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f25ce-268">Windows Server 2012</span></span>



| <span data-ttu-id="f25ce-269">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f25ce-269">Entry</span></span> | <span data-ttu-id="f25ce-270">Wert</span><span class="sxs-lookup"><span data-stu-id="f25ce-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f25ce-271">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f25ce-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f25ce-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f25ce-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f25ce-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="f25ce-273">System-Only</span></span>            | <span data-ttu-id="f25ce-274">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-274">False</span></span>                           |
| <span data-ttu-id="f25ce-275">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f25ce-275">Is-Single-Valued</span></span>       | <span data-ttu-id="f25ce-276">Richtig</span><span class="sxs-lookup"><span data-stu-id="f25ce-276">True</span></span>                            |
| <span data-ttu-id="f25ce-277">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f25ce-277">Is Indexed</span></span>             | <span data-ttu-id="f25ce-278">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-278">False</span></span>                           |
| <span data-ttu-id="f25ce-279">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f25ce-279">In Global Catalog</span></span>      | <span data-ttu-id="f25ce-280">False</span><span class="sxs-lookup"><span data-stu-id="f25ce-280">False</span></span>                           |
| <span data-ttu-id="f25ce-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f25ce-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="f25ce-282">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f25ce-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f25ce-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f25ce-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f25ce-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f25ce-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f25ce-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f25ce-285">Search-Flags</span></span>           | <span data-ttu-id="f25ce-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f25ce-286">0x00000000</span></span>                      |
| <span data-ttu-id="f25ce-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f25ce-287">System-Flags</span></span>           | <span data-ttu-id="f25ce-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f25ce-288">0x00000010</span></span>                      |
| <span data-ttu-id="f25ce-289">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f25ce-289">Classes used in</span></span>        | [<span data-ttu-id="f25ce-290">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f25ce-290">**Top**</span></span>](c-top.md)<br/> |



 

 





