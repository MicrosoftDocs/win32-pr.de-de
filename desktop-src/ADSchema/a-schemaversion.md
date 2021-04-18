---
title: Schema-Version-Attribut
description: Die Versionsnummer für das Schema.
ms.assetid: b937d704-cd76-41fc-84df-5ea614b1785d
ms.tgt_platform: multiple
keywords:
- AD-Schema für Schema-Version-Attribut
- Schema Version-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Schema-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d00ca6ad8626933b39a82b2288f89454225ed47f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480242"
---
# <a name="schema-version-attribute"></a><span data-ttu-id="6aac7-105">Schema-Version-Attribut</span><span class="sxs-lookup"><span data-stu-id="6aac7-105">Schema-Version attribute</span></span>

<span data-ttu-id="6aac7-106">Die Versionsnummer für das Schema.</span><span class="sxs-lookup"><span data-stu-id="6aac7-106">The version number for the schema.</span></span>



| <span data-ttu-id="6aac7-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6aac7-107">Entry</span></span> | <span data-ttu-id="6aac7-108">Wert</span><span class="sxs-lookup"><span data-stu-id="6aac7-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6aac7-109">CN</span><span class="sxs-lookup"><span data-stu-id="6aac7-109">CN</span></span>                | <span data-ttu-id="6aac7-110">Schema-Version</span><span class="sxs-lookup"><span data-stu-id="6aac7-110">Schema-Version</span></span>                       |
| <span data-ttu-id="6aac7-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6aac7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6aac7-112">schemaVersion</span><span class="sxs-lookup"><span data-stu-id="6aac7-112">schemaVersion</span></span>                        |
| <span data-ttu-id="6aac7-113">Size</span><span class="sxs-lookup"><span data-stu-id="6aac7-113">Size</span></span>              | <span data-ttu-id="6aac7-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="6aac7-114">4 bytes</span></span>                              |
| <span data-ttu-id="6aac7-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="6aac7-115">Update Privilege</span></span>  | <span data-ttu-id="6aac7-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6aac7-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="6aac7-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="6aac7-117">Update Frequency</span></span>  | <span data-ttu-id="6aac7-118">Jedes Mal, wenn das Schema freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6aac7-118">Each time the schema is released.</span></span>    |
| <span data-ttu-id="6aac7-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6aac7-119">Attribute-Id</span></span>      | <span data-ttu-id="6aac7-120">1.2.840.113556.1.2.471</span><span class="sxs-lookup"><span data-stu-id="6aac7-120">1.2.840.113556.1.2.471</span></span>               |
| <span data-ttu-id="6aac7-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6aac7-121">System-Id-Guid</span></span>    | <span data-ttu-id="6aac7-122">bf967a2c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6aac7-122">bf967a2c-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="6aac7-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="6aac7-123">Syntax</span></span>            | [<span data-ttu-id="6aac7-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="6aac7-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="6aac7-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="6aac7-125">Implementations</span></span>

-   [<span data-ttu-id="6aac7-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6aac7-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6aac7-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6aac7-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6aac7-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="6aac7-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6aac7-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6aac7-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6aac7-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6aac7-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6aac7-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6aac7-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6aac7-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6aac7-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6aac7-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6aac7-133">Windows 2000 Server</span></span>



| <span data-ttu-id="6aac7-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6aac7-134">Entry</span></span> | <span data-ttu-id="6aac7-135">Wert</span><span class="sxs-lookup"><span data-stu-id="6aac7-135">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6aac7-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6aac7-136">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6aac7-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6aac7-137">MAPI-Id</span></span>                | <span data-ttu-id="6aac7-138">0x817c</span><span class="sxs-lookup"><span data-stu-id="6aac7-138">0x817C</span></span>                                      |
| <span data-ttu-id="6aac7-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="6aac7-139">System-Only</span></span>            | <span data-ttu-id="6aac7-140">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-140">False</span></span>                                       |
| <span data-ttu-id="6aac7-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6aac7-141">Is-Single-Valued</span></span>       | <span data-ttu-id="6aac7-142">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-142">False</span></span>                                       |
| <span data-ttu-id="6aac7-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6aac7-143">Is Indexed</span></span>             | <span data-ttu-id="6aac7-144">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-144">False</span></span>                                       |
| <span data-ttu-id="6aac7-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6aac7-145">In Global Catalog</span></span>      | <span data-ttu-id="6aac7-146">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-146">False</span></span>                                       |
| <span data-ttu-id="6aac7-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6aac7-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="6aac7-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6aac7-148">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6aac7-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6aac7-149">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6aac7-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6aac7-150">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6aac7-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6aac7-151">Search-Flags</span></span>           | <span data-ttu-id="6aac7-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6aac7-152">0x00000000</span></span>                                  |
| <span data-ttu-id="6aac7-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6aac7-153">System-Flags</span></span>           | <span data-ttu-id="6aac7-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6aac7-154">0x00000010</span></span>                                  |
| <span data-ttu-id="6aac7-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6aac7-155">Classes used in</span></span>        | [<span data-ttu-id="6aac7-156">**Container**</span><span class="sxs-lookup"><span data-stu-id="6aac7-156">**Container**</span></span>](c-container.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6aac7-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6aac7-157">Windows Server 2003</span></span>



| <span data-ttu-id="6aac7-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6aac7-158">Entry</span></span> | <span data-ttu-id="6aac7-159">Wert</span><span class="sxs-lookup"><span data-stu-id="6aac7-159">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6aac7-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6aac7-160">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6aac7-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6aac7-161">MAPI-Id</span></span>                | <span data-ttu-id="6aac7-162">0x817c</span><span class="sxs-lookup"><span data-stu-id="6aac7-162">0x817C</span></span>                                      |
| <span data-ttu-id="6aac7-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="6aac7-163">System-Only</span></span>            | <span data-ttu-id="6aac7-164">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-164">False</span></span>                                       |
| <span data-ttu-id="6aac7-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6aac7-165">Is-Single-Valued</span></span>       | <span data-ttu-id="6aac7-166">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-166">False</span></span>                                       |
| <span data-ttu-id="6aac7-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6aac7-167">Is Indexed</span></span>             | <span data-ttu-id="6aac7-168">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-168">False</span></span>                                       |
| <span data-ttu-id="6aac7-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6aac7-169">In Global Catalog</span></span>      | <span data-ttu-id="6aac7-170">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-170">False</span></span>                                       |
| <span data-ttu-id="6aac7-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6aac7-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="6aac7-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6aac7-172">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6aac7-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6aac7-173">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6aac7-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6aac7-174">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6aac7-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6aac7-175">Search-Flags</span></span>           | <span data-ttu-id="6aac7-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6aac7-176">0x00000000</span></span>                                  |
| <span data-ttu-id="6aac7-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6aac7-177">System-Flags</span></span>           | <span data-ttu-id="6aac7-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6aac7-178">0x00000010</span></span>                                  |
| <span data-ttu-id="6aac7-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6aac7-179">Classes used in</span></span>        | [<span data-ttu-id="6aac7-180">**Container**</span><span class="sxs-lookup"><span data-stu-id="6aac7-180">**Container**</span></span>](c-container.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6aac7-181">Adam</span><span class="sxs-lookup"><span data-stu-id="6aac7-181">ADAM</span></span>



| <span data-ttu-id="6aac7-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6aac7-182">Entry</span></span> | <span data-ttu-id="6aac7-183">Wert</span><span class="sxs-lookup"><span data-stu-id="6aac7-183">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6aac7-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6aac7-184">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6aac7-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6aac7-185">MAPI-Id</span></span>                | <span data-ttu-id="6aac7-186">0x817c</span><span class="sxs-lookup"><span data-stu-id="6aac7-186">0x817C</span></span>                                      |
| <span data-ttu-id="6aac7-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="6aac7-187">System-Only</span></span>            | <span data-ttu-id="6aac7-188">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-188">False</span></span>                                       |
| <span data-ttu-id="6aac7-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6aac7-189">Is-Single-Valued</span></span>       | <span data-ttu-id="6aac7-190">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-190">False</span></span>                                       |
| <span data-ttu-id="6aac7-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6aac7-191">Is Indexed</span></span>             | <span data-ttu-id="6aac7-192">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-192">False</span></span>                                       |
| <span data-ttu-id="6aac7-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6aac7-193">In Global Catalog</span></span>      | <span data-ttu-id="6aac7-194">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-194">False</span></span>                                       |
| <span data-ttu-id="6aac7-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6aac7-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="6aac7-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6aac7-196">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6aac7-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6aac7-197">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6aac7-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6aac7-198">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6aac7-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6aac7-199">Search-Flags</span></span>           | <span data-ttu-id="6aac7-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6aac7-200">0x00000000</span></span>                                  |
| <span data-ttu-id="6aac7-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6aac7-201">System-Flags</span></span>           | <span data-ttu-id="6aac7-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6aac7-202">0x00000010</span></span>                                  |
| <span data-ttu-id="6aac7-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6aac7-203">Classes used in</span></span>        | [<span data-ttu-id="6aac7-204">**Container**</span><span class="sxs-lookup"><span data-stu-id="6aac7-204">**Container**</span></span>](c-container.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6aac7-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6aac7-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6aac7-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6aac7-206">Entry</span></span> | <span data-ttu-id="6aac7-207">Wert</span><span class="sxs-lookup"><span data-stu-id="6aac7-207">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6aac7-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6aac7-208">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6aac7-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6aac7-209">MAPI-Id</span></span>                | <span data-ttu-id="6aac7-210">0x817c</span><span class="sxs-lookup"><span data-stu-id="6aac7-210">0x817C</span></span>                                      |
| <span data-ttu-id="6aac7-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="6aac7-211">System-Only</span></span>            | <span data-ttu-id="6aac7-212">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-212">False</span></span>                                       |
| <span data-ttu-id="6aac7-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6aac7-213">Is-Single-Valued</span></span>       | <span data-ttu-id="6aac7-214">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-214">False</span></span>                                       |
| <span data-ttu-id="6aac7-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6aac7-215">Is Indexed</span></span>             | <span data-ttu-id="6aac7-216">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-216">False</span></span>                                       |
| <span data-ttu-id="6aac7-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6aac7-217">In Global Catalog</span></span>      | <span data-ttu-id="6aac7-218">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-218">False</span></span>                                       |
| <span data-ttu-id="6aac7-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6aac7-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="6aac7-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6aac7-220">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6aac7-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6aac7-221">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6aac7-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6aac7-222">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6aac7-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6aac7-223">Search-Flags</span></span>           | <span data-ttu-id="6aac7-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6aac7-224">0x00000000</span></span>                                  |
| <span data-ttu-id="6aac7-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6aac7-225">System-Flags</span></span>           | <span data-ttu-id="6aac7-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6aac7-226">0x00000010</span></span>                                  |
| <span data-ttu-id="6aac7-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6aac7-227">Classes used in</span></span>        | [<span data-ttu-id="6aac7-228">**Container**</span><span class="sxs-lookup"><span data-stu-id="6aac7-228">**Container**</span></span>](c-container.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6aac7-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6aac7-229">Windows Server 2008</span></span>



| <span data-ttu-id="6aac7-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6aac7-230">Entry</span></span> | <span data-ttu-id="6aac7-231">Wert</span><span class="sxs-lookup"><span data-stu-id="6aac7-231">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6aac7-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6aac7-232">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6aac7-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6aac7-233">MAPI-Id</span></span>                | <span data-ttu-id="6aac7-234">0x817c</span><span class="sxs-lookup"><span data-stu-id="6aac7-234">0x817C</span></span>                                      |
| <span data-ttu-id="6aac7-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="6aac7-235">System-Only</span></span>            | <span data-ttu-id="6aac7-236">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-236">False</span></span>                                       |
| <span data-ttu-id="6aac7-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6aac7-237">Is-Single-Valued</span></span>       | <span data-ttu-id="6aac7-238">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-238">False</span></span>                                       |
| <span data-ttu-id="6aac7-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6aac7-239">Is Indexed</span></span>             | <span data-ttu-id="6aac7-240">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-240">False</span></span>                                       |
| <span data-ttu-id="6aac7-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6aac7-241">In Global Catalog</span></span>      | <span data-ttu-id="6aac7-242">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-242">False</span></span>                                       |
| <span data-ttu-id="6aac7-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6aac7-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="6aac7-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6aac7-244">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6aac7-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6aac7-245">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6aac7-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6aac7-246">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6aac7-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6aac7-247">Search-Flags</span></span>           | <span data-ttu-id="6aac7-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6aac7-248">0x00000000</span></span>                                  |
| <span data-ttu-id="6aac7-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6aac7-249">System-Flags</span></span>           | <span data-ttu-id="6aac7-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6aac7-250">0x00000010</span></span>                                  |
| <span data-ttu-id="6aac7-251">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6aac7-251">Classes used in</span></span>        | [<span data-ttu-id="6aac7-252">**Container**</span><span class="sxs-lookup"><span data-stu-id="6aac7-252">**Container**</span></span>](c-container.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6aac7-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6aac7-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6aac7-254">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6aac7-254">Entry</span></span> | <span data-ttu-id="6aac7-255">Wert</span><span class="sxs-lookup"><span data-stu-id="6aac7-255">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6aac7-256">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6aac7-256">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6aac7-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6aac7-257">MAPI-Id</span></span>                | <span data-ttu-id="6aac7-258">0x817c</span><span class="sxs-lookup"><span data-stu-id="6aac7-258">0x817C</span></span>                                      |
| <span data-ttu-id="6aac7-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="6aac7-259">System-Only</span></span>            | <span data-ttu-id="6aac7-260">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-260">False</span></span>                                       |
| <span data-ttu-id="6aac7-261">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6aac7-261">Is-Single-Valued</span></span>       | <span data-ttu-id="6aac7-262">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-262">False</span></span>                                       |
| <span data-ttu-id="6aac7-263">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6aac7-263">Is Indexed</span></span>             | <span data-ttu-id="6aac7-264">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-264">False</span></span>                                       |
| <span data-ttu-id="6aac7-265">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6aac7-265">In Global Catalog</span></span>      | <span data-ttu-id="6aac7-266">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-266">False</span></span>                                       |
| <span data-ttu-id="6aac7-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6aac7-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="6aac7-268">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6aac7-268">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6aac7-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6aac7-269">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6aac7-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6aac7-270">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6aac7-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6aac7-271">Search-Flags</span></span>           | <span data-ttu-id="6aac7-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6aac7-272">0x00000000</span></span>                                  |
| <span data-ttu-id="6aac7-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6aac7-273">System-Flags</span></span>           | <span data-ttu-id="6aac7-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6aac7-274">0x00000010</span></span>                                  |
| <span data-ttu-id="6aac7-275">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6aac7-275">Classes used in</span></span>        | [<span data-ttu-id="6aac7-276">**Container**</span><span class="sxs-lookup"><span data-stu-id="6aac7-276">**Container**</span></span>](c-container.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6aac7-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6aac7-277">Windows Server 2012</span></span>



| <span data-ttu-id="6aac7-278">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6aac7-278">Entry</span></span> | <span data-ttu-id="6aac7-279">Wert</span><span class="sxs-lookup"><span data-stu-id="6aac7-279">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="6aac7-280">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6aac7-280">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="6aac7-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6aac7-281">MAPI-Id</span></span>                | <span data-ttu-id="6aac7-282">0x817c</span><span class="sxs-lookup"><span data-stu-id="6aac7-282">0x817C</span></span>                                      |
| <span data-ttu-id="6aac7-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="6aac7-283">System-Only</span></span>            | <span data-ttu-id="6aac7-284">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-284">False</span></span>                                       |
| <span data-ttu-id="6aac7-285">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6aac7-285">Is-Single-Valued</span></span>       | <span data-ttu-id="6aac7-286">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-286">False</span></span>                                       |
| <span data-ttu-id="6aac7-287">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6aac7-287">Is Indexed</span></span>             | <span data-ttu-id="6aac7-288">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-288">False</span></span>                                       |
| <span data-ttu-id="6aac7-289">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6aac7-289">In Global Catalog</span></span>      | <span data-ttu-id="6aac7-290">False</span><span class="sxs-lookup"><span data-stu-id="6aac7-290">False</span></span>                                       |
| <span data-ttu-id="6aac7-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6aac7-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="6aac7-292">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6aac7-292">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="6aac7-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6aac7-293">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="6aac7-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6aac7-294">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="6aac7-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6aac7-295">Search-Flags</span></span>           | <span data-ttu-id="6aac7-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6aac7-296">0x00000000</span></span>                                  |
| <span data-ttu-id="6aac7-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6aac7-297">System-Flags</span></span>           | <span data-ttu-id="6aac7-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6aac7-298">0x00000010</span></span>                                  |
| <span data-ttu-id="6aac7-299">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6aac7-299">Classes used in</span></span>        | [<span data-ttu-id="6aac7-300">**Container**</span><span class="sxs-lookup"><span data-stu-id="6aac7-300">**Container**</span></span>](c-container.md)<br/> |



 

 





