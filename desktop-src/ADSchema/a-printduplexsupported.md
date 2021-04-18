---
title: Print-Duplex unterstütztes Attribut
description: Gibt den Typ der Duplex Unterstützung eines Druckers an.
ms.assetid: c7d3e3f1-d6a1-41b7-a54d-c932a00b2a68
ms.tgt_platform: multiple
keywords:
- Print-Duplex unterstütztes AD-Schema für Attribute
- printduplexsupported-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Print-Duplex-Supported
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7027b5af8d2c2bc8ece810a00c17060608b7824c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106338823"
---
# <a name="print-duplex-supported-attribute"></a><span data-ttu-id="ecd2f-105">Print-Duplex unterstütztes Attribut</span><span class="sxs-lookup"><span data-stu-id="ecd2f-105">Print-Duplex-Supported attribute</span></span>

<span data-ttu-id="ecd2f-106">Gibt den Typ der Duplex Unterstützung eines Druckers an.</span><span class="sxs-lookup"><span data-stu-id="ecd2f-106">Indicates the type of duplex support a printer has.</span></span>



| <span data-ttu-id="ecd2f-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ecd2f-107">Entry</span></span> | <span data-ttu-id="ecd2f-108">Wert</span><span class="sxs-lookup"><span data-stu-id="ecd2f-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="ecd2f-109">CN</span><span class="sxs-lookup"><span data-stu-id="ecd2f-109">CN</span></span>                | <span data-ttu-id="ecd2f-110">Print-Duplex-unterstützt</span><span class="sxs-lookup"><span data-stu-id="ecd2f-110">Print-Duplex-Supported</span></span>                                |
| <span data-ttu-id="ecd2f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ecd2f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ecd2f-112">printDuplexSupported</span><span class="sxs-lookup"><span data-stu-id="ecd2f-112">printDuplexSupported</span></span>                                  |
| <span data-ttu-id="ecd2f-113">Size</span><span class="sxs-lookup"><span data-stu-id="ecd2f-113">Size</span></span>              | <span data-ttu-id="ecd2f-114">4 Bytes.</span><span class="sxs-lookup"><span data-stu-id="ecd2f-114">4 bytes.</span></span> <span data-ttu-id="ecd2f-115">Duplex unterstützt = 2.</span><span class="sxs-lookup"><span data-stu-id="ecd2f-115">Duplex supported = 2.</span></span> <span data-ttu-id="ecd2f-116">Nur simplex = 1 oder 0.</span><span class="sxs-lookup"><span data-stu-id="ecd2f-116">Simplex only = 1 or 0.</span></span> |
| <span data-ttu-id="ecd2f-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ecd2f-117">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="ecd2f-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="ecd2f-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="ecd2f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ecd2f-119">Attribute-Id</span></span>      | <span data-ttu-id="ecd2f-120">1.2.840.113556.1.4.1311</span><span class="sxs-lookup"><span data-stu-id="ecd2f-120">1.2.840.113556.1.4.1311</span></span>                               |
| <span data-ttu-id="ecd2f-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ecd2f-121">System-Id-Guid</span></span>    | <span data-ttu-id="ecd2f-122">281416cc-1968-11D0-a28f -00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ecd2f-122">281416cc-1968-11d0-a28f-00aa003049e2</span></span>                  |
| <span data-ttu-id="ecd2f-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecd2f-123">Syntax</span></span>            | [<span data-ttu-id="ecd2f-124">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="ecd2f-124">**Boolean**</span></span>](s-boolean.md)                          |



## <a name="implementations"></a><span data-ttu-id="ecd2f-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ecd2f-125">Implementations</span></span>

-   [<span data-ttu-id="ecd2f-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ecd2f-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ecd2f-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ecd2f-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ecd2f-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ecd2f-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ecd2f-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ecd2f-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ecd2f-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ecd2f-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ecd2f-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ecd2f-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ecd2f-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ecd2f-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ecd2f-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ecd2f-133">Entry</span></span> | <span data-ttu-id="ecd2f-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ecd2f-134">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="ecd2f-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ecd2f-135">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="ecd2f-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecd2f-136">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="ecd2f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecd2f-137">System-Only</span></span>            | <span data-ttu-id="ecd2f-138">False</span><span class="sxs-lookup"><span data-stu-id="ecd2f-138">False</span></span>                                          |
| <span data-ttu-id="ecd2f-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ecd2f-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-140">True</span></span>                                           |
| <span data-ttu-id="ecd2f-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ecd2f-141">Is Indexed</span></span>             | <span data-ttu-id="ecd2f-142">False</span><span class="sxs-lookup"><span data-stu-id="ecd2f-142">False</span></span>                                          |
| <span data-ttu-id="ecd2f-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ecd2f-143">In Global Catalog</span></span>      | <span data-ttu-id="ecd2f-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-144">True</span></span>                                           |
| <span data-ttu-id="ecd2f-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ecd2f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecd2f-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ecd2f-146">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="ecd2f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecd2f-147">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="ecd2f-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecd2f-148">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="ecd2f-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecd2f-149">Search-Flags</span></span>           | <span data-ttu-id="ecd2f-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecd2f-150">0x00000000</span></span>                                     |
| <span data-ttu-id="ecd2f-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecd2f-151">System-Flags</span></span>           | <span data-ttu-id="ecd2f-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecd2f-152">0x00000010</span></span>                                     |
| <span data-ttu-id="ecd2f-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ecd2f-153">Classes used in</span></span>        | [<span data-ttu-id="ecd2f-154">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="ecd2f-154">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ecd2f-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ecd2f-155">Windows Server 2003</span></span>



| <span data-ttu-id="ecd2f-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ecd2f-156">Entry</span></span> | <span data-ttu-id="ecd2f-157">Wert</span><span class="sxs-lookup"><span data-stu-id="ecd2f-157">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="ecd2f-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ecd2f-158">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="ecd2f-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecd2f-159">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="ecd2f-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecd2f-160">System-Only</span></span>            | <span data-ttu-id="ecd2f-161">False</span><span class="sxs-lookup"><span data-stu-id="ecd2f-161">False</span></span>                                          |
| <span data-ttu-id="ecd2f-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ecd2f-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-163">True</span></span>                                           |
| <span data-ttu-id="ecd2f-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ecd2f-164">Is Indexed</span></span>             | <span data-ttu-id="ecd2f-165">False</span><span class="sxs-lookup"><span data-stu-id="ecd2f-165">False</span></span>                                          |
| <span data-ttu-id="ecd2f-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ecd2f-166">In Global Catalog</span></span>      | <span data-ttu-id="ecd2f-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-167">True</span></span>                                           |
| <span data-ttu-id="ecd2f-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ecd2f-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecd2f-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ecd2f-169">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="ecd2f-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecd2f-170">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="ecd2f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecd2f-171">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="ecd2f-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecd2f-172">Search-Flags</span></span>           | <span data-ttu-id="ecd2f-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecd2f-173">0x00000000</span></span>                                     |
| <span data-ttu-id="ecd2f-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecd2f-174">System-Flags</span></span>           | <span data-ttu-id="ecd2f-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecd2f-175">0x00000010</span></span>                                     |
| <span data-ttu-id="ecd2f-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ecd2f-176">Classes used in</span></span>        | [<span data-ttu-id="ecd2f-177">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="ecd2f-177">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ecd2f-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ecd2f-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ecd2f-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ecd2f-179">Entry</span></span> | <span data-ttu-id="ecd2f-180">Wert</span><span class="sxs-lookup"><span data-stu-id="ecd2f-180">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="ecd2f-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ecd2f-181">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="ecd2f-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecd2f-182">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="ecd2f-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecd2f-183">System-Only</span></span>            | <span data-ttu-id="ecd2f-184">False</span><span class="sxs-lookup"><span data-stu-id="ecd2f-184">False</span></span>                                          |
| <span data-ttu-id="ecd2f-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ecd2f-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-186">True</span></span>                                           |
| <span data-ttu-id="ecd2f-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ecd2f-187">Is Indexed</span></span>             | <span data-ttu-id="ecd2f-188">False</span><span class="sxs-lookup"><span data-stu-id="ecd2f-188">False</span></span>                                          |
| <span data-ttu-id="ecd2f-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ecd2f-189">In Global Catalog</span></span>      | <span data-ttu-id="ecd2f-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-190">True</span></span>                                           |
| <span data-ttu-id="ecd2f-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ecd2f-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecd2f-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ecd2f-192">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="ecd2f-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecd2f-193">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="ecd2f-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecd2f-194">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="ecd2f-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecd2f-195">Search-Flags</span></span>           | <span data-ttu-id="ecd2f-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecd2f-196">0x00000000</span></span>                                     |
| <span data-ttu-id="ecd2f-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecd2f-197">System-Flags</span></span>           | <span data-ttu-id="ecd2f-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecd2f-198">0x00000010</span></span>                                     |
| <span data-ttu-id="ecd2f-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ecd2f-199">Classes used in</span></span>        | [<span data-ttu-id="ecd2f-200">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="ecd2f-200">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ecd2f-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ecd2f-201">Windows Server 2008</span></span>



| <span data-ttu-id="ecd2f-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ecd2f-202">Entry</span></span> | <span data-ttu-id="ecd2f-203">Wert</span><span class="sxs-lookup"><span data-stu-id="ecd2f-203">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="ecd2f-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ecd2f-204">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="ecd2f-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecd2f-205">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="ecd2f-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecd2f-206">System-Only</span></span>            | <span data-ttu-id="ecd2f-207">False</span><span class="sxs-lookup"><span data-stu-id="ecd2f-207">False</span></span>                                          |
| <span data-ttu-id="ecd2f-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ecd2f-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-209">True</span></span>                                           |
| <span data-ttu-id="ecd2f-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ecd2f-210">Is Indexed</span></span>             | <span data-ttu-id="ecd2f-211">False</span><span class="sxs-lookup"><span data-stu-id="ecd2f-211">False</span></span>                                          |
| <span data-ttu-id="ecd2f-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ecd2f-212">In Global Catalog</span></span>      | <span data-ttu-id="ecd2f-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-213">True</span></span>                                           |
| <span data-ttu-id="ecd2f-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ecd2f-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecd2f-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ecd2f-215">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="ecd2f-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecd2f-216">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="ecd2f-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecd2f-217">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="ecd2f-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecd2f-218">Search-Flags</span></span>           | <span data-ttu-id="ecd2f-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecd2f-219">0x00000000</span></span>                                     |
| <span data-ttu-id="ecd2f-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecd2f-220">System-Flags</span></span>           | <span data-ttu-id="ecd2f-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecd2f-221">0x00000010</span></span>                                     |
| <span data-ttu-id="ecd2f-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ecd2f-222">Classes used in</span></span>        | [<span data-ttu-id="ecd2f-223">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="ecd2f-223">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ecd2f-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ecd2f-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ecd2f-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ecd2f-225">Entry</span></span> | <span data-ttu-id="ecd2f-226">Wert</span><span class="sxs-lookup"><span data-stu-id="ecd2f-226">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="ecd2f-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ecd2f-227">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="ecd2f-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecd2f-228">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="ecd2f-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecd2f-229">System-Only</span></span>            | <span data-ttu-id="ecd2f-230">False</span><span class="sxs-lookup"><span data-stu-id="ecd2f-230">False</span></span>                                          |
| <span data-ttu-id="ecd2f-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ecd2f-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-232">True</span></span>                                           |
| <span data-ttu-id="ecd2f-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ecd2f-233">Is Indexed</span></span>             | <span data-ttu-id="ecd2f-234">False</span><span class="sxs-lookup"><span data-stu-id="ecd2f-234">False</span></span>                                          |
| <span data-ttu-id="ecd2f-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ecd2f-235">In Global Catalog</span></span>      | <span data-ttu-id="ecd2f-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-236">True</span></span>                                           |
| <span data-ttu-id="ecd2f-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ecd2f-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecd2f-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ecd2f-238">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="ecd2f-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecd2f-239">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="ecd2f-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecd2f-240">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="ecd2f-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecd2f-241">Search-Flags</span></span>           | <span data-ttu-id="ecd2f-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecd2f-242">0x00000000</span></span>                                     |
| <span data-ttu-id="ecd2f-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecd2f-243">System-Flags</span></span>           | <span data-ttu-id="ecd2f-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecd2f-244">0x00000010</span></span>                                     |
| <span data-ttu-id="ecd2f-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ecd2f-245">Classes used in</span></span>        | [<span data-ttu-id="ecd2f-246">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="ecd2f-246">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ecd2f-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ecd2f-247">Windows Server 2012</span></span>



| <span data-ttu-id="ecd2f-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ecd2f-248">Entry</span></span> | <span data-ttu-id="ecd2f-249">Wert</span><span class="sxs-lookup"><span data-stu-id="ecd2f-249">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="ecd2f-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ecd2f-250">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="ecd2f-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecd2f-251">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="ecd2f-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecd2f-252">System-Only</span></span>            | <span data-ttu-id="ecd2f-253">False</span><span class="sxs-lookup"><span data-stu-id="ecd2f-253">False</span></span>                                          |
| <span data-ttu-id="ecd2f-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-254">Is-Single-Valued</span></span>       | <span data-ttu-id="ecd2f-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-255">True</span></span>                                           |
| <span data-ttu-id="ecd2f-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ecd2f-256">Is Indexed</span></span>             | <span data-ttu-id="ecd2f-257">False</span><span class="sxs-lookup"><span data-stu-id="ecd2f-257">False</span></span>                                          |
| <span data-ttu-id="ecd2f-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ecd2f-258">In Global Catalog</span></span>      | <span data-ttu-id="ecd2f-259">Richtig</span><span class="sxs-lookup"><span data-stu-id="ecd2f-259">True</span></span>                                           |
| <span data-ttu-id="ecd2f-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ecd2f-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecd2f-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ecd2f-261">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="ecd2f-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecd2f-262">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="ecd2f-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecd2f-263">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="ecd2f-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecd2f-264">Search-Flags</span></span>           | <span data-ttu-id="ecd2f-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecd2f-265">0x00000000</span></span>                                     |
| <span data-ttu-id="ecd2f-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecd2f-266">System-Flags</span></span>           | <span data-ttu-id="ecd2f-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecd2f-267">0x00000010</span></span>                                     |
| <span data-ttu-id="ecd2f-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ecd2f-268">Classes used in</span></span>        | [<span data-ttu-id="ecd2f-269">**Druck Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="ecd2f-269">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





