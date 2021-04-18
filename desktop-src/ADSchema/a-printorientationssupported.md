---
title: Durch Print-Ausrichtungen unterstütztes Attribut
description: Die Seiten Drehung für das Querformat.
ms.assetid: a3e910f1-452e-4b85-8ede-50b7274475a0
ms.tgt_platform: multiple
keywords:
- Vom Print-Ausrichtungen unterstütztes AD-Schema für Attribute
- printorientationssupported-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Print-Orientations-Supported
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49888caa713de7dd12616dcb9932e52b15b2a454
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106343507"
---
# <a name="print-orientations-supported-attribute"></a><span data-ttu-id="1b4cc-105">Durch Print-Ausrichtungen unterstütztes Attribut</span><span class="sxs-lookup"><span data-stu-id="1b4cc-105">Print-Orientations-Supported attribute</span></span>

<span data-ttu-id="1b4cc-106">Die Seiten Drehung für das Querformat.</span><span class="sxs-lookup"><span data-stu-id="1b4cc-106">The page rotation for landscape printing.</span></span>



| <span data-ttu-id="1b4cc-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1b4cc-107">Entry</span></span> | <span data-ttu-id="1b4cc-108">Wert</span><span class="sxs-lookup"><span data-stu-id="1b4cc-108">Value</span></span> |
|-------------------|-------------------------------------------------------------|
| <span data-ttu-id="1b4cc-109">CN</span><span class="sxs-lookup"><span data-stu-id="1b4cc-109">CN</span></span>                | <span data-ttu-id="1b4cc-110">Print-Ausrichtungen-unterstützt</span><span class="sxs-lookup"><span data-stu-id="1b4cc-110">Print-Orientations-Supported</span></span>                                |
| <span data-ttu-id="1b4cc-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1b4cc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1b4cc-112">printorientationssupported</span><span class="sxs-lookup"><span data-stu-id="1b4cc-112">printOrientationsSupported</span></span>                                  |
| <span data-ttu-id="1b4cc-113">Size</span><span class="sxs-lookup"><span data-stu-id="1b4cc-113">Size</span></span>              | <span data-ttu-id="1b4cc-114">4 Bytes.</span><span class="sxs-lookup"><span data-stu-id="1b4cc-114">4 bytes.</span></span> <span data-ttu-id="1b4cc-115">Mögliche Werte: 0, 90, 270 und 0 = keine Querformat.</span><span class="sxs-lookup"><span data-stu-id="1b4cc-115">Possible values: 0, 90, 270, and 0 = no landscape.</span></span> |
| <span data-ttu-id="1b4cc-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="1b4cc-116">Update Privilege</span></span>  | \-                                                          |
| <span data-ttu-id="1b4cc-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="1b4cc-117">Update Frequency</span></span>  | \-                                                          |
| <span data-ttu-id="1b4cc-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1b4cc-118">Attribute-Id</span></span>      | <span data-ttu-id="1b4cc-119">1.2.840.113556.1.4.240</span><span class="sxs-lookup"><span data-stu-id="1b4cc-119">1.2.840.113556.1.4.240</span></span>                                      |
| <span data-ttu-id="1b4cc-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1b4cc-120">System-Id-Guid</span></span>    | <span data-ttu-id="1b4cc-121">281416d0-1968-11D0-a28f -00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1b4cc-121">281416d0-1968-11d0-a28f-00aa003049e2</span></span>                        |
| <span data-ttu-id="1b4cc-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b4cc-122">Syntax</span></span>            | [<span data-ttu-id="1b4cc-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1b4cc-123">**String(Unicode)**</span></span>](s-string-unicode.md)                 |



## <a name="implementations"></a><span data-ttu-id="1b4cc-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="1b4cc-124">Implementations</span></span>

-   [<span data-ttu-id="1b4cc-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1b4cc-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1b4cc-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1b4cc-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1b4cc-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1b4cc-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1b4cc-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1b4cc-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1b4cc-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1b4cc-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1b4cc-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1b4cc-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1b4cc-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1b4cc-131">Windows 2000 Server</span></span>



| <span data-ttu-id="1b4cc-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1b4cc-132">Entry</span></span> | <span data-ttu-id="1b4cc-133">Wert</span><span class="sxs-lookup"><span data-stu-id="1b4cc-133">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="1b4cc-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1b4cc-134">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="1b4cc-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b4cc-135">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="1b4cc-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b4cc-136">System-Only</span></span>            | <span data-ttu-id="1b4cc-137">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-137">False</span></span>                                          |
| <span data-ttu-id="1b4cc-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1b4cc-138">Is-Single-Valued</span></span>       | <span data-ttu-id="1b4cc-139">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-139">False</span></span>                                          |
| <span data-ttu-id="1b4cc-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1b4cc-140">Is Indexed</span></span>             | <span data-ttu-id="1b4cc-141">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-141">False</span></span>                                          |
| <span data-ttu-id="1b4cc-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1b4cc-142">In Global Catalog</span></span>      | <span data-ttu-id="1b4cc-143">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-143">False</span></span>                                          |
| <span data-ttu-id="1b4cc-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1b4cc-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b4cc-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1b4cc-145">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="1b4cc-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b4cc-146">Range-Lower</span></span>            | <span data-ttu-id="1b4cc-147">1</span><span class="sxs-lookup"><span data-stu-id="1b4cc-147">1</span></span>                                              |
| <span data-ttu-id="1b4cc-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b4cc-148">Range-Upper</span></span>            | <span data-ttu-id="1b4cc-149">256</span><span class="sxs-lookup"><span data-stu-id="1b4cc-149">256</span></span>                                            |
| <span data-ttu-id="1b4cc-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b4cc-150">Search-Flags</span></span>           | <span data-ttu-id="1b4cc-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b4cc-151">0x00000000</span></span>                                     |
| <span data-ttu-id="1b4cc-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b4cc-152">System-Flags</span></span>           | <span data-ttu-id="1b4cc-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b4cc-153">0x00000010</span></span>                                     |
| <span data-ttu-id="1b4cc-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1b4cc-154">Classes used in</span></span>        | [<span data-ttu-id="1b4cc-155">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="1b4cc-155">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1b4cc-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1b4cc-156">Windows Server 2003</span></span>



| <span data-ttu-id="1b4cc-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1b4cc-157">Entry</span></span> | <span data-ttu-id="1b4cc-158">Wert</span><span class="sxs-lookup"><span data-stu-id="1b4cc-158">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="1b4cc-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1b4cc-159">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="1b4cc-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b4cc-160">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="1b4cc-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b4cc-161">System-Only</span></span>            | <span data-ttu-id="1b4cc-162">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-162">False</span></span>                                          |
| <span data-ttu-id="1b4cc-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1b4cc-163">Is-Single-Valued</span></span>       | <span data-ttu-id="1b4cc-164">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-164">False</span></span>                                          |
| <span data-ttu-id="1b4cc-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1b4cc-165">Is Indexed</span></span>             | <span data-ttu-id="1b4cc-166">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-166">False</span></span>                                          |
| <span data-ttu-id="1b4cc-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1b4cc-167">In Global Catalog</span></span>      | <span data-ttu-id="1b4cc-168">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-168">False</span></span>                                          |
| <span data-ttu-id="1b4cc-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1b4cc-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b4cc-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1b4cc-170">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="1b4cc-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b4cc-171">Range-Lower</span></span>            | <span data-ttu-id="1b4cc-172">1</span><span class="sxs-lookup"><span data-stu-id="1b4cc-172">1</span></span>                                              |
| <span data-ttu-id="1b4cc-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b4cc-173">Range-Upper</span></span>            | <span data-ttu-id="1b4cc-174">256</span><span class="sxs-lookup"><span data-stu-id="1b4cc-174">256</span></span>                                            |
| <span data-ttu-id="1b4cc-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b4cc-175">Search-Flags</span></span>           | <span data-ttu-id="1b4cc-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b4cc-176">0x00000000</span></span>                                     |
| <span data-ttu-id="1b4cc-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b4cc-177">System-Flags</span></span>           | <span data-ttu-id="1b4cc-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b4cc-178">0x00000010</span></span>                                     |
| <span data-ttu-id="1b4cc-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1b4cc-179">Classes used in</span></span>        | [<span data-ttu-id="1b4cc-180">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="1b4cc-180">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1b4cc-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1b4cc-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1b4cc-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1b4cc-182">Entry</span></span> | <span data-ttu-id="1b4cc-183">Wert</span><span class="sxs-lookup"><span data-stu-id="1b4cc-183">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="1b4cc-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1b4cc-184">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="1b4cc-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b4cc-185">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="1b4cc-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b4cc-186">System-Only</span></span>            | <span data-ttu-id="1b4cc-187">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-187">False</span></span>                                          |
| <span data-ttu-id="1b4cc-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1b4cc-188">Is-Single-Valued</span></span>       | <span data-ttu-id="1b4cc-189">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-189">False</span></span>                                          |
| <span data-ttu-id="1b4cc-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1b4cc-190">Is Indexed</span></span>             | <span data-ttu-id="1b4cc-191">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-191">False</span></span>                                          |
| <span data-ttu-id="1b4cc-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1b4cc-192">In Global Catalog</span></span>      | <span data-ttu-id="1b4cc-193">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-193">False</span></span>                                          |
| <span data-ttu-id="1b4cc-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1b4cc-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b4cc-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1b4cc-195">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="1b4cc-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b4cc-196">Range-Lower</span></span>            | <span data-ttu-id="1b4cc-197">1</span><span class="sxs-lookup"><span data-stu-id="1b4cc-197">1</span></span>                                              |
| <span data-ttu-id="1b4cc-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b4cc-198">Range-Upper</span></span>            | <span data-ttu-id="1b4cc-199">256</span><span class="sxs-lookup"><span data-stu-id="1b4cc-199">256</span></span>                                            |
| <span data-ttu-id="1b4cc-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b4cc-200">Search-Flags</span></span>           | <span data-ttu-id="1b4cc-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b4cc-201">0x00000000</span></span>                                     |
| <span data-ttu-id="1b4cc-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b4cc-202">System-Flags</span></span>           | <span data-ttu-id="1b4cc-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b4cc-203">0x00000010</span></span>                                     |
| <span data-ttu-id="1b4cc-204">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1b4cc-204">Classes used in</span></span>        | [<span data-ttu-id="1b4cc-205">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="1b4cc-205">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1b4cc-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b4cc-206">Windows Server 2008</span></span>



| <span data-ttu-id="1b4cc-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1b4cc-207">Entry</span></span> | <span data-ttu-id="1b4cc-208">Wert</span><span class="sxs-lookup"><span data-stu-id="1b4cc-208">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="1b4cc-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1b4cc-209">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="1b4cc-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b4cc-210">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="1b4cc-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b4cc-211">System-Only</span></span>            | <span data-ttu-id="1b4cc-212">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-212">False</span></span>                                          |
| <span data-ttu-id="1b4cc-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1b4cc-213">Is-Single-Valued</span></span>       | <span data-ttu-id="1b4cc-214">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-214">False</span></span>                                          |
| <span data-ttu-id="1b4cc-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1b4cc-215">Is Indexed</span></span>             | <span data-ttu-id="1b4cc-216">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-216">False</span></span>                                          |
| <span data-ttu-id="1b4cc-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1b4cc-217">In Global Catalog</span></span>      | <span data-ttu-id="1b4cc-218">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-218">False</span></span>                                          |
| <span data-ttu-id="1b4cc-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1b4cc-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b4cc-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1b4cc-220">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="1b4cc-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b4cc-221">Range-Lower</span></span>            | <span data-ttu-id="1b4cc-222">1</span><span class="sxs-lookup"><span data-stu-id="1b4cc-222">1</span></span>                                              |
| <span data-ttu-id="1b4cc-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b4cc-223">Range-Upper</span></span>            | <span data-ttu-id="1b4cc-224">256</span><span class="sxs-lookup"><span data-stu-id="1b4cc-224">256</span></span>                                            |
| <span data-ttu-id="1b4cc-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b4cc-225">Search-Flags</span></span>           | <span data-ttu-id="1b4cc-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b4cc-226">0x00000000</span></span>                                     |
| <span data-ttu-id="1b4cc-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b4cc-227">System-Flags</span></span>           | <span data-ttu-id="1b4cc-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b4cc-228">0x00000010</span></span>                                     |
| <span data-ttu-id="1b4cc-229">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1b4cc-229">Classes used in</span></span>        | [<span data-ttu-id="1b4cc-230">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="1b4cc-230">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1b4cc-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1b4cc-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1b4cc-232">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1b4cc-232">Entry</span></span> | <span data-ttu-id="1b4cc-233">Wert</span><span class="sxs-lookup"><span data-stu-id="1b4cc-233">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="1b4cc-234">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1b4cc-234">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="1b4cc-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b4cc-235">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="1b4cc-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b4cc-236">System-Only</span></span>            | <span data-ttu-id="1b4cc-237">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-237">False</span></span>                                          |
| <span data-ttu-id="1b4cc-238">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1b4cc-238">Is-Single-Valued</span></span>       | <span data-ttu-id="1b4cc-239">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-239">False</span></span>                                          |
| <span data-ttu-id="1b4cc-240">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1b4cc-240">Is Indexed</span></span>             | <span data-ttu-id="1b4cc-241">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-241">False</span></span>                                          |
| <span data-ttu-id="1b4cc-242">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1b4cc-242">In Global Catalog</span></span>      | <span data-ttu-id="1b4cc-243">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-243">False</span></span>                                          |
| <span data-ttu-id="1b4cc-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1b4cc-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b4cc-245">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1b4cc-245">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="1b4cc-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b4cc-246">Range-Lower</span></span>            | <span data-ttu-id="1b4cc-247">1</span><span class="sxs-lookup"><span data-stu-id="1b4cc-247">1</span></span>                                              |
| <span data-ttu-id="1b4cc-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b4cc-248">Range-Upper</span></span>            | <span data-ttu-id="1b4cc-249">256</span><span class="sxs-lookup"><span data-stu-id="1b4cc-249">256</span></span>                                            |
| <span data-ttu-id="1b4cc-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b4cc-250">Search-Flags</span></span>           | <span data-ttu-id="1b4cc-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b4cc-251">0x00000000</span></span>                                     |
| <span data-ttu-id="1b4cc-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b4cc-252">System-Flags</span></span>           | <span data-ttu-id="1b4cc-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b4cc-253">0x00000010</span></span>                                     |
| <span data-ttu-id="1b4cc-254">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1b4cc-254">Classes used in</span></span>        | [<span data-ttu-id="1b4cc-255">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="1b4cc-255">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1b4cc-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1b4cc-256">Windows Server 2012</span></span>



| <span data-ttu-id="1b4cc-257">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1b4cc-257">Entry</span></span> | <span data-ttu-id="1b4cc-258">Wert</span><span class="sxs-lookup"><span data-stu-id="1b4cc-258">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="1b4cc-259">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1b4cc-259">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="1b4cc-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b4cc-260">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="1b4cc-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b4cc-261">System-Only</span></span>            | <span data-ttu-id="1b4cc-262">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-262">False</span></span>                                          |
| <span data-ttu-id="1b4cc-263">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1b4cc-263">Is-Single-Valued</span></span>       | <span data-ttu-id="1b4cc-264">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-264">False</span></span>                                          |
| <span data-ttu-id="1b4cc-265">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1b4cc-265">Is Indexed</span></span>             | <span data-ttu-id="1b4cc-266">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-266">False</span></span>                                          |
| <span data-ttu-id="1b4cc-267">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1b4cc-267">In Global Catalog</span></span>      | <span data-ttu-id="1b4cc-268">False</span><span class="sxs-lookup"><span data-stu-id="1b4cc-268">False</span></span>                                          |
| <span data-ttu-id="1b4cc-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1b4cc-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b4cc-270">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1b4cc-270">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="1b4cc-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b4cc-271">Range-Lower</span></span>            | <span data-ttu-id="1b4cc-272">1</span><span class="sxs-lookup"><span data-stu-id="1b4cc-272">1</span></span>                                              |
| <span data-ttu-id="1b4cc-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b4cc-273">Range-Upper</span></span>            | <span data-ttu-id="1b4cc-274">256</span><span class="sxs-lookup"><span data-stu-id="1b4cc-274">256</span></span>                                            |
| <span data-ttu-id="1b4cc-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b4cc-275">Search-Flags</span></span>           | <span data-ttu-id="1b4cc-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b4cc-276">0x00000000</span></span>                                     |
| <span data-ttu-id="1b4cc-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b4cc-277">System-Flags</span></span>           | <span data-ttu-id="1b4cc-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b4cc-278">0x00000010</span></span>                                     |
| <span data-ttu-id="1b4cc-279">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1b4cc-279">Classes used in</span></span>        | [<span data-ttu-id="1b4cc-280">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="1b4cc-280">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





