---
title: Logon-Hours-Attribut
description: Die Stunden, die der Benutzer für die Anmeldung bei der Domäne berechtigt ist.
ms.assetid: b97cc8b0-7f26-45c1-b1c9-bae6467bdfb6
ms.tgt_platform: multiple
keywords:
- AD-Schema für Logon-Hours-Attribut
- LogonHours-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Logon-Hours
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f764192ac57efdb1f14d55f691183240f0eddfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479770"
---
# <a name="logon-hours-attribute"></a><span data-ttu-id="0fce0-105">Logon-Hours-Attribut</span><span class="sxs-lookup"><span data-stu-id="0fce0-105">Logon-Hours attribute</span></span>

<span data-ttu-id="0fce0-106">Die Stunden, die der Benutzer für die Anmeldung bei der Domäne berechtigt ist.</span><span class="sxs-lookup"><span data-stu-id="0fce0-106">The hours that the user is allowed to logon to the domain.</span></span>



| <span data-ttu-id="0fce0-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0fce0-107">Entry</span></span> | <span data-ttu-id="0fce0-108">Wert</span><span class="sxs-lookup"><span data-stu-id="0fce0-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="0fce0-109">CN</span><span class="sxs-lookup"><span data-stu-id="0fce0-109">CN</span></span>                | <span data-ttu-id="0fce0-110">Logon-Hours</span><span class="sxs-lookup"><span data-stu-id="0fce0-110">Logon-Hours</span></span>                                           |
| <span data-ttu-id="0fce0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0fce0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0fce0-112">LogonHours</span><span class="sxs-lookup"><span data-stu-id="0fce0-112">logonHours</span></span>                                            |
| <span data-ttu-id="0fce0-113">Size</span><span class="sxs-lookup"><span data-stu-id="0fce0-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="0fce0-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0fce0-114">Update Privilege</span></span>  | <span data-ttu-id="0fce0-115">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="0fce0-115">Domain administrator</span></span>                                  |
| <span data-ttu-id="0fce0-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="0fce0-116">Update Frequency</span></span>  | <span data-ttu-id="0fce0-117">Immer, wenn die Anmeldezeiten des Kontos geändert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0fce0-117">Whenever the account's logon hours needs to change.</span></span>   |
| <span data-ttu-id="0fce0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0fce0-118">Attribute-Id</span></span>      | <span data-ttu-id="0fce0-119">1.2.840.113556.1.4.64</span><span class="sxs-lookup"><span data-stu-id="0fce0-119">1.2.840.113556.1.4.64</span></span>                                 |
| <span data-ttu-id="0fce0-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0fce0-120">System-Id-Guid</span></span>    | <span data-ttu-id="0fce0-121">bf9679ab-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0fce0-121">bf9679ab-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="0fce0-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fce0-122">Syntax</span></span>            | [<span data-ttu-id="0fce0-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="0fce0-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="0fce0-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="0fce0-124">Implementations</span></span>

-   [<span data-ttu-id="0fce0-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0fce0-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0fce0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0fce0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0fce0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0fce0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0fce0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0fce0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0fce0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0fce0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0fce0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0fce0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0fce0-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0fce0-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0fce0-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0fce0-132">Entry</span></span> | <span data-ttu-id="0fce0-133">Wert</span><span class="sxs-lookup"><span data-stu-id="0fce0-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0fce0-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0fce0-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0fce0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0fce0-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0fce0-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0fce0-136">System-Only</span></span>            | <span data-ttu-id="0fce0-137">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-137">False</span></span>                             |
| <span data-ttu-id="0fce0-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0fce0-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0fce0-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="0fce0-139">True</span></span>                              |
| <span data-ttu-id="0fce0-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0fce0-140">Is Indexed</span></span>             | <span data-ttu-id="0fce0-141">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-141">False</span></span>                             |
| <span data-ttu-id="0fce0-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0fce0-142">In Global Catalog</span></span>      | <span data-ttu-id="0fce0-143">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-143">False</span></span>                             |
| <span data-ttu-id="0fce0-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0fce0-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0fce0-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0fce0-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0fce0-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0fce0-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0fce0-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0fce0-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0fce0-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0fce0-148">Search-Flags</span></span>           | <span data-ttu-id="0fce0-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0fce0-149">0x00000010</span></span>                        |
| <span data-ttu-id="0fce0-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0fce0-150">System-Flags</span></span>           | <span data-ttu-id="0fce0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0fce0-151">0x00000010</span></span>                        |
| <span data-ttu-id="0fce0-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0fce0-152">Classes used in</span></span>        | [<span data-ttu-id="0fce0-153">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="0fce0-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0fce0-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0fce0-154">Windows Server 2003</span></span>



| <span data-ttu-id="0fce0-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0fce0-155">Entry</span></span> | <span data-ttu-id="0fce0-156">Wert</span><span class="sxs-lookup"><span data-stu-id="0fce0-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0fce0-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0fce0-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0fce0-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0fce0-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0fce0-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="0fce0-159">System-Only</span></span>            | <span data-ttu-id="0fce0-160">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-160">False</span></span>                             |
| <span data-ttu-id="0fce0-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0fce0-161">Is-Single-Valued</span></span>       | <span data-ttu-id="0fce0-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="0fce0-162">True</span></span>                              |
| <span data-ttu-id="0fce0-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0fce0-163">Is Indexed</span></span>             | <span data-ttu-id="0fce0-164">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-164">False</span></span>                             |
| <span data-ttu-id="0fce0-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0fce0-165">In Global Catalog</span></span>      | <span data-ttu-id="0fce0-166">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-166">False</span></span>                             |
| <span data-ttu-id="0fce0-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0fce0-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="0fce0-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0fce0-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0fce0-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0fce0-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0fce0-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0fce0-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0fce0-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0fce0-171">Search-Flags</span></span>           | <span data-ttu-id="0fce0-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0fce0-172">0x00000010</span></span>                        |
| <span data-ttu-id="0fce0-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0fce0-173">System-Flags</span></span>           | <span data-ttu-id="0fce0-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0fce0-174">0x00000010</span></span>                        |
| <span data-ttu-id="0fce0-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0fce0-175">Classes used in</span></span>        | [<span data-ttu-id="0fce0-176">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="0fce0-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0fce0-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0fce0-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0fce0-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0fce0-178">Entry</span></span> | <span data-ttu-id="0fce0-179">Wert</span><span class="sxs-lookup"><span data-stu-id="0fce0-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0fce0-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0fce0-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0fce0-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0fce0-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0fce0-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="0fce0-182">System-Only</span></span>            | <span data-ttu-id="0fce0-183">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-183">False</span></span>                             |
| <span data-ttu-id="0fce0-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0fce0-184">Is-Single-Valued</span></span>       | <span data-ttu-id="0fce0-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="0fce0-185">True</span></span>                              |
| <span data-ttu-id="0fce0-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0fce0-186">Is Indexed</span></span>             | <span data-ttu-id="0fce0-187">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-187">False</span></span>                             |
| <span data-ttu-id="0fce0-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0fce0-188">In Global Catalog</span></span>      | <span data-ttu-id="0fce0-189">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-189">False</span></span>                             |
| <span data-ttu-id="0fce0-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0fce0-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="0fce0-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0fce0-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0fce0-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0fce0-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0fce0-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0fce0-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0fce0-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0fce0-194">Search-Flags</span></span>           | <span data-ttu-id="0fce0-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0fce0-195">0x00000010</span></span>                        |
| <span data-ttu-id="0fce0-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0fce0-196">System-Flags</span></span>           | <span data-ttu-id="0fce0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0fce0-197">0x00000010</span></span>                        |
| <span data-ttu-id="0fce0-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0fce0-198">Classes used in</span></span>        | [<span data-ttu-id="0fce0-199">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="0fce0-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0fce0-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fce0-200">Windows Server 2008</span></span>



| <span data-ttu-id="0fce0-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0fce0-201">Entry</span></span> | <span data-ttu-id="0fce0-202">Wert</span><span class="sxs-lookup"><span data-stu-id="0fce0-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0fce0-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0fce0-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0fce0-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0fce0-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0fce0-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="0fce0-205">System-Only</span></span>            | <span data-ttu-id="0fce0-206">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-206">False</span></span>                             |
| <span data-ttu-id="0fce0-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0fce0-207">Is-Single-Valued</span></span>       | <span data-ttu-id="0fce0-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="0fce0-208">True</span></span>                              |
| <span data-ttu-id="0fce0-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0fce0-209">Is Indexed</span></span>             | <span data-ttu-id="0fce0-210">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-210">False</span></span>                             |
| <span data-ttu-id="0fce0-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0fce0-211">In Global Catalog</span></span>      | <span data-ttu-id="0fce0-212">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-212">False</span></span>                             |
| <span data-ttu-id="0fce0-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0fce0-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="0fce0-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0fce0-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0fce0-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0fce0-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0fce0-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0fce0-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0fce0-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0fce0-217">Search-Flags</span></span>           | <span data-ttu-id="0fce0-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0fce0-218">0x00000010</span></span>                        |
| <span data-ttu-id="0fce0-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0fce0-219">System-Flags</span></span>           | <span data-ttu-id="0fce0-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0fce0-220">0x00000010</span></span>                        |
| <span data-ttu-id="0fce0-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0fce0-221">Classes used in</span></span>        | [<span data-ttu-id="0fce0-222">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="0fce0-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0fce0-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0fce0-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0fce0-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0fce0-224">Entry</span></span> | <span data-ttu-id="0fce0-225">Wert</span><span class="sxs-lookup"><span data-stu-id="0fce0-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0fce0-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0fce0-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0fce0-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0fce0-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0fce0-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="0fce0-228">System-Only</span></span>            | <span data-ttu-id="0fce0-229">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-229">False</span></span>                             |
| <span data-ttu-id="0fce0-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0fce0-230">Is-Single-Valued</span></span>       | <span data-ttu-id="0fce0-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="0fce0-231">True</span></span>                              |
| <span data-ttu-id="0fce0-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0fce0-232">Is Indexed</span></span>             | <span data-ttu-id="0fce0-233">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-233">False</span></span>                             |
| <span data-ttu-id="0fce0-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0fce0-234">In Global Catalog</span></span>      | <span data-ttu-id="0fce0-235">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-235">False</span></span>                             |
| <span data-ttu-id="0fce0-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0fce0-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="0fce0-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0fce0-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0fce0-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0fce0-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0fce0-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0fce0-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0fce0-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0fce0-240">Search-Flags</span></span>           | <span data-ttu-id="0fce0-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0fce0-241">0x00000010</span></span>                        |
| <span data-ttu-id="0fce0-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0fce0-242">System-Flags</span></span>           | <span data-ttu-id="0fce0-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0fce0-243">0x00000010</span></span>                        |
| <span data-ttu-id="0fce0-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0fce0-244">Classes used in</span></span>        | [<span data-ttu-id="0fce0-245">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="0fce0-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0fce0-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0fce0-246">Windows Server 2012</span></span>



| <span data-ttu-id="0fce0-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0fce0-247">Entry</span></span> | <span data-ttu-id="0fce0-248">Wert</span><span class="sxs-lookup"><span data-stu-id="0fce0-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0fce0-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0fce0-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0fce0-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0fce0-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0fce0-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="0fce0-251">System-Only</span></span>            | <span data-ttu-id="0fce0-252">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-252">False</span></span>                             |
| <span data-ttu-id="0fce0-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0fce0-253">Is-Single-Valued</span></span>       | <span data-ttu-id="0fce0-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="0fce0-254">True</span></span>                              |
| <span data-ttu-id="0fce0-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0fce0-255">Is Indexed</span></span>             | <span data-ttu-id="0fce0-256">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-256">False</span></span>                             |
| <span data-ttu-id="0fce0-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0fce0-257">In Global Catalog</span></span>      | <span data-ttu-id="0fce0-258">False</span><span class="sxs-lookup"><span data-stu-id="0fce0-258">False</span></span>                             |
| <span data-ttu-id="0fce0-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0fce0-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="0fce0-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0fce0-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0fce0-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0fce0-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0fce0-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0fce0-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0fce0-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0fce0-263">Search-Flags</span></span>           | <span data-ttu-id="0fce0-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0fce0-264">0x00000010</span></span>                        |
| <span data-ttu-id="0fce0-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0fce0-265">System-Flags</span></span>           | <span data-ttu-id="0fce0-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0fce0-266">0x00000010</span></span>                        |
| <span data-ttu-id="0fce0-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0fce0-267">Classes used in</span></span>        | [<span data-ttu-id="0fce0-268">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="0fce0-268">**User**</span></span>](c-user.md)<br/> |



 

 





