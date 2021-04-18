---
title: ms-DS-Never-Reveal-Group-Attribut
description: Wird mit RODCs verwendet, um zu definieren, welchen Benutzern, Computern und Gruppen die Kenn Wörter auf einem RODC zwischengespeichert werden dürfen.
ms.assetid: 203a660b-503e-4cf1-a796-eac024629b3e
ms.tgt_platform: multiple
keywords:
- AD-Schema für das Attribut "ms-DS-Never-Reveal-Group"
- AD-Schema des msDS-NeverRevealGroup-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Never-Reveal-Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1308fb1bc0818601a037e66b764e607c0a32532
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344748"
---
# <a name="ms-ds-never-reveal-group-attribute"></a><span data-ttu-id="88c3a-105">ms-DS-Never-Reveal-Group-Attribut</span><span class="sxs-lookup"><span data-stu-id="88c3a-105">ms-DS-Never-Reveal-Group attribute</span></span>

<span data-ttu-id="88c3a-106">Wird mit RODCs verwendet, um zu definieren, welchen Benutzern, Computern und Gruppen die Kenn Wörter auf einem RODC zwischengespeichert werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="88c3a-106">Used with RODCs to define which users, computers, and groups are not allowed to have their passwords cached on an RODC.</span></span>



| <span data-ttu-id="88c3a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88c3a-107">Entry</span></span> | <span data-ttu-id="88c3a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="88c3a-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="88c3a-109">CN</span><span class="sxs-lookup"><span data-stu-id="88c3a-109">CN</span></span>                | <span data-ttu-id="88c3a-110">ms-DS-Never-Reveal-Group</span><span class="sxs-lookup"><span data-stu-id="88c3a-110">ms-DS-Never-Reveal-Group</span></span>                |
| <span data-ttu-id="88c3a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="88c3a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="88c3a-112">msDS-NeverRevealGroup</span><span class="sxs-lookup"><span data-stu-id="88c3a-112">msDS-NeverRevealGroup</span></span>                   |
| <span data-ttu-id="88c3a-113">Size</span><span class="sxs-lookup"><span data-stu-id="88c3a-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="88c3a-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="88c3a-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="88c3a-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="88c3a-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="88c3a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="88c3a-116">Attribute-Id</span></span>      | <span data-ttu-id="88c3a-117">1.2.840.113556.1.4.1926</span><span class="sxs-lookup"><span data-stu-id="88c3a-117">1.2.840.113556.1.4.1926</span></span>                 |
| <span data-ttu-id="88c3a-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="88c3a-118">System-Id-Guid</span></span>    | <span data-ttu-id="88c3a-119">15585999-fd49-4d66-b25d-eeb96aba8174</span><span class="sxs-lookup"><span data-stu-id="88c3a-119">15585999-fd49-4d66-b25d-eeb96aba8174</span></span>    |
| <span data-ttu-id="88c3a-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="88c3a-120">Syntax</span></span>            | [<span data-ttu-id="88c3a-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="88c3a-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="88c3a-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="88c3a-122">Implementations</span></span>

-   [<span data-ttu-id="88c3a-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="88c3a-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="88c3a-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="88c3a-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="88c3a-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="88c3a-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="88c3a-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88c3a-126">Windows Server 2008</span></span>



| <span data-ttu-id="88c3a-127">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88c3a-127">Entry</span></span> | <span data-ttu-id="88c3a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="88c3a-128">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="88c3a-129">Link-ID</span><span class="sxs-lookup"><span data-stu-id="88c3a-129">Link-Id</span></span>                | <span data-ttu-id="88c3a-130">2106</span><span class="sxs-lookup"><span data-stu-id="88c3a-130">2106</span></span>                                                                               |
| <span data-ttu-id="88c3a-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c3a-131">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="88c3a-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c3a-132">System-Only</span></span>            | <span data-ttu-id="88c3a-133">False</span><span class="sxs-lookup"><span data-stu-id="88c3a-133">False</span></span>                                                                              |
| <span data-ttu-id="88c3a-134">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="88c3a-134">Is-Single-Valued</span></span>       | <span data-ttu-id="88c3a-135">False</span><span class="sxs-lookup"><span data-stu-id="88c3a-135">False</span></span>                                                                              |
| <span data-ttu-id="88c3a-136">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="88c3a-136">Is Indexed</span></span>             | <span data-ttu-id="88c3a-137">False</span><span class="sxs-lookup"><span data-stu-id="88c3a-137">False</span></span>                                                                              |
| <span data-ttu-id="88c3a-138">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="88c3a-138">In Global Catalog</span></span>      | <span data-ttu-id="88c3a-139">False</span><span class="sxs-lookup"><span data-stu-id="88c3a-139">False</span></span>                                                                              |
| <span data-ttu-id="88c3a-140">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="88c3a-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c3a-141">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="88c3a-141">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="88c3a-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c3a-142">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="88c3a-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c3a-143">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="88c3a-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c3a-144">Search-Flags</span></span>           | <span data-ttu-id="88c3a-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88c3a-145">0x00000000</span></span>                                                                         |
| <span data-ttu-id="88c3a-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c3a-146">System-Flags</span></span>           | <span data-ttu-id="88c3a-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88c3a-147">0x00000010</span></span>                                                                         |
| <span data-ttu-id="88c3a-148">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="88c3a-148">Classes used in</span></span>        | [<span data-ttu-id="88c3a-149">**Computer**</span><span class="sxs-lookup"><span data-stu-id="88c3a-149">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="88c3a-150">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="88c3a-150">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="88c3a-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="88c3a-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="88c3a-152">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88c3a-152">Entry</span></span> | <span data-ttu-id="88c3a-153">Wert</span><span class="sxs-lookup"><span data-stu-id="88c3a-153">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="88c3a-154">Link-ID</span><span class="sxs-lookup"><span data-stu-id="88c3a-154">Link-Id</span></span>                | <span data-ttu-id="88c3a-155">2106</span><span class="sxs-lookup"><span data-stu-id="88c3a-155">2106</span></span>                                                                               |
| <span data-ttu-id="88c3a-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c3a-156">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="88c3a-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c3a-157">System-Only</span></span>            | <span data-ttu-id="88c3a-158">False</span><span class="sxs-lookup"><span data-stu-id="88c3a-158">False</span></span>                                                                              |
| <span data-ttu-id="88c3a-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="88c3a-159">Is-Single-Valued</span></span>       | <span data-ttu-id="88c3a-160">False</span><span class="sxs-lookup"><span data-stu-id="88c3a-160">False</span></span>                                                                              |
| <span data-ttu-id="88c3a-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="88c3a-161">Is Indexed</span></span>             | <span data-ttu-id="88c3a-162">False</span><span class="sxs-lookup"><span data-stu-id="88c3a-162">False</span></span>                                                                              |
| <span data-ttu-id="88c3a-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="88c3a-163">In Global Catalog</span></span>      | <span data-ttu-id="88c3a-164">False</span><span class="sxs-lookup"><span data-stu-id="88c3a-164">False</span></span>                                                                              |
| <span data-ttu-id="88c3a-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="88c3a-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c3a-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="88c3a-166">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="88c3a-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c3a-167">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="88c3a-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c3a-168">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="88c3a-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c3a-169">Search-Flags</span></span>           | <span data-ttu-id="88c3a-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88c3a-170">0x00000000</span></span>                                                                         |
| <span data-ttu-id="88c3a-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c3a-171">System-Flags</span></span>           | <span data-ttu-id="88c3a-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88c3a-172">0x00000010</span></span>                                                                         |
| <span data-ttu-id="88c3a-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="88c3a-173">Classes used in</span></span>        | [<span data-ttu-id="88c3a-174">**Computer**</span><span class="sxs-lookup"><span data-stu-id="88c3a-174">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="88c3a-175">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="88c3a-175">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="88c3a-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88c3a-176">Windows Server 2012</span></span>



| <span data-ttu-id="88c3a-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88c3a-177">Entry</span></span> | <span data-ttu-id="88c3a-178">Wert</span><span class="sxs-lookup"><span data-stu-id="88c3a-178">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="88c3a-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="88c3a-179">Link-Id</span></span>                | <span data-ttu-id="88c3a-180">2106</span><span class="sxs-lookup"><span data-stu-id="88c3a-180">2106</span></span>                                                                               |
| <span data-ttu-id="88c3a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c3a-181">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="88c3a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c3a-182">System-Only</span></span>            | <span data-ttu-id="88c3a-183">False</span><span class="sxs-lookup"><span data-stu-id="88c3a-183">False</span></span>                                                                              |
| <span data-ttu-id="88c3a-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="88c3a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="88c3a-185">False</span><span class="sxs-lookup"><span data-stu-id="88c3a-185">False</span></span>                                                                              |
| <span data-ttu-id="88c3a-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="88c3a-186">Is Indexed</span></span>             | <span data-ttu-id="88c3a-187">False</span><span class="sxs-lookup"><span data-stu-id="88c3a-187">False</span></span>                                                                              |
| <span data-ttu-id="88c3a-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="88c3a-188">In Global Catalog</span></span>      | <span data-ttu-id="88c3a-189">False</span><span class="sxs-lookup"><span data-stu-id="88c3a-189">False</span></span>                                                                              |
| <span data-ttu-id="88c3a-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="88c3a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c3a-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="88c3a-191">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="88c3a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c3a-192">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="88c3a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c3a-193">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="88c3a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c3a-194">Search-Flags</span></span>           | <span data-ttu-id="88c3a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88c3a-195">0x00000000</span></span>                                                                         |
| <span data-ttu-id="88c3a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c3a-196">System-Flags</span></span>           | <span data-ttu-id="88c3a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88c3a-197">0x00000010</span></span>                                                                         |
| <span data-ttu-id="88c3a-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="88c3a-198">Classes used in</span></span>        | [<span data-ttu-id="88c3a-199">**Computer**</span><span class="sxs-lookup"><span data-stu-id="88c3a-199">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="88c3a-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="88c3a-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





