---
title: Package-Type-Attribut
description: Dieses Attribut beschreibt den Installationstyp, der für ein Anwendungspaket erforderlich ist, z. b. msi, exe, CAB.
ms.assetid: 76505575-a2c9-4113-84ac-1d0689d9e0e4
ms.tgt_platform: multiple
keywords:
- AD-Schema für Package-Type-Attribut
- PackageType-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Package-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 325bb00484a3ee44cd23b98931c40fb440cdb3b1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122726"
---
# <a name="package-type-attribute"></a><span data-ttu-id="628bd-105">Package-Type-Attribut</span><span class="sxs-lookup"><span data-stu-id="628bd-105">Package-Type attribute</span></span>

<span data-ttu-id="628bd-106">Dieses Attribut beschreibt den Installationstyp, der für ein Anwendungspaket erforderlich ist, z. b. msi, exe, CAB.</span><span class="sxs-lookup"><span data-stu-id="628bd-106">This attribute describes the type of installation required for an application package, for example, MSI, EXE, CAB.</span></span>



| <span data-ttu-id="628bd-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="628bd-107">Entry</span></span> | <span data-ttu-id="628bd-108">Wert</span><span class="sxs-lookup"><span data-stu-id="628bd-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="628bd-109">CN</span><span class="sxs-lookup"><span data-stu-id="628bd-109">CN</span></span>                | <span data-ttu-id="628bd-110">Package-Type</span><span class="sxs-lookup"><span data-stu-id="628bd-110">Package-Type</span></span>                         |
| <span data-ttu-id="628bd-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="628bd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="628bd-112">packageType</span><span class="sxs-lookup"><span data-stu-id="628bd-112">packageType</span></span>                          |
| <span data-ttu-id="628bd-113">Size</span><span class="sxs-lookup"><span data-stu-id="628bd-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="628bd-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="628bd-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="628bd-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="628bd-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="628bd-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="628bd-116">Attribute-Id</span></span>      | <span data-ttu-id="628bd-117">1.2.840.113556.1.4.324</span><span class="sxs-lookup"><span data-stu-id="628bd-117">1.2.840.113556.1.4.324</span></span>               |
| <span data-ttu-id="628bd-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="628bd-118">System-Id-Guid</span></span>    | <span data-ttu-id="628bd-119">7d6c0e96-7E20-11D0-afd6-00c04f d930c9</span><span class="sxs-lookup"><span data-stu-id="628bd-119">7d6c0e96-7e20-11d0-afd6-00c04fd930c9</span></span> |
| <span data-ttu-id="628bd-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="628bd-120">Syntax</span></span>            | [<span data-ttu-id="628bd-121">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="628bd-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="628bd-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="628bd-122">Implementations</span></span>

-   [<span data-ttu-id="628bd-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="628bd-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="628bd-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="628bd-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="628bd-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="628bd-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="628bd-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="628bd-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="628bd-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="628bd-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="628bd-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="628bd-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="628bd-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="628bd-129">Windows 2000 Server</span></span>



| <span data-ttu-id="628bd-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="628bd-130">Entry</span></span> | <span data-ttu-id="628bd-131">Wert</span><span class="sxs-lookup"><span data-stu-id="628bd-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="628bd-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="628bd-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="628bd-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="628bd-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="628bd-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="628bd-134">System-Only</span></span>            | <span data-ttu-id="628bd-135">False</span><span class="sxs-lookup"><span data-stu-id="628bd-135">False</span></span>                                                            |
| <span data-ttu-id="628bd-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="628bd-136">Is-Single-Valued</span></span>       | <span data-ttu-id="628bd-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="628bd-137">True</span></span>                                                             |
| <span data-ttu-id="628bd-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="628bd-138">Is Indexed</span></span>             | <span data-ttu-id="628bd-139">False</span><span class="sxs-lookup"><span data-stu-id="628bd-139">False</span></span>                                                            |
| <span data-ttu-id="628bd-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="628bd-140">In Global Catalog</span></span>      | <span data-ttu-id="628bd-141">False</span><span class="sxs-lookup"><span data-stu-id="628bd-141">False</span></span>                                                            |
| <span data-ttu-id="628bd-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="628bd-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="628bd-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="628bd-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="628bd-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="628bd-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="628bd-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="628bd-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="628bd-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="628bd-146">Search-Flags</span></span>           | <span data-ttu-id="628bd-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="628bd-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="628bd-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="628bd-148">System-Flags</span></span>           | <span data-ttu-id="628bd-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="628bd-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="628bd-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="628bd-150">Classes used in</span></span>        | [<span data-ttu-id="628bd-151">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="628bd-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="628bd-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="628bd-152">Windows Server 2003</span></span>



| <span data-ttu-id="628bd-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="628bd-153">Entry</span></span> | <span data-ttu-id="628bd-154">Wert</span><span class="sxs-lookup"><span data-stu-id="628bd-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="628bd-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="628bd-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="628bd-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="628bd-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="628bd-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="628bd-157">System-Only</span></span>            | <span data-ttu-id="628bd-158">False</span><span class="sxs-lookup"><span data-stu-id="628bd-158">False</span></span>                                                            |
| <span data-ttu-id="628bd-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="628bd-159">Is-Single-Valued</span></span>       | <span data-ttu-id="628bd-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="628bd-160">True</span></span>                                                             |
| <span data-ttu-id="628bd-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="628bd-161">Is Indexed</span></span>             | <span data-ttu-id="628bd-162">False</span><span class="sxs-lookup"><span data-stu-id="628bd-162">False</span></span>                                                            |
| <span data-ttu-id="628bd-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="628bd-163">In Global Catalog</span></span>      | <span data-ttu-id="628bd-164">False</span><span class="sxs-lookup"><span data-stu-id="628bd-164">False</span></span>                                                            |
| <span data-ttu-id="628bd-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="628bd-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="628bd-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="628bd-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="628bd-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="628bd-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="628bd-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="628bd-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="628bd-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="628bd-169">Search-Flags</span></span>           | <span data-ttu-id="628bd-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="628bd-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="628bd-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="628bd-171">System-Flags</span></span>           | <span data-ttu-id="628bd-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="628bd-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="628bd-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="628bd-173">Classes used in</span></span>        | [<span data-ttu-id="628bd-174">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="628bd-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="628bd-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="628bd-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="628bd-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="628bd-176">Entry</span></span> | <span data-ttu-id="628bd-177">Wert</span><span class="sxs-lookup"><span data-stu-id="628bd-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="628bd-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="628bd-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="628bd-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="628bd-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="628bd-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="628bd-180">System-Only</span></span>            | <span data-ttu-id="628bd-181">False</span><span class="sxs-lookup"><span data-stu-id="628bd-181">False</span></span>                                                            |
| <span data-ttu-id="628bd-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="628bd-182">Is-Single-Valued</span></span>       | <span data-ttu-id="628bd-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="628bd-183">True</span></span>                                                             |
| <span data-ttu-id="628bd-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="628bd-184">Is Indexed</span></span>             | <span data-ttu-id="628bd-185">False</span><span class="sxs-lookup"><span data-stu-id="628bd-185">False</span></span>                                                            |
| <span data-ttu-id="628bd-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="628bd-186">In Global Catalog</span></span>      | <span data-ttu-id="628bd-187">False</span><span class="sxs-lookup"><span data-stu-id="628bd-187">False</span></span>                                                            |
| <span data-ttu-id="628bd-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="628bd-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="628bd-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="628bd-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="628bd-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="628bd-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="628bd-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="628bd-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="628bd-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="628bd-192">Search-Flags</span></span>           | <span data-ttu-id="628bd-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="628bd-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="628bd-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="628bd-194">System-Flags</span></span>           | <span data-ttu-id="628bd-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="628bd-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="628bd-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="628bd-196">Classes used in</span></span>        | [<span data-ttu-id="628bd-197">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="628bd-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="628bd-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="628bd-198">Windows Server 2008</span></span>



| <span data-ttu-id="628bd-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="628bd-199">Entry</span></span> | <span data-ttu-id="628bd-200">Wert</span><span class="sxs-lookup"><span data-stu-id="628bd-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="628bd-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="628bd-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="628bd-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="628bd-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="628bd-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="628bd-203">System-Only</span></span>            | <span data-ttu-id="628bd-204">False</span><span class="sxs-lookup"><span data-stu-id="628bd-204">False</span></span>                                                            |
| <span data-ttu-id="628bd-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="628bd-205">Is-Single-Valued</span></span>       | <span data-ttu-id="628bd-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="628bd-206">True</span></span>                                                             |
| <span data-ttu-id="628bd-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="628bd-207">Is Indexed</span></span>             | <span data-ttu-id="628bd-208">False</span><span class="sxs-lookup"><span data-stu-id="628bd-208">False</span></span>                                                            |
| <span data-ttu-id="628bd-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="628bd-209">In Global Catalog</span></span>      | <span data-ttu-id="628bd-210">False</span><span class="sxs-lookup"><span data-stu-id="628bd-210">False</span></span>                                                            |
| <span data-ttu-id="628bd-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="628bd-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="628bd-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="628bd-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="628bd-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="628bd-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="628bd-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="628bd-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="628bd-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="628bd-215">Search-Flags</span></span>           | <span data-ttu-id="628bd-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="628bd-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="628bd-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="628bd-217">System-Flags</span></span>           | <span data-ttu-id="628bd-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="628bd-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="628bd-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="628bd-219">Classes used in</span></span>        | [<span data-ttu-id="628bd-220">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="628bd-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="628bd-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="628bd-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="628bd-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="628bd-222">Entry</span></span> | <span data-ttu-id="628bd-223">Wert</span><span class="sxs-lookup"><span data-stu-id="628bd-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="628bd-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="628bd-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="628bd-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="628bd-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="628bd-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="628bd-226">System-Only</span></span>            | <span data-ttu-id="628bd-227">False</span><span class="sxs-lookup"><span data-stu-id="628bd-227">False</span></span>                                                            |
| <span data-ttu-id="628bd-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="628bd-228">Is-Single-Valued</span></span>       | <span data-ttu-id="628bd-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="628bd-229">True</span></span>                                                             |
| <span data-ttu-id="628bd-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="628bd-230">Is Indexed</span></span>             | <span data-ttu-id="628bd-231">False</span><span class="sxs-lookup"><span data-stu-id="628bd-231">False</span></span>                                                            |
| <span data-ttu-id="628bd-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="628bd-232">In Global Catalog</span></span>      | <span data-ttu-id="628bd-233">False</span><span class="sxs-lookup"><span data-stu-id="628bd-233">False</span></span>                                                            |
| <span data-ttu-id="628bd-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="628bd-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="628bd-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="628bd-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="628bd-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="628bd-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="628bd-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="628bd-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="628bd-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="628bd-238">Search-Flags</span></span>           | <span data-ttu-id="628bd-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="628bd-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="628bd-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="628bd-240">System-Flags</span></span>           | <span data-ttu-id="628bd-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="628bd-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="628bd-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="628bd-242">Classes used in</span></span>        | [<span data-ttu-id="628bd-243">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="628bd-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="628bd-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="628bd-244">Windows Server 2012</span></span>



| <span data-ttu-id="628bd-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="628bd-245">Entry</span></span> | <span data-ttu-id="628bd-246">Wert</span><span class="sxs-lookup"><span data-stu-id="628bd-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="628bd-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="628bd-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="628bd-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="628bd-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="628bd-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="628bd-249">System-Only</span></span>            | <span data-ttu-id="628bd-250">False</span><span class="sxs-lookup"><span data-stu-id="628bd-250">False</span></span>                                                            |
| <span data-ttu-id="628bd-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="628bd-251">Is-Single-Valued</span></span>       | <span data-ttu-id="628bd-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="628bd-252">True</span></span>                                                             |
| <span data-ttu-id="628bd-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="628bd-253">Is Indexed</span></span>             | <span data-ttu-id="628bd-254">False</span><span class="sxs-lookup"><span data-stu-id="628bd-254">False</span></span>                                                            |
| <span data-ttu-id="628bd-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="628bd-255">In Global Catalog</span></span>      | <span data-ttu-id="628bd-256">False</span><span class="sxs-lookup"><span data-stu-id="628bd-256">False</span></span>                                                            |
| <span data-ttu-id="628bd-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="628bd-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="628bd-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="628bd-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="628bd-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="628bd-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="628bd-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="628bd-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="628bd-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="628bd-261">Search-Flags</span></span>           | <span data-ttu-id="628bd-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="628bd-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="628bd-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="628bd-263">System-Flags</span></span>           | <span data-ttu-id="628bd-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="628bd-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="628bd-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="628bd-265">Classes used in</span></span>        | [<span data-ttu-id="628bd-266">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="628bd-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





