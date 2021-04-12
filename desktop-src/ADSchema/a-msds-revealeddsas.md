---
title: ms-DS-enthüllte-DSAs-Attribut
description: Rückwärts Verknüpfung für ms-DS-offen-Benutzer. Gibt an, welcher RODC den geheimen Benutzer des Benutzers enthält.
ms.assetid: cd84db75-d961-4290-8aa7-2805febbd842
ms.tgt_platform: multiple
keywords:
- das AD-Schema "ms-DS-enthüllte-DSAs-Attribut"
- AD-Schema des msDS-revealeddsas-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Revealed-DSAs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e77dfd69fafffc3286f0ff9419965d7ae9daaa0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480071"
---
# <a name="ms-ds-revealed-dsas-attribute"></a><span data-ttu-id="9a0ae-106">ms-DS-enthüllte-DSAs-Attribut</span><span class="sxs-lookup"><span data-stu-id="9a0ae-106">ms-DS-Revealed-DSAs attribute</span></span>

<span data-ttu-id="9a0ae-107">Rückwärts Verknüpfung für [**ms-DS-offen-Benutzer**](a-msds-revealedusers.md).</span><span class="sxs-lookup"><span data-stu-id="9a0ae-107">Backward link for [**ms-DS-Revealed-Users**](a-msds-revealedusers.md).</span></span> <span data-ttu-id="9a0ae-108">Gibt an, welcher RODC den geheimen Schlüssel dieses Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-108">Identifies which RODC holds that user's secret.</span></span>



| <span data-ttu-id="9a0ae-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a0ae-109">Entry</span></span> | <span data-ttu-id="9a0ae-110">Wert</span><span class="sxs-lookup"><span data-stu-id="9a0ae-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="9a0ae-111">CN</span><span class="sxs-lookup"><span data-stu-id="9a0ae-111">CN</span></span>                | <span data-ttu-id="9a0ae-112">ms-DS-offengelegt-DSAs</span><span class="sxs-lookup"><span data-stu-id="9a0ae-112">ms-DS-Revealed-DSAs</span></span>                     |
| <span data-ttu-id="9a0ae-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9a0ae-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9a0ae-114">MSDS-revealeddsas</span><span class="sxs-lookup"><span data-stu-id="9a0ae-114">msDS-RevealedDSAs</span></span>                       |
| <span data-ttu-id="9a0ae-115">Size</span><span class="sxs-lookup"><span data-stu-id="9a0ae-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="9a0ae-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="9a0ae-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="9a0ae-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="9a0ae-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="9a0ae-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9a0ae-118">Attribute-Id</span></span>      | <span data-ttu-id="9a0ae-119">1.2.840.113556.1.4.1930</span><span class="sxs-lookup"><span data-stu-id="9a0ae-119">1.2.840.113556.1.4.1930</span></span>                 |
| <span data-ttu-id="9a0ae-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9a0ae-120">System-Id-Guid</span></span>    | <span data-ttu-id="9a0ae-121">94f 6f 2AC-c76d-4b5e-b71l-o332c3e93c22</span><span class="sxs-lookup"><span data-stu-id="9a0ae-121">94f6f2ac-c76d-4b5e-b71f-f332c3e93c22</span></span>    |
| <span data-ttu-id="9a0ae-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a0ae-122">Syntax</span></span>            | [<span data-ttu-id="9a0ae-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="9a0ae-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="9a0ae-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="9a0ae-124">Implementations</span></span>

-   [<span data-ttu-id="9a0ae-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9a0ae-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9a0ae-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9a0ae-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9a0ae-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9a0ae-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="9a0ae-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a0ae-128">Windows Server 2008</span></span>



| <span data-ttu-id="9a0ae-129">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a0ae-129">Entry</span></span> | <span data-ttu-id="9a0ae-130">Wert</span><span class="sxs-lookup"><span data-stu-id="9a0ae-130">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9a0ae-131">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a0ae-131">Link-Id</span></span>                | <span data-ttu-id="9a0ae-132">2103</span><span class="sxs-lookup"><span data-stu-id="9a0ae-132">2103</span></span>                            |
| <span data-ttu-id="9a0ae-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a0ae-133">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="9a0ae-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a0ae-134">System-Only</span></span>            | <span data-ttu-id="9a0ae-135">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a0ae-135">True</span></span>                            |
| <span data-ttu-id="9a0ae-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a0ae-136">Is-Single-Valued</span></span>       | <span data-ttu-id="9a0ae-137">False</span><span class="sxs-lookup"><span data-stu-id="9a0ae-137">False</span></span>                           |
| <span data-ttu-id="9a0ae-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a0ae-138">Is Indexed</span></span>             | <span data-ttu-id="9a0ae-139">False</span><span class="sxs-lookup"><span data-stu-id="9a0ae-139">False</span></span>                           |
| <span data-ttu-id="9a0ae-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a0ae-140">In Global Catalog</span></span>      | <span data-ttu-id="9a0ae-141">False</span><span class="sxs-lookup"><span data-stu-id="9a0ae-141">False</span></span>                           |
| <span data-ttu-id="9a0ae-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a0ae-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a0ae-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a0ae-143">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9a0ae-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a0ae-144">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9a0ae-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a0ae-145">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9a0ae-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a0ae-146">Search-Flags</span></span>           | <span data-ttu-id="9a0ae-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a0ae-147">0x00000000</span></span>                      |
| <span data-ttu-id="9a0ae-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a0ae-148">System-Flags</span></span>           | <span data-ttu-id="9a0ae-149">0x00000011</span><span class="sxs-lookup"><span data-stu-id="9a0ae-149">0x00000011</span></span>                      |
| <span data-ttu-id="9a0ae-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a0ae-150">Classes used in</span></span>        | [<span data-ttu-id="9a0ae-151">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="9a0ae-151">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9a0ae-152">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9a0ae-152">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9a0ae-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a0ae-153">Entry</span></span> | <span data-ttu-id="9a0ae-154">Wert</span><span class="sxs-lookup"><span data-stu-id="9a0ae-154">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9a0ae-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a0ae-155">Link-Id</span></span>                | <span data-ttu-id="9a0ae-156">2103</span><span class="sxs-lookup"><span data-stu-id="9a0ae-156">2103</span></span>                            |
| <span data-ttu-id="9a0ae-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a0ae-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="9a0ae-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a0ae-158">System-Only</span></span>            | <span data-ttu-id="9a0ae-159">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a0ae-159">True</span></span>                            |
| <span data-ttu-id="9a0ae-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a0ae-160">Is-Single-Valued</span></span>       | <span data-ttu-id="9a0ae-161">False</span><span class="sxs-lookup"><span data-stu-id="9a0ae-161">False</span></span>                           |
| <span data-ttu-id="9a0ae-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a0ae-162">Is Indexed</span></span>             | <span data-ttu-id="9a0ae-163">False</span><span class="sxs-lookup"><span data-stu-id="9a0ae-163">False</span></span>                           |
| <span data-ttu-id="9a0ae-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a0ae-164">In Global Catalog</span></span>      | <span data-ttu-id="9a0ae-165">False</span><span class="sxs-lookup"><span data-stu-id="9a0ae-165">False</span></span>                           |
| <span data-ttu-id="9a0ae-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a0ae-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a0ae-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a0ae-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9a0ae-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a0ae-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9a0ae-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a0ae-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9a0ae-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a0ae-170">Search-Flags</span></span>           | <span data-ttu-id="9a0ae-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a0ae-171">0x00000000</span></span>                      |
| <span data-ttu-id="9a0ae-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a0ae-172">System-Flags</span></span>           | <span data-ttu-id="9a0ae-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="9a0ae-173">0x00000011</span></span>                      |
| <span data-ttu-id="9a0ae-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a0ae-174">Classes used in</span></span>        | [<span data-ttu-id="9a0ae-175">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="9a0ae-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9a0ae-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9a0ae-176">Windows Server 2012</span></span>



| <span data-ttu-id="9a0ae-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a0ae-177">Entry</span></span> | <span data-ttu-id="9a0ae-178">Wert</span><span class="sxs-lookup"><span data-stu-id="9a0ae-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9a0ae-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a0ae-179">Link-Id</span></span>                | <span data-ttu-id="9a0ae-180">2103</span><span class="sxs-lookup"><span data-stu-id="9a0ae-180">2103</span></span>                            |
| <span data-ttu-id="9a0ae-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a0ae-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="9a0ae-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a0ae-182">System-Only</span></span>            | <span data-ttu-id="9a0ae-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a0ae-183">True</span></span>                            |
| <span data-ttu-id="9a0ae-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a0ae-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9a0ae-185">False</span><span class="sxs-lookup"><span data-stu-id="9a0ae-185">False</span></span>                           |
| <span data-ttu-id="9a0ae-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a0ae-186">Is Indexed</span></span>             | <span data-ttu-id="9a0ae-187">False</span><span class="sxs-lookup"><span data-stu-id="9a0ae-187">False</span></span>                           |
| <span data-ttu-id="9a0ae-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a0ae-188">In Global Catalog</span></span>      | <span data-ttu-id="9a0ae-189">False</span><span class="sxs-lookup"><span data-stu-id="9a0ae-189">False</span></span>                           |
| <span data-ttu-id="9a0ae-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a0ae-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a0ae-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a0ae-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9a0ae-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a0ae-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9a0ae-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a0ae-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9a0ae-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a0ae-194">Search-Flags</span></span>           | <span data-ttu-id="9a0ae-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a0ae-195">0x00000000</span></span>                      |
| <span data-ttu-id="9a0ae-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a0ae-196">System-Flags</span></span>           | <span data-ttu-id="9a0ae-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="9a0ae-197">0x00000011</span></span>                      |
| <span data-ttu-id="9a0ae-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a0ae-198">Classes used in</span></span>        | [<span data-ttu-id="9a0ae-199">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="9a0ae-199">**Top**</span></span>](c-top.md)<br/> |



 

 





