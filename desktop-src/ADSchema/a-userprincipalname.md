---
title: Benutzer Prinzipal Name-Attribut
description: Dieses Attribut enthält den UPN, bei dem es sich um einen Anmelde Namen im Internet Format für einen Benutzer handelt, der auf dem Internet Standard RFC 822 basiert.
ms.assetid: 588e76fa-45b6-4853-821a-9e5730255b9f
ms.tgt_platform: multiple
keywords:
- AD-Schema für Benutzer Prinzipal Namen-Attribut
- userPrincipalName-Attribut AD-Schema
topic_type:
- apiref
api_name:
- User-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffdb5bde76325409e0911615d1d21b1b4f593c06
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957432"
---
# <a name="user-principal-name-attribute"></a><span data-ttu-id="72b3b-105">Benutzer Prinzipal Name-Attribut</span><span class="sxs-lookup"><span data-stu-id="72b3b-105">User-Principal-Name attribute</span></span>

<span data-ttu-id="72b3b-106">Dieses Attribut enthält den UPN, bei dem es sich um einen Anmelde Namen im Internet Format für einen Benutzer handelt, der auf dem Internet Standard [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)basiert.</span><span class="sxs-lookup"><span data-stu-id="72b3b-106">This attribute contains the UPN that is an Internet-style login name for a user based on the Internet standard [RFC 822](https://www.ietf.org/rfc/rfc0822.txt).</span></span> <span data-ttu-id="72b3b-107">Der UPN ist kürzer als der Distinguished Name und ist leichter zu merken.</span><span class="sxs-lookup"><span data-stu-id="72b3b-107">The UPN is shorter than the distinguished name and easier to remember.</span></span> <span data-ttu-id="72b3b-108">Gemäß der Konvention sollte dies dem e-Mail-Namen des Benutzers entsprechen.</span><span class="sxs-lookup"><span data-stu-id="72b3b-108">By convention, this should map to the user email name.</span></span> <span data-ttu-id="72b3b-109">Der für dieses Attribut festgelegte Wert ist gleich der Länge der Benutzer-ID und des Domänen Namens.</span><span class="sxs-lookup"><span data-stu-id="72b3b-109">The value set for this attribute is equal to the length of the user's ID and the domain name.</span></span> <span data-ttu-id="72b3b-110">Weitere Informationen zu diesem Attribut finden Sie unter [Benutzer Benennungs Attribute](/windows/desktop/AD/naming-properties).</span><span class="sxs-lookup"><span data-stu-id="72b3b-110">For more information about this attribute, see [User Naming Attributes](/windows/desktop/AD/naming-properties).</span></span>



| <span data-ttu-id="72b3b-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="72b3b-111">Entry</span></span> | <span data-ttu-id="72b3b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="72b3b-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="72b3b-113">CN</span><span class="sxs-lookup"><span data-stu-id="72b3b-113">CN</span></span>                | <span data-ttu-id="72b3b-114">Benutzerprinzipalname</span><span class="sxs-lookup"><span data-stu-id="72b3b-114">User-Principal-Name</span></span>                         |
| <span data-ttu-id="72b3b-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="72b3b-115">Ldap-Display-Name</span></span> | <span data-ttu-id="72b3b-116">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="72b3b-116">userPrincipalName</span></span>                           |
| <span data-ttu-id="72b3b-117">Size</span><span class="sxs-lookup"><span data-stu-id="72b3b-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="72b3b-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="72b3b-118">Update Privilege</span></span>  | <span data-ttu-id="72b3b-119">Domänen Administrator oder Konto Besitzer.</span><span class="sxs-lookup"><span data-stu-id="72b3b-119">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="72b3b-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="72b3b-120">Update Frequency</span></span>  | <span data-ttu-id="72b3b-121">Theoretisch sollte sich dies nie ändern.</span><span class="sxs-lookup"><span data-stu-id="72b3b-121">In theory this should never change.</span></span>         |
| <span data-ttu-id="72b3b-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="72b3b-122">Attribute-Id</span></span>      | <span data-ttu-id="72b3b-123">1.2.840.113556.1.4.656</span><span class="sxs-lookup"><span data-stu-id="72b3b-123">1.2.840.113556.1.4.656</span></span>                      |
| <span data-ttu-id="72b3b-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="72b3b-124">System-Id-Guid</span></span>    | <span data-ttu-id="72b3b-125">28630ebb-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="72b3b-125">28630ebb-41d5-11d1-a9c1-0000f80367c1</span></span>        |
| <span data-ttu-id="72b3b-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="72b3b-126">Syntax</span></span>            | [<span data-ttu-id="72b3b-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="72b3b-127">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="72b3b-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="72b3b-128">Implementations</span></span>

-   [<span data-ttu-id="72b3b-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="72b3b-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="72b3b-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="72b3b-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="72b3b-131">**Adam**</span><span class="sxs-lookup"><span data-stu-id="72b3b-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="72b3b-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="72b3b-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="72b3b-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="72b3b-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="72b3b-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="72b3b-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="72b3b-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="72b3b-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="72b3b-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="72b3b-136">Windows 2000 Server</span></span>



| <span data-ttu-id="72b3b-137">Eingabe</span><span class="sxs-lookup"><span data-stu-id="72b3b-137">Entry</span></span> | <span data-ttu-id="72b3b-138">Wert</span><span class="sxs-lookup"><span data-stu-id="72b3b-138">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="72b3b-139">Link-ID</span><span class="sxs-lookup"><span data-stu-id="72b3b-139">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="72b3b-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72b3b-140">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="72b3b-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="72b3b-141">System-Only</span></span>            | <span data-ttu-id="72b3b-142">False</span><span class="sxs-lookup"><span data-stu-id="72b3b-142">False</span></span>                             |
| <span data-ttu-id="72b3b-143">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="72b3b-143">Is-Single-Valued</span></span>       | <span data-ttu-id="72b3b-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-144">True</span></span>                              |
| <span data-ttu-id="72b3b-145">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="72b3b-145">Is Indexed</span></span>             | <span data-ttu-id="72b3b-146">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-146">True</span></span>                              |
| <span data-ttu-id="72b3b-147">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="72b3b-147">In Global Catalog</span></span>      | <span data-ttu-id="72b3b-148">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-148">True</span></span>                              |
| <span data-ttu-id="72b3b-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72b3b-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="72b3b-150">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="72b3b-150">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="72b3b-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72b3b-151">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="72b3b-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72b3b-152">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="72b3b-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72b3b-153">Search-Flags</span></span>           | <span data-ttu-id="72b3b-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72b3b-154">0x00000001</span></span>                        |
| <span data-ttu-id="72b3b-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72b3b-155">System-Flags</span></span>           | <span data-ttu-id="72b3b-156">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72b3b-156">0x00000012</span></span>                        |
| <span data-ttu-id="72b3b-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="72b3b-157">Classes used in</span></span>        | [<span data-ttu-id="72b3b-158">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="72b3b-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="72b3b-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72b3b-159">Windows Server 2003</span></span>



| <span data-ttu-id="72b3b-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="72b3b-160">Entry</span></span> | <span data-ttu-id="72b3b-161">Wert</span><span class="sxs-lookup"><span data-stu-id="72b3b-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="72b3b-162">Link-ID</span><span class="sxs-lookup"><span data-stu-id="72b3b-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="72b3b-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72b3b-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="72b3b-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="72b3b-164">System-Only</span></span>            | <span data-ttu-id="72b3b-165">False</span><span class="sxs-lookup"><span data-stu-id="72b3b-165">False</span></span>                             |
| <span data-ttu-id="72b3b-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="72b3b-166">Is-Single-Valued</span></span>       | <span data-ttu-id="72b3b-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-167">True</span></span>                              |
| <span data-ttu-id="72b3b-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="72b3b-168">Is Indexed</span></span>             | <span data-ttu-id="72b3b-169">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-169">True</span></span>                              |
| <span data-ttu-id="72b3b-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="72b3b-170">In Global Catalog</span></span>      | <span data-ttu-id="72b3b-171">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-171">True</span></span>                              |
| <span data-ttu-id="72b3b-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72b3b-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="72b3b-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="72b3b-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="72b3b-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72b3b-174">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="72b3b-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72b3b-175">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="72b3b-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72b3b-176">Search-Flags</span></span>           | <span data-ttu-id="72b3b-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72b3b-177">0x00000001</span></span>                        |
| <span data-ttu-id="72b3b-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72b3b-178">System-Flags</span></span>           | <span data-ttu-id="72b3b-179">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72b3b-179">0x00000012</span></span>                        |
| <span data-ttu-id="72b3b-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="72b3b-180">Classes used in</span></span>        | [<span data-ttu-id="72b3b-181">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="72b3b-181">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="72b3b-182">Adam</span><span class="sxs-lookup"><span data-stu-id="72b3b-182">ADAM</span></span>



| <span data-ttu-id="72b3b-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="72b3b-183">Entry</span></span> | <span data-ttu-id="72b3b-184">Wert</span><span class="sxs-lookup"><span data-stu-id="72b3b-184">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="72b3b-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="72b3b-185">Link-Id</span></span>                | \-           |
| <span data-ttu-id="72b3b-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72b3b-186">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="72b3b-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="72b3b-187">System-Only</span></span>            | <span data-ttu-id="72b3b-188">False</span><span class="sxs-lookup"><span data-stu-id="72b3b-188">False</span></span>        |
| <span data-ttu-id="72b3b-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="72b3b-189">Is-Single-Valued</span></span>       | <span data-ttu-id="72b3b-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-190">True</span></span>         |
| <span data-ttu-id="72b3b-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="72b3b-191">Is Indexed</span></span>             | <span data-ttu-id="72b3b-192">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-192">True</span></span>         |
| <span data-ttu-id="72b3b-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="72b3b-193">In Global Catalog</span></span>      | <span data-ttu-id="72b3b-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-194">True</span></span>         |
| <span data-ttu-id="72b3b-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72b3b-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="72b3b-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="72b3b-196">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="72b3b-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72b3b-197">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="72b3b-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72b3b-198">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="72b3b-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72b3b-199">Search-Flags</span></span>           | <span data-ttu-id="72b3b-200">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72b3b-200">0x00000001</span></span>   |
| <span data-ttu-id="72b3b-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72b3b-201">System-Flags</span></span>           | <span data-ttu-id="72b3b-202">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72b3b-202">0x00000012</span></span>   |
| <span data-ttu-id="72b3b-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="72b3b-203">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="72b3b-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="72b3b-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="72b3b-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="72b3b-205">Entry</span></span> | <span data-ttu-id="72b3b-206">Wert</span><span class="sxs-lookup"><span data-stu-id="72b3b-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="72b3b-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="72b3b-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="72b3b-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72b3b-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="72b3b-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="72b3b-209">System-Only</span></span>            | <span data-ttu-id="72b3b-210">False</span><span class="sxs-lookup"><span data-stu-id="72b3b-210">False</span></span>                             |
| <span data-ttu-id="72b3b-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="72b3b-211">Is-Single-Valued</span></span>       | <span data-ttu-id="72b3b-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-212">True</span></span>                              |
| <span data-ttu-id="72b3b-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="72b3b-213">Is Indexed</span></span>             | <span data-ttu-id="72b3b-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-214">True</span></span>                              |
| <span data-ttu-id="72b3b-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="72b3b-215">In Global Catalog</span></span>      | <span data-ttu-id="72b3b-216">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-216">True</span></span>                              |
| <span data-ttu-id="72b3b-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72b3b-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="72b3b-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="72b3b-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="72b3b-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72b3b-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="72b3b-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72b3b-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="72b3b-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72b3b-221">Search-Flags</span></span>           | <span data-ttu-id="72b3b-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72b3b-222">0x00000001</span></span>                        |
| <span data-ttu-id="72b3b-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72b3b-223">System-Flags</span></span>           | <span data-ttu-id="72b3b-224">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72b3b-224">0x00000012</span></span>                        |
| <span data-ttu-id="72b3b-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="72b3b-225">Classes used in</span></span>        | [<span data-ttu-id="72b3b-226">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="72b3b-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="72b3b-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72b3b-227">Windows Server 2008</span></span>



| <span data-ttu-id="72b3b-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="72b3b-228">Entry</span></span> | <span data-ttu-id="72b3b-229">Wert</span><span class="sxs-lookup"><span data-stu-id="72b3b-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="72b3b-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="72b3b-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="72b3b-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72b3b-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="72b3b-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="72b3b-232">System-Only</span></span>            | <span data-ttu-id="72b3b-233">False</span><span class="sxs-lookup"><span data-stu-id="72b3b-233">False</span></span>                             |
| <span data-ttu-id="72b3b-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="72b3b-234">Is-Single-Valued</span></span>       | <span data-ttu-id="72b3b-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-235">True</span></span>                              |
| <span data-ttu-id="72b3b-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="72b3b-236">Is Indexed</span></span>             | <span data-ttu-id="72b3b-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-237">True</span></span>                              |
| <span data-ttu-id="72b3b-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="72b3b-238">In Global Catalog</span></span>      | <span data-ttu-id="72b3b-239">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-239">True</span></span>                              |
| <span data-ttu-id="72b3b-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72b3b-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="72b3b-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="72b3b-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="72b3b-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72b3b-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="72b3b-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72b3b-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="72b3b-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72b3b-244">Search-Flags</span></span>           | <span data-ttu-id="72b3b-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72b3b-245">0x00000001</span></span>                        |
| <span data-ttu-id="72b3b-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72b3b-246">System-Flags</span></span>           | <span data-ttu-id="72b3b-247">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72b3b-247">0x00000012</span></span>                        |
| <span data-ttu-id="72b3b-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="72b3b-248">Classes used in</span></span>        | [<span data-ttu-id="72b3b-249">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="72b3b-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="72b3b-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72b3b-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="72b3b-251">Eingabe</span><span class="sxs-lookup"><span data-stu-id="72b3b-251">Entry</span></span> | <span data-ttu-id="72b3b-252">Wert</span><span class="sxs-lookup"><span data-stu-id="72b3b-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="72b3b-253">Link-ID</span><span class="sxs-lookup"><span data-stu-id="72b3b-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="72b3b-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72b3b-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="72b3b-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="72b3b-255">System-Only</span></span>            | <span data-ttu-id="72b3b-256">False</span><span class="sxs-lookup"><span data-stu-id="72b3b-256">False</span></span>                             |
| <span data-ttu-id="72b3b-257">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="72b3b-257">Is-Single-Valued</span></span>       | <span data-ttu-id="72b3b-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-258">True</span></span>                              |
| <span data-ttu-id="72b3b-259">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="72b3b-259">Is Indexed</span></span>             | <span data-ttu-id="72b3b-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-260">True</span></span>                              |
| <span data-ttu-id="72b3b-261">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="72b3b-261">In Global Catalog</span></span>      | <span data-ttu-id="72b3b-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-262">True</span></span>                              |
| <span data-ttu-id="72b3b-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72b3b-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="72b3b-264">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="72b3b-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="72b3b-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72b3b-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="72b3b-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72b3b-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="72b3b-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72b3b-267">Search-Flags</span></span>           | <span data-ttu-id="72b3b-268">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72b3b-268">0x00000001</span></span>                        |
| <span data-ttu-id="72b3b-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72b3b-269">System-Flags</span></span>           | <span data-ttu-id="72b3b-270">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72b3b-270">0x00000012</span></span>                        |
| <span data-ttu-id="72b3b-271">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="72b3b-271">Classes used in</span></span>        | [<span data-ttu-id="72b3b-272">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="72b3b-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="72b3b-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72b3b-273">Windows Server 2012</span></span>



| <span data-ttu-id="72b3b-274">Eingabe</span><span class="sxs-lookup"><span data-stu-id="72b3b-274">Entry</span></span> | <span data-ttu-id="72b3b-275">Wert</span><span class="sxs-lookup"><span data-stu-id="72b3b-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="72b3b-276">Link-ID</span><span class="sxs-lookup"><span data-stu-id="72b3b-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="72b3b-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72b3b-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="72b3b-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="72b3b-278">System-Only</span></span>            | <span data-ttu-id="72b3b-279">False</span><span class="sxs-lookup"><span data-stu-id="72b3b-279">False</span></span>                             |
| <span data-ttu-id="72b3b-280">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="72b3b-280">Is-Single-Valued</span></span>       | <span data-ttu-id="72b3b-281">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-281">True</span></span>                              |
| <span data-ttu-id="72b3b-282">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="72b3b-282">Is Indexed</span></span>             | <span data-ttu-id="72b3b-283">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-283">True</span></span>                              |
| <span data-ttu-id="72b3b-284">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="72b3b-284">In Global Catalog</span></span>      | <span data-ttu-id="72b3b-285">Richtig</span><span class="sxs-lookup"><span data-stu-id="72b3b-285">True</span></span>                              |
| <span data-ttu-id="72b3b-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72b3b-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="72b3b-287">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="72b3b-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="72b3b-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72b3b-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="72b3b-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72b3b-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="72b3b-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72b3b-290">Search-Flags</span></span>           | <span data-ttu-id="72b3b-291">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72b3b-291">0x00000001</span></span>                        |
| <span data-ttu-id="72b3b-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72b3b-292">System-Flags</span></span>           | <span data-ttu-id="72b3b-293">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72b3b-293">0x00000012</span></span>                        |
| <span data-ttu-id="72b3b-294">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="72b3b-294">Classes used in</span></span>        | [<span data-ttu-id="72b3b-295">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="72b3b-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="72b3b-296">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72b3b-296">Remarks</span></span>

<span data-ttu-id="72b3b-297">In Adam muss dieses Attribut nicht im Internet Standard RFC 822-Format vorliegen. Dies kann ein einfacher Name sein.</span><span class="sxs-lookup"><span data-stu-id="72b3b-297">In ADAM, this attribute is not required to be in the Internet standard RFC 822 format; it can be a simple name.</span></span>

 

