---
title: ms-DS-additional-Sam-Account-Name-Attribut
description: Dieses Attribut wird verwendet, um die SAM-Kontonamen zu speichern, die den DNS-Hostnamen in "ms-DS-additional-DNS-Host-Name" entsprechen.
ms.assetid: eb69e1d4-42b7-42e1-aeae-77188db307ef
ms.tgt_platform: multiple
keywords:
- "\"ms-DS-additional-Sam-Account-Name\"-Attribut AD-Schema"
- AD-Schema für das msDS-additionalsamaccountname-Attribut
topic_type:
- apiref
api_name:
- ms-DS-Additional-Sam-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a437c30e6ddb0e551498480f7589791bce59feaf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344147"
---
# <a name="ms-ds-additional-sam-account-name-attribute"></a><span data-ttu-id="a057c-105">ms-DS-additional-Sam-Account-Name-Attribut</span><span class="sxs-lookup"><span data-stu-id="a057c-105">ms-DS-Additional-Sam-Account-Name attribute</span></span>

<span data-ttu-id="a057c-106">Dieses Attribut wird verwendet, um die SAM-Kontonamen zu speichern, die den DNS-Hostnamen in "ms-DS-additional-DNS-Host-Name" entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a057c-106">This attribute is used to store the SAM account names that correspond to the DNS host names in ms-DS-Additional-Dns-Host-Name.</span></span>



| <span data-ttu-id="a057c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a057c-107">Entry</span></span> | <span data-ttu-id="a057c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="a057c-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a057c-109">CN</span><span class="sxs-lookup"><span data-stu-id="a057c-109">CN</span></span>                | <span data-ttu-id="a057c-110">ms-DS-additional-Sam-Account-Name</span><span class="sxs-lookup"><span data-stu-id="a057c-110">ms-DS-Additional-Sam-Account-Name</span></span>           |
| <span data-ttu-id="a057c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a057c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a057c-112">MSDS-additionalsamaccountname</span><span class="sxs-lookup"><span data-stu-id="a057c-112">msDS-AdditionalSamAccountName</span></span>               |
| <span data-ttu-id="a057c-113">Size</span><span class="sxs-lookup"><span data-stu-id="a057c-113">Size</span></span>              | <span data-ttu-id="a057c-114">Weniger als 20 Bytes.</span><span class="sxs-lookup"><span data-stu-id="a057c-114">Less than 20 bytes.</span></span>                         |
| <span data-ttu-id="a057c-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a057c-115">Update Privilege</span></span>  | <span data-ttu-id="a057c-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a057c-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="a057c-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="a057c-117">Update Frequency</span></span>  | <span data-ttu-id="a057c-118">Wenn der DC umbenannt wird.</span><span class="sxs-lookup"><span data-stu-id="a057c-118">When the DC is renamed.</span></span>                     |
| <span data-ttu-id="a057c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a057c-119">Attribute-Id</span></span>      | <span data-ttu-id="a057c-120">1.2.840.113556.1.4.1718</span><span class="sxs-lookup"><span data-stu-id="a057c-120">1.2.840.113556.1.4.1718</span></span>                     |
| <span data-ttu-id="a057c-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a057c-121">System-Id-Guid</span></span>    | <span data-ttu-id="a057c-122">975571df-a4d5-429A-9F 59-cdc6581d91e6</span><span class="sxs-lookup"><span data-stu-id="a057c-122">975571df-a4d5-429a-9f59-cdc6581d91e6</span></span>        |
| <span data-ttu-id="a057c-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="a057c-123">Syntax</span></span>            | [<span data-ttu-id="a057c-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a057c-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a057c-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="a057c-125">Implementations</span></span>

-   [<span data-ttu-id="a057c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a057c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a057c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a057c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a057c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a057c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a057c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a057c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a057c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a057c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a057c-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a057c-131">Windows Server 2003</span></span>



| <span data-ttu-id="a057c-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a057c-132">Entry</span></span> | <span data-ttu-id="a057c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="a057c-133">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a057c-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a057c-134">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="a057c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a057c-135">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="a057c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a057c-136">System-Only</span></span>            | <span data-ttu-id="a057c-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="a057c-137">True</span></span>                                      |
| <span data-ttu-id="a057c-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a057c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a057c-139">False</span><span class="sxs-lookup"><span data-stu-id="a057c-139">False</span></span>                                     |
| <span data-ttu-id="a057c-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a057c-140">Is Indexed</span></span>             | <span data-ttu-id="a057c-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="a057c-141">True</span></span>                                      |
| <span data-ttu-id="a057c-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a057c-142">In Global Catalog</span></span>      | <span data-ttu-id="a057c-143">False</span><span class="sxs-lookup"><span data-stu-id="a057c-143">False</span></span>                                     |
| <span data-ttu-id="a057c-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a057c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a057c-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a057c-145">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="a057c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a057c-146">Range-Lower</span></span>            | <span data-ttu-id="a057c-147">0</span><span class="sxs-lookup"><span data-stu-id="a057c-147">0</span></span>                                         |
| <span data-ttu-id="a057c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a057c-148">Range-Upper</span></span>            | <span data-ttu-id="a057c-149">256</span><span class="sxs-lookup"><span data-stu-id="a057c-149">256</span></span>                                       |
| <span data-ttu-id="a057c-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a057c-150">Search-Flags</span></span>           | <span data-ttu-id="a057c-151">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="a057c-151">0x0000000D</span></span>                                |
| <span data-ttu-id="a057c-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a057c-152">System-Flags</span></span>           | <span data-ttu-id="a057c-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a057c-153">0x00000010</span></span>                                |
| <span data-ttu-id="a057c-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a057c-154">Classes used in</span></span>        | [<span data-ttu-id="a057c-155">**Computer**</span><span class="sxs-lookup"><span data-stu-id="a057c-155">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a057c-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a057c-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a057c-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a057c-157">Entry</span></span> | <span data-ttu-id="a057c-158">Wert</span><span class="sxs-lookup"><span data-stu-id="a057c-158">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a057c-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a057c-159">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="a057c-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a057c-160">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="a057c-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a057c-161">System-Only</span></span>            | <span data-ttu-id="a057c-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="a057c-162">True</span></span>                                      |
| <span data-ttu-id="a057c-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a057c-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a057c-164">False</span><span class="sxs-lookup"><span data-stu-id="a057c-164">False</span></span>                                     |
| <span data-ttu-id="a057c-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a057c-165">Is Indexed</span></span>             | <span data-ttu-id="a057c-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="a057c-166">True</span></span>                                      |
| <span data-ttu-id="a057c-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a057c-167">In Global Catalog</span></span>      | <span data-ttu-id="a057c-168">False</span><span class="sxs-lookup"><span data-stu-id="a057c-168">False</span></span>                                     |
| <span data-ttu-id="a057c-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a057c-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a057c-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a057c-170">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="a057c-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a057c-171">Range-Lower</span></span>            | <span data-ttu-id="a057c-172">0</span><span class="sxs-lookup"><span data-stu-id="a057c-172">0</span></span>                                         |
| <span data-ttu-id="a057c-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a057c-173">Range-Upper</span></span>            | <span data-ttu-id="a057c-174">256</span><span class="sxs-lookup"><span data-stu-id="a057c-174">256</span></span>                                       |
| <span data-ttu-id="a057c-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a057c-175">Search-Flags</span></span>           | <span data-ttu-id="a057c-176">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="a057c-176">0x0000000D</span></span>                                |
| <span data-ttu-id="a057c-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a057c-177">System-Flags</span></span>           | <span data-ttu-id="a057c-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a057c-178">0x00000010</span></span>                                |
| <span data-ttu-id="a057c-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a057c-179">Classes used in</span></span>        | [<span data-ttu-id="a057c-180">**Computer**</span><span class="sxs-lookup"><span data-stu-id="a057c-180">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a057c-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a057c-181">Windows Server 2008</span></span>



| <span data-ttu-id="a057c-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a057c-182">Entry</span></span> | <span data-ttu-id="a057c-183">Wert</span><span class="sxs-lookup"><span data-stu-id="a057c-183">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a057c-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a057c-184">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="a057c-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a057c-185">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="a057c-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="a057c-186">System-Only</span></span>            | <span data-ttu-id="a057c-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="a057c-187">True</span></span>                                      |
| <span data-ttu-id="a057c-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a057c-188">Is-Single-Valued</span></span>       | <span data-ttu-id="a057c-189">False</span><span class="sxs-lookup"><span data-stu-id="a057c-189">False</span></span>                                     |
| <span data-ttu-id="a057c-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a057c-190">Is Indexed</span></span>             | <span data-ttu-id="a057c-191">Richtig</span><span class="sxs-lookup"><span data-stu-id="a057c-191">True</span></span>                                      |
| <span data-ttu-id="a057c-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a057c-192">In Global Catalog</span></span>      | <span data-ttu-id="a057c-193">False</span><span class="sxs-lookup"><span data-stu-id="a057c-193">False</span></span>                                     |
| <span data-ttu-id="a057c-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a057c-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="a057c-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a057c-195">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="a057c-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a057c-196">Range-Lower</span></span>            | <span data-ttu-id="a057c-197">0</span><span class="sxs-lookup"><span data-stu-id="a057c-197">0</span></span>                                         |
| <span data-ttu-id="a057c-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a057c-198">Range-Upper</span></span>            | <span data-ttu-id="a057c-199">256</span><span class="sxs-lookup"><span data-stu-id="a057c-199">256</span></span>                                       |
| <span data-ttu-id="a057c-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a057c-200">Search-Flags</span></span>           | <span data-ttu-id="a057c-201">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="a057c-201">0x0000000D</span></span>                                |
| <span data-ttu-id="a057c-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a057c-202">System-Flags</span></span>           | <span data-ttu-id="a057c-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a057c-203">0x00000010</span></span>                                |
| <span data-ttu-id="a057c-204">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a057c-204">Classes used in</span></span>        | [<span data-ttu-id="a057c-205">**Computer**</span><span class="sxs-lookup"><span data-stu-id="a057c-205">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a057c-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a057c-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a057c-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a057c-207">Entry</span></span> | <span data-ttu-id="a057c-208">Wert</span><span class="sxs-lookup"><span data-stu-id="a057c-208">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a057c-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a057c-209">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="a057c-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a057c-210">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="a057c-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="a057c-211">System-Only</span></span>            | <span data-ttu-id="a057c-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="a057c-212">True</span></span>                                      |
| <span data-ttu-id="a057c-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a057c-213">Is-Single-Valued</span></span>       | <span data-ttu-id="a057c-214">False</span><span class="sxs-lookup"><span data-stu-id="a057c-214">False</span></span>                                     |
| <span data-ttu-id="a057c-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a057c-215">Is Indexed</span></span>             | <span data-ttu-id="a057c-216">Richtig</span><span class="sxs-lookup"><span data-stu-id="a057c-216">True</span></span>                                      |
| <span data-ttu-id="a057c-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a057c-217">In Global Catalog</span></span>      | <span data-ttu-id="a057c-218">False</span><span class="sxs-lookup"><span data-stu-id="a057c-218">False</span></span>                                     |
| <span data-ttu-id="a057c-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a057c-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="a057c-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a057c-220">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="a057c-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a057c-221">Range-Lower</span></span>            | <span data-ttu-id="a057c-222">0</span><span class="sxs-lookup"><span data-stu-id="a057c-222">0</span></span>                                         |
| <span data-ttu-id="a057c-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a057c-223">Range-Upper</span></span>            | <span data-ttu-id="a057c-224">256</span><span class="sxs-lookup"><span data-stu-id="a057c-224">256</span></span>                                       |
| <span data-ttu-id="a057c-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a057c-225">Search-Flags</span></span>           | <span data-ttu-id="a057c-226">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="a057c-226">0x0000000D</span></span>                                |
| <span data-ttu-id="a057c-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a057c-227">System-Flags</span></span>           | <span data-ttu-id="a057c-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a057c-228">0x00000010</span></span>                                |
| <span data-ttu-id="a057c-229">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a057c-229">Classes used in</span></span>        | [<span data-ttu-id="a057c-230">**Computer**</span><span class="sxs-lookup"><span data-stu-id="a057c-230">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a057c-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a057c-231">Windows Server 2012</span></span>



| <span data-ttu-id="a057c-232">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a057c-232">Entry</span></span> | <span data-ttu-id="a057c-233">Wert</span><span class="sxs-lookup"><span data-stu-id="a057c-233">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a057c-234">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a057c-234">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="a057c-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a057c-235">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="a057c-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="a057c-236">System-Only</span></span>            | <span data-ttu-id="a057c-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="a057c-237">True</span></span>                                      |
| <span data-ttu-id="a057c-238">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a057c-238">Is-Single-Valued</span></span>       | <span data-ttu-id="a057c-239">False</span><span class="sxs-lookup"><span data-stu-id="a057c-239">False</span></span>                                     |
| <span data-ttu-id="a057c-240">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a057c-240">Is Indexed</span></span>             | <span data-ttu-id="a057c-241">Richtig</span><span class="sxs-lookup"><span data-stu-id="a057c-241">True</span></span>                                      |
| <span data-ttu-id="a057c-242">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a057c-242">In Global Catalog</span></span>      | <span data-ttu-id="a057c-243">False</span><span class="sxs-lookup"><span data-stu-id="a057c-243">False</span></span>                                     |
| <span data-ttu-id="a057c-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a057c-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="a057c-245">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a057c-245">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="a057c-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a057c-246">Range-Lower</span></span>            | <span data-ttu-id="a057c-247">0</span><span class="sxs-lookup"><span data-stu-id="a057c-247">0</span></span>                                         |
| <span data-ttu-id="a057c-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a057c-248">Range-Upper</span></span>            | <span data-ttu-id="a057c-249">256</span><span class="sxs-lookup"><span data-stu-id="a057c-249">256</span></span>                                       |
| <span data-ttu-id="a057c-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a057c-250">Search-Flags</span></span>           | <span data-ttu-id="a057c-251">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="a057c-251">0x0000000D</span></span>                                |
| <span data-ttu-id="a057c-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a057c-252">System-Flags</span></span>           | <span data-ttu-id="a057c-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a057c-253">0x00000010</span></span>                                |
| <span data-ttu-id="a057c-254">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a057c-254">Classes used in</span></span>        | [<span data-ttu-id="a057c-255">**Computer**</span><span class="sxs-lookup"><span data-stu-id="a057c-255">**Computer**</span></span>](c-computer.md)<br/> |



 

 





