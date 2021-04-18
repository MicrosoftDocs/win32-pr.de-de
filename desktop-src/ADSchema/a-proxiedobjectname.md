---
title: Proxy-Object-Name-Attribut
description: Dieses Attribut wird intern von Active Directory verwendet, um die Verschiebung von zwischen Domänen zu unterstützen.
ms.assetid: 661ea322-f78c-44dc-8d64-4f28ead1a7aa
ms.tgt_platform: multiple
keywords:
- 'Proxy: Objekt Namensattribut AD-Schema'
- proxiedobjectname-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Proxied-Object-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ffafbbea411c950954102a788226c29589029e1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344517"
---
# <a name="proxied-object-name-attribute"></a><span data-ttu-id="0b94c-105">Proxy-Object-Name-Attribut</span><span class="sxs-lookup"><span data-stu-id="0b94c-105">Proxied-Object-Name attribute</span></span>

<span data-ttu-id="0b94c-106">Dieses Attribut wird intern von Active Directory verwendet, um die Verschiebung von zwischen Domänen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0b94c-106">This attribute is used internally by Active Directory to help track interdomain moves.</span></span>



| <span data-ttu-id="0b94c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b94c-107">Entry</span></span> | <span data-ttu-id="0b94c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="0b94c-108">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="0b94c-109">CN</span><span class="sxs-lookup"><span data-stu-id="0b94c-109">CN</span></span>                | <span data-ttu-id="0b94c-110">Proxy-Objekt Name</span><span class="sxs-lookup"><span data-stu-id="0b94c-110">Proxied-Object-Name</span></span>                             |
| <span data-ttu-id="0b94c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0b94c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0b94c-112">proxiedobjectname</span><span class="sxs-lookup"><span data-stu-id="0b94c-112">proxiedObjectName</span></span>                               |
| <span data-ttu-id="0b94c-113">Size</span><span class="sxs-lookup"><span data-stu-id="0b94c-113">Size</span></span>              | \-                                              |
| <span data-ttu-id="0b94c-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0b94c-114">Update Privilege</span></span>  | <span data-ttu-id="0b94c-115">Diese wird vom System verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b94c-115">This is used by the system.</span></span>                     |
| <span data-ttu-id="0b94c-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="0b94c-116">Update Frequency</span></span>  | \-                                              |
| <span data-ttu-id="0b94c-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0b94c-117">Attribute-Id</span></span>      | <span data-ttu-id="0b94c-118">1.2.840.113556.1.4.1249</span><span class="sxs-lookup"><span data-stu-id="0b94c-118">1.2.840.113556.1.4.1249</span></span>                         |
| <span data-ttu-id="0b94c-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0b94c-119">System-Id-Guid</span></span>    | <span data-ttu-id="0b94c-120">e1aea402-cd5b-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="0b94c-120">e1aea402-cd5b-11d0-afff-0000f80367c1</span></span>            |
| <span data-ttu-id="0b94c-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b94c-121">Syntax</span></span>            | [<span data-ttu-id="0b94c-122">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="0b94c-122">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="0b94c-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="0b94c-123">Implementations</span></span>

-   [<span data-ttu-id="0b94c-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0b94c-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0b94c-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0b94c-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0b94c-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="0b94c-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0b94c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0b94c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0b94c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0b94c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0b94c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0b94c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0b94c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0b94c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0b94c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0b94c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0b94c-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b94c-132">Entry</span></span> | <span data-ttu-id="0b94c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="0b94c-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b94c-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b94c-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0b94c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b94c-135">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0b94c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b94c-136">System-Only</span></span>            | <span data-ttu-id="0b94c-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-137">True</span></span>                            |
| <span data-ttu-id="0b94c-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b94c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0b94c-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-139">True</span></span>                            |
| <span data-ttu-id="0b94c-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b94c-140">Is Indexed</span></span>             | <span data-ttu-id="0b94c-141">False</span><span class="sxs-lookup"><span data-stu-id="0b94c-141">False</span></span>                           |
| <span data-ttu-id="0b94c-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b94c-142">In Global Catalog</span></span>      | <span data-ttu-id="0b94c-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-143">True</span></span>                            |
| <span data-ttu-id="0b94c-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b94c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b94c-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b94c-145">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b94c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b94c-146">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b94c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b94c-147">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b94c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b94c-148">Search-Flags</span></span>           | <span data-ttu-id="0b94c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b94c-149">0x00000000</span></span>                      |
| <span data-ttu-id="0b94c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b94c-150">System-Flags</span></span>           | <span data-ttu-id="0b94c-151">0x00000012</span><span class="sxs-lookup"><span data-stu-id="0b94c-151">0x00000012</span></span>                      |
| <span data-ttu-id="0b94c-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b94c-152">Classes used in</span></span>        | [<span data-ttu-id="0b94c-153">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0b94c-153">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0b94c-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0b94c-154">Windows Server 2003</span></span>



| <span data-ttu-id="0b94c-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b94c-155">Entry</span></span> | <span data-ttu-id="0b94c-156">Wert</span><span class="sxs-lookup"><span data-stu-id="0b94c-156">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b94c-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b94c-157">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0b94c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b94c-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0b94c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b94c-159">System-Only</span></span>            | <span data-ttu-id="0b94c-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-160">True</span></span>                            |
| <span data-ttu-id="0b94c-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b94c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="0b94c-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-162">True</span></span>                            |
| <span data-ttu-id="0b94c-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b94c-163">Is Indexed</span></span>             | <span data-ttu-id="0b94c-164">False</span><span class="sxs-lookup"><span data-stu-id="0b94c-164">False</span></span>                           |
| <span data-ttu-id="0b94c-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b94c-165">In Global Catalog</span></span>      | <span data-ttu-id="0b94c-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-166">True</span></span>                            |
| <span data-ttu-id="0b94c-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b94c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b94c-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b94c-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b94c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b94c-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b94c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b94c-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b94c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b94c-171">Search-Flags</span></span>           | <span data-ttu-id="0b94c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b94c-172">0x00000000</span></span>                      |
| <span data-ttu-id="0b94c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b94c-173">System-Flags</span></span>           | <span data-ttu-id="0b94c-174">0x00000012</span><span class="sxs-lookup"><span data-stu-id="0b94c-174">0x00000012</span></span>                      |
| <span data-ttu-id="0b94c-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b94c-175">Classes used in</span></span>        | [<span data-ttu-id="0b94c-176">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0b94c-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0b94c-177">Adam</span><span class="sxs-lookup"><span data-stu-id="0b94c-177">ADAM</span></span>



| <span data-ttu-id="0b94c-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b94c-178">Entry</span></span> | <span data-ttu-id="0b94c-179">Wert</span><span class="sxs-lookup"><span data-stu-id="0b94c-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b94c-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b94c-180">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0b94c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b94c-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0b94c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b94c-182">System-Only</span></span>            | <span data-ttu-id="0b94c-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-183">True</span></span>                            |
| <span data-ttu-id="0b94c-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b94c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="0b94c-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-185">True</span></span>                            |
| <span data-ttu-id="0b94c-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b94c-186">Is Indexed</span></span>             | <span data-ttu-id="0b94c-187">False</span><span class="sxs-lookup"><span data-stu-id="0b94c-187">False</span></span>                           |
| <span data-ttu-id="0b94c-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b94c-188">In Global Catalog</span></span>      | <span data-ttu-id="0b94c-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-189">True</span></span>                            |
| <span data-ttu-id="0b94c-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b94c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b94c-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b94c-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b94c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b94c-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b94c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b94c-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b94c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b94c-194">Search-Flags</span></span>           | <span data-ttu-id="0b94c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b94c-195">0x00000000</span></span>                      |
| <span data-ttu-id="0b94c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b94c-196">System-Flags</span></span>           | <span data-ttu-id="0b94c-197">0x00000012</span><span class="sxs-lookup"><span data-stu-id="0b94c-197">0x00000012</span></span>                      |
| <span data-ttu-id="0b94c-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b94c-198">Classes used in</span></span>        | [<span data-ttu-id="0b94c-199">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0b94c-199">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0b94c-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0b94c-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0b94c-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b94c-201">Entry</span></span> | <span data-ttu-id="0b94c-202">Wert</span><span class="sxs-lookup"><span data-stu-id="0b94c-202">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b94c-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b94c-203">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0b94c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b94c-204">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0b94c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b94c-205">System-Only</span></span>            | <span data-ttu-id="0b94c-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-206">True</span></span>                            |
| <span data-ttu-id="0b94c-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b94c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="0b94c-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-208">True</span></span>                            |
| <span data-ttu-id="0b94c-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b94c-209">Is Indexed</span></span>             | <span data-ttu-id="0b94c-210">False</span><span class="sxs-lookup"><span data-stu-id="0b94c-210">False</span></span>                           |
| <span data-ttu-id="0b94c-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b94c-211">In Global Catalog</span></span>      | <span data-ttu-id="0b94c-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-212">True</span></span>                            |
| <span data-ttu-id="0b94c-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b94c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b94c-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b94c-214">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b94c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b94c-215">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b94c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b94c-216">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b94c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b94c-217">Search-Flags</span></span>           | <span data-ttu-id="0b94c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b94c-218">0x00000000</span></span>                      |
| <span data-ttu-id="0b94c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b94c-219">System-Flags</span></span>           | <span data-ttu-id="0b94c-220">0x00000012</span><span class="sxs-lookup"><span data-stu-id="0b94c-220">0x00000012</span></span>                      |
| <span data-ttu-id="0b94c-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b94c-221">Classes used in</span></span>        | [<span data-ttu-id="0b94c-222">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0b94c-222">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0b94c-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b94c-223">Windows Server 2008</span></span>



| <span data-ttu-id="0b94c-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b94c-224">Entry</span></span> | <span data-ttu-id="0b94c-225">Wert</span><span class="sxs-lookup"><span data-stu-id="0b94c-225">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b94c-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b94c-226">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0b94c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b94c-227">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0b94c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b94c-228">System-Only</span></span>            | <span data-ttu-id="0b94c-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-229">True</span></span>                            |
| <span data-ttu-id="0b94c-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b94c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="0b94c-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-231">True</span></span>                            |
| <span data-ttu-id="0b94c-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b94c-232">Is Indexed</span></span>             | <span data-ttu-id="0b94c-233">False</span><span class="sxs-lookup"><span data-stu-id="0b94c-233">False</span></span>                           |
| <span data-ttu-id="0b94c-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b94c-234">In Global Catalog</span></span>      | <span data-ttu-id="0b94c-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-235">True</span></span>                            |
| <span data-ttu-id="0b94c-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b94c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b94c-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b94c-237">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b94c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b94c-238">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b94c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b94c-239">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b94c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b94c-240">Search-Flags</span></span>           | <span data-ttu-id="0b94c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b94c-241">0x00000000</span></span>                      |
| <span data-ttu-id="0b94c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b94c-242">System-Flags</span></span>           | <span data-ttu-id="0b94c-243">0x00000012</span><span class="sxs-lookup"><span data-stu-id="0b94c-243">0x00000012</span></span>                      |
| <span data-ttu-id="0b94c-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b94c-244">Classes used in</span></span>        | [<span data-ttu-id="0b94c-245">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0b94c-245">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0b94c-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0b94c-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0b94c-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b94c-247">Entry</span></span> | <span data-ttu-id="0b94c-248">Wert</span><span class="sxs-lookup"><span data-stu-id="0b94c-248">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b94c-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b94c-249">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0b94c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b94c-250">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0b94c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b94c-251">System-Only</span></span>            | <span data-ttu-id="0b94c-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-252">True</span></span>                            |
| <span data-ttu-id="0b94c-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b94c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="0b94c-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-254">True</span></span>                            |
| <span data-ttu-id="0b94c-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b94c-255">Is Indexed</span></span>             | <span data-ttu-id="0b94c-256">False</span><span class="sxs-lookup"><span data-stu-id="0b94c-256">False</span></span>                           |
| <span data-ttu-id="0b94c-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b94c-257">In Global Catalog</span></span>      | <span data-ttu-id="0b94c-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-258">True</span></span>                            |
| <span data-ttu-id="0b94c-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b94c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b94c-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b94c-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b94c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b94c-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b94c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b94c-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b94c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b94c-263">Search-Flags</span></span>           | <span data-ttu-id="0b94c-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b94c-264">0x00000000</span></span>                      |
| <span data-ttu-id="0b94c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b94c-265">System-Flags</span></span>           | <span data-ttu-id="0b94c-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="0b94c-266">0x00000012</span></span>                      |
| <span data-ttu-id="0b94c-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b94c-267">Classes used in</span></span>        | [<span data-ttu-id="0b94c-268">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0b94c-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0b94c-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0b94c-269">Windows Server 2012</span></span>



| <span data-ttu-id="0b94c-270">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b94c-270">Entry</span></span> | <span data-ttu-id="0b94c-271">Wert</span><span class="sxs-lookup"><span data-stu-id="0b94c-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b94c-272">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0b94c-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0b94c-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b94c-273">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0b94c-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b94c-274">System-Only</span></span>            | <span data-ttu-id="0b94c-275">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-275">True</span></span>                            |
| <span data-ttu-id="0b94c-276">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0b94c-276">Is-Single-Valued</span></span>       | <span data-ttu-id="0b94c-277">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-277">True</span></span>                            |
| <span data-ttu-id="0b94c-278">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0b94c-278">Is Indexed</span></span>             | <span data-ttu-id="0b94c-279">False</span><span class="sxs-lookup"><span data-stu-id="0b94c-279">False</span></span>                           |
| <span data-ttu-id="0b94c-280">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0b94c-280">In Global Catalog</span></span>      | <span data-ttu-id="0b94c-281">Richtig</span><span class="sxs-lookup"><span data-stu-id="0b94c-281">True</span></span>                            |
| <span data-ttu-id="0b94c-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0b94c-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b94c-283">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0b94c-283">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b94c-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b94c-284">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b94c-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b94c-285">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b94c-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b94c-286">Search-Flags</span></span>           | <span data-ttu-id="0b94c-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b94c-287">0x00000000</span></span>                      |
| <span data-ttu-id="0b94c-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b94c-288">System-Flags</span></span>           | <span data-ttu-id="0b94c-289">0x00000012</span><span class="sxs-lookup"><span data-stu-id="0b94c-289">0x00000012</span></span>                      |
| <span data-ttu-id="0b94c-290">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0b94c-290">Classes used in</span></span>        | [<span data-ttu-id="0b94c-291">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0b94c-291">**Top**</span></span>](c-top.md)<br/> |



 

 





