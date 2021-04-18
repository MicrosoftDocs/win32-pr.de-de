---
title: RDN-Attribut
description: Der Relative Distinguished Name (RDN) eines Objekts.
ms.assetid: 07fe0e81-1b18-4dbb-abca-a059a8bf993e
ms.tgt_platform: multiple
keywords:
- AD-Schema für RDN-Attribut
- Namensattribut AD-Schema
topic_type:
- apiref
api_name:
- RDN
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe49bd525d0fa3f4ed95874f2020d9d2a5eb9554
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344140"
---
# <a name="rdn-attribute"></a><span data-ttu-id="c4f30-105">RDN-Attribut</span><span class="sxs-lookup"><span data-stu-id="c4f30-105">RDN attribute</span></span>

<span data-ttu-id="c4f30-106">Der Relative Distinguished Name (RDN) eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="c4f30-106">The Relative Distinguished Name (RDN) of an object.</span></span> <span data-ttu-id="c4f30-107">Ein RDN ist der relative Teil eines Distinguished Name (DN), der ein LDAP-Objekt eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c4f30-107">An RDN is the relative portion of a distinguished name (DN), which uniquely identifies an LDAP object.</span></span>



| <span data-ttu-id="c4f30-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4f30-108">Entry</span></span> | <span data-ttu-id="c4f30-109">Wert</span><span class="sxs-lookup"><span data-stu-id="c4f30-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="c4f30-110">CN</span><span class="sxs-lookup"><span data-stu-id="c4f30-110">CN</span></span>                | <span data-ttu-id="c4f30-111">RDN</span><span class="sxs-lookup"><span data-stu-id="c4f30-111">RDN</span></span>                                            |
| <span data-ttu-id="c4f30-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c4f30-112">Ldap-Display-Name</span></span> | <span data-ttu-id="c4f30-113">name</span><span class="sxs-lookup"><span data-stu-id="c4f30-113">name</span></span>                                           |
| <span data-ttu-id="c4f30-114">Size</span><span class="sxs-lookup"><span data-stu-id="c4f30-114">Size</span></span>              | \-                                             |
| <span data-ttu-id="c4f30-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c4f30-115">Update Privilege</span></span>  | <span data-ttu-id="c4f30-116">Dieser Wert wird vom Schema Administrator festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c4f30-116">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="c4f30-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="c4f30-117">Update Frequency</span></span>  | \-                                             |
| <span data-ttu-id="c4f30-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c4f30-118">Attribute-Id</span></span>      | <span data-ttu-id="c4f30-119">1.2.840.113556.1.4.1</span><span class="sxs-lookup"><span data-stu-id="c4f30-119">1.2.840.113556.1.4.1</span></span>                           |
| <span data-ttu-id="c4f30-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c4f30-120">System-Id-Guid</span></span>    | <span data-ttu-id="c4f30-121">bf967a0e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c4f30-121">bf967a0e-0de6-11d0-a285-00aa003049e2</span></span>           |
| <span data-ttu-id="c4f30-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4f30-122">Syntax</span></span>            | [<span data-ttu-id="c4f30-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c4f30-123">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="c4f30-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="c4f30-124">Implementations</span></span>

-   [<span data-ttu-id="c4f30-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c4f30-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c4f30-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c4f30-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c4f30-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="c4f30-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c4f30-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c4f30-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c4f30-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c4f30-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c4f30-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c4f30-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c4f30-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c4f30-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c4f30-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c4f30-132">Windows 2000 Server</span></span>



| <span data-ttu-id="c4f30-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4f30-133">Entry</span></span> | <span data-ttu-id="c4f30-134">Wert</span><span class="sxs-lookup"><span data-stu-id="c4f30-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c4f30-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c4f30-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c4f30-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4f30-136">MAPI-Id</span></span>                | <span data-ttu-id="c4f30-137">0x8202</span><span class="sxs-lookup"><span data-stu-id="c4f30-137">0x8202</span></span>                          |
| <span data-ttu-id="c4f30-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4f30-138">System-Only</span></span>            | <span data-ttu-id="c4f30-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-139">True</span></span>                            |
| <span data-ttu-id="c4f30-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c4f30-140">Is-Single-Valued</span></span>       | <span data-ttu-id="c4f30-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-141">True</span></span>                            |
| <span data-ttu-id="c4f30-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c4f30-142">Is Indexed</span></span>             | <span data-ttu-id="c4f30-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-143">True</span></span>                            |
| <span data-ttu-id="c4f30-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c4f30-144">In Global Catalog</span></span>      | <span data-ttu-id="c4f30-145">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-145">True</span></span>                            |
| <span data-ttu-id="c4f30-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4f30-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4f30-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c4f30-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c4f30-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4f30-148">Range-Lower</span></span>            | <span data-ttu-id="c4f30-149">1</span><span class="sxs-lookup"><span data-stu-id="c4f30-149">1</span></span>                               |
| <span data-ttu-id="c4f30-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4f30-150">Range-Upper</span></span>            | <span data-ttu-id="c4f30-151">255</span><span class="sxs-lookup"><span data-stu-id="c4f30-151">255</span></span>                             |
| <span data-ttu-id="c4f30-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4f30-152">Search-Flags</span></span>           | <span data-ttu-id="c4f30-153">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="c4f30-153">0x0000000D</span></span>                      |
| <span data-ttu-id="c4f30-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4f30-154">System-Flags</span></span>           | <span data-ttu-id="c4f30-155">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c4f30-155">0x00000012</span></span>                      |
| <span data-ttu-id="c4f30-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c4f30-156">Classes used in</span></span>        | [<span data-ttu-id="c4f30-157">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c4f30-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c4f30-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c4f30-158">Windows Server 2003</span></span>



| <span data-ttu-id="c4f30-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4f30-159">Entry</span></span> | <span data-ttu-id="c4f30-160">Wert</span><span class="sxs-lookup"><span data-stu-id="c4f30-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c4f30-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c4f30-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c4f30-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4f30-162">MAPI-Id</span></span>                | <span data-ttu-id="c4f30-163">0x8202</span><span class="sxs-lookup"><span data-stu-id="c4f30-163">0x8202</span></span>                          |
| <span data-ttu-id="c4f30-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4f30-164">System-Only</span></span>            | <span data-ttu-id="c4f30-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-165">True</span></span>                            |
| <span data-ttu-id="c4f30-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c4f30-166">Is-Single-Valued</span></span>       | <span data-ttu-id="c4f30-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-167">True</span></span>                            |
| <span data-ttu-id="c4f30-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c4f30-168">Is Indexed</span></span>             | <span data-ttu-id="c4f30-169">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-169">True</span></span>                            |
| <span data-ttu-id="c4f30-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c4f30-170">In Global Catalog</span></span>      | <span data-ttu-id="c4f30-171">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-171">True</span></span>                            |
| <span data-ttu-id="c4f30-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4f30-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4f30-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c4f30-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c4f30-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4f30-174">Range-Lower</span></span>            | <span data-ttu-id="c4f30-175">1</span><span class="sxs-lookup"><span data-stu-id="c4f30-175">1</span></span>                               |
| <span data-ttu-id="c4f30-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4f30-176">Range-Upper</span></span>            | <span data-ttu-id="c4f30-177">255</span><span class="sxs-lookup"><span data-stu-id="c4f30-177">255</span></span>                             |
| <span data-ttu-id="c4f30-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4f30-178">Search-Flags</span></span>           | <span data-ttu-id="c4f30-179">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="c4f30-179">0x0000000D</span></span>                      |
| <span data-ttu-id="c4f30-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4f30-180">System-Flags</span></span>           | <span data-ttu-id="c4f30-181">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c4f30-181">0x00000012</span></span>                      |
| <span data-ttu-id="c4f30-182">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c4f30-182">Classes used in</span></span>        | [<span data-ttu-id="c4f30-183">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c4f30-183">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c4f30-184">Adam</span><span class="sxs-lookup"><span data-stu-id="c4f30-184">ADAM</span></span>



| <span data-ttu-id="c4f30-185">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4f30-185">Entry</span></span> | <span data-ttu-id="c4f30-186">Wert</span><span class="sxs-lookup"><span data-stu-id="c4f30-186">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c4f30-187">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c4f30-187">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c4f30-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4f30-188">MAPI-Id</span></span>                | <span data-ttu-id="c4f30-189">0x8202</span><span class="sxs-lookup"><span data-stu-id="c4f30-189">0x8202</span></span>                          |
| <span data-ttu-id="c4f30-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4f30-190">System-Only</span></span>            | <span data-ttu-id="c4f30-191">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-191">True</span></span>                            |
| <span data-ttu-id="c4f30-192">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c4f30-192">Is-Single-Valued</span></span>       | <span data-ttu-id="c4f30-193">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-193">True</span></span>                            |
| <span data-ttu-id="c4f30-194">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c4f30-194">Is Indexed</span></span>             | <span data-ttu-id="c4f30-195">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-195">True</span></span>                            |
| <span data-ttu-id="c4f30-196">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c4f30-196">In Global Catalog</span></span>      | <span data-ttu-id="c4f30-197">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-197">True</span></span>                            |
| <span data-ttu-id="c4f30-198">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4f30-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4f30-199">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c4f30-199">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c4f30-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4f30-200">Range-Lower</span></span>            | <span data-ttu-id="c4f30-201">1</span><span class="sxs-lookup"><span data-stu-id="c4f30-201">1</span></span>                               |
| <span data-ttu-id="c4f30-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4f30-202">Range-Upper</span></span>            | <span data-ttu-id="c4f30-203">255</span><span class="sxs-lookup"><span data-stu-id="c4f30-203">255</span></span>                             |
| <span data-ttu-id="c4f30-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4f30-204">Search-Flags</span></span>           | <span data-ttu-id="c4f30-205">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="c4f30-205">0x0000000D</span></span>                      |
| <span data-ttu-id="c4f30-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4f30-206">System-Flags</span></span>           | <span data-ttu-id="c4f30-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c4f30-207">0x00000012</span></span>                      |
| <span data-ttu-id="c4f30-208">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c4f30-208">Classes used in</span></span>        | [<span data-ttu-id="c4f30-209">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c4f30-209">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c4f30-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c4f30-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c4f30-211">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4f30-211">Entry</span></span> | <span data-ttu-id="c4f30-212">Wert</span><span class="sxs-lookup"><span data-stu-id="c4f30-212">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c4f30-213">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c4f30-213">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c4f30-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4f30-214">MAPI-Id</span></span>                | <span data-ttu-id="c4f30-215">0x8202</span><span class="sxs-lookup"><span data-stu-id="c4f30-215">0x8202</span></span>                          |
| <span data-ttu-id="c4f30-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4f30-216">System-Only</span></span>            | <span data-ttu-id="c4f30-217">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-217">True</span></span>                            |
| <span data-ttu-id="c4f30-218">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c4f30-218">Is-Single-Valued</span></span>       | <span data-ttu-id="c4f30-219">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-219">True</span></span>                            |
| <span data-ttu-id="c4f30-220">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c4f30-220">Is Indexed</span></span>             | <span data-ttu-id="c4f30-221">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-221">True</span></span>                            |
| <span data-ttu-id="c4f30-222">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c4f30-222">In Global Catalog</span></span>      | <span data-ttu-id="c4f30-223">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-223">True</span></span>                            |
| <span data-ttu-id="c4f30-224">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4f30-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4f30-225">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c4f30-225">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c4f30-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4f30-226">Range-Lower</span></span>            | <span data-ttu-id="c4f30-227">1</span><span class="sxs-lookup"><span data-stu-id="c4f30-227">1</span></span>                               |
| <span data-ttu-id="c4f30-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4f30-228">Range-Upper</span></span>            | <span data-ttu-id="c4f30-229">255</span><span class="sxs-lookup"><span data-stu-id="c4f30-229">255</span></span>                             |
| <span data-ttu-id="c4f30-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4f30-230">Search-Flags</span></span>           | <span data-ttu-id="c4f30-231">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="c4f30-231">0x0000000D</span></span>                      |
| <span data-ttu-id="c4f30-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4f30-232">System-Flags</span></span>           | <span data-ttu-id="c4f30-233">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c4f30-233">0x00000012</span></span>                      |
| <span data-ttu-id="c4f30-234">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c4f30-234">Classes used in</span></span>        | [<span data-ttu-id="c4f30-235">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c4f30-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c4f30-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4f30-236">Windows Server 2008</span></span>



| <span data-ttu-id="c4f30-237">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4f30-237">Entry</span></span> | <span data-ttu-id="c4f30-238">Wert</span><span class="sxs-lookup"><span data-stu-id="c4f30-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c4f30-239">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c4f30-239">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c4f30-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4f30-240">MAPI-Id</span></span>                | <span data-ttu-id="c4f30-241">0x8202</span><span class="sxs-lookup"><span data-stu-id="c4f30-241">0x8202</span></span>                          |
| <span data-ttu-id="c4f30-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4f30-242">System-Only</span></span>            | <span data-ttu-id="c4f30-243">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-243">True</span></span>                            |
| <span data-ttu-id="c4f30-244">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c4f30-244">Is-Single-Valued</span></span>       | <span data-ttu-id="c4f30-245">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-245">True</span></span>                            |
| <span data-ttu-id="c4f30-246">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c4f30-246">Is Indexed</span></span>             | <span data-ttu-id="c4f30-247">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-247">True</span></span>                            |
| <span data-ttu-id="c4f30-248">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c4f30-248">In Global Catalog</span></span>      | <span data-ttu-id="c4f30-249">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-249">True</span></span>                            |
| <span data-ttu-id="c4f30-250">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4f30-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4f30-251">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c4f30-251">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c4f30-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4f30-252">Range-Lower</span></span>            | <span data-ttu-id="c4f30-253">1</span><span class="sxs-lookup"><span data-stu-id="c4f30-253">1</span></span>                               |
| <span data-ttu-id="c4f30-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4f30-254">Range-Upper</span></span>            | <span data-ttu-id="c4f30-255">255</span><span class="sxs-lookup"><span data-stu-id="c4f30-255">255</span></span>                             |
| <span data-ttu-id="c4f30-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4f30-256">Search-Flags</span></span>           | <span data-ttu-id="c4f30-257">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="c4f30-257">0x0000000D</span></span>                      |
| <span data-ttu-id="c4f30-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4f30-258">System-Flags</span></span>           | <span data-ttu-id="c4f30-259">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c4f30-259">0x00000012</span></span>                      |
| <span data-ttu-id="c4f30-260">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c4f30-260">Classes used in</span></span>        | [<span data-ttu-id="c4f30-261">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c4f30-261">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c4f30-262">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c4f30-262">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c4f30-263">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4f30-263">Entry</span></span> | <span data-ttu-id="c4f30-264">Wert</span><span class="sxs-lookup"><span data-stu-id="c4f30-264">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c4f30-265">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c4f30-265">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c4f30-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4f30-266">MAPI-Id</span></span>                | <span data-ttu-id="c4f30-267">0x8202</span><span class="sxs-lookup"><span data-stu-id="c4f30-267">0x8202</span></span>                          |
| <span data-ttu-id="c4f30-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4f30-268">System-Only</span></span>            | <span data-ttu-id="c4f30-269">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-269">True</span></span>                            |
| <span data-ttu-id="c4f30-270">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c4f30-270">Is-Single-Valued</span></span>       | <span data-ttu-id="c4f30-271">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-271">True</span></span>                            |
| <span data-ttu-id="c4f30-272">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c4f30-272">Is Indexed</span></span>             | <span data-ttu-id="c4f30-273">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-273">True</span></span>                            |
| <span data-ttu-id="c4f30-274">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c4f30-274">In Global Catalog</span></span>      | <span data-ttu-id="c4f30-275">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-275">True</span></span>                            |
| <span data-ttu-id="c4f30-276">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4f30-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4f30-277">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c4f30-277">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c4f30-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4f30-278">Range-Lower</span></span>            | <span data-ttu-id="c4f30-279">1</span><span class="sxs-lookup"><span data-stu-id="c4f30-279">1</span></span>                               |
| <span data-ttu-id="c4f30-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4f30-280">Range-Upper</span></span>            | <span data-ttu-id="c4f30-281">255</span><span class="sxs-lookup"><span data-stu-id="c4f30-281">255</span></span>                             |
| <span data-ttu-id="c4f30-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4f30-282">Search-Flags</span></span>           | <span data-ttu-id="c4f30-283">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="c4f30-283">0x0000000D</span></span>                      |
| <span data-ttu-id="c4f30-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4f30-284">System-Flags</span></span>           | <span data-ttu-id="c4f30-285">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c4f30-285">0x00000012</span></span>                      |
| <span data-ttu-id="c4f30-286">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c4f30-286">Classes used in</span></span>        | [<span data-ttu-id="c4f30-287">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c4f30-287">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c4f30-288">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c4f30-288">Windows Server 2012</span></span>



| <span data-ttu-id="c4f30-289">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4f30-289">Entry</span></span> | <span data-ttu-id="c4f30-290">Wert</span><span class="sxs-lookup"><span data-stu-id="c4f30-290">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c4f30-291">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c4f30-291">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c4f30-292">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4f30-292">MAPI-Id</span></span>                | <span data-ttu-id="c4f30-293">0x8202</span><span class="sxs-lookup"><span data-stu-id="c4f30-293">0x8202</span></span>                          |
| <span data-ttu-id="c4f30-294">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4f30-294">System-Only</span></span>            | <span data-ttu-id="c4f30-295">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-295">True</span></span>                            |
| <span data-ttu-id="c4f30-296">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c4f30-296">Is-Single-Valued</span></span>       | <span data-ttu-id="c4f30-297">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-297">True</span></span>                            |
| <span data-ttu-id="c4f30-298">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c4f30-298">Is Indexed</span></span>             | <span data-ttu-id="c4f30-299">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-299">True</span></span>                            |
| <span data-ttu-id="c4f30-300">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c4f30-300">In Global Catalog</span></span>      | <span data-ttu-id="c4f30-301">Richtig</span><span class="sxs-lookup"><span data-stu-id="c4f30-301">True</span></span>                            |
| <span data-ttu-id="c4f30-302">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4f30-302">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4f30-303">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c4f30-303">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c4f30-304">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4f30-304">Range-Lower</span></span>            | <span data-ttu-id="c4f30-305">1</span><span class="sxs-lookup"><span data-stu-id="c4f30-305">1</span></span>                               |
| <span data-ttu-id="c4f30-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4f30-306">Range-Upper</span></span>            | <span data-ttu-id="c4f30-307">255</span><span class="sxs-lookup"><span data-stu-id="c4f30-307">255</span></span>                             |
| <span data-ttu-id="c4f30-308">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4f30-308">Search-Flags</span></span>           | <span data-ttu-id="c4f30-309">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="c4f30-309">0x0000000D</span></span>                      |
| <span data-ttu-id="c4f30-310">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4f30-310">System-Flags</span></span>           | <span data-ttu-id="c4f30-311">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c4f30-311">0x00000012</span></span>                      |
| <span data-ttu-id="c4f30-312">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c4f30-312">Classes used in</span></span>        | [<span data-ttu-id="c4f30-313">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="c4f30-313">**Top**</span></span>](c-top.md)<br/> |



 

 





