---
title: ms-DS-zwischen gespeicherter Mitgliedschafts Zeitstempel-Attribut
description: Das Attribut ms-DS-Cached-Membership-Zeitstempel wird vom Sicherheits Konten-Manager für die Gruppen Erweiterung während der tokenauswertung verwendet.
ms.assetid: cb096f79-a57b-4001-b197-e75522904734
ms.tgt_platform: multiple
keywords:
- "\"ms-DS--zwischen gespeicherter-Zeitstempel Attribut-AD-Schema\""
- AD-Schema für das mit MSDS zwischengespeicherte Mitgliedschafts-Zeitstempel Attribut
topic_type:
- apiref
api_name:
- ms-DS-Cached-Membership-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 403e87288d906587a11f2a140a9f447ce8236aca
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106340040"
---
# <a name="ms-ds-cached-membership-time-stamp-attribute"></a><span data-ttu-id="d733a-105">ms-DS-zwischen gespeicherter Mitgliedschafts Zeitstempel-Attribut</span><span class="sxs-lookup"><span data-stu-id="d733a-105">ms-DS-Cached-Membership-Time-Stamp attribute</span></span>

<span data-ttu-id="d733a-106">Das Attribut **ms-DS-Cached-Membership-Zeitstempel** wird vom Sicherheits Konten-Manager für die Gruppen Erweiterung während der tokenauswertung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d733a-106">The **ms-DS-Cached-Membership-Time-Stamp** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="d733a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d733a-107">Entry</span></span> | <span data-ttu-id="d733a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="d733a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d733a-109">CN</span><span class="sxs-lookup"><span data-stu-id="d733a-109">CN</span></span>                | <span data-ttu-id="d733a-110">ms-DS-zwischengespeicherte Mitgliedschafts Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="d733a-110">ms-DS-Cached-Membership-Time-Stamp</span></span>   |
| <span data-ttu-id="d733a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d733a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d733a-112">MSDS-Cache-Membership-Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="d733a-112">msDS-Cached-Membership-Time-Stamp</span></span>    |
| <span data-ttu-id="d733a-113">Size</span><span class="sxs-lookup"><span data-stu-id="d733a-113">Size</span></span>              | <span data-ttu-id="d733a-114">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="d733a-114">8 bytes</span></span>                              |
| <span data-ttu-id="d733a-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d733a-115">Update Privilege</span></span>  | <span data-ttu-id="d733a-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d733a-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="d733a-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="d733a-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="d733a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d733a-118">Attribute-Id</span></span>      | <span data-ttu-id="d733a-119">1.2.840.113556.1.4.1442</span><span class="sxs-lookup"><span data-stu-id="d733a-119">1.2.840.113556.1.4.1442</span></span>              |
| <span data-ttu-id="d733a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d733a-120">System-Id-Guid</span></span>    | <span data-ttu-id="d733a-121">3566bf1f-Beee-4dcb-8abe-ef89fcfec6c1</span><span class="sxs-lookup"><span data-stu-id="d733a-121">3566bf1f-beee-4dcb-8abe-ef89fcfec6c1</span></span> |
| <span data-ttu-id="d733a-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="d733a-122">Syntax</span></span>            | [<span data-ttu-id="d733a-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="d733a-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="d733a-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="d733a-124">Implementations</span></span>

-   [<span data-ttu-id="d733a-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d733a-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d733a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d733a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d733a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d733a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d733a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d733a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d733a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d733a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d733a-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d733a-130">Windows Server 2003</span></span>



| <span data-ttu-id="d733a-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d733a-131">Entry</span></span> | <span data-ttu-id="d733a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="d733a-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d733a-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d733a-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d733a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d733a-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d733a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d733a-135">System-Only</span></span>            | <span data-ttu-id="d733a-136">False</span><span class="sxs-lookup"><span data-stu-id="d733a-136">False</span></span>                             |
| <span data-ttu-id="d733a-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d733a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d733a-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="d733a-138">True</span></span>                              |
| <span data-ttu-id="d733a-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d733a-139">Is Indexed</span></span>             | <span data-ttu-id="d733a-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="d733a-140">True</span></span>                              |
| <span data-ttu-id="d733a-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d733a-141">In Global Catalog</span></span>      | <span data-ttu-id="d733a-142">False</span><span class="sxs-lookup"><span data-stu-id="d733a-142">False</span></span>                             |
| <span data-ttu-id="d733a-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d733a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d733a-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d733a-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d733a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d733a-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d733a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d733a-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d733a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d733a-147">Search-Flags</span></span>           | <span data-ttu-id="d733a-148">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d733a-148">0x00000001</span></span>                        |
| <span data-ttu-id="d733a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d733a-149">System-Flags</span></span>           | <span data-ttu-id="d733a-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="d733a-150">0x00000011</span></span>                        |
| <span data-ttu-id="d733a-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d733a-151">Classes used in</span></span>        | [<span data-ttu-id="d733a-152">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="d733a-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d733a-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d733a-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d733a-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d733a-154">Entry</span></span> | <span data-ttu-id="d733a-155">Wert</span><span class="sxs-lookup"><span data-stu-id="d733a-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d733a-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d733a-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d733a-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d733a-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d733a-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d733a-158">System-Only</span></span>            | <span data-ttu-id="d733a-159">False</span><span class="sxs-lookup"><span data-stu-id="d733a-159">False</span></span>                             |
| <span data-ttu-id="d733a-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d733a-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d733a-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="d733a-161">True</span></span>                              |
| <span data-ttu-id="d733a-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d733a-162">Is Indexed</span></span>             | <span data-ttu-id="d733a-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="d733a-163">True</span></span>                              |
| <span data-ttu-id="d733a-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d733a-164">In Global Catalog</span></span>      | <span data-ttu-id="d733a-165">False</span><span class="sxs-lookup"><span data-stu-id="d733a-165">False</span></span>                             |
| <span data-ttu-id="d733a-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d733a-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d733a-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d733a-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d733a-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d733a-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d733a-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d733a-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d733a-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d733a-170">Search-Flags</span></span>           | <span data-ttu-id="d733a-171">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d733a-171">0x00000001</span></span>                        |
| <span data-ttu-id="d733a-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d733a-172">System-Flags</span></span>           | <span data-ttu-id="d733a-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="d733a-173">0x00000011</span></span>                        |
| <span data-ttu-id="d733a-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d733a-174">Classes used in</span></span>        | [<span data-ttu-id="d733a-175">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="d733a-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d733a-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d733a-176">Windows Server 2008</span></span>



| <span data-ttu-id="d733a-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d733a-177">Entry</span></span> | <span data-ttu-id="d733a-178">Wert</span><span class="sxs-lookup"><span data-stu-id="d733a-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d733a-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d733a-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d733a-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d733a-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d733a-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d733a-181">System-Only</span></span>            | <span data-ttu-id="d733a-182">False</span><span class="sxs-lookup"><span data-stu-id="d733a-182">False</span></span>                             |
| <span data-ttu-id="d733a-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d733a-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d733a-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="d733a-184">True</span></span>                              |
| <span data-ttu-id="d733a-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d733a-185">Is Indexed</span></span>             | <span data-ttu-id="d733a-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="d733a-186">True</span></span>                              |
| <span data-ttu-id="d733a-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d733a-187">In Global Catalog</span></span>      | <span data-ttu-id="d733a-188">False</span><span class="sxs-lookup"><span data-stu-id="d733a-188">False</span></span>                             |
| <span data-ttu-id="d733a-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d733a-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d733a-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d733a-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d733a-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d733a-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d733a-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d733a-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d733a-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d733a-193">Search-Flags</span></span>           | <span data-ttu-id="d733a-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d733a-194">0x00000001</span></span>                        |
| <span data-ttu-id="d733a-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d733a-195">System-Flags</span></span>           | <span data-ttu-id="d733a-196">0x00000011</span><span class="sxs-lookup"><span data-stu-id="d733a-196">0x00000011</span></span>                        |
| <span data-ttu-id="d733a-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d733a-197">Classes used in</span></span>        | [<span data-ttu-id="d733a-198">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="d733a-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d733a-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d733a-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d733a-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d733a-200">Entry</span></span> | <span data-ttu-id="d733a-201">Wert</span><span class="sxs-lookup"><span data-stu-id="d733a-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d733a-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d733a-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d733a-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d733a-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d733a-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d733a-204">System-Only</span></span>            | <span data-ttu-id="d733a-205">False</span><span class="sxs-lookup"><span data-stu-id="d733a-205">False</span></span>                             |
| <span data-ttu-id="d733a-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d733a-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d733a-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="d733a-207">True</span></span>                              |
| <span data-ttu-id="d733a-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d733a-208">Is Indexed</span></span>             | <span data-ttu-id="d733a-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="d733a-209">True</span></span>                              |
| <span data-ttu-id="d733a-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d733a-210">In Global Catalog</span></span>      | <span data-ttu-id="d733a-211">False</span><span class="sxs-lookup"><span data-stu-id="d733a-211">False</span></span>                             |
| <span data-ttu-id="d733a-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d733a-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d733a-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d733a-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d733a-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d733a-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d733a-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d733a-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d733a-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d733a-216">Search-Flags</span></span>           | <span data-ttu-id="d733a-217">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d733a-217">0x00000001</span></span>                        |
| <span data-ttu-id="d733a-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d733a-218">System-Flags</span></span>           | <span data-ttu-id="d733a-219">0x00000011</span><span class="sxs-lookup"><span data-stu-id="d733a-219">0x00000011</span></span>                        |
| <span data-ttu-id="d733a-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d733a-220">Classes used in</span></span>        | [<span data-ttu-id="d733a-221">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="d733a-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d733a-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d733a-222">Windows Server 2012</span></span>



| <span data-ttu-id="d733a-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d733a-223">Entry</span></span> | <span data-ttu-id="d733a-224">Wert</span><span class="sxs-lookup"><span data-stu-id="d733a-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d733a-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d733a-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d733a-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d733a-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d733a-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d733a-227">System-Only</span></span>            | <span data-ttu-id="d733a-228">False</span><span class="sxs-lookup"><span data-stu-id="d733a-228">False</span></span>                             |
| <span data-ttu-id="d733a-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d733a-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d733a-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="d733a-230">True</span></span>                              |
| <span data-ttu-id="d733a-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d733a-231">Is Indexed</span></span>             | <span data-ttu-id="d733a-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="d733a-232">True</span></span>                              |
| <span data-ttu-id="d733a-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d733a-233">In Global Catalog</span></span>      | <span data-ttu-id="d733a-234">False</span><span class="sxs-lookup"><span data-stu-id="d733a-234">False</span></span>                             |
| <span data-ttu-id="d733a-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d733a-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d733a-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d733a-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d733a-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d733a-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d733a-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d733a-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d733a-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d733a-239">Search-Flags</span></span>           | <span data-ttu-id="d733a-240">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d733a-240">0x00000001</span></span>                        |
| <span data-ttu-id="d733a-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d733a-241">System-Flags</span></span>           | <span data-ttu-id="d733a-242">0x00000011</span><span class="sxs-lookup"><span data-stu-id="d733a-242">0x00000011</span></span>                        |
| <span data-ttu-id="d733a-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d733a-243">Classes used in</span></span>        | [<span data-ttu-id="d733a-244">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="d733a-244">**User**</span></span>](c-user.md)<br/> |



 

 





