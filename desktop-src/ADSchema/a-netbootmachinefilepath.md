---
title: NetBoot-Machine-File-path-Attribut
description: Dieses Attribut gibt den Server an, der den Client beantwortet. Beginnend mit dem Betriebssystem Windows Server 2003 können Sie den Startrom.com-Wert angeben, der vom Client abgerufen wird.
ms.assetid: 8706bf38-8027-4260-b382-4d4c2a6e0f6e
ms.tgt_platform: multiple
keywords:
- NetBoot-Machine-File-path-Attribut AD-Schema
- netbootMachineFilePath-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Netboot-Machine-File-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d03ead4f307b7c0b524192d9c865ee437fbd9d2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106341067"
---
# <a name="netboot-machine-file-path-attribute"></a><span data-ttu-id="22a6c-106">NetBoot-Machine-File-path-Attribut</span><span class="sxs-lookup"><span data-stu-id="22a6c-106">Netboot-Machine-File-Path attribute</span></span>

<span data-ttu-id="22a6c-107">Dieses Attribut gibt den Server an, der den Client beantwortet.</span><span class="sxs-lookup"><span data-stu-id="22a6c-107">This attribute specifies the server that answers the client.</span></span> <span data-ttu-id="22a6c-108">Beginnend mit dem Betriebssystem Windows Server 2003 können Sie den Startrom.com-Wert angeben, der vom Client abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="22a6c-108">Beginning with the Windows Server 2003 operating system, it can indicate the Startrom.com that the client gets.</span></span>



| <span data-ttu-id="22a6c-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22a6c-109">Entry</span></span> | <span data-ttu-id="22a6c-110">Wert</span><span class="sxs-lookup"><span data-stu-id="22a6c-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="22a6c-111">CN</span><span class="sxs-lookup"><span data-stu-id="22a6c-111">CN</span></span>                | <span data-ttu-id="22a6c-112">NetBoot-Machine-Dateipfad</span><span class="sxs-lookup"><span data-stu-id="22a6c-112">Netboot-Machine-File-Path</span></span>                   |
| <span data-ttu-id="22a6c-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="22a6c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="22a6c-114">netbootMachineFilePath</span><span class="sxs-lookup"><span data-stu-id="22a6c-114">netbootMachineFilePath</span></span>                      |
| <span data-ttu-id="22a6c-115">Size</span><span class="sxs-lookup"><span data-stu-id="22a6c-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="22a6c-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="22a6c-116">Update Privilege</span></span>  | <span data-ttu-id="22a6c-117">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22a6c-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="22a6c-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="22a6c-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="22a6c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="22a6c-119">Attribute-Id</span></span>      | <span data-ttu-id="22a6c-120">1.2.840.113556.1.4.361</span><span class="sxs-lookup"><span data-stu-id="22a6c-120">1.2.840.113556.1.4.361</span></span>                      |
| <span data-ttu-id="22a6c-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="22a6c-121">System-Id-Guid</span></span>    | <span data-ttu-id="22a6c-122">3e978923-8c01-11D0-AFDA-00c04f 930c9</span><span class="sxs-lookup"><span data-stu-id="22a6c-122">3e978923-8c01-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="22a6c-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="22a6c-123">Syntax</span></span>            | [<span data-ttu-id="22a6c-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="22a6c-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="22a6c-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="22a6c-125">Implementations</span></span>

-   [<span data-ttu-id="22a6c-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="22a6c-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="22a6c-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="22a6c-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="22a6c-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="22a6c-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="22a6c-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="22a6c-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="22a6c-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="22a6c-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="22a6c-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="22a6c-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="22a6c-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="22a6c-132">Windows 2000 Server</span></span>



| <span data-ttu-id="22a6c-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22a6c-133">Entry</span></span> | <span data-ttu-id="22a6c-134">Wert</span><span class="sxs-lookup"><span data-stu-id="22a6c-134">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22a6c-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="22a6c-135">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="22a6c-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22a6c-136">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="22a6c-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="22a6c-137">System-Only</span></span>            | <span data-ttu-id="22a6c-138">False</span><span class="sxs-lookup"><span data-stu-id="22a6c-138">False</span></span>                                                                                                |
| <span data-ttu-id="22a6c-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="22a6c-139">Is-Single-Valued</span></span>       | <span data-ttu-id="22a6c-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="22a6c-140">True</span></span>                                                                                                 |
| <span data-ttu-id="22a6c-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="22a6c-141">Is Indexed</span></span>             | <span data-ttu-id="22a6c-142">False</span><span class="sxs-lookup"><span data-stu-id="22a6c-142">False</span></span>                                                                                                |
| <span data-ttu-id="22a6c-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="22a6c-143">In Global Catalog</span></span>      | <span data-ttu-id="22a6c-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="22a6c-144">True</span></span>                                                                                                 |
| <span data-ttu-id="22a6c-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22a6c-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="22a6c-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="22a6c-146">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="22a6c-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22a6c-147">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="22a6c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22a6c-148">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="22a6c-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22a6c-149">Search-Flags</span></span>           | <span data-ttu-id="22a6c-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22a6c-150">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="22a6c-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22a6c-151">System-Flags</span></span>           | <span data-ttu-id="22a6c-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22a6c-152">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="22a6c-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="22a6c-153">Classes used in</span></span>        | [<span data-ttu-id="22a6c-154">**Computer**</span><span class="sxs-lookup"><span data-stu-id="22a6c-154">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="22a6c-155">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="22a6c-155">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="22a6c-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="22a6c-156">Windows Server 2003</span></span>



| <span data-ttu-id="22a6c-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22a6c-157">Entry</span></span> | <span data-ttu-id="22a6c-158">Wert</span><span class="sxs-lookup"><span data-stu-id="22a6c-158">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22a6c-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="22a6c-159">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="22a6c-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22a6c-160">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="22a6c-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="22a6c-161">System-Only</span></span>            | <span data-ttu-id="22a6c-162">False</span><span class="sxs-lookup"><span data-stu-id="22a6c-162">False</span></span>                                                                                                |
| <span data-ttu-id="22a6c-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="22a6c-163">Is-Single-Valued</span></span>       | <span data-ttu-id="22a6c-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="22a6c-164">True</span></span>                                                                                                 |
| <span data-ttu-id="22a6c-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="22a6c-165">Is Indexed</span></span>             | <span data-ttu-id="22a6c-166">False</span><span class="sxs-lookup"><span data-stu-id="22a6c-166">False</span></span>                                                                                                |
| <span data-ttu-id="22a6c-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="22a6c-167">In Global Catalog</span></span>      | <span data-ttu-id="22a6c-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="22a6c-168">True</span></span>                                                                                                 |
| <span data-ttu-id="22a6c-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22a6c-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="22a6c-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="22a6c-170">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="22a6c-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22a6c-171">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="22a6c-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22a6c-172">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="22a6c-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22a6c-173">Search-Flags</span></span>           | <span data-ttu-id="22a6c-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22a6c-174">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="22a6c-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22a6c-175">System-Flags</span></span>           | <span data-ttu-id="22a6c-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22a6c-176">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="22a6c-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="22a6c-177">Classes used in</span></span>        | [<span data-ttu-id="22a6c-178">**Computer**</span><span class="sxs-lookup"><span data-stu-id="22a6c-178">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="22a6c-179">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="22a6c-179">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="22a6c-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="22a6c-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="22a6c-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22a6c-181">Entry</span></span> | <span data-ttu-id="22a6c-182">Wert</span><span class="sxs-lookup"><span data-stu-id="22a6c-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22a6c-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="22a6c-183">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="22a6c-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22a6c-184">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="22a6c-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="22a6c-185">System-Only</span></span>            | <span data-ttu-id="22a6c-186">False</span><span class="sxs-lookup"><span data-stu-id="22a6c-186">False</span></span>                                                                                                |
| <span data-ttu-id="22a6c-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="22a6c-187">Is-Single-Valued</span></span>       | <span data-ttu-id="22a6c-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="22a6c-188">True</span></span>                                                                                                 |
| <span data-ttu-id="22a6c-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="22a6c-189">Is Indexed</span></span>             | <span data-ttu-id="22a6c-190">False</span><span class="sxs-lookup"><span data-stu-id="22a6c-190">False</span></span>                                                                                                |
| <span data-ttu-id="22a6c-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="22a6c-191">In Global Catalog</span></span>      | <span data-ttu-id="22a6c-192">Richtig</span><span class="sxs-lookup"><span data-stu-id="22a6c-192">True</span></span>                                                                                                 |
| <span data-ttu-id="22a6c-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22a6c-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="22a6c-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="22a6c-194">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="22a6c-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22a6c-195">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="22a6c-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22a6c-196">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="22a6c-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22a6c-197">Search-Flags</span></span>           | <span data-ttu-id="22a6c-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22a6c-198">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="22a6c-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22a6c-199">System-Flags</span></span>           | <span data-ttu-id="22a6c-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22a6c-200">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="22a6c-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="22a6c-201">Classes used in</span></span>        | [<span data-ttu-id="22a6c-202">**Computer**</span><span class="sxs-lookup"><span data-stu-id="22a6c-202">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="22a6c-203">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="22a6c-203">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="22a6c-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22a6c-204">Windows Server 2008</span></span>



| <span data-ttu-id="22a6c-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22a6c-205">Entry</span></span> | <span data-ttu-id="22a6c-206">Wert</span><span class="sxs-lookup"><span data-stu-id="22a6c-206">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22a6c-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="22a6c-207">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="22a6c-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22a6c-208">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="22a6c-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="22a6c-209">System-Only</span></span>            | <span data-ttu-id="22a6c-210">False</span><span class="sxs-lookup"><span data-stu-id="22a6c-210">False</span></span>                                                                                                |
| <span data-ttu-id="22a6c-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="22a6c-211">Is-Single-Valued</span></span>       | <span data-ttu-id="22a6c-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="22a6c-212">True</span></span>                                                                                                 |
| <span data-ttu-id="22a6c-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="22a6c-213">Is Indexed</span></span>             | <span data-ttu-id="22a6c-214">False</span><span class="sxs-lookup"><span data-stu-id="22a6c-214">False</span></span>                                                                                                |
| <span data-ttu-id="22a6c-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="22a6c-215">In Global Catalog</span></span>      | <span data-ttu-id="22a6c-216">Richtig</span><span class="sxs-lookup"><span data-stu-id="22a6c-216">True</span></span>                                                                                                 |
| <span data-ttu-id="22a6c-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22a6c-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="22a6c-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="22a6c-218">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="22a6c-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22a6c-219">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="22a6c-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22a6c-220">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="22a6c-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22a6c-221">Search-Flags</span></span>           | <span data-ttu-id="22a6c-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22a6c-222">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="22a6c-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22a6c-223">System-Flags</span></span>           | <span data-ttu-id="22a6c-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22a6c-224">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="22a6c-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="22a6c-225">Classes used in</span></span>        | [<span data-ttu-id="22a6c-226">**Computer**</span><span class="sxs-lookup"><span data-stu-id="22a6c-226">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="22a6c-227">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="22a6c-227">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="22a6c-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="22a6c-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="22a6c-229">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22a6c-229">Entry</span></span> | <span data-ttu-id="22a6c-230">Wert</span><span class="sxs-lookup"><span data-stu-id="22a6c-230">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22a6c-231">Link-ID</span><span class="sxs-lookup"><span data-stu-id="22a6c-231">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="22a6c-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22a6c-232">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="22a6c-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="22a6c-233">System-Only</span></span>            | <span data-ttu-id="22a6c-234">False</span><span class="sxs-lookup"><span data-stu-id="22a6c-234">False</span></span>                                                                                                |
| <span data-ttu-id="22a6c-235">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="22a6c-235">Is-Single-Valued</span></span>       | <span data-ttu-id="22a6c-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="22a6c-236">True</span></span>                                                                                                 |
| <span data-ttu-id="22a6c-237">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="22a6c-237">Is Indexed</span></span>             | <span data-ttu-id="22a6c-238">False</span><span class="sxs-lookup"><span data-stu-id="22a6c-238">False</span></span>                                                                                                |
| <span data-ttu-id="22a6c-239">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="22a6c-239">In Global Catalog</span></span>      | <span data-ttu-id="22a6c-240">Richtig</span><span class="sxs-lookup"><span data-stu-id="22a6c-240">True</span></span>                                                                                                 |
| <span data-ttu-id="22a6c-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22a6c-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="22a6c-242">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="22a6c-242">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="22a6c-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22a6c-243">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="22a6c-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22a6c-244">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="22a6c-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22a6c-245">Search-Flags</span></span>           | <span data-ttu-id="22a6c-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22a6c-246">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="22a6c-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22a6c-247">System-Flags</span></span>           | <span data-ttu-id="22a6c-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22a6c-248">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="22a6c-249">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="22a6c-249">Classes used in</span></span>        | [<span data-ttu-id="22a6c-250">**Computer**</span><span class="sxs-lookup"><span data-stu-id="22a6c-250">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="22a6c-251">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="22a6c-251">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="22a6c-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="22a6c-252">Windows Server 2012</span></span>



| <span data-ttu-id="22a6c-253">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22a6c-253">Entry</span></span> | <span data-ttu-id="22a6c-254">Wert</span><span class="sxs-lookup"><span data-stu-id="22a6c-254">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22a6c-255">Link-ID</span><span class="sxs-lookup"><span data-stu-id="22a6c-255">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="22a6c-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22a6c-256">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="22a6c-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="22a6c-257">System-Only</span></span>            | <span data-ttu-id="22a6c-258">False</span><span class="sxs-lookup"><span data-stu-id="22a6c-258">False</span></span>                                                                                                |
| <span data-ttu-id="22a6c-259">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="22a6c-259">Is-Single-Valued</span></span>       | <span data-ttu-id="22a6c-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="22a6c-260">True</span></span>                                                                                                 |
| <span data-ttu-id="22a6c-261">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="22a6c-261">Is Indexed</span></span>             | <span data-ttu-id="22a6c-262">False</span><span class="sxs-lookup"><span data-stu-id="22a6c-262">False</span></span>                                                                                                |
| <span data-ttu-id="22a6c-263">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="22a6c-263">In Global Catalog</span></span>      | <span data-ttu-id="22a6c-264">Richtig</span><span class="sxs-lookup"><span data-stu-id="22a6c-264">True</span></span>                                                                                                 |
| <span data-ttu-id="22a6c-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22a6c-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="22a6c-266">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="22a6c-266">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="22a6c-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22a6c-267">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="22a6c-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22a6c-268">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="22a6c-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22a6c-269">Search-Flags</span></span>           | <span data-ttu-id="22a6c-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22a6c-270">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="22a6c-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22a6c-271">System-Flags</span></span>           | <span data-ttu-id="22a6c-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22a6c-272">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="22a6c-273">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="22a6c-273">Classes used in</span></span>        | [<span data-ttu-id="22a6c-274">**Computer**</span><span class="sxs-lookup"><span data-stu-id="22a6c-274">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="22a6c-275">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="22a6c-275">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 





