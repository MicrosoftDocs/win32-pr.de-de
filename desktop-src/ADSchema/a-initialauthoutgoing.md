---
title: Ursprüngliches Authentifizierungs Attribut
description: Enthält Informationen über eine anfängliche ausgehende Authentifizierung, die vom Authentifizierungsserver für diese Domäne an den Client gesendet wurde, der die Authentifizierung angefordert hat.
ms.assetid: cc5ceb14-0424-4caa-bcd9-1e48988af67a
ms.tgt_platform: multiple
keywords:
- AD-Schema für das anfängliche auth-ausgehende Attribut
- AD-Schema des initialauthoutgoing-Attributs
topic_type:
- apiref
api_name:
- Initial-Auth-Outgoing
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84faaa443c9589e04f4998dc41d72fe870b5f2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107043"
---
# <a name="initial-auth-outgoing-attribute"></a><span data-ttu-id="2767e-105">Ursprüngliches Authentifizierungs Attribut</span><span class="sxs-lookup"><span data-stu-id="2767e-105">Initial-Auth-Outgoing attribute</span></span>

<span data-ttu-id="2767e-106">Enthält Informationen über eine anfängliche ausgehende Authentifizierung, die vom Authentifizierungsserver für diese Domäne an den Client gesendet wurde, der die Authentifizierung angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="2767e-106">Contains information about an initial outgoing authentication sent by the authentication server for this domain to the client that requested authentication.</span></span> <span data-ttu-id="2767e-107">Der Server, der dieses Attribut verwendet, empfängt die Autorisierung vom Authentifizierungsserver und sendet Sie an den Client.</span><span class="sxs-lookup"><span data-stu-id="2767e-107">The server that uses this attribute receives the authorization from the authentication server and sends it to the client.</span></span>



| <span data-ttu-id="2767e-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2767e-108">Entry</span></span> | <span data-ttu-id="2767e-109">Wert</span><span class="sxs-lookup"><span data-stu-id="2767e-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="2767e-110">CN</span><span class="sxs-lookup"><span data-stu-id="2767e-110">CN</span></span>                | <span data-ttu-id="2767e-111">Anfängliche Authentifizierung: ausgehend</span><span class="sxs-lookup"><span data-stu-id="2767e-111">Initial-Auth-Outgoing</span></span>                       |
| <span data-ttu-id="2767e-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2767e-112">Ldap-Display-Name</span></span> | <span data-ttu-id="2767e-113">initialauthoutgoing</span><span class="sxs-lookup"><span data-stu-id="2767e-113">initialAuthOutgoing</span></span>                         |
| <span data-ttu-id="2767e-114">Size</span><span class="sxs-lookup"><span data-stu-id="2767e-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="2767e-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2767e-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="2767e-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="2767e-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="2767e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2767e-117">Attribute-Id</span></span>      | <span data-ttu-id="2767e-118">1.2.840.113556.1.4.540</span><span class="sxs-lookup"><span data-stu-id="2767e-118">1.2.840.113556.1.4.540</span></span>                      |
| <span data-ttu-id="2767e-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2767e-119">System-Id-Guid</span></span>    | <span data-ttu-id="2767e-120">52458024-ca6a-11D0-affinf-0000f 80367c1</span><span class="sxs-lookup"><span data-stu-id="2767e-120">52458024-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="2767e-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="2767e-121">Syntax</span></span>            | [<span data-ttu-id="2767e-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="2767e-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="2767e-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="2767e-123">Implementations</span></span>

-   [<span data-ttu-id="2767e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2767e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2767e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2767e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2767e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2767e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2767e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2767e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2767e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2767e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2767e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2767e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2767e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2767e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="2767e-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2767e-131">Entry</span></span> | <span data-ttu-id="2767e-132">Wert</span><span class="sxs-lookup"><span data-stu-id="2767e-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2767e-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2767e-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2767e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2767e-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2767e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="2767e-135">System-Only</span></span>            | <span data-ttu-id="2767e-136">False</span><span class="sxs-lookup"><span data-stu-id="2767e-136">False</span></span>                                                |
| <span data-ttu-id="2767e-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2767e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="2767e-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="2767e-138">True</span></span>                                                 |
| <span data-ttu-id="2767e-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2767e-139">Is Indexed</span></span>             | <span data-ttu-id="2767e-140">False</span><span class="sxs-lookup"><span data-stu-id="2767e-140">False</span></span>                                                |
| <span data-ttu-id="2767e-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2767e-141">In Global Catalog</span></span>      | <span data-ttu-id="2767e-142">False</span><span class="sxs-lookup"><span data-stu-id="2767e-142">False</span></span>                                                |
| <span data-ttu-id="2767e-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2767e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="2767e-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2767e-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2767e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2767e-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2767e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2767e-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2767e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2767e-147">Search-Flags</span></span>           | <span data-ttu-id="2767e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2767e-148">0x00000000</span></span>                                           |
| <span data-ttu-id="2767e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2767e-149">System-Flags</span></span>           | <span data-ttu-id="2767e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2767e-150">0x00000010</span></span>                                           |
| <span data-ttu-id="2767e-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2767e-151">Classes used in</span></span>        | [<span data-ttu-id="2767e-152">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="2767e-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2767e-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2767e-153">Windows Server 2003</span></span>



| <span data-ttu-id="2767e-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2767e-154">Entry</span></span> | <span data-ttu-id="2767e-155">Wert</span><span class="sxs-lookup"><span data-stu-id="2767e-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2767e-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2767e-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2767e-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2767e-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2767e-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2767e-158">System-Only</span></span>            | <span data-ttu-id="2767e-159">False</span><span class="sxs-lookup"><span data-stu-id="2767e-159">False</span></span>                                                |
| <span data-ttu-id="2767e-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2767e-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2767e-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="2767e-161">True</span></span>                                                 |
| <span data-ttu-id="2767e-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2767e-162">Is Indexed</span></span>             | <span data-ttu-id="2767e-163">False</span><span class="sxs-lookup"><span data-stu-id="2767e-163">False</span></span>                                                |
| <span data-ttu-id="2767e-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2767e-164">In Global Catalog</span></span>      | <span data-ttu-id="2767e-165">False</span><span class="sxs-lookup"><span data-stu-id="2767e-165">False</span></span>                                                |
| <span data-ttu-id="2767e-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2767e-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2767e-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2767e-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2767e-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2767e-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2767e-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2767e-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2767e-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2767e-170">Search-Flags</span></span>           | <span data-ttu-id="2767e-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2767e-171">0x00000000</span></span>                                           |
| <span data-ttu-id="2767e-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2767e-172">System-Flags</span></span>           | <span data-ttu-id="2767e-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2767e-173">0x00000010</span></span>                                           |
| <span data-ttu-id="2767e-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2767e-174">Classes used in</span></span>        | [<span data-ttu-id="2767e-175">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="2767e-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2767e-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2767e-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2767e-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2767e-177">Entry</span></span> | <span data-ttu-id="2767e-178">Wert</span><span class="sxs-lookup"><span data-stu-id="2767e-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2767e-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2767e-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2767e-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2767e-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2767e-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2767e-181">System-Only</span></span>            | <span data-ttu-id="2767e-182">False</span><span class="sxs-lookup"><span data-stu-id="2767e-182">False</span></span>                                                |
| <span data-ttu-id="2767e-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2767e-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2767e-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="2767e-184">True</span></span>                                                 |
| <span data-ttu-id="2767e-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2767e-185">Is Indexed</span></span>             | <span data-ttu-id="2767e-186">False</span><span class="sxs-lookup"><span data-stu-id="2767e-186">False</span></span>                                                |
| <span data-ttu-id="2767e-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2767e-187">In Global Catalog</span></span>      | <span data-ttu-id="2767e-188">False</span><span class="sxs-lookup"><span data-stu-id="2767e-188">False</span></span>                                                |
| <span data-ttu-id="2767e-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2767e-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2767e-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2767e-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2767e-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2767e-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2767e-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2767e-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2767e-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2767e-193">Search-Flags</span></span>           | <span data-ttu-id="2767e-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2767e-194">0x00000000</span></span>                                           |
| <span data-ttu-id="2767e-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2767e-195">System-Flags</span></span>           | <span data-ttu-id="2767e-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2767e-196">0x00000010</span></span>                                           |
| <span data-ttu-id="2767e-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2767e-197">Classes used in</span></span>        | [<span data-ttu-id="2767e-198">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="2767e-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2767e-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2767e-199">Windows Server 2008</span></span>



| <span data-ttu-id="2767e-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2767e-200">Entry</span></span> | <span data-ttu-id="2767e-201">Wert</span><span class="sxs-lookup"><span data-stu-id="2767e-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2767e-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2767e-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2767e-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2767e-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2767e-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="2767e-204">System-Only</span></span>            | <span data-ttu-id="2767e-205">False</span><span class="sxs-lookup"><span data-stu-id="2767e-205">False</span></span>                                                |
| <span data-ttu-id="2767e-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2767e-206">Is-Single-Valued</span></span>       | <span data-ttu-id="2767e-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="2767e-207">True</span></span>                                                 |
| <span data-ttu-id="2767e-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2767e-208">Is Indexed</span></span>             | <span data-ttu-id="2767e-209">False</span><span class="sxs-lookup"><span data-stu-id="2767e-209">False</span></span>                                                |
| <span data-ttu-id="2767e-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2767e-210">In Global Catalog</span></span>      | <span data-ttu-id="2767e-211">False</span><span class="sxs-lookup"><span data-stu-id="2767e-211">False</span></span>                                                |
| <span data-ttu-id="2767e-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2767e-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="2767e-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2767e-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2767e-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2767e-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2767e-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2767e-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2767e-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2767e-216">Search-Flags</span></span>           | <span data-ttu-id="2767e-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2767e-217">0x00000000</span></span>                                           |
| <span data-ttu-id="2767e-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2767e-218">System-Flags</span></span>           | <span data-ttu-id="2767e-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2767e-219">0x00000010</span></span>                                           |
| <span data-ttu-id="2767e-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2767e-220">Classes used in</span></span>        | [<span data-ttu-id="2767e-221">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="2767e-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2767e-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2767e-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2767e-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2767e-223">Entry</span></span> | <span data-ttu-id="2767e-224">Wert</span><span class="sxs-lookup"><span data-stu-id="2767e-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2767e-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2767e-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2767e-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2767e-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2767e-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="2767e-227">System-Only</span></span>            | <span data-ttu-id="2767e-228">False</span><span class="sxs-lookup"><span data-stu-id="2767e-228">False</span></span>                                                |
| <span data-ttu-id="2767e-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2767e-229">Is-Single-Valued</span></span>       | <span data-ttu-id="2767e-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="2767e-230">True</span></span>                                                 |
| <span data-ttu-id="2767e-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2767e-231">Is Indexed</span></span>             | <span data-ttu-id="2767e-232">False</span><span class="sxs-lookup"><span data-stu-id="2767e-232">False</span></span>                                                |
| <span data-ttu-id="2767e-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2767e-233">In Global Catalog</span></span>      | <span data-ttu-id="2767e-234">False</span><span class="sxs-lookup"><span data-stu-id="2767e-234">False</span></span>                                                |
| <span data-ttu-id="2767e-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2767e-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="2767e-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2767e-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2767e-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2767e-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2767e-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2767e-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2767e-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2767e-239">Search-Flags</span></span>           | <span data-ttu-id="2767e-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2767e-240">0x00000000</span></span>                                           |
| <span data-ttu-id="2767e-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2767e-241">System-Flags</span></span>           | <span data-ttu-id="2767e-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2767e-242">0x00000010</span></span>                                           |
| <span data-ttu-id="2767e-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2767e-243">Classes used in</span></span>        | [<span data-ttu-id="2767e-244">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="2767e-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2767e-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2767e-245">Windows Server 2012</span></span>



| <span data-ttu-id="2767e-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2767e-246">Entry</span></span> | <span data-ttu-id="2767e-247">Wert</span><span class="sxs-lookup"><span data-stu-id="2767e-247">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2767e-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2767e-248">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2767e-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2767e-249">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2767e-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="2767e-250">System-Only</span></span>            | <span data-ttu-id="2767e-251">False</span><span class="sxs-lookup"><span data-stu-id="2767e-251">False</span></span>                                                |
| <span data-ttu-id="2767e-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2767e-252">Is-Single-Valued</span></span>       | <span data-ttu-id="2767e-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="2767e-253">True</span></span>                                                 |
| <span data-ttu-id="2767e-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2767e-254">Is Indexed</span></span>             | <span data-ttu-id="2767e-255">False</span><span class="sxs-lookup"><span data-stu-id="2767e-255">False</span></span>                                                |
| <span data-ttu-id="2767e-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2767e-256">In Global Catalog</span></span>      | <span data-ttu-id="2767e-257">False</span><span class="sxs-lookup"><span data-stu-id="2767e-257">False</span></span>                                                |
| <span data-ttu-id="2767e-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2767e-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="2767e-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2767e-259">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2767e-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2767e-260">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2767e-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2767e-261">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2767e-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2767e-262">Search-Flags</span></span>           | <span data-ttu-id="2767e-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2767e-263">0x00000000</span></span>                                           |
| <span data-ttu-id="2767e-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2767e-264">System-Flags</span></span>           | <span data-ttu-id="2767e-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2767e-265">0x00000010</span></span>                                           |
| <span data-ttu-id="2767e-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2767e-266">Classes used in</span></span>        | [<span data-ttu-id="2767e-267">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="2767e-267">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





