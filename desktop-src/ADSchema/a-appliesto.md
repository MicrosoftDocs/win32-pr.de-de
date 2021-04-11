---
title: Applies-To-Attribut
description: Enthält die Liste der Objektklassen, für die das erweiterte Recht gilt. In der Liste wird eine Objektklasse durch die schemaIDGUID-Eigenschaft für das zugehörige Schema Schema dargestellt.
ms.assetid: 8333e508-627c-42ce-865b-db061a5603db
ms.tgt_platform: multiple
keywords:
- AD-Schema für Applies-To-Attribut
- appliesTo-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Applies-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b96a2690f420259b038b54b6d2b070b41f56d4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123199"
---
# <a name="applies-to-attribute"></a><span data-ttu-id="9700e-106">Applies-To-Attribut</span><span class="sxs-lookup"><span data-stu-id="9700e-106">Applies-To attribute</span></span>

<span data-ttu-id="9700e-107">Enthält die Liste der Objektklassen, für die das erweiterte Recht gilt.</span><span class="sxs-lookup"><span data-stu-id="9700e-107">Contains the list of object classes that the extended right applies to.</span></span> <span data-ttu-id="9700e-108">In der Liste wird eine Objektklasse durch die schemaIDGUID-Eigenschaft für das zugehörige Schema Schema dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9700e-108">In the list, an object class is represented by the schemaIDGUID property for its schemaClass object.</span></span>



| <span data-ttu-id="9700e-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9700e-109">Entry</span></span> | <span data-ttu-id="9700e-110">Wert</span><span class="sxs-lookup"><span data-stu-id="9700e-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9700e-111">CN</span><span class="sxs-lookup"><span data-stu-id="9700e-111">CN</span></span>                | <span data-ttu-id="9700e-112">Applies-To</span><span class="sxs-lookup"><span data-stu-id="9700e-112">Applies-To</span></span>                                  |
| <span data-ttu-id="9700e-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9700e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9700e-114">appliesTo</span><span class="sxs-lookup"><span data-stu-id="9700e-114">appliesTo</span></span>                                   |
| <span data-ttu-id="9700e-115">Size</span><span class="sxs-lookup"><span data-stu-id="9700e-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="9700e-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="9700e-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="9700e-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="9700e-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="9700e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9700e-118">Attribute-Id</span></span>      | <span data-ttu-id="9700e-119">1.2.840.113556.1.4.341</span><span class="sxs-lookup"><span data-stu-id="9700e-119">1.2.840.113556.1.4.341</span></span>                      |
| <span data-ttu-id="9700e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9700e-120">System-Id-Guid</span></span>    | <span data-ttu-id="9700e-121">8297931d-86d3-11D0-AFDA-00c04f 930c9</span><span class="sxs-lookup"><span data-stu-id="9700e-121">8297931d-86d3-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="9700e-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="9700e-122">Syntax</span></span>            | [<span data-ttu-id="9700e-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9700e-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9700e-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="9700e-124">Implementations</span></span>

-   [<span data-ttu-id="9700e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9700e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9700e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9700e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9700e-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="9700e-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9700e-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9700e-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9700e-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9700e-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9700e-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9700e-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9700e-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9700e-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9700e-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9700e-132">Windows 2000 Server</span></span>



| <span data-ttu-id="9700e-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9700e-133">Entry</span></span> | <span data-ttu-id="9700e-134">Wert</span><span class="sxs-lookup"><span data-stu-id="9700e-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9700e-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9700e-135">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9700e-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9700e-136">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9700e-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="9700e-137">System-Only</span></span>            | <span data-ttu-id="9700e-138">False</span><span class="sxs-lookup"><span data-stu-id="9700e-138">False</span></span>                                                           |
| <span data-ttu-id="9700e-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9700e-139">Is-Single-Valued</span></span>       | <span data-ttu-id="9700e-140">False</span><span class="sxs-lookup"><span data-stu-id="9700e-140">False</span></span>                                                           |
| <span data-ttu-id="9700e-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9700e-141">Is Indexed</span></span>             | <span data-ttu-id="9700e-142">False</span><span class="sxs-lookup"><span data-stu-id="9700e-142">False</span></span>                                                           |
| <span data-ttu-id="9700e-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9700e-143">In Global Catalog</span></span>      | <span data-ttu-id="9700e-144">False</span><span class="sxs-lookup"><span data-stu-id="9700e-144">False</span></span>                                                           |
| <span data-ttu-id="9700e-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9700e-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="9700e-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9700e-146">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9700e-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9700e-147">Range-Lower</span></span>            | <span data-ttu-id="9700e-148">36</span><span class="sxs-lookup"><span data-stu-id="9700e-148">36</span></span>                                                              |
| <span data-ttu-id="9700e-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9700e-149">Range-Upper</span></span>            | <span data-ttu-id="9700e-150">36</span><span class="sxs-lookup"><span data-stu-id="9700e-150">36</span></span>                                                              |
| <span data-ttu-id="9700e-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9700e-151">Search-Flags</span></span>           | <span data-ttu-id="9700e-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9700e-152">0x00000000</span></span>                                                      |
| <span data-ttu-id="9700e-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9700e-153">System-Flags</span></span>           | <span data-ttu-id="9700e-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9700e-154">0x00000010</span></span>                                                      |
| <span data-ttu-id="9700e-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9700e-155">Classes used in</span></span>        | [<span data-ttu-id="9700e-156">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="9700e-156">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9700e-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9700e-157">Windows Server 2003</span></span>



| <span data-ttu-id="9700e-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9700e-158">Entry</span></span> | <span data-ttu-id="9700e-159">Wert</span><span class="sxs-lookup"><span data-stu-id="9700e-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9700e-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9700e-160">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9700e-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9700e-161">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9700e-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="9700e-162">System-Only</span></span>            | <span data-ttu-id="9700e-163">False</span><span class="sxs-lookup"><span data-stu-id="9700e-163">False</span></span>                                                           |
| <span data-ttu-id="9700e-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9700e-164">Is-Single-Valued</span></span>       | <span data-ttu-id="9700e-165">False</span><span class="sxs-lookup"><span data-stu-id="9700e-165">False</span></span>                                                           |
| <span data-ttu-id="9700e-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9700e-166">Is Indexed</span></span>             | <span data-ttu-id="9700e-167">False</span><span class="sxs-lookup"><span data-stu-id="9700e-167">False</span></span>                                                           |
| <span data-ttu-id="9700e-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9700e-168">In Global Catalog</span></span>      | <span data-ttu-id="9700e-169">False</span><span class="sxs-lookup"><span data-stu-id="9700e-169">False</span></span>                                                           |
| <span data-ttu-id="9700e-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9700e-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="9700e-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9700e-171">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9700e-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9700e-172">Range-Lower</span></span>            | <span data-ttu-id="9700e-173">36</span><span class="sxs-lookup"><span data-stu-id="9700e-173">36</span></span>                                                              |
| <span data-ttu-id="9700e-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9700e-174">Range-Upper</span></span>            | <span data-ttu-id="9700e-175">36</span><span class="sxs-lookup"><span data-stu-id="9700e-175">36</span></span>                                                              |
| <span data-ttu-id="9700e-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9700e-176">Search-Flags</span></span>           | <span data-ttu-id="9700e-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9700e-177">0x00000000</span></span>                                                      |
| <span data-ttu-id="9700e-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9700e-178">System-Flags</span></span>           | <span data-ttu-id="9700e-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9700e-179">0x00000010</span></span>                                                      |
| <span data-ttu-id="9700e-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9700e-180">Classes used in</span></span>        | [<span data-ttu-id="9700e-181">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="9700e-181">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9700e-182">Adam</span><span class="sxs-lookup"><span data-stu-id="9700e-182">ADAM</span></span>



| <span data-ttu-id="9700e-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9700e-183">Entry</span></span> | <span data-ttu-id="9700e-184">Wert</span><span class="sxs-lookup"><span data-stu-id="9700e-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9700e-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9700e-185">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9700e-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9700e-186">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9700e-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="9700e-187">System-Only</span></span>            | <span data-ttu-id="9700e-188">False</span><span class="sxs-lookup"><span data-stu-id="9700e-188">False</span></span>                                                           |
| <span data-ttu-id="9700e-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9700e-189">Is-Single-Valued</span></span>       | <span data-ttu-id="9700e-190">False</span><span class="sxs-lookup"><span data-stu-id="9700e-190">False</span></span>                                                           |
| <span data-ttu-id="9700e-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9700e-191">Is Indexed</span></span>             | <span data-ttu-id="9700e-192">False</span><span class="sxs-lookup"><span data-stu-id="9700e-192">False</span></span>                                                           |
| <span data-ttu-id="9700e-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9700e-193">In Global Catalog</span></span>      | <span data-ttu-id="9700e-194">False</span><span class="sxs-lookup"><span data-stu-id="9700e-194">False</span></span>                                                           |
| <span data-ttu-id="9700e-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9700e-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="9700e-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9700e-196">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9700e-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9700e-197">Range-Lower</span></span>            | <span data-ttu-id="9700e-198">36</span><span class="sxs-lookup"><span data-stu-id="9700e-198">36</span></span>                                                              |
| <span data-ttu-id="9700e-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9700e-199">Range-Upper</span></span>            | <span data-ttu-id="9700e-200">36</span><span class="sxs-lookup"><span data-stu-id="9700e-200">36</span></span>                                                              |
| <span data-ttu-id="9700e-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9700e-201">Search-Flags</span></span>           | <span data-ttu-id="9700e-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9700e-202">0x00000000</span></span>                                                      |
| <span data-ttu-id="9700e-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9700e-203">System-Flags</span></span>           | <span data-ttu-id="9700e-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9700e-204">0x00000010</span></span>                                                      |
| <span data-ttu-id="9700e-205">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9700e-205">Classes used in</span></span>        | [<span data-ttu-id="9700e-206">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="9700e-206">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9700e-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9700e-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9700e-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9700e-208">Entry</span></span> | <span data-ttu-id="9700e-209">Wert</span><span class="sxs-lookup"><span data-stu-id="9700e-209">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9700e-210">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9700e-210">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9700e-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9700e-211">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9700e-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="9700e-212">System-Only</span></span>            | <span data-ttu-id="9700e-213">False</span><span class="sxs-lookup"><span data-stu-id="9700e-213">False</span></span>                                                           |
| <span data-ttu-id="9700e-214">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9700e-214">Is-Single-Valued</span></span>       | <span data-ttu-id="9700e-215">False</span><span class="sxs-lookup"><span data-stu-id="9700e-215">False</span></span>                                                           |
| <span data-ttu-id="9700e-216">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9700e-216">Is Indexed</span></span>             | <span data-ttu-id="9700e-217">False</span><span class="sxs-lookup"><span data-stu-id="9700e-217">False</span></span>                                                           |
| <span data-ttu-id="9700e-218">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9700e-218">In Global Catalog</span></span>      | <span data-ttu-id="9700e-219">False</span><span class="sxs-lookup"><span data-stu-id="9700e-219">False</span></span>                                                           |
| <span data-ttu-id="9700e-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9700e-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="9700e-221">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9700e-221">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9700e-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9700e-222">Range-Lower</span></span>            | <span data-ttu-id="9700e-223">36</span><span class="sxs-lookup"><span data-stu-id="9700e-223">36</span></span>                                                              |
| <span data-ttu-id="9700e-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9700e-224">Range-Upper</span></span>            | <span data-ttu-id="9700e-225">36</span><span class="sxs-lookup"><span data-stu-id="9700e-225">36</span></span>                                                              |
| <span data-ttu-id="9700e-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9700e-226">Search-Flags</span></span>           | <span data-ttu-id="9700e-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9700e-227">0x00000000</span></span>                                                      |
| <span data-ttu-id="9700e-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9700e-228">System-Flags</span></span>           | <span data-ttu-id="9700e-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9700e-229">0x00000010</span></span>                                                      |
| <span data-ttu-id="9700e-230">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9700e-230">Classes used in</span></span>        | [<span data-ttu-id="9700e-231">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="9700e-231">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9700e-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9700e-232">Windows Server 2008</span></span>



| <span data-ttu-id="9700e-233">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9700e-233">Entry</span></span> | <span data-ttu-id="9700e-234">Wert</span><span class="sxs-lookup"><span data-stu-id="9700e-234">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9700e-235">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9700e-235">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9700e-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9700e-236">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9700e-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="9700e-237">System-Only</span></span>            | <span data-ttu-id="9700e-238">False</span><span class="sxs-lookup"><span data-stu-id="9700e-238">False</span></span>                                                           |
| <span data-ttu-id="9700e-239">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9700e-239">Is-Single-Valued</span></span>       | <span data-ttu-id="9700e-240">False</span><span class="sxs-lookup"><span data-stu-id="9700e-240">False</span></span>                                                           |
| <span data-ttu-id="9700e-241">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9700e-241">Is Indexed</span></span>             | <span data-ttu-id="9700e-242">False</span><span class="sxs-lookup"><span data-stu-id="9700e-242">False</span></span>                                                           |
| <span data-ttu-id="9700e-243">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9700e-243">In Global Catalog</span></span>      | <span data-ttu-id="9700e-244">False</span><span class="sxs-lookup"><span data-stu-id="9700e-244">False</span></span>                                                           |
| <span data-ttu-id="9700e-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9700e-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="9700e-246">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9700e-246">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9700e-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9700e-247">Range-Lower</span></span>            | <span data-ttu-id="9700e-248">36</span><span class="sxs-lookup"><span data-stu-id="9700e-248">36</span></span>                                                              |
| <span data-ttu-id="9700e-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9700e-249">Range-Upper</span></span>            | <span data-ttu-id="9700e-250">36</span><span class="sxs-lookup"><span data-stu-id="9700e-250">36</span></span>                                                              |
| <span data-ttu-id="9700e-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9700e-251">Search-Flags</span></span>           | <span data-ttu-id="9700e-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9700e-252">0x00000000</span></span>                                                      |
| <span data-ttu-id="9700e-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9700e-253">System-Flags</span></span>           | <span data-ttu-id="9700e-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9700e-254">0x00000010</span></span>                                                      |
| <span data-ttu-id="9700e-255">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9700e-255">Classes used in</span></span>        | [<span data-ttu-id="9700e-256">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="9700e-256">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9700e-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9700e-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9700e-258">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9700e-258">Entry</span></span> | <span data-ttu-id="9700e-259">Wert</span><span class="sxs-lookup"><span data-stu-id="9700e-259">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9700e-260">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9700e-260">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9700e-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9700e-261">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9700e-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="9700e-262">System-Only</span></span>            | <span data-ttu-id="9700e-263">False</span><span class="sxs-lookup"><span data-stu-id="9700e-263">False</span></span>                                                           |
| <span data-ttu-id="9700e-264">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9700e-264">Is-Single-Valued</span></span>       | <span data-ttu-id="9700e-265">False</span><span class="sxs-lookup"><span data-stu-id="9700e-265">False</span></span>                                                           |
| <span data-ttu-id="9700e-266">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9700e-266">Is Indexed</span></span>             | <span data-ttu-id="9700e-267">False</span><span class="sxs-lookup"><span data-stu-id="9700e-267">False</span></span>                                                           |
| <span data-ttu-id="9700e-268">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9700e-268">In Global Catalog</span></span>      | <span data-ttu-id="9700e-269">False</span><span class="sxs-lookup"><span data-stu-id="9700e-269">False</span></span>                                                           |
| <span data-ttu-id="9700e-270">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9700e-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="9700e-271">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9700e-271">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9700e-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9700e-272">Range-Lower</span></span>            | <span data-ttu-id="9700e-273">36</span><span class="sxs-lookup"><span data-stu-id="9700e-273">36</span></span>                                                              |
| <span data-ttu-id="9700e-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9700e-274">Range-Upper</span></span>            | <span data-ttu-id="9700e-275">36</span><span class="sxs-lookup"><span data-stu-id="9700e-275">36</span></span>                                                              |
| <span data-ttu-id="9700e-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9700e-276">Search-Flags</span></span>           | <span data-ttu-id="9700e-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9700e-277">0x00000000</span></span>                                                      |
| <span data-ttu-id="9700e-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9700e-278">System-Flags</span></span>           | <span data-ttu-id="9700e-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9700e-279">0x00000010</span></span>                                                      |
| <span data-ttu-id="9700e-280">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9700e-280">Classes used in</span></span>        | [<span data-ttu-id="9700e-281">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="9700e-281">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9700e-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9700e-282">Windows Server 2012</span></span>



| <span data-ttu-id="9700e-283">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9700e-283">Entry</span></span> | <span data-ttu-id="9700e-284">Wert</span><span class="sxs-lookup"><span data-stu-id="9700e-284">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9700e-285">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9700e-285">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9700e-286">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9700e-286">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9700e-287">System-Only</span><span class="sxs-lookup"><span data-stu-id="9700e-287">System-Only</span></span>            | <span data-ttu-id="9700e-288">False</span><span class="sxs-lookup"><span data-stu-id="9700e-288">False</span></span>                                                           |
| <span data-ttu-id="9700e-289">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9700e-289">Is-Single-Valued</span></span>       | <span data-ttu-id="9700e-290">False</span><span class="sxs-lookup"><span data-stu-id="9700e-290">False</span></span>                                                           |
| <span data-ttu-id="9700e-291">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9700e-291">Is Indexed</span></span>             | <span data-ttu-id="9700e-292">False</span><span class="sxs-lookup"><span data-stu-id="9700e-292">False</span></span>                                                           |
| <span data-ttu-id="9700e-293">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9700e-293">In Global Catalog</span></span>      | <span data-ttu-id="9700e-294">False</span><span class="sxs-lookup"><span data-stu-id="9700e-294">False</span></span>                                                           |
| <span data-ttu-id="9700e-295">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9700e-295">NT-Security-Descriptor</span></span> | <span data-ttu-id="9700e-296">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9700e-296">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9700e-297">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9700e-297">Range-Lower</span></span>            | <span data-ttu-id="9700e-298">36</span><span class="sxs-lookup"><span data-stu-id="9700e-298">36</span></span>                                                              |
| <span data-ttu-id="9700e-299">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9700e-299">Range-Upper</span></span>            | <span data-ttu-id="9700e-300">36</span><span class="sxs-lookup"><span data-stu-id="9700e-300">36</span></span>                                                              |
| <span data-ttu-id="9700e-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9700e-301">Search-Flags</span></span>           | <span data-ttu-id="9700e-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9700e-302">0x00000000</span></span>                                                      |
| <span data-ttu-id="9700e-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9700e-303">System-Flags</span></span>           | <span data-ttu-id="9700e-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9700e-304">0x00000010</span></span>                                                      |
| <span data-ttu-id="9700e-305">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9700e-305">Classes used in</span></span>        | [<span data-ttu-id="9700e-306">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="9700e-306">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





