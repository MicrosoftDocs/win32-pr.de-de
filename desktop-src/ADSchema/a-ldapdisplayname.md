---
title: LDAP-Display-Name-Attribut
description: Der Name, der von LDAP-Clients, z. b. dem ADSI LDAP-Anbieter, zum Lesen und Schreiben des Attributs mithilfe des LDAP-Protokolls verwendet wird.
ms.assetid: 9cb0b2f0-16cf-4fc6-85b2-d21ff71bc477
ms.tgt_platform: multiple
keywords:
- AD-Schema für LDAP-Display-Name-Attribut
- ldapDisplayName-Attribut AD-Schema
topic_type:
- apiref
api_name:
- LDAP-Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ffa25777ec4b5139a41ba9e56d8d5f0a9a3d92
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104213761"
---
# <a name="ldap-display-name-attribute"></a><span data-ttu-id="354d8-105">LDAP-Display-Name-Attribut</span><span class="sxs-lookup"><span data-stu-id="354d8-105">LDAP-Display-Name attribute</span></span>

<span data-ttu-id="354d8-106">Der Name, der von LDAP-Clients, z. b. dem ADSI LDAP-Anbieter, zum Lesen und Schreiben des Attributs mithilfe des LDAP-Protokolls verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="354d8-106">The name used by LDAP clients, such as the ADSI LDAP provider, to read and write the attribute by using the LDAP protocol.</span></span>



| <span data-ttu-id="354d8-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="354d8-107">Entry</span></span> | <span data-ttu-id="354d8-108">Wert</span><span class="sxs-lookup"><span data-stu-id="354d8-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="354d8-109">CN</span><span class="sxs-lookup"><span data-stu-id="354d8-109">CN</span></span>                | <span data-ttu-id="354d8-110">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="354d8-110">LDAP-Display-Name</span></span>                           |
| <span data-ttu-id="354d8-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="354d8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="354d8-112">lDAPDisplayName</span><span class="sxs-lookup"><span data-stu-id="354d8-112">lDAPDisplayName</span></span>                             |
| <span data-ttu-id="354d8-113">Size</span><span class="sxs-lookup"><span data-stu-id="354d8-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="354d8-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="354d8-114">Update Privilege</span></span>  | <span data-ttu-id="354d8-115">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="354d8-115">Schema administrator</span></span>                        |
| <span data-ttu-id="354d8-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="354d8-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="354d8-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="354d8-117">Attribute-Id</span></span>      | <span data-ttu-id="354d8-118">1.2.840.113556.1.2.460</span><span class="sxs-lookup"><span data-stu-id="354d8-118">1.2.840.113556.1.2.460</span></span>                      |
| <span data-ttu-id="354d8-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="354d8-119">System-Id-Guid</span></span>    | <span data-ttu-id="354d8-120">bf96799a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="354d8-120">bf96799a-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="354d8-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="354d8-121">Syntax</span></span>            | [<span data-ttu-id="354d8-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="354d8-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="354d8-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="354d8-123">Implementations</span></span>

-   [<span data-ttu-id="354d8-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="354d8-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="354d8-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="354d8-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="354d8-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="354d8-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="354d8-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="354d8-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="354d8-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="354d8-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="354d8-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="354d8-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="354d8-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="354d8-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="354d8-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="354d8-131">Windows 2000 Server</span></span>



| <span data-ttu-id="354d8-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="354d8-132">Entry</span></span> | <span data-ttu-id="354d8-133">Wert</span><span class="sxs-lookup"><span data-stu-id="354d8-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="354d8-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="354d8-134">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="354d8-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="354d8-135">MAPI-Id</span></span>                | <span data-ttu-id="354d8-136">0x8171</span><span class="sxs-lookup"><span data-stu-id="354d8-136">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="354d8-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="354d8-137">System-Only</span></span>            | <span data-ttu-id="354d8-138">False</span><span class="sxs-lookup"><span data-stu-id="354d8-138">False</span></span>                                                                                                     |
| <span data-ttu-id="354d8-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="354d8-139">Is-Single-Valued</span></span>       | <span data-ttu-id="354d8-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-140">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="354d8-141">Is Indexed</span></span>             | <span data-ttu-id="354d8-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-142">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="354d8-143">In Global Catalog</span></span>      | <span data-ttu-id="354d8-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-144">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="354d8-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="354d8-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="354d8-146">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="354d8-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="354d8-147">Range-Lower</span></span>            | <span data-ttu-id="354d8-148">1</span><span class="sxs-lookup"><span data-stu-id="354d8-148">1</span></span>                                                                                                         |
| <span data-ttu-id="354d8-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="354d8-149">Range-Upper</span></span>            | <span data-ttu-id="354d8-150">256</span><span class="sxs-lookup"><span data-stu-id="354d8-150">256</span></span>                                                                                                       |
| <span data-ttu-id="354d8-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="354d8-151">Search-Flags</span></span>           | <span data-ttu-id="354d8-152">0x00000009</span><span class="sxs-lookup"><span data-stu-id="354d8-152">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="354d8-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="354d8-153">System-Flags</span></span>           | <span data-ttu-id="354d8-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="354d8-154">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="354d8-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="354d8-155">Classes used in</span></span>        | [<span data-ttu-id="354d8-156">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="354d8-156">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="354d8-157">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="354d8-157">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="354d8-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="354d8-158">Windows Server 2003</span></span>



| <span data-ttu-id="354d8-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="354d8-159">Entry</span></span> | <span data-ttu-id="354d8-160">Wert</span><span class="sxs-lookup"><span data-stu-id="354d8-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="354d8-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="354d8-161">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="354d8-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="354d8-162">MAPI-Id</span></span>                | <span data-ttu-id="354d8-163">0x8171</span><span class="sxs-lookup"><span data-stu-id="354d8-163">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="354d8-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="354d8-164">System-Only</span></span>            | <span data-ttu-id="354d8-165">False</span><span class="sxs-lookup"><span data-stu-id="354d8-165">False</span></span>                                                                                                     |
| <span data-ttu-id="354d8-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="354d8-166">Is-Single-Valued</span></span>       | <span data-ttu-id="354d8-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-167">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="354d8-168">Is Indexed</span></span>             | <span data-ttu-id="354d8-169">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-169">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="354d8-170">In Global Catalog</span></span>      | <span data-ttu-id="354d8-171">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-171">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="354d8-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="354d8-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="354d8-173">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="354d8-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="354d8-174">Range-Lower</span></span>            | <span data-ttu-id="354d8-175">1</span><span class="sxs-lookup"><span data-stu-id="354d8-175">1</span></span>                                                                                                         |
| <span data-ttu-id="354d8-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="354d8-176">Range-Upper</span></span>            | <span data-ttu-id="354d8-177">256</span><span class="sxs-lookup"><span data-stu-id="354d8-177">256</span></span>                                                                                                       |
| <span data-ttu-id="354d8-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="354d8-178">Search-Flags</span></span>           | <span data-ttu-id="354d8-179">0x00000009</span><span class="sxs-lookup"><span data-stu-id="354d8-179">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="354d8-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="354d8-180">System-Flags</span></span>           | <span data-ttu-id="354d8-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="354d8-181">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="354d8-182">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="354d8-182">Classes used in</span></span>        | [<span data-ttu-id="354d8-183">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="354d8-183">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="354d8-184">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="354d8-184">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="354d8-185">Adam</span><span class="sxs-lookup"><span data-stu-id="354d8-185">ADAM</span></span>



| <span data-ttu-id="354d8-186">Eingabe</span><span class="sxs-lookup"><span data-stu-id="354d8-186">Entry</span></span> | <span data-ttu-id="354d8-187">Wert</span><span class="sxs-lookup"><span data-stu-id="354d8-187">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="354d8-188">Link-ID</span><span class="sxs-lookup"><span data-stu-id="354d8-188">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="354d8-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="354d8-189">MAPI-Id</span></span>                | <span data-ttu-id="354d8-190">0x8171</span><span class="sxs-lookup"><span data-stu-id="354d8-190">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="354d8-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="354d8-191">System-Only</span></span>            | <span data-ttu-id="354d8-192">False</span><span class="sxs-lookup"><span data-stu-id="354d8-192">False</span></span>                                                                                                     |
| <span data-ttu-id="354d8-193">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="354d8-193">Is-Single-Valued</span></span>       | <span data-ttu-id="354d8-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-194">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-195">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="354d8-195">Is Indexed</span></span>             | <span data-ttu-id="354d8-196">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-196">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-197">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="354d8-197">In Global Catalog</span></span>      | <span data-ttu-id="354d8-198">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-198">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="354d8-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="354d8-200">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="354d8-200">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="354d8-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="354d8-201">Range-Lower</span></span>            | <span data-ttu-id="354d8-202">1</span><span class="sxs-lookup"><span data-stu-id="354d8-202">1</span></span>                                                                                                         |
| <span data-ttu-id="354d8-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="354d8-203">Range-Upper</span></span>            | <span data-ttu-id="354d8-204">256</span><span class="sxs-lookup"><span data-stu-id="354d8-204">256</span></span>                                                                                                       |
| <span data-ttu-id="354d8-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="354d8-205">Search-Flags</span></span>           | <span data-ttu-id="354d8-206">0x00000009</span><span class="sxs-lookup"><span data-stu-id="354d8-206">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="354d8-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="354d8-207">System-Flags</span></span>           | <span data-ttu-id="354d8-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="354d8-208">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="354d8-209">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="354d8-209">Classes used in</span></span>        | [<span data-ttu-id="354d8-210">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="354d8-210">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="354d8-211">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="354d8-211">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="354d8-212">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="354d8-212">Windows Server 2003 R2</span></span>



| <span data-ttu-id="354d8-213">Eingabe</span><span class="sxs-lookup"><span data-stu-id="354d8-213">Entry</span></span> | <span data-ttu-id="354d8-214">Wert</span><span class="sxs-lookup"><span data-stu-id="354d8-214">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="354d8-215">Link-ID</span><span class="sxs-lookup"><span data-stu-id="354d8-215">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="354d8-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="354d8-216">MAPI-Id</span></span>                | <span data-ttu-id="354d8-217">0x8171</span><span class="sxs-lookup"><span data-stu-id="354d8-217">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="354d8-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="354d8-218">System-Only</span></span>            | <span data-ttu-id="354d8-219">False</span><span class="sxs-lookup"><span data-stu-id="354d8-219">False</span></span>                                                                                                     |
| <span data-ttu-id="354d8-220">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="354d8-220">Is-Single-Valued</span></span>       | <span data-ttu-id="354d8-221">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-221">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-222">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="354d8-222">Is Indexed</span></span>             | <span data-ttu-id="354d8-223">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-223">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-224">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="354d8-224">In Global Catalog</span></span>      | <span data-ttu-id="354d8-225">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-225">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-226">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="354d8-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="354d8-227">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="354d8-227">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="354d8-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="354d8-228">Range-Lower</span></span>            | <span data-ttu-id="354d8-229">1</span><span class="sxs-lookup"><span data-stu-id="354d8-229">1</span></span>                                                                                                         |
| <span data-ttu-id="354d8-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="354d8-230">Range-Upper</span></span>            | <span data-ttu-id="354d8-231">256</span><span class="sxs-lookup"><span data-stu-id="354d8-231">256</span></span>                                                                                                       |
| <span data-ttu-id="354d8-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="354d8-232">Search-Flags</span></span>           | <span data-ttu-id="354d8-233">0x00000009</span><span class="sxs-lookup"><span data-stu-id="354d8-233">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="354d8-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="354d8-234">System-Flags</span></span>           | <span data-ttu-id="354d8-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="354d8-235">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="354d8-236">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="354d8-236">Classes used in</span></span>        | [<span data-ttu-id="354d8-237">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="354d8-237">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="354d8-238">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="354d8-238">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="354d8-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="354d8-239">Windows Server 2008</span></span>



| <span data-ttu-id="354d8-240">Eingabe</span><span class="sxs-lookup"><span data-stu-id="354d8-240">Entry</span></span> | <span data-ttu-id="354d8-241">Wert</span><span class="sxs-lookup"><span data-stu-id="354d8-241">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="354d8-242">Link-ID</span><span class="sxs-lookup"><span data-stu-id="354d8-242">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="354d8-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="354d8-243">MAPI-Id</span></span>                | <span data-ttu-id="354d8-244">0x8171</span><span class="sxs-lookup"><span data-stu-id="354d8-244">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="354d8-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="354d8-245">System-Only</span></span>            | <span data-ttu-id="354d8-246">False</span><span class="sxs-lookup"><span data-stu-id="354d8-246">False</span></span>                                                                                                     |
| <span data-ttu-id="354d8-247">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="354d8-247">Is-Single-Valued</span></span>       | <span data-ttu-id="354d8-248">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-248">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-249">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="354d8-249">Is Indexed</span></span>             | <span data-ttu-id="354d8-250">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-250">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-251">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="354d8-251">In Global Catalog</span></span>      | <span data-ttu-id="354d8-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-252">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-253">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="354d8-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="354d8-254">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="354d8-254">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="354d8-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="354d8-255">Range-Lower</span></span>            | <span data-ttu-id="354d8-256">1</span><span class="sxs-lookup"><span data-stu-id="354d8-256">1</span></span>                                                                                                         |
| <span data-ttu-id="354d8-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="354d8-257">Range-Upper</span></span>            | <span data-ttu-id="354d8-258">256</span><span class="sxs-lookup"><span data-stu-id="354d8-258">256</span></span>                                                                                                       |
| <span data-ttu-id="354d8-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="354d8-259">Search-Flags</span></span>           | <span data-ttu-id="354d8-260">0x00000009</span><span class="sxs-lookup"><span data-stu-id="354d8-260">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="354d8-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="354d8-261">System-Flags</span></span>           | <span data-ttu-id="354d8-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="354d8-262">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="354d8-263">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="354d8-263">Classes used in</span></span>        | [<span data-ttu-id="354d8-264">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="354d8-264">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="354d8-265">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="354d8-265">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="354d8-266">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="354d8-266">Windows Server 2008 R2</span></span>



| <span data-ttu-id="354d8-267">Eingabe</span><span class="sxs-lookup"><span data-stu-id="354d8-267">Entry</span></span> | <span data-ttu-id="354d8-268">Wert</span><span class="sxs-lookup"><span data-stu-id="354d8-268">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="354d8-269">Link-ID</span><span class="sxs-lookup"><span data-stu-id="354d8-269">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="354d8-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="354d8-270">MAPI-Id</span></span>                | <span data-ttu-id="354d8-271">0x8171</span><span class="sxs-lookup"><span data-stu-id="354d8-271">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="354d8-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="354d8-272">System-Only</span></span>            | <span data-ttu-id="354d8-273">False</span><span class="sxs-lookup"><span data-stu-id="354d8-273">False</span></span>                                                                                                     |
| <span data-ttu-id="354d8-274">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="354d8-274">Is-Single-Valued</span></span>       | <span data-ttu-id="354d8-275">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-275">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-276">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="354d8-276">Is Indexed</span></span>             | <span data-ttu-id="354d8-277">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-277">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-278">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="354d8-278">In Global Catalog</span></span>      | <span data-ttu-id="354d8-279">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-279">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-280">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="354d8-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="354d8-281">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="354d8-281">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="354d8-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="354d8-282">Range-Lower</span></span>            | <span data-ttu-id="354d8-283">1</span><span class="sxs-lookup"><span data-stu-id="354d8-283">1</span></span>                                                                                                         |
| <span data-ttu-id="354d8-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="354d8-284">Range-Upper</span></span>            | <span data-ttu-id="354d8-285">256</span><span class="sxs-lookup"><span data-stu-id="354d8-285">256</span></span>                                                                                                       |
| <span data-ttu-id="354d8-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="354d8-286">Search-Flags</span></span>           | <span data-ttu-id="354d8-287">0x00000009</span><span class="sxs-lookup"><span data-stu-id="354d8-287">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="354d8-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="354d8-288">System-Flags</span></span>           | <span data-ttu-id="354d8-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="354d8-289">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="354d8-290">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="354d8-290">Classes used in</span></span>        | [<span data-ttu-id="354d8-291">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="354d8-291">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="354d8-292">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="354d8-292">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="354d8-293">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="354d8-293">Windows Server 2012</span></span>



| <span data-ttu-id="354d8-294">Eingabe</span><span class="sxs-lookup"><span data-stu-id="354d8-294">Entry</span></span> | <span data-ttu-id="354d8-295">Wert</span><span class="sxs-lookup"><span data-stu-id="354d8-295">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="354d8-296">Link-ID</span><span class="sxs-lookup"><span data-stu-id="354d8-296">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="354d8-297">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="354d8-297">MAPI-Id</span></span>                | <span data-ttu-id="354d8-298">0x8171</span><span class="sxs-lookup"><span data-stu-id="354d8-298">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="354d8-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="354d8-299">System-Only</span></span>            | <span data-ttu-id="354d8-300">False</span><span class="sxs-lookup"><span data-stu-id="354d8-300">False</span></span>                                                                                                     |
| <span data-ttu-id="354d8-301">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="354d8-301">Is-Single-Valued</span></span>       | <span data-ttu-id="354d8-302">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-302">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-303">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="354d8-303">Is Indexed</span></span>             | <span data-ttu-id="354d8-304">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-304">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-305">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="354d8-305">In Global Catalog</span></span>      | <span data-ttu-id="354d8-306">Richtig</span><span class="sxs-lookup"><span data-stu-id="354d8-306">True</span></span>                                                                                                      |
| <span data-ttu-id="354d8-307">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="354d8-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="354d8-308">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="354d8-308">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="354d8-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="354d8-309">Range-Lower</span></span>            | <span data-ttu-id="354d8-310">1</span><span class="sxs-lookup"><span data-stu-id="354d8-310">1</span></span>                                                                                                         |
| <span data-ttu-id="354d8-311">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="354d8-311">Range-Upper</span></span>            | <span data-ttu-id="354d8-312">256</span><span class="sxs-lookup"><span data-stu-id="354d8-312">256</span></span>                                                                                                       |
| <span data-ttu-id="354d8-313">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="354d8-313">Search-Flags</span></span>           | <span data-ttu-id="354d8-314">0x00000009</span><span class="sxs-lookup"><span data-stu-id="354d8-314">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="354d8-315">System-Flags</span><span class="sxs-lookup"><span data-stu-id="354d8-315">System-Flags</span></span>           | <span data-ttu-id="354d8-316">0x00000010</span><span class="sxs-lookup"><span data-stu-id="354d8-316">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="354d8-317">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="354d8-317">Classes used in</span></span>        | [<span data-ttu-id="354d8-318">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="354d8-318">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="354d8-319">**Class-Schema**</span><span class="sxs-lookup"><span data-stu-id="354d8-319">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





