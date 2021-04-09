---
title: Anzeige Name-druckbares Attribut
description: Der druckbare Anzeige Name für ein Objekt.
ms.assetid: e8e5ff25-66dd-4c74-9571-9ec765d6d1af
ms.tgt_platform: multiple
keywords:
- Anzeige Name-druckbares Attribut AD-Schema
- AD-Schema des displayNamePrintable-Attributs
topic_type:
- apiref
api_name:
- Display-Name-Printable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eff05c2279f026e3a94b707b522509b4801ff27
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859893"
---
# <a name="display-name-printable-attribute"></a><span data-ttu-id="f418f-105">Anzeige Name-druckbares Attribut</span><span class="sxs-lookup"><span data-stu-id="f418f-105">Display-Name-Printable attribute</span></span>

<span data-ttu-id="f418f-106">Der druckbare Anzeige Name für ein Objekt.</span><span class="sxs-lookup"><span data-stu-id="f418f-106">The printable display name for an object.</span></span> <span data-ttu-id="f418f-107">Der Druck Bare Anzeige Name ist normalerweise die Kombination aus dem Vornamen, dem mittleren Anfangs-und Nachnamen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="f418f-107">The printable display name is usually the combination of the user's first name, middle initial, and last name.</span></span>



| <span data-ttu-id="f418f-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f418f-108">Entry</span></span> | <span data-ttu-id="f418f-109">Wert</span><span class="sxs-lookup"><span data-stu-id="f418f-109">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="f418f-110">CN</span><span class="sxs-lookup"><span data-stu-id="f418f-110">CN</span></span>                | <span data-ttu-id="f418f-111">Anzeige Name-druckdruck</span><span class="sxs-lookup"><span data-stu-id="f418f-111">Display-Name-Printable</span></span>                 |
| <span data-ttu-id="f418f-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f418f-112">Ldap-Display-Name</span></span> | <span data-ttu-id="f418f-113">Display Name Print</span><span class="sxs-lookup"><span data-stu-id="f418f-113">displayNamePrintable</span></span>                   |
| <span data-ttu-id="f418f-114">Size</span><span class="sxs-lookup"><span data-stu-id="f418f-114">Size</span></span>              | \-                                     |
| <span data-ttu-id="f418f-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f418f-115">Update Privilege</span></span>  | <span data-ttu-id="f418f-116">Domänen Administrator oder Konto Besitzer.</span><span class="sxs-lookup"><span data-stu-id="f418f-116">Domain administrator or account owner.</span></span> |
| <span data-ttu-id="f418f-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f418f-117">Update Frequency</span></span>  | \-                                     |
| <span data-ttu-id="f418f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f418f-118">Attribute-Id</span></span>      | <span data-ttu-id="f418f-119">1.2.840.113556.1.2.353</span><span class="sxs-lookup"><span data-stu-id="f418f-119">1.2.840.113556.1.2.353</span></span>                 |
| <span data-ttu-id="f418f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f418f-120">System-Id-Guid</span></span>    | <span data-ttu-id="f418f-121">bf967954-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f418f-121">bf967954-0de6-11d0-a285-00aa003049e2</span></span>   |
| <span data-ttu-id="f418f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="f418f-122">Syntax</span></span>            | [<span data-ttu-id="f418f-123">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="f418f-123">**String(IA5)**</span></span>](s-string-ia5.md)    |



## <a name="implementations"></a><span data-ttu-id="f418f-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f418f-124">Implementations</span></span>

-   [<span data-ttu-id="f418f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f418f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f418f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f418f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f418f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f418f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f418f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f418f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f418f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f418f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f418f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f418f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f418f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f418f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f418f-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f418f-132">Entry</span></span> | <span data-ttu-id="f418f-133">Wert</span><span class="sxs-lookup"><span data-stu-id="f418f-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f418f-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f418f-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f418f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f418f-135">MAPI-Id</span></span>                | <span data-ttu-id="f418f-136">0x39ff</span><span class="sxs-lookup"><span data-stu-id="f418f-136">0x39FF</span></span>                          |
| <span data-ttu-id="f418f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f418f-137">System-Only</span></span>            | <span data-ttu-id="f418f-138">False</span><span class="sxs-lookup"><span data-stu-id="f418f-138">False</span></span>                           |
| <span data-ttu-id="f418f-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f418f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f418f-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="f418f-140">True</span></span>                            |
| <span data-ttu-id="f418f-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f418f-141">Is Indexed</span></span>             | <span data-ttu-id="f418f-142">False</span><span class="sxs-lookup"><span data-stu-id="f418f-142">False</span></span>                           |
| <span data-ttu-id="f418f-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f418f-143">In Global Catalog</span></span>      | <span data-ttu-id="f418f-144">False</span><span class="sxs-lookup"><span data-stu-id="f418f-144">False</span></span>                           |
| <span data-ttu-id="f418f-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f418f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f418f-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f418f-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f418f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f418f-147">Range-Lower</span></span>            | <span data-ttu-id="f418f-148">1</span><span class="sxs-lookup"><span data-stu-id="f418f-148">1</span></span>                               |
| <span data-ttu-id="f418f-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f418f-149">Range-Upper</span></span>            | <span data-ttu-id="f418f-150">256</span><span class="sxs-lookup"><span data-stu-id="f418f-150">256</span></span>                             |
| <span data-ttu-id="f418f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f418f-151">Search-Flags</span></span>           | <span data-ttu-id="f418f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f418f-152">0x00000000</span></span>                      |
| <span data-ttu-id="f418f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f418f-153">System-Flags</span></span>           | <span data-ttu-id="f418f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f418f-154">0x00000010</span></span>                      |
| <span data-ttu-id="f418f-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f418f-155">Classes used in</span></span>        | [<span data-ttu-id="f418f-156">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f418f-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f418f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f418f-157">Windows Server 2003</span></span>



| <span data-ttu-id="f418f-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f418f-158">Entry</span></span> | <span data-ttu-id="f418f-159">Wert</span><span class="sxs-lookup"><span data-stu-id="f418f-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f418f-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f418f-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f418f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f418f-161">MAPI-Id</span></span>                | <span data-ttu-id="f418f-162">0x39ff</span><span class="sxs-lookup"><span data-stu-id="f418f-162">0x39FF</span></span>                          |
| <span data-ttu-id="f418f-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="f418f-163">System-Only</span></span>            | <span data-ttu-id="f418f-164">False</span><span class="sxs-lookup"><span data-stu-id="f418f-164">False</span></span>                           |
| <span data-ttu-id="f418f-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f418f-165">Is-Single-Valued</span></span>       | <span data-ttu-id="f418f-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="f418f-166">True</span></span>                            |
| <span data-ttu-id="f418f-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f418f-167">Is Indexed</span></span>             | <span data-ttu-id="f418f-168">False</span><span class="sxs-lookup"><span data-stu-id="f418f-168">False</span></span>                           |
| <span data-ttu-id="f418f-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f418f-169">In Global Catalog</span></span>      | <span data-ttu-id="f418f-170">False</span><span class="sxs-lookup"><span data-stu-id="f418f-170">False</span></span>                           |
| <span data-ttu-id="f418f-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f418f-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="f418f-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f418f-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f418f-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f418f-173">Range-Lower</span></span>            | <span data-ttu-id="f418f-174">1</span><span class="sxs-lookup"><span data-stu-id="f418f-174">1</span></span>                               |
| <span data-ttu-id="f418f-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f418f-175">Range-Upper</span></span>            | <span data-ttu-id="f418f-176">256</span><span class="sxs-lookup"><span data-stu-id="f418f-176">256</span></span>                             |
| <span data-ttu-id="f418f-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f418f-177">Search-Flags</span></span>           | <span data-ttu-id="f418f-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f418f-178">0x00000000</span></span>                      |
| <span data-ttu-id="f418f-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f418f-179">System-Flags</span></span>           | <span data-ttu-id="f418f-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f418f-180">0x00000010</span></span>                      |
| <span data-ttu-id="f418f-181">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f418f-181">Classes used in</span></span>        | [<span data-ttu-id="f418f-182">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f418f-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f418f-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f418f-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f418f-184">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f418f-184">Entry</span></span> | <span data-ttu-id="f418f-185">Wert</span><span class="sxs-lookup"><span data-stu-id="f418f-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f418f-186">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f418f-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f418f-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f418f-187">MAPI-Id</span></span>                | <span data-ttu-id="f418f-188">0x39ff</span><span class="sxs-lookup"><span data-stu-id="f418f-188">0x39FF</span></span>                          |
| <span data-ttu-id="f418f-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="f418f-189">System-Only</span></span>            | <span data-ttu-id="f418f-190">False</span><span class="sxs-lookup"><span data-stu-id="f418f-190">False</span></span>                           |
| <span data-ttu-id="f418f-191">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f418f-191">Is-Single-Valued</span></span>       | <span data-ttu-id="f418f-192">Richtig</span><span class="sxs-lookup"><span data-stu-id="f418f-192">True</span></span>                            |
| <span data-ttu-id="f418f-193">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f418f-193">Is Indexed</span></span>             | <span data-ttu-id="f418f-194">False</span><span class="sxs-lookup"><span data-stu-id="f418f-194">False</span></span>                           |
| <span data-ttu-id="f418f-195">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f418f-195">In Global Catalog</span></span>      | <span data-ttu-id="f418f-196">False</span><span class="sxs-lookup"><span data-stu-id="f418f-196">False</span></span>                           |
| <span data-ttu-id="f418f-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f418f-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="f418f-198">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f418f-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f418f-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f418f-199">Range-Lower</span></span>            | <span data-ttu-id="f418f-200">1</span><span class="sxs-lookup"><span data-stu-id="f418f-200">1</span></span>                               |
| <span data-ttu-id="f418f-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f418f-201">Range-Upper</span></span>            | <span data-ttu-id="f418f-202">256</span><span class="sxs-lookup"><span data-stu-id="f418f-202">256</span></span>                             |
| <span data-ttu-id="f418f-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f418f-203">Search-Flags</span></span>           | <span data-ttu-id="f418f-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f418f-204">0x00000000</span></span>                      |
| <span data-ttu-id="f418f-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f418f-205">System-Flags</span></span>           | <span data-ttu-id="f418f-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f418f-206">0x00000010</span></span>                      |
| <span data-ttu-id="f418f-207">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f418f-207">Classes used in</span></span>        | [<span data-ttu-id="f418f-208">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f418f-208">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f418f-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f418f-209">Windows Server 2008</span></span>



| <span data-ttu-id="f418f-210">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f418f-210">Entry</span></span> | <span data-ttu-id="f418f-211">Wert</span><span class="sxs-lookup"><span data-stu-id="f418f-211">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f418f-212">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f418f-212">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f418f-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f418f-213">MAPI-Id</span></span>                | <span data-ttu-id="f418f-214">0x39ff</span><span class="sxs-lookup"><span data-stu-id="f418f-214">0x39FF</span></span>                          |
| <span data-ttu-id="f418f-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="f418f-215">System-Only</span></span>            | <span data-ttu-id="f418f-216">False</span><span class="sxs-lookup"><span data-stu-id="f418f-216">False</span></span>                           |
| <span data-ttu-id="f418f-217">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f418f-217">Is-Single-Valued</span></span>       | <span data-ttu-id="f418f-218">Richtig</span><span class="sxs-lookup"><span data-stu-id="f418f-218">True</span></span>                            |
| <span data-ttu-id="f418f-219">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f418f-219">Is Indexed</span></span>             | <span data-ttu-id="f418f-220">False</span><span class="sxs-lookup"><span data-stu-id="f418f-220">False</span></span>                           |
| <span data-ttu-id="f418f-221">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f418f-221">In Global Catalog</span></span>      | <span data-ttu-id="f418f-222">False</span><span class="sxs-lookup"><span data-stu-id="f418f-222">False</span></span>                           |
| <span data-ttu-id="f418f-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f418f-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="f418f-224">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f418f-224">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f418f-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f418f-225">Range-Lower</span></span>            | <span data-ttu-id="f418f-226">1</span><span class="sxs-lookup"><span data-stu-id="f418f-226">1</span></span>                               |
| <span data-ttu-id="f418f-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f418f-227">Range-Upper</span></span>            | <span data-ttu-id="f418f-228">256</span><span class="sxs-lookup"><span data-stu-id="f418f-228">256</span></span>                             |
| <span data-ttu-id="f418f-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f418f-229">Search-Flags</span></span>           | <span data-ttu-id="f418f-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f418f-230">0x00000000</span></span>                      |
| <span data-ttu-id="f418f-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f418f-231">System-Flags</span></span>           | <span data-ttu-id="f418f-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f418f-232">0x00000010</span></span>                      |
| <span data-ttu-id="f418f-233">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f418f-233">Classes used in</span></span>        | [<span data-ttu-id="f418f-234">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f418f-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f418f-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f418f-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f418f-236">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f418f-236">Entry</span></span> | <span data-ttu-id="f418f-237">Wert</span><span class="sxs-lookup"><span data-stu-id="f418f-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f418f-238">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f418f-238">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f418f-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f418f-239">MAPI-Id</span></span>                | <span data-ttu-id="f418f-240">0x39ff</span><span class="sxs-lookup"><span data-stu-id="f418f-240">0x39FF</span></span>                          |
| <span data-ttu-id="f418f-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="f418f-241">System-Only</span></span>            | <span data-ttu-id="f418f-242">False</span><span class="sxs-lookup"><span data-stu-id="f418f-242">False</span></span>                           |
| <span data-ttu-id="f418f-243">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f418f-243">Is-Single-Valued</span></span>       | <span data-ttu-id="f418f-244">Richtig</span><span class="sxs-lookup"><span data-stu-id="f418f-244">True</span></span>                            |
| <span data-ttu-id="f418f-245">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f418f-245">Is Indexed</span></span>             | <span data-ttu-id="f418f-246">False</span><span class="sxs-lookup"><span data-stu-id="f418f-246">False</span></span>                           |
| <span data-ttu-id="f418f-247">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f418f-247">In Global Catalog</span></span>      | <span data-ttu-id="f418f-248">False</span><span class="sxs-lookup"><span data-stu-id="f418f-248">False</span></span>                           |
| <span data-ttu-id="f418f-249">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f418f-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="f418f-250">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f418f-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f418f-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f418f-251">Range-Lower</span></span>            | <span data-ttu-id="f418f-252">1</span><span class="sxs-lookup"><span data-stu-id="f418f-252">1</span></span>                               |
| <span data-ttu-id="f418f-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f418f-253">Range-Upper</span></span>            | <span data-ttu-id="f418f-254">256</span><span class="sxs-lookup"><span data-stu-id="f418f-254">256</span></span>                             |
| <span data-ttu-id="f418f-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f418f-255">Search-Flags</span></span>           | <span data-ttu-id="f418f-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f418f-256">0x00000000</span></span>                      |
| <span data-ttu-id="f418f-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f418f-257">System-Flags</span></span>           | <span data-ttu-id="f418f-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f418f-258">0x00000010</span></span>                      |
| <span data-ttu-id="f418f-259">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f418f-259">Classes used in</span></span>        | [<span data-ttu-id="f418f-260">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f418f-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f418f-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f418f-261">Windows Server 2012</span></span>



| <span data-ttu-id="f418f-262">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f418f-262">Entry</span></span> | <span data-ttu-id="f418f-263">Wert</span><span class="sxs-lookup"><span data-stu-id="f418f-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f418f-264">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f418f-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f418f-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f418f-265">MAPI-Id</span></span>                | <span data-ttu-id="f418f-266">0x39ff</span><span class="sxs-lookup"><span data-stu-id="f418f-266">0x39FF</span></span>                          |
| <span data-ttu-id="f418f-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="f418f-267">System-Only</span></span>            | <span data-ttu-id="f418f-268">False</span><span class="sxs-lookup"><span data-stu-id="f418f-268">False</span></span>                           |
| <span data-ttu-id="f418f-269">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f418f-269">Is-Single-Valued</span></span>       | <span data-ttu-id="f418f-270">Richtig</span><span class="sxs-lookup"><span data-stu-id="f418f-270">True</span></span>                            |
| <span data-ttu-id="f418f-271">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f418f-271">Is Indexed</span></span>             | <span data-ttu-id="f418f-272">False</span><span class="sxs-lookup"><span data-stu-id="f418f-272">False</span></span>                           |
| <span data-ttu-id="f418f-273">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f418f-273">In Global Catalog</span></span>      | <span data-ttu-id="f418f-274">False</span><span class="sxs-lookup"><span data-stu-id="f418f-274">False</span></span>                           |
| <span data-ttu-id="f418f-275">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f418f-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="f418f-276">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f418f-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f418f-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f418f-277">Range-Lower</span></span>            | <span data-ttu-id="f418f-278">1</span><span class="sxs-lookup"><span data-stu-id="f418f-278">1</span></span>                               |
| <span data-ttu-id="f418f-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f418f-279">Range-Upper</span></span>            | <span data-ttu-id="f418f-280">256</span><span class="sxs-lookup"><span data-stu-id="f418f-280">256</span></span>                             |
| <span data-ttu-id="f418f-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f418f-281">Search-Flags</span></span>           | <span data-ttu-id="f418f-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f418f-282">0x00000000</span></span>                      |
| <span data-ttu-id="f418f-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f418f-283">System-Flags</span></span>           | <span data-ttu-id="f418f-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f418f-284">0x00000010</span></span>                      |
| <span data-ttu-id="f418f-285">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f418f-285">Classes used in</span></span>        | [<span data-ttu-id="f418f-286">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f418f-286">**Top**</span></span>](c-top.md)<br/> |



 

 





