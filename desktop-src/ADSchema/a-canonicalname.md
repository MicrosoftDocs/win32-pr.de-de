---
title: Canonical-Name-Attribut
description: Der Name des Objekts im kanonischen Format.
ms.assetid: f217e5fa-f70b-4f4d-afa6-53e4f7e8a0e1
ms.tgt_platform: multiple
keywords:
- AD-Schema für Canonical-Name-Attribut
- CanonicalName-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Canonical-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 487476271456fa0465e8d47791f5376f33617eb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859898"
---
# <a name="canonical-name-attribute"></a><span data-ttu-id="6cb9b-105">Canonical-Name-Attribut</span><span class="sxs-lookup"><span data-stu-id="6cb9b-105">Canonical-Name attribute</span></span>

<span data-ttu-id="6cb9b-106">Der Name des Objekts im kanonischen Format.</span><span class="sxs-lookup"><span data-stu-id="6cb9b-106">The name of the object in canonical format.</span></span> <span data-ttu-id="6cb9b-107">myserver2.fabrikam.com/users/JeffSmith ist ein Beispiel für einen Distinguished Name im kanonischen Format.</span><span class="sxs-lookup"><span data-stu-id="6cb9b-107">myserver2.fabrikam.com/users/jeffsmith is an example of a distinguished name in canonical format.</span></span> <span data-ttu-id="6cb9b-108">Dies ist ein konstruiertes Attribut.</span><span class="sxs-lookup"><span data-stu-id="6cb9b-108">This is a constructed attribute.</span></span> <span data-ttu-id="6cb9b-109">Die zurückgegebenen Ergebnisse sind identisch mit denen, die von der folgenden Active Directory-Funktion zurückgegeben werden: DsCrackNames (null, DS- \_ \_ namensflag \_ syntaktisch \_ only, DS \_ FQDN \_ 1779 \_ Name, DS \_ kanonischer \_ Name,...).</span><span class="sxs-lookup"><span data-stu-id="6cb9b-109">The results returned are identical to those returned by the following Active Directory function: DsCrackNames(NULL, DS\_NAME\_FLAG\_SYNTACTICAL\_ONLY, DS\_FQDN\_1779\_NAME, DS\_CANONICAL\_NAME, ...).</span></span>

<span data-ttu-id="6cb9b-110">Weitere Informationen zu namens Formaten finden Sie unter [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).</span><span class="sxs-lookup"><span data-stu-id="6cb9b-110">For more information about name formats, see [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).</span></span>



| <span data-ttu-id="6cb9b-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6cb9b-111">Entry</span></span> | <span data-ttu-id="6cb9b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="6cb9b-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6cb9b-113">CN</span><span class="sxs-lookup"><span data-stu-id="6cb9b-113">CN</span></span>                | <span data-ttu-id="6cb9b-114">Canonical-Name</span><span class="sxs-lookup"><span data-stu-id="6cb9b-114">Canonical-Name</span></span>                              |
| <span data-ttu-id="6cb9b-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6cb9b-115">Ldap-Display-Name</span></span> | <span data-ttu-id="6cb9b-116">canonicalName</span><span class="sxs-lookup"><span data-stu-id="6cb9b-116">canonicalName</span></span>                               |
| <span data-ttu-id="6cb9b-117">Size</span><span class="sxs-lookup"><span data-stu-id="6cb9b-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="6cb9b-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="6cb9b-118">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="6cb9b-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="6cb9b-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="6cb9b-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6cb9b-120">Attribute-Id</span></span>      | <span data-ttu-id="6cb9b-121">1.2.840.113556.1.4.916</span><span class="sxs-lookup"><span data-stu-id="6cb9b-121">1.2.840.113556.1.4.916</span></span>                      |
| <span data-ttu-id="6cb9b-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6cb9b-122">System-Id-Guid</span></span>    | <span data-ttu-id="6cb9b-123">9a7ad945-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="6cb9b-123">9a7ad945-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="6cb9b-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cb9b-124">Syntax</span></span>            | [<span data-ttu-id="6cb9b-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6cb9b-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6cb9b-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="6cb9b-126">Implementations</span></span>

-   [<span data-ttu-id="6cb9b-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6cb9b-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6cb9b-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6cb9b-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6cb9b-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="6cb9b-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6cb9b-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6cb9b-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6cb9b-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6cb9b-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6cb9b-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6cb9b-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6cb9b-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6cb9b-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6cb9b-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6cb9b-134">Windows 2000 Server</span></span>



| <span data-ttu-id="6cb9b-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6cb9b-135">Entry</span></span> | <span data-ttu-id="6cb9b-136">Wert</span><span class="sxs-lookup"><span data-stu-id="6cb9b-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6cb9b-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6cb9b-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6cb9b-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cb9b-138">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6cb9b-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cb9b-139">System-Only</span></span>            | <span data-ttu-id="6cb9b-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="6cb9b-140">True</span></span>                            |
| <span data-ttu-id="6cb9b-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6cb9b-141">Is-Single-Valued</span></span>       | <span data-ttu-id="6cb9b-142">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-142">False</span></span>                           |
| <span data-ttu-id="6cb9b-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6cb9b-143">Is Indexed</span></span>             | <span data-ttu-id="6cb9b-144">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-144">False</span></span>                           |
| <span data-ttu-id="6cb9b-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6cb9b-145">In Global Catalog</span></span>      | <span data-ttu-id="6cb9b-146">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-146">False</span></span>                           |
| <span data-ttu-id="6cb9b-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6cb9b-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cb9b-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6cb9b-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6cb9b-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cb9b-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6cb9b-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cb9b-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6cb9b-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cb9b-151">Search-Flags</span></span>           | <span data-ttu-id="6cb9b-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cb9b-152">0x00000000</span></span>                      |
| <span data-ttu-id="6cb9b-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cb9b-153">System-Flags</span></span>           | <span data-ttu-id="6cb9b-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6cb9b-154">0x08000014</span></span>                      |
| <span data-ttu-id="6cb9b-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6cb9b-155">Classes used in</span></span>        | [<span data-ttu-id="6cb9b-156">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="6cb9b-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6cb9b-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6cb9b-157">Windows Server 2003</span></span>



| <span data-ttu-id="6cb9b-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6cb9b-158">Entry</span></span> | <span data-ttu-id="6cb9b-159">Wert</span><span class="sxs-lookup"><span data-stu-id="6cb9b-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6cb9b-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6cb9b-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6cb9b-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cb9b-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6cb9b-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cb9b-162">System-Only</span></span>            | <span data-ttu-id="6cb9b-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="6cb9b-163">True</span></span>                            |
| <span data-ttu-id="6cb9b-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6cb9b-164">Is-Single-Valued</span></span>       | <span data-ttu-id="6cb9b-165">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-165">False</span></span>                           |
| <span data-ttu-id="6cb9b-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6cb9b-166">Is Indexed</span></span>             | <span data-ttu-id="6cb9b-167">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-167">False</span></span>                           |
| <span data-ttu-id="6cb9b-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6cb9b-168">In Global Catalog</span></span>      | <span data-ttu-id="6cb9b-169">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-169">False</span></span>                           |
| <span data-ttu-id="6cb9b-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6cb9b-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cb9b-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6cb9b-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6cb9b-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cb9b-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6cb9b-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cb9b-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6cb9b-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cb9b-174">Search-Flags</span></span>           | <span data-ttu-id="6cb9b-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cb9b-175">0x00000000</span></span>                      |
| <span data-ttu-id="6cb9b-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cb9b-176">System-Flags</span></span>           | <span data-ttu-id="6cb9b-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6cb9b-177">0x08000014</span></span>                      |
| <span data-ttu-id="6cb9b-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6cb9b-178">Classes used in</span></span>        | [<span data-ttu-id="6cb9b-179">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="6cb9b-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6cb9b-180">Adam</span><span class="sxs-lookup"><span data-stu-id="6cb9b-180">ADAM</span></span>



| <span data-ttu-id="6cb9b-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6cb9b-181">Entry</span></span> | <span data-ttu-id="6cb9b-182">Wert</span><span class="sxs-lookup"><span data-stu-id="6cb9b-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6cb9b-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6cb9b-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6cb9b-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cb9b-184">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6cb9b-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cb9b-185">System-Only</span></span>            | <span data-ttu-id="6cb9b-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="6cb9b-186">True</span></span>                            |
| <span data-ttu-id="6cb9b-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6cb9b-187">Is-Single-Valued</span></span>       | <span data-ttu-id="6cb9b-188">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-188">False</span></span>                           |
| <span data-ttu-id="6cb9b-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6cb9b-189">Is Indexed</span></span>             | <span data-ttu-id="6cb9b-190">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-190">False</span></span>                           |
| <span data-ttu-id="6cb9b-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6cb9b-191">In Global Catalog</span></span>      | <span data-ttu-id="6cb9b-192">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-192">False</span></span>                           |
| <span data-ttu-id="6cb9b-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6cb9b-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cb9b-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6cb9b-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6cb9b-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cb9b-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6cb9b-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cb9b-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6cb9b-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cb9b-197">Search-Flags</span></span>           | <span data-ttu-id="6cb9b-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cb9b-198">0x00000000</span></span>                      |
| <span data-ttu-id="6cb9b-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cb9b-199">System-Flags</span></span>           | <span data-ttu-id="6cb9b-200">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6cb9b-200">0x08000014</span></span>                      |
| <span data-ttu-id="6cb9b-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6cb9b-201">Classes used in</span></span>        | [<span data-ttu-id="6cb9b-202">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="6cb9b-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6cb9b-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6cb9b-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6cb9b-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6cb9b-204">Entry</span></span> | <span data-ttu-id="6cb9b-205">Wert</span><span class="sxs-lookup"><span data-stu-id="6cb9b-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6cb9b-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6cb9b-206">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6cb9b-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cb9b-207">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6cb9b-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cb9b-208">System-Only</span></span>            | <span data-ttu-id="6cb9b-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="6cb9b-209">True</span></span>                            |
| <span data-ttu-id="6cb9b-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6cb9b-210">Is-Single-Valued</span></span>       | <span data-ttu-id="6cb9b-211">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-211">False</span></span>                           |
| <span data-ttu-id="6cb9b-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6cb9b-212">Is Indexed</span></span>             | <span data-ttu-id="6cb9b-213">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-213">False</span></span>                           |
| <span data-ttu-id="6cb9b-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6cb9b-214">In Global Catalog</span></span>      | <span data-ttu-id="6cb9b-215">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-215">False</span></span>                           |
| <span data-ttu-id="6cb9b-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6cb9b-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cb9b-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6cb9b-217">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6cb9b-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cb9b-218">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6cb9b-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cb9b-219">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6cb9b-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cb9b-220">Search-Flags</span></span>           | <span data-ttu-id="6cb9b-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cb9b-221">0x00000000</span></span>                      |
| <span data-ttu-id="6cb9b-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cb9b-222">System-Flags</span></span>           | <span data-ttu-id="6cb9b-223">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6cb9b-223">0x08000014</span></span>                      |
| <span data-ttu-id="6cb9b-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6cb9b-224">Classes used in</span></span>        | [<span data-ttu-id="6cb9b-225">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="6cb9b-225">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6cb9b-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6cb9b-226">Windows Server 2008</span></span>



| <span data-ttu-id="6cb9b-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6cb9b-227">Entry</span></span> | <span data-ttu-id="6cb9b-228">Wert</span><span class="sxs-lookup"><span data-stu-id="6cb9b-228">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6cb9b-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6cb9b-229">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6cb9b-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cb9b-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6cb9b-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cb9b-231">System-Only</span></span>            | <span data-ttu-id="6cb9b-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="6cb9b-232">True</span></span>                            |
| <span data-ttu-id="6cb9b-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6cb9b-233">Is-Single-Valued</span></span>       | <span data-ttu-id="6cb9b-234">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-234">False</span></span>                           |
| <span data-ttu-id="6cb9b-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6cb9b-235">Is Indexed</span></span>             | <span data-ttu-id="6cb9b-236">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-236">False</span></span>                           |
| <span data-ttu-id="6cb9b-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6cb9b-237">In Global Catalog</span></span>      | <span data-ttu-id="6cb9b-238">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-238">False</span></span>                           |
| <span data-ttu-id="6cb9b-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6cb9b-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cb9b-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6cb9b-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6cb9b-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cb9b-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6cb9b-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cb9b-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6cb9b-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cb9b-243">Search-Flags</span></span>           | <span data-ttu-id="6cb9b-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cb9b-244">0x00000000</span></span>                      |
| <span data-ttu-id="6cb9b-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cb9b-245">System-Flags</span></span>           | <span data-ttu-id="6cb9b-246">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6cb9b-246">0x08000014</span></span>                      |
| <span data-ttu-id="6cb9b-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6cb9b-247">Classes used in</span></span>        | [<span data-ttu-id="6cb9b-248">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="6cb9b-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6cb9b-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6cb9b-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6cb9b-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6cb9b-250">Entry</span></span> | <span data-ttu-id="6cb9b-251">Wert</span><span class="sxs-lookup"><span data-stu-id="6cb9b-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6cb9b-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6cb9b-252">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6cb9b-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cb9b-253">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6cb9b-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cb9b-254">System-Only</span></span>            | <span data-ttu-id="6cb9b-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="6cb9b-255">True</span></span>                            |
| <span data-ttu-id="6cb9b-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6cb9b-256">Is-Single-Valued</span></span>       | <span data-ttu-id="6cb9b-257">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-257">False</span></span>                           |
| <span data-ttu-id="6cb9b-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6cb9b-258">Is Indexed</span></span>             | <span data-ttu-id="6cb9b-259">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-259">False</span></span>                           |
| <span data-ttu-id="6cb9b-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6cb9b-260">In Global Catalog</span></span>      | <span data-ttu-id="6cb9b-261">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-261">False</span></span>                           |
| <span data-ttu-id="6cb9b-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6cb9b-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cb9b-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6cb9b-263">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6cb9b-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cb9b-264">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6cb9b-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cb9b-265">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6cb9b-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cb9b-266">Search-Flags</span></span>           | <span data-ttu-id="6cb9b-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cb9b-267">0x00000000</span></span>                      |
| <span data-ttu-id="6cb9b-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cb9b-268">System-Flags</span></span>           | <span data-ttu-id="6cb9b-269">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6cb9b-269">0x08000014</span></span>                      |
| <span data-ttu-id="6cb9b-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6cb9b-270">Classes used in</span></span>        | [<span data-ttu-id="6cb9b-271">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="6cb9b-271">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6cb9b-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6cb9b-272">Windows Server 2012</span></span>



| <span data-ttu-id="6cb9b-273">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6cb9b-273">Entry</span></span> | <span data-ttu-id="6cb9b-274">Wert</span><span class="sxs-lookup"><span data-stu-id="6cb9b-274">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6cb9b-275">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6cb9b-275">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6cb9b-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cb9b-276">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6cb9b-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cb9b-277">System-Only</span></span>            | <span data-ttu-id="6cb9b-278">Richtig</span><span class="sxs-lookup"><span data-stu-id="6cb9b-278">True</span></span>                            |
| <span data-ttu-id="6cb9b-279">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6cb9b-279">Is-Single-Valued</span></span>       | <span data-ttu-id="6cb9b-280">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-280">False</span></span>                           |
| <span data-ttu-id="6cb9b-281">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6cb9b-281">Is Indexed</span></span>             | <span data-ttu-id="6cb9b-282">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-282">False</span></span>                           |
| <span data-ttu-id="6cb9b-283">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6cb9b-283">In Global Catalog</span></span>      | <span data-ttu-id="6cb9b-284">False</span><span class="sxs-lookup"><span data-stu-id="6cb9b-284">False</span></span>                           |
| <span data-ttu-id="6cb9b-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6cb9b-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cb9b-286">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6cb9b-286">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6cb9b-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cb9b-287">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6cb9b-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cb9b-288">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6cb9b-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cb9b-289">Search-Flags</span></span>           | <span data-ttu-id="6cb9b-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cb9b-290">0x00000000</span></span>                      |
| <span data-ttu-id="6cb9b-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cb9b-291">System-Flags</span></span>           | <span data-ttu-id="6cb9b-292">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6cb9b-292">0x08000014</span></span>                      |
| <span data-ttu-id="6cb9b-293">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6cb9b-293">Classes used in</span></span>        | [<span data-ttu-id="6cb9b-294">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="6cb9b-294">**Top**</span></span>](c-top.md)<br/> |



 

