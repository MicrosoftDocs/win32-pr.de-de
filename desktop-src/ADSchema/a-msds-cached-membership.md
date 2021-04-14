---
title: ms-DS-zwischengespeicherte Mitgliedschafts Attribut
description: Das Attribut "ms-DS-Cached-Membership" wird vom Sicherheits Konten-Manager für die Gruppen Erweiterung während der tokenbewertung verwendet.
ms.assetid: e54c5d55-d292-4a6e-942a-3818f5d75301
ms.tgt_platform: multiple
keywords:
- AD-Schema für die Mitgliedschaft in der Mitgliedschaft in ms-DS-Cache
- AD-Schema für MSDS-zwischengespeicherte Mitgliedschafts Attribute
topic_type:
- apiref
api_name:
- ms-DS-Cached-Membership
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936c5c21d33d19ee51dba7f1dec0b03299cee346
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104520175"
---
# <a name="ms-ds-cached-membership-attribute"></a><span data-ttu-id="5b978-105">ms-DS-zwischengespeicherte Mitgliedschafts Attribut</span><span class="sxs-lookup"><span data-stu-id="5b978-105">ms-DS-Cached-Membership attribute</span></span>

<span data-ttu-id="5b978-106">Das Attribut " **ms-DS-Cached-Membership** " wird vom Sicherheits Konten-Manager für die Gruppen Erweiterung während der tokenbewertung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b978-106">The **ms-DS-Cached-Membership** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="5b978-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5b978-107">Entry</span></span> | <span data-ttu-id="5b978-108">Wert</span><span class="sxs-lookup"><span data-stu-id="5b978-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="5b978-109">CN</span><span class="sxs-lookup"><span data-stu-id="5b978-109">CN</span></span>                | <span data-ttu-id="5b978-110">ms-DS-zwischengespeicherte Mitgliedschaft</span><span class="sxs-lookup"><span data-stu-id="5b978-110">ms-DS-Cached-Membership</span></span>                               |
| <span data-ttu-id="5b978-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5b978-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5b978-112">zwischengespeicherte MSDS-Mitgliedschaft</span><span class="sxs-lookup"><span data-stu-id="5b978-112">msDS-Cached-Membership</span></span>                                |
| <span data-ttu-id="5b978-113">Size</span><span class="sxs-lookup"><span data-stu-id="5b978-113">Size</span></span>              | <span data-ttu-id="5b978-114">Binäres Blob von bis zu 3 Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="5b978-114">Binary BLOB of up to 3 kilobytes.</span></span>                     |
| <span data-ttu-id="5b978-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5b978-115">Update Privilege</span></span>  | <span data-ttu-id="5b978-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5b978-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="5b978-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="5b978-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="5b978-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5b978-118">Attribute-Id</span></span>      | <span data-ttu-id="5b978-119">1.2.840.113556.1.4.1441</span><span class="sxs-lookup"><span data-stu-id="5b978-119">1.2.840.113556.1.4.1441</span></span>                               |
| <span data-ttu-id="5b978-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5b978-120">System-Id-Guid</span></span>    | <span data-ttu-id="5b978-121">69cab008-cdd4-4bc9-bab8-0ff37efe1b20</span><span class="sxs-lookup"><span data-stu-id="5b978-121">69cab008-cdd4-4bc9-bab8-0ff37efe1b20</span></span>                  |
| <span data-ttu-id="5b978-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b978-122">Syntax</span></span>            | [<span data-ttu-id="5b978-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="5b978-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="5b978-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="5b978-124">Implementations</span></span>

-   [<span data-ttu-id="5b978-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5b978-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5b978-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5b978-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5b978-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5b978-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5b978-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5b978-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5b978-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5b978-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="5b978-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5b978-130">Windows Server 2003</span></span>



| <span data-ttu-id="5b978-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5b978-131">Entry</span></span> | <span data-ttu-id="5b978-132">Wert</span><span class="sxs-lookup"><span data-stu-id="5b978-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="5b978-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5b978-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="5b978-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b978-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="5b978-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b978-135">System-Only</span></span>            | <span data-ttu-id="5b978-136">False</span><span class="sxs-lookup"><span data-stu-id="5b978-136">False</span></span>                             |
| <span data-ttu-id="5b978-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5b978-137">Is-Single-Valued</span></span>       | <span data-ttu-id="5b978-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="5b978-138">True</span></span>                              |
| <span data-ttu-id="5b978-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5b978-139">Is Indexed</span></span>             | <span data-ttu-id="5b978-140">False</span><span class="sxs-lookup"><span data-stu-id="5b978-140">False</span></span>                             |
| <span data-ttu-id="5b978-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5b978-141">In Global Catalog</span></span>      | <span data-ttu-id="5b978-142">False</span><span class="sxs-lookup"><span data-stu-id="5b978-142">False</span></span>                             |
| <span data-ttu-id="5b978-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5b978-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b978-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5b978-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="5b978-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b978-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="5b978-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b978-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="5b978-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b978-147">Search-Flags</span></span>           | <span data-ttu-id="5b978-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b978-148">0x00000000</span></span>                        |
| <span data-ttu-id="5b978-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b978-149">System-Flags</span></span>           | <span data-ttu-id="5b978-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5b978-150">0x00000011</span></span>                        |
| <span data-ttu-id="5b978-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5b978-151">Classes used in</span></span>        | [<span data-ttu-id="5b978-152">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="5b978-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5b978-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5b978-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5b978-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5b978-154">Entry</span></span> | <span data-ttu-id="5b978-155">Wert</span><span class="sxs-lookup"><span data-stu-id="5b978-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="5b978-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5b978-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="5b978-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b978-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="5b978-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b978-158">System-Only</span></span>            | <span data-ttu-id="5b978-159">False</span><span class="sxs-lookup"><span data-stu-id="5b978-159">False</span></span>                             |
| <span data-ttu-id="5b978-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5b978-160">Is-Single-Valued</span></span>       | <span data-ttu-id="5b978-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="5b978-161">True</span></span>                              |
| <span data-ttu-id="5b978-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5b978-162">Is Indexed</span></span>             | <span data-ttu-id="5b978-163">False</span><span class="sxs-lookup"><span data-stu-id="5b978-163">False</span></span>                             |
| <span data-ttu-id="5b978-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5b978-164">In Global Catalog</span></span>      | <span data-ttu-id="5b978-165">False</span><span class="sxs-lookup"><span data-stu-id="5b978-165">False</span></span>                             |
| <span data-ttu-id="5b978-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5b978-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b978-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5b978-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="5b978-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b978-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="5b978-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b978-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="5b978-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b978-170">Search-Flags</span></span>           | <span data-ttu-id="5b978-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b978-171">0x00000000</span></span>                        |
| <span data-ttu-id="5b978-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b978-172">System-Flags</span></span>           | <span data-ttu-id="5b978-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5b978-173">0x00000011</span></span>                        |
| <span data-ttu-id="5b978-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5b978-174">Classes used in</span></span>        | [<span data-ttu-id="5b978-175">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="5b978-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5b978-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b978-176">Windows Server 2008</span></span>



| <span data-ttu-id="5b978-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5b978-177">Entry</span></span> | <span data-ttu-id="5b978-178">Wert</span><span class="sxs-lookup"><span data-stu-id="5b978-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="5b978-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5b978-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="5b978-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b978-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="5b978-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b978-181">System-Only</span></span>            | <span data-ttu-id="5b978-182">False</span><span class="sxs-lookup"><span data-stu-id="5b978-182">False</span></span>                             |
| <span data-ttu-id="5b978-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5b978-183">Is-Single-Valued</span></span>       | <span data-ttu-id="5b978-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="5b978-184">True</span></span>                              |
| <span data-ttu-id="5b978-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5b978-185">Is Indexed</span></span>             | <span data-ttu-id="5b978-186">False</span><span class="sxs-lookup"><span data-stu-id="5b978-186">False</span></span>                             |
| <span data-ttu-id="5b978-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5b978-187">In Global Catalog</span></span>      | <span data-ttu-id="5b978-188">False</span><span class="sxs-lookup"><span data-stu-id="5b978-188">False</span></span>                             |
| <span data-ttu-id="5b978-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5b978-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b978-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5b978-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="5b978-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b978-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="5b978-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b978-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="5b978-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b978-193">Search-Flags</span></span>           | <span data-ttu-id="5b978-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b978-194">0x00000000</span></span>                        |
| <span data-ttu-id="5b978-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b978-195">System-Flags</span></span>           | <span data-ttu-id="5b978-196">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5b978-196">0x00000011</span></span>                        |
| <span data-ttu-id="5b978-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5b978-197">Classes used in</span></span>        | [<span data-ttu-id="5b978-198">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="5b978-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5b978-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5b978-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5b978-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5b978-200">Entry</span></span> | <span data-ttu-id="5b978-201">Wert</span><span class="sxs-lookup"><span data-stu-id="5b978-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="5b978-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5b978-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="5b978-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b978-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="5b978-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b978-204">System-Only</span></span>            | <span data-ttu-id="5b978-205">False</span><span class="sxs-lookup"><span data-stu-id="5b978-205">False</span></span>                             |
| <span data-ttu-id="5b978-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5b978-206">Is-Single-Valued</span></span>       | <span data-ttu-id="5b978-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="5b978-207">True</span></span>                              |
| <span data-ttu-id="5b978-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5b978-208">Is Indexed</span></span>             | <span data-ttu-id="5b978-209">False</span><span class="sxs-lookup"><span data-stu-id="5b978-209">False</span></span>                             |
| <span data-ttu-id="5b978-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5b978-210">In Global Catalog</span></span>      | <span data-ttu-id="5b978-211">False</span><span class="sxs-lookup"><span data-stu-id="5b978-211">False</span></span>                             |
| <span data-ttu-id="5b978-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5b978-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b978-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5b978-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="5b978-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b978-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="5b978-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b978-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="5b978-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b978-216">Search-Flags</span></span>           | <span data-ttu-id="5b978-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b978-217">0x00000000</span></span>                        |
| <span data-ttu-id="5b978-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b978-218">System-Flags</span></span>           | <span data-ttu-id="5b978-219">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5b978-219">0x00000011</span></span>                        |
| <span data-ttu-id="5b978-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5b978-220">Classes used in</span></span>        | [<span data-ttu-id="5b978-221">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="5b978-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5b978-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5b978-222">Windows Server 2012</span></span>



| <span data-ttu-id="5b978-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5b978-223">Entry</span></span> | <span data-ttu-id="5b978-224">Wert</span><span class="sxs-lookup"><span data-stu-id="5b978-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="5b978-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5b978-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="5b978-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b978-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="5b978-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b978-227">System-Only</span></span>            | <span data-ttu-id="5b978-228">False</span><span class="sxs-lookup"><span data-stu-id="5b978-228">False</span></span>                             |
| <span data-ttu-id="5b978-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5b978-229">Is-Single-Valued</span></span>       | <span data-ttu-id="5b978-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="5b978-230">True</span></span>                              |
| <span data-ttu-id="5b978-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5b978-231">Is Indexed</span></span>             | <span data-ttu-id="5b978-232">False</span><span class="sxs-lookup"><span data-stu-id="5b978-232">False</span></span>                             |
| <span data-ttu-id="5b978-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5b978-233">In Global Catalog</span></span>      | <span data-ttu-id="5b978-234">False</span><span class="sxs-lookup"><span data-stu-id="5b978-234">False</span></span>                             |
| <span data-ttu-id="5b978-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5b978-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b978-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5b978-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="5b978-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b978-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="5b978-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b978-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="5b978-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b978-239">Search-Flags</span></span>           | <span data-ttu-id="5b978-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b978-240">0x00000000</span></span>                        |
| <span data-ttu-id="5b978-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b978-241">System-Flags</span></span>           | <span data-ttu-id="5b978-242">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5b978-242">0x00000011</span></span>                        |
| <span data-ttu-id="5b978-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5b978-243">Classes used in</span></span>        | [<span data-ttu-id="5b978-244">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="5b978-244">**User**</span></span>](c-user.md)<br/> |



 

 





