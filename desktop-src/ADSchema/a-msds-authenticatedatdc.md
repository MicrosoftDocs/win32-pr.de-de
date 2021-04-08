---
title: ms-DS-Authenticator-DC-Attribut
description: Forward-Link für ms-DS-authentipeedto-accountlist. Identifiziert den Domänen Controller, bei dem sich ein Benutzer authentifiziert hat.
ms.assetid: 91d6f022-e48b-4e2a-9294-cbac3590760f
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-authenticedat-DC-Attribut
- AD-Schema des msDS-AuthenticatedAtDC-Attributs
topic_type:
- apiref
api_name:
- ms-DS-AuthenticatedAt-DC
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2f41be139f3676beb154a923552b4d794de6d3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957521"
---
# <a name="ms-ds-authenticatedat-dc-attribute"></a><span data-ttu-id="70c93-106">ms-DS-Authenticator-DC-Attribut</span><span class="sxs-lookup"><span data-stu-id="70c93-106">ms-DS-AuthenticatedAt-DC attribute</span></span>

<span data-ttu-id="70c93-107">Forward-Link für [**ms-DS-authentipeedto-accountlist**](a-msds-authenticatedtoaccountlist.md).</span><span class="sxs-lookup"><span data-stu-id="70c93-107">Forward link for [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md).</span></span> <span data-ttu-id="70c93-108">Identifiziert den Domänen Controller, bei dem sich ein Benutzer authentifiziert hat.</span><span class="sxs-lookup"><span data-stu-id="70c93-108">Identifies which DC a user has authenticated to.</span></span>



| <span data-ttu-id="70c93-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="70c93-109">Entry</span></span> | <span data-ttu-id="70c93-110">Wert</span><span class="sxs-lookup"><span data-stu-id="70c93-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="70c93-111">CN</span><span class="sxs-lookup"><span data-stu-id="70c93-111">CN</span></span>                | <span data-ttu-id="70c93-112">ms-DS-Authenticator-DC</span><span class="sxs-lookup"><span data-stu-id="70c93-112">ms-DS-AuthenticatedAt-DC</span></span>                |
| <span data-ttu-id="70c93-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="70c93-113">Ldap-Display-Name</span></span> | <span data-ttu-id="70c93-114">MSDS-AuthenticatedAtDC</span><span class="sxs-lookup"><span data-stu-id="70c93-114">msDS-AuthenticatedAtDC</span></span>                  |
| <span data-ttu-id="70c93-115">Size</span><span class="sxs-lookup"><span data-stu-id="70c93-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="70c93-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="70c93-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="70c93-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="70c93-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="70c93-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="70c93-118">Attribute-Id</span></span>      | <span data-ttu-id="70c93-119">1.2.840.113556.1.4.1958</span><span class="sxs-lookup"><span data-stu-id="70c93-119">1.2.840.113556.1.4.1958</span></span>                 |
| <span data-ttu-id="70c93-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="70c93-120">System-Id-Guid</span></span>    | <span data-ttu-id="70c93-121">3e1ee99c-6604-4489-89d9-84798a89515a</span><span class="sxs-lookup"><span data-stu-id="70c93-121">3e1ee99c-6604-4489-89d9-84798a89515a</span></span>    |
| <span data-ttu-id="70c93-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="70c93-122">Syntax</span></span>            | [<span data-ttu-id="70c93-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="70c93-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="70c93-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="70c93-124">Implementations</span></span>

-   [<span data-ttu-id="70c93-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="70c93-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="70c93-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="70c93-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="70c93-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="70c93-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="70c93-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70c93-128">Windows Server 2008</span></span>



| <span data-ttu-id="70c93-129">Eingabe</span><span class="sxs-lookup"><span data-stu-id="70c93-129">Entry</span></span> | <span data-ttu-id="70c93-130">Wert</span><span class="sxs-lookup"><span data-stu-id="70c93-130">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="70c93-131">Link-ID</span><span class="sxs-lookup"><span data-stu-id="70c93-131">Link-Id</span></span>                | <span data-ttu-id="70c93-132">2112</span><span class="sxs-lookup"><span data-stu-id="70c93-132">2112</span></span>                                                                        |
| <span data-ttu-id="70c93-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70c93-133">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="70c93-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="70c93-134">System-Only</span></span>            | <span data-ttu-id="70c93-135">False</span><span class="sxs-lookup"><span data-stu-id="70c93-135">False</span></span>                                                                       |
| <span data-ttu-id="70c93-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="70c93-136">Is-Single-Valued</span></span>       | <span data-ttu-id="70c93-137">False</span><span class="sxs-lookup"><span data-stu-id="70c93-137">False</span></span>                                                                       |
| <span data-ttu-id="70c93-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="70c93-138">Is Indexed</span></span>             | <span data-ttu-id="70c93-139">False</span><span class="sxs-lookup"><span data-stu-id="70c93-139">False</span></span>                                                                       |
| <span data-ttu-id="70c93-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="70c93-140">In Global Catalog</span></span>      | <span data-ttu-id="70c93-141">False</span><span class="sxs-lookup"><span data-stu-id="70c93-141">False</span></span>                                                                       |
| <span data-ttu-id="70c93-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="70c93-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="70c93-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="70c93-143">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="70c93-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70c93-144">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="70c93-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70c93-145">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="70c93-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70c93-146">Search-Flags</span></span>           | <span data-ttu-id="70c93-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70c93-147">0x00000000</span></span>                                                                  |
| <span data-ttu-id="70c93-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70c93-148">System-Flags</span></span>           | <span data-ttu-id="70c93-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="70c93-149">0x00000010</span></span>                                                                  |
| <span data-ttu-id="70c93-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="70c93-150">Classes used in</span></span>        | [<span data-ttu-id="70c93-151">**Computer**</span><span class="sxs-lookup"><span data-stu-id="70c93-151">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="70c93-152">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="70c93-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="70c93-153">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="70c93-153">Windows Server 2008 R2</span></span>



| <span data-ttu-id="70c93-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="70c93-154">Entry</span></span> | <span data-ttu-id="70c93-155">Wert</span><span class="sxs-lookup"><span data-stu-id="70c93-155">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="70c93-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="70c93-156">Link-Id</span></span>                | <span data-ttu-id="70c93-157">2112</span><span class="sxs-lookup"><span data-stu-id="70c93-157">2112</span></span>                                                                        |
| <span data-ttu-id="70c93-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70c93-158">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="70c93-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="70c93-159">System-Only</span></span>            | <span data-ttu-id="70c93-160">False</span><span class="sxs-lookup"><span data-stu-id="70c93-160">False</span></span>                                                                       |
| <span data-ttu-id="70c93-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="70c93-161">Is-Single-Valued</span></span>       | <span data-ttu-id="70c93-162">False</span><span class="sxs-lookup"><span data-stu-id="70c93-162">False</span></span>                                                                       |
| <span data-ttu-id="70c93-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="70c93-163">Is Indexed</span></span>             | <span data-ttu-id="70c93-164">False</span><span class="sxs-lookup"><span data-stu-id="70c93-164">False</span></span>                                                                       |
| <span data-ttu-id="70c93-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="70c93-165">In Global Catalog</span></span>      | <span data-ttu-id="70c93-166">False</span><span class="sxs-lookup"><span data-stu-id="70c93-166">False</span></span>                                                                       |
| <span data-ttu-id="70c93-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="70c93-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="70c93-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="70c93-168">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="70c93-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70c93-169">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="70c93-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70c93-170">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="70c93-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70c93-171">Search-Flags</span></span>           | <span data-ttu-id="70c93-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70c93-172">0x00000000</span></span>                                                                  |
| <span data-ttu-id="70c93-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70c93-173">System-Flags</span></span>           | <span data-ttu-id="70c93-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="70c93-174">0x00000010</span></span>                                                                  |
| <span data-ttu-id="70c93-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="70c93-175">Classes used in</span></span>        | [<span data-ttu-id="70c93-176">**Computer**</span><span class="sxs-lookup"><span data-stu-id="70c93-176">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="70c93-177">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="70c93-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="70c93-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="70c93-178">Windows Server 2012</span></span>



| <span data-ttu-id="70c93-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="70c93-179">Entry</span></span> | <span data-ttu-id="70c93-180">Wert</span><span class="sxs-lookup"><span data-stu-id="70c93-180">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="70c93-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="70c93-181">Link-Id</span></span>                | <span data-ttu-id="70c93-182">2112</span><span class="sxs-lookup"><span data-stu-id="70c93-182">2112</span></span>                                                                        |
| <span data-ttu-id="70c93-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70c93-183">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="70c93-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="70c93-184">System-Only</span></span>            | <span data-ttu-id="70c93-185">False</span><span class="sxs-lookup"><span data-stu-id="70c93-185">False</span></span>                                                                       |
| <span data-ttu-id="70c93-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="70c93-186">Is-Single-Valued</span></span>       | <span data-ttu-id="70c93-187">False</span><span class="sxs-lookup"><span data-stu-id="70c93-187">False</span></span>                                                                       |
| <span data-ttu-id="70c93-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="70c93-188">Is Indexed</span></span>             | <span data-ttu-id="70c93-189">False</span><span class="sxs-lookup"><span data-stu-id="70c93-189">False</span></span>                                                                       |
| <span data-ttu-id="70c93-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="70c93-190">In Global Catalog</span></span>      | <span data-ttu-id="70c93-191">False</span><span class="sxs-lookup"><span data-stu-id="70c93-191">False</span></span>                                                                       |
| <span data-ttu-id="70c93-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="70c93-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="70c93-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="70c93-193">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="70c93-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70c93-194">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="70c93-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70c93-195">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="70c93-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70c93-196">Search-Flags</span></span>           | <span data-ttu-id="70c93-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70c93-197">0x00000000</span></span>                                                                  |
| <span data-ttu-id="70c93-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70c93-198">System-Flags</span></span>           | <span data-ttu-id="70c93-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="70c93-199">0x00000010</span></span>                                                                  |
| <span data-ttu-id="70c93-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="70c93-200">Classes used in</span></span>        | [<span data-ttu-id="70c93-201">**Computer**</span><span class="sxs-lookup"><span data-stu-id="70c93-201">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="70c93-202">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="70c93-202">**User**</span></span>](c-user.md)<br/> |



 

 





