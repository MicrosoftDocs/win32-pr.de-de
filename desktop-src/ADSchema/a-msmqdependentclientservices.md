---
title: MSMQ-abhängige-Client-Services-Attribut
description: Gibt an, ob MSMQ, das auf diesem Computer installiert ist, MSMQ-abhängige Client Dienste bereitstellt.
ms.assetid: 6f16db7f-f328-4fe2-9ecc-b40c1c845064
ms.tgt_platform: multiple
keywords:
- AD-Schema für MSMQ-abhängige Client Dienst Attribute
- AD-Schema des msmqdependentclientservices-Attributs
topic_type:
- apiref
api_name:
- MSMQ-Dependent-Client-Services
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1ea2ccae62904fd4fc25e9ffaa5f93f2de0ab9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957492"
---
# <a name="msmq-dependent-client-services-attribute"></a><span data-ttu-id="8e11d-105">MSMQ-abhängige-Client-Services-Attribut</span><span class="sxs-lookup"><span data-stu-id="8e11d-105">MSMQ-Dependent-Client-Services attribute</span></span>

<span data-ttu-id="8e11d-106">Gibt an, ob MSMQ, das auf diesem Computer installiert ist, MSMQ-abhängige Client Dienste bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8e11d-106">Indicates whether the MSMQ installed on this computer provides MSMQ dependent client services.</span></span>



| <span data-ttu-id="8e11d-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e11d-107">Entry</span></span> | <span data-ttu-id="8e11d-108">Wert</span><span class="sxs-lookup"><span data-stu-id="8e11d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8e11d-109">CN</span><span class="sxs-lookup"><span data-stu-id="8e11d-109">CN</span></span>                | <span data-ttu-id="8e11d-110">MSMQ-abhängige Client Dienste</span><span class="sxs-lookup"><span data-stu-id="8e11d-110">MSMQ-Dependent-Client-Services</span></span>       |
| <span data-ttu-id="8e11d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8e11d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8e11d-112">msmqdependentclientservices</span><span class="sxs-lookup"><span data-stu-id="8e11d-112">mSMQDependentClientServices</span></span>          |
| <span data-ttu-id="8e11d-113">Size</span><span class="sxs-lookup"><span data-stu-id="8e11d-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="8e11d-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="8e11d-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="8e11d-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="8e11d-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8e11d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8e11d-116">Attribute-Id</span></span>      | <span data-ttu-id="8e11d-117">1.2.840.113556.1.4.1226</span><span class="sxs-lookup"><span data-stu-id="8e11d-117">1.2.840.113556.1.4.1226</span></span>              |
| <span data-ttu-id="8e11d-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8e11d-118">System-Id-Guid</span></span>    | <span data-ttu-id="8e11d-119">2df90d76-009F -11d2-aa4c-00c04f d83a</span><span class="sxs-lookup"><span data-stu-id="8e11d-119">2df90d76-009f-11d2-aa4c-00c04fd7d83a</span></span> |
| <span data-ttu-id="8e11d-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e11d-120">Syntax</span></span>            | [<span data-ttu-id="8e11d-121">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="8e11d-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="8e11d-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="8e11d-122">Implementations</span></span>

-   [<span data-ttu-id="8e11d-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8e11d-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8e11d-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8e11d-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8e11d-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8e11d-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8e11d-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8e11d-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8e11d-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8e11d-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8e11d-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8e11d-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8e11d-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8e11d-129">Windows 2000 Server</span></span>



| <span data-ttu-id="8e11d-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e11d-130">Entry</span></span> | <span data-ttu-id="8e11d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="8e11d-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8e11d-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8e11d-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8e11d-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e11d-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8e11d-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e11d-134">System-Only</span></span>            | <span data-ttu-id="8e11d-135">False</span><span class="sxs-lookup"><span data-stu-id="8e11d-135">False</span></span>                                                        |
| <span data-ttu-id="8e11d-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8e11d-136">Is-Single-Valued</span></span>       | <span data-ttu-id="8e11d-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e11d-137">True</span></span>                                                         |
| <span data-ttu-id="8e11d-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8e11d-138">Is Indexed</span></span>             | <span data-ttu-id="8e11d-139">False</span><span class="sxs-lookup"><span data-stu-id="8e11d-139">False</span></span>                                                        |
| <span data-ttu-id="8e11d-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8e11d-140">In Global Catalog</span></span>      | <span data-ttu-id="8e11d-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e11d-141">True</span></span>                                                         |
| <span data-ttu-id="8e11d-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8e11d-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e11d-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8e11d-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8e11d-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e11d-144">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8e11d-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e11d-145">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8e11d-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e11d-146">Search-Flags</span></span>           | <span data-ttu-id="8e11d-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e11d-147">0x00000000</span></span>                                                   |
| <span data-ttu-id="8e11d-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e11d-148">System-Flags</span></span>           | <span data-ttu-id="8e11d-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e11d-149">0x00000010</span></span>                                                   |
| <span data-ttu-id="8e11d-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8e11d-150">Classes used in</span></span>        | [<span data-ttu-id="8e11d-151">**MSMQ-Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="8e11d-151">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8e11d-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8e11d-152">Windows Server 2003</span></span>



| <span data-ttu-id="8e11d-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e11d-153">Entry</span></span> | <span data-ttu-id="8e11d-154">Wert</span><span class="sxs-lookup"><span data-stu-id="8e11d-154">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8e11d-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8e11d-155">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8e11d-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e11d-156">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8e11d-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e11d-157">System-Only</span></span>            | <span data-ttu-id="8e11d-158">False</span><span class="sxs-lookup"><span data-stu-id="8e11d-158">False</span></span>                                                        |
| <span data-ttu-id="8e11d-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8e11d-159">Is-Single-Valued</span></span>       | <span data-ttu-id="8e11d-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e11d-160">True</span></span>                                                         |
| <span data-ttu-id="8e11d-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8e11d-161">Is Indexed</span></span>             | <span data-ttu-id="8e11d-162">False</span><span class="sxs-lookup"><span data-stu-id="8e11d-162">False</span></span>                                                        |
| <span data-ttu-id="8e11d-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8e11d-163">In Global Catalog</span></span>      | <span data-ttu-id="8e11d-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e11d-164">True</span></span>                                                         |
| <span data-ttu-id="8e11d-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8e11d-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e11d-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8e11d-166">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8e11d-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e11d-167">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8e11d-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e11d-168">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8e11d-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e11d-169">Search-Flags</span></span>           | <span data-ttu-id="8e11d-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e11d-170">0x00000000</span></span>                                                   |
| <span data-ttu-id="8e11d-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e11d-171">System-Flags</span></span>           | <span data-ttu-id="8e11d-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e11d-172">0x00000010</span></span>                                                   |
| <span data-ttu-id="8e11d-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8e11d-173">Classes used in</span></span>        | [<span data-ttu-id="8e11d-174">**MSMQ-Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="8e11d-174">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8e11d-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8e11d-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8e11d-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e11d-176">Entry</span></span> | <span data-ttu-id="8e11d-177">Wert</span><span class="sxs-lookup"><span data-stu-id="8e11d-177">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8e11d-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8e11d-178">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8e11d-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e11d-179">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8e11d-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e11d-180">System-Only</span></span>            | <span data-ttu-id="8e11d-181">False</span><span class="sxs-lookup"><span data-stu-id="8e11d-181">False</span></span>                                                        |
| <span data-ttu-id="8e11d-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8e11d-182">Is-Single-Valued</span></span>       | <span data-ttu-id="8e11d-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e11d-183">True</span></span>                                                         |
| <span data-ttu-id="8e11d-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8e11d-184">Is Indexed</span></span>             | <span data-ttu-id="8e11d-185">False</span><span class="sxs-lookup"><span data-stu-id="8e11d-185">False</span></span>                                                        |
| <span data-ttu-id="8e11d-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8e11d-186">In Global Catalog</span></span>      | <span data-ttu-id="8e11d-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e11d-187">True</span></span>                                                         |
| <span data-ttu-id="8e11d-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8e11d-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e11d-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8e11d-189">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8e11d-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e11d-190">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8e11d-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e11d-191">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8e11d-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e11d-192">Search-Flags</span></span>           | <span data-ttu-id="8e11d-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e11d-193">0x00000000</span></span>                                                   |
| <span data-ttu-id="8e11d-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e11d-194">System-Flags</span></span>           | <span data-ttu-id="8e11d-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e11d-195">0x00000010</span></span>                                                   |
| <span data-ttu-id="8e11d-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8e11d-196">Classes used in</span></span>        | [<span data-ttu-id="8e11d-197">**MSMQ-Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="8e11d-197">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8e11d-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e11d-198">Windows Server 2008</span></span>



| <span data-ttu-id="8e11d-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e11d-199">Entry</span></span> | <span data-ttu-id="8e11d-200">Wert</span><span class="sxs-lookup"><span data-stu-id="8e11d-200">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8e11d-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8e11d-201">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8e11d-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e11d-202">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8e11d-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e11d-203">System-Only</span></span>            | <span data-ttu-id="8e11d-204">False</span><span class="sxs-lookup"><span data-stu-id="8e11d-204">False</span></span>                                                        |
| <span data-ttu-id="8e11d-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8e11d-205">Is-Single-Valued</span></span>       | <span data-ttu-id="8e11d-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e11d-206">True</span></span>                                                         |
| <span data-ttu-id="8e11d-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8e11d-207">Is Indexed</span></span>             | <span data-ttu-id="8e11d-208">False</span><span class="sxs-lookup"><span data-stu-id="8e11d-208">False</span></span>                                                        |
| <span data-ttu-id="8e11d-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8e11d-209">In Global Catalog</span></span>      | <span data-ttu-id="8e11d-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e11d-210">True</span></span>                                                         |
| <span data-ttu-id="8e11d-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8e11d-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e11d-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8e11d-212">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8e11d-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e11d-213">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8e11d-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e11d-214">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8e11d-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e11d-215">Search-Flags</span></span>           | <span data-ttu-id="8e11d-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e11d-216">0x00000000</span></span>                                                   |
| <span data-ttu-id="8e11d-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e11d-217">System-Flags</span></span>           | <span data-ttu-id="8e11d-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e11d-218">0x00000010</span></span>                                                   |
| <span data-ttu-id="8e11d-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8e11d-219">Classes used in</span></span>        | [<span data-ttu-id="8e11d-220">**MSMQ-Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="8e11d-220">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8e11d-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8e11d-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8e11d-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e11d-222">Entry</span></span> | <span data-ttu-id="8e11d-223">Wert</span><span class="sxs-lookup"><span data-stu-id="8e11d-223">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8e11d-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8e11d-224">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8e11d-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e11d-225">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8e11d-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e11d-226">System-Only</span></span>            | <span data-ttu-id="8e11d-227">False</span><span class="sxs-lookup"><span data-stu-id="8e11d-227">False</span></span>                                                        |
| <span data-ttu-id="8e11d-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8e11d-228">Is-Single-Valued</span></span>       | <span data-ttu-id="8e11d-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e11d-229">True</span></span>                                                         |
| <span data-ttu-id="8e11d-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8e11d-230">Is Indexed</span></span>             | <span data-ttu-id="8e11d-231">False</span><span class="sxs-lookup"><span data-stu-id="8e11d-231">False</span></span>                                                        |
| <span data-ttu-id="8e11d-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8e11d-232">In Global Catalog</span></span>      | <span data-ttu-id="8e11d-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e11d-233">True</span></span>                                                         |
| <span data-ttu-id="8e11d-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8e11d-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e11d-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8e11d-235">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8e11d-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e11d-236">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8e11d-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e11d-237">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8e11d-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e11d-238">Search-Flags</span></span>           | <span data-ttu-id="8e11d-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e11d-239">0x00000000</span></span>                                                   |
| <span data-ttu-id="8e11d-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e11d-240">System-Flags</span></span>           | <span data-ttu-id="8e11d-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e11d-241">0x00000010</span></span>                                                   |
| <span data-ttu-id="8e11d-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8e11d-242">Classes used in</span></span>        | [<span data-ttu-id="8e11d-243">**MSMQ-Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="8e11d-243">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8e11d-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8e11d-244">Windows Server 2012</span></span>



| <span data-ttu-id="8e11d-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e11d-245">Entry</span></span> | <span data-ttu-id="8e11d-246">Wert</span><span class="sxs-lookup"><span data-stu-id="8e11d-246">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8e11d-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8e11d-247">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8e11d-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e11d-248">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8e11d-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e11d-249">System-Only</span></span>            | <span data-ttu-id="8e11d-250">False</span><span class="sxs-lookup"><span data-stu-id="8e11d-250">False</span></span>                                                        |
| <span data-ttu-id="8e11d-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8e11d-251">Is-Single-Valued</span></span>       | <span data-ttu-id="8e11d-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e11d-252">True</span></span>                                                         |
| <span data-ttu-id="8e11d-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8e11d-253">Is Indexed</span></span>             | <span data-ttu-id="8e11d-254">False</span><span class="sxs-lookup"><span data-stu-id="8e11d-254">False</span></span>                                                        |
| <span data-ttu-id="8e11d-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8e11d-255">In Global Catalog</span></span>      | <span data-ttu-id="8e11d-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="8e11d-256">True</span></span>                                                         |
| <span data-ttu-id="8e11d-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8e11d-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e11d-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8e11d-258">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8e11d-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e11d-259">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8e11d-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e11d-260">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8e11d-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e11d-261">Search-Flags</span></span>           | <span data-ttu-id="8e11d-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e11d-262">0x00000000</span></span>                                                   |
| <span data-ttu-id="8e11d-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e11d-263">System-Flags</span></span>           | <span data-ttu-id="8e11d-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e11d-264">0x00000010</span></span>                                                   |
| <span data-ttu-id="8e11d-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8e11d-265">Classes used in</span></span>        | [<span data-ttu-id="8e11d-266">**MSMQ-Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="8e11d-266">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



 

 





