---
title: MS-DS-Machine-Account-Quota-Attribut
description: Die Anzahl der Computer Konten, die ein Benutzer in einer Domäne erstellen darf.
ms.assetid: bcfc6a9c-b891-48c2-9c42-8154345caf08
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-DS-Machine-Account-Quota-Attributs
- AD-Schema des ms-DS-machineaccountquota-Attributs
topic_type:
- apiref
api_name:
- MS-DS-Machine-Account-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86de012aa876e5a0d52ac866048801872a365f1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107871"
---
# <a name="ms-ds-machine-account-quota-attribute"></a><span data-ttu-id="a3ab0-105">MS-DS-Machine-Account-Quota-Attribut</span><span class="sxs-lookup"><span data-stu-id="a3ab0-105">MS-DS-Machine-Account-Quota attribute</span></span>

<span data-ttu-id="a3ab0-106">Die Anzahl der Computer Konten, die ein Benutzer in einer Domäne erstellen darf.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-106">The number of computer accounts that a user is allowed to create in a domain.</span></span>



| <span data-ttu-id="a3ab0-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3ab0-107">Entry</span></span> | <span data-ttu-id="a3ab0-108">Wert</span><span class="sxs-lookup"><span data-stu-id="a3ab0-108">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="a3ab0-109">CN</span><span class="sxs-lookup"><span data-stu-id="a3ab0-109">CN</span></span>                | <span data-ttu-id="a3ab0-110">MS-DS-Computer-Account-Quota</span><span class="sxs-lookup"><span data-stu-id="a3ab0-110">MS-DS-Machine-Account-Quota</span></span>                      |
| <span data-ttu-id="a3ab0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a3ab0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a3ab0-112">ms-DS-machineaccountquota</span><span class="sxs-lookup"><span data-stu-id="a3ab0-112">ms-DS-MachineAccountQuota</span></span>                        |
| <span data-ttu-id="a3ab0-113">Size</span><span class="sxs-lookup"><span data-stu-id="a3ab0-113">Size</span></span>              | <span data-ttu-id="a3ab0-114">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="a3ab0-114">4 bytes</span></span>                                          |
| <span data-ttu-id="a3ab0-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a3ab0-115">Update Privilege</span></span>  | <span data-ttu-id="a3ab0-116">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="a3ab0-116">Domain administrator</span></span>                             |
| <span data-ttu-id="a3ab0-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="a3ab0-117">Update Frequency</span></span>  | <span data-ttu-id="a3ab0-118">Wann immer das Kontingent für eine Domäne geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-118">Whenever the quota for a domain needs to change.</span></span> |
| <span data-ttu-id="a3ab0-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a3ab0-119">Attribute-Id</span></span>      | <span data-ttu-id="a3ab0-120">1.2.840.113556.1.4.1411</span><span class="sxs-lookup"><span data-stu-id="a3ab0-120">1.2.840.113556.1.4.1411</span></span>                          |
| <span data-ttu-id="a3ab0-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a3ab0-121">System-Id-Guid</span></span>    | <span data-ttu-id="a3ab0-122">d064fb68-1480-11d3-91c1-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="a3ab0-122">d064fb68-1480-11d3-91c1-0000f87a57d4</span></span>             |
| <span data-ttu-id="a3ab0-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3ab0-123">Syntax</span></span>            | [<span data-ttu-id="a3ab0-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="a3ab0-124">**Enumeration**</span></span>](s-enumeration.md)             |



## <a name="implementations"></a><span data-ttu-id="a3ab0-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="a3ab0-125">Implementations</span></span>

-   [<span data-ttu-id="a3ab0-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a3ab0-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a3ab0-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a3ab0-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a3ab0-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a3ab0-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a3ab0-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a3ab0-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a3ab0-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a3ab0-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a3ab0-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a3ab0-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a3ab0-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a3ab0-132">Windows 2000 Server</span></span>



| <span data-ttu-id="a3ab0-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3ab0-133">Entry</span></span> | <span data-ttu-id="a3ab0-134">Wert</span><span class="sxs-lookup"><span data-stu-id="a3ab0-134">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a3ab0-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a3ab0-135">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a3ab0-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3ab0-136">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a3ab0-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3ab0-137">System-Only</span></span>            | <span data-ttu-id="a3ab0-138">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-138">False</span></span>                                        |
| <span data-ttu-id="a3ab0-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a3ab0-139">Is-Single-Valued</span></span>       | <span data-ttu-id="a3ab0-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="a3ab0-140">True</span></span>                                         |
| <span data-ttu-id="a3ab0-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a3ab0-141">Is Indexed</span></span>             | <span data-ttu-id="a3ab0-142">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-142">False</span></span>                                        |
| <span data-ttu-id="a3ab0-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a3ab0-143">In Global Catalog</span></span>      | <span data-ttu-id="a3ab0-144">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-144">False</span></span>                                        |
| <span data-ttu-id="a3ab0-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a3ab0-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3ab0-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a3ab0-146">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a3ab0-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3ab0-147">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a3ab0-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3ab0-148">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a3ab0-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3ab0-149">Search-Flags</span></span>           | <span data-ttu-id="a3ab0-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3ab0-150">0x00000000</span></span>                                   |
| <span data-ttu-id="a3ab0-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3ab0-151">System-Flags</span></span>           | <span data-ttu-id="a3ab0-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3ab0-152">0x00000010</span></span>                                   |
| <span data-ttu-id="a3ab0-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a3ab0-153">Classes used in</span></span>        | [<span data-ttu-id="a3ab0-154">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="a3ab0-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a3ab0-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3ab0-155">Windows Server 2003</span></span>



| <span data-ttu-id="a3ab0-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3ab0-156">Entry</span></span> | <span data-ttu-id="a3ab0-157">Wert</span><span class="sxs-lookup"><span data-stu-id="a3ab0-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a3ab0-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a3ab0-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a3ab0-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3ab0-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a3ab0-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3ab0-160">System-Only</span></span>            | <span data-ttu-id="a3ab0-161">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-161">False</span></span>                                        |
| <span data-ttu-id="a3ab0-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a3ab0-162">Is-Single-Valued</span></span>       | <span data-ttu-id="a3ab0-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="a3ab0-163">True</span></span>                                         |
| <span data-ttu-id="a3ab0-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a3ab0-164">Is Indexed</span></span>             | <span data-ttu-id="a3ab0-165">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-165">False</span></span>                                        |
| <span data-ttu-id="a3ab0-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a3ab0-166">In Global Catalog</span></span>      | <span data-ttu-id="a3ab0-167">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-167">False</span></span>                                        |
| <span data-ttu-id="a3ab0-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a3ab0-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3ab0-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a3ab0-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a3ab0-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3ab0-170">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a3ab0-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3ab0-171">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a3ab0-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3ab0-172">Search-Flags</span></span>           | <span data-ttu-id="a3ab0-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3ab0-173">0x00000000</span></span>                                   |
| <span data-ttu-id="a3ab0-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3ab0-174">System-Flags</span></span>           | <span data-ttu-id="a3ab0-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3ab0-175">0x00000010</span></span>                                   |
| <span data-ttu-id="a3ab0-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a3ab0-176">Classes used in</span></span>        | [<span data-ttu-id="a3ab0-177">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="a3ab0-177">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a3ab0-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a3ab0-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a3ab0-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3ab0-179">Entry</span></span> | <span data-ttu-id="a3ab0-180">Wert</span><span class="sxs-lookup"><span data-stu-id="a3ab0-180">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a3ab0-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a3ab0-181">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a3ab0-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3ab0-182">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a3ab0-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3ab0-183">System-Only</span></span>            | <span data-ttu-id="a3ab0-184">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-184">False</span></span>                                        |
| <span data-ttu-id="a3ab0-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a3ab0-185">Is-Single-Valued</span></span>       | <span data-ttu-id="a3ab0-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="a3ab0-186">True</span></span>                                         |
| <span data-ttu-id="a3ab0-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a3ab0-187">Is Indexed</span></span>             | <span data-ttu-id="a3ab0-188">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-188">False</span></span>                                        |
| <span data-ttu-id="a3ab0-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a3ab0-189">In Global Catalog</span></span>      | <span data-ttu-id="a3ab0-190">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-190">False</span></span>                                        |
| <span data-ttu-id="a3ab0-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a3ab0-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3ab0-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a3ab0-192">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a3ab0-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3ab0-193">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a3ab0-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3ab0-194">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a3ab0-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3ab0-195">Search-Flags</span></span>           | <span data-ttu-id="a3ab0-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3ab0-196">0x00000000</span></span>                                   |
| <span data-ttu-id="a3ab0-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3ab0-197">System-Flags</span></span>           | <span data-ttu-id="a3ab0-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3ab0-198">0x00000010</span></span>                                   |
| <span data-ttu-id="a3ab0-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a3ab0-199">Classes used in</span></span>        | [<span data-ttu-id="a3ab0-200">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="a3ab0-200">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a3ab0-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3ab0-201">Windows Server 2008</span></span>



| <span data-ttu-id="a3ab0-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3ab0-202">Entry</span></span> | <span data-ttu-id="a3ab0-203">Wert</span><span class="sxs-lookup"><span data-stu-id="a3ab0-203">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a3ab0-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a3ab0-204">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a3ab0-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3ab0-205">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a3ab0-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3ab0-206">System-Only</span></span>            | <span data-ttu-id="a3ab0-207">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-207">False</span></span>                                        |
| <span data-ttu-id="a3ab0-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a3ab0-208">Is-Single-Valued</span></span>       | <span data-ttu-id="a3ab0-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="a3ab0-209">True</span></span>                                         |
| <span data-ttu-id="a3ab0-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a3ab0-210">Is Indexed</span></span>             | <span data-ttu-id="a3ab0-211">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-211">False</span></span>                                        |
| <span data-ttu-id="a3ab0-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a3ab0-212">In Global Catalog</span></span>      | <span data-ttu-id="a3ab0-213">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-213">False</span></span>                                        |
| <span data-ttu-id="a3ab0-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a3ab0-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3ab0-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a3ab0-215">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a3ab0-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3ab0-216">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a3ab0-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3ab0-217">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a3ab0-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3ab0-218">Search-Flags</span></span>           | <span data-ttu-id="a3ab0-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3ab0-219">0x00000000</span></span>                                   |
| <span data-ttu-id="a3ab0-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3ab0-220">System-Flags</span></span>           | <span data-ttu-id="a3ab0-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3ab0-221">0x00000010</span></span>                                   |
| <span data-ttu-id="a3ab0-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a3ab0-222">Classes used in</span></span>        | [<span data-ttu-id="a3ab0-223">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="a3ab0-223">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a3ab0-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a3ab0-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a3ab0-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3ab0-225">Entry</span></span> | <span data-ttu-id="a3ab0-226">Wert</span><span class="sxs-lookup"><span data-stu-id="a3ab0-226">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a3ab0-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a3ab0-227">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a3ab0-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3ab0-228">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a3ab0-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3ab0-229">System-Only</span></span>            | <span data-ttu-id="a3ab0-230">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-230">False</span></span>                                        |
| <span data-ttu-id="a3ab0-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a3ab0-231">Is-Single-Valued</span></span>       | <span data-ttu-id="a3ab0-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="a3ab0-232">True</span></span>                                         |
| <span data-ttu-id="a3ab0-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a3ab0-233">Is Indexed</span></span>             | <span data-ttu-id="a3ab0-234">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-234">False</span></span>                                        |
| <span data-ttu-id="a3ab0-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a3ab0-235">In Global Catalog</span></span>      | <span data-ttu-id="a3ab0-236">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-236">False</span></span>                                        |
| <span data-ttu-id="a3ab0-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a3ab0-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3ab0-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a3ab0-238">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a3ab0-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3ab0-239">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a3ab0-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3ab0-240">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a3ab0-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3ab0-241">Search-Flags</span></span>           | <span data-ttu-id="a3ab0-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3ab0-242">0x00000000</span></span>                                   |
| <span data-ttu-id="a3ab0-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3ab0-243">System-Flags</span></span>           | <span data-ttu-id="a3ab0-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3ab0-244">0x00000010</span></span>                                   |
| <span data-ttu-id="a3ab0-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a3ab0-245">Classes used in</span></span>        | [<span data-ttu-id="a3ab0-246">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="a3ab0-246">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a3ab0-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3ab0-247">Windows Server 2012</span></span>



| <span data-ttu-id="a3ab0-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3ab0-248">Entry</span></span> | <span data-ttu-id="a3ab0-249">Wert</span><span class="sxs-lookup"><span data-stu-id="a3ab0-249">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a3ab0-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a3ab0-250">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a3ab0-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3ab0-251">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a3ab0-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3ab0-252">System-Only</span></span>            | <span data-ttu-id="a3ab0-253">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-253">False</span></span>                                        |
| <span data-ttu-id="a3ab0-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a3ab0-254">Is-Single-Valued</span></span>       | <span data-ttu-id="a3ab0-255">Richtig</span><span class="sxs-lookup"><span data-stu-id="a3ab0-255">True</span></span>                                         |
| <span data-ttu-id="a3ab0-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a3ab0-256">Is Indexed</span></span>             | <span data-ttu-id="a3ab0-257">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-257">False</span></span>                                        |
| <span data-ttu-id="a3ab0-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a3ab0-258">In Global Catalog</span></span>      | <span data-ttu-id="a3ab0-259">False</span><span class="sxs-lookup"><span data-stu-id="a3ab0-259">False</span></span>                                        |
| <span data-ttu-id="a3ab0-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a3ab0-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3ab0-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a3ab0-261">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a3ab0-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3ab0-262">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a3ab0-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3ab0-263">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a3ab0-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3ab0-264">Search-Flags</span></span>           | <span data-ttu-id="a3ab0-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3ab0-265">0x00000000</span></span>                                   |
| <span data-ttu-id="a3ab0-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3ab0-266">System-Flags</span></span>           | <span data-ttu-id="a3ab0-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3ab0-267">0x00000010</span></span>                                   |
| <span data-ttu-id="a3ab0-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a3ab0-268">Classes used in</span></span>        | [<span data-ttu-id="a3ab0-269">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="a3ab0-269">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





