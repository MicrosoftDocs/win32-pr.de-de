---
title: Anderes-Well-Known-Objects-Attribut
description: Enthält eine Liste der Container nach GUID und Distinguished Name. Dies ermöglicht das Abrufen eines Objekts, nachdem es mit nur der GUID und dem Domänen Namen verschoben wurde. Wenn das Objekt verschoben wird, aktualisiert das System automatisch den Distinguished Name.
ms.assetid: 2f33c4ac-235c-47a1-9340-5b90f7edb73b
ms.tgt_platform: multiple
keywords:
- AD-Schema für ein anderes-Well-Known-Objects-Attribut
- OtherWellKnownObjects-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Other-Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d38b4f4b86f90368859f9fb966031f539f0399f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480271"
---
# <a name="other-well-known-objects-attribute"></a><span data-ttu-id="d3263-107">Anderes-Well-Known-Objects-Attribut</span><span class="sxs-lookup"><span data-stu-id="d3263-107">Other-Well-Known-Objects attribute</span></span>

<span data-ttu-id="d3263-108">Enthält eine Liste der Container nach GUID und Distinguished Name.</span><span class="sxs-lookup"><span data-stu-id="d3263-108">Contains a list of containers by GUID and Distinguished Name.</span></span> <span data-ttu-id="d3263-109">Dies ermöglicht das Abrufen eines Objekts, nachdem es mit nur der GUID und dem Domänen Namen verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="d3263-109">This permits retrieving an object after it has been moved by using just the GUID and the domain name.</span></span> <span data-ttu-id="d3263-110">Wenn das Objekt verschoben wird, aktualisiert das System automatisch den Distinguished Name.</span><span class="sxs-lookup"><span data-stu-id="d3263-110">Whenever the object is moved, the system automatically updates the Distinguished Name.</span></span>



| <span data-ttu-id="d3263-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3263-111">Entry</span></span> | <span data-ttu-id="d3263-112">Wert</span><span class="sxs-lookup"><span data-stu-id="d3263-112">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3263-113">CN</span><span class="sxs-lookup"><span data-stu-id="d3263-113">CN</span></span>                | <span data-ttu-id="d3263-114">Andere-bekannte Objekte</span><span class="sxs-lookup"><span data-stu-id="d3263-114">Other-Well-Known-Objects</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="d3263-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d3263-115">Ldap-Display-Name</span></span> | <span data-ttu-id="d3263-116">otherWellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="d3263-116">otherWellKnownObjects</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="d3263-117">Size</span><span class="sxs-lookup"><span data-stu-id="d3263-117">Size</span></span>              | <span data-ttu-id="d3263-118">Beispiel für das Abrufen des Benutzer Containers in der Microsoft-Domäne: LDAP://(wkguid = a9d1ca15768811d1aded00c04fd8d5cd, DC = Microsoft, DC = com).</span><span class="sxs-lookup"><span data-stu-id="d3263-118">Sample for retrieving the Users container in the microsoft domain: LDAP://(WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=microsoft,dc=com).</span></span> <span data-ttu-id="d3263-119">Hinweis: durch Klammern ersetzte spitzen Klammern, um XML-Konflikte zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="d3263-119">NOTE: Angle brackets replaced by parentheses to avoid XML conflicts.</span></span> |
| <span data-ttu-id="d3263-120">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d3263-120">Update Privilege</span></span>  | <span data-ttu-id="d3263-121">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="d3263-121">Schema administrator</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="d3263-122">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="d3263-122">Update Frequency</span></span>  | <span data-ttu-id="d3263-123">Immer dann, wenn das-Objekt verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="d3263-123">Whenever the object is moved.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="d3263-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d3263-124">Attribute-Id</span></span>      | <span data-ttu-id="d3263-125">1.2.840.113556.1.4.1359</span><span class="sxs-lookup"><span data-stu-id="d3263-125">1.2.840.113556.1.4.1359</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="d3263-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d3263-126">System-Id-Guid</span></span>    | <span data-ttu-id="d3263-127">1ea64e5d-ac0f -11d2-90df-00c04f d91ab1</span><span class="sxs-lookup"><span data-stu-id="d3263-127">1ea64e5d-ac0f-11d2-90df-00c04fd91ab1</span></span>                                                                                                                                                                          |
| <span data-ttu-id="d3263-128">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3263-128">Syntax</span></span>            | [<span data-ttu-id="d3263-129">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="d3263-129">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                                                                                               |



## <a name="implementations"></a><span data-ttu-id="d3263-130">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="d3263-130">Implementations</span></span>

-   [<span data-ttu-id="d3263-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d3263-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d3263-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d3263-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d3263-133">**Adam**</span><span class="sxs-lookup"><span data-stu-id="d3263-133">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d3263-134">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d3263-134">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d3263-135">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d3263-135">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d3263-136">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d3263-136">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d3263-137">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d3263-137">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d3263-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d3263-138">Windows 2000 Server</span></span>



| <span data-ttu-id="d3263-139">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3263-139">Entry</span></span> | <span data-ttu-id="d3263-140">Wert</span><span class="sxs-lookup"><span data-stu-id="d3263-140">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d3263-141">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3263-141">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d3263-142">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3263-142">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d3263-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3263-143">System-Only</span></span>            | <span data-ttu-id="d3263-144">False</span><span class="sxs-lookup"><span data-stu-id="d3263-144">False</span></span>                           |
| <span data-ttu-id="d3263-145">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3263-145">Is-Single-Valued</span></span>       | <span data-ttu-id="d3263-146">False</span><span class="sxs-lookup"><span data-stu-id="d3263-146">False</span></span>                           |
| <span data-ttu-id="d3263-147">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3263-147">Is Indexed</span></span>             | <span data-ttu-id="d3263-148">False</span><span class="sxs-lookup"><span data-stu-id="d3263-148">False</span></span>                           |
| <span data-ttu-id="d3263-149">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3263-149">In Global Catalog</span></span>      | <span data-ttu-id="d3263-150">False</span><span class="sxs-lookup"><span data-stu-id="d3263-150">False</span></span>                           |
| <span data-ttu-id="d3263-151">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3263-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3263-152">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3263-152">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d3263-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3263-153">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d3263-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3263-154">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d3263-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3263-155">Search-Flags</span></span>           | <span data-ttu-id="d3263-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3263-156">0x00000000</span></span>                      |
| <span data-ttu-id="d3263-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3263-157">System-Flags</span></span>           | <span data-ttu-id="d3263-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3263-158">0x00000010</span></span>                      |
| <span data-ttu-id="d3263-159">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3263-159">Classes used in</span></span>        | [<span data-ttu-id="d3263-160">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="d3263-160">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d3263-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d3263-161">Windows Server 2003</span></span>



| <span data-ttu-id="d3263-162">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3263-162">Entry</span></span> | <span data-ttu-id="d3263-163">Wert</span><span class="sxs-lookup"><span data-stu-id="d3263-163">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d3263-164">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3263-164">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d3263-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3263-165">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d3263-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3263-166">System-Only</span></span>            | <span data-ttu-id="d3263-167">False</span><span class="sxs-lookup"><span data-stu-id="d3263-167">False</span></span>                           |
| <span data-ttu-id="d3263-168">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3263-168">Is-Single-Valued</span></span>       | <span data-ttu-id="d3263-169">False</span><span class="sxs-lookup"><span data-stu-id="d3263-169">False</span></span>                           |
| <span data-ttu-id="d3263-170">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3263-170">Is Indexed</span></span>             | <span data-ttu-id="d3263-171">False</span><span class="sxs-lookup"><span data-stu-id="d3263-171">False</span></span>                           |
| <span data-ttu-id="d3263-172">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3263-172">In Global Catalog</span></span>      | <span data-ttu-id="d3263-173">False</span><span class="sxs-lookup"><span data-stu-id="d3263-173">False</span></span>                           |
| <span data-ttu-id="d3263-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3263-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3263-175">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3263-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d3263-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3263-176">Range-Lower</span></span>            | <span data-ttu-id="d3263-177">16</span><span class="sxs-lookup"><span data-stu-id="d3263-177">16</span></span>                              |
| <span data-ttu-id="d3263-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3263-178">Range-Upper</span></span>            | <span data-ttu-id="d3263-179">16</span><span class="sxs-lookup"><span data-stu-id="d3263-179">16</span></span>                              |
| <span data-ttu-id="d3263-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3263-180">Search-Flags</span></span>           | <span data-ttu-id="d3263-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3263-181">0x00000000</span></span>                      |
| <span data-ttu-id="d3263-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3263-182">System-Flags</span></span>           | <span data-ttu-id="d3263-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3263-183">0x00000010</span></span>                      |
| <span data-ttu-id="d3263-184">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3263-184">Classes used in</span></span>        | [<span data-ttu-id="d3263-185">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="d3263-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d3263-186">Adam</span><span class="sxs-lookup"><span data-stu-id="d3263-186">ADAM</span></span>



| <span data-ttu-id="d3263-187">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3263-187">Entry</span></span> | <span data-ttu-id="d3263-188">Wert</span><span class="sxs-lookup"><span data-stu-id="d3263-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d3263-189">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3263-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d3263-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3263-190">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d3263-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3263-191">System-Only</span></span>            | <span data-ttu-id="d3263-192">False</span><span class="sxs-lookup"><span data-stu-id="d3263-192">False</span></span>                           |
| <span data-ttu-id="d3263-193">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3263-193">Is-Single-Valued</span></span>       | <span data-ttu-id="d3263-194">False</span><span class="sxs-lookup"><span data-stu-id="d3263-194">False</span></span>                           |
| <span data-ttu-id="d3263-195">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3263-195">Is Indexed</span></span>             | <span data-ttu-id="d3263-196">False</span><span class="sxs-lookup"><span data-stu-id="d3263-196">False</span></span>                           |
| <span data-ttu-id="d3263-197">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3263-197">In Global Catalog</span></span>      | <span data-ttu-id="d3263-198">False</span><span class="sxs-lookup"><span data-stu-id="d3263-198">False</span></span>                           |
| <span data-ttu-id="d3263-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3263-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3263-200">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3263-200">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d3263-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3263-201">Range-Lower</span></span>            | <span data-ttu-id="d3263-202">16</span><span class="sxs-lookup"><span data-stu-id="d3263-202">16</span></span>                              |
| <span data-ttu-id="d3263-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3263-203">Range-Upper</span></span>            | <span data-ttu-id="d3263-204">16</span><span class="sxs-lookup"><span data-stu-id="d3263-204">16</span></span>                              |
| <span data-ttu-id="d3263-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3263-205">Search-Flags</span></span>           | <span data-ttu-id="d3263-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3263-206">0x00000000</span></span>                      |
| <span data-ttu-id="d3263-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3263-207">System-Flags</span></span>           | <span data-ttu-id="d3263-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3263-208">0x00000010</span></span>                      |
| <span data-ttu-id="d3263-209">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3263-209">Classes used in</span></span>        | [<span data-ttu-id="d3263-210">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="d3263-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d3263-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d3263-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d3263-212">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3263-212">Entry</span></span> | <span data-ttu-id="d3263-213">Wert</span><span class="sxs-lookup"><span data-stu-id="d3263-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d3263-214">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3263-214">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d3263-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3263-215">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d3263-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3263-216">System-Only</span></span>            | <span data-ttu-id="d3263-217">False</span><span class="sxs-lookup"><span data-stu-id="d3263-217">False</span></span>                           |
| <span data-ttu-id="d3263-218">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3263-218">Is-Single-Valued</span></span>       | <span data-ttu-id="d3263-219">False</span><span class="sxs-lookup"><span data-stu-id="d3263-219">False</span></span>                           |
| <span data-ttu-id="d3263-220">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3263-220">Is Indexed</span></span>             | <span data-ttu-id="d3263-221">False</span><span class="sxs-lookup"><span data-stu-id="d3263-221">False</span></span>                           |
| <span data-ttu-id="d3263-222">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3263-222">In Global Catalog</span></span>      | <span data-ttu-id="d3263-223">False</span><span class="sxs-lookup"><span data-stu-id="d3263-223">False</span></span>                           |
| <span data-ttu-id="d3263-224">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3263-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3263-225">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3263-225">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d3263-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3263-226">Range-Lower</span></span>            | <span data-ttu-id="d3263-227">16</span><span class="sxs-lookup"><span data-stu-id="d3263-227">16</span></span>                              |
| <span data-ttu-id="d3263-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3263-228">Range-Upper</span></span>            | <span data-ttu-id="d3263-229">16</span><span class="sxs-lookup"><span data-stu-id="d3263-229">16</span></span>                              |
| <span data-ttu-id="d3263-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3263-230">Search-Flags</span></span>           | <span data-ttu-id="d3263-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3263-231">0x00000000</span></span>                      |
| <span data-ttu-id="d3263-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3263-232">System-Flags</span></span>           | <span data-ttu-id="d3263-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3263-233">0x00000010</span></span>                      |
| <span data-ttu-id="d3263-234">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3263-234">Classes used in</span></span>        | [<span data-ttu-id="d3263-235">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="d3263-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d3263-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3263-236">Windows Server 2008</span></span>



| <span data-ttu-id="d3263-237">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3263-237">Entry</span></span> | <span data-ttu-id="d3263-238">Wert</span><span class="sxs-lookup"><span data-stu-id="d3263-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d3263-239">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3263-239">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d3263-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3263-240">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d3263-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3263-241">System-Only</span></span>            | <span data-ttu-id="d3263-242">False</span><span class="sxs-lookup"><span data-stu-id="d3263-242">False</span></span>                           |
| <span data-ttu-id="d3263-243">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3263-243">Is-Single-Valued</span></span>       | <span data-ttu-id="d3263-244">False</span><span class="sxs-lookup"><span data-stu-id="d3263-244">False</span></span>                           |
| <span data-ttu-id="d3263-245">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3263-245">Is Indexed</span></span>             | <span data-ttu-id="d3263-246">False</span><span class="sxs-lookup"><span data-stu-id="d3263-246">False</span></span>                           |
| <span data-ttu-id="d3263-247">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3263-247">In Global Catalog</span></span>      | <span data-ttu-id="d3263-248">False</span><span class="sxs-lookup"><span data-stu-id="d3263-248">False</span></span>                           |
| <span data-ttu-id="d3263-249">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3263-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3263-250">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3263-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d3263-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3263-251">Range-Lower</span></span>            | <span data-ttu-id="d3263-252">16</span><span class="sxs-lookup"><span data-stu-id="d3263-252">16</span></span>                              |
| <span data-ttu-id="d3263-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3263-253">Range-Upper</span></span>            | <span data-ttu-id="d3263-254">16</span><span class="sxs-lookup"><span data-stu-id="d3263-254">16</span></span>                              |
| <span data-ttu-id="d3263-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3263-255">Search-Flags</span></span>           | <span data-ttu-id="d3263-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3263-256">0x00000000</span></span>                      |
| <span data-ttu-id="d3263-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3263-257">System-Flags</span></span>           | <span data-ttu-id="d3263-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3263-258">0x00000010</span></span>                      |
| <span data-ttu-id="d3263-259">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3263-259">Classes used in</span></span>        | [<span data-ttu-id="d3263-260">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="d3263-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d3263-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d3263-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d3263-262">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3263-262">Entry</span></span> | <span data-ttu-id="d3263-263">Wert</span><span class="sxs-lookup"><span data-stu-id="d3263-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d3263-264">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3263-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d3263-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3263-265">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d3263-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3263-266">System-Only</span></span>            | <span data-ttu-id="d3263-267">False</span><span class="sxs-lookup"><span data-stu-id="d3263-267">False</span></span>                           |
| <span data-ttu-id="d3263-268">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3263-268">Is-Single-Valued</span></span>       | <span data-ttu-id="d3263-269">False</span><span class="sxs-lookup"><span data-stu-id="d3263-269">False</span></span>                           |
| <span data-ttu-id="d3263-270">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3263-270">Is Indexed</span></span>             | <span data-ttu-id="d3263-271">False</span><span class="sxs-lookup"><span data-stu-id="d3263-271">False</span></span>                           |
| <span data-ttu-id="d3263-272">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3263-272">In Global Catalog</span></span>      | <span data-ttu-id="d3263-273">False</span><span class="sxs-lookup"><span data-stu-id="d3263-273">False</span></span>                           |
| <span data-ttu-id="d3263-274">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3263-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3263-275">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3263-275">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d3263-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3263-276">Range-Lower</span></span>            | <span data-ttu-id="d3263-277">16</span><span class="sxs-lookup"><span data-stu-id="d3263-277">16</span></span>                              |
| <span data-ttu-id="d3263-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3263-278">Range-Upper</span></span>            | <span data-ttu-id="d3263-279">16</span><span class="sxs-lookup"><span data-stu-id="d3263-279">16</span></span>                              |
| <span data-ttu-id="d3263-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3263-280">Search-Flags</span></span>           | <span data-ttu-id="d3263-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3263-281">0x00000000</span></span>                      |
| <span data-ttu-id="d3263-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3263-282">System-Flags</span></span>           | <span data-ttu-id="d3263-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3263-283">0x00000010</span></span>                      |
| <span data-ttu-id="d3263-284">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3263-284">Classes used in</span></span>        | [<span data-ttu-id="d3263-285">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="d3263-285">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d3263-286">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d3263-286">Windows Server 2012</span></span>



| <span data-ttu-id="d3263-287">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3263-287">Entry</span></span> | <span data-ttu-id="d3263-288">Wert</span><span class="sxs-lookup"><span data-stu-id="d3263-288">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d3263-289">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d3263-289">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d3263-290">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3263-290">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d3263-291">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3263-291">System-Only</span></span>            | <span data-ttu-id="d3263-292">False</span><span class="sxs-lookup"><span data-stu-id="d3263-292">False</span></span>                           |
| <span data-ttu-id="d3263-293">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d3263-293">Is-Single-Valued</span></span>       | <span data-ttu-id="d3263-294">False</span><span class="sxs-lookup"><span data-stu-id="d3263-294">False</span></span>                           |
| <span data-ttu-id="d3263-295">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d3263-295">Is Indexed</span></span>             | <span data-ttu-id="d3263-296">False</span><span class="sxs-lookup"><span data-stu-id="d3263-296">False</span></span>                           |
| <span data-ttu-id="d3263-297">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3263-297">In Global Catalog</span></span>      | <span data-ttu-id="d3263-298">False</span><span class="sxs-lookup"><span data-stu-id="d3263-298">False</span></span>                           |
| <span data-ttu-id="d3263-299">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3263-299">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3263-300">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d3263-300">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d3263-301">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3263-301">Range-Lower</span></span>            | <span data-ttu-id="d3263-302">16</span><span class="sxs-lookup"><span data-stu-id="d3263-302">16</span></span>                              |
| <span data-ttu-id="d3263-303">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3263-303">Range-Upper</span></span>            | <span data-ttu-id="d3263-304">16</span><span class="sxs-lookup"><span data-stu-id="d3263-304">16</span></span>                              |
| <span data-ttu-id="d3263-305">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3263-305">Search-Flags</span></span>           | <span data-ttu-id="d3263-306">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3263-306">0x00000000</span></span>                      |
| <span data-ttu-id="d3263-307">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3263-307">System-Flags</span></span>           | <span data-ttu-id="d3263-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3263-308">0x00000010</span></span>                      |
| <span data-ttu-id="d3263-309">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d3263-309">Classes used in</span></span>        | [<span data-ttu-id="d3263-310">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="d3263-310">**Top**</span></span>](c-top.md)<br/> |



 

 





