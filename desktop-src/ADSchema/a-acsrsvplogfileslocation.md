---
title: ACS-RSVP-Log-Files-Location-Attribut
description: Der Dateisystempfad für die Speicherung von RSVP-Protokolldateien.
ms.assetid: c1b3d476-db94-426f-9619-42eec39d1309
ms.tgt_platform: multiple
keywords:
- AD-Schema des ACS-RSVP-Log-Files-location-Attributs
- acsrsvplogfilesloation-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ACS-RSVP-Log-Files-Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b118819456d3f6d6c5a5b449896b1bfe77d788
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344284"
---
# <a name="acs-rsvp-log-files-location-attribute"></a><span data-ttu-id="a2e09-105">ACS-RSVP-Log-Files-Location-Attribut</span><span class="sxs-lookup"><span data-stu-id="a2e09-105">ACS-RSVP-Log-Files-Location attribute</span></span>

<span data-ttu-id="a2e09-106">Der Dateisystempfad für die Speicherung von RSVP-Protokolldateien.</span><span class="sxs-lookup"><span data-stu-id="a2e09-106">The file system path for storage of RSVP log files.</span></span>



| <span data-ttu-id="a2e09-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a2e09-107">Entry</span></span> | <span data-ttu-id="a2e09-108">Wert</span><span class="sxs-lookup"><span data-stu-id="a2e09-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a2e09-109">CN</span><span class="sxs-lookup"><span data-stu-id="a2e09-109">CN</span></span>                | <span data-ttu-id="a2e09-110">ACS-RSVP-Log-Files-Location</span><span class="sxs-lookup"><span data-stu-id="a2e09-110">ACS-RSVP-Log-Files-Location</span></span>                 |
| <span data-ttu-id="a2e09-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a2e09-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a2e09-112">acsrsvplogfileslokation</span><span class="sxs-lookup"><span data-stu-id="a2e09-112">aCSRSVPLogFilesLocation</span></span>                     |
| <span data-ttu-id="a2e09-113">Size</span><span class="sxs-lookup"><span data-stu-id="a2e09-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="a2e09-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a2e09-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="a2e09-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="a2e09-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="a2e09-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a2e09-116">Attribute-Id</span></span>      | <span data-ttu-id="a2e09-117">1.2.840.113556.1.4.773</span><span class="sxs-lookup"><span data-stu-id="a2e09-117">1.2.840.113556.1.4.773</span></span>                      |
| <span data-ttu-id="a2e09-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a2e09-118">System-Id-Guid</span></span>    | <span data-ttu-id="a2e09-119">1cb3559b-56d0-11d1-a9c6-0000b C1</span><span class="sxs-lookup"><span data-stu-id="a2e09-119">1cb3559b-56d0-11d1-a9c6-0000f80367c1</span></span>        |
| <span data-ttu-id="a2e09-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2e09-120">Syntax</span></span>            | [<span data-ttu-id="a2e09-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a2e09-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a2e09-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="a2e09-122">Implementations</span></span>

-   [<span data-ttu-id="a2e09-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a2e09-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a2e09-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a2e09-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a2e09-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a2e09-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a2e09-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a2e09-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a2e09-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a2e09-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a2e09-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a2e09-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a2e09-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a2e09-129">Windows 2000 Server</span></span>



| <span data-ttu-id="a2e09-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a2e09-130">Entry</span></span> | <span data-ttu-id="a2e09-131">Wert</span><span class="sxs-lookup"><span data-stu-id="a2e09-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2e09-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a2e09-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2e09-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2e09-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2e09-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2e09-134">System-Only</span></span>            | <span data-ttu-id="a2e09-135">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-135">False</span></span>                                        |
| <span data-ttu-id="a2e09-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a2e09-136">Is-Single-Valued</span></span>       | <span data-ttu-id="a2e09-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="a2e09-137">True</span></span>                                         |
| <span data-ttu-id="a2e09-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a2e09-138">Is Indexed</span></span>             | <span data-ttu-id="a2e09-139">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-139">False</span></span>                                        |
| <span data-ttu-id="a2e09-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a2e09-140">In Global Catalog</span></span>      | <span data-ttu-id="a2e09-141">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-141">False</span></span>                                        |
| <span data-ttu-id="a2e09-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2e09-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2e09-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a2e09-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2e09-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2e09-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2e09-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2e09-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2e09-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2e09-146">Search-Flags</span></span>           | <span data-ttu-id="a2e09-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2e09-147">0x00000000</span></span>                                   |
| <span data-ttu-id="a2e09-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2e09-148">System-Flags</span></span>           | <span data-ttu-id="a2e09-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2e09-149">0x00000010</span></span>                                   |
| <span data-ttu-id="a2e09-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a2e09-150">Classes used in</span></span>        | [<span data-ttu-id="a2e09-151">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="a2e09-151">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a2e09-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a2e09-152">Windows Server 2003</span></span>



| <span data-ttu-id="a2e09-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a2e09-153">Entry</span></span> | <span data-ttu-id="a2e09-154">Wert</span><span class="sxs-lookup"><span data-stu-id="a2e09-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2e09-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a2e09-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2e09-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2e09-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2e09-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2e09-157">System-Only</span></span>            | <span data-ttu-id="a2e09-158">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-158">False</span></span>                                        |
| <span data-ttu-id="a2e09-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a2e09-159">Is-Single-Valued</span></span>       | <span data-ttu-id="a2e09-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="a2e09-160">True</span></span>                                         |
| <span data-ttu-id="a2e09-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a2e09-161">Is Indexed</span></span>             | <span data-ttu-id="a2e09-162">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-162">False</span></span>                                        |
| <span data-ttu-id="a2e09-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a2e09-163">In Global Catalog</span></span>      | <span data-ttu-id="a2e09-164">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-164">False</span></span>                                        |
| <span data-ttu-id="a2e09-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2e09-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2e09-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a2e09-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2e09-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2e09-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2e09-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2e09-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2e09-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2e09-169">Search-Flags</span></span>           | <span data-ttu-id="a2e09-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2e09-170">0x00000000</span></span>                                   |
| <span data-ttu-id="a2e09-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2e09-171">System-Flags</span></span>           | <span data-ttu-id="a2e09-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2e09-172">0x00000010</span></span>                                   |
| <span data-ttu-id="a2e09-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a2e09-173">Classes used in</span></span>        | [<span data-ttu-id="a2e09-174">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="a2e09-174">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a2e09-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a2e09-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a2e09-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a2e09-176">Entry</span></span> | <span data-ttu-id="a2e09-177">Wert</span><span class="sxs-lookup"><span data-stu-id="a2e09-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2e09-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a2e09-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2e09-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2e09-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2e09-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2e09-180">System-Only</span></span>            | <span data-ttu-id="a2e09-181">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-181">False</span></span>                                        |
| <span data-ttu-id="a2e09-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a2e09-182">Is-Single-Valued</span></span>       | <span data-ttu-id="a2e09-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="a2e09-183">True</span></span>                                         |
| <span data-ttu-id="a2e09-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a2e09-184">Is Indexed</span></span>             | <span data-ttu-id="a2e09-185">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-185">False</span></span>                                        |
| <span data-ttu-id="a2e09-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a2e09-186">In Global Catalog</span></span>      | <span data-ttu-id="a2e09-187">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-187">False</span></span>                                        |
| <span data-ttu-id="a2e09-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2e09-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2e09-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a2e09-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2e09-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2e09-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2e09-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2e09-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2e09-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2e09-192">Search-Flags</span></span>           | <span data-ttu-id="a2e09-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2e09-193">0x00000000</span></span>                                   |
| <span data-ttu-id="a2e09-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2e09-194">System-Flags</span></span>           | <span data-ttu-id="a2e09-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2e09-195">0x00000010</span></span>                                   |
| <span data-ttu-id="a2e09-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a2e09-196">Classes used in</span></span>        | [<span data-ttu-id="a2e09-197">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="a2e09-197">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a2e09-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2e09-198">Windows Server 2008</span></span>



| <span data-ttu-id="a2e09-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a2e09-199">Entry</span></span> | <span data-ttu-id="a2e09-200">Wert</span><span class="sxs-lookup"><span data-stu-id="a2e09-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2e09-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a2e09-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2e09-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2e09-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2e09-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2e09-203">System-Only</span></span>            | <span data-ttu-id="a2e09-204">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-204">False</span></span>                                        |
| <span data-ttu-id="a2e09-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a2e09-205">Is-Single-Valued</span></span>       | <span data-ttu-id="a2e09-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="a2e09-206">True</span></span>                                         |
| <span data-ttu-id="a2e09-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a2e09-207">Is Indexed</span></span>             | <span data-ttu-id="a2e09-208">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-208">False</span></span>                                        |
| <span data-ttu-id="a2e09-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a2e09-209">In Global Catalog</span></span>      | <span data-ttu-id="a2e09-210">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-210">False</span></span>                                        |
| <span data-ttu-id="a2e09-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2e09-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2e09-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a2e09-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2e09-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2e09-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2e09-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2e09-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2e09-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2e09-215">Search-Flags</span></span>           | <span data-ttu-id="a2e09-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2e09-216">0x00000000</span></span>                                   |
| <span data-ttu-id="a2e09-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2e09-217">System-Flags</span></span>           | <span data-ttu-id="a2e09-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2e09-218">0x00000010</span></span>                                   |
| <span data-ttu-id="a2e09-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a2e09-219">Classes used in</span></span>        | [<span data-ttu-id="a2e09-220">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="a2e09-220">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a2e09-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a2e09-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a2e09-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a2e09-222">Entry</span></span> | <span data-ttu-id="a2e09-223">Wert</span><span class="sxs-lookup"><span data-stu-id="a2e09-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2e09-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a2e09-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2e09-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2e09-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2e09-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2e09-226">System-Only</span></span>            | <span data-ttu-id="a2e09-227">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-227">False</span></span>                                        |
| <span data-ttu-id="a2e09-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a2e09-228">Is-Single-Valued</span></span>       | <span data-ttu-id="a2e09-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="a2e09-229">True</span></span>                                         |
| <span data-ttu-id="a2e09-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a2e09-230">Is Indexed</span></span>             | <span data-ttu-id="a2e09-231">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-231">False</span></span>                                        |
| <span data-ttu-id="a2e09-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a2e09-232">In Global Catalog</span></span>      | <span data-ttu-id="a2e09-233">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-233">False</span></span>                                        |
| <span data-ttu-id="a2e09-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2e09-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2e09-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a2e09-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2e09-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2e09-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2e09-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2e09-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2e09-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2e09-238">Search-Flags</span></span>           | <span data-ttu-id="a2e09-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2e09-239">0x00000000</span></span>                                   |
| <span data-ttu-id="a2e09-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2e09-240">System-Flags</span></span>           | <span data-ttu-id="a2e09-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2e09-241">0x00000010</span></span>                                   |
| <span data-ttu-id="a2e09-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a2e09-242">Classes used in</span></span>        | [<span data-ttu-id="a2e09-243">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="a2e09-243">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a2e09-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2e09-244">Windows Server 2012</span></span>



| <span data-ttu-id="a2e09-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a2e09-245">Entry</span></span> | <span data-ttu-id="a2e09-246">Wert</span><span class="sxs-lookup"><span data-stu-id="a2e09-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2e09-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a2e09-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2e09-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2e09-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2e09-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2e09-249">System-Only</span></span>            | <span data-ttu-id="a2e09-250">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-250">False</span></span>                                        |
| <span data-ttu-id="a2e09-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a2e09-251">Is-Single-Valued</span></span>       | <span data-ttu-id="a2e09-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="a2e09-252">True</span></span>                                         |
| <span data-ttu-id="a2e09-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a2e09-253">Is Indexed</span></span>             | <span data-ttu-id="a2e09-254">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-254">False</span></span>                                        |
| <span data-ttu-id="a2e09-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a2e09-255">In Global Catalog</span></span>      | <span data-ttu-id="a2e09-256">False</span><span class="sxs-lookup"><span data-stu-id="a2e09-256">False</span></span>                                        |
| <span data-ttu-id="a2e09-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2e09-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2e09-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a2e09-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2e09-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2e09-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2e09-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2e09-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2e09-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2e09-261">Search-Flags</span></span>           | <span data-ttu-id="a2e09-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2e09-262">0x00000000</span></span>                                   |
| <span data-ttu-id="a2e09-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2e09-263">System-Flags</span></span>           | <span data-ttu-id="a2e09-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2e09-264">0x00000010</span></span>                                   |
| <span data-ttu-id="a2e09-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a2e09-265">Classes used in</span></span>        | [<span data-ttu-id="a2e09-266">**ACS-Subnetz**</span><span class="sxs-lookup"><span data-stu-id="a2e09-266">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





