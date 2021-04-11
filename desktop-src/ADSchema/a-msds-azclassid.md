---
title: ms-DS-AZ-Class-ID-Attribut
description: Eine Klassen-ID, die von der azrollen-Benutzeroberfläche für das AzApplication-Objekt benötigt wird.
ms.assetid: cbbdc898-82b2-410e-8c9d-ae4f9641ac1a
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-DS-AZ-Class-ID-Attributs
- AD-Schema des msDS-azclassid-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Az-Class-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77d7ae6376deceaf23a9b7fa3c85ee8cb2b9748
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122978"
---
# <a name="ms-ds-az-class-id-attribute"></a><span data-ttu-id="3ee32-105">ms-DS-AZ-Class-ID-Attribut</span><span class="sxs-lookup"><span data-stu-id="3ee32-105">ms-DS-Az-Class-ID attribute</span></span>

<span data-ttu-id="3ee32-106">Eine Klassen-ID, die von der azrollen-Benutzeroberfläche für das AzApplication-Objekt benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="3ee32-106">A class ID required by the AzRoles UI on the AzApplication object.</span></span>



| <span data-ttu-id="3ee32-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3ee32-107">Entry</span></span> | <span data-ttu-id="3ee32-108">Wert</span><span class="sxs-lookup"><span data-stu-id="3ee32-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="3ee32-109">CN</span><span class="sxs-lookup"><span data-stu-id="3ee32-109">CN</span></span>                | <span data-ttu-id="3ee32-110">ms-DS-AZ-Class-ID</span><span class="sxs-lookup"><span data-stu-id="3ee32-110">ms-DS-Az-Class-ID</span></span>                           |
| <span data-ttu-id="3ee32-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3ee32-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3ee32-112">MSDS-azclassid</span><span class="sxs-lookup"><span data-stu-id="3ee32-112">msDS-AzClassId</span></span>                              |
| <span data-ttu-id="3ee32-113">Size</span><span class="sxs-lookup"><span data-stu-id="3ee32-113">Size</span></span>              | <span data-ttu-id="3ee32-114">36 Zeichen</span><span class="sxs-lookup"><span data-stu-id="3ee32-114">36 characters</span></span>                               |
| <span data-ttu-id="3ee32-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="3ee32-115">Update Privilege</span></span>  | <span data-ttu-id="3ee32-116">Azrollen-Administrator</span><span class="sxs-lookup"><span data-stu-id="3ee32-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="3ee32-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="3ee32-117">Update Frequency</span></span>  | <span data-ttu-id="3ee32-118">Während der Initialisierung oder Richtlinien Änderung.</span><span class="sxs-lookup"><span data-stu-id="3ee32-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="3ee32-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3ee32-119">Attribute-Id</span></span>      | <span data-ttu-id="3ee32-120">1.2.840.113556.1.4.1816</span><span class="sxs-lookup"><span data-stu-id="3ee32-120">1.2.840.113556.1.4.1816</span></span>                     |
| <span data-ttu-id="3ee32-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3ee32-121">System-Id-Guid</span></span>    | <span data-ttu-id="3ee32-122">013a7277-5c2d-49ef-a7de-b765b36a3f 6F</span><span class="sxs-lookup"><span data-stu-id="3ee32-122">013a7277-5c2d-49ef-a7de-b765b36a3f6f</span></span>        |
| <span data-ttu-id="3ee32-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ee32-123">Syntax</span></span>            | [<span data-ttu-id="3ee32-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3ee32-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="3ee32-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="3ee32-125">Implementations</span></span>

-   [<span data-ttu-id="3ee32-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3ee32-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3ee32-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3ee32-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3ee32-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3ee32-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3ee32-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3ee32-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3ee32-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3ee32-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="3ee32-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3ee32-131">Windows Server 2003</span></span>



| <span data-ttu-id="3ee32-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3ee32-132">Entry</span></span> | <span data-ttu-id="3ee32-133">Wert</span><span class="sxs-lookup"><span data-stu-id="3ee32-133">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="3ee32-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3ee32-134">Link-Id</span></span>                | \-           |
| <span data-ttu-id="3ee32-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ee32-135">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="3ee32-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ee32-136">System-Only</span></span>            | <span data-ttu-id="3ee32-137">False</span><span class="sxs-lookup"><span data-stu-id="3ee32-137">False</span></span>        |
| <span data-ttu-id="3ee32-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3ee32-138">Is-Single-Valued</span></span>       | <span data-ttu-id="3ee32-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="3ee32-139">True</span></span>         |
| <span data-ttu-id="3ee32-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3ee32-140">Is Indexed</span></span>             | <span data-ttu-id="3ee32-141">False</span><span class="sxs-lookup"><span data-stu-id="3ee32-141">False</span></span>        |
| <span data-ttu-id="3ee32-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3ee32-142">In Global Catalog</span></span>      | <span data-ttu-id="3ee32-143">False</span><span class="sxs-lookup"><span data-stu-id="3ee32-143">False</span></span>        |
| <span data-ttu-id="3ee32-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ee32-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ee32-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3ee32-145">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="3ee32-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ee32-146">Range-Lower</span></span>            | <span data-ttu-id="3ee32-147">0</span><span class="sxs-lookup"><span data-stu-id="3ee32-147">0</span></span>            |
| <span data-ttu-id="3ee32-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ee32-148">Range-Upper</span></span>            | <span data-ttu-id="3ee32-149">40</span><span class="sxs-lookup"><span data-stu-id="3ee32-149">40</span></span>           |
| <span data-ttu-id="3ee32-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ee32-150">Search-Flags</span></span>           | <span data-ttu-id="3ee32-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ee32-151">0x00000000</span></span>   |
| <span data-ttu-id="3ee32-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ee32-152">System-Flags</span></span>           | <span data-ttu-id="3ee32-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ee32-153">0x00000010</span></span>   |
| <span data-ttu-id="3ee32-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3ee32-154">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3ee32-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3ee32-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3ee32-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3ee32-156">Entry</span></span> | <span data-ttu-id="3ee32-157">Wert</span><span class="sxs-lookup"><span data-stu-id="3ee32-157">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="3ee32-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3ee32-158">Link-Id</span></span>                | \-           |
| <span data-ttu-id="3ee32-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ee32-159">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="3ee32-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ee32-160">System-Only</span></span>            | <span data-ttu-id="3ee32-161">False</span><span class="sxs-lookup"><span data-stu-id="3ee32-161">False</span></span>        |
| <span data-ttu-id="3ee32-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3ee32-162">Is-Single-Valued</span></span>       | <span data-ttu-id="3ee32-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="3ee32-163">True</span></span>         |
| <span data-ttu-id="3ee32-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3ee32-164">Is Indexed</span></span>             | <span data-ttu-id="3ee32-165">False</span><span class="sxs-lookup"><span data-stu-id="3ee32-165">False</span></span>        |
| <span data-ttu-id="3ee32-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3ee32-166">In Global Catalog</span></span>      | <span data-ttu-id="3ee32-167">False</span><span class="sxs-lookup"><span data-stu-id="3ee32-167">False</span></span>        |
| <span data-ttu-id="3ee32-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ee32-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ee32-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3ee32-169">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="3ee32-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ee32-170">Range-Lower</span></span>            | <span data-ttu-id="3ee32-171">0</span><span class="sxs-lookup"><span data-stu-id="3ee32-171">0</span></span>            |
| <span data-ttu-id="3ee32-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ee32-172">Range-Upper</span></span>            | <span data-ttu-id="3ee32-173">40</span><span class="sxs-lookup"><span data-stu-id="3ee32-173">40</span></span>           |
| <span data-ttu-id="3ee32-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ee32-174">Search-Flags</span></span>           | <span data-ttu-id="3ee32-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ee32-175">0x00000000</span></span>   |
| <span data-ttu-id="3ee32-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ee32-176">System-Flags</span></span>           | <span data-ttu-id="3ee32-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ee32-177">0x00000010</span></span>   |
| <span data-ttu-id="3ee32-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3ee32-178">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="3ee32-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ee32-179">Windows Server 2008</span></span>



| <span data-ttu-id="3ee32-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3ee32-180">Entry</span></span> | <span data-ttu-id="3ee32-181">Wert</span><span class="sxs-lookup"><span data-stu-id="3ee32-181">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="3ee32-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3ee32-182">Link-Id</span></span>                | \-           |
| <span data-ttu-id="3ee32-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ee32-183">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="3ee32-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ee32-184">System-Only</span></span>            | <span data-ttu-id="3ee32-185">False</span><span class="sxs-lookup"><span data-stu-id="3ee32-185">False</span></span>        |
| <span data-ttu-id="3ee32-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3ee32-186">Is-Single-Valued</span></span>       | <span data-ttu-id="3ee32-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="3ee32-187">True</span></span>         |
| <span data-ttu-id="3ee32-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3ee32-188">Is Indexed</span></span>             | <span data-ttu-id="3ee32-189">False</span><span class="sxs-lookup"><span data-stu-id="3ee32-189">False</span></span>        |
| <span data-ttu-id="3ee32-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3ee32-190">In Global Catalog</span></span>      | <span data-ttu-id="3ee32-191">False</span><span class="sxs-lookup"><span data-stu-id="3ee32-191">False</span></span>        |
| <span data-ttu-id="3ee32-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ee32-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ee32-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3ee32-193">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="3ee32-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ee32-194">Range-Lower</span></span>            | <span data-ttu-id="3ee32-195">0</span><span class="sxs-lookup"><span data-stu-id="3ee32-195">0</span></span>            |
| <span data-ttu-id="3ee32-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ee32-196">Range-Upper</span></span>            | <span data-ttu-id="3ee32-197">40</span><span class="sxs-lookup"><span data-stu-id="3ee32-197">40</span></span>           |
| <span data-ttu-id="3ee32-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ee32-198">Search-Flags</span></span>           | <span data-ttu-id="3ee32-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ee32-199">0x00000000</span></span>   |
| <span data-ttu-id="3ee32-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ee32-200">System-Flags</span></span>           | <span data-ttu-id="3ee32-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ee32-201">0x00000010</span></span>   |
| <span data-ttu-id="3ee32-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3ee32-202">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3ee32-203">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3ee32-203">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3ee32-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3ee32-204">Entry</span></span> | <span data-ttu-id="3ee32-205">Wert</span><span class="sxs-lookup"><span data-stu-id="3ee32-205">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="3ee32-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3ee32-206">Link-Id</span></span>                | \-           |
| <span data-ttu-id="3ee32-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ee32-207">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="3ee32-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ee32-208">System-Only</span></span>            | <span data-ttu-id="3ee32-209">False</span><span class="sxs-lookup"><span data-stu-id="3ee32-209">False</span></span>        |
| <span data-ttu-id="3ee32-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3ee32-210">Is-Single-Valued</span></span>       | <span data-ttu-id="3ee32-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="3ee32-211">True</span></span>         |
| <span data-ttu-id="3ee32-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3ee32-212">Is Indexed</span></span>             | <span data-ttu-id="3ee32-213">False</span><span class="sxs-lookup"><span data-stu-id="3ee32-213">False</span></span>        |
| <span data-ttu-id="3ee32-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3ee32-214">In Global Catalog</span></span>      | <span data-ttu-id="3ee32-215">False</span><span class="sxs-lookup"><span data-stu-id="3ee32-215">False</span></span>        |
| <span data-ttu-id="3ee32-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ee32-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ee32-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3ee32-217">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="3ee32-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ee32-218">Range-Lower</span></span>            | <span data-ttu-id="3ee32-219">0</span><span class="sxs-lookup"><span data-stu-id="3ee32-219">0</span></span>            |
| <span data-ttu-id="3ee32-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ee32-220">Range-Upper</span></span>            | <span data-ttu-id="3ee32-221">40</span><span class="sxs-lookup"><span data-stu-id="3ee32-221">40</span></span>           |
| <span data-ttu-id="3ee32-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ee32-222">Search-Flags</span></span>           | <span data-ttu-id="3ee32-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ee32-223">0x00000000</span></span>   |
| <span data-ttu-id="3ee32-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ee32-224">System-Flags</span></span>           | <span data-ttu-id="3ee32-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ee32-225">0x00000010</span></span>   |
| <span data-ttu-id="3ee32-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3ee32-226">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="3ee32-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3ee32-227">Windows Server 2012</span></span>



| <span data-ttu-id="3ee32-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3ee32-228">Entry</span></span> | <span data-ttu-id="3ee32-229">Wert</span><span class="sxs-lookup"><span data-stu-id="3ee32-229">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="3ee32-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3ee32-230">Link-Id</span></span>                | \-           |
| <span data-ttu-id="3ee32-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ee32-231">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="3ee32-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ee32-232">System-Only</span></span>            | <span data-ttu-id="3ee32-233">False</span><span class="sxs-lookup"><span data-stu-id="3ee32-233">False</span></span>        |
| <span data-ttu-id="3ee32-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3ee32-234">Is-Single-Valued</span></span>       | <span data-ttu-id="3ee32-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="3ee32-235">True</span></span>         |
| <span data-ttu-id="3ee32-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3ee32-236">Is Indexed</span></span>             | <span data-ttu-id="3ee32-237">False</span><span class="sxs-lookup"><span data-stu-id="3ee32-237">False</span></span>        |
| <span data-ttu-id="3ee32-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3ee32-238">In Global Catalog</span></span>      | <span data-ttu-id="3ee32-239">False</span><span class="sxs-lookup"><span data-stu-id="3ee32-239">False</span></span>        |
| <span data-ttu-id="3ee32-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ee32-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ee32-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3ee32-241">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="3ee32-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ee32-242">Range-Lower</span></span>            | <span data-ttu-id="3ee32-243">0</span><span class="sxs-lookup"><span data-stu-id="3ee32-243">0</span></span>            |
| <span data-ttu-id="3ee32-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ee32-244">Range-Upper</span></span>            | <span data-ttu-id="3ee32-245">40</span><span class="sxs-lookup"><span data-stu-id="3ee32-245">40</span></span>           |
| <span data-ttu-id="3ee32-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ee32-246">Search-Flags</span></span>           | <span data-ttu-id="3ee32-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ee32-247">0x00000000</span></span>   |
| <span data-ttu-id="3ee32-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ee32-248">System-Flags</span></span>           | <span data-ttu-id="3ee32-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ee32-249">0x00000010</span></span>   |
| <span data-ttu-id="3ee32-250">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3ee32-250">Classes used in</span></span>        | \-           |



 

 




