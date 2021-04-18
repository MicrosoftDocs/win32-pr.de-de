---
title: DS-Heuristics-Attribut
description: Enthält globale Einstellungen für die gesamte Gesamtstruktur.
ms.assetid: d5fd990b-7bbf-4ede-a3af-7f3f7ac959b3
ms.tgt_platform: multiple
keywords:
- AD-Schema für DS-Heuristics-Attribut
- AD-Schema des dSHeuristics-Attributs
topic_type:
- apiref
api_name:
- DS-Heuristics
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65922b580975ec05877ae33d213ff3a3675ec72f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344731"
---
# <a name="ds-heuristics-attribute"></a><span data-ttu-id="04eab-105">DS-Heuristics-Attribut</span><span class="sxs-lookup"><span data-stu-id="04eab-105">DS-Heuristics attribute</span></span>

<span data-ttu-id="04eab-106">Enthält globale Einstellungen für die gesamte Gesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="04eab-106">Contains global settings for the entire forest.</span></span>

<span data-ttu-id="04eab-107">Informationen zu den AdminSDHolder-Ausschluss Bits, die auf der Microsoft Hilfe-und Support-Website verfügbar sind, finden Sie in Artikelnummer [817433, Delegierte Berechtigungen sind nicht verfügbar, und die Vererbung wird automatisch deaktiviert](https://support.microsoft.com/default.aspx?scid=kb;EN-US;817433).</span><span class="sxs-lookup"><span data-stu-id="04eab-107">There is information about adminSDholder exclusion bits available on the Microsoft Help and Support website in an article number [817433, Delegated permissions are not available and inheritance is automatically disabled](https://support.microsoft.com/default.aspx?scid=kb;EN-US;817433).</span></span>



| <span data-ttu-id="04eab-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04eab-108">Entry</span></span> | <span data-ttu-id="04eab-109">Wert</span><span class="sxs-lookup"><span data-stu-id="04eab-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="04eab-110">CN</span><span class="sxs-lookup"><span data-stu-id="04eab-110">CN</span></span>                | <span data-ttu-id="04eab-111">DS-Heuristics</span><span class="sxs-lookup"><span data-stu-id="04eab-111">DS-Heuristics</span></span>                               |
| <span data-ttu-id="04eab-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="04eab-112">Ldap-Display-Name</span></span> | <span data-ttu-id="04eab-113">dsheuristik</span><span class="sxs-lookup"><span data-stu-id="04eab-113">dSHeuristics</span></span>                                |
| <span data-ttu-id="04eab-114">Size</span><span class="sxs-lookup"><span data-stu-id="04eab-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="04eab-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="04eab-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="04eab-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="04eab-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="04eab-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="04eab-117">Attribute-Id</span></span>      | <span data-ttu-id="04eab-118">1.2.840.113556.1.2.212</span><span class="sxs-lookup"><span data-stu-id="04eab-118">1.2.840.113556.1.2.212</span></span>                      |
| <span data-ttu-id="04eab-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="04eab-119">System-Id-Guid</span></span>    | <span data-ttu-id="04eab-120">f0f8ff86-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="04eab-120">f0f8ff86-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="04eab-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="04eab-121">Syntax</span></span>            | [<span data-ttu-id="04eab-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="04eab-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="04eab-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="04eab-123">Implementations</span></span>

-   [<span data-ttu-id="04eab-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="04eab-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="04eab-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="04eab-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="04eab-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="04eab-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="04eab-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="04eab-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="04eab-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="04eab-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="04eab-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="04eab-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="04eab-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="04eab-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="04eab-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04eab-131">Windows 2000 Server</span></span>



| <span data-ttu-id="04eab-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04eab-132">Entry</span></span> | <span data-ttu-id="04eab-133">Wert</span><span class="sxs-lookup"><span data-stu-id="04eab-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="04eab-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04eab-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="04eab-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04eab-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="04eab-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="04eab-136">System-Only</span></span>            | <span data-ttu-id="04eab-137">False</span><span class="sxs-lookup"><span data-stu-id="04eab-137">False</span></span>                                            |
| <span data-ttu-id="04eab-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04eab-138">Is-Single-Valued</span></span>       | <span data-ttu-id="04eab-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="04eab-139">True</span></span>                                             |
| <span data-ttu-id="04eab-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04eab-140">Is Indexed</span></span>             | <span data-ttu-id="04eab-141">False</span><span class="sxs-lookup"><span data-stu-id="04eab-141">False</span></span>                                            |
| <span data-ttu-id="04eab-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04eab-142">In Global Catalog</span></span>      | <span data-ttu-id="04eab-143">False</span><span class="sxs-lookup"><span data-stu-id="04eab-143">False</span></span>                                            |
| <span data-ttu-id="04eab-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04eab-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="04eab-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04eab-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="04eab-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04eab-146">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="04eab-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04eab-147">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="04eab-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04eab-148">Search-Flags</span></span>           | <span data-ttu-id="04eab-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04eab-149">0x00000000</span></span>                                       |
| <span data-ttu-id="04eab-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04eab-150">System-Flags</span></span>           | <span data-ttu-id="04eab-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04eab-151">0x00000010</span></span>                                       |
| <span data-ttu-id="04eab-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04eab-152">Classes used in</span></span>        | [<span data-ttu-id="04eab-153">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="04eab-153">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="04eab-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="04eab-154">Windows Server 2003</span></span>



| <span data-ttu-id="04eab-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04eab-155">Entry</span></span> | <span data-ttu-id="04eab-156">Wert</span><span class="sxs-lookup"><span data-stu-id="04eab-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="04eab-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04eab-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="04eab-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04eab-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="04eab-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="04eab-159">System-Only</span></span>            | <span data-ttu-id="04eab-160">False</span><span class="sxs-lookup"><span data-stu-id="04eab-160">False</span></span>                                            |
| <span data-ttu-id="04eab-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04eab-161">Is-Single-Valued</span></span>       | <span data-ttu-id="04eab-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="04eab-162">True</span></span>                                             |
| <span data-ttu-id="04eab-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04eab-163">Is Indexed</span></span>             | <span data-ttu-id="04eab-164">False</span><span class="sxs-lookup"><span data-stu-id="04eab-164">False</span></span>                                            |
| <span data-ttu-id="04eab-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04eab-165">In Global Catalog</span></span>      | <span data-ttu-id="04eab-166">False</span><span class="sxs-lookup"><span data-stu-id="04eab-166">False</span></span>                                            |
| <span data-ttu-id="04eab-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04eab-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="04eab-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04eab-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="04eab-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04eab-169">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="04eab-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04eab-170">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="04eab-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04eab-171">Search-Flags</span></span>           | <span data-ttu-id="04eab-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04eab-172">0x00000000</span></span>                                       |
| <span data-ttu-id="04eab-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04eab-173">System-Flags</span></span>           | <span data-ttu-id="04eab-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04eab-174">0x00000010</span></span>                                       |
| <span data-ttu-id="04eab-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04eab-175">Classes used in</span></span>        | [<span data-ttu-id="04eab-176">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="04eab-176">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="04eab-177">Adam</span><span class="sxs-lookup"><span data-stu-id="04eab-177">ADAM</span></span>



| <span data-ttu-id="04eab-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04eab-178">Entry</span></span> | <span data-ttu-id="04eab-179">Wert</span><span class="sxs-lookup"><span data-stu-id="04eab-179">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="04eab-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04eab-180">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="04eab-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04eab-181">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="04eab-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="04eab-182">System-Only</span></span>            | <span data-ttu-id="04eab-183">False</span><span class="sxs-lookup"><span data-stu-id="04eab-183">False</span></span>                                            |
| <span data-ttu-id="04eab-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04eab-184">Is-Single-Valued</span></span>       | <span data-ttu-id="04eab-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="04eab-185">True</span></span>                                             |
| <span data-ttu-id="04eab-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04eab-186">Is Indexed</span></span>             | <span data-ttu-id="04eab-187">False</span><span class="sxs-lookup"><span data-stu-id="04eab-187">False</span></span>                                            |
| <span data-ttu-id="04eab-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04eab-188">In Global Catalog</span></span>      | <span data-ttu-id="04eab-189">False</span><span class="sxs-lookup"><span data-stu-id="04eab-189">False</span></span>                                            |
| <span data-ttu-id="04eab-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04eab-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="04eab-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04eab-191">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="04eab-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04eab-192">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="04eab-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04eab-193">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="04eab-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04eab-194">Search-Flags</span></span>           | <span data-ttu-id="04eab-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04eab-195">0x00000000</span></span>                                       |
| <span data-ttu-id="04eab-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04eab-196">System-Flags</span></span>           | <span data-ttu-id="04eab-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04eab-197">0x00000010</span></span>                                       |
| <span data-ttu-id="04eab-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04eab-198">Classes used in</span></span>        | [<span data-ttu-id="04eab-199">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="04eab-199">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="04eab-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="04eab-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="04eab-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04eab-201">Entry</span></span> | <span data-ttu-id="04eab-202">Wert</span><span class="sxs-lookup"><span data-stu-id="04eab-202">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="04eab-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04eab-203">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="04eab-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04eab-204">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="04eab-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="04eab-205">System-Only</span></span>            | <span data-ttu-id="04eab-206">False</span><span class="sxs-lookup"><span data-stu-id="04eab-206">False</span></span>                                            |
| <span data-ttu-id="04eab-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04eab-207">Is-Single-Valued</span></span>       | <span data-ttu-id="04eab-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="04eab-208">True</span></span>                                             |
| <span data-ttu-id="04eab-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04eab-209">Is Indexed</span></span>             | <span data-ttu-id="04eab-210">False</span><span class="sxs-lookup"><span data-stu-id="04eab-210">False</span></span>                                            |
| <span data-ttu-id="04eab-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04eab-211">In Global Catalog</span></span>      | <span data-ttu-id="04eab-212">False</span><span class="sxs-lookup"><span data-stu-id="04eab-212">False</span></span>                                            |
| <span data-ttu-id="04eab-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04eab-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="04eab-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04eab-214">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="04eab-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04eab-215">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="04eab-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04eab-216">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="04eab-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04eab-217">Search-Flags</span></span>           | <span data-ttu-id="04eab-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04eab-218">0x00000000</span></span>                                       |
| <span data-ttu-id="04eab-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04eab-219">System-Flags</span></span>           | <span data-ttu-id="04eab-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04eab-220">0x00000010</span></span>                                       |
| <span data-ttu-id="04eab-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04eab-221">Classes used in</span></span>        | [<span data-ttu-id="04eab-222">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="04eab-222">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="04eab-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04eab-223">Windows Server 2008</span></span>



| <span data-ttu-id="04eab-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04eab-224">Entry</span></span> | <span data-ttu-id="04eab-225">Wert</span><span class="sxs-lookup"><span data-stu-id="04eab-225">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="04eab-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04eab-226">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="04eab-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04eab-227">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="04eab-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="04eab-228">System-Only</span></span>            | <span data-ttu-id="04eab-229">False</span><span class="sxs-lookup"><span data-stu-id="04eab-229">False</span></span>                                            |
| <span data-ttu-id="04eab-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04eab-230">Is-Single-Valued</span></span>       | <span data-ttu-id="04eab-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="04eab-231">True</span></span>                                             |
| <span data-ttu-id="04eab-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04eab-232">Is Indexed</span></span>             | <span data-ttu-id="04eab-233">False</span><span class="sxs-lookup"><span data-stu-id="04eab-233">False</span></span>                                            |
| <span data-ttu-id="04eab-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04eab-234">In Global Catalog</span></span>      | <span data-ttu-id="04eab-235">False</span><span class="sxs-lookup"><span data-stu-id="04eab-235">False</span></span>                                            |
| <span data-ttu-id="04eab-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04eab-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="04eab-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04eab-237">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="04eab-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04eab-238">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="04eab-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04eab-239">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="04eab-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04eab-240">Search-Flags</span></span>           | <span data-ttu-id="04eab-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04eab-241">0x00000000</span></span>                                       |
| <span data-ttu-id="04eab-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04eab-242">System-Flags</span></span>           | <span data-ttu-id="04eab-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04eab-243">0x00000010</span></span>                                       |
| <span data-ttu-id="04eab-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04eab-244">Classes used in</span></span>        | [<span data-ttu-id="04eab-245">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="04eab-245">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="04eab-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="04eab-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="04eab-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04eab-247">Entry</span></span> | <span data-ttu-id="04eab-248">Wert</span><span class="sxs-lookup"><span data-stu-id="04eab-248">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="04eab-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04eab-249">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="04eab-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04eab-250">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="04eab-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="04eab-251">System-Only</span></span>            | <span data-ttu-id="04eab-252">False</span><span class="sxs-lookup"><span data-stu-id="04eab-252">False</span></span>                                            |
| <span data-ttu-id="04eab-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04eab-253">Is-Single-Valued</span></span>       | <span data-ttu-id="04eab-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="04eab-254">True</span></span>                                             |
| <span data-ttu-id="04eab-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04eab-255">Is Indexed</span></span>             | <span data-ttu-id="04eab-256">False</span><span class="sxs-lookup"><span data-stu-id="04eab-256">False</span></span>                                            |
| <span data-ttu-id="04eab-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04eab-257">In Global Catalog</span></span>      | <span data-ttu-id="04eab-258">False</span><span class="sxs-lookup"><span data-stu-id="04eab-258">False</span></span>                                            |
| <span data-ttu-id="04eab-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04eab-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="04eab-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04eab-260">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="04eab-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04eab-261">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="04eab-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04eab-262">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="04eab-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04eab-263">Search-Flags</span></span>           | <span data-ttu-id="04eab-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04eab-264">0x00000000</span></span>                                       |
| <span data-ttu-id="04eab-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04eab-265">System-Flags</span></span>           | <span data-ttu-id="04eab-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04eab-266">0x00000010</span></span>                                       |
| <span data-ttu-id="04eab-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04eab-267">Classes used in</span></span>        | [<span data-ttu-id="04eab-268">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="04eab-268">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="04eab-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04eab-269">Windows Server 2012</span></span>



| <span data-ttu-id="04eab-270">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04eab-270">Entry</span></span> | <span data-ttu-id="04eab-271">Wert</span><span class="sxs-lookup"><span data-stu-id="04eab-271">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="04eab-272">Link-ID</span><span class="sxs-lookup"><span data-stu-id="04eab-272">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="04eab-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04eab-273">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="04eab-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="04eab-274">System-Only</span></span>            | <span data-ttu-id="04eab-275">False</span><span class="sxs-lookup"><span data-stu-id="04eab-275">False</span></span>                                            |
| <span data-ttu-id="04eab-276">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="04eab-276">Is-Single-Valued</span></span>       | <span data-ttu-id="04eab-277">Richtig</span><span class="sxs-lookup"><span data-stu-id="04eab-277">True</span></span>                                             |
| <span data-ttu-id="04eab-278">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="04eab-278">Is Indexed</span></span>             | <span data-ttu-id="04eab-279">False</span><span class="sxs-lookup"><span data-stu-id="04eab-279">False</span></span>                                            |
| <span data-ttu-id="04eab-280">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="04eab-280">In Global Catalog</span></span>      | <span data-ttu-id="04eab-281">False</span><span class="sxs-lookup"><span data-stu-id="04eab-281">False</span></span>                                            |
| <span data-ttu-id="04eab-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04eab-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="04eab-283">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="04eab-283">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="04eab-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04eab-284">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="04eab-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04eab-285">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="04eab-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04eab-286">Search-Flags</span></span>           | <span data-ttu-id="04eab-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04eab-287">0x00000000</span></span>                                       |
| <span data-ttu-id="04eab-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04eab-288">System-Flags</span></span>           | <span data-ttu-id="04eab-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04eab-289">0x00000010</span></span>                                       |
| <span data-ttu-id="04eab-290">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="04eab-290">Classes used in</span></span>        | [<span data-ttu-id="04eab-291">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="04eab-291">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="04eab-292">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04eab-292">Remarks</span></span>

<span data-ttu-id="04eab-293">Jede Active Directory Gesamtstruktur enthält ein DS-Heuristics Attribut, das Einstellungen für die gesamte Gesamtstruktur enthält.</span><span class="sxs-lookup"><span data-stu-id="04eab-293">Each Active Directory forest contains a DS-Heuristics attribute that contains settings for the entire forest.</span></span> <span data-ttu-id="04eab-294">Das DS-Heuristics-Attribut ist ein Attribut des-Objekts "CN = Directory Service, CN = Windows NT, CN = Services, CN = Configuration <Domain> ".</span><span class="sxs-lookup"><span data-stu-id="04eab-294">The DS-Heuristics attribute is an attribute of the "CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,<Domain>" object.</span></span>

<span data-ttu-id="04eab-295">DS-Heuristics ist eine Unicode-Zeichenfolge, in der jedes Zeichen einen Wert für eine einzelne Domänen weite Einstellung enthält.</span><span class="sxs-lookup"><span data-stu-id="04eab-295">DS-Heuristics is a Unicode string in which each character contains a value for a single domain-wide setting.</span></span> <span data-ttu-id="04eab-296">Die DS-Heuristics Zeichenfolge hat das folgende Format.</span><span class="sxs-lookup"><span data-stu-id="04eab-296">The DS-Heuristics string takes the following format.</span></span>

``` syntax
|<1>|<2>|<3>|<4>|<5>|<6>|<7>|<8>|<9>|<10>|<11>|<12>|<13>|<14>|<15>|<16>|<17>|<18>|<19>|<20>|<21>|<22>|<23>|<24>|<25>|
```

<span data-ttu-id="04eab-297">Um die Datenvalidierung bereitzustellen, wird jedes zehnte Zeichen auf die Zeichenzahl dividiert durch 10 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="04eab-297">To provide data validation, each tenth character is set to the character number divided by ten.</span></span> <span data-ttu-id="04eab-298">Das zehnte Zeichen ist z. b. "1". Das 20. Zeichen ist "2" und so weiter.</span><span class="sxs-lookup"><span data-stu-id="04eab-298">For example, the tenth character is '1'; the twentieth character is '2', and so on.</span></span>

<span data-ttu-id="04eab-299">Bei allen Zeichen, die nicht festgelegt sind, wird angenommen, dass es sich um eine "0" handelt</span><span class="sxs-lookup"><span data-stu-id="04eab-299">Any character that is not set is assumed to be a '0'.</span></span> <span data-ttu-id="04eab-300">Wenn das DS-Heuristics-Attribut nicht festgelegt ist, wird davon ausgegangen, dass alle Werte "0" sind.</span><span class="sxs-lookup"><span data-stu-id="04eab-300">If the DS-Heuristics attribute is not set, all values are assumed to be '0'.</span></span> <span data-ttu-id="04eab-301">Zurzeit werden 25 Zeichen verwendet, und es ist nicht erforderlich, die Zeichenfolge aufzufüllen, um alle 25 Zeichen auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="04eab-301">There are currently 25 characters being used and it is not necessary to pad the string to fill all 25 characters.</span></span> <span data-ttu-id="04eab-302">Wenn z. b. das höchste verwendete Zeichen 7 ist, ist die Zeichenfolge "0000002" zulässig.</span><span class="sxs-lookup"><span data-stu-id="04eab-302">For example, if the highest character being used is 7, then the string "0000002" is acceptable.</span></span>

<span data-ttu-id="04eab-303">Ausführliche Informationen zu den einzelnen Zeichen finden Sie unter [dSHeuristics in \[ MS-ADTs \] Active Directory Technical Specification](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5).</span><span class="sxs-lookup"><span data-stu-id="04eab-303">For details about each character, see [dSHeuristics in \[MS-ADTS\] Active Directory Technical Specification](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5).</span></span>

### <a name="anr-search-filters"></a><span data-ttu-id="04eab-304">ANR-Suchfilter</span><span class="sxs-lookup"><span data-stu-id="04eab-304">ANR Search Filters</span></span>

<span data-ttu-id="04eab-305">Die Zeichen 1, 2 und 4 werden verwendet, um das Verhalten von ANR-Suchfiltern zu ändern.</span><span class="sxs-lookup"><span data-stu-id="04eab-305">Characters 1, 2, and 4 are used to modify the behavior of ANR search filters.</span></span> <span data-ttu-id="04eab-306">Wenn Zeichen 1 auf ' 1 ' festgelegt ist, wird die Erweiterung des ANR-Filters mit dem **Namen ' givenName**  -  **Nachname** ' (wenn Platz gefunden wird) deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="04eab-306">If character 1 is set to '1', then the expansion of the ANR filter to include **GivenName** - **Surname** (when space is found) is disabled.</span></span> <span data-ttu-id="04eab-307">Wenn Zeichen 2 auf ' 1 ' festgelegt ist, ist die Erweiterung des ANR-Filters auf den **Nachnamen**  -  **givenName** deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="04eab-307">If character 2 is set to '1', the expansion of the ANR filter to include **Surname** - **GivenName** is disabled.</span></span> <span data-ttu-id="04eab-308">Wenn ein eingebettetes Leerzeichen in der Such Zeichenfolge vorhanden ist, wird die Such Zeichenfolge normalerweise in zwei Zeichen folgen unterteilt, die paarweise mit den Attributen **givenName** und **Nachname** verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="04eab-308">If an embedded space is present in the search string, the search string will normally be divided into two strings, which are compared pair-wise against the **GivenName** and **Surname** attributes.</span></span> <span data-ttu-id="04eab-309">Durch Festlegen der Zeichen 1 und 2 auf ' 1 ' wird verhindert, dass diese Übereinstimmungen gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="04eab-309">Setting characters 1 and 2 to '1' will prevent those matches from being attempted.</span></span> <span data-ttu-id="04eab-310">Diese Übereinstimmung ist möglicherweise deaktiviert, wenn der Administrator sicher ist, dass die Suche nach "Jeff Smith" immer als "Jeff Smith" und nicht als "Smith, Jeff" bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="04eab-310">This matching might be disabled if the administrator is confident that searches for "Jeff Smith" would always be provided as "jeff smith" and not "smith, jeff".</span></span> <span data-ttu-id="04eab-311">Normalerweise wird nur eine oder die andere Übereinstimmung entsprechend der lokalen Konvention unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="04eab-311">Normally only one or the other match would be suppressed, according to local convention.</span></span>

<span data-ttu-id="04eab-312">Wenn das Zeichen 4 auf ' 1 ' festgelegt ist, führt Active Directory die "präemptiven Spitznamen Auflösung" aus.</span><span class="sxs-lookup"><span data-stu-id="04eab-312">If the character 4 is set to '1' then Active Directory will perform "pre-emptive nickname resolution".</span></span> <span data-ttu-id="04eab-313">Das heißt, wenn die Such Zeichenfolge genau mit dem Spitznamen genau eines Objekts im Suchbereich übereinstimmt, wird ein Objekt als Ergebnis der Suche zurückgegeben, und der Rest von ANR wird übersprungen.</span><span class="sxs-lookup"><span data-stu-id="04eab-313">That is, if the search string exactly matches the nickname of exactly one object in the search scope, that one object is returned as the result of the search, and the rest of ANR is skipped.</span></span> <span data-ttu-id="04eab-314">Beachten Sie Folgendes: während der Rest der ANR-Suche über LDAP verfügbar ist, ist die präemptiv Spitzname-Auflösung (auch bekannt als "Spitzname-Snap") nur über MAPI verfügbar.</span><span class="sxs-lookup"><span data-stu-id="04eab-314">Note that while the rest of ANR searching is available through LDAP, pre-emptive nickname resolution (also known as "nickname snap") is available only through MAPI.</span></span>

## <a name="see-also"></a><span data-ttu-id="04eab-315">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04eab-315">See also</span></span>

<dl> <dt>

<span data-ttu-id="04eab-316">[dSHeuristics in \[ MS-ADTs \] Active Directory technische Spezifikation](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5)</span><span class="sxs-lookup"><span data-stu-id="04eab-316">[dSHeuristics in \[MS-ADTS\] Active Directory Technical Specification](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5)</span></span>
</dt> </dl>

 

