---
title: Token-Groups-Attribut
description: Ein berechnetes Attribut, das die Liste der SIDs aufgrund eines transitiven Gruppen Mitgliedschafts Erweiterungs Vorgangs für einen bestimmten Benutzer oder Computer enthält. Tokengruppen können nicht abgerufen werden, wenn kein globaler Katalog vorhanden ist, um die transitiven umgekehrten Mitgliedschaften abzurufen.
ms.assetid: bb430c9f-20b7-4f21-804d-fbd4864b6505
ms.tgt_platform: multiple
keywords:
- AD-Schema für Token-Groups-Attribut
- Schema Gruppen-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Token-Groups
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5342d1ff2bf549796340532b0514d5c5b060c2c1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344287"
---
# <a name="token-groups-attribute"></a><span data-ttu-id="6c4c2-106">Token-Groups-Attribut</span><span class="sxs-lookup"><span data-stu-id="6c4c2-106">Token-Groups attribute</span></span>

<span data-ttu-id="6c4c2-107">Ein berechnetes Attribut, das die Liste der SIDs aufgrund eines transitiven Gruppen Mitgliedschafts Erweiterungs Vorgangs für einen bestimmten Benutzer oder Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="6c4c2-107">A computed attribute that contains the list of SIDs due to a transitive group membership expansion operation on a given user or computer.</span></span> <span data-ttu-id="6c4c2-108">Tokengruppen können nicht abgerufen werden, wenn kein globaler Katalog vorhanden ist, um die transitiven umgekehrten Mitgliedschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6c4c2-108">Token Groups cannot be retrieved if no Global Catalog is present to retrieve the transitive reverse memberships.</span></span>



| <span data-ttu-id="6c4c2-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c4c2-109">Entry</span></span> | <span data-ttu-id="6c4c2-110">Wert</span><span class="sxs-lookup"><span data-stu-id="6c4c2-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6c4c2-111">CN</span><span class="sxs-lookup"><span data-stu-id="6c4c2-111">CN</span></span>                | <span data-ttu-id="6c4c2-112">Token-Groups</span><span class="sxs-lookup"><span data-stu-id="6c4c2-112">Token-Groups</span></span>                         |
| <span data-ttu-id="6c4c2-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6c4c2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6c4c2-114">tokenGroups</span><span class="sxs-lookup"><span data-stu-id="6c4c2-114">tokenGroups</span></span>                          |
| <span data-ttu-id="6c4c2-115">Size</span><span class="sxs-lookup"><span data-stu-id="6c4c2-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="6c4c2-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="6c4c2-116">Update Privilege</span></span>  | <span data-ttu-id="6c4c2-117">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6c4c2-117">This value is set by the system.</span></span>     |
| <span data-ttu-id="6c4c2-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="6c4c2-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="6c4c2-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6c4c2-119">Attribute-Id</span></span>      | <span data-ttu-id="6c4c2-120">1.2.840.113556.1.4.1301</span><span class="sxs-lookup"><span data-stu-id="6c4c2-120">1.2.840.113556.1.4.1301</span></span>              |
| <span data-ttu-id="6c4c2-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6c4c2-121">System-Id-Guid</span></span>    | <span data-ttu-id="6c4c2-122">b7c69e6d-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="6c4c2-122">b7c69e6d-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="6c4c2-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c4c2-123">Syntax</span></span>            | [<span data-ttu-id="6c4c2-124">**Zeichenfolge (SID)**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-124">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="6c4c2-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="6c4c2-125">Implementations</span></span>

-   [<span data-ttu-id="6c4c2-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6c4c2-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6c4c2-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6c4c2-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6c4c2-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6c4c2-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6c4c2-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6c4c2-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c4c2-133">Windows 2000 Server</span></span>



| <span data-ttu-id="6c4c2-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c4c2-134">Entry</span></span> | <span data-ttu-id="6c4c2-135">Wert</span><span class="sxs-lookup"><span data-stu-id="6c4c2-135">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6c4c2-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c4c2-136">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6c4c2-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c4c2-137">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6c4c2-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c4c2-138">System-Only</span></span>            | <span data-ttu-id="6c4c2-139">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-139">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c4c2-140">Is-Single-Valued</span></span>       | <span data-ttu-id="6c4c2-141">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-141">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c4c2-142">Is Indexed</span></span>             | <span data-ttu-id="6c4c2-143">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-143">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c4c2-144">In Global Catalog</span></span>      | <span data-ttu-id="6c4c2-145">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-145">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c4c2-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c4c2-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c4c2-147">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6c4c2-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c4c2-148">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6c4c2-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c4c2-149">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6c4c2-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c4c2-150">Search-Flags</span></span>           | <span data-ttu-id="6c4c2-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c4c2-151">0x00000000</span></span>                                                   |
| <span data-ttu-id="6c4c2-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c4c2-152">System-Flags</span></span>           | <span data-ttu-id="6c4c2-153">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6c4c2-153">0x08000014</span></span>                                                   |
| <span data-ttu-id="6c4c2-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c4c2-154">Classes used in</span></span>        | [<span data-ttu-id="6c4c2-155">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-155">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6c4c2-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c4c2-156">Windows Server 2003</span></span>



| <span data-ttu-id="6c4c2-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c4c2-157">Entry</span></span> | <span data-ttu-id="6c4c2-158">Wert</span><span class="sxs-lookup"><span data-stu-id="6c4c2-158">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6c4c2-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c4c2-159">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6c4c2-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c4c2-160">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6c4c2-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c4c2-161">System-Only</span></span>            | <span data-ttu-id="6c4c2-162">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-162">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c4c2-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6c4c2-164">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-164">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c4c2-165">Is Indexed</span></span>             | <span data-ttu-id="6c4c2-166">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-166">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c4c2-167">In Global Catalog</span></span>      | <span data-ttu-id="6c4c2-168">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-168">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c4c2-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c4c2-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c4c2-170">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6c4c2-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c4c2-171">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6c4c2-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c4c2-172">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6c4c2-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c4c2-173">Search-Flags</span></span>           | <span data-ttu-id="6c4c2-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c4c2-174">0x00000000</span></span>                                                   |
| <span data-ttu-id="6c4c2-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c4c2-175">System-Flags</span></span>           | <span data-ttu-id="6c4c2-176">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6c4c2-176">0x08000014</span></span>                                                   |
| <span data-ttu-id="6c4c2-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c4c2-177">Classes used in</span></span>        | [<span data-ttu-id="6c4c2-178">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-178">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6c4c2-179">Adam</span><span class="sxs-lookup"><span data-stu-id="6c4c2-179">ADAM</span></span>



| <span data-ttu-id="6c4c2-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c4c2-180">Entry</span></span> | <span data-ttu-id="6c4c2-181">Wert</span><span class="sxs-lookup"><span data-stu-id="6c4c2-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6c4c2-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c4c2-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6c4c2-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c4c2-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6c4c2-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c4c2-184">System-Only</span></span>            | <span data-ttu-id="6c4c2-185">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-185">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c4c2-186">Is-Single-Valued</span></span>       | <span data-ttu-id="6c4c2-187">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-187">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c4c2-188">Is Indexed</span></span>             | <span data-ttu-id="6c4c2-189">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-189">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c4c2-190">In Global Catalog</span></span>      | <span data-ttu-id="6c4c2-191">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-191">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c4c2-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c4c2-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c4c2-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6c4c2-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c4c2-194">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6c4c2-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c4c2-195">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6c4c2-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c4c2-196">Search-Flags</span></span>           | <span data-ttu-id="6c4c2-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c4c2-197">0x00000000</span></span>                                                   |
| <span data-ttu-id="6c4c2-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c4c2-198">System-Flags</span></span>           | <span data-ttu-id="6c4c2-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6c4c2-199">0x08000014</span></span>                                                   |
| <span data-ttu-id="6c4c2-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c4c2-200">Classes used in</span></span>        | [<span data-ttu-id="6c4c2-201">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-201">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6c4c2-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6c4c2-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6c4c2-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c4c2-203">Entry</span></span> | <span data-ttu-id="6c4c2-204">Wert</span><span class="sxs-lookup"><span data-stu-id="6c4c2-204">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6c4c2-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c4c2-205">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6c4c2-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c4c2-206">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6c4c2-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c4c2-207">System-Only</span></span>            | <span data-ttu-id="6c4c2-208">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-208">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c4c2-209">Is-Single-Valued</span></span>       | <span data-ttu-id="6c4c2-210">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-210">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c4c2-211">Is Indexed</span></span>             | <span data-ttu-id="6c4c2-212">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-212">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c4c2-213">In Global Catalog</span></span>      | <span data-ttu-id="6c4c2-214">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-214">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c4c2-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c4c2-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c4c2-216">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6c4c2-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c4c2-217">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6c4c2-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c4c2-218">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6c4c2-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c4c2-219">Search-Flags</span></span>           | <span data-ttu-id="6c4c2-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c4c2-220">0x00000000</span></span>                                                   |
| <span data-ttu-id="6c4c2-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c4c2-221">System-Flags</span></span>           | <span data-ttu-id="6c4c2-222">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6c4c2-222">0x08000014</span></span>                                                   |
| <span data-ttu-id="6c4c2-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c4c2-223">Classes used in</span></span>        | [<span data-ttu-id="6c4c2-224">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-224">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6c4c2-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c4c2-225">Windows Server 2008</span></span>



| <span data-ttu-id="6c4c2-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c4c2-226">Entry</span></span> | <span data-ttu-id="6c4c2-227">Wert</span><span class="sxs-lookup"><span data-stu-id="6c4c2-227">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6c4c2-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c4c2-228">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6c4c2-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c4c2-229">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6c4c2-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c4c2-230">System-Only</span></span>            | <span data-ttu-id="6c4c2-231">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-231">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c4c2-232">Is-Single-Valued</span></span>       | <span data-ttu-id="6c4c2-233">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-233">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c4c2-234">Is Indexed</span></span>             | <span data-ttu-id="6c4c2-235">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-235">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c4c2-236">In Global Catalog</span></span>      | <span data-ttu-id="6c4c2-237">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-237">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c4c2-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c4c2-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c4c2-239">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6c4c2-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c4c2-240">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6c4c2-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c4c2-241">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6c4c2-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c4c2-242">Search-Flags</span></span>           | <span data-ttu-id="6c4c2-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c4c2-243">0x00000000</span></span>                                                   |
| <span data-ttu-id="6c4c2-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c4c2-244">System-Flags</span></span>           | <span data-ttu-id="6c4c2-245">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6c4c2-245">0x08000014</span></span>                                                   |
| <span data-ttu-id="6c4c2-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c4c2-246">Classes used in</span></span>        | [<span data-ttu-id="6c4c2-247">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6c4c2-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6c4c2-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6c4c2-249">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c4c2-249">Entry</span></span> | <span data-ttu-id="6c4c2-250">Wert</span><span class="sxs-lookup"><span data-stu-id="6c4c2-250">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6c4c2-251">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c4c2-251">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6c4c2-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c4c2-252">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6c4c2-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c4c2-253">System-Only</span></span>            | <span data-ttu-id="6c4c2-254">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-254">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-255">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c4c2-255">Is-Single-Valued</span></span>       | <span data-ttu-id="6c4c2-256">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-256">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-257">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c4c2-257">Is Indexed</span></span>             | <span data-ttu-id="6c4c2-258">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-258">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-259">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c4c2-259">In Global Catalog</span></span>      | <span data-ttu-id="6c4c2-260">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-260">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c4c2-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c4c2-262">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c4c2-262">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6c4c2-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c4c2-263">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6c4c2-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c4c2-264">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6c4c2-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c4c2-265">Search-Flags</span></span>           | <span data-ttu-id="6c4c2-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c4c2-266">0x00000000</span></span>                                                   |
| <span data-ttu-id="6c4c2-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c4c2-267">System-Flags</span></span>           | <span data-ttu-id="6c4c2-268">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6c4c2-268">0x08000014</span></span>                                                   |
| <span data-ttu-id="6c4c2-269">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c4c2-269">Classes used in</span></span>        | [<span data-ttu-id="6c4c2-270">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-270">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6c4c2-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6c4c2-271">Windows Server 2012</span></span>



| <span data-ttu-id="6c4c2-272">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6c4c2-272">Entry</span></span> | <span data-ttu-id="6c4c2-273">Wert</span><span class="sxs-lookup"><span data-stu-id="6c4c2-273">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6c4c2-274">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6c4c2-274">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6c4c2-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c4c2-275">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6c4c2-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c4c2-276">System-Only</span></span>            | <span data-ttu-id="6c4c2-277">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-277">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-278">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6c4c2-278">Is-Single-Valued</span></span>       | <span data-ttu-id="6c4c2-279">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-279">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-280">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6c4c2-280">Is Indexed</span></span>             | <span data-ttu-id="6c4c2-281">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-281">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-282">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6c4c2-282">In Global Catalog</span></span>      | <span data-ttu-id="6c4c2-283">False</span><span class="sxs-lookup"><span data-stu-id="6c4c2-283">False</span></span>                                                        |
| <span data-ttu-id="6c4c2-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c4c2-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c4c2-285">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6c4c2-285">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6c4c2-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c4c2-286">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6c4c2-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c4c2-287">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6c4c2-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c4c2-288">Search-Flags</span></span>           | <span data-ttu-id="6c4c2-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c4c2-289">0x00000000</span></span>                                                   |
| <span data-ttu-id="6c4c2-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c4c2-290">System-Flags</span></span>           | <span data-ttu-id="6c4c2-291">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6c4c2-291">0x08000014</span></span>                                                   |
| <span data-ttu-id="6c4c2-292">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6c4c2-292">Classes used in</span></span>        | [<span data-ttu-id="6c4c2-293">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-293">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





