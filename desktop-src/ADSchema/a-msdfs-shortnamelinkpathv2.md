---
title: MS-DFS-Short-Name-Link-Path-v2-Attribut
description: Der DFS-Linkpfad des Kurznamens relativ zur DFS-Stamm Ziel Freigabe (d. h. ohne die Komponenten Server/Domäne und DFS-Namespace Name). Verwenden Sie Schrägstriche (/) anstelle von umgekehrten Schrägstrichen ( \) , damit LDAP-Suchvorgänge ausgeführt werden können, ohne dass Escapezeichen verwendet werden müssen.
ms.assetid: 0589d3f5-9734-4f95-bba9-22f13bb1c9f1
ms.tgt_platform: multiple
keywords:
- "\"MS-DFS-Short-Name-Link-Path-V2\"-Attribut AD-Schema"
- Schema für msdfs-ShortNameLinkPathv2-Attribut
topic_type:
- apiref
api_name:
- ms-DFS-Short-Name-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a536abdf13bed7acc99c1036d3c259493994b28
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344554"
---
# <a name="ms-dfs-short-name-link-path-v2-attribute"></a><span data-ttu-id="0bb12-106">MS-DFS-Short-Name-Link-Path-v2-Attribut</span><span class="sxs-lookup"><span data-stu-id="0bb12-106">ms-DFS-Short-Name-Link-Path-v2 attribute</span></span>

<span data-ttu-id="0bb12-107">Der DFS-Linkpfad des Kurznamens relativ zur DFS-Stamm Ziel Freigabe (d. h. ohne die Komponenten Server/Domäne und DFS-Namespace Name).</span><span class="sxs-lookup"><span data-stu-id="0bb12-107">Short Name DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="0bb12-108">Verwenden Sie Schrägstriche (/) anstelle von umgekehrten Schrägstrichen ( \) , damit LDAP-Suchvorgänge ausgeführt werden können, ohne dass Escapezeichen verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0bb12-108">Use forward slashes (/) instead of backslashes (\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="0bb12-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0bb12-109">Entry</span></span> | <span data-ttu-id="0bb12-110">Wert</span><span class="sxs-lookup"><span data-stu-id="0bb12-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="0bb12-111">CN</span><span class="sxs-lookup"><span data-stu-id="0bb12-111">CN</span></span>                | <span data-ttu-id="0bb12-112">MS-DFS-Short-Name-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="0bb12-112">ms-DFS-Short-Name-Link-Path-v2</span></span>              |
| <span data-ttu-id="0bb12-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0bb12-113">Ldap-Display-Name</span></span> | <span data-ttu-id="0bb12-114">msdfs-ShortNameLinkPathv2</span><span class="sxs-lookup"><span data-stu-id="0bb12-114">msDFS-ShortNameLinkPathv2</span></span>                   |
| <span data-ttu-id="0bb12-115">Size</span><span class="sxs-lookup"><span data-stu-id="0bb12-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="0bb12-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0bb12-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="0bb12-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="0bb12-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="0bb12-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0bb12-118">Attribute-Id</span></span>      | <span data-ttu-id="0bb12-119">1.2.840.113556.1.4.2042</span><span class="sxs-lookup"><span data-stu-id="0bb12-119">1.2.840.113556.1.4.2042</span></span>                     |
| <span data-ttu-id="0bb12-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0bb12-120">System-Id-Guid</span></span>    | <span data-ttu-id="0bb12-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span><span class="sxs-lookup"><span data-stu-id="0bb12-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span></span>        |
| <span data-ttu-id="0bb12-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bb12-122">Syntax</span></span>            | [<span data-ttu-id="0bb12-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="0bb12-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="0bb12-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="0bb12-124">Implementations</span></span>

-   [<span data-ttu-id="0bb12-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0bb12-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0bb12-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0bb12-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0bb12-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0bb12-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="0bb12-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0bb12-128">Windows Server 2008</span></span>



| <span data-ttu-id="0bb12-129">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0bb12-129">Entry</span></span> | <span data-ttu-id="0bb12-130">Wert</span><span class="sxs-lookup"><span data-stu-id="0bb12-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb12-131">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0bb12-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="0bb12-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bb12-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="0bb12-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bb12-133">System-Only</span></span>            | <span data-ttu-id="0bb12-134">False</span><span class="sxs-lookup"><span data-stu-id="0bb12-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="0bb12-135">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0bb12-135">Is-Single-Valued</span></span>       | <span data-ttu-id="0bb12-136">Richtig</span><span class="sxs-lookup"><span data-stu-id="0bb12-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="0bb12-137">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0bb12-137">Is Indexed</span></span>             | <span data-ttu-id="0bb12-138">False</span><span class="sxs-lookup"><span data-stu-id="0bb12-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="0bb12-139">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0bb12-139">In Global Catalog</span></span>      | <span data-ttu-id="0bb12-140">False</span><span class="sxs-lookup"><span data-stu-id="0bb12-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="0bb12-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0bb12-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bb12-142">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0bb12-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="0bb12-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bb12-143">Range-Lower</span></span>            | <span data-ttu-id="0bb12-144">0</span><span class="sxs-lookup"><span data-stu-id="0bb12-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="0bb12-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bb12-145">Range-Upper</span></span>            | <span data-ttu-id="0bb12-146">32766</span><span class="sxs-lookup"><span data-stu-id="0bb12-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="0bb12-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb12-147">Search-Flags</span></span>           | <span data-ttu-id="0bb12-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bb12-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="0bb12-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb12-149">System-Flags</span></span>           | <span data-ttu-id="0bb12-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bb12-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="0bb12-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0bb12-151">Classes used in</span></span>        | [<span data-ttu-id="0bb12-152">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="0bb12-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="0bb12-153">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="0bb12-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0bb12-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0bb12-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0bb12-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0bb12-155">Entry</span></span> | <span data-ttu-id="0bb12-156">Wert</span><span class="sxs-lookup"><span data-stu-id="0bb12-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb12-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0bb12-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="0bb12-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bb12-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="0bb12-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bb12-159">System-Only</span></span>            | <span data-ttu-id="0bb12-160">False</span><span class="sxs-lookup"><span data-stu-id="0bb12-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="0bb12-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0bb12-161">Is-Single-Valued</span></span>       | <span data-ttu-id="0bb12-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="0bb12-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="0bb12-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0bb12-163">Is Indexed</span></span>             | <span data-ttu-id="0bb12-164">False</span><span class="sxs-lookup"><span data-stu-id="0bb12-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="0bb12-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0bb12-165">In Global Catalog</span></span>      | <span data-ttu-id="0bb12-166">False</span><span class="sxs-lookup"><span data-stu-id="0bb12-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="0bb12-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0bb12-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bb12-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0bb12-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="0bb12-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bb12-169">Range-Lower</span></span>            | <span data-ttu-id="0bb12-170">0</span><span class="sxs-lookup"><span data-stu-id="0bb12-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="0bb12-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bb12-171">Range-Upper</span></span>            | <span data-ttu-id="0bb12-172">32766</span><span class="sxs-lookup"><span data-stu-id="0bb12-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="0bb12-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb12-173">Search-Flags</span></span>           | <span data-ttu-id="0bb12-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bb12-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="0bb12-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb12-175">System-Flags</span></span>           | <span data-ttu-id="0bb12-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bb12-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="0bb12-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0bb12-177">Classes used in</span></span>        | [<span data-ttu-id="0bb12-178">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="0bb12-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="0bb12-179">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="0bb12-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0bb12-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0bb12-180">Windows Server 2012</span></span>



| <span data-ttu-id="0bb12-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0bb12-181">Entry</span></span> | <span data-ttu-id="0bb12-182">Wert</span><span class="sxs-lookup"><span data-stu-id="0bb12-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb12-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="0bb12-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="0bb12-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bb12-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="0bb12-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bb12-185">System-Only</span></span>            | <span data-ttu-id="0bb12-186">False</span><span class="sxs-lookup"><span data-stu-id="0bb12-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="0bb12-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="0bb12-187">Is-Single-Valued</span></span>       | <span data-ttu-id="0bb12-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="0bb12-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="0bb12-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="0bb12-189">Is Indexed</span></span>             | <span data-ttu-id="0bb12-190">False</span><span class="sxs-lookup"><span data-stu-id="0bb12-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="0bb12-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="0bb12-191">In Global Catalog</span></span>      | <span data-ttu-id="0bb12-192">False</span><span class="sxs-lookup"><span data-stu-id="0bb12-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="0bb12-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0bb12-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bb12-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="0bb12-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="0bb12-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bb12-195">Range-Lower</span></span>            | <span data-ttu-id="0bb12-196">0</span><span class="sxs-lookup"><span data-stu-id="0bb12-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="0bb12-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bb12-197">Range-Upper</span></span>            | <span data-ttu-id="0bb12-198">32766</span><span class="sxs-lookup"><span data-stu-id="0bb12-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="0bb12-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb12-199">Search-Flags</span></span>           | <span data-ttu-id="0bb12-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bb12-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="0bb12-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bb12-201">System-Flags</span></span>           | <span data-ttu-id="0bb12-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bb12-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="0bb12-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="0bb12-203">Classes used in</span></span>        | [<span data-ttu-id="0bb12-204">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="0bb12-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="0bb12-205">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="0bb12-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





