---
title: Previous-Parent-ca-Attribut
description: Verweis auf die Zertifizierungsstellen, die das letzte abgelaufene Zertifikat für eine Zertifizierungsstelle ausgestellt haben.
ms.assetid: 9772d6cb-1105-426c-9982-473b4c1bf0d8
ms.tgt_platform: multiple
keywords:
- Previous-übergeordnetes Zertifizierungsstellen-Attribut AD-Schema
- "\"previousparentca\"-Attribut AD-Schema"
topic_type:
- apiref
api_name:
- Previous-Parent-CA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a4c89652ef7ffffdc731614cfc57572b3edcde
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104041034"
---
# <a name="previous-parent-ca-attribute"></a><span data-ttu-id="dfd1c-105">Previous-Parent-ca-Attribut</span><span class="sxs-lookup"><span data-stu-id="dfd1c-105">Previous-Parent-CA attribute</span></span>

<span data-ttu-id="dfd1c-106">Verweis auf die Zertifizierungsstellen, die das letzte abgelaufene Zertifikat für eine Zertifizierungsstelle ausgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="dfd1c-106">Reference to the certification authorities that issued the last expired certificate for a certification authority.</span></span>



| <span data-ttu-id="dfd1c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfd1c-107">Entry</span></span> | <span data-ttu-id="dfd1c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="dfd1c-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="dfd1c-109">CN</span><span class="sxs-lookup"><span data-stu-id="dfd1c-109">CN</span></span>                | <span data-ttu-id="dfd1c-110">Previous-Parent-ca</span><span class="sxs-lookup"><span data-stu-id="dfd1c-110">Previous-Parent-CA</span></span>                      |
| <span data-ttu-id="dfd1c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="dfd1c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="dfd1c-112">previousparentca</span><span class="sxs-lookup"><span data-stu-id="dfd1c-112">previousParentCA</span></span>                        |
| <span data-ttu-id="dfd1c-113">Size</span><span class="sxs-lookup"><span data-stu-id="dfd1c-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="dfd1c-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="dfd1c-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="dfd1c-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="dfd1c-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="dfd1c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dfd1c-116">Attribute-Id</span></span>      | <span data-ttu-id="dfd1c-117">1.2.840.113556.1.4.694</span><span class="sxs-lookup"><span data-stu-id="dfd1c-117">1.2.840.113556.1.4.694</span></span>                  |
| <span data-ttu-id="dfd1c-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dfd1c-118">System-Id-Guid</span></span>    | <span data-ttu-id="dfd1c-119">963d273d-48be-11d1-a9c3-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="dfd1c-119">963d273d-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="dfd1c-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfd1c-120">Syntax</span></span>            | [<span data-ttu-id="dfd1c-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="dfd1c-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="dfd1c-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="dfd1c-122">Implementations</span></span>

-   [<span data-ttu-id="dfd1c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dfd1c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dfd1c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dfd1c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dfd1c-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dfd1c-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dfd1c-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dfd1c-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dfd1c-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dfd1c-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dfd1c-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dfd1c-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dfd1c-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dfd1c-129">Windows 2000 Server</span></span>



| <span data-ttu-id="dfd1c-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfd1c-130">Entry</span></span> | <span data-ttu-id="dfd1c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="dfd1c-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="dfd1c-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dfd1c-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dfd1c-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfd1c-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dfd1c-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfd1c-134">System-Only</span></span>            | <span data-ttu-id="dfd1c-135">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-135">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dfd1c-136">Is-Single-Valued</span></span>       | <span data-ttu-id="dfd1c-137">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-137">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dfd1c-138">Is Indexed</span></span>             | <span data-ttu-id="dfd1c-139">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-139">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dfd1c-140">In Global Catalog</span></span>      | <span data-ttu-id="dfd1c-141">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-141">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfd1c-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfd1c-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dfd1c-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="dfd1c-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfd1c-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="dfd1c-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfd1c-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="dfd1c-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfd1c-146">Search-Flags</span></span>           | <span data-ttu-id="dfd1c-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfd1c-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="dfd1c-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfd1c-148">System-Flags</span></span>           | <span data-ttu-id="dfd1c-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfd1c-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="dfd1c-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dfd1c-150">Classes used in</span></span>        | [<span data-ttu-id="dfd1c-151">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="dfd1c-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dfd1c-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dfd1c-152">Windows Server 2003</span></span>



| <span data-ttu-id="dfd1c-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfd1c-153">Entry</span></span> | <span data-ttu-id="dfd1c-154">Wert</span><span class="sxs-lookup"><span data-stu-id="dfd1c-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="dfd1c-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dfd1c-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dfd1c-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfd1c-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dfd1c-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfd1c-157">System-Only</span></span>            | <span data-ttu-id="dfd1c-158">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-158">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dfd1c-159">Is-Single-Valued</span></span>       | <span data-ttu-id="dfd1c-160">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-160">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dfd1c-161">Is Indexed</span></span>             | <span data-ttu-id="dfd1c-162">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-162">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dfd1c-163">In Global Catalog</span></span>      | <span data-ttu-id="dfd1c-164">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-164">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfd1c-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfd1c-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dfd1c-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="dfd1c-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfd1c-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="dfd1c-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfd1c-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="dfd1c-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfd1c-169">Search-Flags</span></span>           | <span data-ttu-id="dfd1c-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfd1c-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="dfd1c-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfd1c-171">System-Flags</span></span>           | <span data-ttu-id="dfd1c-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfd1c-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="dfd1c-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dfd1c-173">Classes used in</span></span>        | [<span data-ttu-id="dfd1c-174">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="dfd1c-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dfd1c-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dfd1c-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dfd1c-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfd1c-176">Entry</span></span> | <span data-ttu-id="dfd1c-177">Wert</span><span class="sxs-lookup"><span data-stu-id="dfd1c-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="dfd1c-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dfd1c-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dfd1c-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfd1c-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dfd1c-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfd1c-180">System-Only</span></span>            | <span data-ttu-id="dfd1c-181">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-181">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dfd1c-182">Is-Single-Valued</span></span>       | <span data-ttu-id="dfd1c-183">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-183">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dfd1c-184">Is Indexed</span></span>             | <span data-ttu-id="dfd1c-185">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-185">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dfd1c-186">In Global Catalog</span></span>      | <span data-ttu-id="dfd1c-187">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-187">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfd1c-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfd1c-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dfd1c-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="dfd1c-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfd1c-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="dfd1c-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfd1c-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="dfd1c-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfd1c-192">Search-Flags</span></span>           | <span data-ttu-id="dfd1c-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfd1c-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="dfd1c-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfd1c-194">System-Flags</span></span>           | <span data-ttu-id="dfd1c-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfd1c-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="dfd1c-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dfd1c-196">Classes used in</span></span>        | [<span data-ttu-id="dfd1c-197">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="dfd1c-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dfd1c-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfd1c-198">Windows Server 2008</span></span>



| <span data-ttu-id="dfd1c-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfd1c-199">Entry</span></span> | <span data-ttu-id="dfd1c-200">Wert</span><span class="sxs-lookup"><span data-stu-id="dfd1c-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="dfd1c-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dfd1c-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dfd1c-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfd1c-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dfd1c-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfd1c-203">System-Only</span></span>            | <span data-ttu-id="dfd1c-204">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-204">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dfd1c-205">Is-Single-Valued</span></span>       | <span data-ttu-id="dfd1c-206">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-206">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dfd1c-207">Is Indexed</span></span>             | <span data-ttu-id="dfd1c-208">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-208">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dfd1c-209">In Global Catalog</span></span>      | <span data-ttu-id="dfd1c-210">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-210">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfd1c-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfd1c-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dfd1c-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="dfd1c-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfd1c-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="dfd1c-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfd1c-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="dfd1c-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfd1c-215">Search-Flags</span></span>           | <span data-ttu-id="dfd1c-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfd1c-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="dfd1c-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfd1c-217">System-Flags</span></span>           | <span data-ttu-id="dfd1c-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfd1c-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="dfd1c-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dfd1c-219">Classes used in</span></span>        | [<span data-ttu-id="dfd1c-220">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="dfd1c-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dfd1c-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dfd1c-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dfd1c-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfd1c-222">Entry</span></span> | <span data-ttu-id="dfd1c-223">Wert</span><span class="sxs-lookup"><span data-stu-id="dfd1c-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="dfd1c-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dfd1c-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dfd1c-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfd1c-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dfd1c-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfd1c-226">System-Only</span></span>            | <span data-ttu-id="dfd1c-227">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-227">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dfd1c-228">Is-Single-Valued</span></span>       | <span data-ttu-id="dfd1c-229">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-229">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dfd1c-230">Is Indexed</span></span>             | <span data-ttu-id="dfd1c-231">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-231">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dfd1c-232">In Global Catalog</span></span>      | <span data-ttu-id="dfd1c-233">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-233">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfd1c-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfd1c-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dfd1c-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="dfd1c-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfd1c-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="dfd1c-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfd1c-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="dfd1c-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfd1c-238">Search-Flags</span></span>           | <span data-ttu-id="dfd1c-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfd1c-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="dfd1c-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfd1c-240">System-Flags</span></span>           | <span data-ttu-id="dfd1c-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfd1c-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="dfd1c-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dfd1c-242">Classes used in</span></span>        | [<span data-ttu-id="dfd1c-243">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="dfd1c-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dfd1c-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dfd1c-244">Windows Server 2012</span></span>



| <span data-ttu-id="dfd1c-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfd1c-245">Entry</span></span> | <span data-ttu-id="dfd1c-246">Wert</span><span class="sxs-lookup"><span data-stu-id="dfd1c-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="dfd1c-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dfd1c-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dfd1c-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfd1c-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dfd1c-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfd1c-249">System-Only</span></span>            | <span data-ttu-id="dfd1c-250">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-250">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dfd1c-251">Is-Single-Valued</span></span>       | <span data-ttu-id="dfd1c-252">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-252">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dfd1c-253">Is Indexed</span></span>             | <span data-ttu-id="dfd1c-254">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-254">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dfd1c-255">In Global Catalog</span></span>      | <span data-ttu-id="dfd1c-256">False</span><span class="sxs-lookup"><span data-stu-id="dfd1c-256">False</span></span>                                                                  |
| <span data-ttu-id="dfd1c-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfd1c-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfd1c-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dfd1c-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="dfd1c-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfd1c-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="dfd1c-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfd1c-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="dfd1c-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfd1c-261">Search-Flags</span></span>           | <span data-ttu-id="dfd1c-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfd1c-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="dfd1c-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfd1c-263">System-Flags</span></span>           | <span data-ttu-id="dfd1c-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfd1c-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="dfd1c-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dfd1c-265">Classes used in</span></span>        | [<span data-ttu-id="dfd1c-266">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="dfd1c-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





