---
title: LabeledURI-Attribut
description: Eine Uniform Resource Identifier, auf die eine Bezeichnung folgt.
ms.assetid: 214b5b4b-7389-4801-977c-24ffc2e025bd
ms.tgt_platform: multiple
keywords:
- AD-Schema für das LabeledURI-Attribut
topic_type:
- apiref
api_name:
- labeledURI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bcfae6b1d2029fd916cf2e796e611a6b76318bc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479783"
---
# <a name="labeleduri-attribute"></a><span data-ttu-id="25565-104">LabeledURI-Attribut</span><span class="sxs-lookup"><span data-stu-id="25565-104">labeledURI attribute</span></span>

<span data-ttu-id="25565-105">Eine Uniform Resource Identifier, auf die eine Bezeichnung folgt.</span><span class="sxs-lookup"><span data-stu-id="25565-105">A Uniform Resource Identifier followed by a label.</span></span> <span data-ttu-id="25565-106">Die Bezeichnung wird verwendet, um die Ressource zu beschreiben, auf die der URI verweist, und ist als Anzeige Name gedacht, der Menschen lesbar ist.</span><span class="sxs-lookup"><span data-stu-id="25565-106">The label is used to describe the resource to which the URI points, and is intended as a display name that is human-readable.</span></span>



| <span data-ttu-id="25565-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="25565-107">Entry</span></span> | <span data-ttu-id="25565-108">Wert</span><span class="sxs-lookup"><span data-stu-id="25565-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="25565-109">CN</span><span class="sxs-lookup"><span data-stu-id="25565-109">CN</span></span>                | <span data-ttu-id="25565-110">LabeledURI</span><span class="sxs-lookup"><span data-stu-id="25565-110">labeledURI</span></span>                                  |
| <span data-ttu-id="25565-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="25565-111">Ldap-Display-Name</span></span> | <span data-ttu-id="25565-112">LabeledURI</span><span class="sxs-lookup"><span data-stu-id="25565-112">labeledURI</span></span>                                  |
| <span data-ttu-id="25565-113">Size</span><span class="sxs-lookup"><span data-stu-id="25565-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="25565-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="25565-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="25565-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="25565-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="25565-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="25565-116">Attribute-Id</span></span>      | <span data-ttu-id="25565-117">1.3.6.1.4.1.250.1.57</span><span class="sxs-lookup"><span data-stu-id="25565-117">1.3.6.1.4.1.250.1.57</span></span>                        |
| <span data-ttu-id="25565-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="25565-118">System-Id-Guid</span></span>    | <span data-ttu-id="25565-119">c569bb46-c680-44bc-a273-e6c227d71b45</span><span class="sxs-lookup"><span data-stu-id="25565-119">c569bb46-c680-44bc-a273-e6c227d71b45</span></span>        |
| <span data-ttu-id="25565-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="25565-120">Syntax</span></span>            | [<span data-ttu-id="25565-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="25565-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="25565-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="25565-122">Implementations</span></span>

-   [<span data-ttu-id="25565-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="25565-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="25565-124">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="25565-124">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="25565-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="25565-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="25565-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="25565-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="25565-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="25565-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="25565-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="25565-128">Windows Server 2003</span></span>



| <span data-ttu-id="25565-129">Eingabe</span><span class="sxs-lookup"><span data-stu-id="25565-129">Entry</span></span> | <span data-ttu-id="25565-130">Wert</span><span class="sxs-lookup"><span data-stu-id="25565-130">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25565-131">Link-ID</span><span class="sxs-lookup"><span data-stu-id="25565-131">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="25565-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25565-132">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="25565-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="25565-133">System-Only</span></span>            | <span data-ttu-id="25565-134">False</span><span class="sxs-lookup"><span data-stu-id="25565-134">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-135">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="25565-135">Is-Single-Valued</span></span>       | <span data-ttu-id="25565-136">False</span><span class="sxs-lookup"><span data-stu-id="25565-136">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-137">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="25565-137">Is Indexed</span></span>             | <span data-ttu-id="25565-138">False</span><span class="sxs-lookup"><span data-stu-id="25565-138">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-139">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="25565-139">In Global Catalog</span></span>      | <span data-ttu-id="25565-140">False</span><span class="sxs-lookup"><span data-stu-id="25565-140">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="25565-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="25565-142">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="25565-142">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="25565-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25565-143">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="25565-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25565-144">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="25565-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25565-145">Search-Flags</span></span>           | <span data-ttu-id="25565-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25565-146">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="25565-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25565-147">System-Flags</span></span>           | <span data-ttu-id="25565-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25565-148">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="25565-149">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="25565-149">Classes used in</span></span>        | [<span data-ttu-id="25565-150">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="25565-150">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="25565-151">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="25565-151">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="25565-152">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="25565-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="25565-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="25565-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="25565-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="25565-154">Entry</span></span> | <span data-ttu-id="25565-155">Wert</span><span class="sxs-lookup"><span data-stu-id="25565-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25565-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="25565-156">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="25565-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25565-157">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="25565-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="25565-158">System-Only</span></span>            | <span data-ttu-id="25565-159">False</span><span class="sxs-lookup"><span data-stu-id="25565-159">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="25565-160">Is-Single-Valued</span></span>       | <span data-ttu-id="25565-161">False</span><span class="sxs-lookup"><span data-stu-id="25565-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="25565-162">Is Indexed</span></span>             | <span data-ttu-id="25565-163">False</span><span class="sxs-lookup"><span data-stu-id="25565-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="25565-164">In Global Catalog</span></span>      | <span data-ttu-id="25565-165">False</span><span class="sxs-lookup"><span data-stu-id="25565-165">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="25565-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="25565-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="25565-167">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="25565-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25565-168">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="25565-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25565-169">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="25565-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25565-170">Search-Flags</span></span>           | <span data-ttu-id="25565-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25565-171">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="25565-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25565-172">System-Flags</span></span>           | <span data-ttu-id="25565-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25565-173">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="25565-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="25565-174">Classes used in</span></span>        | [<span data-ttu-id="25565-175">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="25565-175">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="25565-176">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="25565-176">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="25565-177">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="25565-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="25565-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25565-178">Windows Server 2008</span></span>



| <span data-ttu-id="25565-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="25565-179">Entry</span></span> | <span data-ttu-id="25565-180">Wert</span><span class="sxs-lookup"><span data-stu-id="25565-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25565-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="25565-181">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="25565-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25565-182">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="25565-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="25565-183">System-Only</span></span>            | <span data-ttu-id="25565-184">False</span><span class="sxs-lookup"><span data-stu-id="25565-184">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="25565-185">Is-Single-Valued</span></span>       | <span data-ttu-id="25565-186">False</span><span class="sxs-lookup"><span data-stu-id="25565-186">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="25565-187">Is Indexed</span></span>             | <span data-ttu-id="25565-188">False</span><span class="sxs-lookup"><span data-stu-id="25565-188">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="25565-189">In Global Catalog</span></span>      | <span data-ttu-id="25565-190">False</span><span class="sxs-lookup"><span data-stu-id="25565-190">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="25565-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="25565-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="25565-192">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="25565-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25565-193">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="25565-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25565-194">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="25565-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25565-195">Search-Flags</span></span>           | <span data-ttu-id="25565-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25565-196">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="25565-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25565-197">System-Flags</span></span>           | <span data-ttu-id="25565-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25565-198">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="25565-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="25565-199">Classes used in</span></span>        | [<span data-ttu-id="25565-200">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="25565-200">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="25565-201">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="25565-201">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="25565-202">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="25565-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="25565-203">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="25565-203">Windows Server 2008 R2</span></span>



| <span data-ttu-id="25565-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="25565-204">Entry</span></span> | <span data-ttu-id="25565-205">Wert</span><span class="sxs-lookup"><span data-stu-id="25565-205">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25565-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="25565-206">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="25565-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25565-207">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="25565-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="25565-208">System-Only</span></span>            | <span data-ttu-id="25565-209">False</span><span class="sxs-lookup"><span data-stu-id="25565-209">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="25565-210">Is-Single-Valued</span></span>       | <span data-ttu-id="25565-211">False</span><span class="sxs-lookup"><span data-stu-id="25565-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="25565-212">Is Indexed</span></span>             | <span data-ttu-id="25565-213">False</span><span class="sxs-lookup"><span data-stu-id="25565-213">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="25565-214">In Global Catalog</span></span>      | <span data-ttu-id="25565-215">False</span><span class="sxs-lookup"><span data-stu-id="25565-215">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="25565-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="25565-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="25565-217">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="25565-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25565-218">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="25565-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25565-219">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="25565-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25565-220">Search-Flags</span></span>           | <span data-ttu-id="25565-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25565-221">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="25565-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25565-222">System-Flags</span></span>           | <span data-ttu-id="25565-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25565-223">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="25565-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="25565-224">Classes used in</span></span>        | [<span data-ttu-id="25565-225">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="25565-225">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="25565-226">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="25565-226">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="25565-227">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="25565-227">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="25565-228">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="25565-228">Windows Server 2012</span></span>



| <span data-ttu-id="25565-229">Eingabe</span><span class="sxs-lookup"><span data-stu-id="25565-229">Entry</span></span> | <span data-ttu-id="25565-230">Wert</span><span class="sxs-lookup"><span data-stu-id="25565-230">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25565-231">Link-ID</span><span class="sxs-lookup"><span data-stu-id="25565-231">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="25565-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25565-232">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="25565-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="25565-233">System-Only</span></span>            | <span data-ttu-id="25565-234">False</span><span class="sxs-lookup"><span data-stu-id="25565-234">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-235">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="25565-235">Is-Single-Valued</span></span>       | <span data-ttu-id="25565-236">False</span><span class="sxs-lookup"><span data-stu-id="25565-236">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-237">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="25565-237">Is Indexed</span></span>             | <span data-ttu-id="25565-238">False</span><span class="sxs-lookup"><span data-stu-id="25565-238">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-239">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="25565-239">In Global Catalog</span></span>      | <span data-ttu-id="25565-240">False</span><span class="sxs-lookup"><span data-stu-id="25565-240">False</span></span>                                                                                                                                      |
| <span data-ttu-id="25565-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="25565-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="25565-242">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="25565-242">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="25565-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25565-243">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="25565-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25565-244">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="25565-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25565-245">Search-Flags</span></span>           | <span data-ttu-id="25565-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25565-246">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="25565-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25565-247">System-Flags</span></span>           | <span data-ttu-id="25565-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25565-248">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="25565-249">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="25565-249">Classes used in</span></span>        | [<span data-ttu-id="25565-250">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="25565-250">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="25565-251">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="25565-251">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="25565-252">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="25565-252">**User**</span></span>](c-user.md)<br/> |



 

 





