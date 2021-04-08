---
title: Lokalisierungs-Display-ID-Attribut
description: Wird verwendet, um in die Datei Extrts.MC zu indizieren, um den lokalisierten Display Name für die Objekte zu UI-Zwecken zu erhalten.
ms.assetid: ed99d499-0064-4832-81ad-75fb3c8c548d
ms.tgt_platform: multiple
keywords:
- "\"Localization-Display-ID\"-Attribut AD-Schema"
- "\"localizationdisplayid\"-Attribut, AD-Schema"
topic_type:
- apiref
api_name:
- Localization-Display-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4d9453b04bd5c944784b68ff5e4442f00bf65f5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744801"
---
# <a name="localization-display-id-attribute"></a><span data-ttu-id="d2f71-105">Lokalisierungs-Display-ID-Attribut</span><span class="sxs-lookup"><span data-stu-id="d2f71-105">Localization-Display-Id attribute</span></span>

<span data-ttu-id="d2f71-106">Wird verwendet, um in die Datei Extrts.MC zu indizieren, um den lokalisierten Display Name für die Objekte zu UI-Zwecken zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2f71-106">Used to index into the file Extrts.mc to get the localized displayName for the objects for UI purposes.</span></span>



| <span data-ttu-id="d2f71-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2f71-107">Entry</span></span> | <span data-ttu-id="d2f71-108">Wert</span><span class="sxs-lookup"><span data-stu-id="d2f71-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d2f71-109">CN</span><span class="sxs-lookup"><span data-stu-id="d2f71-109">CN</span></span>                | <span data-ttu-id="d2f71-110">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="d2f71-110">Localization-Display-Id</span></span>              |
| <span data-ttu-id="d2f71-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d2f71-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d2f71-112">localizationdisplayid</span><span class="sxs-lookup"><span data-stu-id="d2f71-112">localizationDisplayId</span></span>                |
| <span data-ttu-id="d2f71-113">Size</span><span class="sxs-lookup"><span data-stu-id="d2f71-113">Size</span></span>              | <span data-ttu-id="d2f71-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="d2f71-114">4 bytes</span></span>                              |
| <span data-ttu-id="d2f71-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d2f71-115">Update Privilege</span></span>  | <span data-ttu-id="d2f71-116">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="d2f71-116">Schema administrator</span></span>                 |
| <span data-ttu-id="d2f71-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="d2f71-117">Update Frequency</span></span>  | <span data-ttu-id="d2f71-118">Eine ID sollte nie geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d2f71-118">An ID should never be changed.</span></span>       |
| <span data-ttu-id="d2f71-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d2f71-119">Attribute-Id</span></span>      | <span data-ttu-id="d2f71-120">1.2.840.113556.1.4.1353</span><span class="sxs-lookup"><span data-stu-id="d2f71-120">1.2.840.113556.1.4.1353</span></span>              |
| <span data-ttu-id="d2f71-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d2f71-121">System-Id-Guid</span></span>    | <span data-ttu-id="d2f71-122">a746f0d1-78d0-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="d2f71-122">a746f0d1-78d0-11d2-9916-0000f87a57d4</span></span> |
| <span data-ttu-id="d2f71-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2f71-123">Syntax</span></span>            | [<span data-ttu-id="d2f71-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="d2f71-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="d2f71-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="d2f71-125">Implementations</span></span>

-   [<span data-ttu-id="d2f71-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d2f71-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d2f71-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d2f71-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d2f71-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="d2f71-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d2f71-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d2f71-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d2f71-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d2f71-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d2f71-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d2f71-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d2f71-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d2f71-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d2f71-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d2f71-133">Windows 2000 Server</span></span>



| <span data-ttu-id="d2f71-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2f71-134">Entry</span></span> | <span data-ttu-id="d2f71-135">Wert</span><span class="sxs-lookup"><span data-stu-id="d2f71-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d2f71-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d2f71-136">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d2f71-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f71-137">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d2f71-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f71-138">System-Only</span></span>            | <span data-ttu-id="d2f71-139">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-139">False</span></span>                                                           |
| <span data-ttu-id="d2f71-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d2f71-140">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f71-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="d2f71-141">True</span></span>                                                            |
| <span data-ttu-id="d2f71-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d2f71-142">Is Indexed</span></span>             | <span data-ttu-id="d2f71-143">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-143">False</span></span>                                                           |
| <span data-ttu-id="d2f71-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d2f71-144">In Global Catalog</span></span>      | <span data-ttu-id="d2f71-145">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-145">False</span></span>                                                           |
| <span data-ttu-id="d2f71-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d2f71-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f71-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d2f71-147">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d2f71-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f71-148">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="d2f71-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f71-149">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="d2f71-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f71-150">Search-Flags</span></span>           | <span data-ttu-id="d2f71-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f71-151">0x00000000</span></span>                                                      |
| <span data-ttu-id="d2f71-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f71-152">System-Flags</span></span>           | <span data-ttu-id="d2f71-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f71-153">0x00000010</span></span>                                                      |
| <span data-ttu-id="d2f71-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d2f71-154">Classes used in</span></span>        | [<span data-ttu-id="d2f71-155">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="d2f71-155">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d2f71-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2f71-156">Windows Server 2003</span></span>



| <span data-ttu-id="d2f71-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2f71-157">Entry</span></span> | <span data-ttu-id="d2f71-158">Wert</span><span class="sxs-lookup"><span data-stu-id="d2f71-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d2f71-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d2f71-159">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d2f71-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f71-160">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d2f71-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f71-161">System-Only</span></span>            | <span data-ttu-id="d2f71-162">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-162">False</span></span>                                                           |
| <span data-ttu-id="d2f71-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d2f71-163">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f71-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="d2f71-164">True</span></span>                                                            |
| <span data-ttu-id="d2f71-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d2f71-165">Is Indexed</span></span>             | <span data-ttu-id="d2f71-166">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-166">False</span></span>                                                           |
| <span data-ttu-id="d2f71-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d2f71-167">In Global Catalog</span></span>      | <span data-ttu-id="d2f71-168">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-168">False</span></span>                                                           |
| <span data-ttu-id="d2f71-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d2f71-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f71-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d2f71-170">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d2f71-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f71-171">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="d2f71-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f71-172">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="d2f71-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f71-173">Search-Flags</span></span>           | <span data-ttu-id="d2f71-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f71-174">0x00000000</span></span>                                                      |
| <span data-ttu-id="d2f71-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f71-175">System-Flags</span></span>           | <span data-ttu-id="d2f71-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f71-176">0x00000010</span></span>                                                      |
| <span data-ttu-id="d2f71-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d2f71-177">Classes used in</span></span>        | [<span data-ttu-id="d2f71-178">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="d2f71-178">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d2f71-179">Adam</span><span class="sxs-lookup"><span data-stu-id="d2f71-179">ADAM</span></span>



| <span data-ttu-id="d2f71-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2f71-180">Entry</span></span> | <span data-ttu-id="d2f71-181">Wert</span><span class="sxs-lookup"><span data-stu-id="d2f71-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d2f71-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d2f71-182">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d2f71-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f71-183">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d2f71-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f71-184">System-Only</span></span>            | <span data-ttu-id="d2f71-185">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-185">False</span></span>                                                           |
| <span data-ttu-id="d2f71-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d2f71-186">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f71-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="d2f71-187">True</span></span>                                                            |
| <span data-ttu-id="d2f71-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d2f71-188">Is Indexed</span></span>             | <span data-ttu-id="d2f71-189">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-189">False</span></span>                                                           |
| <span data-ttu-id="d2f71-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d2f71-190">In Global Catalog</span></span>      | <span data-ttu-id="d2f71-191">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-191">False</span></span>                                                           |
| <span data-ttu-id="d2f71-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d2f71-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f71-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d2f71-193">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d2f71-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f71-194">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="d2f71-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f71-195">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="d2f71-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f71-196">Search-Flags</span></span>           | <span data-ttu-id="d2f71-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f71-197">0x00000000</span></span>                                                      |
| <span data-ttu-id="d2f71-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f71-198">System-Flags</span></span>           | <span data-ttu-id="d2f71-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f71-199">0x00000010</span></span>                                                      |
| <span data-ttu-id="d2f71-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d2f71-200">Classes used in</span></span>        | [<span data-ttu-id="d2f71-201">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="d2f71-201">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d2f71-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d2f71-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d2f71-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2f71-203">Entry</span></span> | <span data-ttu-id="d2f71-204">Wert</span><span class="sxs-lookup"><span data-stu-id="d2f71-204">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d2f71-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d2f71-205">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d2f71-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f71-206">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d2f71-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f71-207">System-Only</span></span>            | <span data-ttu-id="d2f71-208">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-208">False</span></span>                                                           |
| <span data-ttu-id="d2f71-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d2f71-209">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f71-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="d2f71-210">True</span></span>                                                            |
| <span data-ttu-id="d2f71-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d2f71-211">Is Indexed</span></span>             | <span data-ttu-id="d2f71-212">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-212">False</span></span>                                                           |
| <span data-ttu-id="d2f71-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d2f71-213">In Global Catalog</span></span>      | <span data-ttu-id="d2f71-214">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-214">False</span></span>                                                           |
| <span data-ttu-id="d2f71-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d2f71-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f71-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d2f71-216">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d2f71-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f71-217">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="d2f71-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f71-218">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="d2f71-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f71-219">Search-Flags</span></span>           | <span data-ttu-id="d2f71-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f71-220">0x00000000</span></span>                                                      |
| <span data-ttu-id="d2f71-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f71-221">System-Flags</span></span>           | <span data-ttu-id="d2f71-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f71-222">0x00000010</span></span>                                                      |
| <span data-ttu-id="d2f71-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d2f71-223">Classes used in</span></span>        | [<span data-ttu-id="d2f71-224">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="d2f71-224">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d2f71-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2f71-225">Windows Server 2008</span></span>



| <span data-ttu-id="d2f71-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2f71-226">Entry</span></span> | <span data-ttu-id="d2f71-227">Wert</span><span class="sxs-lookup"><span data-stu-id="d2f71-227">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d2f71-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d2f71-228">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d2f71-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f71-229">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d2f71-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f71-230">System-Only</span></span>            | <span data-ttu-id="d2f71-231">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-231">False</span></span>                                                           |
| <span data-ttu-id="d2f71-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d2f71-232">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f71-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="d2f71-233">True</span></span>                                                            |
| <span data-ttu-id="d2f71-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d2f71-234">Is Indexed</span></span>             | <span data-ttu-id="d2f71-235">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-235">False</span></span>                                                           |
| <span data-ttu-id="d2f71-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d2f71-236">In Global Catalog</span></span>      | <span data-ttu-id="d2f71-237">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-237">False</span></span>                                                           |
| <span data-ttu-id="d2f71-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d2f71-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f71-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d2f71-239">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d2f71-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f71-240">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="d2f71-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f71-241">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="d2f71-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f71-242">Search-Flags</span></span>           | <span data-ttu-id="d2f71-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f71-243">0x00000000</span></span>                                                      |
| <span data-ttu-id="d2f71-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f71-244">System-Flags</span></span>           | <span data-ttu-id="d2f71-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f71-245">0x00000010</span></span>                                                      |
| <span data-ttu-id="d2f71-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d2f71-246">Classes used in</span></span>        | [<span data-ttu-id="d2f71-247">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="d2f71-247">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d2f71-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d2f71-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d2f71-249">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2f71-249">Entry</span></span> | <span data-ttu-id="d2f71-250">Wert</span><span class="sxs-lookup"><span data-stu-id="d2f71-250">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d2f71-251">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d2f71-251">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d2f71-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f71-252">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d2f71-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f71-253">System-Only</span></span>            | <span data-ttu-id="d2f71-254">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-254">False</span></span>                                                           |
| <span data-ttu-id="d2f71-255">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d2f71-255">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f71-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="d2f71-256">True</span></span>                                                            |
| <span data-ttu-id="d2f71-257">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d2f71-257">Is Indexed</span></span>             | <span data-ttu-id="d2f71-258">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-258">False</span></span>                                                           |
| <span data-ttu-id="d2f71-259">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d2f71-259">In Global Catalog</span></span>      | <span data-ttu-id="d2f71-260">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-260">False</span></span>                                                           |
| <span data-ttu-id="d2f71-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d2f71-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f71-262">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d2f71-262">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d2f71-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f71-263">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="d2f71-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f71-264">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="d2f71-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f71-265">Search-Flags</span></span>           | <span data-ttu-id="d2f71-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f71-266">0x00000000</span></span>                                                      |
| <span data-ttu-id="d2f71-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f71-267">System-Flags</span></span>           | <span data-ttu-id="d2f71-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f71-268">0x00000010</span></span>                                                      |
| <span data-ttu-id="d2f71-269">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d2f71-269">Classes used in</span></span>        | [<span data-ttu-id="d2f71-270">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="d2f71-270">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d2f71-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d2f71-271">Windows Server 2012</span></span>



| <span data-ttu-id="d2f71-272">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2f71-272">Entry</span></span> | <span data-ttu-id="d2f71-273">Wert</span><span class="sxs-lookup"><span data-stu-id="d2f71-273">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d2f71-274">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d2f71-274">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d2f71-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f71-275">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d2f71-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f71-276">System-Only</span></span>            | <span data-ttu-id="d2f71-277">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-277">False</span></span>                                                           |
| <span data-ttu-id="d2f71-278">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d2f71-278">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f71-279">Richtig</span><span class="sxs-lookup"><span data-stu-id="d2f71-279">True</span></span>                                                            |
| <span data-ttu-id="d2f71-280">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d2f71-280">Is Indexed</span></span>             | <span data-ttu-id="d2f71-281">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-281">False</span></span>                                                           |
| <span data-ttu-id="d2f71-282">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d2f71-282">In Global Catalog</span></span>      | <span data-ttu-id="d2f71-283">False</span><span class="sxs-lookup"><span data-stu-id="d2f71-283">False</span></span>                                                           |
| <span data-ttu-id="d2f71-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d2f71-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f71-285">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d2f71-285">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d2f71-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f71-286">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="d2f71-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f71-287">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="d2f71-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f71-288">Search-Flags</span></span>           | <span data-ttu-id="d2f71-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f71-289">0x00000000</span></span>                                                      |
| <span data-ttu-id="d2f71-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f71-290">System-Flags</span></span>           | <span data-ttu-id="d2f71-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f71-291">0x00000010</span></span>                                                      |
| <span data-ttu-id="d2f71-292">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d2f71-292">Classes used in</span></span>        | [<span data-ttu-id="d2f71-293">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="d2f71-293">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





