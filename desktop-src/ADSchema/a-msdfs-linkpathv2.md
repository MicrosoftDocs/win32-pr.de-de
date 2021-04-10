---
title: MS-DFS-Link-Path-v2-Attribut
description: Der DFS-Linkpfad relativ zur DFS-Stamm Ziel Freigabe (also ohne die Komponenten Server/Domäne und DFS-Namespace Name). Verwenden Sie Schrägstriche (/) anstelle von umgekehrten Schrägstrichen ( \) , damit LDAP-Suchvorgänge ausgeführt werden können, ohne dass Escapezeichen verwendet werden müssen.
ms.assetid: 98fd6e99-0d7e-4ffa-b8ec-d26ca03ffead
ms.tgt_platform: multiple
keywords:
- MS-DFS-Link-Path-v2-Attribut AD-Schema
- Schema für msdfs-LinkPathv2-Attribut
topic_type:
- apiref
api_name:
- ms-DFS-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 892cee6a5e6f423a0ed750858e19e1accccbe45f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123019"
---
# <a name="ms-dfs-link-path-v2-attribute"></a><span data-ttu-id="5ab26-106">MS-DFS-Link-Path-v2-Attribut</span><span class="sxs-lookup"><span data-stu-id="5ab26-106">ms-DFS-Link-Path-v2 attribute</span></span>

<span data-ttu-id="5ab26-107">Der DFS-Linkpfad relativ zur DFS-Stamm Ziel Freigabe (also ohne die Komponenten Server/Domäne und DFS-Namespace Name).</span><span class="sxs-lookup"><span data-stu-id="5ab26-107">DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="5ab26-108">Verwenden Sie Schrägstriche (/) anstelle von umgekehrten Schrägstrichen ( \) , damit LDAP-Suchvorgänge ausgeführt werden können, ohne dass Escapezeichen verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5ab26-108">Use forward slashes (/) instead of backslashes (\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="5ab26-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ab26-109">Entry</span></span> | <span data-ttu-id="5ab26-110">Wert</span><span class="sxs-lookup"><span data-stu-id="5ab26-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5ab26-111">CN</span><span class="sxs-lookup"><span data-stu-id="5ab26-111">CN</span></span>                | <span data-ttu-id="5ab26-112">MS-DFS-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="5ab26-112">ms-DFS-Link-Path-v2</span></span>                         |
| <span data-ttu-id="5ab26-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5ab26-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5ab26-114">msdfs-LinkPathv2</span><span class="sxs-lookup"><span data-stu-id="5ab26-114">msDFS-LinkPathv2</span></span>                            |
| <span data-ttu-id="5ab26-115">Size</span><span class="sxs-lookup"><span data-stu-id="5ab26-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="5ab26-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5ab26-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="5ab26-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="5ab26-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="5ab26-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5ab26-118">Attribute-Id</span></span>      | <span data-ttu-id="5ab26-119">1.2.840.113556.1.4.2039</span><span class="sxs-lookup"><span data-stu-id="5ab26-119">1.2.840.113556.1.4.2039</span></span>                     |
| <span data-ttu-id="5ab26-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5ab26-120">System-Id-Guid</span></span>    | <span data-ttu-id="5ab26-121">86b021f 6-10ab-40A2-A252-1dc0cc3be6a9</span><span class="sxs-lookup"><span data-stu-id="5ab26-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span></span>        |
| <span data-ttu-id="5ab26-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ab26-122">Syntax</span></span>            | [<span data-ttu-id="5ab26-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5ab26-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5ab26-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="5ab26-124">Implementations</span></span>

-   [<span data-ttu-id="5ab26-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5ab26-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5ab26-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5ab26-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5ab26-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5ab26-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="5ab26-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ab26-128">Windows Server 2008</span></span>



| <span data-ttu-id="5ab26-129">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ab26-129">Entry</span></span> | <span data-ttu-id="5ab26-130">Wert</span><span class="sxs-lookup"><span data-stu-id="5ab26-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab26-131">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5ab26-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5ab26-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ab26-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5ab26-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ab26-133">System-Only</span></span>            | <span data-ttu-id="5ab26-134">False</span><span class="sxs-lookup"><span data-stu-id="5ab26-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="5ab26-135">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5ab26-135">Is-Single-Valued</span></span>       | <span data-ttu-id="5ab26-136">Richtig</span><span class="sxs-lookup"><span data-stu-id="5ab26-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="5ab26-137">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5ab26-137">Is Indexed</span></span>             | <span data-ttu-id="5ab26-138">False</span><span class="sxs-lookup"><span data-stu-id="5ab26-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="5ab26-139">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5ab26-139">In Global Catalog</span></span>      | <span data-ttu-id="5ab26-140">False</span><span class="sxs-lookup"><span data-stu-id="5ab26-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="5ab26-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5ab26-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ab26-142">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5ab26-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="5ab26-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ab26-143">Range-Lower</span></span>            | <span data-ttu-id="5ab26-144">0</span><span class="sxs-lookup"><span data-stu-id="5ab26-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="5ab26-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ab26-145">Range-Upper</span></span>            | <span data-ttu-id="5ab26-146">32766</span><span class="sxs-lookup"><span data-stu-id="5ab26-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="5ab26-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ab26-147">Search-Flags</span></span>           | <span data-ttu-id="5ab26-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ab26-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="5ab26-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ab26-149">System-Flags</span></span>           | <span data-ttu-id="5ab26-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5ab26-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="5ab26-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5ab26-151">Classes used in</span></span>        | [<span data-ttu-id="5ab26-152">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5ab26-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="5ab26-153">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5ab26-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5ab26-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5ab26-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5ab26-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ab26-155">Entry</span></span> | <span data-ttu-id="5ab26-156">Wert</span><span class="sxs-lookup"><span data-stu-id="5ab26-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab26-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5ab26-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5ab26-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ab26-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5ab26-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ab26-159">System-Only</span></span>            | <span data-ttu-id="5ab26-160">False</span><span class="sxs-lookup"><span data-stu-id="5ab26-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="5ab26-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5ab26-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5ab26-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="5ab26-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="5ab26-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5ab26-163">Is Indexed</span></span>             | <span data-ttu-id="5ab26-164">False</span><span class="sxs-lookup"><span data-stu-id="5ab26-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="5ab26-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5ab26-165">In Global Catalog</span></span>      | <span data-ttu-id="5ab26-166">False</span><span class="sxs-lookup"><span data-stu-id="5ab26-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="5ab26-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5ab26-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ab26-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5ab26-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="5ab26-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ab26-169">Range-Lower</span></span>            | <span data-ttu-id="5ab26-170">0</span><span class="sxs-lookup"><span data-stu-id="5ab26-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="5ab26-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ab26-171">Range-Upper</span></span>            | <span data-ttu-id="5ab26-172">32766</span><span class="sxs-lookup"><span data-stu-id="5ab26-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="5ab26-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ab26-173">Search-Flags</span></span>           | <span data-ttu-id="5ab26-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ab26-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="5ab26-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ab26-175">System-Flags</span></span>           | <span data-ttu-id="5ab26-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5ab26-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="5ab26-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5ab26-177">Classes used in</span></span>        | [<span data-ttu-id="5ab26-178">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5ab26-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="5ab26-179">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5ab26-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5ab26-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ab26-180">Windows Server 2012</span></span>



| <span data-ttu-id="5ab26-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ab26-181">Entry</span></span> | <span data-ttu-id="5ab26-182">Wert</span><span class="sxs-lookup"><span data-stu-id="5ab26-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab26-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5ab26-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5ab26-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ab26-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5ab26-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ab26-185">System-Only</span></span>            | <span data-ttu-id="5ab26-186">False</span><span class="sxs-lookup"><span data-stu-id="5ab26-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="5ab26-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5ab26-187">Is-Single-Valued</span></span>       | <span data-ttu-id="5ab26-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="5ab26-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="5ab26-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5ab26-189">Is Indexed</span></span>             | <span data-ttu-id="5ab26-190">False</span><span class="sxs-lookup"><span data-stu-id="5ab26-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="5ab26-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5ab26-191">In Global Catalog</span></span>      | <span data-ttu-id="5ab26-192">False</span><span class="sxs-lookup"><span data-stu-id="5ab26-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="5ab26-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5ab26-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ab26-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5ab26-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="5ab26-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ab26-195">Range-Lower</span></span>            | <span data-ttu-id="5ab26-196">0</span><span class="sxs-lookup"><span data-stu-id="5ab26-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="5ab26-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ab26-197">Range-Upper</span></span>            | <span data-ttu-id="5ab26-198">32766</span><span class="sxs-lookup"><span data-stu-id="5ab26-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="5ab26-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ab26-199">Search-Flags</span></span>           | <span data-ttu-id="5ab26-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ab26-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="5ab26-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ab26-201">System-Flags</span></span>           | <span data-ttu-id="5ab26-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5ab26-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="5ab26-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5ab26-203">Classes used in</span></span>        | [<span data-ttu-id="5ab26-204">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5ab26-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="5ab26-205">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5ab26-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





