---
title: ms-DS-Entry-Time-to-das-Attribut
description: Enthält die absolute Ablaufzeit eines dynamischen Objekts im Verzeichnis.
ms.assetid: 233a61a7-3e95-409e-89c3-1eeeca562173
ms.tgt_platform: multiple
keywords:
- AD-Schema für die ms-DS-Entry-Time-to-das-Attribut
- AD-Schema für MSDS-Entry-Time-to-das-Attribut
topic_type:
- apiref
api_name:
- ms-DS-Entry-Time-To-Die
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f074fbd5300cca87a437d4624100a0bd4734a52a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346797"
---
# <a name="ms-ds-entry-time-to-die-attribute"></a><span data-ttu-id="cb86a-105">ms-DS-Entry-Time-to-das-Attribut</span><span class="sxs-lookup"><span data-stu-id="cb86a-105">ms-DS-Entry-Time-To-Die attribute</span></span>

<span data-ttu-id="cb86a-106">Enthält die absolute Ablaufzeit eines dynamischen Objekts im Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="cb86a-106">Holds the absolute expiration time of a dynamic object in the directory.</span></span>



| <span data-ttu-id="cb86a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cb86a-107">Entry</span></span> | <span data-ttu-id="cb86a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="cb86a-108">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="cb86a-109">CN</span><span class="sxs-lookup"><span data-stu-id="cb86a-109">CN</span></span>                | <span data-ttu-id="cb86a-110">ms-DS-Entry-Time-to-be</span><span class="sxs-lookup"><span data-stu-id="cb86a-110">ms-DS-Entry-Time-To-Die</span></span>                                       |
| <span data-ttu-id="cb86a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cb86a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cb86a-112">MSDS-Entry-Time-to-be</span><span class="sxs-lookup"><span data-stu-id="cb86a-112">msDS-Entry-Time-To-Die</span></span>                                        |
| <span data-ttu-id="cb86a-113">Size</span><span class="sxs-lookup"><span data-stu-id="cb86a-113">Size</span></span>              | \-                                                            |
| <span data-ttu-id="cb86a-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="cb86a-114">Update Privilege</span></span>  | <span data-ttu-id="cb86a-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cb86a-115">This value is set by the system.</span></span>                              |
| <span data-ttu-id="cb86a-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="cb86a-116">Update Frequency</span></span>  | \-                                                            |
| <span data-ttu-id="cb86a-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cb86a-117">Attribute-Id</span></span>      | <span data-ttu-id="cb86a-118">1.2.840.113556.1.4.1622</span><span class="sxs-lookup"><span data-stu-id="cb86a-118">1.2.840.113556.1.4.1622</span></span>                                       |
| <span data-ttu-id="cb86a-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cb86a-119">System-Id-Guid</span></span>    | <span data-ttu-id="cb86a-120">e1e9bad7-c6dd-4101-A843-794cec85b038</span><span class="sxs-lookup"><span data-stu-id="cb86a-120">e1e9bad7-c6dd-4101-a843-794cec85b038</span></span>                          |
| <span data-ttu-id="cb86a-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb86a-121">Syntax</span></span>            | [<span data-ttu-id="cb86a-122">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="cb86a-122">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="cb86a-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="cb86a-123">Implementations</span></span>

-   [<span data-ttu-id="cb86a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cb86a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cb86a-125">**Adam**</span><span class="sxs-lookup"><span data-stu-id="cb86a-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cb86a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cb86a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cb86a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cb86a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cb86a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cb86a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cb86a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cb86a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="cb86a-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cb86a-130">Windows Server 2003</span></span>



| <span data-ttu-id="cb86a-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cb86a-131">Entry</span></span> | <span data-ttu-id="cb86a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="cb86a-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cb86a-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cb86a-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cb86a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb86a-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cb86a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb86a-135">System-Only</span></span>            | <span data-ttu-id="cb86a-136">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-136">True</span></span>                                                 |
| <span data-ttu-id="cb86a-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cb86a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="cb86a-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-138">True</span></span>                                                 |
| <span data-ttu-id="cb86a-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cb86a-139">Is Indexed</span></span>             | <span data-ttu-id="cb86a-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-140">True</span></span>                                                 |
| <span data-ttu-id="cb86a-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cb86a-141">In Global Catalog</span></span>      | <span data-ttu-id="cb86a-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-142">True</span></span>                                                 |
| <span data-ttu-id="cb86a-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cb86a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb86a-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cb86a-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cb86a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb86a-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="cb86a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb86a-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="cb86a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb86a-147">Search-Flags</span></span>           | <span data-ttu-id="cb86a-148">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cb86a-148">0x00000009</span></span>                                           |
| <span data-ttu-id="cb86a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb86a-149">System-Flags</span></span>           | <span data-ttu-id="cb86a-150">0x00000018</span><span class="sxs-lookup"><span data-stu-id="cb86a-150">0x00000018</span></span>                                           |
| <span data-ttu-id="cb86a-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cb86a-151">Classes used in</span></span>        | [<span data-ttu-id="cb86a-152">**Dynamic-Object**</span><span class="sxs-lookup"><span data-stu-id="cb86a-152">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cb86a-153">Adam</span><span class="sxs-lookup"><span data-stu-id="cb86a-153">ADAM</span></span>



| <span data-ttu-id="cb86a-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cb86a-154">Entry</span></span> | <span data-ttu-id="cb86a-155">Wert</span><span class="sxs-lookup"><span data-stu-id="cb86a-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cb86a-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cb86a-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cb86a-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb86a-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cb86a-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb86a-158">System-Only</span></span>            | <span data-ttu-id="cb86a-159">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-159">True</span></span>                                                 |
| <span data-ttu-id="cb86a-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cb86a-160">Is-Single-Valued</span></span>       | <span data-ttu-id="cb86a-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-161">True</span></span>                                                 |
| <span data-ttu-id="cb86a-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cb86a-162">Is Indexed</span></span>             | <span data-ttu-id="cb86a-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-163">True</span></span>                                                 |
| <span data-ttu-id="cb86a-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cb86a-164">In Global Catalog</span></span>      | <span data-ttu-id="cb86a-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-165">True</span></span>                                                 |
| <span data-ttu-id="cb86a-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cb86a-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb86a-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cb86a-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cb86a-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb86a-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="cb86a-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb86a-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="cb86a-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb86a-170">Search-Flags</span></span>           | <span data-ttu-id="cb86a-171">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cb86a-171">0x00000009</span></span>                                           |
| <span data-ttu-id="cb86a-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb86a-172">System-Flags</span></span>           | <span data-ttu-id="cb86a-173">0x00000018</span><span class="sxs-lookup"><span data-stu-id="cb86a-173">0x00000018</span></span>                                           |
| <span data-ttu-id="cb86a-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cb86a-174">Classes used in</span></span>        | [<span data-ttu-id="cb86a-175">**Dynamic-Object**</span><span class="sxs-lookup"><span data-stu-id="cb86a-175">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cb86a-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cb86a-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cb86a-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cb86a-177">Entry</span></span> | <span data-ttu-id="cb86a-178">Wert</span><span class="sxs-lookup"><span data-stu-id="cb86a-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cb86a-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cb86a-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cb86a-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb86a-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cb86a-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb86a-181">System-Only</span></span>            | <span data-ttu-id="cb86a-182">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-182">True</span></span>                                                 |
| <span data-ttu-id="cb86a-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cb86a-183">Is-Single-Valued</span></span>       | <span data-ttu-id="cb86a-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-184">True</span></span>                                                 |
| <span data-ttu-id="cb86a-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cb86a-185">Is Indexed</span></span>             | <span data-ttu-id="cb86a-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-186">True</span></span>                                                 |
| <span data-ttu-id="cb86a-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cb86a-187">In Global Catalog</span></span>      | <span data-ttu-id="cb86a-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-188">True</span></span>                                                 |
| <span data-ttu-id="cb86a-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cb86a-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb86a-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cb86a-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cb86a-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb86a-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="cb86a-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb86a-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="cb86a-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb86a-193">Search-Flags</span></span>           | <span data-ttu-id="cb86a-194">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cb86a-194">0x00000009</span></span>                                           |
| <span data-ttu-id="cb86a-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb86a-195">System-Flags</span></span>           | <span data-ttu-id="cb86a-196">0x00000018</span><span class="sxs-lookup"><span data-stu-id="cb86a-196">0x00000018</span></span>                                           |
| <span data-ttu-id="cb86a-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cb86a-197">Classes used in</span></span>        | [<span data-ttu-id="cb86a-198">**Dynamic-Object**</span><span class="sxs-lookup"><span data-stu-id="cb86a-198">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cb86a-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb86a-199">Windows Server 2008</span></span>



| <span data-ttu-id="cb86a-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cb86a-200">Entry</span></span> | <span data-ttu-id="cb86a-201">Wert</span><span class="sxs-lookup"><span data-stu-id="cb86a-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cb86a-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cb86a-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cb86a-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb86a-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cb86a-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb86a-204">System-Only</span></span>            | <span data-ttu-id="cb86a-205">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-205">True</span></span>                                                 |
| <span data-ttu-id="cb86a-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cb86a-206">Is-Single-Valued</span></span>       | <span data-ttu-id="cb86a-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-207">True</span></span>                                                 |
| <span data-ttu-id="cb86a-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cb86a-208">Is Indexed</span></span>             | <span data-ttu-id="cb86a-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-209">True</span></span>                                                 |
| <span data-ttu-id="cb86a-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cb86a-210">In Global Catalog</span></span>      | <span data-ttu-id="cb86a-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-211">True</span></span>                                                 |
| <span data-ttu-id="cb86a-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cb86a-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb86a-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cb86a-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cb86a-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb86a-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="cb86a-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb86a-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="cb86a-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb86a-216">Search-Flags</span></span>           | <span data-ttu-id="cb86a-217">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cb86a-217">0x00000009</span></span>                                           |
| <span data-ttu-id="cb86a-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb86a-218">System-Flags</span></span>           | <span data-ttu-id="cb86a-219">0x00000018</span><span class="sxs-lookup"><span data-stu-id="cb86a-219">0x00000018</span></span>                                           |
| <span data-ttu-id="cb86a-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cb86a-220">Classes used in</span></span>        | [<span data-ttu-id="cb86a-221">**Dynamic-Object**</span><span class="sxs-lookup"><span data-stu-id="cb86a-221">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cb86a-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cb86a-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cb86a-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cb86a-223">Entry</span></span> | <span data-ttu-id="cb86a-224">Wert</span><span class="sxs-lookup"><span data-stu-id="cb86a-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cb86a-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cb86a-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cb86a-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb86a-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cb86a-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb86a-227">System-Only</span></span>            | <span data-ttu-id="cb86a-228">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-228">True</span></span>                                                 |
| <span data-ttu-id="cb86a-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cb86a-229">Is-Single-Valued</span></span>       | <span data-ttu-id="cb86a-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-230">True</span></span>                                                 |
| <span data-ttu-id="cb86a-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cb86a-231">Is Indexed</span></span>             | <span data-ttu-id="cb86a-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-232">True</span></span>                                                 |
| <span data-ttu-id="cb86a-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cb86a-233">In Global Catalog</span></span>      | <span data-ttu-id="cb86a-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-234">True</span></span>                                                 |
| <span data-ttu-id="cb86a-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cb86a-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb86a-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cb86a-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cb86a-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb86a-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="cb86a-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb86a-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="cb86a-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb86a-239">Search-Flags</span></span>           | <span data-ttu-id="cb86a-240">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cb86a-240">0x00000009</span></span>                                           |
| <span data-ttu-id="cb86a-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb86a-241">System-Flags</span></span>           | <span data-ttu-id="cb86a-242">0x00000018</span><span class="sxs-lookup"><span data-stu-id="cb86a-242">0x00000018</span></span>                                           |
| <span data-ttu-id="cb86a-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cb86a-243">Classes used in</span></span>        | [<span data-ttu-id="cb86a-244">**Dynamic-Object**</span><span class="sxs-lookup"><span data-stu-id="cb86a-244">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cb86a-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cb86a-245">Windows Server 2012</span></span>



| <span data-ttu-id="cb86a-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cb86a-246">Entry</span></span> | <span data-ttu-id="cb86a-247">Wert</span><span class="sxs-lookup"><span data-stu-id="cb86a-247">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cb86a-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cb86a-248">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cb86a-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb86a-249">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cb86a-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb86a-250">System-Only</span></span>            | <span data-ttu-id="cb86a-251">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-251">True</span></span>                                                 |
| <span data-ttu-id="cb86a-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cb86a-252">Is-Single-Valued</span></span>       | <span data-ttu-id="cb86a-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-253">True</span></span>                                                 |
| <span data-ttu-id="cb86a-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cb86a-254">Is Indexed</span></span>             | <span data-ttu-id="cb86a-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-255">True</span></span>                                                 |
| <span data-ttu-id="cb86a-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cb86a-256">In Global Catalog</span></span>      | <span data-ttu-id="cb86a-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="cb86a-257">True</span></span>                                                 |
| <span data-ttu-id="cb86a-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cb86a-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb86a-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cb86a-259">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cb86a-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb86a-260">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="cb86a-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb86a-261">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="cb86a-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb86a-262">Search-Flags</span></span>           | <span data-ttu-id="cb86a-263">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cb86a-263">0x00000009</span></span>                                           |
| <span data-ttu-id="cb86a-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb86a-264">System-Flags</span></span>           | <span data-ttu-id="cb86a-265">0x00000018</span><span class="sxs-lookup"><span data-stu-id="cb86a-265">0x00000018</span></span>                                           |
| <span data-ttu-id="cb86a-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cb86a-266">Classes used in</span></span>        | [<span data-ttu-id="cb86a-267">**Dynamic-Object**</span><span class="sxs-lookup"><span data-stu-id="cb86a-267">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



 

 





