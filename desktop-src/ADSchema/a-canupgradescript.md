---
title: "\"Can-Upgrade-Script\"-Attribut"
description: Mit diesem Attribut wird die Liste der Anwendungspakete gespeichert, die durch aktualisiert werden können, oder die ein Upgrade für dieses Anwendungspaket durchführen können.
ms.assetid: 95dea9c7-dbbd-42fb-ab32-6b89490aa5d6
ms.tgt_platform: multiple
keywords:
- Kann-Upgrade-Skript Attribut AD-Schema
- AD-Schema des canupgradescript-Attributs
topic_type:
- apiref
api_name:
- Can-Upgrade-Script
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305e5b90c45d124a8647dd5d3a0af9c4a2ca6c4f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106343534"
---
# <a name="can-upgrade-script-attribute"></a><span data-ttu-id="9f15f-105">"Can-Upgrade-Script"-Attribut</span><span class="sxs-lookup"><span data-stu-id="9f15f-105">Can-Upgrade-Script attribute</span></span>

<span data-ttu-id="9f15f-106">Mit diesem Attribut wird die Liste der Anwendungspakete gespeichert, die durch aktualisiert werden können, oder die ein Upgrade für dieses Anwendungspaket durchführen können.</span><span class="sxs-lookup"><span data-stu-id="9f15f-106">This attribute stores the list of application packages that can be upgraded by or which can upgrade this application package.</span></span>



| <span data-ttu-id="9f15f-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9f15f-107">Entry</span></span> | <span data-ttu-id="9f15f-108">Wert</span><span class="sxs-lookup"><span data-stu-id="9f15f-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9f15f-109">CN</span><span class="sxs-lookup"><span data-stu-id="9f15f-109">CN</span></span>                | <span data-ttu-id="9f15f-110">"Can-Upgrade-Script"</span><span class="sxs-lookup"><span data-stu-id="9f15f-110">Can-Upgrade-Script</span></span>                          |
| <span data-ttu-id="9f15f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9f15f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9f15f-112">canupgradescript</span><span class="sxs-lookup"><span data-stu-id="9f15f-112">canUpgradeScript</span></span>                            |
| <span data-ttu-id="9f15f-113">Size</span><span class="sxs-lookup"><span data-stu-id="9f15f-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="9f15f-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="9f15f-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="9f15f-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="9f15f-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="9f15f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9f15f-116">Attribute-Id</span></span>      | <span data-ttu-id="9f15f-117">1.2.840.113556.1.4.815</span><span class="sxs-lookup"><span data-stu-id="9f15f-117">1.2.840.113556.1.4.815</span></span>                      |
| <span data-ttu-id="9f15f-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9f15f-118">System-Id-Guid</span></span>    | <span data-ttu-id="9f15f-119">d9e18314-8939-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="9f15f-119">d9e18314-8939-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="9f15f-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f15f-120">Syntax</span></span>            | [<span data-ttu-id="9f15f-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9f15f-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9f15f-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="9f15f-122">Implementations</span></span>

-   [<span data-ttu-id="9f15f-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9f15f-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9f15f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9f15f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9f15f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9f15f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9f15f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9f15f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9f15f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9f15f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9f15f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9f15f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9f15f-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9f15f-129">Windows 2000 Server</span></span>



| <span data-ttu-id="9f15f-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9f15f-130">Entry</span></span> | <span data-ttu-id="9f15f-131">Wert</span><span class="sxs-lookup"><span data-stu-id="9f15f-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="9f15f-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9f15f-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9f15f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f15f-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9f15f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f15f-134">System-Only</span></span>            | <span data-ttu-id="9f15f-135">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-135">False</span></span>                                                            |
| <span data-ttu-id="9f15f-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9f15f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="9f15f-137">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-137">False</span></span>                                                            |
| <span data-ttu-id="9f15f-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9f15f-138">Is Indexed</span></span>             | <span data-ttu-id="9f15f-139">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-139">False</span></span>                                                            |
| <span data-ttu-id="9f15f-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9f15f-140">In Global Catalog</span></span>      | <span data-ttu-id="9f15f-141">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-141">False</span></span>                                                            |
| <span data-ttu-id="9f15f-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9f15f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f15f-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9f15f-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="9f15f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f15f-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="9f15f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f15f-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="9f15f-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f15f-146">Search-Flags</span></span>           | <span data-ttu-id="9f15f-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f15f-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="9f15f-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f15f-148">System-Flags</span></span>           | <span data-ttu-id="9f15f-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f15f-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="9f15f-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9f15f-150">Classes used in</span></span>        | [<span data-ttu-id="9f15f-151">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="9f15f-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9f15f-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9f15f-152">Windows Server 2003</span></span>



| <span data-ttu-id="9f15f-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9f15f-153">Entry</span></span> | <span data-ttu-id="9f15f-154">Wert</span><span class="sxs-lookup"><span data-stu-id="9f15f-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="9f15f-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9f15f-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9f15f-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f15f-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9f15f-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f15f-157">System-Only</span></span>            | <span data-ttu-id="9f15f-158">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-158">False</span></span>                                                            |
| <span data-ttu-id="9f15f-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9f15f-159">Is-Single-Valued</span></span>       | <span data-ttu-id="9f15f-160">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-160">False</span></span>                                                            |
| <span data-ttu-id="9f15f-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9f15f-161">Is Indexed</span></span>             | <span data-ttu-id="9f15f-162">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-162">False</span></span>                                                            |
| <span data-ttu-id="9f15f-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9f15f-163">In Global Catalog</span></span>      | <span data-ttu-id="9f15f-164">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-164">False</span></span>                                                            |
| <span data-ttu-id="9f15f-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9f15f-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f15f-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9f15f-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="9f15f-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f15f-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="9f15f-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f15f-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="9f15f-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f15f-169">Search-Flags</span></span>           | <span data-ttu-id="9f15f-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f15f-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="9f15f-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f15f-171">System-Flags</span></span>           | <span data-ttu-id="9f15f-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f15f-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="9f15f-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9f15f-173">Classes used in</span></span>        | [<span data-ttu-id="9f15f-174">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="9f15f-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9f15f-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9f15f-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9f15f-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9f15f-176">Entry</span></span> | <span data-ttu-id="9f15f-177">Wert</span><span class="sxs-lookup"><span data-stu-id="9f15f-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="9f15f-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9f15f-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9f15f-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f15f-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9f15f-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f15f-180">System-Only</span></span>            | <span data-ttu-id="9f15f-181">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-181">False</span></span>                                                            |
| <span data-ttu-id="9f15f-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9f15f-182">Is-Single-Valued</span></span>       | <span data-ttu-id="9f15f-183">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-183">False</span></span>                                                            |
| <span data-ttu-id="9f15f-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9f15f-184">Is Indexed</span></span>             | <span data-ttu-id="9f15f-185">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-185">False</span></span>                                                            |
| <span data-ttu-id="9f15f-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9f15f-186">In Global Catalog</span></span>      | <span data-ttu-id="9f15f-187">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-187">False</span></span>                                                            |
| <span data-ttu-id="9f15f-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9f15f-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f15f-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9f15f-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="9f15f-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f15f-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="9f15f-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f15f-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="9f15f-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f15f-192">Search-Flags</span></span>           | <span data-ttu-id="9f15f-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f15f-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="9f15f-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f15f-194">System-Flags</span></span>           | <span data-ttu-id="9f15f-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f15f-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="9f15f-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9f15f-196">Classes used in</span></span>        | [<span data-ttu-id="9f15f-197">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="9f15f-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9f15f-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f15f-198">Windows Server 2008</span></span>



| <span data-ttu-id="9f15f-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9f15f-199">Entry</span></span> | <span data-ttu-id="9f15f-200">Wert</span><span class="sxs-lookup"><span data-stu-id="9f15f-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="9f15f-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9f15f-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9f15f-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f15f-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9f15f-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f15f-203">System-Only</span></span>            | <span data-ttu-id="9f15f-204">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-204">False</span></span>                                                            |
| <span data-ttu-id="9f15f-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9f15f-205">Is-Single-Valued</span></span>       | <span data-ttu-id="9f15f-206">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-206">False</span></span>                                                            |
| <span data-ttu-id="9f15f-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9f15f-207">Is Indexed</span></span>             | <span data-ttu-id="9f15f-208">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-208">False</span></span>                                                            |
| <span data-ttu-id="9f15f-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9f15f-209">In Global Catalog</span></span>      | <span data-ttu-id="9f15f-210">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-210">False</span></span>                                                            |
| <span data-ttu-id="9f15f-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9f15f-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f15f-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9f15f-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="9f15f-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f15f-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="9f15f-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f15f-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="9f15f-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f15f-215">Search-Flags</span></span>           | <span data-ttu-id="9f15f-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f15f-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="9f15f-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f15f-217">System-Flags</span></span>           | <span data-ttu-id="9f15f-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f15f-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="9f15f-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9f15f-219">Classes used in</span></span>        | [<span data-ttu-id="9f15f-220">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="9f15f-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9f15f-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9f15f-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9f15f-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9f15f-222">Entry</span></span> | <span data-ttu-id="9f15f-223">Wert</span><span class="sxs-lookup"><span data-stu-id="9f15f-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="9f15f-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9f15f-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9f15f-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f15f-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9f15f-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f15f-226">System-Only</span></span>            | <span data-ttu-id="9f15f-227">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-227">False</span></span>                                                            |
| <span data-ttu-id="9f15f-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9f15f-228">Is-Single-Valued</span></span>       | <span data-ttu-id="9f15f-229">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-229">False</span></span>                                                            |
| <span data-ttu-id="9f15f-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9f15f-230">Is Indexed</span></span>             | <span data-ttu-id="9f15f-231">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-231">False</span></span>                                                            |
| <span data-ttu-id="9f15f-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9f15f-232">In Global Catalog</span></span>      | <span data-ttu-id="9f15f-233">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-233">False</span></span>                                                            |
| <span data-ttu-id="9f15f-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9f15f-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f15f-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9f15f-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="9f15f-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f15f-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="9f15f-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f15f-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="9f15f-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f15f-238">Search-Flags</span></span>           | <span data-ttu-id="9f15f-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f15f-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="9f15f-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f15f-240">System-Flags</span></span>           | <span data-ttu-id="9f15f-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f15f-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="9f15f-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9f15f-242">Classes used in</span></span>        | [<span data-ttu-id="9f15f-243">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="9f15f-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9f15f-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9f15f-244">Windows Server 2012</span></span>



| <span data-ttu-id="9f15f-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9f15f-245">Entry</span></span> | <span data-ttu-id="9f15f-246">Wert</span><span class="sxs-lookup"><span data-stu-id="9f15f-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="9f15f-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9f15f-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9f15f-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f15f-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9f15f-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f15f-249">System-Only</span></span>            | <span data-ttu-id="9f15f-250">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-250">False</span></span>                                                            |
| <span data-ttu-id="9f15f-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9f15f-251">Is-Single-Valued</span></span>       | <span data-ttu-id="9f15f-252">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-252">False</span></span>                                                            |
| <span data-ttu-id="9f15f-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9f15f-253">Is Indexed</span></span>             | <span data-ttu-id="9f15f-254">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-254">False</span></span>                                                            |
| <span data-ttu-id="9f15f-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9f15f-255">In Global Catalog</span></span>      | <span data-ttu-id="9f15f-256">False</span><span class="sxs-lookup"><span data-stu-id="9f15f-256">False</span></span>                                                            |
| <span data-ttu-id="9f15f-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9f15f-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f15f-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9f15f-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="9f15f-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f15f-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="9f15f-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f15f-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="9f15f-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f15f-261">Search-Flags</span></span>           | <span data-ttu-id="9f15f-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f15f-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="9f15f-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f15f-263">System-Flags</span></span>           | <span data-ttu-id="9f15f-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f15f-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="9f15f-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9f15f-265">Classes used in</span></span>        | [<span data-ttu-id="9f15f-266">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="9f15f-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





