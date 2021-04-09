---
title: ms-DS-Settings-Attribut
description: Wird verwendet, um Einstellungen für ein Objekt zu speichern. Die Verwendung hängt ausschließlich vom Besitzer des Objekts ab. Es wird empfohlen, diese zum Speichern von Name-Wert-Paaren zu verwenden. Beispielsweise Color Blue.
ms.assetid: 44e3a9e2-5528-4328-9cb7-1b6a4a77950a
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-Settings-Attribut
- AD-Schema für das msDS-Settings-Attribut
topic_type:
- apiref
api_name:
- ms-DS-Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f466bd5aa5a904482ff9c84c1f818c12205f69c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859668"
---
# <a name="ms-ds-settings-attribute"></a><span data-ttu-id="a7e38-108">ms-DS-Settings-Attribut</span><span class="sxs-lookup"><span data-stu-id="a7e38-108">ms-DS-Settings attribute</span></span>

<span data-ttu-id="a7e38-109">Wird verwendet, um Einstellungen für ein Objekt zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a7e38-109">Used to store settings for an object.</span></span> <span data-ttu-id="a7e38-110">Die Verwendung hängt ausschließlich vom Besitzer des Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="a7e38-110">Its use is solely determined by the object's owner.</span></span> <span data-ttu-id="a7e38-111">Es wird empfohlen, diese zum Speichern von Name-Wert-Paaren zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a7e38-111">We recommend using it to store name/value pairs.</span></span> <span data-ttu-id="a7e38-112">Beispielsweise Color = Blue.</span><span class="sxs-lookup"><span data-stu-id="a7e38-112">For example, color=blue.</span></span>



| <span data-ttu-id="a7e38-113">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a7e38-113">Entry</span></span> | <span data-ttu-id="a7e38-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a7e38-114">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a7e38-115">CN</span><span class="sxs-lookup"><span data-stu-id="a7e38-115">CN</span></span>                | <span data-ttu-id="a7e38-116">ms-DS-Settings</span><span class="sxs-lookup"><span data-stu-id="a7e38-116">ms-DS-Settings</span></span>                              |
| <span data-ttu-id="a7e38-117">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a7e38-117">Ldap-Display-Name</span></span> | <span data-ttu-id="a7e38-118">MSDS-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="a7e38-118">msDS-Settings</span></span>                               |
| <span data-ttu-id="a7e38-119">Size</span><span class="sxs-lookup"><span data-stu-id="a7e38-119">Size</span></span>              | \-                                          |
| <span data-ttu-id="a7e38-120">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a7e38-120">Update Privilege</span></span>  | <span data-ttu-id="a7e38-121">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="a7e38-121">Domain administrator</span></span>                        |
| <span data-ttu-id="a7e38-122">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="a7e38-122">Update Frequency</span></span>  | <span data-ttu-id="a7e38-123">Jedes Mal, wenn die Einstellungs Werte geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a7e38-123">Each time the settings values change.</span></span>       |
| <span data-ttu-id="a7e38-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a7e38-124">Attribute-Id</span></span>      | <span data-ttu-id="a7e38-125">1.2.840.113556.1.4.1697</span><span class="sxs-lookup"><span data-stu-id="a7e38-125">1.2.840.113556.1.4.1697</span></span>                     |
| <span data-ttu-id="a7e38-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a7e38-126">System-Id-Guid</span></span>    | <span data-ttu-id="a7e38-127">0e1b47d7-40A3-4 B48-8d1b-4cac0c1cdf21</span><span class="sxs-lookup"><span data-stu-id="a7e38-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span></span>        |
| <span data-ttu-id="a7e38-128">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7e38-128">Syntax</span></span>            | [<span data-ttu-id="a7e38-129">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a7e38-129">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a7e38-130">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="a7e38-130">Implementations</span></span>

-   [<span data-ttu-id="a7e38-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a7e38-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a7e38-132">**Adam**</span><span class="sxs-lookup"><span data-stu-id="a7e38-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a7e38-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a7e38-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a7e38-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a7e38-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a7e38-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a7e38-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a7e38-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a7e38-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a7e38-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a7e38-137">Windows Server 2003</span></span>



| <span data-ttu-id="a7e38-138">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a7e38-138">Entry</span></span> | <span data-ttu-id="a7e38-139">Wert</span><span class="sxs-lookup"><span data-stu-id="a7e38-139">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e38-140">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a7e38-140">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="a7e38-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7e38-141">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="a7e38-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7e38-142">System-Only</span></span>            | <span data-ttu-id="a7e38-143">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-143">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-144">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a7e38-144">Is-Single-Valued</span></span>       | <span data-ttu-id="a7e38-145">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-145">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-146">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a7e38-146">Is Indexed</span></span>             | <span data-ttu-id="a7e38-147">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-147">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-148">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a7e38-148">In Global Catalog</span></span>      | <span data-ttu-id="a7e38-149">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-149">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-150">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7e38-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7e38-151">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a7e38-151">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="a7e38-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7e38-152">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="a7e38-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7e38-153">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="a7e38-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e38-154">Search-Flags</span></span>           | <span data-ttu-id="a7e38-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e38-155">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="a7e38-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e38-156">System-Flags</span></span>           | <span data-ttu-id="a7e38-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e38-157">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="a7e38-158">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a7e38-158">Classes used in</span></span>        | [<span data-ttu-id="a7e38-159">**Anwendungseinstellungen**</span><span class="sxs-lookup"><span data-stu-id="a7e38-159">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="a7e38-160">**Verbindungspunkt**</span><span class="sxs-lookup"><span data-stu-id="a7e38-160">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a7e38-161">Adam</span><span class="sxs-lookup"><span data-stu-id="a7e38-161">ADAM</span></span>



| <span data-ttu-id="a7e38-162">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a7e38-162">Entry</span></span> | <span data-ttu-id="a7e38-163">Wert</span><span class="sxs-lookup"><span data-stu-id="a7e38-163">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="a7e38-164">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a7e38-164">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a7e38-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7e38-165">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a7e38-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7e38-166">System-Only</span></span>            | <span data-ttu-id="a7e38-167">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-167">False</span></span>                                                            |
| <span data-ttu-id="a7e38-168">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a7e38-168">Is-Single-Valued</span></span>       | <span data-ttu-id="a7e38-169">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-169">False</span></span>                                                            |
| <span data-ttu-id="a7e38-170">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a7e38-170">Is Indexed</span></span>             | <span data-ttu-id="a7e38-171">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-171">False</span></span>                                                            |
| <span data-ttu-id="a7e38-172">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a7e38-172">In Global Catalog</span></span>      | <span data-ttu-id="a7e38-173">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-173">False</span></span>                                                            |
| <span data-ttu-id="a7e38-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7e38-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7e38-175">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a7e38-175">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="a7e38-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7e38-176">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="a7e38-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7e38-177">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="a7e38-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e38-178">Search-Flags</span></span>           | <span data-ttu-id="a7e38-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e38-179">0x00000000</span></span>                                                       |
| <span data-ttu-id="a7e38-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e38-180">System-Flags</span></span>           | <span data-ttu-id="a7e38-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e38-181">0x00000000</span></span>                                                       |
| <span data-ttu-id="a7e38-182">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a7e38-182">Classes used in</span></span>        | [<span data-ttu-id="a7e38-183">**Anwendungseinstellungen**</span><span class="sxs-lookup"><span data-stu-id="a7e38-183">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a7e38-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a7e38-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a7e38-185">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a7e38-185">Entry</span></span> | <span data-ttu-id="a7e38-186">Wert</span><span class="sxs-lookup"><span data-stu-id="a7e38-186">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e38-187">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a7e38-187">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="a7e38-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7e38-188">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="a7e38-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7e38-189">System-Only</span></span>            | <span data-ttu-id="a7e38-190">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-190">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-191">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a7e38-191">Is-Single-Valued</span></span>       | <span data-ttu-id="a7e38-192">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-192">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-193">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a7e38-193">Is Indexed</span></span>             | <span data-ttu-id="a7e38-194">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-194">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-195">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a7e38-195">In Global Catalog</span></span>      | <span data-ttu-id="a7e38-196">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-196">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7e38-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7e38-198">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a7e38-198">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="a7e38-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7e38-199">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="a7e38-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7e38-200">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="a7e38-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e38-201">Search-Flags</span></span>           | <span data-ttu-id="a7e38-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e38-202">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="a7e38-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e38-203">System-Flags</span></span>           | <span data-ttu-id="a7e38-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e38-204">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="a7e38-205">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a7e38-205">Classes used in</span></span>        | [<span data-ttu-id="a7e38-206">**Anwendungseinstellungen**</span><span class="sxs-lookup"><span data-stu-id="a7e38-206">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="a7e38-207">**Verbindungspunkt**</span><span class="sxs-lookup"><span data-stu-id="a7e38-207">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a7e38-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7e38-208">Windows Server 2008</span></span>



| <span data-ttu-id="a7e38-209">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a7e38-209">Entry</span></span> | <span data-ttu-id="a7e38-210">Wert</span><span class="sxs-lookup"><span data-stu-id="a7e38-210">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e38-211">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a7e38-211">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="a7e38-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7e38-212">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="a7e38-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7e38-213">System-Only</span></span>            | <span data-ttu-id="a7e38-214">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-214">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-215">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a7e38-215">Is-Single-Valued</span></span>       | <span data-ttu-id="a7e38-216">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-216">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-217">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a7e38-217">Is Indexed</span></span>             | <span data-ttu-id="a7e38-218">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-218">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-219">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a7e38-219">In Global Catalog</span></span>      | <span data-ttu-id="a7e38-220">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-220">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-221">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7e38-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7e38-222">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a7e38-222">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="a7e38-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7e38-223">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="a7e38-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7e38-224">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="a7e38-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e38-225">Search-Flags</span></span>           | <span data-ttu-id="a7e38-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e38-226">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="a7e38-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e38-227">System-Flags</span></span>           | <span data-ttu-id="a7e38-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e38-228">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="a7e38-229">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a7e38-229">Classes used in</span></span>        | [<span data-ttu-id="a7e38-230">**Anwendungseinstellungen**</span><span class="sxs-lookup"><span data-stu-id="a7e38-230">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="a7e38-231">**Verbindungspunkt**</span><span class="sxs-lookup"><span data-stu-id="a7e38-231">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a7e38-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a7e38-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a7e38-233">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a7e38-233">Entry</span></span> | <span data-ttu-id="a7e38-234">Wert</span><span class="sxs-lookup"><span data-stu-id="a7e38-234">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e38-235">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a7e38-235">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="a7e38-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7e38-236">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="a7e38-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7e38-237">System-Only</span></span>            | <span data-ttu-id="a7e38-238">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-238">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-239">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a7e38-239">Is-Single-Valued</span></span>       | <span data-ttu-id="a7e38-240">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-240">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-241">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a7e38-241">Is Indexed</span></span>             | <span data-ttu-id="a7e38-242">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-242">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-243">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a7e38-243">In Global Catalog</span></span>      | <span data-ttu-id="a7e38-244">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-244">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7e38-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7e38-246">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a7e38-246">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="a7e38-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7e38-247">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="a7e38-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7e38-248">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="a7e38-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e38-249">Search-Flags</span></span>           | <span data-ttu-id="a7e38-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e38-250">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="a7e38-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e38-251">System-Flags</span></span>           | <span data-ttu-id="a7e38-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e38-252">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="a7e38-253">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a7e38-253">Classes used in</span></span>        | [<span data-ttu-id="a7e38-254">**Anwendungseinstellungen**</span><span class="sxs-lookup"><span data-stu-id="a7e38-254">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="a7e38-255">**Verbindungspunkt**</span><span class="sxs-lookup"><span data-stu-id="a7e38-255">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a7e38-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a7e38-256">Windows Server 2012</span></span>



| <span data-ttu-id="a7e38-257">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a7e38-257">Entry</span></span> | <span data-ttu-id="a7e38-258">Wert</span><span class="sxs-lookup"><span data-stu-id="a7e38-258">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e38-259">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a7e38-259">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="a7e38-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7e38-260">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="a7e38-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7e38-261">System-Only</span></span>            | <span data-ttu-id="a7e38-262">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-262">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-263">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a7e38-263">Is-Single-Valued</span></span>       | <span data-ttu-id="a7e38-264">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-264">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-265">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a7e38-265">Is Indexed</span></span>             | <span data-ttu-id="a7e38-266">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-266">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-267">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a7e38-267">In Global Catalog</span></span>      | <span data-ttu-id="a7e38-268">False</span><span class="sxs-lookup"><span data-stu-id="a7e38-268">False</span></span>                                                                                                                     |
| <span data-ttu-id="a7e38-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7e38-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7e38-270">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a7e38-270">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="a7e38-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7e38-271">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="a7e38-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7e38-272">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="a7e38-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e38-273">Search-Flags</span></span>           | <span data-ttu-id="a7e38-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e38-274">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="a7e38-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e38-275">System-Flags</span></span>           | <span data-ttu-id="a7e38-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e38-276">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="a7e38-277">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a7e38-277">Classes used in</span></span>        | [<span data-ttu-id="a7e38-278">**Anwendungseinstellungen**</span><span class="sxs-lookup"><span data-stu-id="a7e38-278">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="a7e38-279">**Verbindungspunkt**</span><span class="sxs-lookup"><span data-stu-id="a7e38-279">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



 

 





