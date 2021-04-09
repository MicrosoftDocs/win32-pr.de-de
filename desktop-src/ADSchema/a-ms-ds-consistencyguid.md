---
title: MS-DS-Konsistenz-GUID-Attribut
description: Dieses Attribut wird verwendet, um die Konsistenz zwischen dem Verzeichnis und einem anderen Objekt, einer Datenbank oder einer Anwendung durch Vergleichen von GUIDs zu überprüfen.
ms.assetid: 1372f46a-5569-4b06-9803-7d3862cdb745
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-DS-Konsistenz-GUID-Attributs
- AD-Schema für ms-DS-consistencyguid "-Attribut
topic_type:
- apiref
api_name:
- MS-DS-Consistency-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdbea1e9fba4ac28f968fdd61a054f55fe47deb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859713"
---
# <a name="ms-ds-consistency-guid-attribute"></a><span data-ttu-id="39a64-105">MS-DS-Konsistenz-GUID-Attribut</span><span class="sxs-lookup"><span data-stu-id="39a64-105">MS-DS-Consistency-Guid attribute</span></span>

<span data-ttu-id="39a64-106">Dieses Attribut wird verwendet, um die Konsistenz zwischen dem Verzeichnis und einem anderen Objekt, einer Datenbank oder einer Anwendung durch Vergleichen von GUIDs zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="39a64-106">This attribute is used to check consistency between the directory and another object, database, or application, by comparing GUIDs.</span></span>



| <span data-ttu-id="39a64-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39a64-107">Entry</span></span> | <span data-ttu-id="39a64-108">Wert</span><span class="sxs-lookup"><span data-stu-id="39a64-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="39a64-109">CN</span><span class="sxs-lookup"><span data-stu-id="39a64-109">CN</span></span>                | <span data-ttu-id="39a64-110">MS-DS-Consistency-Guid</span><span class="sxs-lookup"><span data-stu-id="39a64-110">MS-DS-Consistency-Guid</span></span>                                |
| <span data-ttu-id="39a64-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="39a64-111">Ldap-Display-Name</span></span> | <span data-ttu-id="39a64-112">mS-DS-consistencyguid "</span><span class="sxs-lookup"><span data-stu-id="39a64-112">mS-DS-ConsistencyGuid</span></span>                                 |
| <span data-ttu-id="39a64-113">Size</span><span class="sxs-lookup"><span data-stu-id="39a64-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="39a64-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="39a64-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="39a64-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="39a64-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="39a64-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="39a64-116">Attribute-Id</span></span>      | <span data-ttu-id="39a64-117">1.2.840.113556.1.4.1360</span><span class="sxs-lookup"><span data-stu-id="39a64-117">1.2.840.113556.1.4.1360</span></span>                               |
| <span data-ttu-id="39a64-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="39a64-118">System-Id-Guid</span></span>    | <span data-ttu-id="39a64-119">23773dc2-b63a-11d2-90e1-00c04f d91ab1</span><span class="sxs-lookup"><span data-stu-id="39a64-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="39a64-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="39a64-120">Syntax</span></span>            | [<span data-ttu-id="39a64-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="39a64-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="39a64-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="39a64-122">Implementations</span></span>

-   [<span data-ttu-id="39a64-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="39a64-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="39a64-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="39a64-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="39a64-125">**Adam**</span><span class="sxs-lookup"><span data-stu-id="39a64-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="39a64-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="39a64-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="39a64-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="39a64-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="39a64-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="39a64-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="39a64-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="39a64-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="39a64-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="39a64-130">Windows 2000 Server</span></span>



| <span data-ttu-id="39a64-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39a64-131">Entry</span></span> | <span data-ttu-id="39a64-132">Wert</span><span class="sxs-lookup"><span data-stu-id="39a64-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="39a64-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39a64-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="39a64-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39a64-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="39a64-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="39a64-135">System-Only</span></span>            | <span data-ttu-id="39a64-136">False</span><span class="sxs-lookup"><span data-stu-id="39a64-136">False</span></span>                           |
| <span data-ttu-id="39a64-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39a64-137">Is-Single-Valued</span></span>       | <span data-ttu-id="39a64-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="39a64-138">True</span></span>                            |
| <span data-ttu-id="39a64-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39a64-139">Is Indexed</span></span>             | <span data-ttu-id="39a64-140">False</span><span class="sxs-lookup"><span data-stu-id="39a64-140">False</span></span>                           |
| <span data-ttu-id="39a64-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39a64-141">In Global Catalog</span></span>      | <span data-ttu-id="39a64-142">False</span><span class="sxs-lookup"><span data-stu-id="39a64-142">False</span></span>                           |
| <span data-ttu-id="39a64-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39a64-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="39a64-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39a64-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="39a64-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39a64-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="39a64-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39a64-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="39a64-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39a64-147">Search-Flags</span></span>           | <span data-ttu-id="39a64-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39a64-148">0x00000000</span></span>                      |
| <span data-ttu-id="39a64-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39a64-149">System-Flags</span></span>           | <span data-ttu-id="39a64-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39a64-150">0x00000010</span></span>                      |
| <span data-ttu-id="39a64-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39a64-151">Classes used in</span></span>        | [<span data-ttu-id="39a64-152">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="39a64-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="39a64-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="39a64-153">Windows Server 2003</span></span>



| <span data-ttu-id="39a64-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39a64-154">Entry</span></span> | <span data-ttu-id="39a64-155">Wert</span><span class="sxs-lookup"><span data-stu-id="39a64-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="39a64-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39a64-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="39a64-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39a64-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="39a64-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="39a64-158">System-Only</span></span>            | <span data-ttu-id="39a64-159">False</span><span class="sxs-lookup"><span data-stu-id="39a64-159">False</span></span>                           |
| <span data-ttu-id="39a64-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39a64-160">Is-Single-Valued</span></span>       | <span data-ttu-id="39a64-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="39a64-161">True</span></span>                            |
| <span data-ttu-id="39a64-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39a64-162">Is Indexed</span></span>             | <span data-ttu-id="39a64-163">False</span><span class="sxs-lookup"><span data-stu-id="39a64-163">False</span></span>                           |
| <span data-ttu-id="39a64-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39a64-164">In Global Catalog</span></span>      | <span data-ttu-id="39a64-165">False</span><span class="sxs-lookup"><span data-stu-id="39a64-165">False</span></span>                           |
| <span data-ttu-id="39a64-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39a64-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="39a64-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39a64-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="39a64-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39a64-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="39a64-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39a64-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="39a64-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39a64-170">Search-Flags</span></span>           | <span data-ttu-id="39a64-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39a64-171">0x00000000</span></span>                      |
| <span data-ttu-id="39a64-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39a64-172">System-Flags</span></span>           | <span data-ttu-id="39a64-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39a64-173">0x00000010</span></span>                      |
| <span data-ttu-id="39a64-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39a64-174">Classes used in</span></span>        | [<span data-ttu-id="39a64-175">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="39a64-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="39a64-176">Adam</span><span class="sxs-lookup"><span data-stu-id="39a64-176">ADAM</span></span>



| <span data-ttu-id="39a64-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39a64-177">Entry</span></span> | <span data-ttu-id="39a64-178">Wert</span><span class="sxs-lookup"><span data-stu-id="39a64-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="39a64-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39a64-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="39a64-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39a64-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="39a64-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="39a64-181">System-Only</span></span>            | <span data-ttu-id="39a64-182">False</span><span class="sxs-lookup"><span data-stu-id="39a64-182">False</span></span>                           |
| <span data-ttu-id="39a64-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39a64-183">Is-Single-Valued</span></span>       | <span data-ttu-id="39a64-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="39a64-184">True</span></span>                            |
| <span data-ttu-id="39a64-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39a64-185">Is Indexed</span></span>             | <span data-ttu-id="39a64-186">False</span><span class="sxs-lookup"><span data-stu-id="39a64-186">False</span></span>                           |
| <span data-ttu-id="39a64-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39a64-187">In Global Catalog</span></span>      | <span data-ttu-id="39a64-188">False</span><span class="sxs-lookup"><span data-stu-id="39a64-188">False</span></span>                           |
| <span data-ttu-id="39a64-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39a64-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="39a64-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39a64-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="39a64-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39a64-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="39a64-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39a64-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="39a64-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39a64-193">Search-Flags</span></span>           | <span data-ttu-id="39a64-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39a64-194">0x00000000</span></span>                      |
| <span data-ttu-id="39a64-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39a64-195">System-Flags</span></span>           | <span data-ttu-id="39a64-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39a64-196">0x00000010</span></span>                      |
| <span data-ttu-id="39a64-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39a64-197">Classes used in</span></span>        | [<span data-ttu-id="39a64-198">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="39a64-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="39a64-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="39a64-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="39a64-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39a64-200">Entry</span></span> | <span data-ttu-id="39a64-201">Wert</span><span class="sxs-lookup"><span data-stu-id="39a64-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="39a64-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39a64-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="39a64-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39a64-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="39a64-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="39a64-204">System-Only</span></span>            | <span data-ttu-id="39a64-205">False</span><span class="sxs-lookup"><span data-stu-id="39a64-205">False</span></span>                           |
| <span data-ttu-id="39a64-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39a64-206">Is-Single-Valued</span></span>       | <span data-ttu-id="39a64-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="39a64-207">True</span></span>                            |
| <span data-ttu-id="39a64-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39a64-208">Is Indexed</span></span>             | <span data-ttu-id="39a64-209">False</span><span class="sxs-lookup"><span data-stu-id="39a64-209">False</span></span>                           |
| <span data-ttu-id="39a64-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39a64-210">In Global Catalog</span></span>      | <span data-ttu-id="39a64-211">False</span><span class="sxs-lookup"><span data-stu-id="39a64-211">False</span></span>                           |
| <span data-ttu-id="39a64-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39a64-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="39a64-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39a64-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="39a64-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39a64-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="39a64-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39a64-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="39a64-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39a64-216">Search-Flags</span></span>           | <span data-ttu-id="39a64-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39a64-217">0x00000000</span></span>                      |
| <span data-ttu-id="39a64-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39a64-218">System-Flags</span></span>           | <span data-ttu-id="39a64-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39a64-219">0x00000010</span></span>                      |
| <span data-ttu-id="39a64-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39a64-220">Classes used in</span></span>        | [<span data-ttu-id="39a64-221">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="39a64-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="39a64-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39a64-222">Windows Server 2008</span></span>



| <span data-ttu-id="39a64-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39a64-223">Entry</span></span> | <span data-ttu-id="39a64-224">Wert</span><span class="sxs-lookup"><span data-stu-id="39a64-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="39a64-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39a64-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="39a64-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39a64-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="39a64-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="39a64-227">System-Only</span></span>            | <span data-ttu-id="39a64-228">False</span><span class="sxs-lookup"><span data-stu-id="39a64-228">False</span></span>                           |
| <span data-ttu-id="39a64-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39a64-229">Is-Single-Valued</span></span>       | <span data-ttu-id="39a64-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="39a64-230">True</span></span>                            |
| <span data-ttu-id="39a64-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39a64-231">Is Indexed</span></span>             | <span data-ttu-id="39a64-232">False</span><span class="sxs-lookup"><span data-stu-id="39a64-232">False</span></span>                           |
| <span data-ttu-id="39a64-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39a64-233">In Global Catalog</span></span>      | <span data-ttu-id="39a64-234">False</span><span class="sxs-lookup"><span data-stu-id="39a64-234">False</span></span>                           |
| <span data-ttu-id="39a64-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39a64-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="39a64-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39a64-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="39a64-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39a64-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="39a64-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39a64-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="39a64-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39a64-239">Search-Flags</span></span>           | <span data-ttu-id="39a64-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39a64-240">0x00000000</span></span>                      |
| <span data-ttu-id="39a64-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39a64-241">System-Flags</span></span>           | <span data-ttu-id="39a64-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39a64-242">0x00000010</span></span>                      |
| <span data-ttu-id="39a64-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39a64-243">Classes used in</span></span>        | [<span data-ttu-id="39a64-244">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="39a64-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="39a64-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39a64-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="39a64-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39a64-246">Entry</span></span> | <span data-ttu-id="39a64-247">Wert</span><span class="sxs-lookup"><span data-stu-id="39a64-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="39a64-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39a64-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="39a64-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39a64-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="39a64-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="39a64-250">System-Only</span></span>            | <span data-ttu-id="39a64-251">False</span><span class="sxs-lookup"><span data-stu-id="39a64-251">False</span></span>                           |
| <span data-ttu-id="39a64-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39a64-252">Is-Single-Valued</span></span>       | <span data-ttu-id="39a64-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="39a64-253">True</span></span>                            |
| <span data-ttu-id="39a64-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39a64-254">Is Indexed</span></span>             | <span data-ttu-id="39a64-255">False</span><span class="sxs-lookup"><span data-stu-id="39a64-255">False</span></span>                           |
| <span data-ttu-id="39a64-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39a64-256">In Global Catalog</span></span>      | <span data-ttu-id="39a64-257">False</span><span class="sxs-lookup"><span data-stu-id="39a64-257">False</span></span>                           |
| <span data-ttu-id="39a64-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39a64-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="39a64-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39a64-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="39a64-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39a64-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="39a64-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39a64-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="39a64-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39a64-262">Search-Flags</span></span>           | <span data-ttu-id="39a64-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39a64-263">0x00000000</span></span>                      |
| <span data-ttu-id="39a64-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39a64-264">System-Flags</span></span>           | <span data-ttu-id="39a64-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39a64-265">0x00000010</span></span>                      |
| <span data-ttu-id="39a64-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39a64-266">Classes used in</span></span>        | [<span data-ttu-id="39a64-267">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="39a64-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="39a64-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="39a64-268">Windows Server 2012</span></span>



| <span data-ttu-id="39a64-269">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39a64-269">Entry</span></span> | <span data-ttu-id="39a64-270">Wert</span><span class="sxs-lookup"><span data-stu-id="39a64-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="39a64-271">Link-ID</span><span class="sxs-lookup"><span data-stu-id="39a64-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="39a64-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39a64-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="39a64-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="39a64-273">System-Only</span></span>            | <span data-ttu-id="39a64-274">False</span><span class="sxs-lookup"><span data-stu-id="39a64-274">False</span></span>                           |
| <span data-ttu-id="39a64-275">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="39a64-275">Is-Single-Valued</span></span>       | <span data-ttu-id="39a64-276">Richtig</span><span class="sxs-lookup"><span data-stu-id="39a64-276">True</span></span>                            |
| <span data-ttu-id="39a64-277">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="39a64-277">Is Indexed</span></span>             | <span data-ttu-id="39a64-278">False</span><span class="sxs-lookup"><span data-stu-id="39a64-278">False</span></span>                           |
| <span data-ttu-id="39a64-279">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="39a64-279">In Global Catalog</span></span>      | <span data-ttu-id="39a64-280">False</span><span class="sxs-lookup"><span data-stu-id="39a64-280">False</span></span>                           |
| <span data-ttu-id="39a64-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39a64-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="39a64-282">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="39a64-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="39a64-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39a64-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="39a64-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39a64-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="39a64-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39a64-285">Search-Flags</span></span>           | <span data-ttu-id="39a64-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39a64-286">0x00000000</span></span>                      |
| <span data-ttu-id="39a64-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39a64-287">System-Flags</span></span>           | <span data-ttu-id="39a64-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39a64-288">0x00000010</span></span>                      |
| <span data-ttu-id="39a64-289">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="39a64-289">Classes used in</span></span>        | [<span data-ttu-id="39a64-290">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="39a64-290">**Top**</span></span>](c-top.md)<br/> |



 

 





