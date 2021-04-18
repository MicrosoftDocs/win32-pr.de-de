---
title: UAS-Compat-Attribut
description: Gibt an, ob der Sicherheits Konto-Manager Datengrößen erzwingt, um Active Directory kompatibel mit dem Benutzerkonto System von LanManager zu machen.
ms.assetid: 745e271e-28f4-4012-83a8-606d88de0221
ms.tgt_platform: multiple
keywords:
- AD-Schema für UAS-Compat-Attribut
- AD-Schema für uascompat-Attribut
topic_type:
- apiref
api_name:
- UAS-Compat
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6bbf1088f48c697b03c4ef423930be2dbd24617
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106343518"
---
# <a name="uas-compat-attribute"></a><span data-ttu-id="50a11-105">UAS-Compat-Attribut</span><span class="sxs-lookup"><span data-stu-id="50a11-105">UAS-Compat attribute</span></span>

<span data-ttu-id="50a11-106">Gibt an, ob der Sicherheits Konto-Manager Datengrößen erzwingt, um Active Directory kompatibel mit dem Benutzerkonto System von LanManager zu machen.</span><span class="sxs-lookup"><span data-stu-id="50a11-106">Indicates if the security account manager will enforce data sizes to make Active Directory compatible with the LanManager User Account System (UAS).</span></span> <span data-ttu-id="50a11-107">Wenn dieser Wert 0 ist, werden keine Grenzwerte erzwungen.</span><span class="sxs-lookup"><span data-stu-id="50a11-107">If this value is 0, no limits are enforced.</span></span> <span data-ttu-id="50a11-108">Wenn dieser Wert 1 ist, werden die folgenden Grenzwerte erzwungen.</span><span class="sxs-lookup"><span data-stu-id="50a11-108">If this value is 1, the following limits are enforced.</span></span>



| <span data-ttu-id="50a11-109">Wert</span><span class="sxs-lookup"><span data-stu-id="50a11-109">Value</span></span>                          | <span data-ttu-id="50a11-110">Länge</span><span class="sxs-lookup"><span data-stu-id="50a11-110">Length</span></span>                         |
|--------------------------------|--------------------------------|
| <span data-ttu-id="50a11-111">Kennwort</span><span class="sxs-lookup"><span data-stu-id="50a11-111">Password</span></span><br/>            | <span data-ttu-id="50a11-112">0 bis 14 Zeichen</span><span class="sxs-lookup"><span data-stu-id="50a11-112">0 to 14 characters</span></span><br/>  |
| <span data-ttu-id="50a11-113">Kontoname</span><span class="sxs-lookup"><span data-stu-id="50a11-113">Account Name</span></span><br/>        | <span data-ttu-id="50a11-114">0 bis 20 Zeichen</span><span class="sxs-lookup"><span data-stu-id="50a11-114">0 to 20 characters</span></span><br/>  |
| <span data-ttu-id="50a11-115">Domänenname</span><span class="sxs-lookup"><span data-stu-id="50a11-115">Domain Name</span></span><br/>         | <span data-ttu-id="50a11-116">0 bis 15 Zeichen</span><span class="sxs-lookup"><span data-stu-id="50a11-116">0 to 15 characters</span></span><br/>  |
| <span data-ttu-id="50a11-117">Computername</span><span class="sxs-lookup"><span data-stu-id="50a11-117">Computer Name</span></span><br/>       | <span data-ttu-id="50a11-118">0 bis 15 Zeichen</span><span class="sxs-lookup"><span data-stu-id="50a11-118">0 to 15 characters</span></span><br/>  |
| <span data-ttu-id="50a11-119">Kommentare</span><span class="sxs-lookup"><span data-stu-id="50a11-119">Comments</span></span><br/>            | <span data-ttu-id="50a11-120">0 bis 48 Zeichen</span><span class="sxs-lookup"><span data-stu-id="50a11-120">0 to 48 characters</span></span><br/>  |
| <span data-ttu-id="50a11-121">Basisverzeichnis</span><span class="sxs-lookup"><span data-stu-id="50a11-121">Home Directory</span></span><br/>      | <span data-ttu-id="50a11-122">0 bis 256 Zeichen</span><span class="sxs-lookup"><span data-stu-id="50a11-122">0 to 256 characters</span></span><br/> |
| <span data-ttu-id="50a11-123">Skript Pfad</span><span class="sxs-lookup"><span data-stu-id="50a11-123">Script Path</span></span><br/>         | <span data-ttu-id="50a11-124">0 bis 256 Zeichen</span><span class="sxs-lookup"><span data-stu-id="50a11-124">0 to 256 characters</span></span><br/> |
| <span data-ttu-id="50a11-125">Zeiteinheiten pro Woche</span><span class="sxs-lookup"><span data-stu-id="50a11-125">Time Units Per Week</span></span><br/> | <span data-ttu-id="50a11-126">168 Bits (21 Bytes)</span><span class="sxs-lookup"><span data-stu-id="50a11-126">168 bits (21 bytes)</span></span><br/> |



 



| <span data-ttu-id="50a11-127">Eingabe</span><span class="sxs-lookup"><span data-stu-id="50a11-127">Entry</span></span> | <span data-ttu-id="50a11-128">Wert</span><span class="sxs-lookup"><span data-stu-id="50a11-128">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="50a11-129">CN</span><span class="sxs-lookup"><span data-stu-id="50a11-129">CN</span></span>                | <span data-ttu-id="50a11-130">UAS-Compat</span><span class="sxs-lookup"><span data-stu-id="50a11-130">UAS-Compat</span></span>                           |
| <span data-ttu-id="50a11-131">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="50a11-131">Ldap-Display-Name</span></span> | <span data-ttu-id="50a11-132">uascompat</span><span class="sxs-lookup"><span data-stu-id="50a11-132">uASCompat</span></span>                            |
| <span data-ttu-id="50a11-133">Size</span><span class="sxs-lookup"><span data-stu-id="50a11-133">Size</span></span>              | \-                                   |
| <span data-ttu-id="50a11-134">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="50a11-134">Update Privilege</span></span>  | <span data-ttu-id="50a11-135">Wird von einem Administrator ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50a11-135">Performed by an administrator.</span></span>       |
| <span data-ttu-id="50a11-136">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="50a11-136">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="50a11-137">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="50a11-137">Attribute-Id</span></span>      | <span data-ttu-id="50a11-138">1.2.840.113556.1.4.155</span><span class="sxs-lookup"><span data-stu-id="50a11-138">1.2.840.113556.1.4.155</span></span>               |
| <span data-ttu-id="50a11-139">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="50a11-139">System-Id-Guid</span></span>    | <span data-ttu-id="50a11-140">bf967a61-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="50a11-140">bf967a61-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="50a11-141">Syntax</span><span class="sxs-lookup"><span data-stu-id="50a11-141">Syntax</span></span>            | [<span data-ttu-id="50a11-142">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="50a11-142">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="50a11-143">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="50a11-143">Implementations</span></span>

-   [<span data-ttu-id="50a11-144">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="50a11-144">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="50a11-145">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="50a11-145">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="50a11-146">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="50a11-146">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="50a11-147">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="50a11-147">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="50a11-148">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="50a11-148">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="50a11-149">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="50a11-149">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="50a11-150">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="50a11-150">Windows 2000 Server</span></span>



| <span data-ttu-id="50a11-151">Eingabe</span><span class="sxs-lookup"><span data-stu-id="50a11-151">Entry</span></span> | <span data-ttu-id="50a11-152">Wert</span><span class="sxs-lookup"><span data-stu-id="50a11-152">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="50a11-153">Link-ID</span><span class="sxs-lookup"><span data-stu-id="50a11-153">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="50a11-154">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50a11-154">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="50a11-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="50a11-155">System-Only</span></span>            | <span data-ttu-id="50a11-156">False</span><span class="sxs-lookup"><span data-stu-id="50a11-156">False</span></span>                                                 |
| <span data-ttu-id="50a11-157">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="50a11-157">Is-Single-Valued</span></span>       | <span data-ttu-id="50a11-158">Richtig</span><span class="sxs-lookup"><span data-stu-id="50a11-158">True</span></span>                                                  |
| <span data-ttu-id="50a11-159">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="50a11-159">Is Indexed</span></span>             | <span data-ttu-id="50a11-160">False</span><span class="sxs-lookup"><span data-stu-id="50a11-160">False</span></span>                                                 |
| <span data-ttu-id="50a11-161">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="50a11-161">In Global Catalog</span></span>      | <span data-ttu-id="50a11-162">False</span><span class="sxs-lookup"><span data-stu-id="50a11-162">False</span></span>                                                 |
| <span data-ttu-id="50a11-163">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="50a11-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="50a11-164">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="50a11-164">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="50a11-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50a11-165">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="50a11-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50a11-166">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="50a11-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50a11-167">Search-Flags</span></span>           | <span data-ttu-id="50a11-168">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50a11-168">0x00000000</span></span>                                            |
| <span data-ttu-id="50a11-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50a11-169">System-Flags</span></span>           | <span data-ttu-id="50a11-170">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50a11-170">0x00000010</span></span>                                            |
| <span data-ttu-id="50a11-171">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="50a11-171">Classes used in</span></span>        | [<span data-ttu-id="50a11-172">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="50a11-172">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="50a11-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="50a11-173">Windows Server 2003</span></span>



| <span data-ttu-id="50a11-174">Eingabe</span><span class="sxs-lookup"><span data-stu-id="50a11-174">Entry</span></span> | <span data-ttu-id="50a11-175">Wert</span><span class="sxs-lookup"><span data-stu-id="50a11-175">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="50a11-176">Link-ID</span><span class="sxs-lookup"><span data-stu-id="50a11-176">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="50a11-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50a11-177">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="50a11-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="50a11-178">System-Only</span></span>            | <span data-ttu-id="50a11-179">False</span><span class="sxs-lookup"><span data-stu-id="50a11-179">False</span></span>                                                 |
| <span data-ttu-id="50a11-180">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="50a11-180">Is-Single-Valued</span></span>       | <span data-ttu-id="50a11-181">Richtig</span><span class="sxs-lookup"><span data-stu-id="50a11-181">True</span></span>                                                  |
| <span data-ttu-id="50a11-182">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="50a11-182">Is Indexed</span></span>             | <span data-ttu-id="50a11-183">False</span><span class="sxs-lookup"><span data-stu-id="50a11-183">False</span></span>                                                 |
| <span data-ttu-id="50a11-184">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="50a11-184">In Global Catalog</span></span>      | <span data-ttu-id="50a11-185">False</span><span class="sxs-lookup"><span data-stu-id="50a11-185">False</span></span>                                                 |
| <span data-ttu-id="50a11-186">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="50a11-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="50a11-187">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="50a11-187">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="50a11-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50a11-188">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="50a11-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50a11-189">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="50a11-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50a11-190">Search-Flags</span></span>           | <span data-ttu-id="50a11-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50a11-191">0x00000000</span></span>                                            |
| <span data-ttu-id="50a11-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50a11-192">System-Flags</span></span>           | <span data-ttu-id="50a11-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50a11-193">0x00000010</span></span>                                            |
| <span data-ttu-id="50a11-194">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="50a11-194">Classes used in</span></span>        | [<span data-ttu-id="50a11-195">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="50a11-195">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="50a11-196">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="50a11-196">Windows Server 2003 R2</span></span>



| <span data-ttu-id="50a11-197">Eingabe</span><span class="sxs-lookup"><span data-stu-id="50a11-197">Entry</span></span> | <span data-ttu-id="50a11-198">Wert</span><span class="sxs-lookup"><span data-stu-id="50a11-198">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="50a11-199">Link-ID</span><span class="sxs-lookup"><span data-stu-id="50a11-199">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="50a11-200">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50a11-200">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="50a11-201">System-Only</span><span class="sxs-lookup"><span data-stu-id="50a11-201">System-Only</span></span>            | <span data-ttu-id="50a11-202">False</span><span class="sxs-lookup"><span data-stu-id="50a11-202">False</span></span>                                                 |
| <span data-ttu-id="50a11-203">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="50a11-203">Is-Single-Valued</span></span>       | <span data-ttu-id="50a11-204">Richtig</span><span class="sxs-lookup"><span data-stu-id="50a11-204">True</span></span>                                                  |
| <span data-ttu-id="50a11-205">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="50a11-205">Is Indexed</span></span>             | <span data-ttu-id="50a11-206">False</span><span class="sxs-lookup"><span data-stu-id="50a11-206">False</span></span>                                                 |
| <span data-ttu-id="50a11-207">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="50a11-207">In Global Catalog</span></span>      | <span data-ttu-id="50a11-208">False</span><span class="sxs-lookup"><span data-stu-id="50a11-208">False</span></span>                                                 |
| <span data-ttu-id="50a11-209">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="50a11-209">NT-Security-Descriptor</span></span> | <span data-ttu-id="50a11-210">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="50a11-210">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="50a11-211">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50a11-211">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="50a11-212">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50a11-212">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="50a11-213">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50a11-213">Search-Flags</span></span>           | <span data-ttu-id="50a11-214">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50a11-214">0x00000000</span></span>                                            |
| <span data-ttu-id="50a11-215">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50a11-215">System-Flags</span></span>           | <span data-ttu-id="50a11-216">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50a11-216">0x00000010</span></span>                                            |
| <span data-ttu-id="50a11-217">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="50a11-217">Classes used in</span></span>        | [<span data-ttu-id="50a11-218">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="50a11-218">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="50a11-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50a11-219">Windows Server 2008</span></span>



| <span data-ttu-id="50a11-220">Eingabe</span><span class="sxs-lookup"><span data-stu-id="50a11-220">Entry</span></span> | <span data-ttu-id="50a11-221">Wert</span><span class="sxs-lookup"><span data-stu-id="50a11-221">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="50a11-222">Link-ID</span><span class="sxs-lookup"><span data-stu-id="50a11-222">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="50a11-223">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50a11-223">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="50a11-224">System-Only</span><span class="sxs-lookup"><span data-stu-id="50a11-224">System-Only</span></span>            | <span data-ttu-id="50a11-225">False</span><span class="sxs-lookup"><span data-stu-id="50a11-225">False</span></span>                                                 |
| <span data-ttu-id="50a11-226">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="50a11-226">Is-Single-Valued</span></span>       | <span data-ttu-id="50a11-227">Richtig</span><span class="sxs-lookup"><span data-stu-id="50a11-227">True</span></span>                                                  |
| <span data-ttu-id="50a11-228">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="50a11-228">Is Indexed</span></span>             | <span data-ttu-id="50a11-229">False</span><span class="sxs-lookup"><span data-stu-id="50a11-229">False</span></span>                                                 |
| <span data-ttu-id="50a11-230">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="50a11-230">In Global Catalog</span></span>      | <span data-ttu-id="50a11-231">False</span><span class="sxs-lookup"><span data-stu-id="50a11-231">False</span></span>                                                 |
| <span data-ttu-id="50a11-232">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="50a11-232">NT-Security-Descriptor</span></span> | <span data-ttu-id="50a11-233">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="50a11-233">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="50a11-234">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50a11-234">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="50a11-235">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50a11-235">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="50a11-236">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50a11-236">Search-Flags</span></span>           | <span data-ttu-id="50a11-237">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50a11-237">0x00000000</span></span>                                            |
| <span data-ttu-id="50a11-238">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50a11-238">System-Flags</span></span>           | <span data-ttu-id="50a11-239">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50a11-239">0x00000010</span></span>                                            |
| <span data-ttu-id="50a11-240">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="50a11-240">Classes used in</span></span>        | [<span data-ttu-id="50a11-241">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="50a11-241">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="50a11-242">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50a11-242">Windows Server 2008 R2</span></span>



| <span data-ttu-id="50a11-243">Eingabe</span><span class="sxs-lookup"><span data-stu-id="50a11-243">Entry</span></span> | <span data-ttu-id="50a11-244">Wert</span><span class="sxs-lookup"><span data-stu-id="50a11-244">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="50a11-245">Link-ID</span><span class="sxs-lookup"><span data-stu-id="50a11-245">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="50a11-246">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50a11-246">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="50a11-247">System-Only</span><span class="sxs-lookup"><span data-stu-id="50a11-247">System-Only</span></span>            | <span data-ttu-id="50a11-248">False</span><span class="sxs-lookup"><span data-stu-id="50a11-248">False</span></span>                                                 |
| <span data-ttu-id="50a11-249">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="50a11-249">Is-Single-Valued</span></span>       | <span data-ttu-id="50a11-250">Richtig</span><span class="sxs-lookup"><span data-stu-id="50a11-250">True</span></span>                                                  |
| <span data-ttu-id="50a11-251">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="50a11-251">Is Indexed</span></span>             | <span data-ttu-id="50a11-252">False</span><span class="sxs-lookup"><span data-stu-id="50a11-252">False</span></span>                                                 |
| <span data-ttu-id="50a11-253">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="50a11-253">In Global Catalog</span></span>      | <span data-ttu-id="50a11-254">False</span><span class="sxs-lookup"><span data-stu-id="50a11-254">False</span></span>                                                 |
| <span data-ttu-id="50a11-255">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="50a11-255">NT-Security-Descriptor</span></span> | <span data-ttu-id="50a11-256">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="50a11-256">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="50a11-257">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50a11-257">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="50a11-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50a11-258">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="50a11-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50a11-259">Search-Flags</span></span>           | <span data-ttu-id="50a11-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50a11-260">0x00000000</span></span>                                            |
| <span data-ttu-id="50a11-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50a11-261">System-Flags</span></span>           | <span data-ttu-id="50a11-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50a11-262">0x00000010</span></span>                                            |
| <span data-ttu-id="50a11-263">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="50a11-263">Classes used in</span></span>        | [<span data-ttu-id="50a11-264">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="50a11-264">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="50a11-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50a11-265">Windows Server 2012</span></span>



| <span data-ttu-id="50a11-266">Eingabe</span><span class="sxs-lookup"><span data-stu-id="50a11-266">Entry</span></span> | <span data-ttu-id="50a11-267">Wert</span><span class="sxs-lookup"><span data-stu-id="50a11-267">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="50a11-268">Link-ID</span><span class="sxs-lookup"><span data-stu-id="50a11-268">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="50a11-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50a11-269">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="50a11-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="50a11-270">System-Only</span></span>            | <span data-ttu-id="50a11-271">False</span><span class="sxs-lookup"><span data-stu-id="50a11-271">False</span></span>                                                 |
| <span data-ttu-id="50a11-272">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="50a11-272">Is-Single-Valued</span></span>       | <span data-ttu-id="50a11-273">Richtig</span><span class="sxs-lookup"><span data-stu-id="50a11-273">True</span></span>                                                  |
| <span data-ttu-id="50a11-274">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="50a11-274">Is Indexed</span></span>             | <span data-ttu-id="50a11-275">False</span><span class="sxs-lookup"><span data-stu-id="50a11-275">False</span></span>                                                 |
| <span data-ttu-id="50a11-276">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="50a11-276">In Global Catalog</span></span>      | <span data-ttu-id="50a11-277">False</span><span class="sxs-lookup"><span data-stu-id="50a11-277">False</span></span>                                                 |
| <span data-ttu-id="50a11-278">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="50a11-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="50a11-279">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="50a11-279">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="50a11-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50a11-280">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="50a11-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50a11-281">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="50a11-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50a11-282">Search-Flags</span></span>           | <span data-ttu-id="50a11-283">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50a11-283">0x00000000</span></span>                                            |
| <span data-ttu-id="50a11-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50a11-284">System-Flags</span></span>           | <span data-ttu-id="50a11-285">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50a11-285">0x00000010</span></span>                                            |
| <span data-ttu-id="50a11-286">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="50a11-286">Classes used in</span></span>        | [<span data-ttu-id="50a11-287">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="50a11-287">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





