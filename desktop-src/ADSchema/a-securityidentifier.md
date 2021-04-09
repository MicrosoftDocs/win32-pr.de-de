---
title: Security-Identifier-Attribut
description: Ein eindeutiger Wert der Variablen Länge, mit dem ein Benutzerkonto, ein Gruppenkonto oder eine Anmelde Sitzung identifiziert wird, für die ein ACE gilt.
ms.assetid: bb6a16f6-d2c1-48f1-af9a-40fe2a59f281
ms.tgt_platform: multiple
keywords:
- AD-Schema für Security-Identifier-Attribut
- SecurityIdentifier-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Security-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd921d0bcba08c2174475007476add8e8787456
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744529"
---
# <a name="security-identifier-attribute"></a><span data-ttu-id="c482f-105">Security-Identifier-Attribut</span><span class="sxs-lookup"><span data-stu-id="c482f-105">Security-Identifier attribute</span></span>

<span data-ttu-id="c482f-106">Ein eindeutiger Wert der Variablen Länge, mit dem ein Benutzerkonto, ein Gruppenkonto oder eine Anmelde Sitzung identifiziert wird, für die ein ACE gilt.</span><span class="sxs-lookup"><span data-stu-id="c482f-106">A unique value of variable length used to identify a user account, group account, or logon session to which an ACE applies.</span></span>



| <span data-ttu-id="c482f-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c482f-107">Entry</span></span> | <span data-ttu-id="c482f-108">Wert</span><span class="sxs-lookup"><span data-stu-id="c482f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c482f-109">CN</span><span class="sxs-lookup"><span data-stu-id="c482f-109">CN</span></span>                | <span data-ttu-id="c482f-110">Security-Identifier</span><span class="sxs-lookup"><span data-stu-id="c482f-110">Security-Identifier</span></span>                  |
| <span data-ttu-id="c482f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c482f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c482f-112">securityIdentifier</span><span class="sxs-lookup"><span data-stu-id="c482f-112">securityIdentifier</span></span>                   |
| <span data-ttu-id="c482f-113">Size</span><span class="sxs-lookup"><span data-stu-id="c482f-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="c482f-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c482f-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c482f-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="c482f-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c482f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c482f-116">Attribute-Id</span></span>      | <span data-ttu-id="c482f-117">1.2.840.113556.1.4.121</span><span class="sxs-lookup"><span data-stu-id="c482f-117">1.2.840.113556.1.4.121</span></span>               |
| <span data-ttu-id="c482f-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c482f-118">System-Id-Guid</span></span>    | <span data-ttu-id="c482f-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c482f-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="c482f-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="c482f-120">Syntax</span></span>            | [<span data-ttu-id="c482f-121">**Zeichenfolge (SID)**</span><span class="sxs-lookup"><span data-stu-id="c482f-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="c482f-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="c482f-122">Implementations</span></span>

-   [<span data-ttu-id="c482f-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c482f-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c482f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c482f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c482f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c482f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c482f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c482f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c482f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c482f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c482f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c482f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c482f-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c482f-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c482f-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c482f-130">Entry</span></span> | <span data-ttu-id="c482f-131">Wert</span><span class="sxs-lookup"><span data-stu-id="c482f-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c482f-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c482f-132">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="c482f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c482f-133">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="c482f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c482f-134">System-Only</span></span>            | <span data-ttu-id="c482f-135">False</span><span class="sxs-lookup"><span data-stu-id="c482f-135">False</span></span>                                                                                                             |
| <span data-ttu-id="c482f-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c482f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c482f-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="c482f-137">True</span></span>                                                                                                              |
| <span data-ttu-id="c482f-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c482f-138">Is Indexed</span></span>             | <span data-ttu-id="c482f-139">False</span><span class="sxs-lookup"><span data-stu-id="c482f-139">False</span></span>                                                                                                             |
| <span data-ttu-id="c482f-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c482f-140">In Global Catalog</span></span>      | <span data-ttu-id="c482f-141">False</span><span class="sxs-lookup"><span data-stu-id="c482f-141">False</span></span>                                                                                                             |
| <span data-ttu-id="c482f-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c482f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c482f-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c482f-143">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="c482f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c482f-144">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="c482f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c482f-145">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="c482f-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c482f-146">Search-Flags</span></span>           | <span data-ttu-id="c482f-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c482f-147">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="c482f-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c482f-148">System-Flags</span></span>           | <span data-ttu-id="c482f-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c482f-149">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="c482f-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c482f-150">Classes used in</span></span>        | [<span data-ttu-id="c482f-151">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="c482f-151">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="c482f-152">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="c482f-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c482f-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c482f-153">Windows Server 2003</span></span>



| <span data-ttu-id="c482f-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c482f-154">Entry</span></span> | <span data-ttu-id="c482f-155">Wert</span><span class="sxs-lookup"><span data-stu-id="c482f-155">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c482f-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c482f-156">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="c482f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c482f-157">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="c482f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c482f-158">System-Only</span></span>            | <span data-ttu-id="c482f-159">False</span><span class="sxs-lookup"><span data-stu-id="c482f-159">False</span></span>                                                                                                             |
| <span data-ttu-id="c482f-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c482f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c482f-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="c482f-161">True</span></span>                                                                                                              |
| <span data-ttu-id="c482f-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c482f-162">Is Indexed</span></span>             | <span data-ttu-id="c482f-163">False</span><span class="sxs-lookup"><span data-stu-id="c482f-163">False</span></span>                                                                                                             |
| <span data-ttu-id="c482f-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c482f-164">In Global Catalog</span></span>      | <span data-ttu-id="c482f-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="c482f-165">True</span></span>                                                                                                              |
| <span data-ttu-id="c482f-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c482f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c482f-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c482f-167">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="c482f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c482f-168">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="c482f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c482f-169">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="c482f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c482f-170">Search-Flags</span></span>           | <span data-ttu-id="c482f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c482f-171">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="c482f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c482f-172">System-Flags</span></span>           | <span data-ttu-id="c482f-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c482f-173">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="c482f-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c482f-174">Classes used in</span></span>        | [<span data-ttu-id="c482f-175">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="c482f-175">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="c482f-176">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="c482f-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c482f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c482f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c482f-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c482f-178">Entry</span></span> | <span data-ttu-id="c482f-179">Wert</span><span class="sxs-lookup"><span data-stu-id="c482f-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c482f-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c482f-180">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="c482f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c482f-181">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="c482f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="c482f-182">System-Only</span></span>            | <span data-ttu-id="c482f-183">False</span><span class="sxs-lookup"><span data-stu-id="c482f-183">False</span></span>                                                                                                             |
| <span data-ttu-id="c482f-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c482f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="c482f-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="c482f-185">True</span></span>                                                                                                              |
| <span data-ttu-id="c482f-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c482f-186">Is Indexed</span></span>             | <span data-ttu-id="c482f-187">False</span><span class="sxs-lookup"><span data-stu-id="c482f-187">False</span></span>                                                                                                             |
| <span data-ttu-id="c482f-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c482f-188">In Global Catalog</span></span>      | <span data-ttu-id="c482f-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="c482f-189">True</span></span>                                                                                                              |
| <span data-ttu-id="c482f-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c482f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="c482f-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c482f-191">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="c482f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c482f-192">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="c482f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c482f-193">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="c482f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c482f-194">Search-Flags</span></span>           | <span data-ttu-id="c482f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c482f-195">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="c482f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c482f-196">System-Flags</span></span>           | <span data-ttu-id="c482f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c482f-197">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="c482f-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c482f-198">Classes used in</span></span>        | [<span data-ttu-id="c482f-199">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="c482f-199">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="c482f-200">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="c482f-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c482f-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c482f-201">Windows Server 2008</span></span>



| <span data-ttu-id="c482f-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c482f-202">Entry</span></span> | <span data-ttu-id="c482f-203">Wert</span><span class="sxs-lookup"><span data-stu-id="c482f-203">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c482f-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c482f-204">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="c482f-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c482f-205">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="c482f-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="c482f-206">System-Only</span></span>            | <span data-ttu-id="c482f-207">False</span><span class="sxs-lookup"><span data-stu-id="c482f-207">False</span></span>                                                                                                             |
| <span data-ttu-id="c482f-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c482f-208">Is-Single-Valued</span></span>       | <span data-ttu-id="c482f-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="c482f-209">True</span></span>                                                                                                              |
| <span data-ttu-id="c482f-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c482f-210">Is Indexed</span></span>             | <span data-ttu-id="c482f-211">False</span><span class="sxs-lookup"><span data-stu-id="c482f-211">False</span></span>                                                                                                             |
| <span data-ttu-id="c482f-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c482f-212">In Global Catalog</span></span>      | <span data-ttu-id="c482f-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="c482f-213">True</span></span>                                                                                                              |
| <span data-ttu-id="c482f-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c482f-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="c482f-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c482f-215">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="c482f-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c482f-216">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="c482f-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c482f-217">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="c482f-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c482f-218">Search-Flags</span></span>           | <span data-ttu-id="c482f-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c482f-219">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="c482f-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c482f-220">System-Flags</span></span>           | <span data-ttu-id="c482f-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c482f-221">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="c482f-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c482f-222">Classes used in</span></span>        | [<span data-ttu-id="c482f-223">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="c482f-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="c482f-224">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="c482f-224">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c482f-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c482f-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c482f-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c482f-226">Entry</span></span> | <span data-ttu-id="c482f-227">Wert</span><span class="sxs-lookup"><span data-stu-id="c482f-227">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c482f-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c482f-228">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="c482f-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c482f-229">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="c482f-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="c482f-230">System-Only</span></span>            | <span data-ttu-id="c482f-231">False</span><span class="sxs-lookup"><span data-stu-id="c482f-231">False</span></span>                                                                                                             |
| <span data-ttu-id="c482f-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c482f-232">Is-Single-Valued</span></span>       | <span data-ttu-id="c482f-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="c482f-233">True</span></span>                                                                                                              |
| <span data-ttu-id="c482f-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c482f-234">Is Indexed</span></span>             | <span data-ttu-id="c482f-235">False</span><span class="sxs-lookup"><span data-stu-id="c482f-235">False</span></span>                                                                                                             |
| <span data-ttu-id="c482f-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c482f-236">In Global Catalog</span></span>      | <span data-ttu-id="c482f-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="c482f-237">True</span></span>                                                                                                              |
| <span data-ttu-id="c482f-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c482f-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="c482f-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c482f-239">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="c482f-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c482f-240">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="c482f-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c482f-241">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="c482f-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c482f-242">Search-Flags</span></span>           | <span data-ttu-id="c482f-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c482f-243">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="c482f-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c482f-244">System-Flags</span></span>           | <span data-ttu-id="c482f-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c482f-245">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="c482f-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c482f-246">Classes used in</span></span>        | [<span data-ttu-id="c482f-247">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="c482f-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="c482f-248">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="c482f-248">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c482f-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c482f-249">Windows Server 2012</span></span>



| <span data-ttu-id="c482f-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c482f-250">Entry</span></span> | <span data-ttu-id="c482f-251">Wert</span><span class="sxs-lookup"><span data-stu-id="c482f-251">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c482f-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c482f-252">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="c482f-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c482f-253">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="c482f-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="c482f-254">System-Only</span></span>            | <span data-ttu-id="c482f-255">False</span><span class="sxs-lookup"><span data-stu-id="c482f-255">False</span></span>                                                                                                             |
| <span data-ttu-id="c482f-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c482f-256">Is-Single-Valued</span></span>       | <span data-ttu-id="c482f-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="c482f-257">True</span></span>                                                                                                              |
| <span data-ttu-id="c482f-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c482f-258">Is Indexed</span></span>             | <span data-ttu-id="c482f-259">False</span><span class="sxs-lookup"><span data-stu-id="c482f-259">False</span></span>                                                                                                             |
| <span data-ttu-id="c482f-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c482f-260">In Global Catalog</span></span>      | <span data-ttu-id="c482f-261">Richtig</span><span class="sxs-lookup"><span data-stu-id="c482f-261">True</span></span>                                                                                                              |
| <span data-ttu-id="c482f-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c482f-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="c482f-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c482f-263">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="c482f-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c482f-264">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="c482f-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c482f-265">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="c482f-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c482f-266">Search-Flags</span></span>           | <span data-ttu-id="c482f-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c482f-267">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="c482f-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c482f-268">System-Flags</span></span>           | <span data-ttu-id="c482f-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c482f-269">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="c482f-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c482f-270">Classes used in</span></span>        | [<span data-ttu-id="c482f-271">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="c482f-271">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="c482f-272">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="c482f-272">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





