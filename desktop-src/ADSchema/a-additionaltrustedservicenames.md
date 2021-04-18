---
title: Zusätzliches-Trusted-Service-names-Attribut
description: Eine Liste der Dienste in der Domäne, die als vertrauenswürdig eingestuft werden können. Wird nicht von AD verwendet.
ms.assetid: 0c574a99-4036-408b-807c-b4b3394624c7
ms.tgt_platform: multiple
keywords:
- AD-Schema für zusätzliches-Trusted-Service-names-Attribut
- additionaltreuhändservicenames-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Additional-Trusted-Service-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8066190082cfe0f1bbb8825768ad135090a7a4f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106340055"
---
# <a name="additional-trusted-service-names-attribute"></a><span data-ttu-id="d7f6e-106">Zusätzliches-Trusted-Service-names-Attribut</span><span class="sxs-lookup"><span data-stu-id="d7f6e-106">Additional-Trusted-Service-Names attribute</span></span>

<span data-ttu-id="d7f6e-107">Eine Liste der Dienste in der Domäne, die als vertrauenswürdig eingestuft werden können.</span><span class="sxs-lookup"><span data-stu-id="d7f6e-107">A list of services in the domain that can be trusted.</span></span> <span data-ttu-id="d7f6e-108">Wird nicht von AD verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7f6e-108">Not used by AD.</span></span>



| <span data-ttu-id="d7f6e-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d7f6e-109">Entry</span></span> | <span data-ttu-id="d7f6e-110">Wert</span><span class="sxs-lookup"><span data-stu-id="d7f6e-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d7f6e-111">CN</span><span class="sxs-lookup"><span data-stu-id="d7f6e-111">CN</span></span>                | <span data-ttu-id="d7f6e-112">Zusätzliche-vertrauenswürdige Dienst-Namen</span><span class="sxs-lookup"><span data-stu-id="d7f6e-112">Additional-Trusted-Service-Names</span></span>            |
| <span data-ttu-id="d7f6e-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d7f6e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d7f6e-114">additionaltreuhändservicenames</span><span class="sxs-lookup"><span data-stu-id="d7f6e-114">additionalTrustedServiceNames</span></span>               |
| <span data-ttu-id="d7f6e-115">Size</span><span class="sxs-lookup"><span data-stu-id="d7f6e-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="d7f6e-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d7f6e-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="d7f6e-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="d7f6e-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="d7f6e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d7f6e-118">Attribute-Id</span></span>      | <span data-ttu-id="d7f6e-119">1.2.840.113556.1.4.889</span><span class="sxs-lookup"><span data-stu-id="d7f6e-119">1.2.840.113556.1.4.889</span></span>                      |
| <span data-ttu-id="d7f6e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d7f6e-120">System-Id-Guid</span></span>    | <span data-ttu-id="d7f6e-121">032160be-9824-11d1-aec0-0000e80367c1</span><span class="sxs-lookup"><span data-stu-id="d7f6e-121">032160be-9824-11d1-aec0-0000f80367c1</span></span>        |
| <span data-ttu-id="d7f6e-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7f6e-122">Syntax</span></span>            | [<span data-ttu-id="d7f6e-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d7f6e-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d7f6e-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="d7f6e-124">Implementations</span></span>

-   [<span data-ttu-id="d7f6e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d7f6e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d7f6e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d7f6e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d7f6e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d7f6e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d7f6e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d7f6e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d7f6e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d7f6e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d7f6e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d7f6e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d7f6e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d7f6e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d7f6e-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d7f6e-132">Entry</span></span> | <span data-ttu-id="d7f6e-133">Wert</span><span class="sxs-lookup"><span data-stu-id="d7f6e-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d7f6e-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d7f6e-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d7f6e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7f6e-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d7f6e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7f6e-136">System-Only</span></span>            | <span data-ttu-id="d7f6e-137">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-137">False</span></span>                                                |
| <span data-ttu-id="d7f6e-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d7f6e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d7f6e-139">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-139">False</span></span>                                                |
| <span data-ttu-id="d7f6e-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d7f6e-140">Is Indexed</span></span>             | <span data-ttu-id="d7f6e-141">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-141">False</span></span>                                                |
| <span data-ttu-id="d7f6e-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d7f6e-142">In Global Catalog</span></span>      | <span data-ttu-id="d7f6e-143">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-143">False</span></span>                                                |
| <span data-ttu-id="d7f6e-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d7f6e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7f6e-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d7f6e-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d7f6e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7f6e-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d7f6e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7f6e-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d7f6e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7f6e-148">Search-Flags</span></span>           | <span data-ttu-id="d7f6e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7f6e-149">0x00000000</span></span>                                           |
| <span data-ttu-id="d7f6e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7f6e-150">System-Flags</span></span>           | <span data-ttu-id="d7f6e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7f6e-151">0x00000010</span></span>                                           |
| <span data-ttu-id="d7f6e-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d7f6e-152">Classes used in</span></span>        | [<span data-ttu-id="d7f6e-153">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="d7f6e-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d7f6e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d7f6e-154">Windows Server 2003</span></span>



| <span data-ttu-id="d7f6e-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d7f6e-155">Entry</span></span> | <span data-ttu-id="d7f6e-156">Wert</span><span class="sxs-lookup"><span data-stu-id="d7f6e-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d7f6e-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d7f6e-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d7f6e-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7f6e-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d7f6e-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7f6e-159">System-Only</span></span>            | <span data-ttu-id="d7f6e-160">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-160">False</span></span>                                                |
| <span data-ttu-id="d7f6e-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d7f6e-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d7f6e-162">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-162">False</span></span>                                                |
| <span data-ttu-id="d7f6e-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d7f6e-163">Is Indexed</span></span>             | <span data-ttu-id="d7f6e-164">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-164">False</span></span>                                                |
| <span data-ttu-id="d7f6e-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d7f6e-165">In Global Catalog</span></span>      | <span data-ttu-id="d7f6e-166">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-166">False</span></span>                                                |
| <span data-ttu-id="d7f6e-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d7f6e-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7f6e-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d7f6e-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d7f6e-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7f6e-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d7f6e-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7f6e-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d7f6e-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7f6e-171">Search-Flags</span></span>           | <span data-ttu-id="d7f6e-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7f6e-172">0x00000000</span></span>                                           |
| <span data-ttu-id="d7f6e-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7f6e-173">System-Flags</span></span>           | <span data-ttu-id="d7f6e-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7f6e-174">0x00000010</span></span>                                           |
| <span data-ttu-id="d7f6e-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d7f6e-175">Classes used in</span></span>        | [<span data-ttu-id="d7f6e-176">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="d7f6e-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d7f6e-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d7f6e-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d7f6e-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d7f6e-178">Entry</span></span> | <span data-ttu-id="d7f6e-179">Wert</span><span class="sxs-lookup"><span data-stu-id="d7f6e-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d7f6e-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d7f6e-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d7f6e-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7f6e-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d7f6e-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7f6e-182">System-Only</span></span>            | <span data-ttu-id="d7f6e-183">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-183">False</span></span>                                                |
| <span data-ttu-id="d7f6e-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d7f6e-184">Is-Single-Valued</span></span>       | <span data-ttu-id="d7f6e-185">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-185">False</span></span>                                                |
| <span data-ttu-id="d7f6e-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d7f6e-186">Is Indexed</span></span>             | <span data-ttu-id="d7f6e-187">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-187">False</span></span>                                                |
| <span data-ttu-id="d7f6e-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d7f6e-188">In Global Catalog</span></span>      | <span data-ttu-id="d7f6e-189">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-189">False</span></span>                                                |
| <span data-ttu-id="d7f6e-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d7f6e-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7f6e-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d7f6e-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d7f6e-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7f6e-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d7f6e-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7f6e-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d7f6e-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7f6e-194">Search-Flags</span></span>           | <span data-ttu-id="d7f6e-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7f6e-195">0x00000000</span></span>                                           |
| <span data-ttu-id="d7f6e-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7f6e-196">System-Flags</span></span>           | <span data-ttu-id="d7f6e-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7f6e-197">0x00000010</span></span>                                           |
| <span data-ttu-id="d7f6e-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d7f6e-198">Classes used in</span></span>        | [<span data-ttu-id="d7f6e-199">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="d7f6e-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d7f6e-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7f6e-200">Windows Server 2008</span></span>



| <span data-ttu-id="d7f6e-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d7f6e-201">Entry</span></span> | <span data-ttu-id="d7f6e-202">Wert</span><span class="sxs-lookup"><span data-stu-id="d7f6e-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d7f6e-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d7f6e-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d7f6e-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7f6e-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d7f6e-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7f6e-205">System-Only</span></span>            | <span data-ttu-id="d7f6e-206">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-206">False</span></span>                                                |
| <span data-ttu-id="d7f6e-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d7f6e-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d7f6e-208">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-208">False</span></span>                                                |
| <span data-ttu-id="d7f6e-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d7f6e-209">Is Indexed</span></span>             | <span data-ttu-id="d7f6e-210">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-210">False</span></span>                                                |
| <span data-ttu-id="d7f6e-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d7f6e-211">In Global Catalog</span></span>      | <span data-ttu-id="d7f6e-212">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-212">False</span></span>                                                |
| <span data-ttu-id="d7f6e-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d7f6e-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7f6e-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d7f6e-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d7f6e-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7f6e-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d7f6e-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7f6e-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d7f6e-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7f6e-217">Search-Flags</span></span>           | <span data-ttu-id="d7f6e-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7f6e-218">0x00000000</span></span>                                           |
| <span data-ttu-id="d7f6e-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7f6e-219">System-Flags</span></span>           | <span data-ttu-id="d7f6e-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7f6e-220">0x00000010</span></span>                                           |
| <span data-ttu-id="d7f6e-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d7f6e-221">Classes used in</span></span>        | [<span data-ttu-id="d7f6e-222">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="d7f6e-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d7f6e-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d7f6e-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d7f6e-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d7f6e-224">Entry</span></span> | <span data-ttu-id="d7f6e-225">Wert</span><span class="sxs-lookup"><span data-stu-id="d7f6e-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d7f6e-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d7f6e-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d7f6e-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7f6e-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d7f6e-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7f6e-228">System-Only</span></span>            | <span data-ttu-id="d7f6e-229">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-229">False</span></span>                                                |
| <span data-ttu-id="d7f6e-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d7f6e-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d7f6e-231">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-231">False</span></span>                                                |
| <span data-ttu-id="d7f6e-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d7f6e-232">Is Indexed</span></span>             | <span data-ttu-id="d7f6e-233">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-233">False</span></span>                                                |
| <span data-ttu-id="d7f6e-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d7f6e-234">In Global Catalog</span></span>      | <span data-ttu-id="d7f6e-235">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-235">False</span></span>                                                |
| <span data-ttu-id="d7f6e-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d7f6e-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7f6e-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d7f6e-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d7f6e-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7f6e-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d7f6e-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7f6e-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d7f6e-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7f6e-240">Search-Flags</span></span>           | <span data-ttu-id="d7f6e-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7f6e-241">0x00000000</span></span>                                           |
| <span data-ttu-id="d7f6e-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7f6e-242">System-Flags</span></span>           | <span data-ttu-id="d7f6e-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7f6e-243">0x00000010</span></span>                                           |
| <span data-ttu-id="d7f6e-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d7f6e-244">Classes used in</span></span>        | [<span data-ttu-id="d7f6e-245">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="d7f6e-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d7f6e-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d7f6e-246">Windows Server 2012</span></span>



| <span data-ttu-id="d7f6e-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d7f6e-247">Entry</span></span> | <span data-ttu-id="d7f6e-248">Wert</span><span class="sxs-lookup"><span data-stu-id="d7f6e-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d7f6e-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d7f6e-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d7f6e-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7f6e-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d7f6e-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7f6e-251">System-Only</span></span>            | <span data-ttu-id="d7f6e-252">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-252">False</span></span>                                                |
| <span data-ttu-id="d7f6e-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d7f6e-253">Is-Single-Valued</span></span>       | <span data-ttu-id="d7f6e-254">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-254">False</span></span>                                                |
| <span data-ttu-id="d7f6e-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d7f6e-255">Is Indexed</span></span>             | <span data-ttu-id="d7f6e-256">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-256">False</span></span>                                                |
| <span data-ttu-id="d7f6e-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d7f6e-257">In Global Catalog</span></span>      | <span data-ttu-id="d7f6e-258">False</span><span class="sxs-lookup"><span data-stu-id="d7f6e-258">False</span></span>                                                |
| <span data-ttu-id="d7f6e-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d7f6e-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7f6e-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d7f6e-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d7f6e-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7f6e-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d7f6e-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7f6e-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d7f6e-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7f6e-263">Search-Flags</span></span>           | <span data-ttu-id="d7f6e-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7f6e-264">0x00000000</span></span>                                           |
| <span data-ttu-id="d7f6e-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7f6e-265">System-Flags</span></span>           | <span data-ttu-id="d7f6e-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7f6e-266">0x00000010</span></span>                                           |
| <span data-ttu-id="d7f6e-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d7f6e-267">Classes used in</span></span>        | [<span data-ttu-id="d7f6e-268">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="d7f6e-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





