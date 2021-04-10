---
title: Site-Server-Attribut
description: Lizenzierungs Hauptserver für einen bestimmten Standort.
ms.assetid: bcae8c63-a953-4721-b2d1-96d0376592c6
ms.tgt_platform: multiple
keywords:
- AD-Schema für Site-Server-Attribut
- AD-Schema des Siteserver-Attributs
topic_type:
- apiref
api_name:
- Site-Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785057cd9ea23c05d58541450dc4c92a502877e5
ms.sourcegitcommit: f10bb95039c20a9de79f21e3fcb93a543f30a00e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "104213799"
---
# <a name="site-server-attribute"></a><span data-ttu-id="9e2a6-105">Site-Server-Attribut</span><span class="sxs-lookup"><span data-stu-id="9e2a6-105">Site-Server attribute</span></span>

<span data-ttu-id="9e2a6-106">Lizenzierungs Hauptserver für einen bestimmten Standort.</span><span class="sxs-lookup"><span data-stu-id="9e2a6-106">Licensing main server for a given Site.</span></span>



| <span data-ttu-id="9e2a6-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9e2a6-107">Entry</span></span> | <span data-ttu-id="9e2a6-108">Wert</span><span class="sxs-lookup"><span data-stu-id="9e2a6-108">Value</span></span> |
|-------------------|----------------------------------------------|
| <span data-ttu-id="9e2a6-109">CN</span><span class="sxs-lookup"><span data-stu-id="9e2a6-109">CN</span></span>                | <span data-ttu-id="9e2a6-110">Site-Server</span><span class="sxs-lookup"><span data-stu-id="9e2a6-110">Site-Server</span></span>                                  |
| <span data-ttu-id="9e2a6-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9e2a6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9e2a6-112">Standort Server</span><span class="sxs-lookup"><span data-stu-id="9e2a6-112">siteServer</span></span>                                   |
| <span data-ttu-id="9e2a6-113">Size</span><span class="sxs-lookup"><span data-stu-id="9e2a6-113">Size</span></span>              | \-                                           |
| <span data-ttu-id="9e2a6-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="9e2a6-114">Update Privilege</span></span>  | <span data-ttu-id="9e2a6-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="9e2a6-115">Domain administrator</span></span>                         |
| <span data-ttu-id="9e2a6-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="9e2a6-116">Update Frequency</span></span>  | <span data-ttu-id="9e2a6-117">Immer, wenn die Lizenzierungs Website geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="9e2a6-117">Whenever the licensing site needs to change.</span></span> |
| <span data-ttu-id="9e2a6-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9e2a6-118">Attribute-Id</span></span>      | <span data-ttu-id="9e2a6-119">1.2.840.113556.1.4.494</span><span class="sxs-lookup"><span data-stu-id="9e2a6-119">1.2.840.113556.1.4.494</span></span>                       |
| <span data-ttu-id="9e2a6-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9e2a6-120">System-Id-Guid</span></span>    | <span data-ttu-id="9e2a6-121">1be8f17c-a9ff-11D0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="9e2a6-121">1be8f17c-a9ff-11d0-afe2-00c04fd930c9</span></span>         |
| <span data-ttu-id="9e2a6-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e2a6-122">Syntax</span></span>            | [<span data-ttu-id="9e2a6-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="9e2a6-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)      |



## <a name="implementations"></a><span data-ttu-id="9e2a6-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="9e2a6-124">Implementations</span></span>

-   [<span data-ttu-id="9e2a6-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9e2a6-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9e2a6-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9e2a6-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9e2a6-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="9e2a6-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9e2a6-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9e2a6-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9e2a6-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9e2a6-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9e2a6-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9e2a6-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9e2a6-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9e2a6-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9e2a6-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9e2a6-132">Windows 2000 Server</span></span>



| <span data-ttu-id="9e2a6-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9e2a6-133">Entry</span></span> | <span data-ttu-id="9e2a6-134">Wert</span><span class="sxs-lookup"><span data-stu-id="9e2a6-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9e2a6-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9e2a6-135">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9e2a6-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2a6-136">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9e2a6-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2a6-137">System-Only</span></span>            | <span data-ttu-id="9e2a6-138">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-138">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9e2a6-139">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2a6-140">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-140">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9e2a6-141">Is Indexed</span></span>             | <span data-ttu-id="9e2a6-142">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-142">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9e2a6-143">In Global Catalog</span></span>      | <span data-ttu-id="9e2a6-144">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-144">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9e2a6-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2a6-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9e2a6-146">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="9e2a6-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2a6-147">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="9e2a6-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2a6-148">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="9e2a6-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a6-149">Search-Flags</span></span>           | <span data-ttu-id="9e2a6-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2a6-150">0x00000000</span></span>                                                            |
| <span data-ttu-id="9e2a6-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a6-151">System-Flags</span></span>           | <span data-ttu-id="9e2a6-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2a6-152">0x00000010</span></span>                                                            |
| <span data-ttu-id="9e2a6-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9e2a6-153">Classes used in</span></span>        | [<span data-ttu-id="9e2a6-154">**Lizenzierung-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="9e2a6-154">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9e2a6-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9e2a6-155">Windows Server 2003</span></span>



| <span data-ttu-id="9e2a6-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9e2a6-156">Entry</span></span> | <span data-ttu-id="9e2a6-157">Wert</span><span class="sxs-lookup"><span data-stu-id="9e2a6-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9e2a6-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9e2a6-158">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9e2a6-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2a6-159">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9e2a6-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2a6-160">System-Only</span></span>            | <span data-ttu-id="9e2a6-161">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-161">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9e2a6-162">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2a6-163">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-163">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9e2a6-164">Is Indexed</span></span>             | <span data-ttu-id="9e2a6-165">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-165">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9e2a6-166">In Global Catalog</span></span>      | <span data-ttu-id="9e2a6-167">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-167">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9e2a6-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2a6-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9e2a6-169">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="9e2a6-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2a6-170">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="9e2a6-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2a6-171">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="9e2a6-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a6-172">Search-Flags</span></span>           | <span data-ttu-id="9e2a6-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2a6-173">0x00000000</span></span>                                                            |
| <span data-ttu-id="9e2a6-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a6-174">System-Flags</span></span>           | <span data-ttu-id="9e2a6-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2a6-175">0x00000010</span></span>                                                            |
| <span data-ttu-id="9e2a6-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9e2a6-176">Classes used in</span></span>        | [<span data-ttu-id="9e2a6-177">**Lizenzierung-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="9e2a6-177">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9e2a6-178">Adam</span><span class="sxs-lookup"><span data-stu-id="9e2a6-178">ADAM</span></span>



| <span data-ttu-id="9e2a6-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9e2a6-179">Entry</span></span> | <span data-ttu-id="9e2a6-180">Wert</span><span class="sxs-lookup"><span data-stu-id="9e2a6-180">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="9e2a6-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9e2a6-181">Link-Id</span></span>                | \-           |
| <span data-ttu-id="9e2a6-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2a6-182">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="9e2a6-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2a6-183">System-Only</span></span>            | <span data-ttu-id="9e2a6-184">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-184">False</span></span>        |
| <span data-ttu-id="9e2a6-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9e2a6-185">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2a6-186">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-186">False</span></span>        |
| <span data-ttu-id="9e2a6-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9e2a6-187">Is Indexed</span></span>             | <span data-ttu-id="9e2a6-188">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-188">False</span></span>        |
| <span data-ttu-id="9e2a6-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9e2a6-189">In Global Catalog</span></span>      | <span data-ttu-id="9e2a6-190">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-190">False</span></span>        |
| <span data-ttu-id="9e2a6-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9e2a6-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2a6-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9e2a6-192">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="9e2a6-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2a6-193">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="9e2a6-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2a6-194">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="9e2a6-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a6-195">Search-Flags</span></span>           | <span data-ttu-id="9e2a6-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2a6-196">0x00000000</span></span>   |
| <span data-ttu-id="9e2a6-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a6-197">System-Flags</span></span>           | <span data-ttu-id="9e2a6-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2a6-198">0x00000010</span></span>   |
| <span data-ttu-id="9e2a6-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9e2a6-199">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9e2a6-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9e2a6-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9e2a6-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9e2a6-201">Entry</span></span> | <span data-ttu-id="9e2a6-202">Wert</span><span class="sxs-lookup"><span data-stu-id="9e2a6-202">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9e2a6-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9e2a6-203">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9e2a6-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2a6-204">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9e2a6-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2a6-205">System-Only</span></span>            | <span data-ttu-id="9e2a6-206">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-206">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9e2a6-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2a6-208">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-208">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9e2a6-209">Is Indexed</span></span>             | <span data-ttu-id="9e2a6-210">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-210">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9e2a6-211">In Global Catalog</span></span>      | <span data-ttu-id="9e2a6-212">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-212">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9e2a6-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2a6-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9e2a6-214">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="9e2a6-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2a6-215">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="9e2a6-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2a6-216">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="9e2a6-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a6-217">Search-Flags</span></span>           | <span data-ttu-id="9e2a6-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2a6-218">0x00000000</span></span>                                                            |
| <span data-ttu-id="9e2a6-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a6-219">System-Flags</span></span>           | <span data-ttu-id="9e2a6-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2a6-220">0x00000010</span></span>                                                            |
| <span data-ttu-id="9e2a6-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9e2a6-221">Classes used in</span></span>        | [<span data-ttu-id="9e2a6-222">**Lizenzierung-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="9e2a6-222">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9e2a6-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e2a6-223">Windows Server 2008</span></span>



| <span data-ttu-id="9e2a6-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9e2a6-224">Entry</span></span> | <span data-ttu-id="9e2a6-225">Wert</span><span class="sxs-lookup"><span data-stu-id="9e2a6-225">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9e2a6-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9e2a6-226">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9e2a6-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2a6-227">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9e2a6-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2a6-228">System-Only</span></span>            | <span data-ttu-id="9e2a6-229">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-229">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9e2a6-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2a6-231">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-231">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9e2a6-232">Is Indexed</span></span>             | <span data-ttu-id="9e2a6-233">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-233">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9e2a6-234">In Global Catalog</span></span>      | <span data-ttu-id="9e2a6-235">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-235">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9e2a6-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2a6-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9e2a6-237">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="9e2a6-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2a6-238">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="9e2a6-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2a6-239">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="9e2a6-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a6-240">Search-Flags</span></span>           | <span data-ttu-id="9e2a6-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2a6-241">0x00000000</span></span>                                                            |
| <span data-ttu-id="9e2a6-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a6-242">System-Flags</span></span>           | <span data-ttu-id="9e2a6-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2a6-243">0x00000010</span></span>                                                            |
| <span data-ttu-id="9e2a6-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9e2a6-244">Classes used in</span></span>        | [<span data-ttu-id="9e2a6-245">**Lizenzierung-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="9e2a6-245">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9e2a6-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9e2a6-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9e2a6-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9e2a6-247">Entry</span></span> | <span data-ttu-id="9e2a6-248">Wert</span><span class="sxs-lookup"><span data-stu-id="9e2a6-248">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9e2a6-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9e2a6-249">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9e2a6-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2a6-250">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9e2a6-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2a6-251">System-Only</span></span>            | <span data-ttu-id="9e2a6-252">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-252">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9e2a6-253">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2a6-254">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-254">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9e2a6-255">Is Indexed</span></span>             | <span data-ttu-id="9e2a6-256">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-256">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9e2a6-257">In Global Catalog</span></span>      | <span data-ttu-id="9e2a6-258">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-258">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9e2a6-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2a6-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9e2a6-260">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="9e2a6-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2a6-261">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="9e2a6-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2a6-262">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="9e2a6-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a6-263">Search-Flags</span></span>           | <span data-ttu-id="9e2a6-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2a6-264">0x00000000</span></span>                                                            |
| <span data-ttu-id="9e2a6-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a6-265">System-Flags</span></span>           | <span data-ttu-id="9e2a6-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2a6-266">0x00000010</span></span>                                                            |
| <span data-ttu-id="9e2a6-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9e2a6-267">Classes used in</span></span>        | [<span data-ttu-id="9e2a6-268">**Lizenzierung-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="9e2a6-268">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9e2a6-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e2a6-269">Windows Server 2012</span></span>



| <span data-ttu-id="9e2a6-270">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9e2a6-270">Entry</span></span> | <span data-ttu-id="9e2a6-271">Wert</span><span class="sxs-lookup"><span data-stu-id="9e2a6-271">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9e2a6-272">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9e2a6-272">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9e2a6-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2a6-273">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9e2a6-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2a6-274">System-Only</span></span>            | <span data-ttu-id="9e2a6-275">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-275">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-276">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9e2a6-276">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2a6-277">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-277">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-278">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9e2a6-278">Is Indexed</span></span>             | <span data-ttu-id="9e2a6-279">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-279">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-280">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9e2a6-280">In Global Catalog</span></span>      | <span data-ttu-id="9e2a6-281">False</span><span class="sxs-lookup"><span data-stu-id="9e2a6-281">False</span></span>                                                                 |
| <span data-ttu-id="9e2a6-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9e2a6-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2a6-283">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9e2a6-283">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="9e2a6-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2a6-284">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="9e2a6-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2a6-285">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="9e2a6-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a6-286">Search-Flags</span></span>           | <span data-ttu-id="9e2a6-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2a6-287">0x00000000</span></span>                                                            |
| <span data-ttu-id="9e2a6-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a6-288">System-Flags</span></span>           | <span data-ttu-id="9e2a6-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2a6-289">0x00000010</span></span>                                                            |
| <span data-ttu-id="9e2a6-290">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9e2a6-290">Classes used in</span></span>        | [<span data-ttu-id="9e2a6-291">**Lizenzierung-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="9e2a6-291">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



 

 





