---
title: Ursprüngliches Authentifizierungs Attribut
description: Enthält Informationen über eine anfängliche eingehende Authentifizierungsanforderung durch einen Client an diesen Server. Diese Anforderung wird dann von diesem Server an den Authentifizierungsserver für die Domäne gesendet.
ms.assetid: d49d45ae-87fe-415d-8110-79b2b321f2b6
ms.tgt_platform: multiple
keywords:
- AD-Schema für das anfängliche auth-eingehende Attribut
- initialauthincoming-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Initial-Auth-Incoming
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 973b00abd5b77b713fc03b5efb3d4cf45b97fc19
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744840"
---
# <a name="initial-auth-incoming-attribute"></a><span data-ttu-id="6c9fc-106">Ursprüngliches Authentifizierungs Attribut</span><span class="sxs-lookup"><span data-stu-id="6c9fc-106">Initial-Auth-Incoming attribute</span></span>

<span data-ttu-id="6c9fc-107">Enthält Informationen über eine anfängliche eingehende Authentifizierungsanforderung durch einen Client an diesen Server.</span><span class="sxs-lookup"><span data-stu-id="6c9fc-107">Contains information about an initial incoming authentication request by a client to this server.</span></span> <span data-ttu-id="6c9fc-108">Diese Anforderung wird dann von diesem Server an den Authentifizierungsserver für die Domäne gesendet.</span><span class="sxs-lookup"><span data-stu-id="6c9fc-108">This request is then sent by this server to the authentication server for the domain.</span></span>



| <span data-ttu-id="6c9fc-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c9fc-109">Entry</span></span> | <span data-ttu-id="6c9fc-110">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9fc-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6c9fc-111">CN</span><span class="sxs-lookup"><span data-stu-id="6c9fc-111">CN</span></span>                | <span data-ttu-id="6c9fc-112">Anfängliche Authentifizierung-eingehende</span><span class="sxs-lookup"><span data-stu-id="6c9fc-112">Initial-Auth-Incoming</span></span>                       |
| <span data-ttu-id="6c9fc-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6c9fc-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6c9fc-114">initialauthincoming</span><span class="sxs-lookup"><span data-stu-id="6c9fc-114">initialAuthIncoming</span></span>                         |
| <span data-ttu-id="6c9fc-115">Size</span><span class="sxs-lookup"><span data-stu-id="6c9fc-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="6c9fc-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="6c9fc-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="6c9fc-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="6c9fc-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="6c9fc-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6c9fc-118">Attribute-Id</span></span>      | <span data-ttu-id="6c9fc-119">1.2.840.113556.1.4.539</span><span class="sxs-lookup"><span data-stu-id="6c9fc-119">1.2.840.113556.1.4.539</span></span>                      |
| <span data-ttu-id="6c9fc-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6c9fc-120">System-Id-Guid</span></span>    | <span data-ttu-id="6c9fc-121">52458023-ca6a-11D0-affinf-0000f 80367c1</span><span class="sxs-lookup"><span data-stu-id="6c9fc-121">52458023-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="6c9fc-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c9fc-122">Syntax</span></span>            | [<span data-ttu-id="6c9fc-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6c9fc-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6c9fc-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="6c9fc-124">Implementations</span></span>

-   [<span data-ttu-id="6c9fc-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6c9fc-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6c9fc-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6c9fc-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6c9fc-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6c9fc-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6c9fc-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6c9fc-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6c9fc-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6c9fc-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6c9fc-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6c9fc-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6c9fc-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c9fc-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6c9fc-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c9fc-132">Entry</span></span> | <span data-ttu-id="6c9fc-133">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9fc-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6c9fc-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c9fc-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6c9fc-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c9fc-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6c9fc-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c9fc-136">System-Only</span></span>            | <span data-ttu-id="6c9fc-137">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-137">False</span></span>                                                |
| <span data-ttu-id="6c9fc-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c9fc-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6c9fc-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="6c9fc-139">True</span></span>                                                 |
| <span data-ttu-id="6c9fc-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c9fc-140">Is Indexed</span></span>             | <span data-ttu-id="6c9fc-141">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-141">False</span></span>                                                |
| <span data-ttu-id="6c9fc-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c9fc-142">In Global Catalog</span></span>      | <span data-ttu-id="6c9fc-143">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-143">False</span></span>                                                |
| <span data-ttu-id="6c9fc-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c9fc-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c9fc-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c9fc-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6c9fc-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c9fc-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6c9fc-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c9fc-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6c9fc-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9fc-148">Search-Flags</span></span>           | <span data-ttu-id="6c9fc-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c9fc-149">0x00000000</span></span>                                           |
| <span data-ttu-id="6c9fc-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9fc-150">System-Flags</span></span>           | <span data-ttu-id="6c9fc-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c9fc-151">0x00000010</span></span>                                           |
| <span data-ttu-id="6c9fc-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c9fc-152">Classes used in</span></span>        | [<span data-ttu-id="6c9fc-153">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="6c9fc-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6c9fc-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c9fc-154">Windows Server 2003</span></span>



| <span data-ttu-id="6c9fc-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c9fc-155">Entry</span></span> | <span data-ttu-id="6c9fc-156">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9fc-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6c9fc-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c9fc-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6c9fc-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c9fc-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6c9fc-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c9fc-159">System-Only</span></span>            | <span data-ttu-id="6c9fc-160">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-160">False</span></span>                                                |
| <span data-ttu-id="6c9fc-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c9fc-161">Is-Single-Valued</span></span>       | <span data-ttu-id="6c9fc-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="6c9fc-162">True</span></span>                                                 |
| <span data-ttu-id="6c9fc-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c9fc-163">Is Indexed</span></span>             | <span data-ttu-id="6c9fc-164">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-164">False</span></span>                                                |
| <span data-ttu-id="6c9fc-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c9fc-165">In Global Catalog</span></span>      | <span data-ttu-id="6c9fc-166">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-166">False</span></span>                                                |
| <span data-ttu-id="6c9fc-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c9fc-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c9fc-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c9fc-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6c9fc-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c9fc-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6c9fc-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c9fc-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6c9fc-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9fc-171">Search-Flags</span></span>           | <span data-ttu-id="6c9fc-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c9fc-172">0x00000000</span></span>                                           |
| <span data-ttu-id="6c9fc-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9fc-173">System-Flags</span></span>           | <span data-ttu-id="6c9fc-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c9fc-174">0x00000010</span></span>                                           |
| <span data-ttu-id="6c9fc-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c9fc-175">Classes used in</span></span>        | [<span data-ttu-id="6c9fc-176">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="6c9fc-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6c9fc-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6c9fc-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6c9fc-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c9fc-178">Entry</span></span> | <span data-ttu-id="6c9fc-179">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9fc-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6c9fc-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c9fc-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6c9fc-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c9fc-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6c9fc-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c9fc-182">System-Only</span></span>            | <span data-ttu-id="6c9fc-183">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-183">False</span></span>                                                |
| <span data-ttu-id="6c9fc-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c9fc-184">Is-Single-Valued</span></span>       | <span data-ttu-id="6c9fc-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="6c9fc-185">True</span></span>                                                 |
| <span data-ttu-id="6c9fc-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c9fc-186">Is Indexed</span></span>             | <span data-ttu-id="6c9fc-187">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-187">False</span></span>                                                |
| <span data-ttu-id="6c9fc-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c9fc-188">In Global Catalog</span></span>      | <span data-ttu-id="6c9fc-189">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-189">False</span></span>                                                |
| <span data-ttu-id="6c9fc-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c9fc-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c9fc-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c9fc-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6c9fc-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c9fc-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6c9fc-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c9fc-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6c9fc-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9fc-194">Search-Flags</span></span>           | <span data-ttu-id="6c9fc-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c9fc-195">0x00000000</span></span>                                           |
| <span data-ttu-id="6c9fc-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9fc-196">System-Flags</span></span>           | <span data-ttu-id="6c9fc-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c9fc-197">0x00000010</span></span>                                           |
| <span data-ttu-id="6c9fc-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c9fc-198">Classes used in</span></span>        | [<span data-ttu-id="6c9fc-199">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="6c9fc-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6c9fc-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c9fc-200">Windows Server 2008</span></span>



| <span data-ttu-id="6c9fc-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c9fc-201">Entry</span></span> | <span data-ttu-id="6c9fc-202">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9fc-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6c9fc-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c9fc-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6c9fc-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c9fc-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6c9fc-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c9fc-205">System-Only</span></span>            | <span data-ttu-id="6c9fc-206">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-206">False</span></span>                                                |
| <span data-ttu-id="6c9fc-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c9fc-207">Is-Single-Valued</span></span>       | <span data-ttu-id="6c9fc-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="6c9fc-208">True</span></span>                                                 |
| <span data-ttu-id="6c9fc-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c9fc-209">Is Indexed</span></span>             | <span data-ttu-id="6c9fc-210">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-210">False</span></span>                                                |
| <span data-ttu-id="6c9fc-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c9fc-211">In Global Catalog</span></span>      | <span data-ttu-id="6c9fc-212">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-212">False</span></span>                                                |
| <span data-ttu-id="6c9fc-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c9fc-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c9fc-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c9fc-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6c9fc-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c9fc-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6c9fc-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c9fc-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6c9fc-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9fc-217">Search-Flags</span></span>           | <span data-ttu-id="6c9fc-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c9fc-218">0x00000000</span></span>                                           |
| <span data-ttu-id="6c9fc-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9fc-219">System-Flags</span></span>           | <span data-ttu-id="6c9fc-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c9fc-220">0x00000010</span></span>                                           |
| <span data-ttu-id="6c9fc-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c9fc-221">Classes used in</span></span>        | [<span data-ttu-id="6c9fc-222">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="6c9fc-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6c9fc-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6c9fc-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6c9fc-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c9fc-224">Entry</span></span> | <span data-ttu-id="6c9fc-225">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9fc-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6c9fc-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c9fc-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6c9fc-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c9fc-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6c9fc-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c9fc-228">System-Only</span></span>            | <span data-ttu-id="6c9fc-229">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-229">False</span></span>                                                |
| <span data-ttu-id="6c9fc-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c9fc-230">Is-Single-Valued</span></span>       | <span data-ttu-id="6c9fc-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="6c9fc-231">True</span></span>                                                 |
| <span data-ttu-id="6c9fc-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c9fc-232">Is Indexed</span></span>             | <span data-ttu-id="6c9fc-233">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-233">False</span></span>                                                |
| <span data-ttu-id="6c9fc-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c9fc-234">In Global Catalog</span></span>      | <span data-ttu-id="6c9fc-235">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-235">False</span></span>                                                |
| <span data-ttu-id="6c9fc-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c9fc-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c9fc-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c9fc-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6c9fc-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c9fc-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6c9fc-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c9fc-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6c9fc-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9fc-240">Search-Flags</span></span>           | <span data-ttu-id="6c9fc-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c9fc-241">0x00000000</span></span>                                           |
| <span data-ttu-id="6c9fc-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9fc-242">System-Flags</span></span>           | <span data-ttu-id="6c9fc-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c9fc-243">0x00000010</span></span>                                           |
| <span data-ttu-id="6c9fc-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c9fc-244">Classes used in</span></span>        | [<span data-ttu-id="6c9fc-245">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="6c9fc-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6c9fc-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6c9fc-246">Windows Server 2012</span></span>



| <span data-ttu-id="6c9fc-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c9fc-247">Entry</span></span> | <span data-ttu-id="6c9fc-248">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9fc-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6c9fc-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c9fc-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6c9fc-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c9fc-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6c9fc-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c9fc-251">System-Only</span></span>            | <span data-ttu-id="6c9fc-252">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-252">False</span></span>                                                |
| <span data-ttu-id="6c9fc-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c9fc-253">Is-Single-Valued</span></span>       | <span data-ttu-id="6c9fc-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="6c9fc-254">True</span></span>                                                 |
| <span data-ttu-id="6c9fc-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c9fc-255">Is Indexed</span></span>             | <span data-ttu-id="6c9fc-256">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-256">False</span></span>                                                |
| <span data-ttu-id="6c9fc-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c9fc-257">In Global Catalog</span></span>      | <span data-ttu-id="6c9fc-258">False</span><span class="sxs-lookup"><span data-stu-id="6c9fc-258">False</span></span>                                                |
| <span data-ttu-id="6c9fc-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c9fc-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c9fc-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c9fc-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6c9fc-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c9fc-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6c9fc-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c9fc-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6c9fc-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9fc-263">Search-Flags</span></span>           | <span data-ttu-id="6c9fc-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c9fc-264">0x00000000</span></span>                                           |
| <span data-ttu-id="6c9fc-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c9fc-265">System-Flags</span></span>           | <span data-ttu-id="6c9fc-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c9fc-266">0x00000010</span></span>                                           |
| <span data-ttu-id="6c9fc-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c9fc-267">Classes used in</span></span>        | [<span data-ttu-id="6c9fc-268">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="6c9fc-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





