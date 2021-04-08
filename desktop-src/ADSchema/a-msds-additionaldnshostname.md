---
title: ms-DS-zusätzliches-DNS-Host-Name-Attribut
description: Das-Attribut wird verwendet, um den zusätzlichen DNS-Hostnamen eines Computer Objekts zu speichern. Dieses Attribut wird verwendet, wenn ein DC umbenannt wird.
ms.assetid: ea06f756-d9b6-409d-a008-0e3a1874ad94
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-additional-DNS-Host-Name-Attribut
- AD-Schema für das msDS-additionaldnshostname-Attribut
topic_type:
- apiref
api_name:
- ms-DS-Additional-Dns-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dea3212a19bf743e608f356170adf7a03c06d0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957523"
---
# <a name="ms-ds-additional-dns-host-name-attribute"></a><span data-ttu-id="bf7e3-106">ms-DS-zusätzliches-DNS-Host-Name-Attribut</span><span class="sxs-lookup"><span data-stu-id="bf7e3-106">ms-DS-Additional-Dns-Host-Name attribute</span></span>

<span data-ttu-id="bf7e3-107">Das-Attribut wird verwendet, um den zusätzlichen DNS-Hostnamen eines Computer Objekts zu speichern.</span><span class="sxs-lookup"><span data-stu-id="bf7e3-107">The attribute is used to store the additional DNS host name of a computer object.</span></span> <span data-ttu-id="bf7e3-108">Dieses Attribut wird zum Zeitpunkt der Umbenennung eines Computers verwendet, oder die Namen werden mit "Netdom Computername" verwaltet.</span><span class="sxs-lookup"><span data-stu-id="bf7e3-108">This attribute is used at the time a computer is renamed, or names are managed with "netdom computername".</span></span>



| <span data-ttu-id="bf7e3-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bf7e3-109">Entry</span></span> | <span data-ttu-id="bf7e3-110">Wert</span><span class="sxs-lookup"><span data-stu-id="bf7e3-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="bf7e3-111">CN</span><span class="sxs-lookup"><span data-stu-id="bf7e3-111">CN</span></span>                | <span data-ttu-id="bf7e3-112">ms-DS-Zusatz-DNS-Hostname</span><span class="sxs-lookup"><span data-stu-id="bf7e3-112">ms-DS-Additional-Dns-Host-Name</span></span>                                              |
| <span data-ttu-id="bf7e3-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bf7e3-113">Ldap-Display-Name</span></span> | <span data-ttu-id="bf7e3-114">MSDS-additionaldnshostname</span><span class="sxs-lookup"><span data-stu-id="bf7e3-114">msDS-AdditionalDnsHostName</span></span>                                                  |
| <span data-ttu-id="bf7e3-115">Size</span><span class="sxs-lookup"><span data-stu-id="bf7e3-115">Size</span></span>              | <span data-ttu-id="bf7e3-116">Jeder Wert kann 2048 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="bf7e3-116">Each value can be 2048 characters.</span></span> <span data-ttu-id="bf7e3-117">Die Anzahl von Werten ist das Daten Bank Limit von ungefähr 1200 Werten.</span><span class="sxs-lookup"><span data-stu-id="bf7e3-117">The number of value is the database limit of about 1200 values.</span></span> |
| <span data-ttu-id="bf7e3-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="bf7e3-118">Update Privilege</span></span>  | <span data-ttu-id="bf7e3-119">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bf7e3-119">This value is set by the system.</span></span>                                            |
| <span data-ttu-id="bf7e3-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="bf7e3-120">Update Frequency</span></span>  | <span data-ttu-id="bf7e3-121">Wenn ein Computer umbenannt wird.</span><span class="sxs-lookup"><span data-stu-id="bf7e3-121">When a computer is renamed.</span></span>                                                 |
| <span data-ttu-id="bf7e3-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bf7e3-122">Attribute-Id</span></span>      | <span data-ttu-id="bf7e3-123">1.2.840.113556.1.4.1717</span><span class="sxs-lookup"><span data-stu-id="bf7e3-123">1.2.840.113556.1.4.1717</span></span>                                                     |
| <span data-ttu-id="bf7e3-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bf7e3-124">System-Id-Guid</span></span>    | <span data-ttu-id="bf7e3-125">80863791-dbe9-4eb8-837e-7F 0ab55d9ac7</span><span class="sxs-lookup"><span data-stu-id="bf7e3-125">80863791-dbe9-4eb8-837e-7f0ab55d9ac7</span></span>                                        |
| <span data-ttu-id="bf7e3-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf7e3-126">Syntax</span></span>            | [<span data-ttu-id="bf7e3-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bf7e3-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                 |



## <a name="implementations"></a><span data-ttu-id="bf7e3-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="bf7e3-128">Implementations</span></span>

-   [<span data-ttu-id="bf7e3-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bf7e3-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bf7e3-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bf7e3-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bf7e3-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bf7e3-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bf7e3-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bf7e3-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bf7e3-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bf7e3-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="bf7e3-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bf7e3-134">Windows Server 2003</span></span>



| <span data-ttu-id="bf7e3-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bf7e3-135">Entry</span></span> | <span data-ttu-id="bf7e3-136">Wert</span><span class="sxs-lookup"><span data-stu-id="bf7e3-136">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="bf7e3-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bf7e3-137">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="bf7e3-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf7e3-138">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="bf7e3-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf7e3-139">System-Only</span></span>            | <span data-ttu-id="bf7e3-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="bf7e3-140">True</span></span>                                      |
| <span data-ttu-id="bf7e3-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bf7e3-141">Is-Single-Valued</span></span>       | <span data-ttu-id="bf7e3-142">False</span><span class="sxs-lookup"><span data-stu-id="bf7e3-142">False</span></span>                                     |
| <span data-ttu-id="bf7e3-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bf7e3-143">Is Indexed</span></span>             | <span data-ttu-id="bf7e3-144">False</span><span class="sxs-lookup"><span data-stu-id="bf7e3-144">False</span></span>                                     |
| <span data-ttu-id="bf7e3-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bf7e3-145">In Global Catalog</span></span>      | <span data-ttu-id="bf7e3-146">False</span><span class="sxs-lookup"><span data-stu-id="bf7e3-146">False</span></span>                                     |
| <span data-ttu-id="bf7e3-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf7e3-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf7e3-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bf7e3-148">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="bf7e3-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf7e3-149">Range-Lower</span></span>            | <span data-ttu-id="bf7e3-150">0</span><span class="sxs-lookup"><span data-stu-id="bf7e3-150">0</span></span>                                         |
| <span data-ttu-id="bf7e3-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf7e3-151">Range-Upper</span></span>            | <span data-ttu-id="bf7e3-152">2048</span><span class="sxs-lookup"><span data-stu-id="bf7e3-152">2048</span></span>                                      |
| <span data-ttu-id="bf7e3-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7e3-153">Search-Flags</span></span>           | <span data-ttu-id="bf7e3-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf7e3-154">0x00000000</span></span>                                |
| <span data-ttu-id="bf7e3-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7e3-155">System-Flags</span></span>           | <span data-ttu-id="bf7e3-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf7e3-156">0x00000010</span></span>                                |
| <span data-ttu-id="bf7e3-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bf7e3-157">Classes used in</span></span>        | [<span data-ttu-id="bf7e3-158">**Computer**</span><span class="sxs-lookup"><span data-stu-id="bf7e3-158">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bf7e3-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bf7e3-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bf7e3-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bf7e3-160">Entry</span></span> | <span data-ttu-id="bf7e3-161">Wert</span><span class="sxs-lookup"><span data-stu-id="bf7e3-161">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="bf7e3-162">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bf7e3-162">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="bf7e3-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf7e3-163">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="bf7e3-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf7e3-164">System-Only</span></span>            | <span data-ttu-id="bf7e3-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="bf7e3-165">True</span></span>                                      |
| <span data-ttu-id="bf7e3-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bf7e3-166">Is-Single-Valued</span></span>       | <span data-ttu-id="bf7e3-167">False</span><span class="sxs-lookup"><span data-stu-id="bf7e3-167">False</span></span>                                     |
| <span data-ttu-id="bf7e3-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bf7e3-168">Is Indexed</span></span>             | <span data-ttu-id="bf7e3-169">False</span><span class="sxs-lookup"><span data-stu-id="bf7e3-169">False</span></span>                                     |
| <span data-ttu-id="bf7e3-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bf7e3-170">In Global Catalog</span></span>      | <span data-ttu-id="bf7e3-171">False</span><span class="sxs-lookup"><span data-stu-id="bf7e3-171">False</span></span>                                     |
| <span data-ttu-id="bf7e3-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf7e3-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf7e3-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bf7e3-173">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="bf7e3-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf7e3-174">Range-Lower</span></span>            | <span data-ttu-id="bf7e3-175">0</span><span class="sxs-lookup"><span data-stu-id="bf7e3-175">0</span></span>                                         |
| <span data-ttu-id="bf7e3-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf7e3-176">Range-Upper</span></span>            | <span data-ttu-id="bf7e3-177">2048</span><span class="sxs-lookup"><span data-stu-id="bf7e3-177">2048</span></span>                                      |
| <span data-ttu-id="bf7e3-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7e3-178">Search-Flags</span></span>           | <span data-ttu-id="bf7e3-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf7e3-179">0x00000000</span></span>                                |
| <span data-ttu-id="bf7e3-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7e3-180">System-Flags</span></span>           | <span data-ttu-id="bf7e3-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf7e3-181">0x00000010</span></span>                                |
| <span data-ttu-id="bf7e3-182">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bf7e3-182">Classes used in</span></span>        | [<span data-ttu-id="bf7e3-183">**Computer**</span><span class="sxs-lookup"><span data-stu-id="bf7e3-183">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bf7e3-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf7e3-184">Windows Server 2008</span></span>



| <span data-ttu-id="bf7e3-185">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bf7e3-185">Entry</span></span> | <span data-ttu-id="bf7e3-186">Wert</span><span class="sxs-lookup"><span data-stu-id="bf7e3-186">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="bf7e3-187">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bf7e3-187">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="bf7e3-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf7e3-188">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="bf7e3-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf7e3-189">System-Only</span></span>            | <span data-ttu-id="bf7e3-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="bf7e3-190">True</span></span>                                      |
| <span data-ttu-id="bf7e3-191">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bf7e3-191">Is-Single-Valued</span></span>       | <span data-ttu-id="bf7e3-192">False</span><span class="sxs-lookup"><span data-stu-id="bf7e3-192">False</span></span>                                     |
| <span data-ttu-id="bf7e3-193">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bf7e3-193">Is Indexed</span></span>             | <span data-ttu-id="bf7e3-194">False</span><span class="sxs-lookup"><span data-stu-id="bf7e3-194">False</span></span>                                     |
| <span data-ttu-id="bf7e3-195">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bf7e3-195">In Global Catalog</span></span>      | <span data-ttu-id="bf7e3-196">False</span><span class="sxs-lookup"><span data-stu-id="bf7e3-196">False</span></span>                                     |
| <span data-ttu-id="bf7e3-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf7e3-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf7e3-198">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bf7e3-198">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="bf7e3-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf7e3-199">Range-Lower</span></span>            | <span data-ttu-id="bf7e3-200">0</span><span class="sxs-lookup"><span data-stu-id="bf7e3-200">0</span></span>                                         |
| <span data-ttu-id="bf7e3-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf7e3-201">Range-Upper</span></span>            | <span data-ttu-id="bf7e3-202">2048</span><span class="sxs-lookup"><span data-stu-id="bf7e3-202">2048</span></span>                                      |
| <span data-ttu-id="bf7e3-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7e3-203">Search-Flags</span></span>           | <span data-ttu-id="bf7e3-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf7e3-204">0x00000000</span></span>                                |
| <span data-ttu-id="bf7e3-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7e3-205">System-Flags</span></span>           | <span data-ttu-id="bf7e3-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf7e3-206">0x00000010</span></span>                                |
| <span data-ttu-id="bf7e3-207">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bf7e3-207">Classes used in</span></span>        | [<span data-ttu-id="bf7e3-208">**Computer**</span><span class="sxs-lookup"><span data-stu-id="bf7e3-208">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bf7e3-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bf7e3-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bf7e3-210">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bf7e3-210">Entry</span></span> | <span data-ttu-id="bf7e3-211">Wert</span><span class="sxs-lookup"><span data-stu-id="bf7e3-211">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="bf7e3-212">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bf7e3-212">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="bf7e3-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf7e3-213">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="bf7e3-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf7e3-214">System-Only</span></span>            | <span data-ttu-id="bf7e3-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="bf7e3-215">True</span></span>                                      |
| <span data-ttu-id="bf7e3-216">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bf7e3-216">Is-Single-Valued</span></span>       | <span data-ttu-id="bf7e3-217">False</span><span class="sxs-lookup"><span data-stu-id="bf7e3-217">False</span></span>                                     |
| <span data-ttu-id="bf7e3-218">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bf7e3-218">Is Indexed</span></span>             | <span data-ttu-id="bf7e3-219">False</span><span class="sxs-lookup"><span data-stu-id="bf7e3-219">False</span></span>                                     |
| <span data-ttu-id="bf7e3-220">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bf7e3-220">In Global Catalog</span></span>      | <span data-ttu-id="bf7e3-221">False</span><span class="sxs-lookup"><span data-stu-id="bf7e3-221">False</span></span>                                     |
| <span data-ttu-id="bf7e3-222">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf7e3-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf7e3-223">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bf7e3-223">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="bf7e3-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf7e3-224">Range-Lower</span></span>            | <span data-ttu-id="bf7e3-225">0</span><span class="sxs-lookup"><span data-stu-id="bf7e3-225">0</span></span>                                         |
| <span data-ttu-id="bf7e3-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf7e3-226">Range-Upper</span></span>            | <span data-ttu-id="bf7e3-227">2048</span><span class="sxs-lookup"><span data-stu-id="bf7e3-227">2048</span></span>                                      |
| <span data-ttu-id="bf7e3-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7e3-228">Search-Flags</span></span>           | <span data-ttu-id="bf7e3-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf7e3-229">0x00000000</span></span>                                |
| <span data-ttu-id="bf7e3-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7e3-230">System-Flags</span></span>           | <span data-ttu-id="bf7e3-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf7e3-231">0x00000010</span></span>                                |
| <span data-ttu-id="bf7e3-232">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bf7e3-232">Classes used in</span></span>        | [<span data-ttu-id="bf7e3-233">**Computer**</span><span class="sxs-lookup"><span data-stu-id="bf7e3-233">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bf7e3-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bf7e3-234">Windows Server 2012</span></span>



| <span data-ttu-id="bf7e3-235">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bf7e3-235">Entry</span></span> | <span data-ttu-id="bf7e3-236">Wert</span><span class="sxs-lookup"><span data-stu-id="bf7e3-236">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="bf7e3-237">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bf7e3-237">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="bf7e3-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf7e3-238">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="bf7e3-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf7e3-239">System-Only</span></span>            | <span data-ttu-id="bf7e3-240">Richtig</span><span class="sxs-lookup"><span data-stu-id="bf7e3-240">True</span></span>                                      |
| <span data-ttu-id="bf7e3-241">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bf7e3-241">Is-Single-Valued</span></span>       | <span data-ttu-id="bf7e3-242">False</span><span class="sxs-lookup"><span data-stu-id="bf7e3-242">False</span></span>                                     |
| <span data-ttu-id="bf7e3-243">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bf7e3-243">Is Indexed</span></span>             | <span data-ttu-id="bf7e3-244">False</span><span class="sxs-lookup"><span data-stu-id="bf7e3-244">False</span></span>                                     |
| <span data-ttu-id="bf7e3-245">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bf7e3-245">In Global Catalog</span></span>      | <span data-ttu-id="bf7e3-246">False</span><span class="sxs-lookup"><span data-stu-id="bf7e3-246">False</span></span>                                     |
| <span data-ttu-id="bf7e3-247">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf7e3-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf7e3-248">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bf7e3-248">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="bf7e3-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf7e3-249">Range-Lower</span></span>            | <span data-ttu-id="bf7e3-250">0</span><span class="sxs-lookup"><span data-stu-id="bf7e3-250">0</span></span>                                         |
| <span data-ttu-id="bf7e3-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf7e3-251">Range-Upper</span></span>            | <span data-ttu-id="bf7e3-252">2048</span><span class="sxs-lookup"><span data-stu-id="bf7e3-252">2048</span></span>                                      |
| <span data-ttu-id="bf7e3-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7e3-253">Search-Flags</span></span>           | <span data-ttu-id="bf7e3-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf7e3-254">0x00000000</span></span>                                |
| <span data-ttu-id="bf7e3-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7e3-255">System-Flags</span></span>           | <span data-ttu-id="bf7e3-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf7e3-256">0x00000010</span></span>                                |
| <span data-ttu-id="bf7e3-257">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bf7e3-257">Classes used in</span></span>        | [<span data-ttu-id="bf7e3-258">**Computer**</span><span class="sxs-lookup"><span data-stu-id="bf7e3-258">**Computer**</span></span>](c-computer.md)<br/> |



 

 





