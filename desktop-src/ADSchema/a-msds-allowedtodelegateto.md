---
title: ms-DS-allowed-to-Delegat-Attribut
description: Hierbei handelt es sich um ein Attribut für Dienst Konto Objekte (Computer-oder Benutzerkonten).
ms.assetid: a370174e-fd00-4f47-b23c-b0cc2657cee7
ms.tgt_platform: multiple
keywords:
- AD-Schema für das "ms-DS-allowed-to-Delegat"-Attribut
- AD-Schema für das msDS-Zustellungs Attribut
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Delegate-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9562442d20053848e48cd2b1d501e65611f7d2a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344134"
---
# <a name="ms-ds-allowed-to-delegate-to-attribute"></a><span data-ttu-id="79ff1-105">ms-DS-allowed-to-Delegat-Attribut</span><span class="sxs-lookup"><span data-stu-id="79ff1-105">ms-DS-Allowed-To-Delegate-To attribute</span></span>

<span data-ttu-id="79ff1-106">Hierbei handelt es sich um ein Attribut für Dienst Konto Objekte (Computer-oder Benutzerkonten).</span><span class="sxs-lookup"><span data-stu-id="79ff1-106">This is an attribute on service account (computer or user account) objects.</span></span> <span data-ttu-id="79ff1-107">Sie enthält eine Liste von Dienst Prinzipal Namen (SPNs).</span><span class="sxs-lookup"><span data-stu-id="79ff1-107">It contains a list of Service Principal Names (SPNs).</span></span> <span data-ttu-id="79ff1-108">Dieses Attribut wird verwendet, um einen Dienst so zu konfigurieren, dass er Dienst Tickets abrufen kann, die für die eingeschränkte Delegierung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="79ff1-108">This attribute is used to configure a service so that it can obtain service tickets that can be used for Constrained Delegation.</span></span>



| <span data-ttu-id="79ff1-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="79ff1-109">Entry</span></span> | <span data-ttu-id="79ff1-110">Wert</span><span class="sxs-lookup"><span data-stu-id="79ff1-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="79ff1-111">CN</span><span class="sxs-lookup"><span data-stu-id="79ff1-111">CN</span></span>                | <span data-ttu-id="79ff1-112">ms-DS-allowed-to-Delegat-an</span><span class="sxs-lookup"><span data-stu-id="79ff1-112">ms-DS-Allowed-To-Delegate-To</span></span>                |
| <span data-ttu-id="79ff1-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="79ff1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="79ff1-114">MSDS-Zuweisung</span><span class="sxs-lookup"><span data-stu-id="79ff1-114">msDS-AllowedToDelegateTo</span></span>                    |
| <span data-ttu-id="79ff1-115">Size</span><span class="sxs-lookup"><span data-stu-id="79ff1-115">Size</span></span>              | <span data-ttu-id="79ff1-116">0 bis 64K</span><span class="sxs-lookup"><span data-stu-id="79ff1-116">0 to 64K</span></span>                                    |
| <span data-ttu-id="79ff1-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="79ff1-117">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="79ff1-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="79ff1-118">Update Frequency</span></span>  | <span data-ttu-id="79ff1-119">Selten</span><span class="sxs-lookup"><span data-stu-id="79ff1-119">Infrequently</span></span>                                |
| <span data-ttu-id="79ff1-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="79ff1-120">Attribute-Id</span></span>      | <span data-ttu-id="79ff1-121">1.2.840.113556.1.4.1787</span><span class="sxs-lookup"><span data-stu-id="79ff1-121">1.2.840.113556.1.4.1787</span></span>                     |
| <span data-ttu-id="79ff1-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="79ff1-122">System-Id-Guid</span></span>    | <span data-ttu-id="79ff1-123">800d94d7-b7a1-42A1-b14d-7cae1423d07f</span><span class="sxs-lookup"><span data-stu-id="79ff1-123">800d94d7-b7a1-42a1-b14d-7cae1423d07f</span></span>        |
| <span data-ttu-id="79ff1-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="79ff1-124">Syntax</span></span>            | [<span data-ttu-id="79ff1-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="79ff1-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="79ff1-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="79ff1-126">Implementations</span></span>

-   [<span data-ttu-id="79ff1-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="79ff1-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="79ff1-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="79ff1-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="79ff1-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="79ff1-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="79ff1-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="79ff1-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="79ff1-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="79ff1-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="79ff1-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="79ff1-132">Windows Server 2003</span></span>



| <span data-ttu-id="79ff1-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="79ff1-133">Entry</span></span> | <span data-ttu-id="79ff1-134">Wert</span><span class="sxs-lookup"><span data-stu-id="79ff1-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="79ff1-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="79ff1-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="79ff1-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79ff1-136">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="79ff1-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="79ff1-137">System-Only</span></span>            | <span data-ttu-id="79ff1-138">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-138">False</span></span>                                                              |
| <span data-ttu-id="79ff1-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="79ff1-139">Is-Single-Valued</span></span>       | <span data-ttu-id="79ff1-140">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-140">False</span></span>                                                              |
| <span data-ttu-id="79ff1-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="79ff1-141">Is Indexed</span></span>             | <span data-ttu-id="79ff1-142">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-142">False</span></span>                                                              |
| <span data-ttu-id="79ff1-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="79ff1-143">In Global Catalog</span></span>      | <span data-ttu-id="79ff1-144">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-144">False</span></span>                                                              |
| <span data-ttu-id="79ff1-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79ff1-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="79ff1-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="79ff1-146">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="79ff1-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79ff1-147">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="79ff1-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79ff1-148">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="79ff1-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79ff1-149">Search-Flags</span></span>           | <span data-ttu-id="79ff1-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79ff1-150">0x00000000</span></span>                                                         |
| <span data-ttu-id="79ff1-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79ff1-151">System-Flags</span></span>           | <span data-ttu-id="79ff1-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79ff1-152">0x00000010</span></span>                                                         |
| <span data-ttu-id="79ff1-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="79ff1-153">Classes used in</span></span>        | [<span data-ttu-id="79ff1-154">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="79ff1-154">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="79ff1-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="79ff1-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="79ff1-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="79ff1-156">Entry</span></span> | <span data-ttu-id="79ff1-157">Wert</span><span class="sxs-lookup"><span data-stu-id="79ff1-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="79ff1-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="79ff1-158">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="79ff1-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79ff1-159">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="79ff1-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="79ff1-160">System-Only</span></span>            | <span data-ttu-id="79ff1-161">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-161">False</span></span>                                                              |
| <span data-ttu-id="79ff1-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="79ff1-162">Is-Single-Valued</span></span>       | <span data-ttu-id="79ff1-163">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-163">False</span></span>                                                              |
| <span data-ttu-id="79ff1-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="79ff1-164">Is Indexed</span></span>             | <span data-ttu-id="79ff1-165">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-165">False</span></span>                                                              |
| <span data-ttu-id="79ff1-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="79ff1-166">In Global Catalog</span></span>      | <span data-ttu-id="79ff1-167">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-167">False</span></span>                                                              |
| <span data-ttu-id="79ff1-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79ff1-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="79ff1-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="79ff1-169">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="79ff1-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79ff1-170">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="79ff1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79ff1-171">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="79ff1-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79ff1-172">Search-Flags</span></span>           | <span data-ttu-id="79ff1-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79ff1-173">0x00000000</span></span>                                                         |
| <span data-ttu-id="79ff1-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79ff1-174">System-Flags</span></span>           | <span data-ttu-id="79ff1-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79ff1-175">0x00000010</span></span>                                                         |
| <span data-ttu-id="79ff1-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="79ff1-176">Classes used in</span></span>        | [<span data-ttu-id="79ff1-177">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="79ff1-177">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="79ff1-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79ff1-178">Windows Server 2008</span></span>



| <span data-ttu-id="79ff1-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="79ff1-179">Entry</span></span> | <span data-ttu-id="79ff1-180">Wert</span><span class="sxs-lookup"><span data-stu-id="79ff1-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="79ff1-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="79ff1-181">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="79ff1-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79ff1-182">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="79ff1-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="79ff1-183">System-Only</span></span>            | <span data-ttu-id="79ff1-184">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-184">False</span></span>                                                              |
| <span data-ttu-id="79ff1-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="79ff1-185">Is-Single-Valued</span></span>       | <span data-ttu-id="79ff1-186">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-186">False</span></span>                                                              |
| <span data-ttu-id="79ff1-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="79ff1-187">Is Indexed</span></span>             | <span data-ttu-id="79ff1-188">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-188">False</span></span>                                                              |
| <span data-ttu-id="79ff1-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="79ff1-189">In Global Catalog</span></span>      | <span data-ttu-id="79ff1-190">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-190">False</span></span>                                                              |
| <span data-ttu-id="79ff1-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79ff1-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="79ff1-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="79ff1-192">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="79ff1-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79ff1-193">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="79ff1-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79ff1-194">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="79ff1-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79ff1-195">Search-Flags</span></span>           | <span data-ttu-id="79ff1-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79ff1-196">0x00000000</span></span>                                                         |
| <span data-ttu-id="79ff1-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79ff1-197">System-Flags</span></span>           | <span data-ttu-id="79ff1-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79ff1-198">0x00000010</span></span>                                                         |
| <span data-ttu-id="79ff1-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="79ff1-199">Classes used in</span></span>        | [<span data-ttu-id="79ff1-200">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="79ff1-200">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="79ff1-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="79ff1-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="79ff1-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="79ff1-202">Entry</span></span> | <span data-ttu-id="79ff1-203">Wert</span><span class="sxs-lookup"><span data-stu-id="79ff1-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="79ff1-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="79ff1-204">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="79ff1-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79ff1-205">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="79ff1-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="79ff1-206">System-Only</span></span>            | <span data-ttu-id="79ff1-207">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-207">False</span></span>                                                              |
| <span data-ttu-id="79ff1-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="79ff1-208">Is-Single-Valued</span></span>       | <span data-ttu-id="79ff1-209">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-209">False</span></span>                                                              |
| <span data-ttu-id="79ff1-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="79ff1-210">Is Indexed</span></span>             | <span data-ttu-id="79ff1-211">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-211">False</span></span>                                                              |
| <span data-ttu-id="79ff1-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="79ff1-212">In Global Catalog</span></span>      | <span data-ttu-id="79ff1-213">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-213">False</span></span>                                                              |
| <span data-ttu-id="79ff1-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79ff1-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="79ff1-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="79ff1-215">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="79ff1-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79ff1-216">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="79ff1-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79ff1-217">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="79ff1-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79ff1-218">Search-Flags</span></span>           | <span data-ttu-id="79ff1-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79ff1-219">0x00000000</span></span>                                                         |
| <span data-ttu-id="79ff1-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79ff1-220">System-Flags</span></span>           | <span data-ttu-id="79ff1-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79ff1-221">0x00000010</span></span>                                                         |
| <span data-ttu-id="79ff1-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="79ff1-222">Classes used in</span></span>        | [<span data-ttu-id="79ff1-223">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="79ff1-223">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="79ff1-224">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="79ff1-224">Windows Server 2012</span></span>



| <span data-ttu-id="79ff1-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="79ff1-225">Entry</span></span> | <span data-ttu-id="79ff1-226">Wert</span><span class="sxs-lookup"><span data-stu-id="79ff1-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="79ff1-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="79ff1-227">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="79ff1-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79ff1-228">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="79ff1-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="79ff1-229">System-Only</span></span>            | <span data-ttu-id="79ff1-230">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-230">False</span></span>                                                              |
| <span data-ttu-id="79ff1-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="79ff1-231">Is-Single-Valued</span></span>       | <span data-ttu-id="79ff1-232">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-232">False</span></span>                                                              |
| <span data-ttu-id="79ff1-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="79ff1-233">Is Indexed</span></span>             | <span data-ttu-id="79ff1-234">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-234">False</span></span>                                                              |
| <span data-ttu-id="79ff1-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="79ff1-235">In Global Catalog</span></span>      | <span data-ttu-id="79ff1-236">False</span><span class="sxs-lookup"><span data-stu-id="79ff1-236">False</span></span>                                                              |
| <span data-ttu-id="79ff1-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79ff1-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="79ff1-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="79ff1-238">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="79ff1-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79ff1-239">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="79ff1-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79ff1-240">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="79ff1-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79ff1-241">Search-Flags</span></span>           | <span data-ttu-id="79ff1-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79ff1-242">0x00000000</span></span>                                                         |
| <span data-ttu-id="79ff1-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79ff1-243">System-Flags</span></span>           | <span data-ttu-id="79ff1-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79ff1-244">0x00000010</span></span>                                                         |
| <span data-ttu-id="79ff1-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="79ff1-245">Classes used in</span></span>        | [<span data-ttu-id="79ff1-246">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="79ff1-246">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





