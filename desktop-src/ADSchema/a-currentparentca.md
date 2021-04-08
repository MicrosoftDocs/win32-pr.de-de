---
title: Current-Parent-ca-Attribut
description: Verweis auf die Zertifizierungsstellen, die die aktuellen Zertifikate für eine Zertifizierungsstelle ausgestellt haben.
ms.assetid: 9b851a7f-4a69-46f2-b7e2-6ee0b2d8eec1
ms.tgt_platform: multiple
keywords:
- AD-Schema des Current-Parent-ca-Attributs
- currentcentca-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Current-Parent-CA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b26be2ccda41d998ed2b2b2c5dcddb1fcd2dcb2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957386"
---
# <a name="current-parent-ca-attribute"></a><span data-ttu-id="653bd-105">Current-Parent-ca-Attribut</span><span class="sxs-lookup"><span data-stu-id="653bd-105">Current-Parent-CA attribute</span></span>

<span data-ttu-id="653bd-106">Verweis auf die Zertifizierungsstellen, die die aktuellen Zertifikate für eine Zertifizierungsstelle ausgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="653bd-106">Reference to the certification authorities that issued the current certificates for a certification authority.</span></span>



| <span data-ttu-id="653bd-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="653bd-107">Entry</span></span> | <span data-ttu-id="653bd-108">Wert</span><span class="sxs-lookup"><span data-stu-id="653bd-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="653bd-109">CN</span><span class="sxs-lookup"><span data-stu-id="653bd-109">CN</span></span>                | <span data-ttu-id="653bd-110">Current-Parent-ca</span><span class="sxs-lookup"><span data-stu-id="653bd-110">Current-Parent-CA</span></span>                       |
| <span data-ttu-id="653bd-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="653bd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="653bd-112">currentparameentca</span><span class="sxs-lookup"><span data-stu-id="653bd-112">currentParentCA</span></span>                         |
| <span data-ttu-id="653bd-113">Size</span><span class="sxs-lookup"><span data-stu-id="653bd-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="653bd-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="653bd-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="653bd-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="653bd-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="653bd-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="653bd-116">Attribute-Id</span></span>      | <span data-ttu-id="653bd-117">1.2.840.113556.1.4.696</span><span class="sxs-lookup"><span data-stu-id="653bd-117">1.2.840.113556.1.4.696</span></span>                  |
| <span data-ttu-id="653bd-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="653bd-118">System-Id-Guid</span></span>    | <span data-ttu-id="653bd-119">963d273b-48be-11d1-a9c3-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="653bd-119">963d273f-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="653bd-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="653bd-120">Syntax</span></span>            | [<span data-ttu-id="653bd-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="653bd-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="653bd-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="653bd-122">Implementations</span></span>

-   [<span data-ttu-id="653bd-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="653bd-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="653bd-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="653bd-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="653bd-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="653bd-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="653bd-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="653bd-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="653bd-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="653bd-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="653bd-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="653bd-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="653bd-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="653bd-129">Windows 2000 Server</span></span>



| <span data-ttu-id="653bd-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="653bd-130">Entry</span></span> | <span data-ttu-id="653bd-131">Wert</span><span class="sxs-lookup"><span data-stu-id="653bd-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="653bd-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="653bd-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="653bd-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="653bd-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="653bd-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="653bd-134">System-Only</span></span>            | <span data-ttu-id="653bd-135">False</span><span class="sxs-lookup"><span data-stu-id="653bd-135">False</span></span>                                                                  |
| <span data-ttu-id="653bd-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="653bd-136">Is-Single-Valued</span></span>       | <span data-ttu-id="653bd-137">False</span><span class="sxs-lookup"><span data-stu-id="653bd-137">False</span></span>                                                                  |
| <span data-ttu-id="653bd-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="653bd-138">Is Indexed</span></span>             | <span data-ttu-id="653bd-139">False</span><span class="sxs-lookup"><span data-stu-id="653bd-139">False</span></span>                                                                  |
| <span data-ttu-id="653bd-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="653bd-140">In Global Catalog</span></span>      | <span data-ttu-id="653bd-141">False</span><span class="sxs-lookup"><span data-stu-id="653bd-141">False</span></span>                                                                  |
| <span data-ttu-id="653bd-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="653bd-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="653bd-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="653bd-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="653bd-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="653bd-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="653bd-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="653bd-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="653bd-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="653bd-146">Search-Flags</span></span>           | <span data-ttu-id="653bd-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="653bd-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="653bd-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="653bd-148">System-Flags</span></span>           | <span data-ttu-id="653bd-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="653bd-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="653bd-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="653bd-150">Classes used in</span></span>        | [<span data-ttu-id="653bd-151">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="653bd-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="653bd-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="653bd-152">Windows Server 2003</span></span>



| <span data-ttu-id="653bd-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="653bd-153">Entry</span></span> | <span data-ttu-id="653bd-154">Wert</span><span class="sxs-lookup"><span data-stu-id="653bd-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="653bd-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="653bd-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="653bd-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="653bd-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="653bd-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="653bd-157">System-Only</span></span>            | <span data-ttu-id="653bd-158">False</span><span class="sxs-lookup"><span data-stu-id="653bd-158">False</span></span>                                                                  |
| <span data-ttu-id="653bd-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="653bd-159">Is-Single-Valued</span></span>       | <span data-ttu-id="653bd-160">False</span><span class="sxs-lookup"><span data-stu-id="653bd-160">False</span></span>                                                                  |
| <span data-ttu-id="653bd-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="653bd-161">Is Indexed</span></span>             | <span data-ttu-id="653bd-162">False</span><span class="sxs-lookup"><span data-stu-id="653bd-162">False</span></span>                                                                  |
| <span data-ttu-id="653bd-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="653bd-163">In Global Catalog</span></span>      | <span data-ttu-id="653bd-164">False</span><span class="sxs-lookup"><span data-stu-id="653bd-164">False</span></span>                                                                  |
| <span data-ttu-id="653bd-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="653bd-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="653bd-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="653bd-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="653bd-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="653bd-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="653bd-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="653bd-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="653bd-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="653bd-169">Search-Flags</span></span>           | <span data-ttu-id="653bd-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="653bd-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="653bd-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="653bd-171">System-Flags</span></span>           | <span data-ttu-id="653bd-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="653bd-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="653bd-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="653bd-173">Classes used in</span></span>        | [<span data-ttu-id="653bd-174">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="653bd-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="653bd-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="653bd-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="653bd-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="653bd-176">Entry</span></span> | <span data-ttu-id="653bd-177">Wert</span><span class="sxs-lookup"><span data-stu-id="653bd-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="653bd-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="653bd-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="653bd-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="653bd-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="653bd-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="653bd-180">System-Only</span></span>            | <span data-ttu-id="653bd-181">False</span><span class="sxs-lookup"><span data-stu-id="653bd-181">False</span></span>                                                                  |
| <span data-ttu-id="653bd-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="653bd-182">Is-Single-Valued</span></span>       | <span data-ttu-id="653bd-183">False</span><span class="sxs-lookup"><span data-stu-id="653bd-183">False</span></span>                                                                  |
| <span data-ttu-id="653bd-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="653bd-184">Is Indexed</span></span>             | <span data-ttu-id="653bd-185">False</span><span class="sxs-lookup"><span data-stu-id="653bd-185">False</span></span>                                                                  |
| <span data-ttu-id="653bd-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="653bd-186">In Global Catalog</span></span>      | <span data-ttu-id="653bd-187">False</span><span class="sxs-lookup"><span data-stu-id="653bd-187">False</span></span>                                                                  |
| <span data-ttu-id="653bd-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="653bd-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="653bd-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="653bd-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="653bd-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="653bd-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="653bd-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="653bd-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="653bd-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="653bd-192">Search-Flags</span></span>           | <span data-ttu-id="653bd-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="653bd-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="653bd-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="653bd-194">System-Flags</span></span>           | <span data-ttu-id="653bd-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="653bd-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="653bd-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="653bd-196">Classes used in</span></span>        | [<span data-ttu-id="653bd-197">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="653bd-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="653bd-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="653bd-198">Windows Server 2008</span></span>



| <span data-ttu-id="653bd-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="653bd-199">Entry</span></span> | <span data-ttu-id="653bd-200">Wert</span><span class="sxs-lookup"><span data-stu-id="653bd-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="653bd-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="653bd-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="653bd-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="653bd-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="653bd-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="653bd-203">System-Only</span></span>            | <span data-ttu-id="653bd-204">False</span><span class="sxs-lookup"><span data-stu-id="653bd-204">False</span></span>                                                                  |
| <span data-ttu-id="653bd-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="653bd-205">Is-Single-Valued</span></span>       | <span data-ttu-id="653bd-206">False</span><span class="sxs-lookup"><span data-stu-id="653bd-206">False</span></span>                                                                  |
| <span data-ttu-id="653bd-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="653bd-207">Is Indexed</span></span>             | <span data-ttu-id="653bd-208">False</span><span class="sxs-lookup"><span data-stu-id="653bd-208">False</span></span>                                                                  |
| <span data-ttu-id="653bd-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="653bd-209">In Global Catalog</span></span>      | <span data-ttu-id="653bd-210">False</span><span class="sxs-lookup"><span data-stu-id="653bd-210">False</span></span>                                                                  |
| <span data-ttu-id="653bd-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="653bd-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="653bd-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="653bd-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="653bd-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="653bd-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="653bd-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="653bd-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="653bd-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="653bd-215">Search-Flags</span></span>           | <span data-ttu-id="653bd-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="653bd-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="653bd-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="653bd-217">System-Flags</span></span>           | <span data-ttu-id="653bd-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="653bd-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="653bd-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="653bd-219">Classes used in</span></span>        | [<span data-ttu-id="653bd-220">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="653bd-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="653bd-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="653bd-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="653bd-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="653bd-222">Entry</span></span> | <span data-ttu-id="653bd-223">Wert</span><span class="sxs-lookup"><span data-stu-id="653bd-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="653bd-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="653bd-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="653bd-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="653bd-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="653bd-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="653bd-226">System-Only</span></span>            | <span data-ttu-id="653bd-227">False</span><span class="sxs-lookup"><span data-stu-id="653bd-227">False</span></span>                                                                  |
| <span data-ttu-id="653bd-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="653bd-228">Is-Single-Valued</span></span>       | <span data-ttu-id="653bd-229">False</span><span class="sxs-lookup"><span data-stu-id="653bd-229">False</span></span>                                                                  |
| <span data-ttu-id="653bd-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="653bd-230">Is Indexed</span></span>             | <span data-ttu-id="653bd-231">False</span><span class="sxs-lookup"><span data-stu-id="653bd-231">False</span></span>                                                                  |
| <span data-ttu-id="653bd-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="653bd-232">In Global Catalog</span></span>      | <span data-ttu-id="653bd-233">False</span><span class="sxs-lookup"><span data-stu-id="653bd-233">False</span></span>                                                                  |
| <span data-ttu-id="653bd-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="653bd-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="653bd-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="653bd-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="653bd-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="653bd-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="653bd-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="653bd-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="653bd-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="653bd-238">Search-Flags</span></span>           | <span data-ttu-id="653bd-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="653bd-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="653bd-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="653bd-240">System-Flags</span></span>           | <span data-ttu-id="653bd-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="653bd-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="653bd-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="653bd-242">Classes used in</span></span>        | [<span data-ttu-id="653bd-243">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="653bd-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="653bd-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="653bd-244">Windows Server 2012</span></span>



| <span data-ttu-id="653bd-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="653bd-245">Entry</span></span> | <span data-ttu-id="653bd-246">Wert</span><span class="sxs-lookup"><span data-stu-id="653bd-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="653bd-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="653bd-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="653bd-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="653bd-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="653bd-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="653bd-249">System-Only</span></span>            | <span data-ttu-id="653bd-250">False</span><span class="sxs-lookup"><span data-stu-id="653bd-250">False</span></span>                                                                  |
| <span data-ttu-id="653bd-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="653bd-251">Is-Single-Valued</span></span>       | <span data-ttu-id="653bd-252">False</span><span class="sxs-lookup"><span data-stu-id="653bd-252">False</span></span>                                                                  |
| <span data-ttu-id="653bd-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="653bd-253">Is Indexed</span></span>             | <span data-ttu-id="653bd-254">False</span><span class="sxs-lookup"><span data-stu-id="653bd-254">False</span></span>                                                                  |
| <span data-ttu-id="653bd-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="653bd-255">In Global Catalog</span></span>      | <span data-ttu-id="653bd-256">False</span><span class="sxs-lookup"><span data-stu-id="653bd-256">False</span></span>                                                                  |
| <span data-ttu-id="653bd-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="653bd-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="653bd-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="653bd-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="653bd-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="653bd-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="653bd-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="653bd-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="653bd-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="653bd-261">Search-Flags</span></span>           | <span data-ttu-id="653bd-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="653bd-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="653bd-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="653bd-263">System-Flags</span></span>           | <span data-ttu-id="653bd-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="653bd-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="653bd-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="653bd-265">Classes used in</span></span>        | [<span data-ttu-id="653bd-266">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="653bd-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





