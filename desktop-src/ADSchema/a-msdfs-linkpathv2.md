---
title: ms-DFS-Link-Path-v2-Attribut
description: DFS-Linkpfad relativ zur DFS-Stammzielfreigabe (d. h. ohne die Server-/Domänen- und DFS-Namespacenamenkomponenten). Verwenden Sie Schrägstriche (/) anstelle umgekehrter Schrägstriche ( \) , damit LDAP-Suchvorgänge ohne Escapevorgänge durchgeführt werden können.
ms.assetid: 98fd6e99-0d7e-4ffa-b8ec-d26ca03ffead
ms.tgt_platform: multiple
keywords:
- MS-DFS-Link-Path-v2-Attribut AD-Schema
- MSDFS-LinkPathv2-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-DFS-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4659dbf00c6a53c77a23e98836ea1af4eeb4c38a
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386859"
---
# <a name="ms-dfs-link-path-v2-attribute"></a><span data-ttu-id="5effd-106">ms-DFS-Link-Path-v2-Attribut</span><span class="sxs-lookup"><span data-stu-id="5effd-106">ms-DFS-Link-Path-v2 attribute</span></span>

<span data-ttu-id="5effd-107">DFS-Linkpfad relativ zur DFS-Stammzielfreigabe (d. h. ohne die Server-/Domänen- und DFS-Namespacenamenkomponenten).</span><span class="sxs-lookup"><span data-stu-id="5effd-107">DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="5effd-108">Verwenden Sie Schrägstriche (/) anstelle umgekehrter Schrägstriche \\ (), damit LDAP-Suchvorgänge ohne Escapevorgänge durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="5effd-108">Use forward slashes (/) instead of backslashes (\\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="5effd-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5effd-109">Entry</span></span> | <span data-ttu-id="5effd-110">Wert</span><span class="sxs-lookup"><span data-stu-id="5effd-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5effd-111">CN</span><span class="sxs-lookup"><span data-stu-id="5effd-111">CN</span></span>                | <span data-ttu-id="5effd-112">ms-DFS-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="5effd-112">ms-DFS-Link-Path-v2</span></span>                         |
| <span data-ttu-id="5effd-113">Ldap-Anzeigename</span><span class="sxs-lookup"><span data-stu-id="5effd-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5effd-114">msDFS-LinkPathv2</span><span class="sxs-lookup"><span data-stu-id="5effd-114">msDFS-LinkPathv2</span></span>                            |
| <span data-ttu-id="5effd-115">Size</span><span class="sxs-lookup"><span data-stu-id="5effd-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="5effd-116">Aktualisieren von Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="5effd-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="5effd-117">Updatehäufigkeit</span><span class="sxs-lookup"><span data-stu-id="5effd-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="5effd-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5effd-118">Attribute-Id</span></span>      | <span data-ttu-id="5effd-119">1.2.840.113556.1.4.2039</span><span class="sxs-lookup"><span data-stu-id="5effd-119">1.2.840.113556.1.4.2039</span></span>                     |
| <span data-ttu-id="5effd-120">System-Id-Guid</span><span class="sxs-lookup"><span data-stu-id="5effd-120">System-Id-Guid</span></span>    | <span data-ttu-id="5effd-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span><span class="sxs-lookup"><span data-stu-id="5effd-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span></span>        |
| <span data-ttu-id="5effd-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5effd-122">Syntax</span></span>            | [<span data-ttu-id="5effd-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5effd-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5effd-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="5effd-124">Implementations</span></span>

-   [<span data-ttu-id="5effd-125">**WindowsServer 2008**</span><span class="sxs-lookup"><span data-stu-id="5effd-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5effd-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5effd-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5effd-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5effd-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="5effd-128">WindowsServer 2008</span><span class="sxs-lookup"><span data-stu-id="5effd-128">Windows Server 2008</span></span>



| <span data-ttu-id="5effd-129">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5effd-129">Entry</span></span> | <span data-ttu-id="5effd-130">Wert</span><span class="sxs-lookup"><span data-stu-id="5effd-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5effd-131">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5effd-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5effd-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5effd-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5effd-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="5effd-133">System-Only</span></span>            | <span data-ttu-id="5effd-134">Falsch</span><span class="sxs-lookup"><span data-stu-id="5effd-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="5effd-135">Ist einwertig</span><span class="sxs-lookup"><span data-stu-id="5effd-135">Is-Single-Valued</span></span>       | <span data-ttu-id="5effd-136">Richtig</span><span class="sxs-lookup"><span data-stu-id="5effd-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="5effd-137">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5effd-137">Is Indexed</span></span>             | <span data-ttu-id="5effd-138">Falsch</span><span class="sxs-lookup"><span data-stu-id="5effd-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="5effd-139">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5effd-139">In Global Catalog</span></span>      | <span data-ttu-id="5effd-140">Falsch</span><span class="sxs-lookup"><span data-stu-id="5effd-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="5effd-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5effd-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="5effd-142">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="5effd-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="5effd-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5effd-143">Range-Lower</span></span>            | <span data-ttu-id="5effd-144">0</span><span class="sxs-lookup"><span data-stu-id="5effd-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="5effd-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5effd-145">Range-Upper</span></span>            | <span data-ttu-id="5effd-146">32766</span><span class="sxs-lookup"><span data-stu-id="5effd-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="5effd-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5effd-147">Search-Flags</span></span>           | <span data-ttu-id="5effd-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5effd-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="5effd-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5effd-149">System-Flags</span></span>           | <span data-ttu-id="5effd-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5effd-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="5effd-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5effd-151">Classes used in</span></span>        | [<span data-ttu-id="5effd-152">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5effd-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="5effd-153">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5effd-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5effd-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5effd-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5effd-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5effd-155">Entry</span></span> | <span data-ttu-id="5effd-156">Wert</span><span class="sxs-lookup"><span data-stu-id="5effd-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5effd-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5effd-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5effd-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5effd-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5effd-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5effd-159">System-Only</span></span>            | <span data-ttu-id="5effd-160">Falsch</span><span class="sxs-lookup"><span data-stu-id="5effd-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="5effd-161">Ist einwertig</span><span class="sxs-lookup"><span data-stu-id="5effd-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5effd-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="5effd-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="5effd-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5effd-163">Is Indexed</span></span>             | <span data-ttu-id="5effd-164">Falsch</span><span class="sxs-lookup"><span data-stu-id="5effd-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="5effd-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5effd-165">In Global Catalog</span></span>      | <span data-ttu-id="5effd-166">Falsch</span><span class="sxs-lookup"><span data-stu-id="5effd-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="5effd-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5effd-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5effd-168">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="5effd-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="5effd-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5effd-169">Range-Lower</span></span>            | <span data-ttu-id="5effd-170">0</span><span class="sxs-lookup"><span data-stu-id="5effd-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="5effd-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5effd-171">Range-Upper</span></span>            | <span data-ttu-id="5effd-172">32766</span><span class="sxs-lookup"><span data-stu-id="5effd-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="5effd-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5effd-173">Search-Flags</span></span>           | <span data-ttu-id="5effd-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5effd-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="5effd-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5effd-175">System-Flags</span></span>           | <span data-ttu-id="5effd-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5effd-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="5effd-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5effd-177">Classes used in</span></span>        | [<span data-ttu-id="5effd-178">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5effd-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="5effd-179">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5effd-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5effd-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5effd-180">Windows Server 2012</span></span>



| <span data-ttu-id="5effd-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5effd-181">Entry</span></span> | <span data-ttu-id="5effd-182">Wert</span><span class="sxs-lookup"><span data-stu-id="5effd-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5effd-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5effd-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5effd-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5effd-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5effd-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="5effd-185">System-Only</span></span>            | <span data-ttu-id="5effd-186">Falsch</span><span class="sxs-lookup"><span data-stu-id="5effd-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="5effd-187">Ist einwertig</span><span class="sxs-lookup"><span data-stu-id="5effd-187">Is-Single-Valued</span></span>       | <span data-ttu-id="5effd-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="5effd-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="5effd-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5effd-189">Is Indexed</span></span>             | <span data-ttu-id="5effd-190">Falsch</span><span class="sxs-lookup"><span data-stu-id="5effd-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="5effd-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5effd-191">In Global Catalog</span></span>      | <span data-ttu-id="5effd-192">Falsch</span><span class="sxs-lookup"><span data-stu-id="5effd-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="5effd-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5effd-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="5effd-194">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="5effd-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="5effd-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5effd-195">Range-Lower</span></span>            | <span data-ttu-id="5effd-196">0</span><span class="sxs-lookup"><span data-stu-id="5effd-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="5effd-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5effd-197">Range-Upper</span></span>            | <span data-ttu-id="5effd-198">32766</span><span class="sxs-lookup"><span data-stu-id="5effd-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="5effd-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5effd-199">Search-Flags</span></span>           | <span data-ttu-id="5effd-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5effd-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="5effd-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5effd-201">System-Flags</span></span>           | <span data-ttu-id="5effd-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5effd-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="5effd-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5effd-203">Classes used in</span></span>        | [<span data-ttu-id="5effd-204">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5effd-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="5effd-205">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5effd-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





