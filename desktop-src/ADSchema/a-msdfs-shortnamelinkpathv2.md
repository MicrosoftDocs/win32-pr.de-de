---
title: ms-DFS-Short-Name-Link-Path-v2-Attribut
description: 'Kurzname: DFS-Linkpfad relativ zur DFS-Stammzielfreigabe (d. h. ohne komponenten des Server-/Domänen- und DFS-Namespacenamens). Verwenden Sie schräge Schrägstriche (/) anstelle von schrägen Schrägstrichen ( ), damit LDAP-Suchvorgänge durchgeführt werden können, ohne \) Escapestriche verwenden zu müssen.'
ms.assetid: 0589d3f5-9734-4f95-bba9-22f13bb1c9f1
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-DFS-Short-Name-Link-Path-v2-Attributs
- AD-Schema des msDFS-ShortNameLinkPathv2-Attributs
topic_type:
- apiref
api_name:
- ms-DFS-Short-Name-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 663ee1ff2dac67eff7bd9eca87aa8eacf40436ff
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386849"
---
# <a name="ms-dfs-short-name-link-path-v2-attribute"></a><span data-ttu-id="38e48-106">ms-DFS-Short-Name-Link-Path-v2-Attribut</span><span class="sxs-lookup"><span data-stu-id="38e48-106">ms-DFS-Short-Name-Link-Path-v2 attribute</span></span>

<span data-ttu-id="38e48-107">Kurzname: DFS-Linkpfad relativ zur DFS-Stammzielfreigabe (d. h. ohne komponenten des Server-/Domänen- und DFS-Namespacenamens).</span><span class="sxs-lookup"><span data-stu-id="38e48-107">Short Name DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="38e48-108">Verwenden Sie schräge Schrägstriche (/) anstelle von schrägen Schrägstrichen (), damit LDAP-Suchvorgänge durchgeführt werden können, ohne \\ Escapestriche verwenden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="38e48-108">Use forward slashes (/) instead of backslashes (\\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="38e48-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38e48-109">Entry</span></span> | <span data-ttu-id="38e48-110">Wert</span><span class="sxs-lookup"><span data-stu-id="38e48-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="38e48-111">CN</span><span class="sxs-lookup"><span data-stu-id="38e48-111">CN</span></span>                | <span data-ttu-id="38e48-112">ms-DFS-Short-Name-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="38e48-112">ms-DFS-Short-Name-Link-Path-v2</span></span>              |
| <span data-ttu-id="38e48-113">Ldap-Anzeigename</span><span class="sxs-lookup"><span data-stu-id="38e48-113">Ldap-Display-Name</span></span> | <span data-ttu-id="38e48-114">msDFS-ShortNameLinkPathv2</span><span class="sxs-lookup"><span data-stu-id="38e48-114">msDFS-ShortNameLinkPathv2</span></span>                   |
| <span data-ttu-id="38e48-115">Size</span><span class="sxs-lookup"><span data-stu-id="38e48-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="38e48-116">Aktualisieren von Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="38e48-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="38e48-117">Updatehäufigkeit</span><span class="sxs-lookup"><span data-stu-id="38e48-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="38e48-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="38e48-118">Attribute-Id</span></span>      | <span data-ttu-id="38e48-119">1.2.840.113556.1.4.2042</span><span class="sxs-lookup"><span data-stu-id="38e48-119">1.2.840.113556.1.4.2042</span></span>                     |
| <span data-ttu-id="38e48-120">System-Id-Guid</span><span class="sxs-lookup"><span data-stu-id="38e48-120">System-Id-Guid</span></span>    | <span data-ttu-id="38e48-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span><span class="sxs-lookup"><span data-stu-id="38e48-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span></span>        |
| <span data-ttu-id="38e48-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="38e48-122">Syntax</span></span>            | [<span data-ttu-id="38e48-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="38e48-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="38e48-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="38e48-124">Implementations</span></span>

-   [<span data-ttu-id="38e48-125">**WindowsServer 2008**</span><span class="sxs-lookup"><span data-stu-id="38e48-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="38e48-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="38e48-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="38e48-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="38e48-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="38e48-128">WindowsServer 2008</span><span class="sxs-lookup"><span data-stu-id="38e48-128">Windows Server 2008</span></span>



| <span data-ttu-id="38e48-129">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38e48-129">Entry</span></span> | <span data-ttu-id="38e48-130">Wert</span><span class="sxs-lookup"><span data-stu-id="38e48-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38e48-131">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38e48-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="38e48-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38e48-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="38e48-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="38e48-133">System-Only</span></span>            | <span data-ttu-id="38e48-134">Falsch</span><span class="sxs-lookup"><span data-stu-id="38e48-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="38e48-135">Is-Single-Valued</span><span class="sxs-lookup"><span data-stu-id="38e48-135">Is-Single-Valued</span></span>       | <span data-ttu-id="38e48-136">Richtig</span><span class="sxs-lookup"><span data-stu-id="38e48-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="38e48-137">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38e48-137">Is Indexed</span></span>             | <span data-ttu-id="38e48-138">Falsch</span><span class="sxs-lookup"><span data-stu-id="38e48-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="38e48-139">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38e48-139">In Global Catalog</span></span>      | <span data-ttu-id="38e48-140">Falsch</span><span class="sxs-lookup"><span data-stu-id="38e48-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="38e48-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38e48-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="38e48-142">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="38e48-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="38e48-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38e48-143">Range-Lower</span></span>            | <span data-ttu-id="38e48-144">0</span><span class="sxs-lookup"><span data-stu-id="38e48-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="38e48-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38e48-145">Range-Upper</span></span>            | <span data-ttu-id="38e48-146">32766</span><span class="sxs-lookup"><span data-stu-id="38e48-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="38e48-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38e48-147">Search-Flags</span></span>           | <span data-ttu-id="38e48-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38e48-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="38e48-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38e48-149">System-Flags</span></span>           | <span data-ttu-id="38e48-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38e48-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="38e48-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38e48-151">Classes used in</span></span>        | [<span data-ttu-id="38e48-152">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="38e48-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="38e48-153">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="38e48-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="38e48-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="38e48-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="38e48-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38e48-155">Entry</span></span> | <span data-ttu-id="38e48-156">Wert</span><span class="sxs-lookup"><span data-stu-id="38e48-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38e48-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38e48-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="38e48-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38e48-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="38e48-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="38e48-159">System-Only</span></span>            | <span data-ttu-id="38e48-160">Falsch</span><span class="sxs-lookup"><span data-stu-id="38e48-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="38e48-161">Is-Single-Valued</span><span class="sxs-lookup"><span data-stu-id="38e48-161">Is-Single-Valued</span></span>       | <span data-ttu-id="38e48-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="38e48-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="38e48-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38e48-163">Is Indexed</span></span>             | <span data-ttu-id="38e48-164">Falsch</span><span class="sxs-lookup"><span data-stu-id="38e48-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="38e48-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38e48-165">In Global Catalog</span></span>      | <span data-ttu-id="38e48-166">Falsch</span><span class="sxs-lookup"><span data-stu-id="38e48-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="38e48-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38e48-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="38e48-168">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="38e48-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="38e48-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38e48-169">Range-Lower</span></span>            | <span data-ttu-id="38e48-170">0</span><span class="sxs-lookup"><span data-stu-id="38e48-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="38e48-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38e48-171">Range-Upper</span></span>            | <span data-ttu-id="38e48-172">32766</span><span class="sxs-lookup"><span data-stu-id="38e48-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="38e48-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38e48-173">Search-Flags</span></span>           | <span data-ttu-id="38e48-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38e48-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="38e48-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38e48-175">System-Flags</span></span>           | <span data-ttu-id="38e48-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38e48-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="38e48-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38e48-177">Classes used in</span></span>        | [<span data-ttu-id="38e48-178">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="38e48-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="38e48-179">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="38e48-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="38e48-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38e48-180">Windows Server 2012</span></span>



| <span data-ttu-id="38e48-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38e48-181">Entry</span></span> | <span data-ttu-id="38e48-182">Wert</span><span class="sxs-lookup"><span data-stu-id="38e48-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38e48-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="38e48-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="38e48-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38e48-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="38e48-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="38e48-185">System-Only</span></span>            | <span data-ttu-id="38e48-186">Falsch</span><span class="sxs-lookup"><span data-stu-id="38e48-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="38e48-187">Is-Single-Valued</span><span class="sxs-lookup"><span data-stu-id="38e48-187">Is-Single-Valued</span></span>       | <span data-ttu-id="38e48-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="38e48-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="38e48-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="38e48-189">Is Indexed</span></span>             | <span data-ttu-id="38e48-190">Falsch</span><span class="sxs-lookup"><span data-stu-id="38e48-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="38e48-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="38e48-191">In Global Catalog</span></span>      | <span data-ttu-id="38e48-192">Falsch</span><span class="sxs-lookup"><span data-stu-id="38e48-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="38e48-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="38e48-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="38e48-194">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="38e48-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="38e48-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38e48-195">Range-Lower</span></span>            | <span data-ttu-id="38e48-196">0</span><span class="sxs-lookup"><span data-stu-id="38e48-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="38e48-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38e48-197">Range-Upper</span></span>            | <span data-ttu-id="38e48-198">32766</span><span class="sxs-lookup"><span data-stu-id="38e48-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="38e48-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38e48-199">Search-Flags</span></span>           | <span data-ttu-id="38e48-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38e48-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="38e48-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38e48-201">System-Flags</span></span>           | <span data-ttu-id="38e48-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38e48-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="38e48-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="38e48-203">Classes used in</span></span>        | [<span data-ttu-id="38e48-204">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="38e48-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="38e48-205">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="38e48-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





