---
title: Pending-CA-Zertifikate-Attribut
description: Die Zertifikate, die für diese Zertifizierungsstelle wirksam werden sollen.
ms.assetid: ec803ff6-3408-4361-84ef-33c47a96e66a
ms.tgt_platform: multiple
keywords:
- AD-Schema für ausstehende Zertifizierungsstellen-Zertifikate
- pdingcacertificates-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Pending-CA-Certificates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1990d336c8cfb8efa0eefd1bfd9c1ccf3f8fa93f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744569"
---
# <a name="pending-ca-certificates-attribute"></a><span data-ttu-id="6362e-105">Pending-CA-Zertifikate-Attribut</span><span class="sxs-lookup"><span data-stu-id="6362e-105">Pending-CA-Certificates attribute</span></span>

<span data-ttu-id="6362e-106">Die Zertifikate, die für diese Zertifizierungsstelle wirksam werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6362e-106">The certificates that are about to become effective for this certification authority.</span></span>



| <span data-ttu-id="6362e-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6362e-107">Entry</span></span> | <span data-ttu-id="6362e-108">Wert</span><span class="sxs-lookup"><span data-stu-id="6362e-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="6362e-109">CN</span><span class="sxs-lookup"><span data-stu-id="6362e-109">CN</span></span>                | <span data-ttu-id="6362e-110">Pending-CA-Zertifikate</span><span class="sxs-lookup"><span data-stu-id="6362e-110">Pending-CA-Certificates</span></span>                               |
| <span data-ttu-id="6362e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6362e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6362e-112">kdingcacertificates</span><span class="sxs-lookup"><span data-stu-id="6362e-112">pendingCACertificates</span></span>                                 |
| <span data-ttu-id="6362e-113">Size</span><span class="sxs-lookup"><span data-stu-id="6362e-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="6362e-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="6362e-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="6362e-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="6362e-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="6362e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6362e-116">Attribute-Id</span></span>      | <span data-ttu-id="6362e-117">1.2.840.113556.1.4.693</span><span class="sxs-lookup"><span data-stu-id="6362e-117">1.2.840.113556.1.4.693</span></span>                                |
| <span data-ttu-id="6362e-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6362e-118">System-Id-Guid</span></span>    | <span data-ttu-id="6362e-119">963d273c-48be-11d1-a9c3-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="6362e-119">963d273c-48be-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="6362e-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="6362e-120">Syntax</span></span>            | [<span data-ttu-id="6362e-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="6362e-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="6362e-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="6362e-122">Implementations</span></span>

-   [<span data-ttu-id="6362e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6362e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6362e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6362e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6362e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6362e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6362e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6362e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6362e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6362e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6362e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6362e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6362e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6362e-129">Windows 2000 Server</span></span>



| <span data-ttu-id="6362e-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6362e-130">Entry</span></span> | <span data-ttu-id="6362e-131">Wert</span><span class="sxs-lookup"><span data-stu-id="6362e-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6362e-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6362e-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6362e-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6362e-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6362e-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="6362e-134">System-Only</span></span>            | <span data-ttu-id="6362e-135">False</span><span class="sxs-lookup"><span data-stu-id="6362e-135">False</span></span>                                                                  |
| <span data-ttu-id="6362e-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6362e-136">Is-Single-Valued</span></span>       | <span data-ttu-id="6362e-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="6362e-137">True</span></span>                                                                   |
| <span data-ttu-id="6362e-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6362e-138">Is Indexed</span></span>             | <span data-ttu-id="6362e-139">False</span><span class="sxs-lookup"><span data-stu-id="6362e-139">False</span></span>                                                                  |
| <span data-ttu-id="6362e-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6362e-140">In Global Catalog</span></span>      | <span data-ttu-id="6362e-141">False</span><span class="sxs-lookup"><span data-stu-id="6362e-141">False</span></span>                                                                  |
| <span data-ttu-id="6362e-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6362e-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="6362e-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6362e-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="6362e-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6362e-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="6362e-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6362e-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="6362e-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6362e-146">Search-Flags</span></span>           | <span data-ttu-id="6362e-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6362e-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="6362e-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6362e-148">System-Flags</span></span>           | <span data-ttu-id="6362e-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6362e-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="6362e-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6362e-150">Classes used in</span></span>        | [<span data-ttu-id="6362e-151">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="6362e-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6362e-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6362e-152">Windows Server 2003</span></span>



| <span data-ttu-id="6362e-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6362e-153">Entry</span></span> | <span data-ttu-id="6362e-154">Wert</span><span class="sxs-lookup"><span data-stu-id="6362e-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6362e-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6362e-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6362e-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6362e-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6362e-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="6362e-157">System-Only</span></span>            | <span data-ttu-id="6362e-158">False</span><span class="sxs-lookup"><span data-stu-id="6362e-158">False</span></span>                                                                  |
| <span data-ttu-id="6362e-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6362e-159">Is-Single-Valued</span></span>       | <span data-ttu-id="6362e-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="6362e-160">True</span></span>                                                                   |
| <span data-ttu-id="6362e-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6362e-161">Is Indexed</span></span>             | <span data-ttu-id="6362e-162">False</span><span class="sxs-lookup"><span data-stu-id="6362e-162">False</span></span>                                                                  |
| <span data-ttu-id="6362e-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6362e-163">In Global Catalog</span></span>      | <span data-ttu-id="6362e-164">False</span><span class="sxs-lookup"><span data-stu-id="6362e-164">False</span></span>                                                                  |
| <span data-ttu-id="6362e-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6362e-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="6362e-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6362e-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="6362e-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6362e-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="6362e-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6362e-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="6362e-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6362e-169">Search-Flags</span></span>           | <span data-ttu-id="6362e-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6362e-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="6362e-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6362e-171">System-Flags</span></span>           | <span data-ttu-id="6362e-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6362e-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="6362e-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6362e-173">Classes used in</span></span>        | [<span data-ttu-id="6362e-174">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="6362e-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6362e-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6362e-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6362e-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6362e-176">Entry</span></span> | <span data-ttu-id="6362e-177">Wert</span><span class="sxs-lookup"><span data-stu-id="6362e-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6362e-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6362e-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6362e-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6362e-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6362e-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="6362e-180">System-Only</span></span>            | <span data-ttu-id="6362e-181">False</span><span class="sxs-lookup"><span data-stu-id="6362e-181">False</span></span>                                                                  |
| <span data-ttu-id="6362e-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6362e-182">Is-Single-Valued</span></span>       | <span data-ttu-id="6362e-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="6362e-183">True</span></span>                                                                   |
| <span data-ttu-id="6362e-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6362e-184">Is Indexed</span></span>             | <span data-ttu-id="6362e-185">False</span><span class="sxs-lookup"><span data-stu-id="6362e-185">False</span></span>                                                                  |
| <span data-ttu-id="6362e-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6362e-186">In Global Catalog</span></span>      | <span data-ttu-id="6362e-187">False</span><span class="sxs-lookup"><span data-stu-id="6362e-187">False</span></span>                                                                  |
| <span data-ttu-id="6362e-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6362e-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="6362e-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6362e-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="6362e-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6362e-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="6362e-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6362e-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="6362e-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6362e-192">Search-Flags</span></span>           | <span data-ttu-id="6362e-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6362e-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="6362e-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6362e-194">System-Flags</span></span>           | <span data-ttu-id="6362e-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6362e-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="6362e-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6362e-196">Classes used in</span></span>        | [<span data-ttu-id="6362e-197">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="6362e-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6362e-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6362e-198">Windows Server 2008</span></span>



| <span data-ttu-id="6362e-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6362e-199">Entry</span></span> | <span data-ttu-id="6362e-200">Wert</span><span class="sxs-lookup"><span data-stu-id="6362e-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6362e-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6362e-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6362e-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6362e-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6362e-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="6362e-203">System-Only</span></span>            | <span data-ttu-id="6362e-204">False</span><span class="sxs-lookup"><span data-stu-id="6362e-204">False</span></span>                                                                  |
| <span data-ttu-id="6362e-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6362e-205">Is-Single-Valued</span></span>       | <span data-ttu-id="6362e-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="6362e-206">True</span></span>                                                                   |
| <span data-ttu-id="6362e-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6362e-207">Is Indexed</span></span>             | <span data-ttu-id="6362e-208">False</span><span class="sxs-lookup"><span data-stu-id="6362e-208">False</span></span>                                                                  |
| <span data-ttu-id="6362e-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6362e-209">In Global Catalog</span></span>      | <span data-ttu-id="6362e-210">False</span><span class="sxs-lookup"><span data-stu-id="6362e-210">False</span></span>                                                                  |
| <span data-ttu-id="6362e-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6362e-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="6362e-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6362e-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="6362e-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6362e-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="6362e-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6362e-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="6362e-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6362e-215">Search-Flags</span></span>           | <span data-ttu-id="6362e-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6362e-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="6362e-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6362e-217">System-Flags</span></span>           | <span data-ttu-id="6362e-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6362e-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="6362e-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6362e-219">Classes used in</span></span>        | [<span data-ttu-id="6362e-220">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="6362e-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6362e-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6362e-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6362e-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6362e-222">Entry</span></span> | <span data-ttu-id="6362e-223">Wert</span><span class="sxs-lookup"><span data-stu-id="6362e-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6362e-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6362e-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6362e-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6362e-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6362e-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="6362e-226">System-Only</span></span>            | <span data-ttu-id="6362e-227">False</span><span class="sxs-lookup"><span data-stu-id="6362e-227">False</span></span>                                                                  |
| <span data-ttu-id="6362e-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6362e-228">Is-Single-Valued</span></span>       | <span data-ttu-id="6362e-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="6362e-229">True</span></span>                                                                   |
| <span data-ttu-id="6362e-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6362e-230">Is Indexed</span></span>             | <span data-ttu-id="6362e-231">False</span><span class="sxs-lookup"><span data-stu-id="6362e-231">False</span></span>                                                                  |
| <span data-ttu-id="6362e-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6362e-232">In Global Catalog</span></span>      | <span data-ttu-id="6362e-233">False</span><span class="sxs-lookup"><span data-stu-id="6362e-233">False</span></span>                                                                  |
| <span data-ttu-id="6362e-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6362e-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="6362e-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6362e-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="6362e-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6362e-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="6362e-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6362e-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="6362e-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6362e-238">Search-Flags</span></span>           | <span data-ttu-id="6362e-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6362e-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="6362e-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6362e-240">System-Flags</span></span>           | <span data-ttu-id="6362e-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6362e-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="6362e-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6362e-242">Classes used in</span></span>        | [<span data-ttu-id="6362e-243">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="6362e-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6362e-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6362e-244">Windows Server 2012</span></span>



| <span data-ttu-id="6362e-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6362e-245">Entry</span></span> | <span data-ttu-id="6362e-246">Wert</span><span class="sxs-lookup"><span data-stu-id="6362e-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6362e-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6362e-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6362e-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6362e-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6362e-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="6362e-249">System-Only</span></span>            | <span data-ttu-id="6362e-250">False</span><span class="sxs-lookup"><span data-stu-id="6362e-250">False</span></span>                                                                  |
| <span data-ttu-id="6362e-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6362e-251">Is-Single-Valued</span></span>       | <span data-ttu-id="6362e-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="6362e-252">True</span></span>                                                                   |
| <span data-ttu-id="6362e-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6362e-253">Is Indexed</span></span>             | <span data-ttu-id="6362e-254">False</span><span class="sxs-lookup"><span data-stu-id="6362e-254">False</span></span>                                                                  |
| <span data-ttu-id="6362e-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6362e-255">In Global Catalog</span></span>      | <span data-ttu-id="6362e-256">False</span><span class="sxs-lookup"><span data-stu-id="6362e-256">False</span></span>                                                                  |
| <span data-ttu-id="6362e-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6362e-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="6362e-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6362e-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="6362e-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6362e-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="6362e-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6362e-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="6362e-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6362e-261">Search-Flags</span></span>           | <span data-ttu-id="6362e-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6362e-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="6362e-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6362e-263">System-Flags</span></span>           | <span data-ttu-id="6362e-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6362e-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="6362e-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6362e-265">Classes used in</span></span>        | [<span data-ttu-id="6362e-266">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="6362e-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





