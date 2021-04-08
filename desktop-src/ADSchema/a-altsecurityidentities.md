---
title: Alt-Security-Identitäten-Attribut
description: Enthält Zuordnungen für X. 509-Zertifikate oder externe Kerberos-Benutzerkonten für diesen Benutzer zum Zweck der Authentifizierung.
ms.assetid: 40b2af9c-fd4f-4883-8494-2b64682ee50c
ms.tgt_platform: multiple
keywords:
- Alt-Security-Identitäten-Attribut AD-Schema
- AD-Schema des altsecurityidentities-Attributs
topic_type:
- apiref
api_name:
- Alt-Security-Identities
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2548e337f29778400bb173a8c15d928d7b06d988
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957392"
---
# <a name="alt-security-identities-attribute"></a><span data-ttu-id="4260e-105">Alt-Security-Identitäten-Attribut</span><span class="sxs-lookup"><span data-stu-id="4260e-105">Alt-Security-Identities attribute</span></span>

<span data-ttu-id="4260e-106">Enthält Zuordnungen für X. 509-Zertifikate oder externe Kerberos-Benutzerkonten für diesen Benutzer zum Zweck der Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="4260e-106">Contains mappings for X.509 certificates or external Kerberos user accounts to this user for the purpose of authentication.</span></span>



| <span data-ttu-id="4260e-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4260e-107">Entry</span></span> | <span data-ttu-id="4260e-108">Wert</span><span class="sxs-lookup"><span data-stu-id="4260e-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="4260e-109">CN</span><span class="sxs-lookup"><span data-stu-id="4260e-109">CN</span></span>                | <span data-ttu-id="4260e-110">Alt-Sicherheit-Identitäten</span><span class="sxs-lookup"><span data-stu-id="4260e-110">Alt-Security-Identities</span></span>                             |
| <span data-ttu-id="4260e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4260e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4260e-112">altSecurityIdentities</span><span class="sxs-lookup"><span data-stu-id="4260e-112">altSecurityIdentities</span></span>                               |
| <span data-ttu-id="4260e-113">Size</span><span class="sxs-lookup"><span data-stu-id="4260e-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="4260e-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="4260e-114">Update Privilege</span></span>  | <span data-ttu-id="4260e-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="4260e-115">Domain administrator</span></span>                                |
| <span data-ttu-id="4260e-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="4260e-116">Update Frequency</span></span>  | <span data-ttu-id="4260e-117">Jedes Mal, wenn ein neuer Authentifizierungsmechanismus benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="4260e-117">Each time a new authentication mechanism is needed.</span></span> |
| <span data-ttu-id="4260e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4260e-118">Attribute-Id</span></span>      | <span data-ttu-id="4260e-119">1.2.840.113556.1.4.867</span><span class="sxs-lookup"><span data-stu-id="4260e-119">1.2.840.113556.1.4.867</span></span>                              |
| <span data-ttu-id="4260e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4260e-120">System-Id-Guid</span></span>    | <span data-ttu-id="4260e-121">00bbfi30c-91fe-11d1-AEbc-0000fi80367c1</span><span class="sxs-lookup"><span data-stu-id="4260e-121">00fbf30c-91fe-11d1-aebc-0000f80367c1</span></span>                |
| <span data-ttu-id="4260e-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="4260e-122">Syntax</span></span>            | [<span data-ttu-id="4260e-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4260e-123">**String(Unicode)**</span></span>](s-string-unicode.md)         |



## <a name="implementations"></a><span data-ttu-id="4260e-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="4260e-124">Implementations</span></span>

-   [<span data-ttu-id="4260e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4260e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4260e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4260e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4260e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4260e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4260e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4260e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4260e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4260e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4260e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4260e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4260e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4260e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="4260e-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4260e-132">Entry</span></span> | <span data-ttu-id="4260e-133">Wert</span><span class="sxs-lookup"><span data-stu-id="4260e-133">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="4260e-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4260e-134">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="4260e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4260e-135">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="4260e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4260e-136">System-Only</span></span>            | <span data-ttu-id="4260e-137">False</span><span class="sxs-lookup"><span data-stu-id="4260e-137">False</span></span>                                                        |
| <span data-ttu-id="4260e-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4260e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4260e-139">False</span><span class="sxs-lookup"><span data-stu-id="4260e-139">False</span></span>                                                        |
| <span data-ttu-id="4260e-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4260e-140">Is Indexed</span></span>             | <span data-ttu-id="4260e-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="4260e-141">True</span></span>                                                         |
| <span data-ttu-id="4260e-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4260e-142">In Global Catalog</span></span>      | <span data-ttu-id="4260e-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="4260e-143">True</span></span>                                                         |
| <span data-ttu-id="4260e-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4260e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4260e-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4260e-145">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="4260e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4260e-146">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="4260e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4260e-147">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="4260e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4260e-148">Search-Flags</span></span>           | <span data-ttu-id="4260e-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4260e-149">0x00000001</span></span>                                                   |
| <span data-ttu-id="4260e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4260e-150">System-Flags</span></span>           | <span data-ttu-id="4260e-151">0x00000012</span><span class="sxs-lookup"><span data-stu-id="4260e-151">0x00000012</span></span>                                                   |
| <span data-ttu-id="4260e-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4260e-152">Classes used in</span></span>        | [<span data-ttu-id="4260e-153">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="4260e-153">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4260e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4260e-154">Windows Server 2003</span></span>



| <span data-ttu-id="4260e-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4260e-155">Entry</span></span> | <span data-ttu-id="4260e-156">Wert</span><span class="sxs-lookup"><span data-stu-id="4260e-156">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="4260e-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4260e-157">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="4260e-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4260e-158">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="4260e-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="4260e-159">System-Only</span></span>            | <span data-ttu-id="4260e-160">False</span><span class="sxs-lookup"><span data-stu-id="4260e-160">False</span></span>                                                        |
| <span data-ttu-id="4260e-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4260e-161">Is-Single-Valued</span></span>       | <span data-ttu-id="4260e-162">False</span><span class="sxs-lookup"><span data-stu-id="4260e-162">False</span></span>                                                        |
| <span data-ttu-id="4260e-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4260e-163">Is Indexed</span></span>             | <span data-ttu-id="4260e-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="4260e-164">True</span></span>                                                         |
| <span data-ttu-id="4260e-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4260e-165">In Global Catalog</span></span>      | <span data-ttu-id="4260e-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="4260e-166">True</span></span>                                                         |
| <span data-ttu-id="4260e-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4260e-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="4260e-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4260e-168">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="4260e-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4260e-169">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="4260e-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4260e-170">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="4260e-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4260e-171">Search-Flags</span></span>           | <span data-ttu-id="4260e-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4260e-172">0x00000001</span></span>                                                   |
| <span data-ttu-id="4260e-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4260e-173">System-Flags</span></span>           | <span data-ttu-id="4260e-174">0x00000012</span><span class="sxs-lookup"><span data-stu-id="4260e-174">0x00000012</span></span>                                                   |
| <span data-ttu-id="4260e-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4260e-175">Classes used in</span></span>        | [<span data-ttu-id="4260e-176">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="4260e-176">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4260e-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4260e-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4260e-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4260e-178">Entry</span></span> | <span data-ttu-id="4260e-179">Wert</span><span class="sxs-lookup"><span data-stu-id="4260e-179">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="4260e-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4260e-180">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="4260e-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4260e-181">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="4260e-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="4260e-182">System-Only</span></span>            | <span data-ttu-id="4260e-183">False</span><span class="sxs-lookup"><span data-stu-id="4260e-183">False</span></span>                                                        |
| <span data-ttu-id="4260e-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4260e-184">Is-Single-Valued</span></span>       | <span data-ttu-id="4260e-185">False</span><span class="sxs-lookup"><span data-stu-id="4260e-185">False</span></span>                                                        |
| <span data-ttu-id="4260e-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4260e-186">Is Indexed</span></span>             | <span data-ttu-id="4260e-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="4260e-187">True</span></span>                                                         |
| <span data-ttu-id="4260e-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4260e-188">In Global Catalog</span></span>      | <span data-ttu-id="4260e-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="4260e-189">True</span></span>                                                         |
| <span data-ttu-id="4260e-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4260e-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="4260e-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4260e-191">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="4260e-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4260e-192">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="4260e-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4260e-193">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="4260e-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4260e-194">Search-Flags</span></span>           | <span data-ttu-id="4260e-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4260e-195">0x00000001</span></span>                                                   |
| <span data-ttu-id="4260e-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4260e-196">System-Flags</span></span>           | <span data-ttu-id="4260e-197">0x00000012</span><span class="sxs-lookup"><span data-stu-id="4260e-197">0x00000012</span></span>                                                   |
| <span data-ttu-id="4260e-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4260e-198">Classes used in</span></span>        | [<span data-ttu-id="4260e-199">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="4260e-199">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4260e-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4260e-200">Windows Server 2008</span></span>



| <span data-ttu-id="4260e-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4260e-201">Entry</span></span> | <span data-ttu-id="4260e-202">Wert</span><span class="sxs-lookup"><span data-stu-id="4260e-202">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="4260e-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4260e-203">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="4260e-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4260e-204">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="4260e-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="4260e-205">System-Only</span></span>            | <span data-ttu-id="4260e-206">False</span><span class="sxs-lookup"><span data-stu-id="4260e-206">False</span></span>                                                        |
| <span data-ttu-id="4260e-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4260e-207">Is-Single-Valued</span></span>       | <span data-ttu-id="4260e-208">False</span><span class="sxs-lookup"><span data-stu-id="4260e-208">False</span></span>                                                        |
| <span data-ttu-id="4260e-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4260e-209">Is Indexed</span></span>             | <span data-ttu-id="4260e-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="4260e-210">True</span></span>                                                         |
| <span data-ttu-id="4260e-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4260e-211">In Global Catalog</span></span>      | <span data-ttu-id="4260e-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="4260e-212">True</span></span>                                                         |
| <span data-ttu-id="4260e-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4260e-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="4260e-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4260e-214">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="4260e-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4260e-215">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="4260e-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4260e-216">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="4260e-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4260e-217">Search-Flags</span></span>           | <span data-ttu-id="4260e-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4260e-218">0x00000001</span></span>                                                   |
| <span data-ttu-id="4260e-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4260e-219">System-Flags</span></span>           | <span data-ttu-id="4260e-220">0x00000012</span><span class="sxs-lookup"><span data-stu-id="4260e-220">0x00000012</span></span>                                                   |
| <span data-ttu-id="4260e-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4260e-221">Classes used in</span></span>        | [<span data-ttu-id="4260e-222">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="4260e-222">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4260e-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4260e-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4260e-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4260e-224">Entry</span></span> | <span data-ttu-id="4260e-225">Wert</span><span class="sxs-lookup"><span data-stu-id="4260e-225">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="4260e-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4260e-226">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="4260e-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4260e-227">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="4260e-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="4260e-228">System-Only</span></span>            | <span data-ttu-id="4260e-229">False</span><span class="sxs-lookup"><span data-stu-id="4260e-229">False</span></span>                                                        |
| <span data-ttu-id="4260e-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4260e-230">Is-Single-Valued</span></span>       | <span data-ttu-id="4260e-231">False</span><span class="sxs-lookup"><span data-stu-id="4260e-231">False</span></span>                                                        |
| <span data-ttu-id="4260e-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4260e-232">Is Indexed</span></span>             | <span data-ttu-id="4260e-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="4260e-233">True</span></span>                                                         |
| <span data-ttu-id="4260e-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4260e-234">In Global Catalog</span></span>      | <span data-ttu-id="4260e-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="4260e-235">True</span></span>                                                         |
| <span data-ttu-id="4260e-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4260e-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="4260e-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4260e-237">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="4260e-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4260e-238">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="4260e-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4260e-239">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="4260e-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4260e-240">Search-Flags</span></span>           | <span data-ttu-id="4260e-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4260e-241">0x00000001</span></span>                                                   |
| <span data-ttu-id="4260e-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4260e-242">System-Flags</span></span>           | <span data-ttu-id="4260e-243">0x00000012</span><span class="sxs-lookup"><span data-stu-id="4260e-243">0x00000012</span></span>                                                   |
| <span data-ttu-id="4260e-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4260e-244">Classes used in</span></span>        | [<span data-ttu-id="4260e-245">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="4260e-245">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4260e-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4260e-246">Windows Server 2012</span></span>



| <span data-ttu-id="4260e-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4260e-247">Entry</span></span> | <span data-ttu-id="4260e-248">Wert</span><span class="sxs-lookup"><span data-stu-id="4260e-248">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="4260e-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4260e-249">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="4260e-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4260e-250">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="4260e-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="4260e-251">System-Only</span></span>            | <span data-ttu-id="4260e-252">False</span><span class="sxs-lookup"><span data-stu-id="4260e-252">False</span></span>                                                        |
| <span data-ttu-id="4260e-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4260e-253">Is-Single-Valued</span></span>       | <span data-ttu-id="4260e-254">False</span><span class="sxs-lookup"><span data-stu-id="4260e-254">False</span></span>                                                        |
| <span data-ttu-id="4260e-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4260e-255">Is Indexed</span></span>             | <span data-ttu-id="4260e-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="4260e-256">True</span></span>                                                         |
| <span data-ttu-id="4260e-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4260e-257">In Global Catalog</span></span>      | <span data-ttu-id="4260e-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="4260e-258">True</span></span>                                                         |
| <span data-ttu-id="4260e-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4260e-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="4260e-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4260e-260">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="4260e-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4260e-261">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="4260e-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4260e-262">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="4260e-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4260e-263">Search-Flags</span></span>           | <span data-ttu-id="4260e-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4260e-264">0x00000001</span></span>                                                   |
| <span data-ttu-id="4260e-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4260e-265">System-Flags</span></span>           | <span data-ttu-id="4260e-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="4260e-266">0x00000012</span></span>                                                   |
| <span data-ttu-id="4260e-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4260e-267">Classes used in</span></span>        | [<span data-ttu-id="4260e-268">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="4260e-268">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





