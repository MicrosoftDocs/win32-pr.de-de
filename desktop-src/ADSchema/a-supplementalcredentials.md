---
title: Supplemental-Credentials-Attribut
description: Gespeicherte Anmelde Informationen für die Verwendung bei der Authentifizierung. Die verschlüsselte Version des Benutzer Kennworts. Dieses Attribut ist weder lesbar noch beschreibbar.
ms.assetid: 642aa699-094e-40ed-a2f8-ec7219c85de2
ms.tgt_platform: multiple
keywords:
- AD-Schema für Supplemental-Credentials-Attribut
- ergänzenden Anmelde Informationen-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Supplemental-Credentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e19a73b3ae3cf19745fc995a59c336b72d264e78
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519655"
---
# <a name="supplemental-credentials-attribute"></a><span data-ttu-id="431d8-107">Supplemental-Credentials-Attribut</span><span class="sxs-lookup"><span data-stu-id="431d8-107">Supplemental-Credentials attribute</span></span>

<span data-ttu-id="431d8-108">Gespeicherte Anmelde Informationen für die Verwendung bei der Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="431d8-108">Stored credentials for use in authenticating.</span></span> <span data-ttu-id="431d8-109">Die verschlüsselte Version des Benutzer Kennworts.</span><span class="sxs-lookup"><span data-stu-id="431d8-109">The encrypted version of the user's password.</span></span> <span data-ttu-id="431d8-110">Dieses Attribut ist weder lesbar noch beschreibbar.</span><span class="sxs-lookup"><span data-stu-id="431d8-110">This attribute is neither readable nor writable.</span></span>



| <span data-ttu-id="431d8-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="431d8-111">Entry</span></span> | <span data-ttu-id="431d8-112">Wert</span><span class="sxs-lookup"><span data-stu-id="431d8-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="431d8-113">CN</span><span class="sxs-lookup"><span data-stu-id="431d8-113">CN</span></span>                | <span data-ttu-id="431d8-114">Supplemental-Credentials</span><span class="sxs-lookup"><span data-stu-id="431d8-114">Supplemental-Credentials</span></span>                              |
| <span data-ttu-id="431d8-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="431d8-115">Ldap-Display-Name</span></span> | <span data-ttu-id="431d8-116">ergänzende Anmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="431d8-116">supplementalCredentials</span></span>                               |
| <span data-ttu-id="431d8-117">Size</span><span class="sxs-lookup"><span data-stu-id="431d8-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="431d8-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="431d8-118">Update Privilege</span></span>  | <span data-ttu-id="431d8-119">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="431d8-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="431d8-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="431d8-120">Update Frequency</span></span>  | <span data-ttu-id="431d8-121">Wenn das Kennwort des Benutzers geändert wird.</span><span class="sxs-lookup"><span data-stu-id="431d8-121">When the user's password changes.</span></span>                     |
| <span data-ttu-id="431d8-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="431d8-122">Attribute-Id</span></span>      | <span data-ttu-id="431d8-123">1.2.840.113556.1.4.125</span><span class="sxs-lookup"><span data-stu-id="431d8-123">1.2.840.113556.1.4.125</span></span>                                |
| <span data-ttu-id="431d8-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="431d8-124">System-Id-Guid</span></span>    | <span data-ttu-id="431d8-125">bf967a3f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="431d8-125">bf967a3f-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="431d8-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="431d8-126">Syntax</span></span>            | [<span data-ttu-id="431d8-127">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="431d8-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="431d8-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="431d8-128">Implementations</span></span>

-   [<span data-ttu-id="431d8-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="431d8-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="431d8-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="431d8-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="431d8-131">**Adam**</span><span class="sxs-lookup"><span data-stu-id="431d8-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="431d8-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="431d8-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="431d8-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="431d8-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="431d8-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="431d8-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="431d8-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="431d8-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="431d8-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="431d8-136">Windows 2000 Server</span></span>



| <span data-ttu-id="431d8-137">Eingabe</span><span class="sxs-lookup"><span data-stu-id="431d8-137">Entry</span></span> | <span data-ttu-id="431d8-138">Wert</span><span class="sxs-lookup"><span data-stu-id="431d8-138">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="431d8-139">Link-ID</span><span class="sxs-lookup"><span data-stu-id="431d8-139">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="431d8-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="431d8-140">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="431d8-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="431d8-141">System-Only</span></span>            | <span data-ttu-id="431d8-142">False</span><span class="sxs-lookup"><span data-stu-id="431d8-142">False</span></span>                                                        |
| <span data-ttu-id="431d8-143">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="431d8-143">Is-Single-Valued</span></span>       | <span data-ttu-id="431d8-144">False</span><span class="sxs-lookup"><span data-stu-id="431d8-144">False</span></span>                                                        |
| <span data-ttu-id="431d8-145">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="431d8-145">Is Indexed</span></span>             | <span data-ttu-id="431d8-146">False</span><span class="sxs-lookup"><span data-stu-id="431d8-146">False</span></span>                                                        |
| <span data-ttu-id="431d8-147">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="431d8-147">In Global Catalog</span></span>      | <span data-ttu-id="431d8-148">False</span><span class="sxs-lookup"><span data-stu-id="431d8-148">False</span></span>                                                        |
| <span data-ttu-id="431d8-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="431d8-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="431d8-150">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="431d8-150">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="431d8-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="431d8-151">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="431d8-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="431d8-152">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="431d8-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="431d8-153">Search-Flags</span></span>           | <span data-ttu-id="431d8-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="431d8-154">0x00000000</span></span>                                                   |
| <span data-ttu-id="431d8-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="431d8-155">System-Flags</span></span>           | <span data-ttu-id="431d8-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="431d8-156">0x00000010</span></span>                                                   |
| <span data-ttu-id="431d8-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="431d8-157">Classes used in</span></span>        | [<span data-ttu-id="431d8-158">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="431d8-158">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="431d8-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="431d8-159">Windows Server 2003</span></span>



| <span data-ttu-id="431d8-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="431d8-160">Entry</span></span> | <span data-ttu-id="431d8-161">Wert</span><span class="sxs-lookup"><span data-stu-id="431d8-161">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="431d8-162">Link-ID</span><span class="sxs-lookup"><span data-stu-id="431d8-162">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="431d8-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="431d8-163">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="431d8-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="431d8-164">System-Only</span></span>            | <span data-ttu-id="431d8-165">False</span><span class="sxs-lookup"><span data-stu-id="431d8-165">False</span></span>                                                        |
| <span data-ttu-id="431d8-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="431d8-166">Is-Single-Valued</span></span>       | <span data-ttu-id="431d8-167">False</span><span class="sxs-lookup"><span data-stu-id="431d8-167">False</span></span>                                                        |
| <span data-ttu-id="431d8-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="431d8-168">Is Indexed</span></span>             | <span data-ttu-id="431d8-169">False</span><span class="sxs-lookup"><span data-stu-id="431d8-169">False</span></span>                                                        |
| <span data-ttu-id="431d8-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="431d8-170">In Global Catalog</span></span>      | <span data-ttu-id="431d8-171">False</span><span class="sxs-lookup"><span data-stu-id="431d8-171">False</span></span>                                                        |
| <span data-ttu-id="431d8-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="431d8-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="431d8-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="431d8-173">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="431d8-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="431d8-174">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="431d8-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="431d8-175">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="431d8-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="431d8-176">Search-Flags</span></span>           | <span data-ttu-id="431d8-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="431d8-177">0x00000000</span></span>                                                   |
| <span data-ttu-id="431d8-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="431d8-178">System-Flags</span></span>           | <span data-ttu-id="431d8-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="431d8-179">0x00000010</span></span>                                                   |
| <span data-ttu-id="431d8-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="431d8-180">Classes used in</span></span>        | [<span data-ttu-id="431d8-181">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="431d8-181">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="adam"></a><span data-ttu-id="431d8-182">Adam</span><span class="sxs-lookup"><span data-stu-id="431d8-182">ADAM</span></span>



| <span data-ttu-id="431d8-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="431d8-183">Entry</span></span> | <span data-ttu-id="431d8-184">Wert</span><span class="sxs-lookup"><span data-stu-id="431d8-184">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="431d8-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="431d8-185">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="431d8-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="431d8-186">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="431d8-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="431d8-187">System-Only</span></span>            | <span data-ttu-id="431d8-188">False</span><span class="sxs-lookup"><span data-stu-id="431d8-188">False</span></span>                                                        |
| <span data-ttu-id="431d8-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="431d8-189">Is-Single-Valued</span></span>       | <span data-ttu-id="431d8-190">False</span><span class="sxs-lookup"><span data-stu-id="431d8-190">False</span></span>                                                        |
| <span data-ttu-id="431d8-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="431d8-191">Is Indexed</span></span>             | <span data-ttu-id="431d8-192">False</span><span class="sxs-lookup"><span data-stu-id="431d8-192">False</span></span>                                                        |
| <span data-ttu-id="431d8-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="431d8-193">In Global Catalog</span></span>      | <span data-ttu-id="431d8-194">False</span><span class="sxs-lookup"><span data-stu-id="431d8-194">False</span></span>                                                        |
| <span data-ttu-id="431d8-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="431d8-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="431d8-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="431d8-196">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="431d8-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="431d8-197">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="431d8-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="431d8-198">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="431d8-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="431d8-199">Search-Flags</span></span>           | <span data-ttu-id="431d8-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="431d8-200">0x00000000</span></span>                                                   |
| <span data-ttu-id="431d8-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="431d8-201">System-Flags</span></span>           | <span data-ttu-id="431d8-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="431d8-202">0x00000010</span></span>                                                   |
| <span data-ttu-id="431d8-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="431d8-203">Classes used in</span></span>        | [<span data-ttu-id="431d8-204">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="431d8-204">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="431d8-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="431d8-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="431d8-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="431d8-206">Entry</span></span> | <span data-ttu-id="431d8-207">Wert</span><span class="sxs-lookup"><span data-stu-id="431d8-207">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="431d8-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="431d8-208">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="431d8-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="431d8-209">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="431d8-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="431d8-210">System-Only</span></span>            | <span data-ttu-id="431d8-211">False</span><span class="sxs-lookup"><span data-stu-id="431d8-211">False</span></span>                                                        |
| <span data-ttu-id="431d8-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="431d8-212">Is-Single-Valued</span></span>       | <span data-ttu-id="431d8-213">False</span><span class="sxs-lookup"><span data-stu-id="431d8-213">False</span></span>                                                        |
| <span data-ttu-id="431d8-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="431d8-214">Is Indexed</span></span>             | <span data-ttu-id="431d8-215">False</span><span class="sxs-lookup"><span data-stu-id="431d8-215">False</span></span>                                                        |
| <span data-ttu-id="431d8-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="431d8-216">In Global Catalog</span></span>      | <span data-ttu-id="431d8-217">False</span><span class="sxs-lookup"><span data-stu-id="431d8-217">False</span></span>                                                        |
| <span data-ttu-id="431d8-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="431d8-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="431d8-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="431d8-219">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="431d8-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="431d8-220">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="431d8-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="431d8-221">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="431d8-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="431d8-222">Search-Flags</span></span>           | <span data-ttu-id="431d8-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="431d8-223">0x00000000</span></span>                                                   |
| <span data-ttu-id="431d8-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="431d8-224">System-Flags</span></span>           | <span data-ttu-id="431d8-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="431d8-225">0x00000010</span></span>                                                   |
| <span data-ttu-id="431d8-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="431d8-226">Classes used in</span></span>        | [<span data-ttu-id="431d8-227">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="431d8-227">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="431d8-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="431d8-228">Windows Server 2008</span></span>



| <span data-ttu-id="431d8-229">Eingabe</span><span class="sxs-lookup"><span data-stu-id="431d8-229">Entry</span></span> | <span data-ttu-id="431d8-230">Wert</span><span class="sxs-lookup"><span data-stu-id="431d8-230">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="431d8-231">Link-ID</span><span class="sxs-lookup"><span data-stu-id="431d8-231">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="431d8-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="431d8-232">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="431d8-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="431d8-233">System-Only</span></span>            | <span data-ttu-id="431d8-234">False</span><span class="sxs-lookup"><span data-stu-id="431d8-234">False</span></span>                                                        |
| <span data-ttu-id="431d8-235">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="431d8-235">Is-Single-Valued</span></span>       | <span data-ttu-id="431d8-236">False</span><span class="sxs-lookup"><span data-stu-id="431d8-236">False</span></span>                                                        |
| <span data-ttu-id="431d8-237">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="431d8-237">Is Indexed</span></span>             | <span data-ttu-id="431d8-238">False</span><span class="sxs-lookup"><span data-stu-id="431d8-238">False</span></span>                                                        |
| <span data-ttu-id="431d8-239">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="431d8-239">In Global Catalog</span></span>      | <span data-ttu-id="431d8-240">False</span><span class="sxs-lookup"><span data-stu-id="431d8-240">False</span></span>                                                        |
| <span data-ttu-id="431d8-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="431d8-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="431d8-242">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="431d8-242">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="431d8-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="431d8-243">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="431d8-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="431d8-244">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="431d8-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="431d8-245">Search-Flags</span></span>           | <span data-ttu-id="431d8-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="431d8-246">0x00000000</span></span>                                                   |
| <span data-ttu-id="431d8-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="431d8-247">System-Flags</span></span>           | <span data-ttu-id="431d8-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="431d8-248">0x00000010</span></span>                                                   |
| <span data-ttu-id="431d8-249">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="431d8-249">Classes used in</span></span>        | [<span data-ttu-id="431d8-250">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="431d8-250">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="431d8-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="431d8-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="431d8-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="431d8-252">Entry</span></span> | <span data-ttu-id="431d8-253">Wert</span><span class="sxs-lookup"><span data-stu-id="431d8-253">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="431d8-254">Link-ID</span><span class="sxs-lookup"><span data-stu-id="431d8-254">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="431d8-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="431d8-255">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="431d8-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="431d8-256">System-Only</span></span>            | <span data-ttu-id="431d8-257">False</span><span class="sxs-lookup"><span data-stu-id="431d8-257">False</span></span>                                                        |
| <span data-ttu-id="431d8-258">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="431d8-258">Is-Single-Valued</span></span>       | <span data-ttu-id="431d8-259">False</span><span class="sxs-lookup"><span data-stu-id="431d8-259">False</span></span>                                                        |
| <span data-ttu-id="431d8-260">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="431d8-260">Is Indexed</span></span>             | <span data-ttu-id="431d8-261">False</span><span class="sxs-lookup"><span data-stu-id="431d8-261">False</span></span>                                                        |
| <span data-ttu-id="431d8-262">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="431d8-262">In Global Catalog</span></span>      | <span data-ttu-id="431d8-263">False</span><span class="sxs-lookup"><span data-stu-id="431d8-263">False</span></span>                                                        |
| <span data-ttu-id="431d8-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="431d8-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="431d8-265">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="431d8-265">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="431d8-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="431d8-266">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="431d8-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="431d8-267">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="431d8-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="431d8-268">Search-Flags</span></span>           | <span data-ttu-id="431d8-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="431d8-269">0x00000000</span></span>                                                   |
| <span data-ttu-id="431d8-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="431d8-270">System-Flags</span></span>           | <span data-ttu-id="431d8-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="431d8-271">0x00000010</span></span>                                                   |
| <span data-ttu-id="431d8-272">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="431d8-272">Classes used in</span></span>        | [<span data-ttu-id="431d8-273">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="431d8-273">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="431d8-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="431d8-274">Windows Server 2012</span></span>



| <span data-ttu-id="431d8-275">Eingabe</span><span class="sxs-lookup"><span data-stu-id="431d8-275">Entry</span></span> | <span data-ttu-id="431d8-276">Wert</span><span class="sxs-lookup"><span data-stu-id="431d8-276">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="431d8-277">Link-ID</span><span class="sxs-lookup"><span data-stu-id="431d8-277">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="431d8-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="431d8-278">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="431d8-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="431d8-279">System-Only</span></span>            | <span data-ttu-id="431d8-280">False</span><span class="sxs-lookup"><span data-stu-id="431d8-280">False</span></span>                                                        |
| <span data-ttu-id="431d8-281">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="431d8-281">Is-Single-Valued</span></span>       | <span data-ttu-id="431d8-282">False</span><span class="sxs-lookup"><span data-stu-id="431d8-282">False</span></span>                                                        |
| <span data-ttu-id="431d8-283">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="431d8-283">Is Indexed</span></span>             | <span data-ttu-id="431d8-284">False</span><span class="sxs-lookup"><span data-stu-id="431d8-284">False</span></span>                                                        |
| <span data-ttu-id="431d8-285">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="431d8-285">In Global Catalog</span></span>      | <span data-ttu-id="431d8-286">False</span><span class="sxs-lookup"><span data-stu-id="431d8-286">False</span></span>                                                        |
| <span data-ttu-id="431d8-287">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="431d8-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="431d8-288">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="431d8-288">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="431d8-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="431d8-289">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="431d8-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="431d8-290">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="431d8-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="431d8-291">Search-Flags</span></span>           | <span data-ttu-id="431d8-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="431d8-292">0x00000000</span></span>                                                   |
| <span data-ttu-id="431d8-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="431d8-293">System-Flags</span></span>           | <span data-ttu-id="431d8-294">0x00000010</span><span class="sxs-lookup"><span data-stu-id="431d8-294">0x00000010</span></span>                                                   |
| <span data-ttu-id="431d8-295">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="431d8-295">Classes used in</span></span>        | [<span data-ttu-id="431d8-296">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="431d8-296">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





