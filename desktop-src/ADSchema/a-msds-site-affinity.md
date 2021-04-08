---
title: ms-DS-Site-Affinitäts Attribut
description: Das Attribut "ms-DS-Site-Affinität" wird vom Sicherheits Konten-Manager für die Gruppen Erweiterung während der tokenbewertung verwendet.
ms.assetid: c05df70a-adbb-48e0-bdcd-c1d83a2e43bd
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-Site-Affinitäts Attribut
- AD-Schema für MSDS-Site-Affinitäts Attribut
topic_type:
- apiref
api_name:
- ms-DS-Site-Affinity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dd3ed17b07c73d9e7a6a2d93d93463e1dea40fc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859834"
---
# <a name="ms-ds-site-affinity-attribute"></a><span data-ttu-id="b33e1-105">ms-DS-Site-Affinitäts Attribut</span><span class="sxs-lookup"><span data-stu-id="b33e1-105">ms-DS-Site-Affinity attribute</span></span>

<span data-ttu-id="b33e1-106">Das Attribut " **ms-DS-Site-Affinität** " wird vom Sicherheits Konten-Manager für die Gruppen Erweiterung während der tokenbewertung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b33e1-106">The **ms-DS-Site-Affinity** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="b33e1-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b33e1-107">Entry</span></span> | <span data-ttu-id="b33e1-108">Wert</span><span class="sxs-lookup"><span data-stu-id="b33e1-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b33e1-109">CN</span><span class="sxs-lookup"><span data-stu-id="b33e1-109">CN</span></span>                | <span data-ttu-id="b33e1-110">ms-DS-Site-Affinität</span><span class="sxs-lookup"><span data-stu-id="b33e1-110">ms-DS-Site-Affinity</span></span>                                                                     |
| <span data-ttu-id="b33e1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b33e1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b33e1-112">MSDS-Site-Affinität</span><span class="sxs-lookup"><span data-stu-id="b33e1-112">msDS-Site-Affinity</span></span>                                                                      |
| <span data-ttu-id="b33e1-113">Size</span><span class="sxs-lookup"><span data-stu-id="b33e1-113">Size</span></span>              | <span data-ttu-id="b33e1-114">Binary BLOB mit mehreren Werten, wobei jeder Wert sizeof (GUID) + sizeof (Large \_ Integer) ist.</span><span class="sxs-lookup"><span data-stu-id="b33e1-114">Multiple-valued binary BLOB, where each value is sizeof(GUID) + sizeof(LARGE\_INTEGER).</span></span> |
| <span data-ttu-id="b33e1-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b33e1-115">Update Privilege</span></span>  | \-                                                                                      |
| <span data-ttu-id="b33e1-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b33e1-116">Update Frequency</span></span>  | <span data-ttu-id="b33e1-117">Standardmäßig alle drei Monate.</span><span class="sxs-lookup"><span data-stu-id="b33e1-117">By default once every three months.</span></span>                                                     |
| <span data-ttu-id="b33e1-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b33e1-118">Attribute-Id</span></span>      | <span data-ttu-id="b33e1-119">1.2.840.113556.1.4.1443</span><span class="sxs-lookup"><span data-stu-id="b33e1-119">1.2.840.113556.1.4.1443</span></span>                                                                 |
| <span data-ttu-id="b33e1-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b33e1-120">System-Id-Guid</span></span>    | <span data-ttu-id="b33e1-121">c17c5602-bcb7-46f0-9656-6370ca884b72</span><span class="sxs-lookup"><span data-stu-id="b33e1-121">c17c5602-bcb7-46f0-9656-6370ca884b72</span></span>                                                    |
| <span data-ttu-id="b33e1-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="b33e1-122">Syntax</span></span>            | [<span data-ttu-id="b33e1-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="b33e1-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                   |



## <a name="implementations"></a><span data-ttu-id="b33e1-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b33e1-124">Implementations</span></span>

-   [<span data-ttu-id="b33e1-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b33e1-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b33e1-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b33e1-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b33e1-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b33e1-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b33e1-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b33e1-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b33e1-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b33e1-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b33e1-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b33e1-130">Windows Server 2003</span></span>



| <span data-ttu-id="b33e1-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b33e1-131">Entry</span></span> | <span data-ttu-id="b33e1-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b33e1-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b33e1-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b33e1-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b33e1-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b33e1-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b33e1-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b33e1-135">System-Only</span></span>            | <span data-ttu-id="b33e1-136">False</span><span class="sxs-lookup"><span data-stu-id="b33e1-136">False</span></span>                             |
| <span data-ttu-id="b33e1-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b33e1-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b33e1-138">False</span><span class="sxs-lookup"><span data-stu-id="b33e1-138">False</span></span>                             |
| <span data-ttu-id="b33e1-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b33e1-139">Is Indexed</span></span>             | <span data-ttu-id="b33e1-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="b33e1-140">True</span></span>                              |
| <span data-ttu-id="b33e1-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b33e1-141">In Global Catalog</span></span>      | <span data-ttu-id="b33e1-142">False</span><span class="sxs-lookup"><span data-stu-id="b33e1-142">False</span></span>                             |
| <span data-ttu-id="b33e1-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b33e1-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b33e1-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b33e1-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b33e1-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b33e1-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b33e1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b33e1-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b33e1-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b33e1-147">Search-Flags</span></span>           | <span data-ttu-id="b33e1-148">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b33e1-148">0x00000001</span></span>                        |
| <span data-ttu-id="b33e1-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b33e1-149">System-Flags</span></span>           | <span data-ttu-id="b33e1-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b33e1-150">0x00000010</span></span>                        |
| <span data-ttu-id="b33e1-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b33e1-151">Classes used in</span></span>        | [<span data-ttu-id="b33e1-152">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b33e1-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b33e1-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b33e1-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b33e1-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b33e1-154">Entry</span></span> | <span data-ttu-id="b33e1-155">Wert</span><span class="sxs-lookup"><span data-stu-id="b33e1-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b33e1-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b33e1-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b33e1-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b33e1-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b33e1-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="b33e1-158">System-Only</span></span>            | <span data-ttu-id="b33e1-159">False</span><span class="sxs-lookup"><span data-stu-id="b33e1-159">False</span></span>                             |
| <span data-ttu-id="b33e1-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b33e1-160">Is-Single-Valued</span></span>       | <span data-ttu-id="b33e1-161">False</span><span class="sxs-lookup"><span data-stu-id="b33e1-161">False</span></span>                             |
| <span data-ttu-id="b33e1-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b33e1-162">Is Indexed</span></span>             | <span data-ttu-id="b33e1-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="b33e1-163">True</span></span>                              |
| <span data-ttu-id="b33e1-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b33e1-164">In Global Catalog</span></span>      | <span data-ttu-id="b33e1-165">False</span><span class="sxs-lookup"><span data-stu-id="b33e1-165">False</span></span>                             |
| <span data-ttu-id="b33e1-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b33e1-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="b33e1-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b33e1-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b33e1-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b33e1-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b33e1-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b33e1-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b33e1-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b33e1-170">Search-Flags</span></span>           | <span data-ttu-id="b33e1-171">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b33e1-171">0x00000001</span></span>                        |
| <span data-ttu-id="b33e1-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b33e1-172">System-Flags</span></span>           | <span data-ttu-id="b33e1-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b33e1-173">0x00000010</span></span>                        |
| <span data-ttu-id="b33e1-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b33e1-174">Classes used in</span></span>        | [<span data-ttu-id="b33e1-175">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b33e1-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b33e1-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b33e1-176">Windows Server 2008</span></span>



| <span data-ttu-id="b33e1-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b33e1-177">Entry</span></span> | <span data-ttu-id="b33e1-178">Wert</span><span class="sxs-lookup"><span data-stu-id="b33e1-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b33e1-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b33e1-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b33e1-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b33e1-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b33e1-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b33e1-181">System-Only</span></span>            | <span data-ttu-id="b33e1-182">False</span><span class="sxs-lookup"><span data-stu-id="b33e1-182">False</span></span>                             |
| <span data-ttu-id="b33e1-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b33e1-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b33e1-184">False</span><span class="sxs-lookup"><span data-stu-id="b33e1-184">False</span></span>                             |
| <span data-ttu-id="b33e1-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b33e1-185">Is Indexed</span></span>             | <span data-ttu-id="b33e1-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="b33e1-186">True</span></span>                              |
| <span data-ttu-id="b33e1-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b33e1-187">In Global Catalog</span></span>      | <span data-ttu-id="b33e1-188">False</span><span class="sxs-lookup"><span data-stu-id="b33e1-188">False</span></span>                             |
| <span data-ttu-id="b33e1-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b33e1-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b33e1-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b33e1-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b33e1-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b33e1-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b33e1-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b33e1-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b33e1-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b33e1-193">Search-Flags</span></span>           | <span data-ttu-id="b33e1-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b33e1-194">0x00000001</span></span>                        |
| <span data-ttu-id="b33e1-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b33e1-195">System-Flags</span></span>           | <span data-ttu-id="b33e1-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b33e1-196">0x00000010</span></span>                        |
| <span data-ttu-id="b33e1-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b33e1-197">Classes used in</span></span>        | [<span data-ttu-id="b33e1-198">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b33e1-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b33e1-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b33e1-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b33e1-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b33e1-200">Entry</span></span> | <span data-ttu-id="b33e1-201">Wert</span><span class="sxs-lookup"><span data-stu-id="b33e1-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b33e1-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b33e1-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b33e1-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b33e1-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b33e1-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="b33e1-204">System-Only</span></span>            | <span data-ttu-id="b33e1-205">False</span><span class="sxs-lookup"><span data-stu-id="b33e1-205">False</span></span>                             |
| <span data-ttu-id="b33e1-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b33e1-206">Is-Single-Valued</span></span>       | <span data-ttu-id="b33e1-207">False</span><span class="sxs-lookup"><span data-stu-id="b33e1-207">False</span></span>                             |
| <span data-ttu-id="b33e1-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b33e1-208">Is Indexed</span></span>             | <span data-ttu-id="b33e1-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="b33e1-209">True</span></span>                              |
| <span data-ttu-id="b33e1-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b33e1-210">In Global Catalog</span></span>      | <span data-ttu-id="b33e1-211">False</span><span class="sxs-lookup"><span data-stu-id="b33e1-211">False</span></span>                             |
| <span data-ttu-id="b33e1-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b33e1-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="b33e1-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b33e1-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b33e1-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b33e1-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b33e1-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b33e1-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b33e1-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b33e1-216">Search-Flags</span></span>           | <span data-ttu-id="b33e1-217">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b33e1-217">0x00000001</span></span>                        |
| <span data-ttu-id="b33e1-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b33e1-218">System-Flags</span></span>           | <span data-ttu-id="b33e1-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b33e1-219">0x00000010</span></span>                        |
| <span data-ttu-id="b33e1-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b33e1-220">Classes used in</span></span>        | [<span data-ttu-id="b33e1-221">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b33e1-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b33e1-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b33e1-222">Windows Server 2012</span></span>



| <span data-ttu-id="b33e1-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b33e1-223">Entry</span></span> | <span data-ttu-id="b33e1-224">Wert</span><span class="sxs-lookup"><span data-stu-id="b33e1-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b33e1-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b33e1-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b33e1-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b33e1-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b33e1-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b33e1-227">System-Only</span></span>            | <span data-ttu-id="b33e1-228">False</span><span class="sxs-lookup"><span data-stu-id="b33e1-228">False</span></span>                             |
| <span data-ttu-id="b33e1-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b33e1-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b33e1-230">False</span><span class="sxs-lookup"><span data-stu-id="b33e1-230">False</span></span>                             |
| <span data-ttu-id="b33e1-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b33e1-231">Is Indexed</span></span>             | <span data-ttu-id="b33e1-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="b33e1-232">True</span></span>                              |
| <span data-ttu-id="b33e1-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b33e1-233">In Global Catalog</span></span>      | <span data-ttu-id="b33e1-234">False</span><span class="sxs-lookup"><span data-stu-id="b33e1-234">False</span></span>                             |
| <span data-ttu-id="b33e1-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b33e1-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b33e1-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b33e1-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b33e1-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b33e1-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b33e1-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b33e1-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b33e1-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b33e1-239">Search-Flags</span></span>           | <span data-ttu-id="b33e1-240">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b33e1-240">0x00000001</span></span>                        |
| <span data-ttu-id="b33e1-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b33e1-241">System-Flags</span></span>           | <span data-ttu-id="b33e1-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b33e1-242">0x00000010</span></span>                        |
| <span data-ttu-id="b33e1-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b33e1-243">Classes used in</span></span>        | [<span data-ttu-id="b33e1-244">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b33e1-244">**User**</span></span>](c-user.md)<br/> |



 

 





