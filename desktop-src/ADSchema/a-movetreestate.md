---
title: Move-Tree-State-Attribut
description: Dieses Attribut enthält Zustandsinformationen für eine Verzeichnisstruktur, die verschoben wird.
ms.assetid: 13ec6d05-ed17-4a38-b2ae-7ad175f17b52
ms.tgt_platform: multiple
keywords:
- AD-Schema des Move-Tree-State-Attributs
- cschema für das Attribut "muvetreestate"
topic_type:
- apiref
api_name:
- Move-Tree-State
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3041d54dfcdb97d7c9e1629162908fab1577b60c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480143"
---
# <a name="move-tree-state-attribute"></a><span data-ttu-id="05d6f-105">Move-Tree-State-Attribut</span><span class="sxs-lookup"><span data-stu-id="05d6f-105">Move-Tree-State attribute</span></span>

<span data-ttu-id="05d6f-106">Dieses Attribut enthält Zustandsinformationen für eine Verzeichnisstruktur, die verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="05d6f-106">This attribute contains state information for a directory tree that is being moved.</span></span>



| <span data-ttu-id="05d6f-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="05d6f-107">Entry</span></span> | <span data-ttu-id="05d6f-108">Wert</span><span class="sxs-lookup"><span data-stu-id="05d6f-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="05d6f-109">CN</span><span class="sxs-lookup"><span data-stu-id="05d6f-109">CN</span></span>                | <span data-ttu-id="05d6f-110">Move-Tree-State</span><span class="sxs-lookup"><span data-stu-id="05d6f-110">Move-Tree-State</span></span>                                       |
| <span data-ttu-id="05d6f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="05d6f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="05d6f-112">"muvetreestate"</span><span class="sxs-lookup"><span data-stu-id="05d6f-112">moveTreeState</span></span>                                         |
| <span data-ttu-id="05d6f-113">Size</span><span class="sxs-lookup"><span data-stu-id="05d6f-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="05d6f-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="05d6f-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="05d6f-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="05d6f-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="05d6f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="05d6f-116">Attribute-Id</span></span>      | <span data-ttu-id="05d6f-117">1.2.840.113556.1.4.1305</span><span class="sxs-lookup"><span data-stu-id="05d6f-117">1.2.840.113556.1.4.1305</span></span>                               |
| <span data-ttu-id="05d6f-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="05d6f-118">System-Id-Guid</span></span>    | <span data-ttu-id="05d6f-119">1F 2ac2c8-3b71-11d2-90cc-00c04f d91ab1</span><span class="sxs-lookup"><span data-stu-id="05d6f-119">1f2ac2c8-3b71-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="05d6f-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="05d6f-120">Syntax</span></span>            | [<span data-ttu-id="05d6f-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="05d6f-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="05d6f-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="05d6f-122">Implementations</span></span>

-   [<span data-ttu-id="05d6f-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="05d6f-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="05d6f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="05d6f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="05d6f-125">**Adam**</span><span class="sxs-lookup"><span data-stu-id="05d6f-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="05d6f-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="05d6f-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="05d6f-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="05d6f-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="05d6f-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="05d6f-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="05d6f-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="05d6f-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="05d6f-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="05d6f-130">Windows 2000 Server</span></span>



| <span data-ttu-id="05d6f-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="05d6f-131">Entry</span></span> | <span data-ttu-id="05d6f-132">Wert</span><span class="sxs-lookup"><span data-stu-id="05d6f-132">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="05d6f-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="05d6f-133">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="05d6f-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05d6f-134">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="05d6f-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="05d6f-135">System-Only</span></span>            | <span data-ttu-id="05d6f-136">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-136">False</span></span>                                               |
| <span data-ttu-id="05d6f-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="05d6f-137">Is-Single-Valued</span></span>       | <span data-ttu-id="05d6f-138">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-138">False</span></span>                                               |
| <span data-ttu-id="05d6f-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="05d6f-139">Is Indexed</span></span>             | <span data-ttu-id="05d6f-140">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-140">False</span></span>                                               |
| <span data-ttu-id="05d6f-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="05d6f-141">In Global Catalog</span></span>      | <span data-ttu-id="05d6f-142">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-142">False</span></span>                                               |
| <span data-ttu-id="05d6f-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="05d6f-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="05d6f-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="05d6f-144">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="05d6f-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05d6f-145">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="05d6f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05d6f-146">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="05d6f-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05d6f-147">Search-Flags</span></span>           | <span data-ttu-id="05d6f-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05d6f-148">0x00000000</span></span>                                          |
| <span data-ttu-id="05d6f-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05d6f-149">System-Flags</span></span>           | <span data-ttu-id="05d6f-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05d6f-150">0x00000010</span></span>                                          |
| <span data-ttu-id="05d6f-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="05d6f-151">Classes used in</span></span>        | [<span data-ttu-id="05d6f-152">**Verloren und gefunden**</span><span class="sxs-lookup"><span data-stu-id="05d6f-152">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="05d6f-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="05d6f-153">Windows Server 2003</span></span>



| <span data-ttu-id="05d6f-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="05d6f-154">Entry</span></span> | <span data-ttu-id="05d6f-155">Wert</span><span class="sxs-lookup"><span data-stu-id="05d6f-155">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="05d6f-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="05d6f-156">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="05d6f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05d6f-157">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="05d6f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="05d6f-158">System-Only</span></span>            | <span data-ttu-id="05d6f-159">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-159">False</span></span>                                               |
| <span data-ttu-id="05d6f-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="05d6f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="05d6f-161">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-161">False</span></span>                                               |
| <span data-ttu-id="05d6f-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="05d6f-162">Is Indexed</span></span>             | <span data-ttu-id="05d6f-163">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-163">False</span></span>                                               |
| <span data-ttu-id="05d6f-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="05d6f-164">In Global Catalog</span></span>      | <span data-ttu-id="05d6f-165">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-165">False</span></span>                                               |
| <span data-ttu-id="05d6f-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="05d6f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="05d6f-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="05d6f-167">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="05d6f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05d6f-168">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="05d6f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05d6f-169">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="05d6f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05d6f-170">Search-Flags</span></span>           | <span data-ttu-id="05d6f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05d6f-171">0x00000000</span></span>                                          |
| <span data-ttu-id="05d6f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05d6f-172">System-Flags</span></span>           | <span data-ttu-id="05d6f-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05d6f-173">0x00000010</span></span>                                          |
| <span data-ttu-id="05d6f-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="05d6f-174">Classes used in</span></span>        | [<span data-ttu-id="05d6f-175">**Verloren und gefunden**</span><span class="sxs-lookup"><span data-stu-id="05d6f-175">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="adam"></a><span data-ttu-id="05d6f-176">Adam</span><span class="sxs-lookup"><span data-stu-id="05d6f-176">ADAM</span></span>



| <span data-ttu-id="05d6f-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="05d6f-177">Entry</span></span> | <span data-ttu-id="05d6f-178">Wert</span><span class="sxs-lookup"><span data-stu-id="05d6f-178">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="05d6f-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="05d6f-179">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="05d6f-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05d6f-180">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="05d6f-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="05d6f-181">System-Only</span></span>            | <span data-ttu-id="05d6f-182">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-182">False</span></span>                                               |
| <span data-ttu-id="05d6f-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="05d6f-183">Is-Single-Valued</span></span>       | <span data-ttu-id="05d6f-184">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-184">False</span></span>                                               |
| <span data-ttu-id="05d6f-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="05d6f-185">Is Indexed</span></span>             | <span data-ttu-id="05d6f-186">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-186">False</span></span>                                               |
| <span data-ttu-id="05d6f-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="05d6f-187">In Global Catalog</span></span>      | <span data-ttu-id="05d6f-188">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-188">False</span></span>                                               |
| <span data-ttu-id="05d6f-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="05d6f-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="05d6f-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="05d6f-190">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="05d6f-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05d6f-191">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="05d6f-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05d6f-192">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="05d6f-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05d6f-193">Search-Flags</span></span>           | <span data-ttu-id="05d6f-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05d6f-194">0x00000000</span></span>                                          |
| <span data-ttu-id="05d6f-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05d6f-195">System-Flags</span></span>           | <span data-ttu-id="05d6f-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05d6f-196">0x00000010</span></span>                                          |
| <span data-ttu-id="05d6f-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="05d6f-197">Classes used in</span></span>        | [<span data-ttu-id="05d6f-198">**Verloren und gefunden**</span><span class="sxs-lookup"><span data-stu-id="05d6f-198">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="05d6f-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="05d6f-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="05d6f-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="05d6f-200">Entry</span></span> | <span data-ttu-id="05d6f-201">Wert</span><span class="sxs-lookup"><span data-stu-id="05d6f-201">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="05d6f-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="05d6f-202">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="05d6f-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05d6f-203">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="05d6f-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="05d6f-204">System-Only</span></span>            | <span data-ttu-id="05d6f-205">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-205">False</span></span>                                               |
| <span data-ttu-id="05d6f-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="05d6f-206">Is-Single-Valued</span></span>       | <span data-ttu-id="05d6f-207">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-207">False</span></span>                                               |
| <span data-ttu-id="05d6f-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="05d6f-208">Is Indexed</span></span>             | <span data-ttu-id="05d6f-209">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-209">False</span></span>                                               |
| <span data-ttu-id="05d6f-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="05d6f-210">In Global Catalog</span></span>      | <span data-ttu-id="05d6f-211">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-211">False</span></span>                                               |
| <span data-ttu-id="05d6f-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="05d6f-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="05d6f-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="05d6f-213">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="05d6f-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05d6f-214">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="05d6f-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05d6f-215">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="05d6f-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05d6f-216">Search-Flags</span></span>           | <span data-ttu-id="05d6f-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05d6f-217">0x00000000</span></span>                                          |
| <span data-ttu-id="05d6f-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05d6f-218">System-Flags</span></span>           | <span data-ttu-id="05d6f-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05d6f-219">0x00000010</span></span>                                          |
| <span data-ttu-id="05d6f-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="05d6f-220">Classes used in</span></span>        | [<span data-ttu-id="05d6f-221">**Verloren und gefunden**</span><span class="sxs-lookup"><span data-stu-id="05d6f-221">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="05d6f-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05d6f-222">Windows Server 2008</span></span>



| <span data-ttu-id="05d6f-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="05d6f-223">Entry</span></span> | <span data-ttu-id="05d6f-224">Wert</span><span class="sxs-lookup"><span data-stu-id="05d6f-224">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="05d6f-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="05d6f-225">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="05d6f-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05d6f-226">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="05d6f-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="05d6f-227">System-Only</span></span>            | <span data-ttu-id="05d6f-228">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-228">False</span></span>                                               |
| <span data-ttu-id="05d6f-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="05d6f-229">Is-Single-Valued</span></span>       | <span data-ttu-id="05d6f-230">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-230">False</span></span>                                               |
| <span data-ttu-id="05d6f-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="05d6f-231">Is Indexed</span></span>             | <span data-ttu-id="05d6f-232">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-232">False</span></span>                                               |
| <span data-ttu-id="05d6f-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="05d6f-233">In Global Catalog</span></span>      | <span data-ttu-id="05d6f-234">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-234">False</span></span>                                               |
| <span data-ttu-id="05d6f-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="05d6f-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="05d6f-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="05d6f-236">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="05d6f-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05d6f-237">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="05d6f-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05d6f-238">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="05d6f-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05d6f-239">Search-Flags</span></span>           | <span data-ttu-id="05d6f-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05d6f-240">0x00000000</span></span>                                          |
| <span data-ttu-id="05d6f-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05d6f-241">System-Flags</span></span>           | <span data-ttu-id="05d6f-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05d6f-242">0x00000010</span></span>                                          |
| <span data-ttu-id="05d6f-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="05d6f-243">Classes used in</span></span>        | [<span data-ttu-id="05d6f-244">**Verloren und gefunden**</span><span class="sxs-lookup"><span data-stu-id="05d6f-244">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="05d6f-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="05d6f-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="05d6f-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="05d6f-246">Entry</span></span> | <span data-ttu-id="05d6f-247">Wert</span><span class="sxs-lookup"><span data-stu-id="05d6f-247">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="05d6f-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="05d6f-248">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="05d6f-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05d6f-249">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="05d6f-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="05d6f-250">System-Only</span></span>            | <span data-ttu-id="05d6f-251">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-251">False</span></span>                                               |
| <span data-ttu-id="05d6f-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="05d6f-252">Is-Single-Valued</span></span>       | <span data-ttu-id="05d6f-253">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-253">False</span></span>                                               |
| <span data-ttu-id="05d6f-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="05d6f-254">Is Indexed</span></span>             | <span data-ttu-id="05d6f-255">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-255">False</span></span>                                               |
| <span data-ttu-id="05d6f-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="05d6f-256">In Global Catalog</span></span>      | <span data-ttu-id="05d6f-257">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-257">False</span></span>                                               |
| <span data-ttu-id="05d6f-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="05d6f-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="05d6f-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="05d6f-259">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="05d6f-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05d6f-260">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="05d6f-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05d6f-261">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="05d6f-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05d6f-262">Search-Flags</span></span>           | <span data-ttu-id="05d6f-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05d6f-263">0x00000000</span></span>                                          |
| <span data-ttu-id="05d6f-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05d6f-264">System-Flags</span></span>           | <span data-ttu-id="05d6f-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05d6f-265">0x00000010</span></span>                                          |
| <span data-ttu-id="05d6f-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="05d6f-266">Classes used in</span></span>        | [<span data-ttu-id="05d6f-267">**Verloren und gefunden**</span><span class="sxs-lookup"><span data-stu-id="05d6f-267">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="05d6f-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="05d6f-268">Windows Server 2012</span></span>



| <span data-ttu-id="05d6f-269">Eingabe</span><span class="sxs-lookup"><span data-stu-id="05d6f-269">Entry</span></span> | <span data-ttu-id="05d6f-270">Wert</span><span class="sxs-lookup"><span data-stu-id="05d6f-270">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="05d6f-271">Link-ID</span><span class="sxs-lookup"><span data-stu-id="05d6f-271">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="05d6f-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05d6f-272">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="05d6f-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="05d6f-273">System-Only</span></span>            | <span data-ttu-id="05d6f-274">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-274">False</span></span>                                               |
| <span data-ttu-id="05d6f-275">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="05d6f-275">Is-Single-Valued</span></span>       | <span data-ttu-id="05d6f-276">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-276">False</span></span>                                               |
| <span data-ttu-id="05d6f-277">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="05d6f-277">Is Indexed</span></span>             | <span data-ttu-id="05d6f-278">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-278">False</span></span>                                               |
| <span data-ttu-id="05d6f-279">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="05d6f-279">In Global Catalog</span></span>      | <span data-ttu-id="05d6f-280">False</span><span class="sxs-lookup"><span data-stu-id="05d6f-280">False</span></span>                                               |
| <span data-ttu-id="05d6f-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="05d6f-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="05d6f-282">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="05d6f-282">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="05d6f-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05d6f-283">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="05d6f-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05d6f-284">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="05d6f-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05d6f-285">Search-Flags</span></span>           | <span data-ttu-id="05d6f-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05d6f-286">0x00000000</span></span>                                          |
| <span data-ttu-id="05d6f-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05d6f-287">System-Flags</span></span>           | <span data-ttu-id="05d6f-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05d6f-288">0x00000010</span></span>                                          |
| <span data-ttu-id="05d6f-289">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="05d6f-289">Classes used in</span></span>        | [<span data-ttu-id="05d6f-290">**Verloren und gefunden**</span><span class="sxs-lookup"><span data-stu-id="05d6f-290">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



 

 





