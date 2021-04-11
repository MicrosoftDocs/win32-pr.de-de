---
title: ACS-Identity-Name-Attribut
description: Dieses Attribut enthält den DN eines Benutzers oder einer Organisationseinheit und ist die Identität eines Benutzers oder einer Gruppe von Benutzern, auf die diese QoS-Richtlinie angewendet wird.
ms.assetid: 00e6e2bd-aec8-426f-b89e-0661c15cfd46
ms.tgt_platform: multiple
keywords:
- AD-Schema für das ACS-Identitäts Name-Attribut
- acsidentityname-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ACS-Identity-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33ef1db92b908ef8474dfb125aca678d3c22d09f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123223"
---
# <a name="acs-identity-name-attribute"></a><span data-ttu-id="8aa0a-105">ACS-Identity-Name-Attribut</span><span class="sxs-lookup"><span data-stu-id="8aa0a-105">ACS-Identity-Name attribute</span></span>

<span data-ttu-id="8aa0a-106">Dieses Attribut enthält den DN eines Benutzers oder einer Organisationseinheit und ist die Identität eines Benutzers oder einer Gruppe von Benutzern, auf die diese QoS-Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8aa0a-106">This attribute contains the DN of a user or OU and is the identity of a user or a group of users to which this QoS policy applies.</span></span>



| <span data-ttu-id="8aa0a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8aa0a-107">Entry</span></span> | <span data-ttu-id="8aa0a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="8aa0a-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="8aa0a-109">CN</span><span class="sxs-lookup"><span data-stu-id="8aa0a-109">CN</span></span>                | <span data-ttu-id="8aa0a-110">ACS-Identitäts Name</span><span class="sxs-lookup"><span data-stu-id="8aa0a-110">ACS-Identity-Name</span></span>                           |
| <span data-ttu-id="8aa0a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8aa0a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8aa0a-112">acsidentityname</span><span class="sxs-lookup"><span data-stu-id="8aa0a-112">aCSIdentityName</span></span>                             |
| <span data-ttu-id="8aa0a-113">Size</span><span class="sxs-lookup"><span data-stu-id="8aa0a-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="8aa0a-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="8aa0a-114">Update Privilege</span></span>  | <span data-ttu-id="8aa0a-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="8aa0a-115">Domain administrator</span></span>                        |
| <span data-ttu-id="8aa0a-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="8aa0a-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="8aa0a-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8aa0a-117">Attribute-Id</span></span>      | <span data-ttu-id="8aa0a-118">1.2.840.113556.1.4.784</span><span class="sxs-lookup"><span data-stu-id="8aa0a-118">1.2.840.113556.1.4.784</span></span>                      |
| <span data-ttu-id="8aa0a-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8aa0a-119">System-Id-Guid</span></span>    | <span data-ttu-id="8aa0a-120">dab029b6-ddf7-11d1-90a5-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="8aa0a-120">dab029b6-ddf7-11d1-90a5-00c04fd91ab1</span></span>        |
| <span data-ttu-id="8aa0a-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="8aa0a-121">Syntax</span></span>            | [<span data-ttu-id="8aa0a-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="8aa0a-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="8aa0a-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="8aa0a-123">Implementations</span></span>

-   [<span data-ttu-id="8aa0a-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8aa0a-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8aa0a-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8aa0a-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8aa0a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8aa0a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8aa0a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8aa0a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8aa0a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8aa0a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8aa0a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8aa0a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8aa0a-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8aa0a-130">Windows 2000 Server</span></span>



| <span data-ttu-id="8aa0a-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8aa0a-131">Entry</span></span> | <span data-ttu-id="8aa0a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="8aa0a-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8aa0a-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8aa0a-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8aa0a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8aa0a-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8aa0a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="8aa0a-135">System-Only</span></span>            | <span data-ttu-id="8aa0a-136">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-136">False</span></span>                                        |
| <span data-ttu-id="8aa0a-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8aa0a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="8aa0a-138">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-138">False</span></span>                                        |
| <span data-ttu-id="8aa0a-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8aa0a-139">Is Indexed</span></span>             | <span data-ttu-id="8aa0a-140">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-140">False</span></span>                                        |
| <span data-ttu-id="8aa0a-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8aa0a-141">In Global Catalog</span></span>      | <span data-ttu-id="8aa0a-142">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-142">False</span></span>                                        |
| <span data-ttu-id="8aa0a-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8aa0a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="8aa0a-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8aa0a-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8aa0a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8aa0a-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8aa0a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8aa0a-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8aa0a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8aa0a-147">Search-Flags</span></span>           | <span data-ttu-id="8aa0a-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8aa0a-148">0x00000000</span></span>                                   |
| <span data-ttu-id="8aa0a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8aa0a-149">System-Flags</span></span>           | <span data-ttu-id="8aa0a-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8aa0a-150">0x00000010</span></span>                                   |
| <span data-ttu-id="8aa0a-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8aa0a-151">Classes used in</span></span>        | [<span data-ttu-id="8aa0a-152">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="8aa0a-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8aa0a-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8aa0a-153">Windows Server 2003</span></span>



| <span data-ttu-id="8aa0a-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8aa0a-154">Entry</span></span> | <span data-ttu-id="8aa0a-155">Wert</span><span class="sxs-lookup"><span data-stu-id="8aa0a-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8aa0a-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8aa0a-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8aa0a-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8aa0a-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8aa0a-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="8aa0a-158">System-Only</span></span>            | <span data-ttu-id="8aa0a-159">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-159">False</span></span>                                        |
| <span data-ttu-id="8aa0a-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8aa0a-160">Is-Single-Valued</span></span>       | <span data-ttu-id="8aa0a-161">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-161">False</span></span>                                        |
| <span data-ttu-id="8aa0a-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8aa0a-162">Is Indexed</span></span>             | <span data-ttu-id="8aa0a-163">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-163">False</span></span>                                        |
| <span data-ttu-id="8aa0a-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8aa0a-164">In Global Catalog</span></span>      | <span data-ttu-id="8aa0a-165">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-165">False</span></span>                                        |
| <span data-ttu-id="8aa0a-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8aa0a-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="8aa0a-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8aa0a-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8aa0a-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8aa0a-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8aa0a-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8aa0a-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8aa0a-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8aa0a-170">Search-Flags</span></span>           | <span data-ttu-id="8aa0a-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8aa0a-171">0x00000000</span></span>                                   |
| <span data-ttu-id="8aa0a-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8aa0a-172">System-Flags</span></span>           | <span data-ttu-id="8aa0a-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8aa0a-173">0x00000010</span></span>                                   |
| <span data-ttu-id="8aa0a-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8aa0a-174">Classes used in</span></span>        | [<span data-ttu-id="8aa0a-175">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="8aa0a-175">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8aa0a-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8aa0a-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8aa0a-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8aa0a-177">Entry</span></span> | <span data-ttu-id="8aa0a-178">Wert</span><span class="sxs-lookup"><span data-stu-id="8aa0a-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8aa0a-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8aa0a-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8aa0a-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8aa0a-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8aa0a-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="8aa0a-181">System-Only</span></span>            | <span data-ttu-id="8aa0a-182">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-182">False</span></span>                                        |
| <span data-ttu-id="8aa0a-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8aa0a-183">Is-Single-Valued</span></span>       | <span data-ttu-id="8aa0a-184">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-184">False</span></span>                                        |
| <span data-ttu-id="8aa0a-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8aa0a-185">Is Indexed</span></span>             | <span data-ttu-id="8aa0a-186">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-186">False</span></span>                                        |
| <span data-ttu-id="8aa0a-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8aa0a-187">In Global Catalog</span></span>      | <span data-ttu-id="8aa0a-188">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-188">False</span></span>                                        |
| <span data-ttu-id="8aa0a-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8aa0a-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="8aa0a-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8aa0a-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8aa0a-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8aa0a-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8aa0a-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8aa0a-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8aa0a-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8aa0a-193">Search-Flags</span></span>           | <span data-ttu-id="8aa0a-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8aa0a-194">0x00000000</span></span>                                   |
| <span data-ttu-id="8aa0a-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8aa0a-195">System-Flags</span></span>           | <span data-ttu-id="8aa0a-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8aa0a-196">0x00000010</span></span>                                   |
| <span data-ttu-id="8aa0a-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8aa0a-197">Classes used in</span></span>        | [<span data-ttu-id="8aa0a-198">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="8aa0a-198">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8aa0a-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8aa0a-199">Windows Server 2008</span></span>



| <span data-ttu-id="8aa0a-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8aa0a-200">Entry</span></span> | <span data-ttu-id="8aa0a-201">Wert</span><span class="sxs-lookup"><span data-stu-id="8aa0a-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8aa0a-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8aa0a-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8aa0a-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8aa0a-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8aa0a-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="8aa0a-204">System-Only</span></span>            | <span data-ttu-id="8aa0a-205">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-205">False</span></span>                                        |
| <span data-ttu-id="8aa0a-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8aa0a-206">Is-Single-Valued</span></span>       | <span data-ttu-id="8aa0a-207">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-207">False</span></span>                                        |
| <span data-ttu-id="8aa0a-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8aa0a-208">Is Indexed</span></span>             | <span data-ttu-id="8aa0a-209">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-209">False</span></span>                                        |
| <span data-ttu-id="8aa0a-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8aa0a-210">In Global Catalog</span></span>      | <span data-ttu-id="8aa0a-211">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-211">False</span></span>                                        |
| <span data-ttu-id="8aa0a-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8aa0a-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="8aa0a-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8aa0a-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8aa0a-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8aa0a-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8aa0a-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8aa0a-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8aa0a-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8aa0a-216">Search-Flags</span></span>           | <span data-ttu-id="8aa0a-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8aa0a-217">0x00000000</span></span>                                   |
| <span data-ttu-id="8aa0a-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8aa0a-218">System-Flags</span></span>           | <span data-ttu-id="8aa0a-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8aa0a-219">0x00000010</span></span>                                   |
| <span data-ttu-id="8aa0a-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8aa0a-220">Classes used in</span></span>        | [<span data-ttu-id="8aa0a-221">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="8aa0a-221">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8aa0a-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8aa0a-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8aa0a-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8aa0a-223">Entry</span></span> | <span data-ttu-id="8aa0a-224">Wert</span><span class="sxs-lookup"><span data-stu-id="8aa0a-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8aa0a-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8aa0a-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8aa0a-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8aa0a-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8aa0a-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="8aa0a-227">System-Only</span></span>            | <span data-ttu-id="8aa0a-228">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-228">False</span></span>                                        |
| <span data-ttu-id="8aa0a-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8aa0a-229">Is-Single-Valued</span></span>       | <span data-ttu-id="8aa0a-230">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-230">False</span></span>                                        |
| <span data-ttu-id="8aa0a-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8aa0a-231">Is Indexed</span></span>             | <span data-ttu-id="8aa0a-232">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-232">False</span></span>                                        |
| <span data-ttu-id="8aa0a-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8aa0a-233">In Global Catalog</span></span>      | <span data-ttu-id="8aa0a-234">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-234">False</span></span>                                        |
| <span data-ttu-id="8aa0a-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8aa0a-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="8aa0a-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8aa0a-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8aa0a-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8aa0a-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8aa0a-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8aa0a-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8aa0a-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8aa0a-239">Search-Flags</span></span>           | <span data-ttu-id="8aa0a-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8aa0a-240">0x00000000</span></span>                                   |
| <span data-ttu-id="8aa0a-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8aa0a-241">System-Flags</span></span>           | <span data-ttu-id="8aa0a-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8aa0a-242">0x00000010</span></span>                                   |
| <span data-ttu-id="8aa0a-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8aa0a-243">Classes used in</span></span>        | [<span data-ttu-id="8aa0a-244">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="8aa0a-244">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8aa0a-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8aa0a-245">Windows Server 2012</span></span>



| <span data-ttu-id="8aa0a-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8aa0a-246">Entry</span></span> | <span data-ttu-id="8aa0a-247">Wert</span><span class="sxs-lookup"><span data-stu-id="8aa0a-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8aa0a-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8aa0a-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8aa0a-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8aa0a-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8aa0a-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="8aa0a-250">System-Only</span></span>            | <span data-ttu-id="8aa0a-251">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-251">False</span></span>                                        |
| <span data-ttu-id="8aa0a-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8aa0a-252">Is-Single-Valued</span></span>       | <span data-ttu-id="8aa0a-253">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-253">False</span></span>                                        |
| <span data-ttu-id="8aa0a-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8aa0a-254">Is Indexed</span></span>             | <span data-ttu-id="8aa0a-255">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-255">False</span></span>                                        |
| <span data-ttu-id="8aa0a-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8aa0a-256">In Global Catalog</span></span>      | <span data-ttu-id="8aa0a-257">False</span><span class="sxs-lookup"><span data-stu-id="8aa0a-257">False</span></span>                                        |
| <span data-ttu-id="8aa0a-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8aa0a-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="8aa0a-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8aa0a-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8aa0a-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8aa0a-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8aa0a-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8aa0a-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8aa0a-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8aa0a-262">Search-Flags</span></span>           | <span data-ttu-id="8aa0a-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8aa0a-263">0x00000000</span></span>                                   |
| <span data-ttu-id="8aa0a-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8aa0a-264">System-Flags</span></span>           | <span data-ttu-id="8aa0a-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8aa0a-265">0x00000010</span></span>                                   |
| <span data-ttu-id="8aa0a-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8aa0a-266">Classes used in</span></span>        | [<span data-ttu-id="8aa0a-267">**ACS-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="8aa0a-267">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





