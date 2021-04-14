---
title: Control-Access-Rights-Attribut
description: Wird von der DS-Sicherheit verwendet, um zu bestimmen, welche Benutzer bestimmte Vorgänge für das Host Objekt ausführen können.
ms.assetid: 5e717160-519c-4e5a-b18f-05ee767a66a3
ms.tgt_platform: multiple
keywords:
- AD-Schema für Control-Access-Rights-Attribut
- controlaccessrights-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Control-Access-Rights
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e3ee9075cfaf4c5bbfbf17e8e2cfef6166be032
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480463"
---
# <a name="control-access-rights-attribute"></a><span data-ttu-id="c4fe2-105">Control-Access-Rights-Attribut</span><span class="sxs-lookup"><span data-stu-id="c4fe2-105">Control-Access-Rights attribute</span></span>

<span data-ttu-id="c4fe2-106">Wird von der DS-Sicherheit verwendet, um zu bestimmen, welche Benutzer bestimmte Vorgänge für das Host Objekt ausführen können.</span><span class="sxs-lookup"><span data-stu-id="c4fe2-106">Used by DS Security to determine which users can perform specific operations on the host object.</span></span>



| <span data-ttu-id="c4fe2-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4fe2-107">Entry</span></span> | <span data-ttu-id="c4fe2-108">Wert</span><span class="sxs-lookup"><span data-stu-id="c4fe2-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="c4fe2-109">CN</span><span class="sxs-lookup"><span data-stu-id="c4fe2-109">CN</span></span>                | <span data-ttu-id="c4fe2-110">Control-Access-Rights</span><span class="sxs-lookup"><span data-stu-id="c4fe2-110">Control-Access-Rights</span></span>                                 |
| <span data-ttu-id="c4fe2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c4fe2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c4fe2-112">controlaccessrights</span><span class="sxs-lookup"><span data-stu-id="c4fe2-112">controlAccessRights</span></span>                                   |
| <span data-ttu-id="c4fe2-113">Size</span><span class="sxs-lookup"><span data-stu-id="c4fe2-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="c4fe2-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c4fe2-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="c4fe2-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="c4fe2-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="c4fe2-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c4fe2-116">Attribute-Id</span></span>      | <span data-ttu-id="c4fe2-117">1.2.840.113556.1.4.200</span><span class="sxs-lookup"><span data-stu-id="c4fe2-117">1.2.840.113556.1.4.200</span></span>                                |
| <span data-ttu-id="c4fe2-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c4fe2-118">System-Id-Guid</span></span>    | <span data-ttu-id="c4fe2-119">6da8a4fc-0e52-11D0-a286-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c4fe2-119">6da8a4fc-0e52-11d0-a286-00aa003049e2</span></span>                  |
| <span data-ttu-id="c4fe2-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4fe2-120">Syntax</span></span>            | [<span data-ttu-id="c4fe2-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="c4fe2-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="c4fe2-122">Implementations</span></span>

-   [<span data-ttu-id="c4fe2-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c4fe2-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c4fe2-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c4fe2-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c4fe2-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c4fe2-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c4fe2-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c4fe2-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c4fe2-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4fe2-130">Entry</span></span> | <span data-ttu-id="c4fe2-131">Wert</span><span class="sxs-lookup"><span data-stu-id="c4fe2-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4fe2-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c4fe2-132">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="c4fe2-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4fe2-133">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="c4fe2-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4fe2-134">System-Only</span></span>            | <span data-ttu-id="c4fe2-135">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-135">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c4fe2-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c4fe2-137">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-137">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c4fe2-138">Is Indexed</span></span>             | <span data-ttu-id="c4fe2-139">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-139">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c4fe2-140">In Global Catalog</span></span>      | <span data-ttu-id="c4fe2-141">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-141">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4fe2-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4fe2-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c4fe2-143">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="c4fe2-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4fe2-144">Range-Lower</span></span>            | <span data-ttu-id="c4fe2-145">16</span><span class="sxs-lookup"><span data-stu-id="c4fe2-145">16</span></span>                                                                                                                 |
| <span data-ttu-id="c4fe2-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4fe2-146">Range-Upper</span></span>            | <span data-ttu-id="c4fe2-147">16</span><span class="sxs-lookup"><span data-stu-id="c4fe2-147">16</span></span>                                                                                                                 |
| <span data-ttu-id="c4fe2-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4fe2-148">Search-Flags</span></span>           | <span data-ttu-id="c4fe2-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4fe2-149">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="c4fe2-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4fe2-150">System-Flags</span></span>           | <span data-ttu-id="c4fe2-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4fe2-151">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="c4fe2-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c4fe2-152">Classes used in</span></span>        | [<span data-ttu-id="c4fe2-153">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-153">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c4fe2-154">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="c4fe2-155">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c4fe2-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c4fe2-156">Windows Server 2003</span></span>



| <span data-ttu-id="c4fe2-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4fe2-157">Entry</span></span> | <span data-ttu-id="c4fe2-158">Wert</span><span class="sxs-lookup"><span data-stu-id="c4fe2-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4fe2-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c4fe2-159">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="c4fe2-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4fe2-160">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="c4fe2-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4fe2-161">System-Only</span></span>            | <span data-ttu-id="c4fe2-162">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-162">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c4fe2-163">Is-Single-Valued</span></span>       | <span data-ttu-id="c4fe2-164">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-164">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c4fe2-165">Is Indexed</span></span>             | <span data-ttu-id="c4fe2-166">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-166">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c4fe2-167">In Global Catalog</span></span>      | <span data-ttu-id="c4fe2-168">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-168">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4fe2-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4fe2-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c4fe2-170">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="c4fe2-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4fe2-171">Range-Lower</span></span>            | <span data-ttu-id="c4fe2-172">16</span><span class="sxs-lookup"><span data-stu-id="c4fe2-172">16</span></span>                                                                                                                 |
| <span data-ttu-id="c4fe2-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4fe2-173">Range-Upper</span></span>            | <span data-ttu-id="c4fe2-174">16</span><span class="sxs-lookup"><span data-stu-id="c4fe2-174">16</span></span>                                                                                                                 |
| <span data-ttu-id="c4fe2-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4fe2-175">Search-Flags</span></span>           | <span data-ttu-id="c4fe2-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4fe2-176">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="c4fe2-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4fe2-177">System-Flags</span></span>           | <span data-ttu-id="c4fe2-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4fe2-178">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="c4fe2-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c4fe2-179">Classes used in</span></span>        | [<span data-ttu-id="c4fe2-180">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-180">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c4fe2-181">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-181">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="c4fe2-182">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-182">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c4fe2-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c4fe2-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c4fe2-184">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4fe2-184">Entry</span></span> | <span data-ttu-id="c4fe2-185">Wert</span><span class="sxs-lookup"><span data-stu-id="c4fe2-185">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4fe2-186">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c4fe2-186">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="c4fe2-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4fe2-187">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="c4fe2-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4fe2-188">System-Only</span></span>            | <span data-ttu-id="c4fe2-189">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-189">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-190">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c4fe2-190">Is-Single-Valued</span></span>       | <span data-ttu-id="c4fe2-191">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-191">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-192">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c4fe2-192">Is Indexed</span></span>             | <span data-ttu-id="c4fe2-193">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-193">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-194">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c4fe2-194">In Global Catalog</span></span>      | <span data-ttu-id="c4fe2-195">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-195">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-196">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4fe2-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4fe2-197">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c4fe2-197">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="c4fe2-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4fe2-198">Range-Lower</span></span>            | <span data-ttu-id="c4fe2-199">16</span><span class="sxs-lookup"><span data-stu-id="c4fe2-199">16</span></span>                                                                                                                 |
| <span data-ttu-id="c4fe2-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4fe2-200">Range-Upper</span></span>            | <span data-ttu-id="c4fe2-201">16</span><span class="sxs-lookup"><span data-stu-id="c4fe2-201">16</span></span>                                                                                                                 |
| <span data-ttu-id="c4fe2-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4fe2-202">Search-Flags</span></span>           | <span data-ttu-id="c4fe2-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4fe2-203">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="c4fe2-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4fe2-204">System-Flags</span></span>           | <span data-ttu-id="c4fe2-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4fe2-205">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="c4fe2-206">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c4fe2-206">Classes used in</span></span>        | [<span data-ttu-id="c4fe2-207">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-207">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c4fe2-208">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-208">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="c4fe2-209">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c4fe2-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4fe2-210">Windows Server 2008</span></span>



| <span data-ttu-id="c4fe2-211">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4fe2-211">Entry</span></span> | <span data-ttu-id="c4fe2-212">Wert</span><span class="sxs-lookup"><span data-stu-id="c4fe2-212">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4fe2-213">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c4fe2-213">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="c4fe2-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4fe2-214">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="c4fe2-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4fe2-215">System-Only</span></span>            | <span data-ttu-id="c4fe2-216">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-216">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-217">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c4fe2-217">Is-Single-Valued</span></span>       | <span data-ttu-id="c4fe2-218">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-218">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-219">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c4fe2-219">Is Indexed</span></span>             | <span data-ttu-id="c4fe2-220">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-220">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-221">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c4fe2-221">In Global Catalog</span></span>      | <span data-ttu-id="c4fe2-222">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-222">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4fe2-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4fe2-224">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c4fe2-224">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="c4fe2-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4fe2-225">Range-Lower</span></span>            | <span data-ttu-id="c4fe2-226">16</span><span class="sxs-lookup"><span data-stu-id="c4fe2-226">16</span></span>                                                                                                                 |
| <span data-ttu-id="c4fe2-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4fe2-227">Range-Upper</span></span>            | <span data-ttu-id="c4fe2-228">16</span><span class="sxs-lookup"><span data-stu-id="c4fe2-228">16</span></span>                                                                                                                 |
| <span data-ttu-id="c4fe2-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4fe2-229">Search-Flags</span></span>           | <span data-ttu-id="c4fe2-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4fe2-230">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="c4fe2-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4fe2-231">System-Flags</span></span>           | <span data-ttu-id="c4fe2-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4fe2-232">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="c4fe2-233">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c4fe2-233">Classes used in</span></span>        | [<span data-ttu-id="c4fe2-234">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-234">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c4fe2-235">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-235">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="c4fe2-236">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-236">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c4fe2-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c4fe2-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c4fe2-238">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4fe2-238">Entry</span></span> | <span data-ttu-id="c4fe2-239">Wert</span><span class="sxs-lookup"><span data-stu-id="c4fe2-239">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4fe2-240">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c4fe2-240">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="c4fe2-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4fe2-241">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="c4fe2-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4fe2-242">System-Only</span></span>            | <span data-ttu-id="c4fe2-243">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-243">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-244">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c4fe2-244">Is-Single-Valued</span></span>       | <span data-ttu-id="c4fe2-245">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-245">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-246">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c4fe2-246">Is Indexed</span></span>             | <span data-ttu-id="c4fe2-247">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-247">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-248">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c4fe2-248">In Global Catalog</span></span>      | <span data-ttu-id="c4fe2-249">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-249">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-250">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4fe2-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4fe2-251">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c4fe2-251">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="c4fe2-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4fe2-252">Range-Lower</span></span>            | <span data-ttu-id="c4fe2-253">16</span><span class="sxs-lookup"><span data-stu-id="c4fe2-253">16</span></span>                                                                                                                 |
| <span data-ttu-id="c4fe2-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4fe2-254">Range-Upper</span></span>            | <span data-ttu-id="c4fe2-255">16</span><span class="sxs-lookup"><span data-stu-id="c4fe2-255">16</span></span>                                                                                                                 |
| <span data-ttu-id="c4fe2-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4fe2-256">Search-Flags</span></span>           | <span data-ttu-id="c4fe2-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4fe2-257">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="c4fe2-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4fe2-258">System-Flags</span></span>           | <span data-ttu-id="c4fe2-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4fe2-259">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="c4fe2-260">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c4fe2-260">Classes used in</span></span>        | [<span data-ttu-id="c4fe2-261">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-261">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c4fe2-262">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-262">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="c4fe2-263">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-263">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c4fe2-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c4fe2-264">Windows Server 2012</span></span>



| <span data-ttu-id="c4fe2-265">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4fe2-265">Entry</span></span> | <span data-ttu-id="c4fe2-266">Wert</span><span class="sxs-lookup"><span data-stu-id="c4fe2-266">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4fe2-267">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c4fe2-267">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="c4fe2-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4fe2-268">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="c4fe2-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4fe2-269">System-Only</span></span>            | <span data-ttu-id="c4fe2-270">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-270">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-271">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c4fe2-271">Is-Single-Valued</span></span>       | <span data-ttu-id="c4fe2-272">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-272">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-273">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c4fe2-273">Is Indexed</span></span>             | <span data-ttu-id="c4fe2-274">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-274">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-275">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c4fe2-275">In Global Catalog</span></span>      | <span data-ttu-id="c4fe2-276">False</span><span class="sxs-lookup"><span data-stu-id="c4fe2-276">False</span></span>                                                                                                              |
| <span data-ttu-id="c4fe2-277">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4fe2-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4fe2-278">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c4fe2-278">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="c4fe2-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4fe2-279">Range-Lower</span></span>            | <span data-ttu-id="c4fe2-280">16</span><span class="sxs-lookup"><span data-stu-id="c4fe2-280">16</span></span>                                                                                                                 |
| <span data-ttu-id="c4fe2-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4fe2-281">Range-Upper</span></span>            | <span data-ttu-id="c4fe2-282">16</span><span class="sxs-lookup"><span data-stu-id="c4fe2-282">16</span></span>                                                                                                                 |
| <span data-ttu-id="c4fe2-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4fe2-283">Search-Flags</span></span>           | <span data-ttu-id="c4fe2-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4fe2-284">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="c4fe2-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4fe2-285">System-Flags</span></span>           | <span data-ttu-id="c4fe2-286">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4fe2-286">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="c4fe2-287">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c4fe2-287">Classes used in</span></span>        | [<span data-ttu-id="c4fe2-288">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-288">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c4fe2-289">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-289">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="c4fe2-290">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c4fe2-290">**User**</span></span>](c-user.md)<br/> |



 

 





