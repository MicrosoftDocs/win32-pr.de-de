---
title: Token-Groups-No-GC-akzeptables-Attribut
description: Dieses Attribut enthält die Liste der SIDs aufgrund eines transitiven Gruppen Mitgliedschafts Erweiterungs Vorgangs für einen bestimmten Benutzer oder Computer. Tokengruppen können nicht abgerufen werden, wenn kein globaler Katalog vorhanden ist, um die transitiven umgekehrten Mitgliedschaften abzurufen.
ms.assetid: 08718c69-6339-40dc-8486-a7cd72028ed1
ms.tgt_platform: multiple
keywords:
- Tokengruppen-No-GC-akzeptables AD-Schema für Attribut
- AD-Schema für das Attribut "tykengroupsnogcacceptable"
topic_type:
- apiref
api_name:
- Token-Groups-No-GC-Acceptable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a87c4b8996586c8c35ed4c815b954dad02b5db03
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859559"
---
# <a name="token-groups-no-gc-acceptable-attribute"></a><span data-ttu-id="5cfd0-106">Token-Groups-No-GC-akzeptables-Attribut</span><span class="sxs-lookup"><span data-stu-id="5cfd0-106">Token-Groups-No-GC-Acceptable attribute</span></span>

<span data-ttu-id="5cfd0-107">Dieses Attribut enthält die Liste der SIDs aufgrund eines transitiven Gruppen Mitgliedschafts Erweiterungs Vorgangs für einen bestimmten Benutzer oder Computer.</span><span class="sxs-lookup"><span data-stu-id="5cfd0-107">This attribute contains the list of SIDs due to a transitive group membership expansion operation on a given user or computer.</span></span> <span data-ttu-id="5cfd0-108">Tokengruppen können nicht abgerufen werden, wenn kein globaler Katalog vorhanden ist, um die transitiven umgekehrten Mitgliedschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5cfd0-108">Token groups cannot be retrieved if a Global Catalog is not present to retrieve the transitive reverse memberships.</span></span>



| <span data-ttu-id="5cfd0-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5cfd0-109">Entry</span></span> | <span data-ttu-id="5cfd0-110">Wert</span><span class="sxs-lookup"><span data-stu-id="5cfd0-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5cfd0-111">CN</span><span class="sxs-lookup"><span data-stu-id="5cfd0-111">CN</span></span>                | <span data-ttu-id="5cfd0-112">Token-Groups-No-GC-akzeptabel</span><span class="sxs-lookup"><span data-stu-id="5cfd0-112">Token-Groups-No-GC-Acceptable</span></span>        |
| <span data-ttu-id="5cfd0-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5cfd0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5cfd0-114">"dekengroupsnogcakzeptabel"</span><span class="sxs-lookup"><span data-stu-id="5cfd0-114">tokenGroupsNoGCAcceptable</span></span>            |
| <span data-ttu-id="5cfd0-115">Size</span><span class="sxs-lookup"><span data-stu-id="5cfd0-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="5cfd0-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5cfd0-116">Update Privilege</span></span>  | <span data-ttu-id="5cfd0-117">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5cfd0-117">The system sets this value.</span></span>          |
| <span data-ttu-id="5cfd0-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="5cfd0-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="5cfd0-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5cfd0-119">Attribute-Id</span></span>      | <span data-ttu-id="5cfd0-120">1.2.840.113556.1.4.1303</span><span class="sxs-lookup"><span data-stu-id="5cfd0-120">1.2.840.113556.1.4.1303</span></span>              |
| <span data-ttu-id="5cfd0-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5cfd0-121">System-Id-Guid</span></span>    | <span data-ttu-id="5cfd0-122">040fc392-33df-11d2-98b2-0000f 87a57d4</span><span class="sxs-lookup"><span data-stu-id="5cfd0-122">040fc392-33df-11d2-98b2-0000f87a57d4</span></span> |
| <span data-ttu-id="5cfd0-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cfd0-123">Syntax</span></span>            | [<span data-ttu-id="5cfd0-124">**Zeichenfolge (SID)**</span><span class="sxs-lookup"><span data-stu-id="5cfd0-124">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="5cfd0-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="5cfd0-125">Implementations</span></span>

-   [<span data-ttu-id="5cfd0-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5cfd0-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5cfd0-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5cfd0-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5cfd0-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5cfd0-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5cfd0-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5cfd0-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5cfd0-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5cfd0-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5cfd0-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5cfd0-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5cfd0-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5cfd0-132">Windows 2000 Server</span></span>



| <span data-ttu-id="5cfd0-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5cfd0-133">Entry</span></span> | <span data-ttu-id="5cfd0-134">Wert</span><span class="sxs-lookup"><span data-stu-id="5cfd0-134">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5cfd0-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5cfd0-135">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5cfd0-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cfd0-136">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5cfd0-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cfd0-137">System-Only</span></span>            | <span data-ttu-id="5cfd0-138">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-138">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5cfd0-139">Is-Single-Valued</span></span>       | <span data-ttu-id="5cfd0-140">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-140">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5cfd0-141">Is Indexed</span></span>             | <span data-ttu-id="5cfd0-142">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-142">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5cfd0-143">In Global Catalog</span></span>      | <span data-ttu-id="5cfd0-144">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-144">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5cfd0-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cfd0-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5cfd0-146">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5cfd0-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cfd0-147">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5cfd0-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cfd0-148">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5cfd0-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cfd0-149">Search-Flags</span></span>           | <span data-ttu-id="5cfd0-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cfd0-150">0x00000000</span></span>                                                   |
| <span data-ttu-id="5cfd0-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cfd0-151">System-Flags</span></span>           | <span data-ttu-id="5cfd0-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5cfd0-152">0x08000014</span></span>                                                   |
| <span data-ttu-id="5cfd0-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5cfd0-153">Classes used in</span></span>        | [<span data-ttu-id="5cfd0-154">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="5cfd0-154">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5cfd0-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5cfd0-155">Windows Server 2003</span></span>



| <span data-ttu-id="5cfd0-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5cfd0-156">Entry</span></span> | <span data-ttu-id="5cfd0-157">Wert</span><span class="sxs-lookup"><span data-stu-id="5cfd0-157">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5cfd0-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5cfd0-158">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5cfd0-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cfd0-159">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5cfd0-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cfd0-160">System-Only</span></span>            | <span data-ttu-id="5cfd0-161">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-161">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5cfd0-162">Is-Single-Valued</span></span>       | <span data-ttu-id="5cfd0-163">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-163">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5cfd0-164">Is Indexed</span></span>             | <span data-ttu-id="5cfd0-165">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-165">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5cfd0-166">In Global Catalog</span></span>      | <span data-ttu-id="5cfd0-167">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-167">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5cfd0-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cfd0-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5cfd0-169">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5cfd0-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cfd0-170">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5cfd0-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cfd0-171">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5cfd0-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cfd0-172">Search-Flags</span></span>           | <span data-ttu-id="5cfd0-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cfd0-173">0x00000000</span></span>                                                   |
| <span data-ttu-id="5cfd0-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cfd0-174">System-Flags</span></span>           | <span data-ttu-id="5cfd0-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5cfd0-175">0x08000014</span></span>                                                   |
| <span data-ttu-id="5cfd0-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5cfd0-176">Classes used in</span></span>        | [<span data-ttu-id="5cfd0-177">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="5cfd0-177">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5cfd0-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5cfd0-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5cfd0-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5cfd0-179">Entry</span></span> | <span data-ttu-id="5cfd0-180">Wert</span><span class="sxs-lookup"><span data-stu-id="5cfd0-180">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5cfd0-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5cfd0-181">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5cfd0-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cfd0-182">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5cfd0-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cfd0-183">System-Only</span></span>            | <span data-ttu-id="5cfd0-184">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-184">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5cfd0-185">Is-Single-Valued</span></span>       | <span data-ttu-id="5cfd0-186">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-186">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5cfd0-187">Is Indexed</span></span>             | <span data-ttu-id="5cfd0-188">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-188">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5cfd0-189">In Global Catalog</span></span>      | <span data-ttu-id="5cfd0-190">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-190">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5cfd0-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cfd0-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5cfd0-192">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5cfd0-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cfd0-193">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5cfd0-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cfd0-194">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5cfd0-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cfd0-195">Search-Flags</span></span>           | <span data-ttu-id="5cfd0-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cfd0-196">0x00000000</span></span>                                                   |
| <span data-ttu-id="5cfd0-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cfd0-197">System-Flags</span></span>           | <span data-ttu-id="5cfd0-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5cfd0-198">0x08000014</span></span>                                                   |
| <span data-ttu-id="5cfd0-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5cfd0-199">Classes used in</span></span>        | [<span data-ttu-id="5cfd0-200">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="5cfd0-200">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5cfd0-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5cfd0-201">Windows Server 2008</span></span>



| <span data-ttu-id="5cfd0-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5cfd0-202">Entry</span></span> | <span data-ttu-id="5cfd0-203">Wert</span><span class="sxs-lookup"><span data-stu-id="5cfd0-203">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5cfd0-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5cfd0-204">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5cfd0-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cfd0-205">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5cfd0-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cfd0-206">System-Only</span></span>            | <span data-ttu-id="5cfd0-207">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-207">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5cfd0-208">Is-Single-Valued</span></span>       | <span data-ttu-id="5cfd0-209">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-209">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5cfd0-210">Is Indexed</span></span>             | <span data-ttu-id="5cfd0-211">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-211">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5cfd0-212">In Global Catalog</span></span>      | <span data-ttu-id="5cfd0-213">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-213">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5cfd0-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cfd0-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5cfd0-215">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5cfd0-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cfd0-216">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5cfd0-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cfd0-217">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5cfd0-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cfd0-218">Search-Flags</span></span>           | <span data-ttu-id="5cfd0-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cfd0-219">0x00000000</span></span>                                                   |
| <span data-ttu-id="5cfd0-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cfd0-220">System-Flags</span></span>           | <span data-ttu-id="5cfd0-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5cfd0-221">0x08000014</span></span>                                                   |
| <span data-ttu-id="5cfd0-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5cfd0-222">Classes used in</span></span>        | [<span data-ttu-id="5cfd0-223">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="5cfd0-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5cfd0-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5cfd0-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5cfd0-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5cfd0-225">Entry</span></span> | <span data-ttu-id="5cfd0-226">Wert</span><span class="sxs-lookup"><span data-stu-id="5cfd0-226">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5cfd0-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5cfd0-227">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5cfd0-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cfd0-228">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5cfd0-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cfd0-229">System-Only</span></span>            | <span data-ttu-id="5cfd0-230">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-230">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5cfd0-231">Is-Single-Valued</span></span>       | <span data-ttu-id="5cfd0-232">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-232">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5cfd0-233">Is Indexed</span></span>             | <span data-ttu-id="5cfd0-234">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-234">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5cfd0-235">In Global Catalog</span></span>      | <span data-ttu-id="5cfd0-236">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-236">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5cfd0-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cfd0-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5cfd0-238">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5cfd0-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cfd0-239">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5cfd0-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cfd0-240">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5cfd0-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cfd0-241">Search-Flags</span></span>           | <span data-ttu-id="5cfd0-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cfd0-242">0x00000000</span></span>                                                   |
| <span data-ttu-id="5cfd0-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cfd0-243">System-Flags</span></span>           | <span data-ttu-id="5cfd0-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5cfd0-244">0x08000014</span></span>                                                   |
| <span data-ttu-id="5cfd0-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5cfd0-245">Classes used in</span></span>        | [<span data-ttu-id="5cfd0-246">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="5cfd0-246">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5cfd0-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5cfd0-247">Windows Server 2012</span></span>



| <span data-ttu-id="5cfd0-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5cfd0-248">Entry</span></span> | <span data-ttu-id="5cfd0-249">Wert</span><span class="sxs-lookup"><span data-stu-id="5cfd0-249">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5cfd0-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5cfd0-250">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5cfd0-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cfd0-251">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5cfd0-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cfd0-252">System-Only</span></span>            | <span data-ttu-id="5cfd0-253">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-253">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5cfd0-254">Is-Single-Valued</span></span>       | <span data-ttu-id="5cfd0-255">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-255">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5cfd0-256">Is Indexed</span></span>             | <span data-ttu-id="5cfd0-257">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-257">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5cfd0-258">In Global Catalog</span></span>      | <span data-ttu-id="5cfd0-259">False</span><span class="sxs-lookup"><span data-stu-id="5cfd0-259">False</span></span>                                                        |
| <span data-ttu-id="5cfd0-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5cfd0-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cfd0-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5cfd0-261">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5cfd0-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cfd0-262">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5cfd0-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cfd0-263">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5cfd0-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cfd0-264">Search-Flags</span></span>           | <span data-ttu-id="5cfd0-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cfd0-265">0x00000000</span></span>                                                   |
| <span data-ttu-id="5cfd0-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cfd0-266">System-Flags</span></span>           | <span data-ttu-id="5cfd0-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5cfd0-267">0x08000014</span></span>                                                   |
| <span data-ttu-id="5cfd0-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5cfd0-268">Classes used in</span></span>        | [<span data-ttu-id="5cfd0-269">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="5cfd0-269">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





